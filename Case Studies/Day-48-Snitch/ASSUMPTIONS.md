# ASSUMPTIONS — Day 48, Snitch

This file exists so that nothing in [README.md](./README.md) has to carry an unmarked assumption. Everything here is mine. None of it is a Snitch statement, a finding, or a fact.

Three categories are kept separate throughout:

- **Assumptions (A)** — things I believe but cannot verify from public sources, which the analysis depends on.
- **Derivations (D)** — arithmetic I performed on published figures. The inputs are sourced; the operation is mine.
- **Constructs (C)** — systems, metrics, personas, thresholds and designs I invented. Nothing in this category exists at Snitch.

**Date of analysis:** 13 August 2026. **Latest Snitch financials available:** FY26 (year ended 31 March 2026), reported to trade press and described as unaudited at the EBITDA line; FY25 is the latest year with a reported bottom line. **Research boundary:** public sources only; no employee contacted, no store visited, no Quick order placed, no authenticated session used.

---

## Part 1 — Assumptions

### A1 — Snitch Quick consumption materially displaces walk-in purchases

**Load-bearing. This is the assumption the whole case study rests on.**

Snitch has stated that Quick orders are fulfilled from its retail stores, which "function as hyperlocal fulfilment hubs." I assume that units picked for Quick during trading hours are, at a material rate, units that a walk-in customer would otherwise have bought — and specifically that the sizes consumed first are the middle of the size curve, which is what walk-in conversion depends on.

**Why I believe it.** Apparel demand is size-curve shaped and concentrated in the middle sizes; Quick and walk-in demand draw on the same curve from the same physical pool; Snitch launches 3–5 new styles a day, which spreads a fixed working-capital envelope thin across an enormous live SKU count and leaves little per-store depth to absorb concurrent draw; and the company has published nothing suggesting any reservation logic exists.

**Why it might be wrong, and this matters.** Quick demand may be genuinely incremental — an occasion-driven purchase that would not have produced a store visit at all. Snitch may already ring-fence floor stock; a sensible retailer might have built exactly this on day one and simply never mentioned it, because inventory allocation logic is not the kind of thing that gets a press release. Quick may also draw disproportionately from styles and sizes that walk-in customers do not want, in which case the displacement is real but immaterial.

**How it gets tested.** §53 Phase 0: two analyst-weeks, on data Snitch necessarily already holds (Quick pick events, store stock states, footfall patterns), with a kill condition written before the analysis — under 5% of trading-hour store-days showing an attributable core-size gap, and no city-level conversion association surviving a non-Quick control, means the proposal is dropped. §54's E4 arm tests the inverse directly by giving Quick full priority.

**If A1 is false:** §50 solves a problem that does not exist, and the correct finding — that Quick is incremental and the floor is not load-bearing — is more valuable to Snitch than the feature would have been. §47's stress rule halves confidence on every A1-dependent item for exactly this reason.

**Confidence:** Medium on direction. Low on magnitude.

### A2 — The reported store counts are complete and comparable across dates

D1 and D2 both depend on five dated store counts (35, 45, 55+, 100, 115+) drawn from different sources over twenty months.

**Why it might be wrong:** "55+" and "115+" are open-ended. If the August 2026 figure is materially above 115 — say 130 — the measured deceleration falls from 58% to roughly 17% and Line 1 of §46 weakens substantially. Counts may also include franchise, shop-in-shop or pop-up formats inconsistently across sources.

**How it is handled rather than assumed away:** the open-ended figures are treated as their stated minimum, which is the conservative choice for D1 (a higher true count reduces the apparent deceleration, so I am not inflating my own finding by rounding up). The sensitivity is stated in the section itself (§13.5), not here. Note that even under the most generous reading, the pace required to reach 300 stores by end-2026 exceeds anything Snitch has ever achieved by a wide margin.

**Confidence:** Medium-high.

### A3 — The FY25 and FY26 channel splits are defined consistently

FY25 offline was reported at "40–45%" of revenue; FY26 at 40%. I assume both refer to the same thing — revenue transacted in physical stores — and that Quick revenue is counted inside the online 60% in FY26.

**Why it might be wrong:** a store-fulfilled Quick order could reasonably be booked as offline revenue by a retailer's accounting, in which case FY26's offline share includes Quick and the per-store figures in D2 are overstated rather than understated. The reporting describes Quick as a share of *online* revenue, which is why I have read it this way, but the definition has not been published.

**Effect if wrong:** D2's FY26 per-store figure would fall further (offline excluding Quick would be ₹306 Cr, giving ≈₹4.0 Cr per average store), which **strengthens** the direction of the finding while making the level less reliable.

**Confidence:** Medium.

### A4 — Snitch does not already operate a governed floor reserve

The proposal assumes the allocation gap is real — that there is no existing mechanism ring-fencing floor stock from Quick.

**Why it might be wrong:** absence of public evidence is weak evidence of absence. Inventory allocation policy is not something a private company publicises.

**How it is handled:** §53 Phase 0 and Phase 1 both check the current state before anything is built. If a reserve mechanism already exists, the proposal collapses to its instrumentation half (R3), which remains valuable — measuring the trade-off is useful whether or not the mechanism exists.

**Confidence:** Medium.

### A5 — Store-level inventory accuracy is high enough for reserves to be meaningful

A reserve on a ledger that disagrees with the rack is decorative.

**Why it might be wrong:** apparel retail inventory accuracy is routinely below 90% at SKU-size level without RFID or disciplined cycle counting, and Snitch has published nothing about either.

**How it is handled rather than assumed away:** acceptance criterion A1 in §51.5 requires ≥95% agreement on a sampled audit. **Below that threshold the reserve ships as advisory only and the pilot is re-scoped rather than launched.** The mechanism is not dropped; only its enforcement is.

**Confidence:** Low-medium — this is the risk most likely to delay the project in practice.

### A6 — Personas and segmentation are representative of Snitch's actual customer base

Aditya, Rohan and Meera are analytical constructs built from disclosed geography, category mix, price positioning and channel behaviour. **No user was interviewed for this case study.** The Browsers / Fitters / Deadliners segmentation is likewise a construct.

**Why it might be wrong:** the underlying customer figures (48% repeat rate, 20 states, Tier II/III strength) are from a company roughly one-twentieth of its current size and have not been refreshed publicly.

**Confidence:** Low as description. The segmentation's *analytical* function — that two customer types contend for one physical unit — does not depend on the personas being accurate.

### A7 — Trade-press figures reflect what the company briefed

Almost every FY26 figure in this document comes from trade press reporting a company briefing, not from a filed statement.

**Why it might be wrong:** briefed figures are selected by the company, unaudited at the EBITDA line by its own description, and rounded. Numbers reported as ranges ("2–3%", "₹18–27 Cr") are bands, not points.

**How it is handled:** EBITDA is described as a band and as unaudited every time it appears, and the FY26 "profitability" claim is explicitly distinguished from FY24's reported PAT throughout (§7, §18.3, Appendix A-5).

**Confidence:** Medium-high on the figures being what was briefed; lower on their comparability to audited numbers.

---

## Part 2 — Derivations

Every derivation states its inputs, its operation and what would break it in the README section where it appears. They are repeated here so that no derived figure travels through this repository without its method attached.

### D1 — Store-opening pace and the 300-store target (§13.5)

**Inputs:** 45 stores (3 Jan 2025) · 100 stores (23 Dec 2025) · 115 stores (12 Aug 2026), all dated public disclosures.

**Operation:**
- 55 stores ÷ 11.6 months = **4.73 stores/month**
- 15 stores ÷ 7.6 months = **1.97 stores/month**
- Deceleration = **58%**
- (300 − 115) ÷ 4.6 months = **39.9 stores/month = 20.3× the current pace**

**What would break it:** A2 (open-ended counts). A Q3 lease-signing surge is genuinely possible — apparel retail does sign leases seasonally — though the required volume is roughly 3.4× Snitch's best-ever full year, compressed into four months.

**Grade:** 🟢 High on inputs, 🟡 Medium on interpretation.

### D2 — Revenue per average store (§13.6)

**Inputs:** FY25 revenue ₹498 Cr, offline 40–45% · FY26 revenue ₹900 Cr, offline 40% · store counts interpolated at fiscal boundaries (~5 at 1 Apr 2024, ~48 at 31 Mar 2025, ~106 at 31 Mar 2026).

**Operation:** offline revenue ÷ average of opening and closing store count.
- FY25: ₹199–224 Cr ÷ 26.5 = **≈₹7.5–8.5 Cr**
- FY26: ₹360 Cr ÷ 77 = **≈₹4.7 Cr**
- Decline **≈38–45%**

**What would break it:** openings were lumpy, not linear (10 in January 2025 alone; a visible push to reach 100 by December 2025), which back-loads FY26 and *understates* FY26 per-store revenue. New stores ramp, so any fast-growing fleet shows falling averages regardless of store quality. A3 (channel-split definitions) also bears on it.

**What it does and does not prove:** it does **not** prove stores are getting worse. It proves the marginal store is materially less productive than the fleet average was when the 300-store plan was written — which is all the argument requires.

**Grade:** 🟡 Medium. This is the softest number in the document and is described as such in §64.

### D3 — Snitch Quick's implied revenue (§13.7)

**Inputs:** FY26 online revenue ₹540 Cr (60% of ₹900 Cr) · Quick at ~10% of online · launched Oct 2025, four cities.

**Operation:** ₹54 Cr in ~6 of 12 FY26 months → annualised run-rate **≈₹108 Cr** → at D2's ₹4.7 Cr per average store, **≈23 stores' worth of annual revenue**, with zero incremental leases.

**What would break it:** incrementality (the second half of A1). If most Quick orders are shifted standard online orders, this is a cost centre with a revenue label. Also A3, if Quick is booked as offline.

**Grade:** 🟡 Medium on the arithmetic, 🟠 Low on the incrementality reading.

### D4 — What a margin point is worth (§13.8)

**Inputs:** FY26 revenue ₹900 Cr · EBITDA margin 2–3% · FY27 target ₹1,400 Cr.

**Operation:**
- EBITDA = ₹18–27 Cr, midpoint **₹22.5 Cr**; therefore ₹1 Cr = **4.4%** of annual EBITDA
- 1pp of offline conversion on ₹360 Cr ≈ ₹3.6 Cr revenue; at ~30% contribution ≈ ₹1.1 Cr ≈ **5% of EBITDA**
- FY27 offline at a 60/40 split = ₹560 Cr; ÷ ₹4.7 Cr per average store = **≈120 average stores, a fleet already built**

**What would break it:** the 30% contribution-margin assumption is mine and is not disclosed (it is listed as construct C11). The ₹22.5 Cr midpoint is the centre of a reported band, not a figure.

**Grade:** 🟢 High on the EBITDA arithmetic; 🟡 Medium on the contribution-margin step.

---

## Part 3 — Constructs

Nothing in this list exists at Snitch. All of it is mine, and none of it should be read as a description of the company.

| # | Construct | Where |
|---|---|---|
| **C1** | **Snitch Reserve** — the entire proposed system | §50, §51 |
| **C2** | **Size-Curve Reserve** — per-store, per-style, per-size floor reserve, invisible to Quick, relaxing outside trading hours | §50.3 |
| **C3** | **Promise Ladder** — three-tier graceful degradation (60 min / same day / tomorrow) | §50.3, §52.1 |
| **C4** | **Reserve Ledger** — the audit trail pricing every floor/Quick trade | §50.3 |
| **C5** | **Dual-Served Store-Days (DSSD)** — the proposed conjunctive North Star, and both of its component floors | §31.1 |
| **C6** | **Displacement Rate (DR)** — the proposed guardrail counter-metric, its three measurement methods, and the veto rule attached to it | §31.2, §51.6 |
| **C7** | The six-event model (`reserve_set`, `quick_allocation_request`, `reserve_breach`, `promise_degraded`, `size_out_logged`, `floor_conversion`) | §32.2 |
| **C8** | Personas Aditya, Rohan and Meera; the Browsers / Fitters / Deadliners segmentation | §19, §20 |
| **C9** | All wireframes, their states and their copy | §52 |
| **C10** | All RICE inputs, the stress rule, and both the base and stressed score tables | §47 |
| **C11** | The ~30% contribution-margin figure used in D4 | §13.8 |
| **C12** | The §13.9 sensitivity ranges (+0.5–2.0pp conversion, +2–5pp fill) | §13.9 |
| **C13** | Phase 0–3 rollout plan; both kill gates and their thresholds (5% of store-days, 3% DR) | §53 |
| **C14** | Experiments E1–E4, including the E4 falsification arm and all stopping rules | §54 |
| **C15** | Acceptance-criterion thresholds (≥95% inventory accuracy, ≥60% logging compliance, ≥40% ladder acceptance) | §51.5 |
| **C16** | The reconstructed technical architecture and data-flow diagrams | §41, §42 |
| **C17** | The reconstructed vision/mission table | §9 |
| **C18** | The KPI dashboard, its ownership assignments, and the two dashboard design rules | §55 |
| **C19** | The staff-data policy recommendation (size-out logs excluded from individual appraisal) | §44, §51.7 |
| **C20** | All ten PM interview questions | §60 |

---

## Part 4 — What would change my mind

Listed so that the argument is falsifiable rather than merely qualified.

| Finding | Effect on this case study |
|---|---|
| Snitch publishes Quick incrementality showing most Quick orders are net-new demand | **A1 weakens badly.** §50 becomes optional; the instrumentation half (R3) survives |
| Snitch confirms an existing floor-reserve mechanism | **A4 falsified.** The proposal collapses to instrumentation and measurement |
| Snitch opens 40+ stores in Q4 2026 | **Line 1 of §46 falsified.** The deceleration was a pause, not a policy — though D2 and lines 3–6 stand |
| Store-level inventory accuracy proves to be below ~90% | **A5 falsified.** Reserves are unenforceable; the project becomes an inventory-accuracy project first |
| E4 (Quick-priority arm) shows total revenue up with no conversion decline | **The thesis in §5 is wrong.** Snitch should stop reserving stock, and possibly reconsider store expansion altogether |
| FY26 audited accounts show a materially different picture from the briefed figures | Every derivation in §13 is recomputed; the *direction* of D1 is unaffected, since it uses store counts rather than financials |

---

*Companion to [README.md](./README.md) · Day 48 of 90*
