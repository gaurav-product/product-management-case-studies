# ASSUMPTIONS — Day 73, Rainbow Children's Medicare Limited

**Case study:** Day 73 of 90 · Rainbow Children's Medicare Limited (CIN L85110TG1998PLC029914)
**Period examined:** Q1 FY27, quarter ended 30 June 2026, reported 30–31 July 2026
**Verification:** `verify.py`, 108 checks, all passing
**Written:** 8 September 2026

Part 1 states what is assumed and gives the rival reading equal weight. Part 2 shows the arithmetic. Part 3 lists what the author invented. Part 4 states what would falsify the thesis. Part 5 records what could not be found out.

---

## Part 1 — Assumptions

### A1 (load-bearing) — that the occupancy dilution is a strategic signal, not only a ramp artefact

**The assumption.** Occupancy falling from 45.3% to 41.2% while capacity grew 26% indicates that Rainbow is adding beds faster than demand is arriving to fill them, and that this matters for a plan requiring 52.98% more capacity.

**What supports it.** The arithmetic is exact and drawn entirely from disclosed figures: 2,435 capacity beds × 76.47% operational × 41.2% occupancy = **31.50% of built capacity in use.** 573 beds are built and not yet commissioned. The FY29 target of 3,725 beds implies **1,535 occupied beds at today's occupancy — 2.00× today's 767.** And the profit consequence is already visible: PAT grew at **48.19%** of the revenue rate with margin down 1.97 points, while newer Bengaluru units are disclosed as loss-making.

**The rival reading, given equal weight, and it is strong.** This is **exactly what a normal ramp looks like.** Operational beds grew 22% and new-hospital operational beds grew **130%**, so the blended occupancy figure is dominated by a weighting shift toward the newest cohort. Both cohorts individually improved. **Occupancy is up 3 percentage points year on year**, meaning that on an annual view Rainbow is filling beds faster than it is building them. Mature hospitals run at 45% with ARPOB up 10%, which is the model working. Management has ramped hospitals before and the historical curve is the basis of the plan. Under this reading, 31.50% is a snapshot mid-build and improves mechanically as the 2024–26 cohort matures.

**Why the case study proceeds anyway, and where it stops.** It proceeds because the *magnitude* of what must be filled is not in dispute under either reading — 2.00× today's occupied beds, funded at 1.17× annualised revenue — and because the utilisation of built capacity is not a number the company reports, so nobody is tracking the thing the plan depends on. **It stops short of claiming the expansion is a mistake.** §14, §36, §55 and §64 all state the ramp reading explicitly, and the top-ranked recommendation is *phasing* capex against occupancy, not cancelling it.

**What would settle it.** Two more quarters of the same multiplication. If occupied-beds-over-capacity rises while capacity keeps growing, A1 is wrong.

### A2 — that family retention after delivery is weak

The §33 funnel reading, the §22 journey and the entire §50 proposal rest on the claim that families met at a Rainbow delivery do not become continuing Rainbow paediatric customers. **Rainbow discloses no retention metric of any kind**, so this is an inference from three things: the absence of any continuity product in the disclosures, the 15-to-1 ratio of outpatient consultations to discharges, and management's stated digital priorities being acquisition-side (CRM, lead management, digital acquisition). **Rainbow may already retain families well and simply not report it.** K1 in §53 is written to kill the proposal outright if that is the case.

### A3 — that occupied beds can be derived by multiplication

Occupied beds of 767 are computed as operational beds × occupancy. This assumes the disclosed occupancy percentage is measured against **operational** beds rather than capacity beds — the standard convention and the one consistent with Rainbow's own mature-versus-new occupancy disclosures. If occupancy were measured against capacity beds instead, occupied beds would be 1,003 and the idle share would be 58.80% rather than 68.50%. **The finding survives either convention**; the specific figure does not, and this is flagged wherever used.

### A4 — that implied ALOS of 2.60 days is meaningful

Average length of stay is derived as occupied bed-days ÷ discharges, using 91 days for the quarter. This ignores outpatient day-cases and any admissions spanning the quarter boundary, so it is indicative rather than exact. It is used descriptively in §18 and §30 and is load-bearing nowhere.

### A5 — that Q1 is not distorted by seasonality

Paediatric demand is seasonal, and one source explicitly attributed part of the sequential decline to "seasonal weakness." This case study does not adjust for it and does not have the quarterly history to do so reliably. **That is a genuine limitation**: some part of the 4.1-point sequential fall may be seasonal rather than structural, which would weaken A1.

---

## Part 2 — Derivations

Every figure below is asserted in `verify.py`. Tags map to that file.

### D1 — Revenue, EBITDA, PAT

Implied prior-year revenue **₹352.85 Cr**, EBITDA **₹103.62 Cr**, PAT **₹53.88 Cr** (D1a–D1c). PAT growth is **48.19%** of revenue growth (D1d), a gap of **17.20 points** (D1e). EBITDA margin **28.64%** against a prior **29.37%** — down **0.73 points** (D1f–D1h). PAT margin **13.30%** against **15.27%** — down **1.97 points** (D1i–D1k).

### D2 — Idle capacity

Occupied beds **767.14** (D2a) — **31.50%** of capacity beds (D2b), leaving **68.50%** earning nothing (D2c). Operational beds are **76.47%** of capacity (D2d), with **573** capacity beds not yet operational (D2e). Empty operational beds **1,094.86** (D2f), **58.80%** of operational (D2g). On the 2,565-bed basis including Madhukar, occupied beds are **29.91%** (D2h).

### D3 — Occupancy trajectory

Sequential change **−4.10 points**, **−9.05%** relative (D3a, D3b). Implied prior-year occupancy **38.20%** (D3c). Mature minus new **10.60 points** (D3d); new is **76.44%** of mature (D3e). Capacity grew **26%** against a 3-point occupancy gain (D3f); capacity growth was **1.18×** operational bed growth (D3g).

### D4 — ARPOB

Mature commands a **19.77%** premium over new (D4a), **₹11,662** (D4b). Blended is **95.18%** of mature (D4c) and **13.99%** above new (D4d). Blended ARPOB growth of 6% is exactly the historical annual rate (D4e); mature ARPOB grew **1.67×** the blended rate (D4f); sequential growth was **1.28×** the year-on-year rate (D4g).

### D5 — Bought versus built

Acquisitions were **8.09%** of revenue (D5a). Organic revenue **₹432 Cr** (D5b), organic growth **22.43%** (D5c). Inorganic contributed **10.77 points** (D5d), **32.44%** of reported growth (D5e). Organic growth exceeded the 20% medium-term target by **2.43 points** (D5f).

### D6 — Expansion

Annualised revenue **₹1,880 Cr** (D6a). The FY29 target is **52.98%** above current capacity (D6b); the five-year pipeline is **102.67%** of it (D6c); beds in development are **49.28%** (D6d). Capex is **1.17×** annualised revenue (D6e) at **₹88 lakh per pipeline bed** (D6f). At today's occupancy the FY29 estate implies **1,534.70** occupied beds (D6g) — **2.00×** today's (D6h).

### D7 — Volume and throughput

Occupied bed-days **69,810** (D7a); implied ALOS **2.60 days** (D7b). **83.62** outpatient consultations and **5.48** discharges per delivery (D7c, D7d). Annualised deliveries **19,640** (D7e). Discharge growth exceeded delivery growth by **5.00 points** (D7f). Revenue per discharge **₹174,812** (D7g); outpatient consultations per operational bed **220.51** (D7h).

### D8 — Stress rule

**31.50%**, occupied beds as a share of capacity beds (D8a). Alternatives computed and not used: occupancy of operational beds at **41.20%** (D8b) and new-hospital occupancy at **34.40%** (D8c).

### D9 — RICE

| Initiative | Base | Stressed |
|---|---|---|
| Capex phasing against occupancy (exempt) | 77.92 | **77.92** |
| Geographic expansion, Mumbai/NCR | 22.16 | 6.98 |
| **Rainbow Continuity (PROPOSED)** | **16.59** | **5.23** |
| ALOS and throughput optimisation (exempt) | 15.04 | 15.04 |

Proposal ranks **3rd at baseline, 4th and last under stress** (D9a, D9b). `verify.py` asserts it is the **weakest stressed initiative at baseline** (D9c) and that it finishes last (D9d). The stressed winner beats it by **14.91×** (D9e).

---

## Part 3 — Constructs

Everything here is the author's invention. None is a Rainbow disclosure, plan or statement.

| Construct | What it is |
|---|---|
| **Rainbow Continuity** | The proposed product: a family membership from delivery through childhood covering preventive care only |
| **CFY/1k** | Proposed North Star — continuous family-years per 1,000 *births attended*, four conjunctive conditions |
| **AAR-90** | Proposed guardrail — avoidable admission rate at the 90th percentile of membership penetration, by hospital |
| The inpatient / ambulatory seam | The §16 double Porter's framing; not a reported segmentation |
| The dilution loop | §36 — an analytical construction from disclosed capacity and occupancy figures |
| Occupied beds and idle share | Derived by multiplication (A3) |
| Implied ALOS | Derived from occupied bed-days ÷ discharges (A4) |
| Prior-year financials | Back-derived from reported growth rates |
| RICE inputs | All reach, impact, confidence and effort values in §47 |
| Stress rule application | 31.50% is computed from disclosed figures; using it as a RICE multiplier is the author's construction |
| Phase 0 kill criteria | K1, K2, K3 in §53, including the judgement that K2 is most likely to fire |
| §54 arms and R1 rule | The falsification design and the 10-point threshold |
| Personas | §20 — illustrative, not researched individuals |

---

## Part 4 — What would change my mind

1. **Occupied-beds-over-capacity rising over the next two quarters while capacity keeps growing.** This is the direct test of A1, computable by anyone from three figures Rainbow already publishes, and it is what management's ramp thesis predicts.
2. **Disclosure that new hospitals are ramping on the historical curve**, with cohort-level occupancy by vintage. That would convert the dilution from a signal into a schedule.
3. **Evidence that families delivering at Rainbow already return for paediatric care.** A2 dies, K1 fires, and §50 becomes unnecessary — Rainbow would already have the relationship it is being told to build.
4. **A disclosed seasonality pattern explaining the sequential fall.** A5 concedes this is possible; a quarterly occupancy history showing a recurring Q1 dip would materially weaken the sequential reading.
5. **Capex proving substantially discretionary.** If most of the ₹2,200 Cr is uncommitted and genuinely phaseable, the top-ranked recommendation is already available to management and the risk in §57 is smaller than stated.

---

## Part 5 — What could not be found out

- **Revenue split between inpatient, outpatient and deliveries**, so the 15-to-1 contact ratio in §16 cannot be converted into a revenue ratio. The most consequential gap for sizing §50.
- **Any family-level retention, repeat-visit or NPS measure** — the quantity A2 infers and CFY/1k is designed to create.
- **Whether a family can be resolved across BirthRight and paediatrics** and across hospitals; the subject of K2 and the largest unknown in costing the proposal.
- **Hospital-level or cohort-level profitability** beyond the disclosed statement that newer Bengaluru units are loss-making, and the timeline to their breakeven.
- **The split of the ₹2,200 Cr capex between committed and discretionary**, which determines how much of §47's top-ranked initiative is actually available.
- **Outpatient revenue per consultation**, so the ambulatory business cannot be sized independently.
- **A quarterly occupancy history** long enough to separate seasonality from trend (A5).
- **Paediatric bed occupancy benchmarks** for comparable single-specialty operators, so 41.2% cannot be judged against a peer norm.
- **A filed transcript** of the Q1 FY27 earnings call in the sources used; call detail comes from coverage and is graded 🟡 accordingly.
