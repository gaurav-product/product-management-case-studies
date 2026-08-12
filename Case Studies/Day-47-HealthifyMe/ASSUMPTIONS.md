# ASSUMPTIONS — Day 47, Healthify

This file exists so that nothing in [README.md](./README.md) has to carry an unmarked assumption. Everything here is mine. None of it is a Healthify statement, a finding, or a fact.

Three categories are kept separate throughout:

- **Assumptions (A)** — things I believe but cannot verify from public sources, which the analysis depends on.
- **Derivations (D)** — arithmetic I performed on published figures. The inputs are sourced; the operation is mine.
- **Constructs (C)** — objects, metrics, prices and designs I invented. Nothing in this category exists at Healthify.

**Date of analysis:** 12 August 2026. **Latest audited Healthify financials available:** FY25 (year ended 31 March 2025). **Research boundary:** public sources only; no employee contacted, no member data accessed, no authenticated session used.

---

## Part 1 — Assumptions

### A1 — Healthify's own members regain weight at rates resembling the trial population

**Load-bearing. This is the assumption the whole case study rests on.**

The STEP 1 trial extension found participants regained two-thirds of their weight loss within a year of withdrawal (−17.3% at week 68 → +11.6 pp regained → −5.6% net at week 120). I assume HealthifyRx members follow a broadly similar trajectory after their programmes end.

**Why I believe it:** obesity's chronicity is well established in the literature, the trial's own authors conclude that "ongoing treatment is required to maintain improvements," and real-world persistence data (A2) suggests real-world outcomes are usually worse than trial outcomes, not better.

**Why it might be wrong, and this matters:** the trial withdrew **drug and lifestyle intervention simultaneously**. HealthifyRx explicitly claims continued support through a five-phase taper with "relapse prevention support to lock in results." If that support works, Healthify's members regain less than the trial cohort, the gap this case study identifies is smaller than claimed, and the proposal weakens proportionally.

**How it gets tested:** §53 Phase 0. One analyst-week, on data Healthify already holds. If A1 is false, the proposal should be abandoned and the finding published as marketing instead. I would consider that a good outcome for the company and a bad one for this document, in that order.

**Confidence:** Medium-high on direction. Low on magnitude.

### A2 — US GLP-1 persistence patterns transfer directionally to Indian self-pay members

The persistence figures (29% at one year, 15% at two years, n = 3,364) come from US commercially-insured patients. India's market is overwhelmingly **self-pay**, with no PBM, formulary or benefit design mediating the decision.

**Direction of the bias:** self-pay should produce **worse** persistence than insured, because every month is a fresh out-of-pocket decision. The Indian figure is therefore more likely below 15% at two years than above it. I use the US figures as a conservative anchor and do not compute anything precise from them.

**Confidence:** Medium on direction. The specific percentages are not transferred.

### A3 — HealthifyRx plan prices reported in trade press are broadly current and complete

I assume ₹48,000 / ₹80,000 / ₹1,00,000 reflect real prices, and that they represent the member's substantially complete cost.

**Why it might be wrong:** prices were not observed at a Healthify checkout. They may exclude consultations, laboratory tests, repeat drug purchases beyond the included doses, or device costs. They may have changed after generic entry on 20 March 2026 — indeed §18.4 argues there is now strong commercial reason to change them.

**Effect if wrong:** §13.6's per-percentage-point figures move proportionally. The **ratio** between peak-outcome and retained-outcome cost (3.1×) is unaffected, because both terms scale together. The ratio is the finding; the absolute rupee figures are illustration.

**Confidence:** Medium.

### A4 — Consumer bioimpedance is adequate for within-member lean-mass trend detection

The Lean-Mass Loss Share guardrail (§31.2) depends on the smart scale Healthify already ships being able to detect a meaningful downward trend in lean mass within an individual over time.

**Why it might be wrong:** consumer bioimpedance is poorly accurate in absolute terms and sensitive to hydration, time of day and recent activity. It is generally more defensible for trend than for level, which is what the guardrail needs — but "generally more defensible" is not "validated."

**How it gets handled rather than assumed away:** §51.5 acceptance criterion A2 requires ≥ 0.60 agreement with clinician assessment on a labelled sample. **Below that bar the guardrail ships as an advisory and the veto rule is enforced manually.** The guardrail does not get dropped; only its automation does.

**Confidence:** Medium.

### A5 — A ₹999/month maintenance tier can carry positive contribution margin

Given that Ria resolves 77% of queries and that Hold is deliberately low-touch (one weigh-in a month, intervention only on a sustained 21-day drift), I assume the cost per Hold member-month sits below ₹999.

**Why it might be wrong:** I have no visibility into Healthify's coach cost per contact, model inference cost, or clinical review cost. If drift interventions are frequent or escalate often, the tier loses money.

**How it gets tested:** §53 Phase 2 measures cost per member-month directly before the tier scales, and §51.5 A5 makes it an acceptance criterion.

**Confidence:** Low-medium. This is the softest commercial assumption in the document.

### A6 — Healthify holds sufficient post-programme weigh-in data to run Phase 0

Phase 0 requires that some meaningful number of members who completed Rx programmes have weighed in afterwards on a paired scale.

**Why it might be wrong:** members may stop weighing in the moment the programme ends — which is itself the behaviour the proposal exists to change. If so, Phase 0 returns "insufficient data," which §53 treats as a **stop-and-fix-measurement** result rather than a proceed.

**Confidence:** Low. This is genuinely unknown and is why Phase 0 has three outcomes rather than two.

### A7 — Novo Nordisk's partnership does not contractually prevent an off-ramp product

I assume nothing in the Novo Nordisk patient-support agreement bars Healthify from selling a product optimised for members successfully discontinuing therapy.

**Why it might be wrong:** the agreement is not public. Patient-support contracts commonly include persistence-related terms, and a product whose North Star rises when members leave the drug sits awkwardly beside one.

**Effect if wrong:** the proposal survives commercially but the partnership does not — which is **R1** in §57, identified there as the risk capable of killing the strategy rather than the feature.

**Confidence:** Low. Treated as a risk, not an assumption I rely on.

### A8 — The FY25 revenue decline is substantially attributable to the advertising withdrawal

§13.5 derives ₹0.48 of revenue lost per ₹1 of advertising withdrawn by comparing two years.

**Why it might be wrong, at some length, because this number is quoted prominently:** total expenses fell 38% and employee benefit expense fell 30% in the same period, so the revenue decline is plausibly over-attributed to advertising by this method. Advertising has lagged effects a same-year ratio cannot capture. Revenue mix shifted across three lines that moved in three different directions. And two data points cannot establish an elasticity.

**What the number is and is not:** it is a **directional, order-of-magnitude claim** that FY24 marketing was buying revenue at a loss. It is **not** an elasticity estimate and is not used as one anywhere in the document.

**Confidence:** Medium on direction. Low on magnitude.

### A9 — "Six-digit" paid subscribers means 100,000–999,999

A literal reading of a company statement. Every unit-economics figure derived from it is presented as a band of that width (§13.2), and §47's stress rule discounts every reach estimate that depends on it.

**Confidence:** High on the reading. The band is the problem, not the interpretation.

### A10 — Generic semaglutide pricing reported at launch will broadly persist

§18.4 uses Natco's reported ₹1,290/month starting-dose price to compute post-generic wrapper share.

**Why it might be wrong:** launch pricing in a market with 40+ entrants is unstable, and starting-dose pricing is not maintenance-dose pricing. Higher doses cost more; a member on a maintenance dose will pay more than ₹1,290.

**Effect if wrong:** the post-generic wrapper share (~92%) falls. It would take a very large error to bring it back down to the pre-generic range, so the direction of §18.4's finding is robust even if the specific percentage is not.

**Confidence:** Medium on direction. Low on the precise figure.

---

## Part 2 — Derivations

Each of these is arithmetic I performed. Inputs are sourced in §61; the operation and the interpretation are mine.

| # | Derivation | Inputs | Result | Where |
|---|---|---|---|---|
| **D1** | Revenue lost per rupee of advertising withdrawn | Revenue −₹29 Cr; advertising −₹60.5 Cr | **≈ ₹0.48** | §13.5 |
| **D2** | Advertising as share of revenue | ₹73.5/₹207; ₹13/₹178 | **35.5% → 7.3%** | §13.5 |
| **D3** | FY24 spend per rupee of same-year revenue | ₹1 ÷ ₹0.48 | **≈ ₹2.09** | §5, §13.5 |
| **D4** | Revenue per registered user | ₹178 Cr ÷ 40M | **≈ ₹44.5/yr** | §13.2 |
| **D5** | ARPPU band | ₹178 Cr ÷ (100,000 … 999,999) | **₹1,780 – ₹17,800** | §13.2 |
| **D6** | Paid conversion band | (100,000 … 999,999) ÷ 40M | **0.25% – 2.5%** | §13.2 |
| **D7** | HealthifyRx monthly equivalents | ₹48,000/3; ₹80,000/6; ₹1,00,000/12 | **₹16,000 / ₹13,333 / ₹8,333** | §18.3 |
| **D8** | Rx-to-Smart-Plan price multiple | ₹16,000 ÷ ₹208 | **≈ 77×** | §5, §18.3 |
| **D9** | Drug share of 3-month plan, pre-generic | (12 × ₹3,500…₹4,000) ÷ ₹48,000; and (12 × ₹1,667) ÷ ₹48,000 | **42% – 100%** | §13.6, §18.4 |
| **D10** | Drug share of 3-month plan, post-generic | (3 × ₹1,290) ÷ ₹48,000 | **≈ 8%** | §13.6, §18.4 |
| **D11** | Cost per percentage point of peak loss | ₹1,00,000 ÷ 17.3 pp | **≈ ₹5,780/pp** | §13.6 |
| **D12** | Cost per percentage point still held at week 120 | ₹1,00,000 ÷ 5.6 pp | **≈ ₹17,857/pp** | §13.6 |
| **D13** | Ratio of D12 to D11 | 17,857 ÷ 5,780 | **≈ 3.1×** | §5, §13.6 |
| **D14** | Share of loss regained | 11.6 ÷ 17.3 | **67.1%** | §13.6 |

**The one caveat that applies to D11–D14 collectively:** they apply a trial cohort's outcomes to a commercial plan price. The trial withdrew lifestyle support alongside the drug; the plan claims not to. See A1. The ratio (D13) is more robust than the absolute figures, because a pricing error scales both terms equally.

---

## Part 3 — Constructs

Nothing in this section exists at Healthify. All of it is mine.

| # | Construct | Detail | Where |
|---|---|---|---|
| **C1** | **Held-Weight Member-Months (HWMM)** | Post-taper member-months inside the contracted band with ≥ 1 verified weigh-in | §31.1 |
| **C2** | **+3 pp hold band** | Nadir + 3 percentage points of body weight. Set wide enough to absorb hydration and scale variance, narrow enough that STEP 1's +11.6 pp mean regain sits far outside. Would require clinical review before deployment; the metric's structure does not depend on the exact figure | §31.1 |
| **C3** | **Lean-Mass Loss Share (LMLS)** and its −8% threshold | The guardrail. Threshold is my choice; the *existence* of the guardrail is not optional | §31.2 |
| **C4** | **Restart Rate** as a reported-not-optimised integrity metric | §31.3 |
| **C5** | **The Band, the Hold Period, the 21-day Drift Window** | Three derived analytics objects that do not currently exist | §32.2 |
| **C6** | **Healthify Hold** — the whole proposal | Hold Contract, Taper Ladder, Hold Price | §50 |
| **C7** | **₹999/month · ₹9,999/year** price point | Reasoned in §39.2 from three constraints: small relative to Rx, above Smart Plan, affordable for years | §39.2 |
| **C8** | **The credit remedy** | Service credit, never cash; conditioned on member weigh-in obligation | §39.3 |
| **C9** | **Personas Meera, Rohit, Anjali** | Constructed from the published product surface, price ladder, eligibility criteria and clinical literature. **No Healthify member was interviewed** | §20 |
| **C10** | **The user journey drop-off shape**, particularly the terminal emotional low | §22 |
| **C11** | **Node K** ("no defined product") in the user flow and the dangling `X5` node in the IA | Both are my readings of a structural absence, not Healthify diagrams | §23, §24 |
| **C12** | **Technical architecture and data flow** | Reconstructions inferred from public product behaviour and stated integrations | §41, §42 |
| **C13** | **All RICE inputs** — reach, impact, confidence, effort — and the stress rule (reach × 0.6; confidence − 20 pp) | The stressed columns are published so the arithmetic is checkable | §47 |
| **C14** | **Acceptance-criteria bars** — drift recall ≥ 0.70 / precision ≥ 0.50; LMLS clinician agreement ≥ 0.60; comprehension ≥ 80% | §51.5 |
| **C15** | **The four-arm experiment**, including **Arm D** built to falsify the author's preferred answer | §54 |
| **C16** | **The reading of FY25 as purchased profitability** | An interpretation of published figures, not a company statement | §5, §18.2 |
| **C17** | **The five-line convergence structure** and the claim that the lines were developed independently | §46 |
| **C18** | **The three strategic positions** (supplier / integrated / outcome owner) and the recommendation of C funded by A | §38.3 |

---

## Part 4 — What is not in this document

Stated so that absence is not mistaken for oversight.

- **No screenshots.** Reproducing an authenticated health app's screens would require a member account and would risk placing another person's health data in a public repository.
- **No Healthify outcome data.** None is published. Every clinical number here belongs to someone else's trial and is cited as such.
- **No churn, renewal, MAU, or Rx enrolment figures.** Not disclosed. Where the analysis needs them it constructs a band and says so.
- **No FY26 financials.** Not public as at the date of analysis.
- **No claim about the Novo Nordisk contract's terms.** Not public. Treated as risk R1.
- **No medical advice.** This document discusses prescription therapies in a commercial and product-strategy context only.

---

## Part 5 — The single sentence version

If only one line of this file survives: **the entire case study depends on assumption A1 — that Healthify's own members regain weight after their programmes end at rates resembling the published trial — and A1 is testable in one analyst-week using data Healthify already holds, which is why §53 tests it before anything is built.**

---

*Companion to [README.md](./README.md) · Day 47 of 90*
