# Day 88 — Qure.ai: Assumptions, Conflicts, and Limitations

Companion to `README.md`. Every judgement that is not itself a primary-source fact, every place the sources disagree or fall silent, and every thing a reader should not conclude.

Five parts:

1. **Assumptions** — judgements made where the evidence did not decide
2. **Source conflicts** — where two sources disagree, and how each was resolved
3. **Absences** — what the record does not contain, stated as findings
4. **Limitations** — what this case study cannot support
5. **Verification record** — what the gate checks, what failed, what was corrected

---

## Part 1 — Assumptions

### 1.1 Classifying a clearance as reporting diagnostic accuracy

**Assumption:** 5 of the 9 clearances report sensitivity, specificity, or AUC; 4 report none.

**Basis:** every summary was read in full.

**The judgement involved.** "Reports diagnostic accuracy" is defined here as: the summary contains at least one sensitivity, specificity, or area-under-the-curve figure **characterising the device's own performance**. Measurement metrics — RMSE, Dice, absolute error, normalized error — do not count.

Applying that definition:

| Clearance | Code | Metrics reported | Counted as accuracy? |
|---|---|---|:---:|
| K200921 | QAS | sensitivity, specificity, AUC | **Yes** |
| K211222 | QIH | absolute error (ml/mm), Dice | No |
| K212690 | QIH | absolute distance error (mm) | No |
| K230899 | QFM | sensitivity, specificity, AUC | **Yes** |
| K231149 | QIH | RMSE, mean absolute error | No |
| K231805 | MYN | sensitivity, specificity, AUC | **Yes** |
| K240740 | QIH | normalized error % | No |
| K251610 | QAS | sensitivity, specificity, AUC | **Yes** |
| K251934 | MYN | AUROC, sensitivity, specificity | **Yes** |

**Confidence:** high. The definition is stated so a reader can reproduce or dispute it.

**What would change it.** A definition counting *any* quantified performance evidence would score 9 of 9, because all four QIH devices report measurement error. That would be a defensible definition and it would erase the finding in §21 — which is why the definition used is stated rather than assumed. The point of §21 is not that four devices lack evidence; it is that the **type** of evidence tracks the product code exactly.

### 1.2 Excluding one "sensitivity" mention

**Assumption:** K240740 contains **zero** device-performance sensitivity figures.

**Basis:** the single string match in that document reads "Conditions of image quality that diminish chest radiographic **sensitivity**, such as noise or..." — a statement about radiography as a modality, in a limitations section.

**The judgement involved.** A pattern-matching count would score this clearance as containing a sensitivity mention and would put the §21 partition at 8 of 9 rather than 9 of 9. The exclusion is based on reading the sentence.

This is the same class of error as Day 87's comment-letter miscount, where financial-statement note captions matched a comment-number pattern. Both were caught the same way. `verify.py` records `k240740_sensitivity_mentions_about_device_performance` as **0**.

### 1.3 The literature count

**Assumption:** the Qure.ai tuberculosis chest-radiograph literature comprises **17** papers, of which **4** have a Qure.ai-affiliated author.

**Method, stated so it can be repeated.** A PubMed search executed 2026-09-26 for `qXR OR "Qure.ai"` combined with chest-radiograph, artificial-intelligence, and tuberculosis terms returned 17 records. Each record's author affiliation strings were searched for "qure". Four matched.

**What this count is not.**

- It is **not** all Qure.ai literature. A broader query — `"Qure.ai"[Affiliation] OR qXR[Title]` — returned **55** records on the same day. The 17-paper set is the tuberculosis-specific subset, chosen because TB is the indication with enough independent work to make an independence ratio meaningful.
- It is **not** a systematic review. There was no protocol, no second screener, and no formal inclusion criteria beyond the query.
- Affiliation matching is imperfect in both directions. An author who has left Qure.ai and lists a new affiliation is counted as independent. An author listing a Qure.ai affiliation on a study the company did not fund is counted as vendor-authored.

**Confidence:** moderate, and deliberately reported as such. The headline ratio — **23.53%** vendor-authored — should be read as "roughly a quarter," not as a precise measurement.

**What does not depend on it.** The direction. Under any reasonable variation of the query, Qure.ai's TB literature is majority-independent, and Day 87's Tempus figure of **73.81%** self-authored is majority-vendor. The **50.28 percentage point** gap is large enough to survive substantial measurement error in either number.

### 1.4 Comparing the two authorship ratios

**Assumption:** the Day 87 and Day 88 authorship shares are meaningfully comparable.

**The judgement involved, stated against itself.** They are not the same measurement:

| | Tempus AI [Day 87] | Qure.ai [Day 88] |
|---|---|---|
| Scope | All product mentions, all indications | One indication (TB) |
| Source | Company's own risk-factor disclosure | Independent PubMed query |
| Definition | "Tempus-authored" per the company | Affiliation string match |
| Date | As of 2024-03-31 | As of 2026-09-26 |

Four differences, any one of which could move a ratio by several points.

**Why the comparison is still made.** Because the *mechanism* being compared is not the ratio but what produced it. Tempus's figure was disclosed because the SEC required it and then stopped being disclosed. Qure.ai's has never been disclosed by the company at all and had to be constructed from outside. The comparison in §28 is between two evidence bases' composition, and the README states the caveats in the same section rather than burying them here.

**What must not be concluded.** That Qure.ai is "3.14× more independent" than Tempus as a general property. The gate records that ratio; §28 states the caveats; neither supports a claim about the companies' relative integrity.

### 1.5 The specificity spread

**Assumption:** comparing 74.30% [P1], 69.20% [P4], and 32.00% [P5] as three measurements of "the same thing in different settings" is legitimate.

**The judgement involved.** They are not identical measurements:

- **[P1]** is specificity at the operating point where sensitivity is fixed at 90%, in screening centres, on qXR **v3**.
- **[P4]** is a pooled meta-analytic estimate across eight studies, for qXR **v2**.
- **[P5]** is specificity at the manufacturer's default threshold, in a hospital triage cohort, on qXR **v4**.

Different versions, different thresholds, different reference standards, different estimators. A strict methodologist would say these three numbers should not appear in one table.

**Why they do.** Because a procurement officer will read them in one table whether or not a methodologist approves, and because the *direction and magnitude* of the effect survive every caveat. The Lima figure is not 32% because of a threshold choice or a version difference; [P5] reports no AUC difference between v3 and v4, and the authors attribute the result to a population where 81% of patients had opacities on chest X-ray for reasons unrelated to TB.

**What the README claims and does not claim.** It claims specificity is a property of the device **and the population**, and that the FDA record reports only one population. It does **not** claim that qXR's specificity "is" any particular number, and it does not rank the three settings as better or worse measurements.

**The comparator sensitivities** (90.00%, 94.40%, 90.80%) carry the same caveats and are used only to establish that sensitivity moves less than specificity — a **4.40 pp** range against **42.30 pp**. That contrast is robust to every objection above, because all three sensitivities come from the same three studies as the specificities.

### 1.6 Counting internal inconsistencies

**Assumption:** 4 of 9 summaries contain an internal numeric contradiction.

**The definition used:** the same statistic, for the same device and measurement, stated twice in one document with two different values.

**What was excluded under that definition:**

- The K230899 predicate comparison table listing findings in **opposite order** in its two columns (predicate: pleural effusion then pneumothorax; subject: pneumothorax then pleural effusion). This makes a horizontal read misleading, but no number contradicts another number. Reported in §58 as a readability observation, **not** counted.
- The training geography summing to 99.97% rather than 100%. This is an arithmetic shortfall, not two values for one statistic. Reported in §23, **not** counted.
- Differences arising purely from decimal representation (0.9829 rendered as 98.29 against a stated 98.28) where the underlying value is the same to the stated precision. The K230899 lower bound is noted in §33 but the clearance is counted on its **upper** bound discrepancy, which is a genuine difference.

**Confidence:** high for all four. Each was confirmed by reading the raw page layout, not from a text-extraction artefact.

### 1.7 Reading the K251934 sentence as an error

**Assumption:** "The overall AUC for aided reads was 0.8466 ... whereas the aided reads showed AUC of 0.8720" contains a word error, and 0.8466 is the unaided value.

**Basis:** Table 5 of the same document labels 0.8466 as unaided AUROC and 0.8720 as aided. The immediately preceding sentence states there was "significant improvement in the aided reads, as compared to the unaided reads."

**Confidence:** very high. Two independent parts of the same document resolve it, and the alternative reading — that the same condition genuinely produced two different AUCs — is not coherent.

**What is not claimed.** That anyone was misled, or that the error affected the clearance. `verify.py` records `the_four_inconsistencies_change_any_clearance_decision` as **False**.

### 1.8 RICE parameters

**Assumption:** the Reach, Impact, Confidence, and Effort values in §47 and the stress multipliers in §48 are the author's estimates.

**They are not derived from Qure.ai's internal data**, because none is public. Reach is ordinal 1–10 with each anchor stated in the table so a reader can substitute their own. Effort is in person-months and estimates disclosure and regulatory work, not engineering.

**What is soft and what is not.** The individual scores are soft. **The ordering reversal is not.** P1 leads the base case and ranks last under stress across a wide range of parameter choices, because the reversal is driven by the structure of its binding constraint — publishing a range in a market where competitors publish point estimates — rather than by the precise multipliers.

**The honest weakness, stated plainly.** Day 87's equivalent reversal could be checked against history: Tempus had in fact stopped publishing the number, so the model reproduced an observed behaviour. Day 88's cannot. **No vendor in this market publishes a stratified specificity table**, which is consistent with §49's argument but does not prove it — the same observation would follow if nobody had thought of it. §57's question 7 states this as an open question rather than resolving it, and it would be falsified the moment one vendor published a range and won business with it.

### 1.9 The evidence ledger

**Assumption:** five questions, selected by the author, represent what a buyer would want answered.

**This is the most subjective construct in the case study**, as it was on Day 87. Rows were chosen on two criteria: material to a purchase decision, and having a **determinable** disclosure status.

**What is robust:** that **zero** rows were volunteered by the company. That holds under any reasonable substitution, because it is a property of the source record — every source used here is a regulator's document, a registry entry, or someone else's research.

### 1.10 Attribution of the geography inversion

**Assumption:** describing the training/test geography as "inverted" is a characterisation, not a criticism.

FDA requires evidence relevant to the US population; testing a US clearance on US data is correct practice. The summary discloses its training composition openly, which is not universal.

**What §23 claims** is narrower than it may read: that the cleared figure describes a mostly-India-trained model's performance on American patients, and is silent on its performance in the population most of its training data came from. That is a statement about what the document covers, not about whether the submission was appropriate.

---

## Part 2 — Source Conflicts

### 2.1 K230899 — pneumothorax AUC upper confidence bound

**The conflict.** The predicate comparison table gives `AUC: 0.9894 (95% CI: [0.9829, 0.9980])`. The results table and narrative give `98.94 (98.28 - 99.82)`.

**Upper bound: 99.80 versus 99.82.** Lower bound: 98.29 versus 98.28.

**Resolution.** Not resolvable from the document. The results table is the more detailed presentation and carries the TP/P and TN/N counts, so it is treated as primary for every figure used in the README. The **0.02** discrepancy is reported and used nowhere else.

### 2.2 K231149 — RMSE confidence intervals

**The conflict.** Narrative and Table 2 give identical point estimates and different intervals.

| Measurement | Point | Narrative | Table 2 |
|---|---:|---|---|
| Cardiac diameter | 7.55 mm | 6.95 – 8.34 | 6.96 – 8.38 |
| Thoracic diameter | 5.43 mm | 4.95 – 6.11 | 4.94 – 6.09 |

The intervals move in **opposite directions** between the two presentations — the table's cardiac interval is wider, its thoracic interval narrower.

**Resolution.** Not resolvable. Table 2 is treated as primary, consistent with 2.1. The point estimates, which agree, are the only values used in the improvement calculations in §34.

### 2.3 K240740 — a degenerate confidence interval

**The conflict.** The predicate comparison table states `Median Absolute Normalized Average Diameter Error [95% CI]: 11.1 (9.1-11.1)`. The results table states 11.1 with an interval of 9.52 – 12.50.

**Resolution.** The comparison table is wrong, and demonstrably so: a two-sided 95% confidence interval cannot have its upper bound equal to its point estimate. The results table is used.

The volume figure conflicts too — 20.7 (17.6 – 22.6) in the comparison table against 20.7 (17.29 – 22.41) in the results table.

**This is the most consequential of the four**, because the comparison table's interval is both impossible and **narrower** than the real one. A reader trusting it would overstate the device's measurement precision.

### 2.4 K251934 — "aided" reported twice

Covered in 1.7. Table 5 resolves it; the narrative sentence is treated as containing a word error.

### 2.5 qXR version mismatch across sources

**The conflict.** The FDA-cleared devices and the versions evaluated in the TB literature are not the same artefacts.

| Source | Version |
|---|---|
| [P4] meta-analysis | qXR **v2** |
| [P1] Lancet Digital Health 2021 | qXR **v3** |
| [P5] PLOS GPH 2024 | qXR **v4** (and v3) |
| [F1]–[F9] FDA clearances | Not version-numbered except K251610 (v1.0) |

**Resolution.** No numeric comparison is made between an FDA-cleared performance figure and a TB literature figure anywhere in this case study. The two records are compared **structurally** — one reports a single population, the other reports many — never numerically. `verify.py` records `qxr_version_in_fda_clearances_same_as_in_tb_studies` as **False**.

This is the single most important guard in the document. Conflating a cleared pneumothorax specificity of 96.36% with a TB specificity of 32.00% would be a category error, and §31's table contains only TB figures for exactly that reason.

### 2.6 qXR's rank differs between two independent studies

**The conflict.** [P1] ranks qXR **first** of five on AUC. [P3] places it in the 0.8–0.9 band, behind Lunit and Nexus.

**Resolution.** Not a conflict — two different populations, cohorts, and competitor sets, three years apart. Reported in §29 and §40 as evidence that **rank is not stable across settings**, which is the finding rather than a problem with either study.

### 2.7 Two transient fetch failures

**What happened.** K212690 initially returned an HTML error page (5,213 bytes) and K231149 returned HTTP 401. Both succeeded on retry against the correct year directory — `pdf21/` and `pdf23/` respectively.

**Why it is recorded.** A silent acceptance of those failures would have produced a case study asserting **seven** clearances instead of nine, and the §21 partition would have been wrong in both numerator and denominator. The openFDA API result (9 records) was the independent check that caught it.

### 2.8 A false lead that was discarded

**What was searched.** CE marking and CDSCO (India) regulatory status, to test whether a second and third regulator compelled different evidence than FDA.

**What was found.** Nothing retrievable through the primary-source routes used in this series. The EU's EUDAMED database and India's CDSCO portal were not accessed.

**Resolution.** CE and CDSCO status are **absent from the README entirely** rather than asserted from secondary sources. This is a real gap: a comparison across three regulators would have strengthened §21 considerably, and its absence is recorded here rather than papered over.

---

## Part 3 — Absences

| # | Absent | Where it would appear | Compelled by anything? |
|---|---|---|---|
| 1 | Revenue, funding, headcount, pricing | A financial filing | **No** |
| 2 | TB performance in a cleared device | An FDA 510(k) | **No** — never submitted |
| 3 | Specificity by setting type | Any vendor document | **No** |
| 4 | Recommended thresholds by population | Any vendor document | **No** — [P5] asked |
| 5 | Version-to-version performance changelog | Any vendor document | **No** |
| 6 | Performance in an Indian screening population | Anywhere | **No** |
| 7 | Vendor confirmation of HIV / prior-TB degradation | Any vendor document | **No** — [P3] found it |
| 8 | Whether the 37 unknown-sex scans differ clinically | K230899 | **No** |
| 9 | Deployment scale | Anywhere in the sources used | **No** |
| 10 | CE / CDSCO status | Not searched (see 2.8) | — |

Items 3, 4, 5, and 7 share a property: **each is a question that published independent research has already raised**, and none has a vendor-side answer. That is not a disclosure failure in the regulatory sense — nothing requires any of them — but it is the gap between what the evidence base asks and what the company addresses.

Item 1 is the mirror of Day 87. Tempus disclosed $1,271.789M of audited revenue and zero algorithm metrics. Qure.ai discloses five clearances of algorithm metrics and zero revenue. **The complement is close to exact, and neither company chose it.**

---

## Part 4 — Limitations

### 4.1 One company

Day 88 examines one manufacturer's regulatory record in depth. The general claims in §54 — that classification determines disclosure, that regulated is not checked, that a performance number without a population is not a performance number — are supported by this record and by contrast with Days 82–87. They are **not** established across a sample of device manufacturers, and nothing here is a statistical claim about 510(k) submissions generally.

In particular, **44.44% of summaries containing an internal contradiction is a fact about these nine documents.** It is not an estimate of an error rate in the 510(k) corpus, and it must not be cited as one.

### 4.2 No secondary sources

No company website, press release, funding announcement, conference abstract, or news article was used.

**What it cost.** Deployment scale, funding history, partnership announcements, and customer names are all publicly reported somewhere. None is here. A reader wanting a complete commercial picture of Qure.ai should read this alongside those sources, not instead of them.

**Why the constraint was kept.** The case study is about what compulsion produces. Mixing compelled disclosure with voluntary communication would have destroyed the tier structure in §6 on which the entire argument rests.

### 4.3 FDA clearance is not approval, and this document is not a safety assessment

Every clearance here is a Traditional 510(k) — a substantial-equivalence determination against a predicate. None is a PMA. None establishes clinical benefit.

Nothing in this case study should be read as an assessment of whether any Qure.ai device is safe, effective, or suitable for any clinical use. It is an assessment of **what the public record contains**.

`verify.py` records `510k_is_an_approval`, `510k_proves_clinical_benefit`, and `fda_endorsed_any_qure_marketing_claim` as **False**.

### 4.4 The four inconsistencies are minor

They are typesetting and transcription defects. Each is recoverable from elsewhere in the same document. None would change a clearance decision, and none is evidence that a device fails to perform as cleared.

They are used in §37 as evidence about a **process** — that the arithmetic in these documents is not independently recomputed between drafting and publication — and for nothing else.

### 4.5 Financials are absent, not searched-for-and-missing

Qure.ai's statutory filings with India's Registrar of Companies exist. They are not freely retrievable through the routes used in this series. §11's "not disclosed" rows mean **not obtainable by the method used here**, which is a weaker statement than "not public."

### 4.6 The independent literature is a sample, not a census

Five studies are discussed in depth. Thirteen independent TB papers exist in the queried set, and 55 records matched a broader Qure.ai query. The five were chosen for study design and independence, not at random, and they skew toward the largest and most rigorous — which is appropriate for the argument being made and does mean the literature as a whole is not characterised.

### 4.7 Point-in-time

All figures as at **2026-09-26**. Clearances after that date are not reflected; the FDA record is live and K-numbers are added continuously.

---

## Part 5 — Verification Record

### 5.1 The gate

`verify.py` contains **344 checks**, all passing. It was written and passing **before the first sentence of `README.md` existed**.

Coverage by section: identity and statutory registration (18); the FDA clearance record (19); the partition (12); K230899 (54); internal inconsistencies (46); remaining accuracy disclosures (23); the uncleared indication (5); the independent literature (77); the specificity spread (14); the evidence ledger (13); RICE and stress test (28); series continuity (18); negative controls (12); counter-examples (5).

Rounding is half-up to two or three decimals via `Decimal.quantize`, not Python's banker's rounding. Tolerance on floating comparisons is 0.005, tightened to 0.0005 where a three-decimal source figure is asserted. Derived values are computed from **unrounded** inputs throughout.

### 5.2 What failed on first run

Two hand-stated expectations failed. **In both cases the machine was right.**

| Check | Stated | Computed | Cause |
|---|---:|---:|---|
| `rice_stress_spread` | 8.08 | **8.09** | Spread taken from rounded scores |
| `day88_over_day86_ratio` | 286.44 | **286.45** | Ratio of two unrounded percentages |

Both are the rounded-intermediate trap this series first hit on Day 82 and has now hit on Day 86, Day 87, and Day 88.

### 5.3 The rounding trap, quantified

The Day 88 / Day 86 ratio is the clearest illustration this series has produced.

- From **unrounded** inputs — 13/17 and 307,000/115,000,000 — the answer is **286.45**.
- From the **rounded** pair — 76.47 ÷ 0.27 — it is **283.22**.

**An error of 3.23**, from a single premature rounding, on a figure quoted in the README's closing argument.

Both values are asserted in the gate: `day88_over_day86_ratio` = 286.45 and `day88_over_day86_ratio_if_rounded_first` = 283.22. The same pattern is applied to the RICE spread, where `rice_stress_spread` = 8.09 and `rice_stress_spread_if_rounded_first` = 8.08.

Asserting the **wrong** value deliberately is what makes `crosscheck.py` useful here: if 283.22 or 8.08 ever appears in prose as a result, the cross-check traces it to a check whose name says it is wrong.

### 5.4 Reconciliation checks

Beyond the derived figures, the gate asserts that the published counts inside K230899 **reconcile**:

- Pneumothorax: 201 + 412 = 613 cases and controls; 289 + 287 + 37 = 613 by sex; 179 + 152 + 125 + 12 + 145 = 613 by region.
- Pleural effusion: 344 + 726 = 1,070; 498 + 551 + 21 = 1,070; 278 + 213 + 6 + 308 + 265 = 1,070.
- Reported sensitivity 94.53% recomputed from 190/201; specificity 96.36% from 397/412.

All six reconcile exactly. This is reported in §22 as a **positive** finding about that submission, and it is the reason the training-geography shortfall of **0.03 pp** in the same document is reported as a minor defect rather than a pattern.

Similarly, [P5]'s counts reconcile: 65 cases + 322 controls = 387, the stated triage cohort, with sensitivity 59/65 = **0.908** and specificity 103/322 = **0.320** against reported values of 0.91 and 0.32.

### 5.5 Negative controls

Twelve checks assert that something is **False**, so no sentence can quietly imply it:

`fda_verified_the_summaries_are_internally_consistent`, `fda_endorsed_any_qure_marketing_claim`, `510k_is_an_approval`, `510k_proves_clinical_benefit`, `tb_performance_is_fda_cleared`, `cleared_specificity_generalises_to_other_populations`, `company_financials_known`, `qure_revenue_known`, `qxr_version_in_fda_clearances_same_as_in_tb_studies`, `the_four_inconsistencies_change_any_clearance_decision`, `day88_uses_mermaid`, `day88_fabricates_any_figure`.

The first four exist because "FDA cleared" is the single most over-read phrase in medical device marketing. The ninth exists because conflating a cleared figure with a TB figure would be this case study's easiest and most damaging error.

### 5.6 The RICE assertion

The requirement that the base-case leader rank **last** under stress is enforced programmatically:

```python
chk_eq("p1_leads_base", base_rank[0], "P1")
chk_eq("p1_ranks_last_under_stress", stress_rank[-1], "P1")
chk_eq("p1_rank_reversal_is_total", base_rank[0] == stress_rank[-1], True)
```

P1 decays **98.00%**, more than any other proposal, which is itself asserted via `p1_decays_more_than_every_other_proposal` rather than observed. The gate also records that exactly **3** proposals gain a place and exactly **1** loses ground, and that the one losing ground is P1.

Unlike Day 87, this result **cannot** be checked against the company's observed behaviour, because no vendor in this market publishes a stratified specificity table. §1.8 above states that limitation and §57's question 7 leaves it open.

### 5.7 Cross-check

`crosscheck.py` extracts every two- and three-decimal figure from `README.md` and `ASSUMPTIONS.md` and confirms each traces to a value asserted in `verify.py`. Figures quoted at source precision — the 0.959 LVO AUC, the 0.944 pooled sensitivity, the 0.8466 unaided AUROC — are allow-listed **with their source reference**. Derived figures are never allow-listed; where the cross-check flagged one, it was added to the gate.

---

*Companion to `README.md`. Day 88 of 90.*
