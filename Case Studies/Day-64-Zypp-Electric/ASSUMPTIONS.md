# Day 64 — Zypp Electric — Assumptions, Derivations and Constructs

Companion to `README.md`. Every derived figure in both files is computed and asserted in `verify.py` (**145 checks, all passing**).

**Entity:** Bycyshare Technologies Private Limited, CIN U63000HR2017PTC070227.
**Basis:** FY2024-25 RoC filings as reported by Entrackr, BW Disrupt, Startuppedia and Inc42; Yulu FY25 RoC filings; Delhi and Karnataka statutory instruments; SEBI statutory provisions; company statements to named journalists; Zypp's own product and franchise pages.

---

## Part 1 — Assumptions

### A1 (load-bearing) — Rider expenses are attributable primarily to the delivery-services line

**The claim.** ₹355 Cr of rider-related expenses maps principally to the ₹323 Cr delivery-services line, making the direct cost of that business **109.91%** of its revenue in FY25 and **115.07%** in FY24.

**Why it is load-bearing.** The entire thesis — that Zypp's growth came from a labour line whose direct cost exceeds its revenue, while the asset line shrank as a share — rests on this attribution. If it fails, the case study still has the mix shift (§18) and the fleet-vs-revenue divergence (§4 derivations), but it loses its sharpest number.

**The rival reading, given equal space.** The source describes rider-related expenses as covering "production, transportation, and operational activities." That is a broad bucket. Vehicles let directly to independent riders under the rental line also incur rider-adjacent operational cost — hub handling, allocation, collection, servicing at handover. If a material share of ₹355 Cr belongs to the rental line, the delivery ratio falls below 109.91% and could fall below 100%. **Zypp has not published a segment-wise cost breakdown, so this cannot be resolved from public sources.** Management's implicit position — that the business is approaching profitability and reached operational profitability from July 2025 — is consistent with the rival reading and is stated in §30 alongside the company's own EBITDA margin.

**Why the case study proceeds anyway.** Three reasons, none of which requires the attribution to be exact. First, the ratio exceeds 100% in **both** years, so a fixed misattribution of constant proportion does not overturn the direction. Second, the mix shift is independently visible and needs no cost attribution at all: rental fell from 28.73% to 25.35% of operating revenue and supplied 18.53% of growth. Third, rider expenses are **63.79% of total expenditure** on a company with an entity-level loss of ₹107.5 Cr — whichever line they sit in, they are the cost that determines whether this business works.

**What would change my mind, and when.** If the FY26 filing or the DRHP breaks rider cost out by segment and delivery-attributed cost lands **below** delivery revenue, A1 is dead and the thesis with it. **Zypp will have to publish that breakdown in a DRHP.** This is the first row of the §55 dashboard for that reason.

---

### A2 — The FOCO payout is a fixed obligation over its 36-month term

**The claim.** ₹1,600–1,900 per vehicle per month is contractually fixed and does not vary with what the vehicle earns.

**Basis.** Consistently described across sources as "assured returns," with a stated monthly payout and a stated three-year total, marketed to individuals, family offices and institutions.

**The rival reading.** All descriptions are marketing and press summaries. **The FOCO contract itself was not obtained.** The payout may be conditional in ways the marketing does not convey — subject to deployment, to force majeure, or to a performance floor. It may also be terminable. A commercial arrangement described as "assured" in a brochure is not necessarily unconditional in its documentation.

**Why it proceeds.** The instrument is marketed on the assurance; the assurance is the product feature being sold. Even if the contract contains conditions, an instrument sold on a fixed monthly number creates a fixed expectation and a reputational obligation, and §50 addresses the sold instrument rather than the drafted one. The §40 discussion is framed as a question throughout for exactly this reason.

---

### A3 — Fleet counts across sources are comparable enough to form a series

**The claim.** 17,000 (Nov 2023) → 22,000 (May 2024) → 20,000 (Nov 2025) → 26,700 usable (Mar 2026) can be read as one series.

**The rival reading.** They are not cleanly comparable. The November 2025 figure of 20,000 is explicitly scoped to three cities; the May 2024 figure of 22,000 aggregated four; "usable fleet" is a different basis again from "vehicles operated." A genuine like-for-like series does not exist publicly.

**Why it proceeds.** The direction is robust under every reading: the fleet has not compounded anywhere near the revenue. Even taking the most flattering pair available (17,000 in Nov 2023 to 26,700 in Mar 2026) the annualised rate is **21.35%** against revenue growth of **49.61%**. The comparability problem is disclosed at Appendix A-8 and the stress rule uses the count the company itself gave alongside its own forward target, which is the most defensible pairing available.

---

### A4 — The ₹250 daily rent is a representative list price

**The claim.** ₹250 per vehicle-day is a reasonable list reference for the derived realisation calculation in §39.

**The rival reading.** Zypp runs daily, weekly and monthly plans that vary by city and vehicle category, and three-wheeler loaders price differently from two-wheelers. A single list number across a mixed fleet is a simplification. The figure comes from one named-journalist report, not from a published rate card.

**Why it proceeds, and how it is handled.** The realisation figure is presented as a **band** (55.29%–71.56% across a 17,000–22,000 fleet), not a point estimate, and §39 gives two competing explanations of the gap equal weight — one about collection and one about the denominator. The conclusion drawn is only that the rental line cannot be reconciled to the fleet at list price, which holds under both.

---

### A5 — Zypp is within the scope of the electrification mandates discussed in §11

**The claim.** The Delhi Motor Vehicle Aggregator and Delivery Service Provider Scheme, 2023 and the CAQM direction of 1 January 2026 are material to Zypp's demand.

**The rival reading.** The mandates bind **delivery service providers and aggregators operating 25+ vehicles** — that is, Zypp's *clients* — more directly than they bind Zypp, which supplies the vehicles. Zypp may benefit as a supplier without being a regulated party itself. Whether Zypp is separately a "delivery service provider" under the scheme, and whether it is an "aggregator" under the Karnataka gig-worker statute, are questions of characterisation that public sources do not settle.

**Why it proceeds.** The case study's use of the mandates is about **demand for electric fleet capacity**, which is unaffected by whether Zypp or its client is the licensed party. Where obligations on Zypp itself are discussed (the Karnataka welfare fee at §57), the uncertainty is stated rather than resolved.

---

## Part 2 — Derivations

All computed in `verify.py`. Inputs are the reported figures in §30 and §18.

**Total expenditure.** Total income + net loss. FY25: 449.0 + 107.5 = **₹556.5 Cr**. FY24: 302.5 + 89.5 = **₹392.0 Cr**. Growth **41.96%**, which reproduces the independently reported "42% increase in total cost" — an internal check on the whole reported set.

**Cost per rupee.** 556.5 ÷ 437.9 = **₹1.2708**, reproducing the independently reported ₹1.27. Two reported figures recovered from two others is what gives confidence the aggregates are internally consistent.

**Rider expense share.** 355 ÷ 556.5 = **63.79%**, reproducing the reported 64%.

**FY24 segment back-derivation.** Delivery 323 ÷ 1.56 = **₹207.05 Cr**; rental 111 ÷ 1.32 = **₹84.09 Cr**; other operating = 292.7 − 207.05 − 84.09 = **₹1.56 Cr**, a small positive residual, which is the expected shape. Rider expense FY24 = 355 ÷ 1.49 = **₹238.26 Cr**.

**A1 ratios.** FY25 355 ÷ 323 = **109.91%**; FY24 238.26 ÷ 207.05 = **115.07%**; improvement **5.16pp**; FY25 rupee gap **₹32.0 Cr**.

**Mix.** Delivery 73.76% (FY24 70.74%); rental 25.35% (FY24 28.73%); rental share change **−3.38pp**.

**Growth decomposition.** Δ operating revenue ₹145.2 Cr; delivery Δ **₹115.95 Cr = 79.85%**; rental Δ **₹26.91 Cr = 18.53%**; other Δ ₹2.44 Cr = 1.68%. Delivery supplied **4.31×** the rupees rental did. Reported segment lines sum to ₹438.0 Cr against ₹437.9 Cr — a **₹0.10 Cr / 0.02%** rounding residual, which makes the decomposition sum to 100.07% rather than 100%. Disclosed, not smoothed.

**Fleet.** 17,000 → 26,700 over 28 months = **+57.06% absolute, 21.35% annualised**. Revenue growth 49.61% is **2.32×** that. Fleet May-24 → Nov-25 = **−9.09%**. FY26 revenue target growth on total income **33.63%** against fleet growth May-24 → Mar-26 of **21.36%** — a ratio of **1.57×**.

**Stress rule.** 20,000 ÷ 100,000 = **20.00%** (generous, used). Alternatives: 20,000 ÷ 200,000 = **10.00%**; 22,000 ÷ 150,000 = **14.67%**; FOCO penetration 500 ÷ 26,700 = **1.87%**. Fleet gap to the standing target: 100,000 − 26,700 = **73,300**, i.e. the target is **3.75×** the usable fleet.

**Rental realisation.** ₹111 Cr ÷ 20,000 = **₹55,500 per vehicle-year = ₹152.05 per vehicle-day = 60.82%** of the ₹250 list. At 17,000: **71.56%**. At 22,000: **55.29%**. Band width **16.27pp**. Implied realised monthly rent at 20,000 fleet: **₹4,625**; list monthly: **₹7,604.17**.

**FOCO.** EV cost from the 100-unit ticket: ₹45 lakh ÷ 100 = **₹45,000**. Independent read from the 500-unit deployment: ₹2.5 Cr ÷ 500 = **₹50,000** — the two agree within 11.1%. Payout per EV-month **₹1,600–1,900, midpoint ₹1,750**. Over 36 months **₹57,600–68,400 = 1.28×–1.52×** capital. Stated three-year total ₹60–66 lakh per 100 EVs = **₹60,000–66,000 per EV**, which **does not reconcile** with the monthly range — logged at Appendix A-4. Payout as share of list monthly rent **23.01%**; of derived realised rent **37.84%**; residual after payout **₹2,875 per vehicle-month** before insurance, maintenance, swap, hubs and idle time.

**Two EBITDA readings.** −15.98% × 437.9 = **−₹69.98 Cr**; −13.20% × 437.9 = **−₹57.80 Cr**; difference **₹12.17 Cr / 2.78pp**. Both negative.

**Yulu mirror.** Revenue growth **98.00%**; rental share **84.67%**; manpower share **5.58%**; loss change **−11.76%** against Zypp's **+20.11%**; EBITDA margins **0.69pp** apart; Yulu's rental share is **3.34×** Zypp's; Zypp revenue **1.84×** Yulu's; Yulu cash fell **93.24%** to ₹9.65 Cr, against Zypp's ₹72.5 Cr — **7.51×** more; Yulu's EBITDA margin improved **64.82pp** off a −80.11% base.

**Operating leverage, which cuts in the company's favour.** Rider cost grew 49.0% and employee cost 43.0% against revenue growth of **49.61%** — both below revenue, giving **0.61pp** and **6.61pp** of genuine operating leverage. The loss still widened, which is the point: leverage on the cost lines was not enough to offset the scale of the base.

**Liquidity.** ₹72.5 Cr ÷ (₹107.5 Cr ÷ 12) = **8.09 months** of FY25 loss run rate; monthly loss **₹8.96 Cr**; cash is **41.55%** of current assets.

**New verticals.** ₹0.30 Cr + ₹0.60 Cr = **₹0.90 Cr = 0.15%** of the ₹600 Cr FY26 target and **0.21%** of FY25 operating revenue. Advertising per vehicle-year **₹112.36 = ₹9.36 per vehicle-month**, below the lowest FleetEase.ai list price of ₹149. At this rate it takes **119.44 years** of new-vertical revenue to equal one year of FY25's loss.

**Statutory ceiling.** ₹100 Cr ÷ ₹45,000 = **22,222 vehicles**. Required gap 73,300 is **3.30×** that; only **30.32%** of the gap is fundable below the threshold; today's 500 vehicles are **2.25%** of it.

---

## Part 3 — Constructs

Author-created. None of this is a Zypp disclosure.

**CVD/1k — Contribution-Verified vehicle-Days per 1,000 deployed vehicle-days.** Conjunctive on four conditions (§31). The denominator is *deployed* vehicle-days so that adding a vehicle which does not earn **lowers** the metric — the inverse of fleet size, deliveries completed and cities entered, all of which rise on asset addition alone. A 26,700 fleet over a year is **9,745,500 deployed vehicle-days**, so one point of CVD/1k is **9,745.5 vehicle-days**.

**RIS-90 — Rider Income Stability at the 90th percentile of rent-repricing intensity.** In the decile of weeks where the earnings-linked rent formula moves most, the share of active riders whose post-rent take-home stays within a published band. Reported by city and by client platform, never in aggregate. Owned by a Rider Economics function with no revenue target.

**Zypp Ledger.** Three components — the per-vehicle contribution ledger, the floor-plus-share instrument replacing the assured payout, and quarterly publication of the contribution distribution including the bottom decile.

**RICE set and stress rule.** Four initiatives, scores and the 20.00% multiplier, with exemption granted only where value accrues without any party changing behaviour. `verify.py` asserts that the proposal is the weakest non-exempt initiative at baseline — the only configuration in which it can finish last honestly.

**Phase 0 kill criteria K1–K3**, with K2 named as the one most likely to fire; the three-arm test and its pre-registered decision rule; the §52 wireframe and every figure in it.

**The FOCO scaling scenario.** ₹329.85 Cr of third-party capital and **₹153.93 Cr a year** of assured payouts to fund the 73,300-vehicle gap; ₹450 Cr and **₹210 Cr a year** for the full 100,000. Those are **25.66%** and **35.00%** of the ₹600 Cr FY26 revenue target, and the annual payout on the gap alone is **1.43×** FY25's entire net loss. **This is a construct, not a plan. Zypp has not stated that it intends to fund its fleet target through FOCO at scale**, and the programme stands at 500 vehicles — 1.87% of the March 2026 fleet. The scenario exists to size an obligation, not to predict one.

---

## Part 4 — What Would Change My Mind

1. **A segment-wise cost breakdown showing delivery-attributed rider cost below delivery revenue.** Kills A1 and the thesis. Most likely to appear in the DRHP.
2. **Rental revenue growing faster than delivery revenue in FY26.** The mix argument reverses; the asset business is genuinely growing.
3. **A published FOCO contract showing the payout is contingent on deployment or performance.** The "fixed obligation" framing weakens substantially and §50 becomes a reporting proposal rather than an instrument proposal.
4. **Fleet reaching or approaching 26,700 usable and then compounding above 40%.** The execution record that sets the 20.00% stress rule stops being predictive, and the RICE result changes.
5. **FY26 landing at or near ₹600 Cr with positive EBITDA on an audited basis.** The company's own account of its trajectory is vindicated and the "spends ₹1.27 to earn ₹1" framing becomes historical.
6. **A DRHP disclosing FOCO obligations as a liability with an explicit characterisation opinion.** Closes the §40 question in either direction, which would be a better outcome than leaving it open.

---

## Part 5 — What Could Not Be Found Out

- **The FOCO contract.** Every quantitative statement about the instrument rests on marketing descriptions and press interviews. This is the single largest evidentiary gap.
- **Segment-wise cost allocation.** Not disclosed; A1's central weakness.
- **Rider retention, churn and utilisation.** Not disclosed at any level. Cumulative onboarding figures exist; daily actives are quoted; retention is not.
- **The rent schedule.** The earnings-linked rule is marketed; the bands, revision frequency and ceiling are not published.
- **Vehicle acquisition cost from Odysse and e-Sprinto.** Explicitly declined by the CEO when asked.
- **FY26 audited figures.** Not yet filed as at 30 August 2026. Everything about FY26 in this case study is a company target or a company statement, labelled as such.
- **Client concentration.** No disclosure of what share of delivery revenue comes from the largest one, three or five platforms — which, given that those platforms set the per-order economics, is the most consequential missing number after segment costs.
- **Whether Zypp is a scheduled "aggregator" under the Karnataka gig-worker statute**, and therefore whether the 1% welfare fee applies to its rider payouts directly.
- **Comparable FY25 financials for Alt Mobility, EVeez, Baaz or Magenta Mobility.** No filings located, so §14 names them without sizing them and constructs no estimates.
