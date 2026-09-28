# Day 90 — Health in ChatGPT: What Happens When Nothing Compels

**A Product Management case study on the largest health-answering system in the world, and the smallest proportion of evidence that measures anything.**

*Final case study in a 90-day series of evidence-based product case studies. Day 90 of 90.*

---

## 1. At a Glance

| | |
|---|---|
| **Subject** | General-purpose conversational AI used to answer health questions |
| **Securities disclosure obligation** | **None** — no SEC registrant |
| **Device authorisation** | **None** — 0 records across 4 FDA endpoints |
| **Health-service registration** | **None** |
| **Regulatory regimes compelling clinical evidence** | **0** |
| **Peer-reviewed papers on LLMs and health** | **21,033** |
| **Tagged as randomised controlled trials** | **220 — 1.05%** |
| **Systematic reviews** | **422 — 1.92 reviews per trial** |
| **RCTs sampled and read in full** | **10** |
| **Of those, false positives with no LLM at all** | **5 — 50.00%** |
| **Of those, measuring a patient health outcome** | **0 — 0.00%** |
| **Verification** | `verify.py` — **180 programmatic checks, all passing** |

---

## 2. Why This, Last

Eighty-nine days of this series have asked one question in different forms: **what makes a company publish evidence about whether its product works?**

The answers have been consistent and uncomfortable. Day 87's Tempus AI, with the maximum securities-disclosure burden available — audited accounts, ten SEC comment letters, sixty-six staff comments — published **zero** performance metrics for its clinical algorithms. Day 88's Qure.ai, private and with no securities obligation at all, published nine FDA clearances, five carrying full sensitivity and specificity. Day 89's registry collects every Indian fertility clinic's outcomes by law and publishes **none** of them.

Three regulators. Three different answers. None of them the one the reader needed.

Day 89 named what had to come last:

> A general-purpose conversational system used for health questions has no device clearance for any indication, no securities disclosure tied to clinical performance, no registry, no clinic-level outcome data, and no indication-specific evidence base. After eighty-nine days of asking what compels evidence, the final case asks what happens when **nothing does**.

This is that case. And the answer is not what eighty-nine days of pattern would predict.

**It is not that nothing gets published.** An enormous amount gets published — 21,033 papers, more evidence by volume than any subject in this series. It is that almost none of it measures an outcome, and that when I read a sample of the studies that appeared to, half of them turned out not to be about language models at all.

---

## 3. How to Read This Case Study

This is the last of ninety, so it does two jobs: it examines one subject, and it closes a series.

- **The regulatory null**: §14 through §20.
- **The literature and what reading it revealed**: §21 through §30.
- **The ninety-day retrospective**: §52 through §62.

Every figure carrying two or three decimal places is produced by `verify.py`. Nothing is estimated or inferred unless the sentence says so.

One framing note, stated at the top because it governs everything below. **This case study does not test any model.** It did not ask a model a health question, did not score an answer, and does not assert any accuracy figure for any system. `verify.py` records `this_case_study_tested_any_model` as **False**. What it examines is the *evidence environment* — what exists, what compels it, and what a person relying on it can establish.

---

## 4. Evidence Standard

The standard this series has used since Day 1, in its final form:

1. **No fabrication.** No metric, date, or relationship appears unless it is in a cited primary source.
2. **Facts and inferences are separated at the sentence level.**
3. **Arithmetic is executed, not asserted.** Every derived figure is computed in `verify.py` from unrounded inputs before any prose exists.
4. **Absences are findings.** What a source does not say is recorded as a fact about the source.
5. **The gate precedes the prose.**
6. **A named company is a specimen, not a defendant** — added on Day 89.
7. **A null requires a positive control** — added today, and §15 explains why it should have been there from the start.

---

## 5. Source Inventory

All sources retrieved 2026-09-28.

**Regulatory and registry**

| Ref | Source |
|---|---|
| **[F]** | openFDA device API — `510k`, `pma`, `classification`, `registrationlisting` endpoints |
| **[FL]** | FDA, *Artificial Intelligence-Enabled Medical Devices* list page |
| **[S]** | SEC EDGAR company search |

**Peer-reviewed literature.** According to PubMed, with DOIs as that source requires:

| Ref | Study | PMID | DOI |
|---|---|---|---|
| **[L1]** | Weissman GE, Mankowitz T, Kanter GP. *Unregulated large language models produce medical device-like output.* npj Digital Medicine 2025;8(1):148 | 40055537 | [10.1038/s41746-025-01544-y](https://doi.org/10.1038/s41746-025-01544-y) |
| **[L2]** | Ahmed A, Leroy G, et al. *Trust in Generative AI for Health Information Consumption and the Effect of Learned Dependency.* J Med Internet Res 2026;28:e98326 | 42747973 | [10.2196/98326](https://doi.org/10.2196/98326) |
| **[L3]** | Yang W, et al. *Effectiveness of ChatGPT and DeepSeek in Urology Medical Education: RCT.* J Med Internet Res 2026;28:e89315 | 42766393 | [10.2196/89315](https://doi.org/10.2196/89315) |
| **[L4]** | He H, et al. *AI Health message intervention.* Patient Educ Couns 2026;152:109807 | 42537382 | [10.1016/j.pec.2026.109807](https://doi.org/10.1016/j.pec.2026.109807) |
| **[L5]** | Borckardt JJ, et al. *Knowledge Acquisition, Case Discussion, and Engagement in Health Professional Students.* JMIR Nurs 2026;9:e98700 | 42777164 | [10.2196/98700](https://doi.org/10.2196/98700) |
| **[L6]** | Kumar A, et al. *Using randomization to compare AI and expert-generated formative assessment questions.* Med Educ Online 2026;31(1):2671586 | 42106900 | [10.1080/10872981.2026.2671586](https://doi.org/10.1080/10872981.2026.2671586) |

No vendor blog, press release, model card, or benchmark announcement is used anywhere in this document. §61 says what that cost.

---

## 6. Evidence Tiers

Day 87 introduced tiering by *what compelled the statement*. Here is the final version, and it is the shortest in the series.

| Tier | Description | Present here? |
|---|---|---|
| **T1 — Regulator-authorised performance data** | Submitted to and accepted by a regulator | **No — none exists** |
| **T2 — Independent peer-reviewed outcome trial** | Researchers with no stake measure a health outcome | **None found in sample** |
| **T3 — Independent peer-reviewed proxy study** | Education, intention, trust, benchmark accuracy | **Yes — the bulk of it** |
| **T4 — Vendor-published benchmark** | The vendor writes the test and reports the score | Exists; **not used here** |
| **T5 — Product surface** | What the system says when asked | Not examined |

The whole evidence base for the most widely used health-answering system sits in **T3**, and T3 measures proxies.

---

## 7. What This Case Study Is About

Precision matters here more than anywhere else in the series, because the subject is diffuse.

**In scope:** the evidence environment surrounding general-purpose conversational AI used for health questions. What regulatory obligations attach, what literature exists, what that literature measures, and what a person can establish.

**Out of scope:** whether any particular model gives good health answers. That is an empirical question requiring a study design, a ground truth, and a clinical panel. This case study has none of those and makes no claim of the kind.

The distinction is the same one Day 88 drew between a device's *cleared performance* and its *performance in your population*, and the same one Day 89 drew between a registry that *collects* and one that *publishes*. Three days, three versions of: **be precise about what your evidence is evidence of.**

---

## 8. Problem Statement

Stated from the evidence:

> A person with a health question has, for the first time, a system that will answer it fluently, immediately, at no cost, in their own language, at any hour, with unlimited follow-up. Every previous option — a search engine, a helpline, a clinic, a relative — was worse on at least one of those dimensions. The system is not authorised as a medical device anywhere, its answers are not covered by any clinical accountability framework, and the literature about it measures examination scores rather than whether anyone got better.

Every clause of that paragraph is a product achievement except the last two.

---

## 9. Jobs to Be Done

| Job | Previous alternative | Why the new option wins |
|---|---|---|
| "Tell me what this symptom might be" | Search engine, forum | Answers the actual question asked, not the closest keyword match |
| "Explain what my doctor said" | Nobody | No prior option existed at all |
| "Is this urgent?" | Helpline, guesswork | Immediate, no queue, no cost |
| "What should I ask at my appointment?" | Nobody | Structured, unhurried |
| "Translate this result" | Search, relative | Handles jargon and language at once |
| **"Is this answer right?"** | — | **Unanswerable** |

Rows 1–5 explain the adoption. Row 6 is this case study.

Note what rows 2 and 4 have in common: **the previous alternative was nothing.** A system does not have to beat a doctor to be used; it has to beat silence. That is a low bar and an honest account of why usage is what it is.

---

## 10. User Personas

Two, both constructed from what the sources establish. No invented quotes.

---

## 11. Persona 1: The Person With a Question at Midnight

**Basis:** [L2]; the job table in §9.

**Context.** Has a symptom, a letter, or a result. Has no access to a clinician at this hour, or does not think the question merits one. Would previously have searched, and would have received ten pages ranked by something other than accuracy.

**What they get.** A direct, fluent, confident answer.

**What they cannot do.** Calibrate it. And [L2] measured exactly this: across two randomised experiments with **338** and **563** participants — **901** in total — participants trusted accurate AI health information more than inaccurate information, **but the more habitually dependent on the system a user was, the less their trust tracked whether the answer was correct.** The interaction between accuracy and learned dependency was negative and significant in both experiments: **−0.399** and **−0.459**.

The authors also tested a design fix — highlighting critical information in the text — and it **did not work**. It neither affected trust nor moderated the dependency effect.

That is the single most product-relevant finding in the whole Day 90 literature: **the users who rely on the system most are the ones least able to tell when it is wrong, and the obvious UI intervention does not help.**

---

## 12. Persona 2: The Clinician Downstream

**Basis:** [L1], [L3], [L5], [L6].

**Context.** Sees patients who arrive having already asked. Is also, increasingly, a user — the sampled literature is dominated by medical education studies.

**What the record gives them.** Four of the five genuine trials in my sample measured **medical education**: AI-generated versus expert-written exam questions [L6], GPT-4o virtual patient cases versus written cases [L5], ChatGPT versus DeepSeek for urology teaching [L3].

**What [L3] found is worth stating plainly.** In a head-to-head randomised trial, the DeepSeek arm outscored both control and ChatGPT arms; **the ChatGPT arm's improvement over traditional study was not statistically significant.** A model that wins on benchmark accuracy did not produce a significant learning gain in a trial.

**What none of them gives them.** Any evidence about what happens to a patient.

---

## 13. User Journey: Asking a Health Question

```
  Person                     System                    Evidence available
     |                          |                              |
 [1] | "should I worry         |                              |
     |  about this?"  -------> |                              |
     |                          | [2] fluent answer,          |
     |                          |     immediate, free          |
     |                          |                              |
 [3] |<------ answer ---------- |                              |
     |                                                          |
 [4] | "is this right?"                                        |
     |    |                                                     |
     |    +--> device authorisation? ------> NONE (0 of 4 FDA endpoints)
     |    +--> securities disclosure? -----> NONE (no registrant)
     |    +--> registry of outcomes? ------> NONE
     |    +--> peer-reviewed outcome trial? -> 0 of 10 sampled
     |    +--> benchmark score? -----------> exists, vendor-authored
     |                                                          |
 [5] | acts on [3]                                             |
```

Step 4 has five branches and four of them terminate in nothing. The fifth reaches a number that the vendor produced by running its own model against its own test.

---

## 14. The Central Question

> **What does the evidence environment look like when no regulator compels anything?**

The eighty-nine days before this would predict silence — the Day 84 pattern, where a vendor's own peer-reviewed studies reported **zero** accuracy metrics, or the Day 89 pattern, where **zero** of 161 clinics published the outcome that mattered.

**That prediction is wrong, and the way it is wrong is the finding.**

There is no silence. There are 21,033 papers. The literature on LLMs in health is larger than the literature this series found for any other subject, by an order of magnitude, and it is growing at **80.21%** a year.

What is missing is not volume. It is **measurement of outcomes** — and, as §23 shows, the count of studies that appear to measure outcomes is itself roughly **double** the true figure.

---

## 15. The Regulatory Null, And How To Earn One

Day 88 used the openFDA API to find nine clearances for Qure.ai. Today the same method, pointed at the vendor of the most widely used health-answering system, returns this:

| FDA endpoint | Records |
|---|---:|
| `510k` — premarket notification | **0** |
| `pma` — premarket approval | **0** |
| `classification` — device classification | **0** |
| `registrationlisting` — establishment registration | **0** |

Four endpoints. Zero records.

**A null result is only worth reporting if the method would have found something.** This series has, until today, relied on an implicit assumption that a query returning nothing means nothing exists. That assumption failed on Day 88, where two of nine clearance PDFs initially returned errors and a silent acceptance would have produced a case study asserting seven clearances instead of nine.

So today the nulls are anchored to **positive controls**:

| Control | Records |
|---|---:|
| `applicant:"qure.ai"` — yesterday's subject | **9** |
| `applicant:Verily` | **4** |

Both non-zero. The endpoint works, the applicant field is populated, the query syntax is right. **The zeros are measurements, not failed queries.** `verify.py` asserts `method_validated_before_asserting_a_null` and `zero_is_a_measurement_not_a_failed_query`.

This is Evidence Standard 7, added on the last day, and it belonged in the list on the first. It is the discipline that separates "I found nothing" from "there is nothing."

SEC EDGAR returns **0** registrants matching the vendor's name. There is no securities filing, because there is nothing to file with.

---

## 16. The Null, Independently Confirmed

A null derived from one researcher's API query is worth less than a null a journal has published. This one has both.

Weissman, Mankowitz and Kanter, in npj Digital Medicine [L1], state it directly:

> "Large language models (LLMs) show considerable promise for clinical decision support (CDS) but **none is currently authorized by the Food and Drug Administration (FDA) as a CDS device.**"

Their study went further than the registry check. They evaluated whether **two** popular LLMs could be induced to produce device-like clinical decision support output, and found that the output "readily produced device-like decision support across a range of scenarios, suggesting a need for regulation if LLMs are formally deployed for clinical use."

That is the substantive version of the finding, and it is sharper than the registry query alone. The question is not whether these systems are *classified* as devices. It is that **they produce the output a device would produce, without being one.**

---

## 17. Even Where an LLM Is Inside a Device, You Cannot Tell

FDA maintains a public list of AI-enabled medical devices. Its own page [FL] says two things that matter.

First, on scope: **"The list is not a comprehensive resource of AI-enabled medical devices."**

Second, and more importantly:

> "To support transparency in the use of modern AI technologies, the FDA **will explore methods to identify and tag** medical devices that incorporate foundation models encompassing a wide range of AI systems, from large language models (LLMs) to multimodal architectures."

*Will explore methods to identify.* Which means that today, **FDA does not tag which authorised devices contain a language model**, and a reader of that list cannot tell.

So the picture is:

- Systems used directly by the public for health questions: **not devices, not authorised, not listed.**
- Systems embedded inside authorised devices: **authorised, listed — and not identifiable as LLM-based.**

Day 88's lesson was that classification is destiny: what a regulator calls your product determines what the public learns about it. Day 90 adds the corollary. **When a technology arrives faster than its classification, the register cannot see it — not because the register is careless, but because a classification system can only describe categories it already has.**

`verify.py` records `fda_has_stated_no_device_contains_an_llm` as **False**, because FDA has stated no such thing. The correct claim is narrower and stranger: nobody can currently tell.

---

## 18. The Benchmark Problem

Day 87 found that Tempus AI's supporting literature was **73.81%** self-authored at its last disclosure, and that the company stopped publishing that ratio once the SEC stopped reviewing its filings.

The same structure exists here, at a larger scale and with an additional turn of the screw.

In this category, the organisation that builds the model frequently also builds the evaluation set, runs the evaluation, and publishes the score. The measuring instrument, the subject of measurement, and the publisher are the same party — and unlike Tempus, no regulator has ever required otherwise, so there is no ratio to stop publishing.

This case study **excludes vendor benchmarks entirely**. `verify.py` asserts `any_vendor_benchmark_score_is_asserted_here` as **False**. That is a deliberate constraint and it has a cost: it makes the evidence picture look thinner than a vendor presentation would. §61 states the trade.

The reason for the exclusion is the one Day 87 arrived at. A number is worth what the independence of its producer is worth, and a benchmark whose author, subject and publisher coincide is not independent in any of the three ways that matter.

**The transferable test, which works on any metric in any industry:** count how many distinct parties stand between the thing being measured and the number you are reading. In a cleared device (Day 88) there are two — the manufacturer and a reviewer. In an independent trial (Day 88's TB literature) there are two, and the second has no commercial stake. In a vendor benchmark there is one.

---

## 19. The Literature

Now the part that breaks the pattern of the preceding eighty-nine days.

A PubMed search on 2026-09-28 for language-model and health terms returns **21,033** papers.

| Cut | Count | Share |
|---|---:|---:|
| All papers | **21,033** | 100% |
| Tagged randomised controlled trial | **220** | **1.05%** |
| Systematic reviews | **422** | **2.01%** |

**One paper in 95.60 is a randomised trial.**

And there are **1.92 systematic reviews for every randomised trial** — **202** more reviews than trials.

That ratio deserves a moment. A systematic review synthesises primary studies. A field with twice as many reviews as trials is **reviewing itself faster than it is testing itself**. The synthesis layer has outgrown the thing it synthesises.

---

## 20. The Growth Curve

| Year | Papers | Growth |
|---|---:|---:|
| 2023 | 1,877 | — |
| 2024 | 4,219 | **+124.77%** |
| 2025 | 7,603 | **+80.21%** |

**4.05 times** as many papers in 2025 as in 2023. The remaining **7,334** fall outside this three-year window.

```
 Papers per year
 8000 |                                    ███ 7,603
      |                                    ███
 6000 |                                    ███
      |                                    ███
 4000 |                   ███ 4,219        ███
      |                   ███              ███
 2000 |   ███ 1,877       ███              ███
      |   ███             ███              ███
    0 +---------------------------------------
        2023             2024             2025
```

Nothing about that curve is a criticism. It is what a field looks like when something genuinely new arrives. The question is what all that work is measuring — and §21 is where I stopped counting and started reading.

---

## 21. Why 1.05% Is Not The Finding

It would be easy to stop at "only 1.05% of the literature is randomised trials," put it on a slide, and move on.

This series has spent eighty-nine days learning not to do that.

Day 87 found that a naive regular expression over SEC comment letters overcounts, because financial-statement note captions look like comment numbers. Day 88 found that a text search for "sensitivity" in an FDA summary returns a hit about *radiographic* sensitivity, not device performance. Day 89 found that "public record system" and "publicly readable" are different claims.

In every case, the correction came from **reading the source instead of counting matches.**

So before using 220, I read ten of them.

---

## 22. What Reading Ten Trials Showed

Ten of the 220 RCT-tagged records, taken from the most recent results, read in full:

| PMID | What it actually is | LLM? | Health outcome? |
|---|---|:---:|:---:|
| 42106900 | AI vs expert-written exam questions, medical students | **Yes** | No — education |
| 42695229 | Alcohol hand rub for newborns, rural Uganda | **No** | No |
| 42634930 | Sodium pentaborate for obesity, phase 1/2 | **No** | No |
| 42537382 | ChatGPT-4o breast screening messages, n=391 | **Yes** | No — intention |
| 42581237 | Shockwave vs diathermy, lumbar spondylosis | **No** | No |
| 42329510 | Nociception-guided opioid titration | **No** | No |
| 42259717 | Valsartan/amlodipine/chlorthalidone, hypertension | **No** | No |
| 42777164 | GPT-4o virtual patients vs written cases | **Yes** | No — education |
| 42766393 | ChatGPT vs DeepSeek, urology teaching | **Yes** | No — education |
| 42747973 | Trust calibration and learned dependency, n=901 | **Yes** | No — trust |

**Five of the ten have nothing to do with language models at all.**

A hand-hygiene trial in Uganda. An obesity drug trial. A physiotherapy trial. An anaesthesia trial. A hypertension drug trial. They are in the result set because the query's term expansion is enormous — PubMed expands "medical OR health OR clinical" into dozens of variants including "clinic", "medication" and "medically" — and a paper can match on the health side without matching meaningfully on the AI side.

**And of the five that genuinely concern language models, not one measured a patient health outcome.** Four measured education. One measured trust.

---

## 23. What That Does To The Headline

| | Value |
|---|---:|
| RCT-tagged records | 220 |
| Sampled | 10 |
| Genuine LLM studies in sample | 5 — **50.00%** |
| False positives | 5 — **50.00%** |
| **Adjusted estimate of genuine LLM RCTs** | **110** |
| **Overcount multiple** | **2.00×** |
| Adjusted share of the literature | **0.52%** |
| **One genuine trial per** | **191.21 papers** |

**220 is a ceiling, not a count.** The honest figure is about half of it, and `verify.py` asserts both — `wrong_rct_share_if_adjusted_ignored` at 1.05 and `right_rct_share_after_sampling` at 0.52 — so that if the larger number ever appears in prose as a result, the cross-check traces it to a check whose name says it is the wrong one.

And the number that matters most is not an estimate at all. **Zero of ten sampled trials measured a patient health outcome.** That is a direct count of what I read.

---

## 24. What The Genuine Trials Did Measure

Three proxies, and they are worth naming because they recur across the field.

**Education.** [L6] found students could not distinguish AI-generated from expert-written exam questions, though they rated **53%** of AI questions as easy against **31%** of expert ones. [L5] found interactive GPT-4o virtual patients beat static written cases on knowledge gain — with **74** enrolled, **58** completing (**78.38%**), unexplained attrition, and **two** authors who founded the company commercialising the platform, all disclosed by the authors themselves. [L3] found DeepSeek beat both control and ChatGPT arms, with the ChatGPT arm **not significantly better than control**.

**Intention.** [L4] randomised **391** participants across generic, targeted and tailored breast-screening messages, human- and AI-generated, and found AI-generated messages performed comparably to human-written ones on self-efficacy and behavioural intention.

**Trust.** [L2], covered in §11.

Every one is a legitimate study answering a legitimate question. **None of them answers "does using this make anyone healthier or safer."**

---

## 25. The Proxy Ladder

This series has now watched the same substitution happen four times, in four industries, under four regulators.

| Day | What was measured | What it stood in for |
|---|---|---|
| 84 | Note-quality scores | Clinical documentation benefit |
| 87 | Development *process* for an algorithm | Algorithm accuracy |
| 88 | Accuracy on one US test set | Accuracy in your population |
| 89 | Pregnancy per transfer | A baby |
| **90** | **Exam scores, intention, trust** | **Whether anyone got better** |

Each substitution is upward — toward something earlier in the causal chain, cheaper to measure, and more flattering. Day 89 made the mechanism explicit: **"per transfer" has already removed every patient who never reached transfer.** An exam score has removed every patient entirely.

> **A proxy is not a lie. It is a measurement of something that is easier to measure, offered in place of something that is harder. The question to ask of any metric is not "is it true" but "what did it replace, and who chose."**

---

## 26. Who Funds Which Evidence

A question worth asking of any literature: who pays for each kind of study, and what does that predict?

| Evidence type | Typical funder | Cost | Produces |
|---|---|---|---|
| Benchmark evaluation | The vendor | Low | A comparable score |
| Academic accuracy study | University, grant | Low–moderate | A published comparison |
| Education RCT | University, department | Moderate | A learning outcome |
| **Health outcome RCT** | **Grant, health system, or vendor** | **High** | **The answer** |

The ordering is not accidental. Cost rises down the table and so does the strength of the claim — and the cheapest row is the one a vendor can run alone, on itself, in an afternoon.

Day 88 is the counter-example that proves the rule. Its most valuable evidence — independent head-to-head comparisons of twelve products — existed because tuberculosis attracts global-health funding, and researchers in Dhaka, Cape Town and Lima had a non-commercial reason to measure. **76.47%** of that literature had no vendor author.

No equivalent funding stream exists for "does a general-purpose assistant improve health decisions." The question is too diffuse for a disease-specific funder, too clinical for a computer-science funder, and too expensive for a vendor to run against its own interest, per §42.

**That is a structural explanation for the 1.05%, and it does not require anyone to have behaved badly.**

---

## 27. The Evidence Ledger

Five questions a person relying on this technology for health would want answered.

| # | Question | Status | What compelled it |
|---|---|---|---|
| 1 | Is it accurate on benchmarks? | **Disclosed** | Vendor and academia |
| 2 | Does it change health outcomes? | **Not disclosed** | *Nothing* |
| 3 | What are the harms? | **Not disclosed** | *Nothing* |
| 4 | Who is clinically accountable? | **Not disclosed** | *Nothing* |
| 5 | Is it a regulated device? | **Disclosed** | Device law |

- **2 of 5 (40.00%)** disclosed.
- **3 of 5 (60.00%)** not disclosed.
- **1** row compelled by a regulator — and **the only thing a regulator compelled is the answer that nothing else is compelled.**

Row 5 is the joke the series ends on. The one question the regulatory system answers definitively is whether the regulatory system applies. It does not.

Across the four regulated-and-unregulated days:

| Day | Subject | Regulator | Ledger answered |
|---|---|---|---:|
| 87 | Tempus AI | Securities | **40.00%** |
| 88 | Qure.ai | Device | **60.00%** |
| 89 | Gaudium IVF | Health service | **20.00%** |
| 90 | Health in ChatGPT | **None** | **40.00%** |

Mean: **40.00%**. The best-answered was the device-regulated one; the worst was the clinical service whose regulator collects and does not publish. **Having no regulator at all scored the same as having the SEC.**

---

## 28. The Four-Regulator Table

The closing structure of the series.

| Regulator | Compels | Does it reach the public? | Compels an outcome measure? |
|---|---|:---:|:---:|
| Securities (Day 87) | Process | **Yes** | **No** |
| Device (Day 88) | Performance | **Yes** | **No** |
| Health service (Day 89) | Collection | **No** | **No** |
| None (Day 90) | Nothing | — | **No** |

- **3 of 4** regimes compel something real.
- **2 of 4 (50.00%)** produce output that reaches a member of the public.
- **0 of 4** compel a measurement of whether anyone is better off.

That bottom-right column is the ninety-day finding. Not that regulation fails — three of these regimes work, and work well, at the job they were designed for. **It is that no one designed a regime whose job was the reader's question.**

---

## 29. Feature Analysis

Assessed as an information product against the alternatives it displaced.

| Capability | Search engine | Clinic | Health helpline | Conversational AI |
|---|:---:|:---:|:---:|:---:|
| Answers the question asked | Partly | Yes | Yes | **Yes** |
| Available immediately | Yes | No | Partly | **Yes** |
| Free at point of use | Yes | Varies | Varies | **Yes** |
| Unlimited follow-up | No | No | No | **Yes** |
| Handles the user's own language | Partly | Varies | Varies | **Yes** |
| **Clinically accountable** | No | **Yes** | **Yes** | **No** |
| **Authorised for the purpose** | No | **Yes** | Varies | **No** |
| **Outcome evidence exists** | No | Varies | Varies | **No** |

The top five rows explain adoption completely. The bottom three explain this case study completely. **The product won on every dimension a user can perceive and lost on every dimension a user cannot.**

---

## 30. Competitive Analysis

The competitive frame that matters is not model-versus-model. It is **evidence regime versus evidence regime**.

| Competitor | Evidence obligation | What a user can check |
|---|---|---|
| A cleared diagnostic device (Day 88) | Device law | Sensitivity, specificity, on one population |
| A listed health company (Day 87) | Securities law | Financials; not algorithm performance |
| A clinic (Day 89) | Registration only | Corporate existence |
| **Conversational AI** | **None** | **Benchmark scores the vendor published** |

The competitive insight for a PM is uncomfortable and worth sitting with: **operating in the unregulated category is a durable structural advantage.** A cleared device must publish performance; a general-purpose assistant answering the same question need not. Any obligation you take on voluntarily is an obligation your closest substitute does not carry.

§45 is about what that does to the obvious recommendation.

---

## 31. Porter's Five Forces

| Force | Assessment | Basis |
|---|---|---|
| **Buyer power** | **Very low** | Cannot evaluate the answer; [L2] shows the most reliant are least calibrated |
| **Rivalry** | **High, on capability** | [L3] shows models being compared head-to-head — on exams |
| **New entrants** | **Moderate** | Capital-intensive to train; trivial to deploy a wrapper |
| **Supplier power** | Not establishable | No disclosure |
| **Substitutes** | **Weak** | §27's top five rows: every substitute loses on perceivable dimensions |

The buyer-power row is the same structural problem Day 89 found in fertility: a buyer who cannot evaluate and does not learn from repetition. **Except here the transaction is free, instantaneous, and repeated many times a day** — which removes even the friction that would prompt someone to seek a second opinion.

---

## 32. SWOT

**Strengths**
- Wins on all five perceivable dimensions in §27.
- Serves jobs where the previous alternative was **nothing**.
- An enormous and fast-growing research literature — **21,033** papers, **+80.21%** year on year.

**Weaknesses**
- **0** regulatory authorisations across 4 FDA endpoints.
- **0** of 10 sampled trials measured a patient health outcome.
- Produces device-like clinical decision support without being a device [L1].
- No clinical accountability framework attaches to any answer.

**Opportunities**
- Publishing one genuine outcome trial would make it the only system in this category with T2 evidence.
- **1.92** reviews per trial means the synthesis capacity already exists and is starved of primary studies.
- [L2]'s failed design intervention is an open problem with a clear brief.

**Threats**
- [L1]'s finding — device-like output — is the argument for regulation, already in a peer-reviewed journal.
- **50.00%** false-positive rate in the RCT-tagged literature means the field's own evidence base is being systematically over-read.
- Learned dependency degrades trust calibration, and the effect **replicated**.

---

## 33. Business Model

| Element | What can be established |
|---|---|
| Revenue | **Not disclosed** — no SEC registrant |
| Pricing for health use | No separate health product to price |
| Usage for health questions | **Not established here** — no figure is asserted |
| Cost per health conversation | Not disclosed |
| Clinical liability | **None attaches** — not a device, no accountability framework |

The row that matters is the last one, and it is the one that makes this category structurally different from everything else in the series.

Day 88's subject bore device liability. Day 89's bore clinical liability as a healthcare provider. Day 87's bore securities liability, with officers personally certifying filings.

Here, a health answer is delivered with **none of the three**. Not because anyone evaded them, but because a general-purpose system answering a health question among millions of other questions does not obviously fall inside any of the three frameworks — which is precisely [L1]'s point about device-like output.

---

## 34. Business Model Canvas

| Block | Content |
|---|---|
| **Key partners** | Not disclosed |
| **Key activities** | Model training; inference; safety work |
| **Key resources** | Models; compute; training data |
| **Value propositions** | Immediate, free, fluent answers in the user's own language, with unlimited follow-up (§29) |
| **Customer relationships** | Self-serve, conversational, repeated |
| **Channels** | App, web, API, embedded surfaces |
| **Customer segments** | Everyone — health is one use among many |
| **Cost structure** | Not disclosed |
| **Revenue streams** | **Not disclosed** |

The segment row is the interesting one. **Health is not a product here; it is a use case that emerged.** Nothing was cleared for it, priced for it, or evidenced for it, because nothing was built specifically as it.

That is the cleanest statement of why every regulatory framework in this series misses: **all four attach to products defined by purpose, and this is a product defined by generality.**

---

## 35. Metrics That Matter

| Metric | Why | Published? |
|---|---|:---:|
| Health outcomes in a randomised trial | The only thing that answers the question | **No** |
| Harm rate in real health conversations | What can go wrong | **No** |
| Refusal / escalation rate on urgent presentations | Whether it sends people to care | **No** |
| Accuracy stratified by language and region | Whether it works outside English | **No** |
| Calibration — does confidence track correctness? | [L2]'s mechanism | **No** |
| Benchmark accuracy | Cheap, comparable, vendor-run | **Yes** |

Six rows. One filled. The one that is filled is the one the vendor can run on itself.

That is Day 87's finding at the largest possible scale. There, 73.81% of the cited literature was self-authored at the last disclosure, and the ratio stopped being published once the SEC stopped reading. Here, the measurement instrument, the subject, and the publisher are the same organisation, and no one has ever required otherwise.

---

## 36. AARRR

| Stage | What is measurable publicly |
|---|---|
| **Acquisition** | Not disclosed; health is not separately acquired |
| **Activation** | First useful answer — not measured anywhere |
| **Retention** | Return use — and see the note below |
| **Revenue** | **Not disclosed** |
| **Referral** | Word of mouth; no outcome-based signal exists |

Day 89 flagged a retention trap in fertility: a second cycle means the first one failed, so naive retention scores a failing clinic as a good one.

There is a sharper version here. **[L2] establishes that habitual reliance — learned dependency — weakens a user's ability to detect when an answer is wrong**, with a negative interaction replicated across **901** participants (**−0.399** and **−0.459**).

Which means retention in this category is not merely an ambiguous success signal. **It is correlated with a measured degradation in the user's ability to evaluate the product.** A team optimising engagement here is optimising something that the only relevant trial says makes users worse at judging the output.

---

## 37. HEART

| Dimension | Signal | Publicly available? |
|---|---|:---:|
| **Happiness** | Satisfaction with answers | Not published |
| **Engagement** | Health conversations per user | Not published |
| **Adoption** | New users asking health questions | Not published |
| **Retention** | Return for further health questions | Not published — and see above |
| **Task success** | **Did the person end up better informed and appropriately in care?** | **Not published** |

Day 87's task-success row was empty for a company with $1.27bn of audited revenue. Day 88's was the only full row in its table, because device regulation required it. Day 89's was empty, and task success there was a baby.

Day 90's is empty too — and this is the last table in the series.

---

## 38. North Star and Guardrails

**North Star:** *Health conversations that end with the person better informed and, where warranted, in contact with care.*

Deliberately two-part. Accuracy alone is insufficient — a correct answer that fails to escalate an emergency is a failure. And escalation alone is insufficient — a system that sends everyone to A&E is useless.

**Guardrails:**

| Guardrail | Discipline |
|---|---|
| Escalation floor | A published minimum escalation rate on urgent presentations |
| Calibration | Expressed confidence must track measured correctness |
| Harm reporting | Published alongside any accuracy claim, in the same document |
| Independence | Any headline accuracy figure carries who built the test |
| **No outcome claim without an outcome study** | An education or benchmark result is never reported as a health result |

The last guardrail is the one this whole series converges on, and it can be stated in one line for any product in any industry:

> **Never let a proxy carry the sentence that only an outcome can support.**

---

## 39. Product Recommendations

**P1 — Publish outcome evidence for health use.**
*Gap:* §21–§22. Zero of ten sampled trials measured a patient health outcome.
*Change:* Fund and publish a randomised trial with a health outcome — decision quality, appropriate escalation, or resolution — in a pre-registered protocol with an independent analysis team.
*Why:* It is the only recommendation that answers the question. Nobody in the category has done it.

**P2 — Label the health-answer surface.**
*Gap:* §15–§17. No authorisation, and the absence is not visible at the point of use.
*Change:* A persistent, plain statement on health-topic conversations: not a medical device, not authorised for diagnosis, here is what to do in an emergency.
*Why:* Cheap, unambiguous, and directly addresses [L1]'s device-like-output finding.

**P3 — Seek a device pathway for one narrow indication.**
*Gap:* §16. Device-like output, no device framework.
*Change:* Take one bounded, high-value use and put it through an actual authorisation process.
*Why:* It converts an unregulated capability into an evidenced one, and it would be first.

**P4 — Publish harms and refusal rates.**
*Gap:* §31. No harm metric of any kind is published.
*Change:* Report escalation rates on urgent presentations and a harm taxonomy with frequencies, beside any accuracy claim.
*Why:* Day 89 found **1 of 79** UK clinic websites mentioned adverse events. The bar is on the floor.

---

## 40. RICE Prioritisation

**Definitions.** Reach ordinal 1–10 with the anchor stated. Impact 0.25/0.5/1/2/3. Confidence 0–1. Effort in person-months. RICE = (R × I × C) / E.

| | Reach | Reach anchor | Impact | Conf. | Effort | **RICE** |
|---|---:|---|---:|---:|---:|---:|
| **P1** Outcome evidence | 10 | Everyone using it for a health question | 3.0 | 0.80 | 1.25 | **19.20** |
| **P2** Label the surface | 5 | Users in health-topic conversations | 1.0 | 0.95 | 0.30 | **15.83** |
| **P3** Device pathway, one indication | 8 | Users of that indication, and the category | 2.0 | 0.55 | 4.00 | **2.20** |
| **P4** Harms and refusal rates | 7 | Users weighing whether to act | 2.0 | 0.70 | 1.75 | **5.60** |

**Base ranking: P1 (19.20) → P2 (15.83) → P4 (5.60) → P3 (2.20).** Spread **17.00**.

---

## 41. The Stress Test

| | Binding constraint | C mult. | E mult. | **Stressed** | Decay |
|---|---|---:|---:|---:|---:|
| **P1** | Publishing an outcome study creates the evidence that the product performs a medical function — which is the argument for classifying it as a device | **0.08** | **8.00** | **0.19** | **−99.00%** |
| **P2** | Copy and design review | 0.95 | 1.20 | **12.53** | −20.83% |
| **P3** | Submission, evidence assembly, review timeline | 0.80 | 1.50 | **1.17** | −46.67% |
| **P4** | Publishing harms invites the question no competitor answers | 0.60 | 2.00 | **1.68** | −70.00% |

**Stressed ranking: P2 (12.53) → P4 (1.68) → P3 (1.17) → P1 (0.19).**

**P1 goes from first to last**, for the fourth consecutive day and the last time. The reversal is asserted programmatically — `p1_leads_base` and `p1_ranks_last_under_stress` are both hard assertions in the gate. The field compresses from **17.00** to **12.34**.

---

## 42. Why P1 Dies — The Last Time

Four days, four mechanisms. They are not the same mechanism wearing different clothes, and the differences are the point.

| Day | P1 | Why it died |
|---|---|---|
| 87 | Restore the self-authorship numerator | **Legal exposure** — a recurring, quantified, unflattering disclosure carries audit and restatement risk |
| 88 | Publish specificity by setting | **Competitive disarmament** — a range next to competitors' point estimates reads as worse |
| 89 | Publish live birth rate by age | **No benchmark** — an honest number alone has nothing to be read against |
| **90** | **Publish outcome evidence** | **The evidence creates the obligation** |

Day 90's mechanism is the strongest of the four, and it is genuinely different from the other three.

P1 decays **99.00%** — the largest decay in the series. The constraint is not cost, not competition, and not the absence of a benchmark. It is that **the act of producing the evidence changes the product's regulatory status.**

[L1] already established that these systems produce device-like clinical decision support output. What converts "device-like output" into "device" is, substantially, a demonstrated intended use. A randomised trial showing that a system improves a health outcome is the most persuasive possible demonstration that the system is intended to, and does, perform a medical function.

> **The evidence and the regulation arrive together.** You cannot publish the proof that it works without publishing the proof that it is the kind of thing that needs approval to work.

And that explains, with no appeal to bad faith, the single most striking feature of this literature: **benchmark scores are published enthusiastically and outcome trials are not.** A benchmark measures capability. An outcome trial measures clinical effect. Only one of them is evidence of intended use.

`verify.py` records this as `this_is_why_benchmarks_are_published_and_trials_are_not`.

---

## 43. MoSCoW

| | Item | Rationale |
|---|---|---|
| **Must** | Label the health-answer surface (P2) | Highest stressed score; cheap; addresses [L1] directly |
| **Must** | Never report a proxy as an outcome | Costs nothing; §32's guardrail |
| **Should** | Publish harms and refusal rates (P4) | Survives stress; genuinely unclaimed |
| **Should** | Device pathway for one indication (P3) | Converts capability into evidence; would be first |
| **Could** | Outcome evidence (P1) | Correct on the merits; §36 explains the cost |
| **Won't** | Claim clinical validation without a trial | The thing this series exists to argue against |

---

## 44. Kano

| Feature | Category | Reasoning |
|---|---|---|
| Fluent, immediate answers | **Must-be** | Table stakes; absence is disqualifying |
| Benchmark accuracy | **Performance** | More is better; comparable across vendors |
| Escalation on urgent presentations | **Must-be, unverified** | Users assume it; nobody publishes the rate |
| Published outcome evidence | **Attractive** | Nobody has it; first mover defines the category |
| Harm disclosure | **Indifferent → Attractive** | Users do not yet expect it |
| Calibrated confidence | **Attractive** | [L2] shows why it matters; not yet demanded |

Row 3 is the dangerous one. **Users assume escalation works because it is a Must-be in their mental model, and no published rate exists.** That is the widest gap in the table between expectation and evidence.

---

## 45. Roadmap

**Horizon 1 — immediate**
- Label the health-answer surface (P2).
- Adopt the no-proxy-as-outcome guardrail internally and state it publicly.

**Horizon 2 — within four quarters**
- Publish escalation rates on urgent presentations and a harm taxonomy (P4).
- Publish calibration data: does stated confidence track measured correctness?
- Fund independent replication of [L2]'s learned-dependency finding.

**Horizon 3 — conditional**
- Device pathway for one bounded indication (P3).
- Outcome trial (P1) — **conditional on the regulatory posture in §36 being resolved**, or pursued deliberately as the price of entering the regulated category.

Horizon 3's conditionality is the honest output of §36, not a hedge.

---

## 46. Risks

| Risk | Basis | Severity |
|---|---|---|
| **Learned dependency degrades calibration** | [L2], replicated across 901 participants | **High** |
| **Device-like output without a device framework** | [L1] | **High** |
| **Proxy evidence read as outcome evidence** | §21–§24 | **High** |
| **Literature over-read** | 50.00% false positives in the RCT sample | **High** |
| **No escalation rate published** | §38 row 3 | **High** |
| **Regulatory arrival** | [L1] argues for it in a journal | **Moderate** |

Row 4 deserves emphasis because it is a risk to *everyone reading this field*, not to the vendor. If half the RCT-tagged records are false positives, then every systematic review counting them is inflated — and there are **1.92** reviews per trial.

---

## 47. Open Questions

1. Does using a conversational AI for health questions change any health outcome, in either direction? **Unknown.**
2. What fraction of urgent presentations are correctly escalated? **Unpublished.**
3. Does expressed confidence track correctness? **Unpublished.**
4. Does [L2]'s dependency effect hold in people with real health concerns rather than experimental participants?
5. What is the true count of genuine LLM health RCTs? My sample says roughly **110**; only a full screen would settle it.
6. If an outcome trial were published, would classification follow? §36 argues yes. It is an argument, not a measurement.
7. How many of the **422** systematic reviews include false-positive primary studies?

Question 7 is the one I would most want answered, and it is the easiest of the seven to answer.

---

## 48. What Would Actually Fix This

Four interventions, ordered by who has to act.

| # | Intervention | Who acts | Precedent | Fixes |
|---|---|---|---|---|
| 1 | **Fund outcome trials for general-purpose health use** | Public research funders | Day 88's TB literature | Ledger rows 2 and 3 |
| 2 | **Tag LLM-based functionality in the device list** | FDA | Already stated as intent [FL] | §17's invisibility |
| 3 | **Require harms and escalation rates beside any capability claim** | Regulator or standards body | Nowhere yet | Ledger row 3 |
| 4 | **Independent benchmark authorship** | Standards body, academia | Nowhere yet | §18's problem |

Intervention 1 is the load-bearing one, and it is the direct descendant of Day 89's conclusion.

Day 89 found that no fertility clinic publishes an honest outcome rate because the regulator publishes no benchmark — **a benchmark is a public good, and one seller cannot build one.** The same logic applies here with an extra turn: §42 shows that a vendor publishing an outcome trial does not merely bear a competitive cost, it invites regulatory classification.

**So the evidence will not come from vendors, for structural reasons, and it will not come from a regulator that has no jurisdiction.** It has to come from the same place Day 88's best evidence came from: people with a non-commercial reason to measure, and funding to do it.

Intervention 2 is already half-done — FDA has said it will explore methods to identify LLM-based devices [FL]. Saying it and doing it are different, and until it is done, §17's invisibility stands.

---

## 49. Method Notes

**What was done.** Regulatory nulls came from four openFDA endpoints with two positive controls. The securities check used SEC EDGAR company search. The device-list finding came from FDA's own page. All literature counts and all ten sampled studies came from PubMed.

**The positive controls are the methodological point of the day.** §15 explains why. A null without a control is not a finding.

**The sample is small and not random.** Ten of 220, taken from the most recent results. Part 1 of `ASSUMPTIONS.md` treats this fully. It is enough to establish that false positives are **common** and that the headline is a **ceiling**; it is not enough to estimate the false-positive rate precisely, and the README says "roughly half", never "exactly 50%", when generalising.

**What was deliberately not done.** No model was asked a health question. No answer was scored. No vendor benchmark is quoted. §61 says what that cost.

**The gate passed on the first run** — zero failures, the second consecutive day with no hand-stated errors. As on Day 89, this reflects the arithmetic being mostly ratios of small integers rather than any improvement in care.

**Diagram standard.** Markdown tables and ASCII only. Mermaid was dropped at Day 50 and never returned.

---

## 50. Limitations

- **Ten of 220 is a small sample**, non-random, and from one date.
- **The PubMed queries are broad.** Term expansion is what produced the false positives; the exact queries are in `ASSUMPTIONS.md`.
- **No model was tested.** Nothing here bears on any system's accuracy.
- **No usage data.** How many people use these systems for health questions is not established here, and no figure is asserted.
- **Vendor benchmarks exist and are excluded**, which makes the evidence picture look thinner than a vendor would present it — deliberately, and §61 explains the trade.
- **"Zero authorisations" is as of 2026-09-28** and across the endpoints queried.
- **Point-in-time.** A fast-moving field; every count is a snapshot.

---

## 51. Anyone Can Check This

```bash
# The regulatory null, with its positive controls
for q in openai qure.ai Verily; do
  curl -sS "https://api.fda.gov/device/510k.json?search=applicant:%22$q%22&limit=1"
done

# The literature counts (PubMed E-utilities)
curl -sS "https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esearch.fcgi?db=pubmed&retmode=json\
&term=(%22large+language+model%22+OR+ChatGPT)+AND+(medical+OR+health+OR+clinical)"
```

The gate and cross-check in this folder reproduce every number above from these inputs and the cited literature.

---

## 52. Verification

`verify.py` — **180 checks, all passing**, written and passing before the first sentence of this README existed.

`crosscheck.py` confirms every two- and three-decimal figure in `README.md` and `ASSUMPTIONS.md` traces to a value asserted in the gate.

---

## 53. Twelve Negative Controls

Asserted **False** in the gate so no sentence can quietly imply them:

`chatgpt_is_a_medical_device` · `chatgpt_is_authorised_for_any_clinical_indication` · `this_case_study_measures_chatgpt_accuracy` · `this_case_study_tested_any_model` · `any_vendor_benchmark_score_is_asserted_here` · `usage_figures_for_health_questions_are_known` · `openai_financials_known` · `the_220_rcts_were_all_read` · `the_sample_is_statistically_representative` · `fda_has_stated_no_device_contains_an_llm` · `day90_uses_mermaid` · `day90_fabricates_any_figure`

The eighth and ninth are the ones that keep §21 honest. I read ten studies, not 220, and ten is not a representative sample. The tenth is the subtlest: FDA has not said that no authorised device contains a language model — it has said it will explore methods to identify them, which is a different and stranger statement.

---

## 54. What a PM Should Take From This

**1. A null needs a positive control.** "The search returned nothing" and "there is nothing" are different claims, and only one of them is a finding. Run the query against something you know exists first. This is Evidence Standard 7, and it took this series eighty-nine days to write it down.

**2. Read the sources; do not count the matches.** Half the trials in my sample were not about the technology at all. Every single day in this arc that produced a real finding produced it by reading something a pattern match had mislabelled.

**3. Ask what a proxy replaced.** Exam scores, click-through, intention, engagement, benchmark accuracy — each is a real measurement of something easier than the thing you care about. The question is never "is this metric true." It is **"what did it replace, and who chose the replacement."**

**4. Volume is not evidence.** 21,033 papers, **1.92** systematic reviews per randomised trial, and roughly **1 genuine outcome-adjacent trial per 191 papers**. A field can be enormous, fast-growing, serious, and still not have measured the thing.

**5. Notice when the evidence and the obligation arrive together.** §36's mechanism generalises well beyond health: in any regulated category, proving your product works can be the act that brings it into scope. When you see a market publishing capability metrics and avoiding effectiveness metrics, this is usually why — and it is a structural explanation, not an accusation.

---

## 55. If You Are Building In This Category

Seven checks, drawn from all ninety days.

1. **Which regulator, if any, defines your evidence obligations?** The answer determines what you will publish, whether you intend it or not.
2. **Is your user in the role list?** Day 89's registry had four login roles and the patient was not one.
3. **How many parties stand between the thing measured and the number published?** One is a vendor benchmark. Two is a cleared device.
4. **What did your headline metric replace?** Every proxy is a substitution, and the substitution was a decision.
5. **Can your buyer learn from repeat purchase?** If not, asymmetry is the equilibrium, not a friction to be designed away.
6. **Would your best number survive being printed beside a competitor's best number?** If not, you need a benchmark, not a disclosure policy.
7. **Does producing the evidence change your regulatory status?** If yes, expect capability metrics and no effectiveness metrics — and expect that to be structural, not cynical.

---

## 56. Ninety Days

This series began as a daily discipline and turned into an argument. Here is the argument, and the numbers that carried it.

| Day | Subject | Headline finding |
|---|---|---|
| 83 | OpenEvidence | **0 of 5** headline claims independently confirmed |
| 84 | Abridge | Vendor's own peer-reviewed studies reported **0** accuracy metrics |
| 85 | Eka Care | National proxy and field study converged to **1.59 pp** |
| 86 | Hippocratic AI | Safety claim rested on **0.27%** evidence coverage |
| 87 | Tempus AI | **66** SEC staff comments; **0** algorithm metrics; **73.81%** self-authored |
| 88 | Qure.ai | **5 of 9** clearances with accuracy; **76.47%** independent literature; **44.44%** of summaries self-contradictory |
| 89 | Gaudium IVF | **51** outcome measures across **53** clinics; **1 of 79** mentioning harms; **0** public registry routes |
| 90 | Health in ChatGPT | **0** authorisations; **1.05%** RCTs; **0 of 10** measuring an outcome |

**Zero was the most common finding in ninety days.** Seven separate headline figures in this arc are exactly zero, and `verify.py` asserts all of them.

---

## 57. What Ninety Days Established

**Obligation beats choice — and the kind of obligation determines the kind of evidence.** Securities regulation produced an elegant description of *process* with no result in it. Device regulation produced sensitivity and specificity, from one population. Health-service regulation produced a complete national outcome database nobody can open. No obligation at all produced 21,033 papers measuring examinations.

**Every regime works. None was built for the reader.** Not one of the four compels a measurement of whether the person at the end is better off. That is not a failure of any individual regulator — each did its job. It is that the reader's question was nobody's job.

**The best evidence often belongs to nobody.** Day 88's most useful facts came from researchers in Dhaka, Cape Town and Lima who measured a product because they wanted to know — **76.47%** of that literature has no vendor author. Day 89 had no such teams, and the gap stayed open.

**Honest disclosure is structurally punished.** Four times, in four industries, the cheapest and most obviously correct recommendation ranked first on base RICE and last under its binding constraint. Legal exposure, competitive disarmament, missing benchmark, regulatory scope. Four different mechanisms, one outcome. **The property that makes a disclosure valuable to the reader is reliably the property that makes it costly to the publisher.**

**And the method mattered more than any single finding.** Writing the verification gate before the prose caught a wrong crossover year, two CAGRs, a confidence interval that could not exist, a comment count inflated by note captions, a sensitivity mention that was about radiography, and — on the last day — a headline that was double the truth.

---

## 58. The Rule That Survived Ninety Days

If the series reduces to one line, it is this:

> **Ask what force produced the number in front of you.**

Not whether it is true — most of these numbers were true. Tempus's "over 800 peer-reviewed articles" is true. Qure.ai's 96.36% specificity is true. A fertility clinic's pregnancy rate per transfer is true. "1.05% of the literature is randomised trials" is true.

Every one of them is also **the answer to a question somebody else chose**, shaped by a regulator's remit, a competitor's convention, or a publisher's interest. The number arrives with a history, and the history is usually more informative than the number.

Three questions that follow from it, and they work on any metric in any industry:

1. **What made them say this?** A rule, a reviewer, a competitor, or a choice?
2. **What did this replace?** Every metric stands in for something harder to measure.
3. **What happens when that force is removed?** Day 87 answered it exactly: the number left the filing the year the reviewer stopped reading.

---

## 59. How Each Case Study Was Built

The method, stated once, because it is the part most reusable by anyone else.

1. **Verify the repository state.** Every session began by confirming what was already published, so a day's work could not silently overwrite or duplicate.
2. **Find the primary source before forming a thesis.** SEC EDGAR, openFDA, GLEIF, CourtListener, government portals, PubMed. Never a press release.
3. **Write the verification gate before the prose.** Every derived figure computed from unrounded inputs and asserted against an expected value. If the gate disagreed, the machine was right.
4. **Include negative controls.** Assert as **False** the things a careless reading would imply, so a later edit cannot smuggle them in.
5. **Write the case study against the gate.**
6. **Cross-check every figure.** A second script extracts every decimal in the prose and confirms it traces to a gate value. Source-precision figures are allow-listed with their source; derived figures never are.
7. **Record what could not be reached.** Day 89's inability to read the ART Act is stated in the README, the assumptions, and the gate.

Steps 3, 4 and 6 are the ones that did the work. **A gate written after the prose verifies the prose.** A gate written first makes the prose survive it — and on Days 82, 86, 87 and 88 it caught hand-stated errors, every one of them the same rounded-intermediate trap.

---

## 60. What I Got Wrong

A series that spent ninety days on other people's evidence owes an account of its own.

**Hand-stated figures the gate rejected.** Day 82: eight, including two rounded-intermediate errors. Day 86: one RICE score. Day 87: seven, including a crossover year misread from adjacent table columns, two CAGRs estimated rather than computed, and a ratio that moved by 3.23 from a single premature rounding. Day 88: two, both the same trap. **In every case the machine was right and the human was wrong.**

**A claim that was too broad.** Day 88 concluded that "India's statutory company classification has no code for medical AI." Day 89 found Gaudium registered under NIC **85100, Hospital activities**, and had to narrow it: the register has health codes and classifies by *activity*, which is why software companies fall to the residual class. The original claim was not false but it was wider than the evidence.

**A methodological standard that arrived eighty-nine days late.** §15's rule — a null requires a positive control — should have been Evidence Standard 1, not 7. Until today, "the search returned nothing" was treated as "there is nothing," and Day 88 came close to asserting seven FDA clearances instead of nine because two fetches failed silently.

**A headline that was double the truth — caught on the last day, in this case study.** 220 RCT-tagged records became roughly **110** once ten were read. Had I not read them, Day 90 would have published a number **2.00×** too generous, in a case study about people publishing numbers that are too generous.

That last one is the appropriate note to end the method on. **The discipline is not that it prevents errors. It is that it catches them before publication — including in the document arguing that everyone else should catch theirs.**

---

## 61. What This Series Deliberately Did Not Do

Stated plainly, because a method's costs belong next to its results.

**No vendor communications.** No press releases, model cards, benchmark announcements, funding news, or marketing. This kept the tier structure clean and made every evidence picture look thinner than a vendor would present it. That was the trade: comparability across ninety days, at the cost of completeness on any one day.

**No primary testing.** This series never ran a model, scored an answer, audited a clinic, or surveyed a user. It examined records. Everything here is about what the public record contains.

**No accusations.** Day 89 added the rule explicitly — a named company is a specimen, not a defendant — and Days 88 and 90 carry negative controls enforcing it. Where behaviour looked bad, the case studies asked what structure produced it, and generally found one.

**One researcher, ninety days, no peer review.** Every case study was produced in a single session, verified programmatically, and published without anyone checking it. The gates catch arithmetic. They do not catch a wrong framing, a missed source, or a misread statute — and Day 89's inability to reach the ART Act text is the clearest example of a limitation a gate cannot fix.

---

## 62. The Numbers That Mattered Most

| | |
|---|---:|
| Papers on LLMs and health | **21,033** |
| Of those, randomised trials | **220 — 1.05%** |
| Systematic reviews per trial | **1.92** |
| Trials sampled and read | **10** |
| False positives among them | **5 — 50.00%** |
| **Measuring a patient health outcome** | **0 — 0.00%** |
| Adjusted genuine trials | **~110 — 0.52%** |
| One genuine trial per | **191.21 papers** |
| FDA endpoints queried | **4** |
| Authorisations found | **0** |
| Positive controls confirming the method | **2** |
| Regulatory regimes compelling clinical evidence | **0** |
| Regimes across the arc compelling an outcome measure | **0 of 4** |

---

## 63. References

**Regulatory and registry sources**, retrieved 2026-09-28.

1. **[F]** openFDA device API. `https://api.fda.gov/device/510k.json`, `/pma.json`, `/classification.json`, `/registrationlisting.json`
2. **[FL]** US Food and Drug Administration. *Artificial Intelligence-Enabled Medical Devices.* `https://www.fda.gov/medical-devices/software-medical-device-samd/artificial-intelligence-enabled-medical-devices`
3. **[S]** US Securities and Exchange Commission. EDGAR company search. `https://www.sec.gov/cgi-bin/browse-edgar`

**Peer-reviewed literature.** According to PubMed:

4. **[L1]** Weissman GE, Mankowitz T, Kanter GP. Unregulated large language models produce medical device-like output. *npj Digital Medicine* 2025;8(1):148. PMID 40055537. DOI [10.1038/s41746-025-01544-y](https://doi.org/10.1038/s41746-025-01544-y)
5. **[L2]** Ahmed A, Leroy G, Sachdeva A, Harber P, Rains S, Youn S, Barai P. Trust in Generative AI for Health Information Consumption and the Effect of Learned Dependency: Randomized Controlled Experimental Study. *J Med Internet Res* 2026;28:e98326. PMID 42747973. DOI [10.2196/98326](https://doi.org/10.2196/98326)
6. **[L3]** Yang W, Xu T, Wei J, Zheng W, Yan W, Wang J, Chu G, Niu H. Effectiveness of ChatGPT and DeepSeek in Urology Medical Education: Randomized Controlled Trial. *J Med Internet Res* 2026;28:e89315. PMID 42766393. DOI [10.2196/89315](https://doi.org/10.2196/89315)
7. **[L4]** He H, Yao S, Ruiz M, Paro FR, Zhang W, Chu H. AI Health message intervention: The role of message customization and message source in breast cancer screening among women of color. *Patient Educ Couns* 2026;152:109807. PMID 42537382. DOI [10.1016/j.pec.2026.109807](https://doi.org/10.1016/j.pec.2026.109807)
8. **[L5]** Borckardt JJ, Henninger-Borckardt D, Barth K, et al. Knowledge Acquisition, Case Discussion, and Engagement in Health Professional Students Using Interactive Virtual Patient Cases Versus Written Case Studies: Randomized Controlled Trial. *JMIR Nurs* 2026;9:e98700. PMID 42777164. DOI [10.2196/98700](https://doi.org/10.2196/98700)
9. **[L6]** Kumar A, Stinson K, Wang L, et al. Using randomization to compare AI and expert-generated formative assessment questions in medical education. *Med Educ Online* 2026;31(1):2671586. PMID 42106900. DOI [10.1080/10872981.2026.2671586](https://doi.org/10.1080/10872981.2026.2671586)

Literature identified via PubMed.

**Assumptions, source conflicts, and limitations:** see `ASSUMPTIONS.md`.

---

## 64. A Note on Fairness

Day 89 added a rule: a named company is a specimen, not a defendant. The finale needs it more than any previous day, because the subject is a category rather than a filing.

**What this case study does not claim.** That any system gives bad health answers. That anyone broke a rule. That any vendor withheld evidence it was obliged to produce. `verify.py` asserts `this_case_study_measures_chatgpt_accuracy` and `this_case_study_tested_any_model` as **False**, and `any_vendor_benchmark_score_is_asserted_here` as **False**.

**What it does claim.** That no regulatory regime compels clinical evidence here — established across four FDA endpoints with two positive controls, corroborated independently by [L1]. That the literature is enormous and overwhelmingly measures proxies. That roughly half the trials tagged as randomised in this area are not about language models at all.

**Why the structural reading is the right one.** §36 shows that a vendor publishing an outcome trial invites device classification, and §28 shows that no regulator in this series compels an outcome measure from anyone. A vendor publishing capability metrics and not effectiveness metrics is responding rationally to that structure. Reading it as evasion would be both unfair and, more importantly, **wrong about the cause** — and a wrong cause produces a useless recommendation.

The same reasoning held on Day 88, where **44.44%** of cleared FDA summaries contradicted themselves and the finding was about review processes rather than about the manufacturer, and on Day 89, where a clinic publishing no success rate was behaving exactly as **0 of 161** Brazilian clinics did.

**Blaming individual actors for a structural outcome is how thirty years of "be more transparent" produced a fertility market where one website in seventy-nine mentions what can go wrong.**

---

## 65. Closing Note

Ninety days ago this started as a way to build a portfolio. It became an argument about evidence, and the argument turned out to be simpler than expected.

Every regulator in this series did its job. The SEC made a company disclose a conflict of interest it would rather not have printed, and did it in one sentence in 2021. The FDA made a company publish sensitivity, specificity and the counts behind them for five separate devices. India's ART authority built a national database of fertility outcomes that genuinely exists and is genuinely complete.

And a person with a health question, at the end of all of it, has: a benchmark score somebody's marketing team commissioned, a clinic website that says "unequalled success rates", a specificity figure measured on a population unlike theirs, and a fluent, immediate, free answer from a system that no one has ever been required to prove works.

Not one of those four was produced by anybody asking what that person needed to know.

That is not a story about bad companies or lazy regulators. It is a story about **whose question gets designed for** — and in ninety days of looking, the answer was almost never the person at the end of the chain.

Which is, in the end, a product management problem. Somebody has to decide who the user is. In every system examined here, somebody did, and it wasn't them.

---

*Day 90 of 90. The series is complete. Written by Gaurav Singh. Sources are primary and cited. Figures are computed, not asserted. Where the record is silent, this document says so — and where a source could not be reached, it says that too.*
