# ADR-002: DEFDR is a sub-tier cyber flow-down assurance platform for UK defence primes

**Status:** Accepted
**Date:** 2026-09-19
**Decided by:** Orchestrator, on the evidence of six research reports and three focus groups

## Decision

DEFDR is **DEFCON 658 / Def Stan 05-138 Issue 4 sub-tier flow-down assurance, sold to UK prime
contractors and tier-1 suppliers.**

It answers one question a prime cannot answer today: *which of my subcontractors need which Defence
Cyber Certification level, under which contract's Cyber Risk Profile, which of them are
non-compliant, and what is the evidence pack when MOD asks?*

## What we are NOT building

- **Not a supplier passport or register.** JOSCAR owns that word, has 30+ buyers and 6,000+
  suppliers, counts **the MOD itself as a buyer member**, and is **free below £1m turnover**.
- **Not offset management** — see below.
- **Not supply-chain illumination.** Govini Ark and Sayari own it (Govini reportedly ~$150k/seat/yr,
  >$100m ARR; Sayari 1.5bn+ entities).
- **Not inventory data quality.** One buyer, £4.3bn+ already committed (BMfS £2.5bn, FDSS £1.8bn),
  behind a network boundary a Cloudflare-only product cannot reach.

## Why this, on the evidence

**It is the only candidate that passes all six selection criteria.**

| Criterion | Verdict |
|---|---|
| 1. Non-ministry year-one buyer | ✓ the prime |
| 2. Survives without US DoD IL4 | ✓ UK-only, OFFICIAL |
| 3. Not incumbent-locked | ✓ JOSCAR collects declarations; it does not run the chase |
| 4. Data obtainable without JOSCAR/NMCRL/GIDEP | ✓ **customer-supplied** |
| 5. Credible UK buyer count | ✓ 100–200 orgs, 60–120 winnable |
| 6. Survives Focus Group C | ✓ the only one |

**The forcing function is contractual, dated, and already in breach — not aspirational.**

| Instrument | Status | Date |
|---|---|---|
| **Def Stan 05-138 Issue 4 / CSM v4 mandatory on all new *and existing* MOD contracts containing DEFCON 658** | **Contractually binding** | **3 Dec 2025** |
| **ISN 2026/02** — confirms DCC as the recognised evidence pathway, mapped to each contract's Cyber Risk Profile | Binding guidance | 30 Mar 2026 |
| DCC Level 0 requested of all MOD industry partners | A *request*, not a mandate | by 31 Dec 2026 |

DEFCON 658 requires primes to **risk-assess every subcontractor and flow obligations down**. A prime
today has a register (JOSCAR), a standard (Def Stan 05-138 Iss 4), a deadline, and **no workflow
between them**. That gap is the product.

**Commercials.** £25k–£50k per prime. £3m ARR needs 60–120 logos, not five impossible ones. Never
per-seat: the Kahootz anchor (£3.69–£11.69/user/month) would cap us far too low for a
compliance-liability purchase.

## Why NOT offsets, despite two experts ranking it first

Recorded because reversing a two-expert consensus needs its reasoning preserved.

1. **The regime does not exist.** GOV.UK still shows the DIS Offset consultation as *"awaiting
   outcome"* **nine months after it closed** (closed 23 Dec 2025). The National Armaments Director's
   own H1-2026 implementation target **has passed with nothing published.** The Defence Investment
   Plan calls the regime *"subject to consultation."*
2. **The convergence was an artefact, not triangulation.** Both experts cited the *same* evidence
   cluster — Freshfields and Pillsbury client alerts on the same consultation, the same PwC India
   page, the same $371bn/$229bn figures. One evidence cluster read twice.
3. **The UK buyer count is 8–15, winnable 4–6.** Foreign-parented firms (Thales, Leonardo, MBDA)
   decide tooling at group level. £3m ARR would need £500k–750k per logo. Not survivable.
4. **"No incumbent" was read backwards.** Forty years and $142bn of agreements produced no category
   winner. The null hypothesis is that the category **does not support a software company**.
   BIS records **1,304 agreements across 51 countries over 30 years** — ~43/year from the entire US
   industry. That is a guild, not a market.
5. **The direction of travel is against offsets.** The EU Commission holds offsets to violate primary
   EU law; **Poland abolished indirect offsets**; **India signed no new offset contract in five
   years** and omits offsets from draft DAP 2026. The world is moving from offsets to embedded local
   content.
6. **"Back British" obligates *foreign* contractors** whose offset budgets sit in Bethesda and
   Düsseldorf, not Bristol — so it is not even a UK-buyer product.

## Claims struck from our own research

Recorded so nothing downstream inherits them:

- **STRUCK:** "certification body capacity is dozens, not hundreds." IASME, MOD's official
  certification partner, runs **350+ certification bodies**. Level 0 is three controls. *(Found
  independently by Focus Group A and confirmed by C. Research 01 and 02 both relied on this.)*
- **STRUCK:** the N-tier *illumination* thesis. It rested on NDAA §805 (US) and SCRIPTS (US). Under
  UK scope both are irrelevant — and §805's indirect limb **expressly carves out "components"**,
  removing most of its force anyway. *(Resolves CONFLICT 1: both experts lose; the cyber flow-down
  limb is what survives.)*
- **DEMOTED:** DCC Level 0 by 31 Dec 2026 is a **request** from an official, and IASME's own FAQ
  still states DCC is not mandatory. The binding hook is DEFCON 658 / CSM v4, which it rides on.
- **DEMOTED to feature:** the eCFR point-in-time regulatory diff. Genuinely compounding and genuinely
  unoccupied, but the eCFR is US law and has no UK buyer. Keep the cron; do not build a company on it.

## The standing test, adopted permanently

> The test is not "has a minister said it" — it is **"is there a contract clause, with a date, that a
> buyer is already in breach of."**

## Conditions attached to this decision

1. **Never sell it as a passport or a register.** Sell the *chase* and the *evidence pack*.
2. **The 31 Dec 2026 rush is already lost.** Build for the **annual recertification cycle from 2027**,
   which is where recurring revenue lives.
3. **Do not depend on JOSCAR data** (criterion 4). Interoperate only via customer-supplied exports.
4. **Two-sided selling is legally dangerous.** Under the Procurement Act 2023 a buyer must publish a
   conflicts assessment, and where a conflict confers unfair advantage and cannot be mitigated,
   **exclusion is mandatory**. Selling primes an optimisation tool *and* MOD an adjudication tool
   would bar us. Defer any MOD-side product; if ever pursued, it needs separate entity, staff,
   tenant-isolation attestation and no cross-tenant derived product.
5. **Resolve the UK data residency gap before any customer claim** — see ADR-003.
