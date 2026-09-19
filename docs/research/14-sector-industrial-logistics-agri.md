# 14 — UK Sector Scan: Manufacturing, Transport & Logistics, Agriculture & Food

**Agent:** UK Sector Analyst — Manufacturing, Transport & Logistics, Agriculture & Food
**Date:** 19 September 2026
**Method:** `docs/method/01-opportunity-scoring-rubric.md` (binding)
**Status:** Wave 1 sector sweep. Candidates scored for cross-sector comparison.

> **Research budget note (honesty first).** The session's shared WebSearch quota (200 calls) was
> exhausted by other agents partway through this sweep. This report rests on **12 web searches and
> 24 web fetches**, weighted heavily toward primary sources: `legislation.gov.uk`, `gov.uk` guidance
> and statistics, HMRC impact notes, the Traffic Commissioners' annual report, ONS business counts,
> and vendor pricing pages. Where a claim could not be verified by fetch it is tagged
> `[UNVERIFIED]`. The fetch count exceeds the brief's requirement; the search count does not, and I
> am flagging that rather than padding it.

---

## Executive summary — top 5 candidates ranked

| # | Candidate | Winnable UK buyers | Score /40 | Verdict |
|---|---|---|---|---|
| 1 | **Packaging EPR recyclability (RAM) assessment & modulated-fee defence** | ~1,800 of 6,936 large producers | **30** | Strongest. Money is already moving, the burden is self-assessed, and the penalty multiplier doubles by 2028-29. Weak axis: compliance schemes own the customer. |
| 2 | **UK CBAM liability engine + carbon price relief evidence pack** | ~500–800 of ~2,000 obligated importers | **28** | Real, dated, genuinely unserved *today* — but a small budget envelope and a serious ETS-linkage tail risk. Deep treatment below. |
| 3 | **Deposit Return Scheme producer onboarding (Oct 2027)** | ~1,200 drinks producers/importers | **26** | Right shape, wrong time. Deposit level and producer fee still unpublished. Revisit Q2 2027. |
| 4 | **Multi-regime packaging & product data spine (EPR + DRS + PPT + Simpler Recycling)** | ~2,500 | **25** | The consolidation play. Loses on incumbency to Valpak/Ecosurety unless sold as a data layer *beneath* them. |
| 5 | **Food & drink supplier specification / allergen data exchange** | ~4,000 manufacturers and wholesalers | **23** | Large buyer count, chronic pain, but Erudus/Kafoodle/Nutritics/Ideagen are entrenched. Marginal. |

**Four candidates were killed outright by LAW 4** and are documented in the Graveyard: O-licence
compliance evidence (73 DVSA-validated vendors), manufacturing QMS/CAPA (Ideagen: 18,500+
organisations), customs declarations (80+ CDS software developers listed by HMRC), and UK ETS
energy-from-waste MRV (**the expansion was delayed on 26 August 2026 with no replacement date** —
LAW 1 kill).

**Headline UK CBAM verdict:** the regime is real and dated, no existing CBAM vendor covers it, and
there is a genuine 12-month window. But the product is **not** the supplier-emissions-survey
business that the EU CBAM vendors built. UK CBAM permits default values, the statutory return asks
for commodity code, weight, origin and carbon price relief — not per-installation emissions — and
HMRC budgets the entire continuing compliance burden at **£16m/year across all affected business**.
It is a tax-optimisation product sitting on customs data, and the realistic ACV is £4k–£12k.

---

## Sector structure

| Sub-sector | UK businesses | Typical software spend | Regulator | Source |
|---|---|---|---|---|
| Manufacturing | **130,000** VAT/PAYE-registered | Low. Dominated by micro-firms; ERP penetration concentrated in the >50-employee tail | HSE, EA, OPSS, MHRA (pharma) | [ONS UK business: activity, size and location 2025](https://www.ons.gov.uk/businessindustryandtrade/business/activitysizeandlocation/bulletins/ukbusinessactivitysizeandlocation/2025) |
| Transport & storage | **114,000** (down 2.1% YoY; road freight down **5.3%**, lowest since 2015) | £15–£50 per vehicle per month for compliance/telematics | DVSA, Traffic Commissioners | ONS 2025; [FleetEase pricing](https://fleetease.co.uk/) |
| Agriculture, forestry & fishing | **141,000** | Very low. Farm software is £500–£3,000/yr | Defra, RPA, EA, APHA | ONS 2025 |
| Food businesses (all establishments incl. retail/catering) | **~613,000** registered with local authorities | Bimodal: £19/mo SME tools to enterprise quotes | FSA, local authority EHOs | [FHRS aggregate data, Sept 2026](https://hygienescout.co.uk/blog/uk-food-hygiene-ratings-2026) |
| Goods vehicle operator licences in force | **66,222** (+ 5,280 PSV) | As above | Traffic Commissioners | [TC Annual Report 2024-25](https://www.gov.uk/government/publications/traffic-commissioners-annual-report-2024-to-2025/traffic-commissioners-for-great-britain-annual-report-2024-25) |
| Packaging EPR large producers | **6,936** (submitted 2024 data by 11 June 2025) | £5k–£50k/yr compliance scheme membership + fees | EA / PackUK / Defra | [ERP UK EPR guide 2026](https://erp-recycling.org/uk/news-and-events/2026/04/uk-packaging-epr-compliance-guide-for-2026/) |
| CBAM-good importers | **~10,000**; **~2,000** above the £50k threshold | Nil today | HMRC | [HMRC CBAM policy paper](https://www.gov.uk/government/publications/introduction-of-carbon-border-adjustment-mechanism/carbon-border-adjustment-mechanism) |
| Red Tractor assured farms | **~78,000** | Nil to minimal | Red Tractor (private scheme) | [Red Tractor](https://en.wikipedia.org/wiki/Red_Tractor) |

The ONS figure of 130,000 manufacturers is the VAT/PAYE-registered count. The brief's ~250,000
figure comes from the DBT Business Population Estimates, which include unregistered sole traders.
**For software buyer-counting the ONS figure is the right one, and it is arguably still too
generous** — a manufacturer with two employees does not buy SaaS.

---

## UK CBAM (1 January 2027) — dedicated deep treatment

### The regime is real. Grade: BINDING (in force 1 Jan 2027, primary and secondary legislation made)

| Element | Detail | Instrument |
|---|---|---|
| Primary legislation | Finance Act 2026, Royal Assent **18 March 2026** | Finance Act 2026 |
| Administrative provisions | **SI 2026/802**, made **13 July 2026**, in force **1 January 2027** | [legislation.gov.uk/uksi/2026/802](https://www.legislation.gov.uk/uksi/2026/802/made/data.html) |
| Rate calculation & carbon price relief | **SI 2026/809**, made 13 July 2026, in force 1 January 2027 | SI 2026/809 |
| Transitory provisions | **SI 2026/830** (registration deadlines, accounting periods, payment dates) | SI 2026/830 |
| Goods in scope | Aluminium, cement, fertiliser, hydrogen, iron & steel. Reaches downstream — screws, bolts, fasteners, aluminium doors and structures, nitric acid, ammonia. **Ferro-alloys and ferrous scrap excluded.** | HMRC guidance |
| Threshold | **£50,000** rolling 12-month look-back, checked on the 1st of each month, **or** forward-looking 30-day expectation | HMRC |
| First accounting period | 1 Jan 2027 – 31 Dec 2027 (12 months) | SI 2026/830 |
| Registration deadline | **31 January 2028** | HMRC |
| First return & payment | **31 May 2028** | HMRC |
| Thereafter | **Quarterly** returns from 1 January 2028 | HMRC |
| Record retention | **6 years** from the day after the end of the accounting period | SI 2026/802 |
| Penalties | HMRC's existing regimes; VAT-style points for late submission/payment. **No CBAM-specific penalty schedule published.** | SI 2026/802 contains no explicit penalty provisions |

This passes the Standing Test cleanly. It is not a consultation, not a strategy paper. It is a tax
with a commencement date, statutory instruments, and a filing deadline.

### Who is obligated, and how many

HMRC's policy paper is explicit:

- **~10,000 businesses** import CBAM goods into the UK.
- The £50,000 threshold **"removes over 80% of otherwise affected importers"**, of whom **"over 70%"
  are SMEs**.
- Implied obligated population: **~2,000 registrable persons.**
- Exchequer yield: **£30m (2026-27), £140m (2027-28), £180m (2028-29), £175m (2029-30), £155m
  (2030-31).**
- **Administrative cost to business: £9m one-off, £16m continuing per year.**

That last line is the single most important number in this report and I want to be blunt about it.
**HMRC has budgeted the entire recurring UK CBAM compliance burden across all of British industry at
£16 million per year.** Spread across ~2,000 obligated importers that is **£8,000 per business per
year, covering staff time, adviser fees and software combined.** A SaaS vendor is competing for a
slice of £8k, not for £8k.

### The data burden — much lighter than the EU analogue, and this is the crux

The EU CBAM vendor category was built on one premise: importers must extract per-installation,
verified embedded-emissions data from non-EU suppliers, and that is agonising. Assent, CBAMBOO,
CarbonChain, Coolset and Kolum all sell supplier-outreach machinery for exactly this.

**UK CBAM does not impose that burden in the same way.** Three structural differences:

1. **The UK runs CBAM as an indirect tax administered by HMRC, not a tradable-certificate scheme.**
   There is no registry, no certificate purchasing, no XML declaration to a central EU system.
2. **The statutory return does not ask for emissions data.** Per SI 2026/802, the return contains,
   for each good: the **8-digit commodity code, the weight, the carbon price relief amount, and the
   place of origin**. Embedded emissions are then derived — weight × emissions factor.
3. **Default values are permitted.** Government will publish default values for each CBAM good before
   1 January 2027, covering direct and indirect emissions, derived from the European Commission's
   Joint Research Centre data. Importers may use defaults **or** actual verified data throughout
   **2027–2030**.

So an importer can be fully compliant with UK CBAM having collected **zero** data from its suppliers.
It needs its own customs data — which it already has, because it filed the declarations.

The counter-argument, and it is a real one: government has signalled defaults will be set so they
**"carry no advantage over real data"**, and KPMG's read of the final regulations is that where
actual data is unavailable importers rely on **"conservative default values – and potentially higher
CBAM liabilities."** So there is an economic incentive to obtain actual data — but it is an
*optimisation* incentive, not a compliance obligation. Optimisation products are bought by people who
have first quantified the saving. In 2027, nobody will have.

Where real friction does exist is **Carbon Price Relief (CPR)**. To deduct an overseas carbon price,
an importer must produce a **Carbon Pricing Verification Form** completed by an accredited overseas
verifier, capturing installation details, emissions data and carbon pricing adjustments. KPMG notes
the documentation must be **"traceable, consistent and independently verified."** That is a
genuine, adversarial, evidence-assembly problem with money attached — and it is the sharpest edge of
UK CBAM.

### Is it already served? No — and that is verified

| Vendor | Base | EU CBAM | **UK CBAM** | Pricing |
|---|---|---|---|---|
| **CBAMBOO** | London | Yes (core product) | **No mention on site** | €9,000/yr Basic; €19,000/yr Pro; supplier side free |
| **CarbonChain** | London | Yes (metals/commodities focus) | **Not mentioned** | Quote-based, enterprise |
| **Assent** | Ottawa | Yes | **"EU CBAM requirements only. No mention of UK coverage."** | Undisclosed; 72,000+ verified supplier contacts |
| **Coolset** | Amsterdam | Yes | Not mentioned | Custom quote only |
| **Kolum / Greenly / Dubrink** | EU | Yes | Not mentioned | Dubrink publishes a price; others quote |
| **SupplyOn** | Germany | Yes | Not mentioned | Enterprise |
| **CBAMReturn** | UK | No | **Yes — UK-specific, pre-launch** | **Waitlist. No pricing. No launch date.** |

An independent vendor review site tracking six CBAM platforms as of 2026 contains **"no information
about UK CBAM support for any reviewed platform."**

This is a genuine LAW 4 result in the *positive* direction, which is rare enough to state plainly:
**as of September 2026, no shipping software product serves UK CBAM.** Two London-headquartered CBAM
specialists — CBAMBOO and CarbonChain — are sitting on the exact capability and have not shipped it.

That should worry us more than it excites us. **CBAMBOO is in London, sells CBAM and nothing else,
and has not built the UK module fifteen months before the regime starts.** The most likely
explanations are that they have judged the UK opportunity too small to prioritise, or that they will
ship it in a quarter whenever they choose to. Both are bad for a new entrant.

### What kills UK CBAM as a business

1. **UK–EU ETS linkage.** The May 2025 UK–EU summit Common Understanding included working toward
   linking the UK and EU emissions trading schemes. If linkage completes, EU-origin imports would
   fall out of UK CBAM scope, removing a large share of the obligated population at a stroke.
   `[UNVERIFIED — could not confirm current negotiation status within the search budget. This must be
   verified before any build decision. It is the single largest tail risk.]`
2. **The Big 4 absorb it.** KPMG, Deloitte, EY and Saffery are all publishing CBAM readiness
   material now. Indirect tax practices will fold CBAM returns into existing VAT/customs engagements
   at marginal cost.
3. **The CDS vendors absorb it.** The return is built from customs data. **HMRC lists 80+ software
   developers providing CDS declaration support**, including AEB, ASM, Descartes, WiseTech, SAP,
   Thomson Reuters ONESOURCE, Customs4trade, iCustoms and KlearNow. Any of them can compute
   weight × default factor from data they already hold. This is the incumbency risk that matters most.
4. **Default values make year one trivial.** The first return is not due until 31 May 2028. Urgency
   in 2027 will be low.

### CBAM verdict

**Build only the narrow, adversarial part: the Carbon Price Relief evidence pack and the
default-versus-actual liability comparison.** The registration-and-return plumbing will be
commoditised by the CDS vendors and given away. What will not be given away is the assembly,
verification-chain custody and six-year retention of overseas verifier documentation that survives an
HMRC challenge, and the quantified answer to "is it worth paying a verifier to beat the default on
this supplier?" That is a defensible wedge. It is also a **£4k–£12k ACV product with perhaps 500–800
winnable buyers**, which at the midpoint is roughly **£5m ARR at full penetration** — respectable,
not transformative, and dependent on a regime that a trade negotiation could shrink.

---

## Full candidate analysis

### CANDIDATE 1 — Packaging EPR recyclability (RAM) assessment and modulated-fee defence

| # | Field | Detail |
|---|---|---|
| 1 | **The gap** | Large packaging producers must self-assign a red/amber/green recyclability rating to every in-scope packaging component under RAM v1.1, that rating now multiplies their disposal fee, regulators will challenge inaccurate self-reports, and most producers are doing this in spreadsheets against a SKU estate in the thousands. |
| 2 | **Pain owner** | Head of Packaging / Packaging Technologist; secondarily Head of Sustainability or Group Environment Manager. |
| 3 | **Budget holder** | Finance Director or Supply Chain Director. The budget line is the EPR fee itself — an opex cost already forecast and already painful — not an IT budget. This matters: it is the easiest budget in this report to reach. |
| 4 | **UK buyer count** | 6,936 large producers submitted 2024 packaging data (EA, 11 June 2025). Method: discount ~40% as foreign-parented groups whose packaging specification sits abroad, and ~20% with SKU estates small enough for a spreadsheet. **Winnable: ~1,800–2,500.** |
| 5 | **Forcing function** | **BINDING.** Producer Responsibility Obligations (Packaging and Packaging Waste) Regulations 2024. Modulation applies to **2026-27 disposal fee calculations**. Red multiplier **1.2× (2026-27) → 1.6× (2027-28) → 2.0× (2028-29)** per the PackUK modulation statement. Producers are reporting RAM ratings now. |
| 6 | **Solved today by** | Compliance schemes as a bundled service, plus spreadsheets and packaging-technologist judgement. Defra's own Report Packaging Data (RPD) portal is a submission form, not an assessment tool. |
| 7 | **Named incumbents** | **Valpak** — explicitly offers "guidance on the Recyclability Assessment Methodology (RAM)", plus Data Insights, Insight and the Rio sustainability platform; clients include Samsung, Coca-Cola, Brother; **membership fees not published**. **Ecosurety** — "over 500 major brands and retailers", end-to-end packaging data management, no published pricing, **no RAM service mentioned on its homepage**. **Comply Direct**, **ERP UK**, **360 Environmental**, **Clarity**. Typical compliance scheme membership sits in the £5k–£50k/yr band `[UNVERIFIED — no scheme publishes pricing]`. |
| 8 | **Willingness to pay** | Anchored on the fee itself. 2025 base disposal fees: **plastic £423/t, fibre-based composite £461/t, wood £280/t, aluminium £266/t, steel £259/t, paper & card £196/t, glass £192/t.** A producer handling 5,000t of plastic faces ~£2.1m at base rate; a red rating at 2.0× in 2028-29 makes that ~£4.2m. **A tool that moves 10% of tonnage from red to green is worth six figures a year to a mid-sized producer.** £15k–£60k ACV is defensible. |
| 9 | **Data required** | Packaging component specifications (material, weight, format, closures, labels, adhesives, colourants) — customer-supplied, and the hard part. RAM v1.1 rules — public. UK reprocessing infrastructure data — public/licensable. No third-party licence blocker. |
| 10 | **Cloudflare fit** | **Excellent.** Structured records, a rules engine, document storage for evidence. D1 + R2 + Workers. No GPU, no scraping, no on-prem. |
| 11 | **5–10 year durability** | The published modulation schedule runs to 2028-29. Beyond that it must be extended or it lapses — a real risk. Offsetting: EU PPWR imposes convergent design rules on anyone exporting to the EU, so the underlying "prove your packaging is recyclable" problem grows. **What kills it:** a compliance scheme (Valpak most likely) ships a credible RAM module and bundles it free into membership. |
| 12 | **Evidence** | Class 4 (regulator dataset/publication): [PackUK modulation statement](https://www.gov.uk/government/publications/extended-producer-responsibility-for-packaging-modulated-disposal-fees) and [large-producer reporting requirements](https://www.gov.uk/guidance/check-what-to-report-for-epr-for-packaging-as-a-large-producer). Class 3 (competitor product/pricing): [Valpak packaging compliance](https://www.valpak.co.uk/services/packaging-compliance/), [Ecosurety](https://www.ecosurety.com/). Class 4 again: [EPR disposal fees per tonne](https://www.gov.uk/guidance/extended-producer-responsibility-for-packaging-recycling-obligations-and-waste-disposal-fees). |

**Scores:** Pain 4 · Forcing 5 · Buyers 4 · WTP 4 · Incumbency **2** · Moat 3 · Cloudflare 5 · Durability 3 = **30/40**

*Incumbency is the weak axis and the sceptic should attack it.* Valpak already names RAM as a
service. The honest framing is that this is a **race against a service business adding software**,
not an empty field. The counter is that compliance schemes monetise PRN broking and fee
administration, and have historically shipped thin software; a tool that reduces a member's fees cuts
against a scheme's own revenue model. That tension is the opening.

---

### CANDIDATE 2 — UK CBAM liability engine and Carbon Price Relief evidence pack

| # | Field | Detail |
|---|---|---|
| 1 | **The gap** | ~2,000 UK importers become liable for a new tax on 1 January 2027, must decide per-supplier whether to use a default emissions value or pay a verifier for actual data, and must assemble independently-verified overseas carbon-price documentation that survives HMRC challenge for six years. Nothing on the market does this for the UK regime. |
| 2 | **Pain owner** | Head of Indirect Tax (larger importers) or Customs/Compliance Manager (mid-market). In smaller importers it lands on the Finance Director by default. |
| 3 | **Budget holder** | Finance Director / Head of Tax. Compliance opex. |
| 4 | **UK buyer count** | ~10,000 importers of CBAM goods; >80% removed by the £50k threshold → **~2,000 obligated**. Discount ~35% foreign-parented (steel and aluminium importing is heavily international), ~25% who will hand it to their customs broker or Big 4 adviser. **Winnable: ~500–800.** Above the 50-buyer floor; the ACV question is the binding constraint, not the count. |
| 5 | **Forcing function** | **BINDING/SCHEDULED.** Finance Act 2026 (RA 18 Mar 2026); SI 2026/802, SI 2026/809 (made 13 Jul 2026, in force **1 Jan 2027**); SI 2026/830. Registration by **31 Jan 2028**; first return **31 May 2028**; quarterly thereafter. |
| 6 | **Solved today by** | Nothing. Spreadsheets, and Big 4 advisory engagements currently at the "readiness assessment" stage. |
| 7 | **Named incumbents** | **For UK CBAM: none shipping.** CBAMBOO (London, €9,000–€19,000/yr, EU-only), CarbonChain (London, quote-based, EU-only), Assent (EU CBAM only, 72,000+ supplier contacts), Coolset, Kolum, Greenly, Dubrink, SupplyOn — all EU-only. **CBAMReturn** is UK-specific but pre-launch (waitlist, no pricing, no date). Adjacent threat: **80+ HMRC-listed CDS software developers** hold the customs data — AEB, ASM, Descartes, WiseTech, SAP, Thomson Reuters ONESOURCE, Customs4trade, iCustoms, KlearNow. |
| 8 | **Willingness to pay** | **The weak axis.** HMRC's own estimate: **£9m one-off and £16m/year continuing admin cost across all affected business** ≈ £8k per obligated importer per year for everything — staff, advisers and software. Realistic ACV **£4k–£12k**. Anchor: CBAMBOO's EU product at €9,000/yr Basic, for a regime with a far heavier data burden. |
| 9 | **Data required** | Customs declaration data (commodity code, weight, origin) — customer-supplied, already held. Government default values — public, publishing before 1 Jan 2027. Overseas carbon pricing regimes and verifier accreditation — public/licensable. Supplier actual-emissions data — customer-supplied, optional. |
| 10 | **Cloudflare fit** | **Excellent.** Rules + rates engine, document custody, quarterly filing. D1/R2/Workers/Queues. No blockers. |
| 11 | **5–10 year durability** | Scope may widen (glass, ceramics, polymers were canvassed). **What kills it:** (a) **UK–EU ETS linkage exempting EU-origin imports** — the largest risk, unverified; (b) a CDS vendor shipping the return for free as a module; (c) Big 4 absorption; (d) default values remaining good enough that nobody optimises. |
| 12 | **Evidence** | Class 4 (regulator dataset/legislation): [SI 2026/802](https://www.legislation.gov.uk/uksi/2026/802/made/data.html), [HMRC CBAM policy paper with business counts and admin costs](https://www.gov.uk/government/publications/introduction-of-carbon-border-adjustment-mechanism/carbon-border-adjustment-mechanism), [HMRC registration guidance](https://www.gov.uk/government/collections/check-if-youll-need-to-register-for-carbon-border-adjustment-mechanism-cbam). Class 3 (competitor pricing): [CBAMBOO review with €9,000/€19,000 tiers](https://cbamguide.com/software/cbamboo/), [CBAM vendor comparison](https://cbamguide.com/software/), [CBAMReturn](https://cbamreturn.co.uk/guides/uk-cbam-guide). |

**Scores:** Pain 3 · Forcing 5 · Buyers 3 · WTP **2** · Incumbency 4 · Moat 3 · Cloudflare 5 · Durability 3 = **28/40**

---

### CANDIDATE 3 — Deposit Return Scheme producer onboarding

| # | Field | Detail |
|---|---|---|
| 1 | **The gap** | Drinks producers must register every in-scope container with the DMO, apply scheme labelling, reconcile deposits flowing through the supply chain, and report volumes — from October 2027, against a scheme whose core parameters are still unpublished. |
| 2 | **Pain owner** | Packaging/Technical Manager; Commercial Finance Manager for deposit reconciliation. |
| 3 | **Budget holder** | Finance Director. |
| 4 | **UK buyer count** | Drinks producers and importers placing PET/aluminium/steel containers 150ml–3l on the market. **Estimate ~1,200 winnable** (large producers plus own-label suppliers), derived from the large-producer EPR population filtered to drinks. `[UNVERIFIED — no published count of DRS-obligated producers exists yet.]` |
| 5 | **Forcing function** | **SCHEDULED.** Deposit Return Scheme regulations; go-live **1 October 2027** (England, Scotland, NI; Wales concurrently for PET/metal with glass transition to 2031). UK DMO Ltd appointed May 2025 (England/NI) and designated in Scotland June 2025. **But:** the deposit amount, the producer fee basis and retailer reimbursement mechanics are all **still unconfirmed**. |
| 6 | **Solved today by** | Nothing yet — the scheme does not exist. Compliance schemes are running member webinars. |
| 7 | **Named incumbents** | **Ecosurety** already markets DRS alongside EPR and plastic packaging tax. **Valpak**, **Comply Direct**, **Clarity**. The DMO itself will build a producer registration portal, which will absorb the core registration job. |
| 8 | **Willingness to pay** | Cannot be anchored. The producer fee is unpublished, so no producer can size the problem. |
| 9 | **Data required** | GTIN/barcode per SKU, container material and volume, volumes placed on market, artwork/label compliance. All customer-supplied. |
| 10 | **Cloudflare fit** | Excellent. |
| 11 | **5–10 year durability** | Scotland's DRS collapsed once already. **What kills it:** the DMO's own portal doing enough; another delay. |
| 12 | **Evidence** | Class 4: [Commons Library briefing CBP-10453](https://commonslibrary.parliament.uk/research-briefings/cbp-10453/), [Defra DRS blog](https://defraenvironment.blog.gov.uk/2025/01/31/introducing-the-deposit-return-scheme-for-drinks-containers/). Class 5 (trade body): [FDF DRS overview](https://www.fdf.org.uk/fdf/business-guidance-hubs/packaging/packaging-latest/deposit-return-scheme/deposit-return-scheme-overview/), [Ecosurety: what we know and don't](https://www.ecosurety.com/news/drs-explained-what-we-know-so-far-what-we-dont-and-what-businesses-should-do). |

**Scores:** Pain 3 · Forcing 4 · Buyers 3 · WTP 2 · Incumbency 4 · Moat 3 · Cloudflare 5 · Durability 2 = **26/40**

**Verdict: right shape, wrong time.** Revisit when the deposit level and producer fee are published.

---

### CANDIDATE 4 — Multi-regime packaging and product data spine

**The gap:** a single packaging-component dataset feeds EPR tonnage reporting, RAM RAG ratings,
Plastic Packaging Tax, DRS container registration and Simpler Recycling — and producers currently
maintain four or five disconnected spreadsheets, each reconciled by hand to a different deadline.

**Pain owner:** Group Packaging Manager. **Budget holder:** Supply Chain Director.
**Buyers:** ~2,500 (the large-producer population with multi-regime exposure).
**Forcing function:** **BINDING** (EPR Regulations 2024; PPT since April 2022; Simpler Recycling in
force **31 March 2025**, micro-firms **31 March 2027**) plus **SCHEDULED** (DRS Oct 2027).
**Incumbents:** Valpak (Data Insights, Rio), Ecosurety (end-to-end data management, 500+ brands),
Comply Direct, ERP UK, Clarity, 360 Environmental.
**WTP:** £20k–£75k for a multi-site producer, anchored on displaced scheme service fees.
**Cloudflare fit:** excellent. **Durability:** high — regimes proliferate, they do not retract.
**Evidence:** [gov.uk EPR large-producer reporting](https://www.gov.uk/guidance/check-what-to-report-for-epr-for-packaging-as-a-large-producer) (Class 4);
[Valpak](https://www.valpak.co.uk/services/packaging-compliance/) and [Ecosurety](https://www.ecosurety.com/) (Class 3);
[Simpler Recycling guidance](https://www.gov.uk/guidance/simpler-recycling-workplace-recycling-in-england) (Class 4).

**Scores:** Pain 3 · Forcing 5 · Buyers 4 · WTP 3 · Incumbency **2** · Moat 3 · Cloudflare 5 · Durability 4 = **25/40**

Same incumbency problem as Candidate 1, more acutely — this *is* what the compliance schemes sell.
Only viable as a data layer sold beneath them, or to producers large enough to self-comply.

---

### CANDIDATE 5 — Food & drink supplier specification and allergen data exchange

**The gap:** food manufacturers and wholesalers maintain product specifications, allergen
declarations and supplier approvals across spreadsheets, PDFs and email, and must reproduce them on
demand for BRCGS/SALSA audits, retailer technical teams and PPDS labelling.

**Pain owner:** Technical Manager / QA Manager. **Budget holder:** Technical Director.
**Buyers:** ~4,000 food and drink manufacturers and wholesalers of meaningful scale (subset of the
130,000 manufacturers and 613,000 food establishments).
**Forcing function:** **BINDING** — Natasha's Law (PPDS allergen labelling) in force **1 October
2021**; Food Information Regulations. Note this is an *old* binding obligation, which per LAW 4 is a
warning sign, not an opening.
**Incumbents — dense:** Erudus (allergen/nutritional data exchange, established), Kafoodle
(enterprise quote, "several hundred pounds per month per site"), Nutritics (£80–£200/month),
FoodCore, Luminos, FoodDocs, NutriCalc (£19/month entry tools), Ideagen (18,500+ organisations,
food & beverage named vertical), Safefood 360, Sedex.
**WTP:** £19/month to several hundred per site per month. Proven but low.
**Cloudflare fit:** excellent. **Durability:** moderate; LLMs plausibly erase spec-extraction by 2029.
**Evidence:** [FSA PPDS guidance](https://www.food.gov.uk/business-guidance/prepacked-for-direct-sale-ppds-allergen-labelling-changes-for-restaurants-cafes-and-pubs) (Class 4);
[Kafoodle pricing](https://www.getapp.com/retail-consumer-services-software/a/kafoodle-kitchen/), [Erudus](https://erudus.com/allergen-nutritional-data-search) (Class 3).

**Scores:** Pain 3 · Forcing 3 · Buyers 4 · WTP 3 · Incumbency **2** · Moat 2 · Cloudflare 5 · Durability 2 = **23/40**

---

### CANDIDATE 6 — EUDR due diligence for UK operators placing goods on the EU market

**Forcing function: SCHEDULED** — EUDR applies to large operators from **30 December 2026**, and to
natural persons, micro and small enterprises from **30 June 2027**. UK firms are in scope only where
they act as the "operator" placing goods on, or exporting from, the EU market; GB is a third country.
**Disconfirming evidence:** the December 2025 simplification package cut expected compliance costs by
**~75%**, micro/small primary operators now file a **one-time simplified declaration** rather than
per-consignment DDS, and the EU-side vendor field (Assent, Sedex, Osapiens, Source Intelligence,
Prewave, LiveEO) is already built. **The UK's own equivalent — Environment Act 2021 Schedule 17
forest risk commodities — has never been commenced. Grade: ASPIRATIONAL. Zero weight.**
**Scores:** Pain 2 · Forcing 3 · Buyers 2 · WTP 2 · Incumbency 2 · Moat 2 · Cloudflare 4 · Durability 3 = **20/40. Rejected.**

---

### CANDIDATE 7 — Farm assurance and SFI evidence management

**Buyers:** ~78,000 Red Tractor assured farms; SFI agreement holders (SFI26 window one closed 1 Sept
2026, restricted to businesses under 50 hectares without an existing agreement).
**Forcing function:** Red Tractor is a **private scheme, not law** — commercially binding via
supermarket supply requirements but legally ASPIRATIONAL. SFI is a **voluntary grant scheme** with
scheme rules and an annual declaration; it has been opened, closed abruptly (March 2025) and
re-opened with restrictions. That volatility is itself disqualifying under LAW 1.
**Willingness to pay:** farm software runs £500–£3,000/yr. With ~1,500 winnable buyers at £1,000 ACV
the ceiling is £1.5m ARR. **Fails the LAW 2 ACV test.**
**Incumbents:** Farmplan Gatekeeper, Muddy Boots/TELUS, Trinity AgTech, Agrecalc, Farm Carbon Toolkit, Sandy.
**Scores:** Pain 3 · Forcing **2** · Buyers 3 · WTP **1 — automatic rejection** · Incumbency 2 · Moat 2 · Cloudflare 5 · Durability 2 = **Rejected.**

---

### CANDIDATE 8 — Simpler Recycling workplace evidence

**Forcing function: BINDING** — in force **31 March 2025**; micro-firms (<10 FTE) from **31 March
2027**; Environment Agency enforces by compliance notice, and failure to comply with a notice is an
offence. **But:** gov.uk guidance specifies **no mandatory record-keeping requirement**. A duty with
no evidential burden generates no software demand. Waste contractors (Biffa, Veolia, Suez) supply
the bins and the paperwork as part of the collection contract.
**Scores:** Pain **1 — automatic rejection** · Forcing 5 · Buyers 5 · WTP 1 · Incumbency 3 · Moat 1 · Cloudflare 5 · Durability 3 = **Rejected.**

---

## Graveyard — killed, with named incumbents

### O-licence compliance evidence — **KILLED BY LAW 4, decisively**

The brief flagged this as potentially existential and asked who manages the evidence. The answer is
published by the regulator itself. **DVSA's Earned Recognition validated-systems list names 73
providers** — 31 for tachograph/driver data and 54 for vehicle maintenance, with overlap.

*Tachograph/driver:* Aquarius IT, Descartes, Stoneridge Electronics, Road Tech Tachomaster,
Continental Automotive, TruTac, Tranzaura, Logistics UK, RHA Analysis, Novadata, DAKO, TMS (Analysis),
Convey Technology, GB Tachopak, plus 17 more.

*Maintenance:* FleetCheck, Microlise, Jaama, Chevin Fleet, r2c Online, Freeway Fleet Systems,
Truckfile, CheckedSafe, Civica, TechnologyOne, IFS Ultimo, Asset Works, Holman, Zenith, Rivus,
Northgate, Prolius, Sopp and Sopp, plus 36 more.

Pricing is transparent and low: **£15–£50 per vehicle per month**, with FleetEase at **£25/month for
up to 50 vehicles then £2/vehicle**. The pain is real — the Traffic Commissioners determined **1,066
public inquiries** in 2024-25 and closed **15,613 vocational driver cases**, with the report citing
vehicles unspecified for years, driving without a driver card, and vehicle units and driver cards not
downloaded for long periods. **But a real pain served by 73 vendors at £25/month is not an
opportunity; it is a commodity.** Compounding this: ONS records road freight business numbers down
**5.3%** in 2025 to their lowest since 2015. A shrinking, price-crushed, 73-vendor market is the
clearest reject in this report.

### Manufacturing QMS / CAPA / NCR / supplier quality — **KILLED BY LAW 4**

**Ideagen** covers NCR, CAPA, audit, document control, supplier quality, inspection, training and
regulatory intelligence across aerospace & defence, food & beverage, pharma, life sciences and
manufacturing, and is **"trusted by 18,500+ organizations."** It has also consolidated the UK
mid-market: **qualsys.co.uk now 301-redirects to ideagen.com.** Add MasterControl, Intelex, ETQ,
Sparta, Veeva, plus SAP/Epicor/Sage QMS modules and the MES layer. The brief asked for an honest
assessment: the honest assessment is that this category has a well-funded consolidator actively
buying its UK competitors. Automatic rejection on Incumbency.

### Customs declarations / Border Target Operating Model — **KILLED BY LAW 4**

HMRC publishes a list of **80+ CDS software developers**, including AEB, Agency Sector Management,
Descartes, WiseTech Global, SAP, Thomson Reuters ONESOURCE, Customs4trade, E2open, iCustoms,
KlearNow, MIC, Maritime Cargo Processing, CNS, Just Trade and Phlo Systems. Forty years of
post-Brexit-adjacent demand produced eighty vendors. There is no opening.

### UK ETS expansion to energy-from-waste — **KILLED BY LAW 1**

This looked strong: a two-year MRV phase from 2026, full obligation from 2028, covering facilities
above 3 t/hr non-hazardous or 10 t/day hazardous waste. **DESNZ confirmed on 26 August 2026 that the
expansion will no longer take place in 2028, with the new timeline "to be set out in due course."**
An obligation with no date is not a forcing function. This is exactly the failure mode the method
exists to catch, and finding it is a success.

### Food allergen labelling (Natasha's Law) — **KILLED BY LAW 4**

Kafoodle, Nutritics (£80–£200/month), Erudus, FoodCore, Luminos, FoodDocs, NutriCalc (from
£19/month), Ideagen, Safefood 360. Five years post-commencement, the field is settled and priced at
the floor.

### Packaging EPR core reporting — **absorbed by the compliance schemes**

Valpak (Data Insights, Insight, Rio platforms; Samsung, Coca-Cola, Brother), Ecosurety (500+ brands),
Comply Direct, ERP UK, 360 Environmental, Clarity. Defra operates the RPD submission service itself.
Only the **RAM/modulation sliver** (Candidate 1) is arguably open, and Valpak already names RAM as a
service line.

---

## Honest verdict: willingness to pay in UK manufacturing and haulage

The brief asked me to be honest about this. I will be.

**UK manufacturing does not have a software budget at the scale this sector's headcount implies.**
The ONS records **130,000 VAT/PAYE-registered manufacturers**, and the UK business population is
overwhelmingly micro — **44.0% of all UK businesses are single-employee limited companies**, and
**2.68 million of 2.73 million operate from a single site**. Strip out the micro tail and the firms
with foreign parents whose systems decisions are made in Stuttgart, Detroit or Osaka, and the
addressable UK-decision-making manufacturer population is plausibly **8,000–15,000 firms**, not
130,000. That is still a real market — but it is an order of magnitude below the sector headline, and
it is the number to plan against.

**Haulage is worse, and is actively deteriorating.** Road freight business numbers fell **5.3% in
2025 to their lowest level since 2015**. The compliance software that hauliers do buy is priced at
**£15–£50 per vehicle per month** across 73 competing vendors, several of which are trade bodies
(Logistics UK, RHA) selling below commercial rates to members. Margins in haulage are thin enough
that a £30/vehicle/month line item is contested annually. **I would not build for UK haulage.**

**The one reliable exception is where the software sits directly against a fee, a tax or a
liability the buyer is already paying.** This is the single most useful pattern in this sweep:

- Packaging EPR producers pay **£192–£461 per tonne** today, doubling for red-rated packaging by
  2028-29. A tool that changes that number is bought from the fee budget, not the IT budget.
- CBAM importers will pay a per-tonne carbon charge from January 2027 against an Exchequer yield
  rising to **£180m in 2028-29**.
- An O-licence revocation is existential — but **73 vendors already arbitrage that fear down to
  £25/month**, which proves the reverse point: fear alone does not sustain price. Contested supply
  does not.

So the rule I would give the Orchestrator is: **in this sector, price against a regulated cash
outflow, never against efficiency or risk.** "Save your team four days a month" does not sell to a UK
manufacturer. "Reduce a £2.1m EPR bill" does. Every candidate above that scores 3+ on willingness to
pay does so because it sits on a fee line; every one that scores 1–2 does so because it sits on a
time-saving argument.

One further caution on CBAM specifically. It is tempting to read "new tax, 2,000 obligated
businesses, no incumbent" as a landgrab. **HMRC has costed the entire continuing compliance burden at
£16m a year across all affected business.** That is the ceiling on the whole category — advisers,
verifiers and software together. A software vendor taking 15% of that would be a **£2.4m ARR market
in total.** UK CBAM is a good product wedge and a mediocre standalone market, and it should be
pursued as the first regime in a multi-regime carbon-and-packaging compliance platform, not as a
company.

---

## Sources

**Primary legislation and regulator publications (evidence class 4)**
- [The Carbon Border Adjustment Mechanism (Administrative Provisions) Regulations 2026, SI 2026/802](https://www.legislation.gov.uk/uksi/2026/802/made/data.html)
- [HMRC/HMT policy paper: Introduction of the Carbon Border Adjustment Mechanism](https://www.gov.uk/government/publications/introduction-of-carbon-border-adjustment-mechanism/carbon-border-adjustment-mechanism) — 10,000 businesses; £9m one-off / £16m continuing; Exchequer yield by year
- [HMRC: Check if you'll need to register for CBAM](https://www.gov.uk/government/collections/check-if-youll-need-to-register-for-carbon-border-adjustment-mechanism-cbam)
- [HMRC: CBAM goods that may not count toward the registration threshold](https://www.gov.uk/guidance/imported-carbon-border-adjustment-cbam-goods-that-may-not-contribute-towards-the-registration-threshold)
- [Draft tax information and impact note, CBAM](https://gov.uk/government/consultations/draft-legislation-carbon-border-adjustment-mechanism/draft-tax-information-and-impact-note)
- [PackUK EPR for packaging: producer disposal fees modulation statement](https://www.gov.uk/government/publications/extended-producer-responsibility-for-packaging-modulated-disposal-fees) — RAM v1.1, red 1.2×/1.6×/2.0×
- [Check what to report for EPR for packaging as a large producer](https://www.gov.uk/guidance/check-what-to-report-for-epr-for-packaging-as-a-large-producer)
- [EPR for packaging: recycling obligations and waste disposal fees](https://www.gov.uk/guidance/extended-producer-responsibility-for-packaging-recycling-obligations-and-waste-disposal-fees) — per-tonne base fees
- [Simpler recycling: workplace recycling in England](https://www.gov.uk/guidance/simpler-recycling-workplace-recycling-in-england)
- [Traffic Commissioners for Great Britain Annual Report 2024-25](https://www.gov.uk/government/publications/traffic-commissioners-annual-report-2024-to-2025/traffic-commissioners-for-great-britain-annual-report-2024-25) — 66,222 goods licences; 1,066 public inquiries
- [DVSA Earned Recognition: validated IT systems and software](https://www.gov.uk/government/publications/dvsa-earned-recognition-it-or-software-you-need/vehicle-operator-it-systems-and-software-that-work-with-dvsa-earned-recognition) — 73 named providers
- [HMRC: software developers providing customs declaration support](https://www.gov.uk/guidance/list-of-software-developers-providing-customs-declaration-support) — 80+ named
- [ONS: UK business — activity, size and location, 2025](https://www.ons.gov.uk/businessindustryandtrade/business/activitysizeandlocation/bulletins/ukbusinessactivitysizeandlocation/2025)
- [FSA: PPDS allergen labelling guidance](https://www.food.gov.uk/business-guidance/prepacked-for-direct-sale-ppds-allergen-labelling-changes-for-restaurants-cafes-and-pubs)
- [Sustainable Farming Incentive uptake, September 2026](https://www.gov.uk/government/statistics/sfi-uptake-september-2026)
- [Commons Library: Deposit return schemes (CBP-10453)](https://commonslibrary.parliament.uk/research-briefings/cbp-10453/)

**Competitor products and pricing (evidence class 3)**
- [CBAMBOO](https://www.cbamboo.com/) and [CBAMBOO review — €9,000/€19,000 per year](https://cbamguide.com/software/cbamboo/)
- [CBAM vendor comparison — no UK CBAM support across six platforms](https://cbamguide.com/software/)
- [CarbonChain review](https://cbamguide.com/software/carbonchain/)
- [Assent CBAM — EU only, 72,000+ supplier contacts](https://www.assent.com/solutions/esg-supply-chain/cbam/)
- [CBAMReturn — UK-specific, pre-launch waitlist](https://cbamreturn.co.uk/guides/uk-cbam-guide)
- [Valpak packaging compliance — names RAM as a service](https://www.valpak.co.uk/services/packaging-compliance/)
- [Ecosurety — 500+ brands](https://www.ecosurety.com/)
- [Ideagen quality — 18,500+ organisations](https://www.ideagen.com/solutions/quality); qualsys.co.uk redirects to ideagen.com
- [FleetEase — £25/month up to 50 vehicles](https://fleetease.co.uk/)
- [Kafoodle pricing](https://www.getapp.com/retail-consumer-services-software/a/kafoodle-kitchen/); [Erudus](https://erudus.com/allergen-nutritional-data-search)

**Professional and trade commentary (evidence classes 5–7 — supporting only)**
- [KPMG: From draft to delivery — HMRC confirm the framework for UK CBAM](https://kpmg.com/uk/en/insights/tax/tmd-from-draft-to-delivery-hmrc-confirm-the-framework.html)
- [Saffery: UK CBAM compliance guide for importers](https://www.saffery.com/insights/articles/carbon-border-adjustment-mechanism/)
- [letsrecycle.com: UK delays expansion of ETS to waste incineration](https://www.letsrecycle.com/news/uk-delays-expansion-of-ets-to-waste-incineration/)
- [ICAP: UK confirms ETS expansions — maritime, waste, carbon removals](https://icapcarbonaction.com/en/news/uk-government-confirms-major-uk-ets-expansions-maritime-waste-and-carbon-removals-be-phased)
- [Ecosurety: DRS explained — what we know, what we don't](https://www.ecosurety.com/news/drs-explained-what-we-know-so-far-what-we-dont-and-what-businesses-should-do)
- [ERP: UK packaging EPR compliance guide 2026](https://erp-recycling.org/uk/news-and-events/2026/04/uk-packaging-epr-compliance-guide-for-2026/) — 6,936 large producers
- [Burges Salmon: EUDR — what's next for UK companies](https://www.burges-salmon.com/articles/102mmru/eu-regulation-on-deforestation-free-products-eudr-whats-next-for-uk-companies/)

**Open items for wave 2**
1. **Verify UK–EU ETS linkage negotiation status.** It is the largest single threat to Candidate 2 and is currently `[UNVERIFIED]`.
2. Confirm whether HMRC has published CBAM default values (due before 1 January 2027) and how conservative they are.
3. Obtain compliance-scheme membership pricing (Valpak, Ecosurety, Comply Direct) — none publish; a mystery-shop would anchor Candidate 1's ACV properly.
4. Find a job posting for a packaging RAM or CBAM compliance role to add evidence class 1; a reed.co.uk "CBAM" search returned 77 results, **all financial-crime roles matching the acronym, none carbon-related** — itself a weak negative signal on role formation.
