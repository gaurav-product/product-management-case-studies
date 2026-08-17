# ASSUMPTIONS — Day 50, Zepto

This file exists so that nothing in [README.md](./README.md) has to carry an unmarked assumption. Everything here is mine. None of it is a Zepto statement, a finding, or a fact.

Three categories are kept separate throughout:

- **Assumptions (A)** — things I believe but cannot verify from public sources, which the analysis depends on.
- **Derivations (D)** — arithmetic I performed on published figures. The inputs are sourced; the operation is mine.
- **Constructs (C)** — objects, metrics, and designs I invented. Nothing in this category exists at Zepto.

**Date of analysis:** 17 August 2026. **Latest financials available:** FY26, as disclosed in Zepto's Updated DRHP (filed June 2026). **Research boundary:** public sources only — DRHP filings, trade press, third-party market trackers. No employee contacted, no internal document accessed, no authenticated session used.

---

## Part 1 — Assumptions

### A1 — Load-bearing. The company-level loss is now mostly a demand-variance and expansion-mix problem, not a fundamentally broken unit-economics problem.

I infer this from two facts held together: (1) Bernstein's estimate that ~3,600 of the top 3,800 dark stores across India's eight largest cities are individually profitable, and (2) net loss has widened every year even as revenue has scaled 130%+ annually and loss-as-a-share-of-revenue actually *improved* in FY26 versus FY25.

**Why it might be wrong:** Bernstein's split is a single secondary source I could not independently verify against Zepto's own store-level data, which is not public. "Profitable" at the store level under Bernstein's methodology may not net out to profitable once corporate overhead, marketing, and technology spend are allocated back — in which case the loss is not primarily a variance problem, it's a genuinely unresolved margin problem at every level.

**How it would be tested:** the Phase 0 data check in §53 — before building anything, confirm whether a meaningful share of existing users already show weekly-repeat-basket behaviour. If they don't, the variance-reduction premise of Zepto Steady has nothing to attach to.

**Confidence:** Medium on direction. Low on magnitude.

### A2 — Zepto Club (2026) is functionally a second attempt at the job Zepto Pass (2024) was built for

Trade press describes Zepto Club as a "return to subscriptions" after Pass and an earlier "Daily" offering were discontinued. Zepto has not, to my knowledge, published a document explicitly framing Club as Pass's successor in these terms.

**Why it might be wrong:** the two products may be strategically distinct rather than sequential — Pass optimised for volume/acquisition, Club could be a genuinely new high-margin-user retention play unrelated to Pass's discontinuation reasons, which are not public.

**Confidence:** Medium.

### A3 — Demand variance, not just average volume, materially affects per-store cost

I assume unpredictable hourly order flow (as opposed to low average volume) raises per-order fulfilment cost through rider idle time, spoilage on fresh categories, and reactive staffing. This is standard operations-management logic for perishable, time-critical fulfilment, but I have no Zepto-specific data confirming its magnitude.

**Confidence:** Medium on direction, low on magnitude.

### A4 — A commitment-based discount can be funded by realised operational savings rather than pure margin giveaway

Assumed, not modelled with real cost data. If fulfilment-cost savings from predictable demand are smaller than the discount offered, Zepto Steady loses money per committed order rather than saving it.

**How it gets tested:** §51.5 acceptance criteria and the Phase 1/Phase 2 gates in §53 require the savings to show up before national rollout.

**Confidence:** Low-medium — the softest assumption in this document.

### A5 — Zepto holds enough historical order data to detect existing weekly-repeat-basket patterns

Required for Phase 0 (§53) to be answerable at all. If users' historical ordering is genuinely random/impulse-driven with no repeat structure, there's nothing for a commitment product to capture.

**Confidence:** Medium — quick-commerce categories (groceries, staples) are inherently more repeat-prone than impulse categories, which supports this directionally, but it is not confirmed for Zepto specifically.

### A6 — The IPO fund-use disclosure reflects genuine strategic prioritisation, not just regulatory boilerplate

I read the ₹1,629 Cr (new stores) + ₹1,735 Cr (lease payments) allocation as evidence that footprint expansion is the dominant near-term strategic bet. DRHP fund-use tables are, in practice, sometimes broader/vaguer than actual spend intent.

**Effect if wrong:** the "money is going to footprint, not utilisation" framing (§45, §46) is weaker than presented, though the underlying loss/variance argument (A1) stands independently of how IPO capital specifically gets allocated.

**Confidence:** Medium.

### A7 — "Total sales" figures reported across FY24–FY26 are not directly comparable to standard operating-revenue lines used elsewhere in retail

I treat the ₹4,454 Cr / ₹9,668.8–11,110 Cr / ₹22,623.6 Cr figures as "total sales including other income," per how multiple sources describe them, and apply the 15–20%-of-GMV operational-revenue convention cautiously, flagging rather than asserting it.

**Effect if wrong:** all revenue-based ratios in §13 and §18 shift; the qualitative finding (widening absolute loss despite improving loss ratio) is more robust than the specific percentages, because it holds under either reading of "revenue."

**Confidence:** Medium.

---

## Part 2 — Derivations

| # | Derivation | Inputs | Result | Where |
|---|---|---|---|---|
| **D1** | FY24→FY25 revenue growth | (9,668.8−4,454)/4,454 | **≈117%** (reported elsewhere as 129% using a slightly different FY24 base of ₹4,223.9 Cr) | §13.3 |
| **D2** | FY25→FY26 revenue growth | (22,623.6−9,668.8)/9,668.8 | **≈134%** | §13.3 |
| **D3** | Loss as % of revenue, FY24 | 1,248.6/4,454 (or 1,214.7/4,223.9) | **≈28%** | §13.3 |
| **D4** | Loss as % of revenue, FY25 | 3,367.3/9,668.8 | **≈35%** | §13.3 |
| **D5** | Loss as % of revenue, FY26 | 5,905.2/22,623.6 | **≈26%** | §13.3 |
| **D6** | Loss growth, FY25→FY26 | (5,905.2−3,367.3)/3,367.3 | **≈75%** | §5 |
| **D7** | Operational revenue estimate, FY25 (15–20% of GMV convention, applied by third-party analysts) | 15–20% × ₹9,668.8–11,110 Cr | **≈₹1,495–1,994 Cr** | §13.4, §18 |
| **D8** | Orders per store per day | 2.33M ÷ 1,139 | **≈2,046** | §13.5 |
| **D9** | Fresh-issue capital to new stores + leases as share of total fresh issue | (1,629+1,735)/8,010 | **≈42%** | §13.6, §46 |
| **D10** | Capex per new dark store (fund-use table) | 1,629 Cr ÷ ~1,900 stores | **≈₹0.86 Cr/store** | §13.6 |
| **D11** | FCF improvement, FY25→FY26 | (5,332−4,330)/5,332 | **≈19% smaller outflow** | §5, §30 |

**The one caveat that applies to D1–D6 collectively:** two different FY24 revenue bases exist in circulation (₹4,454 Cr vs ₹4,223.9 Cr) depending on source, and two different FY25 revenue figures exist (₹9,668.8 Cr vs ₹11,110 Cr). The direction of every derivation here (fast growth, widening absolute loss, improving loss ratio) holds regardless of which base is used; the precise percentages would shift by a few points either way.

---

## Part 3 — Constructs

| # | Construct | Detail | Where |
|---|---|---|---|
| **C1** | **Zepto Steady** | The entire proposal — commitment subscription, discount structure, scheduling flow | §50 |
| **C2** | **Held Order Predictability (HOP)** | Proposed North Star metric | §31 |
| **C3** | **Slot-Commitment Rate, Demand-Variance Index, Fill-Rate on Committed Baskets** | Proposed analytics objects | §32 |
| **C4** | **Personas Aditi, Karan, Meenal** | Constructed from category-typical user patterns, not Zepto data | §20 |
| **C5** | **All RICE inputs and the stress rule** | §47 |
| **C6** | **Acceptance-criteria bars** (fill-rate ≥85%, slot adherence ≥90%) | §51.5 |
| **C7** | **The four-arm A/B design, including Arm D as falsifier** | §54 |
| **C8** | **Technical architecture and data-flow reconstructions** | §41, §42 |
| **C9** | **The reading of Zepto Pass → Zepto Club as one continuous, still-incomplete experiment** | §39.2 |
| **C10** | **The "footprint vs utilisation" framing of IPO capital allocation** | §46 |

---

## Part 4 — What is not in this document

- **No screenshots or authenticated-session data.** No Zepto account was used.
- **No Zepto-disclosed store-level profitability data.** The Bernstein estimate is a secondary source, not company disclosure.
- **No confirmed operational-revenue line from Zepto itself** — the 15–20%-of-GMV figure is a third-party analyst convention applied to Zepto, not a Zepto-reported number.
- **No claim about the FEMA-related regulatory matter's merits.** Disclosed in the DRHP; treated as a risk (§57, R1), not adjudicated here.
- **No post-July-2026 IPO timeline commitment**, since the process was paused and no new date was public as of the date of analysis.

---

## Part 5 — The single sentence version

If only one line of this file survives: **the entire case study depends on assumption A1 — that Zepto's widening company-level loss is now primarily a demand-variance and expansion-mix problem sitting on top of a mostly-working store base, rather than evidence the core model doesn't work — and A1 is testable in a single-city Phase 0 data check before anything is built, which is why §53 tests it first.**

---

*Companion to [README.md](./README.md) · Day 50 of 90*
