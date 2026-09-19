# UK Sector Sweep — Financial Services & Professional Services

**Agent:** UK Sector Analyst — Financial Services & Professional Services
**Date:** 19 September 2026
**Method:** `docs/method/01-opportunity-scoring-rubric.md` (binding). All five laws applied.
**Searches:** 27 web searches, 40+ fetches. Unverifiable claims tagged `[UNVERIFIED]`.

---

## Executive summary — top 5 candidates ranked

1. **Labour-supply-chain PAYE assurance for recruitment agencies** (score **31**). Since 6 April 2026 the *agency*, not the umbrella company, is responsible for operating PAYE, and HMRC can recover underpayments from it. HMRC counts ~30,000 agencies using ~400 umbrellas across ~700,000 workers. Nothing reconciles what the umbrella actually paid and remitted against what the agency funded.
2. **Legal AML evidence spine — source-of-funds ↔ client-ledger reconciliation and Regulation 21 audit pack** (score **29**). The SRA found 32.4% of inspected firms non-compliant, only 48% had done a Regulation 21 independent audit, and **8% of files showed a mismatch between the documented source of funds and the client ledger**. The onboarding vendors hold the ID; the practice-management vendors hold the ledger; nobody joins them.
3. **FCA material third-party register and operational incident reporting readiness (PS26/2)** (score **26**). Final rules published 18 March 2026, in force 18 March 2027 — a genuinely dated, enacted obligation. Downgraded on willingness to pay: the FCA's own cost-benefit analysis puts *ongoing* annual cost across the entire in-scope population at £0.04m–£0.12m.
4. **Consumer Duty annual board-report evidence pack for small FCA firms** (score **25**). Binding since 31 July 2023; FCA reviewed 180 firms including 55 with under 10 employees and found data quality insufficient to support the conclusions drawn. Crowded advisory market.
5. **Professional-services consolidator control plane** (score **24**). PE roll-ups now hold over a quarter of the UK Top 75 accountancy firms; the FCA's October 2025 multi-firm review found consolidators "did not scale systems and controls in line with their growth". Fails LAW 2 on raw buyer count (~60–120 groups) and needs an explicit ACV case.

**The single most important kill:** *ongoing-advice-service evidencing for IFAs*, the obvious-looking Consumer Duty adjacency. The FCA's February 2025 multi-firm review found suitability reviews were delivered in **~83%** of cases with a further 15% declined or unanswered, concluded there is **no systemic issue**, and is now consulting on **dropping the annual review requirement altogether**. Building on it would have been building on a regulator's retreat.

---

## Sector structure

| Sub-sector | UK count | Employment / scale | Key regulator | Source |
|---|---|---|---|---|
| Law firms (England & Wales) | **8,923** firms (Aug 2026); 9,149 authorised bodies on the AML basis | 179,054 practising solicitors (Aug 2026); 214,773 on the roll | SRA | [SRA regulated population statistics](https://www.sra.org.uk/sra/research-publications/regulated-community-statistics/data/solicitor_firms/) |
| Law firms in scope of the Money Laundering Regulations | **5,569** (≈ two-thirds of authorised firms) | 5,873 files reviewed by SRA inspectors in 2024-25 | SRA / OPBAS | [SRA AML Annual Report 2024-25](https://www.sra.org.uk/sra/research-publications/aml-annual-report-2024-25/) |
| Accountancy profession | **3,760** statutory audit firms (2024, down 24.9% in five years) | 408,000 members UK & ROI; ~9,600 approved training offices | FRC / ICAEW / ACCA (RSBs) | [FRC Key Facts & Trends 2025, 15 Oct 2025](https://www.frc.org.uk/library/supervision/professional-bodies-supervision/key-facts-and-trends-in-the-accountancy-profession/key-facts-and-trends-in-the-accountancy-profession-2025/) |
| Financial advice firms | **4,294** firms (2025, down from 4,340) | 26,435 advisers; 37,517 retail investment adviser posts; £6.5bn intermediation revenue | FCA | [FCA retail intermediary market data 2025](https://www.fca.org.uk/data/retail-intermediary-market-data-2025) |
| Mortgage and insurance intermediaries | ~**12,000** firms complete at least one RMAR element | 32,990 mortgage adviser posts; £27.7bn non-investment insurance distribution revenue | FCA | FCA RMAR 2025 (as above) |
| Recruitment agencies using umbrella companies | ~**30,000** agencies; ~**400** umbrella companies | ~700,000 workers paid through umbrellas | HMRC / EAS | [HMRC umbrella company market policy paper](https://www.gov.uk/government/publications/paye-changes-for-the-umbrella-company-market/umbrella-company-market-changes-to-income-tax-rules-to-tackle-non-compliance) |
| Professional, scientific & technical activities (SIC M) | **819,000** SMEs = 14% of the SME population | 11% of SME turnover | — | [DBT Business Population Estimates 2025](https://www.gov.uk/government/statistics/business-population-estimates-2025/business-population-estimates-for-the-uk-and-regions-2025-statistical-release) |
| All UK private-sector businesses | **5,690,265** (start of 2025); 1.4m with employees | 28.1m private-sector employment | — | DBT BPE 2025 (as above) |

**Correction to the brief.** The brief assumed "~10,000 UK law firms and ~40,000 accountancy practices". The first is high: the SRA regulates **8,923** firms. The second could **not be verified from a primary source** in this run — ICAEW's firm-size statistics page would not render and the FRC publishes members and *audit* firms only. Treat "40,000 accountancy practices" as `[UNVERIFIED]`. What is verified is 3,760 statutory audit firms and 408,000 members across UK and ROI.

---

## Where the money actually leaks — findings across the research lines

**Manual reconciliation is the recurring shape.** Three separate regulators independently describe the same failure: data that exists in two systems and is never joined. The SRA found 8% of matter files where the documented source of funds did not match the client ledger. The FCA found consolidators whose management information could not support governance of multiple entities. HMRC has just made recruitment agencies liable for PAYE they neither calculate nor remit. In each case the pain is a *join*, not a judgement — which matters enormously for the AI-durability test in Hard Rule 4.

**Spreadsheets at scale, evidenced.** The FCA's new material third-party regime ships as **two Excel templates** for a relational six-data-group submission — the regulator itself is distributing spreadsheets in 2026. Delegated-authority bordereaux are "typically exchanged as spreadsheets, with no enforced standardisation of format or terminology between partners". The Consumer Duty board report is, for most small firms, a Word document assembled by hand from whatever MI exists.

**Regulatory burden: what survived the Standing Test.** Of the instruments in the brief, these are **BINDING**: MLR 2017 (regs 18, 19, 21); the SRA annual AML and sanctions data return (deadline 27 July 2026, all firms open on 10 June 2026, under Code of Conduct for Firms rule 3.3 and Legal Services Act 2007 s.111A); Consumer Duty PRIN 2A annual board assessment; SYSC 15A operational resilience, fully in force since 31 March 2025; Finance Act 2026 s.24 (umbrella PAYE), in force 6 April 2026; Making Tax Digital for Income Tax for over-£50k, live since 6 April 2026. **SCHEDULED**: FCA PS26/2 operational incident and third-party reporting, 18 March 2027; the SRA client-money package announced 2 June 2026, effective early 2027 subject to Legal Services Board approval. **DEAD**: audit reform / ARGA — the Department for Business and Trade has confirmed no draft Bill this session and the body has been renamed the Corporate Reporting Authority; and London Market Blueprint Two, wound down at the end of 2025 with the name "sunset".

**The small-firm problem is real and the regulator has admitted it.** On 24 February 2026 the FCA updated its Consumer Duty board-report guidance specifically because "smaller firms have different challenges" — its sample of 180 firms included 55 small firms, "some with less than 10 employees", and its advice to them amounts to *find a knowledgeable critical friend*, which is a regulator conceding there is no product. Similarly, the SRA's own AML data shows only 48% of firms had done the Regulation 21 independent audit that the regulator says most in-scope firms should have.

**Consolidation is genuine but the buyer count is small.** Over a quarter of the UK Top 75 accountancy firms are now PE-backed, with the 20 PE-backed firms growing fee income 20% to £3.18bn. Xeinadin was assembled from 122 firms; Affinia runs 33 offices on £160m revenue. The FCA's 31 October 2025 multi-firm review on advice-sector consolidation found due diligence that "appeared to be 'tick box' in nature", groups that "did not scale systems and controls in line with their growth", and insufficient "management information to allow for effective governance of multiple entities". The thesis is real; the addressable population is 60–120 groups, which is under LAW 2's threshold and requires an explicit ACV argument.

**What AI destroys and what it creates.** AI plausibly erases: first-draft compliance policies, board-report narrative writing, file summarisation, research memos, bordereaux field mapping. AI does *not* erase: an authoritative join between two systems of record that the customer controls, a regulator-specified submission format, or a liability that attaches to a named individual. The new need AI creates is narrower than it looks. *Ayinde v London Borough of Haringey and Al-Haroun v Qatar National Bank* [2025] EWHC 1383 (Admin) saw the Divisional Court refer every lawyer involved to the SRA over fabricated citations and warn of contempt. That is a genuine trigger — but it is currently met by guidance, not by a dated obligation, so it scores PROPOSED at best on the Standing Test.

**Insurance specifics.** Verified: bordereaux are spreadsheet-driven; carrier audit findings on bordereau accuracy are rising. Also verified: **VIPR holds over 50% of the Lloyd's managing agent market and processes 375,000–400,000 bordereaux a year**, and is the DA platform for four of the world's ten largest brokers. This is the clearest LAW 4 kill in the sector. CASS 5 client money for brokers is more interesting — the FCA has flagged firms misunderstanding the audit exemption threshold and treats credit write-backs as breaches of fiduciary duty — but the audit itself is a reserved accountancy engagement.

