# ASSUMPTIONS — Day 61: Atomberg (Atomberg Technologies)

Companion to `README.md`. Everything in the case study that is *not* a directly disclosed figure is listed here: what was assumed, how each derived number was computed, what was constructed by the author, what would falsify the thesis, and what could not be found out.

Every derived figure in both files is verified programmatically. `verify.py` — **92 checks, all passing** — is delivered with this case study but not committed to the repository.

---

## Part 1 — Assumptions

### A1 (load-bearing) — That the widening gap between adjusted EBITDA and net loss reflects a deliberate, continuing capital commitment rather than a one-year accounting event

**What is assumed.** §16 reads the growth of the gap between adjusted EBITDA loss and net loss — ₹66.40 Cr to ₹111.88 Cr, **+68.49%** against revenue growth of 34.84% — as the accounting footprint of Atomberg's shift from a design-and-outsource model to a manufacture-and-own one, and reads the Voltas JV as evidence that the shift continues.

**The rival reading, given equal weight.** A single year is a single year. The gap could widen because of a lease renegotiation, an accelerated write-down of tooling for a discontinued SKU, a one-off borrowing to fund working capital ahead of a listing, or a deferred-tax adjustment — none of which would indicate a strategic direction. **₹40.88 Cr of the gap is finance cost and tax that is not separately broken out**, and a further ₹12.77 Cr of FY26's result is unreconciled entirely (§18, A-2). A reader could reasonably say the case study has built a strategic narrative on a line item it cannot fully decompose.

**Why the case study proceeds anyway.** Two independent, non-accounting facts point the same way. Atomberg operates a components subsidiary and sells proprietary components as a revenue line, so vertical integration is disclosed strategy rather than inference. And the Voltas JV — announced the same day as the DRHP — commits the company to compressor manufacture with an anchor customer. The accounting is consistent with a strategy the company has separately announced twice.

**What would kill it, and when.** If FY27's gap grows **more slowly than revenue**, the widening was a one-year effect and A1 is dead. Atomberg will publish both numbers; no interpretation is required. This is the first row of §55.

### A2 (medium) — That FY25 comparatives back-derived from growth rates are close enough to use

Several FY25 figures are reconstructed from disclosed growth rates rather than stated absolutes. Disclosed rates are rounded, so each carries error.

**Where this is acceptable:** the materials-cost finding in §16. Materials grew 37.94% against revenue's 34.84%; the 3.11-point difference would have to be wrong by more than three points — far outside any plausible rounding on figures of this size — to reverse the conclusion that materials outgrew revenue.

**Where it is weaker:** the segment growth contributions in §17. Fans at 64.62% of growth and kitchen at 31.32% are computed from four reconstructed base figures, and the second decimal place should not be relied on. The *ordering* — fans supplying less of the growth than of the revenue — is robust; the precision is not.

### A3 (medium) — That the ₹40.88 Cr residual is finance cost and tax

The gap between adjusted EBITDA loss and net loss less D&A of ₹71 Cr leaves ₹40.88 Cr. Finance cost and tax are the only conventional candidates at that position in the P&L, but neither is separately disclosed in the summaries available. The case study says "finance cost and tax" and flags it (A-2) rather than asserting a split. Note the direction of the assumption: if any part of that residual is a one-off, A1 weakens.

### A4 (author-constructed, explicitly unverified) — That a bulk and institutional channel exists at a size worth addressing

§50's proposal concentrates its value in buyers who fit many fans into buildings whose electricity they do not pay for. **Atomberg discloses no channel split between retail and bulk.** The existence of such a channel is inferred from the presence of 626 distributors and direct dealers, which is a weak inference — most of those serve retail. This is the single largest hole in the proposal, it is named as §53's K2, and it is the criterion the case study bets will fire.

### A5 (medium) — That the labelling regime materially eroded Atomberg's differentiation

§8 argues that mandatory standards and labelling converted a private, unverifiable claim into a public specification, and §14 supports it with Crompton's own attribution of share gains to BLDC. The counter-argument is that Atomberg's advantage was never purely informational — motor design, cost and quality are real, and a label does not hand a competitor a good motor. The case study's position is that labelling removed the *verification* barrier rather than the *engineering* one, which is a narrower claim and the one the evidence supports.

### A6 (low, non-load-bearing) — That the 46.08% premium-fan share is not a fan-market share

Treated throughout with its three qualifiers intact (§13, A-5). Nothing in the case study depends on the figure; it is reported because the company reports it.

---

## Part 2 — Derivations

All labels correspond to check IDs in `verify.py`.

**D1 — the opposing signals.** Adjusted EBITDA loss ₹51.4 Cr → ₹37.12 Cr = **−27.78%** (improving). Net loss ₹117.8 Cr → ₹149 Cr = **+26.49%** (worsening). EBITDA loss improved 18.03%. Adjusted EBITDA margin −5.36% → **−2.87%**. Disclosed EBITDA margins of −6.35% and −3.86% reconcile to the loss and revenue figures within 0.02 points.

**D2 — the mechanism.** Gap = net loss less adjusted EBITDA loss: **₹66.40 Cr (FY25) → ₹111.88 Cr (FY26), +68.49%**. Revenue growth **34.84%**. Ratio **1.97×**. D&A ₹71 Cr = **5.49% of revenue** and **63.46% of the gap**; residual **₹40.88 Cr**.

**D3 — the reconciliation residual.** Total income ₹1,323.77 Cr less total expenditure ₹1,460 Cr = **−₹136.23 Cr** against a reported net loss of ₹149 Cr ⇒ **₹12.77 Cr** unexplained. FY25 equivalent **₹0.80 Cr**. Ratio **15.96×** — which is why FY26's is flagged and FY25's is not.

**D4 — product economics.** Materials growth **37.94%**, exceeding revenue growth by **3.11 points**; materials **55.76% → 57.04%** of revenue (**+1.28 points**). Cost per ₹1 of revenue **₹1.1652 → ₹1.1285**. Employee cost growth **32.08%**, below revenue by 2.76 points. Advertising **10.43%** and R&D **6.71%** of revenue.

**D5 — segment mix.** Fans **89.12%** of revenue, kitchen **9.58%**, components **1.33%** (the stress rule). Growth: fans **+23.05%**, kitchen **6.42×**, components **4.74×**. Contribution to the ₹334.27 Cr of absolute growth: fans **64.62%**, kitchen **31.32%**, components **4.06%**. Fans' revenue share exceeds its growth share by **24.50 points**. Online **35.28%** of revenue.

**D6 — the competitive mirror.** Crompton revenue **6.26×** Atomberg's; adjusted EBITDA margin gap **17.87 points**; Crompton ECD ≈ **₹6,072 Cr**, **5.27×** Atomberg's fan business; revenue per unit **+38.76%**; premium mix **+7 points**; FY22–FY26 revenue **+50.09%**. Crompton's own adjusted margin **fell 1.6 points** over the same window, and its reported margin sits **4.8 points** below its adjusted one.

**D7 — the IPO.** Named uses ₹340 Cr = **75.56%** of the ₹450 Cr fresh issue; residual ₹110 Cr general corporate. Marketing ÷ R&D = **1.5×**; marketing ÷ FY26 advertising spend = **1.11×**. Fresh issue = **3.02×** FY26 net loss. Debt repayment **20%** of the fresh issue. Cash ₹41 Cr = **3.30 months** of FY26 losses.

**D8 — scale.** Implied permanent workforce **1,003** (254 R&D engineers ÷ 25.32%). Revenue per permanent employee **₹1.29 Cr**. Retail touchpoints per distributor **74.97**; per city **29.33**. R&D spend per R&D engineer **₹0.34 Cr**.

**D9 — the regulatory mechanism.** Against the 72.5W midpoint of the cited 70–75W range: super-efficient (35W) saves **51.72%**; the regulated floor (55W) saves **24.14%**. The floor therefore delivers **46.67%** of the super-efficient saving — nearly half of Atomberg's original pitch, mandated for everyone. 1-star plus 5-star models were **85%** of registrations in June 2022.

**D10 — RICE.** Reach in ₹Cr of FY26 revenue touched; Effort in person-quarters; stress multiplier **0.013295** applied to Reach for stressed initiatives only. Baseline: distribution **80.71**, kitchen **49.60**, Proof **19.41**, BEE **13.75**. Stressed: BEE **13.75** (exempt), distribution **1.07**, kitchen **0.66**, Proof **0.26**. **Proof 3rd → 4th and last**, and `verify.py` asserts programmatically that Proof is the weakest *stressed* initiative at baseline — the only configuration in which the demotion can occur.

---

## Part 3 — Constructs

Everything below is the author's, not Atomberg's, and none of it should be read as reported fact.

**The thesis itself** — that Atomberg's differentiation was informational, that mandatory labelling dissolved it, and that vertical integration is a deliberate substitution of ownership for knowledge whose cost is invisible in the company's headline metric. Atomberg does not describe its position this way, and Crompton's BLDC attribution is used as corroboration, not as Atomberg's own admission.

**Personas** (§11) — constructed from disclosed operating data and the product portfolio. No primary research, no published segmentation.

**Jobs To Be Done** (§33) and **Kano classifications** (§34) — constructed. The claim that efficiency completed a migration from *attractive* to *must-be* is an argument built on §8, not an observation.

**The entire Atomberg Proof proposal** (§50–52) — on-device metering, the pre-registered immutable baseline, third-party audit, per-SKU per-climate-zone publication including the underperforming decile, and savings-linked bulk procurement contracts. None of this exists or has been proposed by Atomberg.

**MSF/1k** (§31) — the metric, its four conjunctive conditions, and the choice of *installed fan-years* as denominator.

**CMG-90** (§40) — the guardrail, its 90th-percentile construction, the by-climate-zone reporting rule (§41), the Verification function, the build-pipeline firewall, and the two-quarter withdrawal trigger.

**The privacy constraint** (§40, §51) — that aggregate totals leave the device and timestamped duty cycles do not. This is the author's design choice, made because a fan reporting run-hours is an occupancy sensor.

**The three permanently excluded incentives** (§48).

**All RICE inputs** (§47) — every Reach, Impact, Confidence and Effort value, the choice of which four initiatives to compare, and the decision to exempt BEE re-registration from stress. The stress *rule* (1.33%) is a disclosed figure; using it as a stress rule is the author's judgement.

**All kill criteria and thresholds** (§53–54) — the 20% metered-versus-rated shortfall, the 2,000-installation and three-climate-zone pilot floor, the 50% baseline-capture threshold, the 10-percentage-point R1 rule, and the two-analyst-week budget.

**The Porter's double run across fans and components** (§39), including the judgement that the two halves invert on nearly every force.

---

## Part 4 — What Would Change My Mind

**The decisive test, and Atomberg will publish it.** If FY27's gap between adjusted EBITDA and net loss grows **more slowly than revenue**, the capital intensity is being absorbed, A1 is wrong, and the thesis fails.

**If materials cost falls back below 55.76% of revenue**, the product-economics finding in §16 was a one-year sourcing effect rather than erosion, and half of the case study's diagnosis goes with it.

**If K2 fires** and the bulk or institutional channel is immaterial to Atomberg's revenue, Atomberg Proof has no buyer worth serving and should not be built. This is named in §53 as the criterion most likely to fire.

**If Crompton's fan share gains stall while its margin keeps falling**, §14's reading inverts: the incumbent would be buying share at a price it cannot sustain, and Atomberg's competitive position would be considerably stronger than this file credits.

**If the Voltas JV proves capital-light** — a licensing or technology arrangement rather than a plant Atomberg part-funds — then §22's characterisation of the pivot as capital-hungry is overstated. The terms are undisclosed, so this is a genuine open question.

**If components revenue scales sharply from ₹17.2 Cr**, §47's stress rule is too harsh, the RICE demotion is an artefact of a stale multiplier, and Atomberg Proof deserves a better hearing than this file gives it.

---

## Part 5 — What Could Not Be Found Out

**Atomberg's channel split between retail and bulk or institutional sales.** The most consequential gap. It makes A4 an assumption rather than a measurement and leaves §13's sizing indicative only.

**Unit volumes, in any category, in any year.** Price and mix cannot be separated from volume anywhere in this file, which is a material limitation for a hardware company and the reason §16 works entirely in ratios.

**The Voltas JV's investment, capacity, location and timeline.** The 2.8 million compressor figure appeared in coverage but not in either company's own announcement (A-3).

**The finance-cost and tax split** inside §16's ₹40.88 Cr residual, and the composition of §18's ₹12.77 Cr FY26 reconciliation residual.

**FY24 financials**, which would turn every single-year comparison here into a trend. Two of the three years a trend needs are present.

**Whether existing motors can be instrumented without a hardware revision** — the difference between a firmware release and a product cycle, and therefore between a cheap experiment and an expensive one.

**The DRHP document itself.** This analysis works from DRHP-derived financial summaries reported by multiple independent outlets, not from the prospectus. The full document would supersede several readings here, particularly §18's expense reconciliation.

**Any post-March-2026 figures**, which do not exist publicly until the company lists and reports.

---

*Day 61 of 90 · Companion to [README.md](./README.md)*
