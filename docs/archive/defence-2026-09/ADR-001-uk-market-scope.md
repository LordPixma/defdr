# ADR-001: Scope DEFDR to the UK market

**Status:** Accepted
**Date:** 2026-09-19
**Decided by:** Product owner, implemented by Orchestrator

## Decision

DEFDR targets the **UK defence market** for launch. Non-UK markets are out of scope for product
decisions, though a UK customer's obligations *to* foreign nations remain firmly in scope.

## Consequences — what this resolves

**CONFLICT 4 is now moot, in our favour.** Cloudflare lacks DoD IL4, which would have excluded the
US DoD CUI market. Under UK scope this stops being a liability entirely. The UK has no equivalent
barrier: OFFICIAL-SENSITIVE is a handling caveat on OFFICIAL, not a separate classification, and
the Government Security Classifications Policy states OFFICIAL uses "good commercial" ICT.

Kahootz sells MOD-assessed OFFICIAL-SENSITIVE collaboration on G-Cloud at **£3.69–£11.69 per user
per month** holding only ISO 27001, Cyber Essentials Plus, UK hosting and a Secure by Design pack.
Realistic year-one compliance cost is **£30k–£80k**, not the $100k–$750k of a FedRAMP path.

**The hosting mandate and the market are now aligned rather than in tension.** This is the single
biggest effect of the scope change.

**CONFLICT 1 is weakened and referred back.** The N-tier supply chain thesis rested largely on NDAA
FY24 Section 805 — a US instrument. Under UK-only scope that forcing function does not apply. The
Sceptic has been asked whether an independent UK forcing function exists for sub-tier visibility, or
whether the thesis was US-dependent all along.

## Consequences — what this sharpens

**The UK market is small, and that is now the central risk.** True UK buyer counts, not global
obligation pools, become the decisive test. A candidate with fewer than ~50 real UK buyers must
justify itself on ACV or be rejected. The $371bn global offset pool is explicitly a vanity metric
and may not be cited in support of a UK decision.

**UK-specific forcing functions now carry the whole weight of the "why now" argument:**

| Forcing function | Date | Status |
|---|---|---|
| UK "Back British" offsets / industrial participation regime | Consultation closed Dec 2025 | **Being verified — decisive** |
| Defence Cyber Certification Level 0 for all MOD industry partners | 31 Dec 2026 | Being verified |
| Segmented Acquisition Model — 3-month software contracting route | Live April 2026 | Being verified |
| G-Cloud 15 listing window | Awarded 6 Aug 2026; reopens ~18 months after go-live | Hard calendar item |
| MOD SME spend commitment | +£2.5bn by 2028 | Published |

**The offsets thesis has two distinct UK shapes**, and they must not be conflated:
1. **Outbound (obligor-side):** UK exporters — BAE, Rolls-Royce, Babcock, MBDA UK, Thales UK,
   Leonardo UK — owe offset obligations to foreign buyer nations. The customer is UK-based even
   though the obligations are international. Available today, no new regime required.
2. **Inbound (authority-side):** the UK itself becoming a buyer nation that imposes industrial
   participation obligations on foreign sellers, under "Back British". Depends entirely on that
   regime actually landing.

Shape 1 does not depend on the new regime and is therefore the lower-risk half. Shape 2 is the
upside. **If the Sceptic finds "Back British" has not bound, shape 1 must be able to stand alone —
or offsets is not the answer.**

## Selection criteria, revised for UK scope

1. Year-one buyer is a **UK prime, UK exporter, or UK innovation body** — not a ministry IT dept.
2. ~~Survives without US DoD IL4~~ — superseded; no longer a constraint under UK scope.
3. Not locked by a long-dated incumbent vehicle. **SCRIPTS is a US vehicle and no longer
   automatically disqualifying** — but JOSCAR/Hellios now becomes the UK incumbent to beat.
4. Required data obtainable under open licence or from the customer directly.
5. **Has a credible UK buyer count.** New, and now the hardest test.
6. Survives Focus Group C.
