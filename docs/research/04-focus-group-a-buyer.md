# 04 — Focus Group A: THE BUYER (government side)

**Author:** Focus Group Agent A — composite of a UK MOD commercial director under National Armaments Director reform, an offset/industrial-participation authority official (India DOMW, UAE Tawazun, Saudi GAMI, Canada ISED ITB), an NSPA procurement officer, and a national audit office director.
**Date:** 19 September 2026
**Standing instruction to the reader:** I am not your customer. I am the person who has to explain your invoice to a Public Accounts Committee. Every sentence below is written from that chair.

---

## 1. Verdict up front

Your two experts ranked offsets #1 from the *market's* chair. From the *buyer's* chair the ranking changes, and not in the direction you would like.

| Rank | Candidate | Buyer verdict | The one-line reason |
|---|---|---|---|
| **1** | **Offset / industrial participation — authority side only** | **Conditional buy** | It is the only candidate with **no incumbent to displace, no classified core, a live audit finding with my name on it, and a price tag small enough that I can sign it myself.** |
| **2** | **Inventory data-quality layer** | **Buy, but not from you yet** | Highest audit salience and already-funded, but I have a £6.7bn prime sitting on the problem and the data classification line is genuinely hard. |
| **3** | **Supplier compliance "readiness passport"** | **No-buy — I will mandate it, not fund it** | I make suppliers pay for their own compliance. And in aggregate your database is a targeting package. |
| **4** | **Multi-tier munitions capacity modelling** | **Want most, can buy least** | The data is industry's, the output is SECRET, and this is a study contract wearing a SaaS costume. |
| **5** | **FOCI / beneficial-ownership workflow** | **No-buy from government** | Not my budget line. It is a contractor compliance cost, the rule is not final, and in the US it is CUI — which your platform cannot legally hold today. |

**The single most important thing in this document:** your rank order is inverted by one fact you have not priced. *Offsets is not one product. It is two products with opposed interests.* Everything below turns on that.

---

## 2. Per-candidate buy/no-buy

### 2.1 Offset / industrial participation obligation management

**Would I buy?** As a *buyer-nation authority*: yes, conditionally. As a ministry buying it *for* my primes: never.

**Whose budget line.** In the UK, the National Armaments Director's office standing up the offsets regime — a new organisation with a new policy and therefore a genuinely new, unallocated line inside the £298bn four-year Defence Investment Plan ([DIP](https://assets.publishing.service.gov.uk/media/6a44e989167a99cf0018da38/The_Defence_Investment_Plan.pdf)). In Canada, ISED's ITB Branch, which has an explicit ministerial commitment to fix its measurement framework after the Auditor General ([ministerial statement, Dec 2024](https://www.canada.ca/en/innovation-science-economic-development/news/2024/12/ministerial-statement-in-response-to-the-auditor-general-of-canadas-report-on-the-industrial-and-technological-benefits-policy.html)). In Saudi Arabia, GAMI, which publishes a localisation number against a 2030 target and therefore has to defend it.

**Who signs.** This is the good news for you. At £60k–£150k a year on a G-Cloud 15 direct-award call-off, a Band B commercial officer with standing delegation signs it. No competition is required — G-Cloud is a direct-award framework. And most Cabinet Office digital and technology spend controls **ceased as a requirement from 1 April 2026** ([CDDO guidance](https://cddo.blog.gov.uk/2024/05/14/understanding-the-new-digital-and-technology-spend-controls/); confirmed cessation), removing a gate that would previously have added three months. Above roughly £500k I need a business case through an investment approvals committee and you have lost a year.

**What makes me say no.**
1. **The policy has not landed.** The DIS offset consultation closed 23 December 2025 and, as of today, the published consultation text still only gestures at *"monitoring mechanisms and enforcement measures to address underperformance"* and *"multipliers to drive investment to priority areas"* ([GOV.UK consultation](https://www.gov.uk/government/consultations/defence-industrial-strategy-dis-offset-written-consultation/defence-industrial-strategy-dis-offset-written-consultation)). It names no threshold, no administering body, no credit methodology. **I cannot buy a system of record for rules that do not exist.** If your data model assumes a credit-and-multiplier architecture and the UK lands on a contractual-commitment architecture instead, I have bought a migration.
2. **Several of my peers already have a portal.** India's DOMW runs an end-to-end web portal through which OEMs submit offset discharge claims against approved discharge schedules, DOMW processes them, and credits are assigned — plus offset proposals and Indian Offset Partner details ([DOMW](https://domw.gov.in/)). That is government-built, sovereign, and already sunk. You are not selling into India. You are selling into the countries that have not built one yet.
3. **Sovereignty.** India's MeitY empanelment requires that all data functions and processing occur within India with export of any data prohibited ([MeitY empanelment summary](https://www.esds.co.in/blog/why-meity-empanelment-is-key-to-sovereign-cloud-in-india/)). Your Cloudflare-only mandate has jurisdictional placement for `eu` and `fedramp`, per the team's platform note — it does not have an Indian or a Saudi boundary. For those markets you are structurally ineligible, not merely uncompetitive.

### 2.2 Supplier compliance "readiness passport"

**Would I buy?** No. I will *mandate* it and make someone else pay.

This is the oldest move in government commercial practice and you should expect it. MOD did not buy JOSCAR; it let Hellios charge suppliers **£725 + VAT a year** above £1m turnover. MOD did not buy Defence Cyber Certification; it appointed IASME as certification partner and suppliers pay certification bodies. If a central supplier evidence record is valuable, my first instinct is to require it in DEFCON terms and let the market fund it.

**Whose budget line if I did.** Defence Supplier Assurance / Defence Digital, as an extension of the Supplier Cyber Protection Service. **Who signs:** that is a departmental service, so £250k+ and a full business case — 9 to 18 months.

**What makes me say no.** Three things, in order. First, **displacement**: I already pay for Hellios JOSCAR, IASME's DCC network and Commerce Decisions AWARD as MOD's official procurement solutions partner. A fourth supplier-data system invites the obvious NAO question. Second, **aggregation risk** — see §4; a single database ranking thousands of UK defence suppliers by weakest cyber control posture is a targeting list, and I would have to classify it above the level your platform serves. Third, **timing**: DCC Level 0 is requested by 31 December 2026 and in the US the CMMC Reform Task Force reported to the Under Secretary in mid-September 2026 with recommendations that may rewrite the framework ([review timeline](https://www.gtlaw.com/en/insights/2026/7/dod-suspends-cmmc-deadlines-and-seeks-to-reassess-requirements)). Buying a compliance-evidence product in the month the compliance regime is being rewritten is how officials end up in front of a committee.

### 2.3 FOCI / beneficial-ownership workflow

**Would I buy?** No — and I want to be clear this is not a soft no.

The DFARS FOCI rule is still *proposed*. Comments closed 6 July 2026 and it remains at proposed stage today ([Federal Register](https://www.federalregister.gov/documents/2026/05/07/2026-09067/defense-federal-acquisition-regulation-supplement-mitigating-risks-related-to-foreign-ownership); [Holland & Knight](https://www.hklaw.com/en/insights/publications/2026/06/got-it-covered-expanded-foci-oversight-for-contractors)). It would expand DCSA's annual FOCI caseload from roughly 2,000 to an estimated 41,000 cases. **That is a US government capacity problem, and the US government solves it inside NBIS, not by buying a commercial SaaS.** On the industry side it is a contractor cost. Either way it is not my budget line, and the sponsoring department cannot legally put SF 328 beneficial-ownership content — CUI — on a platform without a DoD IL4 provisional authorisation, which Cloudflare has announced intent to pursue and does not hold.

### 2.4 Multi-tier munitions capacity modelling

**Would I buy?** I want this more than anything else on your list and I can buy it least.

The need is not in doubt. US missile procurement requested $70.5bn for FY27 against $24.4bn in FY26, with PAC-3 MSE going 357 → 3,203 rounds, and DoW is now signing multiyear framework agreements explicitly to grow PAC-3 MSE capacity from roughly 600 to 2,000 interceptors a year by 2030 and THAAD from 96 to 400 ([Hudson Institute on the Office of Industrial Base Growth](https://www.hudson.org/national-security-defense/new-initiatives-dows-office-industrial-base-growth-nadia-schadlow-michael-dressler)).

**Why I cannot buy it from you.** The input data — actual line rates, tooling constraints, energetics availability, named sub-tier chokepoints — is commercially proprietary to firms that will not give it to a startup, and once assembled the output is a map of how to stop Western munitions production with a small number of interventions. In the UK that output is SECRET. It never touches a commercial cloud. The realistic procurement is a government-sponsored industrial base assessment under a classified task order to a cleared body, which is how Avascent, RAND and the FFRDCs already get paid. **You would be bidding against an incumbent model of delivery, not an incumbent vendor.**

### 2.5 Inventory data-quality layer

**Would I buy?** Yes in principle, and this is the candidate with the most direct audit pressure on me: £11.8bn of inventory, 640,000 types, 740 million items, two 40-year-old core systems, 105,500m³ of central-warehouse stock not currently fit for use ([NAO](https://www.nao.org.uk/press-releases/defence-inventory-management/)).

**Whose budget line.** Defence Support / DE&S, as a work package inside the already-funded £2.5bn pan-defence inventory transformation programme. **Who signs:** the programme SRO, and realistically I would route it through the existing prime.

**What makes me say no.** The **£6.7bn Leidos LCST contract**, which already covers storage, distribution and procurement and inventory management of 70,000 commodity NSNs, and which has just been through a mid-life refresh delivering £272m of savings ([Leidos LCST](https://www.leidos.com/company/global/uk-europe/LCST)). My first question to you is the one I will be asked: *"why is this not in scope of a contract I am already paying £6.7bn for?"* You need an answer to that in one sentence, and the only answer that works is: **because the prime cannot mark its own homework on data quality, and I need the defect measurement in my hands, not theirs.**

---

## 3. What I am personally measured on

Be specific, so here are the metrics with my name against them:

- **UK commercial director:** SME spend rising from ~£5bn to £7.5bn, i.e. **+£2.5bn by May 2028** ([SME Action Plan](https://www.gov.uk/government/publications/mod-small-and-medium-sized-enterprise-sme-action-plan/ministry-of-defences-small-and-medium-sized-enterprise-sme-action-plan)) — against a baseline where only ~5% of direct procurement spend reached SMEs in 2024 and **75% of SME spend flows indirectly through primes, which I cannot see**. Also: contracting software within the Segmented Acquisition Model's **three-month** target.
- **Offset authority official:** discharge rate against obligation. India's PAC recorded **$4.48bn of $9.9bn (45%) unfulfilled at 31 December 2025**. GAMI publishes **24.89% localisation at end-2024 against a 50%-by-2030 target** ([GAMI](https://www.gami.gov.sa/en/news/gami-reports-localization-military-spending-saudi-arabia-increases-2489)). Canada's AG found **8 of 60 eligible >C$100M procurements had no ITB obligations at all** ([OAG Report 10](https://www.canada.ca/en/auditor-general/our-work/audit-reports/parl-oag-202412-10-e.html)).
- **Audit director:** number of open recommendations I can close this year.

**Which candidate maps to a metric I am scored on?** Offsets — directly, numerically, and publicly. The readiness passport maps to the SME target only *indirectly*. Inventory maps to an NAO recommendation. Munitions maps to a readiness metric I cannot yet measure. FOCI maps to nothing I own.

That is the honest answer to your question, and it is the strongest single argument for your #1 pick — **but only on the authority side.**

---

## 4. The two-sided question, answered honestly

**What do I need that a contractor-side tool would never give me?**

1. **An obligation register that is authoritative independently of the obligor.** Today the obligor keeps the master and sends me claims. Transparency International's verdict on the US model is that it *"effectively leaves defence firms to mark their own homework"* ([TI-Defence](https://ti-defence.org/blissfully-blind-security-risks-defence-contract-offset/)). I need the register to be mine.
2. **Cross-obligor aggregation.** The question I actually cannot answer is *"what is the total outstanding obligation against my nation, by year, by sector, by region, across all obligors?"* No contractor tool will ever show me that, because no contractor can see its competitors' obligations. This is the single function that only an authority-side product can perform, and it is the one my minister asks about.
3. **Credit-claim adjudication with a defensible audit trail** — evidence, multiplier justification, valuation basis, decision, appeal. India's CAG accepted only **48% of claimed discharge value**. The disputed 52% is where my legal exposure lives.
4. **Double-counting detection across obligors.** The same Indian or British subcontract placed by two primes, claimed twice. Only I can see that.
5. **Policy counterfactual.** Canada's AG said the benefits and full costs of ITB *"were unknown."* I need to be able to answer that, not deflect it.

**Is there a two-sided product?** Yes — and that is precisely the problem.

**Would I tolerate the vendor also serving the companies I regulate?** *Not without conditions I doubt you will accept, and in one configuration, not at all.*

The disqualifying configuration is this: you sell obligors a tool that helps them **optimise** discharge — find the cheapest qualifying transaction, maximise multiplier capture, structure claims for acceptance — while selling me the tool that **adjudicates** those claims. That is not a conflict I can mitigate. That is selling the exam and the revision guide. I would be excluded from buying it, and under the Procurement Act 2023 I would have to prepare and publish a conflicts assessment before I even issued a tender notice; where a conflict puts a supplier at unfair advantage and cannot be avoided, exclusion is **mandatory** ([Procurement Pathway guidance](https://www.procurementpathway.civilservice.gov.uk/documents/guidance/conflicts-of-interest); [Procurement Act 2023](https://www.legislation.gov.uk/ukpga/2023/54/contents)).

The tolerable configuration is narrower than you want: **you may supply the obligor with a submission portal and me with the register, provided you do not supply advice, optimisation, benchmarking or any derived analytics on either side.** Be the pipe, not the adviser. Concretely, I would require in the contract:

- a **prohibition on advisory, brokerage or optimisation services** to any obligor with a live obligation in my jurisdiction, for the term plus two years;
- **no cross-tenant derived product** — no benchmarks, no "market rates for multiplier capture", no aggregate insight sold back to industry from data I put in;
- **legally and technically separated tenancy**, evidenced by an independent **ISAE 3000 / SOC 2 Type II** report scoped specifically to tenant isolation and absence of cross-tenant data flow;
- **the authority holds the keys and the export right**, with full ledger export in an open schema on demand;
- **disclosure of every obligor customer** in my jurisdiction, in writing, within five working days of contract signature;
- **my right to audit, including code and configuration**, and step-in on breach.

Blunt commercial advice: if you build one product and sell it to both sides, you will win the industry side and lose every authority procurement that has a competent commercial lawyer. If you want the authority side — which is the side with the metric, the audit finding and the clean procurement — **treat the obligor product as a separate legal entity with separate staff, or do not build it at all.**

---

## 5. Where the classification line actually is

The team's routes-to-market note is right that UK **OFFICIAL-SENSITIVE is commercially reachable** and that G-Cloud Lot 1b (above OFFICIAL, £75m insurance) is a door you should not attempt. So the question is not "can you hold OFFICIAL-SENSITIVE" — it is "which fields in each candidate are above it."

| Candidate | Comfortable at OFFICIAL / OFFICIAL-SENSITIVE (IL2) | **Never in your cloud** |
|---|---|---|
| **Offsets** | Obligation value, ratio, milestone dates, credit claims, multipliers, evidence packs, counterparty names, adjudication decisions — all post-award and commercial-in-confidence | **Pre-announcement programme identity and forward buy intent.** A national offset pipeline is a forward order book: it tells a reader what we are buying, from whom, and when, years before announcement. Mitigation: anonymised programme IDs until award publication, and no linkage table in the system. |
| **Readiness passport** | An individual supplier's own certification status, held by that supplier and shared by consent | **The aggregate.** Thousands of suppliers ranked by weakest cyber posture is a prioritised target list for a hostile actor. Individually OFFICIAL, collectively above it. Mitigation: no cross-supplier ranking, no exportable "weakest 100", per-supplier consent-scoped disclosure only. |
| **FOCI** | Public-register-derived ownership graph (Companies House PSC, GLEIF) | **SF 328 content and DCSA mitigation correspondence.** In the US this is CUI → IL4 → not available on your platform today. |
| **Munitions capacity** | Published budget lines, announced capacity targets, open-source trade flows | **Everything that makes it useful:** actual rates, named chokepoints, single-point-of-failure sub-tiers, shortfall against requirement. UK SECRET. Do not design for this. |
| **Inventory DQ** | **Defect telemetry** — record counts, field completeness, duplicate rates, reconciliation variances, age of record, by system and by category | **Holdings.** Quantity and location by NSN — especially guided weapons and ammunition — is operationally sensitive and frequently above OFFICIAL. |

**The general rule I apply:** individual records are usually OFFICIAL-SENSITIVE; *the aggregate is what gets classified up.* Your architecture must be able to prove that the aggregate view does not exist outside my boundary. Design the schema so the sensitive join is impossible, not merely disabled.

---

## 6. Top three objections that would kill the procurement — and the evidence that overcomes each

**Objection 1 — "You will not exist in five years and my obligation runs for fifteen."**
Offset obligations run 10–15 years. Vendor failure mid-obligation means I lose the audit trail for a live legal exposure. This kills more govtech deals than price.
**Evidence that overcomes it:** source-code and data escrow with a named agent and a *tested* release, demonstrated in front of my team, not asserted in a PDF; full ledger export in an open, documented schema, on demand, including evidence binaries; a written commitment that the register is reconstructible from exports alone, proven in a rehearsal; financial standing evidence at the Gold Standard Financial Viability level; and contractual step-in rights. Show me a successful restore from export. That single demonstration is worth more than your entire deck.

**Objection 2 — "You also sell to the people I regulate."**
See §4. Unmitigated, this is a mandatory exclusion under the Procurement Act 2023, not a discussion.
**Evidence that overcomes it:** an ISAE 3000/SOC 2 Type II report scoped to tenant isolation and no cross-tenant derivation; separate legal entity and separate personnel for the obligor product; written disclosure of every obligor customer in my jurisdiction; a contractual bar on advisory/optimisation/benchmarking; my right to audit code and configuration. Anything less and my conflicts assessment cannot be signed.

**Objection 3 — "This becomes a permanent running cost and the NAO asks why I did not use what I already have."**
This is not hypothetical. MOD's own Defence Digital built a commercial audit tool to spot overpayments and then wrote off **£2.15m in constructive losses**, with the stated reason that *"maintaining the original tool would have involved ongoing running costs, it was decided that continuing to support it did not represent value for money"* ([PublicTechnology, 17 Sept 2026](https://www.publictechnology.net/2026/09/17/defence-and-security/mod-records-2m-loss-on-digital-tool-created-to-spot-overpayments/)). That is a fresh, named, quantified precedent that will be quoted at me.
**Evidence that overcomes it:** a quantified status-quo baseline in FTE days — how many person-days the annual offset return, the claim adjudication cycle and the ministerial question pack take today — and a five-year total cost of ownership against it; a G-Cloud call-off with short termination rather than a bespoke build, so exit is cheap; a benefits realisation plan my finance director will counter-sign; and a named comparator already running the same thing at a peer authority.

**Honourable mention — "Tell the prime to do it."** My instinct, and you should have an answer. Under the Single Source Contract Regulations a prime's compliance tooling is an overhead recovered through the Allowable Costs AAR test — so **I pay for it either way, just opaquely, and I do not get the data** ([SSRO guidance](https://www.ssro.gov.uk/allowable-costs-guidance-overheads-and-indirect-costs)). The counter-argument that works on me is exactly one sentence: *the regulated party cannot be the system of record for its own compliance.* That sentence is your whole sales pitch to government. Use it.

---

## 7. What I would actually sign tomorrow

Not the platform. Three small things, in this order.

1. **A 12-month, £60k–£150k G-Cloud 15 direct-award call-off for an authority-side offset/industrial-participation obligation register**, scoped explicitly to OFFICIAL-SENSITIVE, UK-hosted, anonymised programme identifiers, full export, escrow, and the §4 conflicts clauses. G-Cloud 15 was awarded 6 August 2026 with buyer access from mid-August, so the vehicle is live now and **direct award means no competition and no tender timetable.** If you are not listed on G-Cloud 15, you have just lost roughly eighteen months, because it does not reopen to new suppliers until then.

2. **A subscription to a date-versioned global offset and local-content rules register** — every regime (GAMI/LCGPA, Tawazun, DAP 2020, SSB, DAPA, ITB, AIC, the Polish Offset Act, Greece's 25% guideline, and the UK regime when it lands), snapshotted daily, diffed, with the change history retained. This is unclassified, has no conflict-of-interest problem, needs no integration with my systems, costs me almost nothing to trial, and is **impossible to backfill** — a competitor starting in 2028 cannot reconstruct 2026. I would buy this today from a vendor I had never met. It is also the cheapest thing on your roadmap to build.

3. **A four-week paid discovery on inventory defect telemetry** with Defence Support, reading metadata only — record counts, completeness, duplicates, reconciliation variances — and never holdings. If it produces a defect league table my Chief of Materiel had not seen, I will find the money inside the transformation programme.

**What I would not sign at any price tomorrow:** the munitions capacity model, the FOCI workflow, or anything that puts an aggregate ranking of my supplier base on a commercial platform.

**Final word.** Your experts picked offsets for the right reason and the wrong buyer. The money on the obligor side is larger and faster; the *defensibility* is on the authority side. If you take both, you will get neither — because the day I discover you sell to my obligors, my conflicts assessment fails, and I am required to exclude you.
