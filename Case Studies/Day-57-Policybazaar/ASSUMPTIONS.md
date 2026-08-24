# ASSUMPTIONS — Day 57, Policybazaar (PB Fintech Limited)

Companion to `README.md`. Everything in the case study that is not a directly disclosed figure appears here. Nothing in this file is a PB Fintech statement unless quoted as one.

---

## Part 1 — Assumptions

### A1 (load-bearing) — that PB Fintech's *selection* caused the mortality improvement

The case study's thesis rests on reading the fall in savings-product mortality from **14.4 to 1.8 deaths per 10,000 (FY23 → FY26)** as evidence that Policybazaar's risk-selection machinery is doing underwriting-grade work. PB Fintech presents the series alongside its fraud-detection framework, which is a strong hint, but it does not publish the causal decomposition.

**Rival readings, given equal weight:**

- **Mix shift.** If the savings book's age, sum-assured or product composition changed materially over three years — for example toward younger, lower-ticket buyers — mortality per 10,000 would fall without any improvement in selection. PB Fintech does not publish the age or ticket distribution of the savings book, so this cannot be ruled out from public data.
- **Industry-wide tightening.** Indian life insurers collectively tightened early-claim scrutiny and documentation standards over this period. Some, possibly most, of the improvement could be sector-level rather than platform-level.
- **Base-period distortion.** FY23 at 14.4 per 10,000 may itself have been anomalous. A single unusually bad base year makes any subsequent series look like a trend.

**Why the case study proceeds anyway.** The ₹9,618 Cr of PB-*initiated* cancellations is a separate, independently disclosed action attributable to Policybazaar rather than to the market — 3.6% of its own policies, refused by its own framework. Even if the mortality series is partly exogenous, the refusal behaviour is not.

**How A1 dies.** §55's early-warning row: if mortality per 10,000 keeps improving while the PB-initiated cancellation rate *falls*, then selection is not the driver and A1 is dead. Both inputs are already published quarterly.

### A2 — that the 3.2%-of-premium figure can be priced at the blended revenue rate

Derivation D1 multiplies FY26 premium (₹29,934 Cr) by the disclosed 3.2% and then by the blended FY26 revenue-to-premium ratio (22.70%) to estimate ~₹217.4 Cr of revenue foregone. Two weaknesses: the 3.2% relates to **life insurance** cancellations, while 22.70% is a **group blended** rate that includes credit-marketplace revenue not earned on premium at all; and refused applications may have converted to a different product rather than being lost entirely. The figure is therefore an **order-of-magnitude estimate**, labelled as such in §5 and §13, and is not used as an input to any other derivation.

### A3 — that the commission cut has not landed on the direct online book

§39 records that core online revenue per ₹100 of premium **rose 29.0 bps** year-on-year despite five insurers cutting gross commission 18% from 1 October 2025. The case study **does not assume a reason.** Three readings are offered and none selected: different contract structures for aggregators than for agents; successful renegotiation; or product-mix offset. Any claim that Policybazaar is "immune" to the cut would be unsupported.

### A4 — that Q1 FY26 segment figures can be derived from disclosed growth rates

Q1 FY26 segment revenue and premium are not disclosed in absolute terms. They are back-derived from Q1 FY27 absolutes and the disclosed YoY growth percentages, which are themselves rounded. The derived Q1 FY26 revenue total (₹1,349.1 Cr) differs from the reported ₹1,348 Cr by ₹1.1 Cr, and the segment-derived premium total (₹5,924.5 Cr) differs from the group-growth-derived ₹5,937.6 Cr by ₹13.1 Cr (0.22%) — both rounding artefacts. The group-level figure is used for every blended ratio. All bps figures computed from these derivations carry that rounding error and should be read to the nearest ~5 bps, not to the decimal.

### A5 — that PB Health's disclosed capital is comparable to group profit

§38 compares PB Fintech's ₹539.40 Cr commitment to FY26 group PAT of ₹670 Cr (80.51%). This is a **scale comparison, not an accounting one** — the commitment is an investment, not an expense, and does not pass through the P&L that way. It is used to convey magnitude only.

---

## Part 2 — Derivations

Every figure below is reproduced in `verify.py`, which must pass before publication.

| ID | Derivation | Inputs | Result |
|---|---|---|---|
| D1 | Revenue foregone on refused premium | ₹29,934 Cr × 3.2% × 22.70% | ₹957.89 Cr premium; ~₹217.41 Cr revenue = **32.45% of FY26 PAT** |
| D2 | Mortality decline | 1.8 ÷ 14.4 | **−87.5%**, 8.0×, annual factor exactly **0.50** |
| D3 | Contribution per ₹1 of revenue | 504/1,194 vs 45/694 | ₹0.4221 vs ₹0.0648 — **6.51× gap** |
| D4 | Growth attribution | Revenue +₹540 Cr; contribution +₹178 Cr | New Initiatives = **33.32%** of revenue growth, **10.11%** of contribution growth |
| D5 | Other income share of PBT | 93/179; 99/93 | **51.96%** Q1 FY27 vs **106.45%** Q1 FY26; ex-OI PBT **−₹6 Cr → +₹86 Cr** |
| D6 | Revenue per ₹100 premium | Blended, core, new; both years | Blended −15.1 bps; **core +29.0 bps**; **new −137.5 bps** |
| D7 | Partner activation | 1.13 lakh ÷ 500,000 | **22.6%** (the RICE stress rule) |
| D8 | Consumer funnel | 28.1 ÷ 158.9; 71.6 ÷ 28.1 | **17.68%** transacting; **2.548** policies per transacting consumer |
| D9 | PB Health scale | 539.40 ÷ 670; 500 ÷ 6,794 | **80.51%** of FY26 PAT; ARR target = **7.36%** of FY26 revenue |
| D10 | Valuation | ₹74,957 Cr ÷ ₹670 Cr | **P/E 111.88×**; implied 46.27 Cr shares at ₹1,620 |
| D11 | Commission-cut arithmetic | 15% × 0.82; 20.75% × 0.82 | **12.30%** (−270 bps of premium); core equivalent **17.02%** (−373.5 bps) |
| D12 | RICE stressed scores | R × I × C ÷ E × 100, stressed R = R × 0.226 | PB Ledger **90.0 → 20.34**, falling from 3rd to **4th of 4** |

---

## Part 3 — Author-constructed content

Not PB Fintech artefacts. Constructed by the author, with reasoning:

- **Personas (§20).** Three composite personas built from disclosed segment facts (tier 2/3 share, protection growth, claims-assistance volume). No PB Fintech persona research is public. Deliberately reduced from four to three to hold length.
- **The user journey's value-capture column (§22).** The stages are inferable from disclosed product behaviour; the *attribution of who captures value at each stage* is the author's analysis and is the mechanism of the whole thesis.
- **RICE inputs (§47).** Reach, Impact, Confidence and Effort are author estimates. Only the **stress multiplier (0.226)** comes from a PB Fintech disclosure. The relative ordering, not the absolute scores, is what the section argues.
- **PB Ledger (§50), the PRD (§51) and the wireframe (§52).** Entirely the author's proposal. PB Fintech has announced nothing resembling an outcome-linked commission instrument.
- **RAQ/1k and DAR-90 (§31).** Author-designed metrics. Neither is a PB Fintech metric, and no company currently publishes either.
- **Kill criteria K1–K3 (§53) and decision rule R1 (§54).** Author-set thresholds, pre-registered so that a later reader can check whether the proposal would have survived its own test.

---

## Part 4 — What would change my mind

1. **PB Fintech disclosing the age and product mix of the savings book across FY23–FY26.** If mix explains the mortality series, A1 collapses and with it the thesis's causal claim.
2. **Evidence that any large Indian insurer already pays an intermediary on realised loss ratio.** The proposal's novelty is part of its argument; if the instrument already exists and is unused by Policybazaar, the question changes from "why not build it" to "why was it refused."
3. **Core online revenue per ₹100 of premium falling sharply next quarter.** That would confirm the commission cut is reaching the direct book and make the proposal more urgent, not less.
4. **PB Health hitting ₹500 Cr ARR and break-even by March 2027.** If the asset-heavy route works on schedule, the "expensive answer" framing in §38 is weakened considerably.
5. **Disclosure that claims-assistance volume is already contractually compensated.** If Policybazaar is paid for claims support in a way not visible in public disclosure, §22's central claim loses one of its three uncompensated stages.

---

## Part 5 — What could not be found out

- **In-force health policy count.** Without it, the ~70K quarterly health claims figure has no denominator and no claims-frequency read is possible.
- **Month-13 persistency on PB-placed policies**, either absolutely or against insurer own-book — the single most important missing number, and the reason K2 exists as a Phase 0 kill criterion rather than an argued claim.
- **The split of the ₹9,618 Cr averted between term and savings products**, and the reason distribution behind PB-initiated cancellations.
- **Whether the 18% commission cut applies to web-aggregator and broker contracts** on the same terms as agent contracts (Assumption A3).
- **PB Fintech's shareholding percentage in PB Healthcare Services**, and PB Health's post-money valuation — neither disclosed.
- **Reconciliation of the loan-disbursal figures** (₹4,366 Cr vs ₹7,003 Cr against "+33% core online") — logged as Appendix A-2 and left unreconciled.
- **Any credible primary-sourced TAM** for Indian online insurance distribution, which is why §13 is run in restricted form.
