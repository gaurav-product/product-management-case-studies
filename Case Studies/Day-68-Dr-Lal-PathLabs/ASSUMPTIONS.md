# ASSUMPTIONS — Day 68, Dr. Lal PathLabs Limited

**Case study:** Day 68 of 90 · Dr. Lal PathLabs Limited (CIN L74899DL1995PLC065388)
**Period examined:** Q1 FY27, quarter ended 30 June 2026, reported 24 July 2026
**Verification:** `verify.py`, 119 checks, all passing
**Written:** 3 September 2026

Part 1 states what is assumed and gives the rival reading equal weight. Part 2 shows the arithmetic. Part 3 lists what the author invented. Part 4 states what would falsify the thesis. Part 5 records what could not be found out.

---

## Part 1 — Assumptions

### A1 (load-bearing) — that rising tests per patient warrants scrutiny rather than celebration

**The assumption.** Dr. Lal's Q1 FY27 growth was driven more by testing intensity and mix than by serving more people, and that composition is a question a product manager should ask about rather than a straightforward efficiency gain.

**What supports it, and it is entirely the company's own arithmetic.** Sample volumes grew 10.70% and patient volumes 8.20% — both disclosed by Dr. Lal. Revenue grew 19.10%. Those three figures multiply exactly: 1.0820 × 1.0231 × 1.0758 = 1.1910, which validates all three against each other. Decomposing logarithmically, **45.10% of growth came from more patients and 54.90% did not.** Management stated no price increase was taken, so the 7.58% rise in revenue per sample can only be test mix. Metropolis reported the same shape in the same quarter — EBITDA growing 5.91 points faster than revenue, also with no price rise — so this is a category pattern, not one company's quirk.

**The rival reading, given equal weight.** More tests per patient is what better medicine looks like. India's disease burden is shifting toward lifestyle and non-communicable conditions, which require broader panels and periodic monitoring rather than single targeted tests; the Executive Chairman said exactly this on the earnings call. A company introducing 13 first-in-India tests and expanding into complex assays would show precisely this signature — rising samples per patient and rising revenue per sample with flat prices — while doing unambiguously good clinical work. Under this reading, the composition of growth is evidence of a maturing market, and the case study's framing is unfair.

**Why the case study proceeds anyway, and where it stops.** It proceeds because the *ambiguity itself* is the finding: the two readings are indistinguishable in every metric Dr. Lal publishes, and one of them is a well-documented harm. It stops short of claiming overtesting is occurring. **This analysis can prove the composition of growth; it cannot prove the composition was wrong.** That distinction is maintained in §5, §14, §30, §47 and §64, and it is precisely why the recommended first action is measurement rather than intervention.

**What would settle it in one quarter.** The yield computation §47 ranks first, from data Dr. Lal already holds. If broad panels return proportionally more actionable findings than narrow ones, A1 is wrong and the intensity growth is justified.

### A2 — that the clinician-ordered / self-ordered seam is real and material

The §16 double Porter's run, and much of the diagnosis, rests on the distinction between tests ordered by a clinician and panels bought directly by consumers. **Dr. Lal does not disclose this split.** The distinction is well established in how diagnostics is sold in India and is implicit in the company's own wellness-platform strategy, but its size here is unmeasured. This is the weakest structural assumption in the case study, it is named as such in §64, and Phase 0's K2 is built specifically to test whether the split can even be recovered from historical data.

### A3 — that the log decomposition is a fair way to apportion growth

Multiplicative growth has no unique additive decomposition. The logarithmic method used in D2 is standard and symmetric, but a simple-share method would give patient growth 8.20 ÷ 19.10 = **42.94%** rather than 45.10%. Both are reported to one decimal in the same range, and no conclusion in the case study turns on the difference. The log method is used because it is order-independent; the alternative figure is stated here so the choice is visible.

### A4 — that Q1 is representative enough to reason from

One quarter is a short window, and Indian diagnostics has seasonality — the June quarter includes the onset of the monsoon and its associated infectious-disease testing. That could inflate both samples and mix independently of any structural shift. This is a genuine limitation. It is partly mitigated by management's own behaviour: beating full-year guidance on all three axes and declining to raise it is consistent with management expecting this composition not to persist.

---

## Part 2 — Derivations

Every figure below is asserted in `verify.py`. Tags map to that file.

### D1 — Where the growth came from

| Measure | Value | Tag |
|---|---|---|
| Revenue growth YoY, computed | **19.10%** | D1a |
| Revenue growth QoQ, computed | **13.52%** | D1b |
| Tests per patient, growth | **+2.31%** | D1c |
| Revenue per sample, growth | **+7.58%** | D1d |
| Revenue per patient, growth | **+10.07%** | D1e |
| Identity: 1.0820 × 1.0231 × 1.0758 | **= 19.10%** | D1f |

D1f is the internal consistency check that makes the rest defensible: the three factors reproduce the reported revenue growth exactly.

### D2 — Decomposition

Logarithmic apportionment of the 19.10%: **more patients 45.10%** (D2a), **more tests per patient 13.07%** (D2b), **richer mix per test 41.83%** (D2c), summing to 100% (D2d). Growth not from serving more people: **54.90%** (D2e), which is **1.22×** the patient contribution (D2f).

### D3 — Guidance

Revenue growth ran **5.10 points** above the guidance midpoint (D3a) and **4.10 points** above the top of the 13–15% band (D3b). EBITDA margin was **290 bps** above the top of the 27–28% band (D3c) and 390 bps above the bottom (D3d). Patient volume was **1.20 points** above the top of the 6–7% band (D3e). Revenue growth was **1.36×** the guidance midpoint (D3f), and the revenue beat was **3.41×** the patient-volume beat in percentage-point terms (D3g).

### D4 — Margins

EBITDA margin is **32.14%** on revenue from operations (D4a) and **30.91%** on total income (D4b) — the reported basis — a gap of **1.24 points** (D4d) caused by **₹31.90 Cr** of non-operating income, **3.85%** of total income (D4j, D4k). Margin expanded **220 bps** (D4e). PAT margin **21.37%** (D4f); EPS growth **27.83%** (D4g). Implied Q1 FY26 PAT **₹133.9987 Cr**, back-derived and load-bearing nowhere (D4h, Appendix A-5). PAT growth exceeded revenue growth by **8.14 points** (D4i).

### D5 — Metropolis comparator

Revenue growth **16.58%** (D5a), EBITDA growth **22.49%** (D5b), computed margin **24.44%** against 24.70% reported (D5c, Appendix A-7), PAT growth **25.72%** (D5d), margin expansion **145 bps** (D5e). Dr. Lal is **1.77×** Metropolis on revenue (D5f) with a **6.21-point** margin advantage (D5g) and **1.52×** the margin expansion (D5j). Both grew EBITDA faster than revenue — Dr. Lal by **9.60 points** (D5h), Metropolis by **5.91** (D5i) — while both disclaimed price increases.

### D6 — Network

Quarterly revenue per laboratory **₹2.56 Cr** (D6a); **24.77** PSCs per lab (D6b); **44.66** PUPs per lab (D6c); **21,662** total collection points (D6d), **69.43** per laboratory (D6e), generating **₹3.68 lakh** each per quarter (D6f).

### D7 — Rural outreach, sized

Seven states of thirty-six is **19.44%** (D7a). 110,000 patients (D7b) is **15,714** per covered state (D7c) and **353** per laboratory (D7d). **The share of total volume cannot be computed** — total patient count is not disclosed (Part 5).

### D8 — Cash and capital

Cash of ₹1,693 Cr is **11.29×** the top of guided FY27 capex (D8a), **12.09×** the bottom (D8b), and **2.12×** one quarter's revenue (D8c). Guided capex is **4.54%** of annualised revenue (D8d). Q1 FY27 revenue growth exceeded FY26's full-year growth by **6.90 points** (D8e). PAT margin is **2.92 points** above the FY26 level (D8g).

### D9 — Stress rule

**19.44%**, the demonstrated state coverage of the rural programme (D9a). Two alternatives were computed and deliberately not used: tests-per-patient growth at **2.31%** would have been far harsher (D9b), and patient share of growth at **45.10%** far more generous (D9c).

### D10 — RICE

| Initiative | Base | Stressed |
|---|---|---|
| Panel yield instrumentation (exempt) | 84.46 | **84.46** |
| Rural outreach expansion | 51.85 | 10.08 |
| **Clinician of Record (PROPOSED)** | **20.61** | **4.01** |
| PSC network densification (exempt) | 11.30 | 11.30 |

Proposal ranks **3rd at baseline, 4th and last under stress** (D10c, D10d). `verify.py` asserts it is the **weakest stressed initiative at baseline** (D10e) — the only configuration in which the demotion is genuine — and that it finishes last (D10f). The stressed winner beats it by **21.08×** (D10g).

---

## Part 3 — Constructs

Everything here is the author's invention. None is a Dr. Lal disclosure, plan or statement.

| Construct | What it is |
|---|---|
| **Clinician of Record** | The proposed product: a named clinician attached to large self-ordered panels, paid a fixed fee per report |
| **AYT/1k** | Proposed North Star — actioned yield tests per 1,000 *tests performed*, four conjunctive conditions |
| **UAR-90** | Proposed guardrail — unactioned abnormal rate at the 90th percentile, by panel and by channel |
| The clinician-ordered / self-ordered seam | The §16 double Porter's framing; not a reported segment (A2) |
| Log decomposition | The apportionment method in D2; standard but a choice (A3) |
| RICE inputs | All reach, impact, confidence and effort values in §47 |
| Stress rule application | 19.44% is disclosed; using it as a RICE multiplier is the author's construction |
| Phase 0 kill criteria | K1, K2, K3 in §53, including the judgement that K2 is most likely to fire |
| §54 arms and R1 rule | The falsification design and the 10 pp threshold |
| Personas | §20 — illustrative, not researched individuals |

---

## Part 4 — What would change my mind

1. **Dr. Lal publishes panel-level yield showing broad panels return proportionally more actionable findings.** This is the direct refutation, it is computable from data the company already holds, and it would mean the intensity growth is clinically earned.
2. **A disclosed channel split showing self-ordered wellness is a small and shrinking share of volume.** The §16 seam and much of the diagnosis would lose their force.
3. **Evidence that the mix shift is driven by the 13 first-in-India tests and complex assays** rather than by panel padding. That would make revenue per sample a technology story, not a composition one.
4. **Tests per patient falling in H2 FY27 while revenue growth holds.** That would show the Q1 gap was seasonal — the monsoon-quarter effect A4 concedes — rather than structural.
5. **Metropolis disclosing a sample-versus-patient split that moves the other way.** The category claim rests on both companies showing the same divergence; a contrary comparator would narrow the finding to Dr. Lal alone.

---

## Part 5 — What could not be found out

- **Total patient count.** Only its growth rate is published. This is the most consequential gap: it makes the rural programme's share of volume, and tests-per-patient in absolute terms, uncomputable.
- **The clinician-ordered versus self-ordered volume split.** The analytical spine of §16 and §36, disclosed nowhere.
- **Abnormality rates, yield or clinical action rates** for any test or panel — the quantities AYT/1k and UAR-90 are designed to measure, and which no Indian diagnostics company appears to publish.
- **The contribution of the Shahbazkers acquisition** to the 19.10%, so organic growth cannot be separated from inorganic.
- **Sovaaka adoption or performance metrics**, so the wellness platform's role in the mix shift cannot be assessed.
- **The composition of the ₹31.90 Cr** of non-operating income beyond the reasonable inference that it is largely treasury income on the ₹1,693 Cr cash balance.
- **Metropolis's sample-versus-patient split**, which would allow the D2 decomposition to be run on the comparator and turn a category inference into a category measurement.
