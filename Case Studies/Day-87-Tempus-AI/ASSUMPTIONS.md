# Day 87 — Tempus AI: Assumptions, Conflicts, and Limitations

Companion to `README.md`. This document states every judgement made in producing the case study that is not itself a primary-source fact, every place the sources disagree or fall silent, and every thing a reader should not conclude from the work.

Five parts:

1. **Assumptions** — judgements made where the evidence did not decide
2. **Source conflicts** — where two sources disagree, and how each was resolved
3. **Absences** — what the record does not contain, stated as findings
4. **Limitations** — what this case study cannot support
5. **Verification record** — what the gate checks, what failed, and what was corrected

---

## Part 1 — Assumptions

### 1.1 Comment counting

**Assumption:** the number of numbered staff comments across the ten letters is **66**.

**Basis:** each letter was read in full and its numbered comments counted by hand.

**The judgement involved.** SEC comment letters number their comments sequentially. They also quote the headings of the documents they are commenting on, and financial-statement note headings are themselves numbered — "9. Stock-Based Compensation, page F-29," "5. Goodwill and Intangibles, page F-23," "10. Convertible Promissory Notes, page F-32." A pattern-matching count cannot distinguish a comment number from a note caption.

The 3 August 2022 letter [B5] is the clearest case. Pattern matching over that document returns comment numbers 1, 2, 3, 4, 5, and 9 — implying up to 9 comments. Reading the letter shows **5** comments; the "9" is the caption of the note that comment 5 addresses. The gate records 5.

**Confidence:** high. The counting rule is stated so a reader can reproduce or dispute it.

**What would change it:** a different treatment of multi-part comments. Several comments in [A] — notably comment 5 and comment 16 — contain bulleted sub-requests that could reasonably be counted separately. Counting sub-bullets would raise the total materially. The convention used throughout is **one numbered item, one comment**.

### 1.2 The 2021 self-authorship figures

**Assumption:** the 2021 draft registration statement disclosed 41 total articles of which 29 were self-authored.

**Basis:** SEC staff comment 7 of [A], which quotes the draft's own page 163.

**The judgement involved.** The draft registration statement itself is **not public** — confidential draft submissions are not filed on EDGAR. The figures are known only because the staff quoted them back to the company in a letter that is public.

This is a sound basis. The staff quotes the registrant's own disclosure, in writing, in a document the registrant received and responded to, and did not dispute. But it should be understood for what it is: **a regulator's quotation of a document no member of the public has seen.**

**Confidence:** high, with the provenance stated above rather than hidden.

### 1.3 "Over 800" treated as a floor

**Assumption:** the FY2025 article count is treated as **at least** 800, never as exactly 800.

**Basis:** [E] says "over 800 peer-reviewed articles."

**Consequences.** Every derived figure using this denominator is stated as a floor or a ratio whose direction is known:

- Articles added since the last numerator disclosure: **674** — a floor.
- Article count multiple 2024→2025: **6.35×** — a floor.
- Article count multiple 2021→2025: **19.51×** — a floor.
- Self-authorship coverage of the current evidence base: **15.75%** — a **ceiling**, since a larger true denominator lowers it.

The direction of each bound is the opposite of what a careless reading would assume for the coverage figure, and it is stated explicitly in the gate.

### 1.4 The counterfactual numerator

**Assumption:** if the 2024 self-authorship rate of 73.81% had held, the FY2025 numerator would be **590.48**.

**This is arithmetic on a hypothetical. It is not a fact about Tempus.** Tempus has never published this figure, has never implied it, and nothing in the case study depends on it.

It appears in §28 for one reason: to make the magnitude of the unknown legible. "The numerator is undisclosed" is a true sentence that conveys nothing about scale. "If the last disclosed rate had held, roughly 590 of the 800 would be the company's own" conveys the scale while remaining explicitly conditional.

The gate records `implied_numerator_is_counterfactual_not_disclosure` as **True** so that the labelling cannot be lost in editing.

### 1.5 Scoring the AI validation answer

**Assumption:** the 21 November 2023 comment contained **6** distinct asks, of which **5** were addressed — **83.33%** coverage.

**The judgement involved.** The comment is a single sentence followed by a list: "please include the data quality and robustness of the relationship predicted by the model over time, the experience of the personnel that developed the model, when the model was developed, and how long the model has been used in a clinical setting." That is four enumerated items, preceded by the two-part stem "how you developed **and** validated."

Splitting the stem into two asks is a judgement. A stricter reading gives 5 asks (4 of 5 addressed, 80.00%); a looser one gives 5 or 6 depending on whether "data quality" and "robustness over time" are separated.

**What does not depend on the judgement:** the one ask that is unambiguously unaddressed. **The experience of the personnel who developed the TO algorithm is not disclosed in [D] or in [E].** That holds under every reading.

### 1.6 Scoring "please consider"

**Assumption:** comment 3 of [B9] — the glossary request — is counted as **not complied with**, giving 2 of 3 AI comments complied with (**66.67%**).

**The judgement involved.** The comment says "please **consider** including definitions." Considering and declining is full compliance with a request phrased that way. Counting it as non-compliance is a judgement about **reader benefit**, not about regulatory conformity.

The README states this explicitly in §33: "That is not evasion; it is the system operating exactly as designed." The scoring is a measure of what reached the reader, not an accusation.

### 1.7 RICE parameters

**Assumption:** the Reach, Impact, Confidence, and Effort values in §55, and the stress multipliers in §56, are the author's estimates.

**They are not derived from Tempus' internal data, because no such data is public.** Reach is an ordinal 1–10 anchored to disclosed counts, and each anchor is stated in the table so a reader can substitute their own. Effort is in person-months and is a judgement about disclosure and measurement work, not engineering work.

**What is robust and what is not.**

The specific scores are soft. The **ordering reversal is not**. P1 leads the base case and ranks last under stress across a wide range of parameter choices, because the reversal is driven by the structure of its binding constraint — a recurring quantified unflattering disclosure carries a legal and audit burden no other proposal carries — rather than by the precise multipliers.

A reader who disagrees with the multipliers should test whether any plausible alternative preserves P1's base lead **and** rescues it under stress. §57 argues that the historical record is itself evidence that it cannot: Tempus stopped publishing the number.

### 1.8 Reading the Personalis projection gap

**Assumption:** the gap between Tempus' and Personalis' revenue projections reflects, at least in part, a genuine difference of opinion about growth.

**The competing explanation, stated fairly.** [H] says Tempus' projections are for Personalis "as a wholly owned subsidiary of Tempus" and warns they "do not reflect, and should not be interpreted to represent or be relied upon as, estimates of the standalone financial performance of Personalis." Integration changes a business — channel conflicts, deprioritised product lines, a different sales motion. Some of the gap is therefore a **different asset**, not a different forecast of the same asset.

**Why the assumption survives anyway.** A **56.07%** markdown by 2030, widening monotonically from **12.22%** in 2026, applied to figures Tempus received in diligence from the company it is buying, is a large effect to attribute wholly to subsidiary-status adjustments — particularly given that the markdown then **reverses**, with Tempus' figure exceeding Personalis' own by **2.08%** in 2039.

A pure integration-drag story predicts a persistent or narrowing discount, not a crossover. A different-growth-shape story predicts exactly what the tables show.

**Confidence:** moderate. The README states the caveat in §38 in the same paragraph as the finding, not in a footnote.

### 1.9 The profitability comparison

**Assumption:** Personalis' own view reaches profitability in **2029E** and Tempus' view of Personalis in **2030E**.

**The measures are not the same.** Personalis' figure is Adj. EBITDA **excluding** stock-based compensation. Tempus' is Adj. EBITDA **including** SBC. An excluding-SBC measure will always cross zero earlier.

**Therefore the one-year difference is not a like-for-like comparison and the README says so**, both in §40 and in the gate (`ebitda_definitions_differ_incl_vs_excl_sbc` = True). What is comparable is direction: the acquirer reaches breakeven later, on a stricter measure, with **8** years of negative unlevered free cash flow.

No claim is made that the gap is exactly one year on a common definition. It cannot be computed, because Personalis' including-SBC row and Tempus' excluding-SBC row are not both published for the overlapping years in a form that permits it.

### 1.10 The disclosure ledger

**Assumption:** five questions, selected by the author, represent what a serious reader would want answered.

**This is the most subjective construct in the case study.** A different analyst would pick different rows. Rows were chosen on two criteria: each must be material to evaluating the business, and each must have a **determinable** disclosure status — the ledger is useless if "disclosed?" is itself a judgement call.

**What is robust:** the conclusion that **every row ever answered was compelled**. That holds for any reasonable substitution of rows, because it is a property of the filing record, not of the selection.

---

## Part 2 — Source Conflicts

### 2.1 Three algorithmic tests, or two?

**The conflict.** Comment 2 of [A]: "Your disclosure on page 9 indicating that you have two algorithmic tests appears inconsistent with your disclosure elsewhere on page 30 indicating that you have three algorithmic tests."

**Resolution.** Not resolvable from public sources — the draft is confidential and the response is not on EDGAR. The conflict is reported in §26 as a fact about the 2021 draft, and no count of algorithmic tests as of 2021 is asserted anywhere in the case study.

**Why it is in the case study at all.** It is the clearest single illustration of what adversarial review catches: a company contradicting itself about the size of its own product line, twenty-one pages apart, in a document its own counsel and auditors had already reviewed.

### 2.2 Product line taxonomy changed

**The conflict.** The 2021 draft describes three product lines — Genomics, Data, Algos. [E] reports two segments — Diagnostics, Data and applications.

**Resolution.** Both are accurate for their own dates. The change is reported as a change (§10), not as an inconsistency, and FY2024 comparatives in [E] are presented on the current basis, so the FY2024→FY2025 comparison in §12 is like-for-like.

**The observation that matters:** Algos have no revenue line in the current structure, so the question comment 4 of [A] asked in 2021 — how much revenue comes from Algos — no longer has a line to point at.

### 2.3 Cost recognition timing

**The conflict.** Comment 27 of [A]: page 110 of the draft said genomics costs were recorded at the time of report delivery; page F-15 said costs were recorded as tests are processed.

**Resolution.** Not resolvable publicly. Reported as an example of the review's depth; no cost-timing claim is made anywhere in the case study.

### 2.4 Purchase obligations

**The conflict.** Comment 14 of [A] notes that total purchase obligations in the contractual-obligations table did not match the amounts on page F-25 of the same draft.

**Resolution.** Not resolvable publicly. Not used.

### 2.5 The crossover year

**The conflict.** An initial reading of the two projection tables in [H] placed the Tempus/Personalis revenue crossover at **2038**. The programmatic search returns **2039**.

**Resolution.** The loop is right. Tempus' 2038E figure of $2,963M is **10.27% below** Personalis' $3,302M; the crossover occurs in 2039, where $3,539M exceeds $3,467M by **2.08%**.

**How it was caught.** `verify.py` locates the crossover with a loop rather than asserting a year, so the discrepancy surfaced on the gate's first run — before any prose existed. Had the gate been written after the README, it would have encoded 2038 and confirmed the error.

### 2.6 Preliminary versus final Personalis projections

**The potential conflict.** [H] describes two sets of Personalis projections: **Preliminary Projections** presented to its board in February 2026, and final **Projections** approved in July 2026. Tempus' own projections were "informed by the revenue information through 2030 included in the Personalis Preliminary Projections." If the preliminary and final revenue lines differed, the §38 comparison would be between mismatched vintages.

**Resolution — this was checked, and it does not.** Footnote (2) to the Personalis projections table states the revenue figures actually provided to Tempus: 2026 **$90M**, 2027 **$143M**, 2028 **$272M**, 2029 **$457M**, 2030 **$758M**. These are **identical** to the first five years of the final Projections revenue row.

Personalis' revenue view did not change between preliminary and final; [H] states the revisions reflected actual H1 2026 performance and cost-assumption adjustments. The unlevered free cash flow line **did** change between vintages — [H] discloses both series — which is why the comparison in §38 is built on revenue and not on cash flow.

The gate asserts `diligence_revenue_matches_final_projection_first_five` directly rather than trusting the reading.

### 2.7 Peer-reviewed article counts across three dates

**The apparent conflict.** 41 articles (2021), 126 (March 2024), over 800 (December 2025).

**Resolution.** Not a conflict — three different as-of dates with a growing count. But the jump from 126 to over 800 in 21 months is large enough to warrant stating what is and is not known.

**What is not known:** whether the counting methodology changed. [D] says "mentioned in 126 peer-reviewed articles published in major journals." [E] says "mentioned in over 800 peer-reviewed articles published in major journals." The phrasing is identical; the definition of "major journals" is given in neither.

**Consequence.** The **6.35×** multiple between the two disclosures is computed and reported, but no inference is drawn from its size. It could reflect genuine growth, a broader definition, or both. The case study's argument does not rest on it — it rests on the numerator's disappearance, which is independent of how the denominator is counted.

### 2.8 A false lead that was discarded

**What was searched.** Whether Tempus' quarterly earnings releases, furnished on Form 8-K under Item 2.02, contain algorithm performance metrics absent from the periodic reports.

**What was found.** The earnings-release exhibits were not used, for the methodological reason in §63: material **furnished** under Item 2.02 is not **filed**, carries different liability treatment, and including it would have blurred the tier distinctions in §6 that the entire case study depends on.

**This is recorded as a limitation, not a finding.** It is possible that an earnings release contains a TO performance metric. The claim made in §31 is precise and is limited to what was examined: **no TO performance metric appears in [D] or [E]**. It is not a claim that no such metric exists anywhere in Tempus' public communications.

---

## Part 3 — Absences

Things the record does not contain. Each is a finding about the filings, not a gap filled by inference.

| # | Absent | Where it would appear | Ever disclosed? |
|---|---|---|---|
| 1 | TO algorithm sensitivity, specificity, or any accuracy metric | [E] Business; [D] | **Never** |
| 2 | Self-authorship numerator for FY2025 | [E] risk factors | Yes — 2021 and 2024 |
| 3 | Experience of personnel who built the TO algorithm | [D], [E] | **Never** — asked in [B9] |
| 4 | Definitions of AI terms | [E] | **Never** — asked in [B9] |
| 5 | Organic vs acquired Diagnostics growth | [E] MD&A | **Never** |
| 6 | Tests delivered per period | [E] MD&A | Requested in [A] comment 11 |
| 7 | Data customer count and concentration | [E] | Requested in [A] comment 22, [B5] comment 2 |
| 8 | Denominator for the 92% oncologist retention rate | — | Requested in [B5] comment 2 |
| 9 | Per-test unit economics | [E] | **Never** |
| 10 | Algo revenue | [E] segment reporting | **No line exists** |
| 11 | GAAP reconciliation of projection non-GAAP measures | [H] | **Exempted by rule** |
| 12 | Company responses to draft registration statement comments | EDGAR | **Not public** |

Items 6, 7, and 8 share a property worth stating plainly: **SEC staff explicitly requested all three between 2021 and 2022, and none appears in the FY2025 annual report.** A comment letter compels a change to the document under review. It does not create a permanent obligation.

Item 11 is the case study's own qualification to its own thesis, and §42 develops it: the same rules that forced fifteen years of forecasts into public view waived the requirement to reconcile them to GAAP.

Item 12 is the most significant limitation on the whole analysis, and Part 4 treats it separately.

---

## Part 4 — Limitations

### 4.1 One side of the correspondence

We can read every question the staff asked. We cannot read a single one of Tempus' answers to the draft-stage comments, because draft registration statement correspondence is not filed publicly.

**What this prevents.** Any claim about Tempus' reasoning, resistance, negotiation, or intent during review. Where the README discusses why something was or was not disclosed, it describes **the constraint structure** (§57) or **the observable outcome** (§28), never a motive.

**The one place this bites hardest** is §34. The correlation between the end of staff review and the disappearance of the self-authorship numerator is documented and exact. The causal claim is **not made**. The README states the correlation in its precise form — "the number was disclosed in both documents prepared under active staff review and absent from the first annual report prepared without it" — and stops there.

### 4.2 No secondary sources

No press release, analyst note, news article, company blog, or social media was used.

**What it cost.** Tempus' earnings releases contain operational metrics the periodic reports omit. Analyst estimates would have provided a third-party comparator for the projections in §38. Trade coverage might have explained the Personalis rationale.

**Why the constraint was kept.** The case study is **about** the relationship between compulsion and evidence. Mixing compelled disclosure with voluntary communication would have destroyed the tier structure in §6 that the entire argument rests on.

**This is a deliberate trade and readers should weigh it.** A reader wanting a complete picture of Tempus should read this alongside the earnings materials, not instead of them.

### 4.3 Projections are not forecasts of the merged company

The fifteen-year projections in [H] are for **Personalis** as a Tempus subsidiary. They say nothing about Tempus' own future revenue, and nothing in this case study should be read as a Tempus forecast.

[H] states they were not prepared with a view toward public disclosure, were not prepared in accordance with GAAP or SEC projection guidelines, and were **not audited, reviewed, examined, or compiled** by either company's auditor. Both auditors — BDO USA, P.C. and PricewaterhouseCoopers LLP — expressly disclaim any assurance on them.

The gate records `projections_were_audited` = **False** and `projections_are_guidance` = **False** as negative controls.

### 4.4 The merger has not closed

As of 2026-09-25 the transaction is pending. The S-4 was filed 31 August 2026; Personalis stockholders had not voted. Everything in §35–§42 describes an **announced** transaction.

Terms could change; the deal could fail. The gate records `merger_has_closed` = **False**.

### 4.5 A single company

Day 87 examines one company's disclosure record in depth. The general claims in §53 and §64 — that obligation compels process rather than performance, that review is episodic, that rules have deliberate edges — are supported by Tempus' record and by contrast with Days 83–86. They are **not** established across a sample of listed companies, and nothing here should be read as a statistical claim about US issuers.

The **59.00×** coverage multiple in §41 is a comparison between **two specific measurements on two specific days** — Tempus' self-authorship coverage of 15.75% and Hippocratic AI's evidence coverage of 0.27%. It is a vivid illustration of a real gap. It is not an estimate of a population parameter, and it should never be cited as one.

### 4.6 Point-in-time

All figures are as at 2026-09-25. Filings after that date are not reflected. The Q2 2026 net income of $5.642M is a single quarter at a **1.48%** margin, against a three-year cumulative loss of **$(1,164.96)M**, and §14 says so in the same breath as it reports the milestone.

---

## Part 5 — Verification Record

### 5.1 The gate

`verify.py` contains **265 checks**, all passing. It was written and passing **before the first sentence of `README.md` existed**.

Coverage by section: identity and registration (11); the self-authorship disclosure (24); the review record (20); the AI validation comment (21); the Personalis projections (48); merger mechanics (15); financials (53); the disclosure ledger (10); RICE and stress test (22); series continuity (16); negative controls (14); counter-examples (11).

Rounding is half-up to two decimals via `Decimal.quantize`, not Python's banker's rounding. Tolerance on floating comparisons is 0.005. Derived values are computed from **unrounded** inputs throughout.

### 5.2 What failed on first run

Six hand-stated expectations failed. **In every case the machine was right and the human was wrong.**

| Check | Stated | Computed | Cause |
|---|---:|---:|---|
| `crossover_year` | 2038 | **2039** | Misread two adjacent table columns |
| `tempus_implied_cagr_2026_2030_pct` | 43.31 | **43.29** | CAGR estimated, not computed |
| `personalis_implied_cagr_2026_2030_pct` | 70.44 | **70.36** | Same |
| `cagr_gap_pp` | 27.13 | **27.07** | Propagated from the two above |
| `fy2024_rnd_pct_of_revenue` | 21.53 | **21.54** | Rounded down at the boundary |
| `day87_over_day86_coverage_multiple` | 58.98 | **59.00** | Rounded-intermediate trap |

A seventh failed on the second run: `q2_net_margin_change_pp`, stated as 15.10, computed as **15.09**. The README was corrected.

### 5.3 The rounded-intermediate trap, again

This series first hit this on Day 82 and it recurred here.

The Day 87 / Day 86 coverage multiple divides two percentages. From **unrounded** inputs — 126/800 and 307,000/115,000,000 — the answer is **59.00**. From the **rounded** pair — 15.75 ÷ 0.27 — it is **58.33**. A single premature rounding moves the result by 0.67, more than one percent of the value.

**Both figures are now asserted in the gate**: `day87_over_day86_coverage_multiple` = 59.00 and `day87_over_day86_multiple_if_rounded_first` = 58.33. Asserting the wrong value deliberately means that if 58.33 ever appears in prose, `crosscheck.py` traces it to a check whose name says it is wrong.

### 5.4 Negative controls

Fourteen checks assert that something is **False**, so that no sentence in the deliverables can quietly imply it:

`sec_verified_tempus_disclosures`, `sec_endorsed_any_tempus_claim`, `sec_reviewed_the_2025_followon`, `projections_were_audited`, `projections_are_guidance`, `projections_reflect_personalis_management_input`, `tempus_projections_were_shared_with_personalis`, `self_authorship_share_known_for_fy2025`, `to_algorithm_accuracy_known`, `personnel_experience_known`, `organic_diagnostics_growth_known`, `merger_has_closed`, `day87_uses_mermaid`, `day87_fabricates_any_figure`.

The first three exist because "it's in their SEC filing" is the single most common way a reader over-reads a public document — and because the SEC itself, in [C], says in writing not to.

### 5.5 The RICE assertion

The requirement that a stress-tested proposal rank **last** is enforced programmatically:

```python
chk_eq("p1_leads_base", base_rank[0], "P1")
chk_eq("p1_ranks_last_under_stress", stress_rank[-1], "P1")
chk_eq("p1_rank_reversal_is_total", base_rank[0] == stress_rank[-1], True)
```

P1 decays **97.69%** under stress, more than any other proposal — itself asserted, via `p1_decays_more_than_every_other_proposal`, rather than observed.

**This is the case study's strongest methodological result.** The stress model was built from each proposal's binding constraint, with no reference to what Tempus actually did. It ranks P1 last. Tempus, in fact, stopped publishing P1's subject matter. The framework reproduced observed behaviour from constraints rather than being fitted to the outcome.

### 5.6 Cross-check

`crosscheck.py` extracts every two- and three-decimal figure from `README.md` and `ASSUMPTIONS.md` and confirms each traces to a value asserted in `verify.py`. Figures quoted directly from a source at source precision — the 0.3356 exchange ratio, the 98.8% and 97.4% assay sensitivities, the 92% retention rate — are allow-listed with their source reference. Derived figures are **never** allow-listed; where the cross-check flagged one, it was added to the gate.

---

*Companion to `README.md`. Day 87 of 90.*
