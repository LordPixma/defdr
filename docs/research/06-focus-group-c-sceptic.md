# Focus Group C — The Sceptic / Red Team

**Author:** Focus Group Agent C (Sceptic / Red Team)
**Date:** 19 September 2026
**Scope:** **UK market only** (re-scoped mid-task by the Orchestrator; every test below is UK-scoped)
**Method:** 24 independent web searches, 11 page fetches. No claim from `01`/`02`/`03` accepted
without re-verification against a primary or near-primary source. Unverified items are flagged.

---

## 1. KILL-LIST VERDICT (read this first)

| # | Candidate | UK verdict | One-line reason |
|---|---|---|---|
| 1 | **Offset / industrial participation management** | **KILL** | The UK regime does not exist. The consultation is still "awaiting outcome" nine months after closing and has already missed its own H1-2026 implementation target. UK buyer count ≈ **8–15**. |
| 2 | **Supplier compliance "readiness passport"** | **KILL AS FRAMED — SURVIVES INVERTED** | JOSCAR already is the UK supplier passport (30+ buyers, 6,000+ suppliers, MOD is a buyer member). The passport is taken. The *prime-side flow-down assurance workflow* is not. |
| 3 | **FOCI / beneficial-ownership workflow** | **KILL (out of scope)** | FOCI is a US DFARS construct whose system of record is DCSA's NISS. Under UK-only scope it has no forcing function and no buyer. |
| 4 | **Multi-tier munitions capacity modelling** | **WOUNDED — not year one** | ~25–35 UK buyers, and the only one with the cross-industry view is the MOD. Violates selection criterion 1. Data acquisition is the product and we do not have it. |
| 5 | **Inventory data-quality layer** | **KILL** | Exactly one UK buyer (MOD), already spending £2.5bn (BMfS) and £1.8bn (FDSS) on the same problem, and the data lives inside MODCloud where a Cloudflare-only product cannot go. |

**Nothing on the shortlist passes all five selection criteria as written.** One candidate passes if it
is inverted. That is my finding, and I am not going to soften it.

---

## 2. THE CONVERGENCE TRAP — Conflict 3 adjudicated

**Verdict: shared evidence bias, not triangulation.**

Two agents independently ranking offsets #1 looks like triangulation. It is not, and the proof is in
their own citation lists. Both cite **Freshfields** and **Pillsbury** client alerts on the *same*
consultation. Both cite **PwC India's** offset tool page. Both cite the **$371bn / $229bn** industry
figures. Both conclude "no category-defining SaaS incumbent."

That is one evidence cluster, not two. The UK MOD's 23 October 2025 consultation triggered a wave of
near-identical law-firm client alerts in October–November 2025, and those alerts now dominate every
search result for "UK defence offsets." Two agents querying similar terms landed in the same SEO
stratum and mistook an echo for a second voice.

Genuine triangulation would require **independent evidence classes**: a buyer interview, a job
posting for a UK offsets role, a procurement record of anyone buying offset software, a competitor's
ARR. None of the three research documents contains any of these. I searched for UK offset-manager job
postings and found none at BAE, Babcock or Rolls-Royce — the only live posting I surfaced was a
**Northrop Grumman** "International Industrial Engagement and Offset Manager" role, i.e. American.

Three further traps specific to offsets:

- **The vanity-metric error.** Both agents quote obligation dollars ($371bn, $142bn, $251bn) as if
  they indicated software spend. The **BIS 28th Study** records **1,304 offset agreements across 51
  countries over 30 years** — ~43 a year from the entire US industry. BIS's historical series shows
  **48 US firms total** reported agreements across 1993–2008, and in 2004 just **fourteen prime
  contractors** reported any. This is not a market. It is a guild.
- **"No incumbent" is being read backwards.** Forty years of the discipline and $142bn of agreements
  have produced no category winner. The null hypothesis is that **the category does not support a
  software company** — not that nobody noticed. Generic contract-obligation management (Icertis,
  Conga, Agiloft, Aavenir Obligationflow) plus a Big-4 bespoke build already absorbs the demand.
  Neither agent tested that.
- **The direction of travel is against offsets.** The Commission's Guidance Note under **Directive
  2009/81/EC** holds that offsets "violate basic rules and principles of primary EU law" — the EU-27
  is largely closed. **Poland abolished indirect offsets.** **India** — the enforcement case study
  both agents used — has signed **no new offset contract in five years** (one materialised Mar 2021–
  Mar 2025) and the **draft DAP 2026** (10 Feb 2026) omits offsets from Volume 1, replacing them with
  indigenous content written into the contract. The world is moving from *offsets* to *embedded local
  content*: a different product, a different buyer.

---

## 3. TRUE UK BUYER COUNTS (method shown)

**Method:** count organisations, not obligations. For each candidate I identify the specific role that
holds the budget, then count UK organisations plausibly employing that role at a scale that justifies
software rather than a spreadsheet. I then discount for (a) foreign-parented firms whose tooling
decision sits abroad, (b) organisations already served by an incumbent.

| Candidate | Budget-holding role | UK organisations | Winnable subset | ACV needed for £3m ARR | Verdict vs ~50 threshold |
|---|---|---|---|---|---|
| **Offsets** | Head of Offsets / Industrial Participation | **8–15** (BAE, Rolls-Royce, Babcock, Thales UK, Leonardo UK, MBDA UK, QinetiQ, Chemring, Ultra/Cobham, Martin-Baker, Marshall, NP Aerospace + the NAD's offsets office) | **4–6** — the foreign-parented ones (Thales, Leonardo, MBDA) buy at group level | **£500k–750k each** | **FATAL.** Not survivable at any credible ACV |
| **Readiness passport (supplier-side)** | SME MD / IT manager | **16,000+** MOD suppliers | ~10,000 not already on JOSCAR | £300/yr | Count is fine; **incumbency kills it** |
| **Flow-down assurance (prime-side)** | Prime supplier-assurance / SCRM lead | **100–200** (primes, tier-1s, framework holders, the ~40 JOSCAR buyer orgs plus non-members) | **60–120** | £25k–50k | **Only candidate that clears the threshold with a non-ministry buyer** |
| **FOCI / beneficial ownership** | Contracts/legal lead, FSO | **~0 UK-specific.** UK analogue is NSI Act notification — episodic, law-firm-owned | negligible | n/a | **FATAL under UK scope** |
| **Munitions capacity modelling** | Munitions programme / industrial base lead | **~25–35** (MOD/DE&S munitions & energetics teams + the **22 firms contracted on 29 July 2026** to study factory sites + BAE, RBSL, Chemring, MBDA, Thales UK) | 10–20 | £150k–300k | **Under threshold.** Survivable at high ACV *only* with MOD as anchor — which breaks criterion 1 |
| **Inventory data quality** | Chief of Materiel / Defence Support | **1** (MOD), plus Team Leidos and 2–3 programme offices | 1 | £1m+ | **FATAL.** One-customer company |

The honest reading: under UK-only scope, **offsets has roughly one twentieth the buyer count of the
weakest respectable SaaS market**, and the inventory play has one buyer. A buyer count of 8–15 is not
"small but high-ACV" — it is a consultancy, staffed by people who already know all fifteen buyers.

---

## 4. FORCING-FUNCTION VERIFICATION TABLE

I verified each independently. **The most important row is the first one.**

| Claim | Real? | Date | Legal status as of 19 Sep 2026 | Source |
|---|---|---|---|---|
| **UK "Back British" offsets regime** | **NO — consultation only** | Published 23 Oct 2025; closed 23 Dec 2025 | **"Closed consultation — awaiting outcome."** GOV.UK still shows *"We are analysing your feedback… Visit this page again soon to download the outcome."* **No government response, no policy, no instrument, nine months after closing.** The stated implementation target ("first half of 2026", NAD Rupert Pearce) has **already been missed.** | [GOV.UK consultation](https://www.gov.uk/government/consultations/defence-industrial-strategy-dis-offset-written-consultation) |
| Defence Investment Plan restates offsets intent | Partially | 30 June 2026 | DIP says the UK will introduce an offsets regime **"subject to consultation"** — a restatement of intent, not a commitment. Pollard "reconfirmed interest" at DPRTE on 25 Mar 2026. | [DIP](https://assets.publishing.service.gov.uk/media/6a44e989167a99cf0018da38/The_Defence_Investment_Plan.pdf) |
| **DCC Level 0 for all MOD suppliers by 31/12/2026** | **Real but REQUESTED, not mandated** | Statement 8 May 2026 | Eleanor Fairford (MOD Director Cyber Defence & Risk): *"I have also recently asked all industry partners to achieve Level 0 DCC certification by 31st December 2026."* The **scheme is voluntary** and IASME's own FAQ still states DCC is **not currently mandatory**. | [Defence Digital blog](https://defencedigital.blog.gov.uk/2026/05/08/one-year-of-defence-cyber-certification-building-stronger-cyber-resilience-together/) |
| **DEFCON 658 / Def Stan 05-138 Iss 4 / CSM v4** | **Real and contractually binding** | Mandatory on all new **and existing** MOD contracts containing DEFCON 658 since **3 Dec 2025**; **ISN 2026/02 (30 Mar 2026)** confirms DCC as the recognised evidence pathway, mapped to each contract's Cyber Risk Profile | **This — not the Level 0 "ask" — is the real UK forcing function.** It binds primes to risk-assess every subcontractor and flow obligations down. | [Fig](https://www.figgroup.co.uk/blog/mod-ciso-dcc-level-0-mandatory-2026); [Logiq](https://www.logiq.co.uk/insights/defcon-658-cyber-obligations/) |
| **Segmented Acquisition Model, 3-month software lane** | **Real, live** | April 2026 | Process reform, not statute. A **target**, against a prior average of 6.5 years to award >£20m contracts. No enforcement mechanism; no published evidence yet of a 3-month award. | [Gowling](https://gowlingwlg.com/en/insights-resources/articles/2026/uk-defence-investment-plan-2026); [UKDJ](https://ukdefencejournal.org.uk/defence-shifts-to-10-year-plan-and-new-procurement-model/) |
| **DIP £298bn / £4.7bn unfunded** | **Real, and worse than reported** | Published 30 June 2026, one year late | £15bn headline ≈ **£11.6bn new cash + £3.4bn reclassified**; **£4.7bn unfunded**, including **£1.8bn needed next financial year**, pending Budget 2026. Military advice asked for ~£28bn. | [Calibre Defence](https://www.calibredefence.co.uk/confirmed-but-not-funded-defence-investment-plan-lands-a-year-late-with-a-4-7-billion-gap-attached/); [Commons Library CBP-10935](https://commonslibrary.parliament.uk/research-briefings/cbp-10935/) |
| **DFARS FOCI, 37,000 entities** | Real proposed rule (**37,740**) | Published 7 May 2026; comments closed 6 Jul 2026 | **Proposed rule only.** DFARS Case **2021-D011** implements **§847 FY2020 NDAA** and **§819 FY2021 NDAA** — statutes from Dec 2019 and Jan 2021. **Six-plus years from statute to proposed rule.** Out of UK scope regardless. | [Federal Register](https://www.federalregister.gov/documents/2026/05/07/2026-09067/defense-federal-acquisition-regulation-supplement-mitigating-risks-related-to-foreign-ownership) |
| **NDAA §805 indirect ban, 30 Jun 2027** | Dates real; **effect overstated** | Direct 30 Jun 2026; indirect 30 Jun 2027 | Statutory — **but the indirect prohibition expressly does not apply to "components"**, defined broadly as an item supplied as part of an end item or another component. That carve-out removes most of its force as an N-tier mandate. **US-only.** | [Crowell / GovCon Legal Forum](https://www.governmentcontractslegalforum.com/2025/01/articles/supply-chain/new-year-updated-list-the-u-s-department-of-defense-updates-its-list-of-chinese-military-companies-with-ancillary-supply-chain-and-usg-contracting-impacts/) |
| **CMMC** | **In flux** | Phase 2 suspended 13 Jul 2026; Reform Task Force reported to the DoW CIO ~mid-Sept 2026 | 1,100 responses / 10,000+ pages ingested. A task-force report **changes nothing on its own** — only a class deviation, a DFARS change or an amendment to 32 CFR 170 does. US-only. | [DefenseScoop](https://defensescoop.com/2026/07/17/pentagon-task-force-to-review-cmmc-hits-the-ground-running/) |

**Net:** of the four forcing functions the team is relying on, **one** (DEFCON 658 / Def Stan 05-138
Iss 4 / CSM v4) is real, dated, binding and UK. One (DCC L0) is a dated request riding on that
contractual hook. Two are out of UK scope. **And the one the whole offsets thesis rests on does not
exist.**

---

## 5. THE JOSCAR KILL TEST

**Question: does JOSCAR/Hellios already solve the UK supplier readiness passport? Answer: yes, as framed.**

JOSCAR is a **shared supplier-assurance register** with, per Hellios, **30+ buyers and 6,000+
suppliers in the UK community**, plus an Australian instance. **The MOD is itself a buyer member.**
Its explicit pitch is the exact pitch in candidate 3: *"a supplier only needs to fill in the JOSCAR
questionnaire once, even if it supplies multiple defence primes."* Supplier cost is £725+VAT/yr above
£1m turnover, **free below it**. Exostar holds a separate multi-decade MOD supplier-collaboration
contract. Risk Ledger sells a reusable supplier profile on a network model. Achilles shipped a
supplier remediation module on 16 September 2026 — three days ago.

So the "one evidence graph per supplier, reused across primes" concept is **occupied by four funded
vendors, one of which counts the MOD as a customer and is free for the SME segment we were going to
target.** Worse, selection criterion 4 forbids us depending on JOSCAR data — so we cannot even
interoperate with the incumbent we would be displacing.

**What JOSCAR does not do** — the entire residual opportunity — is run the **DEFCON 658 → contract
Cyber Risk Profile → required DCC level → subcontractor gap → chase → evidence pack** workflow that
ISN 2026/02 obliges primes to perform across tiers 2–n. It collects declarations. A prime today has a
register (JOSCAR), a standard (Def Stan 05-138 Iss 4), a deadline (31 Dec 2026) and no workflow
between them. That gap is real but small, and dozens of IASME certification bodies and consultancies
(Fig, Periculo, Vincent, Pera Prometheus, CyberSmart, Logiq, RightCue) are already selling into it —
nine appeared on page one of a single search. A product started now ships **after** the December rush.

**Verdict: candidate 3 dies as a supplier-side passport. It survives only inverted — sold to the
prime who must chase, not the supplier who must comply.**

---

## 6. CONFLICT 1 ADJUDICATED — N-tier visibility under UK-only scope

**Both experts lose, for different reasons, and the conflict dissolves.**

The Procurement Expert's case rests entirely on **NDAA §805**, a US statute — and I have shown its
indirect limb carves out components, which is most of the sub-tier. The Sector Expert's case rests on
**SCRIPTS**, a $919m **US federal** vehicle. Under UK-only scope **both instruments are irrelevant**.

Is there a UK substitute? Partially, and narrower than either agent assumed:

- **Yes, for cyber.** DEFCON 658 + Def Stan 05-138 Iss 4 + CSM v4 require primes to risk-assess *every*
  subcontractor and flow obligations down — binding since 3 December 2025. A genuine, dated,
  contractual UK sub-tier obligation.
- **No, for ownership or country-of-origin.** The UK has **no analogue of §1260H or §805**. Its
  instruments are the **NSI Act 2021** (transaction-triggered, episodic, law-firm-owned) and sanctions.
  There is no UK supply-chain content ban to build against.
- **Weakly, for SME spend.** MOD must measure indirect SME spend through primes (£5bn → £7.5bn by
  2028) — real, but the buyer is a ministry.

**Adjudication: the N-tier *illumination* thesis was US-dependent and does not survive UK-only scope.
The N-tier *cyber assurance flow-down* thesis does, and it is the same thing as the inverted
candidate 3.** That is the one place where the two experts' evidence actually converges on something
UK-real.

---

## 7. CLOUDFLARE-CONSTRAINT HARM ANALYSIS (UK buyers only)

IL4 is now irrelevant, which removes the largest theoretical harm. Three real ones remain, and one of
them is not in the platform document.

**Harm A — there is no `uk` jurisdiction.** Cloudflare's R2 and D1 jurisdictional options are `eu`
and `fedramp`. **Post-Brexit, `eu` is not UK data residency.** Durable Object placement is driven by
*location hints* (`weur`), which are hints, not guarantees. UK buyers at OFFICIAL-SENSITIVE ask for
contractual UK residency; "Western Europe, probably" will not clear a Secure by Design review without
Regional Services and the Data Localisation Suite configured and evidenced. This is a specific,
checkable gap that `00-cloudflare-platform-constraints.md` does not flag. **Verify before any
customer claim.**

**Harm B — CLOUD Act exposure.** Cloudflare is US-owned, so UK-hosted data remains reachable under the
US CLOUD Act. UK public-sector buyers increasingly ask for that exposure to be eliminated for
sensitive workloads; the MOD's £400m Google Distributed Cloud air-gapped deal shows the appetite is
real at the top end. At OFFICIAL this is survivable; at OFFICIAL-SENSITIVE it is an objection to
answer in every deal.

**Harm C — Workers egress 403s.** Verified by our own webscraper against war.gov, dla.mil, usgs.gov,
tenders.gov.au, NSPA and NCIA. Harms data-ingestion-heavy products; harmless where data comes from
the customer.

| Candidate | Cloudflare harm (UK) | Why |
|---|---|---|
| **Flow-down assurance (inverted C3)** | **LOWEST** | Data is supplied by the prime and its suppliers. No external scraping. OFFICIAL at most. Per-seat pricing matches the Kahootz £3.69–£11.69/user/month anchor. **Harm A manageable, B answerable, C irrelevant.** |
| Offsets | Low–medium | Customer-supplied data, but offset agreements carry export-controlled technology-transfer detail; sovereignty objections will be sharp for a tiny buyer set |
| Munitions capacity modelling | **HIGH** | Industrial-base data at OFFICIAL-SENSITIVE+; buyer will want MODCloud or on-prem; needs external ingestion (Harm C) |
| FOCI | High | System of record is DCSA's NISS, a US government system we cannot write to |
| **Inventory data quality** | **HIGHEST — disqualifying** | The data lives beside MJDI/SAP/Leidos inside MOD networks. A Cloudflare-only product **cannot be deployed there at all.** |

**Least harmed, and it is not close: the inverted candidate 3.** That matters enormously for the pick.

---

## 8. THE DATA-MOAT CHALLENGE — is the webscraper's Join 1 novel?

**No. It is Govini Ark Supply Chain and Exiger, feature for feature.**

- **Govini Ark (Supply Chain)** — *"maps foreign ownership risks and generates vendor due diligence
  reports… evaluating foreign influence, geographic risk, supplier financial health"* across contract
  portfolios. On the $919m SCRIPTS BPA **and** a five-year Army IDIQ; reported **~$150k/seat/yr**,
  **>$100m ARR**. Award data joined to ownership joined to risk. Exactly Join 1.
- **Sayari** — **1.5bn+ entities, 250+ jurisdictions, 11.7bn+ primary-source records, 4bn trade
  transactions**; markets ownership-to-sanctions traversal explicitly (*"one Tier-2 supplier… shares
  three officers with a sanctioned entity added to OFAC SDN Q3 2024"*); customers include US CBP and
  Treasury. Pricing quote-only.
- **Exiger** — SCRIPTS BPA; government and enterprise transshipment and SCRM.
- **Kharon** — sanctions and ownership intelligence; runs dedicated briefings for government
  contractors on 1260H obligations. Quote-only.
- **Altana** — multi-tier supplier mapping. Quote-only.
- Price comparator for the screening layer: **Descartes Visual Compliance ≈ $3,000/user/yr rising to
  $100,000+/yr**, ~$20k/yr for ~50,000 entities.

The **only** genuinely unoccupied element in the webscraper's analysis is **Join 2** — point-in-time
regulatory reconstruction from the eCFR Versioner API, diffed daily. That is real and genuinely
compounding. **It is a feature, not a company**, and under UK-only scope it has no UK buyer (the
eCFR is US law). Keep the daily snapshot cron running — it costs nothing — but do not build a
business on it.

---

## 9. THE "WHY NOW" TEST

| Candidate | Why hasn't it been built? | Honest answer |
|---|---|---|
| Offsets | It has been, repeatedly, and quietly: PwC India's web tool, Eurostep ShareAspace, Rheinmetall's in-house function, and generic CLM obligation modules (Icertis, Conga, Agiloft, Aavenir). None scaled. | **The market is too small.** ~14 US primes report in a typical year; 8–15 UK organisations. Forty years, no winner. |
| Readiness passport | **It has been built — well.** JOSCAR (30+ buyers, 6,000+ suppliers, MOD as member, free under £1m turnover), Exostar, Risk Ledger, Achilles. | **Taken.** Only the prime-side workflow layer is open. |
| FOCI | Because the rule is still proposed after six years, and the filing destination is a closed government system. | **Not yet real, and the system of record is not ours to own.** |
| Munitions capacity | Because the input data sits with sub-tier energetics firms who will not share it without government compulsion. | **Data acquisition is the product, and we cannot get it** without MOD sponsorship. |
| Inventory DQ | Because the MOD is doing it itself: **£2.5bn BMfS** (~65,000 users), **£1.8bn FDSS** replacing LCST in 2028, plus a **£350m deal being prepared in September 2026** to upgrade legacy weapons-management systems. | **One buyer, already spending £4.3bn+ on it, behind a network boundary we cannot reach.** |

---

## 10. TEST AGAINST THE FIVE SELECTION CRITERIA

| Criterion | Offsets | Passport (as framed) | **Flow-down (inverted)** | FOCI | Munitions | Inventory |
|---|---|---|---|---|---|---|
| 1. Non-ministry year-one buyer | ✗ (NAD office) | ✓ | **✓ prime** | ✗ | ✗ (MOD) | ✗ (MOD) |
| 2. Survives without IL4 | ✓ | ✓ | **✓** | ✗ | ✓ | ✓ |
| 3. Not incumbent-locked | ✓ | ✗ (JOSCAR) | **✓** | ✓ | ✓ | ✗ (BMfS/FDSS) |
| 4. Data obtainable, no JOSCAR/NMCRL/GIDEP/NC | ✓ | ✗ | **✓ customer-supplied** | ✗ (NISS) | ✗ | ✗ |
| 5. Survives Focus Group C | ✗ | ✗ | **✓ conditionally** | ✗ | ✗ | ✗ |

---

## 11. RECOMMENDATION AND WARNING

### The one candidate most likely to reach paying customers

**Candidate 3, inverted: DEFCON 658 / Def Stan 05-138 Issue 4 sub-tier flow-down assurance, sold to
UK primes — not a supplier passport.**

It is the only candidate that clears all five criteria. The buyer is a **prime**, which satisfies the
criterion the Orchestrator already ruled on. The obligation is **contractual and dated**, not
consultative: CSM v4 mandatory on DEFCON 658 contracts since 3 December 2025, ISN 2026/02 of 30 March
2026 mapping DCC levels to contract Cyber Risk Profiles, and a 31 December 2026 Level 0 ask sitting
on top. The data is supplied by the customer, so no licence and no egress problem. Cloudflare harm is
the lowest of any candidate. UK buyer count is **100–200**, the only shortlist entry above the
50-buyer threshold with a commercial buyer. Price it at £25k–50k per prime against the £4–£12/user/
month Kahootz anchor, and £3m ARR needs 60–120 logos rather than five impossible ones.

**Conditions I attach:** do not sell it as a passport or a register — JOSCAR owns that word and the
MOD is its customer. Sell the *chase*: which of my 400 subcontractors need which DCC level under
which contract's Cyber Risk Profile, who is non-compliant, and what is the evidence pack. And accept
that the 31 December 2026 rush is already lost; build for the **annual recertification cycle from
2027**, which is where the recurring revenue actually is.

### The one candidate most likely to waste two years

**Offsets — and it is the one two experts ranked first.**

The regime it depends on **does not exist**. GOV.UK still shows the consultation as "awaiting
outcome" nine months after it closed, the National Armaments Director's own H1-2026 implementation
target has passed with nothing published, and the Defence Investment Plan describes the regime as
"subject to consultation." The UK buyer count is **8–15**, and a UK "Back British" regime obligates
**foreign** contractors whose offset functions and tooling budgets sit in Bethesda and Düsseldorf,
not Bristol. The wider market is contracting, not growing: the EU Commission holds offsets to violate
primary EU law, Poland abolished indirect offsets, and India — the enforcement case study both agents
cited — has signed no new offset contract in five years and omitted offsets from draft DAP 2026.

Two years spent building offset software would end with a working product, a slipped or abandoned UK
regime, and a total addressable buyer list you could fit on one page. **The convergence was not
triangulation. It was two agents reading the same three law-firm blog posts about a consultation that
has not landed.**

### My single strongest warning

**Stop treating regulatory *intent* as a forcing function.** Of the four instruments this team has
been building theses on, one is real, dated and binding in the UK (DEFCON 658 / Def Stan 05-138
Issue 4 / CSM v4); one is a request from an official (DCC Level 0); one is a proposed US rule six
years from statute and still not final (DFARS FOCI); and one is a consultation with no published
outcome and a missed implementation date (UK offsets). **Build only against the first kind.** The
test is not "has a minister said it" — it is "is there a contract clause, with a date, that a buyer
is already in breach of." Only one of our candidates passes that test, and it is not the one that
came first.

---

### Items I could not verify

- **Cloudflare service-level FedRAMP scope** — no public itemisation of Workers/Durable Objects in the
  authorisation. Do not claim inheritance. Check the FedRAMP Marketplace entry directly.
- **Absence of a `uk` R2/D1 jurisdiction** — inferred from published `eu`/`fedramp` options; confirm
  with Cloudflare before any UK residency commitment.
- **GOCA/GICA membership count** — DNS resolution failed for globaloffset.org; my 8–15 UK offset buyer
  estimate is built from named UK exporters, not from a membership roll.
- **JOSCAR module coverage** — Hellios does not publish which compliance domains JOSCAR assesses. My
  "declarations, not workflow" claim is inference from their public marketing and should be confirmed
  with a supplier who holds a JOSCAR record.
- **Whether any UK prime currently buys flow-down assurance software** — I found no evidence either
  way. This is the single highest-value validation call to make before writing code.
