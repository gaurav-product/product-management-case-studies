# ASSUMPTIONS — Day 66: Star Health and Allied Insurance

Companion to `README.md`. Everything in this case study that is not a directly disclosed figure is set out here: what was assumed, how it was derived, what was constructed, what would change my mind, and what could not be established.

All derived figures are computed and asserted in `verify.py` (81 checks, all passing, exit code 0).

---

## Part 1 — Assumptions

### A1 (load-bearing) — that the retail claims ratio is the variable that matters, and that it has not improved

**The assumption.** Star Health's FY26 underwriting improvement is substantially attributable to the group book and to mix, not to the retail book; and because retail is 95.05% of premium, the flatness of retail ICR is the fact that determines the company's medium-term economics.

**What supports it.** The retail and group ICRs are separately disclosed by Star in its own NSE-filed presentation: retail 69.6% → 69.4% over nine months, group 92.1% → 80.6%. Group premium over the same period fell from ₹1,030 Cr to ₹686 Cr, a 33.40% contraction, derived from total and retail GWP on the same page. Weighting the two segment ratios by their premium shares reproduces the disclosed blended loss ratio to within 0.05pp, which is what licenses the attribution: retail contributed −0.18pp of a −1.58pp move, or 11.55%. An analyst put the same point to management on the Q4 FY26 call, noting retail loss ratios near 68% against roughly 65–66% two years earlier and asking whether something structural now prevents a return.

**The honest rival reading, given equal weight.** Management's position is that this is disciplined underwriting working as intended, and that reducing an unprofitable group book *is* the underwriting improvement — a deliberate portfolio decision rather than an accounting artefact. That reading is legitimate and defensible. Exiting a 92% ICR book is exactly what a disciplined underwriter should do, and criticising a company for doing it is not obviously fair. Further, Q4 FY26 retail loss ratio did improve materially — 294 bps to 64.8% — and the retail improvement across FY26 accelerated quarter by quarter (0.8%, 1%, 3% YoY in Q2, Q3, Q4). It is entirely possible that the nine-month flatness understates a genuine retail improvement that arrived late in the year.

**Why the case study proceeds anyway.** Because the group lever is available exactly once. Group is now 4.95% of premium; there is no second 33% to remove. From FY28 the retail ratio is the only variable of consequence, and it currently sits 3.60pp above where it was in FY24. The case study's claim is not that management made a bad decision; it is that the improvement being celebrated is not repeatable and the underlying problem is not yet addressed.

**Early warning — what kills A1.** Star discloses retail ICR every quarter. If FY27 retail ICR comes in materially below 69%, and particularly if it approaches FY24's 65.8%, A1 is dead and the late-FY26 acceleration was the real signal. Star publishes the number itself, so this is falsifiable within two quarters.

### A2 — that the Ind AS / IGAAP divergence is a measurement effect, not evidence of misstatement

Nothing in this case study alleges impropriety. Both bases are disclosed by the company in the same document, the reconciliation between them is published line by line, and Ind AS adoption was mandated by IRDAI from April 2026 with a transition date of 1 April 2025. Unrealised investment gains flowing through the P&L is the correct treatment under the new standard. The observation is narrower: the two bases give 9M profit changes of +87.21% and −30.85%, a 118.06pp divergence, and readers taking the headline at face value are reading the more flattering of two published answers.

### A3 — that the Niva Bupa comparison is a correlation and is used as one

Niva Bupa settles 2.40pp more claims, grows 1.71× faster, and runs a combined ratio 2.60pp worse. The case study reads this as two companies occupying opposite ends of one trade-off. It does **not** claim that Star's settlement ratio causes its underwriting profit. Niva Bupa is 46.31% of Star's size, has a materially different channel mix (banca 19.5% against Star's 7.0%), and a younger book will show different claims behaviour for reasons unrelated to settlement policy. This is stated in §14 and is the weakest link in the argument.

### A4 — that "new to insurance" means no prior insurer record

The RICE stress rule of 7.00% assumes that Star's disclosed 93% new-to-insurance mix implies those customers have no prior insurance history to enumerate from. Star has not published a definition of the term. If "new to insurance" means new to *Star* rather than new to insurance entirely, the addressable share is larger and the stress rule is too harsh. The harsher alternative (6.00%, from the Q4 mix) was available and the more generous figure was used, but the definitional risk runs the other way and is unresolved.

### A5 — that no undisclosed one-off sits inside the group ICR improvement

The group ICR moved 11.50pp in nine months. Reserve releases, a single large account exit, or a reinsurance change could each account for part of it. Star does not break the group book down further. The mix and rate effects are separated arithmetically, but *within* the group rate effect the case study cannot distinguish repricing from reserve movement.

---

## Part 2 — Derivations

Every figure below is computed in `verify.py`. Disclosed inputs are marked [D]; everything else is derived.

**Segment and attribution**
- Group GWP = total GWP [D] − retail GWP [D]: ₹11,964 − ₹10,934 = **₹1,030 Cr**; ₹13,856 − ₹13,170 = **₹686 Cr**. Change **−33.3981%**.
- Retail share = retail GWP ÷ total GWP: **91.3908%** → **95.0491%**, change **+3.6583pp**.
- Reconstructed blended ICR = (retail share × retail ICR) + (group share × group ICR): **71.5375%** → **69.9542%**. Error against disclosed 70.0% = **0.0458pp**.
- Retail rate effect = 9M FY25 retail weight × Δ retail ICR = **−0.1828pp**.
- Group rate effect = 9M FY25 group weight × Δ group ICR = **−0.9900pp**.
- Mix effect = total change − retail rate − group rate = **−0.4105pp**.
- Retail share of the improvement = **11.5455%**; group rate + mix = **88.4545%**.

**Accounting divergence**
- IGAAP 9M PAT change = 446 ÷ 645 − 1 = **−30.8527%**. Ind AS = 966 ÷ 516 − 1 = **+87.2093%**. Divergence **118.0620pp**.
- IFRS impact swing = 521 − (−130) = **₹651 Cr**.
- Unrealised gain share of IFRS impact = 413 ÷ 521 = **79.2706%**; of the ₹450 Cr Ind AS PAT increase = **91.7778%**.
- DAC share of IFRS impact = 281 ÷ 521 = **53.9347%**.
- Reconciliation residual: components sum to **₹520 Cr** against disclosed ₹521 Cr; 446 + 521 = **₹967 Cr** against disclosed ₹966 Cr. Each residual = **0.1035%** of PAT. See Appendix A-1.
- CoR gap 9M FY26: IGAAP 102.7% − Ind AS 99.8% = **2.90pp**.

**The reversal**
- Q4 MTM loss ÷ 9M unrealised gain = 558 ÷ 413 = **1.3511×**. Net full-year unrealised = **−₹145 Cr**.
- Q4 MTM loss ÷ Q4 underwriting profit = 558 ÷ 186 = **3.0000×**.
- Q4 PAT swing = −42 − 270 = **−₹312 Cr**. Q4 underwriting profit growth = **+200.00%**.

**Full year and Q1 FY27**
- FY26 GWP growth **16.0428%**; Ind AS PAT growth **15.7561%**; normalised PAT growth **45.4762%**; gap **29.7201pp**; normalised premium over Ind AS **₹311 Cr**, a multiple of **1.3414×**.
- Q1 FY27: underwriting profit multiple **6.9375×**; Ind AS PAT growth **25.5708%**; Ind AS premium over normalised **42.4870%**; investment income ÷ underwriting profit **5.8018×**; underwriting share of combined pre-tax contribution **14.7020%**.

**Comparator**
- Niva Bupa GWP growth **27.3563%**, which is **1.7052×** Star's 16.0428%. PAT growth **80.3448%**. Star GWP = **2.1594×** Niva Bupa's.

**Regulatory**
- "Repudiated without reasons" complaint share 3.15% → 6.54% = **+107.6190%**, or **+3.39pp**.
- IRDAI penalty ₹3.39 Cr = **0.3721%** of FY26 Ind AS PAT and **0.0166%** of FY26 GWP.

**RICE**
- Stress = 100% − 93% new-to-insurance = **7.00%**. Alternative on Q4 mix = 6.00%.
- Proposal baseline **24.4286** (3rd of 4); stressed **1.7100** (4th and last). Asserted programmatically as the weakest stressed initiative at baseline.

---

## Part 3 — Constructs

Not Star Health's, and not to be attributed to the company:

- The rate-versus-mix attribution (§30) and its validation method.
- **LCP/1k** (Locked-Contestability Policies per 1,000 policies issued) and its four conjunctive conditions (§31).
- **ERD-90** (Enumerated Rejection Density at the 90th percentile) and its ownership, reporting cut and automatic-review trigger (§31).
- All three personas (§20). Composites, not real customers.
- All RICE inputs, the exempt/stressed split, and the stress rule's construction (§47).
- ***Star Enumerated*** in full — mechanism, trade-off analysis, PRD, wireframes, rollout, kill criteria K1–K3, the R1 gate, and the Arm B falsification design (§50–54).
- The SAM range in §13, derived from Star's own share disclosure and explicitly not a market-research figure.
- The characterisation of the GST exemption's demand effect as partly exogenous to Star's performance.

---

## Part 4 — What would change my mind

| Evidence | Effect |
|---|---|
| FY27 retail ICR materially below 69%, approaching FY24's 65.8% | **A1 dies.** The late-FY26 retail acceleration was the real signal and the case study read a lag as a plateau. |
| Star discloses that the group ICR improvement was repricing rather than reserve release or account exit | Strengthens management's reading; weakens A5 but not A1. |
| Star publishes a definition of "new to insurance" showing it means new to Star | The 7.00% stress rule is too harsh and the RICE demotion is an artefact. |
| A structured repudiation-reason field turns out to exist and be queryable | Phase 0's K3 is dead, the measurement opportunity is easier than assumed, and §32's central claim is wrong. |
| Niva Bupa's FY27 combined ratio falls below 100% while its settlement ratio holds at 94.4% | The trade-off framing in §14 collapses — you can pay more claims *and* underwrite profitably, and Star's position is simply worse. |
| Phase 0 shows non-disclosure dominates repudiation grounds | K2 fires; *Star Enumerated* is the wrong instrument and the work moves to declaration design. |

---

## Part 5 — What could not be found out

- **A registry-verified CIN.** The CIN and IRDAI registration number in §2 come from secondary compilation. No registry extract was pulled in this session. Graded 🟡.
- **FY26 retail health premium.** Two irreconcilable figures, ₹17,743 Cr and ₹19,341 Cr, in same-day materials. Not used anywhere.
- **Q4 FY26 GWP.** Three values: ₹6,529 Cr, ₹6,259 Cr, and ₹6,513 Cr implied from FY26 minus 9M. Not used.
- **Star's own repudiation rate.** IRDAI publishes overall industry repudiation data and the Government confirmed in July 2026 that it holds no data on *reasons*. An insurer-level, reason-coded repudiation rate for Star does not exist in public sources. This absence is the case study's finding, not a gap in the research.
- **Whether repudiation grounds are stored in a structured field.** Not disclosed. §53's Phase 0 exists specifically to answer this cheaply rather than to assume it.
- **Full-year FY26 retail and group ICR.** The segment split was found for FY24, FY25 and 9M FY26 in the Q3 deck. The FY26 full-year segment split was not located, so every segment calculation uses the nine-month basis and says so.
- **The composition of the group book being exited.** No breakdown published.
- **Independent verification of post-breach security remediation.** Star states it strengthened its posture; this is not externally verifiable.
- **Current CFO.** Not independently re-verified against a dated primary source in this session, and therefore not named in §2. Following the Day 60 lesson, a named officer is not asserted without registry or dated-filing confirmation.

---

*Companion to Day 66 of 90 · [← Day 65 — Vodafone Idea](../Day-65-Vodafone-Idea) · Day 67 →*
