# DEFDR — Data Sources Research (Category 03)

**Author:** Webscraper / Data-Sourcing Agent
**Date:** 18 September 2026
**Status:** Primary research complete. All endpoints marked VERIFIED were live-tested with `curl` from a datacentre IP on 18 Sep 2026.

## How to read this document

- **VERIFIED** = I issued a real HTTP request and recorded the status code, content type and payload size. Evidence is inline.
- **[UNVERIFIED]** = I could not complete a live test (blocked, needs credentials, or proxy failure). Treated as an assumption, not a fact.
- **Licence verdict** is my reading of published terms. It is engineering guidance, not legal advice. Anything marked NEEDS LICENCE or DO NOT SCRAPE should go past counsel before it touches production.

### Critical cross-cutting finding: CDN bot-blocking

A large set of defence-adjacent government sites return **403 to datacentre IPs** via Akamai or Cloudflare, regardless of what their terms permit. This matters enormously for a Cloudflare-hosted product, because **Cloudflare Workers egress from datacentre ranges**. Affected and confirmed blocked: `www.war.gov` (ex-defense.gov), `www.dla.mil`, `www.usgs.gov`, `www.tenders.gov.au`, `www.nspa.nato.int` (Cloudflare challenge), `www.ncia.nato.int`.

This is an availability constraint, not a legal one, but it kills naive "just fetch it from a Worker" designs. Plan for it: every one of these has an alternate machine-readable route documented below, and we should prefer the alternate rather than fight the CDN.

---

## A. DEFENCE TENDERS & CONTRACT AWARDS

| Source | URL | Access | Auth | Format | Cadence | Licence verdict | Notes |
|---|---|---|---|---|---|---|---|
| **UK Find a Tender (FTS)** | `https://www.find-tender.service.gov.uk/api/1.0/ocdsReleasePackages?updatedFrom=<ISO8601>&limit=<n>` | REST API | **None** | OCDS 1.1.5 JSON | Continuous; daily XML zips | **SAFE TO USE** — OGL v3.0 | **VERIFIED** HTTP 200, 23,927 bytes. Above-threshold UK notices post-Brexit. `ocdsRecordPackages` also exists. No robots.txt on host (404) → no crawl restriction. Best single UK source. |
| **UK Contracts Finder** | `https://www.contractsfinder.service.gov.uk/Published/Notices/OCDS/Search?publishedFrom=YYYY-MM-DD&publishedTo=YYYY-MM-DD&size=<n>` | REST API | **None** | OCDS 1.1 JSON | Continuous | **SAFE TO USE** — OGL v3.0 | **VERIFIED** HTTP 200, 570,699 bytes for a 10-day window. Covers sub-threshold + historic. Server silently appends `limit=100`. No robots.txt (404). |
| **UK MOD Defence Sourcing Portal (DSP)** | `https://contracts.mod.uk/` (Jaggaer) | HTML only, auth wall | Supplier registration | HTML | n/a | **DO NOT SCRAPE** | **VERIFIED** `robots.txt` = `User-agent: *` / `Disallow: /esop`. `/esop` is precisely the tender area. No API. MOD notices above threshold also appear on FTS — **use FTS instead**. |
| **US USAspending.gov** | `https://api.usaspending.gov/api/v2/...` | REST API (GET+POST) | **None** | JSON | Daily from FPDS/FABS | **SAFE TO USE** — US Gov public domain | **VERIFIED** twice. `GET /references/toptier_agencies/` → 200, 52,613 bytes. `POST /search/spending_by_award/` filtered to DoD FY26 → 200, returned live GE and Lockheed Martin awards with `generated_internal_id`. No key, no quota. **Highest-value US source.** |
| **US FPDS-NG ATOM** | `https://www.fpds.gov/ezsearch/FEEDS/ATOM?FEEDNAME=PUBLIC&q=AGENCY_CODE%3A%229700%22&templateName=1.5.3&s=FPDS.GOV` | ATOM feed | **None** | ATOM XML | Near-real-time | **SAFE TO USE** — public domain | **VERIFIED** HTTP 200, 174,857 bytes. `AGENCY_CODE:"9700"` = DoD. Transaction-level detail (mod-by-mod) that USAspending flattens. Paginated 10/page — slow for bulk, excellent for deltas. |
| **US SAM.gov Opportunities v2** | `https://api.sam.gov/opportunities/v2/search` | REST API | **Free key, severely rate-limited** | JSON | Daily | NEEDS CARE — key ToS | **VERIFIED** docs at open.gsa.gov. Endpoint confirmed; `postedFrom`/`postedTo` required, max 1yr, `limit` max 1000. **Rate limit is the problem: ~10 requests/day on a non-federal personal key**, 1,000/day with a role. [UNVERIFIED] exact tier numbers — GSA docs say only "limited based on federal or non-federal roles". Plan around a daily budget, not per-second. |
| **US SAM.gov Entity API** | `https://api.sam.gov/entity-information/v3/entities` | REST API | Key + approved role | JSON | Daily | NEEDS CARE | **VERIFIED** returns HTTP 404 with no key. Sensitive entity fields need explicit role approval. |
| **US DoD daily contract announcements** | `https://www.defense.gov/DesktopModules/ArticleCS/RSS.ashx?ContentType=400&Site=945` | RSS | **None** | RSS 2.0 | Daily ~21:00 GMT | SAFE (feed) / **blocked (articles)** | **VERIFIED** — I brute-forced the feed parameters to find this. 200, returns `contracts-for-sept-18-2026`. **But `<description>` is empty and the linked `www.war.gov` article is 403 Akamai.** Feed gives you title/link/date only. Note the department was renamed — defense.gov now serves "Department of War News Feed". |
| **US DIBBS** | `https://www.dibbs.bsm.dla.mil/` | HTML | Click-through consent | HTML | Daily | **DO NOT SCRAPE** | **VERIFIED** HTTP 200 but serves a "DoD Warning and Consent Banner" interstitial. Automated acceptance of a US Government consent banner is a legal risk we should not take. |
| **EU TED (Tenders Electronic Daily)** | `POST https://api.ted.europa.eu/v3/notices/search` | REST API (**POST only**) | **None** | JSON + XML/PDF links | Daily | **SAFE TO USE** — EU reuse policy | **VERIFIED** — `GET` returns `405 Request method 'GET' is not supported`; `POST` with `{"query":"classification-cpv=35000000","limit":2,"fields":[...]}` → **200 with real notices**. No API key needed. CPV 35000000 = security/defence equipment. `robots.txt` permits notice crawling. |
| **EU Funding & Tenders Portal** | `https://api.tech.ec.europa.eu/search-api/prod/rest/search?apiKey=SEDIA` | REST API | Public `SEDIA` key | JSON | Continuous | [UNVERIFIED] | **VERIFIED as 405** on GET — requires POST with a multipart/form body. Endpoint exists and the `SEDIA` key is public, but I did not get a successful query. Covers EDF/EDIRPA defence R&D calls — worth a follow-up spike. |
| **Ukraine Prozorro** | `https://public.api.openprocurement.org/api/2.5/tenders` | REST API | **None** | JSON | Real-time | **SAFE TO USE** — open data by law | **VERIFIED** twice. List → 200 with `next_page` offset cursor for full-history replay. Detail fetch of a real tender ID → 200 with full structured record. Genuinely excellent: complete wartime procurement record, changelog-style pagination. |
| **Canada — CanadaBuys** | `https://canadabuys.canada.ca/opendata/pub/openTenderNotice-ouvertAvisAppelOffres.csv` | Bulk file | **None** | CSV (bilingual) | Daily | **SAFE TO USE** — Open Government Licence Canada | **VERIFIED** HTTP 200, **6,563,814 bytes**. Straight download, no key. |
| **Netherlands — TenderNed** | `https://www.tenderned.nl/papi/tenderned-rs-tns/v2/publicaties?page=0&size=<n>` | REST API | **None** | JSON | Continuous | **SAFE TO USE** [UNVERIFIED licence text] | **VERIFIED** HTTP 200, live data dated 2026-09-18. Undocumented-but-public `papi` endpoint. Licence page not read — confirm before production. |
| **Poland — eZamowienia** | `https://ezamowienia.gov.pl/mo-board/api/v1/Board/Search?PageSize=<n>` | REST API | **None** | JSON | Continuous | **SAFE TO USE** [UNVERIFIED licence text] | **VERIFIED** HTTP 200, 2,713 bytes, real BZP notices. Poland is a top-3 European defence spender right now — high strategic value. |
| **Norway — Doffin** | `https://api.doffin.no/public/v2/search` | REST API | **Free key required** | JSON | Continuous | NEEDS FREE KEY | **VERIFIED** HTTP 401: *"Access denied due to missing subscription key."* Azure APIM. Registration should be quick. |
| **Australia — AusTender** | `https://data.gov.au/data/api/3/action/package_show?id=austender-contract-notice-export` | CKAN API → CSV | **None** | CSV | Weekly (Sundays) | **SAFE TO USE** — CC-BY | **VERIFIED** CKAN HTTP 200. Direct `tenders.gov.au` is **403 CDN-blocked (VERIFIED)** — go via data.gov.au. A community OCDS wrapper exists at github.com/austender/austender-ocds-api [UNVERIFIED]. |
| **NATO NSPA / NCIA** | `nspa.nato.int`, `ncia.nato.int` | HTML only | None | HTML | Irregular | **AVOID AUTOMATION** | **VERIFIED** both 403. NSPA returns a Cloudflare "Just a moment..." JS challenge; NCIA 403s. No API. Bypassing a bot challenge is a ToS problem as well as a technical one. Treat NATO opportunities as manual/low-volume. |

---

## B. COMPANY / SUPPLY CHAIN DATA

| Source | URL | Access | Auth | Format | Cadence | Licence verdict | Notes |
|---|---|---|---|---|---|---|---|
| **GLEIF LEI** | `https://api.gleif.org/api/v1/lei-records?page[size]=<n>` | REST API + bulk | **None** | JSON:API / XML / CSV | **3x daily golden copy** | **SAFE TO USE** — **CC0** | **VERIFIED** HTTP 200. Response metadata: `"total": 3434832` records, `goldenCopy.publishDate: 2026-09-18T16:00:00Z`. CC0 is the most permissive licence in this entire document. Includes Level 2 parent/child ownership. **Backbone entity resolver.** |
| **UK Companies House** | `https://api.company-information.service.gov.uk/` | REST + streaming + bulk | **Free key** | JSON | Real-time (stream) | **SAFE TO USE** — OGL v3.0 | **VERIFIED** 401 `{"error":"Empty Authorization header"}` without key → endpoint live. **Rate limit VERIFIED from official docs: 600 requests per 5 minutes, then 429.** No paid tier to raise it — CH explicitly says contact them. Correct architecture is bulk snapshot for first load + streaming API to stay current + REST for lookups. PSC (beneficial ownership) included. |
| **OpenCorporates** | `https://api.opencorporates.com/v0.4/...` | REST API | **Paid** | JSON | Varies | **NEEDS LICENCE** | **VERIFIED** HTTP 401 `{"error":{"message":"Invalid Api Token..."}}`. Commercial licence required. Largely redundant given GLEIF (CC0) + Companies House (OGL) for our core markets. |
| **OpenOwnership Register** | `https://api.openownership.org/` | REST + bulk JSONL | None (bulk) | BODS JSON | Periodic | [UNVERIFIED] | Live test failed: `curl (56) CONNECT tunnel failed, response 502` — a proxy failure, not a site failure. Could not confirm. Bulk BODS data is believed open-licensed; **re-test before relying on it**. |
| **US CAGE / NCAGE** | `https://eportal.nspa.nato.int/Codification/Search/BasicSearch` | HTML form | None | HTML | Continuous | AVOID AUTOMATION | **VERIFIED** HTTP 200 **but page serves `<meta name="robots" content="noindex,nofollow">`** — an explicit signal against automated indexing. CAGE data is also inside SAM entity API. |
| **NATO NSN / NMCRL** | `https://eportal.nspa.nato.int/ac135/nmcrl/` | Subscription product | **Paid** | Web / offline DB | Periodic | **NEEDS LICENCE** | NMCRL Web is the only NATO-approved NSN database and is a paid NSPA product. Free third-party mirrors (nsnlookup.com, govcagecodes.com) exist but are **re-publishers of NATO data with their own ToS** — using them does not launder the licence. **This is the single biggest paid-data gap in the defence stack.** |
| **JOSCAR / Hellios** | `https://hellios.com/joscar` | Closed platform | Membership | n/a | n/a | **DO NOT SCRAPE** | **VERIFIED closed.** Suppliers pay £725+VAT/yr (free under £1m turnover). Hellios states data "will only be shared with the buying organisations who are members of the community and will not be shared with any other third party." Contractually off-limits. Confirms the original hypothesis. |

---

## C. SANCTIONS, EXPORT CONTROL & RISK

| Source | URL | Access | Auth | Format | Cadence | Licence verdict | Notes |
|---|---|---|---|---|---|---|---|
| **US OFAC SDN + Consolidated** | `https://sanctionslistservice.ofac.treas.gov/api/PublicationPreview/exports/SDN.CSV` · `.../CONS_ADVANCED.XML` | Bulk file | **None** | CSV / XML (schema'd) | On change (often daily) | **SAFE TO USE** — US public domain | **VERIFIED both.** SDN.CSV → 200, **5,695,725 bytes** (302 redirect, follow it). CONS_ADVANCED.XML → 200, **4,537,353 bytes**, `Version="3"` with an XSD. The ADVANCED XML is far richer than CSV — use it. |
| **UK Sanctions List (FCDO)** | `https://sanctionslist.fcdo.gov.uk/docs/UK-Sanctions-List.xml` (also `.csv`, `.ods`, `.html`, `.txt`, `.pdf`) | Bulk file | **None** | XML / CSV / ODS | Daily | **SAFE TO USE** — OGL v3.0 | **MAJOR FINDING — the obvious URL is dead.** The OFSI Consolidated List of Asset Freeze Targets **closed on 28 January 2026**; the UK Sanctions List is now the single official source. I **VERIFIED** the old `assets.publishing.service.gov.uk/media/ConList.json` returns **HTTP 404**. Anyone still integrating against OFSI ConList is reading a frozen file. Also note the identifier change: **"OFSI Group ID" → "Unique ID#"** — this will break naive entity matching. |
| **EU Consolidated Sanctions (FSD)** | `https://webgate.ec.europa.eu/fsd/fsf/public/files/xmlFullSanctionsList_1_1/content?token=dG9rZW4tMjAxNw` | Bulk file | Public token in URL | XML | On change | **SAFE TO USE** — EU reuse | **VERIFIED** HTTP 200, **25,766,640 bytes** (largest file tested). `generationDate="2026-08-05"`. The `token` is a well-known public constant, not a secret. |
| **UN Security Council Consolidated** | `https://scsanctions.un.org/resources/xml/en/consolidated.xml` | Bulk file | **None** | XML (XSD) | On change | **SAFE TO USE** | **VERIFIED** HTTP 200, **2,176,957 bytes**, `dateGenerated="2026-09-18T23:00:04Z"` — regenerated the same day I fetched it. |
| **US Consolidated Screening List — BULK** | `https://data.trade.gov/downloadable_consolidated_screening_list/v1/consolidated.json` · `.../consolidated.csv` | Bulk file | **NONE** | JSON / CSV | Daily | **SAFE TO USE** — public domain | **KEY FINDING.** The *search API* requires a key (**VERIFIED** 401 "missing subscription key"), but the **bulk files need no authentication at all**. **VERIFIED**: JSON → 200, **33,793,738 bytes**; CSV → 200, **16,789,447 bytes**. Consolidates 12+ US lists in one file — **BIS Entity List, Denied Persons, Unverified List**, DDTC debarred, OFAC, and more. This single URL replaces most of section C's US scope and **sidesteps the API key entirely.** |
| **ITAR USML (22 CFR 121)** | `https://www.ecfr.gov/api/versioner/v1/full/<date>/title-22.xml?part=121` | REST API | **None** | Structured XML | On amendment | **SAFE TO USE** — public domain | **VERIFIED** HTTP 200, 240,765 bytes decompressed. Parsed out `Category I—Firearms and Related Articles`, `Category II—Guns and Armament`. **Gotcha: the endpoint returns HTTP 406 unless you send `Accept-Encoding` permitting compression** (`curl --compressed`). Error message is explicit about this. |
| **EAR CCL (15 CFR 774)** | `https://www.ecfr.gov/api/versioner/v1/full/<date>/title-15.xml?part=774` | REST API | **None** | Structured XML | On amendment | **SAFE TO USE** — public domain | **VERIFIED** HTTP 200, **2,131,189 bytes**. Full Commerce Control List with ECCNs. Same compression requirement. |
| **EAR Entity List (15 CFR 744)** | `https://www.ecfr.gov/api/versioner/v1/full/<date>/title-15.xml?part=744` | REST API | **None** | Structured XML | On amendment | **SAFE TO USE** — public domain | **VERIFIED** HTTP 200, **2,510,387 bytes**. The `<date>` path segment means you can fetch **any historical version** — this makes point-in-time "what was controlled when" queries possible, which is unusual and valuable. |
| **EU Dual-Use Annex I** | EUR-Lex | Bulk doc | None | PDF / HTML / XML | Annual delegated reg | SAFE TO USE — EU reuse | [UNVERIFIED] as structured data. EUR-Lex offers Formex XML but Annex I is a deeply nested list; expect real parsing work. Not a clean table. |
| **UK Strategic Export Control Lists** | GOV.UK | Bulk doc | None | PDF / ODT | Periodic | SAFE TO USE — OGL | [UNVERIFIED] structured availability. Published as documents, not data. |
| **OpenSanctions** | `https://data.opensanctions.org/datasets/latest/default/index.json` | Bulk + API | None (bulk) | FtM JSON / CSV | Daily | **NEEDS LICENCE for commercial** | **VERIFIED** HTTP 200. Metadata: **4,066,734 entities**, 1,227,645 targets, `updated_at: 2026-09-18T18:53:01`. Superb pre-reconciled aggregate — **but licence is CC BY-NC**, so our commercial SaaS cannot use the free tier. Reseller/OEM licence explicitly permits redistribution. **Decision needed: pay OpenSanctions, or build our own union of the free primary lists above.** |
| **UK NSI Act 2021 notifications** | `gov.uk/government/collections/national-security-and-investment-act` | HTML / PDF | None | HTML, PDF | Annual report + ad-hoc | SAFE TO USE — OGL | **VERIFIED** HTTP 200. **Not structured data** — final orders published as individual pages, statistics as annual PDF. Scrapeable but needs bespoke parsing. |
| **US CFIUS** | Treasury.gov | PDF | None | PDF | Annual | SAFE TO USE | [UNVERIFIED] Annual report PDF only. Aggregate statistics, no transaction-level feed. Low automation value. |

---

## D. OBSOLESCENCE / PARTS / ELECTRONIC COMPONENTS

**This is the weakest category by far — and that is itself the finding.** Almost everything genuinely useful is either membership-gated or commercially licensed.

| Source | URL | Access | Auth | Format | Cadence | Licence verdict | Notes |
|---|---|---|---|---|---|---|---|
| **GIDEP** | `https://www.gidep.org/` | Members-only portal | **Membership** | Web / reports | Continuous | **DO NOT REDISTRIBUTE** | **VERIFIED** site loads (200, Angular SPA) but data is behind membership. Membership is **free but restricted to US/Canadian government agencies and their contractors**. Members may not republish GIDEP alerts to non-members. This is the authoritative source for diminishing-manufacturing-sources (DMSMS) and counterfeit-part alerts — and we structurally **cannot** resell it. |
| **DLA public logistics (FLIS/WebFLIS/PUB LOG)** | `https://www.dla.mil/...Public-Logistics-Information/` | HTML / paid DVD | None | Mixed | Periodic | AVOID / [UNVERIFIED] | **VERIFIED HTTP 403** — Akamai blocks datacentre IPs. PUB LOG historically ships as a paid subscription disc. No usable public API found. |
| **Nexar / Octopart** | `https://nexar.com/api` | GraphQL API | **Paid key** | JSON | Continuous | **NEEDS LICENCE** | **VERIFIED** docs live (200). Free tier "Welcome 1K" = **1,000 API calls/month**. Standard ≈ **$500/month for ~2,000 parts/month**, and notably **restricts lifecycle status, lead times and datasheets** — i.e. the exact obsolescence fields we want are the upsell. Redistribution terms at nexar.com/api/legal must be reviewed by counsel. |
| **Mouser API** | `https://www.mouser.com/api-home/` | REST API | Free key | JSON | Continuous | NEEDS CARE | Live test inconclusive: `curl (92) HTTP/2 stream not closed cleanly`. [UNVERIFIED]. Free keys exist; ToS typically forbids bulk caching/redistribution — **read before caching**. |
| **DigiKey API** | `https://developer.digikey.com/` | REST API (OAuth2) | Free key | JSON | Continuous | NEEDS CARE | **VERIFIED** portal 200. OAuth2, free tier available. Same redistribution caveat: fine for on-demand enrichment, not for building a resellable parts database. |
| **Semiconductor PCN/EOL notices** | Per-vendor (TI, ADI, Microchip…) | HTML / PDF per vendor | None | HTML, PDF | Ad-hoc | FRAGMENTED | [UNVERIFIED] No consolidated free feed exists. Each vendor publishes its own PCN page. Aggregating these is **real, defensible work** — see Join Idea 2. |

---

## E. CRITICAL MINERALS / INDUSTRIAL BASE

| Source | URL | Access | Auth | Format | Cadence | Licence verdict | Notes |
|---|---|---|---|---|---|---|---|
| **UN Comtrade** | `https://comtradeapi.un.org/public/v1/preview/C/A/HS?reporterCode=<n>&period=<yr>&cmdCode=<hs>&flowCode=X` | REST API | **None (preview)** / free key (full) | JSON | Annual + monthly | **SAFE TO USE** — UN open data | **VERIFIED** HTTP 200, **200,297 bytes**, `"count": 224` rows for a single reporter-year. The `/public/v1/preview/` path works with **no key at all**. Full API with higher limits needs a free key. HS codes 93xx (arms/ammunition) and 8710 (tanks) give a direct defence trade view. |
| **USGS Mineral Commodity Summaries** | `https://www.sciencebase.gov/catalog/items?q=mineral+commodity+summaries&format=json` | Catalog API → CSV/XLSX | **None** | JSON catalog → CSV | Annual (Jan/Feb) | **SAFE TO USE** — US public domain | **VERIFIED workaround.** `www.usgs.gov` is **403 CDN-blocked (VERIFIED)**, but the **ScienceBase catalog API works: HTTP 200, `"total": 354` matching items.** Fetch data files via ScienceBase item IDs instead of the USGS web page. |
| **EU Critical Raw Materials Act list** | `https://single-market-economy.ec.europa.eu/sectors/raw-materials/areas-specific-interest/critical-raw-materials_en` | HTML / PDF | None | HTML, PDF | ~Every 3 years | SAFE TO USE — EU reuse | **VERIFIED** HTTP 200. The CRM/SRM lists are short and stable enough to **hand-curate once** rather than scrape. Low effort, do it manually. |

---

## F. OPEN SOURCE INTELLIGENCE / DEFENCE NEWS

| Source | URL | Access | Auth | Format | Cadence | Licence verdict | Notes |
|---|---|---|---|---|---|---|---|
| **GOV.UK news (MOD-filtered)** | `https://www.gov.uk/search/news-and-communications.atom?organisations%5B%5D=ministry-of-defence` | ATOM | **None** | ATOM XML | Continuous | **SAFE TO USE** — OGL v3.0 | **VERIFIED** HTTP 200, 13,308 bytes. Every GOV.UK search page has an `.atom` twin — this generalises to DIT, DBT, BEIS, OFSI notices etc. Very useful and very cheap. |
| **US DoD/DoW news** | `https://www.defense.gov/DesktopModules/ArticleCS/RSS.ashx?ContentType=1&Site=945` | RSS | **None** | RSS 2.0 | Daily | SAFE TO USE — public domain | **VERIFIED** 200, 10,017 bytes. Note `ContentType` selects feed: **1 = news, 9 = releases, 400 = contracts**. Article bodies on `war.gov` are 403-blocked. |
| **Breaking Defense** | `https://breakingdefense.com/feed/` | RSS | **None** | RSS 2.0 | Continuous | HEADLINES ONLY | **VERIFIED** HTTP 200, 5,977 bytes. Standard WordPress feed. Use titles/links/dates as signals; **do not republish article text** — that is their copyright. |
| **Defense News** | `https://www.defensenews.com/arc/outboundfeeds/rss/category/pentagon/?outputType=xml` | RSS | **None** | RSS 2.0 | Continuous | HEADLINES ONLY | **VERIFIED** HTTP 200, **54,024 bytes** (rich feed). Category-scoped feeds available. Same copyright caveat. |
| **Janes** | `janes.com` | Paywalled | **Paid** | Web / API | Continuous | **NEEDS LICENCE** | Commercial intelligence subscription. Enterprise pricing. Not accessible for ingestion — and a direct competitor in parts of our space. |

---

## TOP 10 HIGHEST-VALUE, LOWEST-FRICTION SOURCES

Ranked by (product value) x (openness of licence) x (ease of ingestion). Every entry is no-auth or free-auth, open-licensed, and live-verified.

| # | Source | Why it ranks here |
|---|---|---|
| **1** | **USAspending.gov API** | No auth, no quota, POST query language, full DoD award graph with recipient identifiers. Public domain. Verified working end-to-end. Nothing else gives this much for this little. |
| **2** | **US Consolidated Screening List (bulk JSON/CSV)** | One unauthenticated 33MB file = BIS Entity List + Denied Persons + Unverified + DDTC debarred + OFAC, refreshed daily. The API needs a key; **the bulk file does not**. Enormous compliance value, zero friction. |
| **3** | **GLEIF LEI (CC0)** | 3.43M legal entities with parent/child ownership, refreshed 3x daily, **CC0** — no attribution, no restriction. The join key that makes everything else connectable across jurisdictions. |
| **4** | **UK Find a Tender + Contracts Finder (OCDS)** | Two no-auth OCDS APIs under OGL v3.0 covering above- and below-threshold UK procurement. Already in a standard schema, so ingestion is cheap. Our home market. |
| **5** | **eCFR Versioner API (USML / CCL / Entity List)** | Export-control law as **structured, date-versioned XML**, public domain, no auth. The date path enables point-in-time reconstruction — a genuinely rare capability. (Remember `--compressed`.) |
| **6** | **EU TED v3 API** | No API key, POST search across all EU procurement, CPV-filterable to defence (35000000). Pan-European coverage in one endpoint. |
| **7** | **OFAC (SDN + CONS_ADVANCED.XML) & UN Consolidated XML** | Schema-backed, public-domain, near-daily sanctions primaries. Together with #2 and the FCDO list they cover the whole Western sanctions surface for free. |
| **8** | **UK Companies House (REST + streaming + bulk)** | Free key, OGL v3.0, includes PSC beneficial ownership. 600 req/5min is a real constraint — architect for bulk-load + stream-to-stay-current, not for live lookups at scale. |
| **9** | **Ukraine Prozorro** | Complete real-time wartime procurement record, open by law, cursor pagination for full history replay. Utterly unique dataset and nobody in the West is productising it well. |
| **10** | **UN Comtrade (preview, no key)** | Physical trade flows by HS code — the only open source that turns supply-chain claims into observable tonnage. HS 93xx/8710 = direct defence trade visibility. |

**Just outside the top 10, and worth keeping:** CanadaBuys bulk CSV (6.5MB, no auth), Poland eZamowienia (no auth, top-3 European defence spender), FPDS ATOM (transaction-level deltas), GOV.UK `.atom` feeds (trivially cheap signal), USGS via ScienceBase (CDN workaround).

---

## WHAT UNIQUE DATASET COULD WE CREATE BY JOINING THESE?

The individual sources are all free and all known. **The moat is not the data — it is the resolved entity graph and the time dimension.** Every join below produces something I could not find sold as a product today.

### Join 1 — The Sanctions-Exposed Defence Supply Chain ("who did we just pay that we shouldn't have")

**Join:** USAspending + FPDS award recipients → GLEIF LEI (CC0) + Companies House PSC → OFAC/UK/EU/UN/CSL sanctions union.

Contract award data names the *prime*. Sanctions lists name *ultimate owners*. Nobody joins them **through beneficial ownership at the entity-resolution layer**, because doing it well requires reconciling UEI ↔ LEI ↔ company number ↔ PSC across four naming conventions.

**Reveals:** primes and subs whose ultimate beneficial owner sits within N hops of a sanctioned or Entity-Listed party. Screening vendors check the *counterparty*; procurement tools check the *contract*. **Neither walks the ownership graph from a live award into a sanctions list.** That is the product.

**Why defensible:** entity resolution is accumulating, not copyable. Every correction compounds. And because CSL bulk, GLEIF (CC0) and OFAC are all free and open-licensed, the *inputs* cost nothing while the *resolved graph* becomes proprietary.

### Join 2 — Point-in-Time Export-Control Exposure ("when did this become controlled?")

**Join:** eCFR versioned XML (USML/CCL/Entity List, **any historical date**) + tender/award technical scope (CPV 35xxxxx, NAICS/PSC codes) + award dates.

The eCFR Versioner API takes a date in the path — so we can reconstruct **exactly what was controlled on any given day** and diff consecutive versions to detect the moment an ECCN or Entity List entry changed.

**Reveals:** live contracts whose technical scope **became** export-controlled *after* award, and suppliers added to the Entity List *while holding* an open contract. This is a compliance event nobody is watching for, because it requires both a legal time-series and a contract time-series in the same system.

**Why defensible:** the historical diff corpus has to be **accumulated from today forward**. A competitor starting in 2027 cannot retroactively build our 2026 change history. Time is the moat.

### Join 3 — Cross-Jurisdiction Programme Tracking ("the same programme, five countries, one view")

**Join:** UK FTS/Contracts Finder (OCDS) + EU TED (CPV 35xxxxx) + Prozorro + CanadaBuys + Poland eZamowienia + AusTender, unified on OCDS and resolved to GLEIF/Companies House entities.

They are all free and all open, but they are in **six schemas, five languages and six entity conventions**. The OCDS ones are half-way there already; TED, Prozorro and eZamowienia are not.

**Reveals:** a single supplier's position across every allied procurement system at once — who is winning in Poland but losing in the UK, which Ukrainian requirements are being mirrored into NATO buys months later, and where one component vendor is a single point of failure across multiple national programmes.

**Why defensible:** this is unglamorous normalisation work at exactly the scale that is too big for a consultancy and too niche for a generalist data vendor. NSPA/NCIA being CDN-blocked means the NATO layer stays manual for everyone — including competitors.

### Join 4 — Obsolescence Risk Against Live Contract Value

**Join:** vendor PCN/EOL notices (scraped per-vendor) + Nexar/DigiKey lifecycle status (licensed) + NSN/part numbers appearing in tender and award documents + contract value and period of performance from USAspending/FPDS.

**Reveals:** *"£X million of contracts currently in delivery depend on a component going end-of-life in 9 months."* Obsolescence tools know parts. Procurement tools know contracts. **Nothing joins part lifecycle to contract financial exposure and delivery dates.**

**Caveat — and it is a real one:** this is the only join with a **licensing dependency**. GIDEP is the authoritative obsolescence source and we structurally cannot resell it (US/Canada members only, no redistribution). Nexar gates lifecycle status behind ~$500/mo and restricts redistribution. **Build this on our own vendor-PCN scraping plus on-demand distributor lookups, and treat the part↔contract linkage as the proprietary asset** — not the lifecycle data itself. Legal review required before launch.

### Join 5 — Critical Mineral Chokepoints Under Live Programmes

**Join:** USGS Mineral Commodity Summaries (via ScienceBase) + EU CRMA list + UN Comtrade flows (HS 93xx, 8710, and mineral codes) + defence contract awards by programme.

**Reveals:** which live allied programmes depend on minerals whose refining is concentrated in a single non-allied jurisdiction — quantified in **contract value at risk**, not in think-tank prose. Every element of this is free and open-licensed; the analysis exists today only as annual PDF reports, never as a queryable, contract-linked feed.

---

## RECOMMENDATIONS

1. **Build the entity resolver first.** GLEIF (CC0) + Companies House (OGL) + SAM UEI is the spine. Joins 1, 3 and 4 are all worthless without it, and it is the only component that genuinely compounds.
2. **Start the eCFR + sanctions snapshot diff on day one, before any UI exists.** Join 2's value is purely a function of how long we have been recording. Every day we delay is a day of moat we can never recover. This is cheap — a daily cron and object storage.
3. **Use CSL bulk, not the CSL API.** Verified no-auth, and it removes an API-key dependency from the compliance path.
4. **Decide OpenSanctions buy-vs-build early.** CC BY-NC blocks our commercial use of the free tier. The free primaries (OFAC + FCDO + EU FSD + UN + CSL) cover most of the same ground — but OpenSanctions has already done the reconciliation, which is precisely the work we are claiming as our moat. Leaning **build**, buying only if time-to-market demands it.
5. **Architect around the CDN blocks now.** war.gov, dla.mil, usgs.gov, tenders.gov.au and NSPA all 403 datacentre IPs, and **Cloudflare Workers egress from datacentre ranges**. Every one of these has a verified alternate route documented above — use the alternate. Do not build a residential-proxy workaround; it converts an availability problem into a ToS problem.
6. **Fix the OFSI→UK Sanctions List migration in any existing code.** The old ConList URL is a verified 404 and the entity identifier changed from "OFSI Group ID" to "Unique ID#".
7. **Treat D (obsolescence) as phase 2 and legally-gated.** It is the highest-value category commercially and the most constrained legally. Do not let it block phases 1 and 3.

## Open items for follow-up

- OpenOwnership bulk BODS — live test blocked by a proxy 502, needs re-testing.
- EU Funding & Tenders Portal — confirm the POST body shape for the SEDIA search API (EDF/EDIRPA coverage).
- TenderNed and eZamowienia — endpoints verified working, but licence text not yet read.
- Doffin — register for the free Azure APIM subscription key.
- Mouser API — inconclusive live test (HTTP/2 stream error).
- EU Dual-Use Annex I and UK Strategic Export Control Lists — assess whether Formex XML parsing is worth it versus hand-curation.
