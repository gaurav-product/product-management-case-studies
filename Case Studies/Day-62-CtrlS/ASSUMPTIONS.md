# ASSUMPTIONS — Day 62: CtrlS Datacenters

Companion to `README.md`. Everything in the case study that is *not* a directly disclosed figure is listed here: what was assumed, how each derived number was computed, what was constructed by the author, what would falsify the thesis, and what could not be found out.

Every derived figure in both files is verified programmatically. `verify.py` — **86 checks, all passing** — is delivered with this case study but not committed to the repository.

**One framing note before anything else.** This is the first case study in the series built entirely on **rating rationales rather than company filings**. CtrlS is private, publishes no results, and has no DRHP on file. ICRA's documents are independent and rigorous, but they are written for a credit audience: they disclose ratios where a filing would disclose lines. Several figures below are therefore *derived from ratios* rather than read off a statement, and each is flagged.

---

## Part 1 — Assumptions

### A1 (load-bearing) — That the FY24→FY25 result is evidence about the FY27–FY28 plan

**What is assumed.** §16 reads one year — revenue +16.65%, OPBDITA +23.90%, PAT +0.00%, interest coverage 5.3× → 3.9× — as indicative of what a capex programme **2.91× larger** will do to the same P&L.

**The rival reading, given equal weight.** One year is one year, and the mechanism is timing rather than economics: in a capacity business, interest and depreciation begin when a building is commissioned and revenue ramps over the following quarters. A single year in which several buildings landed will always show exactly this pattern, and it says nothing about steady-state returns. On this reading CtrlS is not failing to convert growth — it is mid-build, which is what mid-build looks like, and the larger programme simply extends the same J-curve.

**Why the case study proceeds anyway.** Three reasons, none conclusive alone. The pattern held across **two consecutive years of flat PAT** (₹248 Cr, ₹248 Cr), not one. The **independent comparator did the same thing harder** — Sify grew EBITDA 30.53% and its loss widened 74.01% (§14) — which is what a structural cause looks like and not what an idiosyncratic build schedule looks like. And the **forward arithmetic is not a projection but a definition**: at 62.5% debt funding, holding leverage at 4× requires OPBDITA of ₹2,806 Cr against ₹969 Cr, which follows from the disclosed numbers regardless of J-curve timing.

**What would kill it, and when.** If FY26 PAT grows materially on ₹248 Cr while leverage rises, the J-curve reading is right and A1 is dead. ICRA publishes both. This is the first row of §55.

### A2 (medium) — That the later rationale's figures should be used where the two disagree

The September 2025 and May 2026 documents differ on FY25 operating income (₹1,567 Cr vs ₹1,562 Cr, **0.32%**) and on FY24/FY25 PAT (₹256/₹251 Cr vs ₹248/₹248 Cr). The later document is used throughout, on the standard assumption that a rating agency's most recent restatement supersedes.

**The finding does not depend on the choice.** On the earlier vintage, revenue grew **17.03%** and PAT **fell 1.95%**; on the later, **16.65%** and **0.00%**. Both say growth did not reach profit. `verify.py` checks both vintages explicitly for this reason.

### A3 (medium) — That interest expense can be derived from interest coverage

§16 and §19 compute interest as OPBDITA ÷ disclosed interest coverage, giving ~₹118.0 Cr (FY24) and ~₹198.7 Cr (FY25). This is arithmetically sound given both inputs are disclosed, but **ICRA's coverage definition may include or exclude items this treatment does not capture** — capitalised interest during construction being the most likely.

The *level* should therefore be treated as indicative. The **direction and relative magnitude** — interest rising far faster than revenue, absorbing 53.98% of the EBITDA increase — are robust to any plausible definitional difference, and that is all the thesis uses.

### A4 (author-constructed, explicitly unverified) — That enterprise capacity earns a meaningful premium over hyperscale

The entire proposal in §50 assumes there is a margin book worth defending: that a Tier-4 rack sold to a bank earns materially more per megawatt than wholesale capacity pre-leased to a hyperscaler. **CtrlS discloses no price split.** The inference rests on the 49.6% blended margin against Sify's 22.0% (§14) and on the general structure of the colocation market, both of which are suggestive rather than probative.

This is the largest hole in the proposal. It is **K1** in §53, checkable in days from contracts CtrlS already holds, and if it fires the proposal has no economic basis at all.

### A5 (medium) — That "a hyperscaler" means concentration is increasing

ICRA writes that incremental capacity is "pre-leased with a hyperscaler." §23 and §39 read the singular as meaningful. It may be generic phrasing covering several counterparties, in which case concentration is materially less acute than the case study implies. Named in §63 as unresolved.

### A6 (low, non-load-bearing) — That midpoints are adequate for range-disclosed figures

Capex (₹4,550 Cr, ₹13,250 Cr), capacity target (975 MW), build rate (42.5 MW/yr), FY26E margin (51%) and debt share (62.5%) are all midpoints of disclosed ranges. Ratios are reported to two decimals for reproducibility, not because the precision exists. Where a range would change a conclusion, both ends are given (§21, §47).

---

## Part 2 — Derivations

All labels correspond to check IDs in `verify.py`.

**D1 — the cascade.** OPBDITA = operating income × margin: **₹625.31 Cr (FY24) → ₹774.75 Cr (FY25) → ₹969.00 Cr (FY26E)**. Revenue growth **16.65%**; margin expansion **+2.9pp**; OPBDITA growth **23.90%**, an increase of **₹149.44 Cr**; PAT growth **0.00%**. PAT growth as a share of OPBDITA growth: **zero**.

**D2 — where it went.** Implied interest = OPBDITA ÷ coverage: **₹117.98 Cr → ₹198.65 Cr**, an increase of **₹80.67 Cr (+68.38%)** — **53.98%** of the OPBDITA increase. Coverage deteriorated **26.42%**. Implied total debt at FY25 = OPBDITA × 3.8 = **₹2,944.06 Cr**.

**D3 — the plan change.** Capex midpoints **₹4,550 Cr (FY26–28, 3 years)** vs **₹13,250 Cr (FY27–28, 2 years)** = **2.91×** total and **4.37×** annualised (₹1,516.67 Cr/yr → ₹6,625 Cr/yr). Capacity: guided **42.5 MW/yr** vs required **(975 − 150) ÷ 3 = 275 MW/yr** = **6.47×**. Target is **6.5×** current capacity. Delivered March 2024 → August 2025 was **43 MW over 17 months = 30.35 MW/yr**.

**D4 — the stress rule.** Demonstrated ÷ required = 42.5 ÷ 275 = **15.45%**. Using delivered rather than guided capacity: 30.35 ÷ 275 = **11.04%**. The more generous figure is used in §47.

**D5 — what the plan requires.** New debt = ₹13,250 Cr × 62.5% = **₹8,281.25 Cr**. Implied total debt = ₹2,944.06 + ₹8,281.25 = **₹11,225.31 Cr**. To hold Debt/OPBDITA at 4×, OPBDITA must reach **₹2,806.33 Cr = 2.90×** FY26E, implying revenue of **₹5,502.60 Cr** at the FY26E margin — also **2.90×**. Undrawn facilities of ₹4,665 Cr cover **56.33%** of the new debt. Capex per megawatt added: ₹13,250 Cr ÷ 825 MW = **₹16.06 Cr/MW**.

**D6 — the comparator.** Sify FY26 revenue **₹4,487.70 Cr (+12.51%)**; segments sum exactly to the total; DC revenue **₹1,751.90 Cr**, **1.12×** all of CtrlS. EBITDA **₹987.10 Cr, +30.53%**, margin **22.00%** — CtrlS's 49.6% is **2.25×** it. Net loss **₹136.60 Cr, +74.01%**. Borrowings less cash reconcile to net debt of **₹3,353.40 Cr** exactly. FY27 contracted MW is **4.76×** FY26 sold MW.

**D7 — the vintage conflict, quantified.** FY25 revenue differs by **₹5 Cr (0.32%)**; FY24 PAT by ₹8 Cr; FY25 PAT by ₹3 Cr. Earlier vintage: revenue **+17.03%**, PAT **−1.95%**. Both vintages show PAT growth ≤ 0. Rated amount enhanced **48%** (₹2,500 Cr → ₹3,700 Cr).

**D8 — concentration and scale.** Top 10 = **₹968.44 Cr** of FY25 OI, averaging **₹96.84 Cr** each; the rest is **₹593.56 Cr**. Revenue per operational MW at FY26E = **₹12.67 Cr**. Total sites 17 + 7 = **24**. Kamath's share of the raise **80%**; the raise is **1.89%** of the FY27–28 capex plan.

**D9 — RICE.** Reach in ₹Cr of FY26E revenue touched; Effort in person-quarters; stress **0.154545** applied to Reach for stressed initiatives only. Baseline: hyperscaler BTS **171.00**, enterprise attach **151.62**, proposal **35.63**, power PPA **31.40**. Stressed: power PPA **31.40** (exempt), BTS **26.43**, attach **23.43**, proposal **5.51**. **Proposal 3rd → 4th and last**, and `verify.py` asserts programmatically that it is the weakest *stressed* initiative at baseline — the only configuration in which the demotion can occur.

---

## Part 3 — Constructs

Everything below is the author's. Neither CtrlS nor ICRA characterises the business this way.

**The thesis** — that growth is stopping at the interest line, that the plan multiplied while the evidence about the smaller plan was already in, and that pre-leasing relocates risk into counterparty leverage rather than removing it.

**Personas** (§11) — three segments constructed from ICRA's description of the client mix. No primary research; no published segmentation.

**Jobs To Be Done** (§33), **Kano classifications** (§34), and the claim that Tier-4 is worth least to the customer taking all incremental capacity (§26).

**The entire CtrlS Regulated Capacity proposal** (§50–52) — the reserved share, the three-quarter window, the published enterprise floor, external disclosure to lenders, automatic release on breach, and the pilot design.

**EMW/100** (§31) — the metric, its four conjunctive conditions, and the choice of *commissioned* megawatts as denominator.

**VUR-90** (§40) — the guardrail, its 90th-percentile construction, the three-quarter vacancy window, reporting by customer size band (§41), and the automatic-release trigger.

**The Capacity Stewardship function** (§58) and the three permanently excluded incentives (§48).

**All RICE inputs** (§47) — every Reach, Impact, Confidence and Effort value, the choice of the four initiatives, and the decision to exempt power procurement from stress. The stress *rule* (15.45%) is derived from disclosed figures; using it as a stress rule is the author's judgement.

**All kill criteria and thresholds** (§53–54) — the 25% enterprise premium, the 10% reserved share, the three-city pilot, the 6-percentage-point R1 rule, the 60% fill-rate success criterion, and the two-analyst-week budget.

**The Porter's double run across hyperscale and enterprise** (§39), including the judgement that enterprise is the better business on four of five forces.

---

## Part 4 — What Would Change My Mind

**The decisive test, and ICRA will publish it.** If FY26 PAT grows materially on two consecutive years at ₹248 Cr while leverage rises, the J-curve reading in A1 is correct and the thesis fails.

**If K1 fires** and enterprise capacity carries no real premium over hyperscale, there is no margin book to defend, the 49.6% margin is explained by something else, and the proposal is solving an imagined problem. This is the largest single risk to the argument.

**If FY27 commissioned capacity lands near 275 MW**, the execution concern in §21 is wrong and §47's stress rule is far too harsh — in which case the proposal's demotion to last is an artefact of a bad multiplier rather than a real finding.

**If top-10 concentration falls** while the build accelerates, ICRA's singular "a hyperscaler" was generic phrasing, A5 is wrong, and §23's premise weakens considerably.

**If a DRHP appears with a disclosed enterprise-versus-hyperscale split**, most of what is assumed here becomes checkable — the outcome this case study would most welcome.

**If ICRA's next rationale shows interest coverage stabilising** above 3.9× through the build, then the financing structure is absorbing the capex better than §19 implies and the urgency behind the proposal drops.

---

## Part 5 — What Could Not Be Found Out

**The enterprise-versus-hyperscale price split.** The most consequential gap; it makes A4 an assumption, is K1 in §53, and prevents §52 from being modelled at all.

**CtrlS's CIN and registry record.** Every case study from Day 46 onward cited one. This one could not, and §2 states the absence rather than quoting an unverified aggregator entry (A-1).

**PUE, power tariffs, renewable mix and land bank** — none disclosed in either rationale, which is why §42 makes no quantitative claim and §47's exempt initiative is sized on judgement.

**Actual interest expense, depreciation and tax.** All derived or inferred from ratios (A3).

**FY26 actuals.** ₹1,900 Cr is ICRA's estimate; everything forward of FY25 is projection.

**Whether "a hyperscaler" is one counterparty or several** (A5) — the difference between acute and manageable concentration.

**The IPO's size, timing and structure** beyond press reports of ~$300 Mn by FY27, and **the terms of the August 2026 ₹250 Cr raise** — valuation, stake, instrument.

**Any segment P&L, unit volumes, or per-customer economics**, none of which a rating rationale is written to provide.

---

*Day 62 of 90 · Companion to [README.md](./README.md)*
