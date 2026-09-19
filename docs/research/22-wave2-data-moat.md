# Wave 2 — Data Sources & Moat Analysis

**Date:** 19 September 2026
**Analyst role:** Data sources & moat
**Method:** binding — `docs/method/01-opportunity-scoring-rubric.md`
**Input:** `docs/decisions/ADR-011-wave-1-synthesis.md`
**Evidence basis:** 46 live HTTP fetches. WebSearch quota exhausted in Wave 1; the GOV.UK Search
API (`/api/search.json`, HTTP 200, OGL) was used as the substitute and is a better instrument for
this purpose — it queries the primary corpus directly rather than a search engine's index of it.

---

## 1. Moat verdict table

| Candidate | Moat strength | Why |
|---|---|---|
| **S1 — Umbrella/agency PAYE assurance** | **REAL** | Two independent compounding assets. (a) HMRC's own named-promoter list **deletes entries after 12 months** under DOTAS — a daily snapshot accumulates a record of named umbrella companies that HMRC itself erases and that has no complete public archive. (b) Cross-customer reconciliation outcomes are customer-supplied, so no licence or egress constraint. Downgraded from STRONG because the Internet Archive holds irregular HTML captures of the list back to at least **2023-06-07**, so partial backfill is possible. |
| **S2 — Heat network authorisation** | **WEAK** | Ofgem's registration runs through a **private digital service**; there is no public register of heat network operators and no published operator-level performance data. Data reporting goes to Ofgem and is not published. Any benchmark must be assembled from your own customers only — proprietary, but small-N and slow. The one public artefact (Energy Ombudsman scheme membership) is fetchable by anyone in eight HTTP requests. |
| **S3 — Packaging EPR / RAM** | **WEAK, trending NONE** | **Disconfirming finding, reported prominently per Part D.3.** The RAM is published in full as an explicit decision tree — a 37,993-character step-by-step ruleset with red/amber/green criteria per material and per recyclability stage. Anyone can reproduce the assessment; a general-purpose AI assistant reproduces it trivially by 2029 (Part D.4 → durability 1–2 on the assessment engine). Compounding further: producers **do not submit** RAM evidence, so the regulator never validates and there is no authoritative ground truth to accumulate. Only the fee-outcome library survives, and it is customer-supplied — where Valpak and Ecosurety already hold more customers. |

**Headline:** only S1 owns a compounding temporal asset of the shape the defence run identified. S3's
apparent moat is an artefact of not having read the methodology; reading it kills the moat.

---

## 2. Per-candidate data map

### S1 — Umbrella / agency PAYE liability assurance

The product must reconcile four artefacts per worker per pay period: the **agency assignment rate**,
the **umbrella payslip**, the **RTI Full Payment Submission**, and evidence that PAYE was actually
**remitted** to HMRC.

| Artefact | Holder | Customer-supplied or external? | Accessible? |
|---|---|---|---|
| Agency assignment rate / contract rate | The agency (our customer) | **Customer-supplied** | Yes — CSV/API from the agency's back-office |
| Umbrella payslip + reconciliation statement | The worker, and the umbrella | **Customer-supplied** (worker consent or agency contract) | Yes |
| RTI FPS | The umbrella, submitted to HMRC | **Third party** — the umbrella | Obtainable only by contractual compulsion, not by API |
| Actual remittance to HMRC | HMRC | **Regulator, not published** | **No public route** |
| Entity resolution for agencies and umbrellas | Companies House | External, licensed | **Yes — tested, 401 without key, free key** |
| Which umbrellas HMRC has named | HMRC | External, published | **Yes — tested, 200, OGL** |

The decisive structural point: **the fourth row does not exist as a data source.** There is no public
or API route to "did this umbrella actually pay HMRC". This is why the product is an *assurance*
product built on reconciliation and inference, not a lookup — and why the cross-customer record is
valuable: it is the only way anyone can approximate the missing row.

Rows 1–3 are all **customer-supplied**, satisfying the rubric's Cloudflare-fit axis (field 10)
cleanly. The two external components are clean too: Companies House requires a free API key over
HTTP Basic and returned **401** unauthenticated on every endpoint tested; HMRC's named-promoter
corpus is OGL content served by the GOV.UK Content API.

One correction to carry forward: the **Employment Agency Standards Inspectorate and the GLAA have
been absorbed into the Fair Work Agency** under the Employment Rights Act 2025. GOV.UK now publishes
*The Fair Work Agency licensing standards for gangmasters* (HTTP 200, dated 2026-04-07). EAS annual
reports on GOV.UK stop in the 2019–20 series. The GLAA's own public register paths returned **404**
across three URL forms and `api.gla.gov.uk` failed CONNECT (**502**). Treat the GLAA register as
**relocated and currently unlocated** — see unverified items.

### S2 — Heat network authorisation compliance

| Artefact | Holder | Supplied or external? | Accessible? |
|---|---|---|---|
| Ofgem registration record | Ofgem, via private digital service | External | **No public register** |
| A09 / data reporting returns | Operator → Ofgem | **Customer-supplied** | Yes from customer; never published |
| Authorisation conditions text | Ofgem, published | External | Yes (HTTP 200) |
| Ombudsman scheme membership | Energy Ombudsman | External, published | **Yes — 3,828 supplier records** |
| Consumer standards / complaint outcomes | Energy Ombudsman | External, partially published | Aggregate only |
| Network performance (heat loss, outage, billing) | Operator | **Customer-supplied** | Yes from customer |

Ofgem's *What happens after registration* page (HTTP 200) confirms the shape: operators register in
a digital service, must notify Ofgem of material changes, and "will be required to provide us with
information and data on an ongoing basis... Data reporting supports monitoring, compliance activity
and the effective regulation of heat networks." Nothing on the page indicates publication. There is
no register endpoint, no CSV, no data-portal dataset for heat network operators.

**The buyer-census finding is the useful one, and it corrects ADR-011.** The Energy Ombudsman
exposes its full membership through eight sitemap files (`sitemaps-12-section-suppliers-1-sitemap-p1`
through `p8`, all HTTP 200) totalling **3,828 unique supplier URLs**. Each supplier page carries an
embedded structured record:

```
data-supplier="{"id":1514923,"status":"Default","sector":"Energy","subCategory":"Heat Network", ...}"
```

A 150-page random sample parsed 102 records: **76 Energy Broker, 17 Heat Network, 5 Green Deal,
4 Energy Supplier**. Scaled across 3,828, that implies roughly **430–640 heat network entities**
already in the Ombudsman scheme — materially above the "290 suppliers registered" figure carried in
ADR-011, and a genuine LAW 3 class-4 evidence source (a regulator-adjacent published dataset) giving
named, findable buyers. The names confirm the buyer shape: `23-25-mortimer-street-rtm-company-ltd`,
`259-city-road-management-co-ltd`, `10-palace-gate-ltd` — building-level RTM and management
companies, not energy majors.

This is excellent **prospecting** data. It is not a moat, because it took eight HTTP requests.

### S3 — Packaging EPR recyclability (RAM)

| Artefact | Holder | Supplied or external? | Accessible? |
|---|---|---|---|
| RAM decision rules | DEFRA/PackUK, published | External | **Yes — fully published, OGL** |
| Packaging component specifications | Producer + packaging manufacturer | **Customer-supplied** | Yes, with supplier chasing |
| Self-assigned RAM rating | Producer | **Customer-supplied** | Yes |
| RAM evidence pack | Producer, retained 7 years | **Customer-supplied** | Yes — **never submitted to regulator** |
| Notice of liability incl. modulation | PackUK → producer via RPD portal | **Customer-supplied** | **Yes — the feedback loop exists** |
| EPR base fee tables | DEFRA, published | External | Yes |
| Register of obligated producers | Environment Agency (NPWD) | External | **Stale — see below** |

**The critical test, answered.** The brief asked whether the RAM methodology is published as a
decision tree. It is, completely. *RAM 2027 materials assessment guidance* (HTTP 200, published
2026-07-01, updated 2026-08-20) is a 37,993-character explicit algorithm:

- **Step 1** — automatic red: integrated EEE/batteries; substances of concern above UK REACH/SVHC/
  POPs/CLP limits; non-EuPIA-compliant inks; >1ppm total PFAS (25ppb in food packaging);
  non-compliant food-contact packaging; restricted single-use formats.
- **Step 2** — material category, with explicit component-separation rules, including the
  **40mm-in-two-dimensions** threshold that decides whether a cap is assessed separately or absorbed
  into predominant material by weight.
- **Step 3** — red/amber/green at each of four stages: collection, sortation, reprocessing,
  application. Green at every stage → green. Green-or-amber at every stage → amber. Red at any stage
  → red. Missing evidence → **red by default**.

The guidance even works the arithmetic for the reader, with a fully worked household-aerosol example
mapping can/cap/valve to reported RAM lines. This is a specification, not a methodology requiring
expertise to apply.

Two further findings compound the problem. First: *"You do not need to submit evidence of your
recyclability assessments, but you must keep the following records for 7 years and provide it to
regulators if they ask for it."* The regulator does not validate, so there is no authoritative
outcome stream to learn from. Second: the **Packaging Producer Public Register** on NPWD (HTTP 200)
offers registration years **2013 to 2024 only** — it is the legacy producer-responsibility register,
not an EPR register, it is an ASP.NET postback form with no API, and its data.gov.uk record
(`packaging-producer-public-register4`, metadata modified 2026-09-18) carries **`license_title: None`**.

**The one genuine positive for S3:** the feedback loop does exist. The *notice of liability* guidance
(HTTP 200, updated 2026-03-23) confirms the notice includes "your disposal fee based on the weight
and type of household packaging you reported and how it was calculated, including any packaging waste
off-set, and **any change in the producers per tonne fee, based on the packaging's environmental
impact (called modulation)**". Producers learn their actual modulated fee, per assessment year, and
PackUK can recalculate. So a component → RAM rating → realised fee library is buildable. It is
customer-supplied and therefore clean. It is simply not defensible, because the incumbents who
already sit in more producers' RPD accounts accumulate it faster.

---

## 3. Tested endpoint table

All fetched live on 19 September 2026 through the agent proxy.

| Source | URL (abbreviated) | Status | Auth | Licence | Verdict |
|---|---|---:|---|---|---|
| Companies House API root | `api.company-information.service.gov.uk/` | **401** | HTTP Basic, free key | CH/OGL, commercial OK | **USE** |
| CH company search | `/search/companies?q=umbrella` | **401** | key | CH/OGL | **USE** |
| CH disqualified officers | `/disqualified-officers/natural/1` | **401** | key | CH/OGL | **USE** |
| CH disqualifications web | `find-and-update.../register-of-disqualifications/A` | 200 | none | OGL | Fallback |
| CH developer specs | `developer-specs.company-information.service.gov.uk/` | 200 | none | OGL | Reference |
| GOV.UK Search API | `www.gov.uk/api/search.json?q=…` | **200** | none | **OGL** | **USE — search substitute** |
| GOV.UK Content API | `www.gov.uk/api/content/<path>` | **200** | none | **OGL** | **USE — primary** |
| HMRC named schemes (parent) | `/publications/named-tax-avoidance-schemes-…` | **200** | none | OGL | **USE — 128 change notes** |
| HMRC current named list | `…/current-list-of-named-tax-avoidance-schemes-…` | **200** | none | OGL | **USE — 202 entities, 343KB** |
| HMRC stop notice list | `…/list-of-tax-avoidance-schemes-subject-to-a-stop-notice` | **200** | none | OGL | **USE — 55 stop notices** |
| HMRC "what we may publish" | `…/information-hmrc-may-publish-…` | **200** | none | OGL | **Source of 12-month rule** |
| RAM 2027 publication | `/publications/assess-packaging-recyclability-…-ram-2027` | 200 | none | OGL | Read — kills S3 moat |
| RAM 2027 materials guidance | `…/ram-2027-materials-assessment-guidance` | **200** | none | OGL | **Full decision tree, 37,993 ch** |
| RAM supplementary guidance | `/guidance/recyclability-assessment-methodology-supplementary-guidance` | 200 | none | OGL | Read |
| EPR notice of liability | `/guidance/…-notice-of-liability` | **200** | none | OGL | Confirms fee feedback loop |
| EPR 2025 base fees | `/publications/…-2025-base-fees` | 200 | none | OGL | Reference |
| Ofgem heat networks hub | `ofgem.gov.uk/low-carbon/heat-networks` | 200 | none | Ofgem/OGL | Reference |
| Ofgem post-registration | `…/what-happens-after-registration` | **200** | none | Ofgem/OGL | **No public register** |
| Ofgem who-should-register | `…/who-should-register` | 200 | none | Ofgem/OGL | Reference |
| Ofgem data portal | `ofgem.gov.uk/news-and-insight/data` | 200 | none | Ofgem/OGL | No heat-network dataset found |
| Energy Ombudsman sitemap index | `energyombudsman.org/sitemap.xml` | **200** | none | **ToS not located** | **Conditional** |
| EO supplier sitemaps p1–p8 | `…-section-suppliers-1-sitemap-p{1..8}.xml` | **200** ×8 | none | ToS not located | **3,828 URLs** |
| EO supplier page (sample) | `/raise-dispute/23-25-mortimer-street-rtm-company-ltd` | **200** | none | ToS not located | **Structured JSON embedded** |
| EO supplier A–Z | `/supplier/suppliers-a-z` | 200 | none | — | JS-rendered, unusable |
| EO JSON/search endpoints | `/api/suppliers`, `…a-z.json` | **404** ×3 | — | — | No API |
| EO heat network portal | `portal.energyombudsman.org/heat-network-suppliers` | 200 | none | — | Sign-in gated |
| NPWD root | `npwd.environment-agency.gov.uk/` | 200 | none | EA copyright | Reference |
| NPWD producer register | `/PublicRegisterProducers.aspx` | **200** | none | **`None`** | **Stale — years to 2024** |
| data.gov.uk CKAN search | `data.gov.uk/api/3/action/package_search` | **200** | none | varies | **USE** |
| data.gov.uk package_show | `…/package_show?id=packaging-producer-public-register4` | 200 | none | **`license_title: None`** | **Red line — see §6** |
| EA public register index | `environment.data.gov.uk/public-register/view/index` | 200 | none | OGL | Reference |
| EA packaging-producer search | `…/view/search-packaging-producers` | **404** | — | — | Does not exist |
| GLAA site root | `gla.gov.uk/` | 200 | none | — | Reference |
| GLAA public register (3 forms) | `/who-we-are/public-register/` etc. | **404** ×3 | — | — | **Not located** |
| GLAA API | `api.gla.gov.uk/` | **502 CONNECT** | — | — | Does not resolve |
| Fair Work Agency gangmaster standards | `/guidance/the-fair-work-agency-licensing-standards-for-gangmasters` | 200 | none | OGL | **EAS/GLAA successor** |
| UK Gov Web Archive (TNA) | `webarchive.nationalarchives.gov.uk/ukgwa/*/…` | **405** | — | OGL | Proxy-blocked — unverified |
| Wayback availability API | `archive.org/wayback/available?url=…` | **200** | none | IA ToS | **Backfill risk — see §4** |
| Wayback CDX API | `web.archive.org/cdx/search/cdx` | **403** | — | — | Blocked by egress policy |

---

## 4. The S1 legal-shareability analysis

The brief flags this as the key question: if we cannot act on or share the signal that "umbrella X
underpays", the S1 moat is dead. The answer is that **we must never make that statement, and we do
not need to.**

### The risk if framed naively

A cross-customer ledger asserting "Umbrella X underpays PAYE" is a statement of fact about an
identified trading company. Under the Defamation Act 2013 s.1(2) a body trading for profit must show
serious financial loss — a surmountable bar for an umbrella whose business is agency referrals.
Truth (s.2) is a defence, but the burden sits on us, and our evidence is *reconciliation variance*,
not proof of non-remittance. As established in §2, **there is no data source that proves
remittance**, so we could not discharge that burden. Honest opinion (s.3) is weakened by stating it
as fact. Malicious falsehood adds exposure. Competition-law risk is secondary but real: a vendor-run
list that agencies collectively use to exclude umbrellas edges toward a collective boycott under
Chapter I CA98 if it hardens into coordinated refusal to deal rather than independent decisions.

### Why the risk is avoidable, and the moat survives

Three framings carry the commercial value without the liability.

**1. Republish the regulator, do not accuse.** HMRC already names umbrella companies. The *Current
list of named tax avoidance schemes, promoters, enablers and suppliers* (HTTP 200, updated
2026-09-10) contains **202 named entities, of which 73 (36%) carry umbrella/payroll-shaped names** —
`Accent Umbrella Ltd`, `AIT Umbrella Limited`, `Century Umbrella Limited`, `Cube Umbrella Limited`,
`Edge Umbrella Limited`, `1st Choice Umbrella Ltd`, `Aura PAYE Limited`, `Evolve Payroll Ltd`,
`Fast Payroll UK Ltd`. A separate list carries **55 stop notices**. HMRC publishes these under
Finance Act 2022, POTAS, DOTAS and the Enablers regime. Saying *"HMRC named this company on
10 September 2026"* is a true statement about a public act of a public body, published under OGL.
That is not defamation; it is citation.

**2. Report the variance, not the verdict.** To our own customer, about their own supply chain, we
report what we measured: *"On 412 of 900 reconciliations this quarter, the umbrella's payslip
deduction did not match the FPS value."* That is a factual account of our customer's own data,
delivered to the party carrying the Finance Act 2026 c.11 s.24 liability. It is not published to
the world, it names no conclusion about the umbrella's conduct, and it is exactly what the buyer
needs in order to act.

**3. Keep the cross-customer layer statistical and unattributed.** *"Umbrellas in the bottom decile
of reconciliation match rate"* as a benchmark, with the customer's own suppliers highlighted only in
their own instance, converts the cross-customer asset into a private signal. The customer draws the
conclusion; we supply the measurement.

**Verdict: the S1 signal is legally actionable and commercially deliverable, provided it is sold as
measurement of the customer's own liability rather than as a public blacklist.** The moat is not
dead. It is constrained in its packaging, not in its value — and the constraint is the same one
every credit-reference and KYC vendor operates under.

---

## 5. The "start recording today" recommendation

**Begin a daily snapshot of the HMRC named tax avoidance schemes corpus.** This is a cron trigger
plus object storage. It is not a product, it costs pennies, and every day of delay is a day of the
asset permanently lost.

### Why it compounds and cannot be backfilled

From HMRC's own *Information HMRC may publish* page (HTTP 200), section 4:

> "Under DOTAS, there is no time limit for how long information published can remain on the list,
> where the scheme has been notified to HMRC by a promoter or other person. **Where a SRN has been
> allocated to the scheme by HMRC without notification by the promoter or other persons, information
> about the promoter/other persons will be held on GOV.UK for a maximum of 12 months. HMRC will
> remove the names of the promoters/other persons** in accordance with DOTAS legislative
> requirements, as well as details of the schemes published under these provisions."

HMRC deletes names. The parent page's `change_history` (128 dated notes back to 2022-04-06 "First
published") confirms removals are routine and records *that* a removal occurred and the original
publication date — for example, *"The details of 2 promoters of tax avoidance schemes first published
on 28 June 2023 have been removed from the list"* — but **it does not name the removed company.**
The name is recoverable only by whoever was recording.

This is precisely the defence run's temporal-asset shape: value is a pure function of how long you
have been recording.

**Red-team, reported honestly:** the Internet Archive holds HTML captures of this page back to at
least **2023-06-07** (availability API, HTTP 200), so a 2029 entrant could partially reconstruct it.
Three things preserve the advantage. Wayback captures are opportunistic and irregular, so exact
first-seen/last-seen dates are unobtainable from them. The **GOV.UK Content API JSON for this page is
not archived at all** (availability API returned `"archived_snapshots": {}`), so the structured form
— clean entity headings, `public_updated_at`, `first_published_at`, the full change history — exists
nowhere but in our snapshots. And the CDX API was **403 blocked by egress policy** here, so true
capture density is unverified. Net: **REAL, not STRONG.** Start today anyway; the cost is negligible
and the downside is zero.

### Exact specification

**Endpoints — four GETs, no auth, OGL:**

```
https://www.gov.uk/api/content/government/publications/named-tax-avoidance-schemes-promoters-enablers-and-suppliers
https://www.gov.uk/api/content/government/publications/named-tax-avoidance-schemes-promoters-enablers-and-suppliers/current-list-of-named-tax-avoidance-schemes-promoters-enablers-and-suppliers
https://www.gov.uk/api/content/government/publications/named-tax-avoidance-schemes-promoters-enablers-and-suppliers/list-of-tax-avoidance-schemes-subject-to-a-stop-notice
https://www.gov.uk/api/content/government/publications/named-tax-avoidance-schemes-promoters-enablers-and-suppliers/information-hmrc-may-publish-about-tax-avoidance-schemes-promoters-enablers-and-suppliers
```

**Cadence:** daily, 06:00 UTC, Cloudflare Workers Cron Trigger. HMRC updates roughly weekly
(observed: 10 Sep, 13 Aug, 6 Aug, 30 Jul, 9 Jul 2026) but daily costs nothing and removes the risk
of straddling an update-and-removal in one interval.

**Storage shape — R2, content-addressed with a derived ledger:**

```
r2://defdr-temporal/hmrc-named/raw/dt=YYYY-MM-DD/{parent,current-list,stop-notices,info}.json
r2://defdr-temporal/hmrc-named/raw/dt=YYYY-MM-DD/manifest.json   # sha256, bytes, http_status, fetched_at
r2://defdr-temporal/hmrc-named/derived/entities.jsonl            # append-only ledger
```

Ledger record:

```json
{"entity_name":"Accent Umbrella Ltd","normalised":"accent umbrella ltd",
 "ch_number":null,"addresses":[],"regime":"DOTAS|POTAS|Enablers|FA2022",
 "scheme_refs":[],"first_seen":"2026-09-19","last_seen":"2026-09-19",
 "removed_on":null,"source":"current-list","snapshot_sha256":"…"}
```

Write raw only when the sha256 changes; write a manifest every day regardless, so absence of change
is itself recorded. At ~350KB/day uncompressed the full corpus is **under 130MB/year** — the storage
cost is rounding error.

**Day-one enrichment (cheap, do it once then incrementally):** resolve each of the 202 entity names
against the Companies House API (`/search/companies`, free key) and store the company number,
incorporation date and status. That converts a list of strings into a linkable entity graph and
makes the ledger joinable to insolvency and disqualification events later.

### Second, smaller recorder — start it too

**Energy Ombudsman supplier register**, because it is nine HTTP requests and captures the arrival
curve of heat network operators into the compliance regime ahead of the **26 January 2027** Ofgem
registration deadline. Nobody is recording this, and the curve itself — who joined when, who left —
is the only longitudinal view of heat-network regime adoption that will exist.

```
https://www.energyombudsman.org/sitemap.xml
https://www.energyombudsman.org/sitemaps-12-section-suppliers-1-sitemap-p{1..8}.xml
```

**Cadence:** daily for the sitemaps (8 requests). Fetch full supplier pages only for URLs new since
yesterday, parsing the embedded `data-supplier` JSON for `id`, `sector`, `subCategory`.

```
r2://defdr-temporal/energy-ombudsman/dt=YYYY-MM-DD/supplier-urls.txt
r2://defdr-temporal/energy-ombudsman/derived/suppliers.jsonl
   {"eo_id":1514923,"slug":"…","sub_category":"Heat Network","first_seen":"…","last_seen":"…"}
```

Baseline already captured today: **3,828 supplier URLs**, ~430–640 of them heat networks.

**Third, near-free:** poll `change_history` on the RAM and EPR fee pages weekly. It is already inside
the Content API responses we fetch, costs one request each, and dates every methodology revision —
useful for S3 diligence even though S3's moat is weak.

---

## 6. Licence red lines

Applying the OpenSanctions CC BY-NC precedent from the previous exercise.

| Dataset | Finding | Verdict |
|---|---|---|
| **data.gov.uk "Packaging Producer Public Register"** | `license_title: None`, `license_id: None`, `license_url: None`. Notes carry only *"© Environment Agency copyright and/or database right 2019. All rights reserved."* — an explicit all-rights-reserved assertion with **no OGL grant** | **RED LINE.** Do not redistribute. Reference by link only, or seek written EA permission. Moot in practice: data stops at 2024 |
| **NPWD producer register (scraped)** | ASP.NET postback form, no API, no robots/ToS grant located, same EA copyright assertion | **RED LINE for automated bulk extraction.** Do not scrape |
| **Energy Ombudsman supplier register** | Sitemaps and pages return 200 with no auth; **no ToS or robots grant located in this session**. Private body, not OGL | **AMBER.** Safe for internal prospecting and for counts. **Do not republish the list as a product feature** without checking ToS and, ideally, asking. Treat as internal research input only |
| **Companies House API** | Free key, Basic auth, OGL-based terms, commercial use permitted; rate limit **600 requests / 5 minutes** per key (per published spec — see unverified) | **GREEN**, observe rate limit |
| **GOV.UK Content & Search APIs** | OGL, no auth, no registration | **GREEN** — the backbone of the recommendation |
| **Ofgem published guidance** | OGL | **GREEN** |
| **Internet Archive** | CDX **403 blocked by egress policy** here; IA terms restrict bulk automated access | **AMBER.** Do not build a backfill dependency on it |

Nothing in the recommended daily recorder touches a red or amber source. The HMRC corpus is OGL
throughout. That is a deliberate design choice, not a coincidence.

---

## 7. Unverified items

Marked per Part D.1. None of these change the verdicts; all should be closed before a build decision.

- **`[UNVERIFIED]` Internet Archive capture density** for the HMRC named list. The CDX API returned
  **403 (blocked by egress policy)**; only the `availability` API was reachable. The 2023-06-07
  snapshot is confirmed; the *frequency* of captures is not. If captures turn out to be near-daily,
  S1's public-record moat weakens from REAL toward WEAK — though the customer-supplied
  reconciliation moat is untouched either way. **Close this first.**
- **`[UNVERIFIED]` UK Government Web Archive coverage.** `webarchive.nationalarchives.gov.uk`
  returned 200 at root but **405** on every `/ukgwa/` path through this proxy (a known proxy
  plain-HTTP artefact per `/root/.ccr/README.md`). TNA may hold its own captures of GOV.UK.
- **`[UNVERIFIED]` GLAA licence register location.** Three URL forms returned **404**; `api.gla.gov.uk`
  failed CONNECT (**502**). The register very likely still exists under the Fair Work Agency.
- **`[UNVERIFIED]` EAS prohibition orders as a public list.** GOV.UK Search surfaced EAS annual
  reports only to 2019–20 and no prohibited-persons publication. May have moved to the Fair Work
  Agency or may not be published at all.
- **`[UNVERIFIED]` Any public list of registered umbrella companies.** None found. HMRC's named list
  is a list of *non-compliant* entities, not a register of legitimate ones. Accreditation bodies
  (FCSA, Professional Passport) hold the nearest thing, privately.
- **`[UNVERIFIED]` Companies House rate limit of 600/5min** — taken from published spec, not measured,
  since every call returned 401 unauthenticated.
- **`[UNVERIFIED]` Energy Ombudsman ToS.** Not located. The 430–640 heat-network estimate is a
  **sample-based extrapolation** (17 of 102 parsed records in a 150-URL random sample), not a census.
  48 of 150 pages yielded no `data-supplier` blob.
- **`[UNVERIFIED]` Whether Ofgem will publish a heat networks register.** No public register exists
  as at today. Ofgem may publish one after the 26 January 2027 deadline; nothing found says so.
- **`[UNVERIFIED]` Whether PackUK discloses modulation at component granularity.** The notice of
  liability confirms modulation is disclosed; whether the breakdown is per material stream or per
  component is not stated in the guidance and materially affects S3's fee-outcome library.
