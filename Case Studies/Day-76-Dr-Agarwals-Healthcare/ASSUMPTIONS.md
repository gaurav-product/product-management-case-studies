# ASSUMPTIONS — Day 76, Dr Agarwal's Health Care Limited

**Case study:** Day 76 of 90 · Dr Agarwal's Health Care Limited (CIN L85100TN2010PLC075403)
**Period examined:** Q1 FY27, quarter ended 30 June 2026; results approved 4 August 2026
**Verification:** `verify.py` — 117 checks, all passing
**Written:** 11 September 2026

Part 1 states what is assumed and gives each rival reading equal weight. Part 2 shows the arithmetic. Part 3 lists what the author invented. Part 4 states what would falsify the thesis. Part 5 records what could not be found out.

---

## Part 1 — Assumptions

### A1 (load-bearing) — that the fall in surgeries per facility reflects demand creation lagging network extension, rather than the young age of the new sites

**The assumption.** Surgeries per facility fell from 316.80 to 299.61, a decline of 5.42%, while the facility count grew 22.09%. The case study reads this as a structural statement: the company is extending its network faster than it is creating surgical demand at the sites it already has.

**The honest rival reading, given equal weight.** Sixteen of the eighteen facilities opened in Q1 FY27 were surgical, and a site commissioned in June 2026 adds a full unit to the denominator while contributing almost no surgery to the numerator. Under this reading the ratio is a ramp artefact, arithmetically guaranteed by fast opening, and it will correct as the 2026 cohort matures. Management's position is consistent with this: the CEO's stated framing of the quarter is that greenfield losses were *contained* despite launching twenty-three surgical facilities in six months — i.e. that the drag is understood, priced and temporary.

**Why the case study proceeds anyway, and how far.** Three things support the structural reading without settling it.

1. The pattern is not confined to one quarter. Facility counts ran 249 → 258 → 269 → 288 → 304 across five reported dates while surgery growth decelerated from **+16.0%** (Q1 FY26) to **+11.2%** (Q3 FY26) to **+15.47%** (Q1 FY27). Volume growth has not kept pace with site growth in any recent period.
2. FY26's greenfield cohort lost **about ₹30 Cr**, which is **17.86% of FY26 profit**. The drag is the company's own disclosed figure, not an inference, and the FY27 plan is **1.20× larger** on an annualised Q1 pace.
3. The mature comparator moved the wrong way. The group's own listed subsidiary — concentrated in the oldest markets — reported operating margin **down 148 bps** in the same quarter the group reported improvement. If the story were simply "young sites drag, mature core compounds", the mature core should have expanded.

**What would settle it, and it is not published.** Mature-facility surgical volume, disclosed separately. The company has published mature-facility *revenue* before — ₹291 Cr, +16.6%, in Q3 FY25 — so the cut exists internally. It was not disclosed for Q1 FY27 in any source examined. **A1 is therefore a direction, not a proof, and the case study does not upgrade it.**

### A2 — that 882,000 is close enough to the true patient count to carry the conversion arithmetic

The company said "over 8.8 lakh". The floor is used. If the real number is 920,000, conversion is **9.90%** rather than 10.33% and every derived figure shifts. **The error runs in the conservative direction:** a higher true footfall makes the unconverted pool larger and the proposal's prize bigger. The estimate therefore understates the argument it supports, which is the correct direction for an estimate to be wrong in.

### A3 — that surgical conversion is a managed quantity at all

The case study assumes some meaningful share of the 89.67% who did not convert were clinically indicated for later intervention. This is medically reasonable for a progressive-disease population, and it is **not measured anywhere in the disclosure**. The rival reading is that the great majority of eye-care footfall is refraction, spectacle purchase and reassurance, and that the indicated-deferral pool is small. Phase 0's K1 exists precisely to test this, and the proposal is designed to die cheaply if the pool is thin.

### A4 — that the margin compression on revenue from operations is real

Operating EBITDA grew 25.2% against revenue growth of 25.97%, implying margin on operating revenue fell from 29.00% to 28.83%, about **17.8 bps**. EBITDA is reported to the nearest ₹1 Cr and its growth to 0.1 of a point. The resulting band runs **−32.98 to −2.63 bps**. **The band never crosses zero**, so the direction is robust; the level is not, and the case study uses only the direction.

### A5 — that the three margin bases in §14 are not secretly the same number

The company reports 28.5% on total income; a third party computes 30.26% for the subsidiary; this case study computes 31.63% and 28.83% on revenue from operations. These are not forced to reconcile, and no comparison is made across bases. The 2.80-point group-versus-subsidiary gap is computed on one consistent basis (revenue from operations) and is the only cross-entity margin claim made.

---

## Part 2 — Derivations

Every figure below is computed in `verify.py` and printed on every run.

**D1 — the thesis.**
- Revenue growth = 614.02 ÷ 487.42 − 1 = **25.97%**
- Surgery growth = 91,082 ÷ 78,882 − 1 = **15.47%**
- Facility growth = 304 ÷ 249 − 1 = **22.09%**
- Surgeries per facility = 78,882 ÷ 249 = **316.80**; 91,082 ÷ 304 = **299.61**; change **−5.42%**
- Revenue per facility = 487.42 ÷ 249 = **₹1.9575 Cr**; 614.02 ÷ 304 = **₹2.0198 Cr**; change **+3.18%**
- Revenue per surgery = **₹61,791** → **₹67,414**; change **+9.10%**
- **Reconstruction check:** (1 + 0.0910) × (1 − 0.0542) − 1 = **3.19%** against the directly computed **3.18%** — a gap of **0.0046 of a point**, which is the rounding of the published inputs
- Facility growth − surgery growth = **6.62pp**; ratio **1.43×**

**D2 — the mix lever.**
- Femto 1,548 + lenticular 1,712 = **3,260** = **3.58%** of surgeries
- Implied prior year: 1,548 ÷ 1.334 = **1,160.42**; 1,712 ÷ 1.362 = **1,256.98**; total **2,417.40** = **3.06%**
- Mix shift **+0.51pp**; premium procedures supplied **6.91%** of the 12,200 additional surgeries
- Cataract **74.05%**; refractive **4.39%**; all named specialised lines 7,996 = **8.78%**
- Unclassified residual = 91,082 − 67,444 − 3,998 − 3,861 − 286 − 589 = **14,904** = **16.36%**

**D3 — the conversion arithmetic.**
- Conversion = 91,082 ÷ 882,000 = **10.33%**; non-conversion **89.67%**
- One point = 8,820 surgeries = **9.68%** of surgical volume
- At ₹67,414 per surgery = **₹59.46 Cr** = **9.68%** of quarterly revenue
- ÷ ₹2.0198 Cr per facility = **29.44 facilities' quarterly revenue** = **1.84×** the sixteen surgical facilities opened
- Patients per facility = **2,901.32**

**D4 — the mature entity.**
- Subsidiary revenue ₹142.97 Cr = **23.28%** of group revenue; growth **22.28%**
- Subsidiary EBITDA margin on own revenue = 45.22 ÷ 142.97 = **31.63%**; group = 177 ÷ 614.02 = **28.83%**; gap **2.80pp**
- Subsidiary reported OPM 30.26% − group 28.83% = **1.43pp**
- Implied prior-year OPM = 30.26 + 1.48 = **31.74%** against the Capital Market reading of 31.76% — a **0.02pp** discrepancy, i.e. the two sources agree
- PBT 30.96 − tax 7.58 = **23.38 = reported PAT exactly**; effective tax rate **24.48%**
- EPS growth **31.75%**; sequential revenue **+19.13%**, sequential PAT **+43.97%**

**D5 — margin on operating revenue.**
- Implied Q1 FY26 EBITDA = 177 ÷ 1.252 = **₹141.37 Cr**; margin **29.00%** → **28.83%** = **−17.81 bps**
- Rounding band: **−32.98 bps** to **−2.63 bps**, width **30.36 bps**, never crossing zero
- Total income implied by the reported 28.5% margin = **₹621.05 Cr**, i.e. other income of **₹7.03 Cr**

**D6 — where the profit came from.**
- PAT growth on the rounded ₹38 Cr base = **44.79%**; base implied by the reported 44.6% = **₹38.05 Cr**; spread **0.19pp**
- PAT margin **7.81% → 8.96%**, **+1.15pp**
- PAT growth − EBITDA growth = **19.40pp**
- Net debt reduction **₹216 Cr**, **−77.70%**; remaining net debt = **28.70%** of the reduction already delivered
- Standalone PAT growth **64.89%**

**D7 — the plan against the record.**
- Facilities at 31 Mar 2026 = 269 + 19 = **288**; **288 + 18 − 2 = 304** ✓ (a clean internal reconciliation)
- FY27 plan of 60 = **20.83%** of the 288-site network
- Q1 annualised gross additions = **72** = **1.20×** the plan
- Greenfield loss ₹30 Cr = **4.89%** of FY26 EBITDA, **17.86%** of FY26 PAT
- FY26 total income growth **20.94%**; FY26 margin on total income **28.89%**
- FY27 acquisition outflow midpoint **₹62.5 Cr**, **−26.47%** on FY26's ₹85 Cr; range width **8.00%** of midpoint

**D8 — the market, sized from the company's own base.**
- Annualised cataract = 67,444 × 4 = **269,776**
- NPCB&VI FY25 ÷ that = **36.33×**; company share **2.75%**
- NPCB&VI cataract CAGR FY21→FY25 = **28.89%**; FY24→FY25 = **8.54%**
- Annualised patients 3,528,000 = **30.01%** of NPCB&VI FY25 beneficiaries

**D9 — RICE.** Stress multiplier **10.33%**; harsher alternative available and unused **3.58%**. Baseline scores **33.08 / 17.99 / 10.58 / 9.40**; stressed **3.42 / 1.86 / 1.09 / 9.40**. Proposal **3rd of 4 at baseline, 4th and last under stress**; exempt initiative beats it **8.60×**; proposal loses **89.67%** of its score, which is the non-conversion rate by construction. Four assertions are enforced programmatically, including that the proposal is the weakest *stressed* initiative at baseline.

**D10 — metric basis difference.** Derived revenue per surgery is **1.57×** the company's FY26 ARPS of ₹42,900, a residual of **₹24,514** per surgery. Derived growth of 9.10% exceeds reported FY26 ARPS growth of 8.5% by **0.60pp**. Reported, not reconciled.

**D11 — entity and capacity.** IPO price × shares = **₹3,027.26 Cr** ✓. Doctors +**9.19%** on FY26's 968. Surgeries per doctor per quarter **86.17**; patients per doctor **834.44**. Authorised ÷ paid-up capital **2.85×**.

---

## Part 3 — Author constructs

Everything below was invented by the author and is not reported by the company.

1. **The *Agarwal Indicated* mechanism** — the indication ledger, the surgeon-set review window, facility ownership of the return, published indication thresholds, the Clinical Indication Audit function, and automatic recall suspension on breach.
2. **ICR/1k**, its four conjunctive conditions, and the choice of indicated deferrals as denominator.
3. **UPI-90**, its 90th-percentile construction, its three-quarter window, its per-facility and per-cohort reporting requirement and the 3.0% threshold.
4. **All four RICE initiatives and every input.** The proposal's Reach of 88.2k is set at 10% of quarterly footfall because the indicated-deferral pool is not disclosed. Sensitivity: the proposal remains third at baseline and last under stress for any Reach between roughly **78.33k and 149.88k** — a **1.91×** range — so the conclusion is insensitive to the construct.
5. **Phase 0 kill criteria K1–K3** and the 4,000-of-5,000 join threshold.
6. **The A/B design**, Arm B as the falsification arm, and both pre-registered decision rules including the 8-percentage-point margin.
7. **Personas (§20), the journey and flow diagrams (§22, §23), both wireframes (§52), the KPI dashboard targets (§55) and the roadmap windows (§56).**
8. **The framing of the public programme as a price floor rather than a competitor** (§11, §16) — an interpretation, not a disclosed fact.

---

## Part 4 — What would change my mind

| Evidence | Effect |
|---|---|
| **Q2 FY27 surgeries per facility flat or rising while facility count grows above 20%** | A1 is dead. The ramp was young and the company will have demonstrated it. This is the first row of §55 for a reason, and the company publishes both numbers itself. |
| Mature-facility surgical volume disclosed and growing faster than the network | A1 is dead by the cleanest possible route. |
| Phase 0 K1 fires: fewer than 20% of deferral-equivalent patients were ever operated in-network | The proposal is dead. There is no latent pool to convert. |
| Phase 0 K2 fires: deferral notes are not reliably recorded today | The proposal is dead in this form; capture discipline would have to be built first, which is a different and much larger project. |
| Arm B matches Arm C on ICR/1k | The apparatus is theatre. Run a reminder campaign and cancel the register. |
| The subsidiary's next filing shows margin recovery above the group's | The §14 finding weakens materially; the 148 bps becomes a one-quarter cost event. |
| Premium mix shift accelerates past roughly 1.5pp a year | The realisation lever is thicker than argued and can carry the network for longer than the case study allows. |

---

## Part 5 — What could not be found out

1. **Q1 FY26 patient volume.** Not disclosed in any source examined, so surgical conversion has **no trend**. This is the single largest gap in the case study and it is stated in §30, §45, §64 and here.
2. **Mature-facility metrics for Q1 FY27.** The company disclosed mature-facility revenue as recently as Q3 FY25 (₹291 Cr, +16.6%) and did not for this quarter in anything examined. Its absence is what keeps A1 at "direction".
3. **The product-versus-services revenue split for Q1 FY27.** The 78.6% / 21.4% split is the prior-year quarter's; the current split was not found.
4. **The composition of 16.36% of surgical volume** — 14,904 procedures that are neither cataract, refractive, nor any of the five separately named lines.
5. **Segment-level or geography-level profitability.** India versus international, and hub versus spoke, are not broken out.
6. **Any disclosed recall, follow-up, second-eye or outcome metric.** None found, which is the proposal's justification and also the reason its baseline cannot be estimated from outside.
7. **Indication thresholds.** No Indian eye-care chain examined publishes the clinical grade at which it recommends surgery.
8. **ASG and Maxivision financials.** Neither files audited results. No estimate was constructed for either.
9. **The exact FY26 closing surgery count.** Three of four quarters are disclosed; the fourth was not found, so no full-year throughput figure is computed.

---

*Companion to `README.md`, Day 76 of 90. All derived figures reproducible via `verify.py`.*
