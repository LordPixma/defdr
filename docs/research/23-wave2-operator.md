# Wave 2 — Operator Review: does the product survive contact with the daily job?

**Role:** Operator (the person who uses it every day, not the person who signs)
**Date:** 19 September 2026
**Inputs:** ADR-011 shortlist (S1 umbrella/agency PAYE, S2 heat network authorisation, S3 packaging RAM)
**Method:** binding — `docs/method/01-opportunity-scoring-rubric.md`
**Budget note:** WebSearch quota exhausted in Wave 1. All evidence below is direct-fetched primary
source: regulator guidance, regulator PDFs, vendor product/pricing pages, developer API catalogues
and a practitioner forum. Gaps are listed in §8.

---

## 1. Verdict table

| Candidate | Removes or creates work? | Is the input data obtainable? | Integration feasible? |
|---|---|---|---|
| **S1 — Umbrella/agency PAYE assurance** | **CREATES WORK** | **NO — not without the umbrella's voluntary consent. There is no legal right and no HMRC feed.** | **NO.** No HMRC third-party API exists for the decisive fact (remittance). Agency back-office APIs do not expose the relevant entities. |
| **S2 — Heat network authorisation** | **NEUTRAL** (creates work in cycle 1, removes it from cycle 2) | **PARTIALLY — the data exists but sits in 3–4 systems the asset officer does not own, and one whole class of it does not exist at all** | **WEAK.** No public API on any billing platform or housing system found; Ofgem's own service is in private beta with bulk upload only "planned" |
| **S3 — Packaging EPR / RAM** | **REMOVES WORK** | **YES — the component list already exists in the producer's own pEPR file; the missing attributes are supplier declarations the regulator has made expensive to lack** | **YES, and cheaply.** Seed from the producer's existing 15-column pEPR CSV. No integration required to reach first value. |

**Headline for the buyer-side agents:** S1 is not an operator product. It is a product whose input
data is held by the party being audited, who has no obligation to hand it over. S3 is the only
candidate where the operator can get value on day one from a file they already have.

---

## 2. S1 — Payroll/compliance administrator at a recruitment agency

### 2.1 What the job actually looks like today

The agency's payroll/compliance administrator sits on **one side of a two-sided record** and has
never seen the other.

The weekly cycle, from the artefacts:

1. **Timesheet in.** Worker or line manager approves hours in the agency back-office (Etz, Bullhorn,
   3R, Merit). Etz markets this as "turn a timesheet into an invoice in 60 seconds."
2. **Self-billing invoice out.** Under VAT Notice 700/62, *the agency raises the umbrella's invoice*
   — "the customer prepares the supplier's invoice and forwards a copy to the supplier with the
   payment." A written self-billing agreement must exist and HMRC advises review every 12 months.
   HMRC's agency guidance lists "Follow the VAT requirements for operating self-billing with an
   umbrella company" as a **must**.
3. **Payment to the umbrella** at the assignment rate × hours.
4. **Quarterly employment intermediaries return.** Mandatory: "Submit the quarterly employment
   intermediaries return for workers you place with end clients, where you do not operate PAYE.
   This should include umbrella company employees." The template is a downloadable **ODS or CSV**
   spreadsheet from GOV.UK, uploaded to the employment intermediaries service.
5. **Key Information Document** per worker, non-delegable: "You cannot defer this to a third party,
   like an umbrella company." The KID must be reissued on significant change.
6. **Due diligence folder.** Companies House match, VAT registration match, insurance, GLAA licence,
   accreditation status, bank-details-to-name match.

So the administrator's existing data is: **hours, assignment rate, £ paid to the umbrella, worker
identity, umbrella identity.** That is the entire left-hand side of the reconciliation.

### 2.2 WHERE DOES THE DATA COME FROM? — and the answer is: it doesn't

This is the decisive finding of this report.

**(a) The umbrella still runs PAYE. The agency does not get the RTI data by operating it.**
GOV.UK, *PAYE rules for labour supply chains that include umbrella companies from 6 April 2026*
(last updated 19 June 2026, "the wording about the rules and draft legislation have been updated
because it is now in force"):

> "If you're the umbrella company employing workers — You're still responsible for working out PAYE
> for your employees correctly and paying us on time."

and for the agency:

> "You're responsible for making sure that the umbrella company operates PAYE correctly. If we find
> an umbrella company has not paid the correct amount of PAYE to us, we'll recover it from you."

**Liability moved. The data did not.** The agency now owns a risk whose evidence lives entirely in
someone else's payroll system.

**(b) There is no statutory right to the umbrella's data.** The only obligation found anywhere is a
single sentence of *guidance*, not statute:

> "You'll need to provide the agency, or end client, with the information they need to check you're
> doing this."

No specified dataset, no format, no frequency, no penalty for refusal, no named information notice.

**(c) HMRC itself routes the agency to the worker, not the umbrella.** *Responsibilities for
employment businesses working with umbrella companies* (updated 17 September 2025), due diligence
section, verbatim:

> "get reconciliation statements (also known as a pay statements) **directly from the worker (where
> they have them)**, to check the assignment rate matches the money you have sent to the umbrella
> company"
> "get payslips **directly from the worker**, to check the umbrella company is acting as the
> employer and operating PAYE"

The regulator's own recommended evidence-gathering route for the exact reconciliation this product
proposes is: **ask each worker individually, and accept that they may not have it.** For an agency
with 2,000 contractors, that is 2,000 consent conversations per pay period. That is not a workflow a
software product improves; it is a workflow a software product inherits.

**(d) The final fact — remittance — is unverifiable by any third party.** I checked HMRC's Developer
Hub API catalogue directly. Every PAYE/employment API (Individual Employment, Individual Income,
Individual Tax, National Insurance, PAYE Online, Real Time Information Online) is **user-restricted
or employer-restricted**. There is no API by which an agency, or a vendor acting for one, can query
whether another company has remitted PAYE.

A practitioner on the ContractorUK umbrella forum states the consequence precisely:

> "[SafeRec] cannot guarantee that PAYE liabilities are paid, only that the calculations done to
> reach the amount of tax and NI payable have been done correctly."
> "Until there is a direct link to HMRC from the third-party audit platforms, that will always be
> the case."

**The agency's liability is for tax not *paid*. No product can see whether it was paid.** The
product can only ever verify the arithmetic on a payslip the umbrella chose to show it.

### 2.3 ADR-011's incumbency claim is wrong

ADR-011 §5 states: *"Nothing reconciles agency rate → umbrella payslip → RTI → HMRC remittance."*
SafeRec's own certification page describes exactly that chain:

- "Real-Time Payslip and CIS Statement Auditing via secure API integration"
- "RTI Cross-Reference & Monthly check of the Umbrella's HMRC tax account"
- "Audits must be conducted directly at source via secure API integrations with the umbrella's
  payroll system. No screenshots. No spreadsheets. No room for manipulation."

The product exists. **But note who it is sold to.** SafeRec solved the data problem by selling the
badge to the *umbrella*, which then voluntarily API-integrates its own payroll and grants access to
its HMRC account. The agency-facing product is free-riding on that consent. Where an umbrella has
not certified, SafeRec's tool degrades to a **drag-and-drop payslip uploader** ("Upload any UK
payslip", "Upload & scan the payslip — format and content captured").

That is the honest architecture of this entire category: **automated where the umbrella volunteers,
manual data entry where it does not.** A new entrant faces the same wall, with none of the installed
base of consenting umbrellas.

### 2.4 The price anchor kills it independently

SafeRec's published pricing: Basic free, **Protect £149/month, Premium £299/month, Elevate
£449/month.** That is **£1,788–£5,388 ACV**. ADR-011 §1 adopted a hard rule: *we do not build a
sub-£10k ACV product.* The market's own price for agency-side umbrella compliance is a fifth to a
third of that floor, set by an incumbent that already has the umbrella API integrations.

### 2.5 Does it create work? **CREATES WORK — decisively**

To produce any output, the administrator must:
- obtain payslips for every worker for every period (from workers, individually, voluntarily), or
- persuade every umbrella on the PSL to integrate its payroll with a vendor it has no contract with

Before the product says anything useful, the operator has performed thousands of chase-ups that did
not exist before. This is the textbook case in the brief: *a product that requires manual data entry
of thousands of workers before it produces value has an adoption problem that pricing cannot fix.*

### 2.6 Integration reality

| System | Public API? | Does it hold what we need? |
|---|---|---|
| HMRC PAYE/RTI | Yes, but **user-restricted only** | Holds the decisive fact; inaccessible to third parties |
| Bullhorn REST | Yes, OAuth 2.0, documented | Candidate, ClientContact, JobOrder, Placement, BillableCharge. **No payroll, umbrella or vendor entities documented.** Gives us the left side we already have |
| Etz | No public API docs found | Timesheets/invoicing; "HMRC ready data" unspecified |
| Umbrella payroll systems | Per-umbrella, private | The right side. Requires the audited party's consent, per umbrella |

Integration would require the cooperation of ~400 umbrella companies individually — each of whom is
the party being checked. Per the brief's own test: *an integration that requires a vendor's
cooperation and they have no API is a two-year sales problem.* Here it is a 400-vendor sales problem
against counterparties with a motive to decline.

---

## 3. S2 — Asset/energy officer at a housing association, 40 heat networks

### 3.1 What the job actually looks like today

There is no existing workflow, because the obligation is new. The asset officer's starting position
is: a property list, a set of M&E asset records of varying quality, a billing contract with Insite /
Switch2 / Evinox, and a service charge schedule owned by Finance.

Two distinct workloads land:

**(a) Registration — deadline 26 January 2027, one-time.** Ofgem's registration information list
(node/180287) gives roughly 40 fields per network across five stages: introductory (regulated
activities, shared ground loop classification, network type, service status, activation date, other
suppliers); technical (primary energy centre address and coordinates, service types, capacity,
primary technology); customers and metering (domestic/non-domestic mix, micro/small business
presence, PPM deployment, metering/billing agent); consumer protections (vulnerable customer count,
PSR status, complaints procedure, payment-difficulty process); billing (frequency, bill calculation
transparency, bill contents). Plus a one-off organisation stage with an SMRI fit-and-proper
declaration.

Two operator-critical facts: the service is **in private beta** as of this fetch, and — importantly —
**"We will not ask you to upload supporting documents or evidence."** Registration is a
self-declaration form. There is no evidence pack to assemble and no document vault to sell.

**(b) Regular data reporting under Authorisation Condition A09 "Provision of Information to the
Authority" — quarterly and annual, forever.** From Ofgem's *Heat networks: regular data reporting*
guidance (31pp, March 2026):

- **Quarterly** (submission window = the month after quarter end): domestic customers meeting the
  debt trigger (>£200 outstanding 3+ months), self-disconnections, disconnections for non-payment,
  customers on repayment plans, reconnections, complaints resolved Day+1 to 8 weeks, and the full
  pricing set — standing charges in pence/day, unit rates in p/kWh, connection charges, other
  charges, flat fees, total charges across domestic and non-domestic customers.
- **Annual** (by 30 April): domestic and non-domestic customer counts, small/micro breakdown, PPM
  counts split smart vs legacy, heat cost allocators, heat meters in dwellings, customers with smart
  metering, billing frequency, customers by payment method, consumers in vulnerable situations, bad
  debt value, charges at 6,000 kWh reference usage, pricing methodology.
- **Financial resilience** (annual): net profit/loss, total income, OPEX, liquid assets, assets vs
  liabilities, hedging. **Local Authorities and Registered Social Housing Providers are explicitly
  exempt from every financial resilience data point.** S2's persona does not have to do the hardest
  table.

### 3.2 WHERE DOES THE DATA COME FROM?

| Data class | Actual holder | Can the asset officer export it? |
|---|---|---|
| Energy centre address, coordinates, capacity, technology | Asset register / M&E O&M manuals / consultant surveys | Sometimes. Often only in PDF drawings per scheme |
| Customer counts, meters, HCAs, PPMs, smart metering | **The billing agent** (Insite, Switch2, Evinox) | Only by asking the agent. Insite's site describes billing, payments, `my insite` portal, KURVE PAYG — **no API, no data export, no Ofgem reporting feature advertised** |
| Vulnerable consumers / PSR | Housing management system (Aareon HomeMaster/ActiveH/QL, NEC, Civica, MRI) | In principle. Aareon's UK site advertises "seamless integrations" but **publishes no developer portal, no API docs, and no heat network or energy functionality** |
| Debt, disconnections, repayment plans | Income/rents team, or the billing agent | Fragmented between two owners |
| Standing charges, unit rates, flat fees | Finance / service charge team | **Frequently does not exist** |

**The one that does not exist.** Ofgem paragraph 2.21:

> "Heat network suppliers may be bundling the heat charge, this is where heat charges are included as
> part of wider costs, for example rent, service charges. This can be a requirement of a lease or
> equivalent agreement. This practice will not be uniform across the sector as **some suppliers will
> have the information on the unbundled heat charge.**"

"Some" is the regulator conceding that many will not. A housing association that recovers heat
through a variable service charge has **no standing charge in pence per day and no unit rate in
pence per kWh**, because it never set one. Ofgem asks for both, quarterly. Producing them is not
extraction — it is **cost apportionment modelling that must be invented, defended and repeated every
quarter.** Similarly, the quarterly debt figures are asked for *heat specifically* ("If heat is
charged separately this should be for heat debt. If charges are bundled with other charges such as
rent the customer numbers in debt should still be provided") — which means a HA must disaggregate
arrears it has never disaggregated.

### 3.3 Does it create work? **NEUTRAL**

Cycle 1 is a data-creation project: 40 networks × ~40 registration fields, plus building an
unbundling methodology from scratch. Nothing removes that. From cycle 2 onward, a product that holds
last quarter's answers and asks only what changed genuinely removes work — and Ofgem has designed
for exactly that: "we will instead allow for users to review their previous data submission and
confirm whether there have been no changes."

Net: neutral. The honest pitch is not "we save you the return", it is "we hold the apportionment
model and the audit trail so you can defend it".

### 3.4 Integration reality — the weakest of the three

- **Ofgem itself:** digital service in **private beta**; data submission functionality "expected to
  be introduced later in 2026"; bulk upload is a plan, not a feature — "We **plan** to allow the bulk
  submission of regularly reported data as part of the ongoing enhancements". There is nothing to
  integrate with today, and no published API.
- **Billing platforms:** Insite — no API or export documentation on site. Switch2 — site returns HTTP
  202 to non-browser clients (bot-walled), could not assess. Evinox — no API documentation found.
- **Housing systems:** Aareon publishes no developer portal. NEC, Civica and MRI not reached
  (budget).

This is a CSV-and-manual-upload product for at least 18 months. That is survivable, but it means the
moat cannot be integration; it has to be the apportionment methodology and the multi-network estate
view.

### 3.5 Enforcement pressure on the operator is currently low

Ofgem's compliance approach: *"Our priority in the first year is to get a good understanding of the
sector"*; "proportionate, pragmatic regulation that supports compliance and good practice without
unnecessary burdens"; self-reporting encouraged; escalation only where an operator "does not work
with us constructively". Under LAW 1b there is **no enforcement record**. The licence-to-operate
argument in ADR-011 stands on the statute, but nothing is pressing the asset officer this year.

The regulator's CBA also caps the category: the RPC-green impact assessment puts **£71m
familiarisation and compliance** plus £52m maintenance on operators, with an **EANDCB of £10.8m**
(2019 prices). Spread across the authorised population that is low single-digit thousands of pounds
per organisation per year for *all* compliance — a hard ceiling on ACV unless sold per network to
large estates, which is exactly the test ADR-011 flagged.

---

## 4. S3 — Packaging technologist at a producer

### 4.1 What the job actually looks like today

The technologist is **already reporting component-level packaging data and has been since 2023.**
This is the most important and most overlooked fact about S3.

The pEPR submission is a **CSV with 15 columns**: `organisation_id`, `subsidiary_id`,
`organisation_size`, `submission_period`, `packaging_activity`, `packaging_type`, `packaging_class`,
`packaging_material`, `packaging_material_subtype`, `from_country`, `to_country`,
`packaging_material_weight`, `packaging_material_units`, `transitional_packaging_units`,
`ram_rag_rating`. Prepared in Excel, tab 3 saved as CSV, uploaded to the Report Packaging Data
service. Twice yearly (H1 due 1 October, H2 due 1 April).

Guidance is explicit: **"You must report the weight and material of each component separately."**
Rows aggregate by activity/type/class/material/subtype/country — **not per SKU**. This matters
enormously for the "does it create work" test: the deliverable is not hundreds of SKU records, it is
an aggregated file the producer already produces.

### 4.2 WHERE DOES THE DATA COME FROM? — held partly, and the gap is priced

**What the producer already holds:** the component inventory with material and weight. Three
reporting cycles of it.

**What the producer usually does not hold** — the attributes that actually drive the RAG rating:
sub-material/polymer identification, printing ink compliance with the EuPIA Exclusion Policy, UK
REACH SVHC content above threshold, intentionally-added PFAS, embedded EEE or batteries. These are
**supplier declarations**, and Defra says so twice:

> "If you are unsure of the material composition of your packaging or packaging components, **it is
> your responsibility to obtain this information from your suppliers.**"
> "If you do not know what the packaging you supply is made of or are missing other technical details
> that you need to complete the assessment, **contact the packaging manufacturer.**"

**And here is the mechanism that makes this a business.** Among the automatic reds:

> "any household packaging within scope of the RAM **which has not been assessed or where the detail
> required to undertake an assessment isn't available**"

**A missing supplier declaration is not a compliance risk. It is a red rating, and a red rating is a
20% uplift on that tonnage's disposal fee.** PackUK: "Red RAM rating applies a 20% increase to the
amount of a liable producer's household packaging waste disposal fees"; amber is neutral; green
receives a reduction funded by the red premium. On a £423/tonne plastic base fee, an unanswered
supplier email costs roughly £85 per tonne, every year, until answered. This is the rubric's WTP
heuristic in its purest observed form: *price against a regulated cash outflow.* The product's job is
supplier-declaration chase-and-evidence, and the ROI is arithmetic.

### 4.3 Does it create work? **REMOVES WORK**

The onboarding cliff that would kill this does not exist, because the SKU/component load has already
happened. Day one is: **upload your last submitted pEPR CSV.** The product immediately shows which
tonnage is defaulting to red for missing detail and what that costs. No manual entry of hundreds of
SKUs precedes first value.

The work it removes is the supplier chase — today an Outlook folder and a shared spreadsheet — and
the annual re-assessment. The RAM roadmap confirms the re-assessment is permanent: **RAM 2027
published July 2026, RAM 2028 July 2027, RAM 2029, RAM 2030**, with quarterly Technical Advisory
Committee meetings and a scheduled sequence of material reviews (flexible plastics Q4 2026, rigid
plastics Q1 2027, printing inks and security tags Q3 2027, glass Q3 2028, paper and board Q4 2028,
aluminium and steel Q1 2029, bioplastics Q2 2029, wood Q3 2029). Every one of those can flip a
component's rating. A producer who assessed once must re-assess annually against a moving
methodology — which is a compounding record, not a one-off project.

### 4.4 Integration reality

None required to reach value — the CSV is the integration. Later, upstream integration to PLM/spec
systems and supplier portals is desirable but optional, and the natural expansion path is a supplier
portal we operate ourselves (we control both ends: producer invites supplier, supplier attests).
That is a far better integration posture than S1 (must integrate with the audited party) or S2 (must
integrate with vendors that publish no APIs).

**Incumbency, honestly stated.** ADR-011 scored this incumbency 2 and it is the right worry. Valpak
sells "Advanced RAM services" — packaging reviews and recyclability assessments, format redesign
advice, and explicitly "RAM Data Solutions… collect, manage and report information aligned with RAM
criteria". Ecosurety has 500+ brands. Compliance schemes already hold the producer's submission file,
which is precisely the asset I described as our onboarding advantage — **they have it too, and they
have it already.** Defra signposts them: "You can also contact a third party provider… Third party
providers are likely to charge a fee for this." The counter is that these are consultancy
engagements, not systems of record with supplier-attestation workflow — but that is an assertion, and
Wave 2's incumbency reviewer should test it. Note also that no free PackUK tool exists; the support
package published is guidance notes and infographic cards, not software.

---

## 5. Time-to-first-value

| Candidate | First useful output | Gating dependency |
|---|---|---|
| **S3** | **Days.** Upload last pEPR CSV → red-exposure model in £ and a prioritised supplier chase list | None. The file exists and the operator owns it |
| **S2** | **4–10 weeks.** Registration pack for 40 networks | Asset data quality; a billing agent willing to export; Finance agreeing an unbundling method |
| **S1** | **Indefinite.** Nothing until payslips arrive | Consent from ~400 umbrellas or thousands of individual workers. Not in the operator's gift |

The Wave 1 Birdie observation (mandatory implementation above 300 care recipients) cuts differently
across the three. For S3 implementation is optional, so it can be sold as a moat-building upsell
rather than a barrier. For S2 implementation is effectively compulsory — someone must build the
apportionment model — which makes services revenue real but slows land-and-expand. For S1 there is
nothing to implement, because there is nothing to load.

---

## 6. What practitioners actually complain about

This is where the thesis and the pain diverge most sharply.

**S1 — they are not complaining about reconciliation. They are complaining about being forced to
switch umbrella.** On the ContractorUK umbrella forum (1,070 topics, 12,493 posts), the live threads
are *"Communication from agencies around JSL"*, *"Forced to change Umbrella. Views on Giant and
Paystream"*, *"Asked to change umbrella mid contract and payment withholding"*, *"Didn't get paid
today"*, *"Umbrella and wrong tax code"*, *"FCSA investigating one of its members"*. **No thread
addresses reconciliation of agency rate to payslip to RTI.**

And the JSL thread reveals what agencies are *actually doing* about April 2026:

> "due to the upcoming legislation changes, we can only work with compliant umbrella providers and
> therefore have decided to restrict our umbrella PSL to the following FCSA members"

**That is the competing product, and it costs the agency nothing.** Shrinking the PSL to accredited
members is faster, cheaper and more legally defensible than buying reconciliation software — and it
shrinks the very problem our product addresses. The second competing response is worse for us still:
HMRC's own policy paper confirms agencies may simply **operate PAYE themselves** — "Agencies
operating PAYE will withhold income tax and NICs before making payments to the umbrella company" —
in which case the agency holds all the data and needs no reconciliation product at all.

The complaints about the incumbent are also instructive. On SafeRec: *"What exactly is the point of
Saferec in the first place? Honest Payroll's accounts were overdue from August 2025 — what on earth
were Saferec doing over that time?"* and advice to ignore the accreditation and *"look at the company
accounts for the listed umbrellas… That's far more important."* Practitioners have already concluded
that a Companies House filing check beats a payslip audit. That is a brutal verdict on the category.

**S2 — the complaint is definitional, not operational.** Ofgem's own support page shows what it
fields: queries on "the registration process", "technical issues with the digital registration
service", "locating relevant Ofgem guidance", "the structure and purpose of authorisation
conditions" — while explicitly refusing "providing legal advice or confirming how legislation applies
to your specific circumstances". The pain is *"am I the operator or the supplier, and is this
building even a heat network?"* — Ofgem's who-should-register guidance turns on whether a building is
"divided into separate premises", with care homes out of scope. A housing association's first
question is not "how do I file the return", it is **"how many heat networks do I actually have, and
which of them am I the supplier of?"** If we build a reporting tool we will be answering the second
question for someone still stuck on the first. A scoping/classification product may be the better
wedge.

**S3 — the regulator has already conceded the complaint, in writing.** PackUK's 2025 recyclability
assessment requirements:

> "Producers have reported **significant concerns regarding the time and resource required** to meet
> their 2025 H1 recyclability assessment obligations"

— from "large producers across several sectors", and the four environmental regulators responded with
a **regulatory position statement effectively allowing producers to skip H1 2025 assessment data**.
The regulator looked at the workload, believed the complaint, and suspended the obligation for half a
year.

That is evidence class 4 (regulator's published position) confirming exactly the pain our product
addresses, in the regulator's own words, with a remedy that proves it was real. **It is the single
strongest piece of practitioner evidence across all three candidates** — and it is the only one where
the stated pain matches the product thesis rather than contradicting it.

---

## 7. Ranking on pure usability and adoption grounds

**1. S3 — Packaging EPR / RAM.** The only candidate where first value requires no new data, no
integration and no third party's consent. The input file already exists and the operator owns it.
The missing data is supplier attributes, and the regulator has converted every missing attribute into
a cash penalty, which makes the chase self-justifying. Annual RAM republication to 2030 makes the
workload recurring rather than a project. Real risk: the compliance schemes already hold the file and
already sell the service — this is an incumbency fight, not a data fight, which is the better fight
to be in.

**2. S2 — Heat network authorisation.** The obligation is real, the population is findable and the
quarterly cadence is permanent. But cycle 1 is data creation, not data assembly; the unbundled tariff
figures a bundled-service-charge landlord must report **do not exist anywhere and must be modelled**;
there is no integration target because Ofgem's own service is in private beta with bulk upload only
planned; and Ofgem has publicly committed to a light-touch first year, which removes the urgency that
drives a purchase. Viable, slow, services-heavy.

**3. S1 — Umbrella/agency PAYE assurance. Recommend removal from the shortlist on operator
grounds.** Four independent failures, any one sufficient:
- **No data.** The umbrella still runs PAYE and RTI; there is no statutory right to its records;
  HMRC's own guidance routes the agency to the *worker*, "where they have them".
- **No verification.** No HMRC API exposes another employer's remittance to a third party, and
  remittance is precisely what the agency is liable for. Practitioners have already worked this out
  in public.
- **No gap.** SafeRec already ships payslip audit, RTI cross-reference and monthly HMRC tax account
  checks — at **£149–£449/month**, an order of magnitude below the £10k ACV floor adopted in
  ADR-011 §1.
- **No demand.** The observed agency response to April 2026 is to restrict the PSL to FCSA members
  (free) or bring PAYE in-house (removes the problem entirely). Neither buys our product.

ADR-011 recorded S1 as passing the LAW 3 convergence check while warning that "both rest on one
instrument — Wave 2 must verify a buyer with budget exists, not merely that the liability exists."
The operator finding is worse than that: the liability exists, the buyer may exist, **but the input
data does not**, and the product cannot answer the question the buyer is liable for.

---

## 8. What I could not check (budget and access)

- **Reddit** — `reddit.com/search.json` returns 403 to this environment. No Reddit evidence.
- **LinkedIn** — not attempted; blocks unauthenticated fetch.
- **Switch2** — `switch2.co.uk` returns HTTP 202 to non-browser clients. Could not assess their
  regulation offering or APIs. This is a material gap for S2 incumbency.
- **Association for Decentralised Energy** — news page 404. No trade-body evidence for S2.
- **letsrecycle / packagingnews** — fetch returned a 2013 archive page, not current headlines. No
  trade-press evidence for S3; the regulator's own position statement substitutes and is stronger.
- **NEC, Civica, MRI** housing management API documentation — not reached.
- **Job postings** — still blocked as in Wave 1. **LAW 3 evidence class 1 remains absent for all three
  candidates.** No candidate should reach build without it.
- **Counts:** number of SafeRec-certified umbrellas (directory loads dynamically); number of heat
  networks registered to date (not published on the pages fetched).
- **Fees:** 2027-28 and 2028-29 modulation multipliers — only the 2026-27 red uplift (+20%) was found
  in primary source. ADR-011's 1.6×/2.0× figures are **not verified here**.
