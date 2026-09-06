# ASSUMPTIONS — Day 71, Akums Drugs and Pharmaceuticals Limited

**Case study:** Day 71 of 90 · Akums Drugs and Pharmaceuticals Limited (CIN L24239DL2004PLC125888)
**Period examined:** Q1 FY27, quarter ended 30 June 2026, announced 10 August 2026
**Verification:** `verify.py`, 107 checks, all passing
**Written:** 6 September 2026

Part 1 states what is assumed and gives the rival reading equal weight. Part 2 shows the arithmetic. Part 3 lists what the author invented. Part 4 states what would falsify the thesis. Part 5 records what could not be found out.

---

## Part 1 — Assumptions

### A1 (load-bearing) — that the branded segments are structurally constrained rather than merely underperforming

**The assumption.** The non-CDMO segments are not shrinking because they are badly run. They are shrinking because growing them requires Akums to compete with the clients who supply 82.63% of its revenue, and that conflict caps them.

**What supports it.** The growth spread is disclosed and enormous: **CDMO +18.57%, everything else −3.98%** — 22.56 points apart, in the same quarter, under one management team, in one market, with one balance sheet. That rules out macro, input-cost and capital explanations in a single comparison. The structural argument is then straightforward: a CDMO client's product manager and Akums's branded field force call on the same doctor about the same molecule, and a client who sees its manufacturer competing for its prescriptions has an obvious response. The company's own strategy, read as a list, is almost entirely more contract manufacturing — the Oriflame acquisition is manufacturing for a brand owner, the Zambia order is supply — which suggests management has drawn a similar conclusion in practice.

**The rival reading, given equal weight, and it is strong.** **API is separately disclosed as loss-making**, and it is 2.7% of revenue. If API accounts for most of the −3.98% and most of the ₹12 Cr EBITDA shortfall, then domestic branded formulations may be performing acceptably and the "structural cap" is a story imposed on ordinary segment noise. Management's own framing supports this reading: it described the branded segments as **muted with initiatives underway to restore growth** — a temporary-underperformance framing, not a structural-limit one. And management guided API to monthly EBITDA break-even by end FY27 and profitability in FY28, which is a company that believes the drag is fixable and identified.

**Why the case study proceeds anyway, and where it stops.** It proceeds because the *structural* claim does not depend on which segment is dragging: a CDMO growing its own competing brands faces a conflict whether or not that conflict is currently binding, and §36's loop is a property of the model rather than of the quarter. **It stops short of claiming the branded businesses are failing.** §14, §45, §64 and Appendix A-4 all state that segment EBITDA is disclosed for CDMO only and that API cannot be separated from branded within the residual.

**What would settle it in one disclosure.** Segment EBITDA for all five segments — which §48 lists as a "Must" and which costs Akums nothing but a reporting decision.

### A2 — that the non-CDMO residual is a fair representation

Non-CDMO revenue and EBITDA are obtained by subtracting the disclosed CDMO figures from the disclosed group figures. **For revenue this is exact.** For EBITDA it is exact as arithmetic but coarse as description: ₹12 Cr blends four businesses of unknown individual profitability, and includes any unallocated corporate cost that sits outside the CDMO segment. A well-performing branded business and a badly-performing one are indistinguishable inside it.

### A3 — that "high teens" volume growth can be read as 17%

The 6.8× industry multiple in D7b uses 17% against an industry midpoint of 2.5%. "High teens" is a verbal range from the earnings call, not a reported figure. At 16% the multiple is 6.4×; at 18% it is 7.2×. **No conclusion in this case study turns on which end is right**, and the range is flagged wherever the figure is used (Appendix A-5).

### A4 — that Q1 CDMO margin is above trend

CDMO EBITDA margin of 16.91% sits **1.91 points above the top of the company's own 14–15% guidance**, and management attributed part of the improvement to API prices it described as volatile. This analysis treats 16.91% as a favourable-input peak rather than a run rate, and §57 says so. Any projection built on 16.91% persisting would be this case study's, not the company's.

### A5 — that Akums's data asset is genuinely distinctive

§50 rests on the claim that Akums observes market demand across a breadth no single client can reconstruct. That follows from its position as India's largest CDMO, but **the number of clients and the share of the market they represent are not disclosed**, so the breadth is asserted from market position rather than measured. K1 and K3 in §53 are both built to test it before anything is built.

---

## Part 2 — Derivations

Every figure below is asserted in `verify.py`. Tags map to that file.

### D1 — The headline

| Measure | Value | Tag |
|---|---|---|
| Revenue growth, computed | **+13.93%** | D1a |
| PAT growth, computed from reported figures | **+55.38%** | D1b |
| Gap to reported PAT growth | **0.72 pp** | D1c |
| Prior-year PAT implied by the reported rate | **₹64.70 Cr** | D1d |
| EBITDA margin expansion | **240 bps** | D1e |
| PAT margin, computed | **8.66%** | D1h |
| Other income implied | **₹30.37 Cr** | D1i |

### D2 — CDMO versus everything else

Non-CDMO revenue **₹202.63 Cr** against **₹211.03 Cr** a year earlier (D2a, D2b) — a decline of **₹8.40 Cr, −3.98%** (D2c, D2d). CDMO grew **18.57%** (D2e). The spread is **22.56 points** (D2f). CDMO is **82.63%** of revenue, non-CDMO **17.37%** (D2g, D2h).

### D3 — Profit concentration

Non-CDMO EBITDA **₹12 Cr** by subtraction (D3a). CDMO is **93.14%** of group EBITDA, non-CDMO **6.86%** (D3b, D3c). CDMO EBITDA margin **16.91%**, non-CDMO **5.92%** (D3d, D3e) — a **2.86×** gap (D3f). Non-CDMO earns at **0.39×** its revenue weight; CDMO at **1.13×** (D3g, D3h). CDMO EBITDA grew **36.97%** computed (D3i), with margin up **227 bps** from 14.64% (D3j, D3k).

### D4 — Operating leverage

Group EBITDA grew **2.54×** as fast as revenue (D4a); CDMO EBITDA **1.98×** as fast as CDMO revenue (D4b) — a **21.48-point** gap between group EBITDA and revenue growth (D4c). Other income is **14.63%** of EBITDA-including-other-income (D4e), and grew more slowly, leaving a **3.70-point** gap between the two EBITDA growth rates (D4d). CDMO margin sits **1.91 points** above the guided top end (D4f).

### D5 — Mix

Disclosed segment shares sum to **100.0%** (D5a), and the disclosed CDMO share of 82.6% matches the computed 82.63% to **0.03 points** (D5b). Branded segments combined are **12.90%** of revenue, **₹150.50 Cr** (D5c, D5d) — **4.78×** API revenue of ₹31.50 Cr (D5e, D5g). Trade generics **₹21.00 Cr** (D5f).

### D6 — Cash and actions

Net cash is **1.39×** quarterly revenue and **34.63%** of annualised revenue (D6a, D6b). The Oriflame acquisition is **3.47%** of net cash and **4.80%** of a quarter's revenue (D6c, D6d). The Zambia order is **5.14%** of annualised revenue and **1.18×** a full quarter of non-CDMO revenue (D6e, D6f). The stock closed at **98.57%** of its 52-week high (D6g).

### D7 — Volume

Industry volume midpoint **2.50%** (D7a). Akums at 17% is **6.80×** the midpoint and **5.67×** the top end (D7b, D7c) — a premium of **14.50 points** (D7d).

### D8 — Stress rule

**6.86%**, the non-CDMO share of group EBITDA (D8a). Alternatives computed and not used: the non-CDMO **revenue** share of **17.37%** would have been far more generous (D8b), and non-CDMO revenue growth is **−3.98%** and unusable as a multiplier (D8c).

### D9 — RICE

| Initiative | Base | Stressed |
|---|---|---|
| CDMO capacity and client depth (exempt) | 136.57 | **136.57** |
| Branded formulations revival | 31.17 | 2.14 |
| **Client Insight (PROPOSED)** | **28.12** | **1.93** |
| API turnaround to break-even (exempt) | 14.70 | 14.70 |

Proposal ranks **3rd at baseline, 4th and last under stress** (D9d, D9e). `verify.py` asserts it is the **weakest stressed initiative at baseline** (D9f) and that it finishes last (D9g). The stressed winner beats it by **70.83×** (D9h).

---

## Part 3 — Constructs

Everything here is the author's invention. None is an Akums disclosure, plan or statement.

| Construct | What it is |
|---|---|
| **Client Insight** | The proposed product: separately-contracted market intelligence sold to existing CDMO clients from aggregated, de-identified order data |
| **CPI/100** | Proposed North Star — client-paid insight revenue per ₹100 of *CDMO revenue*, four conjunctive conditions |
| **RIR-90** | Proposed guardrail — re-identification risk at the 90th percentile of client concentration, by therapeutic category |
| The CDMO / branded seam | The §16 double Porter's framing; not a reported segmentation |
| The self-limiting loop | §36 — an inference from the business model, not a company statement (A1) |
| Non-CDMO EBITDA and margin | Derived by subtraction; blends four segments (A2) |
| "High teens" read as 17% | A3 |
| RICE inputs | All reach, impact, confidence and effort values in §47 |
| Stress rule application | 6.86% is derived from disclosed figures; using it as a RICE multiplier is the author's construction |
| Phase 0 kill criteria | K1, K2, K3 in §53, including the judgement that K2 is most likely to fire |
| §54 matched-cohort arms and R1 | The falsification design and the 0.50 CPI/100 threshold |
| Personas | §20 — illustrative, not researched individuals |

---

## Part 4 — What would change my mind

1. **Segment EBITDA published for all five segments, showing API as the whole of the drag.** This is the direct test of A1, it costs Akums nothing but a reporting decision, and it would show the branded businesses are healthier than the blended residual implies.
2. **Domestic branded formulations returning to growth while CDMO growth holds.** If both halves can compound simultaneously, the conflict is not binding at current scale and §36's loop is theoretical rather than operative.
3. **Evidence that clients are indifferent to Akums's branded presence** — for instance, disclosed client concentration stable or improving while Akumentis grows. That would falsify the central mechanism directly.
4. **K2 firing in Phase 0.** If existing contracts prohibit any secondary use of order data, the proposal is not merely last on the list; it is unbuildable from the existing book, and only new business could ever participate.
5. **CDMO margin normalising to 14–15% as guided while non-CDMO margin holds.** That would narrow the 2.86× gap materially and weaken the framing of CDMO as structurally superior rather than currently favoured by input prices.

---

## Part 5 — What could not be found out

- **EBITDA for domestic branded, international branded, API and trade generics individually.** The single most consequential gap; it forces the blended residual throughout and prevents separating A1 from its rival reading.
- **Client concentration by therapeutic category**, which determines whether the §50 product is buildable at all and is the subject of K1.
- **Whether existing manufacturing contracts permit secondary use of order data** — K2, and the question on which the entire proposal turns.
- **The number of CDMO clients** and the share of Indian formulations manufacturing they represent, so the breadth claim in A5 rests on market position rather than measurement.
- **How much of the 227 bps CDMO margin expansion is API pricing** versus operating leverage; management attributed part to API prices without quantifying the split.
- **On-time-in-full, audit outcomes or batch-rejection data** — the metrics a CDMO client actually buys on, none of which is published.
- **Unallocated corporate costs**, which sit inside the derived non-CDMO EBITDA residual and cannot be separated from segment performance.
- **A filed transcript** of the Q1 FY27 earnings call in the sources used; call detail comes from coverage and is graded 🟡 accordingly.
