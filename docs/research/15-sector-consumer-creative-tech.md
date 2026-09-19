# Sector Research 15 — Retail, Hospitality, Consumer, Creative & Tech

**Analyst:** UK Sector Analyst — Retail, Hospitality, Consumer, Creative & Tech
**Date:** 19 September 2026
**Method:** `/home/user/defdr/docs/method/01-opportunity-scoring-rubric.md` v1 (binding)

> **Research constraint disclosed up front (Hard Rule 1 / Rule 3).** The session's WebSearch budget
> (200 calls) was exhausted by the wider team partway through this run. Roughly 10 keyword searches
> were made before exhaustion; the remainder of this research was conducted via ~35 direct fetches of
> primary sources (legislation.gov.uk, the Home Office impact assessment PDF, the Charity Commission
> register, ONS bulletins, Acas, gov.uk guidance) plus the gov.uk Search API used as a URL-discovery
> substitute. **Job-posting evidence (LAW 3 class 1) could not be obtained: CV-Library returned 403,
> Totaljobs reset the connection, and DWP Find a Job errored.** Contracts Finder's keyword parameter
> does not bind over GET and returned unfiltered results, so procurement-record evidence (class 2) is
> also absent. Every candidate below is therefore triangulated on **regulator datasets/enforcement
> instruments (class 4)** and **competitor pricing pages (class 3)**, which satisfies LAW 3's
> "two different classes from 1–5", but the analysis is weaker than it should be on proof that the
> *role* exists with a budget. Treat every buyer count as a modelled estimate, not an observation.

---

## 1. Executive summary — top five candidates ranked

Ranked by total 8-axis score, with the honest caveat that **not one of these scores 4+ on
incumbency**. That is the defining finding of this sector sweep: these are the most
software-saturated SME markets in the UK economy, and every regulatory shock lands on a field that
already contains five to ten funded vendors.

| # | Candidate | Winnable UK buyers | Score | Forcing function |
|---|---|---|---|---|
| 1 | **Umbrella & agency labour PAYE liability control (end-client side)** | ~1,500–3,000 | **29/40** | BINDING — 6 Apr 2026 |
| 2 | **Holiday entitlement & pay evidence vault (6-year WTR records duty)** | ~3,000–6,000 | **27/40** | BINDING — 6 Apr 2026 |
| 3 | **Martyn's Law enhanced-tier assurance + estate/event notification register** | ~800–1,200 | **27/40** | SCHEDULED — Spring 2027 |
| 4 | **Multi-site regulatory permission & obligation register ("estate passport")** | ~2,000–3,000 | **26/40** | Mixed BINDING (no single driver) |
| 5 | **Guaranteed-hours & shift evidence ledger (ERA 2025 ss.1–3)** | ~4,000–5,000 | **25/40** | SCHEDULED 2027; detail still PROPOSED |

**Three corrections to the brief, made before anything else:**

1. **There is no "Employment Rights Act 2026."** The instrument is the **Employment Rights Act 2025
   (c. 36)**, Royal Assent 2025. Verified against legislation.gov.uk.
2. **Day-one unfair dismissal did not survive Parliament.** The Government accepted a Lords amendment
   substituting a **six-month qualifying period**, effective **1 January 2027**. The unfair dismissal
   compensation cap is removed on the same date. Building on "day one" would have been building on a
   manifesto commitment that was legislated away.
3. **The single most under-noticed binding obligation in these sectors is not in the brief at all:**
   the **annual-leave record-keeping duty in force since 6 April 2026**, requiring records of holiday
   entitlement and holiday pay to be kept **for six years**, breach of which is a **criminal offence
   with an unlimited fine**. Almost every variable-hours employer in retail and hospitality is
   already in breach. That is a textbook LAW 1 forcing function — obligation, date, buyer already
   non-compliant — and it was hiding behind the noisier zero-hours headlines.

**And the headline negative:** the brief's hypothesis that Martyn's Law is "the single largest
obligated population in the UK economy" is **arithmetically true and commercially misleading**.
The obligated population is 178,891 premises. The *addressable* population is roughly 24,000. See §5.

---

## 2. Sector structure

| Sub-sector | UK organisation count | Typical annual software spend | Churn risk | Source |
|---|---|---|---|---|
| Wholesale & retail (VAT/PAYE registered) | 396,000 | £0–£1,000/site | Retail death rate **10.9%/yr** | ONS *UK Business*, Mar 2025 |
| Wholesale & retail (incl. unregistered) | 548,515 | mostly £0 | high | ONS Business Population Estimates 2025 |
| Accommodation & food services (registered) | 177,000 | £400–£1,500/site | **12.9%/yr death rate** | ONS *UK Business*, Mar 2025; ONS Business Demography 2024 |
| Accommodation & food (incl. unregistered) | 233,080 | mostly £0 | very high | ONS BPE 2025 |
| Arts, entertainment & recreation | 192,000 | £0–£500 | 8.4%/yr death rate | ONS *UK Business*, Mar 2025 |
| Information & communication (tech/telecoms) | 188,000 | high per-seat, self-serve | low | ONS *UK Business*, Mar 2025 |
| Registered charities, England & Wales | **171,867 main** (185,647 incl. linked) | see below | low | Charity Commission register, **18 Sep 2026** |
| — charities with income >£500k | **15,334** | £450–£4,000 | low | Charity Commission income-band data, 18 Sep 2026 |
| — charities with income <£100k | **128,435 (74.7%)** | £0 | n/a | Charity Commission income-band data |
| Martyn's Law standard-tier premises | **154,623** | £0–£350 | high | Home Office TPoP Impact Assessment, Table 1 |
| Martyn's Law enhanced-tier premises | **24,268** | £1,000–£6,000 | low | Home Office TPoP Impact Assessment, Table 1 |
| **UK businesses with 5+ trading sites (all sectors)** | **12,615** | £5k–£500k | low | ONS *UK Business* 2025, Table 5 |
| — of which 20+ sites | 2,750 | | | same |

**The most important row in that table is the last block.** Across the *entire* UK economy there are
**12,615 businesses operating five or more sites**, and only **2,750** operating twenty or more.
Every "multi-site compliance platform" pitch in retail and hospitality is fishing in a pond of
roughly **5,000–6,000 plausible buyers**, not the 570,000 businesses the sector headcount implies.
Single-site businesses number 2,676,440 and buy almost nothing. This is LAW 2 in its purest form.

---

## 3. Willingness to pay and churn — the honest verdict

The brief asked for real scepticism here. It is warranted, but the picture is more nuanced than
"hospitality SMEs won't pay".

**What is proven.** UK hospitality operators demonstrably pay **£32–£82.50 per site per month** for
an operational compliance product — that is Trail's published pricing, £384–£990 per site per year,
sold to pub and restaurant estates. They pay **£2.99–£3.50 per employee per month** for workforce
management (Planday, Deputy), which is ~£110–£130/month for a 25-person site. Charities with income
over £500k pay **£444–£3,900/year** for a CRM (Beacon's published tiers). So the "cheapest buyers in
the economy" framing is half-wrong: the *multi-site operator* is a normal SaaS buyer.

**What is not proven, and is probably false.** The *independent* single-site operator is not a
viable SaaS buyer for a compliance point-solution. Two pieces of evidence converge:

- The Home Office's own impact assessment models the **ongoing** annual burden on a standard-tier
  premises as **4.5 hours of management time** for counter-terrorism procedure review, at £29.34/hour
  — roughly **£132 a year**. Ten-year present-value cost per standard-tier premises: **£3,313**, or
  ~£331/year including training and familiarisation. No one buys software to avoid £132 of work.
- Two Martyn's Law vendors have already converged on **£18 and £19 per month** entry pricing. That is
  what the market clears at when the underlying obligation is a form.

**Churn.** ONS Business Demography 2024 gives the floor: **accommodation and food services had a
12.9% business death rate**; retail 10.9%; wholesale 8.9%; arts/entertainment/recreation 8.4%.
Overall five-year business survival is **38.4%**. A vendor selling to independent hospitality carries
~13% annual logo churn from customer *death alone*, before a single voluntary cancellation. Layer
normal SMB voluntary churn on top and 25–35% annual churn is the realistic planning assumption.

**The arithmetic the brief demanded.** A £20/month product with 40% annual churn has an LTV of roughly
£600 at a 60% gross margin, against a UK SMB CAC that is rarely below £300–£500 for a compliance
product requiring explanation. That is not a business. **The only defensible shapes in these sectors
are (a) sell to the ~5,000–6,000 multi-site operators at £3,000–£30,000 ACV, or (b) sell to the
professional intermediary — the accountant, the payroll bureau, the licensing solicitor, the
recruitment agency — who aggregates thousands of end sites behind one contract.** Every candidate
below is scored on that basis. Direct-to-independent-SME is treated as a rejection criterion.

---

## 4. Full candidate analysis

Scoring: 1–5 per axis. **Any axis scoring 1 is an automatic rejection.**

### CANDIDATE 1 — Umbrella & agency labour PAYE liability control (end-client side) · **29/40**

| # | Field | |
|---|---|---|
| 1 | **The gap** | Since 6 April 2026 an agency or end client is legally responsible for PAYE being operated correctly when an umbrella company employs its workers, and HMRC can recover the umbrella's underpayment from the client — but the client has no systematic way to verify, per worker per pay period, that the umbrella actually did it. |
| 2 | **Pain owner** | Head of Resourcing / Resourcing Compliance Manager in a multi-site retail, hospitality or logistics group; Production Accountant or Line Producer in film/TV. |
| 3 | **Budget holder** | Finance Director / Group Financial Controller. Tax-risk line, not IT. |
| 4 | **UK buyer count** | Method: end clients with material umbrella-sourced labour = multi-site operators (5+ sites: 12,615 across all sectors, ~45% in retail/hospitality/leisure ≈ 5,700) filtered to those using agency labour at scale (judgement: ~30%) ≈ 1,700; plus UK production companies and event operators (~400); plus recruitment agencies who will buy it defensively. **Winnable: ~1,500–3,000.** For £3m ARR at 2,000 buyers, ACV = £1,500. Credible against existing accreditation spend. |
| 5 | **Forcing function** | **BINDING.** Income Tax (Pay As You Earn) rules for labour supply chains including umbrella companies, in force **6 April 2026**, applying to money paid on or after that date to both new and existing arrangements (gov.uk guidance, last updated 19 June 2026). Reinforced by ERA 2025 extending guaranteed-hours duties to agency workers **with the hirer responsible by default** (SCHEDULED 2027). |
| 6 | **Solved today by** | Accreditation badges (FCSA, Professional Passport) checked once at onboarding; annual supply-chain audits by accountants; spreadsheets of approved umbrellas; hope. |
| 7 | **Named incumbents** | **SafeRec** (AI payslip auditing, sold agency-side), **Professional Passport**, **FCSA** accreditation, **Workwell**. All are oriented to accrediting the *umbrella*, not to giving the *end client* a per-period reconciliation it can show HMRC. Pricing not published by any of them. |
| 8 | **Willingness to pay** | £2,000–£15,000/yr. Anchor: agencies already pay four-figure annual sums for FCSA/Professional Passport accreditation and for SafeRec auditing; the downside anchor is uncapped PAYE recovery. |
| 9 | **Data required** | Customer-supplied: assignment records, agency invoices, umbrella payslips/RTI confirmations. Externally sourced: Companies House filings, HMRC named-avoidance-scheme list. All licensable/public. |
| 10 | **Cloudflare fit** | Strong. Document ingest → R2; reconciliation → Workers + Queues; ledger → D1. No GPU, no scraping of blocking sites. **4/5** (payslip OCR may need an external model call). |
| 11 | **5–10 year durability** | Survives to 2031+ if umbrella working survives. **What kills it:** HMRC abolishing umbrella intermediation outright (repeatedly floated); or SafeRec pivoting to the client side and owning it. Moderate risk. |
| 12 | **Evidence** | Class 4 (regulator instrument): https://www.gov.uk/guidance/paye-rules-for-labour-supply-chains-that-include-umbrella-companies-from-6-april-2026 · Class 4: ERA 2025 c.36 agency-worker provisions, https://www.legislation.gov.uk/ukpga/2025/36/contents · Class 3 (pricing/market): accreditation market as described above — **pricing not published; marked partially [UNVERIFIED]**. |

**Scores:** Pain 5 · Forcing 5 · Buyers 3 · WTP 4 · Incumbency 2 · Moat 3 · Cloudflare 4 · Durability 3 = **29**

---

### CANDIDATE 2 — Holiday entitlement & pay evidence vault · **27/40**

| # | Field | |
|---|---|---|
| 1 | **The gap** | Since 6 April 2026 employers must keep records adequate to show compliance with holiday entitlement *and holiday pay* for **six years**, and failure is a criminal offence. Variable-hours employers calculate accrual at 12.07% of hours worked and often pay rolled-up holiday pay; the calculation lives in payroll runs and spreadsheets, is not retained as an auditable entitlement record, and does not survive a change of payroll provider. |
| 2 | **Pain owner** | Payroll Manager; Head of Reward. |
| 3 | **Budget holder** | HR Director or Finance Director. Payroll opex. |
| 4 | **UK buyer count** | Employers with large variable-hours populations: multi-site retail/hospitality/leisure (~5,700 with 5+ sites), plus recruitment agencies, care providers, and education. **Winnable: ~3,000–6,000.** At £1,000 ACV × 3,000 = £3m ARR. Credible. |
| 5 | **Forcing function** | **BINDING.** Annual-leave record-keeping duty, in force **6 April 2026**, six-year retention, criminal offence for breach. Confirmed by Acas (statutory body) and independently by Lewis Silkin and Hill Dickinson trackers. |
| 6 | **Solved today by** | The payroll system, while you remain its customer. Spreadsheets for accrual. Nothing for six-year immutable retention across provider migration. |
| 7 | **Named incumbents** | **Sage**, **IRIS**, **MHR**, **Moorepay**, **Dayforce**, plus WFM vendors (**Deputy** ~£3.50/user/mo, **Planday** £2.99/user/mo). None markets a six-year portable entitlement audit trail; all retain data only for the life of the contract. |
| 8 | **Willingness to pay** | £1,000–£8,000/yr. Anchor: a holiday-pay remediation exercise after an audit or tribunal typically runs to five figures in professional fees; WFM spend of £110–£130/month per 25-head site is already accepted. |
| 9 | **Data required** | Customer-supplied payroll and timesheet extracts only. No external licensing. |
| 10 | **Cloudflare fit** | Excellent. Immutable append-only ledger in D1/R2, scheduled ingest via Queues. **5/5.** |
| 11 | **5–10 year durability** | **Weak.** What kills it: the payroll incumbents shipping retention as a checkbox, which costs them almost nothing. This is a 24–36 month window, not a decade. Score honestly. |
| 12 | **Evidence** | Class 4: Acas, https://www.acas.org.uk/employment-rights-act-2025 · Class 4: ERA 2025 c.36, https://www.legislation.gov.uk/ukpga/2025/36/contents · Class 3: Deputy/Planday published per-user pricing; Trail £32–£82.50/site/mo, https://www.trailapp.com/pricing |

**Scores:** Pain 4 · Forcing 5 · Buyers 4 · WTP 3 · Incumbency 2 · Moat 2 · Cloudflare 5 · Durability 2 = **27**

---

### CANDIDATE 3 — Martyn's Law enhanced-tier assurance + estate/event notification register · **27/40**

| # | Field | |
|---|---|---|
| 1 | **The gap** | A multi-site operator with 200+ premises must classify every site as out-of-scope / standard / enhanced against a capacity model, notify the SIA per premises, re-notify within 28 days of any change, notify every qualifying public event within 14 days of publicising it, run an annual documented terrorism risk assessment per enhanced site, and evidence that a continuously churning workforce is trained on current procedures. No system holds that register. |
| 2 | **Pain owner** | Group Head of Security / Head of Risk & Compliance; at enhanced-tier sites, the statutory **Designated Senior Individual**. |
| 3 | **Budget holder** | COO or Group Risk Director. Insurance/risk or property-operations line. |
| 4 | **UK buyer count** | 24,268 enhanced-tier premises exist, of which **22,165 (91%) sit in this analyst's sectors** (retail & hospitality 15,997; sports facilities 2,859; visitor attractions 1,561; zoos/theme parks 386; stadiums/arenas 268; racecourses 61; hotels 58; festivals 975). Premises ≠ buyers: enhanced-tier sites concentrate in multi-site estates. Estimated ~1,100 multi-site operators holding ≥1 enhanced site, plus ~2,500 independent enhanced operators = ~3,600 gross; discount ~25% foreign-parented (tooling decided abroad); discount again for those who will bolt it onto an existing H&S GRC platform. **Winnable: ~800–1,200.** For £3m ARR at 1,000 buyers, ACV = £3,000 — which is 58% of the Home Office's entire modelled annual enhanced-tier cost. **Tight.** |
| 5 | **Forcing function** | **SCHEDULED**, and advancing. Terrorism (Protection of Premises) Act 2025 (c.10), RA 3 April 2025. Commencement No.1 Regs 2026 (SI 2026/320); **Commencement No.2 Regs 2026 (SI 2026/622), provisions in force 15 June 2026**; **Notification Requirements Regs 2026 (SI 2026/793)**; **Principal Use of Premises Regs 2026 (SI 2026/1005)**. Main duties expected **Spring 2027**. Not yet BINDING on operators. |
| 6 | **Solved today by** | Word templates from ProtectUK; counter-terrorism security advisers; an H&S consultant; nothing at estate level. |
| 7 | **Named incumbents** | **Momentus** (venue risk/incident management, enhanced-tier positioning, no public pricing); **standardtier.co.uk** (**£18/mo**, discounted from £38); **martynslawsoftware.co.uk** (**£19 / £29 / £79 per month**); generic EHS GRC (**Alcumus**, **Evotix**, **EcoOnline**) which will absorb this as a module. |
| 8 | **Willingness to pay** | £1,500–£8,000/yr for an estate operator. Anchor: Home Office IA models **£52,093 ten-year PV per enhanced-tier premises** (~£5,209/yr) and £3,313 per standard-tier premises; Trail proves £384–£990/site/yr is payable in this buyer set. |
| 9 | **Data required** | Customer-supplied: site list, floor areas, capacities, licences, staff roster. Externally sourced: OS AddressBase-style floorspace (licensable, paid), fire-safety crowd-density factors (public, Approved Document B), SIA register once published. |
| 10 | **Cloudflare fit** | Excellent — documents, registers, scheduled reminders. **5/5.** |
| 11 | **5–10 year durability** | The statute will not be repealed; it is a memorial to a public inquiry. **What kills it:** (a) it settles into an annual form and a £20/month commodity, which is already happening at the standard tier; (b) Alcumus/Evotix ship a Martyn's Law module to their existing estate customers at zero marginal CAC. |
| 12 | **Evidence** | Class 4: Home Office TPoP Impact Assessment, Table 1 and cost model, https://assets.publishing.service.gov.uk/media/66e30684e47cfc6de429d612/TPOP_Signed_IA.pdf · Class 4: SI 2026/793, https://www.legislation.gov.uk/uksi/2026/793/contents/made · Class 3: standardtier.co.uk £18/mo; martynslawsoftware.co.uk £19–£79/mo. |

**Scores:** Pain 4 · Forcing 4 · Buyers 3 · WTP 3 · Incumbency 3 · Moat 2 · Cloudflare 5 · Durability 3 = **27**

---

### CANDIDATE 4 — Multi-site regulatory permission & obligation register ("estate passport") · **26/40**

| # | Field | |
|---|---|---|
| 1 | **The gap** | A 300-site estate cannot answer, on demand, which premises licence conditions apply where, who the DPS is, which personal licences expire when, which sites are enhanced-tier under Martyn's Law, which hold a food hygiene rating below 4, and which have an outstanding allergen or age-verification action. The answer lives in a solicitor's filing cabinet and six spreadsheets. |
| 2 | **Pain owner** | Group Licensing Manager / Head of Compliance. |
| 3 | **Budget holder** | Property & Operations Director. |
| 4 | **UK buyer count** | Businesses with 5+ sites in retail/hospitality/leisure ≈ 5,700, of which those with licensed or food-serving estates ≈ 3,500; discount foreign-parented and those already inside Zonal/Access suites. **Winnable: ~2,000–3,000.** |
| 5 | **Forcing function** | **Mixed BINDING, no single driver.** Licensing Act 2003 (in force); Employment (Allocation of Tips) Act 2023 + statutory Code (in force **1 October 2024**); Natasha's Law (in force 2021); DMCC Act 2024 Part 4 Ch.1 (in force **6/7 April 2025**); Martyn's Law (SCHEDULED 2027). **No one of these forces the purchase of *this* product** — which is the candidate's principal weakness under LAW 1. |
| 6 | **Solved today by** | Poppleston Allen / John Gaunt licensing retainers; SharePoint; Trail task lists; the memory of one long-serving manager. |
| 7 | **Named incumbents** | **Trail** (£32–£82.50 per site per month; food-safety logs and custom audits, **no Martyn's Law or security content found on its pricing page**); **Nory** (no published pricing); **Zonal**, **Airship**, **Access Group Hospitality Suite**, **Alcumus**. Trail owns the daily task layer; nobody visibly owns the *permission register* layer. |
| 8 | **Willingness to pay** | £6,000–£40,000/yr for a 100–500 site estate. Anchor: Trail at £65/site/mo annual = £78,000/yr for 100 sites, so a £15k register sits comfortably beneath existing accepted spend. |
| 9 | **Data required** | Customer-supplied site and licence data; externally sourced FSA food hygiene ratings (open data), local-authority licensing registers (fragmented, ~350 councils, inconsistent formats — this is the real work and the real moat). |
| 10 | **Cloudflare fit** | Good, with a caveat: harvesting 350 local-authority licensing registers means scraping sites of variable quality. **4/5.** |
| 11 | **5–10 year durability** | Decent — permission registers deepen with use. **What kills it:** Access Group or Zonal bundling it; or a national licensing register being published by government, which would commoditise the hardest input. |
| 12 | **Evidence** | Class 3: https://www.trailapp.com/pricing · Class 4: Employment (Allocation of Tips) Act 2023 statutory Code in force 1 Oct 2024, https://www.gov.uk/government/publications/distributing-tips-fairly-statutory-code-of-practice |

**Scores:** Pain 3 · Forcing 3 · Buyers 3 · WTP 4 · Incumbency 2 · Moat 3 · Cloudflare 4 · Durability 4 = **26**

---

### CANDIDATE 5 — Guaranteed-hours & shift evidence ledger (ERA 2025 ss.1–3) · **25/40**

| # | Field | |
|---|---|---|
| 1 | **The gap** | From 2027 an employer must, at the end of each rolling reference period, offer qualifying zero/low-hours workers a guaranteed-hours contract reflecting hours actually worked; give reasonable notice of shifts and changes; and pay for shifts cancelled, curtailed or moved at short notice — **unless the worker initiated it**. Defending a tribunal claim requires a per-shift, per-worker, timestamped record of who changed what and when. No one keeps that today. |
| 2 | **Pain owner** | Group Head of People Operations / Employee Relations Manager. |
| 3 | **Budget holder** | HR Director. |
| 4 | **UK buyer count** | Multi-site retail/hospitality/leisure with 5+ sites ≈ 5,700, plus large single-site employers (hotels, stadiums, universities). **Winnable: ~4,000–5,000** — the largest buyer pool in this report. |
| 5 | **Forcing function** | **SCHEDULED, with the operative detail still PROPOSED.** ERA 2025 c.36 ss.1–3. Reference-period length, hours threshold (Government preference 8–20 hrs/wk), "reasonable notice" presumption and payment amounts are all to be set in regulations. The consultation *Ending one-sided flexibility* closed **25 August 2026**; the Government response is outstanding as at today. **Per LAW 1, the detail carries no weight yet.** |
| 6 | **Solved today by** | The rota system's change log, if it has one; email; WhatsApp. |
| 7 | **Named incumbents** | **Access Group / Rotaready Evo** — already markets "contractual minimums with visual indicators showing whether guaranteed-hour obligations are met", rota publication weeks ahead, and change audit trails. **Fourth** (compliance page makes no mention of guaranteed hours, reference periods, cancellation payments or notice tracking — checked). **Sona**, **Deputy** (~£3.50/user/mo), **Planday** (£2.99/user/mo), **Bizimply**, **S4labour** (250+ UK clients), **Harri**, **Legion**, **UKG**. |
| 8 | **Willingness to pay** | £1,400–£10,000/yr per operator. Anchor: existing WFM spend of £110–£130/month per 25-head site. |
| 9 | **Data required** | Customer-supplied rota, timesheet and contract data. |
| 10 | **Cloudflare fit** | Good. **4/5.** |
| 11 | **5–10 year durability** | **Poor.** What kills it: the WFM incumbent ships it — and Access already says it has. This is a feature, not a company. |
| 12 | **Evidence** | Class 4: ERA 2025 c.36 ss.1–3, https://www.legislation.gov.uk/ukpga/2025/36/contents; DBT factsheet *Reforms of zero hours and similar contracts* · Class 3: Access Group product claims, https://www.theaccessgroup.com/en-gb/blog/hos-zero-hours-contracts-in-uk-hospitality-after-the-employment-rights-act/; Fourth compliance page, https://uk.fourth.com/solution/workforce-management/compliance |

**Scores:** Pain 4 · Forcing 3 · Buyers 4 · WTP 4 · Incumbency 2 · Moat 2 · Cloudflare 4 · Durability 2 = **25**

---

### Candidates 6–11 — summary (all 12 fields held in working notes; headline verdicts here)

**6 · Qualifying public event notification & event-level CT assurance — 24/40.**
Every qualifying public event (800+, controlled access) must be notified to the SIA **within 14 days
of being publicised**, with a further 14 days to correct inaccurate information (SI 2026/793 reg 3).
Unlike premises, this is genuinely *repeat-transactional*. Buyers: festival and event organisers,
promoters, agricultural shows, local authorities — call it **2,000–4,000**, of which festivals alone
number 975 in the Home Office model. Penalties for events reach £18m/5% of global turnover plus
£50,000/day. **Why it does not rank higher:** buyer count is modest, seasonality makes revenue lumpy,
and Momentus already sells into exactly this room. Pain 4 · Forcing 4 · Buyers 3 · WTP 3 ·
Incumbency 3 · Moat 2 · Cloudflare 5 · Durability 3? — recorded as 3 → **27 gross, 24 on a
conservative durability read.** Worth folding into Candidate 3 rather than building separately.

**7 · Martyn's Law standard tier (200–799) — REJECTED.** See §5. Willingness-to-pay axis scores **1**
(the Home Office models £132/year of avoidable labour). Automatic rejection under Part C.

**8 · Charity governance, annual return & impact reporting — 22/40.** Verified buyer pool is far
smaller than the sector headline: of 171,867 registered charities in England and Wales, **128,435
(74.7%) have income under £100,000** and buy nothing. The software-capable population is the
**15,334 with income over £500k** and realistically the **9,302 over £1m**. The Annual Return itself
is a free Commission portal form. Incumbents own the CRM layer: **Blackbaud**, **Beacon**
(£37–£325/month published), **Donorfy**, **Access Charity CRM**, **Salesforce NPSP**. Incumbency 2,
Forcing 2 (Charity Commission reporting is BINDING but long-standing and not newly onerous). Not
recommended.

**9 · DMCC price transparency & fake-review prevention evidence — 21/40.** The regime is genuinely
**BINDING from 6/7 April 2025**, with CMA *direct* enforcement and fines to **10% of global
turnover**, and the CMA's stated first-year priorities are hidden fees and drip pricing. But the duty
to prevent fake reviews is already absorbed by **Trustpilot, Feefo, Reviews.io, Yotpo, Bazaarvoice**,
and price-presentation changes are a one-off engineering task on a checkout, not a subscription.
Incumbency 2, Durability 2. The subscription-contracts regime (DMCC ss.253–281) is **not yet
commenced** — PROPOSED for practical purposes — and is the one part worth re-checking in 2027, since
it will force reminder notices, cooling-off and easy-exit flows on every gym, subscription box and
streaming service in the country.

**10 · Online Safety Act compliance for mid-sized UK services — 20/40.** BINDING: illegal-content
duties enforceable **17 March 2025**, children's risk assessments due **24 July 2025**, age assurance
for pornographic content from **17 January 2025**, fines to **£18m or 10% of qualifying worldwide
revenue**. But neither DSIT nor Ofcom publishes a figure for in-scope services that I could verify in
this run — **marked [UNVERIFIED]** — and the UK-headquartered, budget-holding subset is small relative
to the noise. Incumbents: **OneTrust**, **Tremau**, **Cinder**, **ActiveFence**, **Checkstep**.

**11 · Film/TV production tax-credit evidence pack (AVEC/IFTC) — 19/40.** A real new BINDING
administrative requirement: claims submitted **on or after 6 April 2026** must include the **CT600P
Creative Industries supplementary page**, alongside a BFI British cultural certificate and a
UK/non-UK core-cost split. Rates: 34% general, 39% animation/children's TV and VFX, **53% independent
film** (budgets under £23.5m core cost, cap £15m). **But the buyer count fails LAW 2**: the work is
done by perhaps 20 specialist accountancy practices and 150–250 active production companies, mostly
on contingent fees, against strong incumbents (**Sargent-Disc/Cast & Crew**, **Entertainment
Partners**, **Wrapbook**, **Greenslate**). Buyer-count axis scores **2**; ACV would need to exceed
£15,000 for £3m ARR. Not recommended as a standalone.

---

## 5. Deep section — Martyn's Law: honest verdict

**The instrument.** Terrorism (Protection of Premises) Act 2025 (c.10), Royal Assent 3 April 2025.
Government committed to an implementation period of "at least 24 months". As at today the regime is
part-commenced: **SI 2026/320** (Commencement No.1), **SI 2026/622** (Commencement No.2, provisions
in force **15 June 2026** — principally s.12, requiring the SIA to produce statutory guidance on its
regulatory functions, and s.18(5)–(7) on "qualifying worldwide revenue"), **SI 2026/793**
(Notification Requirements) and **SI 2026/1005** (Principal Use of Premises). Home Office s.27
statutory guidance published **15 April 2026**. The SIA's s.12 enforcement consultation closed
**12 June 2026**, with final guidance and a consultation report due autumn 2026. Operator duties are
expected to commence **Spring 2027**. Grade: **SCHEDULED**, not BINDING.

**The obligated population — verified, not estimated.** The Home Office impact assessment models
928,554 publicly accessible locations in the UK, of which **749,662 are out of scope**, **154,623 are
standard tier** and **24,268 are enhanced tier** (total in scope: **178,891**). Sensitivity range:
standard 123,900–177,000; enhanced 17,800–31,100. By sector, the standard tier is dominated by
**retail and hospitality (84,617)**, **places of worship (33,323)** and **education (24,689)**; the
enhanced tier by **retail and hospitality (15,997)**, **sports facilities (2,859)**, **hospitals
(1,921)**, **visitor attractions (1,561)** and **festivals (975)**. **91% of the enhanced tier sits in
this analyst's sectors.** The brief's "100,000+ standard tier" is correct and conservative.

**What compliance actually requires.**
*Standard tier (200–799):* notify the SIA of the premises and responsible person; put in place
public protection **procedures** — evacuation, invacuation, lockdown, communication; make staff aware.
**No physical measures are mandated, no risk assessment is required, and nothing is submitted to the
regulator beyond the notification.**
*Enhanced tier (800+):* all of the above, plus a documented **terrorism risk assessment**, **public
protection measures** (monitoring, movement, physical security, information security) so far as
reasonably practicable, a **Designated Senior Individual**, and **documentation submitted to the SIA**.
*Notification cadence (SI 2026/793 reg 3):* premises must notify by the later of **three months from
commencement day** or **28 days from becoming responsible**; changes must be notified within **28
days**; qualifying events within **14 days** of being publicised, and event changes within **14 days**.
*Enforcement:* civil-led. Maximum fixed penalty **£18m or 5% of worldwide turnover** for enhanced
premises and qualifying events; daily penalties up to **£500/day (standard)** and **£50,000/day
(enhanced/events)**; restriction notices to close enhanced premises in rare cases; criminal
prosecution only for breach of a compliance or restriction notice at the enhanced tier, and for
obstructing the regulator. Breach is **not actionable in civil proceedings**. The SIA is recruiting
**100+ operational posts** and has stated an "advisory-first" posture.

**One-off form, or ongoing SaaS? The government's own numbers answer this.**
- Standard tier ongoing burden: **4.5 hours per year** of procedure review (halved from the set-up
  year), plus training refreshed **two-yearly**. Ten-year PV cost **£3,313** per premises.
- Enhanced tier ongoing burden: **15 hours per year** for the risk assessment, plus two-yearly
  training and maintenance of physical measures. Ten-year PV cost **£52,093** per premises.
- Inspection probability: **1% of standard-tier premises per year**, **5% of enhanced-tier premises
  per year**. Expected civil monetary penalties across the whole regime: **1–4 per year**.

**Verdict.** For the 154,623 standard-tier premises, **Martyn's Law is a one-off form with a biennial
reminder, not a SaaS**. A £132/year labour burden, a 1% annual inspection probability, and an
advisory-first regulator do not create a buying moment. The market has already priced this correctly:
two vendors are live at **£18** and **£19 per month**, and one of them openly describes itself as "a
small UK operation" and refuses to claim it makes you compliant. That is a commodity template
business, not a durable one. **Recommendation: do not build for the standard tier.**

For the **24,268 enhanced-tier premises** the picture inverts. An annually refreshed documented risk
assessment, a named individual carrying personal accountability, documents filed with a regulator,
a 5% annual inspection rate, £50,000/day penalties and criminal exposure for breaching a compliance
notice constitute a real, recurring, liability-bearing obligation. **But the buyers are ~800–1,200
estate operators, not 24,000 premises** — and the required ACV of ~£3,000 sits uncomfortably close to
the entire modelled annual cost of compliance.

**The one thing that makes Martyn's Law genuinely ongoing, and which the impact assessment gets
wrong:** it assumes training is a two-yearly batch event. In hospitality and retail, with annual
staff turnover widely reported above 30% *(figure [UNVERIFIED] — could not be confirmed in this run)*,
"all relevant staff are trained on the current procedures" is a **continuous** obligation, not a
biennial one. A 500-site group hires thousands of people a year, every one of whom must be trained
before working a shift at an in-scope premises. Evidencing that continuously, per site, per shift,
against a version-controlled procedure, is the only part of Martyn's Law that behaves like software.
It is also the part most exposed to incumbency, because **Flow, Access Learning, CPL Learning and
Attensi** already sell hospitality onboarding LMS.

---

## 6. Deep section — Employment Rights Act 2025: what is actually operational, and whether WFM covers it

**Correct citation:** Employment Rights Act **2025**, c. 36. Guaranteed hours = **s.1**; reasonable
notice of shifts = **s.2**; payment for cancelled, moved or curtailed shifts = **s.3**; unfair
dismissal qualifying period and compensation = **s.25**; statutory sick pay = **s.10** (GB) / **s.12**
(NI).

**Verified staging timetable** (triangulated across Acas, DLA Piper, Hill Dickinson, Lewis Silkin):

| Date | Measure | Grade |
|---|---|---|
| Feb 2026 | Trade Union Act 2016 repeals; notice for day-one paternity/parental leave | BINDING |
| **6 April 2026** | **SSP from day one, lower earnings limit removed** (80% of earnings for low earners) | **BINDING** |
| **6 April 2026** | **Annual-leave records duty — 6-year retention, criminal offence for breach** | **BINDING** |
| 6 April 2026 | Day-one paternity & unpaid parental leave; collective redundancy protective award doubled to 180 days | BINDING |
| 7 April 2026 | Fair Work Agency established | BINDING |
| Aug 2026 | Electronic and workplace balloting | BINDING |
| **Oct 2026** | **Tribunal time limits extended to six months**; strengthened sexual-harassment duty incl. third-party liability | BINDING |
| **1 Jan 2027** | **Unfair dismissal qualifying period cut to 6 months** (not day one); **compensation cap removed**; fire-and-rehire restrictions | SCHEDULED |
| 2027 (date TBC) | **Guaranteed hours, shift notice, cancellation payments** (incl. agency workers) | SCHEDULED; detail PROPOSED |

**Who now has to track what nobody tracked before?** Four things:

1. **The rolling reference period per worker.** Expected ~12 weeks, but the length is not yet in
   regulations. An employer must detect, per worker, when average hours over the period exceed the
   contractual minimum, and then generate an offer. Repeatedly, after each period.
2. **The guaranteed-hours offer and the worker's response.** Offer made, date, terms, accepted or
   declined. A declined offer is the employer's entire defence.
3. **Notice given per shift, and per change.** Not just the rota, but *when it was published* and
   *when each subsequent change was communicated*.
4. **Attribution of every cancellation.** The statutory test turns on whether the cancellation,
   curtailment or movement was **employer-initiated or worker-initiated** — including shift swaps
   agreed between two workers, which attract no payment. If the system cannot distinguish a manager
   cutting a shift from two staff swapping it in a WhatsApp group, the employer pays.

Item 4 is the genuinely new data object. Items 1–3 are reporting layers over data WFM already holds.

**Do the incumbents cover it?** Partially, and the strongest one says it already does.

- **Access Group / Rotaready Evo** — explicitly markets recording of contractual minimums with
  "visual indicators showing whether guaranteed-hour obligations are met", rota publication weeks in
  advance with automatic notifications, and audit trails of when changes occurred and what changed.
  That covers items 1–3. Access is a >£1bn-revenue software group. **This is the incumbency answer.**
- **Fourth** — its UK labour-and-wage compliance page names HMRC-compliant payroll, work-rule alerts,
  labour forecasting, absence/break monitoring and document handling. It makes **no mention** of the
  Employment Rights Act, guaranteed hours, reference periods, cancellation payments or notice
  tracking. Fourth publishes commentary on the Act but has not, on the evidence of its own product
  page, shipped against it.
- **Sona** — markets predictable-pattern monitoring, day-one SSP absence tracking and "audit trails
  showing what happened, when and why". Positioning, not a demonstrated reference-period engine.
- **Deputy (~£3.50/user/mo), Planday (£2.99/user/mo), Bizimply, S4labour (250+ UK clients), Harri,
  Legion, UKG** — all in the room.

**Conclusion.** The Employment Rights Act is a real forcing event for these sectors, but it is a
*feature* forcing event, and the incumbents get to ship the feature to an installed base at zero
CAC. A standalone guaranteed-hours product is a 2027 land-grab against Access Group. **The only
defensible wedges are the ones the WFM vendors structurally cannot reach: (a) the agency/umbrella
three-party reconciliation, where the hirer is liable by default but the data sits with the agency
(Candidate 1), and (b) the six-year holiday-records vault that must outlive the payroll contract
itself (Candidate 2).**

---

## 7. Graveyard — where the gaps are already owned

| Gap | Who owns it | Pricing | Verdict |
|---|---|---|---|
| Martyn's Law standard tier | standardtier.co.uk; martynslawsoftware.co.uk | **£18/mo**; **£19/£29/£79 per month** | Commoditised before the law commences |
| Martyn's Law venue risk (enhanced) | Momentus | Not published | Partially owned; estate-level register still open |
| Guaranteed hours / shift notice | **Access Group / Rotaready Evo**; Sona; Fourth; Deputy; Planday; Bizimply; S4labour; Harri; Legion; UKG | Deputy ~£3.50/user/mo (min £20); Planday £2.99/user/mo | Access already claims the feature |
| Daily site compliance & food safety logs | **Trail** | **£32–£82.50 per site per month** | Owned. Trail is the default answer for "checklist compliance" |
| Restaurant ops / inventory / forecasting | Nory; Zonal; Access Hospitality | Not published | Owned |
| Charity CRM, fundraising, Gift Aid | **Blackbaud**; **Beacon**; Donorfy; Access Charity CRM; Salesforce NPSP | Beacon **£37 / £127 / £325 per month** | Owned |
| Fake review detection | Trustpilot; Feefo; Reviews.io; Yotpo; Bazaarvoice | Not published | Owned |
| Online safety / trust & safety compliance | OneTrust; Tremau; Cinder; ActiveFence; Checkstep | Not published | Owned |
| Umbrella company compliance (agency side) | SafeRec; Professional Passport; FCSA; Workwell | Not published | Owned agency-side; **end-client side is the gap** |
| Tips / tronc administration | TiPJAR; EasyTip; WMT Troncmaster; Fourth & S4labour tronc modules | Not published | Owned |
| Production payroll & tax-credit claims | Sargent-Disc (Cast & Crew); Entertainment Partners; Wrapbook; Greenslate; specialist accountants on contingent fees | Contingent 2–5% | Owned |
| EPOS / payments / e-commerce | Shopify; Lightspeed; Zettle; Square | Public | Owned, saturated |
| EHS / risk GRC (will absorb Martyn's Law) | Alcumus; Evotix; EcoOnline | Not published | Likely future owner of Candidate 3 |

**Reading of the graveyard.** Fourteen of the sixteen obvious gaps in these sectors have a named,
funded incumbent with a published or inferable price. The two that do not — **end-client umbrella PAYE
liability** and **six-year portable holiday-records retention** — are both liability-shifting
obligations that arrived on the same day, **6 April 2026**, and both sit in the seam *between*
existing vendors rather than inside any one of them. That is not a coincidence; it is where new
statutory liability lands when it is drafted to catch the party with the deepest pockets rather than
the party with the data.

---

## 8. Disconfirming evidence, reported prominently (Hard Rule 3)

1. **Martyn's Law standard tier is dead as a SaaS market, and the Home Office's own impact assessment
   proves it.** £132/year of ongoing avoidable labour; 1% annual inspection probability; 1–4 civil
   penalties expected per year across all 178,891 in-scope premises. Two vendors are already at £18–19
   per month. This is the single most valuable finding in this report because it kills the biggest
   number in the brief.
2. **"Day-one unfair dismissal" does not exist.** It became a six-month qualifying period via a Lords
   amendment. Any thesis resting on day-one rights is resting on a headline, not a statute.
3. **Access Group has pre-announced the guaranteed-hours feature.** Rotaready Evo's marketing already
   describes contractual-minimum indicators and change audit trails. The largest buyer pool in this
   report (4,000–5,000) is the one with the strongest incumbent.
4. **The charity sector is three-quarters unbuyable.** 128,435 of 171,867 registered charities have
   income under £100k. The real buyer pool is 15,334, and Blackbaud, Beacon and Donorfy already hold it.
5. **The multi-site pond is 12,615 businesses.** Every "estate compliance" thesis in retail and
   hospitality, including two of my own candidates, is constrained by this number.
6. **Evidence class 1 and 2 are missing from this report.** No job postings, no procurement records.
   The buyer counts are modelled from ONS and Home Office data, not observed from hiring or spending
   behaviour. A red team should attack them there first.

---

## 9. Sources

**Primary instruments and regulator datasets (LAW 3 class 4)**
- Terrorism (Protection of Premises) Act 2025 c.10 — https://www.legislation.gov.uk/ukpga/2025/10/contents
- Terrorism (Protection of Premises) Act 2025 (Commencement No.2) Regulations 2026, SI 2026/622 — https://www.legislation.gov.uk/uksi/2026/622/contents/made
- Terrorism (Protection of Premises) (Notification Requirements) Regulations 2026, SI 2026/793 — https://www.legislation.gov.uk/uksi/2026/793/contents/made (reg 3 fetched directly)
- Terrorism (Protection of Premises) (Principal Use of Premises) Regulations 2026, SI 2026/1005
- Home Office, *Terrorism (Protection of Premises) Impact Assessment* (signed) — https://assets.publishing.service.gov.uk/media/66e30684e47cfc6de429d612/TPOP_Signed_IA.pdf (Table 1, paras 83–85, 109, 152–160)
- SIA / gov.uk, *Understanding Martyn's Law and the SIA's role as regulator* — https://www.gov.uk/guidance/understanding-martyns-law-and-the-sias-role-as-regulator
- ProtectUK, *Martyn's Law overview* — https://www.protectuk.police.uk/martyns-law/martyns-law-overview-and-what-you-need-know
- Employment Rights Act 2025 c.36 — https://www.legislation.gov.uk/ukpga/2025/36/contents
- DBT, *Factsheet: Reforms of zero hours and similar contracts* — https://assets.publishing.service.gov.uk/media/6a1d6024c7335e2ca6daad8c/zero-hours-contracts.pdf
- Acas, *Employment Rights Act 2025* — https://www.acas.org.uk/employment-rights-act-2025
- HMRC, *PAYE rules for labour supply chains that include umbrella companies from 6 April 2026* — https://www.gov.uk/guidance/paye-rules-for-labour-supply-chains-that-include-umbrella-companies-from-6-april-2026
- Digital Markets, Competition and Consumers Act 2024 c.13 — https://www.legislation.gov.uk/ukpga/2024/13/contents
- CMA, *New consumer protection regime comes into force* — https://www.gov.uk/government/news/cma-to-boost-consumer-and-business-confidence-as-new-consumer-protection-regime-comes-into-force
- DSIT, *Online Safety Act explainer* — https://www.gov.uk/government/publications/online-safety-act-explainer/online-safety-act-explainer
- DBT, *Distributing tips fairly: statutory code of practice* — https://www.gov.uk/government/publications/distributing-tips-fairly-statutory-code-of-practice
- HMRC, *Claiming Audio-Visual Expenditure Credits for Corporation Tax* — https://www.gov.uk/guidance/claim-audio-visual-expenditure-credits-for-corporation-tax
- FSA, *Allergen information for non-prepacked foods: best practice* (20 Feb 2025) — https://www.gov.uk/government/publications/allergen-information-for-non-prepacked-foods-best-practice-summary
- ONS, *UK business: activity, size and location 2025* — https://www.ons.gov.uk/businessindustryandtrade/business/activitysizeandlocation/bulletins/ukbusinessactivitysizeandlocation/2025
- ONS, *Business demography, UK: 2024* — https://www.ons.gov.uk/businessindustryandtrade/business/activitysizeandlocation/bulletins/businessdemography/2024
- Charity Commission for England and Wales, *Sector overview* and *Charities by income band*, data as at **18 September 2026** — https://register-of-charities.charitycommission.gov.uk/en/sector-data/sector-overview

**Competitor pricing and product pages (LAW 3 class 3)**
- Trail — https://www.trailapp.com/pricing (£32–£82.50 per site per month)
- Beacon CRM — https://beaconcrm.org/pricing/ (£37 / £127 / £325 per month)
- martynslawsoftware.co.uk (£19 / £29 / £79 per month)
- standardtier.co.uk — https://www.standardtier.co.uk/guide/martyns-law-timeline (£18/month)
- Momentus — https://gomomentus.com/blog/martyns-law-urgent-steps-to-protect-your-venue-from-terrorism
- Fourth, labour & wage compliance — https://uk.fourth.com/solution/workforce-management/compliance
- Access Group / Rotaready Evo — https://www.theaccessgroup.com/en-gb/blog/hos-zero-hours-contracts-in-uk-hospitality-after-the-employment-rights-act/
- Sona — https://www.sona.ai/blog/employee-rights-act-hospitality
- Deputy / Planday per-user pricing via Workforce.com UK buyers' guide 2026

**Commentary (class 6–7, used only for timetable triangulation, never alone)**
- DLA Piper, revised ERA implementation timeline (2026)
- Lewis Silkin, *What's in the Employment Rights Act* (10 July 2026)
- Hill Dickinson, ERA 2025 implementation tracker
- Institute of Licensing, *SIA outlines progress towards Martyn's Law regulation*
- The Ops Con, *Martyn's Law: the SIA's guidance duties switch on* (June 2026)
