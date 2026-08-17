# ASSUMPTIONS — Day 52, Lenskart

This file exists so that nothing in [README.md](./README.md) has to carry an unmarked assumption. Everything here is mine. None of it is a Lenskart statement, a finding, or a fact.

- **Assumptions (A)** — things I believe but cannot verify from public sources, which the analysis depends on.
- **Derivations (D)** — arithmetic I performed on published figures.
- **Constructs (C)** — objects, metrics, and designs I invented. Nothing in this category exists at Lenskart.

**Date of analysis:** 17 August 2026. **Latest financials available:** FY26 (year ended 31 March 2026), per Lenskart's Q4 FY26 shareholders' letter and subsequent coverage. **Research boundary:** public sources only.

---

## Part 1 — Assumptions

### A1 — Load-bearing. The gap between Titan's $3.4B TAM estimate and Lenskart's $9.2B estimate is genuinely unresolved by any disclosed conversion data, not merely a difference in analytical framing that both sides already understand and have priced in.

I infer this from the fact that Titan has publicly and repeatedly restated its narrower figure even after Lenskart's IPO, and that no source I found shows Lenskart publicly disclosing a conversion-rate metric specific to the "previously uncorrected" population that would settle the dispute with data rather than assertion.

**Why it might be wrong:** Lenskart may track this internally and simply not disclose it (a reasonable competitive-secrecy decision), in which case the "gap" is a disclosure gap, not a measurement gap — a distinction I flag in §64 but cannot resolve from outside the company.

**How it gets tested:** the Phase 0 baseline in §53 — before proposing a new flow, check whether existing outreach-camp data already shows a clear conversion pattern that simply hasn't been surfaced publicly.

**Confidence:** Medium on the disclosure gap existing. Low on whether the underlying measurement gap also exists internally.

### A2 — The $9.2B TAM and 943-million-uncorrected figures, sourced to RedSeer via Lenskart's own DRHP, should be treated with more caution than an independent third-party estimate would warrant

RedSeer's report was commissioned in the context of Lenskart's DRHP process. I do not have evidence of methodology bias, but the commissioning relationship is a standard reason for caution with any company-sponsored market-sizing study, regardless of the specific researcher's rigor.

**Confidence:** Medium — a general caution, not a specific finding of error.

### A3 — A "starter pair" priced near breakeven can be sustained without materially damaging the ~70% blended gross margin the company currently reports

Assumed, not modelled with Lenskart's actual per-unit cost structure for the specific cohort proposed. If financing default rates or refit costs in this segment are higher than assumed, the near-breakeven framing in §39.3 could understate the actual margin drag.

**Effect if wrong:** §39.2's cost-benefit framing would need revision; the disclosure argument (§46) stands independently of the exact pricing construct, since the core proposal is about measurement, not about this specific pricing mechanism.

**Confidence:** Low-medium — the softest assumption in this document.

### A4 — Lenskart's outreach programme (Drishti) already reaches a large enough sample of first-time-uncorrected individuals for a meaningful Phase 0 baseline to be possible without new outreach infrastructure

Based on the disclosed figure of 910,000+ individuals screened across 940 villages. I have no visibility into how many of those screenings resulted in a "needs correction" outcome, nor how that subset's purchase behaviour was or wasn't tracked.

**Confidence:** Medium.

### A5 — The FY26 profit figures reported across different sources (₹493.61 Cr, ₹500.95 Cr, "~₹501 Cr") reflect reporting-cut differences (standalone vs. consolidated, or rounding/timing of the figure's publication) rather than a genuine restatement or error

**Confidence:** Medium — not independently reconciled against a single primary filing in this analysis.

---

## Part 2 — Derivations

| # | Derivation | Inputs | Result | Where |
|---|---|---|---|---|
| **D1** | One-time gain as share of FY25 reported profit | 167.2 ÷ 297.3 | **≈56%** | §5, §13.5 |
| **D2** | FY25→FY26 revenue growth | (8,814.0−6,652.5)/6,652.5 | **≈32.5%** | §13.4 |
| **D3** | FY24→FY25 revenue growth | (6,652.5−5,427.7)/5,427.7 | **≈22.6%** | §13.4 |
| **D4** | FY23→FY24 revenue growth | (5,427.7−3,788)/3,788 | **≈43.3%** | §11, §13.4, Appendix A-3 |
| **D5** | Unadjusted FY25→FY26 PAT growth | (~501−297.3)/297.3 | **≈68.5%** | §5, §13.5 |
| **D6** | Company-reported "adjusted" FY25→FY26 PAT growth (excluding the one-time gain from the FY25 base) | Per company's Q4 FY26 letter | **≈148%** (company-reported figure, not independently recomputed here) | §5, §13.5 |
| **D7** | SAM range, Titan-basis vs Lenskart-basis, at ~25% claimed organised share | 25% × $3.4B; 25% × $9.2B | **≈$0.85B – $2.3B** | §13.3 |
| **D8** | Unit gap, correction need vs. current sales | 943M (need) − 242M (FY25 units sold) | **≈701M person-gap** (not literally comparable 1:1 since units≠people, but directionally illustrates the scale of the claimed opportunity) | §13.2 |

**The one caveat that applies to D5–D6:** this document reports both the unadjusted (68.5%) and company-adjusted (~148%) PAT growth figures as stated by Lenskart itself; D6 was not independently recomputed from first principles in this analysis and is carried at face value from the company's own shareholder letter.

---

## Part 3 — Constructs

| # | Construct | Detail | Where |
|---|---|---|---|
| **C1** | **First Pair Promise** | The entire proposal — cohort-tagged flow, starter pricing, financing, refit guarantee | §50 |
| **C2** | **Verified First-Correction Rate (VFCR)** (North Star) | §31 |
| **C3** | **First-Time Tester Conversion Funnel, Time-to-First-Purchase, Outreach-Channel Attribution** | §32 |
| **C4** | **Personas Ritika, Manoj, Aarav** | §20 — constructed archetypes, not real individuals or disclosed customer profiles |
| **C5** | **All RICE inputs and the stress rule** | §47 |
| **C6** | **Acceptance-criteria bars** | §51.5 |
| **C7** | **The three-arm A/B design, including Arm C as falsifier** | §54 |
| **C8** | **Technical architecture and data-flow reconstructions** | §41, §42 |
| **C9** | **The framing of Lenskart's valuation as "a bet on a growth theory" and the TAM dispute as the central strategic question** | §13.3, §46 |

---

## Part 4 — What is not in this document

- **No screenshots or authenticated-session data.**
- **No Lenskart-disclosed cohort-level conversion data.** All first-time/repeat distinctions in this document are inferred from aggregate disclosures (e.g., "46% first-time tests") or constructed as personas, not sourced from a disaggregated Lenskart dataset.
- **No independent verification of the RedSeer TAM methodology.** Treated as a company-cited, company-favourable estimate (A2), not an audited figure.
- **No claim about the merits or motives of the post-lock-in block-deal selling** (§8, §15) — noted as a normal part of the IPO lifecycle, not evidence of anything beyond that.

---

## Part 5 — The single sentence version

If only one line of this file survives: **the entire case study depends on assumption A1 — that the gap between Titan's $3.4B and Lenskart's $9.2B eyewear TAM estimates is currently unresolved by any public conversion data, rather than a dispute both companies already understand and have priced in — and A1 is testable with a Phase 0 baseline check of Lenskart's existing outreach-camp conversion data, before any new flow is built.**

---

*Companion to [README.md](./README.md) · Day 52 of 90*
