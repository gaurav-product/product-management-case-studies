# ASSUMPTIONS — Day 65, Vodafone Idea Limited

Companion to `README.md`. Everything in the case study that is not a directly reported figure is derived, assumed or constructed, and this file says which, and how.

**Entity:** Vodafone Idea Limited · CIN L32100GJ1996PLC030976
**Primary period:** Q1 FY27, quarter ended 30 June 2026, reported 10 August 2026
**Verification:** `verify.py`, 139 checks, all passing

---

## Part 1 — Assumptions

### A1 (load-bearing) — The VLR gap is a product-position fact, not an artefact

**The assumption.** That Vi's 83.98% peak-VLR ratio, against 99.27% at Airtel and 99.07% at Jio, reflects Vi occupying the *secondary* SIM slot in a large share of Indian dual-SIM households — and that this is a durable structural position rather than a measurement quirk or a lagging indicator of past churn.

**Why it proceeds.**
- The gap is enormous and stable, not noisy: 85.28% (Jan) → 85.24% (Feb) → 85.26% (Apr) → 84.41% (May) → 83.98% (Jun 2026), falling monotonically over the last three readings.
- It is published by the regulator on an identical basis for all operators, so it is not a definitional difference between companies.
- The obvious alternative explanation fails on the competitor's own data: Airtel carries **1.56×** Vi's M2M intensity (17.00% of base vs 10.87%) and still registers 99.27%.
- Even granting the most generous version of that alternative — treating *every one* of Vi's 21.62 mn M2M connections as non-registering — a residual of **10.23 mn** unexplained inactive connections remains, still **1.24×** Airtel's and Jio's total inactive pools combined.
- Every other Vi metric is consistent with a secondary-SIM position: ARPU below both rivals, data per user 63.08% of Airtel's, and the ability to add connections while losing active users.

**The honest rival reading, given equal weight.** Vi's own account is that this is a *recovery in progress*: five consecutive months of net additions from February 2026, driven by network investment reaching new users, with activation naturally lagging acquisition. On that reading the VLR ratio is a trailing indicator that will improve as new cohorts mature and as 4G coverage reaches the 63.0 mn connections still on 2G. This reading is coherent, is management's stated position, and cannot be dismissed from outside.

**Why the case study still proceeds.** Because the two readings make opposite predictions about the same monthly published number, and the last three readings went the wrong way for management's. Acquisition and activation moved in opposite directions for five consecutive months; a genuine lag would show the ratio flattening, not falling.

**The weakest point, stated plainly.** Vi does not disclose primary-versus-secondary SIM position and no external dataset establishes it. The secondary-SIM diagnosis is **inferred from converging indirect evidence, not observed**. It is graded 🟠 in Appendix B for that reason, and every derived figure in the case study stands independently of it — the VLR gap, the inactive pool and the M2M falsification are all true whatever causes them.

**Early warning that would kill A1.** If Vi's VLR ratio rises for two consecutive months while net additions stay positive, the lag reading is correct and A1 is dead. TRAI publishes the number monthly, roughly four weeks after month-end, so this is falsifiable on a known schedule without Vi's cooperation.

### A2 — The stress rule's dormancy behaviour still holds

That the 90% never-return rate at 60 days of non-usage, which Vodafone filed with TRAI, remains approximately true in 2026. **This is the weakest sourced input in the case study.** The submission is a pre-merger Vodafone document of approximately 2012 vintage (it references DoT's July 2011 numbering circular and states that periodic SMS had been sent "from Aug 2011"). The 2026 market differs materially: minimum recharge has risen roughly twentyfold, dual-SIM ownership is far more common, and the OTP economy did not exist in its current form.

Mitigation: the **more generous** of the two available readings is used — 10.00% from the 60-day figure rather than 20.00% from the 30-day one — so the stress rule is softer on the proposal than the source supports, not harsher. No more recent figure was found.

### A3 — The two subscriber bases are not reconciled

Vi reports 193.1 mn subscribers at 30 June 2026; TRAI reports 198.82 mn on the same date. The 5.72 mn (2.96%) gap is not explained by either party. The direction is notable: **Jio's company figure (533.3 mn) sits above TRAI's (503.58 mn), while Vi's sits below** — so this is not a single industry-wide definitional offset.

No attempt is made to resolve it. D1 is computed on **both bases independently**, giving 7.67 active users lost per connection gained on the company basis and 6.88 on the TRAI basis. The finding survives either.

### A4 — Q1 FY26 comparatives are as restated in the Q1 FY27 release

Revenue of ₹11,023 Cr for Q1 FY26 is taken from the Q1 FY27 release; the original Q1 FY26 release reported ₹11,022.5 Cr. The 0.5 Cr difference is rounding and affects the YoY growth calculation in the fourth decimal only (6.0419% computed vs 6.0437% on the unrounded figure). Immaterial, but stated.

### A5 — The exceptional gain is non-recurring

That the ₹1,816 Cr gain on remeasurement of settlement assets does not repeat. Vi does not guide on this. The assumption is conservative in the direction that matters: if it *does* repeat, the underlying loss is worse relative to the headline than stated, which strengthens rather than weakens §5's reading.

---

## Part 2 — Derivations

All figures below are computed in `verify.py` and reproduced from its printed output.

### D1 — Connections up, active users down

| Basis | Total change | Active change | Active lost per connection gained |
|---|---|---|---|
| Company (192.8→193.1; 169.3→167.0 mn) | **+0.30 mn** | **−2.30 mn** | **7.67×** |
| TRAI (198.485→198.823 mn; 169.31→166.97) | **+0.338 mn** | **−2.34 mn** | **6.88×** |

The March 2026 TRAI base (198.485 mn) is back-derived by subtracting April's disclosed net additions (53,257) from the disclosed April base (198,538,052). Cross-check: Vi's company-reported Q4 FY26 VLR of 169.3 mn against that base implies a March VLR ratio of **85.30%**, consistent with the published 85.26% (April) and 85.24% (February).

Independent confirmation that the two datasets agree on *activity*: TRAI's June base × 83.98% = **166.97 mn**, against Vi's reported 167.0 mn. The bases disagree; the active counts do not.

### D2 — The inactive pool

| Operator | Base (mn) | Active (mn) | Inactive (mn) | Inactive % |
|---|---|---|---|---|
| Vodafone Idea | 198.82 | 166.97 | **31.85** | **16.02%** |
| Bharti Airtel | 486.80 | 483.23 | 3.57 | 0.73% |
| Reliance Jio | 503.58 | 498.89 | 4.69 | 0.93% |

- Vi inactive ÷ (Airtel + Jio inactive) = **3.86×**, on a base **20.08%** of theirs.
- Vi inactive *share* ÷ Airtel's = **21.84×**; ÷ Jio's = **17.20×**.

### D3 — Market share, two ways

| Operator | Share of connections | Share of active users | Difference |
|---|---|---|---|
| Vodafone Idea | **15.50%** | **13.90%** | **−1.60 pp** |
| Bharti Airtel | 37.96% | 40.23% | +2.27 pp |
| Reliance Jio | 39.27% | 41.54% | +2.27 pp |

Vi's connection share overstates its active share by **11.53% in relative terms** (15.50 ÷ 13.90). Industry check: 1,201.06 ÷ 1,282.38 = 93.66%, matching TRAI's published figure exactly.

### D4 — The five-month streak

Cumulative net additions Feb–Jun 2026: 21,927 + 102,899 + 53,257 + 121,289 + 163,757 = **463,129**.

Over the same five months the base rose **0.44 mn** while the active base fell **2.13 mn** — **4.83 active users lost per connection added**. The VLR ratio fell **1.26 pp** (85.24% → 83.98%) from February and **1.30 pp** from January. Jio's rose **0.78 pp** over the same window (98.29% → 99.07%).

### D5 — ARPU restated per active subscriber

| | Reported ARPU | ARPU per active subscriber |
|---|---|---|
| Vodafone Idea | ₹195 | **₹225.47** |
| Bharti Airtel | ₹264 | **₹265.95** |

Headline deficit 26.14%; activity-adjusted deficit 15.22%. **41.77% of the apparent gap is denominator, not price.**

Internal consistency: ₹195 × 193.1 mn × 3 months = **₹11,296.35 Cr**, against reported revenue from operations of ₹11,689 Cr, leaving **₹392.65 Cr (3.36%)** for non-mobile revenue — a plausible residual.

Revenue growth 6.0% against ARPU growth 10.2% implies an average base decline of **3.81%**, against a reported point-to-point decline of **2.33%** — a **1.48 pp** spread attributable to averaging effects and non-mobile revenue, not reconciled.

The two published ARPUs differ by **10.17%**. If blended ARPU is computed on the reported base, the implied customer base is **175.28 mn**, leaving **17.82 mn** revenue-earning non-customer connections against a disclosed M2M base of 21.62 mn. These do not reconcile and are not forced to (Appendix A-3).

### D6 — The M2M falsification

M2M as a share of own base: Airtel **17.00%**, Vi **10.87%**, Jio **5.12%**. Airtel is **1.56×** Vi's M2M intensity and runs a 99.27% VLR ratio.

Crediting Vi's entire M2M base as non-registering leaves **10.23 mn** unexplained (**5.15%** of its base) — still **1.24×** Airtel's and Jio's total inactive pools.

### D7 — FWA

Jio 70.40% and Airtel 29.52% of India's 12.94 mn 5G FWA base = **99.92%**. Residual for all other operators: **0.01 mn**.

### D8 — The P&L

| | Value |
|---|---|
| Revenue growth YoY | 6.04% |
| EBITDA growth YoY | 9.15%; computed margin 43.07% vs reported 43.1% |
| Net loss narrowing | ₹2,854 Cr, **43.19%** |
| Net exceptional gain | ₹1,611 Cr = **56.45%** of the narrowing; **42.91%** of the reported loss |
| Loss ex-exceptionals-and-tax | improved **18.95%** YoY, **2.85%** QoQ |
| **Headline ÷ underlying narrowing** | **2.28×** |
| D&A + finance cost | ₹10,587 Cr = **90.57%** of revenue, **2.10×** EBITDA |
| Deferred obligations | ₹156,058 Cr = **3.34×** annualised revenue, **7.75×** annualised EBITDA |

Exceptional components reconcile exactly: ₹1,816 Cr − ₹205 Cr = ₹1,611 Cr.

### D9 — Capex and the competitive gap

Vi capex ₹1,930 Cr = **16.51%** of its own revenue. Airtel's India revenue is **3.53×** Vi's total revenue; Airtel's India EBITDA **4.92×** Vi's total EBITDA, at a margin **17.06 pp** higher. Vi data per 4G/5G subscriber is **63.08%** of Airtel's per-customer figure and **49.66%** of Jio's per-capita figure.

*Caveat:* the denominators differ. Vi's 21.7 GB is per 4G/5G subscriber; Airtel's 34.4 GB is per customer; Jio's 43.7 GB is per capita. Vi's is measured on the narrowest and therefore most flattering base of the three, so the true gap is wider than shown, not narrower.

### D10 — The stress rule

100% − 90% (Vodafone's filed 60-day never-return rate) = **10.00%**. Applied to the 31.85 mn dormant base gives **3.19 mn** realistically addressable connections. The harsher alternative from the 30-day figure (20.00%) is available and not used.

### D11 — RICE

Reach figures are grounded in disclosed base sizes: non-4G/5G connections = 193.1 − 130.1 = **63.0 mn** (**32.63%** of base); dormant connections = 31.85 mn; active base = 166.97 mn.

| Initiative | Base | Stressed | Base rank | Stressed rank |
|---|---|---|---|---|
| Spectrum refarm / 4G capacity *(exempt)* | 6.45 | 6.45 | 1 | 1 |
| 2G-to-4G device-financed upgrade | 2.91 | 0.29 | 2 | 3 |
| **Vi Anchor (PROPOSED)** | **1.01** | **0.10** | **3** | **4 — last** |
| Dormancy release + reconciliation *(exempt)* | 0.83 | 0.83 | 4 | 2 |

`verify.py` asserts two conditions programmatically rather than leaving them to arithmetic done on paper: that Vi Anchor finishes **last** under stress, and that it is the **weakest stressed initiative at baseline** — the only configuration in which the demotion is a result rather than an arrangement.

---

## Part 3 — Constructs

The following are the author's inventions. None is a Vodafone Idea product, plan, disclosure or statement.

**Vi Anchor.** The payer-substitution mechanism in §50: enterprise verification counterparties fund the service validity of dormant connections, which the subscriber receives free in exchange for consented, boolean-only verification. The *precedent* is real — Vi's silent mobile verification partnership with Meta went live in the quarter examined — but the extension to funding dormant-connection validity is constructed.

**AVC/1k.** Anchor-Verified Connections per 1,000 dormant connections held. Four conjunctive conditions: VLR-registered on the peak date; verification revenue received; live DPDP consent; not reactivated by Vi-funded promotional recharge. The denominator is deliberately *dormant connections held*, so that acquiring or retaining dormant connections lowers the metric.

**SSR-90.** Subscriber Suspension Rate at the 90th percentile of verification intensity — the consent-withdrawal rate among the decile of numbers most heavily queried, over a rolling three-quarter window, reported by circle rather than in aggregate, owned outside the enterprise revenue line, with automatic cohort suspension on breach.

**The RICE initiative set.** All four initiatives, their impact/confidence/effort scores, and the exemption rule (initiatives requiring no change in customer behaviour are not stressed). Reach figures are disclosed; the rest are the author's judgement.

**Phase 0 kill criteria K1–K3**, with K2 named as most likely to fire; the **Arm B falsification design** (subsidised validity with no verification product attached); and the **R1 decision rule** (8 pp on AVC/1k across two quarters including one non-festive quarter, plus two further conditions).

**The primary-versus-secondary SIM double run of Porter's Five Forces** in §16, including the claim that buyer power is near-total and exit frictionless on the secondary line.

---

## Part 4 — What would change my mind

| Evidence | Effect |
|---|---|
| Vi's VLR ratio rises two consecutive months while net additions stay positive | **A1 dead.** Management's lag reading is correct and the thesis is an over-reading of five months |
| Circle-level VLR data showing the gap concentrated in low-4G-coverage rural circles rather than legacy-Vodafone urban ones | Secondary-SIM diagnosis substantially weakened; a coverage explanation would fit better |
| Vi discloses a reconciliation of its 193.1 mn base to TRAI's 198.82 mn that accounts for the difference definitionally | A-2 closes; D1's company-basis figure may need restating |
| A post-2020 Indian dormancy-return study materially above 10% | The stress rule loosens and Vi Anchor's RICE position improves — though it would still need to beat 0.83 to escape last place |
| Evidence that enterprise verification demand concentrates on dormant rather than active numbers | K2 does not fire; the proposal's central commercial premise is confirmed |
| Vi publishing VLR-basis subscriber and ARPU figures voluntarily | §47's first recommendation is already being executed, and the case study's main criticism falls away |

---

## Part 5 — What could not be found out

- **Circle-level VLR ratios.** TRAI publishes national operator-level VLR percentages but the circle-level breakdown needed to test the secondary-SIM diagnosis directly was not located.
- **Any Vi disclosure distinguishing primary from secondary SIM position**, or any independent Indian dataset doing so. This is the single largest gap in the analysis.
- **A dormancy-return rate dated after 2020.** The stress rule rests on a ~2012 filing for want of anything newer.
- **The basis of Vi's own 193.1 mn subscriber figure** and why it sits below TRAI's, when Jio's sits above.
- **A reconciliation between Vi's customer ARPU (₹195) and blended ARPU (₹177).** Neither the results release nor the coverage explains the definitional difference.
- **Primary documentation for the AGR relief quantum** (~₹54,200 Cr, or a 27% cut). Both figures are reported rather than filed, are graded 🟡, and are used in no derived calculation.
- **Vi's Q1 FY27 site count and 5G city list from a primary company document.** Figures used (≈205,000 towers, +15,600 YoY, 200+ cities, 17 circles, 87% 4G population coverage) come from the results release as reported in secondary coverage.
- **Jio's VLR ratio for February and March 2026**, which would have completed the six-month comparison series; January, April, May and June were located.

---

*Companion to [README.md](README.md) · Day 65 of 90*
