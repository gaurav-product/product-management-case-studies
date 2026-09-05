# ASSUMPTIONS — Day 70, Poly Medicure Limited

**Case study:** Day 70 of 90 · Poly Medicure Limited (CIN L40300DL1995PLC066923)
**Period examined:** Q1 FY27, quarter ended 30 June 2026, board approved 7 August 2026
**Verification:** `verify.py`, 114 checks, all passing
**Written:** 5 September 2026

Part 1 states what is assumed and gives the rival reading equal weight. Part 2 shows the arithmetic. Part 3 lists what the author invented. Part 4 states what would falsify the thesis. Part 5 records what could not be found out.

---

## Part 1 — Assumptions

### A1 (load-bearing) — that the standalone/consolidated gap reflects acquisition economics rather than a one-off

**The assumption.** The ₹2.85 Cr by which standalone PAT exceeds consolidated PAT represents the operating economics of the acquired businesses, and indicates a structural cost-base problem rather than a timing artefact.

**What supports it.** The subtraction itself is exact and requires no estimation: standalone PAT ₹88.12 Cr, consolidated PAT ₹85.27 Cr, both in the same filing. The implied subsidiary revenue of ₹94.28 Cr reconciles with the disclosed ₹72.3 Cr of acquisition revenue plus pre-existing foreign subsidiaries. And the mechanism is visible in the margin structure rather than only in the bottom line: **consolidated gross margin is 1.90 points above standalone while consolidated EBITDA margin is 3.90 points below**, so the gap opens between gross profit and EBITDA — which is where overhead sits, not where one-off charges usually sit.

**The rival reading, given equal weight, and it is strong.** These are **first-year, integration-mode assets**. First-year consolidation of an acquisition routinely carries transaction costs, purchase-price allocation amortisation, duplicated management, systems migration and severance — all of which depress reported margin without saying anything about the underlying business. Management explicitly attributed margin pressure to "higher costs from acquisitions" and described the entities as in integration. Under this reading, ₹2.85 Cr of negative contribution on a portfolio bought within the year is unremarkable, and the correct response is patience rather than strategy change.

**Why the case study proceeds anyway, and where it stops.** It proceeds because the *structural* observation survives either reading: **an acquired European product carries an acquired European cost base, and Poly Medicure's competitive advantage is specifically a cost base.** That is true whether or not this quarter's figure normalises. **It stops short of claiming the acquisitions were bad decisions.** §14 and §64 both say a snapshot cannot separate integration cost from structural cost, and §55's first row makes it a two-quarter test rather than a verdict.

**What would settle it.** Two more quarters. If the subsidiary EBITDA margin climbs from 6.27% toward the parent's 28.0%, A1 is wrong and integration was the whole story.

### A2 — that the derived subsidiary figures are a fair representation

Subsidiary revenue, PAT and EBITDA are all obtained by subtracting standalone from consolidated. That subtraction is arithmetically exact for revenue and PAT. **For EBITDA it is not exact**, because it applies rounded reported margins (28.0% and 24.1%) to precise revenue figures, so the derived ₹5.91 Cr subsidiary EBITDA carries rounding sensitivity of roughly ±₹2.6 Cr. The finding rests on the *direction and magnitude* of the gap, which survives any plausible rounding; the precise figure should be read as indicative and is flagged as such in Appendix A-5.

A second limitation: consolidation adjustments and inter-company eliminations are not disclosed, so the "subsidiary" residual technically includes any consolidation entries as well as the subsidiaries themselves.

### A3 — that the acquired entities are the main content of the residual

The residual is attributed to acquisitions because ₹72.3 Cr of the ₹94.28 Cr subsidiary revenue is disclosed as acquisition contribution. The remaining ₹21.98 Cr belongs to pre-existing foreign subsidiaries — including Polymed Brazil — whose separate economics are not disclosed. **So the residual is not purely acquisition-driven**, and a well-performing legacy subsidiary would mean the acquisitions are worse than the blended figure implies, while a loss-making legacy subsidiary would mean they are better.

### A4 — that Q1 is informative about the year

One quarter is short, and Poly Medicure's guidance implies acceleration: the run rate is 89.43% of the midpoint. Management also guided that standalone gross margin will normalise **down** to 68–69% from the reported 71.5%, which means the parent's margin advantage over the subsidiaries would narrow somewhat on that measure alone. This case study does not assume the guidance is missed and does not extrapolate the quarter.

---

## Part 2 — Derivations

Every figure below is asserted in `verify.py`. Tags map to that file.

### D1 — Consolidated versus standalone

| Measure | Value | Tag |
|---|---|---|
| Consolidated revenue growth, computed | **+30.30%** | D1a |
| Consolidated PAT change, computed | **−8.39%** | D1b |
| Standalone revenue growth, computed | **+12.25%** | D1c |
| Standalone PAT growth, computed | **+0.22%** | D1d |
| Swing between consolidated revenue and PAT growth | **38.69 pp** | D1e |
| Consolidated growth ÷ standalone growth | **2.47×** | D1f |

### D2 — What the subsidiaries contributed

Subsidiary PAT **−₹2.85 Cr** (D2a) on subsidiary revenue **₹94.28 Cr** (D2b) — a net margin of **−3.02%** (D2c) against the parent's **+20.44%** (D2d) and a consolidated **+16.23%** (D2e). Consolidation diluted net margin by **4.21 points** (D2f). Subsidiaries were **17.95%** of consolidated revenue (D2g). **Standalone PAT is 103.34% of consolidated PAT** (D2i).

### D3 — Bought versus built

Inorganic contribution **17.90 points** (D3a), **59.08%** of consolidated growth (D3b); organic was **40.92%** (D3d). Acquisitions were **13.76%** of consolidated revenue (D3c). Consolidated international growth exceeded standalone international growth by **26.70 points** (D3e), a ratio of **3.67×** (D3f).

### D4 — The margin paradox

Consolidated gross margin is **1.90 points above** standalone (D4a) while consolidated EBITDA margin is **3.90 points below** (D4b). Gross-to-EBITDA conversion: standalone **39.16%**, consolidated **32.83%** (D4c, D4d) — a gap of **6.33 points** (D4e). Standalone EBITDA **₹120.71 Cr**, consolidated **₹126.62 Cr**, implied subsidiary **₹5.91 Cr** (D4f–D4h) at a **6.27%** margin (D4i) — **22.38%** of the parent's (D4j). Reported standalone gross margin sits **2.50 to 3.50 points above** the guided normal range (D4k, D4l).

### D5 — Organic pressure

Renal growth was **31.02%** of standalone revenue growth (D5a), a shortfall of **8.45 points** (D5b). Employee costs grew **16.75 points faster** than standalone revenue (D5c), a ratio of **2.37×** (D5d). Middle East exports **−32%** (D5f). US exposure is roughly **1.57%** of annualised consolidated revenue at an assumed 88 INR/USD (D5g, Appendix A-8).

### D6 — Guidance

Consolidated annualised **₹2,101.50 Cr** (D6a), standalone **₹1,724.40 Cr** (D6b) — **89.43%** and **88.43%** of their guidance midpoints (D6c, D6d). The shortfall to the consolidated guidance floor is **₹198.50 Cr** (D6e); Q1 delivered **22.36%** of the midpoint (D6f). Reaching the guidance floor requires the remaining quarters to average **12.59% above** Q1 revenue (D6g). Standalone EBITDA margin came in **1.00 point above** the guided top (D6h); consolidated **1.10 points above** the guided bottom (D6i).

### D7 — Balance sheet

Cash of ₹854.7 Cr is **1.63×** quarterly consolidated revenue (D7a), **3.42×** standalone working capital debt (D7b) and **40.67%** of annualised revenue (D7c). The 140-day working capital cycle is **38.36%** of a year (D7d). The annualised run rate is **1.24×** FY25 revenue (D7e).

### D8 — Stress rule

**22.38%**, the subsidiary EBITDA margin as a share of the parent's (D8a). Alternatives computed and not used: the subsidiary **net** margin is **−3.02%** and unusable as a multiplier (D8b), and the organic share of growth at **40.92%** would have been far more generous (D8c).

### D9 — RICE

| Initiative | Base | Stressed |
|---|---|---|
| Integration opex programme (exempt) | 40.07 | **40.07** |
| High-complexity product expansion | 63.23 | 14.15 |
| **Licence-to-Make (PROPOSED)** | **16.76** | **3.75** |
| Working capital reduction (exempt) | 14.01 | 14.01 |

Proposal ranks **3rd at baseline, 4th and last under stress** (D9b, D9c). `verify.py` asserts it is the **weakest stressed initiative at baseline** (D9d) and that it finishes last (D9e). The stressed winner beats it by **10.68×** (D9f).

---

## Part 3 — Constructs

Everything here is the author's invention. None is a Poly Medicure disclosure, plan or statement.

| Construct | What it is |
|---|---|
| **Licence-to-Make** | The proposed instrument: license high-complexity designs and manufacture them in Indian facilities rather than acquiring the owning entities |
| **LMR/100** | Proposed North Star — licence-manufactured revenue per ₹100 of *high-complexity revenue*, four conjunctive conditions |
| **QDR-90** | Proposed guardrail — quality deviation rate at the 90th percentile of licensed-line volume, against the licensor's pre-transfer baseline |
| The parent / subsidiary seam | The §16 double Porter's framing; not a reported segmentation |
| Subsidiary EBITDA and margin | Derived from rounded reported margins (A2) |
| Attribution of the residual to acquisitions | An inference from the disclosed ₹72.3 Cr contribution (A3) |
| RICE inputs | All reach, impact, confidence and effort values in §47 |
| Stress rule application | 22.38% is derived from disclosed margins; using it as a RICE multiplier is the author's construction |
| Phase 0 kill criteria | K1, K2, K3 in §53, including the judgement that K2 is most likely to fire |
| §54 matched-pair arms and R1 rule | The falsification design and the 6-point threshold |
| Personas | §20 — illustrative, not researched individuals |
| USD/INR rate of 88 | Assumed for D5g only (A-8) |

---

## Part 4 — What would change my mind

1. **Subsidiary EBITDA margin climbing toward the parent's over the next two quarters.** This is the direct refutation of A1 and the outcome management's own integration framing predicts. It is computable by anyone from the next two filings using the same subtraction.
2. **Per-entity disclosure showing one weak asset rather than a uniformly weak portfolio.** The strategic response to a single bad acquisition is entirely different from the response to a structural cost-base problem, and the blended figure cannot distinguish them.
3. **Evidence that approvals are genuinely site-bound.** If K1 fires, licensing offers no time advantage over acquisition and the proposal is not merely last on the list but wrong.
4. **Arm B closing the margin gap.** If applying the parent's operating disciplines at an acquired European site recovers most of the gap between 6.27% and 28.0%, the binding constraint was management, not geography — and the acquisition strategy is sound as long as integration improves.
5. **Standalone gross margin normalising to 68–69% as guided while consolidated holds at 73.4%.** That would narrow the parent's apparent advantage and weaken the framing of the acquired products as high-margin-but-expensive-to-run.

---

## Part 5 — What could not be found out

- **Per-acquisition economics** — revenue, EBITDA, purchase price, integration cost or timetable for any individual acquired entity. The most consequential gap; it forces the blended treatment throughout.
- **The split between newly acquired entities and pre-existing foreign subsidiaries** within the ₹94.28 Cr residual (A3).
- **Consolidation adjustments and inter-company eliminations**, which are included in the derived residual and cannot be separated from it.
- **Renal revenue in absolute terms**, so the 3.8% growth cannot be sized against the rest of the portfolio.
- **The therapeutic-area split of the ₹72.3 Cr acquisition contribution.**
- **Whether the acquired entities' regulatory approvals are site-bound** — the question K1 exists to answer and the one the entire proposal depends on.
- **Any published clinical outcome, complaint-rate or field-action data** for Poly Medicure's own devices.
- **A filed transcript of the Q1 FY27 earnings call** in the sources used; segment and cost commentary comes from call coverage and is graded 🟡 accordingly.
