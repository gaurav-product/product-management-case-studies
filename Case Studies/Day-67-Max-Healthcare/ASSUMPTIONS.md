# ASSUMPTIONS — Day 67, Max Healthcare Institute Limited

**Case study:** Day 67 of 90 · Max Healthcare Institute Limited (CIN L72200MH2001PLC322854)
**Period examined:** Q1 FY27, quarter ended 30 June 2026, reported 13 August 2026
**Verification:** `verify.py`, 108 checks, all passing
**Written:** 2 September 2026

This file exists so that every judgement in README.md can be separated from every fact. Part 1 states what is assumed and gives the rival reading equal weight. Part 2 shows the arithmetic. Part 3 lists what the author invented. Part 4 states what would falsify the thesis. Part 5 records what could not be found out.

---

## Part 1 — Assumptions

### A1 (load-bearing) — that mix, not price, drove the 5% ARPOB increase

**The assumption.** Max's reported ARPOB growth of 5% to ₹81,900 in Q1 FY27 reflects a change in what Max treated and who it treated, rather than an increase in what Max charges per unit of care.

**What supports it.** Three things, none of them opinion. First, ARPOB is definitionally revenue divided by occupied bed days, and reconstructing it from the two disclosed growth rates — revenue +15.85%, OBD +10% — yields **5.32%**, against a reported 5%. There is no tariff term in that calculation. Second, Apollo Hospitals discontinued reporting ARPOB on exactly this basis, stating that it blends pricing, length of stay and occupancy and that a high reading can reflect acuity mix and bed turnover rather than patient revenue. Third, the disclosed mix moved in the direction the assumption predicts: international patients, the only segment Max prices unilaterally, grew at **1.14×** the network rate.

**The rival reading, given equal weight.** Prices genuinely did rise this quarter. Max disclosed that insurance renewals now carry an **automatic 6% price revision**, and that CGHS complex-specialty rates began flowing from June. Both are real price events inside the quarter, and either could contribute several points of ARPOB growth. Under this reading the 5% is substantially price, and the case study's central claim is wrong.

**Why the case study proceeds anyway, and where it stops.** It proceeds because the *capability* claim survives regardless: a metric that can rise 5% with no price change is not a price metric, and Apollo said so first. It stops short of quantifying the split, because Max publishes neither payer mix, case mix nor length of stay. **This case study can show ARPOB is uninterpretable; it cannot show what the correct interpretation is.** That distinction is maintained throughout §14, §30 and §47, and it is why the recommended first action is decomposition rather than repricing.

**What would settle it in one disclosure.** The decomposition §47 ranks first. If Max published price, acuity, length-of-stay and payer-mix effects separately, A1 would be confirmed or refuted immediately — which is a large part of why that initiative outranks the author's own proposal.

### A2 — that the international share is a fair proxy for unilaterally-priced revenue

The stress rule uses the disclosed 9% international share of hospital revenue as the portion of revenue Max prices without a counterparty's agreement. This under-counts: domestic self-pay patients also pay list prices and are not separately disclosed, so the true unilaterally-priced share is somewhat above 9%. The rule is therefore **conservative against the author's own proposal**, which is the correct direction for a stress test, and no attempt was made to inflate it.

### A3 — that the 2025 cashless disputes describe the 2026 pricing environment

The AHPI–Bajaj Allianz, AHPI–Star Health and Niva Bupa–Max suspensions all occurred in 2025. This case study treats them as evidence about the negotiating environment Max operated in during the June 2026 quarter. That is an inference across a year. It is supported by the disclosure of a 6% automatic revision in FY27 renewals — a settlement mechanism only necessary because the negotiation was contested — but the disputes themselves are not 2026 events and are dated wherever cited.

### A4 — that network gross revenue is the right denominator for growth comparisons

Max reports three revenue figures for the same quarter (Appendix A-2). This analysis uses network gross revenue of ₹2,982 Cr for growth and mix, because it is the figure the company itself uses for the ARPOB and segment discussion. Computed margin on that base is 23.61% against a reported 24.8%, and both are stated rather than reconciled.

---

## Part 2 — Derivations

Every figure below is asserted in `verify.py`. Tags map to that file.

### D1 — The metric ladder

| Measure | Value | Tag |
|---|---|---|
| Network revenue growth YoY | **15.85%** | D1a |
| Network PAT growth YoY | **3.48%** | D1b |
| PAT change QoQ | **−7.75%** | D1c |
| Revenue growth ÷ PAT growth | **4.56×** | D1d |
| ARPOB growth YoY | **5.00%** | D1e |
| PAT growth as share of revenue growth | **21.94%** | D1g |

### D2 — ARPOB reconstructed

Revenue growth of 15.85% over OBD growth of 10% gives **5.32%** (D2c); using the rounded 16% headline, **5.45%** (D2a). Reported ARPOB growth is 5.00%. The reconstruction contains only revenue and volume — **no price term exists in it**.

Against medical inflation of 7–8%, ARPOB growth of 5% is **2 to 3 points negative in real terms** (D2d, D2e), and is **71.43%** of the low end (D2f). On a two-year view the ARPOB CAGR from Q1 FY25 is **3.07%** (D2i), **3.93 points below** low-end medical inflation (D2j).

### D3 — Mix

Implied hospital revenue = ₹247 Cr ÷ 9% = **₹2,744.44 Cr** (D3a), **92.03%** of network revenue (D3b). International growth exceeds network growth by **2.15pp**, a ratio of **1.14×** (D3c, D3d). Kalinga entered at an ARPOB of ₹35,000, **42.74%** of network ARPOB and a **57.27% discount** (D3e, D3f) — and network ARPOB rose regardless, which is the mix effect made visible.

### D4 — The margin denominator

Computed EBITDA margin on network gross revenue is **23.61%** (D4a) against a reported **24.8%**, a gap of **1.19pp** (D4c). The reported margin implies a revenue base of **₹2,838.71 Cr** (D4d), **₹143.29 Cr** or **4.81%** below network gross (D4e, D4f). Consolidated revenue is **79.35%** of network (D4g), a further ₹615.83 Cr apart (D4h). All three are disclosed; none is treated as authoritative over the others.

### D5 — Capacity vs utilisation

Bed capacity grew 13% against OBD 10%, a **3pp** gap (D5a); OBD growth is **76.92%** of capacity growth (D5b). EBITDA per bed rose **3.94%** (D5c), **11.91 points below** revenue growth (D5d). Net debt rose **₹476 Cr, 24.95%** (D5e, D5f) — **1.20×** the quarter's free cash flow (D5g).

### D6 — Apollo comparator

Apollo consolidated PAT growth **34.18%** (D6a); healthcare-services revenue **+21.53%**, EBITDA **+20.06%**, margin **24.17%**, PAT **+25.00%** (D6b–D6e). **Max's PAT growth is 10.18% of Apollo's** (D6f). Apollo consolidated revenue is **2.36×** Max network revenue (D6g). Max's computed EBITDA margin is **0.56pp below** Apollo's healthcare-services margin (D6j) — so the profit divergence is entirely below EBITDA. Max's occupancy exceeds Apollo's by **5pp** (D6i), the number that cuts against this case study's argument.

### D7 — Stress rule

Unilaterally-priced share of hospital revenue: **9.00%** (D7a); negotiated share **91.00%** (D7b). The disclosed automatic insurance revision of **6%** sits **1 to 2 points below** medical inflation (D7d, D7e). Annualised bases: network **₹11,928 Cr**, hospital **₹10,977.78 Cr**, international **₹988 Cr** (D7f–D7h).

### D8 — RICE

| Initiative | Base | Stressed |
|---|---|---|
| ARPOB decomposition + reporting (exempt) | 472.15 | **472.15** |
| International patient expansion | 115.27 | 10.37 |
| **Episode Price (PROPOSED)** | **96.06** | **8.64** |
| Occupancy ramp, new capacity (exempt) | 82.38 | 82.38 |

Proposal ranks **3rd at baseline, 4th and last under stress** (D8b, D8c). `verify.py` asserts it is the **weakest stressed initiative at baseline** (D8d) — the only configuration in which the demotion is genuine — and that it finishes last (D8e). The stressed winner beats it by **54.62×** (D8f).

---

## Part 3 — Constructs

Everything in this list is the author's invention. None of it is a Max disclosure, plan or statement.

| Construct | What it is |
|---|---|
| **Episode Price** | The proposed product: a single published all-in price per episode, complications absorbed within a defined window |
| **EPE/1k** | Proposed North Star — episode-priced episodes per 1,000 *eligible admissions*, four conjunctive conditions |
| **CSR-90** | Proposed guardrail — case-severity refusal at the 90th percentile of bundle intensity, by specialty |
| RICE inputs | All reach, impact, confidence and effort values in §47 |
| Stress rule application | The 9% figure is disclosed; using it as a RICE multiplier is the author's construction |
| Phase 0 kill criteria | K1, K2, K3 in §53, including the judgement that K2 is most likely to fire |
| §54 arms and R1 rule | The falsification design and the 10pp threshold |
| Personas | §20 — illustrative, not researched individuals |
| The primary/secondary payer seam | The §16 double Porter's framing |

---

## Part 4 — What would change my mind

1. **Max publishes an ARPOB decomposition showing a materially positive price component.** This is the direct refutation and Max can produce it from data it already holds. If the price effect is, say, 3 of the 5 points, A1 is wrong.
2. **Payer mix disclosure showing the negotiated share fell sharply.** If insured revenue share dropped and self-pay rose, the mix story is confirmed rather than refuted — but if the negotiated share is stable *and* ARPOB rose, price becomes the likelier explanation.
3. **Evidence that the 6% automatic revision applied to the full insured book from 1 April 2026.** That would put roughly 5.5 points of price into the quarter on its own and would largely explain the ARPOB move without any mix effect.
4. **Apollo reinstating ARPOB.** If the largest operator concluded the metric is serviceable after all, the central external support for this case study weakens considerably.
5. **PAT growth converging on revenue growth in H2 FY27.** If the newly commissioned capacity ramps and PAT growth moves toward 15%, the gap documented here is a commissioning artefact rather than a structural one — which Max's own guidance implies and this case study does not dismiss.

---

## Part 5 — What could not be found out

- **Payer mix by revenue.** Not disclosed. This is the single most important missing figure; with it, A1 could be tested directly rather than inferred.
- **Case mix and average length of stay.** Not disclosed at any level, so the acuity and turnover components of ARPOB cannot be separated.
- **The composition of the ₹143.29 Cr gap** between network gross revenue and the revenue base implied by the reported 24.8% margin. Presumed a gross-to-net adjustment; not broken out.
- **Segment-level tariff outcomes** from the FY27 insurance renewals beyond the stated 6% automatic revision — which insurers, which specialties, and whether the 6% is a floor or a cap.
- **Whether the medical-education ROCE above 25%** is a board target or a modelled expectation. Reported as stated, not adopted.
- **Complication and readmission rates by procedure**, which would determine whether Episode Price is priceable at all — the question Phase 0's K2 exists to answer.
- **A 2026 primary statistic for Indian medical inflation.** The 7–8% range used throughout comes from 2025 dispute reporting and is dated wherever cited.
