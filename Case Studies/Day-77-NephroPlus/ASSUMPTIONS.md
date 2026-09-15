# ASSUMPTIONS — Day 77, Nephrocare Health Services Limited (NephroPlus)

**Case study:** Day 77 of 90 · Nephrocare Health Services Limited (CIN L85100TG2009PLC066359)
**Period examined:** Q1 FY27, quarter ended 30 June 2026; results 11 August 2026, earnings call 12 August 2026
**Verification:** `verify.py` — 117 checks, all passing. All SQL in README §32 validated as parsing Postgres.
**Written:** 12 September 2026

Part 1 states what is assumed and gives each rival reading equal weight. Part 2 shows the arithmetic. Part 3 lists what the author invented. Part 4 states what would falsify the thesis. Part 5 records what could not be found out.

---

## Part 1 — Assumptions

### A1 (load-bearing) — that the great majority of NephroPlus's Indian guests are prescribed three sessions a week

**The assumption.** Every dose-adequacy figure in this case study divides delivered treatments by a denominator of three sessions per week. India's 26.02 treatments per guest-quarter becomes "66.73% of adequate" only if the prescription is three.

**The honest rival reading, given equal weight.** **Incremental haemodialysis is legitimate practice.** A patient with meaningful residual kidney function can be correctly started on twice-weekly dialysis and stepped up as function declines. It is used more widely in India than in high-income systems, for reasons that are partly clinical and partly economic. If a large share of NephroPlus's Indian guests are *correctly prescribed* twice-weekly, then the 66.73% understates true adequacy — possibly substantially — and the dose "gap" is partly a prescribing convention rather than a delivery failure.

**Why the case study proceeds anyway, and how far.** Four things support the reading without settling it.

1. **The internal comparison controls for almost everything.** The same operator, same protocols, same management and largely the same equipment delivers **2.51 sessions a week internationally and 2.00 in India**. Clinical need does not differ by 25% between a Manila patient and a Nashik patient. What differs is who pays per session.
2. **The direction of the trend is consistent with a delivery constraint, not a prescribing one.** Group dose adequacy rose **63.82% → 66.56% → 69.10%** across FY25, FY26 and Q1 FY27 annualised. Prescribing conventions do not move that fast; mix and delivery do.
3. **Incremental dialysis is a starting protocol, not a steady state.** It is indicated for patients with residual function, which declines. A population with mean tenure of several years should converge toward thrice-weekly, so a stable two-a-week average across a large cohort is harder to explain clinically than economically.
4. **The company's own marketing and clinical positioning is built on adequacy**, not on incremental protocols.

**What would settle it, and it is not published.** The distribution of prescribed frequency across the Indian guest base. That is one histogram, it exists inside the company, and its absence is why **A1 is a direction rather than a proof — and why Phase 0's K1 is designed to kill the proposal in two analyst-weeks if the prescription record cannot even supply the denominator.**

### A2 — that the segment revenue split of 55/45 is close enough to carry the realisation arithmetic

Both segment realisations (₹1,802.21 India, ₹7,459.41 international) derive from a rounded 55/45 revenue split applied to ₹281.8 Cr. At a true 54/46 the ratio moves from 4.14× to **4.31×**; at 56/44 to **3.97×**. **In every case it remains inside the company's own disclosed 3.3×–13.6× premium band**, which is the check that makes the claim safe. The 4.14× is used as an order-of-magnitude statement about payer mix, never as a precise figure.

### A3 — that the approximate treatment counts can bear division

India's "approximately 860,000" and international's "approximately 170,000" sum to 10,30,000 against a reported 10,31,084, a residual of **1,084 treatments, 0.11%**. Dividing an approximation by an exact guest count is defensible at this precision: the India dose band under ±5,000 of rounding is **66.34%–67.11%**, a spread of 0.77 of a point. Every dose claim survives the band.

### A4 — that reported PAT can be reconstructed by reversing the disclosed adjustments

Reported PAT of ₹31.90 Cr is computed as adjusted PAT ₹36.8 Cr less the ₹3.6 Cr JV loss and ₹1.3 Cr ESOP that the company states it adjusted for. This assumes those are the **only** adjustments to PAT and that they are stated pre-tax-effect as presented. If either assumption is wrong the reconstruction moves. The rival reading is that the disclosed adjustment list is incomplete, in which case reported PAT is lower still and the 7.10-point gap **widens** — so the estimate is conservative against the argument it supports.

### A5 — that the unquantified "Saudi expenses" are not immaterial

Adjusted EBITDA is struck for ESOP (₹1.3 Cr, quantified) and Saudi expenses (not quantified). The case study states only an **upper bound** — reported EBITDA margin ≤ 22.64% — and constructs no estimate. Given that Saudi is in an investment phase with a clinic open, home dialysis running and ₹70 Cr of collateral committed, assuming the line is trivial would be the less defensible choice. It is left as a bound.

---

## Part 2 — Derivations

Every figure below is computed in `verify.py` and printed on every run.

**D1 — the dose gap.**
- Clinical denominator: 3 × 13 = **39** treatments per quarter; 3 × 52 = **156** per year
- India: 860,000 ÷ 33,047 = **26.02** per guest-quarter = **2.00**/week = **66.73%** of standard; shortfall **12.98** per guest-quarter
- International: 170,000 ÷ 5,215 = **32.60** = **2.51**/week = **83.59%**; **1.25×** India; gap **6.57** treatments
- Group: 10,31,084 ÷ 38,262 = **26.95** = **69.10%**
- **Internal check 1:** 33,047 + 5,215 = **38,262**, exactly the reported total
- **Internal check 2:** 10,31,084 − (860,000 + 170,000) = **1,084** = **0.11%**
- Sensitivity band on India: **66.34%** (855,000) to **67.11%** (865,000)

**D2 — the dose trend, three independent readings.**
- FY26: 38,40,000 ÷ 36,981 = **103.84** per guest-year = **66.56%**
- Implied FY25: treatments **32,93,310**, guests **33,078** ⇒ **99.56** = **63.82%**
- Q1 FY27 annualised: 26.95 × 4 = **107.79** = **69.10%**; improvement on FY25 **5.28pp**
- India FY25 standalone: 28,85,450 ÷ 29,281 = **98.54** = **63.17%**; India improvement **3.56pp**

**D3 — where realisation comes from.**
- Blended: ₹281.8 Cr ÷ 10,31,084 = **₹2,733.05** against the disclosed **₹2,733** — a **₹0.05** agreement
- India revenue 55% = **₹154.99 Cr**; international 45% = **₹126.81 Cr**
- India **₹1,802.21**/treatment; international **₹7,459.41**; ratio **4.14×**, inside the disclosed 3.3×–13.6× band
- India **83.50%** of treatments against 55% of revenue = **−28.50pp**; international **+28.50pp**
- International revenue share **31.8% → 41.8% → 45%** = **+13.20pp** in five quarters
- Implied FY25 revenue per treatment **₹2,293.03**

**D4 — reported versus adjusted profit.**
- Reported PAT: Q1 FY27 **₹31.90 Cr**, Q1 FY26 **₹23.70 Cr**, Q4 FY26 **₹30.30 Cr**
- Reported growth **34.60%** against the reported adjusted 41.7% — gap **7.10pp**
- Adjusted growth computed from the two adjusted figures: **41.54%**
- Reported PAT margin **10.40% → 11.32%**, **+0.92pp**, against adjusted **+1.70pp** — a **1.86×** difference
- Adjustments **₹4.90 Cr** = **13.32%** of adjusted PAT, from **8.85%** (ESOP only) a year earlier
- JV loss alone = **9.78%** of adjusted PAT; up **16.13%** on Q4 FY26's ₹3.1 Cr
- Sequential: reported **+5.28%**, adjusted **+4.84%**

**D5 — the unquantified adjustment.**
- EBITDA after removing only ESOP: **₹63.80 Cr** ⇒ margin **≤22.64%** against the presented 23.10%
- Overstatement from the ESOP adjustment alone: **0.46pp**
- Adjusted EBITDA growth computed: **30.72%**; Q1 FY26 margin computed **21.86%**; sequential gain **2.20pp**

**D6 — growth quality.**
- Revenue **+23.71%**, treatments **+13.31%** ⇒ revenue outgrew volume by **10.40pp**
- Revenue per treatment **+9.19%**
- Treatment growth **decelerated 3.30pp** on FY26; revenue growth decelerated **8.50pp**; guest growth **accelerated 1.20pp**
- Revenue growth ran **3.70pp above** the top of the company's 15–20% guidance
- Treatments per clinic: group **1,874.70**, India **1,765.91**, international **2,698.41** = **1.53×**
- Guests per clinic: India **67.86**, international **82.78**
- Treatments per employee **672.59** on 1,533 staff

**D7 — the market, sized from the company's own base.**
- Implied national dialysis population: 29,281 ÷ 10% = **292,810**
- Required volume: 292,810 × 156 = **45.68 million** treatments a year
- NephroPlus FY25 India delivered 28,85,450 = **6.32%**; implied national shortfall **42.79 million**
- **Closing only the existing Indian guest base to three a week: 428,833 treatments/quarter = 49.86% more Indian volume = ₹77.28 Cr = 27.43% of group revenue**

**D8 — capital and events.**
- IPO listing gain **6.52%**; band width **5.02%** of the floor; fresh issue **40.57%** of the ₹871.05 Cr issue
- Use of fresh issue: India clinic capex **36.53%**, debt repayment **38.48%** — debt repayment **1.05×** the clinic capex
- Authorised-to-paid-up **1.74×**
- September grant **4,01,362** = **20.00%** of the 2026 scheme, at ₹230 = **50.00%** of the IPO price
- Uzbekistan assessment ₹14.79 Cr = **40.19%** of Q1 FY27 adjusted PAT
- Saudi collateral ₹70 Cr = **24.84%** of quarterly revenue

**D9 — RICE.** Stress multiplier **33.27%** (the share of prescribed Indian dose not delivered). Baseline **4.46 / 3.57 / 3.13 / 1.32**; stressed **1.48 / 1.19 / 3.13 / 0.44**. Proposal **1st at baseline, 2nd under stress**; the exempt initiative beats it **2.11×**; the proposal loses **66.73%** of its score, identical to India's dose adequacy because the stress rule is the adherence gap. Three assertions enforced programmatically.

---

## Part 3 — Author constructs

Everything below was invented by the author and is not reported by the company.

1. **The *NephroPlus Dose* mechanism** — the append-only clinician-signed prescription ledger, the read-only adequacy engine, the reason-coded downward-revision flag, the adequacy function with no volume target, automatic outreach suspension on breach, and the distinction in routing between a guest who skipped and a guest whose scheme entitlement is exhausted.
2. **The weekly bundled price** covering prescribed sessions below 3× the per-session rate. This is a pricing design, not a disclosed company plan.
3. **DAG/1k**, its four conjunctive conditions and the choice of prescribed guest-weeks as denominator.
4. **PSC-90**, its 90th-percentile-of-improvement construction, its per-clinic and per-clinician reporting requirement and the 3.0% threshold.
5. **All SQL in §32** — the schema (`guests`, `prescriptions`, `sessions`, `clinics`, `calendar`, and the materialised `clinic_quarter_dose` and `guest_dose_90d`), the three queries, and the exit-type taxonomy including the 60-day lapse window. Validated as parsing Postgres; the schema is inferred from what the business must hold, not from any disclosed data model.
6. **All four RICE initiatives and every input.** The proposal's Reach of 33.0k is the Indian guest base rounded down from 33,047 — the only construct here is which initiatives to compare it against and their Impact, Confidence and Effort values.
7. **Phase 0 kill criteria K1–K3** and the 85%-of-guest-weeks join threshold.
8. **The four-arm test design**, Arm C as the falsification arm, and all three pre-registered rules including the 6-percentage-point margin, the monsoon-quarter requirement and the mortality/hospitalisation safety endpoints.
9. **Personas (§20), the journey and data-flow diagrams (§22, §42), both wireframes (§52), the KPI dashboard targets (§55) and the roadmap windows (§56).**
10. **The framing of per-session pricing as the mechanism suppressing dose** (§16, §38, §39, §50) — an interpretation, and the central interpretive claim of the case study.

---

## Part 4 — What would change my mind

| Evidence | Effect |
|---|---|
| **The prescribed-frequency distribution shows a large correctly-prescribed twice-weekly cohort** | A1 weakens severely and the headline percentage is wrong. This is the single most dangerous disclosure to the thesis and the company holds it. |
| **Q2 FY27 Indian dose adequacy rises materially with no pricing or outreach change** | The thesis is wrong — the gap was a titration artefact of newly enrolled guests. Computable by anyone from the quarterly treatment and guest figures. |
| Phase 0 K1 fires: the prescription record does not carry sessions-per-week per guest | The proposal dies in two analyst-weeks. Named as the criterion most likely to fire. |
| Phase 0 K2 fires: adequacy is uniformly ~2.0 across every clinic, payer and tenure cohort | There is nothing to target; the answer is national pricing policy, not a product. |
| Arm C matches Arm D | The ledger is overhead. Reprice and drop the apparatus. |
| Any arm raises volume while PSC-90 rises | Prescription gaming or over-treatment; the arm is disqualified regardless of its adequacy gain. |
| International dose adequacy falls toward India's as international scales | The payer explanation weakens and a capability explanation gains ground. |
| The company quantifies "Saudi expenses" and the reported EBITDA margin lands near 23% | The §45 point 6 criticism dissolves; nothing else in the case study moves. |

---

## Part 5 — What could not be found out

1. **The distribution of prescribed session frequency across the Indian guest base.** The single disclosure that would settle A1. Not published.
2. **Prior-year India and international splits** for guests and treatments, so the dose gap has **no geographic trend**.
3. **Mortality, hospitalisation and cohort survival.** A chronic-care provider's most meaningful outcome metrics; none disclosed. §32's third query is written for exactly this and cannot be run from outside.
4. **Session duration against prescribed duration.** A short session is a partial dose; nothing disclosed distinguishes them.
5. **The quantum of "Saudi expenses"** excluded from adjusted EBITDA.
6. **Any competitor's audited financials.** India's organised dialysis market is consolidated and unlisted apart from NephroPlus, so no peer comparison was constructed.
7. **State-scheme entitlement caps by state**, which would size how much of the Indian gap is affordability versus entitlement exhaustion — two opposite problems the proposal must distinguish and an outsider cannot.
8. **Per-payer or per-format realisation** (captive hospital versus standalone versus PPP), beyond the H1 FY26 captive revenue share of 36.51%.
9. **Reported (unadjusted) EBITDA and PAT as printed in the financial statements.** Both are reconstructed here from the disclosed adjustments, not read off a filed statement.

---

*Companion to `README.md`, Day 77 of 90. All derived figures reproducible via `verify.py`; all SQL in §32 validated as parsing.*
