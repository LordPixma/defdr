# Wave 2 — Sceptic / Red Team report on the ADR-011 shortlist

**Status:** Veto exercised. **Date:** 19 September 2026
**Method:** `docs/method/01-opportunity-scoring-rubric.md` (LAW 1b Enforcement Test; the CBA-ceiling rule; the WTP heuristic)
**Evidence:** primary sources only — legislation.gov.uk raw XHTML, gov.uk content/search APIs, DEFRA and HMRC impact assessments, Ofgem service pages, one vendor page. No reliance on law-firm alerts.

---

## 1. VERDICT UP FRONT

**S1 — Umbrella/agency PAYE liability assurance: KILLED.** The central legal claim in ADR-011 is
wrong in mechanism and wrong in scope. Finance Act 2026 s.24 does **not** move PAYE operation to the
agency; it creates **joint and several liability** while the umbrella remains the employer and keeps
operating PAYE. And the end client — ADR-011's "decisive" unserved buyer — is liable **only where
there is no agency in the chain**. HMRC's own policy paper says so in two bullets. The end-client
market that two analysts converged on does not exist in the form described. HMRC then caps the
category: **£21.7m ongoing annual cost across ~30,400 businesses = ~£714 per firm per year.**

**S2 — Heat network authorisation compliance: KILLED.** The Enforcement Test score of 5 is factually
wrong. Regulation 27 of SI 2025/269 confers **deemed authorisation** on every existing operator, and
that authorisation "remains in force after the initial period." Nothing is mechanically blocked.
Ofgem's enforcement register carries **zero heat network cases** eight months into the regime. And
the kill-shot landed: **Ofgem has already launched a free digital registration service, and will
provide a free digital data-reporting service from Autumn 2026.** DESNZ caps the category at an
**EANDCB of £10.8m/year across the entire GB heat network industry.**

**S3 — Packaging EPR recyclability (RAM): SURVIVES, DEMOTED, CONDITIONAL.** The legal claim verifies
(with three corrections below). The WTP anchor is the only genuine one on the shortlist. But
**94% of obligated producers already use a compliance scheme**, Valpak already sells RAM assessment
at three service levels, and the methodology is a **free published decision tree**. This is a
channel product or a compliance-scheme feature, not a direct-sell £50k SaaS.

**Single strongest warning:** all three shortlisted candidates were scored on a *policy
announcement* rather than on *enacted text and regulator behaviour*. For S1 the announcement and
the statute say different things. For S2 the statute and Ofgem's service say different things. The
Wave 1 process read the press release, not the provision.

---

## 2. LEGAL VERIFICATION TABLE

| Claim | Verified? | Operative provision (quoted) | Status |
|---|---|---|---|
| S1: "Finance Act 2026 c.11 s.24" exists | **YES** | Royal Assent **18 March 2026**. s.24 heading: "Umbrella companies". | In force |
| S1: applies from 6 Apr 2026 | **YES** | s.24(11): *"The amendments made by this section have effect in relation to payments made on or after 6 April 2026."* | In force |
| S1: "the agency, not the umbrella, now operates PAYE" | **NO — FALSE** | New ITEPA s.61Y(2): *"Each relevant party … is, **along with the umbrella company**, jointly and severally liable to pay any amount payable, in accordance with the PAYE provisions, **by the umbrella company**…"* The umbrella remains employer and operates PAYE. | **Claim fails** |
| S1: "HMRC can recover from the agency **or end client**" | **PARTIALLY — materially overstated** | s.61Z(2): the client is a relevant party only if *"the contract … is between the umbrella company and the client"* or the intermediary *"is connected with the umbrella company, or is non-UK resident."* HMRC policy paper: *"more than one agency, the rules apply to the agency that has the direct contract with the end client … **no agency, the rules apply to the end client**."* | **Either/or, not both** |
| S2: heat networks regulated from 27 Jan 2026 | **YES** | SI 2025/269 reg.1(4): remaining provisions in force **27 Jan 2026**. Enforcement (reg.28) in force 27.1.2026. | In force |
| S2: "mandatory Ofgem registration by 26 Jan 2027" | **YES, but not a licence gate** | Ofgem: *"Operators and suppliers of relevant heat networks must give us details about their heat network's organisation, ownership, financial resilience and consumer protection arrangements by 26 January 2027."* But reg.27(1)–(2): existing operators are *"treated as holding a heat network authorisation"* which *"remains in force after the initial period."* | **Deemed authorisation — no cliff** |
| S2: amended/delayed? | **AMENDED TWICE** | SI 2026/7 (made 6 Jan 2026) inserted Part 3A and reg.23A and stripped several Heat Network (Metering and Billing) Regulations 2014 duties. SI 2026/10 (in force 28 Jan 2026) re-cut micro/small-business definitions for redress. Reg.69 requires a **statutory review report within 5 years**. | Live churn + review clause |
| S3: producers self-assign RAG under RAM | **YES** | gov.uk RAM guidance: *"an output for each sub-material – red, amber or green"*; producers *"carry out their recyclability assessments"* themselves. SI 2024/1332 reg.26 + Sch.5 (assessments); reg.64 (modulation). | In force |
| S3: "fees modulate 1.2× → 1.6× → 2.0×" | **YES, with a correction** | PackUK modulation statement Table One: 2026-27 **1.2**, 2027-28 **1.6**, 2028-29 **2.0** — *"These factors apply specifically to red-rated materials."* *"Amber-rated material will see no change."* Green receives a redistribution discount (illustratively **−20.903%**). | **Red only** |
| S3: "base fee £423/t plastic" | **STALE** | Year 2 (2026-27) illustrative **amber** fee for plastic is **£455/t**. Fibre composite £525, aluminium £270, steel £290, glass £205, paper/board £210, wood £450, other £225. | Correct upward |

### The S1 finding in plain terms

ADR-011 §5 says: *"HMRC can recover the umbrella's unpaid PAYE from the agency **or the end client**.
Existing vendors sell agency-side accreditation. The end client carries the same liability with no
product at all."* The enacted scheme does not work that way. Where a UK agency sits between client
and umbrella — which is the ordinary case across the ~30,000 agencies cited — **the agency is the
relevant party and the client is not**. The client becomes liable only where it contracts the
umbrella directly, or where the agency is connected to the umbrella or offshore. The "unserved
side" that made S1 a shortlist candidate is a residual, not a market of 1,500–3,000 buyers.

This is the same failure mode as the defence run: two experts converged on a reading of a policy
announcement. Neither read s.61Z.

---

## 3. ENFORCEMENT TEST (LAW 1b) — SCORES

| | S1 Umbrella JSL | S2 Heat networks | S3 pEPR / RAM |
|---|---|---|---|
| Has the regulator penalised anyone under *this* obligation? | No — power is 5 months old | **No — zero cases** | Not under RAM; yes under predecessor packaging regs |
| Published enforcement register? | No JSL register. HMRC publishes *named tax avoidance schemes* and Spotlights 64/71 — promoter-facing, not JSL | Ofgem publishes an enforcement case list (A Shade Greener, Tomato Energy). **No heat network case appears.** Ofgem has published *enforcement guidelines* and a *penalty policy* only | EA enforcement undertakings exist for the 2007 regs (e.g. £54,880 charity payment, 2021). pEPR: no published register found |
| Does non-compliance mechanically block the business? | **No.** JSL is a recovery power after the event | **No.** Reg.27 deemed authorisation; it *"remains in force after the initial period"* | **Partially yes.** PackUK issues an annual **notice of liability** functioning as an invoice; non-payment within 50 days triggers interest and a variable monetary penalty of the higher of 20% of unpaid fees or 2–5% of UK turnover |
| **Score** | **3** | **2** | **4** |

S2's ADR-011 score of **5** was the single largest scoring error in Wave 1. It rested on
"authorisation is a licence to operate." It is — for *new entrants*. For the entire existing
population of ~14,000 networks, authorisation was conferred automatically by operation of law on
1 April 2025 and does not lapse. The 26 January 2027 date is an **information-supply obligation
inside an authorisation you already hold**, enforceable by compliance order and penalty — i.e. a
theoretical fine, which is exactly the class the gender-pay-gap precedent warns about.

S3 is the only candidate where non-compliance reaches the cash. The notice-of-liability mechanism
is a real, dated, financially-enforced obligation with a turnover-percentage penalty behind it.

---

## 4. CBA CEILING TABLE

| Candidate | Source | Obligated population | Government's modelled ongoing annual cost | Implied per-firm ceiling | Required ACV (ADR-011 rule) | Verdict |
|---|---|---:|---:|---:|---:|---|
| **S1** | HMRC TIIN, *Umbrella company market — changes to Income Tax rules* | 30,000 agencies + 400 umbrellas | **£21.7m/yr** continuing (plus £9.9m one-off familiarisation and training on due-diligence checks) | **~£714/firm/yr** | £50,000 | **Fails by ~70×** |
| **S2** | DESNZ IA, RPC opinion (green-rated) | GB heat network operators (~14,000 networks) | **EANDCB £10.8m/yr** (2019 prices). Operator costs £123m over 30yr: familiarisation & compliance £71m + maintenance £52m | not disclosed per-network; £10.8m is the whole-industry annual figure | £25,000 × 600 = **£15m** | **Target revenue exceeds the entire national EANDCB** |
| **S3** | DEFRA IA (UKIA 2024/197, Final, RPC "fit for purpose") | **6,971 large + 3,105 small + 46 online marketplace producers** | Data reporting **£24.0m/yr** under pEPR vs **£10.5m/yr** baseline → **£13.5m/yr increment**. Producer familiarisation only **£2.5m** total across the 10-year appraisal | **~£1,300–2,400/producer/yr** | £50,000 | **Fails by 20–40× on the CBA test** |

Three notes, in fairness to S3:

1. **DEFRA never costed RAM.** The phrase "recyclability assessment" returns **zero hits** across the
   125-page final IA (signed 23 Oct 2024). RAM v1.1 post-dates it. So the £13.5m/yr increment is a
   ceiling on *pEPR data reporting*, not on RAM specifically. There is no published RAM CBA. That is
   a genuine gap in the ceiling argument, and it is the only reason S3 is not killed outright here.
2. **S3 is the one candidate where the WTP heuristic bites correctly.** The fee line is regulated
   cash. A 5,000t plastic producer at £455/t pays £2.275m. All-red in 2026-27 adds ~£455k; all-green
   subtracts ~£475k. The swing is ~£930k, rising as the factor goes 1.6 then 2.0.
3. **But the swing is bought with packaging engineering, not software.** The rating is a property of
   the physical pack. A RAM tool *measures* the fee; it does not *reduce* it. The buyer's money goes
   to material substitution and pack redesign. That is a consultancy and a materials-science spend,
   which is precisely where Valpak has positioned ("eco-modulation cost modelling", three service
   levels).

S1 and S2 both breach the ceiling by the same arithmetic that killed Martyn's Law (enhanced tier)
and the FCA material third-party register in Wave 1. Applied consistently, they die for the same
reason.

---

## 5. EVIDENCE GAP (LAW 3 CLASSES 1 AND 2)

### Class 1 — job postings

Indeed (403), CV-Library (403) and Totaljobs (connection refused) remain closed. **Reed.co.uk
returns HTTP 200** and was used. Important methodological caveat discovered in the process: **Reed's
quoted-phrase search does not bind as an exact phrase.** A search for `"heat network"` returned 86
results whose visible titles were overwhelmingly *Heating Engineer*, *Heat Treatment Operator*,
*Data Centre Network Engineer* and *Air Conditioning Engineer* — with exactly **one** genuine heat
network role in the first fourteen (*Operations Manager – Heat Networks/Energy Centre*, Penguin
Recruitment). Counts below are therefore **upper bounds**, inflated by fuzzy matching.

| Search term | Reed result count (upper bound) | Assessment |
|---|---:|---|
| `"labour supply chain"` | **0** | **S1's budget-holding role does not exist as a UK job title.** |
| `"supply chain compliance"` | 8 | Generic, not labour-supply-specific |
| `"payroll compliance"` | 73 | Exists, but is an agency back-office function, not a new buying centre |
| `"heat network"` | 86 (≈1 genuine in top 14) | **S2's role effectively does not exist** |
| `"heat networks"` | 12 | — |
| `"packaging compliance"` | 5 | **Tiny** |
| `"extended producer responsibility"` | 5 | **Tiny** |
| `"packaging technologist"` | 3 | Tiny |

**Finding: no candidate has a budget-holding role that exists in volume as a UK job title.** This is
a material negative across all three, and it is the first time the shortlist has been tested against
class-1 evidence at all. For S1 the figure is literally zero.

### Class 2 — procurement records

**Not obtainable.** I re-tested every route the brief suggested and confirmed Wave 1's finding
empirically rather than by assertion:

- **Find a Tender** `Search/Results?keywords=…` — parameter does **not** bind. `heat network`,
  `recyclability assessment`, `packaging compliance scheme` and the control term `zzzznonsensezzz`
  **all returned identically 311,208 notices**.
- **Contracts Finder OCDS** `/Published/Notices/OCDS/Search?keyword=…` — returns HTTP 200 and a
  valid 562KB OCDS release package, but the server echoes the keyword into the `uri` field and
  returns the unfiltered latest-100 award set. The keyword is accepted and ignored.
- **Contracts Finder POST** `/Published/Notices/Search` — HTTP 404.
- **Contracts Finder website search** `Search/Results?Keywords=…` — returns no parseable count.

Exhaustive keyword retrieval would require paging the full OCDS corpus (hundreds of thousands of
notices) and grepping locally, which is out of budget. **So for all three candidates the question
"has anyone ever bought software for this?" remains unanswered.** Given that class 1 has now come
back near-zero for all three, the absence of class 2 should be treated as an aggravating unknown,
not a neutral one.

The single class-2-adjacent datum found: **94% of obligated packaging producers already purchase
through a compliance scheme** (DEFRA IA, used to select the £564 regulator fee). That is a
procurement fact, and it is bad news for S3.

---

## 6. WHAT KILLS THIS BY 2031

**S1 — the measure is designed to shrink its own market, and HMRC has published the decay curve.**
The TIIN's Exchequer impact runs **+£155m, +£715m, +£635m, +£540m, +£425m, +£255m** across 2025-26
to 2030-31. That is a 64% decline from peak. HMRC is modelling behavioural change: agencies dropping
umbrellas and insourcing PAYE, and non-compliant umbrellas exiting. The 400-umbrella population is
the thing being regulated out of existence. This is the **same shape as the sponsor-licence payroll
candidate killed in Wave 1** — peak pain now, structural decay after. A product whose TAM is
explicitly forecast by the Treasury to fall by two thirds inside the build window is not a two-year
bet. Secondary killer: the rational response is contractual, and HMRC says so — its own guidance
notes agencies *"can add a clause … requiring their directors to indemnify you against tax
liabilities."* An indemnity plus a tax-liability insurance wrapper costs a fraction of software and
is available today.

**S2 — Ofgem is the incumbent.** Ofgem has *already launched* the free digital registration service,
and states *"From Autumn 2026, heat networks can submit data using our digital service"*, with an
RFI issued to all registered parties before each window and reporting *"on both a quarterly and
annual basis."* The regulator is building the collection layer, the schema and the calendar, free.
What remains sellable is assembling the underlying data — heat sold, tariffs, outages, customer
counts — and that data already sits inside the billing platforms ADR-011 names (Insite ~38,000
residents, Switch2, Evinox). Those vendors are one feature release from absorbing it. Secondary
killer: ADR-011 treats **66% social-landlord ownership** as buyer concentration. It is the opposite.
Social landlords are the least-funded buyer class in the UK, are simultaneously absorbing Awaab's
Law, the Building Safety Act golden thread and decarbonisation capex, and will use the free Ofgem
portal. Tertiary: SI 2025/269 reg.69 mandates a review report within five years, and SI 2026/7
already stripped duties out of the 2014 metering regulations — the regime is being simplified, not
tightened, in its first year.

**S3 — the compliance schemes absorb it, or PackUK ships the tool.** 94% of producers already buy
through a scheme; Valpak already sells RAM assessment with *"three service levels"* including
*"review of in-house assessments"* and *"eco-modulation cost modelling"*, and gives *"RAM Decision
Trees … to members"*. PackUK publishes free RAM one-page material guidance cards (standard and
colourblind versions), free supplementary guidance, and the decision tree itself under OGL v3.0.
The gap PackUK has *not* filled is a calculator — but the RAM roadmap shows quarterly Technical
Advisory Committee meetings and annual republication (RAM 2027 published July 2026, RAM 2028
July 2027), which is exactly the cadence at which a scheme administrator eventually ships a tool.
Secondary killer: the **2027/28 pEPR policy review** is on PackUK's own published roadmap. Tertiary:
AI commoditisation is a real threat here in a way it is not for S1/S2 — the methodology is a
published decision tree over a bounded material taxonomy, which is close to the ideal shape for a
general-purpose assistant to execute from the gov.uk pages by 2029.

---

## 7. KILL-SHOT RESULTS

**S1(a) — is the end client genuinely liable?** **No, not in the ordinary case.** s.61Z(2) plus
HMRC's two-bullet rule: with an agency in the chain, liability attaches to the agency with the
direct client contract; the client is caught only where there is no agency, or the agency is
connected/offshore. **The end-client product has no population.**

**S1(b) — does HMRC impose a check obligation?** **Softly, yes — six checks are listed** (due
diligence on the whole supply chain; check payslips that PAYE is operated on the full amount;
caution with offshore umbrellas or those offering incentives; check the named tax avoidance schemes
list; check Companies House filings for consistency; educate workers). This is the strongest
remaining element of S1. But it is guidance, not a statutory duty, and the same page offers the
cheaper alternative in the same breath — a director indemnity clause. **If the rational response is
a contractual indemnity rather than software, S1 dies. The guidance itself proposes the indemnity.**

**S1(c) — do FCSA / Professional Passport discharge the duty?** **No, and HMRC does not mention them
at all.** This is the one finding that *favours* S1: accreditation is not a safe harbour, so
accredited-supplier-list vendors do not close the gap. It is not enough to save the candidate
against the population and CBA failures.

**S2(a) — will Ofgem provide the portal and templates free?** **Yes. Already done for registration;
committed for data reporting from Autumn 2026, quarterly and annual, with Ofgem issuing the RFI.**
Kill-shot lands.

**S2(b) — is 26 Jan 2027 a one-off?** **Yes.** It is a one-time submission of organisation,
ownership, financial resilience and consumer protection details. Ongoing reporting exists but runs
through Ofgem's own free service on Ofgem's own schema, which Ofgem has not yet finalised
(*"We'll publish further guidance about the data reporting process before the first reporting
period"*). Selling a SaaS against an unpublished schema that the regulator will service for free is
not a product plan.

**S2(c) — is 66% social-landlord ownership a problem?** **Yes.** See §6.

**S3(a) — does Valpak already sell RAM assessment?** **Yes**, at three service levels, covering
one-time assessments, review of in-house assessments, data collection and reporting, and
eco-modulation cost modelling. **No public pricing** — quotes only, which is itself a signal that
the price is consultative and per-project, not a recurring licence.

**S3(b) — does PackUK publish the methodology and free tooling?** **Methodology yes, tooling no.**
Decision tree, material guidance cards and supplementary guidance are free under OGL. No calculator
or spreadsheet is published. **This is the entire remaining aperture for S3.**

**S3(c) — is it a spreadsheet rather than a SaaS?** For a single-SKU producer, yes. For a
multi-thousand-SKU FMCG producer facing an annually-republished methodology, a quarterly TAC
changing definitions, and a fee factor rising 1.2 → 1.6 → 2.0, no — the version-control problem is
real and a spreadsheet goes stale every July. **This is the strongest surviving argument on the
entire shortlist.**

**S3(d) — do schemes bundle RAM free with membership?** **Not established.** Valpak's page gives no
pricing and does not present RAM as included. Ecosurety's and Beyondly's pages returned HTTP 200 but
rendered as navigation and footer only — I could not extract service or pricing content from either.
**This is the highest-value unresolved question in the whole report.** If Ecosurety and Beyondly
bundle RAM free with scheme membership, S3 dies on LAW 4 and the shortlist is empty.

---

## 8. FINAL RANKING

| Rank | Candidate | Call | Decisive reason |
|---|---|---|---|
| 1 | **S3 — pEPR RAM** | **SURVIVES — conditional, demoted from "best arithmetic" to "only one left"** | Legal claim verified; only candidate with a real cash-outflow WTP anchor and a real enforcement mechanism (notice of liability, 2–5% turnover penalty). But 94% of buyers are behind a compliance-scheme channel and the incumbent already sells it. |
| 2 | **S2 — Heat networks** | **KILL** | Enforcement score was wrong by three points (deemed authorisation, zero cases). Ofgem ships the portal free. Whole-industry EANDCB £10.8m/yr is below the target revenue. |
| 3 | **S1 — Umbrella/agency PAYE** | **KILL** | Legal mechanism misstated; the end-client buyer does not exist as described; £714/firm/yr published ceiling; zero job postings; Treasury forecasts its own TAM down 64% by 2030-31. |

**Condition on S3:** do not proceed until someone has obtained, in writing, the RAM service terms and
pricing of **Ecosurety, Beyondly and Clarity Environmental**. If any of them includes RAM assessment
in scheme membership, kill S3 and declare Wave 2 empty. That is a half-day of phone calls and it
governs a two-year commitment.

**Second condition:** S3 must be re-specified as a **per-SKU, sold-through-schemes** product with
the schemes as channel, not as a direct-sell £50k platform. At 6,971 large producers, £50k ACV needs
60 customers = 0.86% of the obligated population — the arithmetic is comfortable. The obstacle is
not the count, it is that 94% of those 6,971 already have a vendor for this exact obligation.

**Strongest single warning, repeated:** Wave 1 scored announcements. S1's announcement (March 2025,
"PAYE moves to the agency") and S1's statute (March 2026, "joint and several liability") describe
different regimes, and the shortlist was built on the announcement. Before any candidate is scored
above 3 on forcing function again, someone must read the enacted operative provision and quote it.

---

## 9. ITEMS I COULD NOT VERIFY

1. **Procurement records (LAW 3 class 2) for any candidate.** Find a Tender and Contracts Finder
   keyword parameters do not bind; confirmed with a nonsense control term. Requires bulk OCDS
   download and local grep.
2. **Whether Ecosurety / Beyondly / Clarity bundle RAM with membership.** Pages fetched HTTP 200 but
   returned only chrome. The most important open question in this report.
3. **Valpak's RAM pricing.** Not published; quote-only.
4. **The "290 suppliers registered with the Energy Ombudsman on day one" figure.** Not re-verified;
   the Energy Ombudsman heat-network supplier portal was identified but not fetched. Note that
   SI 2025/269 reg.56(9) binds deemed-authorised non-members to the Scheme Terms *anyway*, which
   makes the 290 figure much less alarming than ADR-011 presents it.
5. **The "~14,000 GB heat networks" figure.** Ofgem's "who should register" page publishes no
   population estimate; the DESNZ IA gives no per-network cost.
6. **Ofgem's per-operator registration burden in hours.** Not published.
7. **Any RAM-specific impact assessment.** None exists; the pEPR IA predates RAM and does not
   mention recyclability assessment once.
8. **Exact job-posting counts.** Reed's quoted search is fuzzy; all counts in §5 are upper bounds.
   Indeed, CV-Library and Totaljobs remain blocked.
9. **SafeRec pricing and whether it has shipped a s.61Y module since April 2026.** Not checked —
   S1 failed on population and CBA before incumbency mattered.
