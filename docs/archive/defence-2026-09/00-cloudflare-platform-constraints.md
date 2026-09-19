# Cloudflare Platform Constraints & Capabilities (Orchestrator research)

**Date:** 2026-09-18
**Author:** Orchestrator
**Purpose:** DEFDR must be hosted and delivered *exclusively* through the Cloudflare ecosystem. This
document establishes what that hard constraint actually permits, and — critically — what it *enables*
as a commercial differentiator when selling to defence buyers.

---

## 1. The headline: Cloudflare is now a credible defence-grade host

| Fact | Evidence | Date |
|---|---|---|
| Cloudflare for Government holds **FedRAMP High** authorization | Cloudflare press release / Trust Hub | Aug 2026 |
| Also holds **GovRAMP Moderate** (state & local) | Cloudflare press release | Aug 2026 |
| Publicly stated intent to pursue **DoD Impact Level 4 (IL4)** | Nextgov/FCW reporting | Aug 2026 |
| Data processed within an **authorized US boundary across 15 metro areas** | Cloudflare press release | Aug 2026 |
| **100+ US government agencies** already use Cloudflare | Cloudflare press release | Aug 2026 |

**So what:** a Cloudflare-only SaaS is not a toy constraint. FedRAMP High is the authorization level
used for high-impact federal data. This is a *sales asset*, not a limitation — it means DEFDR can
credibly claim a path to US federal deployment that most startup SaaS vendors cannot.

**Caveat to manage:** FedRAMP authorization is Cloudflare's, not ours. We inherit *some* controls;
we remain responsible for every control marked "Partial" or "No" in Cloudflare's Customer
Responsibility Matrix. We must never claim DEFDR "is FedRAMP authorized" — only that it is built on
a FedRAMP High authorized platform and is architected for inheritance.

---

## 2. CRITICAL: what is actually inside the FedRAMP High boundary

Cloudflare's Trust Hub lists the in-scope **Developer Platform** services as:

> Cache Reserve, Cloudflare Images, Cloudflare for SaaS, **Durable Objects**, **R2**, Stream,
> **Workers**, **Workers KV**, **Hyperdrive**

**Conspicuously absent: D1, Queues, Vectorize, Workers AI, Workflows, Analytics Engine, Pipelines.**

Cloudflare states: *"We introduce those to our FedRAMP High scope depending on the annual assessment
cycle"* — so absence means "not yet assessed", not "never". But we must architect for today.

### → ARCHITECTURAL DECISION DRIVER #1
**The primary system of record must be Durable Objects with the SQLite storage backend, not D1.**

Durable Objects are in FedRAMP High scope *and* now provide a SQLite-backed transactional store with
strict serializability. That gives us relational semantics inside the authorized boundary. D1 —
despite being the "obvious" choice for a relational app — sits outside it.

This single decision is what makes the difference between "a SaaS that happens to run on Cloudflare"
and "a SaaS with a defensible federal accreditation story". It is also a genuine engineering
trade-off (see §4) and must be made deliberately, not by default.

Anything using Vectorize / Workers AI / Queues must therefore be designed as a **severable
enrichment tier** — valuable, but removable for a high-assurance deployment without breaking the
core product. Tenants must be able to run in a "boundary mode" that disables out-of-scope services.

---

## 3. Data residency & sovereignty

Defence buyers are sovereignty-obsessed. Cloudflare gives us real tools here:

- **D1 jurisdictions**: `eu` and `fedramp` jurisdictions can be set — but **only at database creation
  time**, never retrofitted. (Changelog, 2025-11-05.) Note the tension with §2: D1 offers a
  `fedramp` jurisdiction while not appearing on the Trust Hub in-scope list — **[NEEDS VERIFICATION
  with Cloudflare before any accreditation claim]**.
- **Data Localization Suite**: Geo Key Manager (where private keys live), Customer Metadata Boundary
  (where traffic metadata stays), Regional Services (which datacentres may decrypt traffic).
- **Durable Objects** support location hints/jurisdiction restriction for placement.
- **R2** supports jurisdictional buckets (`eu`, `fedramp`).

### → ARCHITECTURAL DECISION DRIVER #2
**Tenancy must be jurisdiction-bound from day one.** Every tenant is created into a declared
jurisdiction (`eu`, `fedramp`, or default/global) and that binding is immutable. Because D1 and R2
jurisdictions cannot be changed after creation, retrofitting this later would require a full data
migration per tenant. Getting this wrong at schema-design time is the single most expensive
reversible-only-by-migration mistake available to us.

---

## 4. Platform capability inventory (for the Architect)

| Product | Best for | Consistency | Known limits |
|---|---|---|---|
| **Workers** | All compute, request handling | — | CPU ms billed; 10,000 subrequests/invocation default on paid (raisable to 10M via wrangler config, 2026-02-11 changelog) |
| **Durable Objects** | Strongly-consistent per-entity state, coordination, SQLite storage | Strict serializability, transactional | Per-object single-threaded |
| **D1** | Relational data | — | **10 GB max per database** |
| **Workers KV** | Config, routing metadata, cached reads | Eventually consistent | **~1 write/sec per unique key**; 500µs–10ms hot reads |
| **R2** | Documents, datasets, logs, evidence files | Strong per-object | Zero egress fees |
| **Queues** | Deferred/background work | At-least-once delivery | Requires idempotent consumers |
| **Vectorize** | Embeddings, semantic search | — | Paid plan only; GA with expanded index sizes |
| **Workers AI** | Inference, 50+ open models | — | Neuron-based billing; 10k neurons/day free tier |
| **Workflows** | Durable multi-step execution | — | Built on Durable Objects |
| **Analytics Engine** | High-cardinality time-series telemetry | — | Write-heavy, SQL query API |
| **Hyperdrive** | Accelerating external Postgres/MySQL | — | In FedRAMP scope |
| **Pipelines** | Streaming ingestion | — | "tens of thousands of records/sec" |

### Notes that matter for design
- **KV's ~1 write/sec per key** rules it out for any counter, cursor or per-tenant mutable state. Use
  Durable Objects for those. This is a classic Cloudflare footgun.
- **Queues at-least-once** means every consumer must be idempotent. Design keys accordingly.
- **D1's 10 GB ceiling** means any large corpus must be sharded per tenant or held in R2.
- **Workers are not long-running.** Anything resembling a batch job must be a Workflow, a Queue
  consumer, or a Cron Trigger fan-out — never a long request.

---

## 5. Auth, access and delivery

- **Cloudflare Access (Zero Trust)** is in FedRAMP High scope — usable for the admin plane and for
  customer SSO federation (SAML/OIDC to a customer's Entra ID / Okta).
- **Cloudflare for SaaS** (in scope) enables custom hostnames per tenant — useful for
  `<agency>.defdr.app` or a customer's own domain.
- **Workers Static Assets / Pages** for the front end.
- **Turnstile** (in scope) for bot resistance on any public surface.
- **mTLS / API Shield** (in scope) for machine-to-machine integration with primes' systems.

---

## 6. What this rules OUT

- No AWS/GCP/Azure anything. No Supabase, no Vercel, no Postgres RDS, no Auth0, no Stripe-hosted
  infrastructure beyond an API call, no S3, no Redis, no Elasticsearch, no Kafka.
- No long-running containers unless via Cloudflare Containers.
- No Node-native libraries requiring filesystem or native bindings — Workers runtime only
  (`nodejs_compat` covers a useful subset).
- Any dependency must run on workerd. This must be enforced in CI.

---

## 7. Open questions for the Technical Architect

1. Durable Objects + SQLite vs D1: confirm the FedRAMP-scope reasoning and quantify the engineering
   cost of the DO-first approach (query ergonomics, cross-entity joins, reporting/aggregation).
2. How do we do cross-tenant analytical queries if the system of record is sharded into DOs?
   (Likely answer: DO for write path + periodic materialisation to R2/Analytics Engine for read path.)
3. Can Vectorize be made severable cleanly, or do we need a non-Vectorize fallback search path for
   boundary-mode tenants?
4. Verify the D1 `fedramp` jurisdiction vs Trust Hub scope discrepancy before any customer claim.

---

## 8. LATE-BREAKING CONSTRAINT: Workers egress and datacentre IP blocking

**Source:** Webscraper agent, verified live testing (see `03-data-sources.md`).

Cloudflare Workers egress from **datacentre IP ranges**. A cluster of defence-relevant sites
(war.gov, dla.mil, usgs.gov, tenders.gov.au, NSPA, NCIA) return **403 to datacentre IPs** via
Akamai/Cloudflare bot protection.

**This is a direct collision between our hosting mandate and our data strategy.** It must shape
ingestion design rather than be discovered at deploy time.

### Mitigations, in order of preference
1. **Prefer sources that do not block.** Every blocked source has a verified alternate route
   (ScienceBase for USGS, data.gov.au for AusTender). Ingestion must be written against the
   alternates, not the blocked primaries.
2. **Prefer bulk files and official APIs over HTML scraping.** Bulk endpoints are generally served
   from CDNs that do not apply the same bot heuristics.
3. **Design the fetcher for per-source route configuration** so a blocked source can be swapped to
   an alternate without a code change.
4. **Do NOT use residential proxies.** This converts an availability problem into a terms-of-service
   problem, and we are selling to buyers who will audit exactly this. Explicitly out of bounds.

### Licence red lines (verified, non-negotiable)
- **OpenSanctions is CC BY-NC** — the free tier cannot back a commercial SaaS. Use the official
  government primaries instead, which are open-licensed.
- **JOSCAR/Hellios, MOD DSP `/esop`, DIBBS, GIDEP, NMCRL/NSN** — off limits or paid. NSN catalogue
  data being paid-only is the single biggest gap in the open-data stack.
- **UK OFSI consolidated list closed 28 Jan 2026.** Use `sanctionslist.fcdo.gov.uk`; the identifier
  field changed from "OFSI Group ID" to "Unique ID#".
- **SAM.gov Opportunities is ~10 requests/day** on a non-federal key — not viable as a primary feed.

### The compounding-asset insight
Date-versioned regulatory snapshots (eCFR ITAR USML / EAR CCL / Entity List, plus sanctions lists)
have value that is **purely a function of how long we have been recording them**. A competitor
starting later cannot backfill this. It is a cron trigger plus R2 — cheap to start, impossible to
catch up on. Whatever product we choose, **start the daily snapshot on day one.**
