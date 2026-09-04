# ASSUMPTIONS — Day 69, MedPlus Health Services Limited

**Case study:** Day 69 of 90 · MedPlus Health Services Limited (CIN L85110TG2006PLC051845)
**Period examined:** Q1 FY27, quarter ended 30 June 2026, reported 22 July 2026
**Verification:** `verify.py`, 137 checks, all passing
**Written:** 4 September 2026

Part 1 states what is assumed and gives the rival reading equal weight. Part 2 shows the arithmetic. Part 3 lists what the author invented. Part 4 states what would falsify the thesis. Part 5 records what could not be found out.

---

## Part 1 — Assumptions

### A1 (load-bearing) — that the cohort curve may be vintage deterioration and not only maturation

**The assumption.** MedPlus's disclosed shop-level EBITDA by opening cohort — 9.3%, 7.1%, 1.9%, 0.7%, −5.0% — is consistent with newer store vintages being structurally weaker, and not only with young stores being young.

**What supports it.** The steps between cohorts are uneven (−2.20, −5.20, −1.20, −5.70), which is what a mixture of ageing and vintage quality produces rather than ageing alone. Two independent disclosures point the same way: **131 of 146 net additions were franchisees**, a channel management itself names as a cause of the gross margin decline, and **private label pharma grew 2%** against 21.8% for the company, so the newest stores are being added into a period when the margin engine is stalling.

**The rival reading, given equal weight, and it is strong.** This is exactly what healthy maturation looks like. A store carries full rent and staff from day one and builds footfall over years; a company opening 146 stores a quarter will always show a young cohort dragging the average. **MedPlus's own data supports this reading: the FY24 cohort is already at 76.34% of mature margin**, which is a real and substantial climb. Under this reading the FY27 vintage reaches 9.3% in due course, the profit compression is the arithmetic of growth, and management's framing is simply correct.

**Why the case study proceeds anyway, and where it stops.** It proceeds because the two readings have very different consequences and are **indistinguishable in the disclosure as published** — and because a company guiding to 800 net additions is making a large bet on the benign reading. **It stops well short of asserting deterioration.** §5, §14, §36 and §64 all state that a snapshot cannot separate the two, and the recommended first action is the disclosure that would.

**What would settle it in one quarter.** The longitudinal cohort series §47 ranks first. Tracking the *same* cohort across quarters, rather than all cohorts at one moment, separates age from vintage immediately, from data MedPlus already computes.

### A2 — that franchisee stores under-index on private label

The §16 seam and the §50 proposal both rest on franchisees having weaker incentives to dispense own label than company-owned stores, because they earn a retail spread on whatever they sell while MedPlus earns a wholesale margin regardless of mix. **MedPlus does not disclose private label penetration by channel**, so this is an inference from incentive structure, not a measurement. It is supported directionally by management naming higher franchisee contribution as a cause of the gross margin decline, but the size is unknown. Phase 0's K1 is built to kill the proposal outright if the gap does not exist.

### A3 — that the two EBITDA margins differ because of lease treatment

The release carries a 7.1% reported EBITDA margin and a 3.5% operating EBITDA margin, 3.60 points and ₹68.35 Cr apart. The most economical explanation for a pharmacy retailer with 5,476 leased stores is that one figure sits before lease rent and the other after it. **This explanation is inferred, not disclosed.** Both figures are used only on their own bases and the inference is load-bearing nowhere.

### A4 — that Q1 composition is informative about the year

One quarter is a short window, and Indian pharmacy retail has seasonality. The FY27 cohort at −5.0% is by definition a partial-year cohort of very young stores and will improve mechanically. The case study does not treat the −5.0% as a steady state; it treats the **shape across cohorts** as the object of interest, and A1 states why that shape is ambiguous.

---

## Part 2 — Derivations

Every figure below is asserted in `verify.py`. Tags map to that file.

### D1 — Revenue up, profit down

| Measure | Value | Tag |
|---|---|---|
| Revenue growth QoQ | **+0.82%** | D1a |
| Swing between revenue and PAT growth | **43.50 pp** | D1b |
| Implied Q1 FY26 revenue, derived | **₹1,543.19 Cr** | D1c |
| Implied Q1 FY26 PAT, derived | **₹42.36 Cr** | D1d |
| Absolute PAT decline | **₹9.19 Cr** | D1e |
| PAT change QoQ | **−48.16%** | D1f |
| PAT margin | **1.76%** | D1g |
| Q1 PAT as share of FY26 PAT | **15.10%** | D1h |

### D2 — Gross profit

Revenue growth exceeded gross profit growth by **7.80 points** (D2a); gross profit grew at **64.22%** of the revenue rate (D2b). Gross profit was **₹460.50 Cr** (D2c) at a 24.5% margin, against an implied prior-year **26.10%** (D2d) — a **6.13%** relative decline (D2e). Revenue growth exceeded operating EBITDA growth by **32.80 points** (D2f).

### D3 — The channel shift

Franchisee growth was **9.11×** company-owned growth (D3a). Franchisee share of pharmacy revenue rose **2.90 points** (D3b), a **2.16×** increase (D3c). Franchisees were **89.73%** of net adds (D3d) and **66.16%** of the 198 gross openings (D3e, D3g). Closures were **26.26%** of gross openings (D3f). Company-owned net adds were **15** (D3h). Franchisee stores number about **657** (D3i) — 12% of stores producing 5.4% of pharmacy revenue, a ratio of **0.45** (D3j). FY27 guidance is **5.48×** the Q1 delivery (D3k); Q1 delivered **18.25%** of it (D3l).

### D4 — The margin engine

Private label pharma grew at **9.17%** of the company's revenue growth rate (D4a). Branded pharma grew **10×** as fast (D4b); private label non-pharma **15×** as fast (D4c). Private label pharma revenue was **₹201.12 Cr** against branded pharma **₹1,293.16 Cr** (D4e, D4f) — a ratio of **6.43×** (D4g). The spread between the fastest and slowest private label lines was **28 points** (D4h).

### D5 — The cohort curve

Steps: **−2.20, −5.20, −1.20, −5.70** points (D5a–D5d); total spread **14.30 points** (D5e). As a share of mature cohort margin: FY24 **76.34%**, FY25 **20.43%**, FY26 **7.53%** (D5h, D5g, D5f). **Two of five cohorts** sit at or below 1% (D5i); **one is loss-making** (D5j).

### D6 — Costs

Pharmacy salaries grew **8.20 points** faster than revenue (D6a); non-pharmacy overhead **12.20 points** faster (D6b). Per-pharmacy salary growth was **16 points** below total salary growth (D6c, D6d) and **7.80 points below** revenue growth (D6e) — so most of the salary increase is store count, not wage inflation per store. Capex ran at **61.66%** of plan (D6f). Capex put on hold totalled **₹155 Cr** (D6g), **4.58×** the quarter's actual capex (D6h).

### D7 — Two EBITDA bases

The two margins are **3.60 points** apart (D7a), a ratio of **2.03×** (D7b), representing **₹68.35 Cr** (D7d). Reported EBITDA margin fell **140 bps** (D7e). Pharmacy is **90.32%** of group operating EBITDA (D7f); diagnostics is **1.97%** of revenue (D7g).

### D8 — Pricing response

Discount cut **1 point**, a **5.00%** relative reduction (D8a, D8b). Membership fee raised **50.51%** (D8c). The uplift is **0.14%** of annualised revenue (D8d) but **114.22%** of the quarter's PAT decline (D8e — see Appendix A-5, indicative only). The stock closed at **63.96%** of its 52-week high (D8g).

### D9 — Stress rule

**7.53%**, the FY26 cohort's shop-level margin as a share of the mature cohort's (D9a). Alternatives computed and not used: FY25 at **20.43%** (D9b, too generous) and FY27 at **−5.0%** (D9c, unusable).

### D10 — RICE

| Initiative | Base | Stressed |
|---|---|---|
| Longitudinal cohort disclosure (exempt) | 357.12 | **357.12** |
| Private label range expansion | 69.40 | 5.22 |
| **Own-Label Compact (PROPOSED)** | **22.56** | **1.70** |
| Site-quality bar on new openings (exempt) | 21.38 | 21.38 |

Proposal ranks **3rd at baseline, 4th and last under stress** (D10d, D10e). `verify.py` asserts it is the **weakest stressed initiative at baseline** (D10f) and that it finishes last (D10g). The stressed winner beats it by **210.36×** (D10h) — the most decisive demotion in this series to date.

---

## Part 3 — Constructs

Everything here is the author's invention. None is a MedPlus disclosure, plan or statement.

| Construct | What it is |
|---|---|
| **Own-Label Compact** | The proposed instrument: published wholesale tiers indexed to own-label penetration on eligible dispenses |
| **PLP/1k** | Proposed North Star — private label prescriptions per 1,000 *substitutable* prescriptions, four conjunctive conditions, reported by channel |
| **SDR-90** | Proposed guardrail — substitution decline rate at the 90th percentile of penetration, by channel and therapy area |
| The COCO / franchisee seam | The §16 double Porter's framing; not a reported segment (A2) |
| Excluded-molecule list | The §40 safety mechanic; no such list is disclosed |
| RICE inputs | All reach, impact, confidence and effort values in §47 |
| Stress rule application | 7.53% is derived from disclosed cohort data; using it as a RICE multiplier is the author's construction |
| Phase 0 kill criteria | K1, K2, K3 in §53, including the judgement that K2 is most likely to fire |
| §54 arms and R1 rule | The falsification design and the 8 pp threshold |
| Personas | §20 — illustrative, not researched individuals |
| Lease-accounting explanation | The A3 inference for the two EBITDA bases |

---

## Part 4 — What would change my mind

1. **A longitudinal cohort series showing each vintage climbing on schedule.** This is the direct refutation of A1, it is computable from data MedPlus already holds, and it would make the whole case study a false alarm — which is precisely why §47 ranks publishing it first.
2. **Private label penetration disclosed by channel, showing franchisees at or near COCO levels.** A2 dies, the §16 seam collapses, and the §50 proposal is pointless. Phase 0's K1 is built to find this.
3. **Private label pharma growth recovering above revenue growth in H2 FY27.** That would make the 2% a one-quarter supply or portfolio event rather than a structural stall, and management has said it expects margin recovery.
4. **Evidence that the 2% private label pharma growth was a deliberate portfolio decision** — pruning low-margin SKUs, or a regulatory or sourcing constraint — rather than a demand or channel effect.
5. **Franchisee stores maturing faster than company-owned ones.** If franchisee operators run tighter cost bases, the channel shift could raise blended shop-level economics even while diluting gross margin, and the §36 adverse loop would not hold.

---

## Part 5 — What could not be found out

- **Private label penetration by channel.** The single most important missing figure; A2 rests on inference without it.
- **Cohort economics split COCO versus franchisee**, which would show whether the vintage decline is a channel effect.
- **The same cohort tracked across quarters** — the disclosure that would resolve A1, and the subject of the top-ranked initiative.
- **The wholesale margin MedPlus earns on franchisee sales**, so the gross margin dilution from channel mix cannot be sized.
- **Why private label pharma growth fell to 2%.** Neither the results nor the available call coverage explains it.
- **The split of the 52 store closures** between company-owned and franchisee stores.
- **Membership subscriber count and renewal rate**, so the ₹99→₹149 repricing cannot be modelled.
- **The unit of the membership-fee revenue uplift**, reported in a way inconsistent with the subscription base (Appendix A-5).
- **Q1 FY26 revenue and PAT as separately reported figures** — both are back-derived here from disclosed growth rates.
