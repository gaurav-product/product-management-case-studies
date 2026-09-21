# ASSUMPTIONS — Day 83, OpenEvidence, Inc. (private)

Companion to `README.md`. Separates what was **disclosed**, **derived**, **constructed**, **unavailable** and **deliberately excluded**.

**This case study departs from the Days 80–82 method, and this file is where that departure is accounted for.** OpenEvidence is private: there is no 10-Q, no 10-K, no audited statement and no filing obligation. Nothing in Part 1 below is an audited figure. Every company-sourced number in this case study is a **claim** — something a company asserted and nobody verified.

Period: company claims to January 2026; federal dockets to 21 September 2026.
Verification: `verify.py`, **164 checks, all passing**.

---

## Part 0 — The claim/fact boundary

The gate asserts this boundary mechanically so that no sentence in the README can promote a claim into a fact:

```
audited_financial_statements_exist            = False
regulatory_filing_obligation_exists           = False
company_claims_independently_confirmed        = False
day82_test_is_runnable_on_this_company        = False
headline_claim_count                          = 5
headline_claims_with_independent_confirmation = 0
unverifiable_claim_count                      = 14
```

The fourteen unverifiable categories: revenue, valuation, registered physician count, daily active users, consultation volume, hospitals reached, Americans treated, USMLE score, gross margin, cost per consultation, headcount, advertising rates, churn, retention.

**Three evidence tiers are used throughout, and the README distinguishes them in every section:**

| Tier | What it is | Example |
|---|---|---|
| **Verified fact** | Public record, checkable by anyone | Six federal dockets; FSMB census |
| **Claim** | A party asserted it; nobody checked | "More than 40% of physicians daily" |
| **Independent evidence** | A third party measured it | The medRxiv preprint |

---

## Part 1 — Disclosed facts

### 1.1 The federal court record — VERIFIED

From CourtListener's public search API, queried 21 September 2026. These are hard facts.

| Case | Court | Filed | Terminated | Cause | Judge |
|---|---|---|---|---|---|
| *OpenEvidence v. Pathway Medical*, 1:25-cv-10471 | D. Mass. | 2025-02-26 | 2025-10-23 | 18 U.S.C. §1836(a) | Myong J. Joun |
| *OpenEvidence v. Doximity*, 1:25-cv-11802 | D. Mass. | 2025-06-20 | — | 18 U.S.C. §1836(b) | Richard G. Stearns |
| *OpenEvidence v. Veracity-Health*, 3:25-cv-05376 | N.D. Cal. | 2025-06-26 | — | 15 U.S.C. §1125 | Charles R. Breyer |
| *OpenEvidence v. Doximity*, 4:25-mc-80387 | N.D. Cal. | 2025-12-15 | — | Civil miscellaneous | Kandis A. Westmore |
| *Longley v. OpenEvidence*, 1:26-cv-13165 | D. Mass. | 2026-07-09 | — | 9 U.S.C. §1 | George A. O'Toole Jr. |
| *Eaton v. OpenEvidence*, 5:26-cv-00651 | E.D.N.C. | 2026-09-08 | — | — | James C. Dever III |

Counsel of record — OpenEvidence: Quinn Emanuel Urquhart & Sullivan; Goodwin Procter; Weil, Gotshal & Manges. Doximity: Morrison & Foerster; WilmerHale; Skadden, Arps, Slate, Meagher & Flom.

Eight individuals appear as named parties across the Pathway and Doximity matters.

### 1.2 Litigation detail from Doximity's Form 10-Q — VERIFIED

Accession 0001516513-26-000040, Note 12, verified in this series on Day 82. This is a certified filing and is the strongest evidence in the case study about what the parties allege.

- OpenEvidence alleges unauthorised access to its platform; claims under the CFAA, breach of contract, unjust enrichment and trespass to chattels.
- Doximity counterclaims for false advertising (Lanham Act), Massachusetts Ch. 93A and common-law defamation.
- 2026-01-22: OpenEvidence's trespass-to-chattels claim dismissed; two Doximity counterclaims dismissed; motions denied as to all other claims.
- 2026-05-26: Doximity granted leave to amend counterclaims regarding OpenEvidence's alleged dissemination of false and misleading statements.
- 2026-06-30: case stayed pending mediation.

### 1.3 Government source — VERIFIED

Federation of State Medical Boards: **1,082,187** licensed physicians in the United States. 2024 census, published 15 August 2025. Used as the denominator throughout.

### 1.4 Company claims — NOT VERIFIED

All from OpenEvidence press releases. Each is a claim.

| Claim | Stated | Source |
|---|---|---|
| Daily use | "actively used daily, on average, by more than 40% of physicians in the U.S." | BusinessWire, 2026-01-21 |
| Registered physicians | 760,000 (Dec 2025) | BusinessWire, 2026-01-21 |
| Registered physicians | "430,000+", "~40% of U.S. physicians" (Jul 2025) | Secondary reporting of the Jul 2025 release |
| Consultations | "about 18 million" (Dec 2025); "about 3 million" a year earlier | BusinessWire, 2026-01-21 |
| Revenue | topped "$100 million in annual revenue last year" | BusinessWire, 2026-01-21 |
| Facilities | "more than 10,000 hospitals and medical centers nationwide" | BusinessWire, 2026-01-21 |
| Patients | "more than 100 million Americans were treated by a doctor using OpenEvidence" | BusinessWire, 2026-01-21 |
| Funding | "nearly $700M" over the past 12 months | BusinessWire, 2026-01-21 |
| Superlative | "the most used AI tool by physicians" | BusinessWire, 2026-01-21 |
| Partnerships | "first official AI partnerships" with NEJM, AMA, NCCN, ACC | BusinessWire, 2026-01-21 |
| Business model | Free to verified physicians; advertising revenue | Company statements |
| Benchmark | 90% USMLE (2023) → 100% (2025) | Company statements |
| Affiliation | "OpenEvidence is a Mayo Clinic Platform Accelerate Company" | Company website |

Funding rounds: Series A Feb 2025, $75M at $1.0B; Series B Jul 2025, $210M at $3.5B; Series C Oct 2025, $200M at $6.0B; Series D Jan 2026, $250M at $12.0B.

**Sourcing caveat.** Only the Series D release was retrieved directly; openevidence.com returned HTTP 403 to automated retrieval. Series A and Series C details, and the July 2025 "430,000+ / ~40%" wording, rest on secondary reporting and are flagged as such wherever used. This is a real weakness in the evidence chain and is not papered over.

### 1.5 NOHARM — a claim about a study, from both litigants

From OpenEvidence's PR Newswire release, 20 July 2026: a randomized study of **101** board-certified U.S. physicians; in the free-choice arm physicians reached for OpenEvidence in **22.3%** of responses against **19.8%** for all other external AI combined; the benchmark evaluated 45 large language models and 4 clinical AI systems with 12,747 expert annotations across 4,249 potential clinical actions. Run by ARISE, described as led by physicians from Stanford and Harvard Medical Schools.

The same release states the NOHARM studies **"are not peer reviewed and should be taken with a grain of salt."**

Doximity's CEO separately claimed, in its Q1 FY2027 earnings release, that Doximity Ask was "the top-performing U.S.-based model in the NOHARM benchmark" (verified on Day 82).

### 1.6 Independent evaluation — THIRD-PARTY, NOT PEER REVIEWED

Preprint, medRxiv, posted 4 December 2025: "The accuracy and repeatability of OpenEvidence on complex medical subspecialty scenarios: a pilot study." Authors at UT Southwestern Medical Center, Virginia Commonwealth University and Centennial High School, Frisco TX. No funding; no declared competing interest.

100 MedXpertQA subspecialty scenarios, two independent evaluators. Quick search accuracy 34% / 28%; Deep Consult 41% / 38%. χ² p = 0.09. Concordance on repeat: quick search 77%, Deep Consult 72%. Cohen's kappa 0.74 / 0.69. In 2–6% of responses the output gave an answer not among the available options.

Authors describe it as a pilot study, likely underpowered for subgroup analysis, with limited API access.

---

## Part 2 — Derived figures

Computed by `verify.py`. Reproducible by running the gate.

### 2.1 Litigation

| Figure | Value |
|---|---|
| Total federal cases | 6 |
| As plaintiff / defendant | 4 / 2 |
| Plaintiff share | **66.67%** |
| Trade-secret actions | 2 |
| Lanham Act actions as plaintiff | 1 |
| Distinct districts | 3 |
| Cases open / terminated | 5 / 1 |
| Span, first to most recent filing | **559 days** |
| Implied filing rate | **3.92 per year** |
| Pathway dismissal → re-addition to Doximity case | **6 days** |

### 2.2 Adoption claims tested against the FSMB denominator

| Figure | Value |
|---|---|
| 430,000 as a share of US licensed physicians | **39.73%** |
| Gap versus the "~40%" characterisation | **0.27pp** |
| 760,000 as a share of US licensed physicians | **70.23%** |
| Implied daily active physicians at "more than 40%" | **432,875** |
| **Implied daily-active as a share of registered** | **56.96%** |
| Offcall figure minus company daily figure | **5.00pp** |
| Physicians implied by the Offcall 45% | **486,984** |

### 2.3 Volume and intensity

| Figure | Value |
|---|---|
| Consultation growth | **+500.00%** (**6.00×**) |
| Registration growth, Jul→Dec 2025 | **+76.74%** |
| Gap | **423.26pp** |
| Consultations per registered physician per month | **23.68** |
| Consultations per registered physician per year | **284.16** |
| Consultations per implied daily user per month | **41.58** |
| Consultations per implied daily user per day | **1.39** |

### 2.4 Unit economics and funding

| Figure | Value |
|---|---|
| Annual consultation run-rate | **216.00M** |
| **Revenue per consultation** | **$0.46** |
| Revenue per registered physician per year | **$131.58** |
| Valuation-to-revenue multiple | **120.00×** |
| Capital raised as a multiple of claimed revenue | **7.35×** |
| Total across four rounds | **$735.00M** |
| Last three rounds | **$660.00M** |
| Valuation multiple since Series A | **12.00×** |
| Valuation steps A→B / B→C / C→D | **3.50× / 1.71× / 2.00×** |

### 2.5 NOHARM

| Figure | Value |
|---|---|
| OpenEvidence lead over all other external AI | **2.50pp** |
| Any external AI used | **42.10%** |
| **No external AI used** | **57.90%** |
| OpenEvidence share of external-AI usage | **52.97%** |
| Annotations per clinical action | **3.00** |
| Annotations per physician | **126.21** |

### 2.6 Independent evaluation

| Figure | Value |
|---|---|
| Quick search mean accuracy | **31.00%** |
| Deep Consult mean accuracy | **39.50%** |
| Difference | **8.50pp**, not significant (p = 0.09) |
| Evaluator spread, quick / deep | **6.00pp / 3.00pp** |
| **Quick search discordance** | **23.00%** |
| **Deep Consult discordance** | **28.00%** |

### 2.7 The invalid comparison, computed only to carry its caveat

| Figure | Value |
|---|---|
| Claimed USMLE improvement, 2023→2025 | **10.00pp** |
| Naive USMLE-minus-MedXpertQA gap | **69.00pp** |

```
usmle_and_medxpertqa_are_same_benchmark = False
naive_comparison_is_invalid             = True
medxpertqa_is_harder_by_design          = True
```

**This gap is not a finding and must never be quoted as one.** MedXpertQA is built to be far harder than licensing-exam questions. The figure exists in the gate solely so that the caveat is forced to travel with it.

---

## Part 3 — Author constructs

**None of the following is disclosed data.**

### 3.1 Frameworks

RICE, MoSCoW, Kano, JTBD, AARRR, HEART, Porter's Five Forces, Business Model Canvas, SWOT and the PRD in section 31 are applied by the author. OpenEvidence publishes none of them.

### 3.2 RICE inputs

| ID | R | I | C | E | Stress |
|---|---|---|---|---|---|
| P1 | 760 | 3.0 | 0.90 | 4.0 | 0.95 |
| P2 | 760 | 3.0 | 0.80 | 8.0 | 0.85 |
| P3 | 760 | 2.0 | 0.95 | 3.0 | 0.95 |
| P4 | 760 | 2.5 | 0.70 | 7.0 | 0.70 |
| P5 | 760 | 2.0 | 0.55 | 14.0 | 0.40 |

Reach is held at 760 (thousands of registered physicians **as claimed** — itself an unverified number, which is a limitation of the model). Stress factors encode the author's judgement about dependence on uncheckable claims plus execution and litigation exposure.

**P5 ranks last under stress by 82.04%**, asserted programmatically by the gate rather than argued in prose, per series rule. Base and stressed rankings are identical.

### 3.3 Personas

Dr. Sarah M. and Marcus L. are **composite constructions** — not real people, not customer research, not drawn from any disclosure. They are a device for reasoning about a product whose user and payer are different parties.

### 3.4 North Star and guardrails

"Repeatability-adjusted answered consultations" is the author's proposal. The 10% discordance target, the 30% expansion floor logic and the advertiser-separation guardrail are the author's. The **23.00%** current estimate is from the medRxiv preprint, not from the company.

### 3.5 Scenarios and sensitivity

All of section 47 and section 48 are author constructs applying arithmetic to stated claims:

- **Scenario A** halves the daily-use claim to 20%. The halving is arbitrary and illustrative.
- **Scenario B** assumes a 30× valuation multiple as a reference point. The company has never stated a target multiple.
- **Scenario C** applies the author's 10% discordance target.
- **Section 48's CPM range** ($100–$500) is the author's assumption about pharmaceutical HCP advertising pricing. **The company has never disclosed its ad load, pricing basis or CPM**, and the revenue may not be sold on an impression basis at all — in which case the entire calculation does not apply. Section 48.1 says so explicitly.

None are forecasts.

### 3.6 Eval plan, failure modes, human-in-the-loop, playbook

Sections 23, 24, 25 and 58 are entirely the author's product judgement. No clinical expertise is claimed. The failure-mode ranking is by the author's estimate of expected harm.

### 3.7 Recommendations, roadmap, and the model-strategy hypothesis

All six recommendations, the MoSCoW allocation and the three-horizon roadmap are the author's. Section 46's suggestion that the discordance finding points at sampling temperature, retrieval variance or non-deterministic routing is an **explicitly labelled hypothesis**, not an established fact — no public source discloses OpenEvidence's architecture.

### 3.8 The ladder and the category questions

The four-rung disclosure ladder (section 35), the four-day synthesis (section 56) and the open category questions (section 57) are the author's framing of a pattern across four unrelated companies. Interpretation, not a disclosed relationship.

---

## Part 4 — Unavailable information

Stated as gaps rather than estimated.

| Not available | Consequence |
|---|---|
| Any audited financial statement | No figure in Part 1.4 can be confirmed |
| Revenue, margin, cost structure | Unit economics rest entirely on claims |
| Ad load, CPM, pricing basis | Section 48 is a range of possibilities, not a finding |
| **Whether advertisers influence the answer surface** | **The highest-stakes unknown in this business** |
| Clinical outcomes or harm-avoided measures | Product efficacy unassessable |
| Accuracy by specialty or question type | Only an aggregate from one pilot exists |
| Retention, churn, cohort behaviour | Engagement claims uncheckable |
| Model architecture | Section 46 is hypothesis only |
| Content licence terms, cost, duration | Supplier risk unquantifiable |
| USMLE evaluation protocol, date, version | The benchmark claim cannot be situated |
| Offcall survey methodology and sample size | The 45% figure cannot be assessed |
| Board composition, control, cap table | Governance unassessable |
| Revenue concentration by advertiser | Concentration risk unquantifiable |
| Litigation spend | Only the firm roster is observable |

**No figure in this case study fills any of these gaps by estimation.**

---

## Part 5 — Deliberate exclusions

| Excluded | Reason |
|---|---|
| PACER document texts (complaints, answers, orders) | Not retrieved. Docket **metadata** from CourtListener; allegation detail from Doximity's 10-Q only. **No complaint text is quoted anywhere in this case study.** |
| Podcast and interview material | Not primary, not checkable |
| CB Insights, Crunchbase, PitchBook | Aggregators, not primary |
| Market data of any kind | Series rule |
| Forbes / CNBC / TechCrunch reporting | Used only to locate primary sources and to establish Series A and Series C details, flagged at 1.4 |
| The company's product itself | Not tested by the author; no first-hand evaluation is claimed |

### 5.1 On including valuation at all

This series excludes market data by rule. Valuation is included here because for a private company it is not a market price but a **company claim**, reported in the company's own release, and it is the only financial datum available. It is treated as a claim throughout and appears in the unverifiable list.

### 5.2 On the Days 80–82 comparators

Day 80's **59.43%** acquisition share, Day 81's **97%** human-hour reduction, and Day 82's **$6.40M** AI cost, **94.95%** margin share and **$570.399M** FY2026 revenue are **recomputed inside this case study's own `verify.py`** rather than carried across as prose. Series rule: no case study asserts a number its own gate has not verified.

---

## Part 6 — Fairness statement

Because this case study is critical of an evidentiary environment rather than of a product, four things are stated plainly.

**Nothing here asserts that any OpenEvidence claim is false.** The finding is that the claims are unverifiable, which is a different and narrower thing.

**Nothing here asserts that any party to any litigation did anything wrong.** A complaint is an allegation. Surviving a motion to dismiss means only that a claim was adequately pleaded. The Doximity matter is stayed for mediation and may settle with no finding either way.

**The independent study is thin and is treated as thin.** One preprint, n=100, two evaluators, no peer review, limited API access. Its **31.00%** accuracy figure is not presented as the truth about OpenEvidence's accuracy. Its **23.00%** discordance figure is more robust to benchmark difficulty but rests on the same small sample.

**Section 50 sets out what OpenEvidence does better than the three public companies preceding it**, and section 51 runs the counterfactual in which every company claim is true. The analysis is designed to survive the company being right about itself.

---

## Verification statement

`verify.py` contains **164 checks** and exits non-zero on any failure. It asserts the court record; the FSMB denominator; every adoption, volume, unit-economic and funding derivation; the NOHARM arithmetic including the **57.90%** neither company quoted; the independent study's accuracy and repeatability figures; the scenario and sensitivity arithmetic; the RICE base and stressed rankings with the proposal ranking last under stress named by the gate; the Days 80–82 comparators; and — critically — the fourteen unverifiable categories and the zero-of-five confirmation count.

`crosscheck.py` independently extracts every two-decimal figure from `README.md` and `ASSUMPTIONS.md` and confirms each traces to a gate value. A figure in the prose the gate does not produce is a build failure.

**Fabricated figures: 0.**
**Verified company claims: 0 — which is the finding.**

---

*Day 83 of 90. OpenEvidence, Inc. (private). Court record to 21 September 2026; company claims to January 2026.*
