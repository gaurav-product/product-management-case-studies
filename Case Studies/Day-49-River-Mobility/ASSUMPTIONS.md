# ASSUMPTIONS — Day 49, River Mobility

This file exists so that nothing in [README.md](./README.md) has to carry an unmarked assumption. Everything here is mine. None of it is a River statement, a finding, or a fact.

Five parts are kept separate throughout:

- **Part 1 — Assumptions (A)** — things I believe but cannot verify from public sources, which the analysis depends on.
- **Part 2 — Derivations (D)** — arithmetic I performed on published figures. The inputs are sourced; the operation is mine.
- **Part 3 — Constructs (C)** — systems, metrics, personas, thresholds and designs I invented. **Nothing in this category exists at River.**
- **Part 4 — What would change my mind** — so the argument is falsifiable rather than merely qualified.
- **Part 5 — What this case study could not find out** — the figures that would settle the argument, and who holds them.

**Date of analysis:** 14 August 2026. **Latest River financials available:** FY25 revenue ₹101 Cr (reported). FY26 is a **company-guided multiple (~4.4×), unaudited, and not a filed figure**. No profit-and-loss detail, contribution margin, or revenue split by line has ever been published. **Research boundary:** public sources only; no River employee, dealer or customer contacted; no store visited; no test ride taken; no authenticated session used.

---

## Part 1 — Assumptions

### A1 — River's post-sale revenue is currently immaterial

**Load-bearing. This is the assumption the whole case study rests on.**

I assume that revenue River earns from vehicles it has already sold — extended cover, paid service, parts, accessories — is small relative to vehicle revenue, and small in absolute terms per vehicle-year. Everything in §18, §50 and §53 follows from it.

**Why I believe it.** River has never published a revenue split. Its extended cover is priced at ₹4,999 and ₹8,399 as one-time charges (§18.4), which caps the achievable per-vehicle-year figure at roughly ₹1,050–2,500 even at 100% attach. The company describes itself in terms of units, capacity and stores; its CEO frames profitability entirely in units per month. Its franchise specification (2,500 sq ft, ≥3 bays) is attached to a P&L whose stated revenue line is vehicle sales. None of River's Series C communications mention aftersales revenue as a driver.

**Why it might be wrong, and this matters.** Absence of disclosure is weak evidence of absence. A private company has no obligation to break out service revenue and generally does not. River's franchise partners may already run a healthy parts-and-labour business that simply never appears in trade press. And a company with 50,000 vehicles in the field and ~225 bays could plausibly already be earning ₹3,000–5,000 per vehicle-year without ever saying so.

**How it gets tested.** §53 Phase 0: two analyst-weeks on data River necessarily already holds — cover attach rate since 1 Oct 2025, paid-service revenue per vehicle-year by cohort, parts and accessories per vehicle-year — with **three kill criteria written before the analysis runs** (K1: post-sale revenue already above ₹4,000/vehicle-year; K2: attach rate already above 60%; K3: median SoH worse than 80% at three years). §54's **E4 arm** tests the inverse directly, by bundling the cover into the sticker price instead of unbundling it.

**If A1 is false:** §50 is redundant, and the finding — that River is already running the ownership business quietly — is more valuable to River than the proposal would have been. §47's stress rule applies River's own worst target-realisation rate (30%) to every A1-dependent item for exactly this reason, and that stress **demotes the proposal's centrepiece below the strategic option the case study argues against.**

**Confidence:** Medium on direction. Low on magnitude.

### A2 — The 25,000-unit breakeven figure means what it appears to mean

The CEO's statement — *"We will continuously be loss-making till we are at 25,000 units a month because the cost structure comes down with volume"* — is treated throughout as a company-level operating-breakeven figure at current product mix and current pricing.

**Why it might be wrong:** it may be a rounded rhetorical figure rather than a modelled one; it may refer to EBITDA rather than net; it may already assume the RX02/RX03 mix rather than Indie-only economics; and it may assume a lower ASP than ₹1.55 lakh. Any of these changes the share arithmetic in D2.

**How it is handled rather than assumed away:** D1 is computed on **two** bases (registrations and River's own stated run rate), and D2 is computed at **two** market-growth rates, so the finding is presented as a range (4.17–5.65× on volume; 7.80–11.84% on share) rather than a point. **The direction survives every reading.**

**Confidence:** Medium-high.

### A3 — The volume ramp to March 2028 is approximately linear

D5's parc projection compounds monthly volume linearly from ~6,000/month (Aug 2026) to River's own declared 15,000–20,000/month by March 2028.

**Why it might be wrong:** hardware ramps are rarely linear. They are typically back-loaded — capacity comes online in steps, a second plant contributes nothing until it contributes a lot, and new models front-load demand at launch. A back-loaded ramp lowers the March-2028 parc; a front-loaded one raises it.

**How it is handled:** three scenarios are published (17,500 / 15,000 / 10,000 per month at the endpoint), and the **most pessimistic — a 43% miss against River's own target — still produces more annual ownership revenue than River's entire FY25 revenue.** The conclusion does not depend on the ramp shape; only the magnitude does.

**Confidence:** Medium on shape. High on the direction of the conclusion.

### A4 — River does not already publish or plan a battery health certificate

The proposal in §50.4 assumes the field is empty — that neither River nor any Indian e-2W competitor issues a customer-facing State-of-Health record.

**Why it might be wrong:** a certificate could exist as a service-centre print-out that has simply never been publicised, or be in development at any of six competitors. Product roadmaps are not public.

**How it is handled:** §53 Phase 0 checks current state before anything is built, and §49 explicitly time-boxes the opportunity — SoH certification is *attractive* today and becomes *must-be* the moment any competitor ships one. If River discovers it already does this internally, the proposal collapses to a distribution and packaging project, which is cheaper and still worth doing.

**Confidence:** Medium-high on River. Medium on competitors.

### A5 — SoH is measured accurately and repeatably enough to certify

The certificate assumes River's workshop diagnostics produce a State-of-Health figure precise enough to put a customer's name next to.

**Why it might be wrong:** SoH estimation is genuinely difficult, method-dependent, and sensitive to temperature, charge state and measurement duration. Two measurements of the same pack on the same day can diverge materially.

**How it is handled rather than assumed away:** acceptance criterion **AC1 in §51.5** requires **±3 percentage points** repeatability on a repeat measurement, same vehicle, same day. **Below that threshold the certificate ships as an indicative band only, or does not ship at all.** This is why §50.4 specifies a band (92–95%) rather than a decimal, and why the certificate carries the words *"This is a measurement, not a prediction."*

**Confidence:** Low-medium. **This is the assumption most likely to delay the project in practice**, and it is a genuine engineering risk rather than a product one.

### A6 — Personas and the segment shares in §19 are representative

Karthik, Meera, Anil and Suresh are analytical constructs built from price point, product design, geography and category behaviour. **No River customer was interviewed for this case study.** The segment shares in §19 (~50/25/15/10) are my estimates, graded 🟡 and 🟠 in the section itself.

**Why it might be wrong:** River publishes no customer demographics at all. The estimates are inference from a ₹1.55 lakh price and a 43-litre boot.

**Confidence:** Low as description. The analytical function the personas serve — that an owner, a prospect and a used buyer all need the same missing artefact — does not depend on their accuracy.

### A7 — Trade-press figures reflect what the company briefed

Most FY26 operating figures in this document come from trade press reporting a company briefing, not from a filed statement. The ₹1.55 lakh ASP, the ~6,000/month run rate, the ~4.4× revenue guidance, the capacity and utilisation figures, and the store targets all originate this way.

**Why it might be wrong:** briefed figures are selected by the company, rounded, and in this case explicitly unaudited. Some are ranges presented as points.

**How it is handled:** FY26 revenue is described as **a guided multiple, unaudited**, every time it appears. Where trade sources conflict — June volume, plant capacity, Series B size, store targets, motor output, claimed range, founding year — the conflict is recorded in **README Appendix A** rather than resolved silently, and the **conservative** reading is used where the choice could flatter the argument.

**Confidence:** Medium-high on the figures being what was briefed; lower on their comparability to audited numbers.

### A8 — The Hero BaaS comparison is a fair analogue

D4 compares River's Plus Five cover against Hero's Vida BaaS as two answers to the same job: *make the expensive part of an EV somebody else's problem.*

**Why it might be wrong, and this is the strongest objection to the case study.** They are structurally different products. Hero's BaaS transfers battery *ownership* and bundles vehicle *financing* — at term end the customer owns the scooter and the batteries. River's plan transfers *replacement risk* on a battery the customer already owns outright. A reader could fairly argue the correct comparison is an insurance premium, not a lease.

**How it is handled:** the objection is stated inside §18.4 rather than buried here, and **both** readings of River's price are published (₹1,050 per covered vehicle-year and ₹1,680 per incremental vehicle-year), with the conservative figure named as the one to quote if only one is used. **The ratio is 47.2× on the headline reading and 29.5× on the conservative one.** No plausible actuarial reading puts fair value for an eight-year battery-replacement guarantee at ₹1,050/year on a ₹1.55 lakh vehicle. The direction survives the objection; the precision does not.

**Confidence:** High on direction. Medium on comparability.

---

## Part 2 — Derivations

Every derivation states its inputs, its operation and what would break it in the README section where it appears. They are repeated here so that no derived figure travels through this repository without its method attached. **All 37 derived figures in this document were recomputed programmatically from sourced inputs before publication; all passed.**

### D1 — The distance to breakeven (§13.3)

**Inputs:** 25,000/month (CEO statement, Aug 2026) · 4,421 (VAHAN, June 2026) · ~6,000/month (company briefing, Aug 2026).

**Operation:**
- 25,000 ÷ 4,421 = **5.65×**
- 25,000 ÷ 6,000 = **4.17×**

**What would break it:** A2 — if 25,000 is rhetorical, or refers to a different mix or a different margin line.

**Grade:** 🟢 High.

### D2 — What 25,000/month requires as market share (§13.4)

**Inputs:** FY26 e-2W market 1,401,818 units, up 21.81% from 1,150,790 (VAHAN) · breakeven targeted Q1–Q2 FY29, three years forward · River's June 2026 share 4,421 ÷ 194,300.

**Operation:**
- At 21.8% CAGR: 1,401,818 × 1.218³ = 2,533,835/yr → **211,153/month** → 25,000 = **11.84%**
- At 40% CAGR: 1,401,818 × 1.40³ = 3,846,589/yr → **320,549/month** → 25,000 = **7.80%**
- River today: 4,421 ÷ 194,300 = **2.28%**
- Required gain: **3.43× to 5.20×**

**What would break it:** the growth assumption. **The derivation is asymmetric against River** — slower growth makes the requirement worse, not better, and the market has never grown at 40% for three consecutive years. The 7.8% figure is therefore the generous bound.

**Also relevant:** construct **C-1**, my estimate that the premium band above ₹1.4 lakh is ~5–8% of the market, is graded 🟠 and is **not used as a load-bearing input** — it is cited once, flagged, and the argument stands without it.

**Grade:** 🟢 High on arithmetic. 🟡 Medium on the three-year projection.

### D3 — Price direction (§13.5)

**Inputs:** launch price ₹1,25,000 · Feb 2024 ₹1,38,000 · Aug 2026 ASP ₹1,55,000.

**Operation:** 155,000 ÷ 125,000 − 1 = **+24.0%**

**What would break it:** ASP is not list price — it is company-stated and may include or exclude accessories, insurance or subsidy differently across periods.

**Grade:** 🟢 High.

### D4 — The ownership-product price gap (§18.4)

**Inputs:** Plus Five ₹8,399 + GST for 8 years / 80,000 km, over a 3-year / 30,000 km standard manufacturing warranty (River's own pricing page) · Plus Two ₹4,999 + GST for 5 years / 50,000 km · Vida VX2 Plus 3-year BaaS ₹1,584/month (Autocar India) · Indie ASP ₹1,55,000 · VX2 ₹59,490.

**Operation:**
- River, per **covered** vehicle-year: 8,399 ÷ 8 = **₹1,050**
- River, per **incremental** vehicle-year: 8,399 ÷ 5 = **₹1,680**
- Hero, per vehicle-year: 1,584 × 12 = **₹19,008**
- Absolute ratios: **18.1×** (headline) and **11.3×** (conservative)
- As % of vehicle price/year: River **0.68%** / **1.08%**; Hero **31.95%**
- Normalised ratios: **47.2×** (headline) and **29.5×** (conservative)
- **Internal inconsistency:** Plus Two = ₹2,500 per incremental year; Plus Five = ₹1,680. **The longer, riskier plan is 33% cheaper per year.**

**What would break it:** A8 — the products are not like-for-like, and the objection is stated in §18.4. Also, ₹8,399 is exclusive of GST while ₹1,584 may be inclusive; that difference is immaterial against an 18–47× gap.

**Grade:** 🟢 High on all inputs (published prices). 🟡 Medium on comparability.

### D5 — The parc compounds (§13.7)

**Inputs:** 50,000th unit produced 27 July 2026 (company milestone) · current run rate ~6,000/month · River's declared target of 15,000–20,000 units/month by March 2028 · 20 months from August 2026 to March 2028 inclusive.

**Operation:** linear monthly ramp from 6,000 to each endpoint; cumulative additions summed and added to the 50,000 base; multiplied by a **construct** revenue figure of ₹5,000/vehicle-year (**C-2**).

| Endpoint | Units added | Parc at Mar 2028 | Revenue at ₹5,000/vehicle-year |
|---|---|---|---|
| 17,500/mo (target midpoint) | 235,000 | **285,000** | **₹142.5 Cr** |
| 15,000/mo (target bottom) | 210,000 | **260,000** | **₹130.0 Cr** |
| 10,000/mo (**43% miss**) | 160,000 | **210,000** | **₹105.0 Cr** |

**River's FY25 revenue was ₹101 Cr. All three scenarios exceed it.**

**Secondary result:** the parc grows **5.70×** from July 2026 while the store network grows **5.0×** (75 → 375) — the parc compounds **14% faster than the network that serves it.**

**What would break it:** A3 (ramp shape) and C-2 (the ₹5,000 multiplier, which is mine, not River's). At ₹3,000/vehicle-year the pessimistic case still yields ₹63 Cr; at ₹8,000 the midpoint yields ₹228 Cr. Scrappage is assumed negligible over the window, which is reasonable for a parc whose oldest vehicles are under five years old.

**Grade:** 🟡 Medium. The parc arithmetic is sound; the revenue multiplier is a construct.

### D6 — The distribution step-up and River's target-realisation record (§13.6)

**Inputs:** dated store counts — 1 (Feb 2024), 4 (Aug 2024), 27 (Jul 2025), ~30 (early 2026), 75+ (Aug 2026) · targets of 200+ by Mar 2027 and 350–400 by Mar 2028 · two historical targets: "100 stores by March 2025" (stated Aug 2024) and "80 outlets by April 2026" (stated early 2026).

**Operation:**
- Achieved pace, Jul 2025 → Aug 2026: 48 ÷ 13 = **3.69/month**
- Required to Mar 2027: 125 ÷ 7 = **17.86/month**
- Step-up: 17.86 ÷ 3.69 = **4.84×**
- Required to Mar 2028: 275 ÷ 19 = **14.47/month** (to 350) or 325 ÷ 19 = **17.11/month** (to 400)
- Realisation: ~27 delivered against 100 targeted ≈ **~30%**; 75 delivered against 80 targeted ≈ **~94%**

**What would break it:** "75+" is open-ended and is treated as its stated minimum, which is the conservative choice — a higher true count *reduces* the apparent step-up, so I am not inflating my own finding. The two historical targets were stated in different formats and their delivery dates are approximate.

**Why it matters beyond §13:** the **30%** figure is used as the RICE stress rule in §47. A company that has publicly stated dated targets and publicly missed them has handed the analyst a calibrated sensitivity band. Using a generic ±20% instead would throw away the best information available.

**Grade:** 🟢 High on the pace arithmetic. 🟡 Medium on the realisation rates.

### D7 — RICE base and stressed scores (§47)

**Inputs:** Reach values of ₹142.5 Cr (D5's Mar-2028 parc opportunity), ₹444 Cr (FY26 guided revenue) and ₹30 Cr (a narrow sub-segment); Impact, Confidence and Effort values that are **entirely mine** (construct C-11).

**Operation:** RICE = Reach × Impact × Confidence ÷ Effort, computed at base, at 30% realisation stress, and at 50% realisation stress.

**Results:** ordering is **identical at both stress levels** — R3, R2, R6, R1, R4, R5, R7. Under stress, **R1 (the Course Plan, this proposal's centrepiece) falls from 3rd to 4th, below R6 (a down-market variant)** — the strategic move the case study argues River has avoided.

**What would break it:** every input except Reach is a judgement of mine. The stress rule is defensible because it uses River's own history; the base scores are not independently verifiable.

**Grade:** 🟠 Low as measurement. 🟢 High as a decision procedure — the value is that the ordering is stable and that it contradicts the author.

---

## Part 3 — Constructs

**Nothing in this list exists at River.** All of it is mine, and none of it should be read as a description of the company.

| # | Construct | Where |
|---|---|---|
| **C-1** | The 5–8% estimate of the premium band's share of the market | §13.4 |
| **C-2** | The **₹5,000/vehicle-year** multiplier used in D5 | §13.7 |
| **C-3** | The **₹5,000–8,000** Course Plan price range | §39.3, §50.5 |
| **C-4** | **River Course** — the entire proposed system | §50, §51 |
| **C-5** | **The State-of-Health Certificate** — its contents, format, band-not-decimal rule, and the free-to-all-owners policy | §50.4, §52.1 |
| **C-6** | **RVY (Revenue per Vehicle-Year in Parc)** — the proposed North Star and its new-vehicle-revenue exclusion rule | §31.1 |
| **C-7** | **SBD (Selling-Bay Displacement)** — the guardrail, its 75th-percentile rule, its retail-operations ownership rule, and the +2pp veto | §31.2, §51.6 |
| **C-8** | The eight-event model (`soh_measured`, `certificate_issued`, `certificate_verified`, `plan_offered`, `plan_activated`, `plan_renewed`, `bay_occupancy_logged`, `sales_capacity_blocked`) | §32.2 |
| **C-9** | Personas Karthik, Meera, Anil and Suresh; the time-based segmentation (prospects / buyers / owners / ex-owners) in §19 | §19, §20 |
| **C-10** | All wireframes and their copy, including *"This is a measurement, not a prediction"* | §52 |
| **C-11** | All RICE inputs, the 30% stress rule, and both stressed tables | §47 |
| **C-12** | The reconstructed vision / mission / operating-belief table | §9 |
| **C-13** | Phases 0–3, all kill gates and every threshold (₹4,000/vehicle-year; 60% attach; 80% SoH at 3 years; +2pp SBD) | §53 |
| **C-14** | Experiments E1–E4, including the **E4 falsification arm** and its pre-registered >10% decision rule | §54 |
| **C-15** | All acceptance criteria and thresholds (±3pp SoH repeatability; ≥90% issuance; ≤5 min added; ≥15% attach; ≥60% renewal; ≥5% verification) | §51.5 |
| **C-16** | The reconstructed technical architecture and data-flow diagrams | §41, §42 |
| **C-17** | The KPI dashboard, its ownership assignments, and its two design rules | §55 |
| **C-18** | The renewal-weighted commission policy and the appraisal-firewall policy for SBD logs | §51.7, §44 |
| **C-19** | The public certificate verification endpoint design and its minimal response | §43 |
| **C-20** | All ten PM interview questions | §60 |
| **C-21** | Segment share estimates in §19 (~50 / 25 / 15 / 10) | §19 |
| **C-22** | The three-roads framing (down-market / more-of-the-same / redefine revenue) | §35.2 |

---

## Part 4 — What would change my mind

Listed so that the argument is falsifiable rather than merely qualified.

| Finding | Effect on this case study |
|---|---|
| River discloses post-sale revenue **above ₹4,000/vehicle-year** | **A1 falsified. §50 is redundant** — River is already running the ownership business. This is Phase 0's kill criterion K1 |
| Cover attach rate is **already above 60%** and rising | **The problem is pricing, not product.** §50 collapses into a repricing project (K2) |
| SoH data shows **median degradation below 80% at three years** | **Do not publish certificates.** The evidence would destroy residuals rather than support them, and River has a product problem outranking everything in this document (K3) |
| **E4's bundled arm beats the unbundled arm by >10%** on 24-month revenue per vehicle | **§50 is wrong and §39.2 is wrong.** River should bundle the 8-year cover into the sticker as a conversion weapon, not unbundle it. Pre-registered in §54.1 |
| River announces a **sub-₹1 lakh product** | §47's stress test was right: the down-market road was the more robust move, and this proposal was second-best |
| River reaches **200 stores by March 2027** | **D6's step-up concern is falsified.** The distribution plan works and Road 2 needs no help |
| **PM E-DRIVE is restored, extended past FY28, or the ₹1.5 lakh ceiling is lifted** | Line 3 of §46 weakens substantially. Lines 1, 4 and 5 stand unchanged |
| A competitor ships a battery health certificate first | **A4 falsified.** §49's Kano migration happens without River, and the opportunity converts from differentiator to table stakes |
| SoH repeatability proves worse than ±3pp | **A5 falsified.** The certificate ships as an indicative band or not at all; the Course Plan survives without it but loses its best sales context |
| River publishes FY26 audited accounts materially different from guidance | Every figure in §18.1 is recomputed. **D1, D2 and D6 are unaffected** — they use volumes and store counts, not financials |
| River's contribution margin is disclosed | **§18.6 becomes computable.** This is the single disclosure that would most change what this document could say |

---

## Part 5 — What this case study could not find out

The figures that would settle the argument, and who holds them. **Every one of these is held by River, and none of them is public.**

| # | Missing figure | Why it matters | Who holds it | What it would settle |
|---|---|---|---|---|
| **M1** | **Contribution margin per vehicle** | The denominator of the revised-breakeven identity | River finance | **§18.6.** Would convert this case study's central claim from directional to quantified |
| **M2** | **Fixed cost base** | The numerator of the same identity | River finance | §18.6 |
| **M3** | **Plus Two / Plus Five attach rate** since 1 Oct 2025 | Whether the ownership product is already working | River retail / DMS | **A1 directly.** Phase 0 kill criterion K2 |
| **M4** | **Paid-service revenue per vehicle-year, by cohort** | The actual current value of the parc | River aftersales | **A1 directly.** Phase 0 kill criterion K1 |
| **M5** | **Parts and accessories revenue per vehicle-year** | Completes the post-sale picture | River aftersales | A1 |
| **M6** | **SoH distribution across the parc by vehicle age** | Whether publishing certificates helps or harms | River engineering | **A5 and Phase 0 kill criterion K3.** Also whether Plus Five is under-priced or correctly priced |
| **M7** | **SoH measurement repeatability** | Whether a certificate can be issued at all | River engineering | **A5.** Acceptance criterion AC1 |
| **M8** | **Bay utilisation during trading hours, by store** | The SBD baseline | River retail operations | Whether the guardrail is already breached before anything ships |
| **M9** | **FY26 audited revenue and P&L** | Everything in §18.1 rests on a guided multiple | River finance / MCA filing | A7 |
| **M10** | **Valuation at any round** | Capital efficiency and the implied volume expectations | River / investors | Context only — nothing in the argument depends on it |
| **M11** | **Revenue and terms of the Yamaha EC-06 contract** | Size of the non-vehicle revenue River already earns | River / Yamaha | Whether contract manufacturing is already a material second business |
| **M12** | **Why Kerala outperforms** — share per store, cohort behaviour, dealer quality | River is about to spend Series C money on a national template | River sales analytics | §35.3. **The cheapest study available to River right now** |
| **M13** | **Used-market transaction prices for Indies** | Whether the uncertainty discount is real and how large | Classifieds platforms; River does not collect it | P2, and the entire Phase 3 residual model |
| **M14** | **Warranty claim rate and cost per claim** | Whether Plus Five at ₹8,399 is profitable or subsidised | River finance | §18.4's internal-inconsistency finding |
| **M15** | **Dealer-level inventory** behind the ~18% Jun-2026 dispatch-vs-registration gap | Whether distribution is running ahead of demand | River sales operations | §32.1, §55 |

**The pattern in this table is the point.** Fifteen figures would settle most of this document, and River holds all fifteen. That is why §53 Phase 0 costs two analyst-weeks rather than a research budget, and why §18.6 refuses to invent the number it cannot source.

---

*Companion to [README.md](./README.md) · Day 49 of 90*
