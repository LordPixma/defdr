# ADR-010: Pivot from defence to a full UK industry opportunity scan

**Status:** Accepted
**Date:** 2026-09-19
**Decided by:** Product owner

## Decision

Abandon the defence sector entirely. Conduct a deep, systematic scan of **all major UK industries**
to find an evidenced gap supporting a unique SaaS product with durable revenue over **5–10 years**.

The defence work is archived under `docs/archive/defence-2026-09/`. It is not deleted: it is the
evidence that the method works, and its research remains valid for its domain.

## Constraints (confirmed by the product owner, 19 Sep 2026)

| Constraint | Decision |
|---|---|
| **Platform** | **Cloudflare only — still a hard constraint.** Becomes a scoring axis: candidates needing on-prem, GPU, or heavy scraping of blocking sites are filtered early. |
| **Buyer type** | **Evidence-led.** No restriction to B2B, B2G or B2C. Ranked purely on gap quality and revenue durability. |
| **Regulatory plays** | **Permitted, but only where the deadline is real.** The Standing Test (LAW 1) applies without exception. |
| **Geography** | UK. |
| **Horizon** | Must plausibly still be a business in 2031–2036. Durability is a scored axis, not an afterthought. |

## Why the defence work still matters

It produced a **method**, now binding on all agents as `docs/method/01-opportunity-scoring-rubric.md`.
That method's value is demonstrated, not theoretical: it killed a candidate that two independent
expert agents had both ranked #1, on the grounds that

- the regime it depended on **did not exist** (consultation still "awaiting outcome" nine months
  after closing, implementation target missed);
- the apparent expert convergence was **one evidence cluster read twice**, not triangulation;
- the "$371bn market" concealed **8–15 actual UK buyers**; and
- forty years without a category winner was evidence the category **cannot support a software
  company**, not evidence of an opening.

Finding that out cost a day of research instead of two years of building. The five laws exist to
reproduce that outcome reliably.

## Team, repurposed

| Original role | Becomes |
|---|---|
| Defence Sector Expert | **Five parallel UK sector analysts** (finance/professional, health/education, built environment/utilities, industrial/logistics/agri, consumer/creative/tech) |
| Procurement Expert | **UK commercial & buying-behaviour analyst** (how UK firms actually buy software, ACV benchmarks) |
| — *(new)* | **UK regulatory forcing-function sweep 2026–2031** — created specifically to serve LAW 1, and the highest-leverage agent in the wave |
| Webscraper | **UK data sources analyst** — deferred to wave 2, once candidate domains are known |
| 3 Focus groups | Retained: Buyer, Operator, Sceptic — applied to the shortlist in wave 2 |
| Technical Architect | Retained, wave 3 |
| Technical PM | Retained, wave 3 |
| Orchestrator | Retained — synthesis, adjudication, and the build |

## Sequence

- **Wave 1 (7 agents, parallel):** five sector sweeps + the regulatory forcing-function sweep +
  the commercial benchmark. Every candidate scored against the rubric so results are comparable
  across sectors rather than seven incompatible essays.
- **Wave 2:** Orchestrator shortlists. Data-sources analyst assesses moat for the shortlist. Three
  focus groups attack it. Sceptic retains veto.
- **Wave 3:** decision ADR, architecture, delivery plan, build, deploy.

## Standing prohibition carried forward

The banned reasoning patterns from the defence run remain banned:
1. Citing market size in place of buyer count.
2. Treating regulatory intent as a forcing function.
3. Treating agreement between sources as triangulation without checking they are independent.
4. Reading "no incumbent" as opportunity without asking why forty years produced no winner.
