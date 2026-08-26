# ASSUMPTIONS — Day 60: IndiGo (InterGlobe Aviation Limited)

Companion to `README.md`. Everything in the case study that is *not* a directly disclosed figure is listed here: what was assumed, how each derived number was computed, what was constructed by the author, what would falsify the thesis, and what could not be found out.

Every derived figure in both files is verified programmatically. `verify.py` — **123 checks, all passing** — is delivered with this case study but is not committed to the repository.

---

## Part 1 — Assumptions

### A1 (load-bearing) — That IndiGo's ex-fuel, ex-FX cost base grows at a rate largely independent of capacity

**What is assumed.** §16 reverses IndiGo's disclosed CASK-ex-fuel-ex-FX growth against its disclosed ASK growth in three periods to derive implied *total* ex-fuel, ex-FX cost growth of 13.66% (FY26), 10.95% (Q4 FY26) and 13.91% (Q1 FY27), and reads the narrowness of that spread — 2.96 points against a 6.6-point spread in capacity growth — as evidence that the cost base grows at roughly 13% regardless of how much IndiGo flies.

**The rival reading, given equal weight.** Two of the three periods are quarters and one is a full year. Quarterly cost carries seasonality — maintenance scheduling, crew utilisation, airport charge timing — that an annual figure averages away, so this is not a like-for-like series and three points is a small sample from which to infer independence. A reader could reasonably say the numbers are consistent with a cost base that *does* flex with capacity, observed at three points where seasonality happens to obscure it. Management's own position supports this reading: the quarter reflects "near-term cost volatility rather than structural demand weakness."

**Why the case study proceeds anyway.** The *direction* is unambiguous and is not a seasonality artefact: ex-fuel, ex-FX unit cost growth rose monotonically — 3.8%, 7.3%, 10.7% — across three consecutive reported periods while capacity growth fell monotonically — 9.5%, 3.4%, 2.9%. Whatever the exact elasticity, unit cost accelerated as capacity decelerated, three times in a row, on a metric containing neither fuel nor currency. That pattern is what the proposal addresses.

**What would kill it, and when.** Q2 FY27 is guided to *flat* capacity. If ex-fuel, ex-FX CASK growth comes in **below** Q1's 10.7% on flat capacity, the cost base flexes and A1 is dead. This is the first row of §55 and requires no interpretation — IndiGo publishes the number.

### A2 (medium) — That the Q1 FY26 comparatives derived from disclosed growth rates are close enough to use

Several prior-year figures are not disclosed as absolutes and are back-derived from disclosed growth rates: revenue from operations ₹20,503.8 Cr (from +19.9%), ancillary ₹2,153.99 Cr (from +13.9%), passenger ticket ₹17,787.48 Cr (from +23.0%), passengers 31.08 Mn (from +0.7%). Disclosed growth rates are rounded, so each carries error.

**Where this is acceptable:** the fuel and revenue comparison in §19 (both figures large; the 122.55% conclusion survives any plausible rounding) and the ancillary comparison in §25 (a 59.22% ratio would have to be wrong by more than 20 points to change the finding that ancillary badly lagged fares).

**Where it is not:** the other-revenue residual in §10. See D10 below and Part 5.

### A3 (medium) — That the ₹1,014.0 Cr gap between CASK × ASK and total expenses is net finance cost

IndiGo does not state CASK's expense base. Net finance cost on a ₹53,755.6 Cr operating lease liability is the most plausible candidate at that magnitude, but it is inferred, not disclosed (Appendix A-3). The case study flags it and notes that whatever it is, its exclusion means CASK *understates* full cost per ASK — which widens the RASK–CASK gap in §16 rather than narrowing it, so the assumption is conservative with respect to the thesis.

### A4 (author-constructed, explicitly unverified) — That the high-frequency cohort is on the order of a fifth of passengers

§13 sizes the 6E Forward opportunity from an assumed high-frequency share of roughly 20% of IndiGo's 12.34 crore FY26 passengers. **IndiGo publishes no trip-frequency distribution.** This number is a placeholder used to show the shape of the arithmetic, is labelled as such in §13, and is the first thing §53's Phase 0 measures. No conclusion in the case study depends on it.

### A5 (medium) — That the ATF cap applied to IndiGo's domestic uplift throughout 1 April – 8 June 2026

The 25% cap and the 7 June benchmark transition are well sourced, and the 75.82% figure in §19 is a straightforward day count. What is assumed is that the cap applied uniformly to IndiGo's domestic fuel purchasing across that window with no carrier-specific exceptions or contractual pass-through arrangements that would alter the effective rate. The ~₹140/litre blended rate is graded 🟡 and comes from management commentary rather than a disclosure line.

### A6 (low, non-load-bearing) — That the ancillary underperformance is at least partly anchoring rather than wholly mix

§25 offers two readings and does not select one. §54's separable test exists precisely because the case study will not assert the anchoring reading without evidence. Nothing in the thesis depends on which is right; §60 names it as something that would change the author's mind about §47's top-ranked initiative, not about §16.

---

## Part 2 — Derivations

All labels correspond to check IDs in `verify.py`.

**D1 — the ex-fuel, ex-FX acceleration.** Disclosed: 3.8% (FY26), 7.3% (Q4 FY26), 10.7% (Q1 FY27). Ratios: Q4 FY26 is 1.92× FY26; Q1 FY27 is 1.47× Q4 FY26 and **2.82× FY26**.

**D2 — implied total ex-fuel, ex-FX cost growth.** (1 + ASK growth) × (1 + unit cost growth) − 1. FY26: 1.095 × 1.038 = **13.66%**. Q4 FY26: 1.034 × 1.073 = **10.95%**. Q1 FY27: 1.029 × 1.107 = **13.91%**. Spread **2.96 points** against a capacity-growth spread of **6.6 points** — **2.23×** wider.

**D3 — RASK less CASK.** FY26 **−₹0.01**; Q4 FY26 **−₹0.48**; Q1 FY27 **−₹0.05**. Q1 FY27's gap × 43.5 bn ASK = **₹217.5 Cr**. Sequential narrowing **43 paise**; Q1 FY27's gap is **10.42%** of Q4 FY26's.

**D4 — CASK internal consistency (four independent checks, all clean).** Fuel CASK ₹2.49 + ex-fuel CASK ₹3.22 = disclosed CASK ₹5.71 exactly. FX loss ₹82.5 Cr ÷ 43.5 bn ASK = ₹0.019; ₹3.22 − ₹0.019 rounds to the disclosed ex-fuel ex-FX ₹3.20. Fuel expense ÷ ASK = ₹2.4903 against disclosed ₹2.49. Revenue from operations ÷ ASK = ₹5.6516 against disclosed RASK ₹5.66. Yield ₹6.04 × load factor 83.3% = ₹5.0313 against disclosed PRASK ₹5.03.

**D5 — the CASK residual.** ₹5.71 × 43.5 bn = ₹24,838.5 Cr against total expenses ₹25,852.5 Cr ⇒ **₹1,014.0 Cr, 3.92%** of total expenses. Derived, not disclosed (A3, Appendix A-3).

**D6 — fuel increase against revenue increase.** Revenue +₹4,080.3 Cr; fuel +₹5,000.3 Cr ⇒ **122.55%**, a **₹920.0 Cr** shortfall. Fuel as a share of revenue from operations **28.45% → 44.07%, +15.62 points**.

**D7 — the capped quarter.** 1 Apr – 8 Jun = **69 days**; the quarter = **91 days** ⇒ **75.82% capped**, 22 days (24.18%) uncapped.

**D8 — the stress rule.** Traffic growth 1.4% ÷ revenue growth 19.9% = **7.04%**. Passengers-carried growth ÷ revenue growth = 3.52%. Capacity growth ÷ revenue growth = 14.57%. Cross-check: (1 + RASK growth)(1 + ASK growth) − 1 = 19.88% against disclosed 19.9%. Second reading: BluChip 2 Mn ÷ 12.34 crore FY26 passengers = **1.62%**.

**D9 — the ancillary finding.** Ancillary per passenger ₹783.83 (from ₹693.00, **+13.11%**); ticket per passenger ₹6,990.00 (from ₹5,723.10, **+22.14%**) ⇒ ancillary grew at **59.22%** of the fare's rate. Ancillary share of revenue from operations **10.51% → 9.98%, −0.53 points**.

**D10 — the residual that is *not* used.** Revenue from operations less passenger ticket less ancillary = **₹252.1 Cr** for Q1 FY27 (1.03% of revenue). The prior-year comparative depends entirely on rounded growth rates: plausible rounding bounds give **₹482 Cr to ₹646 Cr**, a band **64.85%** as wide as the current-year figure. **Excluded from load-bearing use** (A2, §63).

**D11 — the FX line.** EBITDAR ex-FX less EBITDAR = **₹232.4 Cr**; net loss less net loss ex-FX = **₹232.4 Cr**. Identical, so the entire FX impact sits above EBITDAR. INR/USD 85.29 → 95.02 = **−11.41%**. Ex-FX net loss is **0.02%** of revenue from operations.

**D12 — the competitive mirror.** Air India group FY26 loss margin **30.94%** vs IndiGo's **2.82%** ⇒ **10.98×**. IndiGo revenue ÷ AI group revenue = **1.18×**. AI group loss ÷ IndiGo loss = **9.29×**. Combined FY26 losses **₹24,631.6 Cr**. AI group loss growth FY25→FY26 **+104.79%**. Entity-to-group residuals: **₹1,330 Cr** revenue, **₹103 Cr** loss (Appendix A-2).

**D13 — the shrinking market.** DGCA Jan–Jul 2026 984.03 lakh vs 977.79 lakh = **+0.64%**; July 2026 **−4.80%** YoY at 1.20 crore, **14.64% below** the seven-month monthly average of 1.41 crore. IndiGo's implied July domestic volume at 67.4% share: **0.81 crore**.

**D14 — scale and balance sheet.** Free ₹39,038.7 Cr + restricted ₹13,845.9 Cr = ₹52,884.6 Cr total cash ✓. Debt ex-lease **₹27,775.7 Cr**; lease liability is **65.93%** of total debt. Free cash covers the quarterly loss **164×**. Total income less total expenses = **−₹238.4 Cr** loss before tax ✓. EBITDAR margin **15.59%**, EBITDAR **−33.21%**. Maintenance **14.23%** and D&A **12.08%** of revenue from operations. Fleet **−9** sequentially. Implied utilisation **1.11 mn ASK per aircraft per day** (freighters included; illustrative only).

**D15 — RICE.** Reach in millions of passengers per year, Effort in person-quarters, stress multiplier **0.0704** applied to Reach for stressed initiatives only. Baseline: Ancillary re-anchoring **49.36**, BluChip **11.52**, 6E Forward **7.40**, A320ceo **4.72**. Stressed: A320ceo **4.72** (exempt), Ancillary **3.47**, BluChip **0.81**, 6E Forward **0.52**. **6E Forward 3rd → 4th and last**, and it is verified programmatically that 6E Forward is the weakest *stressed* initiative at baseline, which is the only way the demotion can occur.

**D17 — the units error.** 2,380 ÷ 238 = **10.0**; 21,763 ÷ 2,176.3 = **10.0**. Under the 10× reading, the implied FX hit would be ₹2,374.4 Cr = **10.22×** the disclosed ₹232.4 Cr FX impact on EBITDAR (Appendix A-1).

---

## Part 3 — Constructs

Everything below is the author's, not IndiGo's, and none of it should be read as reported fact.

**The thesis itself** (§16) — that IndiGo's cost base grows at ~13% independent of capacity, and that this rather than fuel is what the quarter reveals. IndiGo does not say this; management says the opposite.

**Personas** (§11) — four segments constructed from disclosed operating data and stated network strategy. No primary research was conducted, no segmentation is published, and these are illustrative.

**Jobs To Be Done** (§33) and **Kano classifications** (§34) — constructed. The classification of price certainty as *absent* rather than *indifferent* is an argument, not an observation.

**The 6E Forward proposal in full** (§50–52) — the corridor unit of sale, the price band, the protected allocation, the cut-off, the non-transferability rule, the corporate variant. IndiGo has proposed none of this.

**CBA/1k** (§31) — the metric, its four conjunctive conditions, and the choice of *planned* ASK at schedule freeze as denominator.

**SDA-90** (§40) — the guardrail, its 90th-percentile construction, the by-route-tier reporting rule (§41), the Passenger Access function, the build-pipeline firewall, and the two-week automatic suspension trigger.

**The three permanently excluded incentives** (§48).

**All RICE inputs** (§47) — every Reach, Impact, Confidence and Effort value, the choice of which initiatives to compare, and the decision to exempt fleet transition from stress. The stress *rule* (7.04%) is derived from disclosed figures; the decision to use it as a stress rule is the author's.

**All kill criteria and thresholds** (§53–54) — the 15% repeat-flying threshold, the 15-of-20 corridor requirement, the 8-percentage-point R1 threshold, the 80% realisation success criterion, and the two-analyst-week budget.

**The Porter's double run across domestic and international** (§39), including the judgement that the two halves sit at opposite ends of nearly every force.

**The reading of the CFO transition timing** (§2) — noted deliberately without interpretation, because no source connects it to the results.

---

## Part 4 — What Would Change My Mind

**The decisive test, available within weeks.** Q2 FY27 is guided to flat capacity. If CASK ex-fuel, ex-FX grows **less than 10.7%** on flat capacity, the cost base flexes with volume, A1 is wrong, and the thesis fails. IndiGo publishes this figure itself; no interpretation is required.

**If the ancillary decline is mix, not anchoring.** A recovery in ancillary share toward 10.5% as fare growth normalises, without any product change, would favour the mix reading, make §47's top-ranked initiative worthless, and make the product diagnosis in §36 half wrong.

**If K2 fires.** If IndiGo's high-frequency cohort already books far enough ahead to avoid fare volatility, 6E Forward solves a problem that cohort does not have, and it should not be built. This is named in §53 as the criterion most likely to fire.

**If domestic traffic returns to growth.** The whole argument depends on capacity being demand-constrained. Sustained recovery from July's −4.8% loosens the constraint, lets the denominator recover on its own, and reduces this to a case study about two bad quarters rather than a structural feature. This is management's stated position and it is not unreasonable.

**If a fuel hedging programme is disclosed.** §52's argument that IndiGo cannot hedge effectively without forward demand certainty assumes it does not already hedge materially. No hedging policy was disclosed on the Q1 FY27 call, but absence of disclosure is not absence of programme.

**If Q2's fare increase works.** PRASK guided above 25% on flat capacity. If that lands with load factor holding at or above 83.3%, then the price lever is not exhausted, IndiGo has more pricing power than §24 credits it with, and the urgency behind the proposal drops considerably.

---

## Part 5 — What Could Not Be Found Out

**IndiGo's trip-frequency distribution.** The most consequential gap in this file. It makes A4 an assumption rather than a measurement and leaves §13's sizing indicative only.

**The composition and prior-year value of the other-revenue residual** (§10, D10). The sensitivity band is 64.85% as wide as the figure itself, so it is reported for the current year only and used for nothing.

**Current BluChip enrolment.** Last published March 2025 at 2 million. §47's stress rule treats 1.62% as a floor and says so explicitly.

**Full Q1 FY26 expense-line comparatives** beyond fuel, which prevented a line-by-line bridge of the 34.4% total expense increase and left §18 unable to attribute the ex-fuel cost growth to specific lines.

**Whether IndiGo hedges fuel, and to what extent.** No hedging policy was disclosed on the Q1 FY27 call. Material to §52.

**The expense base underlying IndiGo's CASK definition**, which is why A3 exists.

**Q1 FY27 results for SpiceJet and SNV Aviation (Akasa Air).** Both file; neither had reported for the quarter ended 30 June 2026 at the time of writing. They are named in §14 rather than ignored, and no estimate was constructed for either.

**IndiGo's lease terms and their sensitivity to utilisation**, which would materially sharpen or refute A1 if available.

---

*Day 60 of 90 · Companion to [README.md](./README.md)*
