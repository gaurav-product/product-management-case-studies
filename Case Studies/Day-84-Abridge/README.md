# Day 84 — Abridge AI, Inc. (private)

### The evidence exists. The vendor didn't produce it.

> **90-Day PM Case Study Challenge — Day 84**
> Evidence-based product teardown built only from primary sources.
> Every derived figure is produced by `verify.py` (198 programmatic checks) before a word of prose was written.

---

## 1. One-paragraph summary

For four days this series has asked the same question of healthcare AI companies and got the same answer: nobody publishes an outcome metric. Day 82 named the specific metric missing for ambient clinical documentation — whether the generated note is good enough to sign — and Day 84's company is the one whose entire product is that note. The finding is not what the previous four days predicted. **That metric now exists.** A 24-week, pre-registered, stepped-wedge randomized trial at the University of Wisconsin, funded by the health system and an NIH award rather than by the vendor, named Abridge explicitly and scored **7,966** randomly sampled notes **in their unedited form** on a validated documentation-quality instrument. It also produced a number-needed-to-treat of **1.68** for reducing clinician burnout. Abridge's own peer-reviewed studies — and it has two, more than Days 80–83 combined — measure clinician satisfaction and cognitive load. **Zero** vendor-linked studies report note accuracy; **one** independent trial does. The evidence a buyer needs exists. It was produced by academics, on someone else's money, and the vendor has never published it.

---

## 2. Why this is the most positive case study in the arc — and still a critique

Days 80 through 83 found an absence. This one finds evidence, and the analysis has to change shape accordingly.

**What is genuinely good here:**

- An independent randomized controlled trial names the product and measures the outcome.
- Abridge has two peer-reviewed publications, one of them a randomized crossover design.
- The company published a detailed technical whitepaper on hallucination detection with a stated methodology, a defined taxonomy and a named comparator.
- The trial reported a **99.92%** patient consent rate, with only **22** patients declining recording.

**What the critique narrows to:**

- Both vendor-linked studies measure the **clinician's experience**, not the **note's correctness**.
- The metric that matters was produced by people the vendor did not pay, and the vendor does not publish it.
- The strongest independent head-to-head trial **anonymises the products**, so a buyer cannot act on it.
- The literature flags a speech-recognition equity problem that the validating trial's population could not detect.

This is what progress looks like partway through. The finding is not that Abridge is behind its peers on evidence — it is clearly ahead. The finding is about **who is doing the measuring, and why that matters when the measurement stops being free.**

---

## 3. Company identification

| Field | Value | Source |
|---|---|---|
| Legal name | Abridge AI, Inc. | Federal docket; NEJM AI trial |
| Status | **Private** — no public filings | — |
| Founded | 2018 | Secondary reporting |
| Founder / CEO | Dr. Shiv Rao (cardiologist) | Secondary reporting |
| Headquarters | Pittsburgh, Pennsylvania | Secondary reporting |
| Product | Ambient clinical documentation — passively records the clinical conversation and drafts the visit note | NEJM AI trial |
| Distribution | Embedded in Epic via private and FHIR R4 APIs | NEJM AI trial |
| Scope claimed | 150+ health systems, 55 specialties, 28 languages | Company, June 2025 |

### 3.1 The register note, again absent

As on Day 83, there is no SIC or NIC code to examine, because a private company produces no such registration. Three of the last five case studies have had no register classification at all. The running tally of register misclassification across this series — **11 of 84** companies examined — is now measuring a shrinking denominator, because the most consequential AI companies in healthcare increasingly do not appear in any register until they exit.

---

## 4. What Abridge actually does

A clinician opens the app on a phone, the patient consents, the conversation is recorded, and a draft visit note appears in the EHR for the clinician to review and sign.

That is the whole product, and its simplicity is the point. The NEJM AI trial describes it precisely: the software was **documentation-only and provided no diagnostic or therapeutic decision support.** Automatic speech recognition plus natural language generation, producing transcripts and drafts.

### 4.1 Why that scope limitation matters enormously

Day 83's OpenEvidence answers clinical questions — it sits inside the clinical reasoning loop, which is why a **23.00%** answer-discordance finding there was so serious. Abridge does not answer questions. It writes down what was said.

That is a far narrower blast radius. A documentation tool that makes an error produces a wrong record; a decision-support tool that makes an error produces a wrong decision. Both matter, and the first is genuinely less dangerous.

**But it is not harmless**, and the reason is the one thing a documentation product uniquely controls: the note *becomes* the record. Downstream coding, billing, quality measurement, malpractice defence, and the next clinician's understanding of the patient all run off it. An omission in a note is invisible in a way an error in an answer is not — nobody sees what was left out.

That is why the trial's **thoroughness** score (major omissions) at **4.57** and its **abstraction** score at **3.97** are more interesting than the headline satisfaction numbers.

---

## 5. Problem statement

The problem is unusually well evidenced, and the trial states it with a number: practitioners spend **1–2 hours documenting after hours for every hour** spent face-to-face with patients.

Documentation burden is a leading, measurable, and repeatedly replicated driver of clinician burnout. Unlike most product problems this series examines, this one has a peer-reviewed literature behind it that predates the product category by a decade.

So the question is not whether the problem is real. It is whether the fix works, and at what cost to the record.

---

## 6. The trial that changes the arc

**Afshar et al., NEJM AI, 2025.** A 24-week, stepped-wedge, individually randomized pragmatic clinical trial across ambulatory clinics in two U.S. states and eight specialties.

| Design feature | Value |
|---|---|
| Practitioners randomized | **66** |
| Waves | **3**, of 6 weeks each |
| Duration | **24 weeks** |
| Registration | **NCT06517082**, registered 9 Aug 2024, before enrolment |
| Funding | University of Wisconsin Hospitals and Clinics; NIH CTSA |
| Vendor funded? | **No** |
| Product named? | **Yes — Abridge AI, Inc.** |
| Peer reviewed? | **Yes** |

```
nejm_funded_by_vendor        = False
nejm_names_the_product       = True
nejm_prospectively_registered = True
```

Statistical analysis plan, analysis code and participant survey data were posted publicly before analysis. That is a higher standard of methodological transparency than anything else in this five-day arc, and it was met by academics rather than by any of the five companies.

### 6.1 Scale

| Measure | Value |
|---|---|
| Total notes authored during the trial | **71,487** |
| Notes generated with ambient AI | **27,092** (**37.90%**) |
| Notes authored by humans only | **44,395** (**62.10%**) |
| Note-weighted mean utilisation | **71.00%** (SD 31.6) |
| Survey completion | **99.70%** (n = 329) |

---

## 7. What the trial found about the clinician

### 7.1 The co-primary outcomes split

| Outcome | Effect | 95% CI | Verdict |
|---|---|---|---|
| Work exhaustion / interpersonal disengagement | **−0.44** points | −0.62 to −0.25 | **Significant** (P<0.001) |
| Professional fulfillment | **+0.14** points | 0.004 to 0.28 | **Not significant** (P=0.04) |

```
nejm_fulfilment_significant = False
```

The fulfillment result is worth pausing on, because it is easy to misreport. P=0.04 looks significant by the usual convention — but this trial had **two** co-primary outcomes and correctly split its type-I error, allocating **0.025** to each. Against that threshold, 0.04 does not clear the bar, and the paper says so plainly: *"a nonsignificant increase in professional fulfillment."*

The effect on exhaustion was **3.14×** the size of the effect on fulfillment.

### 7.2 The distinction that matters for product strategy

The authors' own interpretation is the sharpest sentence in the paper: the result *"may reflect relief from negative affect (burnout) through documentation efficiencies without corresponding gains in positive affect (fulfillment), which may be influenced by broader organizational factors, such as staffing levels, professional autonomy, and team climate."*

**Ambient AI removed something bad. It did not add something good.**

That is a precise and useful finding for any product leader selling into clinician burnout. The category's pitch is usually "give clinicians their joy back." The best evidence says it takes away a specific misery, and that joy depends on staffing, autonomy and team climate — none of which a scribe touches.

### 7.3 Number needed to treat

| Measure | Value |
|---|---|
| **NNT** | **1.68** (95% CI 1.55–1.82) |
| Absolute risk reduction | **0.60** |
| Above the burnout threshold at baseline | 56.1% |
| Above it at study end | 35.4% |
| Absolute change | **−20.70pp** |
| Relative reduction | **36.90%** |

An NNT of **1.68** is a remarkable number in any clinical context — it means roughly every second practitioner given the tool experienced the defined improvement. For comparison, most pharmaceutical interventions celebrated in clinical practice have NNTs in the tens.

That deserves to be said clearly, because the rest of this document is more critical: **on burnout, this is strong evidence of a real effect.**

### 7.4 And the fulfillment threshold moved anyway

| Measure | Value |
|---|---|
| Above the high-fulfillment threshold at baseline | 25.8% |
| At study end | 41.5% |
| Absolute change | **+15.70pp** |
| Relative increase | **60.85%** |

The continuous fulfillment measure was not significant; the proportion crossing the clinically meaningful threshold rose **60.85%**. Both are true. The honest reading is that the fulfillment signal is real but weaker and less certain than the exhaustion signal — which is exactly what the co-primary analysis concluded.

---

## 8. What the trial found about the clock

| Measure | Effect | 95% CI | Survives sensitivity analysis? |
|---|---|---|---|
| Time spent on notes | **−0.36 h/day** (**−21.90 min**) | −0.55 to −0.17 | **Yes** |
| Work outside work | **−0.50 h/day** (**−30.00 min**) | −0.90 to −0.09 | **No** |

```
nejm_note_time_survives_trimming = True
nejm_wow_survives_trimming       = False
```

### 8.1 The after-hours result does not hold

This is the most important caveat in the trial and the one most likely to be dropped in summary.

Work outside work fell by half an hour a day — a headline result, and exactly what the category promises. But excluding the top **3%** of daily observations, the effect attenuates to **−0.19 h** (95% CI −0.40 to 0.03) and is **no longer significant**.

| Measure | Value |
|---|---|
| Attenuation after trimming | **62.00%** |

The authors are explicit that the effect *"was likely concentrated among a small subset with extreme after-hours burden."*

**So the tool helped the most overloaded clinicians substantially, and the typical clinician's evening did not measurably change.** Time spent on notes during the day fell consistently across every sensitivity analysis; the pajama time did not.

For a product manager this is the difference between two very different value propositions. "This gives everyone their evenings back" is not supported. "This rescues the people drowning worst" is.

---

## 9. The metric Day 82 asked for

Day 82 ended by proposing a specific disclosure: the percentage of AI-generated notes signed without material edit. It argued that a company selling an ambient scribe should publish whether the note is good enough to sign, and that none did.

This trial measured note quality directly, using the **Provider Documentation Summarization Quality Instrument 9 (PDSQI-9)**, a validated instrument, on **7,966** randomly sampled notes, **scored in their unedited form before practitioner review**.

```
day82_requested_metric_now_exists            = True
day82_requested_metric_published_by_vendor   = False
pdsqi_notes_scored_unedited                  = True
```

### 9.1 The results

| Domain | What it measures | Score (of 5) | SD |
|---|---|---|---|
| **Comprehensibility** | Can it be understood | **4.99** | 0.13 |
| **Organisation** | Is it well structured | **4.90** | 0.16 |
| **Usefulness** | Helpful for specialty decision-making | **4.83** | 0.51 |
| **Succinctness** | Appropriately concise | **4.63** | 0.55 |
| **Thoroughness** | Major omissions | **4.57** | 0.68 |
| **Accuracy** | Extraction fidelity; falsification / fabrication | **4.44** | 0.93 |
| **Abstraction** | Synthesis across data elements | **3.97** | 0.58 |

| Measure | Value |
|---|---|
| Mean across domains | **4.62** |
| Range | **1.02** |
| Lowest domain | **abstraction** |
| Highest domain | **comprehensibility** |
| Accuracy as a share of scale | **88.80%** |
| Abstraction as a share of scale | **79.40%** |
| Notes containing stigmatising language | 12 (**0.15%**) |

### 9.2 The shape of the result is the finding

Group the domains by what they actually test.

| Group | Domains | Mean |
|---|---|---|
| **Language** | organisation, comprehensibility, succinctness | **4.84** |
| **Substance** | accuracy, thoroughness, abstraction | **4.33** |
| **Gap** | | **0.51** |

```
pdsqi_language_scores_above_substance = True
```

**The notes read better than they think.** Every language quality scores above every substance quality. The model is excellent at producing a well-organised, comprehensible, appropriately concise clinical document, and measurably less good at getting the facts complete and synthesising them.

The lowest score of all — **3.97**, abstraction — is the domain that requires clinical reasoning rather than transcription. That is exactly where you would predict a speech-to-text-plus-generation system to be weakest, and the data agrees.

For a clinician deciding how carefully to read a draft, this ordering is the single most useful thing in the trial: **the note will look finished before it is correct.** Fluency is not a signal of accuracy here, and a well-written note is precisely the kind a busy reviewer signs.

### 9.3 The caveat that must travel with these numbers

```
pdsqi_scored_by_llm_judge              = True
pdsqi_scored_directly_by_physicians    = False
pdsqi_judge_validated_against_physicians = True
```

The PDSQI-9 scoring used **an LLM-as-a-judge implementation**, validated against physician ratings across multiple note-generation tasks — not physicians scoring notes directly.

That is a defensible methodological choice at a sample of 7,966 notes, and the authors validated the judge properly, which is the right thing to do. But it must be stated: **this is an AI grading an AI's notes.** Whether a language model is a reliable judge of the subtle failure it is itself most prone to — a fluent, well-organised note that quietly omits something — is not established by validating it on average agreement.

The accuracy domain also carries the largest standard deviation of any domain (**0.93**), more than seven times the SD on comprehensibility. The mean is good; the variance is where the risk lives.

---

## 10. The second trial, and why a buyer cannot use it

**Chowdhury et al., JAMIA, 2026.** An open-label randomized crossover trial at a tertiary academic medical centre, comparing **two** ambient AI scribes head to head.

| Measure | Value |
|---|---|
| Clinicians randomized | **160** |
| Surveys analysed | **136** (**85.00%**) |
| Satisfaction improvement, product A | +1.91 (7-point scale) |
| Satisfaction improvement, product B | +2.51 |
| **Difference** | **0.60** (95% CI 0.32–0.90) — **8.57%** of the scale |
| Minutes in notes per day, B versus A | **−3.19** (95% CI −4.87 to −1.50) |
| Burnout difference between tools | **Not meaningful** |
| Pajama time difference | **Not meaningful** |

### 10.1 The products are anonymised

```
jamia_products_named        = False
jamia_actionable_for_a_buyer = False
```

This is a properly designed, adequately powered, peer-reviewed head-to-head randomized trial of two ambient scribes — the exact study a health system CIO would want before spending millions — and **it does not say which products it compared.**

A buyer reading it learns that one unnamed product beat another unnamed product by 0.60 points of satisfaction and 3.19 minutes a day. That is unactionable.

There are legitimate reasons a trial anonymises commercial products — contractual constraints, institutional caution, a desire to avoid the paper being used as marketing. But the effect is that the most decision-relevant independent evidence in the category is deliberately stripped of the one detail that would make it decision-relevant.

A third trial cited within the Wisconsin paper, by Lukac et al., **did** name its products: Microsoft DAX and Nabla, with a significant note-time reduction for Nabla and not for DAX (**41** versus **18** seconds).

```
independent_trial_count  = 3
trials_naming_products   = 2
trials_naming_share_pct  = 66.67
```

Two of three name their products. Practice is inconsistent, and the inconsistency is not in the buyer's favour.

### 10.2 The comparison that reframes the purchase decision

| Measure | Value |
|---|---|
| Wisconsin: using ambient AI versus not | **−21.90 min/day** |
| Duke: the better product versus the worse | **−3.19 min/day** |
| **Ratio** | **6.87×** |

```
choosing_any_tool_matters_more_than_which = True
```

**The gap between using a scribe and not using one is roughly seven times the gap between the better scribe and the worse one.**

That is the most commercially important finding across both trials, and neither vendor would put it in a deck. It says procurement teams running twelve-month bake-offs between vendors are optimising the small variable while the large one — adoption — waits.

And adoption is where the variance actually is: utilisation was **71.00%** in the Wisconsin trial and approximately **30%** in the Lukac trial, a gap of **41.00pp**, or **2.37×**. The Wisconsin authors attribute their higher fidelity to implementation work — pilot cycles with implementation scientists and human-factors experts.

**Implementation quality moved utilisation more than product choice moved minutes.**

---

## 11. What Abridge's own research measures

Abridge has two peer-reviewed publications. Both are real, both are in reputable venues, and having them puts Abridge ahead of every other company in this five-day arc.

### 11.1 JAMIA Open, February 2025

Pre- and post-intervention surveys of approximately **100** clinicians across specialties at the University of Kansas Medical Center.

| Self-reported result | Value |
|---|---|
| Found the documentation workflow easy to use | **81%** |
| Felt it improved patient care by decreasing documentation burden | **77%** |
| Reported decreased time documenting outside clinical hours | **73%** |
| Felt less at risk of burnout | **67%** |
| Felt increased satisfaction at work | **64%** |
| Mean across the five | **72.40%** |
| Spread, highest to lowest | **17.00pp** |

Clinicians were reported as **seven times** more likely to find their workflow easy and **five times** more likely to believe they could complete notes before the next patient visit.

**Design:** pre/post survey. No control group, no randomization, self-reported throughout.

### 11.2 Mayo Clinic Proceedings: Digital Health, March 2025

A **randomized crossover** design with **40** ambulatory clinicians, comparing two comparable clinic sessions, measuring cognitive load on the NASA-TLX index.

**Result: a 61% reduction in cognitive load.**

This is a properly randomized design and the result is substantial.

### 11.3 The finding

```
kumc1_reports_note_accuracy                     = False
kumc2_reports_note_accuracy                     = False
vendor_linked_studies_reporting_note_accuracy   = 0
independent_studies_reporting_note_accuracy     = 1
note_quality_measured_by_vendor                 = False
note_quality_measured_by_independent_trial      = True
```

**Neither vendor-linked study reports any measure of note accuracy.**

They measure workflow ease, perceived patient care, after-hours time, burnout risk, work satisfaction and cognitive load. Every one of those is about the clinician. Not one is about the note.

This is the same shape as Day 81, where Hinge Health disclosed a **97%** reduction in human care hours — a genuine, specific, disclosed metric that measured what the AI *saved* rather than what it *achieved*. Abridge's research measures how the doctor feels about the note, not whether the note is right.

To be fair about why: satisfaction and cognitive load are far cheaper to measure, they are what a health-system buyer asks about first, and they are the outcomes most directly tied to the purchase rationale. These are reasonable studies to have run. The gap is that the harder study — the one the Wisconsin team ran on someone else's money — is the one that tells a patient whether their record is accurate.

---

## 12. The confabulation whitepaper

Abridge published a technical whitepaper, *The Science of Confabulation Elimination: Toward Hallucination-Free AI-Generated Clinical Notes.* It is internal and **not peer reviewed**, but it is substantive and deserves credit for that.

**Method.** Claims in a generated note are classified into five support categories — Directly Supported; Circumstantially Supported, Reasonable Inference; Circumstantially Supported, Questionable Inference; Unmentioned; and Contradiction — with severity assessed separately as Major, Moderate or Minimal. A task-specific detection model trained on over **50,000** examples flags unsupported claims, and an automated system corrects, deletes, or dismisses them as false alarms. The internal benchmark holds over **10,000** realistic clinical encounters, informed by over **1,000 hours** of annotation by board-certified physicians.

**Result.** *"our technology outperforms GPT-4o by a wide margin, catching 97% of the confabulations, while GPT-4o only catches 82%."*

| Measure | Value |
|---|---|
| Abridge detection rate | **97.00%** |
| GPT-4o detection rate | **82.00%** |
| Advantage | **15.00pp** (**18.29%** relative) |
| **Confabulations missed** | **3.00%** |

### 12.1 What 97% detection is not

```
wp_detection_rate_equals_note_cleanliness      = False
wp_reports_underlying_generation_rate          = False
```

**A detection rate is not a note-cleanliness rate.** The whitepaper reports how often the detector catches a confabulation that is present. It does not report how often confabulations are generated in the first place, so the residual rate in a delivered note — the number a clinician actually needs — cannot be computed from it.

And **3.00%** of confabulations are missed by the detector's own measure.

### 12.2 The title is careful; the shorthand is not

```
wp_title_claims_hallucination_free   = False
wp_marketing_shorthand_drops_toward  = True
```

The whitepaper is titled *"**Toward** Hallucination-Free AI-Generated Clinical Notes."* Its conclusion says the company *"believe[s] that the adoption of ambient AI has the potential to nearly eliminate all mistakes"* — a belief about potential, carefully hedged twice.

The product page's shorthand is "hallucination-free."

The engineering document is honest and the marketing compression is not, which is a specific and fixable gap. It is also the most common failure mode across this entire five-day arc: Doximity's CEO quote, OpenEvidence's 40% that changed meaning, and now a "toward" that falls off in transit.

---

## 13. The equity gap nobody could test

**Wolfe & Welsh, Cureus, 2026** — a PRISMA-ScR scoping review of **27** sources on ambient documentation, prospectively registered on the Open Science Framework.

Its most consequential finding is not about any product. It is that the computer science literature has identified **significant racial and dialect-based disparities in the automatic speech recognition systems that underpin ambient documentation, with higher word error rates for Black speakers than for White speakers.**

```
scope_finds_asr_racial_disparity = True
guardrail_equity_reported        = False
```

Ambient documentation is ASR plus generation. If the ASR layer has differential word error rates by speaker race or dialect, then note quality is differential by patient population — and the error is invisible, because nobody reads the transcript against the audio.

### 13.1 The trial that validates the product cannot detect this

| Wisconsin trial population | Share |
|---|---|
| Practitioners identifying as non-Hispanic white | 89.4% |
| **Non-white practitioners** | **10.60%** |
| Patients identified as non-Hispanic white | 88.4% |
| **Non-white patients** | **11.60%** |
| English preferred | 98.1% |
| **Non-English encounters** | **1.90%** |

```
trial_population_can_test_asr_equity   = False
equity_gap_acknowledged_by_trial_authors = True
```

A PDSQI-9 accuracy score of **4.44** was measured in a population that was **88.4%** non-Hispanic white and **98.1%** English-preferring. The authors acknowledge the generalisability limit explicitly and to their credit.

But the consequence stands: **the best evidence that ambient documentation produces accurate notes comes from a population in which the literature's main equity concern could not have shown up.** Abridge claims support for 28 languages. No public evidence reports note quality by language, dialect or patient race.

That is the single largest unexamined risk in this product category, and closing it requires exactly one thing — stratifying an existing measurement.

---

## 14. Displacement of burden

**Sucharitrak, Cureus, 2026** — a narrative review weighting evidence by study design, with randomized trials carrying the greatest interpretive weight.

Its conclusion: *"AI tends to displace work rather than reduce it. Tasks are not eliminated but moved: from production to oversight, and potentially from physicians to nurses and assistants."* The review proposes **"displacement of burden"** as a testable framework, replacing earlier metaphors of a "double-edged scalpel" and a "productivity paradox."

```
narrative_review_proposes_displacement_of_burden = True
displacement_echoes_day81_finding                = True
```

### 14.1 Why this echoes Day 81

Day 81 found that Hinge Health disclosed an approximately **97%** reduction in human care hours — and that the metric measured labour removed, not health delivered. The open question there was whether the work disappeared or moved.

The displacement framework says: for ambient documentation, it moves. From writing to reviewing. And potentially down the professional hierarchy, from physicians to nurses and assistants.

The Wisconsin trial is partly consistent with this: daytime note time fell **21.90 minutes** reliably, while after-hours work did not fall reliably once outliers were trimmed. Work compressed into the day rather than disappearing.

**For a product manager, this reframes the category's core claim.** "We save clinicians two hours a day" is a production-side claim. The oversight cost — reading, correcting, and bearing responsibility for a fluent document you did not write — is real, is borne by the clinician, and is measured by nobody.

---

## 15. User personas

### 15.1 Dr. James O. — the attending (uses; his employer pays)

Family medicine, 50 patients a week, 14 years in practice — the median participant in the Wisconsin trial. Opens the app at the start of each visit, reviews the draft afterwards, signs.

**Jobs to be done:** finish the note before the next patient; stop charting at 10pm; be present in the room rather than behind a screen.

**What the evidence says he gets:** **21.90** fewer minutes a day on notes, a real reduction in exhaustion (NNT **1.68**), a **61%** drop in cognitive load — and, unless he is in the most overloaded few percent, **no reliable change to his evening.**

**What he cannot see:** whether the fluent note in front of him has the omission the **4.57** thoroughness score implies exists somewhere, or whether the **3.97** abstraction score means the synthesis is subtly wrong. The note reads well. That is precisely the problem.

### 15.2 Dr. Priya N. — the CMIO (evaluates, signs the contract)

Owns the ambient AI decision for a multi-hospital system. Has three vendors in a bake-off.

**Jobs to be done:** pick the right vendor; justify the spend; satisfy security and clinical governance; not be the person who deployed a tool that corrupted the record.

**What the evidence gives her:** a named independent RCT on one product, an anonymised head-to-head on two others, and the knowledge that **choosing any tool matters roughly 6.87× more than choosing which one.**

**What it does not give her:** any comparative note-quality data, anything stratified by her patient population's languages, and any vendor-published acceptance rate. She will run the bake-off anyway, because that is what procurement does — and the evidence says her implementation effort would return more than her selection effort.

### 15.3 The patient — present, recorded, and not represented

The Wisconsin trial reports a **99.92%** consent rate, with **22** patients declining and no recording-related complaints documented.

That is a genuinely reassuring number and it should be said. But consent to recording is not the same as understanding that a language model will draft the medical record, and the trial notes its own gap: it *"did not collect patient-reported outcomes related to comfort or disclosure."*

**The person whose record is being written is the only party to this transaction whose experience has not been measured by anyone.**

---

## 16. Jobs to be Done

| Job | Who has it | Served? | Evidence |
|---|---|---|---|
| "Finish my note before the next patient" | Clinician | Yes | −21.90 min/day |
| "Stop charting at night" | Clinician | **Unreliably** | WoW effect fails trimming |
| "Be present with the patient" | Clinician | Yes | 61% cognitive load reduction |
| "Don't let the record be wrong" | Clinician, patient | **Unmeasured by vendor** | PDSQI-9, independent only |
| "Code the visit correctly" | Health system | Yes | ICD-10 6.87 vs 5.94 |
| "Pick the right vendor" | CMIO | **No** | Head-to-head anonymised |
| "Know it works for my patients" | Health system | **No** | No stratified evidence |

---

## 17. The billing finding, which nobody is talking about

| Measure | Ambient AI notes | Human-authored notes |
|---|---|---|
| ICD-10 coding compliance (0–10, adjudicated by certified coders) | **6.87** (95% CI 6.76–6.98) | **5.94** (95% CI 5.81–6.07) |

| Derived | Value |
|---|---|
| Difference | **0.93** |
| Relative improvement | **15.66%** |
| Notes sampled | **6,110** |

P<0.001, assessed by professional health-system coders against a standardised rubric, not by the AI.

**This is the most commercially significant result in the trial and it received the least attention.** Coding compliance drives reimbursement directly. A **15.66%** improvement in diagnostic coding compliance across a health system is a revenue-cycle effect that dwarfs the soft-dollar value of clinician satisfaction, and it is adjudicated by humans rather than by a language model.

It also explains a strategic move that otherwise looks like drift: the company's stated intent to *"embed revenue cycle intelligence earlier in the clinical conversation."* Abridge is not wandering from documentation into billing. **The trial evidence says documentation quality is already producing a billing effect** — and the company is following its own data.

### 17.1 The tension that creates

A documentation product optimised for coding compliance and a documentation product optimised for clinical accuracy are not the same product, and they diverge quietly. Codeable specificity is not the same as clinical truth. Nobody is currently measuring whether pressure toward the first degrades the second, and the PDSQI-9 abstraction score of **3.97** is where that would show up first.

---

## 18. Business model and distribution

**Model.** Enterprise SaaS sold to health systems, per clinician. The clinician does not pay and the patient does not pay.

**Distribution.** Embedded in Epic through private and FHIR R4 APIs, delivered via Epic Haiku mobile. The Wisconsin trial required participants to use an Apple mobile device with Epic Haiku access.

### 18.1 Epic is the distribution and the dependency

This is the sharpest strategic contrast with the previous four days. Days 80–83 all went direct — direct-to-consumer, direct-to-physician, or through a network the company owned. Abridge goes through Epic.

That is an enormous distribution advantage: Epic sits in the clinical workflow already, and integration means the tool appears where the clinician works rather than asking them to go somewhere else. It is also the concentration risk that defines the company. The integration runs on **Epic's private APIs** — access granted by a partner that also builds ambient documentation itself.

No public source discloses the commercial or contractual terms of that access. It is the most consequential undisclosed fact about this business.

### 18.2 The device requirement as a quiet equity issue

The trial's eligibility required an **Apple mobile device**. Whether that reflects the product or only the trial protocol is not stated in the sources examined — but a documentation tool whose access depends on a personally owned premium device has a distribution floor, and it will not be evenly distributed across health systems or clinician seniority.

---

## 19. Funding and scale claims

| Round | Date | Amount | Valuation |
|---|---|---|---|
| Series C | Feb 2024 | $150M | — |
| Series D | Feb 2025 | $250M | — |
| Series E | Jun 2025 | **$300M** | **$5.3B** |

| Measure | Value |
|---|---|
| Three named rounds | **$700.00M** |
| Total raised, as claimed | **$800.00M** |
| Not attributed to the three named rounds | **$100.00M** |
| Valuation per claimed health system | **$35.33M** |

Company claims as of the Series E: **150+** health systems, **55** specialties, **28** languages, a projected **50 million** medical conversations for the year, a proprietary dataset of over **1.5 million** encounters, Johns Hopkins rolling out across **6,700** clinicians and Mayo Clinic to approximately **2,000** — **8,700** clinicians across those two systems alone.

| Derived | Value |
|---|---|
| Conversations per health system per year | **333.33 thousand** |
| Proprietary dataset as a share of one year's conversation volume | **3.00%** |

In June 2026 the company announced a strategic investment from Eli Lilly and a collaboration with NVIDIA on a clinical-conversation foundation model. **Terms were not disclosed for either**, and a widely cited cumulative figure of $1.1B raised could not be confirmed against a primary source. Both are recorded in Appendix A rather than used.

---

## 20. Competitive analysis

| Competitor | Position |
|---|---|
| **Microsoft / Nuance DAX** | The incumbent; named in the Lukac trial, where its note-time effect was **not** significant |
| **Nabla** | Named in the Lukac trial with a significant effect (**41** vs **18** seconds) |
| **Ambience Healthcare** | Enterprise ambient documentation |
| **Epic's own ambient tooling** | The distribution partner competing in the category |
| **Doximity Scribe** (Day 82) | Bundled free inside Workflow Solutions seats |
| **Suki, Augmedix** | Ambient documentation |

### 20.1 Porter's Five Forces

**Threat of new entrants — Moderate.** ASR and generation are commoditising. The moat is the Epic integration, the health-system contracts and the proprietary annotated dataset — over **1.5 million** encounters.

**Bargaining power of buyers — High.** Health systems run formal bake-offs and the switching cost is a retraining exercise, not a data migration. And the evidence says the products differ by **3.19 minutes a day**.

**Bargaining power of suppliers — Very high, and concentrated in one name.** Epic controls the integration surface and competes in the category.

**Threat of substitutes — Moderate.** Human scribes, templates, and doing nothing. Day 82's Doximity gives a scribe away bundled inside Workflow seats, which is a real pricing threat.

**Competitive rivalry — Intense.** Well-funded competitors, a commoditising core, and an active trade-secrets suit.

### 20.2 The moat question

**Abridge's moat is the Epic relationship and the annotated dataset. Neither is owned outright.** The dataset is the more durable of the two — 1,000+ hours of board-certified physician annotation is genuinely expensive to replicate — but it is only **3.00%** of a single year's conversation volume, which means competitors operating at scale accumulate comparable raw material quickly. The annotation, not the audio, is the asset.

---

## 21. SWOT

**Strengths.** An independent, NIH-supported, pre-registered RCT that names the product and reports an NNT of **1.68**. Two peer-reviewed vendor-linked studies. A detailed hallucination-detection whitepaper with a stated method. Note quality independently measured at a **4.62** mean across seven domains. ICD-10 compliance **15.66%** above human-authored notes. Epic distribution. A **99.92%** patient consent rate.

**Weaknesses.** Zero vendor-published note-accuracy metrics. Abstraction — the reasoning domain — is the weakest at **3.97**. Accuracy carries the largest variance (SD 0.93). "Toward hallucination-free" compresses to "hallucination-free" in marketing. No evidence stratified by language, dialect or patient race. After-hours benefit does not survive sensitivity analysis.

**Opportunities.** Publish PDSQI-9 per release and own the metric outright. Publish the unedited-note acceptance rate. Stratify quality by language and close the equity gap first. Convert the coding-compliance result into a revenue-cycle position. Fund named head-to-head trials.

**Threats.** Epic as both channel and competitor. Commoditising ASR and generation. Day 82's Doximity bundling a scribe free. An active DTSA claim. The displacement-of-burden critique, if it is validated, undercuts the category's headline promise.

---

## 22. The litigation

```
abridge_is_defendant       = True
abridge_cases_as_plaintiff = 0
abridge_cases_as_defendant = 1
```

**Arslani v. Abridge AI, Inc.**, No. 3:26-cv-50118 (N.D. Ill.), filed 23 March 2026, before Judge Iain D. Johnston. Cause of action: **18 U.S.C. §1836(b), the Defend Trade Secrets Act**. Jury demanded by both. An amended complaint was filed on 3 April 2026. The case is open.

### 22.1 The inversion from Day 83

Day 83's OpenEvidence had **six** federal cases in 559 days and filed **four** of them. Abridge has **one**, and is the defendant.

| Measure | Value |
|---|---|
| Day 83 total cases | 6 |
| Day 83 cases as plaintiff | 4 |
| Day 84 cases, as a ratio of Day 83's | **0.17** |

```
both_day83_and_day84_face_dtsa_claims = True
```

Both companies are party to Defend Trade Secrets Act litigation. Two of the most prominent clinical AI companies in the United States are in trade-secret disputes, which says something about how this category's talent and technique move between organisations.

Nothing here establishes that anyone did anything wrong. A complaint is an allegation.

### 22.2 A case this study does not characterise

```
abridge_is_party_to_sutter_case        = False
sutter_case_characterised_in_this_study = False
```

A separate docket, *Washington v. Sutter Health*, No. 4:26-cv-03012 (N.D. Cal.), surfaces in a full-text search for "Abridge AI." **Abridge is not a party to it.** The term appears somewhere in the case documents, and without retrieving those documents this study cannot say in what capacity or context.

It is recorded here only so that a reader running the same search is not left wondering why it was omitted. **No allegation in that case is described, attributed or implied.**

---

## 23. User journey

| Stage | Clinician experience | Where the risk sits |
|---|---|---|
| Consent | Patient informed at check-in and verbally; may decline | **99.92%** consent — friction is negligible |
| Capture | Conversation recorded ambiently | ASR error, unevenly distributed by speaker |
| Generation | Draft note appears in Epic | Abstraction **3.97**; omissions invisible |
| **Review** | Clinician reads and edits | **The only safety gate, and it is unmeasured** |
| Signature | Note enters the record | Becomes the legal and billing record |
| Downstream | Coding, billing, next clinician, malpractice defence | ICD-10 compliance **6.87** |

### 23.1 The review step is the whole product

Everything upstream of review is recoverable. Everything downstream is not.

And the review step has a specific adversary built into the product's strength: **the note reads well**. Language quality scored **4.84** against substance at **4.33**. A fluent, well-organised, appropriately concise document invites a faster read than a rough one does.

Nobody measures how long clinicians spend reviewing, what fraction they edit, or whether review time falls as trust grows. The Wisconsin trial scored notes *before* review — which is the right scientific choice, and it means the trial tells us about the draft rather than about the signed record.

**The gap between what was measured and what reaches the patient's chart is the clinician's attention, and it is the least instrumented part of the system.**

---

## 24. AARRR funnel

| Stage | Position | Evidence |
|---|---|---|
| **Acquisition** | Strong — 150+ health systems claimed | Company |
| **Activation** | Variable — **71.00%** utilisation at Wisconsin, ~30% at Lukac | Trials |
| **Retention** | Strong where implementation is strong | **10.61%** low-fidelity users |
| **Referral** | Peer and CMIO networks; unmeasured | — |
| **Revenue** | Per-clinician enterprise licensing | Not disclosed |

The funnel's weak joint is activation, and it is an **implementation** variable rather than a product one. The **41.00pp** utilisation gap between two trials of similar tools is the single largest number in this case study that a vendor can actually move.

---

## 25. HEART framework

| Dimension | Measure | Reported? |
|---|---|---|
| **Happiness** | Clinician satisfaction | **Yes** — vendor studies and both RCTs |
| **Engagement** | Utilisation rate | **Yes** — 71.00% (independent) |
| **Adoption** | Time to first note | No |
| **Retention** | Sustained utilisation | Partially — 7 low-fidelity users identified |
| **Task success** | **Note signed without material edit** | **No — by anyone** |

Four of five dimensions have some evidence. Task success — the one that says whether the product did its job — has none.

This is a narrower gap than Days 80–83 faced, and it is the same gap.

---

## 26. Kano analysis

| Feature | Category | Note |
|---|---|---|
| Accurate capture of what was said | **Must-be** | Accuracy 4.44, SD 0.93 — the variance is the risk |
| No fabricated content | **Must-be** | Detector catches 97%; **3.00%** missed |
| Note ready before the next patient | **Performance** | −21.90 min/day |
| Correct clinical synthesis | **Performance** | **3.97** — the weakest domain |
| Coding compliance | **Attractive** | **15.66%** above human notes; unexpected |
| Multi-language support | **Attractive** | 28 claimed; **quality unmeasured** |

The must-be features carry the measurement risk. The attractive features carry the commercial upside. Coding compliance is the genuinely delightful surprise in this product and it was discovered by an independent trial, not marketed by the vendor.

---

## 27. Eval plan

What a company with this product should be running continuously.

**Repeatability.** Same encounter audio, repeated generation, measure divergence. Day 83 found **23.00%** answer discordance at a different clinical AI product; nobody has published the equivalent for ambient documentation.

**Omission detection against the transcript.** The thoroughness domain scored **4.57** — good, and the most dangerous failure mode in documentation is the thing that is not there. Automated entailment checking of transcript content against note content, reported as a recall rate.

**Stratified accuracy.** By patient language, dialect, accent and race; by specialty; by encounter length and complexity. This is the equity gap in section 13 and it requires only disaggregating a measurement already being taken.

**Unedited acceptance rate in production.** What share of drafts are signed with no material edit, and how does that change over a clinician's first 90 days? A rate trending to 100% is a warning, not a triumph.

**Adversarial safety.** Negation, dose units, medication name confusion, laterality (left versus right), and temporal ordering of symptoms.

**Release gating.** No model version ships without non-regression on omission recall and the safety suite. PDSQI-9 published per version.

---

## 28. Ranked failure modes

By expected harm.

**1. A clinically significant omission in a signed note.** Highest harm, hardest to detect, invisible by construction — nobody notices absent information. Thoroughness **4.57** implies a non-zero rate. Mitigation: transcript-to-note recall checking with the omission surfaced in the review UI.

**2. A fabricated finding that survives review.** Detector catches **97.00%**; **3.00%** are missed and the generation rate is not published. Mitigation: publish the residual rate in delivered notes, not just detector recall.

**3. Differential accuracy by patient population.** Potentially the highest aggregate harm on this list, ranked third only because there is no evidence either way. The literature flags ASR disparities; the validating trial was **88.4%** non-Hispanic white and **98.1%** English. Mitigation: stratify and publish.

**4. Faster review as trust grows.** The note reads better than it thinks (**0.51** language-over-substance gap), which makes it easy to sign. Mitigation: monitor edit rates over tenure; treat a falling rate as a risk signal.

**5. Coding pressure degrading clinical accuracy.** Section 17.1. Mitigation: track abstraction and accuracy alongside coding compliance and watch for divergence.

**6. Laterality and temporal errors.** Left versus right, before versus after. Low frequency, high consequence, classic ASR-plus-generation failure. Mitigation: dedicated release-gating test suite.

**7. Silent regression after a model update.** The Wisconsin trial ran drift monitoring across 15 rolling windows and found none — which is the correct control and is the best example in this arc of a health system instrumenting a vendor properly.

Failure modes 1, 2 and 3 all concern the record rather than the clinician. All three are measurable. None is published by the vendor.

---

## 29. Human-in-the-loop design

The clinician signs the note, so the loop exists by construction. Whether it is load-bearing depends on three things the product controls.

**Show what is uncertain.** The confabulation taxonomy already distinguishes "Directly Supported" from "Questionable Inference" from "Unmentioned." That classification exists inside the system. Surfacing it in the review UI — highlighting the spans the model itself rated as weakly supported — would convert an internal quality signal into a clinical safety feature at almost no cost.

**Show what is missing.** Harder and more valuable. An omission cannot be highlighted in a note because it is not in the note. It can, however, be flagged from the transcript: "the patient mentioned a medication that does not appear in this draft."

**Measure the loop.** Edit rate per clinician over time. Review duration. Which domains get edited most. None of this is published, and all of it is already instrumentable.

### 29.1 The incentive here is better than Day 83's

Day 83's OpenEvidence ran on advertising, where every second a clinician spends checking a citation is a second not generating another impression — an incentive pointing away from a careful loop.

Abridge sells per-clinician enterprise licences. **Revenue does not scale with how fast the clinician signs.** A health system that discovers its notes are unreliable does not renew, so the commercial incentive and the safety incentive point the same way.

That is a structurally healthier position than any of the previous four days, and it is worth naming because it means the missing disclosures here are an oversight to fix rather than a conflict to manage.

---

## 30. Pricing

Per-clinician enterprise licensing, terms undisclosed.

| Model | Alignment with safety | Current |
|---|---|---|
| Per clinician per year | **Good** — revenue independent of note volume or review speed | **Current** |
| Per encounter | Poor — rewards volume | — |
| Outcome-based (per note accepted unedited) | Strong, and would force the metric to exist | — |
| Bundled free (Day 82's Doximity) | Poor — no revenue to fund evaluation | — |

The current model is the right one. An outcome-based tier would be the interesting experiment: pricing tied to unedited acceptance would create the first commercial reason for anyone to publish that number.

---

## 31. Product recommendations

Six, each with the evidence and the proof metric.

### R1. Publish PDSQI-9 scores with every model release

**Evidence:** an independent trial measured this on **7,966** notes; the vendor publishes nothing equivalent.
**Proposal:** adopt the instrument the independent literature already validated, run it per release on a fixed sample, publish all seven domains.
**Why first:** the instrument exists, the method is published, the comparison baseline is public, and no competitor does it. It converts the strongest external finding about Abridge into an owned position.
**Success:** two consecutive releases published under an unchanged method.
**Cost:** Low.

### R2. Publish the unedited-note acceptance rate from production

**Evidence:** the metric Day 82 asked for; measured by nobody, including the independent trial, which scored drafts rather than signed notes.
**Proposal:** publish the share of drafts signed with no material edit, with a published materiality threshold, stratified by specialty.
**Why:** it is the only metric that describes what actually reaches the patient's chart, and the company already has the data.
**Success:** published quarterly; the rate is stable or improving without approaching 100%.
**Cost:** Low technically. The hard part is that a very high number is as concerning as a low one, and the company would have to explain why.

### R3. Report note quality stratified by language and dialect

**Evidence:** the scoping review's ASR disparity finding; a validating trial that was **98.1%** English.
**Proposal:** disaggregate PDSQI-9 by patient preferred language and, where measurable, dialect. Publish the gaps.
**Why:** this is the largest unexamined risk in the category. A vendor claiming 28 languages with no quality evidence by language is making a distribution claim, not a quality one.
**Success:** published disaggregation with gaps under a stated threshold.
**Cost:** Moderate — requires the sample, not new science.

### R4. Fund head-to-head trials that name the products

**Evidence:** the Duke trial is anonymised and therefore unactionable; two of three independent trials name products.
**Proposal:** fund independent comparative trials with a binding pre-commitment to publish whatever the result is, products named.
**Why:** the **6.87×** finding says adoption matters more than selection, which is an argument Abridge can only make credibly if it is willing to be named in a comparison it might lose.
**Success:** a published named head-to-head, whatever the outcome.
**Cost:** High, and genuinely risky.

### R5. Surface the confabulation classification in the review interface

**Evidence:** the five-category taxonomy already exists internally; the review loop is the only safety gate and is unassisted.
**Proposal:** highlight spans the internal classifier rates below "Directly Supported," and flag transcript content absent from the draft.
**Why:** turns an internal quality system into a clinical safety feature, and directly addresses failure modes 1, 2 and 4.
**Success:** measurable increase in targeted edits without an increase in total review time.
**Cost:** Moderate — a real product change.

### R6. Submit the confabulation benchmark for peer review

**Evidence:** the whitepaper is substantive but internal; its **97.00%** detection claim has no external validation.
**Proposal:** publish the benchmark and methodology in a peer-reviewed venue, and release the benchmark for others to run against.
**Why:** an internal benchmark showing your product beating GPT-4o is marketing until someone else can run it.
**Success:** peer-reviewed publication; third-party replication.
**Cost:** High, slow, and it exposes the method to criticism.

---

## 32. RICE prioritisation

R, I, C, E and every stress factor are **author estimates, not disclosed data**. Reach is held at 150 — the claimed health-system count — because every proposal's audience is the buying institution. Stress discounts by dependence on uncheckable claims and by execution exposure.

| ID | Proposal | R | I | C | E | Base | Stress | Stressed |
|---|---|---|---|---|---|---|---|---|
| P1 | Publish PDSQI-9 per release | 150 | 3.0 | 0.90 | 3.0 | **135.00** | 0.95 | **128.25** |
| P4 | Publish unedited-note acceptance rate | 150 | 2.5 | 0.80 | 4.0 | **75.00** | 0.85 | **63.75** |
| P3 | Stratify note quality by language | 150 | 2.5 | 0.85 | 5.0 | **63.75** | 0.90 | **57.38** |
| P2 | Fund named head-to-head trials | 150 | 3.0 | 0.70 | 9.0 | **35.00** | 0.60 | **21.00** |
| P5 | Submit confabulation benchmark for peer review | 150 | 2.0 | 0.60 | 10.0 | **18.00** | 0.50 | **9.00** |

```
rice_base_ranking           = ('P1', 'P4', 'P3', 'P2', 'P5')
rice_stress_ranking         = ('P1', 'P4', 'P3', 'P2', 'P5')
rice_last_under_stress      = 'P5'
rice_last_under_stress_name = 'Submit the confabulation benchmark for peer review'
rice_last_gap_pct           = 57.14
```

### 32.1 Reading the ranking

The ordering is stable under stress, so the top proposals are robust rather than marginal.

**P5 ranks last, by 57.14% below P2** — asserted by the gate, not argued here. Peer-reviewing the confabulation benchmark would do more than anything else to settle whether the **97.00%** detection claim means what it appears to mean. It ranks last because it has low confidence (0.60), the highest effort (10 person-months), and the harshest stress factor (0.50): peer review is slow, the outcome is not controllable, and a benchmark built and run by the vendor may not survive external scrutiny of its construction.

**That last clause is the real reason, and it generalises.** A company that builds its own benchmark, runs it, and publishes the result has produced something that is useful internally and nearly worthless externally — and converting it into external evidence means surrendering control of the method. Most companies decline, which is why internal benchmarks proliferate and peer-reviewed ones do not.

P1 loses only **5.00%** under stress because it depends on no contested claim — it requires running a published instrument and publishing the output. P5 loses **50.00%**.

---

## 33. MoSCoW

**Must have.** R1 (PDSQI-9 per release); R2 (unedited acceptance rate); R3 (stratify by language).

**Should have.** R5 (surface classification in review).

**Could have.** R4 (named head-to-head trials).

**Won't have this cycle.** R6 (peer-review the benchmark) — sequencing, not rejection. See 32.1.

---

## 34. PRD: unedited-note acceptance rate (R2)

**Problem.** Independent research scored Abridge drafts on quality. Nobody — vendor or academic — reports what share of those drafts reach the patient's chart unchanged. The clinician's review is the only safety gate in the system and it is uninstrumented in public.

**Objective.** Publish the unedited-note acceptance rate quarterly under a fixed, public method.

**Proposed metric.** The share of AI-generated drafts signed with no material edit, where "material" is defined by a published threshold distinguishing substantive change from formatting and phrasing.

**Non-goals.** Not an accuracy claim. Not a safety certification. Not a replacement for PDSQI-9, which measures the draft rather than the signed note.

**Requirements.**
- R2.1 Define materiality before first publication and publish the definition. **This is the hard part** — a clinician correcting "patient denies chest pain" to "patient reports chest pain" and one restructuring a paragraph must not count the same.
- R2.2 Compute at signature, per note, stratified by specialty and clinician tenure.
- R2.3 Publish the distribution, not only the mean.
- R2.4 Restate prior periods if the definition changes, and say so.
- R2.5 Report alongside review duration, so that acceptance and attention can be read together.

**Success criteria.** Two consecutive quarters under an unchanged method. Secondary: a competitor adopts it, making it a category standard.

**Risks.** A high rate could mean the notes are excellent or that clinicians have stopped reading — the metric cannot distinguish these alone, which is why R2.5 matters. The first number may be unflattering. It becomes a commitment that cannot be withdrawn. **All three are reasons to publish it.**

---

## 35. Roadmap

**Horizon 1 — next two quarters.** R1 (PDSQI-9 per release), R2 (unedited acceptance rate). Both use data the company already has; both establish that it will publish numbers that can move against it.

**Horizon 2 — quarters three and four.** R3 (stratify by language), R5 (surface classification in review). R3 needs Horizon 1's measurement pipeline; R5 is a product change that Horizon 1 makes measurable.

**Horizon 3 — year two.** R4 (named head-to-head), R6 (peer-review the benchmark). Both are only credible once the company has a track record of publishing unflattering numbers.

### 35.1 Sequencing logic

Ordered by **evidence dependency and reversibility**. Every later item needs an earlier one to be credible, and the two Horizon 3 items both involve surrendering control of a method to outsiders — which is only rational once the easy disclosures have established that the company survives publishing its own numbers.

---

## 36. Risks to this analysis

**One trial names the product.** The Wisconsin trial is the backbone of this case study. It is well designed, pre-registered, independently funded and peer reviewed — and it is **one** trial, n=66, at one academic health system, in a predominantly white, English-speaking, family-medicine-heavy population of self-selected early adopters. The authors say all of this themselves.

**The PDSQI-9 scores were produced by an LLM judge.** Validated against physician ratings, which is the right approach, but it is an AI grading an AI. Section 9.3.

**The trial population was self-selected.** Participation required volunteering and a willingness to adopt. The trial notes that expectancy and Hawthorne effects are possible under the open-label design.

**Vendor-linked studies are not thereby wrong.** The JAMIA Open and Mayo Clinic Proceedings papers are peer reviewed and the second is randomized. The criticism is about what they measure, not about their integrity.

**"Independent" is doing work.** The Wisconsin trial was funded by the health system that deployed the product commercially and by an NIH award. That is independent of the vendor, which is the relevant sense — but the institution had an operational contract with Abridge concurrently, which the paper states plainly.

**The equity concern is inferred, not measured.** The scoping review documents ASR disparities in the underlying technology class. **No study examined here measured Abridge's accuracy by patient race, dialect or language.** The risk is well founded; the magnitude for this product is unknown.

**Court filings are allegations.** Section 22 establishes nothing about anyone's conduct.

**RICE inputs are the author's.** Section 32 and ASSUMPTIONS.md.

---

## 37. What a product manager should take from this

**The evidence you need may already exist, produced by someone who does not sell to you.** Before accepting that a category has no outcome data, search the peer-reviewed literature rather than the vendor's website. In this case a pre-registered RCT with 71,487 notes answered the question the vendor's marketing did not.

**Check whether the study measures your users or your product.** Abridge's two peer-reviewed papers measure clinician satisfaction and cognitive load. Those are real outcomes and they are not note accuracy. The distinction between "our users are happier" and "our output is correct" is the most consistent blind spot across this five-day arc.

**Fluency is not accuracy, and it is the enemy of review.** Language scored **4.84** against substance at **4.33**. A well-written wrong note is more dangerous than a badly written one, because it gets signed faster. If your product generates text a human must check, measure how good it *looks* separately from how good it *is*.

**Sensitivity analysis is where headline results go to die.** The after-hours result — the most marketable number in the trial — did not survive trimming the top 3% of observations. Attenuation of **62.00%**. When a vendor quotes a study, find the sensitivity analysis before quoting it back.

**Adoption beats selection.** The difference between using a scribe and not using one was **6.87×** the difference between the better and worse product. Utilisation varied **41.00pp** between two trials of similar tools. Time spent on implementation returns more than time spent in a bake-off.

**Watch the word that falls off in transit.** "Toward hallucination-free" becomes "hallucination-free." A 97% detection rate becomes a cleanliness guarantee. The engineering is usually honest; the compression is where the claim breaks.

---

## 38. The five-rung ladder

| Rung | Company | Status | What is disclosed about AI outcomes |
|---|---|---|---|
| 1 | **Day 80 — Hims & Hers** | Public | **No AI metric at all** |
| 2 | **Day 81 — Hinge Health** | Public | A **cost** metric (~**97%** human care hour reduction); no outcome |
| 3 | **Day 82 — Doximity** | Public | AI cost audited; all four AI claims quote-only |
| 4 | **Day 83 — OpenEvidence** | Private | No filing; one independent preprint; **23.00%** discordance |
| 5 | **Day 84 — Abridge** | Private | **Independent randomized trials measure the outcome** |

```
ladder_length                       = 5
days_with_independent_outcome_evidence = 1
share_of_arc_with_outcome_evidence_pct = 20.00
```

**One company in five has independent outcome evidence, and it did not produce it.**

That is the five-day finding, and it is more hopeful than the four-day version. The evidence is possible. Academic teams with NIH funding and a health system's cooperation can measure documentation quality on eight thousand notes in a randomized design. It is not prohibitively hard and it does not require the vendor's permission.

**It just is not anyone's commercial job.**

---

## 39. The two private companies, side by side

| Measure | Day 83 — OpenEvidence | Day 84 — Abridge |
|---|---|---|
| Product | Clinical reference and search | Ambient documentation |
| In the reasoning loop? | **Yes** | **No** — documentation only |
| Monetisation | Advertising (free to clinician) | Per-clinician enterprise licence |
| Incentive alignment | Revenue rises with usage | Revenue independent of usage |
| Independent evidence | One preprint, n=100, not peer reviewed | **Three peer-reviewed trials**, one naming the product |
| Outcome measured independently | Accuracy **31.00%**, discordance **23.00%** | PDSQI-9 mean **4.62**, NNT **1.68** |
| Vendor-published outcome metric | None | None |
| Federal cases | **6** in 559 days, 4 as plaintiff | **1**, as defendant |

Two private clinical AI companies, both facing DTSA claims, with opposite evidentiary positions. The difference is not that one is more honest. **The difference is that one operates in a category academics could study with a randomized trial, and the other does not.**

You can randomise clinicians to a documentation tool and measure the notes. You cannot easily randomise physicians to a reference tool and measure whether their decisions improved. **The category determines how much evidence is possible**, and that is a structural fact about the product, not a choice about disclosure.

---

## 40. Counterfactual: suppose the vendor published everything

Worth running, because the critique should not depend on assuming bad faith.

Suppose Abridge published PDSQI-9 per release, the unedited acceptance rate, and stratified quality by language tomorrow.

**What would change:** a CMIO could compare vendors on note quality. The equity question would be answerable. Clinicians would know how carefully to read. Competitors would be pressured to match, and the category would get a standard.

**What would not change:** the head-to-head trial would still be anonymised. The **6.87×** finding would still say implementation beats selection. Displacement of burden would still be unresolved. Patient-reported outcomes would still be uncollected.

**And the deeper problem would remain.** Voluntary disclosure can be withdrawn, and a vendor-run measurement of a vendor's product is a lower tier of evidence than an independent trial however well intentioned. The reason the Wisconsin trial is worth more than anything Abridge could publish is not that Abridge would lie. **It is that the trial's authors had no stake in the answer.**

That is an argument for funding independent evaluation as infrastructure — the same argument the FDA embodies for drugs — rather than for asking vendors to grade themselves more diligently.

---

## 41. Regulatory position

The Wisconsin trial states the scope precisely: the software was **documentation-only and provided no diagnostic or therapeutic decision support.**

That sentence is load-bearing. Clinical decision support software approaches FDA device regulation; transcription and documentation tooling generally does not. A product that drafts a note from a conversation is, in regulatory terms, closer to a dictation system than to a diagnostic aid.

Two consequences follow.

**The scope boundary is a regulatory asset and should be defended deliberately.** Every feature that edges toward suggesting a diagnosis, flagging a differential, or recommending an order moves the product toward a different regulatory class. The revenue-cycle direction described in section 17 is commercially attractive precisely because coding is not clinical recommendation — it stays on the safe side of the line.

**The record it produces is still a regulated artefact**, even if the tool is not a regulated device. Documentation accuracy sits under medical-record and billing-integrity requirements regardless of who or what drafted it, and the accountability rests with the signing clinician.

No public source addresses Abridge's regulatory classification and this section makes no claim about it.

---

## 42. Privacy and consent

**Consent worked, at the level the trial measured.** A **99.92%** consent rate with **22** declines and no documented recording-related complaints is a strong operational result, and it suggests patients are not meaningfully resistant to being recorded in a clinical encounter.

Three things that rate does not establish:

**Understanding is not consent.** Patients were informed at check-in and verbally by the practitioner that ambient AI would be used. Whether they understood that a language model would draft their medical record, and that the draft would carry an omission risk, is not something a consent rate measures. The trial acknowledges it collected no patient-reported outcomes on comfort or disclosure.

**Audio retention is undisclosed.** What happens to the recording after the note is generated — retention period, use for model training, de-identification standard — is not addressed in any source examined. The company references a proprietary dataset of over **1.5 million** encounters, which makes the question concrete rather than theoretical.

**Declining may not be costless in practice.** The trial states patients could decline without consequence, and 22 did. In a real clinic, declining a default that everyone else accepts carries a social cost that a trial environment with research oversight tends to minimise.

---

## 43. Concentration and governance

| Dimension | Position |
|---|---|
| Distribution | **Single channel** — Epic |
| Channel is also a competitor | **Yes** |
| Customer type | Health systems only |
| Revenue concentration by customer | Not disclosed |
| Geographic | United States |
| Investors | a16z, Khosla, Eli Lilly (terms undisclosed), others |
| Board and control | Not disclosed |

The Epic dependency is the governance fact that matters. A product distributed through a partner's private APIs, in a category that partner also competes in, has its most important commercial term set by someone else and disclosed to no one.

An Eli Lilly equity position is worth noting separately. A pharmaceutical manufacturer holding equity in the company that drafts clinical notes is not an obvious conflict — Abridge does not sell advertising and does not surface treatment recommendations — but it is the kind of relationship that becomes one if the product ever moves toward suggesting orders. Terms were not disclosed.

---

## 44. Scenario analysis

Author constructs applying arithmetic to published results. Not forecasts.

### 44.1 If the PDSQI-9 accuracy floor were set at 4.50

| Measure | Value |
|---|---|
| Measured accuracy | **4.44** |
| Proposed floor | **4.50** |
| Shortfall | **0.06** |
| Floor currently met? | **No** |

```
guardrail_accuracy_currently_met = False
```

A floor of 4.50 on a five-point scale is not aggressive — it is 90% of scale. The measured accuracy sits **0.06** below it. That is a narrow miss, and it is the kind of threshold that only becomes meaningful once someone publishes the number every release and the trend becomes visible.

### 44.2 If abstraction is where clinical risk concentrates

Abstraction scored **3.97**, the lowest of seven domains and **79.40%** of scale, against comprehensibility at **99.80%**.

Abstraction is synthesis — integrating across data elements to produce a clinical picture. It is the domain closest to reasoning and furthest from transcription, and it is the one a documentation tool is least equipped to do well.

**A product that transcribes at 99.80% of scale and synthesises at 79.40% is a very good stenographer and a mediocre clinician** — which is exactly what it should be, given the documentation-only scope in section 41. The risk is not that abstraction is weak. The risk is that the note's fluency implies a synthesis quality the score does not support.

### 44.3 If utilisation drove the outcome more than the product did

| Measure | Value |
|---|---|
| Wisconsin utilisation | **71.00%** |
| Lukac utilisation | **30.00%** |
| Gap | **41.00pp** (**2.37×**) |
| Wisconsin note-time effect | **−21.90 min/day** |
| Lukac between-product effect | **23.00 seconds** |

The trial with more than double the utilisation found an effect an order of magnitude larger. The Wisconsin authors attribute their fidelity to implementation science and human-factors work, not to the product.

**The most likely reading is that implementation quality, not model quality, is the dominant variable in whether ambient documentation works at a given health system.** That is uncomfortable for every vendor in the category, because it means the differentiated asset is a services capability rather than a model.

---

## 45. Sensitivity: what the trial would need to change its conclusion

**On burnout.** An NNT of **1.68** with a CI of 1.55–1.82 is robust. It would take a substantially larger trial finding a materially smaller effect to overturn this, and the effect direction is consistent across the vendor-linked studies, the Duke trial and the reviews. **This conclusion is unlikely to move.**

**On after-hours time.** Already fragile. The effect vanished on trimming **3%** of observations. A single larger trial could settle it either way.

**On note quality.** A **4.62** mean across domains from an LLM judge on **7,966** notes would be meaningfully challenged by a physician-scored study on a smaller sample showing a lower accuracy figure. The variance (SD **0.93** on accuracy) suggests a physician-scored subsample would be the cheapest high-value follow-up anyone could run.

**On equity.** There is nothing to overturn, because nothing has been measured. Any stratified study would be the first datapoint.

---

## 46. What would change my mind

**I would drop the disclosure criticism** if Abridge published PDSQI-9 per release or the unedited acceptance rate. Either would make it the first company in this five-day arc to publish an outcome metric, and the criticism in this document would be obsolete.

**I would revise the equity concern** if a stratified study showed no material accuracy gap by patient language or dialect. The concern is inferred from the technology class, not measured on this product.

**I would revise the fluency-versus-substance framing** if a physician-scored evaluation found accuracy and abstraction at parity with the language domains. The **0.51** gap comes from a single LLM-judged evaluation.

**I would not revise the structural finding.** A private company has no obligation to publish anything, voluntary disclosure can be withdrawn, and vendor-produced evidence about a vendor's product will always rank below independent evidence. That is a fact about incentives, not about Abridge.

---

## 47. Recommended diagrams

Per series standard from Day 50: **no Mermaid**. Markdown tables and ASCII only.

**D1 — Who measured what.** Two columns: "Abridge's own peer-reviewed studies" (workflow ease, patient care, after-hours, burnout risk, satisfaction, cognitive load) against "Independent trial" (PDSQI-9 accuracy, thoroughness, abstraction, ICD-10 compliance, NNT). The split is the case study.

**D2 — The note reads better than it thinks.** Seven horizontal bars, PDSQI-9 domains sorted descending, with the three language domains in one colour and the three substance domains in another, and the **0.51** gap annotated.

**D3 — The result that didn't survive.** Two paired bars: note time −21.90 min (survives trimming) against work-outside-work −30.00 min falling to −11.40 min equivalent (does not survive), with **62.00%** attenuation called out.

**D4 — Adoption beats selection.** Two bars: −21.90 minutes (using a tool versus none) against −3.19 minutes (better tool versus worse), annotated **6.87×**.

**D5 — The five-rung ladder.** Days 80–84 with the rung labels from section 38, Day 84 highlighted as the first with independent outcome evidence.

### 47.1 ASCII rendering of D1

```
   ABRIDGE'S OWN STUDIES          |    INDEPENDENT TRIAL (NEJM AI)
   peer reviewed, vendor-linked   |    NIH + health system funded
  --------------------------------+---------------------------------
   Workflow ease           81%    |    PDSQI-9 accuracy        4.44
   Improved patient care   77%    |    Thoroughness            4.57
   Less after-hours work   73%    |    Abstraction             3.97
   Lower burnout risk      67%    |    ICD-10 vs human    6.87/5.94
   Work satisfaction       64%    |    Burnout NNT             1.68
   Cognitive load          -61%   |    Notes scored           7,966
                                  |
   MEASURES THE CLINICIAN         |    MEASURES THE NOTE
   note-accuracy metrics:  0      |    note-accuracy metrics:     1
```

---

## 48. Recommended screenshots and visual assets

1. The NEJM AI methods paragraph naming "Abridge AI, Inc." and stating the documentation-only scope.
2. The PDSQI-9 results paragraph with the seven domain scores.
3. The sensitivity-analysis sentence where the work-outside-work effect attenuates.
4. The Duke JAMIA abstract showing "product A" and "product B."
5. The scoping review's sentence on ASR word error rates by speaker race.
6. The whitepaper title showing the word "Toward," beside the product page's "hallucination-free."

Items 4 and 6 are the strongest single visuals — each is a one-line juxtaposition that makes its own argument. All are public documents.

---

## 49. The category question: is ambient documentation solved?

On the evidence, partly, and the parts divide cleanly.

**Solved.** Producing a readable, well-organised clinical document from a conversation. Comprehensibility **4.99**, organisation **4.90**. This is effectively done, and the remaining variance is not where risk lives.

**Working.** Reducing documentation time during the day (**−21.90 min**) and reducing clinician exhaustion (NNT **1.68**). Replicated across independent and vendor-linked studies with consistent direction.

**Unresolved.** Whether after-hours burden actually falls. Whether the record is complete. Whether quality holds across languages and dialects. Whether oversight replaces production rather than reducing total work.

**Unmeasured.** What share of notes are signed unchanged. What the patient thinks. What happens to review quality over years of use.

A category where the hard technical problem is solved and the hard evaluation problem is untouched is a category at a specific stage: **the engineering has outrun the measurement.** That is where ambient documentation is in 2026, and it is why the most useful work available to a product manager here is instrumentation rather than modelling.

---

## 50. What Abridge does better than Days 80–83

Stated explicitly, because the balance matters.

**It has peer-reviewed research at all.** Two publications, one randomized. Hims & Hers had none. Doximity had none. OpenEvidence had one independent preprint it did not commission.

**It published a real technical methodology.** The confabulation whitepaper has a taxonomy, a training-set size, an annotation budget, a named comparator and a stated result. Day 82's NOHARM citation was a sentence in a CEO quote; this is a document with a method.

**Its scope is honest.** "Documentation-only, no diagnostic or therapeutic decision support" is a restraint claim, and restraint claims are the rarest kind in AI marketing.

**Its incentives align with safety.** Per-clinician licensing means revenue does not rise when clinicians review less carefully. Day 83's advertising model had the opposite property.

**It let itself be studied.** The Wisconsin trial named the product. A company can make that easy or hard, and the deployment, the Epic integration and the operational cooperation made a 24-week randomized trial possible.

That last point deserves the most weight. **The best evidence in this five-day arc exists because the vendor in question was willing to be measured by someone it did not pay.** The criticism in this document is that it has not yet published the measurement itself — which is a much smaller gap than any of the four days before it.

---

## 51. Day 85 connection

Tomorrow is **Eka Care** — and it moves the series from the United States to India, which changes the evidentiary environment entirely.

The last two days established a method for private companies: verify the court record, test claims against each other, name what cannot be checked. Day 84 added a fourth tier — independent peer-reviewed evidence — which turned out to be the richest source available.

India offers a different mix. Company registration data is publicly available through the MCA in a way US private-company data is not, which restores a primary source this arc has been missing since Day 82. The peer-reviewed literature on Indian digital health products is thinner. And the regulatory frame — ABDM, the Digital Personal Data Protection Act — is specific and public.

**The method will shift again, and section 2 of tomorrow's case study will say how.**

---

## 52. A closing note on method

The most useful thing this case study did was search PubMed before searching the company's website.

Four days of this arc had established a pattern — vendors do not publish outcome metrics — and the obvious move on day five was to confirm it a fifth time. Instead the search returned a pre-registered randomized controlled trial, funded by the NIH and a university hospital, that named the product and scored **7,966** unedited notes on a validated instrument.

**The pattern was real and the conclusion drawn from it was wrong.** "No vendor publishes outcome data" is true. "Therefore no outcome data exists" does not follow, and four days of finding absence had made that inference feel safe.

For a product manager evaluating any vendor in a clinical or scientific category, the order is: peer-reviewed literature first, vendor materials second. The literature is slower, older and less flattering, and in this case it was the only place the actual answer lived.

---

## 53. What five days established

| Day | Company | Status | The finding |
|---|---|---|---|
| 80 | Hims & Hers | Public | An AI narrative with no AI metric behind it |
| 81 | Hinge Health | Public | An AI metric measuring cost saved, not health gained |
| 82 | Doximity | Public | AI cost audited; AI claims quote-only |
| 83 | OpenEvidence | Private | No filing; claims tested only when someone sues |
| 84 | Abridge | Private | **Independent trials measure the outcome; the vendor does not publish it** |

Five healthcare AI companies. **Zero vendor-published AI outcome metrics. One product with independent outcome evidence.**

The refined finding, after five days, is sharper than the four-day version:

**Vendors disclose what obligation or competition forces them to disclose. Outcome evidence appears when an academic institution decides to produce it, and that decision has nothing to do with the vendor's commercial incentives.**

Doximity published AI cost because a certified filing required it. Hinge published an automation metric because it made the product look good. Abridge's outcome evidence exists because the University of Wisconsin and the NIH paid for a trial.

**None of the five produced outcome evidence because a customer demanded it** — which is the gap a product manager can actually close, by demanding it.

---

## 54. Open questions for the category

**Why does note-quality measurement require an NIH grant?** The instrument is published and validated. The data sits in every vendor's production system. The cost of running PDSQI-9 on a sample is trivial next to a Series E.

**Who should fund independent evaluation of clinical AI?** Drug evaluation has a regulator and a trial infrastructure. Clinical AI has neither, and the gap is currently filled by whichever academic health system is curious enough to apply for funding.

**Should comparative trials name products?** Two of three do. The one that does not is the most decision-relevant and the least usable. Whatever the reasons, the convention costs buyers real money.

**Does oversight work replace production work?** The displacement-of-burden framework is testable and untested. It is the question that determines whether this category delivers the value it claims.

**What does the patient think?** Five days, five companies, zero patient-reported outcomes anywhere.

---

## 55. Appendix A — source conflicts and reconciliations

Series rule: every conflict is documented, never silently resolved.

### A1. −0.36 hours reported as −21.9 minutes

The NEJM AI trial reports a reduction in note time of **−0.36 hours per day** and describes it in the discussion as **−21.9 minutes**. Multiplying 0.36 by 60 gives **21.60** minutes.

| Measure | Value |
|---|---|
| Gap | **0.30 minutes** |

**Resolution:** the paper is rounding a more precise underlying value (0.365 hours) to two decimal places in the results and converting the unrounded figure in the discussion. Both figures are computed in the gate. The paper's stated **−21.90 minutes** is used in prose, and this note exists so that a reader recomputing from 0.36 is not confused.

### A2. Professional fulfillment: P=0.04 reported as nonsignificant

P=0.04 would be significant at a conventional 0.05 threshold. The trial had two co-primary outcomes and split its type-I error, allocating **0.025** to each — so 0.04 does not clear the threshold and the paper reports it as a nonsignificant increase.

**Not a conflict.** Correct multiplicity control. Documented because a casual reader would reasonably call P=0.04 significant.

### A3. Total funding: $700M in named rounds versus ~$800M claimed

Three named rounds (Series C, D, E) sum to **$700.00M**. Reporting describes approximately **$800M** raised to date.

**Reconciliation:** the **$100.00M** difference is presumably earlier rounds (Series A and B) not itemised in the sources examined. Both figures are computed in the gate. Not treated as a discrepancy.

### A4. The 2026 funding picture is unresolved

A June 2026 announcement described an Eli Lilly strategic investment and an NVIDIA foundation-model collaboration, **with terms undisclosed for both**. A cumulative figure of $1.1B raised appears in a funding database but could not be confirmed against a company release or a primary source; the STAT report is paywalled beyond the announcement.

**Treatment:** the Series E figures are used throughout. The 2026 arrangements are described as announced-without-terms, and no derived figure uses them.

### A5. The Sutter docket

*Washington v. Sutter Health*, No. 4:26-cv-03012 (N.D. Cal.) matches a full-text search for "Abridge AI." **Abridge is not a party.** The underlying documents were not retrieved, so the context in which the term appears is unknown.

**Treatment:** recorded in section 22.2 and asserted in the gate as not characterised. No allegation is described or implied.

### A6. "Independent" and the deploying institution

The Wisconsin trial was funded by University of Wisconsin Hospitals and Clinics and an NIH CTSA — independent of the vendor. The same institution had a concurrent commercial contract with Abridge for operational deployment, which the paper states plainly.

**Treatment:** described as independent of the vendor, which is the relevant sense, with the commercial relationship noted here and in section 36.

### A7. Study design labels

Abridge's JAMIA Open study is a pre/post survey; its Mayo Clinic Proceedings study is a randomized crossover. Summaries sometimes describe both as "peer-reviewed research" without distinguishing design strength.

**Treatment:** both are labelled by design in section 11 and in the gate (`kumc1_design_randomised = False`, `kumc2_design_randomised = True`).

---

## 56. Appendix B — sources examined and not used

**PACER document texts.** Not retrieved. Docket metadata comes from CourtListener's public search API. No complaint text is quoted and no characterisation of any pleading appears in this document.

**The Lukac et al. trial directly.** Described only as cited within the NEJM AI discussion, because the primary source is a preprint that was not retrieved. Its figures are attributed as second-hand in ASSUMPTIONS.md.

**STAT's June 2026 reporting.** Paywalled beyond the announcement. Used only for the fact that a Lilly investment and an NVIDIA collaboration were announced, with terms undisclosed.

**CB Insights, Crunchbase, Dealroom, Sacra.** Aggregators, not primary. Used to locate the $1.1B figure, which is then explicitly not used.

**Vendor review sites and comparison blogs.** Excluded — commercially motivated, no methodology.

**Market data.** Excluded by series rule. Valuation appears only as a company claim.

**The product itself.** Not tested by the author. No first-hand evaluation is claimed.

---

## 57. Methodology

**Source acquisition.** Peer-reviewed literature retrieved through PubMed and PubMed Central, including full text for the NEJM AI trial. Federal docket metadata from the CourtListener public search API, queried 22 September 2026. Company claims from the company's own blog, product pages and whitepaper, plus contemporaneous reporting of the Series E.

**Gate-first discipline.** `verify.py` was written and passing before any prose existed. Every derived figure here is produced by the gate.

**Evidence tiering.** The gate distinguishes four tiers — court record, company claims, vendor-linked peer-reviewed studies, and independent trials — and asserts which tier each finding rests on, so that no sentence can promote a company claim to the standing of a randomized trial.

**Rounding.** Percentages to two decimals, tolerance 0.005 absolute unless stated. Derived figures computed from unrounded inputs.

**Cross-checking.** `crosscheck.py` extracts every two-decimal figure in this README and in ASSUMPTIONS.md and confirms each traces to a gate value. A figure the gate does not produce is a build failure.

**Author constructs.** RICE inputs, stress factors, personas, the North Star proposal, guardrail thresholds, the eval plan, the failure-mode ranking and all scenario parameters are the author's and are labelled as such.

**Fabrication policy.** No figure, quote, date, case number or study result is invented. Where information is unavailable, this document says so.

---

## 58. Reproducing this analysis

```bash
# 1. The independent trial (open access via PMC)
#    Afshar M, et al. NEJM AI 2025;2(12). PMID 41625485. PMC12858090.
#    DOI 10.1056/aioa2500945   ClinicalTrials.gov NCT06517082

# 2. The head-to-head trial
#    Chowdhury A, et al. JAMIA 2026;33(5):990-999. PMID 41729180.
#    DOI 10.1093/jamia/ocag018

# 3. Federal dockets (public, no key required)
curl -A "<your contact>" --get \
  "https://www.courtlistener.com/api/rest/v4/search/" \
  --data-urlencode 'q=party:("Abridge AI, Inc.")' --data-urlencode "type=r"

# 4. Run the gate. 198 checks. Non-zero exit on any failure.
python3 verify.py

# 5. Cross-check the prose against the gate.
python3 crosscheck.py
```

`verify.py` is self-contained and declares every input as a named constant with its source.

---

## 59. Limitations

This analysis rests on three peer-reviewed trials, two reviews, one internal whitepaper, one federal docket and a set of company claims. No audited financials exist and none are used.

No clinical assessment of Abridge is made or implied. This document evaluates the evidence about the product, not the product.

The PDSQI-9 figures come from a single trial at one academic health system, in a predominantly white, English-speaking population, scored by an LLM judge validated against physician ratings. Every one of those qualifiers matters and section 36 states them.

Nothing here asserts that any Abridge claim is false, or that any party to the litigation did anything wrong.

The equity concern is inferred from the technology class, not measured on this product.

---

## 60. References

**Independent peer-reviewed evidence.** According to PubMed:

Afshar M, Baumann MR, Resnik F, et al. "A Pragmatic Randomized Controlled Trial of Ambient Artificial Intelligence to Improve Health Practitioner Well-Being." *NEJM AI* 2025;2(12). PMID 41625485. [DOI](https://doi.org/10.1056/aioa2500945). ClinicalTrials.gov NCT06517082. Funded by University of Wisconsin Hospitals and Clinics and an NIH Clinical and Translational Science Award.

Chowdhury A, Casey M, Wilson J, Pollak KI, Goldstein BA, Bedoya A, Poon EG. "Comparing ambient scribes: a randomized crossover clinical trial addressing ambient scribe technologies' impact on physician burnout." *Journal of the American Medical Informatics Association* 2026;33(5):990-999. PMID 41729180. [DOI](https://doi.org/10.1093/jamia/ocag018).

Wolfe J, Welsh SM. "Ambient Documentation Systems in Emergency Medicine: A Scoping Review of Clinical Precision, Patient Experience, Throughput, and Quality." *Cureus* 2026;18(4):e106643. PMID 42110031. [DOI](https://doi.org/10.7759/cureus.106643).

Sucharitrak C. "Artificial Intelligence and Clinician Burnout in the United States: A Narrative Review." *Cureus* 2026;18(7):e112814. PMID 42465700. [DOI](https://doi.org/10.7759/cureus.112814).

**Vendor-linked peer-reviewed studies.** Albrecht M, et al., *JAMIA Open*, February 2025 (University of Kansas Medical Center, pre/post survey, approximately 100 clinicians). Hudson TJ, et al., *Mayo Clinic Proceedings: Digital Health*, March 2025 (randomized crossover, 40 clinicians, NASA-TLX).

**Company sources.** Abridge, "The Science of Confabulation Elimination: Toward Hallucination-Free AI-Generated Clinical Notes" (internal whitepaper, not peer reviewed). Abridge product and research pages. Series E announcement via Fierce Healthcare, 24 June 2025.

**Federal docket.** *Arslani v. Abridge AI, Inc.*, No. 3:26-cv-50118 (N.D. Ill.), via CourtListener public search API, queried 2026-09-22.

**Series cross-references.** Day 80–83 comparator figures are recomputed inside this case study's own `verify.py` and are not carried across as prose assertions.

---

## 61. Document control

| Field | Value |
|---|---|
| Case study | Day 84 of 90 |
| Subject | Abridge AI, Inc. (private) |
| Method | Independent peer-reviewed evidence + docket record + claim consistency |
| Primary sources | 4 peer-reviewed papers, 2 vendor-linked studies, 1 whitepaper, 1 federal docket |
| Verification checks | **198**, all passing |
| Unverifiable categories asserted | **12** |
| Vendor-published outcome metrics | **0** |
| Independent trials measuring note quality | **1** |
| Diagrams | Markdown tables and ASCII only |
| Fabricated figures | **0** |

---

## 62. Series index

| Day | Company | Central finding |
|---|---|---|
| 80 | Hims & Hers | AI narrative with zero disclosed AI metrics |
| 81 | Hinge Health | Discloses an AI cost metric, not a clinical one |
| 82 | Doximity | AI cost is audited; every AI claim is quote-only |
| 83 | OpenEvidence | No filing exists; the only adversarial test is litigation |
| **84** | **Abridge** | **The evidence exists — the vendor didn't produce it** |
| 85 | Eka Care | *(forthcoming — the series moves to India)* |

---

## 63. Standing questions for Abridge

Ordered by how much the answer would change the assessment.

1. **What share of AI-generated notes are signed with no material edit?** The company has this number today. Nobody has published it.
2. **What is note quality by patient language and dialect?** 28 languages are claimed; quality evidence exists for a population that was 98.1% English-preferring.
3. **What is the confabulation rate in delivered notes**, as opposed to the **97.00%** detection rate of the detector?
4. **What are the commercial terms of the Epic integration**, given that Epic competes in this category?
5. **What happens to the audio after the note is generated** — retention, training use, de-identification standard?

---

## 64. The one-line version

For four days this series asked healthcare AI companies to show evidence that their products work, and found none.

On the fifth day the evidence turned up — in a journal, funded by the NIH, produced by people who do not sell anything.

**That is the good news and the problem in a single sentence.**

---

## 65. Postscript: on being wrong in public

This case study was expected to find what the four before it found. It did not, and the draft structure had to be rebuilt after the literature search came back.

That is worth recording in the document rather than quietly fixing, for two reasons.

The first is that a series which only ever confirms its own thesis is not research, it is a format. Four consecutive findings of absence created a strong prior, and the only thing that broke it was searching a source the previous four days had not needed.

The second is that the correction improved the finding. "Nobody measures AI outcomes in healthcare" is a complaint. "The measurement exists, costs little, and is produced by academics because no commercial actor has a reason to produce it" is a diagnosis — and unlike the complaint, it points at something a buyer can fix by asking for it in a contract.

---

*Day 84 of 90. Built from primary sources. 198 programmatic checks. Zero fabricated figures. One independent randomized trial — which is one more than the four days before it.*
