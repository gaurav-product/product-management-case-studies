# ASSUMPTIONS — Day 86, Hippocratic AI, Inc. (US, private)

Companion to `README.md`. Separates what was **disclosed**, **derived**, **constructed**, **unavailable** and **deliberately excluded**.

This is the first product in the arc with **no human between the AI and the patient**. That raises the evidentiary bar rather than lowering it, and it is why this file separates evidence by *tier* more carefully than any previous day.

Court record and company claims to 24 September 2026; peer-reviewed literature to August 2026; preprints to March 2025.
Verification: `verify.py`, **160 checks, all passing**.

---

## Part 0 — The four evidence tiers

Every finding rests on exactly one, and the README says which.

| Tier | What it is | Standing | Example here |
|---|---|---|---|
| **1. Peer-reviewed** | Externally refereed | Highest available | JMIR Form Res; JAMA Ophthalmol |
| **2. Preprint** | Published, not refereed | Substantive, unchallenged | RWE-LLM; Polaris |
| **3. Court record** | Public docket metadata | Factual; allegations only | *Hippocratic AI v. Health GPT* |
| **4. Company claim** | Asserted, undated, no methodology | Lowest | "115 million... no safety issues" |

```
peer_reviewed_vendor_studies           = 2
peer_reviewed_studies_measuring_safety = 0
safety_evidence_is_preprint_only       = True
independent_non_vendor_safety_study_found = False
```

**The decisive fact about this company's evidence base:** everything peer-reviewed measures something other than safety, and everything measuring safety is a preprint. **No independent, non-vendor safety study was found.**

---

## Part 1 — Disclosed facts

### 1.1 Tier 4 — The marketing claim

Series C announcement via BusinessWire, 3 November 2025: **"completed over 115 million clinical patient interactions with no safety issues."**

Also claimed: partnerships with **over 50** large health systems, payors and pharma clients in **6 countries**; **over 1,000** clinical use cases built; **5 of the top 10** payors and **3 of the top 8** pharma companies; **15 months** post-commercialisation; agents do **not prescribe** and do **not diagnose**; "non-diagnostic patient-facing clinical AI agents"; "Polaris Safety Constellation Architecture."

Funding: Series A $53M at $500M (May 2024); Series B $141M at $1.64B (January 2025); Series C **$126M at $3.5B** (November 2025); **$404M** total raised. Lead investor Avenir Growth; others include CapitalG, General Catalyst, Andreessen Horowitz, Kleiner Perkins, Premji Invest, **Universal Health Services**, **Cincinnati Children's Hospital Medical Center**, **WellSpan Health**, John Doerr, Rick Klausner.

Named health-system partners include Cleveland Clinic, Northwestern Medicine, Ochsner Health, Moffitt Cancer Center, University Hospitals, Guy's & St Thomas' NHS Trust, Advocate Health and Cincinnati Children's.

**No third-party verification, audit methodology, peer-reviewed study, FDA clearance or independent safety validation is referenced in the release.**

From the company research page: "over **7 million** clinical calls"; "**8.95/10** satisfaction rating"; "**5.0T+** parameter constellation architecture" using "**22** models for safety validation". **None carries a date or methodology.**

### 1.2 Tier 2 — The company's own safety research

*Real-World Evaluation of Large Language Models in Healthcare (RWE-LLM): A New Realm of AI Safety & Validation.* medRxiv 2025.03.17.25324157v1. **Preprint, not peer reviewed.**

**Over 307,000 unique calls** evaluated. **6,234 clinicians** — **5,969 nurses**, **265 physicians**. Three-tier review: nursing review first, physician adjudication where necessary. Errors flagged "across multiple severity categories, from minor clinical inaccuracies to significant safety concerns"; precise categorical definitions not specified in the retrieved excerpt.

| Generation | Correct advice | Incorrect, potential minor harm | Severe harm concerns |
|---|---|---|---|
| Pre-Polaris | ~80.0% | 1.32% | 0.06% |
| Polaris 1.0 | 96.79% | 0.13% | 0.10% |
| Polaris 2.0 | 98.75% | — | — |
| Polaris 3.0 | **99.38%** | **0.07%** | **0.00%** |

The approach is described as "resource-intensive"; no formal limitations section appears in the retrieved excerpt.

### 1.3 Tier 2 — The simulated evaluation

*Polaris: A Safety-focused LLM Constellation Architecture for Healthcare.* arXiv:2403.13313, submitted **20 March 2024**. **Preprint, not peer reviewed.**

"One-trillion parameter constellation system" of cooperative agents — a stateful primary agent plus specialist support agents. Evaluated by **over 1,100 US licensed nurses** and **over 130 US licensed physicians** (**1,230+** clinicians) who **posed as patients**. Reports that Polaris "performs on par with human nurses **on aggregate**" across medical safety, clinical readiness, conversational quality and bedside manner. Specialist agents reported to outperform GPT-4 and LLaMA-2 70B; specific figures not given in the abstract.

### 1.4 Tier 1 — Peer-reviewed publications

**Sanz Ausin M, et al.** *JMIR Formative Research* 2026;10:e87704. PMID 42627706. DOI 10.2196/87704. Eight of nine authors Hippocratic AI; one at UBC School of Population and Public Health.

Retrospective analysis of **4,415 AI care agent calls from 4,189 patients**, linear mixed-effects models. Each additional memory associated with **+2.47 minutes** call duration (95% CI 2.03–2.91, p<.001); attenuated to **+0.54 min** in completed calls only (p=.004). **Memory usage showed no significant association with patient satisfaction across any analysis.** Authors note "a disconnect between engagement duration and patient-reported experience" and that the study "may have been underpowered."

**Jacobs A, et al.** *JAMA Ophthalmology* 2026;144(6):563-566. PMID 42133343. DOI 10.1001/jamaophthalmol.2026.1307. Co-authored with Roche and Genentech. Subject: **patient education in ophthalmology**. Abstract not available through PubMed; **cited for existence, venue and authorship only — no result used.**

### 1.5 Tier 3 — Court record

*Hippocratic AI, Inc. v. Health GPT, Inc.*, No. 3:23-cv-04738 (N.D. Cal.). Filed **14 September 2023**, terminated **27 November 2023** (74 days). Cause: **15 U.S.C. §1051 trademark infringement**. Judge Rita F. Lin. Munjal Shah named as a party. Hippocratic AI is **plaintiff**. **No product liability or patient-harm litigation identified.**

---

## Part 2 — Derived figures

Computed by `verify.py`.

### 2.1 The central arithmetic

| Figure | Value |
|---|---|
| **Incorrect rate at Polaris 3.0** | **0.62%** |
| Improvement in correct advice, pre-Polaris to 3.0 | **+19.38pp** |
| Reduction in minor-harm rate | **94.70%** |
| Peak severe-harm rate across generations | **0.10%** |
| Implied interactions with incorrect advice at 115M | **713.00 thousand** |
| Implied interactions with minor-harm potential at 115M | **80.50 thousand** |

### 2.2 The rule of three

| Figure | Value |
|---|---|
| **Safety-study coverage of claimed volume** | **0.27%** |
| Interactions not examined | **114.69 million** |
| Claimed volume ÷ studied volume | **374.59×** |
| 95% upper bound on the severe-event rate | **0.000977%** |
| As a frequency | **1 in 102,330** |
| **Implied severe events across 115M at that bound** | **1,123.78** |

```
zero_severe_events_observed_in_study            = True
study_licenses_claim_of_zero_across_full_volume = False
absence_of_evidence_equals_evidence_of_absence  = False
```

### 2.3 Study composition

| Figure | Value |
|---|---|
| Nurse share of RWE-LLM clinicians | **95.75%** |
| Calls per clinician | **49.25** |
| Nurse share of Polaris evaluators | **89.43%** |

### 2.4 The peer-reviewed study

| Figure | Value |
|---|---|
| Calls per patient | **1.05** |
| Duration effect CI width | **0.88** |
| **Attenuation, all calls to completed only** | **78.14%** |

### 2.5 Claim consistency

| Figure | Value |
|---|---|
| Interactions ÷ calls | **16.43×** |
| Difference | **108.00 million** |
| Parameter claim gap | **4.00 trillion** (**5.00×**) |
| Satisfaction as share of scale | **89.50%** |

### 2.6 Commercial

| Figure | Value |
|---|---|
| Three named rounds | **$320.00M** |
| Not attributed to named rounds | **$84.00M** |
| Valuation multiple since Series A | **7.00×** |
| Valuation per claimed customer | **$70.00M** |
| Valuation per claimed interaction | **$30.43** |
| Investor-customers as share of claimed customers | **6.00%** |
| Claimed interactions per month | **7.67 million** |
| Claimed use cases per customer | **20.00** |

---

## Part 3 — Author constructs

**None of the following is disclosed data.**

### 3.1 Frameworks

RICE, MoSCoW, Kano, JTBD, AARRR, HEART, Porter's Five Forces, SWOT and the PRD in section 31 are applied by the author.

### 3.2 RICE inputs

| ID | R | I | C | E | Stress |
|---|---|---|---|---|---|
| P1 | 115 | 3.0 | 0.95 | 2.0 | 0.95 |
| P2 | 115 | 3.0 | 0.90 | 3.0 | 0.90 |
| P3 | 115 | 2.5 | 0.80 | 5.0 | 0.85 |
| P4 | 115 | 3.0 | 0.65 | 9.0 | 0.60 |
| P5 | 115 | 2.5 | 0.55 | 12.0 | 0.45 |

Reach held at 115 (millions of **claimed** interactions — itself an unverified, undefined figure, which is a limitation of the model). **P5 ranks last under stress by 60.33%**, asserted programmatically. Base and stressed rankings identical.

### 3.3 The rule-of-three application

The **calculation** is standard statistics. The **application** — treating the 307,000-call study as a sample from the 115-million-interaction population — is the author's, and it assumes the study population is representative of the deployment. **Nothing in the retrieved sources describes the sampling frame**, so this assumption is stated rather than verified. Section 33 says so.

The choice of the rule-of-three approximation over the exact binomial bound is documented in Appendix A5; the difference is negligible at n = 307,000.

### 3.4 Applying a call-level rate to an interaction-level count

Section 7.3's implied counts apply an error rate measured on **calls** to a claimed count of **interactions**. The two units are not defined by the company and may differ materially. **This is the most consequential assumption in the case study** and is flagged in section 33 and Appendix A2.

### 3.5 Personas

Mrs. Dolores K. and Sandra P. are **composite constructions** — not real people, not customer research. The third "persona," the displaced nurse, is a framing device rather than a user.

### 3.6 North Star and guardrails

"Adjudicated adverse-event rate per 100,000 interactions" is the author's proposal. The **1.00%** coverage floor is the author's; the **0.27%** current figure is derived from company sources.

### 3.7 Scenarios, eval plan, failure modes, human-in-the-loop

Sections 25, 26, 27 and 42 are the author's product judgement. No clinical expertise is claimed. The failure-mode ranking is by the author's estimate of expected harm. The assertion in section 26 that failure to escalate "does not appear as an error in a correctness taxonomy" is an inference about the taxonomy, whose definitions were not retrieved.

### 3.8 The counterfactual argument

Section 40's argument that the product is *probably* net-beneficial against a no-call baseline is the author's reasoning, **not a measured finding**. No study comparing called against uncalled patients was found, and the section says so.

### 3.9 Interpretive framings

The "inverted evidence pyramid" (section 22), the "measurement and communication are separate failures" synthesis (section 51), the seven-rung ladder and the arc reframing (section 63) are the author's.

---

## Part 4 — Unavailable information

| Not available | Consequence |
|---|---|
| Definition of "safety issue" | **The central claim cannot be checked** |
| Adverse-event detection method outside sampling | No independent signal exists |
| Escalation-to-human rate | The scope limit's enforcement is unmeasured |
| Whether patients know they are speaking to an AI | Consent and calibration unassessable |
| RWE-LLM sampling frame and blinding | Representativeness unverifiable |
| Revenue, ARR, margin, cost per interaction | No commercial assessment |
| Headcount, churn, retention, pricing | — |
| Actual interaction volume, independently | Only company claims exist |
| Clinical outcomes — readmission, adherence | Net benefit unmeasured |
| What happened to displaced nursing hours | The labour question is unexamined |

---

## Part 5 — Deliberate exclusions

| Excluded | Reason |
|---|---|
| PACER document texts | Not retrieved; docket metadata only, no pleading characterised |
| RWE-LLM full methods section | Abstract and results only; **absence from this analysis is a limitation, not an assertion** |
| Polaris full paper | Abstract only; GPT-4 and LLaMA-2 comparison figures not used |
| JAMA Ophthalmology full text | Not available via PubMed; cited for existence only |
| Contrary Research, CB Insights, PitchBook, aiwiki | Aggregators, not primary |
| Vendor review and comparison sites | Commercially motivated, no methodology |
| Market data | Series rule; valuation appears only as a company claim |
| The product itself | Not tested by the author |

### 5.1 Three false-match dockets

A full-text search returned four dockets; three are unrelated — *AAUP v. Rubio*, *Groq, Inc. v. Groq Health, Inc.*, and *China Central Television v. Create New Technology HK Limited*. Discarded before any figure was derived. Documented in Appendix A7.

### 5.2 On the Days 80–85 comparators

Day 80's **59.43%**, Day 81's **97%**, Day 82's **94.95%**, Day 83's **23.00%**, Day 84's **4.62** and **4.44**, and Day 85's **23.96%** are **recomputed inside this case study's own `verify.py`** rather than carried across as prose.

---

## Part 6 — Fairness statement

This case study is hard on a company that measures more than any of the six before it, and that requires justification rather than apology.

**The bar moves with the product.** When a clinician signs every note, a measurement gap is a reporting problem — the clinician is still there. When an AI speaks to a patient alone, the measurement **is** the safety system.

**The company deserves specific credit.** It published a safety study on 307,000 real calls with 6,234 clinicians. It reported a metric that moved the wrong way — severe-harm concerns rising from 0.06% to 0.10% between architecture generations. It states an explicit non-diagnostic scope limit. It has cleared peer review in JAMA Ophthalmology. Its correct-advice trajectory from ~80% to 99.38% is substantial, real engineering progress.

**Nothing here asserts that any patient was harmed**, that any claim is false, or that the product is unsafe. The **1,123.78** figure is an upper bound on what the evidence cannot exclude — **not an estimate that a thousand events occurred**, and section 33 states this explicitly.

**Section 40 runs the counterfactual in the company's favour** and concludes the product is probably net-beneficial, because the honest comparator is a call that never happens rather than a careful nurse.

**The criticism is narrow and specific:** the safety claim in the marketing is not the safety finding in the research; the coverage is 0.27%; and nothing about safety has been peer reviewed or externally audited. Three of the five recommendations cost almost nothing and could ship this quarter.

---

## Verification statement

`verify.py` contains **160 checks** and exits non-zero on any failure. It asserts the structural absence of a human intermediary; the marketing claim and its missing definition; every figure in the company's safety preprint including the non-zero error rate and the severe-harm regression; the rule-of-three upper bound and the explicit assertion that the study does not license the population-level claim; the simulated nature of the Polaris evaluation; both peer-reviewed studies and the zero count of peer-reviewed safety studies; the volume and parameter claim inconsistencies; the funding and investor-customer structure; the court record; the Days 80–85 comparators; the RICE base and stressed rankings with the proposal ranking last under stress named by the gate; and the fourteen unverifiable categories.

`crosscheck.py` independently extracts every two-decimal figure from `README.md` and `ASSUMPTIONS.md` and confirms each traces to a gate value.

**Fabricated figures: 0.**
**Peer-reviewed studies measuring safety: 0.**
**Share of claimed interactions any clinician has reviewed: 0.27%.**

---

*Day 86 of 90. Hippocratic AI, Inc. Court record and company claims to 24 September 2026; literature to August 2026.*
