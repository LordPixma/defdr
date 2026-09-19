# ADR-011: Wave 1 synthesis — the arithmetic filter and the shortlist

**Status:** Accepted (shortlist), pending Wave 2 adversarial review
**Date:** 2026-09-19
**Inputs:** 7 reports, ~49,000 words, ~60 scored candidates

---

## 1. The finding that reorders everything

The commercial analyst's feasibility matrix is the most consequential output of Wave 1, because it
is arithmetic rather than judgement.

**UK denominator (DBT Business Population Estimates 2025, extracted from source tables):**

| Population | Count |
|---|---|
| UK private-sector businesses | 5,690,265 |
| ...with **any** employee | **1,417,730** |
| ...with 50+ employees | **46,765** |
| ...with 250+ employees | **8,330** |
| Largest single SIC section with 50+ employees | 5,965 |

**Customers needed for £3m ARR:**

| ACV | Customers needed |
|---:|---:|
| £1,000 | 3,000 |
| £5,000 | 600 |
| £10,000 | 300 |
| £25,000 | 120 |
| £50,000 | 60 |
| £100,000 | 30 |

**Evidenced penetration:** 1–3% over five years is the base case. **Ideagen — the UK's strongest
recent vertical SaaS — holds 3.2% of its own serviceable market** at ~£200m ARR after 11 years and
30+ acquisitions. Craneware needed 26 years.

### → CONCLUSION: at realistic penetration, only ACVs of £50,000+ reach £3m ARR from a single
### UK vertical of 50+ employee firms.

This kills more candidates than every other finding combined, and it is not negotiable by optimism.

### The churn corollary
**47.7% of every UK software-publishing company ever incorporated (SIC 58290) is dissolved** —
18,606 dissolved vs 20,320 active. The mechanism is churn: at sub-$10/month ARPA, median annual
logo retention is ~48%. A 3,000-customer base at £1,000 ACV must be half-rebuilt every year on a
CAC that permits no human contact. **Every low-ACV survivor buys lock-in structurally** — BrightHR
sells 36-month contracts; Birdie makes implementation mandatory above 300 care recipients; Civica
charges **25% more** for 30-day notice than for a 3-year term.

**Rule adopted: we do not build a sub-£10k ACV product.**

### The expansion corollary
Winners live on expansion, not new logos. **Craneware took only 2% of new sales value from new
hospitals in FY25** — the rest was expansion within an installed base built over 26 years.

**Rule adopted: the product must have a natural expansion axis** (per site, per unit, per worker,
per SKU) so that revenue grows without a proportional increase in logos won.

---

## 2. Candidates eliminated by arithmetic

Required penetration is computed against each analyst's own **winnable** subset — already a
filtered figure, so anything needing >15% of it is treated as implausible.

| Candidate | Score | Winnable | ACV | Customers needed | % of winnable | Verdict |
|---|---:|---|---:|---:|---:|---|
| BNG 30-year ledger | 31 | 250–450 | £10k | 300 | **67–120%** | **DEAD — arithmetic** |
| Social care income assurance | 30 | 2,500–4,000 | £5k | 600 | 15–24% | Marginal — survives only on value-based pricing |
| Holiday pay evidence vault | 27 | 3,000–6,000 | ~£2k | 1,500 | 25–50% | **DEAD — arithmetic + churn** |
| Martyn's Law (standard tier) | 27 | 178,891 obligated | ~£500 | 6,000 | — | **DEAD — sub-£10k rule.** Addressable is ~24,000, not 178,891 |
| FCA material third-party register | 26 | 1,500–1,800 | — | — | — | **DEAD — regulator's CBA caps the whole category at £0.04–0.12m/yr** |
| UK CBAM | 28 | 500–800 | £4–12k | 300 | 38–60% | **DEAD standalone** — a module, not a company |
| DRS producer onboarding | 26 | ~1,200 | — | — | — | Deferred — deposit level still unpublished |

## 3. Candidates eliminated by incumbency (LAW 4)

| Candidate | Killed by |
|---|---|
| Building Safety Act golden thread | Zutec acquired Operance to consolidate; RiskBase £1/unit/month |
| Awaab's Law clock | Plentific, Switchee (130+ providers), NEC, Civica, MRI, Aareon + HazardClock |
| O-licence compliance | **DVSA's own list names 73 validated vendors** |
| Manufacturing QMS/CAPA | Ideagen (18,500+ orgs); Qualsys now redirects to ideagen.com |
| Customs/BTOM | 80+ HMRC-listed CDS developers |
| Duty-holder prequalification | Constructionline / CHAS — the JOSCAR pattern |

## 4. Candidates eliminated by durability (the 5–10 year test)

| Candidate | Pain | Forcing | Killed by |
|---|---|---|---|
| Sponsor licence payroll assurance | **5** | **5** | **Durability 2.** Care visa route closed Jul 2025; sponsored recruitment 105,000 → ~30,000. Peak pain now, structural decay after. |
| UK ETS energy-from-waste MRV | — | — | DESNZ delayed it 26 Aug 2026, no replacement date |
| IFA ongoing-advice evidencing | — | — | FCA found **no systemic issue** and is consulting on **dropping** the requirement |
| EHCP timeliness | 5 | 5 | **46.4% compliance on a statutory duty — and no buyer.** Breach is not a market unless the breaching party has budget *and* motive |

---

## 5. The shortlist

Three survive both the arithmetic and the qualitative filters.

### S1 — Umbrella / agency labour PAYE liability assurance
**Found independently by two sector analysts, from opposite sides of the same transaction.**

- **Forcing function: BINDING, 6 April 2026.** The *agency*, not the umbrella, now operates PAYE,
  and HMRC "can recover any underpayment of PAYE from them" (Finance Act 2026 c.11 s.24).
- **Pain 5.** This is joint liability for another party's tax — the strongest commercial pain class.
- **Population:** ~30,000 agencies, ~400 umbrellas, ~700,000 workers (HMRC impact note). Agency-side
  winnable 2,500–4,000; end-client side 1,500–3,000.
- **Expansion axis: per worker.** 700,000 workers is the strongest expansion denominator found.
- **Moat:** a cross-customer record of which umbrellas actually remit correctly. Compounding, and a
  later entrant cannot backfill it — the same shape as the defence run's temporal-moat insight.
- **Incumbency:** SafeRec does forensic payslip audit; its own due-diligence page does not mention
  the April 2026 shift. Nothing reconciles agency rate → umbrella payslip → RTI → HMRC remittance.
- **Convergence check (LAW 3):** PASSES. The two analysts identified *different buyers* (agency vs
  end-client) and *different populations* from the same statute. This is structurally independent
  analysis, not the same source read twice. **But both rest on one instrument — Wave 2 must verify
  a buyer with budget exists, not merely that the liability exists.**

### S2 — Heat network authorisation compliance (highest single score, 33/40)
- **Forcing function: BINDING since 27 Jan 2026; registration deadline 26 Jan 2027.** Scores 5 on
  the Enforcement Test because **authorisation is a licence to operate** — non-compliance
  mechanically blocks the business, which beats any theoretical fine.
- **Already in breach:** on day one of regulation, **290 suppliers registered against ~14,000 sites**.
- **Buyer concentration:** Ofgem puts **66% of networks in social landlord ownership** — 1,581
  registered providers is a finite, findable list.
- **Incumbency 4:** incumbents own *billing* (Insite ~38,000 residents, Switch2, Evinox), not
  compliance. The only compliance tooling found is a 46-template Word generator.
- **Arithmetic risk:** winnable 600–900 at £4–25k requires 13–20% penetration. **Only works if ACV
  reaches £25k+ via per-network pricing to multi-network landlords.** This is the key Wave 2 test.

### S3 — Packaging EPR recyclability (RAM) assessment & fee modulation
- **Forcing function: BINDING.** Producers self-assign red/amber/green under RAM v1.1; PackUK
  modulation multiplies fees **1.2× (2026-27) → 1.6× → 2.0× (2028-29)**.
- **Best WTP ratio found.** Base fees are per-tonne cash: plastic £423, fibre composite £461,
  aluminium £266, glass £192. A 5,000t plastic producer faces **~£2.1m rising to ~£4.2m**. A £50k
  ACV is ~1–2% of the fee line it protects — this satisfies the "price against a regulated cash
  outflow" heuristic better than anything else found.
- **Arithmetic:** winnable 1,800–2,500 at £50k needs 60 customers = **2.4–3.3% penetration**, the
  only shortlisted candidate matching the evidenced base case without strain.
- **Expansion axis:** per SKU / per component.
- **Weakness — incumbency 2.** **Valpak already names RAM as a service** and runs Data Insights;
  Ecosurety has 500+ brands. This is the axis Wave 2 must attack hardest.

---

## 6. Corrections to the record

| Claim | Correction |
|---|---|
| "Employment Rights Act 2026" | **No such instrument.** It is the Employment Rights Act **2025** (c. 36) |
| Day-one unfair dismissal | **Legislated away.** Lords amendment substituted a **six-month qualifying period**, effective 1 Jan 2027 |
| Martyn's Law = "largest obligated population" | Arithmetically true (178,891), commercially misleading — **addressable ~24,000** |
| UK law firms ~10,000 | **8,923** |
| "40,000 accountancy practices" | `[UNVERIFIED]` — could not be confirmed |
| Commercial MEES EPC C by 2027 | **Does not exist** — dropped 18 Jun 2026 |
| Gender pay gap enforcement | **1,886 warning notices 2023–25 → zero fines, zero investigations** |

## 7. Research-quality caveat (must carry into Wave 2)

The session-wide WebSearch budget (200 calls) was exhausted partway through the sweep. Later agents
substituted direct primary-source fetching, which was in some cases *better* evidence. But **LAW 3
class-1 evidence (job postings) and class-2 evidence (procurement records) are absent for several
candidates** — job boards returned 403s and Contracts Finder's keyword parameter does not bind over
GET. Every buyer count in the consumer report in particular is a **modelled estimate, not an
observation**. Wave 2 must close this gap for the shortlist before any build decision.
