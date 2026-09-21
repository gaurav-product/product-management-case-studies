# Day 83 — OpenEvidence, Inc. (private)

### There is no filing to check. So the only place the claims get tested is court.

> **90-Day PM Case Study Challenge — Day 83**
> Evidence-based product teardown built only from primary sources.
> Every derived figure is produced by `verify.py` (164 programmatic checks) before a word of prose was written.
> **This case study uses a different method from Days 80–82, and section 2 explains why.**

---

## 1. One-paragraph summary

Yesterday's case study ended with a test: take a company's AI marketing claims, search for them in its SEC filings, and see which ones survive. OpenEvidence is the company that breaks the test — not because its claims fail it, but because **the test cannot be run.** OpenEvidence is private. There is no 10-Q, no 10-K, no audited statement, no disclosure obligation of any kind. Its headline claims — daily use by more than 40% of U.S. physicians, 18 million monthly consultations, over $100 million in revenue, a 100% score on the USMLE — appear only in its own press releases, and **not one of the five has independent confirmation.** What OpenEvidence does have is a federal court docket: **six cases in 559 days**, four as plaintiff, two as defendant, across three districts, litigated by Quinn Emanuel, Goodwin Procter and Weil Gotshal. In court, statements are made under Rule 11. In a press release they are not. For a company with no filing obligation, **litigation is the only adversarial disclosure regime it has** — and that, not the AI, is the most interesting thing about this product.

---

## 2. Why this case study uses a different method

Days 80, 81 and 82 were built on SEC EDGAR. Each figure came from a 10-Q or a 10-K, and `verify.py` asserted arithmetic against as-filed values. That method is unavailable here, and the honest response is to change the method rather than to pretend the evidence is equivalent.

**What this gate can verify:**

1. **The court record.** Case numbers, courts, filing dates, causes of action, judges, parties and dispositions, from the public federal dockets. These are hard facts, as solid as anything in the series.
2. **Internal consistency.** The company's own claims tested against *each other* and against an authoritative external denominator. Arithmetic on stated claims is verifiable even when the claims are not.
3. **Independent evidence.** The one independent evaluation of the product that exists, reported at its own precision and with its own stated limits.

**What it cannot verify, and says so programmatically:**

```
audited_financial_statements_exist       = False
regulatory_filing_obligation_exists      = False
company_claims_independently_confirmed   = False
day82_test_is_runnable_on_this_company   = False
unverifiable_claim_count                 = 14
```

Revenue, valuation, user counts, consultation volume, hospitals reached, USMLE score, margins, headcount, churn — fourteen categories are asserted as **UNVERIFIABLE** in the gate itself, so that no sentence downstream can quietly promote a claim into a fact.

This distinction is the whole case study. Read everything below with it in mind: where this document says "claims," it means a company said it and nobody checked.

---

## 3. Company identification

| Field | Value | Source |
|---|---|---|
| Legal name | OpenEvidence, Inc. | Federal dockets |
| Status | **Private** — no public filings | — |
| Founded | 2022 | Secondary reporting |
| Founders | Daniel Nadler, Zachary Ziegler | Secondary reporting |
| Headquarters | Cambridge / Boston, Massachusetts | Docket venue |
| Product | Clinical AI reference and search for verified physicians | Company website |
| Business model | **Free to verified physicians; revenue from advertising** | Company statements |
| Affiliation claimed | "OpenEvidence is a Mayo Clinic Platform Accelerate Company" | Company website |

### 3.1 The register note, inverted

Every prior case study in this series has included a register-classification note — the SIC or NIC code that misdescribes the business. OpenEvidence has no such code to examine, because it has no registration obligation that produces one.

That is the inversion worth sitting with. For 82 days this series has criticised register codes for being coarse and misleading. Here there is no code at all, and the absence is worse than a bad one. A wrong code at least tells you somebody had to file something.

---

## 4. What OpenEvidence actually sells, and to whom

The product is a clinical reference tool. A verified physician asks a clinical question and receives a synthesised, citation-backed answer drawn from the medical literature. The company describes a second mode, Deep Consult, for more involved queries, and a literature-triage feature it calls TL;Dr.

Physicians pay nothing. **Revenue comes from advertising.**

### 4.1 The sentence that explains the litigation

OpenEvidence sells pharmaceutical advertising against physician attention.

So does Doximity.

That single fact reframes everything in section 8. These two companies are described in the press as rivals in clinical AI. They are more precisely rivals for the **same pharmaceutical marketing budget**, reaching the **same physician population**, with **the same monetisation model**. The trade-secret litigation between them is a fight over an advertising market that happens to be conducted in the vocabulary of AI.

```
both_monetise_via_pharma_advertising = True
```

Day 82 established Doximity's FY2026 revenue at **$570.399M**. OpenEvidence claims over **$100M**. On the claimed figures Doximity is **5.70×** larger by revenue — while, on the claimed figures, OpenEvidence reaches more physicians.

### 4.2 The consequence nobody discloses

If the product is free to the user and paid for by advertisers, then **the answer surface is also an advertising surface**, and the only question that matters for clinical safety is whether advertiser relationships influence what a physician is shown.

No public source — company or independent — addresses this. It is not in the gate because there is nothing to put there. It is the single most important undisclosed fact about this product, and it recurs in sections 24, 25.1 and 28.

---

## 5. Problem statement

The stated problem is real and well evidenced: the biomedical literature grows faster than any clinician can track — the company's own framing is that it "expands by two papers every minute, 24 hours a day" — and physicians need answers at the point of care in seconds, not a literature review in an afternoon.

That problem is genuine. Nothing in this case study disputes it, and the adoption figures, even discounted, suggest the product addresses it well enough that physicians return to it.

The problem this case study examines is different: **when a clinical tool this widely used is accountable to no disclosure regime, how does anyone — a physician, a hospital, a regulator — establish whether it works?**

---

## 6. The five headline claims

These are the claims that carry OpenEvidence's public narrative. All five come from company press releases.

| Claim | Stated value | Source |
|---|---|---|
| Daily physician use | "actively used daily, on average, by more than 40% of physicians in the U.S." | Jan 2026 release |
| Registered physicians | 760,000 U.S. physicians (Dec 2025) | Jan 2026 release |
| Consultation volume | "about 18 million clinical consultations" in Dec 2025, up from "about 3 million" a year earlier | Jan 2026 release |
| Revenue | topped "$100 million in annual revenue last year" | Jan 2026 release |
| Benchmark | 90% on USMLE (2023), rising to 100% (2025) | Company statements |

```
headline_claim_count                            = 5
headline_claims_with_independent_confirmation   = 0
```

**None of the five has independent confirmation.** That is not an accusation that any is false. It is a statement about the evidentiary environment: there is no mechanism by which anyone outside the company could establish that any of them is true.

---

## 7. Testing the claims against each other

Claims that cannot be verified externally can still be tested internally. The Federation of State Medical Boards counts **1,082,187 licensed physicians** in the United States (2024 census, published 15 August 2025). That is an authoritative denominator, and it lets several claims be checked against one another.

### 7.1 The July 2025 claim holds

In July 2025 the company reported **430,000+ registered physicians** and characterised this as roughly 40% of U.S. physicians.

| Measure | Value |
|---|---|
| 430,000 as a share of 1,082,187 | **39.73%** |
| Gap versus the "~40%" characterisation | **0.27pp** |

That checks out. The characterisation was accurate and the denominator was the right one.

### 7.2 By January 2026, the same number means something different

| Measure | Value |
|---|---|
| 760,000 registered as a share of U.S. licensed physicians | **70.23%** |
| Claim in the same release | "used **daily**, on average, by **more than 40%** of physicians in the U.S." |

```
forty_pct_meant_registered_in_jul2025          = True
forty_pct_meant_daily_use_in_jan2026           = True
metric_definition_changed_while_number_did_not = True
```

In July 2025, **40% meant registered**. In January 2026, **40% means daily active**. The number did not move. The metric underneath it did.

This is exactly the failure Day 82 found at Doximity, where "prescribers" in a CEO quote and "providers" in the 10-Q were different populations presented as though comparable. Here it is the same company, six months apart, using the same figure for two different things.

### 7.3 What the daily claim implies

| Measure | Value |
|---|---|
| Implied daily active physicians (40% of 1,082,187) | **432,875** |
| Registered physicians claimed (Dec 2025) | 760,000 |
| **Implied daily-active as a share of registered** | **56.96%** |

A product where **57% of everyone who ever registered uses it every single day** would be among the most engaging software ever built, in any category. That may be what is happening — clinical reference is a high-frequency job, and a physician in clinic has a reason to open it hourly.

But it is an extraordinary figure, it is nowhere substantiated, and it follows from combining two claims the company itself never combined. The gate flags the threshold rather than the judgement:

```
dau_ratio_exceeds_50_pct = True
```

### 7.4 Consultation volume is internally coherent

| Measure | Value |
|---|---|
| Consultations per registered physician per month | **23.68** |
| Consultations per implied daily user per month | **41.58** |
| Consultations per implied daily user per day | **1.39** |

A daily user averaging **1.39** consultations per day is entirely plausible. The volume claim is not where the tension is. The tension is the 56.96% in 7.3 — the *population*, not the *intensity*.

### 7.5 Intensity grew faster than the user base

| Measure | Value |
|---|---|
| Registered physicians, Jul 2025 → Dec 2025 | **+76.74%** |
| Monthly consultations, Dec 2024 → Dec 2025 | **+500.00%** (6.00×) |
| Gap | **423.26pp** |

Consultation growth outran registration growth by a wide margin, which means existing users increased their usage rather than growth coming from new sign-ups alone. Measured over different windows — a limitation noted in Appendix A — but directionally this is the healthiest signal in the entire claim set, and it is the one the company emphasises least.

### 7.6 A third number, from a fourth source

The January 2026 release attributes its adoption figure to a survey by Offcall, which reportedly found **45%** of physicians using OpenEvidence.

| Measure | Value |
|---|---|
| Offcall figure minus the company's daily-use figure | **5.00pp** |
| Physicians implied by 45% | **486,984** |

```
offcall_methodology_disclosed  = False
offcall_sample_size_disclosed  = False
```

Neither the sample size nor the methodology is disclosed in the sources examined. A survey figure of 45% and a company figure of "more than 40% daily" are not the same measurement, and the release does not distinguish them.

---

## 8. The litigation, which is the real disclosure record

Six federal cases name OpenEvidence, Inc.

| # | Case | Court | Filed | Status | Cause of action |
|---|---|---|---|---|---|
| 1 | *OpenEvidence v. Pathway Medical* — 1:25-cv-10471 | D. Mass. | 2025-02-26 | **Terminated 2025-10-23** | 18 U.S.C. §1836(a) — injunction against trade-secret misappropriation |
| 2 | *OpenEvidence v. Doximity* — 1:25-cv-11802 | D. Mass. | 2025-06-20 | Open | 18 U.S.C. §1836(b) — Defend Trade Secrets Act |
| 3 | *OpenEvidence v. Veracity-Health* — 3:25-cv-05376 | N.D. Cal. | 2025-06-26 | Open | 15 U.S.C. §1125 — Lanham Act trademark infringement |
| 4 | *OpenEvidence v. Doximity* — 4:25-mc-80387 | N.D. Cal. | 2025-12-15 | Open | Civil miscellaneous (ancillary discovery) |
| 5 | *Longley v. OpenEvidence* — 1:26-cv-13165 | D. Mass. | 2026-07-09 | Open | 9 U.S.C. §1 — U.S. Arbitration Act |
| 6 | *Eaton v. OpenEvidence* — 5:26-cv-00651 | E.D.N.C. | 2026-09-08 | Open | — |

| Measure | Value |
|---|---|
| Total cases | **6** |
| As plaintiff | **4** (66.67%) |
| As defendant | **2** |
| Distinct districts | **3** |
| Cases in D. Mass. | **3** |
| Span, first filing to most recent | **559 days** |
| Implied filing rate | **3.92 cases per year** |
| Cases terminated | **1** |
| Cases still open | **5** |

A company founded in 2022 has been party to six federal cases in under nineteen months, and initiated four of them.

### 8.1 The Pathway manoeuvre

The procedural sequence is worth laying out, because it is visible only in the docket and it shows deliberate strategy.

- **26 Feb 2025** — OpenEvidence sues Pathway Medical and six named individuals in D. Mass. under the Defend Trade Secrets Act.
- **20 Jun 2025** — OpenEvidence sues Doximity, separately, under the DTSA.
- *Between these dates, Doximity acquires Pathway Medical.*
- **23 Oct 2025** — OpenEvidence **voluntarily dismisses** the standalone Pathway case.
- **29 Oct 2025** — OpenEvidence amends its Doximity complaint to add Pathway and further individuals as defendants.

```
pathway_dismiss_to_readd_days = 6
```

**Six days.** The claims were not abandoned; they were consolidated into the case against the acquirer. Eight individuals appear as named parties across the two matters — six in the Pathway case, two more added in the Doximity case.

That detail matters for a product manager for a specific reason: **individual engineers were named personally in federal litigation.** Whatever the merits, that is the environment in which clinical AI talent currently moves between these two companies.

### 8.2 What each side is actually alleging

From Doximity's 10-Q (verified in this series on Day 82), OpenEvidence alleges the defendants gained unauthorised access to its platform, asserting claims under the Computer Fraud and Abuse Act, breach of contract, unjust enrichment and trespass to chattels. Doximity counterclaims for **false advertising under the Lanham Act**, Massachusetts Chapter 93A, and common-law defamation.

Note the discrepancy in how the case is characterised: the docket's cause of action is the **Defend Trade Secrets Act**, while the 10-Q enumerates CFAA, contract, unjust enrichment and trespass. Both descriptions are of the same case, from different vantage points. Documented in Appendix A rather than resolved.

Dispositions:

| Date | Ruling |
|---|---|
| 2026-01-22 | OpenEvidence's trespass-to-chattels claim **dismissed**; two Doximity counterclaims (Lanham Act, Ch. 93A) **dismissed**; motions denied as to all other claims |
| 2026-05-26 | Doximity granted **leave to amend** counterclaims, adding allegations about OpenEvidence's alleged dissemination of false and misleading statements about Doximity |
| 2026-06-30 | Case **stayed** pending mediation |

### 8.3 The recursion

Read 8.2 again alongside section 6.

OpenEvidence's five headline claims have no independent confirmation and no filing to check them against. And the live counterclaim against OpenEvidence, which survived a motion to dismiss and which the court then allowed to be *expanded*, is **false advertising**.

```
dox_counterclaim_is_false_advertising = True
```

The one forum in which OpenEvidence's public claims are being adversarially tested is a lawsuit it started.

That is the thesis of Day 83 in a sentence. A private company's marketing is checked by nobody — until it sues a public one, and the public one checks back.

### 8.4 OpenEvidence as Lanham Act plaintiff

The symmetry goes further. In *OpenEvidence v. Veracity-Health* (N.D. Cal., filed 26 June 2025), OpenEvidence is itself the plaintiff under **15 U.S.C. §1125 — the Lanham Act**, the same statute Doximity has invoked against it.

```
lanham_cases_as_plaintiff = 1
```

OpenEvidence is simultaneously alleging that a competitor misrepresents itself, and defending an allegation that it misrepresents itself.

### 8.5 The counsel roster as a capital-allocation signal

| Side | Firms of record |
|---|---|
| OpenEvidence | Quinn Emanuel Urquhart & Sullivan; Goodwin Procter; Weil, Gotshal & Manges |
| Doximity | Morrison & Foerster; WilmerHale; Skadden, Arps, Slate, Meagher & Flom |

Six of the most expensive litigation practices in the United States, on a single dispute, for a company whose claimed annual revenue is just over **$100M**.

The spend is not disclosed and is not computable:

```
guardrail_litigation_spend_computable = False
top_tier_firms_retained_by_oe         = 3
```

But the roster is observable, and for a product manager it is the signal. **A company that retains Quinn Emanuel has decided that its competitive position is a legal asset**, not only a product one. That is a strategy choice with a real opportunity cost, and it is being made at a scale that is material relative to claimed revenue.

---

## 9. The NOHARM convergence

This is where Day 82 and Day 83 collide, and it is the strongest finding across the two days.

**Day 82.** Doximity's CEO, in the Q1 FY2027 earnings release: *"our clinical AI assistant, Doximity Ask, was the top-performing U.S.-based model in the NOHARM benchmark."* Day 83's gate confirms that claim appears zero times in Doximity's 10-Q or 10-K.

**Day 83.** OpenEvidence, in a press release dated 20 July 2026: *"Physicians Choose OpenEvidence Over Every Other AI Chatbot Combined in Independent Stanford-Harvard Study of Clinical AI"* — the study being NOHARM, run by ARISE, described as a clinical AI research network led by physicians from Stanford and Harvard Medical Schools.

```
noharm_cited_by_openevidence = True
noharm_cited_by_doximity     = True
competitors_citing_same_benchmark = 2
```

**Both litigants claim a win from the same benchmark.**

### 9.1 Both claims can be true

They are measuring different things.

| Company | What it claimed from NOHARM |
|---|---|
| Doximity | **Model performance** — top-performing U.S.-based model |
| OpenEvidence | **Revealed preference** — physicians reached for it more than all other external AI combined |

```
noharm_oe_claim_is_revealed_preference = True
noharm_dox_claim_is_model_performance  = True
noharm_claims_are_mutually_compatible  = True
```

A benchmark that evaluates both which model scores best and which tool physicians choose can produce both results at once. Neither company is contradicting the other. **Both are selecting the dimension on which they won.**

### 9.2 The NOHARM figures, and the one neither quoted

| Measure | Value |
|---|---|
| Board-certified U.S. physicians in the free-choice arm | **101** |
| Responses using OpenEvidence | **22.3%** |
| Responses using all other external AI combined | **19.8%** |
| OpenEvidence's lead | **2.50pp** |
| OpenEvidence's share of external-AI usage | **52.97%** |
| **Responses using no external AI at all** | **57.90%** |

Scope: 45 large language models and 4 clinical AI systems, 12,747 expert annotations across 4,249 potential clinical actions — **3.00** annotations per action, **126.21** per physician.

The headline is accurate: 22.3% does exceed 19.8%, and "more than every other external AI combined" is a fair reading.

But in the arm where physicians could reach for anything at all, **57.90% of responses used no external AI tool.** The most common choice was not OpenEvidence, and it was not ChatGPT. It was nothing.

Neither company quoted that number. It is the most informative figure in the study for anyone deciding whether clinical AI has actually been adopted into practice, as opposed to registered for.

### 9.3 The disclaimer, from the company doing the claiming

OpenEvidence's own press release states that **"the NOHARM benchmarking studies are not peer reviewed and should be taken with a grain of salt."**

```
noharm_not_peer_reviewed_per_openevidence = True
noharm_grain_of_salt_per_openevidence     = True
```

Put the two days together. A public company anchored its principal AI quality claim — the only AI quality claim in its quarter, made by its CEO, in an unaudited release — to a benchmark that **the other company claiming a win from it publicly describes as not peer reviewed and to be taken with a grain of salt.**

Both statements are from the companies' own releases. Neither requires anyone's interpretation.

### 9.4 What a product manager should take from this

A benchmark cited by both sides of a lawsuit, disclaimed by one of them, and used to support two different claims is not evidence of product quality. **It is marketing collateral that both parties found useful.**

The test is simple and general: when a vendor cites a benchmark, ask what the benchmark measured, who else cites it, what *they* claim from it, and whether the vendor's own materials caveat it. If a competitor cites the same study for the opposite conclusion, the study is not settling anything.

---

## 10. The only independent evaluation of the product

One independent evaluation of OpenEvidence exists in the sources examined: a pilot study posted to medRxiv on 4 December 2025, by authors at UT Southwestern Medical Center, Virginia Commonwealth University and Centennial High School in Frisco, Texas.

```
mrx_peer_reviewed          = False
mrx_funded_by_openevidence = False
```

It is a **preprint, not peer reviewed**. The authors declared no funding and no competing interest. They describe it as a pilot study, likely underpowered for subgroup analysis, with limited API access preventing full-dataset testing.

### 10.1 What it found

100 complex medical subspecialty scenarios from MedXpertQA, scored by two independent evaluators, across both product modes.

| Measure | Quick search | Deep Consult |
|---|---|---|
| Evaluator 1 accuracy | 34% | 41% |
| Evaluator 2 accuracy | 28% | 38% |
| **Mean accuracy** | **31.00%** | **39.50%** |
| Evaluator spread | **6.00pp** | **3.00pp** |
| **Concordance (same answer on repeat)** | **77%** | **72%** |
| **Discordance** | **23.00%** | **28.00%** |
| Cohen's kappa | 0.74 | 0.69 |

Deep Consult scored **8.50pp** higher, but the difference was **not statistically significant** (χ², p = 0.09).

### 10.2 The accuracy figures require a caveat, and here it is

The company claims a **100%** USMLE result. This study reports **31.00%** on MedXpertQA. The arithmetic gap is **69.00pp** — and comparing the two directly would be **invalid**.

```
usmle_and_medxpertqa_are_same_benchmark = False
naive_comparison_is_invalid             = True
medxpertqa_is_harder_by_design          = True
```

MedXpertQA is deliberately constructed to be far harder than licensing-exam questions — it exists precisely because models saturate USMLE-style benchmarks. A low score on it is expected and is **not** evidence that the USMLE claim is false.

The gate computes the 69.00pp gap only so that this caveat is forced to travel with it. **The finding is not that the company overstated its benchmark. The finding is that no mechanism exists to reconcile the two numbers, because nothing obliges anyone to publish a comparable measurement.**

### 10.3 The repeatability finding, which needs no caveat

The accuracy comparison is contested. The repeatability result is not, and it is the more important number.

**Ask the same clinical question twice, and roughly one time in four you get a different answer.** 23.00% discordance in quick search, 28.00% in Deep Consult.

That finding is independent of benchmark difficulty. It does not matter how hard MedXpertQA is — a tool that answers the same question differently on repeat has a consistency problem, and consistency is not a nice-to-have in clinical reference. Two physicians on the same ward asking the same question about the same patient may receive different guidance.

```
mrx_deeper_mode_less_repeatable = True
```

And the deeper, more expensive mode is **less** repeatable than the quick one — 72% against 77%. More reasoning produced more variance. For a product manager that is the single most actionable line in this document: the premium mode's additional computation is not buying determinism, and the user has no way to know that.

### 10.4 Proportion and honesty about this study

One preprint, n=100, two evaluators, no peer review, limited API access, written partly by a high-school student. It is not definitive and this document does not treat it as such.

But it is **the entire independent evidence base for a product its maker says is used daily by more than 40% of American physicians.** That asymmetry is the point. The appropriate response is not to accept the 31% figure as the truth about OpenEvidence's accuracy. It is to notice that a clinical tool at this scale has attracted exactly one independent evaluation, and that it was nobody's job to produce a better one.

---

## 11. Funding and the valuation ladder

| Round | Date | Amount | Post-money valuation |
|---|---|---|---|
| Series A | Feb 2025 | $75M | $1.0B |
| Series B | Jul 2025 | $210M | $3.5B |
| Series C | Oct 2025 | $200M | $6.0B |
| Series D | Jan 2026 | $250M | $12.0B |

| Measure | Value |
|---|---|
| Total across the four rounds | **$735.00M** |
| Last three rounds | **$660.00M** |
| Valuation step, A→B | **3.50×** |
| Valuation step, B→C | **1.71×** |
| Valuation step, C→D | **2.00×** |
| **Valuation multiple since Series A** | **12.00×** |
| Months, Series A to Series D | **11** |

A 12× valuation increase in eleven months.

### 11.1 A note on including valuation at all

This series excludes market data by rule — no share prices, no market capitalisations, no multiples. Valuation is included here for one reason: for a private company it is not a market price but a **company claim**, reported in the company's own release, and it is the only financial datum available. It is treated throughout as a claim, not as a fact, and it is listed in the unverifiable set.

### 11.2 The only computable unit economics

Advertising revenue divided by the consultations that carry the advertising is the unit that matters, and the claims permit it.

| Measure | Value |
|---|---|
| Annual consultation run-rate, at the Dec 2025 rate | **216.00M** |
| Claimed revenue | $100M |
| **Revenue per consultation** | **$0.46** |
| Revenue per registered physician | **$131.58** |
| Valuation-to-revenue multiple | **120.00×** |
| Capital raised as a multiple of claimed revenue | **7.35×** |

Forty-six cents per clinical consultation. That is the whole business model in one number, and it is computed entirely from the company's own claims.

It is also the number that makes the strategy legible. At **$0.46** per consultation, the path to justifying a **$12.0B** valuation runs through volume, not price — which means every product decision that increases consultations is a revenue decision, and every decision that slows a physician down is a cost. Section 25.1 returns to what that pressure does to a clinical safety design.

---

## 12. User personas

Two personas, and as at Doximity, only one of them pays.

### 12.1 Dr. Sarah M. — attending physician (uses, does not pay)

Hospitalist, mid-career, high patient volume. Opens OpenEvidence several times a shift — a drug interaction, an unfamiliar presentation, a guideline she last read two years ago. Values that the answer carries citations, and that it takes fifteen seconds rather than fifteen minutes.

**Jobs to be done:** get a trustworthy answer fast enough to use in front of a patient; see the source so she can judge it herself; not have to leave the workflow she is already in.

**What she pays:** nothing.

**What she does not know:** whether the answer she just read would have been the same if she had asked five minutes earlier — the independent estimate says **23.00%** of the time it would not. And whether any commercial relationship influenced what was surfaced.

**Design implication:** her trust is the product's core asset and it is built on citations. Citations make an answer *checkable in principle*. They do not make it *consistent*, and consistency is the thing the only independent study found wanting.

### 12.2 Marcus L. — pharmaceutical brand lead (pays for everything)

Runs a specialty brand. Buys physician reach. Measures impressions against a defined specialty audience and, eventually, script lift.

**Jobs to be done:** reach the right prescribers at the moment of clinical decision; demonstrate channel effectiveness; place budget.

**Why this channel is valuable to him:** it is the highest-intent moment in medicine. A physician asking a clinical question about a condition is closer to a prescribing decision than a physician scrolling a newsfeed. **Proximity to the decision is the entire premium.**

**And that is the tension.** The thing that makes the inventory valuable to Marcus is precisely the thing that makes advertiser influence over the answer surface a clinical safety question rather than a marketing question. Sections 4.2 and 29 carry this forward.

### 12.3 Who is missing

There is no third persona, and that is itself the finding. At Doximity the health-system buyer (Day 82's Priya S.) sits between the clinician and the vendor, runs security review, and holds a renewal. **OpenEvidence's free-to-physician model removes that intermediary entirely.**

No procurement. No security review. No institutional evaluation. A physician signs up individually with an NPI number, and the tool enters clinical practice without any organisation ever having assessed it.

That is a remarkable distribution achievement and a remarkable governance gap, and they are the same fact.

---

## 13. Jobs to be Done

| Job | Who has it | How OpenEvidence serves it | Monetised? |
|---|---|---|---|
| "Answer this clinical question now" | Physician | Quick search | No — free |
| "Work through something complicated" | Physician | Deep Consult | No — free |
| "Keep up with new literature" | Physician | TL;Dr triage | No — free |
| "Show me the source so I can judge it" | Physician | Citations | No — free |
| "Reach prescribers at the decision point" | Pharma brand lead | Advertising | **Yes — entirely** |

Every physician job is free. The single monetised job belongs to the advertiser. The product has exactly one paying customer type and it is not the user.

---

## 14. Business Model Canvas

**Customer segments.** Pharmaceutical advertisers (paying). Verified U.S. physicians (using, not paying).

**Value propositions.** To physicians: fast, cited clinical answers, free. To advertisers: reach at the highest-intent moment in medicine.

**Channels.** Direct physician sign-up via NPI verification — no institutional gatekeeper. Direct enterprise sales to advertisers.

**Customer relationships.** No contract with the user. No procurement relationship with their employer.

**Revenue streams.** Advertising. **$0.46** per consultation on the claimed figures.

**Key resources.** The verified physician base; content licences with the AMA, NEJM, NCCN and the American College of Cardiology among others; the models.

**Key activities.** Model development and evaluation; publisher licensing; advertising sales; **litigation**.

**Key partners.** Medical publishers and societies; Mayo Clinic Platform; investors.

**Cost structure.** Inference; content licensing; engineering; sales; **top-tier litigation counsel at three firms**.

### 14.1 What the canvas exposes

Litigation appears as both a key activity and a cost line. In 82 previous case studies that has not happened. For OpenEvidence the docket is not an incidental legal matter — it is a strategic instrument, used four times as plaintiff in 559 days.

---

## 15. Competitive analysis

| Competitor | Overlap | Position |
|---|---|---|
| **Doximity** (Day 82) | Physician network, pharma advertising, clinical AI | Direct on all three; litigating both ways |
| **UpToDate (Wolters Kluwer)** | Clinical reference | The incumbent; subscription-paid, institutionally procured |
| **ChatGPT / Claude / Gemini** | General-purpose clinical Q&A | Free, ubiquitous, no clinical provenance |
| **Epic in-EHR AI** | Answers inside the record of truth | Distribution advantage OpenEvidence cannot match |
| **Veracity-Health** | Clinical AI | OpenEvidence sued it under the Lanham Act |

### 15.1 Porter's Five Forces

**Threat of new entrants — Moderate.** The models are not the moat; publisher licences and physician trust are. But NOHARM found **57.90%** of responses used no external AI at all, which says the category is not yet locked.

**Bargaining power of buyers — High.** Advertisers pay, and pharmaceutical budgets are discretionary and concentrated. The users have no contract and no switching cost whatsoever — a physician can leave mid-consultation.

**Bargaining power of suppliers — High and structural.** Medical publishers hold the licensed content that distinguishes this from a general chatbot. The AMA, NEJM and NCCN can reprice. This is the most underrated force in the business.

**Threat of substitutes — High.** A physician can ask a general-purpose model for free. The differentiators are citation provenance and clinical framing — real, but not durable.

**Competitive rivalry — Intense, and largely legal.** Four plaintiff-side federal actions in 559 days.

### 15.2 The moat question

Doximity's moat is a verified network of more than 85% of U.S. physicians, built over a decade. OpenEvidence's claimed reach is comparable and was built in about three years — because it gave the product away and bypassed procurement entirely.

That speed is the achievement. It is also the vulnerability: **what was acquired without procurement can be lost without procurement.** There is no contract, no renewal cycle and no institutional lock-in to slow a departure. The only retention mechanism is that the product is good enough to reopen tomorrow.

Which is precisely why the **23.00%** discordance figure matters more here than it would at a company with enterprise contracts.

---

## 16. SWOT

**Strengths.** Extraordinary claimed physician reach achieved in roughly three years. Free distribution that bypasses procurement. Licensed content from the AMA, NEJM, NCCN and ACC. Consultation intensity growing far faster than registration (**+500.00%** against **+76.74%**). **$735.00M** raised. Advertising at the highest-intent moment in medicine.

**Weaknesses.** No disclosure obligation and **zero of five** headline claims independently confirmed. Adoption metric changed definition while keeping the same number. **23.00%** answer discordance in the only independent test, worse in the premium mode. No institutional evaluation anywhere in the funnel. **$0.46** revenue per consultation. Litigation as a standing cost at three top-tier firms.

**Opportunities.** Publish a repeatability rate and own a dimension no competitor discloses. Commission genuine peer-reviewed evaluation. Convert free physician reach into institutional contracts. Disclose advertiser separation and make governance a differentiator.

**Threats.** A live false-advertising counterclaim that survived dismissal and was expanded. Publisher licence repricing. Epic and Microsoft distribution inside the EHR. Zero switching cost. A **120.00×** valuation-to-revenue multiple on claimed revenue that nobody has audited.

---

## 17. Metrics: what exists, what does not

### 17.1 Claimed by the company

Daily use by "more than 40%" of U.S. physicians; 760,000 registered; ~18M monthly consultations; ">$100M" revenue; ">10,000 hospitals"; "more than 100 million Americans treated"; 100% USMLE.

### 17.2 Independently measured

**31.00%** mean accuracy on MedXpertQA and **23.00%** answer discordance — one preprint, n=100, not peer reviewed. That is the complete list.

### 17.3 Not measured anywhere

- Whether advertiser relationships influence the answer surface
- Clinical outcomes, or any harm-avoided measure
- Time saved per consultation
- Rate at which physicians act on an answer
- Accuracy by specialty, question type, or patient population
- Retention or churn
- Cost per consultation

**The third list decides whether this product is safe and whether it works. It is empty.**

---

## 18. Proposed North Star metric

**Repeatability-adjusted answered consultations** — the share of consultations that would return the same clinical answer if the same question were asked again.

```
north_star_computable_by_company = True
north_star_computable_by_public  = False
```

Unlike Day 82's proposed north star, this one **is computable today** — internally. The company can ask its own system the same question twice at scale for a trivial fraction of its inference budget. The only reason the number does not exist publicly is that nobody has to publish it.

### 18.1 Why this rather than accuracy

Accuracy is contested, benchmark-dependent and expensive to establish. Repeatability is none of those things. It is cheap, unambiguous, and it is a *floor condition*: a tool that cannot answer consistently cannot be accurate reliably, whatever a benchmark says. It is the measurement with the best ratio of clinical significance to cost of production, and it is the one the independent study could produce on n=100 with no cooperation from the company.

### 18.2 Guardrails

**Guardrail 1 — answer discordance rate.** Independent estimate **23.00%**. Not disclosed by the company. Target: below 10%, published quarterly.

**Guardrail 2 — adoption metric denominator stability.** Already breached: the 40% figure changed from registered to daily-active between July 2025 and January 2026.
```
guardrail_denominator_stability_breached = True
```

**Guardrail 3 — advertiser separation.** Not computable from outside, and the most important of the three. Minimum viable version: publish whether commercial relationships can influence answer content or ordering, and who inside the company can change that.

---

## 19. User journey

| Stage | Physician experience | OpenEvidence cost | OpenEvidence revenue |
|---|---|---|---|
| Discovery | Hears about it from a colleague | — | — |
| Verification | Enters NPI number, verified as a physician | Verification cost | — |
| First consultation | Asks a question, gets a cited answer | **Inference begins** | **Ad impression begins** |
| Habit | Opens it several times per shift | **Inference scales with use** | **Revenue scales with use** |
| Advocacy | Recommends to the ward | Inference scales further | Revenue scales further |

### 19.1 The structural contrast with Day 82

At Doximity, cost scales with usage and revenue is a seat-based step function that moves once a year. Adoption is a cost event before it is a revenue event, and the gross margin showed it.

At OpenEvidence, **cost and revenue scale together**, because the monetisation is per-impression rather than per-seat. That is a structurally better fit between the cost curve and the revenue curve, and it is a genuine advantage of the advertising model that Day 82's analysis makes visible by contrast.

The trade-off is what sits on the other side of it. A model where revenue rises with every consultation puts commercial pressure on the answer surface itself. Doximity's seat-based pricing has a margin problem; OpenEvidence's impression-based pricing has a governance problem. **Neither is free.**

### 19.2 The missing gate

There is no step in this journey at which any institution evaluates the tool. No procurement, no security review, no clinical governance committee, no medical staff approval. A physician verifies an NPI and begins using a clinical reference product in patient care.

---

## 20. AARRR funnel

| Stage | Position | Evidence |
|---|---|---|
| **Acquisition** | Exceptional — 430,000 → 760,000 registered in five months | Company claims |
| **Activation** | Strong — consultations grew **500.00%** against registration **+76.74%** | Company claims |
| **Retention** | Claimed extraordinary (**56.96%** implied daily/registered); unverified | Derived from claims |
| **Referral** | Peer recommendation in clinical settings; not measured | — |
| **Revenue** | **$0.46** per consultation | Derived from claims |

The funnel is wide everywhere and thin only at revenue per unit. That is a deliberate choice, not a failure: the company is buying reach now and pricing later.

---

## 21. HEART framework

| Dimension | Proposed measure | Disclosed? |
|---|---|---|
| **Happiness** | Physician satisfaction with answer quality | No |
| **Engagement** | Consultations per active physician per week | Partially — monthly figures only |
| **Adoption** | First consultation within 7 days of verification | No |
| **Retention** | Week-4 retention by specialty cohort | No |
| **Task success** | **Did the physician act on the answer?** | **No** |

Task success is the entire question and it is the one nobody measures. A cited answer that a physician reads and discards has consumed inference and produced an ad impression, and has changed no clinical decision. On the advertising model, **that consultation is worth exactly as much as one that changed a prescription.**

That is the deepest misalignment in this business, and unlike most of this document it is not a disclosure problem. It is a design problem, and it would exist even if everything were disclosed.

---

## 22. Kano analysis

| Feature | Category | Reasoning |
|---|---|---|
| Cited sources | **Must-be** | An uncited clinical answer is unusable |
| Fast response | **Must-be** | Slower than a colleague means it goes unused |
| **Consistent answers** | **Must-be** | And the only independent measurement says **23.00%** discordance |
| Deep Consult mode | **Performance** | More depth, more value — but **less repeatable** |
| Literature triage (TL;Dr) | **Attractive** | Unexpected, builds habit outside the query loop |
| Specialty tuning | **Performance** | Value scales with fit |

Consistency is a must-be, and it is the one with an independent measurement against it. Must-be failures do not reduce satisfaction gradually — they break trust discontinuously. A physician who catches the tool contradicting itself once on a question they know well may stop trusting it on questions they do not.

---

## 23. Eval plan

What a clinical reference product at this scale should be running, none of which is disclosed.

**Repeatability suite.** The same question, asked n times, across specialties and phrasings. Report the distribution, not the mean. This is cheap and it is the north star in section 18.

**Accuracy against adjudicated ground truth.** Board-certified reviewers, stratified by specialty and question type, inter-rater reliability reported. Expensive; no substitute.

**Citation fidelity.** Does the cited source actually support the claim it is attached to? This is distinct from accuracy and is the specific failure mode that erodes trust in a citation-based product fastest — a real citation attached to a claim it does not support is worse than no citation, because it survives spot-checking.

**Adversarial safety.** Negation handling, drug-name confusion pairs, dose units, paediatric weight-based dosing, contraindication retrieval.

**Commercial-influence audit.** Hold questions constant and vary nothing; confirm answer content and ordering are invariant to advertiser relationships. Publish the method.

**Release gating.** No model version ships without non-regression on the safety and repeatability suites. Benchmark scores are not a release criterion.

---

## 24. Ranked failure modes

Ranked by expected harm.

**1. A confidently wrong clinical answer acted upon.** Highest harm. Mitigation: uncertainty surfaced at the span level, refusal outside the evidence base, mandatory citation.

**2. Citation that does not support the claim.** High harm, and specifically corrosive because the citation is the trust mechanism. Mitigation: automated claim-to-source entailment checking before display.

**3. Answer inconsistency on repeat.** **Independently measured at 23.00%.** Two clinicians, same question, different guidance. Mitigation: determinism controls; publish the rate.

**4. Advertiser influence on clinical content.** Potentially the highest harm on this list, and unranked above only because there is no evidence either way. Mitigation: structural separation, audited and published.

**5. Negation or dose inversion.** Known model failure mode with a short path to patient harm. Mitigation: dedicated release-gating test suite.

**6. Automation complacency.** Physicians check less as trust grows. Worsens as the product improves. Mitigation: monitor per-user acceptance trending toward unquestioning.

**7. Silent regression after a model update.** Nobody notices because usage is the only tracked metric. Mitigation: continuous repeatability monitoring with alerting.

Failure modes 1–6 are clinical. Only number 3 has any public measurement, and it came from a high-school student and two academics with limited API access rather than from the company.

---

## 25. Human-in-the-loop design

The physician is the human in the loop. The question, as on Day 82, is whether the loop is load-bearing or ceremonial.

Here it is genuinely better than at most AI products, for one specific reason: **citations make the loop checkable.** A physician can click through and read the source. That is real, and it is the strongest safety property this product has.

Three things would make it load-bearing rather than available:

**Surface disagreement between sources.** When the literature conflicts, say so rather than synthesising a confident single answer. Conflict is clinically informative; smoothing it away destroys information.

**Surface uncertainty at the span level.** Highlight which parts of an answer are weakly supported. A physician who knows which sentence is shaky will check that sentence.

**Show when an answer has changed.** If the same question returned something different last week — which the independent study says happens **23.00%** of the time — the physician should be told. Currently they cannot know.

### 25.1 The conflict of interest in loop design

On an advertising model, every second a physician spends checking a citation is a second not generating another consultation. A loop that is genuinely load-bearing is **slower**, and slower means fewer impressions.

That does not mean the company has degraded its loop — there is no evidence of that and none is alleged. It means the incentive points the wrong way, permanently, and a product manager should name that rather than assume good intentions will hold at scale.

---

## 26. AI cost per consultation

Not computable, and the reason is instructive.

| Known | Value |
|---|---|
| Claimed revenue | $100M |
| Claimed annual consultation run-rate | **216.00M** |
| **Revenue per consultation** | **$0.46** |

| Unknown | |
|---|---|
| Inference cost per consultation | Not disclosed |
| Content licensing cost | Not disclosed |
| Gross margin | Not disclosed |

Day 82 could compute Doximity's AI cost because a reviewed filing disclosed it. Here the revenue side is a claim and the cost side does not exist publicly at all.

What can be said: at **$0.46** of revenue per consultation, the inference cost per consultation must be a small fraction of that for the model to work at scale — which constrains how much computation can be spent per answer. **Deep Consult, the mode that reasons longer, is also the mode the independent study found least repeatable at 72%.** Whether those two facts are related is unknown and unknowable from outside, but it is the question a product manager should ask first.

---

## 27. Pricing analysis

| Model | Alignment with user value | Alignment with clinical safety | Current |
|---|---|---|---|
| Free + advertising | Poor — value to user, revenue from third party | **Weak — revenue scales with impressions** | **Current** |
| Physician subscription | Good | Good | — |
| Institutional licence | Good | Good — brings procurement back | — |
| Hybrid: free tier + paid institutional | Good | Good | — |

The free-plus-advertising model achieved the distribution. It is also the model that removes procurement, removes institutional evaluation, and makes the answer surface commercially valuable.

**The obvious fix — institutional licensing — would reintroduce the gatekeeper the company routed around to grow this fast.** That is a genuine strategic conflict, not an oversight, and it is why the recommendation in section 28 sequences disclosure before pricing.

---

## 28. Product recommendations

Six recommendations. Each names the evidence and the proof metric.

### R1. Publish a repeatability rate with every model release

**Evidence:** `guardrail_discordance_disclosed_by_company = False`; independent estimate **23.00%**.
**Proposal:** Publish the answer-discordance rate quarterly, with a fixed method, alongside each model version.
**Why this one first:** cheapest, most clinically meaningful, entirely within the company's control, and no competitor discloses it. It converts the sharpest external criticism into a differentiator.
**Success:** two consecutive quarters published with an unchanged method, and a declining rate.
**Cost:** Low.

### R2. Commission an independent peer-reviewed accuracy study

**Evidence:** `mrx_peer_reviewed = False`; one preprint is the entire evidence base.
**Proposal:** Fund an independent, pre-registered, peer-reviewed evaluation with published protocol, and commit to publishing the result whatever it says.
**Why:** the current position — 100% USMLE claimed by the company, 31.00% on a harder benchmark found by a preprint — is unreconcilable by anyone, and that ambiguity is a liability in live false-advertising litigation.
**Success:** publication in a peer-reviewed venue with the company as funder but not author.
**Cost:** Moderate. The real cost is accepting the result in advance.

### R3. Fix the adoption metric to one definition with a fixed denominator

**Evidence:** `metric_definition_changed_while_number_did_not = True`.
**Proposal:** Publish registered, monthly-active and daily-active separately, each against the FSMB denominator, each named explicitly.
**Why:** beyond accuracy — a company defending a false-advertising counterclaim should not have a headline metric that changed meaning while keeping its number.
**Success:** three definitions, three numbers, one denominator, held stable for a year.
**Cost:** Low technically. Higher politically: the honest daily-active figure will be smaller than "more than 40%."

### R4. Disclose advertiser separation from the answer surface

**Evidence:** sections 4.2, 24 and 25.1. No public source addresses this.
**Proposal:** Publish whether commercial relationships can influence answer content or ordering, what technical separation exists, and who can change it.
**Why:** this is the highest-harm undisclosed fact about the product. It is also the one where a clean answer would be a genuine and durable competitive advantage.
**Success:** a published policy plus an external audit attestation.
**Cost:** Moderate. Low if the separation already exists; high if it does not — which is precisely why the disclosure is informative.

### R5. Surface answer changes and source conflict to the physician

**Evidence:** **23.00%** discordance; failure modes 2 and 3.
**Proposal:** Show when a repeated question yields a different answer, and show when the underlying literature conflicts rather than synthesising it away.
**Why:** converts the repeatability weakness into a transparency feature, and gives the clinician the information they need to apply judgment.
**Success:** measurable increase in citation click-through without a fall in consultations.
**Cost:** Moderate — a real product change, not a disclosure.

### R6. Build an institutional evaluation path

**Evidence:** section 12.3 — no procurement, no security review, no clinical governance anywhere in the funnel.
**Proposal:** Offer hospitals a formal evaluation package: security review materials, an accuracy dossier, an advertiser-separation attestation and usage reporting.
**Why:** creates the institutional relationship that free distribution deliberately skipped, without taking anything away from the physician.
**Success:** named institutional agreements that do not reduce individual sign-ups.
**Cost:** High. This is the one that changes the company's shape.

---

## 29. RICE prioritisation

Reach, Impact, Confidence, Effort and every stress factor are **author estimates, not disclosed data**. Reach is held at 760 (thousands of registered physicians as claimed), because each proposal's audience is the clinician user base. The stress factor discounts each proposal by how much of its value rests on claims that are currently uncheckable, plus execution exposure.

| ID | Proposal | R | I | C | E | Base | Stress | Stressed |
|---|---|---|---|---|---|---|---|---|
| P1 | Publish a repeatability rate every release | 760 | 3.0 | 0.90 | 4.0 | **513.00** | 0.95 | **487.35** |
| P3 | One adoption metric, fixed denominator | 760 | 2.0 | 0.95 | 3.0 | **481.33** | 0.95 | **457.27** |
| P2 | Independent peer-reviewed accuracy study | 760 | 3.0 | 0.80 | 8.0 | **228.00** | 0.85 | **193.80** |
| P4 | Disclose advertiser influence | 760 | 2.5 | 0.70 | 7.0 | **190.00** | 0.70 | **133.00** |
| P5 | Voluntary audited financials ahead of any IPO | 760 | 2.0 | 0.55 | 14.0 | **59.71** | 0.40 | **23.89** |

```
rice_base_ranking           = ('P1', 'P3', 'P2', 'P4', 'P5')
rice_stress_ranking         = ('P1', 'P3', 'P2', 'P4', 'P5')
rice_last_under_stress      = 'P5'
rice_last_under_stress_name = 'Publish voluntary audited financials ahead of any IPO'
rice_last_gap_pct           = 82.04
```

### 29.1 Reading the ranking

The order is stable under stress, which says the top proposals are robust rather than marginal.

**P5 ranks last, by 82.04% below P4** — asserted by the gate, not argued here. Voluntary audited financials would resolve more of this case study's complaints than anything else on the list: it would convert revenue, margin and user counts from claims into facts in one move. It ranks last because it has the lowest confidence (0.55), by far the highest effort (14 person-months), and the harshest stress factor (0.40).

The reasoning is not that transparency is unwise. It is that **a company in active false-advertising litigation, mid-mediation, will not voluntarily produce audited figures that opposing counsel could use.** The litigation posture makes the most complete remedy the least available one.

That is worth stating plainly because it generalises: **litigation does not only consume money and attention, it forecloses transparency options.** A company that sues its competitor has, as a side effect, made it harder to answer reasonable questions from everyone else.

P1 and P3 both lose only **5.00%** under stress, because neither depends on any contested claim — each requires only publishing a number the company already has. P5 loses **59.99%**.

---

## 30. MoSCoW

**Must have.** R1 (repeatability rate); R3 (fixed adoption metric); R4 (advertiser separation).

**Should have.** R2 (independent study); R5 (surface changes and conflict).

**Could have.** R6 (institutional evaluation path).

**Won't have this cycle.** Voluntary audited financials (P5) — sequencing, not rejection. See 29.1.

---

## 31. PRD: repeatability disclosure (R1)

**Problem.** The only independent evaluation of OpenEvidence found that the same clinical question returns a different answer **23.00%** of the time in quick search and **28.00%** in Deep Consult. The company publishes no repeatability figure, so physicians cannot know this and hospitals cannot evaluate it.

**Objective.** Publish a repeatability rate with every model release, under a fixed and public method.

**Proposed metric.** Answer-discordance rate: the share of a fixed question set for which two independent invocations return clinically non-equivalent answers, adjudicated by board-certified reviewers against a published equivalence rubric.

**Non-goals.** Not an accuracy claim. Not a safety certification. Not a replacement for peer-reviewed evaluation.

**Requirements.**
- R1.1 Fixed question set, stratified by specialty, versioned and published.
- R1.2 Published clinical-equivalence rubric — this is the hard part, since "different wording, same guidance" must not count as discordance.
- R1.3 Two independent invocations per question, minimum interval specified.
- R1.4 Board-certified adjudication with inter-rater reliability reported.
- R1.5 Published per model version, with prior versions restated if the method changes.

**Success criteria.** Two consecutive releases published under an unchanged method, with a declining rate. Secondary: adoption of the metric by a competitor, which would make it a category standard.

**Risks.** The first number may be worse than 23.00%. It becomes a commitment that cannot be withdrawn. Competitors will benchmark against it. **All three are arguments for publishing it** — a metric that cannot embarrass you is not a metric.

---

## 32. Roadmap

**Horizon 1 — next two quarters.** R1 (repeatability rate), R3 (fixed adoption metric). Low effort, high credibility, no strategic disruption. These establish that the company will publish numbers that can move against it.

**Horizon 2 — quarters three and four.** R4 (advertiser separation), R5 (surface changes and conflict). R4 requires legal alignment; R5 is a real product change that Horizon 1's instrumentation makes measurable.

**Horizon 3 — year two.** R2 (independent peer-reviewed study), R6 (institutional evaluation path). Both are only credible once Horizons 1 and 2 have produced a track record.

**Deliberately unscheduled.** Voluntary audited financials. Revisit when the litigation resolves — see 29.1.

### 32.1 Sequencing logic

Ordered by **evidence dependency and litigation exposure**, not by impact. Every later item needs an earlier one to be credible, and the most complete remedies are the ones the lawsuit currently forecloses.

---

## 33. Risks to this analysis

**The evidence base is thin, and that is the subject rather than a flaw.** A private company with no filing obligation gives an outside analyst very little. This document is explicit about which statements are claims and which are verified, and the gate asserts the distinction mechanically. But a reader should hold every company-sourced number loosely.

**The independent study is one preprint.** n=100, two evaluators, not peer reviewed, limited API access, acknowledged by its authors as underpowered. Section 10.4 says so. Its **31.00%** accuracy figure should not be treated as the truth about OpenEvidence's accuracy, and the **23.00%** discordance figure, while more robust to benchmark difficulty, rests on the same small sample.

**The USMLE comparison is invalid and is marked invalid.** MedXpertQA and USMLE are different benchmarks of different difficulty. The gate records the 69.00pp arithmetic gap and asserts `naive_comparison_is_invalid = True` so the caveat cannot be dropped.

**Court filings are allegations.** Nothing in section 8 establishes that any party did anything wrong. A complaint is a claim; a surviving motion to dismiss means only that a claim was adequately pleaded. The case is stayed for mediation and may settle with no finding.

**The 56.96% daily-active ratio is derived, not claimed.** It combines a percentage-of-all-physicians claim with a registered-user claim the company never presented together. The company may define its terms in a way that reconciles them. Flagged in Appendix A.

**Different measurement windows.** Registration growth is measured July–December 2025; consultation growth is measured December 2024–December 2025. The **423.26pp** gap in 7.5 is directional, not a like-for-like comparison.

**RICE inputs are the author's.** Declared in section 29 and in ASSUMPTIONS.md.

---

## 34. What a product manager should take from this

**A claim with no filing behind it is not a weaker claim — it is an unfalsifiable one.** Day 82 asked which marketing claims survive a search of the filings. Day 83 is the case where that test returns nothing, because there are no filings. Before treating a private vendor's adoption or accuracy figure as information, ask what document it would have to appear in for anyone to be accountable for it. Often the answer is none.

**Watch the number that stays the same while its meaning changes.** OpenEvidence's 40% meant registered users in July 2025 and daily active users in January 2026. Doximity's prescribers and providers were different populations quoted as one. This is the most common metric failure in the series and it is nearly invisible unless you write the definition down each time you see the number.

**A benchmark cited by both sides of a lawsuit is settling nothing.** NOHARM was invoked by Doximity for model performance and by OpenEvidence for revealed preference, and OpenEvidence's own release says it is not peer reviewed and should be taken with a grain of salt. When a vendor cites a benchmark, find out who else cites it and what they claim from it.

**Read the number nobody quoted.** In NOHARM's free-choice arm, **57.90%** of responses used no external AI at all. Both companies quoted their own share of the remaining 42.1%. The most important finding in a study is often the one that serves no one's press release.

**Consistency is a must-be, and almost nobody measures it.** A tool that answers the same clinical question differently **23.00%** of the time has a problem no accuracy benchmark will reveal. Repeatability is cheap to measure, clinically decisive, and absent from every AI disclosure in this four-day arc.

**Free distribution routes around the people whose job is to evaluate you.** Giving the product to physicians directly is why OpenEvidence reached this scale in three years. It is also why no security review, no procurement process and no clinical governance committee has ever assessed it. Distribution speed and evaluation rigour were traded against each other, and the trade was never made explicit.

---

## 35. The four-rung disclosure ladder

| Rung | Company | Status | What is actually disclosed about AI |
|---|---|---|---|
| 1 | **Day 80 — Hims & Hers** | Public | **No AI metric at all** |
| 2 | **Day 81 — Hinge Health** | Public | A **cost** metric (~**97%** human care hour reduction); no outcome |
| 3 | **Day 82 — Doximity** | Public | AI **cost audited** in the 10-Q (**$6.40M**, **94.95%** of the margin contraction); all four AI claims quote-only |
| 4 | **Day 83 — OpenEvidence** | **Private** | **No filing exists.** Claims tested only in litigation |

```
ladder_length        = 4
ladder_private_count = 1
```

Four companies, four positions on a ladder, and **not one of them has disclosed an AI outcome metric.**

The ladder descends in accountability even as it ascends in candour. Doximity discloses the most and is the most exposed for it — its AI cost is in a certified filing precisely because it had to be. OpenEvidence discloses whichever numbers it chooses, in whatever form, because nothing compels otherwise.

**Disclosure quality is a function of obligation, not of virtue.** That is the four-day finding.

---

## 36. The two litigants, side by side

| Measure | Day 82 — Doximity | Day 83 — OpenEvidence |
|---|---|---|
| Status | Public (NYSE: DOCS) | Private |
| Monetisation | **Pharma advertising** | **Pharma advertising** |
| Revenue | **$570.399M** (FY2026, audited) | ">$100M" (claimed) |
| Revenue ratio | **5.70×** | — |
| Physician reach | >85% of U.S. physicians (network members) | 70.23% registered, ">40% daily" (claimed) |
| Pricing to clinician | Bundled in health-system seats | Free |
| AI cost disclosed | **$6.40M**, in the 10-Q | Not disclosed |
| Independent evaluation | None | One preprint |
| AI claims in a reviewed filing | **0 of 4** | **No filing exists** |
| Federal cases (this dispute) | Defendant + counterclaimant | **Plaintiff, 4 cases in 559 days** |

They sell the same thing to the same people and are suing each other about it. Doximity is 5.70× larger by revenue on the claimed figures; OpenEvidence claims greater physician reach. Both anchor AI quality claims to the same non-peer-reviewed benchmark.

---

## 37. Recommended diagrams

Per series standard from Day 50: **no Mermaid**. Markdown tables and ASCII only.

**D1 — Where the claims live.** Three columns: "In a certified filing" (empty for OpenEvidence), "In a press release" (all five headline claims), "In a court filing" (the litigation claims, under Rule 11). The empty first column is the image.

**D2 — The 40% that changed meaning.** A timeline: Jul 2025, 430,000 registered = 39.73% of U.S. physicians. Jan 2026, 760,000 registered = 70.23%, and "40%" now denotes daily use. Same number, two definitions.

**D3 — The NOHARM split.** A single stacked bar of 100% of responses: OpenEvidence 22.3%, all other external AI 19.8%, **no external AI 57.90%** — with the third segment highlighted and captioned "the number neither company quoted."

**D4 — Repeatability.** Two bars: quick search 77% concordance, Deep Consult 72%, with discordance shaded and the caption that the deeper mode is less consistent.

**D5 — The litigation timeline.** Six cases on a 559-day axis, plaintiff filings above the line and defendant filings below, with the six-day Pathway dismissal-to-re-addition gap annotated.

### 37.1 ASCII rendering of D1

```
   IN A CERTIFIED FILING     |   IN A PRESS RELEASE      |  IN A COURT FILING
   (officer certification)   |   (no legal standard)     |  (Rule 11 applies)
  ---------------------------+---------------------------+--------------------
                             |  >40% of US physicians    |  Trade secret claims
        ( N O N E )          |  760,000 registered       |  CFAA claims
                             |  18M monthly consults     |  Lanham Act claims
   OpenEvidence is private   |  $100M+ revenue           |  Contract claims
   and files nothing.        |  100% on USMLE            |
                             |                           |
   VERIFIABLE CLAIMS:  0     |  CONFIRMED:  0 of 5       |  6 CASES, 559 DAYS
```

---

## 38. Recommended screenshots and visual assets

1. The CourtListener docket header for *OpenEvidence Inc. v. Doximity, Inc.*, 1:25-cv-11802, showing the DTSA cause of action and Judge Stearns.
2. The January 2026 press release passage containing "used daily, on average, by more than 40% of physicians in the U.S."
3. The July 2025 passage characterising 430,000 registered physicians as ~40% — placed directly beside item 2.
4. The FSMB census headline, 1,082,187 licensed physicians.
5. The medRxiv abstract showing the concordance figures.
6. The PR Newswire passage stating the NOHARM studies "are not peer reviewed and should be taken with a grain of salt."

Items 2 and 3 side by side are the strongest single visual in this case study. All are public documents.

---

## 39. Appendix A — source conflicts and reconciliations

Series rule: every conflict is documented, never silently resolved.

### A1. Series D date — December 2025 or January 2026

One secondary source dates the $250M Series D to December 2025; the company's own BusinessWire release is dated **21 January 2026**, as is contemporaneous reporting.

**Resolution:** the company's own release date is used. The December reference likely reflects when the round closed rather than when it was announced. Not material to any derived figure.

### A2. Total funding — "$735M" or "nearly $700M"

The four disclosed rounds sum to **$735.00M**. The company's January 2026 release describes "nearly $700M" raised "over the past 12 months."

**Reconciliation:** the last three rounds (Series B, C, D) sum to **$660.00M**, which is consistent with "nearly $700M over the past 12 months" if the February 2025 Series A is excluded from that window. Both figures are computed in the gate and both are reported. **Not treated as a discrepancy** — the two statements measure different windows.

### A3. Adoption — 40% (company) versus 45% (Offcall)

The company claims daily use by "more than 40%" of U.S. physicians. The Offcall survey it cites reportedly found **45%** using the product. Gap: **5.00pp**.

**Not reconciled.** These are different measurements — one a daily-use claim, one a survey of usage — and neither the sample size nor the methodology of the Offcall survey is disclosed in the sources examined.

### A4. The Doximity case — DTSA or CFAA

The docket's cause of action for 1:25-cv-11802 is **18 U.S.C. §1836(b), Defend Trade Secrets Act**. Doximity's 10-Q describes OpenEvidence's claims as arising under the CFAA, breach of contract, unjust enrichment and trespass to chattels.

**Not a conflict.** A docket records one governing cause for administrative purposes; a complaint may plead many counts. Both descriptions are accurate from their respective vantage points. Reported as stated on both sides.

### A5. The 56.96% daily-active ratio is derived, not claimed

This figure combines the "more than 40% of U.S. physicians daily" claim with the 760,000 registered claim. **The company never presented these two figures as a ratio.** The derivation is this document's, it is flagged in the gate, and the company may define its terms in a way that reconciles them.

### A6. Measurement windows differ

Registration growth (**+76.74%**) covers July–December 2025. Consultation growth (**+500.00%**) covers December 2024–December 2025. The **423.26pp** gap in section 7.5 is directional and is not a like-for-like comparison.

### A7. USMLE versus MedXpertQA

Addressed at length in 10.2. The **69.00pp** arithmetic gap is computed in the gate solely so the invalidity caveat travels with it. `naive_comparison_is_invalid = True`.

---

## 40. Appendix B — sources examined and not used

**PACER document texts.** The underlying complaints, answers and orders were not purchased or retrieved. Docket *metadata* — case numbers, causes, dates, parties, judges, counsel — comes from the public CourtListener search API. Allegation detail comes from Doximity's 10-Q, a primary source verified on Day 82. **No complaint text is quoted in this document**, and no characterisation of the pleadings goes beyond what the 10-Q states.

**The company's own website beyond the landing page.** Fetched; it returned no user counts, funding figures, founding date or benchmark scores. Only the advisory-board affiliations, the Mayo Clinic Platform statement and the literature-growth framing were available, and those are cited where used.

**Podcast and interview material.** Excluded. Not primary, and not checkable.

**Forbes, CNBC, TechCrunch and similar reporting.** Used only to locate primary sources and to establish the funding history where the company's own release is unavailable. No figure in this document rests on secondary reporting alone except the Series A and Series C details, which are flagged as such in ASSUMPTIONS.md Part 1.

**CB Insights, Crunchbase and similar databases.** Excluded — aggregators, not primary.

**Market data.** Excluded by series rule. Valuation is included only as a company claim; see 11.1.

---


---

## 41. Content licensing — the supplier power nobody prices

OpenEvidence's differentiator against a general-purpose chatbot is not the model. It is that the answers are grounded in licensed, citable medical literature. The company has announced content partnerships with the American Medical Association, the *New England Journal of Medicine*, the National Comprehensive Cancer Network and the American College of Cardiology, among others.

That is a genuine moat, and it is rented.

### 41.1 Why this is the most underrated risk in the business

Porter's supplier force (section 15.1) is rated high for a specific structural reason: **the suppliers are the only party in this market who can verify the product's core claim and who also hold a contractual lever over it.** A medical society knows whether its guidelines are being represented accurately. It also controls whether they can be used at all.

Three things follow that no public source addresses:

- **Term and renewal.** No licence length, renewal date or exclusivity provision is disclosed for any partnership.
- **Cost.** Content licensing is a cost line that does not appear anywhere. At **$0.46** of revenue per consultation, a licensing repricing has nowhere to hide.
- **Accuracy conditions.** Whether any licence conditions continued use on faithful representation of the licensed content is unknown — and that is exactly the clause a publisher would want after reading a **23.00%** discordance finding.

### 41.2 The asymmetry with Doximity

Doximity's moat is a network it owns outright. OpenEvidence's moat is content it licenses from parties who could license it to anyone. A network cannot be repriced by a third party; a content licence can.

---

## 42. NPI verification as a product decision

The product verifies physicians by National Provider Identifier. That single choice produces most of the company's strategic position, good and bad.

**What it buys.** A clean, verified, high-value audience — exactly what a pharmaceutical advertiser will pay a premium for. It also creates instant credibility for the user: this is a room of clinicians, not the open internet.

**What it costs.** NPI verification confirms that someone *is* a registered provider. It does not confirm specialty scope, active practice, or that the person holding the number is the person typing. It is an identity gate, not a competence or context gate.

**What it removes.** By verifying the individual, the product no longer needs the institution. That is the decision that bypassed procurement (section 12.3) and produced three-year scale — and the same decision that means no hospital has ever run a security review.

### 42.1 The denominator problem it creates

The FSMB counts **1,082,187** licensed physicians. NPI numbers are issued far more broadly than to licensed physicians and are not withdrawn on retirement. So "registered physicians" and "licensed physicians" are drawn from different registries, and every percentage in section 7 inherits that mismatch.

This is not a criticism of the company's arithmetic — the FSMB denominator is the right one to use and the July 2025 figure checked out against it at **39.73%**. It is a caution about precision: figures like **70.23%** should be read as approximate, because the numerator and denominator come from different systems that count different populations.

---

## 43. Regulatory exposure

OpenEvidence sits close to a boundary that is moving.

Clinical decision support software falls outside FDA device regulation when a clinician can independently review the basis for the recommendation — which is precisely why citation-backed answers are not merely a trust feature but a **regulatory posture**. The citations are what make the tool reviewable, and reviewability is what keeps it on the unregulated side of the line.

That has two consequences a product manager should hold:

**The citation feature cannot be degraded for speed.** Whatever commercial pressure exists to shorten answers (section 25.1), the citation is load-bearing in a legal sense, not only a UX sense.

**Citation fidelity becomes a regulatory question, not just a quality one.** If a citation does not support the claim attached to it — failure mode 2 — then the clinician cannot in fact independently review the basis, and the premise of the exemption weakens. This is why section 23 ranks citation fidelity as a distinct evaluation axis rather than folding it into accuracy.

No public source addresses OpenEvidence's regulatory classification, and this section makes no claim about it. It identifies where the question sits.

---

## 44. Trust, safety and privacy

Three obligations follow from what this product is.

**Physicians must be able to tell model output from source text.** Citation-backed synthesis blurs this by design: the answer is generated, the sources are real. The boundary between what the literature says and what the model concluded is the boundary that matters clinically, and it is the hardest one to render in an interface.

**Query content is clinically sensitive.** A physician's questions describe patients, even when de-identified — a rare presentation plus a timestamp plus a specialty can be identifying. What is retained, for how long, and whether query content informs advertising targeting is not disclosed in any source examined. Given that the business is advertising, this is not a hypothetical concern.

**Errors must be traceable to a model version.** When an answer is wrong, the organisation needs to know which version produced it, on what input, and which other answers are affected. Most products build this after the first incident.

---

## 45. The talent question

Eight individuals are named as parties across the Pathway and Doximity matters — six in the first, two more added in the second.

```
individuals_in_pathway_case  = 6
individuals_in_doximity_case = 8
```

Naming individual engineers personally in federal trade-secret litigation is lawful and not unusual in this area of law. It is also a signal about the labour market these two companies share.

For a product leader the implication is practical: **clinical AI is a small talent pool, and movement between the two largest players in it now carries personal legal exposure.** That raises the cost of hiring from a competitor, slows the diffusion of practice between organisations, and makes candidates more cautious about what they can say in an interview about what they have built.

Whether the claims have merit is for the court. The chilling effect on mobility exists either way, and it is a cost that does not appear in any budget.

---

## 46. Model strategy

No public source discloses whether OpenEvidence trains its own models, fine-tunes open-weight models, calls third-party APIs, or combines these. This matters more than it usually would, for two reasons the evidence makes concrete.

**The repeatability finding points at the architecture.** A **23.00%** discordance rate is what you would expect from non-zero sampling temperature, a retrieval step that returns different passages on different calls, or an ensemble with non-deterministic routing. All three are architectural choices, and all three are fixable — determinism is largely a configuration decision, traded against answer diversity. The fact that the deeper mode is **less** repeatable (**72%** against **77%**) suggests more sampling or more retrieval steps, not a worse model.

**The cost ceiling constrains the choice.** At **$0.46** of revenue per consultation (section 26), inference must be a small fraction of that. That is a real constraint on how much computation any single answer can consume, and it is the kind of constraint that makes non-deterministic shortcuts attractive.

None of this is established. It is the hypothesis the published evidence supports, and it is testable by the company in an afternoon.

---

## 47. Scenario analysis

All three scenarios apply arithmetic to the company's stated claims. They are **author constructs**, not forecasts and not company guidance.

### 47.1 Scenario A — the daily-use claim is half what is stated

Suppose daily use is 20% of U.S. physicians rather than more than 40%.

| Measure | Value |
|---|---|
| Implied daily active physicians | **216,437** |
| As a share of registered | **28.48%** |
| Consultations per daily user per month | **83.16** |
| Consultations per daily user per day | **2.77** |

Here is the thing worth noticing: **halving the population claim makes the intensity claim harder, not easier.** The 18 million consultations have to come from somewhere. Fewer users means each one is doing more — 2.77 consultations every day, sustained.

```
scenA_intensity_rises_when_population_falls = True
```

The two claims constrain each other. You cannot discount one without inflating the other, which means the claim set as a whole is more internally disciplined than any single figure in it appears. That is a point in the company's favour and it emerged only from testing the claims against each other.

### 47.2 Scenario B — what the valuation implies about volume

At a $12.0B valuation and claimed revenue over $100M, the multiple is **120.00×**. Suppose the company needs to reach a 30× multiple to justify that valuation on conventional terms.

| Measure | Value |
|---|---|
| Revenue required | **$400.00M** |
| Gap from claimed revenue | **$300.00M** |
| Revenue multiple required | **4.00×** |
| At $0.46 per consultation, annual consultations required | **869.57M** |
| Monthly consultations required | **72.46M** |
| **Volume multiple required** | **4.03×** |

To grow into the valuation at current unit economics, OpenEvidence needs roughly **four times** its December 2025 consultation volume — from 18 million a month to over 72 million.

There are only two routes: more physicians, or more consultations per physician. The company already claims **70.23%** registration penetration of U.S. licensed physicians, so the first route is close to exhausted domestically. **That leaves intensity — or price.**

And intensity is the variable that section 21 identifies as clinically neutral: the business earns the same whether a consultation changed a decision or not.

### 47.3 Scenario C — closing the repeatability gap

| Measure | Value |
|---|---|
| Independent discordance estimate | **23.00%** |
| Proposed target | **10.00%** |
| Gap | **13.00pp** |
| **Required reduction** | **56.52%** |

Halving discordance and a bit more. For a determinism problem this is a tractable engineering target, not a research programme — which is what makes its absence from any public disclosure notable.

---

## 48. Sensitivity: how many ads fit in a consultation

The advertising model permits one more computation, and it is the most revealing in this document.

If each consultation carries exactly one ad impression, then claimed revenue over claimed volume implies:

| Measure | Value |
|---|---|
| Annual consultation run-rate | **216.00M** |
| **Implied CPM at one impression per consultation** | **$462.96** |

A $463 CPM would be extraordinarily high even for pharmaceutical HCP targeting, which is among the most expensive advertising in any market. Inverting the calculation is more informative:

| Assumed CPM | Ad units required per consultation |
|---|---|
| $500 | **0.93** |
| $250 | **1.85** |
| $100 | **4.63** |

| Measure | Value |
|---|---|
| Consultations per registered physician per year | **284.16** |
| Revenue per registered physician per year | **$131.58** |

### 48.1 What this tells a product manager

At a realistic pharmaceutical CPM of $100–250, **each clinical consultation must carry roughly two to five ad units.** That is a meaningful amount of commercial content inside a clinical answer surface.

This does not establish that OpenEvidence shows two to five ads per consultation. The revenue may be sold on other terms entirely — sponsorships, programme fees, data products — and the calculation collapses if so.

But it does establish the shape of the question. **If the revenue claim and the volume claim are both true, the ad load is either high or the pricing is exceptional.** Which of those is the case is exactly what section 28's R4 asks the company to disclose, and it is why advertiser separation is the highest-stakes undisclosed fact in this business rather than a governance footnote.

---

## 49. What would change my mind

Stated in advance, because an analysis that cannot be falsified is not an analysis.

**I would substantially revise the disclosure criticism if:** the company published a repeatability rate, or an independent peer-reviewed evaluation appeared. Either would move OpenEvidence above Doximity on the ladder in section 35, and neither is difficult.

**I would revise the adoption criticism if:** the company published registered, monthly-active and daily-active separately against a stated denominator, and the daily figure held up. The current criticism is about definitional drift, not about whether the product is widely used — the evidence that it is widely used is reasonably strong.

**I would revise the repeatability criticism if:** a larger, better-powered study found materially lower discordance. One pilot with n=100 is thin evidence and section 10.4 says so.

**I would revise the advertising-governance concern if:** the company disclosed structural separation with an external attestation. This is the one where a clean answer would be genuinely reassuring rather than merely compliant.

**Nothing would revise the structural finding.** Whatever the company chooses to publish, a private company has no obligation to publish anything, and voluntary disclosure can be withdrawn. That is a fact about the regime, not about OpenEvidence.

---

## 50. What OpenEvidence does better than Days 80–82

The criticism in this document is about evidence, not about the product, and the balance deserves stating.

**It solves a real problem at real scale.** Whatever discount is applied to the adoption claims, this product is used heavily by clinicians who are not paid to use it and can stop at any moment. Days 80 and 81 both described products purchased by an institution on the user's behalf. This one is chosen.

**It gave the product away.** Free access to verified physicians removed cost as a barrier to clinical reference, which is a defensible public-interest position as well as a growth strategy.

**Its citations make review possible.** Neither Hims & Hers nor Hinge Health offered the user any mechanism to check the AI's work. OpenEvidence does, in the product, by default. That is the strongest safety property in the four-day arc.

**Its cost and revenue curves align.** Section 19.1 — the advertising model scales revenue with usage, avoiding the structural trap that compressed Doximity's gross margin by **4.31pp** in a single quarter.

**Its consultation growth outran its user growth.** **+500.00%** against **+76.74%**. Existing users used it more. On the claimed figures that is genuine product-market fit, and it is the claim the company emphasises least.

The problem is not that the product is bad. **The problem is that nobody outside the company can tell.**

---

## 51. Counterfactual: suppose every claim is true

Worth running, because the case study should not depend on scepticism.

Assume daily use by more than 40% of U.S. physicians, 760,000 registered, 18 million monthly consultations, over $100M revenue, 100% on the USMLE. Assume the **56.96%** daily-to-registered ratio is exactly right.

**Most of this analysis survives unchanged.**

The metric definition still drifted between July 2025 and January 2026. The repeatability finding — **23.00%** discordance, worse in the premium mode — is independent of every company claim. NOHARM is still cited by both litigants for different conclusions and still disclaimed by one of them. **57.90%** of physicians in the free-choice arm still reached for no AI at all. There is still no institutional evaluation anywhere in the funnel, no disclosed advertiser separation, and no clinical outcome measure.

And the structural finding is *strengthened*: if the claims are all true, then a product used daily by 430,000 American physicians in live patient care has been subject to exactly one independent evaluation, by two academics and a high-school student with limited API access.

**The scale is the argument for scrutiny, not against it.**

---

## 52. Governance and concentration

| Dimension | Position |
|---|---|
| Ownership | Private; investors include Sequoia, GV, Kleiner Perkins, Coatue, Thrive, DST, Blackstone, Nvidia, Mayo Clinic |
| Board and control | Not disclosed |
| Revenue concentration | Not disclosed — unknown how many advertisers produce the claimed $100M |
| Supplier concentration | High — a small number of medical publishers and societies |
| Geographic concentration | United States |
| Customer type concentration | **Single** — pharmaceutical advertising |

The last row is the exposure. OpenEvidence has one revenue type, from one industry, in one country. Doximity at least splits revenue across Marketing, Hiring and Workflow Solutions plus a staffing line that grew **28.38%** in the quarter examined on Day 82.

A single-industry revenue base is fine while that industry's marketing budgets grow. Pharmaceutical promotional spending is discretionary, cyclical and politically exposed.

---

## 53. The expansion surface

Three directions are available, and each trades against something.

**International.** The content licences, the NPI verification mechanism and the advertising relationships are all United States constructs. Each would need rebuilding per market, and pharmaceutical advertising to physicians is regulated very differently outside the US. The domestic registration claim of **70.23%** means growth must eventually come from somewhere else, and this is the obvious somewhere — at the cost of rebuilding the moat in each market.

**Adjacent users.** Nurse practitioners, physician assistants, pharmacists and students expand the audience but dilute the "verified physician" premium that makes the inventory valuable to advertisers. Reach and price per impression move in opposite directions.

**Institutional.** Section 28's R6. The largest opportunity and the one that reintroduces the gatekeeper the company routed around.

Each path costs the thing that made the current position work. That is what a strong position looks like at the point where it stops compounding by itself.

---

## 54. Day 84 connection

Tomorrow is **Abridge** — ambient clinical documentation, the category Doximity entered with Scribe and a company whose entire product is the thing Day 82 said nobody measures: whether a generated clinical note is good enough to sign.

Abridge is also private, so Day 84 will face the same evidence problem this case study faced. The method established in section 2 carries forward: verify what can be verified, test claims against each other, name what cannot be checked, and never promote a claim to a fact.

The four-day arc has examined AI disclosure by companies that *sell* AI features. Day 84 examines a company whose product *is* the measurement problem.

---

## 55. A closing note on method

The most useful thing this case study did was run a search that returned six rows.

Six federal cases, 559 days, four as plaintiff. No modelling, no framework, no company cooperation — a public API, a company name, and a sort by filing date. It cost nothing and it produced the spine of the analysis: a company whose claims are checked nowhere else is checked, thoroughly and adversarially, in court.

That technique generalises to any private vendor. Before signing with one, search the federal dockets for its name. You will learn what it fights about, who it fights, how often, how much it is willing to spend on counsel, and — from the counterclaims — what its opponents say about its marketing. For a company that files nothing, **the docket is the closest thing to an annual report that exists.**

---

## 56. What four days established

| Day | Company | Status | The finding |
|---|---|---|---|
| 80 | Hims & Hers | Public | An AI narrative with no AI metric behind it |
| 81 | Hinge Health | Public | An AI metric that measures cost saved, not health gained |
| 82 | Doximity | Public | The AI cost is audited; the AI claims are quote-only |
| 83 | OpenEvidence | **Private** | No filing exists; claims are tested only when someone sues |

Four healthcare companies, four different AI positions, and **not one disclosed AI outcome metric between them.**

Across the four, the pattern is consistent enough to state as a finding: **companies disclose AI economics before AI efficacy, and they disclose either only to the extent they are compelled to.** Doximity published the most and is the most exposed, because a certified filing required it. OpenEvidence publishes what it likes, because nothing requires anything.

The practical instruction for a product manager evaluating any AI vendor is the same in all four cases. Ask where the claim is written down, and what happens to the person who signed it if it is wrong. If the answer is "a press release" and "nothing," the claim is marketing. If the answer is "a filing" and "liability," it is closer to evidence. And if there is no document at all, the only remaining test is whether anyone has ever had standing to challenge it.

---

## 57. Open questions for the category

Beyond this company, four questions the four-day arc raises and none of the four companies answers.

**Why does no clinical AI product publish a repeatability rate?** It is cheap, decisive and entirely within each company's control. The absence across four companies suggests a category norm rather than an oversight.

**Why is there no standard AI outcome metric in healthcare?** Every company measures something different, so nothing is comparable. Until a metric is standard, each company will report the dimension on which it wins — exactly what both parties did with NOHARM.

**Who evaluates AI tools that reach clinicians directly?** The free-to-physician model bypasses hospital procurement entirely, and no other body has stepped into that gap.

**What happens when the benchmark is the marketing?** NOHARM was cited by two competitors for opposite conclusions and disclaimed by one. If benchmarks are produced and promoted by the parties with the most at stake, they measure marketing capability as much as model capability.

---

## 58. A playbook: evaluating a private AI vendor

Generalised from this case study, for a product manager assessing a vendor that files nothing. Roughly two hours, no budget, no vendor cooperation.

**1. Search the federal dockets.** CourtListener's API is free and unauthenticated. Query the company name. Read the causes of action, count plaintiff versus defendant filings, note the law firms, and read any counterclaims — a counterclaim is the only place you will find an adversary's sworn characterisation of the vendor's marketing.

**2. Find an authoritative denominator.** Every adoption percentage has one hiding in it. For US physicians it is the FSMB census. Recompute the vendor's percentage yourself; a claim that checks out is a good sign, and one that does not is the beginning of a conversation.

**3. Write down what each metric means, every time you see it.** Then compare across releases. OpenEvidence's 40% meant registered in July and daily active in January; Doximity's prescribers and providers were different populations. **Definitional drift is the most common failure and it is invisible unless you keep a list.**

**4. Test the claims against each other.** Consultations divided by users. Revenue divided by volume. Implied CPM. Claims that cannot be checked externally can be checked internally, and the arithmetic sometimes shows they constrain each other in ways that are reassuring (section 47.1) as well as ways that are not.

**5. Search for independent evaluation.** medRxiv, arXiv, PubMed, and the venue for the relevant specialty. Ask who funded it. If the only evidence is vendor-produced, say so in your evaluation in those words.

**6. Check who else cites the vendor's benchmark.** If a competitor cites the same study for a contradictory conclusion, the benchmark is not settling anything.

**7. Ask the repeatability question.** Send the same query twice, a few minutes apart, twenty times. You can do this in an afternoon from a trial account, and no vendor in this four-day arc publishes the answer.

**8. Write down what you could not verify.** Then treat that list as the actual risk register. In this case study it ran to fourteen categories, and it was more informative than anything the vendor published.

---

## 59. Methodology

**Source acquisition.** Federal docket metadata from the CourtListener REST search API (public, unauthenticated), queried 21 September 2026. Company claims from BusinessWire and PR Newswire releases. Physician census from the Federation of State Medical Boards. Independent evaluation from medRxiv. Doximity's account of the litigation from its Form 10-Q, verified on Day 82.

**Gate-first discipline.** `verify.py` was written and passing before any prose existed. Every derived figure here is produced by the gate.

**The claim/fact boundary.** The gate asserts `company_claims_independently_confirmed = False` and enumerates fourteen unverifiable categories, so that no sentence can promote a claim to a fact without the gate contradicting it. Where this document says "claims," a company said it and nobody checked.

**Rounding.** Percentages to two decimals, tolerance 0.005 absolute unless stated. Derived figures computed from unrounded inputs — the rounded-intermediate error class found earlier in this series is guarded against explicitly.

**Cross-checking.** `crosscheck.py` extracts every two-decimal figure in this README and in ASSUMPTIONS.md and confirms each traces to a gate value. A figure in the prose the gate does not produce is a build failure.

**Author constructs.** RICE inputs, stress factors, personas, the North Star proposal, guardrail thresholds, the eval plan and the failure-mode ranking are the author's and are labelled as such.

**Fabrication policy.** No figure, quote, date or case number is invented. Where information is unavailable, this document says so.

---

## 60. Reproducing this analysis

```bash
# 1. Federal dockets (public, no key required)
curl -A "<your contact>" \
  "https://www.courtlistener.com/api/rest/v4/search/?q=OpenEvidence&type=r&order_by=dateFiled%20desc"

# 2. Run the gate. 164 checks. Non-zero exit on any failure.
python3 verify.py

# 3. Cross-check the prose against the gate.
python3 crosscheck.py
```

`verify.py` is self-contained and declares every input as a named constant with its source.

---

## 61. Limitations

Covers one private company using six docket records, four company press releases, one government census and one preprint. No audited financials exist and none are used.

No clinical assessment of OpenEvidence is made or implied. This document does not evaluate whether the product is medically safe; it evaluates what evidence exists about that question, and finds almost none.

Nothing here asserts that any OpenEvidence claim is false, or that any party to any litigation did anything wrong.

The **23.00%** discordance and **31.00%** accuracy figures come from a single unreviewed pilot study and carry its limitations.

---

## 62. References

**Federal dockets** — CourtListener public search API, queried 2026-09-21:
*OpenEvidence Inc. v. Pathway Medical, Inc.*, No. 1:25-cv-10471 (D. Mass.);
*OpenEvidence Inc. v. Doximity, Inc.*, No. 1:25-cv-11802 (D. Mass.);
*OpenEvidence Inc. v. Veracity-Health, Inc.*, No. 3:25-cv-05376 (N.D. Cal.);
*OpenEvidence, Inc. v. Doximity, Inc.*, No. 4:25-mc-80387 (N.D. Cal.);
*Longley v. OpenEvidence Inc.*, No. 1:26-cv-13165 (D. Mass.);
*Eaton v. OpenEvidence, Inc.*, No. 5:26-cv-00651 (E.D.N.C.).

**Company statements.** OpenEvidence press release via BusinessWire, 21 January 2026, "OpenEvidence Raises $250 Million to Build Medical Superintelligence for Doctors." OpenEvidence press release via PR Newswire, 20 July 2026, "Physicians Choose OpenEvidence Over Every Other AI Chatbot Combined in Independent Stanford-Harvard Study of Clinical AI." OpenEvidence company website.

**Government source.** Federation of State Medical Boards, "FSMB Physician Census Identifies 1,082,187 Licensed Physicians in U.S.," published 15 August 2025 (2024 census).

**Independent evaluation.** "The accuracy and repeatability of OpenEvidence on complex medical subspecialty scenarios: a pilot study," preprint, medRxiv, posted 4 December 2025. Not peer reviewed.

**Cross-series primary source.** Doximity, Inc. Form 10-Q, accession 0001516513-26-000040, Note 12 — Commitments and Contingencies. Verified on Day 82.

**Series cross-references.** Day 80, 81 and 82 comparator figures are recomputed inside this case study's own `verify.py` and are not carried across as prose assertions.

---

## 63. Document control

| Field | Value |
|---|---|
| Case study | Day 83 of 90 |
| Subject | OpenEvidence, Inc. (private) |
| Method | **Docket record + internal consistency + independent evidence** — see section 2 |
| Primary sources | 6 federal dockets, 2 company releases, 1 government census, 1 preprint, 1 SEC filing |
| Verification checks | **164**, all passing |
| Unverifiable categories asserted | **14** |
| Headline claims with independent confirmation | **0 of 5** |
| Diagrams | Markdown tables and ASCII only |
| Fabricated figures | **0** |

---

## 64. Series index

| Day | Company | Central finding |
|---|---|---|
| 80 | Hims & Hers | AI narrative with zero disclosed AI metrics |
| 81 | Hinge Health | Discloses an AI cost metric, not a clinical one |
| 82 | Doximity | AI cost is audited; every AI claim is quote-only |
| **83** | **OpenEvidence** | **No filing exists; the only adversarial test is litigation** |
| 84 | Abridge | *(forthcoming)* |

---

## 65. Standing questions for OpenEvidence

Five questions this analysis cannot answer, ordered by how much they would change the assessment.

1. **Can advertiser relationships influence answer content or ordering, and who inside the company can change that?** The highest-stakes undisclosed fact about the product.
2. **What is the answer-discordance rate?** The company can measure it today. An independent pilot puts it near **23.00%**.
3. **Does a citation always support the claim it is attached to?** Citations are the trust mechanism; nobody has audited them.
4. **What does "more than 40% of physicians use it daily" mean, precisely, and against what denominator?** The same figure meant registration six months earlier.
5. **What did the 100% USMLE evaluation consist of?** No protocol, date, version or scoring method is public.

---

*Day 83 of 90. Built from primary sources. 164 programmatic checks. Zero fabricated figures. Zero verified company claims — which is the finding.*
