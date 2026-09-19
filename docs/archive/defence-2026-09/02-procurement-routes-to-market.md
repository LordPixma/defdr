# DEFDR Research 02 — Defence Procurement: Routes to Market, Accreditation Boundaries and How a SaaS Vendor Actually Gets Paid

**Author:** Defence Procurement Expert (research agent)
**Date:** September 2026
**Status:** Evidence-based. Every substantive claim carries a source URL. Items marked `[UNVERIFIED]` could not be confirmed against a primary or strong secondary source and must not be used in external material.

---

## 1. Executive Summary

**The money is real and growing, but almost none of it is reachable by a new SaaS vendor in year one through the front door.** UK MOD spent £31.7bn with UK industry in 2024/25 ([MOD official statistics](https://www.gov.uk/government/statistics/mod-trade-industry-and-contracts-2025/mod-trade-industry-and-contracts-2025)), yet only ~5% of direct procurement spend reached SMEs in 2024, against a central government average of 11% ([Tussell Defence Procurement Tracker](https://www.tussell.com/insights/defence-procurement-tracker)). The top five suppliers took over 29% of all MOD procurement spend in 2025, and of the top ten frameworks used to award more than £6bn of new MOD contracts, half contained fewer than 20 suppliers and three contained fewer than ten (same source). Defence procurement is a concentrated, framework-mediated market with a small number of doors.

**Ten findings that shape product strategy:**

1. **The accreditation boundary is the single most important commercial fact.** In the UK, a commercial SaaS can hold data at **OFFICIAL and OFFICIAL-SENSITIVE** using ordinary commercial assurance — ISO 27001, Cyber Essentials Plus, UK data residency, MOD Secure by Design assessment. Kahootz sells exactly this on G-Cloud at **£3.69–£11.69 per user per month** ([Digital Marketplace listing](https://www.applytosupply.digitalmarketplace.service.gov.uk/g-cloud/services/863966228041800)). No SECRET accreditation is needed. This is where a new vendor lives.
2. **In the US the equivalent floor is FedRAMP Moderate / DoD IL2**, and the DoD Cloud Computing SRG uses the FedRAMP Moderate baseline at all impact levels; a FedRAMP High provisional authorisation is accepted for an IL4 PA without re-assessing controls, though non-control SRG requirements still apply ([Google Cloud compliance scope](https://docs.cloud.google.com/docs/security/compliance/fedramp-dod-compliance-scope)).
3. **FedRAMP has become materially cheaper and faster.** Rev5 Moderate ran **$250k–$750k**; early estimates for FedRAMP 20x Low/Moderate are **$100k–$300k**, and the first 20x pilot authorised in **119 days against a 660-day programme average** ([Secureframe cost analysis](https://secureframe.com/hub/fedramp/costs)). Phase 3 is live and the submission pipeline opened in 2026 ([fedramp.gov/20x](https://www.fedramp.gov/20x/)).
4. **Cloudflare hosting is now a defensible US public-sector posture but not yet a DoD one.** Cloudflare for Government achieved **FedRAMP High and GovRAMP Moderate in August 2026** and has stated intent to pursue **DoD IL4** ([Cloudflare press release](https://www.cloudflare.com/press/press-releases/2026/cloudflare-achieves-fedramp-high-authorization-to-secure-and-accelerate-the-u-s-governments-critical-missions/); [Nextgov](https://www.nextgov.com/acquisition/2026/08/cloudflare-seek-dod-il4-authorization-after-new-fedramp-govramp-designations/415299/)). Until IL4 lands, a Cloudflare-hosted product sells to UK OFFICIAL-SENSITIVE and US federal civilian, not to CUI-bearing DoD workloads.
5. **The UK has just created a three-month fast lane for software.** The Segmented Acquisition Model, live April 2026, targets **three months to contract for software, AI and off-the-shelf products**, one year for upgrades and two years for major platforms, inside a **£298bn four-year Defence Investment Plan** ([Defence Investment Plan coverage](https://gowlingwlg.com/en/insights-resources/articles/2026/uk-defence-investment-plan-2026)). This is the single best-timed opening in the addressable market.
6. **Offsets are an enormous, badly-tracked obligation pool.** US firms alone signed **$142.1bn of offset agreements against $251.7bn of export contracts between 1993 and 2022 — an average 56.46% offset ratio** — while delivering only **$125.4bn of offset credits** ([BIS 28th Annual Offsets Report](https://www.bis.gov/media/documents/public-version-28th-annual-offsets-report.pdf)). Transparency International puts the projected global offset market at **$371bn for 2021–2025** and describes the US government's oversight as leaving "defence firms to mark their own homework" ([TI-Defence](https://ti-defence.org/blissfully-blind-security-risks-defence-contract-offset/)).
7. **Government auditors are now naming offset tracking as a failure.** Canada's Auditor General found 99 contracts worth at least $39bn with obligations exceeding $36bn (2014–2023), and that "the specific benefits and the full costs of the Industrial and Technological Benefits Policy were unknown" ([OAG Report 10, Dec 2024](https://www.canada.ca/en/auditor-general/our-work/audit-reports/parl-oag-202412-10-e.html)). India's PAC found **$4.48bn of $9.9bn (45%) of offset obligations unfulfilled as of 31 December 2025** ([Bharat Shakti](https://bharatshakti.in/pending-rs-42000-crore-defence-offsets-trigger-scrutiny-expert-says-concerns-may-be-overstated/)).
8. **N-tier supply chain visibility is becoming a legal obligation, not a nice-to-have.** Section 805 of the FY2024 NDAA bars DoD from contracting directly with listed entities from **30 June 2026** and indirectly — anywhere upstream — from **30 June 2027** ([Wiley analysis](https://www.wiley.law/alert-NDAA-Provisions-Impacting-Governments-Contractors-and-Their-Supply-Chains)). That converts sub-tier mapping from a procurement preference into a compliance requirement.
9. **Prequalification cost is low in cash and high in calendar time.** JOSCAR Stage 1 is free; Stage 2 is free below £1m turnover and **£725 + VAT per year** above it ([Hellios](https://hellios.com/supplier-payment-info-joscar/)). SAM.gov registration runs **1–3 weeks**. A GSA Schedule runs **6–12 months**. FedRAMP runs 4–18 months. The barrier is elapsed time and evidence production, not fees.
10. **The realistic fastest path to first defence revenue is a UK OFFICIAL-SENSITIVE SaaS sold to a prime or an innovation body, not a ministry.** Credible time-to-first-cash is **4–9 months** via DASA/UKDI innovation contracts (£100k–£350k) or a prime-paid subscription, versus **12–30 months** for a direct MOD or DoD programme-of-record award.

---

## 2. Routes to Market

### 2.1 Comparison table

| Market | Mechanism | Accreditation needed | Time to first revenue | Realistic first deal | Source |
|---|---|---|---|---|---|
| **UK** | **G-Cloud 15 (RM1557.15)** — open framework, awarded 6 Aug 2026, buyer access mid-Aug 2026, runs to ~Sept 2030 | Lots 1a/2/3: CE+, ISO 9001/20000-1/27001/27018, £7m insurance. **Lot 1b (above OFFICIAL): £75m insurance + Gold Standard Financial Viability Assessment** | 3–9 months to list; 1–6 months to first call-off | £25k–£250k/yr call-off | [Stotles](https://www.stotles.com/resource/blog/g-cloud-15-award-date-moves-to-6-august-2026-what-suppliers-need-to-know); [Computer Weekly](https://www.computerweekly.com/news/366634470/CCS-under-fire-over-anti-SME-supplier-requirements-for-G-Cloud-15) |
| **UK** | **Defence Sourcing Portal (DSP)** — all MOD opportunities >£10,000 | Free registration; DEFCON 658 / Cyber Essentials; DCC once contracted | 6–18 months (tender cycle) | £50k–£500k | [digital.mod.uk](https://www.digital.mod.uk/sme-dosbg/contracting-with-defence/supplying-to-defence) |
| **UK** | **DASA / UK Defence Innovation (UKDI)** — open calls, themed competitions | None at bid stage; security assessed per project | 4–9 months (call → contract) | **£100k–£350k**, 100% funded, 12–18 months | [DASA](https://www.gov.uk/government/publications/defence-and-security-accelerator-dasa-open-call-for-innovation); [UKDI launch](https://www.gov.uk/government/news/ukdi-unifies-innovation-to-accelerate-frontline-capabilities-and-drive-national-growth) |
| **UK** | **Prime subcontract** (BAE, Babcock, Leonardo, Thales, QinetiQ) | **JOSCAR** (Stage 1 free; Stage 2 £725+VAT/yr >£1m turnover); CE/CE+ | 3–12 months | £30k–£300k/yr | [Hellios](https://hellios.com/supplier-payment-info-joscar/) |
| **US** | **SAM.gov + micro-purchase / SAP** | UEI + CAGE; CMMC L1 self-assessment if handling FCI | 1–3 weeks registration, then opportunity-dependent | <$250k | [SAM guidance](https://blogs.usfcr.com/sam-registration-what-they-dont-tell-you) |
| **US** | **SBIR / STTR** | None at Phase I | 6–12 months | **Phase I ≤ $250k; Phase II ≤ $1.75M** | [SBIR.gov](https://www.sbir.gov/tutorials/program-basics/tutorial-4) |
| **US** | **DIU Commercial Solutions Opening → OT prototype** | Commercial track record required; ATO needed to deploy | **60–90 day target; ~120 day recent average** | $500k–$5M prototype | [DIU](https://www.diu.mil/work-with-us/open-solicitations) |
| **US** | **GSA Multiple Award Schedule (SIN 54151S)** | FedRAMP for cloud; pricing disclosure | **6–12 months to award** (IT 3–4 months post-submission) | Task-order dependent | [GSA MAS](https://www.gsa.gov/buy-through-us/purchasing-programs/multiple-award-schedule) |
| **US DoD** | **IL4/IL5 workloads** | FedRAMP Moderate/High + DoD PA + **CMMC L2** | 12–24 months | $250k–$2M/yr | [DoD CC SRG](https://docs.cloud.google.com/docs/security/compliance/fedramp-dod-compliance-scope) |
| **NATO** | **NSPA Source File** | Free registration + **national Declaration of Eligibility** | 2–6 months registration; award cycle longer | €50k–€500k | [NSPA](https://www.nspa.nato.int/business/procurement/vendor) |
| **NATO** | **NCIA Basic Ordering Agreement** | Declaration of Eligibility from home nation | 3–9 months to BOA; then mini-competitions | €100k–€1M | [NCIA BOA](https://www.ncia.nato.int/business/do-business-with-us/basic-ordering-agreement-programme/what-is-a-basic-ordering-agreement-boa.html) |
| **NATO** | **DIANA accelerator** | None; dual-use eligibility | ~6–9 months from application | **€100k Phase 1, up to +€300k Phase 2** | [Innovate UK / DIANA](https://iuk-business-connect.org.uk/opportunities/nato-defence-innovation-accelerator-diana-2026-cohort/) |
| **EU** | **European Defence Fund (EDF) 2026** | EU/associated-country establishment; consortium ≥3 entities from ≥3 states | 9–15 months (call → grant) | Open-topic ≤ €6M; topic projects €10–100M | [FFG EDF 2026](https://www.ffg.at/en/europe/edf/calls/2026) |
| **EU** | **EDIP** (in force 30 Dec 2025, €1.5bn 2025–27) | **Non-EU components ≤35% of component cost; design authority in EU** | 12–24 months | Programme-scale | [Council](https://www.consilium.europa.eu/en/press/press-releases/2025/12/08/european-defence-industry-programme-council-gives-final-approval/) |
| **Australia** | Defence tender + **AIC Plan** | AIC Plan mandatory above **A$4M** (A$7.5M construction) | 9–18 months | A$100k–A$1M | [ANAO](https://www.anao.gov.au/work/performance-audit/maximising-australian-industry-participation-through-defence-contracting) |
| **Canada** | Defence procurement + **ITB/Value Proposition** | ITB mandatory >C$100M; reviewed C$25–100M | 12–24 months | C$100k–C$1M | [ISED](https://ised-isde.canada.ca/site/industrial-technological-benefits/en/itb-policy) |
| **Gulf (KSA)** | GAMI-managed procurement + **LCGPA local content** | Local content score weighted **≥30%** of financial bid; some tenders require ≥40% to bid | 12–36 months; local entity effectively required | $250k–$2M | [LCGPA/SPA](https://spa.gov.sa/en/N2563894) |
| **Gulf (UAE)** | Tawazun-managed procurement | **60% offset obligation**, 8.5% bank guarantee | 12–36 months | $250k–$2M | [Chambers](https://chambers.com/articles/new-tawazun-economic-program-policy-guidelines-issued) |

### 2.2 What the table means

The pattern is consistent across markets: **innovation funds pay in months, framework call-offs pay in quarters, programmes of record pay in years.** A vendor that designs its business model around innovation contracts and framework call-offs can be revenue-positive inside a year; a vendor that targets programmes of record needs 24–36 months of runway.

Two structural facts compound this. First, UK MOD's own Segmented Acquisition Model concedes the point: software gets a **three-month** contracting target precisely because the default is slow ([Bird & Bird / Gowling analysis](https://gowlingwlg.com/en/insights-resources/articles/2026/uk-defence-investment-plan-2026)). Second, the NAO has documented that across 13 major programmes, forecast net delays reached **254 months** in achieving entry into service, with average full-operating-capability delay of **26 months** ([NAO via Commons Library](https://commonslibrary.parliament.uk/research-briefings/cbp-9566/)). A SaaS vendor should not price or plan against programme timelines.

---

## 3. Accreditation Boundary Analysis — Where a Commercial SaaS Can Legally Operate

This is the decisive question for product viability. The answer is more permissive than the industry's reputation suggests.

### 3.1 UK: OFFICIAL and OFFICIAL-SENSITIVE are commercially reachable

The Government Security Classifications Policy sets three tiers — OFFICIAL, SECRET, TOP SECRET — and states that technical controls at OFFICIAL use **"good commercial"** ICT products and services ([GSCP](https://www.gov.uk/government/publications/government-security-classifications/government-security-classifications-policy-html)). **OFFICIAL-SENSITIVE is not a separate classification**; it is a handling caveat applied to a subset of OFFICIAL information that "is not intended for public release and that is of at least some interest to threat actors" (same source). This matters enormously: there is no separate accreditation regime to cross.

The empirical proof is on the Digital Marketplace. Kahootz Enterprise is listed as **"assessed to Secure-by-Design principles to store and share information marked up to OFFICIAL-SENSITIVE"**, hosted in the **United Kingdom**, ISO/IEC 27001 certified and Cyber Essentials Plus certified, at **£3.69 to £11.69 a user a month** ([listing](https://www.applytosupply.digitalmarketplace.service.gov.uk/g-cloud/services/863966228041800)). That is a commodity SaaS price point for defence-classified collaboration.

**What a UK SaaS actually needs at OFFICIAL-SENSITIVE:**

| Requirement | Detail | Source |
|---|---|---|
| UK data residency | Expected for most public sector workloads | [G-Cloud framework guidance](https://www.gov.uk/government/news/g-cloud-relaunches-with-biggest-upgrade-in-its-history) |
| ISO/IEC 27001 | Mandatory for G-Cloud 15 lots | [Computer Weekly](https://www.computerweekly.com/news/366634470/CCS-under-fire-over-anti-SME-supplier-requirements-for-G-Cloud-15) |
| ISO 9001, ISO 20000-1, ISO 27018 | Mandatory for G-Cloud 15 | same |
| Cyber Essentials / Plus | Mandatory at every level of the MOD Cyber Security Model; CE+ for higher risk profiles | [IASME](https://iasme.co.uk/articles/iasme-launches-defence-cyber-certification-dcc-scheme-for-uk-ministry-of-defence-suppliers/) |
| **Defence Cyber Certification (DCC)** | New organisation-wide scheme replacing per-contract assurance. Level 0 = 3 controls; Level 1 = 101 controls; Levels 2–3 require CE+ | [IASME](https://iasme.co.uk/articles/iasme-launches-defence-cyber-certification-dcc-scheme-for-uk-ministry-of-defence-suppliers/) |
| Secure by Design | Mandated MOD approach for capabilities and services handling Defence data, including supplier-delivered | [Logiq summary](https://www.logiq.co.uk/insights/mod-secure-by-design-guide/) |
| DEFCON 658 | Contractual cyber clause; binds cyber risk obligations | [Logiq](https://www.logiq.co.uk/insights/defcon-658-cyber-obligations/) |

**So-what:** a well-run SaaS with ISO 27001, CE+, UK hosting and a Secure by Design evidence pack can sell to UK defence at OFFICIAL-SENSITIVE **without a single classified accreditation**. Total cost of this posture is realistically £30k–£80k in year one (certification, audit, pen testing, documentation) — an order of magnitude below FedRAMP.

**The one place the door is closing:** G-Cloud 15's **Lot 1b** (hosting data above OFFICIAL) now demands **£75m of insurance**, up from roughly £7m under G-Cloud 14, plus a Gold Standard Financial Viability Readiness Assessment. A supplier quoted by Computer Weekly said the requirements "make it very clear that smaller and SME cloud providers are not welcome." Security specialist Owen Sayers warned that "services above 'official' are one of the last existing preserves of UK SMEs" ([source](https://www.computerweekly.com/news/366634470/CCS-under-fire-over-anti-SME-supplier-requirements-for-G-Cloud-15)). **Design the product to stay at or below OFFICIAL-SENSITIVE.**

### 3.2 US: IL2 is commercial, IL4 is the CUI wall, IL5 is a different business

- **IL2** handles publicly releasable and non-critical mission information; its baseline security requirements are equivalent to **FedRAMP Moderate**, and IL2 information may be hosted in a cloud service offering that minimally holds a FedRAMP Moderate or High provisional authorisation.
- **IL4** protects **Controlled Unclassified Information (CUI)**. A FedRAMP High provisional authorisation is accepted for a DoD IL4 PA without assessment of extra controls, but assessment of non-control SRG requirements is still needed.
- **IL5** covers mission-critical CUI and unclassified National Security Systems.
([Google Cloud FedRAMP/DoD scope](https://docs.cloud.google.com/docs/security/compliance/fedramp-dod-compliance-scope); [Microsoft IL4 offering](https://learn.microsoft.com/en-us/azure/compliance/offerings/offering-dod-il4))

**What is sellable without accreditation:** advisory and integration services, on-premise/self-hosted deployments the customer accredits, products sold to *contractors* rather than to government systems, and unclassified-data products at IL2 once FedRAMP Moderate is in hand. Second Front's guidance to SaaS vendors is explicitly architectural rather than accreditation-first: **containerise** with Docker/Podman, **limit external service dependencies** for IL4+, and **design cloud-agnostic** deployments ([Second Front](https://www.secondfront.com/resources/blog/how-to-know-if-your-saas-product-is-ready-for-defense-use/)).

**CMMC is now live and non-optional.** The 48 CFR acquisition rule was published **10 September 2025** and took effect **10 November 2025**. Phase 1 (first 12 months) is largely Level 1/Level 2 **self-assessment**; from **November 2026**, Level 2 third-party (C3PAO) certification appears in all applicable solicitations; Level 3 from November 2027 ([PreVeil](https://www.preveil.com/blog/cmmc-final-rule-published/); [Summit 7](https://summit7.us/blog/final-rule-update-48-cfr-and-the-cmmc)). **So-what:** a vendor that will touch CUI should budget for C3PAO assessment in FY2027, not defer it.

**The accreditation shortcut that actually works.** Rather than pursuing a standalone ATO, vendors deploy onto an already-accredited platform. Second Front's Game Warden offers inheritable controls from a **FedRAMP High / DoD IL5 / GovRAMP High** platform, with ATO "in as little as 90 days"; one customer is cited as earning accreditation in **58 days** ([Second Front](https://www.secondfront.com/solutions/dod-accreditations/)). This converts a 12–18 month, $500k–$2M accreditation project into a quarter and a platform fee.

### 3.3 Cloudflare specifically

For a Cloudflare-hosted SaaS the position as of September 2026 is:

- **US federal civilian: viable now.** Cloudflare for Government holds **FedRAMP High** (August 2026) and **GovRAMP Moderate** (April 2026), covering integrated security, performance, AI and developer services ([Cloudflare](https://www.cloudflare.com/press/press-releases/2026/cloudflare-achieves-fedramp-high-authorization-to-secure-and-accelerate-the-u-s-governments-critical-missions/); [Nextgov](https://www.nextgov.com/acquisition/2026/08/cloudflare-seek-dod-il4-authorization-after-new-fedramp-govramp-designations/415299/)). Departments including Energy, HHS, Commerce, Homeland Security, Interior, Justice and State already deploy Cloudflare technologies.
- **DoD CUI (IL4): not yet.** Cloudflare has announced *intent* to pursue IL4; it does not hold it. A CUI-bearing product cannot run on the commercial Cloudflare estate today.
- **UK OFFICIAL-SENSITIVE: viable, with care.** Nothing in GSCP or the MOD Secure by Design regime prohibits a commercial hyperscale edge provider. The binding constraints are **UK data residency** for the data store and demonstrable ISO 27001/CE+ control coverage, which a Cloudflare-hosted architecture can satisfy if regional data localisation is configured and evidenced.
- The press release does not itemise Workers or individual developer products as separately authorised components — a vendor should confirm scope per-service before claiming inheritance. `[Treat product-level scope as UNVERIFIED until checked against the FedRAMP Marketplace entry.]`

---

## 4. Offset and Industrial Participation Obligations — Deep Dive

### 4.1 The size of the pool

The authoritative primary source is the US Bureau of Industry and Security's annual report to Congress under Section 723 of the Defense Production Act. The **28th study** (covering 1993–2022) reports:

| Metric (1993–2022 cumulative, US firms only) | Value | Source |
|---|---|---|
| Defense export contract value with associated offsets | **$251,704M** | [BIS 28th Study, Table 2-1](https://www.bis.gov/media/documents/public-version-28th-annual-offsets-report.pdf) |
| Offset agreement value | **$142,118M** | same |
| **Average offset as % of contract value** | **56.46%** | same |
| Number of offset agreements | **1,304** across **51 countries** | same |
| Offset transactions — actual value | **$106,953M** | Table 3-1 |
| Offset transactions — credit value | **$125,374M** | Table 3-1 |
| Number of transactions | **17,952** | Table 3-1 |

**Derived figure (DEFDR's own arithmetic, not a BIS statement):** $142.1bn of agreements less $125.4bn of credits delivered implies roughly **$16.7bn of unretired offset credit obligation held by US firms alone** over the period. Treat as an indicative floor, not a published figure.

For 2022 alone: **27 new offset agreements with 13 countries valued at $5.88bn**, equal to **32.82%** of $17.91bn in reported export contracts; **464 offset transactions with 24 countries**, actual value **$4.52bn**, credit value **$5.10bn**.

**Category mix (2022, by actual value)** — this is the shape of the work that offset obligations actually generate:

| Category | Actual value | % of total | Transactions |
|---|---|---|---|
| Purchasing | $1,218.4M | 26.96% | 186 (40.09%) |
| Investment | $1,209.3M | 26.76% | 34 |
| Technology transfer | $650.2M | 14.39% | 65 |
| Subcontract | $628.9M | 13.92% | 117 (25.22%) |
| Licensed production | $602.3M | 13.33% | 32 |
| Other | $135.6M | 3.00% | 20 |
| Training | $55.1M | 1.22% | 8 |
| Co-production | $18.9M | 0.42% | 2 |

Source: [BIS 28th Study, Table 3-2](https://www.bis.gov/media/documents/public-version-28th-annual-offsets-report.pdf). Note that **42 transactions (9.05%) carried a multiplier greater than one** — multipliers are a core reason offset accounting is hard and therefore a core reason software is needed.

Transparency International projects the **global** offset market at **$371bn for 2021–2025**, with US firms providing **$36.5bn–$52.4bn for FY2021–22 combined**, and identifies Indonesia, Malaysia, Oman, Saudi Arabia, Taiwan, UAE and the UK as high or very high corruption risk in offsets ([TI-Defence](https://ti-defence.org/blissfully-blind-security-risks-defence-contract-offset/)).

### 4.2 Country table

| Country | Regime / body | Threshold | Obligation level | Enforcement | Source |
|---|---|---|---|---|---|
| **Saudi Arabia** | GAMI (defence); LCGPA (general govt) | GAMI-managed procurement exempt from general procurement law | **50% localisation of military spend by 2030**; achieved **24.89% at end-2024**. LCGPA: local content weighting **≥30%** of financial bid; some tenders require **≥40%** score to bid | Bid ineligibility; binding contractual local-content targets | [GAMI](https://www.gami.gov.sa/en/news/gami-reports-localization-military-spending-saudi-arabia-increases-2489); [SPA/LCGPA](https://spa.gov.sa/en/N2563894) |
| **UAE** | Tawazun Economic Programme | Contract **> $10M** (or already-active obligations); 2019 guidelines raised trigger to **AED 36.73M** | **60% of contract value** in offset credits | **Unconditional on-demand bank guarantee = 8.5% of contract value**; Tawazun may liquidate the full guarantee and declare default | [Chambers](https://chambers.com/articles/new-tawazun-economic-program-policy-guidelines-issued); [Afridi & Angell](https://afridi-angell.com/new-tawazun-economic-program-policy-guidelines-issued/) |
| **India** | DAP 2020 offset guidelines | **₹2,000 crore** (Buy Global / Buy & Make) | **30% of acquisition cost**; waived if Indian vendor meets ≥30% indigenous content | PAC scrutiny; MoD rejects a large share of claims | [Mondaq](https://www.mondaq.com/india/government-contracts-procurement-ppp/1016564/offset-obligations-under-the-defence-acquisition-procedure-2020) |
| **India — performance** | CAG + PAC | — | CAG: 46 contracts 2005–Mar 2018 worth **₹66,427 crore**; **₹19,223 crore** due by Dec 2018, only **₹11,396 crore (59%)** claimed discharged, only **₹5,457 crore (48% of claims)** accepted. PAC: **26 contracts, $9.9bn obligations, $4.48bn (45%) unfulfilled at 31 Dec 2025** | PAC criticised MoD for "lacking a mechanism to measure the actual impact" | [CAG via PRS](https://prsindia.org/policy/report-summaries/management-of-defence-offsets); [Bharat Shakti](https://bharatshakti.in/pending-rs-42000-crore-defence-offsets-trigger-scrutiny-expert-says-concerns-may-be-overstated/) |
| **Türkiye** | SSB Industrial Participation/Offset Guideline | Set by SSB per procurement | **Minimum 70% of contract value** | Contractual; guideline revised 2011 and 2022 | [Herdem](https://herdem.av.tr/offset-and-industrial-participation-oip-regime-in-turkey) |
| **South Korea** | DAPA | Per procurement | **≥50%** competitive; **≥30%** sole-source. Policy shifting from technology transfer toward local manufacture | Contractual | [Lexology](https://www.lexology.com/library/detail.aspx?g=bd45be56-3415-4a71-9631-a4830e4149d9); [Defense Mirror](https://defensemirror.com/news/22772/S_Korean_Defence_Offsets_Policy_to_Seek_Local_Manufacture_Instead_of_Tech_Transfer) |
| **Poland** | Offset Act 2014 | No automatic threshold (previous EUR 5M auto-trigger removed) | Case-by-case; **indirect offsets abolished** — direct only | Ministry of Defence-negotiated | [TGC](https://www.tgc.eu/en/publications/new-offset-act-vs-offset-crisis-in-poland/); [Dentons guide](https://www.dentons.com/en/insights/guides-reports-and-whitepapers/2024/december/9/a-brief-guide-to-offset-agreements-in-poland) |
| **Greece** | Administrative guideline (not yet law) | Weapons system purchases under €30bn/12-yr programme | **25% of work to Greek domestic production**; potential **€6–8bn** to Greek industry over 12 years | Currently guideline only; industry pressing for legislation | [Greek City Times](https://greekcitytimes.com/2026/06/29/greek-defence-industry-30-billion-programme-25-percent-rule/); [ProtoThema](https://en.protothema.gr/2026/06/27/greek-defence-industry-a-last-major-opportunity-and-the-open-challenge-of-the-25-local-rarticipation-rule/) |
| **Norway** | Industrial Cooperation Agreements | **> NOK 50M** | Negotiated | Norwegian Defence Procurement Code | [GlobalSecurity](https://www.globalsecurity.org/military/world/europe/no-industry.htm) |
| **Canada** | ITB Policy + Value Proposition (ISED) | Mandatory **> C$100M**; reviewed C$25–100M | **100% of contract value** in Canadian business activity | AG found 8 of 60 eligible >$100M procurements had **no** ITB obligations and 2 had **<100%**; "benefits and full costs... were unknown" | [ISED](https://ised-isde.canada.ca/site/industrial-technological-benefits/en/itb-policy); [OAG Report 10](https://www.canada.ca/en/auditor-general/our-work/audit-reports/parl-oag-202412-10-e.html) |
| **Australia** | Australian Industry Capability (AIC) Plan | **A$4M** materiel/non-materiel; **A$7.5M** construction | AIC Plan/Schedule, contractually binding | ANAO performance audit; 32 Defence templates require AIC above threshold | [Defence AIC](https://www.defence.gov.au/business-industry/industry-capability-programs/australian-industry-capability-program) |
| **Brazil** | PComTIC Defesa (Ordinance GM-MD 3,990, 3 Aug 2023) | Imports **> $50M** (previously $5M since 2002) | Cooperation agreements mandatory unless proven impossible | Ministry of Defence | [FRS](https://www.frstrategie.org/web/documents/publications/defense-et-industries/2024/20/DefenseIndustries_N20_art6.pdf) |
| **Switzerland** | armasuisse offset register | — | **18 ongoing programmes, CHF 5.42bn total; CHF 2.85bn executed to end-2025** → ~**CHF 2.57bn outstanding** | Public register | [fedpol/armasuisse](https://www.fedpol.admin.ch/en/newnsb/v5kepmCgLH7b4rQEfTgqR) |
| **Netherlands** | Industrial Participation policy | — | `[UNVERIFIED]` — commonly cited at 100% of contract value but not confirmed against a primary source in this research | — | — |
| **Israel** | SIBAT / IMOD reciprocal procurement | — | `[UNVERIFIED]` — 35%/50% figures widely repeated but not confirmed against a primary source | — | — |

### 4.3 How obligations are tracked today — the opportunity

**Badly, and mostly in spreadsheets.** The evidence is consistent across three independent auditors and one consultancy:

- TI-Defence: the US government's "hands-off" approach "effectively leaves defence firms to mark their own homework," and US defence companies show "weak controls to prevent corruption in offsets. Many lack explicit policies and procedures to address the risks" ([source](https://ti-defence.org/blissfully-blind-security-risks-defence-contract-offset/)).
- Canada's Auditor General: ISED "lacked some elements to ensure sound administration," including inadequate "tracking of contract obligations, economic benefits, and job creation" ([source](https://www.canada.ca/en/auditor-general/our-work/audit-reports/parl-oag-202412-10-e.html)).
- India's PAC criticised MoD for "lacking a mechanism to measure the actual impact of defence offsets" ([source](https://bharatshakti.in/pending-rs-42000-crore-defence-offsets-trigger-scrutiny-expert-says-concerns-may-be-overstated/)).
- McKinsey notes offset obligations range from **30% to as much as 120%** of sales contract value and that reforms are "raising the bar for contractors' industrial participation" ([McKinsey](https://www.mckinsey.com/industries/public-sector/our-insights/defense-offsets-from-contractual-burden-to-competitive-weapon)).

Existing tooling is thin. PwC India markets a **web-based offset compliance monitoring application** that auto-generates periodic compliance reports and offset proposal documents ([PwC](https://www.pwc.in/assets/pdfs/industries/aerospace-and-defence/offset-management-tool.pdf)). Eurostep positions **ShareAspace** for controlled data sharing in offset-like collaborations ([Eurostep](https://eurostep.com/defense-offsets-from-contractual-burden-to-competitive-weapon/)). Rheinmetall runs offset compliance as an internal corporate function ([Rheinmetall](https://www.rheinmetall.com/en/company/compliance/offset-agreements)). **There is no dominant, named, multi-country offset obligation management SaaS.** That is a genuine white space — with the caveat that the buyer is a prime contractor's compliance function or a national offset authority, not a ministry's IT department.

---

## 5. Buying-Process Friction Catalogue

### 5.1 Opportunity discovery is fragmented by design

A vendor selling into three countries must monitor, at minimum:

| Portal | Scope | Threshold |
|---|---|---|
| Defence Sourcing Portal (contracts.mod.uk) | All UK MOD opportunities | **> £10,000** |
| Find a Tender Service (UK) | High-value UK public sector | usually **> £139,688** inc VAT |
| Contracts Finder (UK) | UK government contracts | **> £12,000** inc VAT |
| Digital Marketplace / G-Cloud | UK cloud call-offs | n/a |
| SAM.gov | All US federal | n/a |
| NSPA ePortal | NATO support/procurement | n/a |
| NCIA BOA portal | NATO CIS | n/a |
| EU Funding & Tenders Portal | EDF/EDIP | n/a |

Sources: [digital.mod.uk](https://www.digital.mod.uk/sme-dosbg/contracting-with-defence/supplying-to-defence); [NSPA](https://www.nspa.nato.int/business/procurement/vendor). Suppliers can also publish their own subcontracting opportunities on the DSP — an underused channel.

### 5.2 Prequalification burden

| Gate | Cost | Elapsed time |
|---|---|---|
| JOSCAR Stage 1 | Free | Days–weeks |
| JOSCAR Stage 2 | Free < £1M turnover; **£725 + VAT/yr** above | Weeks |
| Cyber Essentials / Plus | Low £k | Weeks; **from 27 April 2026 the Danzell question set makes MFA on all cloud services an auto-fail item** ([Amtivo](https://amtivo.com/uk/standards/cyber-essentials/guides/mod-cyber-essentials-requirements-guide/)) |
| Defence Cyber Certification Level 0 | Not published | MOD asked industry partners to achieve **Level 0 by 31 December 2026** ([NCC Group](https://www.nccgroup.com/understanding-the-defence-cyber-certification-dcc-scheme-what-suppliers-need-to-know/)) |
| ISO 27001 + 9001 + 20000-1 + 27018 | £20k–£60k | 4–9 months |
| SAM.gov (UEI + CAGE) | Free | **1–3 weeks** (UEI 1–2 days; CAGE 7–10 business days) |
| GSA MAS | Consultant fees | **6–12 months** |
| FedRAMP Rev5 Moderate | **$250k–$750k** | 12–18 months |
| FedRAMP 20x Low/Mod | **~$100k–$300k** (early estimates) | Pilot achieved **119 days** |
| CMMC Level 2 (C3PAO) | Not published | Required in all applicable solicitations from **Nov 2026** |

### 5.3 Bid costs

BidWrite's analysis of Australian defence tendering estimates industry bid cost at **1.5% of contract value per bid**, with an average **3.3 bids per tender**, putting total industry investment in bid costs at approximately **A$1.4bn in FY22–23**; sub-contractors supporting a prime's proposal typically invest a further **up to 0.5%** of their potential contract value ([BidWrite](https://www.bidwrite.com.au/insights/reducing-the-1b-cost-of-defence-tendering/)). **So-what:** for a £200k SaaS deal, a compliant bid costs ~£3k of direct effort — but the expected-value calculation collapses if win rate is below ~30%, which it will be for a new entrant without a framework position.

### 5.4 Concentration and framework lock-out

- Top five suppliers: **over 29% of all MOD procurement spending** in 2025.
- Top ten frameworks awarded **over £6bn** of new MOD contracts in 2025; **half had fewer than 20 suppliers, three had fewer than ten**.
- SME share of MOD direct procurement spend: **5% in 2024**; defence-sector spending with SMEs **3% in 2025**.
([Tussell](https://www.tussell.com/insights/defence-procurement-tracker))

### 5.5 Sub-tier visibility — the flow-down problem

Prime contractors have lost visibility into their sub-tiers, "especially below third-tier levels," and most sub-tier verification remains "document-based, paper-based, or simply implicit" ([IdentiGate](https://identigate.com/defence/supply-chain/); [CE Interim](https://ceinterim.com/defence-supply-chain-bottlenecks/)). This is now being regulated:

- **Section 805, FY2024 NDAA:** DoD may not directly contract with a 1260H-listed company or a controlled entity from **30 June 2026**; from **30 June 2027** it may not *indirectly* contract — i.e. buy goods or services containing listed-entity content **anywhere upstream** ([Plante Moran](https://www.plantemoran.com/explore-our-thinking/insight/2026/07/your-tier-2-suppliers-are-now-a-dod-compliance-question); [Wiley](https://www.wiley.law/alert-NDAA-Provisions-Impacting-Governments-Contractors-and-Their-Supply-Chains)).
- **Supply Chain Illumination:** established in the FY2025 NDAA and continued in the FY2026 NDAA; major systems contractors must submit supply chain information ([Government Contracts Legal Forum](https://www.governmentcontractslegalforum.com/2025/12/articles/dod/the-fy-2026-national-defense-authorization-act/)).
- UK MOD's SME Action Plan commits to working with strategic partners on aligned action plans and spend projections, but **contains no explicit mandate for tier 2+ subcontract spend disclosure** ([SME Action Plan](https://www.gov.uk/government/publications/mod-small-and-medium-sized-enterprise-sme-action-plan/ministry-of-defences-small-and-medium-sized-enterprise-sme-action-plan)) — even though 75% of MOD's ~£5bn SME spend flows through the supply chain rather than direct award, meaning MOD cannot see three-quarters of its own SME spend without asking primes.

**So-what:** the mandated obligation (Section 805) plus the measurement gap (UK 75% indirect SME spend) plus the audit criticism (Canada, India) is the strongest triangulated case in this report for a supply-chain/obligation data product.

---

## 6. Incumbents and Comparable Pricing

### 6.1 Adjacent vendors and their pricing

| Vendor | Category | Published/reported price | Source |
|---|---|---|---|
| **Deltek GovWin IQ** | US opportunity intelligence | **$13,000–$119,000/yr**, average ~**$29,000/yr**; single seat ~$12,000/yr, enterprise $42,000+/yr | [Civic IQ analysis](https://civiciq.com/blog/govwin-iq-pricing-2026) |
| **Loopio** | RFP response management | **~$1,440 per user per year** + ~**$3,000** one-time implementation | [Vendr](https://www.vendr.com/marketplace/loopio) |
| **Responsive (ex-RFPIO)** | RFP response management | Custom; reported **~$20,000 floor** | [Vercor](https://vercor.ai/resources/rfp-response/rfp-software-pricing-2026) |
| **Stotles** | UK/EU public sector tender intelligence | Not published `[UNVERIFIED]` | [stotles.com](https://www.stotles.com/) |
| **Tussell** | UK public sector spend data | Not published `[UNVERIFIED]` | [tussell.com](https://www.tussell.com/) |
| **Commerce Decisions (AWARD)** | Tender evaluation — **MOD's official procurement solutions partner** | Not published | [commercedecisions.com](https://commercedecisions.com/mod/) |
| **PwC India** | Offset compliance monitoring tool | Not published | [PwC](https://www.pwc.in/assets/pdfs/industries/aerospace-and-defence/offset-management-tool.pdf) |
| **Eurostep ShareAspace** | Controlled data sharing for offsets/export control | Not published | [Eurostep](https://eurostep.com/defense-offsets-from-contractual-burden-to-competitive-weapon/) |
| **Second Front (Game Warden)** | Accreditation-as-a-service | "Transparent, usage-based pricing"; not published | [Second Front](https://www.secondfront.com/products/game-warden/) |

### 6.2 What defence actually pays for software

| Contract | Value | Notes | Source |
|---|---|---|---|
| **Palantir — US Army Enterprise Agreement** | **Up to $10bn / 10 years** | Ceiling, not commitment; consolidates 75 contracts (15 prime, 60 subcontracts) | [CNBC](https://www.cnbc.com/2025/08/01/palantir-lands-10-billion-army-software-and-data-contract.html) |
| **Palantir — Maven Smart System** | **~$1.3bn** | Ceiling increase | [The Defense Post](https://thedefensepost.com/2025/08/02/palantir-us-army-contract/) |
| **DISA — Broadcom/VMware BPA** | **$970M / 5 years** | March 2026 | [SLED.AI summary](https://www.sledai.com/blog/government-contracts-for-it-companies/) |
| **UK MOD — Google Cloud sovereign cloud** | **£400M** | Google Distributed Cloud air-gapped platform, Sept 2025 | [Google Cloud](https://www.googlecloudpresscorner.com/2025-09-11-Google-Cloud-Awarded-Landmark-Sovereign-Cloud-Contract-with-UK-Ministry-of-Defence) |
| **UK MOD — commercial/procurement technology & data platform** | **£2,500,000** | Published 31 July 2026; end-to-end procurement lifecycle integration, single source of truth for commercial data, AI-enabled automation | [TenderTracker](https://tendertracker.co.uk/contracts/ocds-h6vhtk-06d85d) |
| **Kahootz Enterprise (OFFICIAL-SENSITIVE collaboration)** | **£3.69–£11.69 per user per month** | The realistic per-seat comparator for a defence SaaS | [Digital Marketplace](https://www.applytosupply.digitalmarketplace.service.gov.uk/g-cloud/services/863966228041800) |
| **G-Cloud market size** | **~£15bn cumulative since 2012; £2.9bn in FY2024/25**; SMEs took **37.43%** of sales over the last five years | | [Advice Cloud / CCS data](https://advice-cloud.co.uk/knowledge-hub/g-cloud-dos-spending-review-2023-24/) |

**Pricing conclusion:** the two credible price anchors for a new defence SaaS are (a) **£4–£12 per user per month** for a commodity collaboration/workflow tool at OFFICIAL-SENSITIVE, and (b) **£150k–£2.5m as a departmental platform** where the product is the system of record for a commercial or supply-chain process. A vendor should not model per-seat pricing above roughly £25/user/month without a defensible differentiator, and should expect a **£2.5m ceiling** for a first-generation MOD commercial data platform.

---

## 7. Procurement Reform Watchlist 2025–2027 — New Obligations Software Could Serve

| Reform | Date | New obligation created | Product implication |
|---|---|---|---|
| **UK Segmented Acquisition Model** | April 2026 | Software/AI/COTS must be contracted in **3 months**; upgrades 1 year; major platforms 2 years | Buyers need tooling that makes a 3-month cycle auditable. Opportunity for pipeline/approval tracking |
| **UK Defence Investment Plan** | June 2026; **£298bn over 4 years** | Six Commercial Pathways published; **300+ procurements have self-selected at least one pathway** | Pathway selection, evidence capture and reporting is a new, unowned workflow |
| **UK Defence Industrial Strategy 2025 + SME Action Plan** | Sept 2025 / Jan 2026 | SME spend to rise **£5bn → £7.5bn by summer 2028** (£2bn direct + £5.5bn indirect by 2027/28); Defence Office for Small Business Growth live Jan 2026 | MOD must *measure* indirect SME spend it currently cannot see — a supply-chain reporting product |
| **Government Commercial Agency (GCA)** | 1 April 2026 | CCS + Cabinet Office central commercial teams merged; **>£400bn annual spend** under one agency | Framework and call-off processes re-platforming; new entrants' window |
| **G-Cloud 15** | Award 6 Aug 2026; buyer access mid-Aug; **G-Cloud 14 expires late Oct 2026**; reopens to new suppliers ~18 months after go-live | New mandatory certifications; Lot 1b £75m insurance | **Hard deadline:** vendors not on G-Cloud 15 wait ~18 months for the reopening |
| **UK Defence Cyber Certification** | Level 0 requested by **31 Dec 2026** | Organisation-wide certification replacing per-contract assurance | Compliance evidence management |
| **CMMC 48 CFR rule** | Effective 10 Nov 2025; **L2 C3PAO in all applicable solicitations from Nov 2026**; L3 Nov 2027 | Certification as condition of award | Assessment-readiness and evidence products |
| **Section 805, FY24 NDAA** | Direct prohibition **30 Jun 2026**; indirect **30 Jun 2027** | Contractors must know and attest sub-tier identity and country of origin **anywhere upstream** | The strongest single regulatory driver for N-tier supply chain data |
| **DoD Supply Chain Illumination** | FY25 NDAA, continued FY26 | Major systems contractors submit supply chain information | Data collection and submission tooling |
| **FedRAMP 20x** | Phase 3 live 2026; Consolidated Rules June 2026; submission pipeline opened Aug 2026 | Continuous monitoring replaces static annual assessments | Continuous-compliance evidence generation |
| **EU EDIP** | In force **30 Dec 2025**; €1.5bn 2025–27 | **Non-EU components ≤35% of component cost**; design authority must generally be in EU | Component-origin tracing and attestation |
| **EDF 2026** | ~**€1.01bn** across 31 topics | Consortium ≥3 entities from ≥3 member states | Consortium formation/management |
| **Saudi LCGPA expansion** | Feb 2026 | Minimum local content percentages increased for Mandatory List products; 30% minimum at company level phasing into consulting tenders | Local content calculation and certification |
| **Greece 25% rule** | Administrative guideline 2026 | 25% of weapons contract work to Greek industry | Local participation tracking |

---

## 8. Fastest Credible Path from Zero to First Paid Defence Customer (Cloudflare-hosted SaaS)

**Answer: roughly 4–9 months, in the UK, at OFFICIAL-SENSITIVE, paid by either an innovation body or a prime contractor — not by a ministry's programme office.**

### Why the UK and not the US

The US path is structurally slower for a Cloudflare-hosted product because the DoD CUI boundary (IL4) is not yet available on Cloudflare's government platform. FedRAMP High covers federal civilian; it does not cover DoD CUI. Pursuing FedRAMP independently costs **$100k–$300k (20x) or $250k–$750k (Rev5)** and 4–18 months before a single dollar arrives. The UK requires no equivalent national cloud authorisation at OFFICIAL-SENSITIVE — only commercial certifications and a Secure by Design evidence pack.

### The sequence

**Months 0–2 — Establish the minimum credible posture.**
1. Register on the **Defence Sourcing Portal** (free) and **JOSCAR Stage 1** (free).
2. Achieve **Cyber Essentials Plus** — noting the Danzell question set from 27 April 2026 makes MFA on all cloud services an auto-fail item.
3. Configure **UK data residency** for all customer data and document it.
4. Begin **ISO 27001** (4–9 months; start now, sell in parallel).
5. Start the **Defence Cyber Certification Level 0** (3 controls) ahead of the 31 Dec 2026 request.

**Months 1–4 — Get paid by an innovation route while the certifications mature.**
6. Bid **DASA / UKDI open calls**. Typical funding **£100k–£350k**, 100% funded, 12–18 month projects, five UKDI themes (Autonomy, Decision Advantage, Logistics and Support, Effects, Protection). This is a *contract*, not a grant — it is revenue, it is a defence customer reference, and it requires no accreditation at bid stage.
7. In parallel, approach **primes** (BAE, Babcock, Leonardo, Thales, QinetiQ) with a subscription priced at **£4–£12 per user per month**. Primes buy from their own budgets, have no OJEU-style tender obligation below threshold, and are motivated by MOD's SME spend target — 75% of the £5bn SME figure flows through them.
8. Apply to **NATO DIANA** if dual-use: **€100k Phase 1**, up to **+€300k** Phase 2. 2026 cohort was 150 firms from 3,000+ applicants — low probability, high signal.

**Months 3–9 — Convert to a repeatable framework position.**
9. **G-Cloud 15 is the single most important calendar item.** It was awarded 6 August 2026 and reopens to new suppliers only ~18 months after go-live. Target **Lot 2/3 (software/support)** — avoid Lot 1b, whose £75m insurance requirement is prohibitive.
10. Once listed, pursue **direct award call-offs** from MOD and wider public sector. G-Cloud is a direct-award framework: no competitive tender is required.

**Months 6–18 — Second market.**
11. **US:** register SAM.gov (1–3 weeks), pursue **SBIR Phase I (≤$250k)** or a **DIU CSO** (60–90 day target, ~120 day actual). For deployment, use an accredited platform such as Game Warden (ATO "in as little as 90 days") rather than a standalone ATO.
12. **NATO:** NSPA Source File registration (free) and an **NCIA Basic Ordering Agreement**, both requiring a national Declaration of Eligibility.

### What to avoid

- **Do not target SECRET or above.** It changes the company, not the product.
- **Do not target G-Cloud Lot 1b.** £75m insurance.
- **Do not build the business plan on a programme of record.** NAO evidence: 13 programmes with 254 months of net forecast delay; average FOC delay 26 months.
- **Do not assume the ministry is the buyer.** In the UK, 75% of MOD SME spend is indirect. The prime is the faster customer.
- **Do not claim inherited Cloudflare authorisations without checking service-level scope** on the FedRAMP Marketplace.

### Expected first-year outcome

A disciplined vendor should expect **£100k–£400k of first-year defence revenue** — one innovation contract plus one or two prime subscriptions — with G-Cloud 15 listing converting into **£250k–£1m of framework call-off pipeline** in year two. Anyone forecasting a seven-figure ministry contract in year one is forecasting a fantasy.

---

## 9. Sources

**Verification note.** All 85 cited URLs were checked. The following were directly retrieved and their content read during this research: the BIS 28th Offsets Report (PDF, text-extracted locally), GOV.UK G-Cloud 15 and MOD SME Action Plan pages, digital.mod.uk, the Kahootz Digital Marketplace listing, fedramp.gov/20x, diu.mil, Cloudflare's press release, Nextgov, Computer Weekly, IASME, Plante Moran, Transparency International, the Canadian Auditor General's Report 10, GAMI, Stotles, Tussell and Bharat Shakti. The remainder were located through search-engine indexing and returned HTTP 403 or a connection timeout to an automated `curl` request — normal bot-protection behaviour for those domains (parliament.uk, consilium.europa.eu, nspa.nato.int, ncia.nato.int, mckinsey.com, anao.gov.au, defence.gov.au, secureframe.com, lexology.com, cnbc.com and similar). Those citations should be opened in a browser before external reuse.

**Primary — government and official**
- BIS, *Offsets in Defense Trade, Twenty-Eighth Study* — https://www.bis.gov/media/documents/public-version-28th-annual-offsets-report.pdf
- GOV.UK, *G-Cloud relaunches with biggest upgrade in its history* — https://www.gov.uk/government/news/g-cloud-relaunches-with-biggest-upgrade-in-its-history
- GOV.UK, *Government Security Classifications Policy* — https://www.gov.uk/government/publications/government-security-classifications/government-security-classifications-policy-html
- GOV.UK, *MOD SME Action Plan* — https://www.gov.uk/government/publications/mod-small-and-medium-sized-enterprise-sme-action-plan/ministry-of-defences-small-and-medium-sized-enterprise-sme-action-plan
- GOV.UK, *MOD trade, industry and contracts 2025* — https://www.gov.uk/government/statistics/mod-trade-industry-and-contracts-2025/mod-trade-industry-and-contracts-2025
- GOV.UK, *UKDI unifies innovation* — https://www.gov.uk/government/news/ukdi-unifies-innovation-to-accelerate-frontline-capabilities-and-drive-national-growth
- GOV.UK, *DASA Open Call for Innovation* — https://www.gov.uk/government/publications/defence-and-security-accelerator-dasa-open-call-for-innovation
- digital.mod.uk, *Supplying to Defence* — https://www.digital.mod.uk/sme-dosbg/contracting-with-defence/supplying-to-defence
- Digital Marketplace, *Kahootz Enterprise* — https://www.applytosupply.digitalmarketplace.service.gov.uk/g-cloud/services/863966228041800
- FedRAMP, *20x* — https://www.fedramp.gov/20x/
- DIU, *Open Solicitations* — https://www.diu.mil/work-with-us/open-solicitations
- NSPA, *Vendor Registration* — https://www.nspa.nato.int/business/procurement/vendor
- NCI Agency, *Basic Ordering Agreement* — https://www.ncia.nato.int/business/do-business-with-us/basic-ordering-agreement-programme/what-is-a-basic-ordering-agreement-boa.html
- Council of the EU, *EDIP final approval* — https://www.consilium.europa.eu/en/press/press-releases/2025/12/08/european-defence-industry-programme-council-gives-final-approval/
- ISED Canada, *ITB Policy* — https://ised-isde.canada.ca/site/industrial-technological-benefits/en/itb-policy
- Auditor General of Canada, *Report 10 — Industrial and Technological Benefits* — https://www.canada.ca/en/auditor-general/our-work/audit-reports/parl-oag-202412-10-e.html
- Australian Government Defence, *AIC Program* — https://www.defence.gov.au/business-industry/industry-capability-programs/australian-industry-capability-program
- ANAO, *Maximising Australian Industry Participation* — https://www.anao.gov.au/work/performance-audit/maximising-australian-industry-participation-through-defence-contracting
- GAMI, *Localization of military spending 24.89%* — https://www.gami.gov.sa/en/news/gami-reports-localization-military-spending-saudi-arabia-increases-2489
- Saudi Press Agency, *LCGPA local content weighting* — https://spa.gov.sa/en/N2563894
- House of Commons Library, *Defence procurement reform* — https://commonslibrary.parliament.uk/research-briefings/cbp-9566/
- House of Commons Defence Committee, *It is broke — and it's time to fix it* — https://publications.parliament.uk/pa/cm5803/cmselect/cmdfence/1099/report.html
- Swiss Confederation, *Offset transactions as of end 2025* — https://www.fedpol.admin.ch/en/newnsb/v5kepmCgLH7b4rQEfTgqR
- SBIR.gov, *Program basics* — https://www.sbir.gov/tutorials/program-basics/tutorial-4
- GSA, *Multiple Award Schedule* — https://www.gsa.gov/buy-through-us/purchasing-programs/multiple-award-schedule

**Vendor and industry**
- Cloudflare press release, FedRAMP High — https://www.cloudflare.com/press/press-releases/2026/cloudflare-achieves-fedramp-high-authorization-to-secure-and-accelerate-the-u-s-governments-critical-missions/
- Nextgov, *Cloudflare to seek DoD IL4* — https://www.nextgov.com/acquisition/2026/08/cloudflare-seek-dod-il4-authorization-after-new-fedramp-govramp-designations/415299/
- Second Front, *DoD Accreditations* — https://www.secondfront.com/solutions/dod-accreditations/
- Second Front, *Is your SaaS ready for defense use* — https://www.secondfront.com/resources/blog/how-to-know-if-your-saas-product-is-ready-for-defense-use/
- Hellios, *JOSCAR payment information* — https://hellios.com/supplier-payment-info-joscar/
- IASME, *Defence Cyber Certification scheme launch* — https://iasme.co.uk/articles/iasme-launches-defence-cyber-certification-dcc-scheme-for-uk-ministry-of-defence-suppliers/
- Tussell, *Defence Procurement Tracker* — https://www.tussell.com/insights/defence-procurement-tracker
- Stotles, *G-Cloud 15 award date* — https://www.stotles.com/resource/blog/g-cloud-15-award-date-moves-to-6-august-2026-what-suppliers-need-to-know
- Computer Weekly, *CCS under fire over anti-SME requirements for G-Cloud 15* — https://www.computerweekly.com/news/366634470/CCS-under-fire-over-anti-SME-supplier-requirements-for-G-Cloud-15
- BidWrite, *Reducing the $1B+ cost of defence tendering* — https://www.bidwrite.com.au/insights/reducing-the-1b-cost-of-defence-tendering/
- Deltek GovWin IQ pricing analysis — https://civiciq.com/blog/govwin-iq-pricing-2026
- Vendr, *Loopio pricing* — https://www.vendr.com/marketplace/loopio
- Secureframe, *FedRAMP cost breakdown Rev5 vs 20x* — https://secureframe.com/hub/fedramp/costs
- PreVeil, *CMMC 48 CFR final rule published* — https://www.preveil.com/blog/cmmc-final-rule-published/
- Wiley, *NDAA provisions impacting contractors and supply chains* — https://www.wiley.law/alert-NDAA-Provisions-Impacting-Governments-Contractors-and-Their-Supply-Chains
- Plante Moran, *Your tier 2 suppliers are now a DoD compliance question* — https://www.plantemoran.com/explore-our-thinking/insight/2026/07/your-tier-2-suppliers-are-now-a-dod-compliance-question
- Transparency International Defence & Security, *Blissfully blind* — https://ti-defence.org/blissfully-blind-security-risks-defence-contract-offset/
- McKinsey, *Defense offsets: from contractual burden to competitive weapon* — https://www.mckinsey.com/industries/public-sector/our-insights/defense-offsets-from-contractual-burden-to-competitive-weapon
- Chambers & Partners, *New Tawazun Economic Program policy guidelines* — https://chambers.com/articles/new-tawazun-economic-program-policy-guidelines-issued
- Herdem, *Offset and Industrial Participation regime in Türkiye* — https://herdem.av.tr/offset-and-industrial-participation-oip-regime-in-turkey
- PRS India, *Management of Defence Offsets (CAG)* — https://prsindia.org/policy/report-summaries/management-of-defence-offsets
- Bharat Shakti, *Pending Rs 42,000 crore defence offsets* — https://bharatshakti.in/pending-rs-42000-crore-defence-offsets-trigger-scrutiny-expert-says-concerns-may-be-overstated/
- Gowling WLG, *UK Defence Investment Plan 2026* — https://gowlingwlg.com/en/insights-resources/articles/2026/uk-defence-investment-plan-2026
- Google Cloud, *UK MoD sovereign cloud contract* — https://www.googlecloudpresscorner.com/2025-09-11-Google-Cloud-Awarded-Landmark-Sovereign-Cloud-Contract-with-UK-Ministry-of-Defence
- Greek City Times, *25% local participation rule* — https://greekcitytimes.com/2026/06/29/greek-defence-industry-30-billion-programme-25-percent-rule/
- FRS, *The Evolution of Brazil's Offset Framework* — https://www.frstrategie.org/web/documents/publications/defense-et-industries/2024/20/DefenseIndustries_N20_art6.pdf

### Items explicitly flagged as unverified
- Netherlands industrial participation obligation percentage — `[UNVERIFIED]`
- Israel SIBAT/IMOD offset percentages and thresholds — `[UNVERIFIED]`
- Stotles and Tussell subscription pricing — `[UNVERIFIED]` (not publicly listed)
- Cloudflare service-level authorisation scope for Workers and individual developer products — `[UNVERIFIED]`; confirm against FedRAMP Marketplace before relying on inheritance
- SBIR Phase II "Strategic Breakthrough" category up to $30M (reported in the April 2026 reauthorisation) — corroborated only by secondary sources in this research
- Poland offset totals (PLN 13bn across 160 of 250 contracts, 2021–22) — secondary source only
- DEFDR's derived ~$16.7bn US-firm unretired offset credit figure — arithmetic derived from BIS tables, not a BIS-published figure
