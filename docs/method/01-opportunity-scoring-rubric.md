# The DEFDR Method — Opportunity Scoring Rubric v1

**Status:** Binding on every research agent.
**Origin:** Distilled from the September 2026 defence-sector exercise, in which this method killed a
candidate that two independent experts had ranked #1 — before any code was written.

---

## Part A — The five laws

These exist because each one was learned by nearly getting it wrong.

### LAW 1 — The Standing Test
> A forcing function is **"an obligation, with a date, that a buyer is already in breach of."**
> It is **not** "a minister said it", a consultation, a strategy paper, a green paper, or a
> proposed rule.

In the defence run, four instruments were being used as forcing functions. Exactly **one** survived
this test. One was a consultation with no published outcome nine months after closing; one was a
polite request from an official; one was a US proposed rule still unfinalised six years after its
statute. **Apply this test before you get excited, not after.**

Grade every forcing function you cite:
- **BINDING** — in force, dated, enforceable, and someone is already non-compliant. Cite the clause.
- **SCHEDULED** — enacted, with a commencement date in the future. Cite the date and the instrument.
- **PROPOSED** — consultation, draft, or announced intent. **Carries no weight on its own.**
- **ASPIRATIONAL** — strategy, target, ambition. **Zero weight. Do not build on it.**

### LAW 1b — The Enforcement Test
> A dated obligation with **no enforcement history** is a weak forcing function.
> Check the enforcement record, not just the statute.

Added 19 Sep 2026 by the regulatory analyst, on evidence. UK **gender pay gap reporting** is
binding, dated, and applies to thousands of employers — and the EHRC issued **1,886 warning notices
between 2023 and 2025 resulting in zero fines, zero investigations and zero court orders**. A
statute nobody enforces does not make anybody buy software.

Before scoring the forcing-function axis above **3**, you must answer:
- Has the regulator actually penalised anyone? How many, how much, how recently?
- Is there a published enforcement register, or only a threat?
- Does non-compliance block something the business needs (filing, licence, contract, insurance)?
  *A blocked transaction is stronger than a theoretical fine.*

Score **5** only where there is a live enforcement record **or** non-compliance mechanically blocks
the business from operating.

### LAW 1c — Read the provision, never the summary
> A forcing function may not be scored above **2** until someone has **quoted the section text from
> legislation.gov.uk**.

Added 19 Sep 2026. Wave 1 scored an umbrella-PAYE regime from its March 2025 *announcement*; the
March 2026 *statute* turned out to describe something materially different — joint and several
liability, not a transfer of PAYE operation — which erased a claimed market of 1,500–3,000 buyers.

Announcements, policy papers, law-firm alerts and trade press are **pointers to** a provision, never
evidence of its content. This is the defence run's failure in a new disguise: there the instrument
did not exist; here it existed and said something else.

### LAW 2 — Count buyers, never market size
> "£X billion market" is a vanity metric and is **banned** as a justification.

In the defence run a "$371bn market" concealed **8–15 actual UK buyers**. You must name the specific
job title that holds the budget, then count UK organisations plausibly employing that role *at a
scale that justifies software rather than a spreadsheet*. Show your method. Discount for
foreign-parented firms whose tooling decisions sit abroad, and for organisations already served by
an incumbent.

**Threshold:** fewer than ~50 winnable UK buyers requires an explicit ACV justification or the
candidate is rejected. Compute: *what ACV is needed for £3m ARR, and is that credible?*

### LAW 3 — Independent evidence classes
> Two sources agreeing means nothing if they are the same source twice.

In the defence run, two experts "independently" converged — both had read the same three law-firm
client alerts about the same consultation. That is one evidence cluster, not triangulation.

A claim is **triangulated** only when supported by **different kinds** of evidence. Prefer, in order:
1. A **job posting** for the role that would own this (proves the role and the budget exist)
2. A **procurement record / contract award** showing someone paying for this
3. A **competitor's pricing page or reported ARR**
4. A **regulator's enforcement action or published dataset**
5. A trade-body or industry survey with a named sample
6. Analyst/consultancy commentary *(weakest — never sufficient alone)*
7. Law-firm client alerts *(weakest — they cluster around single events)*

**Every candidate must carry at least two DIFFERENT classes from 1–5.**

### LAW 4 — Hunt the incumbent before you fall in love
> "No incumbent" is usually read backwards.

If a real pain has existed for decades and nobody has won, the null hypothesis is that **the
category does not support a software company** — not that nobody noticed. In the defence run, one
candidate died to a single search (JOSCAR — 30+ buyers, 6,000+ suppliers, free below £1m turnover).

You must actively search for incumbents and **name them with pricing where findable**. Include
adjacent generic tools that already absorb the demand (CLM, ERP modules, spreadsheets + a
consultant). State explicitly: *what does a firm do about this today, and what does it cost them?*

### LAW 5 — The sceptic has veto
Nothing reaches the build stage without surviving adversarial review. If it cannot survive a red
team, it will not survive a customer.

---

## Part B — Required output per candidate gap

Every candidate you propose **must** carry all 12 fields. Incomplete candidates are discarded.

| # | Field | Requirement |
|---|---|---|
| 1 | **The gap** | One concrete sentence. What is broken, for whom. |
| 2 | **Pain owner** | Exact job title. Not "the business". |
| 3 | **Budget holder** | Who signs. Which budget (opex line, compliance, IT, ops). |
| 4 | **UK buyer count** | Number + method + winnable subset. Apply LAW 2. |
| 5 | **Forcing function** | Graded BINDING / SCHEDULED / PROPOSED / ASPIRATIONAL per LAW 1, with instrument + date. "None" is an acceptable answer for a purely operational pain. |
| 6 | **Solved today by** | Spreadsheets? Consultants? An incumbent? Nothing? Be specific. |
| 7 | **Named incumbents** | Per LAW 4, with pricing if findable. "None found" only after a real search. |
| 8 | **Willingness to pay** | GBP, with an anchor (a comparable tool's price, or current cost of the manual alternative). |
| 9 | **Data required** | What data does the product need, who holds it, is it customer-supplied or externally sourced, and is it licensable? |
| 10 | **Cloudflare fit** | Can it be built Workers/DO/R2/KV/D1/Queues-only? Flag anything needing on-prem, heavy scraping of blocking sites, GPU, or huge datasets. |
| 11 | **5–10 year durability** | Does this still exist in 2031–2036? **What kills it?** Name the specific thing: AI commoditisation, regulation repealed, incumbent ships it, market consolidates. |
| 12 | **Evidence** | URLs. At least two different evidence classes per LAW 3. |

## Part C — Scoring

Score each candidate 1–5 on each axis. **Any axis scoring 1 is an automatic rejection**, regardless
of total.

| Axis | 1 (reject) | 5 (excellent) |
|---|---|---|
| **Pain intensity** | Mild annoyance | Someone is personally liable / losing real money |
| **Forcing function** | Aspirational or none, in a market that needs one | BINDING, dated, already in breach |
| **Buyer count** | <20 winnable UK buyers | 500+ winnable UK buyers |
| **Willingness to pay** | No evidenced budget | Proven spend on an inferior alternative |

> **WTP heuristic (added 19 Sep 2026, industrial sector analyst):** *price against a regulated cash
> outflow, never against efficiency or risk.* Observed empirically — every candidate scoring 3+ on
> WTP sat on an existing fee line the buyer already pays; every candidate scoring 1–2 rested on a
> time-saving or risk-reduction argument. If your pricing story is "we save you time", expect a 1–2.

> **The regulator's CBA is your ceiling (added 19 Sep 2026, finance analyst).** When a UK regulator
> publishes an impact assessment or cost-benefit analysis for a new obligation, it states the
> expected ongoing compliance cost *across the entire obligated population*. That figure is a
> published upper bound on the category's total software spend, and buyers cite it back at you.
> Example: the FCA's CBA for the material third-party register puts ongoing annual cost across all
> ~1,500-1,800 firms at **£0.04m-£0.12m** — the regulator has capped the category at roughly £70
> per firm per year. **Always find the CBA before scoring willingness to pay.**
| **Incumbency** | Well-funded incumbent owns it | Genuinely unserved, and you know why |
| **Data moat** | Anyone could rebuild it in a week | Compounding, proprietary, or hard-won |
| **Cloudflare fit** | Needs on-prem or a non-Cloudflare dependency | Natural fit, customer-supplied data |
| **Durability to 2031+** | AI or a regulator erases it | Structural, deepens over time |

## Part D — Hard rules

1. **No hallucinated citations.** Verify URLs by fetching. Mark unverifiable as `[UNVERIFIED]`.
2. **Prefer specific numbers to adjectives.**
3. **Report disconfirming evidence.** If you find the reason a candidate fails, that is a *success*,
   not a failure. Say so prominently.
4. **"AI will do this" is a threat, not a feature.** For every candidate ask: *does a general-purpose
   AI assistant erase this product by 2029?* If plausibly yes, score durability 1–2.
5. **Do not propose a candidate you would not personally bet two years on.**
