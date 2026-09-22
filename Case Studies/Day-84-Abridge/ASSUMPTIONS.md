# ASSUMPTIONS — Day 84, Abridge AI, Inc. (private)

Companion to `README.md`. Separates what was **disclosed**, **derived**, **constructed**, **unavailable** and **deliberately excluded**.

Abridge is private, so the Day 83 method applies. But Day 84 has something no earlier day in this arc had: **a substantial body of independent, peer-reviewed, randomized evidence**, including one trial that names the product, was funded by a university hospital and an NIH award, was pre-registered, and measured documentation quality on a validated instrument.

That changes what this file has to track. It is no longer enough to separate "claim" from "fact" — this study also has to separate **who produced each piece of evidence and who paid for it.**

Court record to 22 September 2026; peer-reviewed literature to July 2026; company claims to June 2026.
Verification: `verify.py`, **198 checks, all passing**.

---

## Part 0 — The four evidence tiers

Every finding in the README rests on exactly one of these, and the README says which.

| Tier | What it is | Weight | Example in this study |
|---|---|---|---|
| **1. Independent trial** | Randomized, peer reviewed, externally funded | Highest | NEJM AI: PDSQI-9 on 7,966 notes; NNT 1.68 |
| **2. Vendor-linked study** | Peer reviewed, but the vendor has an interest | High | JAMIA Open, Mayo Clin Proc Digit Health |
| **3. Court record** | Public docket metadata | Factual, but allegations only | *Arslani v. Abridge AI* |
| **4. Company claim** | Asserted by the company, unchecked | Lowest | 150+ health systems, 50M conversations |

The gate asserts the tier boundaries:

```
note_quality_measured_by_vendor              = False
note_quality_measured_by_independent_trial   = True
vendor_linked_studies_reporting_note_accuracy = 0
independent_studies_reporting_note_accuracy   = 1
day82_requested_metric_now_exists             = True
day82_requested_metric_published_by_vendor    = False
```

---

## Part 1 — Disclosed facts

### 1.1 Tier 1 — The independent randomized trial — VERIFIED

Afshar M, et al., *NEJM AI* 2025;2(12). PMID 41625485. DOI 10.1056/aioa2500945. NCT06517082, registered 9 August 2024. Funded by University of Wisconsin Hospitals and Clinics and an NIH CTSA. Retrieved via PubMed/PMC. **Names Abridge AI, Inc. explicitly.**

**Design.** 24-week, stepped-wedge, individually randomized pragmatic trial. 66 practitioners, three 6-week sequences, 1:1:1 stratified permuted-block randomization, ambulatory clinics across two states and eight specialties. Statistical analysis plan, analysis code and survey data posted publicly.

**Scale.** 71,487 notes authored; 27,092 ambient-generated; 44,395 human-authored. Note-weighted mean utilisation 71.0% (SD 31.6). Survey completion 99.70% (n=329). Patient consent rate 99.92%; 22 patients declined; no recording-related complaints documented.

**Co-primary outcomes.** Work exhaustion/interpersonal disengagement −0.44 points (95% CI −0.62 to −0.25; P<0.001). Professional fulfillment +0.14 points (95% CI 0.004 to 0.28; P=0.04), reported as **nonsignificant** against an alpha of 0.025 per co-primary outcome. NNT 1.68 (95% CI 1.55–1.82); ARR 0.60. Above the burnout threshold: 56.1% at baseline, 35.4% at end. Above the high-fulfillment threshold: 25.8% to 41.5%.

**Efficiency.** Time on notes −0.36 h/day (95% CI −0.55 to −0.17), stated as −21.9 minutes; survives trimming. Work outside work −0.50 h/day (95% CI −0.90 to −0.09); **attenuates to −0.19 h (95% CI −0.40 to 0.03) and loses significance** after excluding the top 3% of observations.

**ICD-10 coding compliance.** 6.87 (95% CI 6.76–6.98) for ambient notes versus 5.94 (95% CI 5.81–6.07) for human-authored, scale 0–10, P<0.001, adjudicated by certified health-system coders. Sample 6,110 notes, 50.4% ambient.

**Documentation quality — PDSQI-9.** 7,966 randomly sampled notes, **scored in unedited form before practitioner review**:

| Domain | Score | SD |
|---|---|---|
| Comprehensibility | 4.99 | 0.13 |
| Organisation | 4.90 | 0.16 |
| Usefulness | 4.83 | 0.51 |
| Succinctness | 4.63 | 0.55 |
| Thoroughness | 4.57 | 0.68 |
| Accuracy | 4.44 | 0.93 |
| Abstraction | 3.97 | 0.58 |

Stigmatising language in 12 notes. Mean input 6,559 tokens (SD 2,436); output 1,953 tokens (SD 334). **Scoring used an LLM-as-a-judge implementation validated against physician ratings — not physicians scoring directly.**

**Drift.** No drift events across 15 sequential one-month rolling windows.

**Population.** Practitioners 78.8% female, median age 42.5, 89.4% non-Hispanic white, 72.7% physicians, 45.5% family medicine, median 14 years in practice, median 50 patients/week. Patients 88.4% non-Hispanic white, 98.1% English preferred, 92.1% in person. Seven practitioners showed low fidelity; three never initiated use.

### 1.2 Tier 1 — The head-to-head trial — VERIFIED

Chowdhury A, et al., *JAMIA* 2026;33(5):990-999. PMID 41729180. DOI 10.1093/jamia/ocag018.

Open-label randomized crossover, 160 outpatient clinicians at a tertiary academic medical centre, 136 surveys analysed. Satisfaction improvement: product A +1.91, product B +2.51 on a 7-point scale; mean difference 0.60 (95% CI 0.32–0.90). Minutes in notes: B − A = −3.19 (95% CI −4.87 to −1.50). Both tools reduced burnout; differences between tools not meaningful. Pajama time largely unaffected.

**The products are anonymised as A and B.**

### 1.3 Tier 1 — Reviews — VERIFIED

Wolfe J, Welsh SM, *Cureus* 2026;18(4):e106643. PRISMA-ScR scoping review, OSF-registered, 27 sources. Finds **significant racial and dialect-based disparities in the ASR systems underpinning ambient documentation, with higher word error rates for Black speakers than White speakers**, and that ambient systems may shift rather than eliminate documentation effort.

Sucharitrak C, *Cureus* 2026;18(7):e112814. Narrative review weighting by study design. Proposes **"displacement of burden"**: tasks move from production to oversight, and potentially from physicians to nurses and assistants.

### 1.4 Tier 2 — Vendor-linked peer-reviewed studies

**Albrecht M, et al., *JAMIA Open*, February 2025.** Pre/post surveys, approximately 100 clinicians, University of Kansas Medical Center. 81% found the workflow easy; 77% felt improved patient care; 73% reported decreased after-hours documentation; 67% felt less burnout risk; 64% reported increased satisfaction. Reported as seven times more likely to find workflow easy; five times more likely to believe notes could be completed before the next visit. **Design: pre/post survey, no control, self-reported.**

**Hudson TJ, et al., *Mayo Clinic Proceedings: Digital Health*, March 2025.** Randomized crossover, 40 ambulatory clinicians, NASA-TLX. **61% reduction in cognitive load.**

**Neither reports any measure of note accuracy.**

### 1.5 Tier 3 — Court record — VERIFIED

*Arslani v. Abridge AI, Inc.*, No. 3:26-cv-50118 (N.D. Ill.), filed 23 March 2026, Judge Iain D. Johnston. Cause: 18 U.S.C. §1836(b), Defend Trade Secrets Act. Jury demanded by both. Amended complaint 3 April 2026. Open. **Abridge is the defendant.** No cases as plaintiff.

*Washington v. Sutter Health*, No. 4:26-cv-03012 (N.D. Cal.) matches a full-text search for "Abridge AI." **Abridge is not a party.** Not characterised anywhere in this study.

### 1.6 Tier 4 — Company claims — NOT VERIFIED

Internal whitepaper, *The Science of Confabulation Elimination: Toward Hallucination-Free AI-Generated Clinical Notes* (**not peer reviewed**): five support categories, three severity levels, detection model trained on 50,000+ examples, internal benchmark of 10,000+ realistic clinical encounters, 1,000+ hours of board-certified physician annotation. Result: *"catching 97% of the confabulations, while GPT-4o only catches 82%."*

Series C $150M (Feb 2024); Series D $250M (Feb 2025); Series E $300M at $5.3B (June 2025); approximately $800M raised to date. 150+ health systems, 55 specialties, 28 languages, a projected 50 million medical conversations for the year, a proprietary dataset of 1.5M+ encounters, Johns Hopkins 6,700 clinicians, Mayo approximately 2,000. "78% of clinicians feel improved work satisfaction" (Sutter Health case study, **no methodology stated**). KLAS 2025 and 2026 market leader. Epic distribution via private and FHIR R4 APIs.

---

## Part 2 — Derived figures

Computed by `verify.py`.

### 2.1 Trial scale and outcomes

| Figure | Value |
|---|---|
| Ambient share of notes | **37.90%** |
| Human-authored share | **62.10%** |
| Exhaustion effect ÷ fulfillment effect | **3.14×** |
| Burnout threshold change | **−20.70pp** (**36.90%** relative) |
| Fulfillment threshold change | **+15.70pp** (**60.85%** relative) |
| Work-outside-work attenuation after trimming | **62.00%** |
| ICD-10 difference | **0.93** (**15.66%** relative) |
| Non-utilisation | **29.00%** |
| Low-fidelity practitioners | **10.61%** |
| Never initiated | **4.55%** |

### 2.2 PDSQI-9

| Figure | Value |
|---|---|
| Mean across seven domains | **4.62** |
| Range | **1.02** |
| Lowest domain | **abstraction** |
| Highest domain | **comprehensibility** |
| Accuracy as share of scale | **88.80%** |
| Abstraction as share of scale | **79.40%** |
| Comprehensibility as share of scale | **99.80%** |
| **Language-domain mean** | **4.84** |
| **Substance-domain mean** | **4.33** |
| **Gap** | **0.51** |
| Stigmatising-language share | **0.15%** |
| Token compression ratio | **3.36×** |

### 2.3 Cross-trial comparison

| Figure | Value |
|---|---|
| JAMIA response rate | **85.00%** |
| Satisfaction difference as share of scale | **8.57%** |
| Use-versus-none ÷ better-versus-worse | **6.87×** |
| Utilisation gap, Wisconsin vs Lukac | **41.00pp** (**2.37×**) |
| Lukac product gap | **23.00 seconds** |
| Independent trials naming products | **2 of 3** (**66.67%**) |

### 2.4 Vendor studies and whitepaper

| Figure | Value |
|---|---|
| Mean of the five self-reported KUMC percentages | **72.40%** |
| Spread, highest to lowest | **17.00pp** |
| Confabulation detection advantage | **15.00pp** (**18.29%** relative) |
| **Confabulations missed by the detector** | **3.00%** |

### 2.5 Equity and company claims

| Figure | Value |
|---|---|
| Non-English encounters in the trial | **1.90%** |
| Non-white patients | **11.60%** |
| Non-white practitioners | **10.60%** |
| Conversations per health system per year | **333.33 thousand** |
| Dataset as share of one year's volume | **3.00%** |
| Valuation per claimed health system | **$35.33M** |
| Funding not attributed to named rounds | **$100.00M** |

---

## Part 3 — Author constructs

**None of the following is disclosed data.**

### 3.1 Frameworks

RICE, MoSCoW, Kano, JTBD, AARRR, HEART, Porter's Five Forces, SWOT and the PRD in section 34 are applied by the author. Abridge publishes none of them.

### 3.2 RICE inputs

| ID | R | I | C | E | Stress |
|---|---|---|---|---|---|
| P1 | 150 | 3.0 | 0.90 | 3.0 | 0.95 |
| P2 | 150 | 3.0 | 0.70 | 9.0 | 0.60 |
| P3 | 150 | 2.5 | 0.85 | 5.0 | 0.90 |
| P4 | 150 | 2.5 | 0.80 | 4.0 | 0.85 |
| P5 | 150 | 2.0 | 0.60 | 10.0 | 0.50 |

Reach held at 150 — the **claimed** health-system count, itself an unverified number, which is a limitation of the model. **P5 ranks last under stress by 57.14%**, asserted programmatically. Base and stressed rankings are identical.

### 3.3 Personas

Dr. James O. and Dr. Priya N. are **composite constructions** — not real people, not customer research. Dr. James O.'s parameters are drawn from the trial's reported median participant (family medicine, 50 patients/week, 14 years in practice) to keep the persona tethered to evidence rather than invention.

### 3.4 North Star and guardrails

"Unedited-note acceptance rate" is the author's proposal, carried forward from Day 82. The PDSQI-9 accuracy floor of **4.50**, the abstraction guardrail and the equity guardrail are the author's. The current values (accuracy **4.44**, abstraction **3.97**) are from the trial, not from the company.

### 3.5 Scenarios and sensitivity

Sections 44 and 45 apply arithmetic to published results and are author constructs. The 4.50 floor is arbitrary and illustrative. The claim in 44.3 that implementation quality may dominate model quality is **an inference from two trials with different utilisation rates**, not a measured finding — the trials differed in product, site and population as well as in implementation.

### 3.6 Eval plan, failure modes, human-in-the-loop, playbook

Sections 27, 28 and 29 are the author's product judgement. No clinical expertise is claimed. The failure-mode ranking is by the author's estimate of expected harm.

### 3.7 Recommendations, roadmap and interpretive framings

All six recommendations, the MoSCoW allocation and the three-horizon roadmap are the author's. The "language scores above substance" framing in section 9.2 is the author's interpretation of the trial's domain scores — the trial reports the scores and does not group them this way.

### 3.8 The ladder and the category synthesis

The five-rung ladder (section 38), the five-day synthesis (section 53) and the open category questions (section 54) are the author's framing of a pattern across five unrelated companies. Interpretation, not a disclosed relationship.

---

## Part 4 — Unavailable information

| Not available | Consequence |
|---|---|
| Revenue, ARR, margin, cost per encounter | No unit economics possible |
| Headcount, churn, retention, contract pricing | Commercial position unassessable |
| 2026 funding terms; Eli Lilly investment size | Section 19 uses Series E figures only |
| Epic integration commercial terms | The largest undisclosed strategic fact |
| Audio retention, training use, de-identification standard | Privacy position unassessable |
| **Unedited-note acceptance rate** | **The metric that describes what reaches the chart** |
| Note quality by language, dialect or patient race | The equity question is unanswerable |
| Confabulation rate in delivered notes | Only detector recall is published |
| Review duration and edit rates in production | The safety gate is uninstrumented in public |
| Patient-reported outcomes | Nobody has measured the recorded party's experience |

---

## Part 5 — Deliberate exclusions

| Excluded | Reason |
|---|---|
| PACER document texts | Not retrieved. Docket metadata only; **no complaint text quoted, no pleading characterised** |
| The Lukac et al. preprint directly | Described only as cited within the NEJM AI discussion; figures attributed as second-hand |
| STAT's June 2026 reporting beyond the announcement | Paywalled |
| CB Insights, Crunchbase, Dealroom, Sacra | Aggregators, not primary. The $1.1B figure located there is explicitly **not used** |
| Vendor review and comparison blogs | Commercially motivated, no methodology |
| Market data | Series rule. Valuation appears only as a company claim |
| The product itself | Not tested by the author; no first-hand evaluation claimed |

### 5.1 On the Days 80–83 comparators

Day 80's **59.43%**, Day 81's **97%**, Day 82's **94.95%** and zero audited AI claims, and Day 83's **23.00%** discordance and zero confirmed claims are **recomputed inside this case study's own `verify.py`** rather than carried across as prose. No case study asserts a number its own gate has not verified.

---

## Part 6 — Fairness statement

This case study is more favourable to its subject than any of the four before it, and the reasons should be explicit.

**Abridge has more independent evidence behind it than any company in this arc.** One randomized trial names it, measures note quality on a validated instrument, and reports a burnout NNT of 1.68. That is a strong result and this document says so.

**Its own research is real.** Two peer-reviewed publications, one randomized. The criticism is about what they measure, not about their integrity.

**Its incentives are structurally better than Day 83's.** Per-clinician licensing means revenue does not rise when clinicians review less carefully.

**It let itself be studied.** The best evidence in this arc exists partly because the vendor cooperated with a trial it did not fund and could not control the outcome of.

**Nothing here asserts that any Abridge claim is false**, or that any party to the litigation did anything wrong. The critique is narrow: the outcome evidence was produced by academics, the vendor does not publish the equivalent, and the metric that describes what reaches the patient's chart is measured by nobody.

**Section 40 runs the counterfactual** in which the vendor publishes everything, and finds most of the structural argument survives — which is the test of whether a critique is about the company or about the system it operates in.

---

## Verification statement

`verify.py` contains **198 checks** and exits non-zero on any failure. It asserts the independent trial's design, scale, co-primary outcomes, NNT, efficiency results and sensitivity analysis; all seven PDSQI-9 domains and the language-versus-substance grouping; the LLM-judge caveat; the head-to-head trial's results and its product anonymisation; the three-trial naming practice; both vendor-linked studies and their zero note-accuracy count; the whitepaper's detection rates and the distinction between detection recall and note cleanliness; the equity population figures; the court record; the company claims; the Days 80–83 comparators; the RICE base and stressed rankings with the proposal ranking last under stress named by the gate; and the twelve unverifiable categories.

`crosscheck.py` independently extracts every two-decimal figure from `README.md` and `ASSUMPTIONS.md` and confirms each traces to a gate value.

**Fabricated figures: 0.**
**Vendor-published outcome metrics: 0.**
**Independent trials measuring the outcome: 1 — which is the finding.**

---

*Day 84 of 90. Abridge AI, Inc. (private). Court record to 22 September 2026; literature to July 2026; company claims to June 2026.*
