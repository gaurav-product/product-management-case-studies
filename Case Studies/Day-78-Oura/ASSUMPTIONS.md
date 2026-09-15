# ASSUMPTIONS — Day 78, Oura Inc.

**Case study:** Day 78 of 90 · Oura Inc. (SEC CIK 0002133022)
**Period examined:** Nine months ended 30 June 2026; FY24 and FY25 for context. Form S-1 filed 3 September 2026.
**Verification:** `verify.py` — 106 checks, all passing. Both SQL queries in README §32 parse as Postgres (`sqlglot`).
**Written:** 15 September 2026

Part 1 states what is assumed and gives each rival reading equal weight. Part 2 shows the arithmetic. Part 3 lists what the author invented. Part 4 states what would falsify the thesis. Part 5 records what could not be found out.

---

## Part 1 — Assumptions

### A1 (load-bearing) — that Oura Advisor's value to members is not yet evidenced, and that this matters for the membership line

**The assumption.** The S-1 describes Advisor as central to the membership and discloses no metric for its use or effect. The case study reads that absence as a real gap — that Oura either does not have, or has chosen not to publish, evidence that Advisor changes retention or willingness to pay.

**The honest rival reading, given equal weight.** Companies routinely keep feature-level metrics out of prospectuses. Oura may track Advisor usage, retention lift and satisfaction in detail and simply regard them as competitively sensitive. Retention has also *risen* across cohorts during the period Advisor was introduced, which is at least consistent with the AI helping. On this reading the gap is one of disclosure, not of knowledge, and the proposal solves a problem Oura has already solved internally.

**Why the case study proceeds anyway, and how far.** Three things support it without settling it.

1. **The filing publishes every other engagement metric** — DAU/MAU, app opens, wear time, retention, annual-plan share, repeat purchase. Advisor is the one headline product capability with no number next to it.
2. **Management's own risk factor says AI compute costs could raise the cost of membership**, and the price has not moved since 2021. A company planning to "evolve pricing" around AI would benefit from publishing evidence that the AI is valued.
3. **Even if Oura measures usage, usage is not outcome.** The proposal is about whether advice *works* for the member, which no disclosed or plausibly internal engagement metric captures without a pre-registered design.

**What would settle it.** Any published Advisor usage figure or retention-by-Advisor-use cohort. Its absence is why A1 is a direction, and why Phase 0 can kill the proposal in two analyst-weeks.

### A2 — that the rounded 89% membership gross margin can carry the gross-profit split

The S-1 gives 89% as a rounded figure. Every membership gross-profit number here inherits that rounding; ±0.5 points moves membership's share of gross profit by about ±0.2 points.

### A3 — that US list price is a fair anchor for cost-to-serve

The $0.66 figure multiplies the US monthly price by 11%. Realised revenue per member is not disclosed, annual plans are 2.63% cheaper, and partner-paid and international memberships may differ. The anchor is used for sensitivity arithmetic, not as a measured cost.

### A4 — that the fall in operating margin is not a one-off

Operating margin fell from 8.64% to 5.86%. **Rival reading:** IPO readiness, IP litigation and the Ring 5 launch are front-loaded costs, and the S-1's fiscal-year history (3.30% in FY24 to 4.99% in FY25) shows margins can rise. The case study uses the nine-month fall to support a narrow claim — that "profitable at IPO" does not mean "operating leverage" in this period — not a claim about the long-run trend.

### A5 — that the repeat-purchase share is a reasonable stress rule

The 11% stress rule is the only disclosed measure of existing members voluntarily taking an optional incremental step. **Rival reading:** buying a new ring is a much larger decision than tapping "test this," so 11% is too harsh. The case study accepts that; a gentler rule — the 65% DAU/MAU ratio — lifts the proposal's stressed score to 162.50, but the premium tier rises to 541.67 and payer expansion to 195.00, so the proposal still finishes last, behind the exempt initiative at 200.00. The proposal's position does not depend on the harsh rule; the exempt initiative's first place does.

---

## Part 2 — Derivations

All $ figures in millions. S-1 figures converted from thousands.

**The headline**
- Revenue growth: 1,214.506 ÷ 697.569 − 1 = **74.11%**
- Hardware growth: 973.980 ÷ 588.726 − 1 = **65.44%**
- Membership growth: 240.526 ÷ 108.843 − 1 = **120.98%**
- Gross margin: 662.167 ÷ 1,214.506 = **54.52%** (S-1: 55%); prior 51.04% (S-1: 51%)

**Membership economics**
- Membership share of revenue: 240.526 ÷ 1,214.506 = **19.80%** (prior 15.60%)
- Membership gross profit: 240.526 × 0.89 = **214.07**
- Share of gross profit: 214.07 ÷ 662.167 = **32.33%**; ratio to revenue share **1.63×**
- Hardware gross profit: 662.167 − 214.07 = **448.10**; hardware margin 448.10 ÷ 973.980 = **46.01%**
- Membership cost of revenue: 240.526 × 0.11 = **26.46**
- Membership growth ÷ paid-member growth: 120.98 ÷ 100.00 = **1.21×**

**Price and cost-to-serve**
- Annual plan per month: 69.99 ÷ 12 = **$5.83**; discount vs $5.99 = **2.63%**
- Cost-to-serve at list: 5.99 × 0.11 = **$0.66**
- Margin points per extra $0.60: 0.60 ÷ 5.99 = **10.02 pp**
- Extra cost that halves margin to 44.5%: 5.99 × 0.445 = **$2.67**

**The profit decomposition**
- Operating income growth: 71.188 ÷ 60.265 − 1 = **18.12%**
- Operating margin: 60.265 ÷ 697.569 = **8.64%** → 71.188 ÷ 1,214.506 = **5.86%**
- PBT increase: 70.083 − 36.467 = **33.616**; of which operating income +10.923 = **32.49%**; below-the-line items (−1.105 vs −23.798) +22.693 = **67.51%**
- Effective tax rate: 34.894 ÷ 36.467 = **95.69%** → 9.315 ÷ 70.083 = **13.29%**
- Net income increase: 60.768 − 1.573 = **59.195**; tax contribution (34.894 − 9.315) ÷ 59.195 = **43.21%**; PBT contribution **56.79%**
- Net result to common: 60.768 − 985.023 = **−924.26**

**Operating expenses**
- Opex: 295.760 → 590.979, **+99.82%**; 42.40% → **48.66%** of revenue
- R&D +104.59%, S&M +83.83%, G&A +132.17%; R&D 17.03% of revenue
- Paid media: 72.8 ÷ 117.585 = **61.91%** of the S&M increase
- Professional fees: 48.3 ÷ 71.912 = **67.17%** of the G&A increase
- FY25 warranty: 84.4 ÷ 294.187 = **28.69%** of the cost-of-revenue increase

**Units and valuation**
- Rings growth on rounded units: 3.1 ÷ 1.8 − 1 = **72.22%** (S-1: 75%)
- TTM rings: 2.3 − 1.8 + 3.1 = **3.6 Mn**; ÷ 212 Mn = **1.70%**
- RPU: $332 → $311 = **−6.33%**; $326 → $311 = **−4.60%**
- Hardware revenue per ring: 973.980 ÷ 3.1 = **$314.19**
- Paid members ÷ rings since FY24: 5.0 ÷ 6.4 = **78.13%**
- First-time-buyer rings: 3.1 × 0.89 = **2.76 Mn**
- Mean paid life if 15% annual churn held constant: 1 ÷ 0.15 = **6.67 years** (an extrapolation the S-1 does not support beyond month 12)
- TTM revenue: 907.856 − 697.569 + 1,214.506 = **1,424.79**; TTM membership **290.15**; TTM net income **59.21**
- $16 Bn ÷ TTM revenue = **11.23×**; ÷ TTM net income = **270.24×**
- Two largest customers (12% + 10%): 0.22 × 1,214.506 = **267.19**

**RICE** (Reach × Impact × Confidence ÷ Effort; stress 11.00%)
- Premium tier 5,000 × 1.0 × 0.50 ÷ 3 = **833.33** → **91.67**
- Payer expansion 1,000 × 2.0 × 0.60 ÷ 4 = **300.00** → **33.00**
- *Oura Loop* 1,500 × 2.0 × 0.50 ÷ 6 = **250.00** → **27.50**
- Inference routing (exempt) 5,000 × 0.5 × 0.80 ÷ 10 = **200.00** → **200.00**
- Exempt ÷ proposal stressed = **7.27×**

---

## Part 3 — Author constructs

| Construct | Where |
|---|---|
| Personas Priya, Mark, Dana | README §20 |
| Eval layers, pass bars, failure-mode ranking, HITL design | §29 |
| VAO/1k and its four conditions; MEM-90 | §31 |
| Schema and both SQL queries | §32 |
| Data-flow diagram | §42 |
| *Oura Loop* mechanism, lever list, 80% wear rule, 7–21-day windows | §50 |
| PRD, AI-specific requirements and thresholds | §51 |
| Wireframes and illustrative values | §52 |
| All RICE initiatives and inputs; choice of stress rule | §47 |
| Phase 0 K1 (25%), K2, K3 (60%); phase lengths | §53 |
| Three-arm test; R1 (8 pp), R2 (1 point), R3 | §54 |
| KPI thresholds ($0.60, 10%, 40%) | §55 |
| Roadmap windows | §56 |

---

## Part 4 — What would change my mind

1. **Oura publishes Advisor usage and a retention lift for Advisor users.** A1 weakens substantially; the proposal becomes an extension, not a gap-filler.
2. **Operating margin recovers above 8.64% in the next reported period with price unchanged.** The cost-pressure half of the thesis weakens.
3. **Oura raises the membership price without retention loss.** Willingness to pay is demonstrated, even if not attributed to AI.
4. **Phase 0 K2 fires.** Advisor's apparent effect is mostly regression to the mean; the proposal as designed would measure little.
5. **Arm B matches Arm C.** Follow-up, not measurement, is what members need.

---

## Part 5 — What could not be found out

- Advisor usage, conversation volume, or share of members using it.
- Inference cost per conversation or per member; the split of membership cost of revenue between hosting, support and model usage.
- Realised membership revenue per member; average paid-member count for the period.
- Retention beyond 12 months.
- The price range and share count for the offering.
- Whether any commercial arrangement with webAI is a related-party transaction under the applicable definition.
- Membership gross margin for FY24 and FY25.
