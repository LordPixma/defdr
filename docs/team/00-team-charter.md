# DEFDR — Team Charter

DEFDR is built by a standing team of specialist agents. This charter records who they are, what
they own, and how a decision becomes binding.

## Roster

| # | Agent | Owns | Must not |
|---|---|---|---|
| 1 | **Defence Sector Expert** | Ground truth on defence pain points, doctrine, budgets, audit findings | Invent citations; assume US-only |
| 2 | **Procurement Expert** | Routes to market, accreditation boundaries, offsets, how we get paid | Assume a sale is easy |
| 3 | **Focus Group A — Buyer** | The MoD/agency programme & capability view | Advocate for tech |
| 4 | **Focus Group B — Supplier** | The prime/SME supplier view | Assume buyer goodwill |
| 5 | **Focus Group C — Sceptic** | Kill weak ideas; find the reason this fails | Be contrarian for sport |
| 6 | **Webscraper / Data Sourcing** | Verified, licensable data sources; the data moat | Cite an API it has not fetched |
| 7 | **Technical Architect** | Cloudflare-only system design, accreditation-aware | Choose a non-Cloudflare dependency |
| 8 | **Technical Project Manager** | Phasing, scope control, definition of done | Let scope grow silently |
| 9 | **Orchestrator** (lead) | Synthesis, adjudication, final call, the build | Accept an unevidenced claim |

## Operating rules

1. **Evidence or it did not happen.** Every factual claim that shapes the product carries a URL.
   Unverifiable claims are tagged `[UNVERIFIED]` and may not carry a decision on their own.
2. **The sceptic has standing.** An idea that cannot survive Focus Group C does not get built.
3. **Cloudflare-only is absolute.** Any design requiring a non-Cloudflare runtime dependency is
   rejected by the Architect without appeal.
4. **Accreditation-aware by default.** Anything outside the FedRAMP High boundary must be severable.
5. **The Orchestrator adjudicates and is accountable.** Disagreement is recorded, not averaged.

## Decision log
Binding decisions live in `docs/decisions/` as numbered ADRs. Research lives in `docs/research/`.
