# Day 90 — Health in ChatGPT: Assumptions, Conflicts, and Limitations

Companion to `README.md`, and the last of ninety. Every judgement that is not itself a primary-source fact, every place the sources fall silent, and every thing a reader should not conclude.

Five parts:

1. **Assumptions** — judgements made where the evidence did not decide
2. **Source conflicts** — where sources disagree or could mislead, and how each was resolved
3. **Absences** — what the record does not contain, stated as findings
4. **Limitations** — what this case study cannot support
5. **Verification record** — what the gate checks, and what it asserts is false

---

## Part 1 — Assumptions

### 1.1 The regulatory null, and why it needed controls

**Assumption:** the vendor of the most widely used health-answering system has no FDA device authorisation of any kind, and no SEC registration.

**Basis:** four openFDA endpoints — `510k`, `pma`, `classification`, `registrationlisting` — each returning zero records, plus an EDGAR company search returning zero registrants.

**The judgement involved, and it is the methodological point of the day.** A query returning nothing has two possible causes: nothing exists, or the query is wrong. Until today this series treated the first as the default, and that was never justified.

Two positive controls were therefore run against the same endpoint with the same syntax:

| Control | Records | Why chosen |
|---|---:|---|
| `applicant:"qure.ai"` | **9** | Day 88's subject; reproduces yesterday's count exactly |
| `applicant:Verily` | **4** | A second, unrelated company |

Both non-zero. The endpoint responds, the applicant field is populated, and the query form is correct. **The zeros are therefore measurements.** `verify.py` asserts `method_validated_before_asserting_a_null` and `zero_is_a_measurement_not_a_failed_query`.

**What would still change it.** An authorisation held under a corporate name not matched by the queries, or a device authorised to a partner rather than the model vendor. The README's claim is scoped to the names and endpoints queried, and [L1] corroborates the substance independently in a peer-reviewed journal.

**A near-miss worth recording.** A search for `applicant:Google` also returned nothing, while `applicant:Verily` returned four. Rather than conclude anything about that company, it was dropped: an unexplained null in a control is a reason to distrust that control, not a finding. Only the two controls that behaved as expected are used.

### 1.2 The literature counts

**Assumption:** the PubMed searches executed on 2026-09-28 returned 21,033 papers, 220 tagged as randomised controlled trials, and 422 systematic reviews.

**The queries, stated so they can be repeated.** The base query combined `("large language model" OR ChatGPT)` with `(medical OR health OR clinical)`. The RCT and systematic-review cuts added `randomized controlled trial[Publication Type]` and `systematic review[Publication Type]` to that same base.

**The critical property, and the reason the ratio is usable.** The numerator and denominator share an identical base query. Whatever the base over-captures, it over-captures in both — so the **proportion** is far more robust than either absolute count.

**What the counts are not.** PubMed expands terms aggressively. `(medical OR health OR clinical)` becomes dozens of variants including "clinic", "medication", "medically" and "medics". The 21,033 is therefore a generous denominator, and §1.3 shows the numerator is generous too.

**Confidence:** high for the counts as returned on that date; moderate for their interpretation, which §1.3 addresses directly.

### 1.3 The sample of ten

**Assumption:** reading ten of the 220 RCT-tagged records establishes that false positives are common and that 220 is a ceiling.

**Method.** Ten records were taken from the most recent results of the RCT-filtered query and read in full — title, abstract, publication types and MeSH terms. Each was classified on two axes: does it concern a language model at all, and does it measure a patient health outcome.

**Result.** Five of ten concerned no language model whatsoever — a neonatal hand-hygiene trial in Uganda, an obesity drug trial, a physiotherapy trial, an anaesthesia trial, and a hypertension drug trial. Of the five that did, none measured a patient health outcome; four measured education and one measured trust.

**What this sample can and cannot support.**

| Claim | Supported? |
|---|---|
| False positives are present and common | **Yes** |
| 220 is a ceiling, not a count | **Yes** |
| No sampled trial measured a health outcome | **Yes — a direct count** |
| The false-positive rate is exactly 50% | **No** |
| The true count is exactly 110 | **No** |

The README says "roughly half" and "adjusted estimate" wherever it generalises, and reserves exact language for the direct count of what was read. `verify.py` asserts `the_sample_is_statistically_representative` as **False** and `the_220_rcts_were_all_read` as **False**.

**The sample is not random.** It is the ten most recent, which may skew toward newer indexing behaviour. A random sample across the full set would be better and was not done.

**Why ten was enough for the claim actually made.** The claim is not an estimate of a rate; it is that the headline number cannot be used as published. One false positive would have established that. Five establishes it beyond argument.

### 1.4 "Measures a patient health outcome"

**Assumption:** none of the ten sampled studies measured a patient health outcome.

**The definition used:** a change in a person's health status, care received, or clinical decision quality, measured in people who were the subject of care. Examination scores, knowledge tests, behavioural intention, self-efficacy, engagement, and trust are excluded.

**Why the definition is strict.** Because the whole point of §25's proxy ladder is that these substitutions are made easily and read past quickly. A loose definition would classify [L4]'s behavioural-intention outcome as a health outcome, which would defeat the purpose of counting.

**Where it is arguable.** [L2] measures trust calibration in health-information consumers, which is closer to a user outcome than anything else in the sample, and a reasonable person could classify it differently. The README treats it as the closest case and says so in §24.

### 1.5 Treating the growth curve as context, not evidence

**Assumption:** the year counts (1,877 / 4,219 / 7,603) describe a field growing quickly and nothing more.

**What is not claimed.** That growth indicates quality, maturity, or consensus. Volume and evidential strength are independent, and the README's §21 exists specifically to separate them.

**A caveat on 2026.** The current year is partial and is not reported as a year figure. The 7,334 papers outside the 2023–2025 window include both the partial current year and anything indexed earlier, and the README reports that residual without decomposing it.

### 1.6 Excluding vendor benchmarks

**Assumption:** excluding vendor-published benchmark results produces a fairer evidence picture than including them.

**The reasoning.** §18 sets it out: in this category the party that builds the model frequently also builds the evaluation, runs it, and publishes the score. Day 87 established the principle — a number is worth what the independence of its producer is worth — and Day 88 quantified the contrast, with **76.47%** of one product's literature having no vendor author.

**The cost, stated plainly.** It makes the evidence base look thinner than a vendor presentation would. A reader wanting the complete picture should read those benchmarks alongside this document, not instead of it.

**What it is not.** It is not a claim that vendor benchmarks are false. `verify.py` asserts only `any_vendor_benchmark_score_is_asserted_here` as **False** — a statement about this document, not about those benchmarks.

### 1.7 RICE parameters

**Assumption:** the Reach, Impact, Confidence and Effort values in §40 and the stress multipliers in §41 are the author's estimates.

Reach is ordinal 1–10 with each anchor stated so a reader can substitute their own. Effort is in person-months and estimates evidence-generation and disclosure work, not engineering.

**What is soft and what is not.** The scores are soft. **The reversal is not**, and Day 90's is the most robust of the four, because its binding constraint is not a matter of degree. Days 87–89 modelled costs that could in principle be absorbed — legal review, competitive disadvantage, an absent benchmark. Day 90's constraint is categorical: publishing an outcome study is evidence of intended use, and intended use is what brings a product into device scope. No choice of multiplier changes that structure.

**The honest weakness, consistent with Days 88 and 89.** This is reasoned from constraint structure, not measured. It is consistent with the observed pattern — capability metrics published, effectiveness trials not — but consistency is not proof, and §47's question 6 leaves it open.

### 1.8 The four-regulator table

**Assumption:** the four regimes in §28 fairly represent what this series examined.

**What the table claims.** That three of the four compel something real, that two produce output reaching a member of the public, and that none compels a measurement of whether anyone is better off.

**What it does not claim.** That these four are the only regimes that matter, that they are representative of regulation generally, or that any of them is badly designed. §57 says the opposite: each did its job.

---

## Part 2 — Source Conflicts

### 2.1 Pattern matching versus reading — the central conflict

**The conflict.** PubMed's publication-type tag says 220 records are randomised controlled trials. Reading ten of them says roughly half are not about the subject at all.

**Resolution.** The tag is correct and the inference from it is wrong. Every one of the five false positives genuinely *is* a randomised controlled trial — of hand rub, of an obesity compound, of shockwave therapy, of opioid titration, of an antihypertensive. The tag was never claiming they involve language models. The base query was.

**Why this matters beyond this case study.** It means any count built on that query — including, potentially, some of the **422** systematic reviews — inherits the same inflation. §47's question 7 raises it, and it is the most consequential unanswered question in this document.

### 2.2 FDA's silence about LLMs in cleared devices

**The apparent conflict.** FDA maintains a public list of AI-enabled devices. A reader might infer from the absence of LLM-based entries that no cleared device uses one.

**Resolution.** That inference is wrong, and FDA's own page says why. It states the list "is not a comprehensive resource" and that the agency "will explore methods to identify and tag medical devices that incorporate foundation models encompassing a wide range of AI systems, from large language models (LLMs) to multimodal architectures."

**Therefore:** FDA has not said no cleared device contains a language model. It has said it does not currently identify which do. `verify.py` asserts `fda_has_stated_no_device_contains_an_llm` as **False** precisely to prevent this document making the inference it is warning against.

### 2.3 A conflict of interest disclosed by the authors

**What was found.** [L5], one of the five genuine LLM trials, discloses that two of its authors founded the company commercialising the platform being tested, that the analysis was completer-based, and that attrition was unexplained — **74** enrolled, **58** completed, **78.38%**.

**Resolution.** The study is used, with the conflict stated in the README's §24 as the authors themselves stated it. It is not excluded: a disclosed conflict handled openly is more useful than an undisclosed one, and the authors' own limitations paragraph is unusually candid.

**Why it is recorded here too.** Because it is a live example of Day 87's and Day 88's finding about vendor-authored evidence, appearing inside the very sample used to test this field's evidence quality.

### 2.4 A benchmark result that did not transfer

**The apparent conflict.** Models are ranked against each other on benchmarks. [L3] ran an actual randomised trial of medical education and found the DeepSeek arm outscored both control and ChatGPT arms, with **the ChatGPT arm not significantly better than traditional study**.

**Resolution.** Not a contradiction — different measurements. A benchmark measures answer accuracy on a fixed set; a trial measures whether learners learn more. The README reports this in §12 and §24 as evidence that the two do not automatically travel together, which is the point of the proxy ladder in §25.

### 2.5 A false lead that was discarded

**What was searched.** Whether any medical device has been cleared with LLM-based functionality, which would have materially changed §17.

**What was found.** Secondary sources assert it. FDA's own page does not identify any, and says it will explore methods to do so.

**Resolution.** The secondary claims are **not used**. §17 relies solely on FDA's own statements. If a cleared LLM-based device exists, the README's claim — that the list does not currently let a reader identify one — remains true, which is why the claim was written in that narrower form.

---

## Part 3 — Absences

| # | Absent | Where it would appear | Compelled by anything? |
|---|---|---|---|
| 1 | Any health-outcome randomised trial | The literature | **No** |
| 2 | Escalation rate on urgent presentations | Anywhere | **No** |
| 3 | Harm taxonomy and frequencies | Anywhere | **No** |
| 4 | Calibration — does confidence track correctness? | Anywhere | **No** |
| 5 | Accuracy stratified by language or region | Anywhere | **No** |
| 6 | Clinical accountability for an answer | Any framework | **No** |
| 7 | Identification of LLM-based cleared devices | FDA device list | Stated as intent, not done |
| 8 | Usage of these systems for health questions | Anywhere in the sources used | **No** |
| 9 | Vendor financials | A filing | **No** |
| 10 | A full screen of the 220 RCT-tagged records | This case study | Not attempted |

Items 1 through 5 share a property that no other day in this series produced: **every one could be published tomorrow by the vendor, at moderate cost, with no regulator involved — and none is.** §42 explains why, and the explanation is structural rather than cynical.

Item 10 is this document's own gap. Ten were read; 210 were not.

---

## Part 4 — Limitations

### 4.1 No model was tested

This case study did not ask any system a health question, score any answer, or assess any model's accuracy. It examined the evidence environment. `verify.py` asserts `this_case_study_tested_any_model` and `this_case_study_measures_chatgpt_accuracy` as **False**.

Anyone wanting to know how accurate these systems are on health questions should read the accuracy literature directly. This document does not answer that question and does not try.

### 4.2 Ten of 220

Covered in §1.3. The sample is small, non-random, and from one date. It supports "the headline is a ceiling"; it does not support a precise rate.

### 4.3 Broad queries

The term expansion that produced the false positives also inflates the denominator. The **ratio** is more robust than either absolute number, because both share a base query — but neither absolute number should be quoted as a precise census of the field.

### 4.4 No usage data

How many people use these systems for health questions is not established here and no figure is asserted. `verify.py` records `usage_figures_for_health_questions_are_known` as **False**. §8's problem statement describes a product's properties, not its scale.

### 4.5 One researcher, no peer review

Every case study in this series, including this one, was produced in a single working session, verified programmatically, and published without external review. The gates catch arithmetic. They do not catch a wrong framing, a missed source, or a misread statute.

### 4.6 Point-in-time

All figures as at **2026-09-28**, in a field where the 2025 literature grew **80.21%** over 2024. Every count here will be wrong within months, in a predictable direction.

---

## Part 5 — Verification Record

### 5.1 The gate

`verify.py` contains **180 checks**, all passing. It was written and passing **before the first sentence of `README.md` existed**.

Rounding is half-up to two or three decimals via `Decimal.quantize`, not Python's banker's rounding. Tolerance on floating comparisons is 0.005, tightened to 0.0005 where a three-decimal source figure is asserted. Derived values are computed from **unrounded** inputs throughout.

### 5.2 What failed on first run

**Nothing.** Zero hand-stated expectations were wrong — the second consecutive day, and only the second in the arc.

As on Day 89, this is reported as an observation rather than an improvement in care. Today's arithmetic is dominated by ratios of integers taken straight from search results (220/21033, 5/10, 422/220), which is the arithmetic least exposed to the rounded-intermediate trap that caught Days 82, 86, 87 and 88.

### 5.3 What the gate asserts that the prose could not

Two checks in Section 10 of the gate carry the day's real methodological finding:

```python
chk("wrong_rct_share_if_adjusted_ignored", 1.05, 1.05)
chk("right_rct_share_after_sampling",      0.52, 0.52)
```

The first is the number this case study would have published had the sample not been read. It is asserted **as wrong**, by name, so that if 1.05% ever appears in prose as the field's genuine trial rate, `crosscheck.py` traces it to a check whose name says so.

This is the same device used on Day 87 (six hand-stated values asserted as wrong), Day 88 (two), and Day 89 (one rounding illustration). It is the cheapest form of self-correction available: **write your errors into the machine so they cannot quietly return.**

### 5.4 Negative controls

Twelve checks assert **False**, listed in §53 of the README. Three deserve comment.

`this_case_study_tested_any_model` and `this_case_study_measures_chatgpt_accuracy` exist because the easiest way to misread this document is as an accuracy assessment. It is not one.

`the_sample_is_statistically_representative` exists because ten is not a sample from which to estimate a rate, and a later edit could easily drift into treating it as one.

`fda_has_stated_no_device_contains_an_llm` exists because that is exactly the inference §17 warns against, and a document warning against an inference should not make it.

### 5.5 The RICE assertion, for the last time

```python
chk_eq("p1_leads_base", base_rank[0], "P1")
chk_eq("p1_ranks_last_under_stress", stress_rank[-1], "P1")
chk_eq("p1_rank_reversal_is_total", base_rank[0] == stress_rank[-1], True)
```

P1 decays **99.00%** — the largest single-proposal decay in the series, across four days that each found the same reversal by a different mechanism.

Three further checks record the conclusion rather than the ranking: `publishing_an_outcome_claim_invites_device_classification`, `the_evidence_and_the_regulation_arrive_together`, and `this_is_why_benchmarks_are_published_and_trials_are_not`. Those are the case study's argument, written into the gate so the prose cannot drift from them.

### 5.6 The series retrospective is gated too

Section 8 of the gate asserts every headline figure from Days 83 to 90 — the 0-of-5 confirmation rate, the 0.27% coverage, the 73.81% self-authorship share, the 55.56% and 76.47% and 44.44% from Day 88, the 51 measures and 1-of-79 from Day 89.

It also counts something worth naming: **seven separate headline figures across this arc are exactly zero**, and `all_headline_zeros_are_zero` asserts it.

### 5.7 Cross-check

`crosscheck.py` extracts every two- and three-decimal figure from `README.md` and `ASSUMPTIONS.md` and confirms each traces to a value asserted in `verify.py`. Figures quoted at source precision are allow-listed with their source reference. Derived figures are never allow-listed; where the cross-check flagged one, it was added to the gate.

---

*Companion to `README.md`. Day 90 of 90. The series is complete.*
