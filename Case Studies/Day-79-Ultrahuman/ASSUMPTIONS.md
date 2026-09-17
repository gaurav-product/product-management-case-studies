# ASSUMPTIONS — Day 79, Ultrahuman

**Case study:** Day 79 of 90 · Ultrahuman Healthcare Private Limited (CIN U74999KA2019PTC129250)
**Period examined:** FY25 (year ended 31 March 2025) consolidated financials, with the position as at September 2026
**Verification:** `verify.py` — 84 checks, all passing. Both SQL queries in README §32 parse as Postgres (`sqlglot`).
**Written:** 17 September 2026

Part 1 states what is assumed and gives each rival reading equal weight. Part 2 shows the arithmetic. Part 3 lists what the author invented. Part 4 states what would falsify the thesis. Part 5 records what could not be found out.

---

## Part 1 — Assumptions

### A1 (load-bearing) — that the collapse in subscription share is a strategic choice with a commercial cost, rather than a temporary artefact of ring growth

**The assumption.** Subscription revenue was an implied 25.81% of FY24 revenue and is 5.14% of FY25 revenue. This case study reads that as the consequence of a deliberate free-AI, no-subscription strategy, and argues it leaves Ultrahuman with a cost advantage it cannot yet monetise.

**The honest rival reading, given equal weight.** **A denominator can collapse a share without anything being wrong with the numerator.** Ring revenue grew 9.5× on a small base after a product finally found its market. Subscription revenue did not fall — it grew. If rings are the product and software is a feature that makes rings sell, then a 5.14% software share is not a failure, it is what a hardware company's accounts look like when the hardware works. On this reading Ultrahuman is a profitable device business with 55% ring gross margins that has correctly refused to tax its own customers, and the free AI is exactly why it grew 45% in a year when its largest market was closed to it.

**Why the case study proceeds anyway, and how far.** Three things support the reading without settling it.

1. **The subscription line did not merely lag — it nearly stalled.** 7.4% growth in a year when the company grew 439.87% is not a base effect; it is a line that is not being sold.
2. **The company has committed capital that only pays off under a software strategy.** Qualcomm silicon, on-chip machine learning and a third-party SDK are platform investments. A pure hardware company would spend that money on supply, which is what §47 concludes it should do first.
3. **The market has priced the difference.** 2.61× ARR against a comparable peer at 11.23× trailing revenue. Multiple gaps have many causes — scale, liquidity, an imminent IPO — but recurring revenue is the standard one.

**What would settle it.** Post-lapse paid conversion on the cohorts whose free plug year has expired. That number exists inside the company and is not published. It is why Phase 0's K2 is designed to kill the proposal in three analyst-weeks.

### A2 — that the FY25 figures reported by Entrackr and Inc42 faithfully represent the consolidated filings

Neither the RoC filing nor the audited statements were read for this case study. Two independent outlets report the same statements, at different precision, and the company's own release corroborates the revenue split and the margin ratios in dollars. **Rival reading:** secondary reporting of filings can drop a line, misread a consolidation boundary or mix entity scopes, and the group has an Indian holding company plus four overseas subsidiaries. The case study treats agreement across three sources as strong but not equivalent to reading a filing, and §64 says so.

### A3 — that the 12% PowerPlugs attach rate can be applied to rings sold

The CEO's figure is "about 12% of its users." This study multiplies it by ~800,000 cumulative rings sold to get ~96,000 payers. **Rival reading:** users and cumulative rings sold differ — some rings are inactive, some users own more than one, and the company separately reported "over 500,000 users" in October 2025. If the true active-user base is materially below rings sold, the payer count and the $4.80 Mn revenue estimate both fall. Every figure derived from this is labelled implied, and no conclusion in the case study reverses if the denominator is smaller — a smaller payer base strengthens the argument rather than weakening it.

### A4 — that the $50 per-plug annual price is a fair proxy

Derived by dividing the company's stated $150 value of the three-plug bundle by three. **Rival reading:** a bundled "value" is a marketing figure and may exceed any price actually charged; plugs may also be priced differently from one another. Used only for an order-of-magnitude revenue estimate, never for a per-user economics claim.

### A5 — that the 12% stress rule is a reasonable proxy for voluntary paid uptake

It is the only disclosed measure of Ultrahuman users taking an optional, incremental, paid step. **Rival reading:** installing a plug is a far smaller decision than the behaviours some initiatives require, so 12% may be too harsh for some and too generous for others — and it is measured on a base that received three plugs free for a year, which inflates it. The case study accepts both criticisms: the sensitivity in Part 2 shows the proposal still finishes last at a 75% stress rule, so the conclusion does not depend on the multiplier.

---

## Part 2 — Derivations

INR in crore, USD in millions. FY25 = year ended 31 March 2025.

**Internal consistency**
- Revenue lines: 516.0 + 29.0 + 20.0 = **565.00**; residual against reported 564.7 = **0.30**
- Total income: 564.7 + 16.1 = **580.80** ✓ matches reported
- PBT: 580.8 − 535.1 = **45.70**
- Unit spend: 535.1 ÷ 564.7 = **0.9476** ✓ matches the reported ₹0.95
- USD lines: 58.4 + 3.2 + 2.2 = **63.80** against a reported 64.0
- Implied rate: 564.7 Cr ÷ $64 Mn = **₹88.23/$**

**Growth**
- Revenue: 564.7 ÷ 104.6 − 1 = **439.87%**; multiple **5.40×**
- Expenses: 535.1 ÷ 146.4 − 1 = **265.51%**; gap to revenue growth **174.36 pp**
- Cost of material: 175.4 ÷ 33.0 = **5.32×**; share of expenses 175.4 ÷ 535.1 = **32.78%**
- Employee: 51.6 ÷ 27.3 − 1 = **89.01%**
- Selling and distribution: 98.4 ÷ 15.0 − 1 = **556.00%**; share of revenue **17.43%**

**Profit**
- PAT − PBT = 71.5 − 45.70 = **25.80** implied net tax credit = **36.08%** of PAT
- Inc42's reported credit: 32.7 ÷ 71.5 = **45.73%** of PAT
- PAT ex-credit: 71.5 − 32.7 = **38.80** = **54.27%** of reported PAT
- PBT margin on operating revenue: 45.70 ÷ 564.7 = **8.09%**

**The subscription line**
- FY25 share: 29.0 ÷ 564.7 = **5.14%**
- Implied FY24 subscription: 29.0 ÷ 1.074 = **27.00**
- FY24 share: 27.00 ÷ 104.6 = **25.81%**
- Fall: 25.81 − 5.14 = **20.68 pp**; ratio **5.03×**
- Implied FY24 rings: 516.0 ÷ 9.5 = **54.32**; FY24 ring share **51.93%**
- FY25 ring share: 516.0 ÷ 564.7 = **91.38%**
- Ring growth ÷ subscription growth: (9.5 − 1) × 100 ÷ 7.4 = **114.86×**

**Geography**
- US 344.2 ÷ 564.7 = **60.95%**; India 15.1 ÷ 564.7 = **2.67%**; Middle East **5.88%**; UK **4.43%**
- Named total **417.50**; residual 564.7 − 417.5 = **147.20** = **26.07%** unattributed
- US share fall to the current quarter: 60.95 − 45 = **15.95 pp**
- India share rise: 11 − 2.67 = **8.33 pp**; now **4.11×** its FY25 level

**Current run rate**
- Growth still needed for the January 2027 target: 200 ÷ 140 − 1 = **42.86%**
- Implied ARR a year ago: 140 ÷ 1.45 = **$96.55 Mn**
- Rings sold since February: 800,000 − 700,000 = **100,000**
- Implied revenue per cumulative ring: $140 Mn ÷ 800,000 = **$175.00**
- Implied payers: 0.12 × 800,000 = **96,000**
- Implied plug price: $150 ÷ 3 = **$50.00**
- Implied plug revenue: 96,000 × $50 = **$4.80 Mn** = **3.43%** of ARR
- Bundle value as share of Ring Pro retail: 150 ÷ 399 = **37.59%**

**The round**
- 65 + 5 = **$70 Mn**; debt share 5 ÷ 70 = **7.14%**
- Valuation multiple on 2023: 365 ÷ 120 = **3.04×**
- On ARR: 365 ÷ 140 = **2.61×**
- Round as share of valuation: 70 ÷ 365 = **19.18%**

**The Day 78 mirror**
- Oura trailing revenue ÷ this ARR: 1,424.793 ÷ 140 = **10.18×**
- Oura multiple: 16,000 ÷ 1,424.793 = **11.23×**
- Multiple gap: 11.23 ÷ 2.61 = **4.31×**
- Paid-attach gap: 0.94 ÷ 0.12 = **7.83×**
- Software revenue-share gap: 19.80 ÷ 5.14 = **3.86×**

**RICE** (Reach × Impact × Confidence ÷ Effort; stress 12.00%)
- Offline expansion 300 × 1.5 × 0.70 ÷ 4 = **78.75** → **9.45**
- Labcorp bundle 250 × 2.0 × 0.60 ÷ 4 = **75.00** → **9.00**
- *PowerPlugs Open* 800 × 2.0 × 0.40 ÷ 10 = **64.00** → **7.68**
- US supply (exempt) 400 × 1.5 × 0.90 ÷ 10 = **54.00** → **54.00**
- Exempt ÷ proposal stressed = **7.03×**; proposal loses **88.00%** of its score
- Sensitivity at a 75% stress rule: proposal **48.00**, Labcorp **56.25**, offline **59.06**, exempt **54.00** — proposal still last

---

## Part 3 — Author constructs

| Construct | Where |
|---|---|
| Personas Aditi, Ben, Farah | README §20 |
| Eval layers, pass bars, failure-mode ranking, human-in-the-loop design | §29 |
| EPW/1k and its four conditions; UCR-90 | §31 |
| Schema and both SQL queries | §32 |
| Data-flow diagram | §42 |
| *PowerPlugs Open* mechanism, evidence gate, revenue-share model | §50 |
| PRD and all AI-specific requirements | §51 |
| Wireframes, and all illustrative plug names, developers and prices | §52 |
| All four RICE initiatives, their inputs, and the choice of stress rule | §47 |
| Phase 0 kill criteria K1 (50%), K2 (4%), K3 (30%); phase lengths | §53 |
| Three-arm test; R1 (15 pp), R2 (1.5 points), R3 | §54 |
| KPI thresholds (4%, 21 days, 90%) | §55 |
| Roadmap windows | §56 |

---

## Part 4 — What would change my mind

1. **Post-lapse paid conversion turns out to be healthy.** If users keep paying for plugs after the free year, the 12% is real demand rather than a bundling artefact, and the marketplace thesis strengthens rather than dies.
2. **The next reported subscription share rises above 5.14% without a marketplace.** Something else is monetising the software layer and the premise weakens.
3. **Ultrahuman publishes Jade usage or an outcome metric.** The "neither company measures its AI" symmetry with Day 78 breaks, and Ultrahuman becomes the more evidenced of the two.
4. **The multiple gap closes after Oura's IPO prices.** If 11.23× was an IPO-window artefact, the recurring-revenue explanation for the gap loses most of its force.
5. **Phase 0's K1 fires.** If Ultrahuman's own plug claims could not pass an evidence gate, the gate is an obstacle to its own roadmap before it is a protection against anyone else's.
6. **The audited FY25 statements differ materially from the reported figures.** A2 is the assumption most likely to be wrong in a way that moves numbers rather than interpretation.

---

## Part 5 — What could not be found out

- Jade usage, conversation volume, latency, or any outcome measure.
- Which models Jade uses, whether any are third-party, and what runs on-ring versus in the cloud.
- PowerPlugs list prices, the plug catalogue size, and post-lapse renewal.
- Active users as distinct from cumulative rings sold.
- FY26 audited figures; the FY26 year closed on 31 March 2026 and no filing-derived figures were found.
- The composition of the ₹147.20 Cr of FY25 revenue not attributed to a named geography.
- How US market access was regained in legal terms — design-around, licence, settlement or CBP determination — beyond the fact of Customs clearance.
- The outcome of the USPTO review of the Oura patent underlying the ITC order.
- Whether the ₹583 Cr RoC share-issue resolution and the $70 Mn announced round describe exactly the same transaction.
