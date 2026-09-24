# Day 86 — Hippocratic AI, Inc. (private)

### "No safety issues" in 115 million interactions. The company's own research says otherwise.

> **90-Day PM Case Study Challenge — Day 86**
> Evidence-based product teardown built only from primary sources.
> Every derived figure is produced by `verify.py` (160 programmatic checks) before a word of prose was written.

---

## 1. One-paragraph summary

Every company in this arc so far has had a human standing between the model and the patient — a clinician signing a note, a physician reading an answer, a patient reading their own record. That human was the safety argument. Hippocratic AI's agents speak to patients directly, by voice, with **no intermediary**. So safety cannot be argued; it has to be measured. The company's Series C announcement says it has "completed over **115 million** clinical patient interactions **with no safety issues**." The company's own safety research says something different: evaluating **307,000** calls with **6,234** clinicians, it reports correct medical advice at **99.38%** — meaning **0.62%** not correct — with incorrect advice carrying potential minor harm at **0.07%** and severe-harm concerns at **0.00%**. The two statements reconcile only if "no safety issues" means "no *severe* harm." And a zero observed in 307,000 calls, by the standard treatment of zero-event data, is statistically compatible with as many as **1,124** severe events across 115 million. The safety study covers **0.27%** of the claimed volume. Two peer-reviewed papers exist; **neither measures safety.**

---

## 2. The structural fact that changes everything

| Day | Company | Who stands between the AI and the patient |
|---|---|---|
| 80 | Hims & Hers | A clinician prescribes |
| 81 | Hinge Health | A clinician supervises |
| 82 | Doximity | A clinician signs the note |
| 83 | OpenEvidence | A physician reads the answer |
| 84 | Abridge | A clinician signs the note |
| 85 | Eka Care | The patient reads their own record |
| **86** | **Hippocratic AI** | **Nobody** |

```
day86_has_human_intermediary        = False
day86_agent_speaks_to_patient_directly = True
```

In every previous case, when this series asked "what if the AI is wrong?", the answer was a person. Day 84's entire analysis turned on whether the clinician's review was load-bearing or ceremonial — but the review existed.

Here the AI calls a patient and talks to them. Whatever it says, the patient hears. **The human-in-the-loop argument is unavailable, and that raises the evidentiary bar rather than lowering it.**

### 2.1 The company's scope limitation is real and matters

```
agents_prescribe = False
agents_diagnose  = False
scope_is_non_diagnostic_patient_facing = True
```

Hippocratic AI states that its agents do not prescribe and do not diagnose, and describes the product as "non-diagnostic patient-facing clinical AI agents." That is a genuine and deliberate restraint, and it is the single most important safety design decision in the product.

It is also not a complete defence. A non-diagnostic agent can still tell a patient something wrong about their medication schedule, misunderstand a described symptom, fail to escalate when escalation was warranted, or reassure someone who needed to be alarmed. **The scope limit constrains the worst case; it does not eliminate the case.**

---

## 3. Company identification

| Field | Value | Source |
|---|---|---|
| Legal name | Hippocratic AI, Inc. | Federal docket |
| Status | **Private** — no public filings | — |
| Founder / CEO | Munjal Shah | Docket; company |
| Headquarters | Palo Alto, California | JMIR author affiliation |
| Product | Voice AI agents for non-diagnostic patient-facing clinical tasks | Company |
| Architecture | "Polaris Safety Constellation" | Company |
| Total raised | **$404M** claimed | Series C release |
| Valuation | **$3.5B** (Series C, Nov 2025) | Series C release |

As on Days 83, 84 and 86, there is no statutory register entry available for a US private company — the thread Day 85 briefly restored via India's CIN system goes dark again.

---

## 4. What the product actually does

An AI agent telephones a patient and holds a conversation: medication reminders, pre-operative instructions, post-discharge check-ins, chronic care follow-up, screening outreach. The company claims **over 1,000 clinical use cases** built across **more than 50** health systems, payors and pharma clients in **6 countries**.

| Derived | Value |
|---|---|
| Claimed use cases per customer | **20.00** |
| Claimed interactions per month since commercialisation | **7.67 million** |
| Share of the top 10 US payors claimed as customers | **50.00%** |
| Share of the top 8 pharma companies claimed | **37.50%** |

### 4.1 Why "non-diagnostic" is doing the regulatory work

A product that diagnoses or recommends treatment approaches FDA device regulation. A product that reminds a patient to take their medication does not. The scope limitation is simultaneously a safety design, a regulatory posture and a market constraint — and the company is explicit about it, which is to its credit.

**The boundary is narrower than it sounds, though.** The gap between "your appointment is Tuesday" and "that sounds like it's probably fine" is a single conversational turn, and it is the model that decides which one it produces.

---

## 5. Problem statement

The problem is real and large. Health systems cannot staff the volume of patient outreach that good care requires: pre-op calls go unmade, discharge follow-ups are skipped, chronic care check-ins happen quarterly instead of weekly, and screening outreach reaches a fraction of the eligible population. Nursing shortages make this worse every year.

An agent that can make unlimited calls at near-zero marginal cost addresses that directly, and the potential benefit is genuine — a patient who gets a post-discharge call they would otherwise not have received is better off, provided the call is correct.

**That last clause is the whole case study.**

---

## 6. The claim

From the Series C announcement, 3 November 2025:

> "completed over 115 million clinical patient interactions with no safety issues"

```
claim_interactions_m             = 115.0
claim_safety_issues              = 0
safety_claim_third_party_verified = False
safety_claim_defines_safety_issue = False
fda_clearance_referenced          = False
```

Three things are absent from the claim and from the release containing it: **a definition of "safety issue," a description of how safety issues would be detected, and any third-party verification.**

A zero is the most demanding number a company can publish. It is also the easiest to produce, because there are three ways to get one: the thing genuinely never happened, the definition is narrow enough that nothing qualifies, or nothing is looking.

The rest of this case study establishes which.

---

## 7. What the company's own safety research says

Hippocratic AI published a safety study: *Real-World Evaluation of Large Language Models in Healthcare (RWE-LLM): A New Realm of AI Safety & Validation*, on medRxiv.

```
rwe_peer_reviewed = False
```

It is a **preprint, not peer reviewed**. It is also substantive, and publishing it deserves credit — most companies in this position publish nothing.

| Measure | Value |
|---|---|
| Unique calls evaluated | **307,000** |
| Clinicians engaged | **6,234** |
| — nurses | 5,969 (**95.75%**) |
| — physicians | 265 |
| Calls per clinician | **49.25** |

Review is described as three-tier: nursing review first, physician adjudication where necessary.

### 7.1 The results

| Architecture generation | Correct medical advice | Incorrect, potential **minor** harm | **Severe** harm concerns |
|---|---|---|---|
| Pre-Polaris | ~80.00% | 1.32% | 0.06% |
| Polaris 1.0 | 96.79% | 0.13% | 0.10% |
| Polaris 2.0 | 98.75% | — | — |
| **Polaris 3.0** | **99.38%** | **0.07%** | **0.00%** |

| Derived | Value |
|---|---|
| Improvement in correct advice, pre-Polaris to 3.0 | **+19.38pp** |
| Reduction in minor-harm rate | **94.70%** |
| **Incorrect rate at Polaris 3.0** | **0.62%** |

The trajectory is genuinely impressive. Correct advice rising from roughly 80% to **99.38%** across three architecture generations is real engineering progress, measured on real calls, adjudicated by thousands of clinicians. This is more safety measurement than any other company in this seven-day arc has published.

### 7.2 And it is not zero

```
company_research_reports_nonzero_error_rate = True
no_safety_issues_consistent_with_all_errors = False
no_safety_issues_consistent_with_severe_only = True
```

**99.38% correct means 0.62% not correct.** The company's own research reports a non-zero error rate at its current architecture generation.

So "no safety issues" is reconcilable with the company's own data **only** if "safety issue" means severe harm specifically — the one category the study reports at **0.00%**.

That is a defensible definition. It is also not what the sentence says, and the sentence does not define the term.

### 7.3 What the stated rates imply at the claimed volume

If the Polaris 3.0 rates held across the claimed 115 million interactions:

| Measure | Implied count |
|---|---|
| Interactions with incorrect medical advice (0.62%) | **713,000** |
| Interactions with incorrect advice carrying potential minor harm (0.07%) | **80,500** |

These are not predictions and the gate does not treat them as measurements — the 307,000-call study population may differ from the full deployment in ways nobody outside the company can assess. They are the arithmetic consequence of the company's own two published numbers placed next to each other.

**Seven hundred thousand interactions containing incorrect medical advice is compatible with "no safety issues" only under a definition the company has not published.**

---

## 8. What a zero measured on 307,000 calls licenses

This is the most important section in the case study, and it is a piece of standard statistics rather than an accusation.

### 8.1 Coverage

| Measure | Value |
|---|---|
| Calls evaluated in the safety study | **307,000** |
| Claimed interactions | 115 million |
| **Share of claimed volume examined** | **0.27%** |
| Interactions not examined | **114.69 million** |
| Claimed volume ÷ studied volume | **374.59×** |

The safety evidence covers **roughly a quarter of one percent** of the interactions the safety claim is made about.

### 8.2 The rule of three

When you observe **zero** events in **n** trials, you cannot conclude the true rate is zero. The standard approximation — the *rule of three* — gives an upper bound on the true rate at 95% confidence of **3/n**.

| Measure | Value |
|---|---|
| Calls observed | 307,000 |
| Severe events observed | 0 |
| **95% upper bound on the true severe-event rate** | **0.000977%** |
| Expressed as a frequency | **about 1 in 102,330** |
| **Implied severe events across 115 million interactions, at that upper bound** | **1,123.78** |

```
zero_severe_events_observed_in_study             = True
study_licenses_claim_of_zero_across_full_volume  = False
absence_of_evidence_equals_evidence_of_absence   = False
zero_observed_is_compatible_with_over_one_thousand = True
```

**Observing zero severe events in 307,000 calls is statistically compatible with more than a thousand severe events across 115 million interactions.**

That is not a claim that a thousand severe events occurred. It is a statement about what the evidence can and cannot exclude — and it is the precise reason a zero on a sample does not license a zero on a population 375 times larger.

### 8.3 Why this matters more here than anywhere else in the arc

Day 84's Abridge had an independent randomized trial measuring note quality, and a clinician reading every note before signing it. If the note was wrong, a trained professional had the opportunity to catch it.

Here there is no catcher. **The measurement is the only safety mechanism, which makes the measurement's coverage a safety property rather than a reporting detail.**

---

## 9. The peer-reviewed evidence, and what it measures

According to PubMed, Hippocratic AI has two peer-reviewed publications. Having any is creditable — Days 80, 82 and 83 had none.

```
peer_reviewed_vendor_studies           = 2
peer_reviewed_studies_measuring_safety = 0
safety_evidence_is_preprint_only       = True
```

### 9.1 JMIR Formative Research, August 2026

*Multicall Memory in an AI Care Agent for Chronic Care Management Among Older Adults: Retrospective Observational Study.* Eight of nine authors are Hippocratic AI staff; one is at the University of British Columbia.

| Measure | Value |
|---|---|
| Calls analysed | **4,415** |
| Patients | **4,189** |
| Calls per patient | **1.05** |
| Effect of each additional memory on call duration | **+2.47 min** (95% CI 2.03–2.91, p<.001) |
| CI width | **0.88** |
| Effect in completed calls only | **+0.54 min** (p=.004) |
| **Attenuation** | **78.14%** |
| **Effect on patient satisfaction** | **None significant** |

```
jmir_measures_call_duration = True
jmir_measures_safety        = False
jmir_measures_clinical_outcome = False
jmir_satisfaction_result_significant = False
```

The study measures **call duration and satisfaction**. It does not measure safety and does not measure any clinical outcome.

### 9.2 The finding inside the finding

The paper's headline result is that memory makes calls **longer**. Its satisfaction result is **null** — and the authors say so plainly, noting *"a disconnect between engagement duration and patient-reported experience"* and acknowledging the study may have been underpowered.

A feature that extends an elderly patient's phone call by **2.47 minutes** with no measurable satisfaction benefit is framed in the abstract as *"enhanced behavioral engagement."* That framing is worth pausing on. **Longer is being read as better, and the paper's own satisfaction data does not support that reading.**

The attenuation is also stark: in completed calls only, the effect falls to **+0.54 min** — a **78.14%** reduction. As on Day 84, the headline number is the one that does not survive the narrower analysis.

### 9.3 JAMA Ophthalmology, June 2026

*Generative Artificial Intelligence-Driven Voice Assistance for Patient Education in Ophthalmology*, co-authored with Roche and Genentech. A top-tier journal, and the appearance is a real credential.

```
jama_is_patient_education_not_safety = True
jama_coauthored_with_pharma          = True
```

It concerns **patient education**, not safety. And the pharma co-authorship is worth noting neutrally: an AI agent that speaks to patients about a condition, co-developed with the manufacturer of a treatment for that condition, is a structure that requires disclosed boundaries. None is described in the sources examined.

### 9.4 The summary position

| Evidence | Venue | Peer reviewed | Measures |
|---|---|---|---|
| RWE-LLM | medRxiv | **No** | **Safety** |
| Polaris | arXiv | **No** | Simulated parity |
| JMIR Form Res | JMIR | **Yes** | Engagement, satisfaction |
| JAMA Ophthalmol | JAMA | **Yes** | Patient education |

**Everything peer-reviewed measures something other than safety. Everything measuring safety is a preprint.**

---

## 10. The simulated evaluation

*Polaris: A Safety-focused LLM Constellation Architecture for Healthcare*, arXiv, submitted 20 March 2024. Also a preprint.

| Measure | Value |
|---|---|
| Nurses | 1,100+ |
| Physicians | 130+ |
| **Total clinicians** | **1,230+** |
| Nurse share | **89.43%** |

The paper describes "the first comprehensive clinician evaluation of an LLM system for healthcare," reporting that Polaris "performs on par with human nurses on aggregate" across medical safety, clinical readiness, conversational quality and bedside manner.

### 10.1 The evaluators posed as patients

```
pol_evaluators_posed_as_patients = True
pol_evaluated_real_patients      = False
pol_parity_claim_is_aggregate    = True
```

This is the methodological point that must travel with the parity claim. **Clinicians role-playing patients is a simulation.** It is a reasonable and common evaluation design, and it is not the same as studying real patients in real clinical situations.

A nurse pretending to be a confused 78-year-old post-discharge patient knows what the system is, knows they are being observed, and knows what a good answer looks like. A real confused 78-year-old does none of those things, and is the person the product actually serves.

The parity claim is also **aggregate** — across dimensions, on average. An aggregate parity claim is compatible with material underperformance on any individual dimension, including medical safety.

### 10.2 A discrepancy in the architecture description

| Source | Parameter claim |
|---|---|
| Polaris paper (arXiv) | "one-trillion parameter constellation" |
| Company research page | "5.0T+ parameter constellation architecture" |

| Derived | Value |
|---|---|
| Gap | **4.00 trillion** |
| Ratio | **5.00×** |

The paper is from March 2024 and the research page is current, so this is very plausibly two accurate statements about two different versions. **Neither source carries a date against the number**, which is the recurring failure of this entire arc: the figure is published and the definition and date are not.

---

## 11. The volume claims do not share a definition

| Source | Claim |
|---|---|
| Series C release, Nov 2025 | "over **115 million** clinical patient **interactions**" |
| Company research page | "over **7 million** clinical **calls**" |

| Derived | Value |
|---|---|
| Ratio | **16.43×** |
| Difference | **108.00 million** |

```
volume_claims_share_a_stated_definition = False
volume_claims_carry_dates               = False
```

"Interactions" and "calls" are different units, and one page may simply be older. But neither is defined and neither is dated, so a reader cannot tell whether the company handles 7 million things or 115 million things, or whether one interaction is a call, a turn within a call, or a task.

**This is the fifth consecutive case study in which a company's headline volume figure has no published definition.** Day 83's OpenEvidence had a 40% that changed meaning; Day 85's Eka Care had 3 crore trusted against 1 crore downloads. It is the most common failure in the series and the cheapest to fix.

The research page also reports an **8.95/10** satisfaction rating — **89.50%** of scale — likewise undated and without methodology.

---

## 12. Funding, and a structure worth naming

| Round | Date | Amount | Valuation |
|---|---|---|---|
| Series A | May 2024 | $53M | $500M |
| Series B | Jan 2025 | $141M | $1.64B |
| Series C | Nov 2025 | **$126M** | **$3.5B** |

| Derived | Value |
|---|---|
| Three named rounds | **$320.00M** |
| Total claimed | **$404.00M** |
| Not attributed to named rounds | **$84.00M** |
| Valuation step, A→B | **3.28×** |
| Valuation step, B→C | **2.13×** |
| **Valuation multiple since Series A** | **7.00×** |
| Valuation per claimed customer | **$70.00M** |
| Valuation per claimed interaction | **$30.43** |

### 12.1 Customers who are also investors

```
investor_customer_count = 3
customers_are_also_investors = True
```

Universal Health Services, Cincinnati Children's Hospital Medical Center and WellSpan Health appear as investors in the Series C announcement. All three are health systems — the customer category the company sells to.

| Measure | Value |
|---|---|
| Investor-customers as a share of claimed customers | **6.00%** |

This is ordinary in health tech and not improper. It is worth naming for one reason: **a health system that holds equity in a vendor is a less independent reference customer than one that does not**, and reference customers are the primary safety signal available to the next buyer. When a prospective customer asks "who else uses this and are they happy," the answer includes three parties with a financial interest in the answer being yes.

---

## 13. The court record

```
hippocratic_is_plaintiff = True
cases_as_defendant       = 0
no_product_liability_cases_found = True
```

One federal case: *Hippocratic AI, Inc. v. Health GPT, Inc.*, No. 3:23-cv-04738 (N.D. Cal.), filed 14 September 2023, cause **15 U.S.C. §1051 trademark infringement**, before Judge Rita F. Lin. Munjal Shah is named as a party. **Terminated 27 November 2023** — 74 days — by stipulation.

A trademark dispute resolved in ten weeks is unremarkable. **No product liability, malpractice or patient-harm litigation was identified.**

### 13.1 What that does and does not tell you

```
absence_of_litigation_proves_safety = False
```

It is a genuinely reassuring datum and it is weak evidence. A patient harmed by a wrong statement on an automated call would have to know the call was wrong, know the harm traced to it, know who operated the agent, and find counsel willing to litigate a novel theory against a vendor rather than the health system that deployed it.

**The absence of suits at this stage is consistent with both a safe product and an unmeasured one**, and the case study cannot distinguish them from the docket.

---

## 14. User personas

### 14.1 Mrs. Dolores K. — the patient on the phone

78, discharged three days ago after a heart failure admission, on six medications, lives alone. The phone rings and a calm voice asks how she is feeling and whether she has been weighing herself.

**Jobs to be done:** understand what she is supposed to be doing; be told whether what she is experiencing is normal; not go back to hospital.

**What she gets:** a call she would probably not otherwise have received. That is a genuine benefit and it should not be minimised — an unmade call has a harm rate of its own.

**What she cannot do:** evaluate the answer. She has no way to know whether the voice is right, and no second opinion in the room. Whether she knows it is an AI at all is not disclosed in any source examined.

**The design implication:** every prior product in this arc had an expert reviewer as the last line. Here the last line is a 78-year-old with heart failure, alone, at 6pm.

### 14.2 Sandra P. — the Chief Nursing Officer who bought it

Runs nursing for a regional system with a vacancy rate she cannot close. Sees an agent that makes every post-discharge call instead of the 30% her staff manage.

**Jobs to be done:** cover the outreach her team cannot; reduce readmissions; not be the person who deployed something that hurt a patient.

**What the evidence gives her:** a preprint reporting **99.38%** correct advice on 307,000 calls, and a marketing claim of zero safety issues across 115 million.

**What it does not:** a definition of safety issue, an independent audit, an escalation rate, or any peer-reviewed safety publication. She is making a staffing decision with real upside using safety evidence that has not been externally reviewed.

### 14.3 The nurse who was going to make the call

**The displaced worker is the persona nobody in this category discusses.** Day 81 found Hinge Health disclosing a ~97% reduction in human care hours. Day 84's literature proposed "displacement of burden" — work moving from production to oversight.

Here the displacement is more complete: the call is not supervised by a nurse, it replaces one. Whether the nurse's time was redeployed to higher-value work or simply not backfilled is the question that determines whether this technology expands care or substitutes for it, and no public evidence addresses it.

---

## 15. Jobs to be Done

| Job | Who | Served? | Evidence |
|---|---|---|---|
| "Call every discharged patient" | Health system | **Yes** | Volume claims |
| "Don't tell them anything wrong" | Patient, health system | **99.38%** of the time | Vendor preprint |
| "Escalate when it matters" | Patient | **Unmeasured** | No escalation rate published |
| "Tell me if it's an AI" | Patient | **Unmeasured** | Not disclosed |
| "Prove it's safe to my board" | CNO | **Partially** | Preprint only, no audit |
| "Cover the shifts I can't staff" | CNO | **Yes** | The core value |

---

## 16. Business model

Enterprise contracts with health systems, payors and pharma. Pricing is not disclosed; the company has described a model priced per hour of agent work, but no figure appears in the sources examined.

### 16.1 The incentive structure, assessed fairly

**Pricing per unit of work delivered aligns revenue with volume.** More calls means more revenue. That is a good alignment for coverage — the company wants the patient to be called — and a concerning one for duration and escalation, because a call that escalates to a human is a call the agent did not complete.

```
guardrail_escalation_rate_disclosed = False
```

**The escalation rate is the single most diagnostic undisclosed number in this business.** An agent that never escalates is either perfect or not trying. An agent that escalates often is safe and expensive. Nobody outside the company knows which this is, and the commercial incentive points one way.

That is not an allegation. It is the reason the metric should be published.

---

## 17. Competitive analysis

| Competitor | Position |
|---|---|
| **Human nurse call centres** | The incumbent; the thing being replaced |
| **Notable, Memora, Luma** | Patient outreach and engagement automation |
| **Traditional IVR** | Cheap, dumb, and nobody claims it is clinical |
| **Health system in-house staff** | The make-versus-buy alternative |
| **Abridge, Nuance** (Day 84) | Adjacent — documentation, not patient contact |

### 17.1 Porter's Five Forces

**Threat of new entrants — High and rising.** Voice models are commoditising fast. The defensible asset is the safety architecture and the clinical review apparatus — 6,234 clinicians is expensive to replicate — not the voice.

**Bargaining power of buyers — Moderate.** Health systems are sophisticated and slow, but the staffing pressure is acute and the alternative is not making the calls.

**Bargaining power of suppliers — Moderate.** Foundation model providers, and the clinician reviewer pool.

**Threat of substitutes — Moderate.** Doing nothing is the real substitute, and it is what most systems do today.

**Competitive rivalry — Intense and well funded.**

### 17.2 The moat

**The moat is the safety apparatus, not the model** — and that is an unusual and strategically strong position. Any competitor can generate fluent speech. Few can assemble 6,234 clinicians to adjudicate 307,000 calls.

Which makes the reporting gap doubly odd: **the company's hardest-to-copy asset is its safety measurement, and its public communication leads with a zero instead of the measurement.** The preprint is a better competitive document than the press release.

---

## 18. SWOT

**Strengths.** A published safety study on 307,000 real calls with 6,234 clinicians — more safety measurement than any other company in this arc. Correct advice improved **+19.38pp** across three architecture generations. Two peer-reviewed publications, one in JAMA Ophthalmology. An explicit non-diagnostic scope limit. **$404M** raised; 50+ named enterprise customers. Addresses a genuine, quantified staffing shortage.

**Weaknesses.** "No safety issues" is undefined and unreconciled with a **0.62%** error rate in the company's own research. Safety evidence is **preprint only**; no peer-reviewed safety publication. The safety study covers **0.27%** of claimed volume. Escalation rate undisclosed. Patient AI-awareness undisclosed. Volume claims differ **16.43×** with no definitions or dates. Parameter claims differ **5.00×** across company sources.

**Opportunities.** Publish the safety definition and detection method and own the category's evidentiary standard. Commission an independent audit — no competitor has one. Publish the escalation rate as a safety feature rather than a cost. Submit the safety work to a clinical journal.

**Threats.** A single well-publicised adverse event would be existential for a company whose claim is zero. Voice commoditisation. Regulatory attention to patient-facing AI. The reference-customer structure includes three investors.

---

## 19. Metrics: what exists, what does not

### 19.1 Published by the company

115 million interactions; 50+ customers; 1,000+ use cases; 6 countries; 8.95/10 satisfaction; 99.38% correct advice; 0.07% minor harm; 0.00% severe harm; 307,000 calls evaluated; 6,234 clinicians.

### 19.2 Peer reviewed

Call duration (**+2.47 min** per memory); satisfaction (**null result**); patient education in ophthalmology.

### 19.3 Measured by nobody outside the company

- Whether "no safety issues" means anything specific
- Escalation-to-human rate
- Whether patients know they are speaking to an AI
- Adverse events detected by any mechanism the company does not control
- Clinical outcomes — readmissions, adherence, mortality
- What happened to the nurse whose call this replaced

**The third list is what decides whether this product is safe and whether it works.**

---

## 20. Proposed North Star metric

**Adjudicated adverse-event rate per 100,000 interactions**, measured on a random sample, against a published definition, with an external adjudicator.

```
north_star_computable_by_company = True
north_star_published_by_company  = False
```

### 20.1 Why this rather than "no safety issues"

Because it is falsifiable. A rate can go up, which is precisely what makes it evidence. **A zero cannot be checked, cannot be compared against a competitor, and cannot show improvement** — the company's own preprint shows improvement from 80% to 99.38%, which is a far better story than zero and it is told in the document nobody reads.

### 20.2 Guardrails

**Guardrail 1 — error rate reported with every volume claim.** Current error rate **0.62%**. Currently the volume appears in the press release and the error rate in a preprint. They should appear in the same sentence.

**Guardrail 2 — sample coverage.** Currently **0.27%**. Proposed floor: **1.00%**. Not currently met.

**Guardrail 3 — escalation-to-human rate.** Undisclosed. This is the guardrail that protects the patient in the cases the error rate does not capture — the ones where the right answer was "let me get a nurse."

---

## 21. HEART framework

| Dimension | Measure | Reported? |
|---|---|---|
| **Happiness** | Satisfaction | **Yes** — 8.95/10, undated; peer-reviewed result null |
| **Engagement** | Call duration | **Yes** — and longer is treated as better |
| **Adoption** | Interactions completed | **Yes** — 115M, undefined |
| **Retention** | Repeat contact | Partially — 1.05 calls per patient in the JMIR study |
| **Task success** | **Did the call achieve its clinical purpose?** | **No** |

Task success is unmeasured for the seventh consecutive day. Here it would mean: did the patient take the medication, attend the appointment, avoid the readmission?

---

## 22. Kano analysis

| Feature | Category | Note |
|---|---|---|
| Says nothing clinically wrong | **Must-be** | 0.62% error rate in vendor research |
| Escalates when it should | **Must-be** | **Unmeasured** |
| Patient knows it is an AI | **Must-be** | **Undisclosed** |
| Calls happen at all | **Performance** | The core value, and it is real |
| Natural conversation, good bedside manner | **Performance** | Polaris parity claim |
| Multi-call memory | **Attractive** | Adds 2.47 min; no satisfaction gain |

All three must-be features are unmeasured or imperfectly measured. The attractive feature has a peer-reviewed null result. **That is an inverted evidence pyramid** — the most-studied feature is the least important one.

---

## 23. User journey

| Stage | What happens | Where the risk sits |
|---|---|---|
| Enrolment | Health system adds the patient to a campaign | Patient may not know they are enrolled |
| Disclosure | Agent identifies itself — or does not | **Not disclosed publicly** |
| Conversation | Agent asks, patient answers, agent responds | **0.62%** incorrect advice in vendor research |
| Escalation | Agent hands off to a human | **Rate undisclosed** |
| Documentation | Outcome written back to the system | Not examined |
| Detection | Something went wrong and someone notices | **This is the step that does not exist publicly** |

### 23.1 The missing step

Every other product in this arc had a detection mechanism built into the workflow: a clinician read the note, a physician read the answer, a patient opened their record. Errors had a chance of surfacing as part of normal use.

**Here, a wrong statement on a phone call to a patient who does not know it is wrong produces no artefact and no signal.** The only detection mechanism is retrospective sampling — the 307,000 calls — which covers **0.27%** of claimed volume.

That is why the coverage figure is a safety property and not a reporting statistic. **At 0.27% coverage, roughly 373 of every 374 interactions are never reviewed by anyone.**

---

## 24. AARRR funnel

| Stage | Position | Evidence |
|---|---|---|
| **Acquisition** | Strong — 50+ enterprise customers, 3 of them investors | Series C |
| **Activation** | Strong — 1,000+ use cases built | Series C |
| **Retention** | 1.05 calls per patient in the one published study | JMIR |
| **Referral** | Reference customers include equity holders | Series C |
| **Revenue** | Not disclosed | — |

The 1.05 figure deserves a caveat — it is from a single retrospective study of a chronic-care cohort, not a company-wide retention metric — but it is the only repeat-contact number in public, and chronic care management is precisely the use case where repeat contact is the point.

---

## 25. Eval plan

What a patient-facing agent with no human in the loop should be running.

**Adverse event detection that does not depend on sampling.** Automated post-call classification of every interaction against a published harm taxonomy, with human adjudication of everything flagged. Sampling 0.27% is a research design; continuous classification is a safety system.

**Escalation appropriateness.** Not just how often the agent escalates, but how often it *should* have and did not. This requires adjudicating calls where no escalation occurred, which is harder and more important.

**Patient comprehension.** Did the patient understand what they were told? A correct statement that is misunderstood by a 78-year-old on six medications has the same outcome as an incorrect one.

**Disclosure verification.** What share of patients, asked afterwards, knew they had spoken to an AI.

**Counterfactual harm.** The honest comparator is not a perfect nurse. It is **no call at all**, which is what most of these patients would otherwise receive. A study comparing agent-called patients against uncalled patients on readmission would be the strongest evidence this company could produce, and it would probably favour them.

**Release gating.** No model version reaches patients without non-regression on the harm taxonomy. The Polaris 1.0→2.0 severe-harm rise from **0.06%** to **0.10%** is exactly what release gating exists to catch.

---

## 26. Ranked failure modes

By expected harm.

**1. Incorrect clinical advice acted on by a patient with no way to check it.** The defining risk. **0.62%** incorrect in vendor research; no independent verification; no detection outside sampling.

**2. Failure to escalate when escalation was warranted.** A patient describes chest pain in vague terms and the agent reassures. This does not appear as an error in a correctness taxonomy — the statement may be accurate — and it is the most dangerous thing a non-diagnostic agent can do. **Unmeasured.**

**3. The patient does not know it is an AI.** Affects how much weight they give the advice and whether they seek a second opinion. **Undisclosed.**

**4. Silent regression after a model update.** Severe-harm concerns rose from **0.06%** to **0.10%** between Polaris 1.0 and 2.0 before reaching 0.00% at 3.0. **The company's own data shows a safety metric moving in the wrong direction across a version change.** That it was caught and reported is creditable; that it happened is the argument for release gating.

**5. Harm to the patient who was never called** because the agent handled the queue and the nurse was not backfilled. Invisible by construction.

**6. Over-trust accumulating over repeated calls.** A patient who has been called twenty times and found the agent helpful applies less scrutiny on the twenty-first.

**7. Commercial influence on content** where an agent discusses a condition under a pharma co-development arrangement. No boundary is described publicly.

Failure modes 1 through 3 are the core of the product's risk. **One is partially measured, two are not measured at all.**

---

## 27. Human-in-the-loop design

There is no human in the loop, so the question becomes: **where should one be put back?**

**At escalation.** The agent already must decide when to hand off. Publishing the rate, and auditing the non-escalations, converts an operational threshold into a safety control.

**At sampling.** 0.27% coverage with retrospective review is a research apparatus. Raising coverage and making review continuous converts it into monitoring.

**At disclosure.** A patient told clearly that they are speaking to an AI is a patient who can apply appropriate scepticism. That is the cheapest safety intervention available and it costs one sentence at the start of a call.

### 27.1 The honest counterargument

A human in the loop on every call defeats the product. The entire value proposition is that these calls happen **because** no human is required — and a call that a nurse must supervise is a call the nurse could have made.

So the loop cannot be restored at the interaction level without destroying the economics. **It has to be restored at the system level: definition, detection, escalation, audit.** That is a genuinely harder design problem than any previous day in this arc faced, and it is the right problem for this company to be working on.

---

## 28. Product recommendations

Five, each with evidence and a proof metric.

### R1. Publish the definition of a safety issue and the detection method

**Evidence:** `safety_claim_defines_safety_issue = False`; a **0.62%** error rate coexists with a claim of zero.
**Proposal:** publish the harm taxonomy, the severity thresholds, what counts as a safety issue, how one would be detected, and who adjudicates.
**Why first:** it costs nothing, it resolves the central contradiction in this case study, and it converts an unfalsifiable claim into a checkable one. It is also the necessary precondition for every other recommendation here.
**Success:** a published definition; the zero claim either survives it or is retired.
**Cost:** Low.

### R2. Report the error rate alongside every volume claim

**Evidence:** 115 million appears in the press release; 99.38% appears in a preprint.
**Proposal:** wherever interaction volume is stated, state the current correct-advice rate and its measurement basis in the same sentence.
**Why:** the improvement from ~80% to **99.38%** is a better story than zero, and it is true. The company is under-selling its own strongest evidence.
**Success:** both figures in the next funding or milestone announcement.
**Cost:** Low. The barrier is entirely a communications choice.

### R3. Publish the escalation rate and the patient AI-awareness rate

**Evidence:** failure modes 2 and 3; both undisclosed.
**Proposal:** publish what share of calls escalate to a human, and what share of patients, surveyed afterwards, understood they spoke to an AI.
**Why:** escalation is where the non-diagnostic scope limit is actually enforced, and disclosure is where patient autonomy lives.
**Success:** both published quarterly.
**Cost:** Moderate. Escalation rate may look high, which is the point.

### R4. Commission an independent safety audit of a random call sample

**Evidence:** `safety_claim_independently_audited = False`; coverage **0.27%**.
**Proposal:** fund an external clinical body to draw a random sample and adjudicate against the published taxonomy, with a binding commitment to publish.
**Why:** Day 84 demonstrated what independent measurement does for a category. No competitor has one, and for a company whose moat is its safety apparatus, an audited number is the strongest possible asset.
**Success:** a published external audit.
**Cost:** High, and the result is not controllable.

### R5. Submit the safety evidence for peer review in a clinical journal

**Evidence:** `safety_evidence_is_preprint_only = True`; two peer-reviewed papers, neither about safety.
**Proposal:** take the RWE-LLM work to a clinical journal.
**Why:** the company has demonstrated it can clear peer review — JAMA Ophthalmology proves that. It has simply not done it for the work that matters most.
**Success:** peer-reviewed publication of the safety evidence.
**Cost:** High, slow, and the methodology will be challenged.

---

## 29. RICE prioritisation

R, I, C, E and every stress factor are **author estimates, not disclosed data**. Reach is held at 115 (millions of claimed interactions) because every proposal's audience is the patients on the other end. Stress discounts by dependence on uncheckable claims and by execution exposure.

| ID | Proposal | R | I | C | E | Base | Stress | Stressed |
|---|---|---|---|---|---|---|---|---|
| P1 | Publish the safety definition and detection method | 115 | 3.0 | 0.95 | 2.0 | **163.88** | 0.95 | **155.68** |
| P2 | Report the error rate with every volume claim | 115 | 3.0 | 0.90 | 3.0 | **103.50** | 0.90 | **93.15** |
| P3 | Publish escalation and AI-awareness rates | 115 | 2.5 | 0.80 | 5.0 | **46.00** | 0.85 | **39.10** |
| P4 | Commission an independent safety audit | 115 | 3.0 | 0.65 | 9.0 | **24.92** | 0.60 | **14.95** |
| P5 | Submit safety evidence for peer review | 115 | 2.5 | 0.55 | 12.0 | **13.18** | 0.45 | **5.93** |

```
rice_base_ranking           = ('P1', 'P2', 'P3', 'P4', 'P5')
rice_stress_ranking         = ('P1', 'P2', 'P3', 'P4', 'P5')
rice_last_under_stress      = 'P5'
rice_last_under_stress_name = 'Submit the safety evidence for peer review in a clinical journal'
rice_last_gap_pct           = 60.33
```

### 29.1 Reading the ranking

Stable under stress. P1 loses only **5.00%** because it requires publishing a definition the company necessarily already uses internally — you cannot adjudicate 307,000 calls without one.

**P5 ranks last, by 60.33% below P4** — asserted by the gate, not argued here. Peer-reviewing the safety evidence would do more than anything else to settle whether the **99.38%** figure means what it appears to mean.

It ranks last for a reason worth stating plainly: **peer review is slow, the outcome is not controllable, and a vendor-designed evaluation of a vendor's own product will have its methodology challenged.** The reviewers will ask how calls were sampled, whether reviewers were blinded, how disagreements were resolved, and whether the taxonomy was fixed before the data was seen. Those are the right questions and the company may not like the answers.

**That is an argument for doing it, not against it — but it correctly ranks below the three things that cost almost nothing and are entirely within the company's control.** P1 through P3 could ship next quarter. P5 is a two-year project.

---

## 30. MoSCoW

**Must have.** R1 (publish the definition); R2 (error rate with volume).

**Should have.** R3 (escalation and AI-awareness rates).

**Could have.** R4 (independent audit).

**Won't have this cycle.** R5 (peer review of safety evidence) — sequencing, not rejection. See 29.1.

---

## 31. PRD: the safety definition (R1)

**Problem.** The company states it has completed over 115 million interactions "with no safety issues" while its own research reports a **0.62%** incorrect-advice rate. Both statements are the company's. Neither defines "safety issue," so the claim cannot be checked, compared, or improved against.

**Objective.** Publish a harm taxonomy and detection methodology such that any external party can state what would and would not count as a safety issue.

**Non-goals.** Not a certification. Not a regulatory submission. Not a commitment to a target rate.

**Requirements.**
- R1.1 Define severity tiers with clinical examples at each boundary — the hard part is the line between "minor harm potential" and "severe."
- R1.2 State the detection method: sampling frame, sample size, selection procedure, and whether detection is retrospective or continuous.
- R1.3 State who adjudicates, their qualifications, and how disagreements are resolved.
- R1.4 State the reporting period and publish the rate against the taxonomy each period.
- R1.5 Restate prior periods if the taxonomy changes.

**Success criteria.** A published taxonomy that a hostile reader could apply to a transcript and reach the same classification the company would. Secondary: a competitor adopts it.

**Risks.** The published rate will not be zero. The definition will be argued with. Prior "no safety issues" language becomes untenable.

**All three are the point.** A safety claim that survives publication of its own definition is worth something; one that does not was never evidence.

---

## 32. Roadmap

**Horizon 1 — next two quarters.** R1 (definition and detection), R2 (error rate with volume). Both are communications and documentation changes using information the company already holds.

**Horizon 2 — quarters three and four.** R3 (escalation and AI-awareness). Requires instrumentation and a patient survey, and it is the first item that could produce an uncomfortable number.

**Horizon 3 — year two.** R4 (independent audit), then R5 (peer review). Both require surrendering control of a method to outsiders, which is only rational once the internal definitions have been published and survived scrutiny.

### 32.1 Sequencing logic

Ordered by **controllability and evidence dependency**. You cannot commission an external audit against a taxonomy you have not published, and you cannot submit for peer review a methodology you have not externally tested. **The cheap items are also the prerequisites.**

---

## 33. Risks to this analysis

**The safety evidence is a preprint and is treated as one.** RWE-LLM has not been peer reviewed, its methodology has not been externally challenged, and its figures are the company's own. This case study uses them because they are the best safety evidence that exists — not because they are verified.

**The rule-of-three calculation is a bound, not an estimate.** **1,123.78** is the upper limit of what observing zero in 307,000 is compatible with across 115 million. The true number could be zero. The point is that the evidence cannot distinguish zero from a thousand, not that a thousand occurred.

**The 307,000-call sample may not represent the full deployment.** If the study over-sampled high-risk use cases the true rate is lower; if it over-sampled simple ones, higher. Nothing in the sources describes the sampling frame.

**"Interactions" and "calls" may not be the same unit.** The extrapolations in section 7.3 assume the error rate measured on calls applies to interactions. If an interaction is smaller than a call, the implied counts change materially. Flagged in Appendix A.

**The Polaris parity claim is simulated and the case study says so throughout**, but simulation is a legitimate evaluation stage and the criticism is about how the result travels, not about running it.

**The counterfactual is not a perfect nurse.** Most of these patients would otherwise receive no call. A 0.62% error rate against a baseline of zero contact may well be a large net benefit, and no public evidence establishes it either way. Section 40 runs this properly.

**Absence of litigation is not evidence of safety**, and section 13.1 says so.

**RICE inputs are the author's.**

---

## 34. What a product manager should take from this

**A zero is a claim about a definition, not about the world.** Whenever a company reports zero of something, the first question is what would have had to happen to count. Here the company's own research reports a non-zero error rate in the same period, which means the zero is a claim about one severity tier — a legitimate claim, undermined by not saying so.

**Ask what share of the population the safety evidence covers.** **0.27%** here. A zero on a sample does not transfer to a population 375 times larger, and the rule of three tells you exactly how far it does transfer. This is a two-line calculation that any PM evaluating any vendor can do.

**When you remove the human, the measurement becomes the safety mechanism.** Every prior product in this arc had a professional who might catch the error. Removing that person does not just remove a cost — it removes the detector, and the detector has to be rebuilt as instrumentation.

**Watch for the metric moving the wrong way across a version.** Severe-harm concerns went **0.06% → 0.10% → 0.00%** across three generations. The company found and published that. Most companies would not have looked.

**The best evidence is often in the document nobody reads.** The press release says zero. The preprint says 80% → 99.38% with 6,234 clinicians adjudicating 307,000 calls. The second is a far better story and it is buried.

**Longer is not better.** A peer-reviewed study found memory adds **2.47 minutes** to an elderly patient's call with no significant satisfaction gain, and the framing calls it enhanced engagement. Check whether your engagement metric is measuring value or measuring duration.

---

## 35. The seven-rung ladder

| Rung | Company | Human between AI and patient | What is disclosed about outcomes |
|---|---|---|---|
| 1 | **Day 80 — Hims & Hers** | Clinician prescribes | **No AI metric at all** |
| 2 | **Day 81 — Hinge Health** | Clinician supervises | Cost metric, no outcome |
| 3 | **Day 82 — Doximity** | Clinician signs | AI cost audited; claims quote-only |
| 4 | **Day 83 — OpenEvidence** | Physician reads | No filing; tested only in court |
| 5 | **Day 84 — Abridge** | Clinician signs | **Independent RCT measures the outcome** |
| 6 | **Day 85 — Eka Care** | Patient reads own record | State measures accounts, not usage |
| 7 | **Day 86 — Hippocratic AI** | **Nobody** | **Safety claimed as zero, measured on 0.27%** |

```
ladder_length              = 7
ladder_days_without_human  = 1
```

### 35.1 The ladder's shape has inverted

For six days the finding was that **companies under-measure**. Day 86 is different in an important way: **this company measures more than any of the six before it** — 307,000 calls, 6,234 clinicians, a published error trajectory across three architecture generations.

And it is the company where measurement matters most, because it is the only one with no human backstop. So the gap here is not between measuring and not measuring. **It is between what was measured and what was said.**

The research says 99.38%. The press release says zero. The first is more impressive and it is the one nobody quotes.

---

## 36. Day 84 and Day 86, side by side

| Measure | Day 84 — Abridge | Day 86 — Hippocratic AI |
|---|---|---|
| Human in the loop | **Yes** — clinician signs | **No** |
| Outcome evidence | **Independent randomized trial** | Vendor preprint |
| Who funded the key evidence | University hospital + NIH | The company |
| Product quality measured at | 7,966 notes, unedited | 307,000 calls |
| Headline quality figure | PDSQI-9 accuracy **4.44/5** (**88.80%** of scale) | Correct advice **99.38%** |
| Peer-reviewed safety study | Not applicable — documentation only | **None** |
| Marketing claim | "Toward hallucination-free" | "No safety issues" |

```
d84_evidence_tier      = 'independent randomized trial'
d86_safety_evidence_tier = 'vendor preprint'
tiers_are_comparable   = False
```

**The two quality figures must not be compared** — different products, different instruments, different evidence tiers — and the gate asserts that explicitly.

What can be compared is the **evidence tier**. Day 84's central number came from academics with NIH funding who could publish whatever they found. Day 86's comes from the company. Both are the best available for their product; only one had an independent party able to say no.

And note the symmetry in the marketing: Day 84's whitepaper said *"toward* hallucination-free" and the product page dropped the "toward." Day 86's research says 99.38% and the press release says zero. **Both companies' engineering is more honest than their marketing, and by roughly the same mechanism.**

---

## 37. The regulatory position

The non-diagnostic scope is the regulatory strategy. Software that diagnoses or recommends treatment approaches FDA device regulation; software that reminds and collects does not.

```
fda_clearance_referenced = False
```

No FDA clearance is referenced in any source examined, which is consistent with a product designed to sit outside the device pathway.

Two observations follow.

**The boundary is maintained by the model, in real time, in conversation.** A scope limit enforced by product design is durable. A scope limit enforced by what a language model says when a patient asks an unexpected question is a probabilistic control, and the **0.62%** is the measurement of how probabilistic.

**The absence of a regulatory pathway is also the absence of a reporting obligation.** A cleared device has post-market surveillance and adverse-event reporting requirements. A non-device has none — which means the only adverse-event data that will ever exist is the data the company chooses to generate and publish.

That is not a criticism of the company's regulatory positioning, which appears sound. It is the reason voluntary measurement matters so much here: **there is no regulator collecting the denominator.**

---

## 38. Disclosure and consent

Whether patients are told they are speaking to an AI is not addressed in any source examined.

Several US states have enacted or proposed requirements that AI systems disclose their non-human status in certain interactions, and the direction of travel is clear. But the case for disclosure here is not primarily legal.

**A patient who knows they are speaking to an AI calibrates differently.** They may ask for a human, seek a second opinion, or weigh the advice less heavily. Every one of those behaviours is a safety mechanism that disclosure switches on and non-disclosure switches off.

That makes disclosure a **safety feature**, not a compliance checkbox — and it makes the undisclosed disclosure rate a genuine gap rather than a procedural one.

---

## 39. Concentration and dependency

| Dimension | Position |
|---|---|
| Customer type | Health systems, payors, pharma |
| Customer concentration | Not disclosed |
| **Reference customers who are investors** | **3** (**6.00%** of claimed customers) |
| Model supply | Foundation model providers, not disclosed |
| Clinical reviewer pool | 6,234 clinicians — an operational asset |
| Regulatory exposure | Outside the device pathway |
| Geographic | 6 countries |

The reviewer pool is the interesting dependency. **6,234 clinicians adjudicating calls is a large, ongoing, expensive operation** — and it is the thing that makes the safety evidence possible. If that apparatus is ever scaled back for cost, the measurement scales back with it, silently.

---

## 40. Counterfactual: what is the honest comparator?

This section matters because the case study would be unfair without it.

**The comparator is not a perfect nurse.** For most of these patients, the alternative is not a careful human call — it is **no call at all**. Post-discharge follow-up, chronic care check-ins and screening outreach are precisely the things health systems do not manage to staff.

So the honest question is not "is the agent as safe as a nurse?" It is **"is a patient called by an agent better off than a patient not called?"**

On plausible assumptions the answer is probably yes. A 0.62% incorrect-advice rate against a baseline of zero contact, for a patient who would otherwise have had no post-discharge follow-up at all, is very likely a net benefit. Missed follow-up has a harm rate too, and it is not small.

**Three things follow.**

First, **this strengthens rather than weakens the case for measurement.** If the product is genuinely net-beneficial, a well-designed study would show it — and that study would be worth more than any marketing claim.

Second, **the counterfactual does not license the zero.** "Better than nothing" and "no safety issues" are different claims, and only the first is defensible on current evidence.

Third, **nobody has run the study.** A comparison of agent-called against uncalled patients on readmission or adherence is the single most valuable piece of evidence this company could produce, it would probably favour them, and it does not exist.

---

## 41. What Hippocratic AI does better than the six before it

Stated explicitly, because the balance matters and this company is not the weakest in the arc on evidence.

**It measures safety at all.** 307,000 calls, 6,234 clinicians, a published trajectory across three architecture generations. Days 80, 82 and 83 published no safety measurement of any kind.

**It published a number that moved the wrong way.** Severe-harm concerns rose from **0.06%** to **0.10%** between Polaris 1.0 and 2.0. A company optimising its narrative would not report that.

**It limits its own scope explicitly.** "Does not prescribe, does not diagnose" is a restraint claim, and restraint claims are rare.

**It clears peer review when it tries.** JAMA Ophthalmology is a genuine credential.

**Its improvement story is real.** ~80% to **99.38%** correct advice is substantial engineering progress on a hard problem, measured against clinician adjudication rather than a benchmark it wrote itself.

**The criticism is narrow and specific:** the safety claim in the marketing is not the safety finding in the research, the coverage is **0.27%**, and nothing about safety has been peer reviewed or externally audited.

---

## 42. Scenario analysis

Author constructs applying arithmetic to published figures. Not forecasts.

### 42.1 If the safety study covered 1% instead of 0.27%

| Measure | Value |
|---|---|
| Current coverage | **0.27%** |
| Proposed floor | **1.00%** |
| Calls that would need review at 115M | 1.15 million |
| Multiple of current review volume | **3.75×** |

At 1% coverage and zero severe events observed, the rule-of-three upper bound would fall by roughly the same factor — tightening the claim substantially. **Coverage is the cheapest lever on evidential strength available**, and it is an operations question rather than a research one.

### 42.2 If the error rate held and volume grew tenfold

At 1.15 billion interactions and a **0.62%** incorrect rate, the implied count of interactions containing incorrect advice grows proportionally. Nothing about the rate improves with scale; only the absolute exposure grows.

**This is the argument for publishing the rate rather than the zero.** A rate stays honest as volume grows. A zero becomes progressively harder to sustain and progressively more damaging when a single counterexample appears.

### 42.3 If one severe adverse event became public

For a company whose public claim is zero, a single well-documented severe event is not a 0.0000009% problem. It is an existential communications problem, because the claim was categorical.

Had the company published **99.38%** and a defined taxonomy, the same event would be a data point within a disclosed distribution.

**The zero is not only weaker evidence than the rate. It is a larger business risk.**

---

## 43. Sensitivity: what would change the conclusion

**On the safety claim.** Publishing the definition would resolve it in a sentence. If "safety issue" means severe harm, the claim is defensible and the criticism becomes one of clarity rather than substance.

**On the error rate.** An independent audit finding a materially different rate — in either direction — would be the most informative single result available.

**On the coverage argument.** Nothing changes it. **0.27%** is arithmetic, and the rule of three is standard.

**On net benefit.** A controlled study against uncalled patients could substantially strengthen the company's position, and section 40 argues it probably would.

---

## 44. What would change my mind

**I would withdraw the central criticism** if the company published its harm taxonomy and the zero claim survived it. The criticism is about an undefined term, not about a belief that the product is unsafe.

**I would revise the coverage criticism** if continuous classification replaced retrospective sampling.

**I would revise the evidence-tier criticism** if the safety work cleared peer review or an external audit.

**I would not revise the structural finding.** A patient-facing agent with no human intermediary and no regulatory reporting obligation generates adverse-event data only if its operator chooses to. That is a fact about the regime, not about this company.

---

## 45. Open questions for the category

**Who collects adverse events for non-device clinical AI?** No regulator requires it. No registry exists. The only data is what vendors publish.

**What is the disclosure standard for AI speaking to patients?** Inconsistent and mostly unmeasured.

**Should escalation rate be a published metric across the category?** It is the point at which a non-diagnostic agent's scope limit is actually enforced, and no vendor publishes it.

**What is the right comparator?** Every vendor implicitly compares to a perfect human. The real comparator is usually no contact at all, and nobody has run that study.

**Who is accountable when an agent is wrong?** The vendor, the health system that deployed it, or nobody. Section 13 suggests the current answer is nobody, and that is not stable.

---

## 46. Day 87 connection

Tomorrow is **Tempus AI** — and it moves from the conversation back to the data.

Tempus is a precision medicine and genomic diagnostics company, and it is **publicly traded**, which restores SEC filings as a primary source for the first time since Day 82. That changes the method again: audited financials, segment reporting, risk factors, and the disclosure obligations that come with being listed.

It also changes the question. Days 83 through 86 have asked what private companies choose to publish. Day 87 asks what a public company must publish, and whether obligation produces better evidence than choice — which is the hypothesis this arc has been building toward since Day 82.

---

## 47. Recommended diagrams

Per series standard from Day 50: **no Mermaid**. Markdown tables and ASCII only.

**D1 — The claim and the research.** Two panels: "Press release — 115 million interactions, no safety issues" against "Company's own preprint — 99.38% correct, 0.62% not, 0.07% minor harm, 0.00% severe." Same company, same period.

**D2 — What 0.27% covers.** A bar of 115 million with a sliver at 307,000 marked, captioned "the share of interactions any clinician has reviewed."

**D3 — The rule of three.** Zero observed in 307,000 → 95% upper bound 1 in 102,330 → up to **1,124** severe events across 115 million. Three boxes, one arrow each.

**D4 — Safety across versions.** Correct advice 80.0 → 96.79 → 98.75 → 99.38, with severe-harm concerns 0.06 → 0.10 → 0.00 plotted beneath, the 1.0→2.0 rise highlighted.

**D5 — The seven-rung ladder.** Days 80–86 with the "who stands between the AI and the patient" column, Day 86 highlighted as the first with nobody.

### 47.1 ASCII rendering of D1

```
   THE PRESS RELEASE              |   THE COMPANY'S OWN RESEARCH
   Series C, 3 Nov 2025           |   RWE-LLM preprint, medRxiv
  --------------------------------+--------------------------------
   115,000,000 interactions       |   307,000 calls evaluated
                                  |   6,234 clinicians adjudicating
   "with no safety issues"        |
                                  |   Correct advice        99.38%
                                  |   NOT correct            0.62%
           ZERO                   |   Minor harm potential   0.07%
                                  |   Severe harm            0.00%
                                  |
   Undefined. Unaudited.          |   Preprint. Not peer reviewed.
                                  |   Covers 0.27% of the volume.
```

---

## 48. Recommended screenshots and visual assets

1. The Series C release sentence containing "115 million clinical patient interactions with no safety issues."
2. The RWE-LLM results passage showing 99.38% / 0.07% / 0.00% across Polaris generations.
3. Items 1 and 2 side by side — this is the case study in one image.
4. The Polaris abstract passage describing evaluators who "posed as patients."
5. The JMIR abstract sentence reporting no significant association between memory usage and patient satisfaction.

Item 3 is the strongest single visual in the series to date: two statements by the same company, in the same period, that require a definition to reconcile.

---

## 49. Is patient-facing voice AI ready?

On the evidence, the layers divide.

**Solved.** Holding a natural, appropriate telephone conversation with a patient. The Polaris evaluation, simulated though it is, and the satisfaction figures suggest conversational quality is not the binding constraint.

**Working.** Coverage. Calls that would not otherwise be made are being made, at a volume no staffing model could reach.

**Unresolved.** Whether the error rate is acceptable, because nobody has said what acceptable means. Whether escalation works. Whether patients know.

**Unmeasured.** Clinical outcomes. Adverse events outside a 0.27% retrospective sample. Net benefit against the real counterfactual.

A category where conversational quality is solved and harm measurement is contested is at a specific stage: **the capability has outrun the accountability.** Day 84 found engineering ahead of measurement; Day 85 found infrastructure ahead of explanation. This is the third variant, and the most consequential, because it is the one with no human backstop.

---

## 50. A closing note on method

The most useful thing this case study did was divide three by 307,000.

The rule of three is a first-year statistics result. It took under a minute and it converted an unfalsifiable marketing claim into a bounded statement: observing zero severe events in 307,000 calls is compatible with up to **1,124** across 115 million.

**Any product manager can run this.** When a vendor reports zero of something, ask how many observations the zero came from, divide three by that number, and multiply by the population the claim covers. If the answer is large, the zero is a statement about the sample, not the world.

The second most useful thing was reading the preprint the press release does not cite. The company's best evidence — 6,234 clinicians, 307,000 calls, ~80% to 99.38% — is in a document its own funding announcement does not mention.

**For the third day running, the finding was in the source the company did not lead with.**

---

## 51. What seven days established

| Day | Company | Human in the loop | The finding |
|---|---|---|---|
| 80 | Hims & Hers | Yes | An AI narrative with no AI metric |
| 81 | Hinge Health | Yes | A metric measuring cost saved, not health gained |
| 82 | Doximity | Yes | AI cost audited; AI claims quote-only |
| 83 | OpenEvidence | Yes | No filing; claims tested only in litigation |
| 84 | Abridge | Yes | Independent trials measure the outcome; the vendor does not publish it |
| 85 | Eka Care | Yes | The state measures accounts; usage is a quarter of them |
| 86 | Hippocratic AI | **No** | **The research says 99.38%; the marketing says zero** |

Seven companies, three countries, four business models.

The six-day finding was that **whoever does the measuring measures their own contribution**. Day 86 refines it, because this company measured the right thing and then said something else:

**Measurement and communication are separate failures, and the second is now the more common one.**

Doximity's AI cost was audited and its AI claims were quote-only. Abridge's whitepaper said "toward hallucination-free" and its product page dropped the word. Eka Care published three crore trusted beside one crore downloads. Hippocratic AI published 99.38% and announced zero.

In every case the engineering document was more honest than the marketing document. **The gap is not a measurement problem. It is a translation problem, and it happens on the way from the research team to the press release.**

---

## 52. Appendix A — source conflicts and reconciliations

Series rule: every conflict documented, never silently resolved.

### A1. "No safety issues" against a 0.62% error rate

The Series C release states 115 million interactions with no safety issues. The company's RWE-LLM preprint reports **99.38%** correct advice at Polaris 3.0 — a **0.62%** incorrect rate — with **0.07%** carrying potential minor harm and **0.00%** severe-harm concerns.

**Reconciliation:** the two are consistent only if "safety issue" denotes the severe-harm category. That is a defensible definition and the company has not stated it. Both figures are reported throughout, and the gate asserts `no_safety_issues_consistent_with_all_errors = False`.

### A2. Interactions versus calls

The Series C release says "over 115 million clinical patient interactions." The research page says "over 7 million clinical calls" — a ratio of **16.43×**.

**Not reconciled.** Different units, neither defined, neither dated. The extrapolations in section 7.3 apply a rate measured on *calls* to a count of *interactions*, which is flagged in section 33 as a material assumption. If an interaction is smaller than a call, those implied counts change.

### A3. Parameter count: one trillion versus 5.0T+

The Polaris paper (March 2024) describes a "one-trillion parameter constellation." The current research page says "5.0T+."

**Resolution:** almost certainly different architecture versions across two years. Neither source dates the figure. Not material to any safety conclusion.

### A4. Total raised: $320M in named rounds versus $404M claimed

Three named rounds sum to **$320.00M**; the Series C release states **$404M** total. The **$84.00M** difference is presumably seed and pre-Series-A funding not itemised. Both computed in the gate; not treated as a discrepancy.

### A5. The rule of three is an approximation

**3/n** is the standard approximation to the exact 95% upper confidence bound for zero events in n trials — the exact binomial bound is 1−0.05^(1/n), which differs negligibly at n = 307,000. The approximation is used because it is the conventional form and the difference does not affect any conclusion.

### A6. Severe-harm rate rose before it fell

The preprint reports severe-harm concerns at **0.06%** (pre-Polaris), **0.10%** (Polaris 1.0) and **0.00%** (Polaris 3.0). The rise is reported as published. No Polaris 2.0 figure for this category appears in the retrieved excerpt.

### A7. Three false-match dockets discarded

A full-text search for "Hippocratic AI" returned four dockets. Three — *American Association of University Professors v. Rubio*, *Groq, Inc. v. Groq Health, Inc.*, and *China Central Television v. Create New Technology HK Limited* — are unrelated and were discarded. Only *Hippocratic AI, Inc. v. Health GPT, Inc.* concerns this company.

---

## 53. Appendix B — sources examined and not used

**PACER document texts.** Not retrieved. Docket metadata only; no complaint text quoted.

**The full RWE-LLM PDF.** The abstract and results summary were retrieved; the full methods section was not parsed. **The sampling frame, blinding procedure and taxonomy definitions are therefore not described here** — and their absence from this analysis is a limitation, not an assertion that they are absent from the paper.

**The full Polaris paper.** Abstract only. Specific numerical comparisons against GPT-4 and LLaMA-2 70B are referenced in the abstract without figures and are not used.

**The JAMA Ophthalmology full text.** The abstract was not available through PubMed. The paper is cited for its existence, venue, authorship and subject only — **no result from it is used.**

**Contrary Research, CB Insights, PitchBook, aiwiki.** Aggregators, not primary.

**Vendor review and comparison sites.** Commercially motivated, no methodology.

**Market data.** Excluded by series rule. Valuation appears only as a company claim.

**The product itself.** Not tested by the author. No first-hand evaluation claimed.

---

## 54. Methodology

**Source acquisition.** Peer-reviewed literature through PubMed. Preprints from medRxiv and arXiv. Company claims from the Series C announcement via BusinessWire and the company research page. Federal docket metadata from the CourtListener public search API, queried 24 September 2026.

**Gate-first discipline.** `verify.py` was written and passing before any prose existed.

**Evidence tiering.** The gate distinguishes peer-reviewed publication, preprint, company claim and court record, and asserts which tier each finding rests on — so a preprint is never treated as peer-reviewed evidence and a press release is never treated as either.

**Statistical treatment.** Zero-event data is handled with the rule of three, the standard approximation for an upper confidence bound when no events are observed. The gate computes the bound and asserts explicitly that the study does not license the population-level claim.

**Rounding.** Percentages to two decimals, tolerance 0.005 absolute unless stated. Derived figures computed from unrounded inputs — the rounded-intermediate error class found earlier in this series was caught again by the gate during construction of this case study.

**Cross-checking.** `crosscheck.py` extracts every two-decimal figure in this README and in ASSUMPTIONS.md and confirms each traces to a gate value.

**Author constructs.** RICE inputs, stress factors, personas, the North Star proposal, guardrail thresholds, the eval plan, the failure-mode ranking and all scenario parameters are the author's and are labelled as such.

**Fabrication policy.** No figure, quote, date, case number or study result is invented. Where information is unavailable, this document says so.

---

## 55. Reproducing this analysis

```bash
# 1. The company's own safety evidence (open access preprint)
#    RWE-LLM: medRxiv 2025.03.17.25324157v1  - NOT peer reviewed
#    Polaris: arXiv:2403.13313               - NOT peer reviewed

# 2. The peer-reviewed publications (via PubMed)
#    Sanz Ausin M, et al. JMIR Form Res 2026;10:e87704. PMID 42627706.
#    DOI 10.2196/87704
#    Jacobs A, et al. JAMA Ophthalmol 2026;144(6):563-566. PMID 42133343.
#    DOI 10.1001/jamaophthalmol.2026.1307

# 3. The rule of three, on the safety claim
python3 - <<'PY'
calls, claimed = 307_000, 115_000_000
ub = 3 / calls                      # 95% upper bound on a zero-event rate
print(f"upper bound rate : {ub:.9f}  (1 in {1/ub:,.0f})")
print(f"implied events   : {claimed * ub:,.2f} across {claimed:,} interactions")
PY

# 4. Federal dockets
curl -A "<your contact>" --get "https://www.courtlistener.com/api/rest/v4/search/" \
  --data-urlencode 'q="Hippocratic AI"' --data-urlencode "type=r"

# 5. Run the gate. 160 checks. Non-zero exit on any failure.
python3 verify.py

# 6. Cross-check the prose against the gate.
python3 crosscheck.py
```

---

## 56. Limitations

This analysis rests on two preprints, two peer-reviewed papers (one cited for existence only), one funding announcement, one company research page and one federal docket. No audited financials exist and none are used.

The safety figures are the company's own, from a preprint whose full methods were not parsed. They are used because they are the best safety evidence that exists, not because they are verified.

The rule-of-three bound is a statement about what the evidence can exclude, not an estimate of harm.

No clinical assessment of Hippocratic AI is made or implied. **Nothing here asserts that any patient was harmed, that any company claim is false, or that the product is unsafe.** The finding is that the central safety claim is undefined and its evidentiary base covers 0.27% of the volume it describes.

Section 40 sets out the counterfactual case in the company's favour, and it is a strong one.

---

## 57. References

**The company's own research.**

"Real-World Evaluation of Large Language Models in Healthcare (RWE-LLM): A New Realm of AI Safety & Validation." medRxiv 2025.03.17.25324157v1. **Preprint, not peer reviewed.**

"Polaris: A Safety-focused LLM Constellation Architecture for Healthcare." arXiv:2403.13313, submitted 20 March 2024. **Preprint, not peer reviewed.**

**Peer-reviewed publications.** According to PubMed:

Sanz Ausin M, Chaurasia A, Miller A, Agnew JD, Lasko R, Raglow-Defranco M, Voisard M, Godil S, Mukherjee S. "Multicall Memory in an AI Care Agent for Chronic Care Management Among Older Adults: Retrospective Observational Study." *JMIR Formative Research* 2026;10:e87704. PMID 42627706. [DOI](https://doi.org/10.2196/87704).

Jacobs A, Anselmo D, McHugh R, Fernandez-Garcia I, Fang C, Lasko R, Mukherjee S, Holekamp N. "Generative Artificial Intelligence-Driven Voice Assistance for Patient Education in Ophthalmology." *JAMA Ophthalmology* 2026;144(6):563-566. PMID 42133343. [DOI](https://doi.org/10.1001/jamaophthalmol.2026.1307). *Cited for existence, venue and authorship only; no result used.*

**Company statements.** Series C announcement via BusinessWire, 3 November 2025. Company research page, retrieved 24 September 2026.

**Federal docket.** *Hippocratic AI, Inc. v. Health GPT, Inc.*, No. 3:23-cv-04738 (N.D. Cal.), via CourtListener public search API, queried 2026-09-24.

**Series cross-references.** Day 80–85 comparator figures are recomputed inside this case study's own `verify.py` and are not carried across as prose assertions.

---

## 58. Document control

| Field | Value |
|---|---|
| Case study | Day 86 of 90 |
| Subject | Hippocratic AI, Inc. (US, private) |
| Method | Vendor preprints + peer-reviewed literature + docket + claim consistency |
| Primary sources | 2 preprints, 2 peer-reviewed papers, 1 funding announcement, 1 docket |
| Verification checks | **160**, all passing |
| Unverifiable categories asserted | **14** |
| Peer-reviewed studies measuring safety | **0** |
| Safety-study coverage of claimed volume | **0.27%** |
| Diagrams | Markdown tables and ASCII only |
| Fabricated figures | **0** |

---

## 59. Series index

| Day | Company | Central finding |
|---|---|---|
| 80 | Hims & Hers | AI narrative with zero disclosed AI metrics |
| 81 | Hinge Health | Discloses an AI cost metric, not a clinical one |
| 82 | Doximity | AI cost is audited; every AI claim is quote-only |
| 83 | OpenEvidence | No filing exists; the only adversarial test is litigation |
| 84 | Abridge | The evidence exists — the vendor didn't produce it |
| 85 | Eka Care | 93.95 crore accounts; about a quarter get used |
| **86** | **Hippocratic AI** | **The research says 99.38%. The marketing says zero.** |
| 87 | Tempus AI | *(forthcoming — SEC filings return)* |

---

## 60. Standing questions for Hippocratic AI

Ordered by how much the answer would change the assessment.

1. **What is a safety issue?** Publishing the taxonomy would resolve the central finding of this case study in one document.
2. **What share of calls escalate to a human**, and how often should they have and did not?
3. **Do patients know they are speaking to an AI?** What share, measured how?
4. **How were the 307,000 calls sampled**, and were reviewers blinded to the architecture version?
5. **What happened to the nurses** whose calls these replaced?

---

## 61. The one-line version

A company whose agents speak to patients with no human listening says it has completed 115 million interactions with no safety issues.

Its own research, on 307,000 of them, reports 99.38% correct — and 0.62% not.

**Both numbers are true. Only one is falsifiable, and it is not the one in the press release.**

---

## 62. Postscript: on grading a company that measured more than the others

This case study is harder on a company that does more measurement than any of the six before it, and that deserves an explanation rather than a disclaimer.

The bar moves with the product. When a clinician signs every note, a measurement gap is a reporting problem — the clinician is still there. When an AI speaks to a patient alone, the measurement **is** the safety system, and a gap in it is a gap in the safety system.

Hippocratic AI built more of that system than its peers and then described it with a number that the system itself does not produce. **The criticism is not that the company measured too little. It is that having measured well, it announced something else.**

That is a fixable problem, and it is fixable this quarter, which is why three of the five recommendations cost almost nothing.

---

## 63. A note on what this arc has become

Seven days ago this was a series about whether healthcare AI companies disclose outcome metrics. The answer was no, consistently, and it would have been a thin finding repeated seven times.

What it became instead is a series about **where a claim lives and what standard it was held to** — a filing, a press release, a court filing, a preprint, a peer-reviewed journal, a government dashboard. Each has a different evidentiary weight, and the weight has almost nothing to do with how the number is used in public.

That reframing came from Day 82, when the Doximity 10-Q and its earnings release told different stories. Everything since has been an elaboration of it, and Day 86 is the sharpest version: **two documents, same company, same quarter, one number each, and only one of them can be checked.**

---

## 64. For the practitioner

If you take one operational habit from this case study, take this one.

**When a vendor gives you a number, ask three questions:**

1. **What document is it in?** A press release, a filing, a preprint and a peer-reviewed paper are four different standards of evidence, and the same company will use all four.
2. **How many observations is it based on, and what share of the whole does that cover?** Divide. If the coverage is under one percent, the number describes a sample and not your deployment.
3. **What would have had to happen for the number to be different?** If you cannot answer that, the number is not a measurement — it is a definition, and you have not been told what it is.

Three questions, five minutes, and they would have caught something in every one of the seven case studies in this arc.

---

## 65. Closing

The product in this case study may well be net-beneficial. Section 40 argues that it probably is, because the honest comparator is not a careful nurse but a call that never happens.

That is precisely why the reporting matters. A company with a genuinely good safety story — 6,234 clinicians, 307,000 calls, ~80% to 99.38% across three architecture generations, a severe-harm regression found and published — chose to lead with a zero that its own research does not support.

**The better story was already true, already measured, and already written down.**

---

*Day 86 of 90. Built from primary sources. 160 programmatic checks. Zero fabricated figures. One number that cannot be checked, and one that can.*
