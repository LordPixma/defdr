# 16 — UK SaaS Commercial Benchmarks: the reality check

**Owner:** UK Commercial & Buying-Behaviour Analyst
**Date:** 19 September 2026
**Status:** Reference document. Binding on every candidate proposed in Wave 1.
**Governed by:** `docs/method/01-opportunity-scoring-rubric.md`

This document exists to stop us pricing a candidate against hope. Every number below is drawn from
a primary source — a statistical release, a published pricing page, a G-Cloud pricing document, a
company's own results, or the Companies House register. Where a number is indicative rather than
verified, it is marked.

**The three findings that should change how the team writes candidates:**

1. **The UK denominator is far smaller than it looks.** 5.69m "businesses" collapses to **1.42m
   employers**, and to **46,765 organisations with 50+ employees** across the whole private sector.
   If a candidate needs a buyer with a real ops team, the national ceiling — before any sector
   filter — is under fifty thousand.
2. **Published self-serve pricing dies at roughly £10k ACV.** Every UK vertical vendor we found
   above that price quotes privately. The only systematic source of published UK enterprise
   software prices is **G-Cloud pricing documents**, because the framework compels disclosure.
   That is now a standing research technique for this team.
3. **Cheap-and-large is the most reliable way to fail.** At sub-$10/month ARPA, median annual logo
   retention is ~48%. A large market at a low price is not a market; it is a leaky bucket.

---

## 1. The UK business population — the denominator

**Source:** DBT/ONS *Business Population Estimates for the UK and regions 2025*, published
2 October 2025, reference date start of 2025. This is the latest release; BPE 2026 is not yet out
as of September 2026. Figures below are extracted directly from the published detailed tables
(Table 1 and Table 5).

### 1.1 The headline table — use this one

| Employee size band | Businesses | Share | Employment (000s) | Turnover (£m) |
|---|---:|---:|---:|---:|
| **All private sector businesses** | **5,690,265** | 100% | 28,128 | 5,524,662 |
| — with no employees (unregistered) | 3,044,940 | 53.5% | 3,356 | 135,561 |
| — with no employees (registered) | 1,227,595 | 21.6% | 1,307 | 267,051 |
| **All employers (1+ employees)** | **1,417,730** | **24.9%** | 23,464 | 5,122,051 |
| 1 employee | 114,170 | 2.0% | 254 | 27,686 |
| 2–4 | 772,535 | 13.6% | 2,124 | 372,779 |
| 5–9 | 264,170 | 4.6% | 1,778 | 300,783 |
| 10–19 | 142,500 | 2.5% | 1,952 | 297,849 |
| 20–49 | 77,585 | 1.4% | 2,372 | 478,314 |
| 50–99 | 26,020 | 0.5% | 1,811 | 422,278 |
| 100–199 | 10,205 | 0.2% | 1,435 | 350,825 |
| 200–249 | 2,210 | <0.05% | 492 | 175,536 |
| 250–499 | 4,290 | 0.1% | 1,491 | 407,886 |
| 500–999 | 2,075 | <0.05% | 1,435 | 524,307 |
| 1,000+ | 1,970 | <0.05% | 8,320 | 1,763,807 |

### 1.2 The numbers to memorise

| Question | Answer |
|---|---|
| UK private sector businesses | **5,690,265** |
| …that have **any** employee | **1,417,730** (24.9%) |
| …that have **10+** employees | **266,850** |
| …that have **50+** employees | **46,765** |
| …that have **250+** employees | **8,330** |
| …that have **1,000+** employees | **1,970** |
| VAT and/or PAYE registered enterprises (whole economy, March 2025) | **2.73 million** (ONS) |

**Read that again.** Three-quarters of the UK business population has no employees at all and
£135.6bn of combined turnover across 3.04m unregistered entities — roughly £45k of turnover each.
These are not software buyers. They are a rounding error dressed as a TAM.

The gap between the ONS 2.73m registered enterprises and DBT's 5.69m is the 3.04m unregistered
non-employers DBT imputes from HMRC self-assessment data. **If a candidate's buyer count relies on
the 5.7m figure, it is wrong by a factor of two before we start.**

### 1.3 Sector × size band — employers only

Extracted from BPE 2025 Table 5. This is the table other agents should cite when counting buyers.

| SIC section | All businesses | All employers | 1–9 | 10–49 | 50–249 | 250+ |
|---|---:|---:|---:|---:|---:|---:|
| **All industries** | 5,690,265 | 1,417,730 | 1,150,875 | 220,085 | 38,435 | 8,330 |
| A Agriculture, forestry, fishing | 147,460 | 50,210 | 45,830 | 3,760 | 515 | 105 |
| B,D,E Mining; utilities; water | 28,395 | 9,135 | 6,550 | 1,960 | 450 | 175 |
| C Manufacturing | 263,085 | 84,295 | 57,210 | 19,880 | 5,965 | 1,240 |
| F Construction | 885,485 | 193,675 | 173,740 | 17,555 | 2,080 | 300 |
| G Wholesale & retail; vehicle repair | 548,515 | 242,510 | 198,950 | 37,275 | 5,115 | 1,170 |
| H Transportation & storage | 328,960 | 45,315 | 36,295 | 6,950 | 1,660 | 410 |
| I Accommodation & food service | 233,080 | 145,630 | 106,100 | 35,465 | 3,375 | 690 |
| J Information & communication | 353,035 | 76,810 | 62,480 | 11,245 | 2,545 | 540 |
| K Financial & insurance | 89,235 | 23,965 | 19,325 | 3,185 | 1,020 | 435 |
| L Real estate | 154,770 | 53,405 | 47,340 | 5,405 | 485 | 175 |
| M Professional, scientific, technical | 819,465 | 186,935 | 157,915 | 23,915 | 4,225 | 880 |
| N Administrative & support services | 474,780 | 121,855 | 98,305 | 17,925 | 4,460 | 1,165 |
| P Education | 312,735 | 22,580 | 17,040 | 4,610 | 785 | 145 |
| Q Human health & social work | 397,995 | 64,055 | 38,210 | 20,765 | 4,455 | 625 |
| R Arts, entertainment, recreation | 277,185 | 29,105 | 23,040 | 4,915 | 920 | 230 |
| S Other service activities | 376,080 | 68,250 | 62,545 | 5,275 | 380 | 50 |

**How to use this.** Pick the section. Pick the size band your product needs. That is your ceiling
*before* discounting for foreign parentage and incumbency (LAW 2). Examples of what it kills
instantly: a product needing a 50+ employee estate agency has **485** possible buyers nationally;
one needing a 50+ employee private education provider has **785**; one needing a 250+ employee
transport operator has **410**.

Regional split (BPE 2025): England 5.0m, Scotland 361,000, Wales 194,000, Northern Ireland 139,000;
London alone 1.042m.

---

## 2. Pricing benchmarks by buyer size — named vendors, real prices

All prices are as published on vendors' own pricing pages or their G-Cloud pricing documents,
retrieved 19 September 2026. Ex-VAT unless stated.

### 2.1 Micro-business (1–9 employees)

| Vendor | Product | Published price | Implied annual ACV |
|---|---|---|---|
| Planday | Rota/scheduling | **£2.99/user/month**, min 5 users | £180 (5 users) – £718 (20 users) |
| Xero | Accounting, "Ignite" | **£18/month** (£1.80 for 6 months) | £216 |
| Xero | Accounting, "Grow" | **£39/month** | £468 |
| Sage | Sage Accounting (0–25 employees) | **from £20/month** | £240 |
| Trail | Hospitality ops, per site | **£32/site/month** annual (£38 monthly) | £384/site |
| Tradify | Trades job management | **£34–£44/user/month** | £408–£528/user |
| BrightHR | HR, Core | **£16.67/employee/month**, min 5 | **£1,000** (5 employees) |

**Micro ACV range: £200 – £1,000.** Note two things. First, Xero's headline is a 90% discount for
six months — UK micro-SaaS is priced at a discount by default. Second, BrightHR is the outlier at
£1,000, and it achieves that by selling **24, 36 and 60-month contracts**, not monthly ones. That
is the only way the CAC works at this size.

### 2.2 SME (10–249 employees)

| Vendor | Product | Published price | Implied annual ACV |
|---|---|---|---|
| Dentally | Dental practice management | **£125–£945/surgery/month** by tier and surgery count | £1,500 – £11,340 |
| Trail | Hospitality ops, Standard/Evo | £65–£71.50/site/month annual | £780–£858/site (×N sites) |
| Birdie (G-Cloud 14) | Domiciliary care | **£9–£21 per active care recipient/month** | 100 recipients @ Advanced = **£20,400** |
| Birdie | Care Management only | £8–£11 per care recipient/month | 100 recipients = £9,600–£13,200 |
| everyLIFE PASS (G-Cloud 15) | Care management | **£890/month** ≤50 service users; £890 + £9.20/person 51–150 | £10,680 – £18,408 (120 users) |
| OneAdvanced (G-Cloud 15) | Care Business Management Core | **£4,550/year** banded, 1–69 users | £4,550 |
| OneAdvanced (G-Cloud 15) | Care Business Management Bundle | **£11,900/year** banded, 1–69 users | £11,900 |
| BrightHR | Full HR + H&S + EAP | £31.30/employee/month | 50 employees ≈ £18,780 |

**SME ACV range: £1,500 – £25,000.** The cleanest single benchmark in this document is Birdie's
G-Cloud 14 pricing schedule, because it is a published procurement record with per-unit rates and
mandatory attachments. A 300-care-recipient domiciliary agency on Advanced pays
**£61,200 subscription + £4,680 mandatory Success & Support = £65,880/year**, plus a one-off
implementation fee of **£28 per care recipient (£8,400)** — implementation is *mandatory* above 300
recipients. That is the real shape of UK SME vertical SaaS: usage-priced, services-attached,
annually committed.

### 2.3 Mid-market (250–999) and enterprise (1,000+)

| Vendor | Product | Published price | Implied annual ACV |
|---|---|---|---|
| OneAdvanced (G-Cloud 15) | Care Bundle, per-user cumulative | £170/user (70–100) → £110 (301–1,000) → £61 (1,001–2,000) → £37 (2,001–9,999) | 500 users ≈ **£55,000**; 2,000 users ≈ **£122,000** |
| Civica (G-Cloud 15) | iCasework, committed 3-year term | **min £10,000/yr**; £1,213/user (1st–20th) → £728/user (201st–300th) | £10,000 – £180,000+ |
| Civica (G-Cloud 15) | iCasework, flexible term (30 days' notice) | **min £12,500/yr** | **+25% for the right to leave** |
| Ideagen | EHS/quality/compliance (Hg portfolio) | not published | **£200m ARR ÷ 13,000 customers ≈ £15,400 average** |
| OneAdvanced | whole business | not published | **£330m turnover ÷ 10,000 customers ≈ £33,000 average** |
| Craneware | US hospital revenue intelligence | not published | **$184m ARR across ~2,000 hospitals ≈ $92,000** |
| Kainos | Digital + Workday | not published | £431.1m revenue ÷ 1,253 customers ≈ £344,000 (services-weighted) |

**Mid-market/enterprise ACV range: £25,000 – £150,000** for a single vertical application;
averages across a whole vendor book land at **£15,000–£33,000** because the book is dominated by
smaller customers.

### 2.4 Public sector and regulated

| Vendor | Product | Published price |
|---|---|---|
| Civica | Xpress Core Election Management System | **£30,000 per unit per year** (+ £6,000 WebReg, + £1,924 canvasser app; implementation on rate card) |
| RIVIAM | NHS multi-agency referral hub | **£40,000 setup + £3,250–£7,500/month** by referral volume (£39,000–£90,000/yr) |
| RIVIAM | optional components | Solution Model £35,000 setup; additional pathway £5,000; extra referral form £3,250–£4,750; PM charge £8,000 on setups over £80,000 |
| Birdie | G-Cloud local authority discount | Advanced falls from £17 to **£14.45** (>150 recipients) and **£12.50** (>250 recipients) |

**Public sector ACV: £30,000 – £90,000 recurring, with £40,000–£100,000+ of one-off setup.** The
services attach rate is enormous and is where the margin risk lives — RIVIAM's mandatory setup
(£40,000) can exceed a full year of subscription.

Civica's Xpress pricing is the perfect LAW 2 illustration. UK election management software: roughly
380 UK local authorities, at £30,000 core. **The entire national category is worth about £11m a
year, and Civica already has it.**

### 2.5 The self-serve / sales-led boundary — derived from the evidence

Vendors who publish a price: Xero, Sage, Planday, Trail, Tradify, Dentally, BrightHR, GoCardless.
Vendors who do not: LEAP, Clio (UK page returns 403 to non-browser clients), Ideagen, Access Group,
Nourish, OneAdvanced, Civica — the last three publish *only* because G-Cloud compels a pricing
document.

**The boundary sits at roughly £10,000 ACV.** Dentally's £945/surgery/month (£11,340/yr) is the
highest self-serve published price we found anywhere in UK vertical SaaS.

---

## 3. The ACV × buyer-count feasibility matrix

### 3.1 Customers required

| ACV | £1m ARR | £3m ARR | £10m ARR |
|---:|---:|---:|---:|
| £500 | 2,000 | 6,000 | 20,000 |
| £1,000 | 1,000 | 3,000 | 10,000 |
| £2,500 | 400 | 1,200 | 4,000 |
| £5,000 | 200 | 600 | 2,000 |
| £10,000 | 100 | 300 | 1,000 |
| £25,000 | 40 | 120 | 400 |
| £50,000 | 20 | 60 | 200 |
| £100,000 | 10 | 30 | 100 |

### 3.2 Overlaying a realistic five-year win rate

What share of a defined UK vertical can a new entrant actually take in five years? The evidence:

- **Ideagen** — the UK's most successful recent vertical compliance SaaS — reports **3.2% market
  share of its own £3.0bn serviceable obtainable market** at £200m+ ARR, after eleven years and
  **30+ acquisitions**. Organic ARR growth was **19% LTM** (April 2024).
- **Craneware** reached $184m ARR over **26 years**, and in FY25 **only 2% of the annual value of
  new sales came from new hospitals** — 83% came from existing customers not even at renewal.
- **Access Group** and **OneAdvanced** reached 160,000 and 10,000 customers respectively; both were
  assembled by acquisition, not organic new-logo sales.

**Conclusion: 1–3% penetration of a defined UK vertical in five years is the realistic base case.
5% is a strong outcome. Above 10% is not supported by any UK precedent we could find for an
organically-grown entrant.**

### 3.3 The required winnable-buyer population (the test that actually bites)

Winnable buyers required = customers needed ÷ penetration rate. For **£3m ARR**:

| ACV | Customers needed | @3% penetration | @5% | @10% (exceptional) |
|---:|---:|---:|---:|---:|
| £1,000 | 3,000 | 100,000 | 60,000 | 30,000 |
| £2,500 | 1,200 | 40,000 | 24,000 | 12,000 |
| £5,000 | 600 | 20,000 | 12,000 | 6,000 |
| £10,000 | 300 | 10,000 | 6,000 | 3,000 |
| £25,000 | 120 | 4,000 | 2,400 | 1,200 |
| £50,000 | 60 | 2,000 | 1,200 | 600 |
| £100,000 | 30 | 1,000 | 600 | 300 |

Now cross-reference §1.3. A vertical of 50+ employee firms in *any single SIC section* has at most
**5,965** members (manufacturing) and typically **under 2,000**. **At a 3% win rate, only ACVs of
£50,000+ reach £3m ARR from a single 50+ employee vertical.** Everything below that requires either
the 10–49 band (where ACV caps around £10–25k) or several sectors at once.

This is the central commercial constraint on the whole DEFDR exercise.

### 3.4 The churn overlay — why the top-left of the matrix is a trap

Gross retention determines how much of the sales effort is spent standing still.

| Target | ACV | Customers | Gross retention (§6) | Customers lost/yr | New logos/yr just to stand still |
|---|---:|---:|---:|---:|---:|
| £3m | £1,000 | 3,000 | ~55% | 1,350 | **1,350** |
| £3m | £5,000 | 600 | ~75% | 150 | **150** |
| £3m | £10,000 | 300 | ~80% | 60 | **60** |
| £3m | £50,000 | 60 | ~87% | 8 | **8** |

Winning 1,350 new customers every year forever, at £1,000 each, with no human permitted to touch
the sale, is not a plan. **The bottom-right of the matrix is the only habitable zone.**

---

## 4. Where UK vertical SaaS has actually won — and what the winners share

| Company | Vertical | Scale | Route |
|---|---|---|---|
| **Ideagen** | EHS / quality / GRC in regulated industries | £200m+ ARR, 13,000+ customers, ~£15.4k avg ACV. Revenue £7m (FY13) → £175m (FY24), 34% CAGR. Acquired by Hg for **£1.09bn**, June 2022 | 30+ acquisitions; £300m+ deployed, £69m ARR acquired under Hg |
| **Craneware** | US hospital revenue integrity & 340B | $184m ARR, $205.7m revenue FY25, ~90% recurring, 32% adj. EBITDA margin, NRR 107%, retention >90% | 26 years, organic + acquisition. **Edinburgh-based; sells entirely into the US** |
| **Access Group** | Multi-vertical UK business software | ~£1.2bn revenue reported Feb 2026; 160,000+ customers | Serial acquisition, PE-backed |
| **OneAdvanced** | UK sector software | £330m turnover, 10,000 customers, 1,800 staff (~£33k avg ACV) | Acquisition-led; "UK's third largest provider of business software" |
| **Civica** | UK local government & public services | Owns categories outright (e.g. election management at £30k/authority) | Incumbency + framework presence |
| **Kainos** | Digital services + Workday products | £431.1m revenue FY26 (+17%), adj. PBT £67.1m (+2%), 1,253 customers, NPS 61 | Services-led, partner-anchored |

### What the winners have in common

1. **They sell into a compliance obligation, not a preference.** Ideagen's ARR sits in life
   sciences, aviation, healthcare, food and government — places where the record *must* exist.
   Craneware sells 340B and pricing-transparency compliance. Civica sells statutory functions.
2. **They own a data asset that compounds.** Craneware: 26 years of data, 200m patient encounters,
   >2,000 hospitals — explicitly cited as its competitive advantage. This is a LAW-4 moat, and it
   is why nobody has displaced it in 26 years.
3. **They grew by acquisition, because organic UK vertical growth is too slow.** Ideagen: 30+ deals.
   Access and OneAdvanced: the same. **No UK vertical SaaS in this list reached scale organically
   inside ten years.**
4. **Their expansion revenue exceeds their new-logo revenue.** Ideagen: NRR 111%+ against gross
   retention 90%+. Craneware: 98% of FY25 new sales value came from existing customers.
   **The land is small; the expand is everything.**
5. **The biggest one isn't selling to the UK.** Craneware is the highest-ACV, highest-margin, most
   durable company on this list and it sells into US hospitals. That is a direct comment on the
   size of the UK denominator in §1.
6. **Efficient, not explosive.** Ideagen's CAC ratio is **0.77** — £0.77 of sales and marketing per
   £1 of net new ARR — with 92%+ gross margin and 30%+ EBITDAC margin. That is the efficiency bar.

---

## 5. Where UK vertical SaaS fails

**Disclosure required by Part D.3:** this session's web-search budget was exhausted before I could
build a properly triangulated list of *named* UK vertical SaaS shutdowns with documented causes.
What follows is (a) structural failure evidence from the Companies House register, which is
primary and verified, and (b) failure mechanisms derived from the pricing and churn evidence above.
The named-case work is handed to Wave 2 as an explicit gap. I would rather report the gap than pad
it with half-verified names.

### 5.1 Structural evidence — Companies House register, 19 September 2026

Advanced company search by SIC code:

| SIC code | Description | Total ever registered | Active | Dissolved | In liquidation | In administration |
|---|---|---:|---:|---:|---:|---:|
| **58290** | Other software publishing (closest proxy for a software *product* company) | 39,035 | 20,320 | **18,606** | 100 | 5 |
| **62012** | Business and domestic software development | 220,649 | 121,402 | **98,218** | 954 | 56 |
| **62020** | IT consultancy activities | 416,625 | 174,010 | **240,234** | — | — |

**47.7% of every UK software-publishing company ever incorporated is dissolved.** For IT
consultancy it is 57.7%.

**Honest caveat:** dissolution includes voluntary strike-off of dormant shells and single-person
contractor companies, so this measures *corporate mortality*, not product failure. It is still the
best available structural base rate, and it says the modal outcome for a UK software company is
that it stops existing.

### 5.2 Verified individual status facts (Companies House)

- **Hopin Ltd (12035150)** — **dissolved 24 May 2026.** The most prominent UK SaaS collapse of the
  decade. (Its funding history and peak valuation are widely reported but `[UNVERIFIED]` here.)
- **Hokodo Services Ltd (11351988)** — **in liquidation**, c/o Interpath Ltd. Note precisely: the
  main trading entity Hokodo Ltd (11215527) remains active. This is a group entity, not the
  business.
- **Zopa Embedded Finance Limited (14602085)** — **dissolved 23 September 2025**, while Zopa's bank
  continues. A discontinued product line, not a company failure.

The precision matters. Name-matching on Companies House produces false positives easily; two of the
three "failures" above are entity-level, not business-level. Wave 2 must verify at trading-entity
level before any candidate is justified by a competitor's demise.

### 5.3 The five mechanisms that kill UK vertical SaaS

Each is evidenced elsewhere in this document.

1. **The denominator was the 5.7m figure.** Three-quarters of it has no employees. (§1)
2. **The ACV was set at the micro-business band but the product needs an SME sales motion.** At
   £1,000 ACV you can afford roughly £770 of CAC (Ideagen's 0.77 ratio). That buys no human contact
   at all. (§3.4, §7)
3. **Churn ate the funnel.** Sub-$10/month ARPA has ~48% median annual logo retention. (§6)
4. **The incumbent bundled it.** Access, OneAdvanced, Iris and Civica sell suites. A single-feature
   product competes against a line item the buyer is already paying for. OneAdvanced's Care Bundle
   at £11,900 versus Core at £4,550 is exactly this weapon: £7,350 buys everything else, so a
   point solution must be worth more than the bundle delta.
5. **The category was never big enough.** Election management: ~380 buyers × £30,000 = ~£11m
   national category, already owned. A 40-year-old pain with no winner is evidence the category
   cannot support a company (LAW 4), not evidence of an opening.

---

## 6. Churn reality

**Source:** ChartMogul *SaaS Retention Report*, 2,100+ SaaS businesses, 12-month cohorts. Global,
not UK-specific — flagged accordingly — but segmented by ARPA, which is the variable that matters.

### By ARPA band (the table that decides viability)

| ARPA | Median logo retention | Median gross revenue retention | Median NRR | % achieving NRR >100% |
|---|---:|---:|---:|---:|
| <$10/month | **~48%** | ~40% | ~45% | 2.7% |
| $10–50/month | ~62% | ~55% | ~60% | ~8% |
| $50–100/month | ~76% | ~75% | ~75% | ~12% |
| $100–500/month | ~76% | ~75% | ~88% | ~25% |
| **>$500/month** | **~84%** | **~87%** | ~100%+ | **41.1%** |

Best-in-class at >$500/month ARPA: >93% logo retention, ~95% GRR, 115–125% NRR.

### UK vendor corroboration

- **Ideagen** (£15.4k avg ACV): gross retention **90%+**, NRR **111%+**.
- **Craneware** ($92k avg ACV): customer retention **>90% on all metrics**, NRR **107%**, top-ten
  customer relationships averaging **20 years**.

Both sit at or above the >$500/month best-in-class band, which is consistent with the ChartMogul
segmentation rather than an independent confirmation of it — treat as one evidence cluster plus
two vendor disclosures.

### The verdict

**A large-but-cheap UK market is not viable.** At ~50% annual logo churn, a 3,000-customer base at
£1,000 ACV must be more than half rebuilt every year. The only ways UK vendors beat this at low
price points are structural, not motivational:

- **Contract length.** BrightHR sells **24, 36 and 60-month** terms at £16.67/employee/month.
- **Mandatory services.** Birdie makes implementation and success packages **compulsory above 300
  care recipients**; Civica charges **25% more** for a 30-day-notice term than a 3-year one.
- **Regulatory record-keeping.** If the system of record holds the CQC/audit evidence, leaving
  means losing the evidence.

**If a candidate has none of these three, assume the ChartMogul median and price accordingly.**

---

## 7. How UK businesses actually buy software

### 7.1 Friction thresholds — what is required at what buyer size

| Buyer | Sales motion | Cycle (indicative) | Security/compliance gate | Payment norm |
|---|---|---|---|---|
| Sole trader / non-employer (0) | Self-serve only | days | none | Card, monthly |
| Micro (1–9) | Self-serve; at most inbound-assisted | 1–4 weeks | none; owner signs personally | Card or Direct Debit, monthly |
| Small (10–49) | Inside sales, demo-led | 1–3 months | DPA; basic supplier form; references | **Direct Debit, annual or multi-year** |
| Medium (50–249) | Field/inside sales, pilot common | 3–6 months | Supplier security questionnaire; **Cyber Essentials commonly requested**; insurance certs; DPIA if high-risk processing | Direct Debit / invoice, annual in advance |
| Large (250+) | Enterprise sales, procurement-led | 6–12 months | Full vendor risk assessment; **ISO 27001 frequently required**; pen-test report; negotiated DPA and SLAs | Invoice, annual or quarterly, 30–60 day terms |
| Public sector / NHS | Framework or Procurement Act tender | 6–18 months | **Cyber Essentials / CE Plus mandatory** (PPN 014); NHS **DSPT**; published pricing document | Invoice, annual in advance |

Cycle lengths are practitioner-standard indicative ranges, not measured from a UK dataset —
`[UNVERIFIED]`. Everything in the compliance column is verified below.

### 7.2 The compliance gates — verified

- **Cyber Essentials / Cyber Essentials Plus — BINDING.** *PPN 014: Cyber Essentials Scheme*,
  published 17 February 2025, updated for the Procurement Act 2023 terminology. "In-scope
  organisations should note the provisions of this PPN from **24 February 2025**." It applies to
  "all central government departments, their executive agencies and non-departmental public bodies,
  **and NHS bodies**." It bites where "personal information of citizens… is handled by a supplier"
  or "where ICT systems and services are supplied which are designed to store, or process data at
  the **OFFICIAL** level." The Model Services Contract extends it to **relevant subcontractors**.
  There is **no contract-value threshold**. It explicitly "should not be applied to all contracts as
  a matter of course."
  **Cost:** certification "priced according to the size of your organisation, **starting at
  £320 + VAT**" (NCSC); CE Plus is quoted per network size and complexity. Annual renewal.
- **NHS Data Security and Protection Toolkit — BINDING for NHS data.** "All organisations that have
  access to NHS patient data and systems must use this toolkit." Current version **2026-27
  version 9** (as at 8 September 2026). Assesses against the National Data Guardian's 10 data
  security standards.
- **ISO 27001** — not statutory, but a de facto gate at 250+ and in financial services. Indicative
  cost: certification body day rates ~$1,800–$2,500; initial certification audit ~$15,000+;
  surveillance audits ~$8,000–$15,000 a year; total audit spend commonly $8,000–$30,000, before
  consultancy or internal effort. Three-year recertification cycle. `[Indicative — source is a
  vendor blog quoting USD, not a UK price list.]`
- **DPIA (UK GDPR Article 35)** — **triggered by the nature of the processing, not the customer's
  headcount.** Required where processing is likely to result in a high risk to individuals
  (special-category data at scale, systematic monitoring, vulnerable data subjects). A ten-person
  care agency processing health data needs one; a 500-person logistics firm buying a rota tool may
  not. **Do not model DPIA cost as a function of customer size** — model it as a function of the
  data the product touches.

**Compliance cost floor for a UK B2B SaaS selling above the micro band:** Cyber Essentials from
£320+VAT annually is trivial. ISO 27001 at roughly £15k–£25k initial and £8k–£12k annually is not,
and it is effectively mandatory for 250+ and public-sector work. **That is the single largest fixed
cost gate in the model, and it lands before the first enterprise customer pays.**

### 7.3 Payment norms — and why Direct Debit is the UK answer

**GoCardless UK pricing (published):** Standard **1% + 20p, capped at £4**; Advanced 1.25% + 20p
capped at £5; Pro 1.4% + 20p capped at £5.60. Additional 0.3% on transactions over £2,000. No
setup costs, no monthly minimum; volume discounts above £1m annual revenue.

The cap is the whole point. On a **£10,000 annual invoice**, Bacs Direct Debit costs **£4**. An
uncapped card rate of ~1.5% + 20p costs **~£150**. That is 1.5 points of gross margin handed away
for nothing.

**Rule: above roughly £300 ACV, UK B2B SaaS should bill annually in advance by Direct Debit.** This
is also why GoCardless is a UK company — the UK's Bacs mandate infrastructure has no equivalent in
most markets, and it is a genuine structural advantage for UK-domiciled SaaS.

### 7.4 What kills UK SME SaaS deals

1. **The price crosses the owner's personal discretion threshold.** Below 50 employees there is
   usually no procurement process — the owner signs. Above roughly £5,000–£10,000 the decision
   stops being a purchase and becomes a project.
2. **The incumbent bundles it.** See §5.3(4).
3. **Migration cost exceeds the annual saving.** LEAP charges a one-off setup covering data
   migration, training and template configuration. Birdie's mandatory implementation is £28 per
   care recipient.
4. **The vendor needs a long contract to make CAC work, and asking for it signals risk.** BrightHR's
   36-month online default is rational for the vendor and alarming to a five-person buyer.
5. **Involuntary churn.** With UK company mortality at the levels in §5.1, a meaningful share of
   micro-business churn is the customer ceasing to exist.

---

## 8. The AI displacement question

**Best available UK evidence:** ONS, *Artificial intelligence in UK businesses*, published
19 July 2026, covering 2023–2026 (Business Insights and Conditions Survey).

| Measure | Figure |
|---|---|
| Businesses (10+ employees) using AI, September 2023 | ~12% |
| Businesses (10+ employees) using AI, June 2026 | **~35%** |
| Micro (0–9 employees) using AI, June 2026 | 28% |
| Large (250+) using AI, June 2026 | 49% |
| Information & communication sector | 58% |
| Construction sector | 13% |
| Reporting **extensive** AI use | **only 10%** |
| Average AI technologies per adopting business | 1.6 (from 1.4 in Sept 2023) |
| **Headcount effect among adopters: no change** | **~50%** |
| **Headcount effect: reduction** | **~7%** (medium-sized firms most affected) |
| Headcount effect: increase | ~1% |
| Businesses reporting AI decreased operational costs | 6% (63% no change) |

### Verdict for a 5–10 year durability assessment

**Adoption is real and fast. Displacement is not yet visible in the data.** AI use among UK
businesses with 10+ employees roughly tripled in under three years, but only **10% describe their
use as extensive**, and only **~7% of adopters report any headcount reduction**. There is no
measurable UK evidence yet of seat reduction or price compression in vertical SaaS specifically.

Two counter-signals worth carrying forward:

- **Craneware and Ideagen are both shipping AI as an embedded feature, not defending against it.**
  Craneware's FY25 deck leads with "leveraging our data & AI innovation" and a strengthened
  Microsoft partnership; Dentally now meters **AI clinical notes per surgery per month** (45 on
  Essentials, 90 on Pro) — AI as a *tiering lever that raises ACV*, not as a substitute.
- **Margin pressure is visible where the product is labour-shaped.** Kainos FY26: revenue **+17%**
  but adjusted pre-tax profit **+2%**. Services-weighted businesses are being squeezed in a way
  product businesses are not.

**Rule for candidate scoring (rubric Part D.4):** score durability 1–2 where the product's value is
*generating text or summarising documents the customer already holds* — a general assistant erases
that. Score 4–5 where value comes from **being the regulated system of record**, from **data the
customer cannot assemble alone**, or from **a compliance obligation with a named liable person**.
AI makes the first category worthless and the third category *more* valuable, because an auditable
record becomes scarcer as generated content becomes cheap.

---

## 9. The DEFDR Commercial Feasibility Test — one page

Apply all six gates to every candidate. **Any gate failed is a rejection**, consistent with the
rubric's "any axis scoring 1 is an automatic rejection".

---

**GATE 1 — The denominator.** State the SIC section and the employee size band your buyer must be
in. Look the number up in §1.3. Reject if you cannot do this without using the 5.69m figure.
> Hard ceilings: 50+ employees = **46,765** nationally. 250+ = **8,330**. 1,000+ = **1,970**.

**GATE 2 — The ACV.** Take the ACV from the §2 band for that buyer size. You may not claim an ACV
above the band ceiling without naming a comparable vendor and its published price.
> Micro £200–£1,000 · SME £1,500–£25,000 · Mid-market/enterprise £25,000–£150,000 · Public sector
> £30,000–£90,000 + setup.

**GATE 3 — The arithmetic.**
> `customers_needed = 3,000,000 / ACV`
> `penetration_needed = customers_needed / winnable_buyers`
>
> **<3%** → proceed. **3–10%** → requires a BINDING forcing function *and* a named incumbent
> weakness. **>10%** → **reject**; no UK precedent supports it.

**GATE 4 — The churn gate.** Look up gross retention for the ACV band in §6. Compute
`customers × (1 − GRR)` = logos you must replace every year forever.
> If ARPA is under ~£500/month **and** the plan needs more than 300 customers, reject — unless the
> candidate has at least one of: **multi-year contracts**, **mandatory implementation**, or **a
> regulatory record the customer cannot take with them**.

**GATE 5 — The friction gate.** From §7.2, price the compliance obligations for the target buyer.
> Public sector or NHS → **Cyber Essentials is mandatory** (PPN 014, in force 24 Feb 2025), and
> so is the DSPT for NHS patient data. 250+ private → assume **ISO 27001 ≈ £15k–£25k initial,
> £8k–£12k/yr**. Reject if year-one revenue does not cover 3× the compliance cost.

**GATE 6 — The CAC gate.** Benchmark: Ideagen spends **£0.77 of S&M per £1 of net new ARR**. Your
affordable CAC is therefore ≈ 0.8 × ACV.
> **ACV < £2,000** → affordable CAC < £1,600 → **no human may touch the sale.** Product-led only.
> **ACV £2,000–£10,000** → inside sales; one rep at ~£90k loaded must close ~25–45 deals/year.
> **ACV > £10,000** → field sales, 3–12 month cycle, and no self-serve conversion will occur.
> Reject if the candidate assumes self-serve above £10,000 or a salesperson below £2,000.

---

**The single sentence version:** *a UK vertical SaaS candidate is feasible if there are at least
1,000–4,000 winnable UK buyers who will pay £25,000–£100,000 a year for a regulated system of
record they cannot leave — and is almost certainly infeasible if it needs tens of thousands of
small buyers at under £5,000.*

---

## 10. Sources

**Business population**
- DBT/ONS, *Business Population Estimates for the UK and regions 2025*, statistical release and
  detailed tables (published 2 October 2025, reference date start of 2025) —
  https://www.gov.uk/government/statistics/business-population-estimates-2025 ; detailed tables
  https://assets.publishing.service.gov.uk/media/68dbccc9c487360cc70c9f4e/BPE_2025_detailed_tables.xlsx
  (Tables 1 and 5 extracted directly)
- ONS, *UK business: activity, size and location, 2025* (IDBR snapshot 14 March 2025) —
  https://www.ons.gov.uk/businessindustryandtrade/business/activitysizeandlocation/bulletins/ukbusinessactivitysizeandlocation/2025

**Pricing (vendor pages, retrieved 19 September 2026)**
- Xero UK — https://www.xero.com/uk/pricing/
- Sage UK shop — https://www.sage.com/en-gb/shop/
- BrightHR — https://www.brighthr.com/pricing/
- Trail — https://trailapp.com/pricing
- Tradify — https://www.tradifyhq.com/en-gb/pricing
- Dentally — https://www.dentally.com/en-gb/pricing
- Planday — https://www.planday.com/pricing
- GoCardless — https://gocardless.com/pricing
- LEAP (no published price) — https://www.leaplegalsoftware.com/uk/pricing/

**Pricing (G-Cloud published pricing documents — the systematic source)**
- Birdie for Home Care, G-Cloud 14 pricing document —
  https://assets.applytosupply.digitalmarketplace.service.gov.uk/g-cloud-14/documents/712652/126012328431224-pricing-document-2024-11-27-1448.pdf
- everyLIFE PASS, G-Cloud 15 (January 2026) —
  https://www.applytosupply.digitalmarketplace.service.gov.uk/g-cloud/services/740151688138416
- OneAdvanced Care Business Management, G-Cloud 15 (1 September 2026) —
  https://www.applytosupply.digitalmarketplace.service.gov.uk/g-cloud/services/963315290903857
- RIVIAM Multi-agency Referral Hub, G-Cloud 15 (January 2026) —
  https://www.applytosupply.digitalmarketplace.service.gov.uk/g-cloud/services/467185388709016
- Civica Xpress Election Management System, G-Cloud 15 —
  https://assets.applytosupply.digitalmarketplace.service.gov.uk/g-cloud-15/documents/92935/499731092779899-pricing-document-2026-01-30-0929.pdf
- Civica iCasework, G-Cloud 15 —
  https://assets.applytosupply.digitalmarketplace.service.gov.uk/g-cloud-15/documents/92935/222290890759829-pricing-document-2026-01-30-1205.pdf

**Company performance**
- Ideagen portfolio spotlight, HgCapital Trust Capital Markets Day 2024 (ARR, retention, CAC ratio,
  revenue history) —
  https://www.hgcapitaltrust.com/~/media/Files/H/Hgcapital-Trust-V2/documents/investors/publications/2024/Capital-markets-day-2024/portfolio-company-spotlight-ideagen.pdf
- Craneware plc FY25 results presentation (year ended 30 June 2025) —
  https://www.thecranewaregroup.com/media/e4ro0uxy/crw-fy25-results-presentation.pdf
- Kainos FY26 results highlights — https://www.kainos.com/investor-relations

**Procurement and compliance**
- *PPN 014: Cyber Essentials Scheme*, published 17 February 2025, in force 24 February 2025 —
  https://www.gov.uk/government/publications/ppn-014-cyber-essentials-scheme/ppn-014-cyber-essentials-scheme-html
- NCSC, Cyber Essentials overview (pricing from £320 + VAT) —
  https://www.ncsc.gov.uk/cyberessentials/overview
- NHS Data Security and Protection Toolkit (2026-27 v9) — https://www.dsptoolkit.nhs.uk/
- Digital Marketplace / G-Cloud service search (3,472 "case management" cloud-software services;
  779 for "care management") —
  https://www.applytosupply.digitalmarketplace.service.gov.uk/g-cloud/search

**Churn**
- ChartMogul, *SaaS Retention Report* (2,100+ SaaS businesses; global, segmented by ARPA) —
  https://chartmogul.com/reports/saas-retention-report/

**AI**
- ONS, *Artificial intelligence in UK businesses, 2023 to 2026*, published 19 July 2026 —
  https://www.ons.gov.uk/businessindustryandtrade/business/businessservices/articles/artificialintelligenceinukbusinesses/2023to2026

**Failure base rates**
- Companies House advanced company search by SIC code, retrieved 19 September 2026 —
  https://find-and-update.company-information.service.gov.uk/advanced-search
  (SIC 58290, 62012, 62020; status filters active / dissolved / liquidation / administration)

---

## 11. Known gaps — handed to Wave 2

1. **Named UK vertical SaaS failures with documented causes.** Web-search budget was exhausted;
   §5 carries structural evidence only. Needed: 5–8 named cases at trading-entity level with cause
   of death.
2. **Measured UK sales-cycle lengths by segment.** §7.1 cycle ranges are practitioner-standard, not
   measured. A UK dataset would strengthen Gate 6.
3. **UK-specific churn data.** §6 is global ChartMogul data segmented by ARPA. A UK vertical
   cohort would be better.
4. **A UK GBP price list for ISO 27001 certification.** §7.2 uses a USD vendor blog.
5. **CCS Power BI framework spend data** for G-Cloud volumes by lot and buyer type, which would let
   us size public-sector categories directly rather than by buyer count × price.
