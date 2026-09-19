# ADR-012: Wave 2 verdict — the shortlist is empty, and why that is structural

**Status:** Accepted
**Date:** 2026-09-19
**Verdict:** **Do not build S1, S2 or S3.** The failure is not bad candidate selection. It is an
arithmetic property of UK-only regulatory-compliance SaaS.

---

## 1. What happened to each candidate

### S1 — Umbrella/agency PAYE liability assurance: **DEAD ON THE STATUTE**

ADR-011 described the mechanism wrongly, and the sceptic caught it by reading the provision rather
than the announcement.

> New ITEPA s.61Y(2): *"Each relevant party … is, **along with the umbrella company**, jointly and
> severally liable to pay any amount payable … **by the umbrella company**."*

PAYE does **not** move to the agency. The umbrella remains the employer and operates PAYE; the
agency acquires *joint and several liability*. And s.61Z(2) makes the end client a relevant party
only where it contracts the umbrella directly or the agency is connected/offshore — HMRC's policy
paper confirms it is **either/or, not both**.

**ADR-011's "decisive" unserved end-client market of 1,500–3,000 buyers does not exist.**

Independently, the buyer found the category already served: Professional Passport's **Fortis**
(verified live) settles PAYE directly to HMRC against the umbrella's own reference — it *controls
the funds*, where our proposal merely *detects* discrepancies. The incumbent has already published
that argument.

### S2 — Heat network authorisation compliance: **DEAD, forcing function mis-scored by 3 points**

- **SI 2025/269 reg.27 confers deemed authorisation** on all existing operators, and it *"remains in
  force after the initial period."* **Nothing is mechanically blocked** — which was the entire basis
  for scoring 5 on the Enforcement Test.
- **Ofgem's enforcement register shows zero heat network cases** eight months in.
- **Ofgem has launched a free digital registration service and commits to free digital data
  reporting from Autumn 2026.** The kill-shot landed.
- Registration is a **one-off**, not a subscription.
- The incumbent already prices the market at **£1,195 one-off / £1,495 per year per organisation** —
  17× below the £25k ACV the arithmetic demanded.

### S3 — Packaging EPR recyclability: **SURVIVES ONLY NOMINALLY**

- The methodology is a **free published decision tree under OGL** — a ~38,000-character explicit
  ruleset. Anyone can reproduce it; a language model reproduces it trivially well inside our
  5–10 year horizon. **Durability fails.**
- *"You do not need to submit evidence of your recyclability assessments"* — the regulator never
  validates, so **no ground truth accumulates** and there is no data moat.
- **Valpak already sells it by name** at three service tiers, including eco-modulation cost
  modelling and what-if design scenarios.
- **94% of obligated producers already buy through a compliance scheme.** If Ecosurety, Beyondly or
  Clarity bundle RAM free with membership, S3 dies outright.

---

## 2. The structural finding — this is the important part

**Every one of the three breached its regulator's own published cost ceiling.**

| Regime | Regulator's modelled ongoing compliance cost | Per firm/year |
|---|---|---|
| Umbrella PAYE (HMRC TIIN) | £21.7m/yr across ~30,400 businesses | **~£714** |
| Heat networks (DESNZ EANDCB) | £10.8m/yr **for the entire GB industry** | — |
| Packaging EPR (DEFRA IA) | £24.0m/yr across 6,971 large producers | **~£1,300–2,400** |
| Martyn's Law standard tier (Home Office) | 4.5 hours/yr | **~£132** |
| FCA material third-party register | £0.04–0.12m/yr across the whole population | **~£70** |

Now set that against the Wave 1 arithmetic: only **46,765 UK businesses have 50+ employees**, and
evidenced five-year penetration is **1–3%**, so **£3m ARR requires an ACV above £50,000**.

> **£50,000 of ACV is 20–70× what UK regulators model the entire compliance task to cost.**

This is not a coincidence across three candidates. It is a general property:

**UK regulators publish cost-benefit analyses that cap per-firm compliance cost in the hundreds to
low thousands of pounds. UK vertical buyer counts are too small to reach meaningful ARR at those
prices. The intersection of (UK-only) × (regulatory compliance) × (viable ARR) is close to empty.**

Two further confirmations from Wave 2:

- **No candidate has a budget-holding role that exists in volume.** Reed: `"labour supply chain"` =
  **0 postings**; `"packaging compliance"` = 5; `"heat network"` = 86 of which ~1 genuine.
- HMRC forecasts its own umbrella-regime Exchequer yield decaying **+£715m → +£255m by 2030-31** —
  the Treasury is forecasting that market **down 64%**.

## 3. The method failure, named

> **"Wave 1 scored press releases, not provisions."** — Wave 2 sceptic

S1's March 2025 *announcement* and its March 2026 *statute* describe different regimes. Wave 1
scored the announcement. This is the same class of error as the defence run's offsets consultation,
in a new disguise: last time the instrument did not exist, this time it existed and said something
different from the coverage of it.

### → LAW 1c, added to the rubric
**Read the operative provision, never the summary.** A forcing function may not be scored above 2
until someone has quoted the section text from legislation.gov.uk. Announcements, policy papers,
law-firm alerts and trade press are *pointers to* a provision, never evidence of its content.

## 4. Where the escape routes are

The binding constraint is the CBA ceiling, so the escape is to **price against something the
regulator has not costed.**

| Route | Assessment |
|---|---|
| **Price against the customer's own money at stake** — recovered revenue, avoided fees, cash leakage | **RECOMMENDED.** A regulator costs *compliance effort*; it does not cap what a buyer will pay to recover their own cash. Uncapped by CBA, and the value scales with the customer rather than with the task. |
| Sell to far fewer, far larger buyers | Weak in the UK — only 8,330 firms have 250+ employees |
| Go international | **Excluded by ADR-010 scope** (UK-only). Worth noting the strongest UK vertical SaaS, Craneware, sells entirely into the US |
| Lower the ARR ambition | Legitimate but changes the brief |

**Note the one Wave 1 candidate that already has this shape:** adult social care **funder income
assurance** scored 30/40 *with a forcing function of 2* — no regulation at all. Its willingness to
pay scored 4 because the buyer pays out of **recovered cash**, the FD signs against their own P&L,
and the sales cycle is **4–12 weeks**. Wave 1 demoted it on a flat £5k ACV assumption; value-based
pricing on recovered cash was never modelled.

## 5. Recommendation

1. **Build none of S1, S2 or S3.**
2. **Retire the "find a binding UK regulation" thesis as the primary search heuristic.** It has now
   produced two dead shortlists. The CBA ceiling explains why, and it will keep producing them.
3. **Re-run selection over the Wave 1 pool with the cash-at-stake lens**, re-pricing candidates on
   value rather than flat ACV — starting with social care funder income assurance and the legal AML
   evidence spine.
4. **Start the HMRC recorder now regardless** (§6) — it is a cron trigger and object storage, it
   costs nothing, and every day not recording is permanently lost.

## 6. The one thing worth doing today, whatever we build

The moat analyst found a genuine compounding asset, and it is time-sensitive:

**HMRC publishes named tax-avoidance promoters and suppliers — 202 current entities, 73 of them
(36%) umbrella or payroll shaped — and then deletes each name after a maximum of 12 months.** The
change notes record *that* a removal happened but **never name the removed company**. Nobody holds
the historical record.

The GOV.UK **Content API JSON is not archived by the Internet Archive at all** (`archived_snapshots:
{}`), unlike the HTML. A daily snapshot builds a record a later entrant cannot buy.

- Daily 06:00 UTC Cron Worker → R2, four unauthenticated OGL GETs against the GOV.UK Content API
- Raw JSON under `dt=YYYY-MM-DD/`, written on sha256 change; manifest daily regardless
- Append-only `entities.jsonl` with `first_seen` / `last_seen` / `removed_on`
- ~130MB/year. Licence: OGL, green.

**Legal packaging constraint (from the moat analysis):** never publish "Umbrella X underpays" —
truth is a defence but no data source proves remittance. Safe framings: republish HMRC's own naming
as a true statement about a public act; report variance on the customer's own data; keep
cross-customer output statistical and unattributed. The constraint is on packaging, not value —
credit reference agencies operate under the same one.
