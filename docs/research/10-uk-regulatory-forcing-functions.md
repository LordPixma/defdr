# UK Regulatory Forcing Functions, September 2026 → 2031

**Agent:** UK Regulatory Forcing-Function Analyst
**Date:** 19 September 2026
**Owns:** LAW 1 (the Standing Test) on behalf of the whole team
**Governing method:** `docs/method/01-opportunity-scoring-rubric.md`

---

## How to read this document

Every instrument below carries a LAW 1 grade. The grades are applied strictly and several
well-known "forcing functions" are demoted here. That is the point of the exercise.

| Grade | Meaning | Weight |
|---|---|---|
| **BINDING** | In force, dated, enforceable, and someone is already non-compliant | Full |
| **SCHEDULED** | Enacted (primary or secondary), with a commencement date in the future | High |
| **PROPOSED** | Consultation, draft, government response without a made SI, or announced intent | **None on its own** |
| **ASPIRATIONAL** | Strategy, target, ambition | **Zero. Do not build on it.** |

Source verification tags: `[FETCHED]` = URL retrieved and content read during this sweep.
`[SEARCH]` = corroborated across search results but the primary URL was not retrieved.
`[UNVERIFIED]` = could not be confirmed; carries no decision weight.

A second, equally important test runs through this document, from LAW 2 and the defence
post-mortem:

> **A one-off registration is not a SaaS. An annual or quarterly evidenced return, with penalties,
> is.** The defence run nearly died on a "£650 one-off form" mistaken for a market.

Every entry is therefore graded **ONE-OFF** or **ONGOING**, and the ONE-OFF ones are explicitly
disqualified as SaaS foundations regardless of how impressive the penalty looks.

---

## Executive summary — the top 12 obligations that create genuine forced software buying

Ranked by: binding-ness × obligated population × ongoing evidenced duty × penalty severity ×
personal liability × weakness of incumbency.

### 1. Martyn's Law — Terrorism (Protection of Premises) Act 2025 — Spring 2027

**SCHEDULED.** Royal Assent 3 April 2025; commencement expected spring 2027 after a stated
implementation period of at least 24 months. Regulator: the Security Industry Authority. Section 27
statutory guidance published 15 April 2026; SIA portal enters volunteer testing "from early 2027".

- **Obligated population: 178,900 premises** (Home Office impact assessment) — the largest
  *documented-evidence* obligation in this entire sweep outside of general employment law.
- **Standard tier (200–799 capacity):** notify the SIA; put in place public protection procedures
  (evacuation, invacuation, lockdown, communication).
- **Enhanced tier (800+):** all of the above, plus public protection *measures* (monitoring,
  movement control, physical security, information security), **plus a documented compliance
  assessment submitted to the SIA**.
- **Penalties:** enhanced tier up to **£18m or 5% of qualifying worldwide revenue**, whichever is
  greater; standard tier max £10,000. Daily penalties of £500 (standard) / £50,000 (enhanced).
  **Criminal offences** for failing to comply with an information, compliance or restriction notice,
  providing false information, or obstructing the SIA — imprisonment and/or a fine.
- **Personal liability: YES.** The responsible person is "the individual, organisation or company
  with control of the premises", and enhanced-tier organisations must **assign a named senior
  individual** for compliance.
- **ONGOING.** Procedures must be maintained, staff trained, capacity re-assessed, notification
  kept current, and (enhanced tier) a document re-submitted. This is not a form.
- **Incumbency: THIN and currently polluted.** The market today is AV integrators and security
  consultants (Strive AV, Masscoms, TIAA, Policy Pros). The SIA has publicly warned that vendors
  claiming "Martyn's Law certified" products are misleading buyers — no product is endorsed. A
  category with 178,900 forced buyers, a named liable human, an £18m ceiling, a regulator building
  its own notification portal, and no credible incumbent is the single strongest finding in this
  sweep.
- **Risk to flag:** commencement has already slipped once from the original "at least 24 months"
  framing. The SIA portal is not live. Treat spring 2027 as the earliest, not the certainty.
- Sources: `[FETCHED]` gov.uk/guidance/understanding-martyns-law-and-the-sias-role-as-regulator;
  `[FETCHED]` protectuk.police.uk/martyns-law/martyns-law-overview-and-what-you-need-know;
  `[FETCHED]` gov.uk/government/collections/terrorism-protection-of-premises-act-2025;
  `[SEARCH]` Home Office impact assessment (178,900 premises); `[SEARCH]` Ashfords / Greenberg
  Traurig on penalty levels.

### 2. Right-to-work check expansion to gig economy and worker contracts — 1 October 2026

**SCHEDULED, 12 days from today.** Border Security, Asylum and Immigration Act 2025 (Royal Assent
2 December 2025), section 48, extends the illegal-working civil penalty regime beyond employees to
**workers' contracts and online matching services**.

- **Obligated population:** every UK organisation engaging labour outside a standard employment
  contract. There are **1,417,730 UK private-sector employers**, and the extension specifically
  captures platforms, couriers, construction labour-only subcontracting, care agencies, hospitality
  and the online marketplaces that match service providers to customers.
- **Penalty: £45,000 per worker first breach, £60,000 per worker repeat breach.** Plus sponsor
  licence revocation for licensed employers, which is existential for care and hospitality.
- **ONGOING.** A right-to-work check is required per engagement, with statutory-excuse evidence
  retained for the duration plus two years, and follow-up checks for time-limited permission. A
  platform onboarding 5,000 couriers a quarter has a continuous evidenced workflow, not a form.
- **Personal liability:** civil penalty falls on the organisation; the separate criminal offence of
  employing someone knowing/having reasonable cause to believe they lack permission carries up to
  5 years and can be charged against directors and managers.
- **Incumbency: REAL but not saturated for this use case.** Yoti, TrustID, Amiqus, Credas and
  Sterling all sell IDVT right-to-work checks to *employers*. The gig/marketplace extension is a
  different integration shape (API into an onboarding funnel, re-check scheduling, multi-party
  evidence) and the incumbents are priced and packaged for HR.
- Sources: `[SEARCH]` Howes Percival, Brodies, Lexology on BSAIA 2025 s.48 and the 1 October 2026
  date; `[FETCHED]` DBT Business Population Estimates 2025 for the employer count.

### 3. UK Carbon Border Adjustment Mechanism — 1 January 2027

**SCHEDULED, legislated.** Liability begins 1 January 2027 on imports of aluminium, cement,
fertiliser, hydrogen, iron and steel. HMRC published further legislation and guidance in August
2026.

- **Registration threshold: £50,000** of CBAM goods over a rolling 12-month period, tested both
  backwards (first day of each month, preceding 12 months) and forwards (next 30 days).
- **First accounting period is the whole of 2027, with the return due 31 May 2028. From 1 January
  2028 reporting moves to quarterly.**
- **ONGOING — and unusually data-hungry.** The liable importer must obtain **installation-level
  embedded-emissions data from non-UK suppliers**, per consignment, per commodity code, or accept
  marked-up default values. This is exactly the shape that defeats a spreadsheet: many suppliers,
  recurring cadence, evidential burden, and a direct cash consequence for poor data.
- **Penalty:** HMRC tax-regime penalties for late registration, late return and inaccuracy, plus the
  economic penalty of paying default values instead of actual supplier emissions.
- **Personal liability:** no bespoke director offence, but this is a tax liability with the usual
  HMRC deliberate-behaviour and personal-liability-notice machinery behind it.
- **Incumbency: EU-shaped, not UK-shaped.** SAP (CBAM Declarants Solution, launched June 2026),
  Sphera, CarbonChain, SINAI, Coolset. All built for EU CBAM. UK CBAM has a different threshold, a
  different return, a different scope list and no certificate market. That gap is real but narrows
  every quarter as the EU vendors add a UK module — durability risk.
- Sources: `[FETCHED]` gov.uk/guidance/work-out-the-date-youll-need-to-register-for-carbon-border-
  adjustment-mechanism-cbam; `[SEARCH]` Baker McKenzie Global Import Blog (Aug 2026 HMRC
  legislation), KPMG UK, Jones Day, Saffery on accounting periods.

### 4. Building Safety Act 2022 — golden thread, safety case, Gateways 2 and 3

**BINDING, and the sector is demonstrably already in breach.** Golden-thread duties have been a
legal requirement since April 2024. Gateway 2 has produced a documented failure: **66% of
applications submitted in 2026 were refused**, and the Building Safety Regulator's own target is
only to reach an 18-week response for non-complex Gateway 2 applications by March 2027.

- **Obligated population: ~12,500 higher-risk buildings in England**, each with a Principal
  Accountable Person, plus every designer, principal contractor and client touching them.
- **Personal liability: YES, and criminal.** Sections 87 and 88 create offences for an Accountable
  Person who without reasonable excuse fails to give prescribed information to the Regulator;
  Building Safety Act offences carry up to **2 years' imprisonment** and a fine.
- **ONGOING.** The golden thread is a maintained record, not a submission. Safety case reports are
  updated and produced on demand. Gateway 3 becomes the 2026–27 pressure point.
- **Incumbency: CONSOLIDATED — read this as a warning.** Zutec (AIM-listed) **acquired Operance in
  February 2025**, combining the two most visible golden-thread platforms. Bimsense/Operance raised
  £575k for exactly this. A well-funded incumbent owns the category. Under LAW 4 this scores low on
  incumbency even though the forcing function is excellent.
- **Adjacent live date:** the **Building Safety Levy applies from 1 October 2026** — 11 days away —
  at £12.70/m² (County Durham) to £100.35/m² (Kensington and Chelsea) of gross internal area, with
  greenfield rates at twice brownfield. Applications submitted before 1 October 2026 are exempt.
- Sources: `[SEARCH]` RIBA on the BSR 2026 plan; Browne Jacobson, Charles Russell Speechlys on
  Gateway refusal rates; legislation.gov.uk BSA 2022 s.87; Gowling WLG on personal liability;
  Gowling WLG / Taylor Wessing / Great Yarmouth BC on the Levy.

### 5. Procurement Act 2023 — contract performance notices and published KPIs

**BINDING since 24 February 2025 and widely unmet.**

- Every contracting authority entering a public contract worth **£5m or more** must set and publish
  **at least three KPIs**, then **publish a contract performance notice assessing the supplier
  against those KPIs at least once every 12 months and on termination**.
- **ONGOING by statutory design** — an annual, evidenced, published return per contract. This is the
  cleanest "annual evidenced return with a deadline" in the public sector.
- **Obligated population:** UK contracting authorities number in the tens of thousands once schools,
  academy trusts, NHS bodies, housing associations acting as authorities and parish councils are
  included. The winnable subset is those actually running £5m+ contracts — realistically **1,500 to
  3,000 organisations**, concentrated in central government, NHS trusts, large local authorities
  and blue-light.
- **Penalty:** no fine. Enforcement is via ministerial investigation, the debarment list, and
  judicial review by aggrieved suppliers. **This weakens it considerably** — see "the enforcement
  gap" below.
- **Incumbency:** Atamis, Proactis, Jaggaer, In-tend, Delta eSourcing, Tussell (data side). Contract
  management modules exist but performance-notice publication is widely handled manually.
- Sources: `[SEARCH]` BCLP, Bird & Bird, Ward Hadaway, Taylor Wessing on Part 4 and s.71.

### 6. Companies House identity verification — transition ends 17 November 2026

**BINDING, and the single largest measured non-compliance in this sweep.**

- **6 to 7 million individuals** must verify identity. **As of end June 2026 only 55% of directors
  and 50% of LLP members had told Companies House they were verified.** The 12-month transition
  ends **17 November 2026 — 59 days from today** — after which active compliance and enforcement
  begins.
- **Penalty:** committing an offence, a financial penalty, and — operationally decisive — **being
  unable to make any filing for the company or incorporate a new one**.
- **CLASSIFICATION: MIXED, and mostly ONE-OFF.** For an individual director, verification is a
  one-time event. **Do not build a SaaS for "director verification".** The ONGOING obligation sits
  with **Authorised Corporate Service Providers** — accountants, solicitors, formation agents,
  chartered secretaries — who must verify, keep records, and re-attest at each confirmation
  statement across a book of hundreds or thousands of clients. That is a real recurring workflow;
  the consumer-facing verification is not.
- **Correction to a widely repeated claim:** software-only accounts filing at Companies House has
  been **delayed from 1 April 2027 to 1 April 2028**. Any candidate that assumed April 2027 is
  wrong by a year.
- Sources: `[FETCHED]` changestoukcompanylaw.campaign.gov.uk/identity-verification/; `[SEARCH]`
  PKF Francis Clark (55%/50% June 2026 figures); ICAEW (April 2028 accounts delay).

### 7. Extended Producer Responsibility for packaging — annual data, escalating fees

**BINDING.** ~£1.5bn per year of local-authority waste cost transferred onto producers. Obligated:
UK organisations with **£1m+ turnover handling 25+ tonnes of packaging**.

- 2025 base fees: **plastic £423/tonne, glass £192/tonne**. The Producer Responsibility Obligations
  (Packaging and Packaging Waste) (Amendment) Regulations 2025 came into force 1 January 2026
  applying an average **8% increase** across all fees.
- **ONGOING.** Large producers report packaging data twice yearly; fees are invoiced annually by
  PackUK; and **recyclability modulation** progressively requires material-, format- and
  recyclability-level data rather than tonnage totals.
- **Already in breach:** the Environment Agency identified **1,183 businesses in England that failed
  to re-register** in April 2025.
- **Incumbency: HEAVY.** Valpak (largest UK scheme), Ecosurety, Beyondly (formerly Comply Direct),
  Reconomy, Repax, Repackd. Compliance schemes already bundle data collection and submission. Under
  LAW 4 this is a category with a 25-year incumbent structure. Score incumbency low.
- Sources: `[SEARCH]` Commons Library CBP-10352; gov.uk 2025 base fees; gov.uk packaging producer
  responsibility monitoring plan 2025 (1,183 non-re-registrants); Resource Recycling.

### 8. ESOS Phase 4 — 5 December 2027, plus annual progress updates

**BINDING (the phase is running; the notification deadline is dated).** Phase 4 runs 6 December
2023 to 5 December 2027.

- **Obligated population:** UK "large undertakings" — 250+ employees, or turnover >£44m *and*
  balance sheet >£38m — plus all UK members of qualifying corporate groups. Against **8,335 UK
  large businesses (250+) and 38,435 medium (50–249)**, the qualifying population is plausibly
  **9,000–12,000 organisations**, the higher number because the turnover/balance-sheet limb catches
  capital-intensive medium-headcount firms.
- **ONGOING and newly so.** Phase 4 requires an **action plan** plus **annual progress updates**,
  and — the important change — **documented progress against the Phase 3 action plan, with an
  explanation where actions were not completed.** ESOS has converted from a four-yearly audit into
  an annually evidenced commitment register. That is a genuine structural shift from one-off to
  recurring.
- **Incumbency:** energy consultancies (Inspired, TEAM Energy, EQUANS, Adler & Allan) own the audit;
  the *annual progress tracking* between audits is largely unserved.
- Sources: `[SEARCH]` gov.uk ESOS guidance; Burges Salmon; Taylor Wessing; Energy Advice Hub.

### 9. Employment Rights Act 2025 — the 2027 cluster

**BINDING for what has commenced; SCHEDULED for the rest.** Royal Assent 18 December 2025.
Commencement is being delivered through numbered regulations; Commencement No. 4 (SI 2026/559) was
verified directly for this sweep.

Confirmed dates (from the government's own timeline, fetched):

| Date | Measure |
|---|---|
| 6 Apr 2026 | SSP lower earnings limit and waiting days removed; day-1 paternity and unpaid parental leave; bereaved partners' paternity leave; collective redundancy protective award doubled; **equality action plans (voluntary)** |
| 7 Apr 2026 | **Fair Work Agency established** |
| 1 Oct 2026 | Employment tribunal claim time limit **3 → 6 months** (Scotland 9 Nov 2026) |
| 30 Oct 2026 | Sexual harassment: **"all reasonable steps"** duty; **third-party harassment** prevention duty; trade union access and notification rights |
| End 2026 | Tipping law strengthened |
| **1 Jan 2027** | **Unfair dismissal qualifying period 6 months; compensatory award cap abolished; fire-and-rehire protections** (SI 2026/559 reg 3 verified) |
| 2027 TBD | **Equality action plans become MANDATORY**; guaranteed-hours offers; bereavement leave incl. pregnancy loss; flexible working; umbrella company regulation; NDA regulations; collective redundancy threshold changes |

- **Section 33 (equality action plans)** came into force 6 April 2026 as an enabling power.
  Employers with **250+ employees** (excluding most public authorities) must publish a plan showing
  steps on the gender pay gap and on supporting employees through menopause, at intervals of not
  less than 12 months. Enforcement is to be prescribed by regulations "otherwise than as an
  offence". **Verified directly against the Act.**
- **Section 35 (records relating to annual leave)** is the sleeper. Employers must keep records
  adequate to show compliance with WTR regs 13, 13A, 15B, 16, 14 and 15E, **retained for six
  years**, in any reasonable format, with **failure constituting an offence under regulation 29(1)
  of the Working Time Regulations 1998**. It applies to England, Wales and Scotland with **no
  small-employer exemption** — i.e. **all 1,417,730 UK employers**. It is **not yet commenced**:
  Commencement No. 4 brings in only s.25(5) and Sch 3 para 5 (1 July 2026) and s.25 with Sch 3
  (1 January 2027). **Grade: SCHEDULED, date not yet appointed.** This is the largest obligated
  population of any single provision in this sweep and deserves a standing watch.
- **Uncapped unfair dismissal compensation from 1 January 2027** is the sharpest commercial edge:
  the current cap (lower of 52 weeks' pay or £118,223) disappears, which materially raises the
  value of documented process.
- Sources: `[FETCHED]` gov.uk Plan to Make Work Pay timeline update; `[FETCHED]`
  legislation.gov.uk ERA 2025 contents, s.33, s.35; `[FETCHED]` SI 2026/559 regs 2 and 3.

### 10. Renters' Rights Act 2025 — 1 May 2026 live; PRS Database opens 15 December 2026

**BINDING (phase 1) / SCHEDULED (database).**

- **1 May 2026:** assured shorthold tenancies abolished; all existing ASTs converted to open-ended
  periodic assured tenancies; **section 21 no-fault notices can no longer be served.**
- **15 December 2026:** registrations open for the **Private Rented Sector Database** — landlords
  must register themselves, their properties **and compliance information** — rolling out by region,
  starting West Midlands.
- **2028:** mandatory sign-up to the Private Landlord Ombudsman.
- **Obligated population:** roughly **2.3 million** private landlords in England (HMRC/English
  Housing Survey order of magnitude) `[UNVERIFIED — not confirmed in this sweep]`, and around
  **20,000** letting and managing agents.
- **Classification: MIXED.** Registration itself is a ONE-OFF per property. The **compliance
  information** attached to the registration (gas safety, EICR, EPC, deposit protection, licensing)
  has expiry dates and must be kept current — that part is ONGOING. Be precise about which one you
  are selling.
- **Incumbency: HEAVY.** Reapit, Alto/Zoopla, Goodlord, Fixflo, PropertyFile, Arthur, Landlord
  Vision. The letting-agent software market is mature and the database will be a field in their
  products within one release cycle.
- Sources: `[SEARCH]` NRLA, Gowling WLG, Mayer Brown, The Independent Landlord.

### 11. Deposit Return Scheme — 1 October 2027

**SCHEDULED.** England, Scotland and Northern Ireland launch together on **1 October 2027**.
Deposit management organisation (Exchange for Change) appointed April 2025.

- Producers, manufacturers, importers and return-point operators must **register with the DMO before
  1 October 2027**, and producers **may not supply in-scope drinks unless registered**.
- **ONGOING.** Producer fees are levied **per container placed on the market**, so producers must
  keep and submit container-level volume records continuously. Return-point operators reconcile
  container flows. 20p deposit on PET, aluminium and steel containers 150ml–3L.
- **Obligated population:** UK drinks producers and importers — low thousands — plus roughly
  **30,000–40,000** obligated return points `[UNVERIFIED]`.
- **Incumbency:** Scotland's aborted 2023 scheme already produced vendors (Zappy, Re-turn, TOMRA on
  the RVM side). Watch for the DMO providing free tooling, which would erase the category.
- Sources: `[SEARCH]` Commons Library CBP-10453; Defra environment blog; Brodies; Brabners.

### 12. Leasehold service charge transparency — statutory instruments laid late 2026, effect 2027

**SCHEDULED (government implementation statement 15 July 2026; SIs not yet made — treat the detail
as PROPOSED until laid).**

- Landlords/managing agents will have to issue service charge demands in a **prescribed form**,
  produce **standardised annual accounts**, and produce a **prescribed-form annual report**.
- **Notice periods:** 12 months for private landlords, **24 months for social landlords** on the
  annual report, demand forms and standardised accounts; 12 months for administration charge
  schedules and insurance transparency.
- **ONGOING and highly structured** — a prescribed annual report in a prescribed form across a
  portfolio is close to an ideal SaaS shape.
- **Obligated population:** roughly **4.9 million leasehold dwellings in England** managed by an
  estimated **15,000–20,000** managing agents and freeholders `[UNVERIFIED]`.
- **Risk:** the prescribed forms do not exist yet. Building before the SIs are laid violates LAW 1.
- Sources: `[SEARCH]` Commons Library CBP-10918; Clarke Willmott; Lease Advice; NRLA.

---

## Full sweep — every obligation found, graded

### Employment and HR

| Instrument | Grade | Key dates | Obligated population | Duty | Penalty | Software? |
|---|---|---|---|---|---|---|
| Employment Rights Act 2025 (c.36) — commenced provisions | **BINDING** | 18 Feb, 6 Apr, 7 Apr, 25 Aug 2026 | 1,417,730 employers | Policy, process, SSP, leave | Tribunal awards | ONGOING (HR/payroll — saturated) |
| ERA 2025 — tribunal time limit 3→6 months | **BINDING** | 1 Oct 2026 (E&W), 9 Nov 2026 (Scot) | All employers | Longer exposure window | n/a | ONGOING (records retention) |
| ERA 2025 — sexual harassment "all reasonable steps" + third-party harassment | **SCHEDULED** | 30 Oct 2026 | All employers | Risk assessment, training, evidence | Uplift to tribunal award | **ONGOING — good shape** |
| ERA 2025 s.25 — unfair dismissal 6-month qualifying period; **compensatory cap abolished** | **SCHEDULED** (SI 2026/559 reg 3 verified) | 1 Jan 2027 | All employers | Documented process from month 6 | Uncapped award | ONGOING |
| ERA 2025 s.33 — equality action plans | **BINDING (power) / SCHEDULED (duty)** | Power 6 Apr 2026; voluntary Apr 2026; **mandatory spring 2027** | ~11,000 employers (250+) | Publish annual plan: gender pay gap + menopause | Prescribed, "otherwise than as an offence" | ONGOING |
| ERA 2025 s.35 — **annual leave records, 6-year retention** | **SCHEDULED (not yet commenced)** | TBC | **All 1,417,730 employers** | Keep records proving WTR compliance | **Criminal offence, WTR 1998 reg 29(1)** | **ONGOING — largest population found** |
| ERA 2025 — guaranteed hours for zero/low-hours workers | **SCHEDULED** | 2027 (reference period consulted at 12 weeks) | Employers of ~1m zero-hours workers | Offer contract reflecting reference-period hours; reasonable shift notice; cancellation pay | Tribunal claims | ONGOING |
| ERA 2025 — fire and rehire restrictions | **SCHEDULED** | 1 Jan 2027 | All employers | Process constraints | Tribunal | Weak software shape |
| ERA 2025 — Fair Work Agency | **BINDING** | 7 Apr 2026 | All employers | Subject to enforcement notices | Civil penalties, labour market enforcement undertakings | Indirect |
| Border Security, Asylum and Immigration Act 2025 s.48 — right to work checks extended to workers, gig, online matching | **SCHEDULED** | **1 Oct 2026** | All labour-engaging orgs + platforms | Per-engagement check + statutory excuse evidence | **£45k / £60k per worker**; criminal offence 5 yrs | **ONGOING — top 3** |
| Gender pay gap reporting (Equality Act 2010 (Gender Pay Gap Information) Regs 2017) | **BINDING** | 30 Mar 2026 (public), 4 Apr 2026 (private), annually | ~11,000–11,250 | Publish 6 metrics | **Zero fines ever issued** | ONGOING but see enforcement gap |
| Ethnicity and disability pay gap reporting | **PROPOSED** | Equality (Race and Disability) Bill; regs to follow | ~11,000 (250+) | Mirror GPG + workforce composition + declaration rates | TBD | ONGOING once real — **do not build yet** |
| Off-payroll / IR35 | **BINDING** | Ongoing since Apr 2021 | Medium/large end clients (~46,770) | SDS per engagement, status determination, appeals | PAYE liability transfer | ONGOING — incumbents own it |
| TUPE | **BINDING** | Ongoing | All employers | ELI, consultation | Up to 13 weeks' pay | Episodic, not SaaS |

### Environment and net zero

| Instrument | Grade | Key dates | Obligated population | Duty | Penalty | Software? |
|---|---|---|---|---|---|---|
| **UK CBAM** | **SCHEDULED** | Liability 1 Jan 2027; first return **31 May 2028**; quarterly from 2028 | Importers >£50k/12mo of Al, cement, fertiliser, H2, iron, steel | Register; collect supplier embedded emissions; file return | HMRC penalty regime | **ONGOING — top 3** |
| Packaging EPR | **BINDING** | Fees live; +8% from 1 Jan 2026; recyclability modulation phasing | £1m turnover + 25t packaging | Twice-yearly data; annual fee | EA compliance notices; 1,183 caught 2025 | ONGOING — heavy incumbency |
| Simpler Recycling (workplaces) | **BINDING** | 31 Mar 2025 (10+ FTE); **31 Mar 2027 (micro-firms <10 FTE)** | Effectively all workplaces | Separate dry recyclables / food / residual | Offence to breach a compliance notice | **ONE-OFF operational change. No record-keeping or reporting duty. NOT A SaaS.** (verified against gov.uk guidance) |
| Deposit Return Scheme | **SCHEDULED** | **1 Oct 2027** | Drinks producers, importers, return points | Register with DMO; per-container fees and records | Cannot supply unregistered | ONGOING |
| ESOS Phase 4 | **BINDING** | Phase ends **5 Dec 2027**; annual progress updates | ~9,000–12,000 large undertakings | Audit 95% of energy; action plan; **annual progress update; explain Phase 3 non-delivery** | EA civil penalties | **ONGOING — newly so** |
| SECR | **BINDING** | Annual, with accounts | Quoted cos + large unquoted (~11,900) `[UNVERIFIED]` | Energy + emissions in directors' report | Accounts filing consequences | ONGOING — absorbed by carbon accounting incumbents |
| **UK SRS S1 / S2** | **PROPOSED** | Standards final 25 Feb 2026 (**voluntary**); FCA CP26/5 closed 20 Mar 2026; **Policy Statement expected autumn 2026**; proposed effect 1 Jan 2027 | ~1,900 listed issuers if adopted | Climate disclosure (S2) mandatory; S1 and Scope 3 comply-or-explain | FCA listing rules | **DO NOT BUILD YET — LAW 1 fails until the Policy Statement lands** |
| Biodiversity Net Gain | **BINDING, but SHRINKING** | Mandatory since Feb 2024; **0.2ha exemption in force 31 Jul / 6 Aug 2026**; self-build exemption removed | Developers on non-exempt sites | 10% gain; 30-year securing, management and monitoring | Planning refusal | ONGOING for non-exempt — **but the de minimis went from 25m² to 2,000m², an 80-fold market contraction. Disconfirming.** |
| Non-domestic MEES | **PROPOSED** | **EPC C 2027 milestone DROPPED** (interim response 18 Jun 2026); EPC B **2031**, only buildings >1,000m², only where cost-effective, SI not made | Commercial landlords | Reach EPC B | TBD | **The widely-cited "EPC C by 2027" forcing function no longer exists. Kill any candidate resting on it.** |
| Domestic MEES (PRS) | **PROPOSED** | Gov response 21 Jan 2026: EPC C by **1 Oct 2030**, £10,000 cap, HEM-based; HEM EPCs delayed to H2 2027, compulsory 1 Oct 2029 | ~2.3m PRS landlords | Reach EPC C | Civil penalty | ONGOING once regs are made — not yet |
| Future Homes Standard (Part L 2026) | **SCHEDULED** | AD published 24 Mar 2026; **in force 24 Mar 2027** (HRBs 24 Sep 2027); transitional to 24 Mar 2028 | Housebuilders | 75%+ emissions reduction vs 2013 | Building control refusal | ONGOING (compliance modelling) — incumbents own it |
| Clean Heat Market Mechanism | **BINDING** | Live 1 Apr 2025; 6% 2025/26, **8% 2026/27** | **~10–20 boiler manufacturers** | Heat pump share of sales or buy credits | £500 per boiler over target | **REJECT on LAW 2 — buyer count is a rounding error** |
| EUDR (EU, affects UK exporters) | **SCHEDULED** | **30 Dec 2026** large/medium; 30 Jun 2027 small/micro | UK exporters of cattle, cocoa, coffee, palm, rubber, soy, wood to EU | Geolocated due diligence statements | EU turnover-based fines | ONGOING — crowded EU vendor field |
| ULEZ / Clean Air Zones | **BINDING** | Live | Fleet operators | Vehicle compliance | Daily charges | Solved by telematics |

### Financial services

| Instrument | Grade | Key dates | Obligated population | Duty | Penalty | Software? |
|---|---|---|---|---|---|---|
| FCA Consumer Duty | **BINDING** | Live since 31 Jul 2023; **annual board report**, third cycle in 2026 | ~42,000–50,000 FCA-regulated firms (Duty scope narrower) | Annual board-approved report evidencing outcomes for retail customers; outcome monitoring | Supervisory action, s.166, enforcement | **ONGOING and evidence-heavy** — but a dense RegTech field |
| Operational resilience (PS21/3) | **BINDING** | **31 Mar 2025 deadline passed** | Banks, insurers, e-money, payments, FMIs | Remain within impact tolerances; mapping; scenario testing | Enforcement | ONGOING; FCA published "one year on" findings Mar/Apr 2026 |
| Critical Third Parties (PS24/16) | **BINDING** | Rules effective **1 Jan 2025** | Designated CTPs only (a handful) | Resilience testing, incident reporting | Statutory | **REJECT on LAW 2 — designated population is tiny** |
| Basel 3.1 / SDDT | **SCHEDULED** | **1 Jan 2027**; market risk 1 Jan 2028; full 1 Jan 2030; SDDT consent closed 31 Mar 2026 | UK banks and building societies (~340) | Capital calculation change | PRA | ONGOING — Regnology, Moody's, Wolters Kluwer own it |
| APP fraud mandatory reimbursement | **BINDING** | **7 Oct 2024** | Faster Payments PSPs | Reimburse up to £85,000; 50/50 split; claim handling within 5 business days | PSR directions | ONGOING — fraud/claims ops |
| Pensions Dashboards | **BINDING/SCHEDULED** | Staged Apr 2025 → Sep 2026; **final connection 31 Oct 2026** | 1,000+ providers and schemes already connected; 60m records | Connect; respond to find requests; match data | TPR enforcement | **Connection is ONE-OFF; matching and find-request handling is ONGOING.** Incumbents (ITM, Origo, Capita, Aquila Heywood) own it |
| Motor finance redress | **SCHEDULED** | FCA scheme | Motor finance lenders (~low hundreds) | Case review, redress calculation | FCA | Episodic remediation, not durable SaaS |

### Data, AI, digital

| Instrument | Grade | Key dates | Obligated population | Duty | Penalty | Software? |
|---|---|---|---|---|---|---|
| Data (Use and Access) Act 2025 | **BINDING** | Part 5 commenced **5 Feb 2026** (SI 2026 Commencement No. 6); complaints duty **19 Jun 2026** | All UK controllers | Complaints procedure; acknowledge within 30 days; ADM under Arts 22A–22D; recognised legitimate interests | ICO fines | ONGOING — privacy-tech incumbents (OneTrust, Securiti) |
| **Cyber Security and Resilience (NIS) Bill** | **PROPOSED** | 2R 6 Jan 2026; Lords Report Sep 2026; **substantive effect ~2028 via secondary legislation after a 2026 implementation consultation** | MSPs, data centres, large load controllers, OES | Registration, incident reporting (24-hour clock proposed) | TBD | **DO NOT BUILD ON THIS YET. It is a Bill, not an Act.** |
| EU AI Act (extraterritorial on UK firms) | **BINDING (GPAI) / SCHEDULED (high-risk, delayed)** | GPAI obligations live 2 Aug 2025; AI Office enforcement powers 2 Aug 2026; **high-risk pushed to Dec 2027 / Aug 2028 by the Digital Omnibus (agreed 2026)** | UK providers placing models/systems on the EU market | Technical documentation, training-data summaries, EU authorised representative (Arts 22, 54), post-market monitoring | Up to 7% global turnover | ONGOING — **but the date you were planning against moved. Re-check before building.** |
| Online Safety Act 2023 | **BINDING** | Illegal harms Mar 2025; children's duties Jul 2025; risk assessments requested by Ofcom May–Jul 2026 | **100,000+ services in scope** | Illegal content and children's risk assessments, record-keeping, produce to Ofcom on request | Up to 10% global turnover; **senior manager criminal liability for information-duty breaches** | **ONGOING. Huge population. Ofcom has 5 enforcement programmes and has investigated 69 platforms.** |
| PSTN / copper switch-off | **Commercial deadline, not statutory** | **31 Jan 2027**, Openreach says no extension | **500,000+ UK business lines still on copper** | Migrate voice, alarms, lifts, EPOS, telecare | Service loss + rising wholesale charges during 2026 | Migration discovery is a project, not a subscription |
| Martyn's Law | **SCHEDULED** | Spring 2027 | 178,900 premises | See top 12 | £18m / 5% revenue | **ONGOING — top pick** |

### Built environment and housing

| Instrument | Grade | Key dates | Obligated population | Duty | Penalty | Software? |
|---|---|---|---|---|---|---|
| Building Safety Act 2022 — golden thread, safety case, Gateways | **BINDING** | Golden thread since Apr 2024; Gateway 3 pressure 2026–27 | ~12,500 HRBs | Maintain golden thread; safety case report; Gateway applications | **Criminal, up to 2 years (ss.87–88)** | ONGOING — **Zutec acquired Operance Feb 2025** |
| **Building Safety Levy** | **SCHEDULED → BINDING in 11 days** | **1 Oct 2026** | Residential and PBSA developers in England | Pay £12.70–£100.35/m² GIA; greenfield 2× | Building control consequences | Calculation/forecasting tool — thin, but very dated |
| Awaab's Law (Social Housing (Regulation) Act 2023) | **BINDING** | **Phase 1 live 27 Oct 2025** (damp, mould, emergency hazards); expansion to further hazards 2026–27 | ~1,600 registered providers of social housing `[UNVERIFIED count]` | Investigate within 14 days; begin repairs within 14 days; evidence it | Tribunal, Ombudsman, RSH regulatory judgement | ONGOING — **but Mobysoft RepairSense, Neo Propsys360, PocketSurvey, Awaab Comply and the HACT data standard already occupy it. LAW 4 disconfirms.** |
| Competence and Conduct Standard | **SCHEDULED** | **October 2026**; transition 3 yrs (1,000+ units) / 4 yrs (<1,000) | Registered providers | Senior housing managers/executives hold or work toward specified qualifications; policy; code of conduct | RSH regulatory judgement | ONGOING (competency register) — plausible gap |
| Decent Homes Standard (new) | **PROPOSED/SCHEDULED** | Direction to RSH; compliance by **2035** | Social landlords | Stock condition | RSH | Too far out; 2035 is not a forcing function today |
| Renters' Rights Act 2025 | **BINDING (phase 1)** | **1 May 2026**; PRS Database opens **15 Dec 2026**; Ombudsman 2028 | ~2.3m landlords, ~20,000 agents | Periodic tenancies; register property + compliance info | Civil penalties, rent repayment orders | Mixed; heavy incumbency |
| Leasehold and Freehold Reform Act 2024 — service charge transparency | **SCHEDULED** | ≥5 SIs late 2026; effect 2027; 12/24-month notice | ~15,000–20,000 managing agents/freeholders | Prescribed-form demands, standardised accounts, **annual report** | Cost recovery barred | **ONGOING — good shape once SIs are laid** |
| Second staircase requirement | **BINDING** | Transitional period ran to 30 Sep 2026 | HRB developers | Design change | Building control | Not software |

### Health and care

| Instrument | Grade | Key dates | Obligated population | Duty | Penalty | Software? |
|---|---|---|---|---|---|---|
| CQC single assessment framework / sector frameworks | **BINDING (regime) / SCHEDULED (reboot)** | Sector-specific frameworks published summer 2026; rollout late 2026, complete by year end | ~18,000 registered providers / ~33,000 locations `[UNVERIFIED]` | Continuous evidence against quality statements; Provider Information Return | Registration conditions, prosecution | **ONGOING** — Access, Birdie, Log my Care, Nourish, Radar Healthcare compete hard |
| DSPT aligned to NCSC CAF v3.4 | **BINDING** | **Annual, 30 June** (30 Jun 2026 just passed); independent assessment Jan–Jun | NHS trusts, ICBs, CSUs, ALBs, OES, genomics (Category 1); plus every NHS supplier | CAF-outcome self-assessment + independent assessment | Contract loss, NHS supplier disqualification | **ONGOING annual evidenced return** — a real shape; DSPTready, Dionach, Bondgate already circling |
| Medical Devices (Post-market Surveillance) Regs 2024 | **BINDING** | In force **16 Jun 2025** | UK medical device manufacturers and UK Responsible Persons | PMS plan, PMS report, periodic safety update reports, vigilance timelines | MHRA enforcement | ONGOING — eQMS incumbents (Greenlight Guru, Qualio, Scilife) |
| UKCA for medical devices | **SCHEDULED, WEAKENING** | CE acceptance to **30 Jun 2028** (MDD) / **30 Jun 2030** (IVDD); **MHRA consulting Feb 2026 on indefinite CE recognition** | Device manufacturers | Re-certify | Market access | **The deadline may be abolished. Do not build on it.** |
| Patient Safety Incident Response Framework | **BINDING** | Rolled out from 2023 | NHS providers (~215 trusts) | PSIRF plan, response, learning | NHSE oversight | ONGOING — Radar Healthcare, InPhase |

### Food, agriculture, product

| Instrument | Grade | Key dates | Obligated population | Duty | Penalty | Software? |
|---|---|---|---|---|---|---|
| Natasha's Law (PPDS allergen labelling) | **BINDING** | Since 1 Oct 2021 | ~600,000 food businesses `[UNVERIFIED]` | Full ingredient + allergen label on PPDS | Improvement notices, prosecution | ONGOING — Erudus, Nutritics, Kafoodle, Jellybean already there |
| "Not for EU" labelling in GB | **PROPOSED, effectively shelved** | GB-wide rollout **not proceeded with** (Oct 2024); powers retained | GB food businesses | — | — | **Dead as a forcing function. Reserve powers only.** |
| Windsor Framework retail movement scheme labelling (GB→NI) | **BINDING** | Phase 3 from 1 Jul 2025 | GB suppliers into NI | Individual item labelling | Movement refusal | ONGOING but narrow |
| UKCA marking (general goods) | **BINDING, indefinitely weakened** | CE recognition extended indefinitely for most goods (2023) | Manufacturers/importers | Conformity | Market surveillance | **Not a forcing function any more** |
| Product Regulation and Metrology Act 2025 | **PROPOSED** | RA 21 Jul 2025 (enabling only); two consultations closed **23 Jun 2026**; response within 12 weeks; SIs to follow | Manufacturers, importers, **online marketplaces** | TBD — expected to mirror EU GPSR | TBD | **Watch closely. The online-marketplace duty could be a 2027–28 forcing function. Not yet.** |
| Tobacco and Vapes Act 2026 (c.18) | **SCHEDULED** | RA **29 Apr 2026**; licensing expected **Oct 2026 – Jan 2027**; consultation early 2027; **Home Office guidance not published** | Every tobacco/vape retailer, physical and online — tens of thousands | Premises licence + personal licence | Licence refusal; trading ban | ONGOING once live — **but no guidance and no application dates exist yet. PROPOSED in substance.** |

### Tax, finance ops and corporate

| Instrument | Grade | Key dates | Obligated population | Duty | Penalty | Software? |
|---|---|---|---|---|---|---|
| Making Tax Digital for Income Tax | **BINDING** | **6 Apr 2026 (£50k+)**; 6 Apr 2027 (£30k+); 6 Apr 2028 (£20k+) | ~780,000 (2026) rising to ~2.75m by 2028 `[UNVERIFIED]` | Digital records + **quarterly updates** + final declaration | Points-based penalties | ONGOING — **but HMRC-recognised software is already a commodity: FreeAgent, Xero, QuickBooks, Sage, Coconut, 123 Sheets. LAW 4 rejects.** |
| ECCTA — identity verification | **BINDING** | Transition **18 Nov 2025 → 17 Nov 2026** | 6–7m individuals; enforcement from 18 Nov 2026 | Verify via GOV.UK One Login or an ACSP | Offence + financial penalty + **filing block** | **ONE-OFF for individuals; ONGOING for ACSPs** |
| ECCTA — software-only accounts filing | **SCHEDULED, DELAYED** | **1 Apr 2028** (was 1 Apr 2027) | All companies on the register (~5.4m) | File accounts via commercial software; small co. P&L filing | Filing rejection | ONGOING — **correct the date; it is not 2027** |
| **Failure to prevent fraud (ECCTA s.199)** | **BINDING** | **1 Sep 2025** | Large orgs: 2 of (250+ employees, >£36m turnover, >£18m balance sheet) — roughly **9,000–12,000 UK organisations** | Maintain "reasonable procedures": risk assessment, due diligence, training, monitoring, top-level commitment | **Unlimited fine; strict liability** | **ONGOING — the defence is evidential, which is a software shape** |
| Economic Crime Levy | **BINDING** | Annual, 30 Sep | AML-regulated entities >£10.2m UK revenue | Return and pay | HMRC penalties | ONE-OFF annual form — thin |
| E-invoicing (Peppol 4-corner) | **SCHEDULED** | Confirmed 23 Jun 2026; **mandatory for all VAT invoices from April 2029**; roadmap at Budget 2026 | All VAT-registered businesses (~2.7m) `[UNVERIFIED]` | Structured e-invoice exchange | TBD | ONGOING — **enormous, but 2029 and the access-point market is already forming (Tungsten, Basware, Pagero, Storecove)** |

### Procurement and public sector

Covered in the top 12 (#5). Additional: the **two-tier procurement code** was reinstated on
**30 October 2026** under the ERA 2025 timeline, creating a workforce-information obligation on
outsourced public service contracts. **SCHEDULED.**

### Transport

| Instrument | Grade | Key dates | Obligated population | Duty | Penalty | Software? |
|---|---|---|---|---|---|---|
| Smart Tachograph 2 retrofit | **BINDING — deadlines already passed** | Analogue/digital → 31 Dec 2024; ST1 → 19 Aug 2025; **>2.5t vans on international hire-or-reward from 1 Jul 2026** | UK operators running internationally | Retrofit hardware | Fines, O-licence consequences | **Hardware, not software** |
| Driver CPC | **BINDING** | 35 hrs / 5 years, rolling | ~600,000 LGV/PCV drivers `[UNVERIFIED]` | Periodic training record | Driving ban | ONGOING — owned by training providers |
| DVSA Earned Recognition | **Voluntary** | — | ~1,000 operators | KPI data submission | Scheme exit | **Voluntary = not a forcing function** |

---

## "Already in breach" — obligations UK firms are failing today

These are the strongest of all under LAW 1. A dated obligation plus a measured non-compliance rate
is the closest thing to a guaranteed buyer.

1. **Companies House identity verification.** At end June 2026, **45% of directors and 50% of LLP
   members had not verified**. 6–7 million individuals in scope. The transition ends **17 November
   2026 — 59 days away** — and Companies House has said enforcement begins immediately after.
   `[FETCHED]` + `[SEARCH]`
2. **Gender pay gap reporting.** Of ~11,250 employers in scope, only **1,460 had reported by 30
   January 2026** against the 4 April 2026 deadline. But read the next section before getting
   excited. `[SEARCH]` / `[FETCHED]` Lewis Silkin
3. **Building Safety Act Gateway 2.** **66% of applications submitted in 2026 were refused.**
   Several hundred HRB projects stalled at a time during 2025. Remediation cases still outstrip
   decisions. This is systemic, documented non-compliance in a criminal-liability regime. `[SEARCH]`
4. **Packaging EPR registration.** The Environment Agency identified **1,183 English businesses that
   failed to re-register** in April 2025; 14 of 344 direct registrants missed recycling obligations
   in 2025. `[SEARCH]`
5. **PSTN migration.** **More than half a million UK business lines remain on copper** with
   Openreach's 31 January 2027 shutdown fixed and wholesale prices deliberately rising through 2026
   to force migration. `[SEARCH]`
6. **Online Safety Act.** Ofcom has run **five enforcement programmes and investigated 69 platforms**
   since March 2025 across a population of 100,000+ in-scope services. `[SEARCH]`
7. **Operational resilience.** The 31 March 2025 impact-tolerance deadline has passed and the FCA
   published "insights and observations" in March/April 2026 identifying gaps — the regulator's
   polite way of saying firms are not there. `[SEARCH]`

---

## Personal and criminal liability — where a named human is on the hook

Per the brief: these buy software fastest. Ranked by how specifically a named individual is exposed.

| Obligation | Who is personally exposed | Exposure |
|---|---|---|
| **Building Safety Act 2022 ss.87–88** | **Accountable Person / Principal Accountable Person** — a named duty-holder on a register | Criminal offence; **up to 2 years' imprisonment** and a fine |
| **Martyn's Law** | **Responsible person**; enhanced-tier orgs must **designate a named senior individual** | Criminal offence for breach of an information/compliance/restriction notice, false information, or obstruction — **imprisonment and/or fine**; org penalty to **£18m or 5% of qualifying worldwide revenue** |
| **Online Safety Act 2023** | **Named senior manager** | Criminal liability for failure to comply with information notices |
| **Failure to prevent fraud (ECCTA s.199)** | The organisation (strict liability), but the **board** carries the "top-level commitment" element of the reasonable-procedures defence | Unlimited fine; reputational and DPA consequences |
| **Illegal working (BSAIA 2025 s.48 + Immigration Act 2016 s.35)** | Directors and managers can be charged with the criminal offence of employing a disqualified person | **Up to 5 years' imprisonment**; civil penalty £45k/£60k per worker |
| **ERA 2025 s.35 annual leave records** | Employer; **offence under WTR 1998 reg 29(1)**, which extends to officers where committed with consent, connivance or neglect | Criminal offence, level 5 fine |
| **Companies House identity verification** | **The individual director or PSC personally** commits an offence | Financial penalty; personal inability to file or incorporate |
| **SM&CR** | **Senior Managers** with statements of responsibility | Prohibition, fine, personal enforcement |
| **Health and Safety at Work Act s.37** | Directors, managers, secretaries | Unlimited fine, imprisonment |

**The best combination in this sweep is Martyn's Law**: a named senior individual, a criminal
offence, a revenue-percentage penalty ceiling, 178,900 obligated premises, and no credible
incumbent. The Building Safety Act is comparable on liability but has a consolidated incumbent.

---

## Obligated-population counts

Method: start from DBT/BEIS **Business Population Estimates 2025** (verified by direct fetch), then
narrow by the statutory test in each instrument. Where a regulator publishes its own register
count, that is preferred.

### Baseline (verified, start of 2025)

| Cohort | Count | Source |
|---|---|---|
| UK private sector businesses (total) | **5,690,265** | `[FETCHED]` BPE 2025 |
| Businesses **with employees** (employers) | **1,417,730** | `[FETCHED]` BPE 2025 |
| Small (0–49 employees) | 5,643,495 | `[FETCHED]` BPE 2025 |
| Medium (50–249 employees) | **38,435** | `[FETCHED]` BPE 2025 |
| Large (250+ employees) | **8,335** | `[FETCHED]` BPE 2025 |

### Derived obligated populations

| Obligation | Population | Confidence | Derivation |
|---|---|---|---|
| ERA 2025 s.35 annual leave records | **1,417,730** | High | All employers, no exemption, verified against the section text |
| Right to work checks (expanded) | ~1,400,000 + platforms | High | All labour-engaging organisations |
| Sexual harassment "all reasonable steps" | 1,417,730 | High | All employers |
| Simpler Recycling micro-firm tranche (2027) | ~1.3m workplaces | Medium | Employers with <10 FTE |
| Online Safety Act | **100,000+ services** | Medium | Ofcom's own figure |
| Martyn's Law | **178,900 premises** | High | Home Office impact assessment |
| MTD ITSA (Apr 2026 tranche) | ~780,000 | Low `[UNVERIFIED]` | HMRC estimate for the £50k band |
| Gender pay gap / equality action plans | **~11,000–11,250** | High | EHRC and Lewis Silkin, cross-checked against 8,335 large private + public sector |
| Ethnicity & disability pay gap (when live) | ~11,000 | High | Same 250+ threshold |
| Failure to prevent fraud | **~9,000–12,000** | Medium | 250+ employees (8,335) plus turnover/balance-sheet limb catching medium-headcount firms |
| ESOS Phase 4 | **~9,000–12,000** | Medium | Large-undertaking test, same logic |
| CBAM registrants | **~3,000–8,000** | Low `[UNVERIFIED]` | Importers of 6 commodity groups above £50k/yr; HMRC has not published a figure this sweep could retrieve |
| Packaging EPR producers | **~9,000–12,000** | Low `[UNVERIFIED]` | £1m turnover + 25t threshold; the Commons Library briefing (CBP-10352) holds the number but returned HTTP 403 |
| FCA-regulated firms | **~42,000–50,000** | Medium | FCA's own published range |
| Higher-risk buildings | **~12,500** | High | BSR register |
| Registered providers of social housing | **~1,600** | Low `[UNVERIFIED]` | RSH publishes a monthly list; the August 2026 accessible version returned 404 |
| Contracting authorities running £5m+ contracts | **1,500–3,000** | Low `[UNVERIFIED]` | Inferred from Contracts Finder/Tussell volume |
| Boiler manufacturers (CHMM) | **~10–20** | High | **Fails LAW 2 outright** |
| Designated Critical Third Parties | **<20** | High | **Fails LAW 2 outright** |

---

## ONE-OFF vs ONGOING — the ruthless cut

This is the section the defence post-mortem demands. A candidate resting on anything in the
left-hand column is rejected on sight.

### ONE-OFF (a form, a registration, a project) — **NOT a SaaS**

| Obligation | Why it fails |
|---|---|
| **Companies House identity verification (individual)** | A director verifies once. There is no recurring event. The recurring layer exists only for ACSPs managing a client book. |
| **Simpler Recycling** | Verified against gov.uk guidance: the duty is to separate waste streams. **There is no record-keeping and no reporting duty.** It is a bin contract, not software. |
| **Pensions Dashboards connection** | Connection is a one-time integration. The ongoing part (find requests, data matching) is already owned by ITM, Origo, Capita and Aquila Heywood. |
| **Smart Tachograph 2 retrofit** | Hardware fitted once. |
| **Second staircase requirement** | A design rule. |
| **UKCA / CE re-marking** | A certification event, and MHRA is consulting on making CE recognition indefinite. |
| **Economic Crime Levy return** | One annual form with no evidential apparatus. |
| **PSTN migration** | A discovery-and-migrate project. Revenue ends when the copper does, on 31 January 2027. |
| **Renters' Rights PRS Database registration** | Registration is per property, once. Only the *compliance-information currency* is recurring. |
| **SDDT consent election** | Closed 31 March 2026. |

### ONGOING (recurring, evidenced, penalised) — **a SaaS can live here**

| Obligation | Cadence | Evidence produced |
|---|---|---|
| **Martyn's Law** | Continuous + re-notification; enhanced tier document submission | Procedures, training records, capacity assessments, measures register |
| **Right to work checks (expanded)** | Per engagement + follow-up checks | Statutory-excuse evidence pack per worker, retained engagement + 2 years |
| **UK CBAM** | Annual 2027, **quarterly from 2028** | Per-consignment embedded emissions, supplier attestations, return |
| **Building Safety golden thread / safety case** | Continuous | Versioned building information, safety case report |
| **Procurement Act contract performance notices** | **Annual per contract + on termination** | Published KPI assessment |
| **ESOS Phase 4** | 4-yearly audit + **annual progress update** | Action plan delivery evidence, explanations for non-delivery |
| **Packaging EPR** | Twice-yearly data + annual fee | Material/format/recyclability tonnage |
| **FCA Consumer Duty** | **Annual board report** + continuous outcome monitoring | Outcome MI, board minutes, product reviews |
| **DSPT / NCSC CAF** | **Annual, 30 June** + independent assessment | CAF outcome evidence |
| **Equality action plans (from 2027)** | Annual | Published plan, gender pay gap actions, menopause actions |
| **ERA 2025 s.35 annual leave records** | Continuous, **6-year retention** | WTR compliance records for every worker |
| **Failure to prevent fraud** | Continuous | Risk assessment, due diligence, training, monitoring |
| **Online Safety Act** | Continuous + on Ofcom request | Illegal content and children's risk assessments, record-keeping |
| **CQC assessment** | Continuous | Evidence against quality statements, PIR |
| **Medical device PMS** | PMS report + PSURs | Vigilance and surveillance data |
| **Leasehold annual report (2027)** | Annual, prescribed form | Standardised service charge accounts |
| **Deposit Return Scheme** | Continuous container accounting | Volumes placed on market |
| **MTD ITSA** | **Quarterly** | Digital records, quarterly updates |

---

## Disconfirming evidence — report it prominently (Hard Rule 3)

These are the findings that should stop other agents wasting a week.

1. **The "EPC C by 2027" commercial MEES deadline no longer exists.** The government's interim
   response of 18 June 2026 **dropped the 2027 interim milestone entirely**. What remains is EPC B
   by **2031**, only for privately-let buildings **over 1,000m²**, only **where cost-effective**,
   and **still subject to secondary legislation that has not been made.** Grade: **PROPOSED**. Any
   candidate built on commercial MEES is dead.

2. **Gender pay gap enforcement is theatre.** Across the 2023, 2024 and 2025 reporting deadlines the
   EHRC issued **1,886 warning notices (652 / 609 / 625)** and imposed **zero fines, opened zero
   investigations, and obtained zero court orders.** Lewis Silkin further notes a credible argument
   that the EHRC is operating beyond its strict statutory remit, because the obligation sits in the
   2017 Regulations rather than the Equality Act itself. A 12-month-late reporting rate with no
   consequence is **not** a forcing function; it is evidence that buyers can safely ignore it. This
   materially damages the ethnicity/disability pay gap thesis too, since it will be enforced by the
   same body under the same architecture.

3. **Companies House software-only accounts filing slipped from 1 April 2027 to 1 April 2028.**
   Widely mis-stated. Check any candidate that cited 2027.

4. **The Cyber Security and Resilience Bill is still a Bill.** At Lords Report stage in September
   2026, with substantive effect expected around **2028** via secondary legislation following an
   implementation consultation. It is **PROPOSED**. This is precisely the failure mode that killed
   the defence candidate — treat with the same suspicion.

5. **EU AI Act high-risk obligations moved.** The Digital Omnibus on AI, agreed in 2026, pushed
   high-risk compliance to **December 2027 and August 2028**. The commonly cited "2 August 2026"
   high-risk date is no longer the operative deadline. GPAI obligations and prohibitions kept their
   original dates.

6. **Biodiversity Net Gain contracted by ~80×.** From 31 July / 6 August 2026 the de minimis
   exemption moved from **25m² to 0.2 hectares (2,000m²)**, removing the overwhelming majority of
   minor development from scope. Self-build exemption removed, which partially offsets. A BNG
   candidate sized in early 2026 is now sized wrong.

7. **UK SRS is voluntary today.** The standards were published 25 February 2026 **for voluntary
   use**. The FCA's Policy Statement is only *expected* in autumn 2026 for a 1 January 2027 effect.
   As of 19 September 2026 there is **no mandatory UK SRS obligation on anyone.** Grade: PROPOSED.

8. **Awaab's Law is already served.** Mobysoft RepairSense, Neo Propsys360, PocketSurvey, Awaab
   Comply, Weightmans' compliance tool, and a HACT UK Housing Data Standard use case all exist. The
   forcing function is excellent and the category is taken — the classic LAW 4 trap.

9. **"Not for EU" GB-wide labelling was abandoned.** Reserve powers retained, no rollout. Only the
   NI Retail Movement Scheme obligation is live.

10. **UKCA is not a forcing function.** CE recognition was extended indefinitely for most goods, and
    MHRA opened a February 2026 consultation on indefinite CE recognition for medical devices too.

11. **Clean Heat Market Mechanism and the Critical Third Parties regime both fail LAW 2 outright** —
    roughly 10–20 and fewer than 20 obligated organisations respectively. Impressive penalties,
    no market.

12. **MTD for Income Tax fails LAW 4.** Enormous population, real quarterly cadence, and a fully
    commoditised HMRC-recognised software list. The category has a dozen funded incumbents.

---

## What I would watch, but not yet build on

- **Product Regulation and Metrology Act 2025 secondary legislation.** Consultations closed
  23 June 2026 with a response due within 12 weeks — i.e. **now**. If the online-marketplace duties
  mirror the EU GPSR, that creates a 2027–28 forcing function over a large, poorly-served
  population. Re-check in Q4 2026.
- **Tobacco and Vapes Act 2026 retail licensing.** Act passed 29 April 2026; regime expected
  October 2026 – January 2027; **no guidance, no application dates**. Tens of thousands of
  retailers needing premises *and* personal licences is a strong shape once it is real.
- **ERA 2025 section 35 commencement.** 1.4m employers, criminal offence, six-year retention. When
  the commencement order appears, this becomes one of the largest forced record-keeping obligations
  in UK law.
- **FCA Policy Statement on UK SRS (autumn 2026).** If it lands as consulted, ~1,900 listed issuers
  get a dated climate reporting duty from 1 January 2027.
- **Cyber Security and Resilience Act implementation consultation.** If MSPs get a registration
  deadline and a 24-hour incident clock, that is a genuine 2028 forcing function over thousands of
  UK MSPs.

---

## Sources

**Verified by direct fetch during this sweep `[FETCHED]`:**

- https://www.gov.uk/government/publications/implementing-the-plan-to-make-work-pay-and-employment-rights-act/plan-to-make-work-pay-and-employment-rights-act-timeline-update
- https://www.legislation.gov.uk/ukpga/2025/36/contents (Employment Rights Act 2025)
- https://www.legislation.gov.uk/ukpga/2025/36/section/33 (equality action plans)
- https://www.legislation.gov.uk/ukpga/2025/36/section/35 (annual leave records, 6-year retention, WTR reg 29(1) offence)
- https://www.legislation.gov.uk/uksi/2026/559/regulation/2/made (ERA Commencement No. 4, 1 Jul 2026)
- https://www.legislation.gov.uk/uksi/2026/559/regulation/3/made (ERA Commencement No. 4, 1 Jan 2027)
- https://www.gov.uk/guidance/work-out-the-date-youll-need-to-register-for-carbon-border-adjustment-mechanism-cbam
- https://www.gov.uk/guidance/understanding-martyns-law-and-the-sias-role-as-regulator
- https://www.protectuk.police.uk/martyns-law/martyns-law-overview-and-what-you-need-know
- https://www.gov.uk/government/collections/terrorism-protection-of-premises-act-2025
- https://www.gov.uk/guidance/simpler-recycling-workplace-recycling-in-england
- https://www.gov.uk/government/statistics/business-population-estimates-2025/business-population-estimates-for-the-uk-and-regions-2025-statistical-release
- https://changestoukcompanylaw.campaign.gov.uk/identity-verification/
- https://www.lewissilkin.com/insights/2026/03/26/gender-pay-gap-reporting-enforcement-zero-fines-to-date-but-rising-checks
- https://gender-pay-gap.service.gov.uk/
- https://www.gov.uk/government/statistics/adult-social-care-provider-statistics-england-quarterly-update-to-february-2026/adult-social-care-provider-statistics-england-quarterly-update-to-february-2026

**Corroborated across search results, primary URL not fetched `[SEARCH]`:**

- gov.uk — Terrorism (Protection of Premises) Bill impact assessment (178,900 premises)
- gov.uk — Awaab's Law guidance for social landlords
- gov.uk — Extended Producer Responsibility for Packaging: 2025 base fees
- gov.uk — Packaging producer responsibility monitoring plan 2025 (1,183 non-re-registrants)
- gov.uk — Non-domestic MEES interim response (18 June 2026, EPC C 2027 dropped)
- gov.uk — ESOS guidance; Energy Savings Opportunity Scheme
- gov.uk — Summary of stakeholder roundtables on unfair dismissal changes
- gov.uk — Government response to the consultation on UK Sustainability Reporting Standards
- fca.org.uk — PS24/16 Critical third parties; CP26/5 sustainability disclosures; Consumer Duty board reports
- pensionsdashboardsprogramme.org.uk — connection deadline 31 October 2026
- commonslibrary.parliament.uk — CBP-10352 (packaging EPR), CBP-10453 (DRS), CBP-10442 (Cyber Security and Resilience Bill), CBP-10918 (leasehold)
- legislation.gov.uk — Tobacco and Vapes Act 2026 (c.18); Building Safety Act 2022 s.87
- Baker McKenzie Global Import Blog — HMRC CBAM legislation and guidance, August 2026
- KPMG UK, Jones Day, Saffery, A&O Shearman — UK CBAM framework and accounting periods
- Howes Percival, Brodies, VWV — right to work expansion, 1 October 2026, BSAIA 2025 s.48
- PKF Francis Clark — Companies House verification rates (55% / 50%, June 2026)
- ICAEW — Companies House accounts changes confirmed for April 2028
- RIBA, Browne Jacobson, Charles Russell Speechlys — BSR 2026 plan and Gateway refusal rates
- Gowling WLG, Taylor Wessing — Building Safety Levy, 1 October 2026
- Ashfords, Greenberg Traurig, Norton Rose Fulbright — Martyn's Law penalties and statutory guidance
- Trowers & Hamlins, CIH, NHF — Competence and Conduct Standard, October 2026
- NRLA, Mayer Brown, Gowling WLG — Renters' Rights Act, 1 May 2026 and PRS Database
- BCLP, Bird & Bird, Ward Hadaway — Procurement Act Part 4, s.71 KPIs
- Gibson Dunn, Cooley, DLA Piper — EU AI Act Digital Omnibus delays
- Wiggin, Burges Salmon, DLA Piper — Online Safety Act 2026–27
- Openreach, The Register, Syntura — PSTN switch-off, 31 January 2027
- Zutec, Operance, Yorkshire Post — golden thread incumbents and the February 2025 acquisition
- Mobysoft, Neo Technology, PocketSurvey, HACT, Weightmans — Awaab's Law incumbents
- Valpak, Ecosurety, Beyondly, Reconomy — packaging EPR incumbents
- SAP News (June 2026), Sphera, CarbonChain, Coolset — CBAM software incumbents
- vatcalc, LexisNexis — UK e-invoicing, Peppol, April 2029
- Burges Salmon, Biodiversity Surveyors, CLA — BNG 0.2ha exemption, 31 July / 6 August 2026

**Could not verify `[UNVERIFIED]` — carries no decision weight:**

- Packaging EPR obligated producer count (Commons Library CBP-10352 PDF returned HTTP 403)
- Registered providers of social housing count (RSH August 2026 list returned HTTP 404)
- CQC registered provider and location counts (the DHSC quarterly statistics publish percentages,
  not absolute totals)
- MTD ITSA taxpayer counts per threshold band
- CBAM affected-business count (HMRC tax information and impact note not retrievable)
- Private landlord, leasehold dwelling, food business and LGV driver population figures

---

## Recommendation to the Orchestrator

Three candidates from this sweep deserve to reach wave 2, in this order:

1. **Martyn's Law compliance and evidence platform.** 178,900 obligated premises, spring 2027
   commencement, a named senior individual with criminal exposure, £18m / 5%-of-revenue ceiling,
   an ongoing documented duty, and a regulator publicly warning that the existing vendor field is
   misleading buyers. The main risk is commencement slippage; mitigate by checking for the
   commencement SI before any build decision.
2. **Right-to-work evidence for non-employment engagement.** Live in 12 days, £45k–£60k per worker,
   a population in the hundreds of thousands, and an incumbent field built for HR rather than for
   marketplaces and labour-only subcontracting.
3. **UK CBAM supplier-emissions collection and return filing.** Cleanest data-moat shape in the
   sweep — proprietary supplier emissions records compound — but the EU CBAM vendors will add a UK
   module, so durability must be argued explicitly.

Two candidates should be killed before they are written up: anything resting on **commercial MEES
EPC C by 2027** (the milestone was dropped), and anything resting on **the Cyber Security and
Resilience Bill** (it is still a Bill, with effect around 2028).

And one standing caution for the whole team: **a dated obligation with no enforcement history is a
weak forcing function.** Gender pay gap reporting has been mandatory since 2017, has ~11,000
obligated employers, has a published non-compliance rate — and has produced **zero fines in three
years**. Check the enforcement record, not just the statute, before scoring the forcing-function
axis above 3.
