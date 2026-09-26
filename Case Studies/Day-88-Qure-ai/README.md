# Day 88 — Qure.ai: The Company With No Investors and All the Numbers

**A Product Management case study on device regulation, independent evidence, and what a single performance figure conceals.**

*Part of a 90-day series of evidence-based product case studies. Day 88 of 90.*

---

## 1. At a Glance

| | |
|---|---|
| **Legal entity** | QURE.AI TECHNOLOGIES PRIVATE LIMITED |
| **Registered office** | Mumbai, India |
| **LEI** | 3358009NQ689LYF5LO48 (status: ISSUED) |
| **CIN** | U74999MH2016PTC283891 |
| **Incorporated** | 2016 |
| **Ownership** | Private — no securities filing obligation of any kind |
| **FDA 510(k) clearances** | **9**, spanning 2020-06-17 to 2026-01-16 |
| **Clearances reporting diagnostic accuracy** | **5 of 9 (55.56%)** |
| **Summaries containing an internal numeric contradiction** | **4 of 9 (44.44%)** |
| **Tuberculosis clearances** | **0** — despite being the most-studied indication |
| **TB literature that is independent of the vendor** | **13 of 17 — 76.47%** |
| **Verification** | `verify.py` — **344 programmatic checks, all passing** |

---

## 2. Why This Company, Today

Day 87 examined Tempus AI, a Nasdaq-listed company with the maximum securities-disclosure burden available: audited financials, certified officers, ten SEC comment letters, sixty-six staff comments, and a merger registration statement that forced fifteen years of internal forecasts into public view.

And after all of that, the number of published performance metrics for its clinical algorithms was **zero**.

Day 87 closed by naming the inverse test:

> Tempus is a company with maximal *disclosure* obligation and minimal *performance* obligation. A regulated medical-imaging device company is the opposite: it can keep its financials private while being compelled, by device regulators rather than securities regulators, to publish sensitivity and specificity. If Day 87 showed that securities disclosure compels process, Day 88 asks whether **device regulation compels results**.

Qure.ai is that company. It is private, Indian, and has never filed a financial statement any member of the public can read. It has also cleared **nine** devices through the US FDA's 510(k) pathway, and the summaries of those clearances are public documents containing sensitivities, specificities, areas under the curve, confidence intervals, subgroup breakdowns, and the counts behind them.

**The answer to the inverse test is yes.** A company with no investors to answer to has published far more about how well its algorithms work than a company with every investor to answer to.

And then there are three complications, and they are the reason this case study runs to 65 sections.

---

## 3. How to Read This Case Study

The spine is a comparison that should not work out the way it does. A private company beats a public one on evidence disclosure, decisively, and the mechanism is not virtue — it is that a different regulator asked a different question.

Three reading paths:

- **If you want the structural finding**: §20 through §30.
- **If you want the errors nobody caught**: §31 through §36.
- **If you want the thing that actually matters to a buyer**: §37 through §44.

Every figure carrying two or three decimal places in this document is produced by `verify.py`. Nothing here is estimated or inferred unless the sentence containing it says so.

---

## 4. Evidence Standard

Unchanged from Day 1, tightened across 87 prior case studies:

1. **No fabrication.** No metric, date, or relationship appears unless it is in a cited primary source.
2. **Facts and inferences are separated at the sentence level.**
3. **Arithmetic is executed, not asserted.** Every derived figure is computed in `verify.py` from unrounded inputs and asserted against an expected value before any prose exists.
4. **Absences are findings.** What a source does not say is recorded as a fact about the source.
5. **The gate precedes the prose.**

Rule 5 earned its place again today. Two hand-stated expectations failed on the gate's first run, both of them the rounded-intermediate trap, and §63 records them.

---

## 5. Source Inventory

All sources retrieved 2026-09-26.

**FDA 510(k) summaries** — `accessdata.fda.gov/cdrh_docs/`

| Ref | K-number | Device | Decision | Product code |
|---|---|---|---|---|
| **[F1]** | K200921 | qER | 2020-06-17 | QAS |
| **[F2]** | K211222 | qER-Quant | 2021-07-30 | QIH |
| **[F3]** | K212690 | qXR-BT | 2021-12-21 | QIH |
| **[F4]** | K230899 | qXR-PTX-PE | 2023-08-22 | QFM |
| **[F5]** | K231149 | qXR-CTR | 2023-09-22 | QIH |
| **[F6]** | K231805 | qXR-LN | 2023-12-22 | MYN |
| **[F7]** | K240740 | qCT LN Quant | 2024-08-16 | QIH |
| **[F8]** | K251610 | qER-CTA (v1.0) | 2025-09-08 | QAS |
| **[F9]** | K251934 | qXR-Detect | 2026-01-16 | MYN |

**Registry and database**

| Ref | Source |
|---|---|
| **[FDB]** | openFDA `device/510k` API, `applicant:"qure.ai"` |
| **[G]** | GLEIF LEI record 3358009NQ689LYF5LO48 |

**Peer-reviewed literature** — via PubMed. Per PubMed's attribution requirement, all literature in this case study is identified according to PubMed with DOIs given.

| Ref | Study | PMID | DOI |
|---|---|---|---|
| **[P1]** | Qin ZZ et al., *Lancet Digital Health* 2021 — five AI algorithms, Bangladesh | 34446265 | [10.1016/S2589-7500(21)00116-3](https://doi.org/10.1016/S2589-7500(21)00116-3) |
| **[P2]** | *Scientific Reports* 2021 — independent evaluation of 12 AI solutions | 34903808 | [10.1038/s41598-021-03265-0](https://doi.org/10.1038/s41598-021-03265-0) |
| **[P3]** | *Lancet Digital Health* 2024 — 12 CAD products, South Africa prevalence survey | 39033067 | [10.1016/S2589-7500(24)00118-3](https://doi.org/10.1016/S2589-7500(24)00118-3) |
| **[P4]** | *International Journal of Medical Informatics* 2023 — rapid review and meta-analysis | 37549498 | [10.1016/j.ijmedinf.2023.105159](https://doi.org/10.1016/j.ijmedinf.2023.105159) |
| **[P5]** | *PLOS Global Public Health* 2024 — Lima, Peru, inpatient triage and screening | 38324610 | [10.1371/journal.pgph.0002031](https://doi.org/10.1371/journal.pgph.0002031) |

No company press release, investor deck, website claim, or news article is used anywhere in this document.

---

## 6. Evidence Tiers

Day 87 tiered by *what compelled the statement*. Day 88 keeps that axis, because it turns out to be the only one that explains the data.

| Tier | Description | What it means | Sources |
|---|---|---|---|
| **T1 — Regulator-reviewed** | Performance data submitted to and accepted by FDA in a cleared 510(k) | A regulator read it and cleared the device | [F1]–[F9] |
| **T2 — Independent peer-reviewed** | Evaluation by researchers with no vendor author | Someone with no stake measured it | [P1]–[P5] |
| **T3 — Vendor peer-reviewed** | Published study with a vendor author | Peer review, but not independence | 4 of 17 TB papers |
| **T4 — Statutory registry** | Facts a company must file to exist | Compelled, but says nothing about the product | [G] |
| **T5 — Company statement** | Anything the company chose to say | Liability only | *not used* |

T5 is empty in this case study by design. That is the constraint, and §63 says what it cost.

The finding that runs through §20 to §44 is that T1 and T2 answer **different questions**, that neither alone is sufficient, and that **the company supplied neither**.

---

## 7. Company Overview

Qure.ai Technologies Private Limited builds deep-learning software that reads medical images — chest X-rays, head CT, chest CT, and CT angiography — and returns findings to clinicians through PACS integration.

The product families, as named in the FDA record:

- **qXR** — chest X-ray. Breathing-tube position, cardiothoracic ratio, pneumothorax and pleural effusion triage, lung nodule detection, and multi-category chest ROI detection.
- **qER** — head CT. Intracranial haemorrhage triage, brain structure quantification, and large vessel occlusion on CT angiography.
- **qCT** — chest CT. Lung nodule quantification.

Outside the FDA record, and extensively documented in the peer-reviewed literature, there is a fourth: **qXR for tuberculosis**, which is the product the world has actually studied, and which appears in none of the nine clearances. §27 is about that.

---

## 8. Statutory Registration

Day 85 established that GLEIF is a free route into Indian corporate registry data when the MCA portal is not directly reachable. The same method applies here.

From [G], the LEI record resolves to **QURE.AI TECHNOLOGIES PRIVATE LIMITED**, Mumbai, LEI status **ISSUED**, with a Corporate Identity Number of:

```
U 74999 MH 2016 PTC 283891
│ │     │  │    │   │
│ │     │  │    │   └── registration number
│ │     │  │    └────── company class: Private Limited
│ │     │  └─────────── year of incorporation: 2016
│ │     └────────────── state: Maharashtra
│ └──────────────────── NIC activity code: 74999
└────────────────────── listing status: U = Unlisted
```

**The NIC code is the finding.** 74999 is "Other professional, scientific and technical activities **n.e.c.**" — not elsewhere classified. It is the residual bucket.

Day 85's subject, Eka Care, is registered as **U74999KA2020PTC141864**. Different state, incorporated **4** years later, entirely different product — and the **same** NIC code.

Two of India's most significant health-AI companies, four years apart, in different states, both land in the register's "everything else" category. India's statutory company classification has no code for medical AI, so the register cannot tell you how many such companies exist. It is an absence with a consequence: you cannot count an industry that the classification system does not name.

---

## 9. What 510(k) Clearance Actually Is

This section exists because the single most common error in reading this evidence is to treat clearance as approval.

A 510(k) is a **premarket notification**. The manufacturer asserts that its device is *substantially equivalent* to a legally marketed predicate device. FDA reviews that assertion. All nine Qure.ai clearances are **Traditional** 510(k)s; none is a PMA, and none is a De Novo.

What this means in practice:

- Clearance says the device is **as safe and effective as a predicate**, not that it produces clinical benefit.
- The comparison anchor is another product, which may itself have been cleared against an earlier product.
- The performance data submitted is **whatever supports the equivalence claim** — not a fixed, standardised battery.

`verify.py` records `510k_is_an_approval` and `510k_proves_clinical_benefit` as **False**, both asserted programmatically, so that nothing downstream in this document can quietly imply otherwise.

Day 87's negative control was "the SEC did not verify." Day 88's is **"FDA cleared, it did not certify."** Both are the same lesson wearing different clothes.

---

## 10. The Clearance Record

Nine clearances over **2,039 days** — **5.58 years** — a mean rate of **1.61** per year.

| # | K-number | Device | Decision | Code | Reports accuracy? |
|---|---|---|---|---|:---:|
| 1 | K200921 | qER | 2020-06-17 | QAS | **Yes** |
| 2 | K211222 | qER-Quant | 2021-07-30 | QIH | No |
| 3 | K212690 | qXR-BT | 2021-12-21 | QIH | No |
| 4 | K230899 | qXR-PTX-PE | 2023-08-22 | QFM | **Yes** |
| 5 | K231149 | qXR-CTR | 2023-09-22 | QIH | No |
| 6 | K231805 | qXR-LN | 2023-12-22 | MYN | **Yes** |
| 7 | K240740 | qCT LN Quant | 2024-08-16 | QIH | No |
| 8 | K251610 | qER-CTA (v1.0) | 2025-09-08 | QAS | **Yes** |
| 9 | K251934 | qXR-Detect | 2026-01-16 | MYN | **Yes** |

The cadence is uneven. The shortest gap between clearances is **31 days** (K230899 to K231149, August to September 2023); the longest is **609 days** (K212690 to K230899). The mean gap is **254.88** days. **Three** clearances landed in calendar 2023 alone.

Four distinct product codes appear: **QIH** (4), **MYN** (2), **QAS** (2), **QFM** (1).

---

## 11. Business Model

This section is short because the honest answer is short, and the shortness is itself a finding.

| Element | What can be established |
|---|---|
| Revenue | **Not disclosed** — no filing obligation |
| Pricing | **Not disclosed** |
| Customers | Named only where a published study discloses a site |
| Funding | **Not disclosed** in any source used here |
| Headcount | **Not disclosed** |
| Deployment scale | **Not disclosed** in the regulatory record |

A private Indian company files its statutory accounts with the Registrar of Companies, but those are not freely retrievable through the routes used in this series, and nothing in the FDA or literature record substitutes for them.

So: everything about **how well the product works** is public, and everything about **how well the company is doing** is not.

Day 87 was the exact inverse. Tempus published $1,271.789M of audited FY2025 revenue and not one algorithm accuracy metric. Qure.ai publishes five clearances' worth of accuracy metrics and no revenue at all.

**Neither company chose either outcome. In both cases a regulator decided which half of the picture the public would get.**

---

## 12. Problem Statement

Stated from the evidence:

> Radiology demand exceeds radiologist supply, and the gap is worst where disease burden is highest. A chest X-ray is cheap, portable, and fast; interpreting one reliably is not. In tuberculosis screening the constraint is sharper still — confirmatory molecular testing is expensive, so the practical question is not "does this patient have TB" but "which patients justify the cost of finding out."

That framing matters for everything that follows. A triage algorithm's job is to **decide who gets tested**, which means its specificity is a budget line, not a statistic. §40 is where that becomes concrete.

---

## 13. Jobs to Be Done

| Job | Who hires it | Alternative | "Done well" looks like |
|---|---|---|---|
| "Tell me which scans to read first" | Emergency radiologist | Chronological worklist | Critical findings surface within minutes |
| "Tell me if this tube is in the right place" | ICU clinician | Manual check | Position confirmed at the bedside |
| "Tell me who to send for a confirmatory TB test" | Screening programme | Symptom screen, or test everyone | Fewer tests, same cases found |
| "Measure this for me, consistently" | Radiologist | Manual calipers | Reproducible measurement |
| "Tell me how well this works **in my population**" | Procurement | Vendor's claim | Evidence from a comparable setting |

The last row is the one this case study can evaluate most completely, and it is the one the regulatory record answers **least** well. §37 onward.

---

## 14. User Personas

Three personas, each constructed from what the sources actually establish about who uses or buys these products. No invented quotes, no synthetic biographies.

---

## 15. Persona 1: The Emergency Radiologist

**Basis:** [F1], [F8] — the two QAS triage-and-notification clearances.

**Context.** Works a worklist that arrives in the order scans are acquired, not in the order of clinical urgency. A subarachnoid haemorrhage and a routine follow-up look identical until opened.

**What they need.** Re-ordering, not diagnosis. The qER and qER-CTA clearances are explicit that output is for triage and prioritisation, is non-diagnostic, and that notified clinicians remain responsible for viewing the full images per the standard of care.

**What the record gives them.** For qER-CTA: AUC **0.959**, sensitivity **91.35%**, specificity **91.86%**, on **584** CT angiography scans (**289** with large vessel occlusion, **295** without), ground-truthed by three US board-certified neuroradiologists with at least ten years of experience each.

That is a real, usable number. It is also one number, from one dataset. §37.

---

## 16. Persona 2: The TB Screening Programme Manager

**Basis:** [P1], [P3], [P4], [P5].

**Context.** Runs a screening programme in a high-burden setting with a fixed budget for confirmatory molecular testing. Every false positive consumes a test that a true positive could have used.

**What they need.** Sensitivity high enough not to miss cases, and specificity high enough that the confirmatory testing budget survives contact with the population.

**What the record gives them.** More independent evidence than almost any product in this 90-day series has produced — [P1] alone evaluated five commercial algorithms on **23,954** chest X-rays from a dataset that had not previously been used to train any of them.

**What the record does not give them.** A number that transfers. §40.

---

## 17. Persona 3: The Procurement Officer

**Basis:** the whole document.

**Context.** Must justify a purchase to a finance committee. Has the FDA clearance summaries, the peer-reviewed literature, and nothing from the company that counts as evidence.

**What they can establish.** How well five of the nine devices performed on their respective clearance datasets; how qXR compares against eleven competitor products on TB in two independent head-to-heads; and that performance degrades in older patients, in people with prior TB, and in people with HIV.

**What they cannot establish.** The vendor's financial viability, its pricing, or how the device will perform in *their* population — which is the only question the committee will ask.

---

## 18. User Journey: A Scan Through qXR-PTX-PE

```
  Acquisition            Device                       Worklist
      |                     |                             |
  [1] | chest X-ray ------> |                             |
      |                     | [2] AI analysis             |
      |                     |     (trained on data that is
      |                     |      74% India, 3.9% US)
      |                     |                             |
      |                     | [3] case-level output       |
      |                     |     PTX and/or PE suspected |
      |                     |             |               |
      |                     |             v               |
  [4] |                     | notification -------------> | priority flag
      |                     |   mean 10 seconds           |
      |                     |                             |
      |                     |                        [5]  | radiologist
      |                     |                             | opens scan
      |                     |                             |
      |   Cleared operating point, US test set:           |
      |     Pneumothorax  sens 94.53%  spec 96.36%        |
      |     Pleural eff.  sens 96.22%  spec 94.90%        |
      |                                                   |
      |   Not established anywhere in the clearance:      |
      |     performance in any other population           |
```

Step 2 and the box at the bottom are the whole case study. The model learned mostly from Indian data; it was tested only on US data; and the number that emerges is reported as though it were a property of the device.

---

## 19. User Journey: A Procurement Officer Reading the Evidence

```
  Reader                  Source                     What they learn
    |                        |                             |
[1] | opens FDA summary ---> |                             |
    |                        | sens/spec, one US dataset   |
    |                        | ONE number per device       |
    |                        |                             |
[2] | "will it work here?" ->| ......... not answered      |
    |                        |                             |
[3] | opens the literature ->|                             |
    |                        | Bangladesh  spec 74.30%     |
    |                        | pooled meta spec 69.20%     |
    |                        | Lima triage spec 32.00%     |
    |                        |                             |
[4] | learns the real answer: performance is a property of |
    |   the device AND the population, and the regulator   |
    |   only ever asked about one population.              |
```

The journey succeeds — but only because researchers with no commercial stake did work that nobody required them to do.

---

## 20. The Central Question

> **Does device regulation compel results, where securities disclosure compelled only process?**

Day 87 established the baseline. Tempus AI, listed, audited, comment-lettered, published:

- **0** performance metrics for any clinical algorithm.
- An exemplary description of *how* it developed and validated its tumour-origin model, containing no result.
- **7** accuracy metrics for its assays, because CLIA requires analytical validation of laboratory-developed tests and nothing requires it of an algorithm.

Day 87's own conclusion was that "numbers appear exactly where a rule requires them." Day 88 tests that by finding a company where a rule *does* require them.

**The answer is yes, emphatically — with three qualifications that occupy the rest of this document:**

1. **Device regulation compels results, but only for the indications it covers** (§27).
2. **It compels one result, from one population** (§37–§40).
3. **It does not verify the document it compels** (§31–§36).

---

## 21. The Partition

Here is the structural finding, and it is exact.

Of nine clearances, **5 (55.56%)** report sensitivity, specificity, or AUC. **4 (44.44%)** report none.

Every clearance that reports no diagnostic accuracy metric carries product code **QIH**. Every QIH clearance lacks them. No non-QIH clearance lacks them.

| Product code | Count | What the device does | What it reports |
|---|---:|---|---|
| **QIH** | 4 | Measures a structure | Absolute error, RMSE, Dice, normalized error |
| **MYN** | 2 | Detects a finding | Sensitivity, specificity, AUC |
| **QAS** | 2 | Triages and notifies | Sensitivity, specificity, AUC |
| **QFM** | 1 | Triages a specific finding | Sensitivity, specificity, AUC |

**The product code predicts the metric type with perfect accuracy across all nine clearances.** `verify.py` asserts this three ways — that every non-accuracy clearance is QIH, that every QIH clearance lacks accuracy metrics, and that every non-QIH clearance has them.

This is not evasion and should not be read as one. A device that measures the cardiothoracic ratio does not make a diagnostic call, so sensitivity is not defined for it. RMSE is the correct metric. `verify.py` records `absence_is_appropriate_not_evasive` as **True**.

But the *mechanism* is exactly the one Day 87 identified. The metric that appears is the metric the device classification requires. Nobody chose to report AUC for qXR-Detect out of transparency; a detection device must characterise detection. Nobody withheld AUC for qXR-CTR; a measurement device has nothing to characterise that way.

**Classification is destiny.** What a regulator calls your product determines what the public gets to know about it.

---

## 22. K230899: The Fullest Disclosure

The pneumothorax and pleural effusion triage clearance is the most complete performance document Qure.ai has in the public record, and it is worth reading closely because it shows both how good this pathway can be and where it stops.

**Pneumothorax study — 613 chest X-rays**

| | |
|---|---:|
| With pneumothorax | 201 |
| Without | 412 |
| **Total** | **613** ✓ |
| Male / Female / Sex unknown | 289 / 287 / 37 ✓ |
| Midwest / West / Northeast / South / unknown | 179 / 152 / 125 / 12 / 145 ✓ |
| **AUC** | **98.94** |
| **Sensitivity** | **94.53%** (190/201) |
| **Specificity** | **96.36%** (397/412) |
| False negatives | **11** |
| False positives | **15** |

**Pleural effusion study — 1,070 chest X-rays**

| | |
|---|---:|
| With pleural effusion / without | 344 / 726 ✓ |
| Female / Male / Sex unknown | 498 / 551 / 21 ✓ |
| Midwest / Northeast / South / West / unknown | 278 / 213 / 6 / 308 / 265 ✓ |
| **AUC** | **98.90** |
| **Sensitivity** | **96.22%** |
| **Specificity** | **94.90%** |

Across both indications, **1,683** scans, ground truth by **3** American Board of Radiology thoracic radiologists with a minimum of **10** years' experience each.

**Every subgroup count reconciles.** The sex breakdown sums to the total for both indications. The regional breakdown sums to the total for both indications. The reported sensitivity of 94.53% is exactly 190/201, and the reported specificity of 96.36% is exactly 397/412, recomputed from the published counts.

That is a genuinely well-constructed disclosure, and it deserves to be said plainly before §31 says the rest.

---

## 23. The Geography Inversion

Inside the same document:

> "The algorithm was trained on training data from across the world. The training dataset consisted of **74%** of the data from India, **20.04%** from the EU, **3.9%** from the US, **1.4%** from Brazil and **0.63%** from Vietnam."

Two things follow.

**First, the percentages sum to 99.97%, not 100%.** A shortfall of **0.03 percentage points**. This is almost certainly the 74% figure being reported without decimals while the others carry two. It is a trivial defect. It is also the kind of defect that exists only in documents nobody recomputes — and it is the first of five arithmetic observations in this case study that a reader can only make by doing the addition.

**Second, and not trivial at all: the training and test geographies are inverted.**

| | Training | Test |
|---|---:|---|
| India | **74.00%** | — |
| EU | 20.04% | — |
| **US** | **3.90%** | **100%** |
| Brazil | 1.40% | — |
| Vietnam | 0.63% | — |

The model learned from **18.97 times** more Indian data than US data, and was evaluated exclusively on US data.

This is not a criticism of the submission. FDA requires evidence relevant to the US population, and testing on US data is exactly right for a US clearance. The summary states the training composition openly, which many would not.

But it produces a specific and under-appreciated consequence: **the cleared performance figure describes how a mostly-India-trained model performs on American patients.** It is silent on how it performs on the population it mostly learned from — which is, by scan volume, where most of the world's chest X-rays are taken.

---

## 24. The Subgroups

K230899 reports pneumothorax AUC across **7** subgroups. Every one of them:

| Subgroup | AUC | 95% CI | CI width |
|---|---:|---|---:|
| Male | 98.67 | 97.63 – 100 | 2.37 |
| Female | 99.30 | 98.64 – 100 | **1.36** |
| **Sex unknown** | **92.47** | **84.95 – 100** | **15.05** |
| Age 22–44 | 99.12 | 98.34 – 100 | 1.66 |
| Age 45–64 | 99.17 | 98.37 – 100 | 1.63 |
| Age 65–84 | 98.69 | 97.61 – 100 | 2.39 |
| Age 85+ | 98.62 | 97.25 – 100 | 2.75 |

**Every single upper bound is exactly 100.** That is the confidence interval being clipped at the boundary of the metric, which is an expected artefact when an estimate sits close to 1.0 — but seven identical upper bounds also mean the intervals are doing very little work on the upside.

The informative column is the width. The **sex unknown** subgroup has a CI **11.07 times** wider than the female subgroup, and an AUC **6.83 percentage points** below it — **6.20** points below the male subgroup.

The summary's own characterisation is that results "were consistent in both genders." That statement is true. It is also true that the third group, the one with neither gender recorded, performs materially worse on a much thinner evidence base, and the summary does not flag it as a limitation.

Whether the 37 unknown-sex scans differ clinically or merely statistically cannot be determined from the document. What can be determined is that a reader who stops at the sentence will not know the question exists.

---

## 25. K251934: The Newest Clearance, And The Most Honest Number

qXR-Detect, cleared **2026-01-16**, is a multi-reader multi-case study: radiologists read scans unaided, then aided by the device, with a **28-day** washout between sessions, across **6** categories of suspicious chest region-of-interest, ground-truthed by **3** truthers.

| | Unaided | Aided | Gain |
|---|---:|---:|---:|
| AUROC | 0.8466 | 0.8720 | **+2.54 pp** |
| Sensitivity | 0.8896 | 0.9338 | **+4.42 pp** |
| **Specificity** | **0.5556** | **0.6219** | **+6.63 pp** |

Standalone AUC by category:

| Category | AUC |
|---|---:|
| Hardware | **0.958** |
| Pleura | 0.95 |
| Lung | 0.893 |
| Mediastinum / Hila | 0.891 |
| Bone | **0.879** |

Three observations.

**The device helps.** Every metric improves, and the largest gain is in specificity, which is the metric that costs money.

**The baseline is startling.** Radiologists reading unaided achieved **55.56%** specificity. Aided, they reached **62.19%** — which still means a false-positive rate of **37.81%**. `verify.py` asserts `k251934_specificity_below_two_thirds_even_when_aided` as **True**. This is a hard task, and the summary reports it without softening.

**The best-performing category is not a pathology.** The highest standalone AUC, **0.958**, is for **Hardware** — pacemakers, lines, surgical clips. The lowest, **0.879**, is Bone. The spread is **0.079**. That objects placed in the body by humans are easier to detect than disease processes is entirely expected, and it is a useful corrective to reading a headline AUC as a statement about diagnostic skill.

---

## 26. qXR-LN: Where The Numbers Stop Agreeing With Each Other

The lung nodule detection clearance [F6] reports two sensitivities:

- **Scan-level sensitivity: 93.83%** (AUC 94.51, specificity 81.09%)
- **Nodule-level sensitivity: 84.1%**

A **9.73 percentage point** gap between them, in the same device, on the same study.

Both are correct and they measure different things. Scan-level asks "did the device flag this scan as containing a nodule." Nodule-level asks "did it find every nodule on the scan." A device can flag the right scans while missing the second and third nodule on each one.

The device performs better on the question that is easier to get right. That is not a flaw; it is a reason to read which question a number answers before quoting it.

Note also that at **81.09%**, qXR-LN has the lowest specificity of the four detection devices with US clearance datasets — meaningfully below qXR-PTX-PE's 96.36% and 94.90%, and below qER-CTA's 91.86%.

Across the five clearances that report specificity, the values span **62.19%** to **96.36%** — a **34.17 percentage point** spread, mean **85.28%**. And the **lowest is the newest**. Clearance recency is not a proxy for performance.

---

## 27. The Indication That Is Not Cleared

Nine clearances cover nine distinct indications: intracranial haemorrhage triage, brain structure quantification, breathing-tube position, pneumothorax and pleural effusion triage, cardiothoracic ratio, lung nodule detection, lung nodule quantification, large vessel occlusion, and chest ROI detection.

**Tuberculosis is not among them. Qure.ai has zero FDA clearances for TB.**

And tuberculosis is, by a wide margin, the Qure.ai indication the world has actually studied. It has been evaluated in a *Lancet Digital Health* head-to-head against four competitors on 23,954 X-rays [P1]; in a *Scientific Reports* independent evaluation of twelve CAD solutions [P2]; in a second *Lancet Digital Health* study against eleven competitors on a South African prevalence survey [P3]; in a formal meta-analysis [P4]; and in a prospective Peruvian hospital cohort [P5].

**The regulatory record and the research record barely overlap.** FDA cleared what the US market needs. The literature studied what the disease burden demands. Neither is wrong, and a reader who consults only one of them will conclude something false about the product.

This is the sharpest limit on §20's answer. Device regulation compels results — **for the indications it covers.** For the indication that matters most in the settings where this company's technology is most deployed, the compelled record is empty, and everything known comes from researchers who volunteered.

---

## 28. The Independent Literature

A PubMed search on 2026-09-26 for qXR and Qure.ai in the tuberculosis chest-radiograph literature returns **17** papers. Of those, **4** have a Qure.ai-affiliated author and **13** do not.

**Vendor-authored share: 23.53%. Independent share: 76.47%.**

Set that against Day 87. Tempus AI's last disclosed self-authorship figure, in its 2024 IPO prospectus, was 93 of 126 articles — **73.81%** self-authored.

| | Vendor-authored share |
|---|---:|
| Tempus AI, at last disclosure (2024) [Day 87] | **73.81%** |
| Qure.ai, TB literature (2026) | **23.53%** |
| **Difference** | **50.28 pp** |

Tempus's self-authorship share is **3.14 times** Qure.ai's.

The public company's evidence base was three-quarters its own writing. The private company's is three-quarters other people's.

Two honest caveats. The comparison is across different literatures — Tempus's figure covers all product mentions, Qure.ai's covers one indication. And Qure.ai benefits from a structural accident: tuberculosis attracts independent academic and global-health funding that precision oncology does not, so researchers had their own reasons to evaluate it.

But that accident is the point. **Independent evidence appeared because independent people had a reason to look, not because a company or a regulator required it.** Neither obligation nor choice produced it. A third thing did.

---

## 29. What The Independent Studies Found

**[P1] — *Lancet Digital Health*, 2021. 23,954 chest X-rays, Bangladesh.**

Five commercial algorithms, read against Xpert MTB/RIF, on a dataset never used to train any of them.

| Algorithm | AUC | 95% CI |
|---|---:|---|
| **qXR (v3)** | **90.81** | 90.33 – 91.29 |
| CAD4TB | 90.34 | 89.81 – 90.87 |
| Lunit INSIGHT CXR | 88.61 | 88.03 – 89.20 |
| InferRead DR | 84.90 | 84.27 – 85.54 |
| JF CXR-1 | 84.89 | 84.26 – 85.53 |

qXR ranked **first**. All five significantly outperformed the radiologists. Only **two of five (40.00%)** met the WHO Target Product Profile for a triage test at 90% sensitivity — qXR at **74.3%** specificity and CAD4TB at **72.9%**. All five reduced required Xpert tests by **50%** while holding sensitivity above 90%.

There is a detail in that table worth pausing on. qXR's margin over second place is **0.47 percentage points**. Its own confidence interval is **0.96** points wide. **The lead is narrower than the uncertainty around it** — `verify.py` asserts this. "Ranked first" and "significantly better than the runner-up" are not the same claim, and this study supports the first, not the second.

**[P2] — *Scientific Reports*, 2021. Twelve AI solutions.**

**6 of 12 (50.00%)** performed on par with an Expert Reader, Qure.ai among them. Only **3 of 12 (25.00%)** performed significantly better than an Intermediate Reader — Qure.ai, Delft Imaging, and Lunit. The majority of solutions showed significantly lower performance in participants with a past history of TB.

**[P3] — *Lancet Digital Health*, 2024. South African prevalence survey, 774 people.**

516 bacteriologically negative, 258 positive (**33.33%** cases). Twelve CAD products. Lunit and Nexus posted AUCs near 0.9; **qXR fell into the 0.8–0.9 band** alongside four others. Three products came in under 0.8.

**qXR ranked first in [P1] and did not rank first in [P3].** Same indication, same product family, different country, different population, different answer.

All products performed worst in older individuals, people with previous TB, and people with HIV.

**[P4] — *International Journal of Medical Informatics*, 2023. Meta-analysis.**

**3,642** studies screened, **10** met criteria (**0.27%**), **8** survived bias assessment for meta-analysis (**0.22%**). Pooled estimates for three products:

| Product | Sensitivity | Specificity | DOR |
|---|---:|---:|---:|
| **qXR v2** | **0.944** | **0.692** | **3.63** |
| Lunit INSIGHT CXR v3.1 | 0.853 | 0.646 | 2.37 |
| CAD4TB v3.07 | 0.917 | 0.371 | 1.91 |
| *All products pooled* | *0.903* | *0.526* | *2.31* |

qXR ranked first on diagnostic odds ratio, **1.26** ahead of second place and **1.90 times** CAD4TB. Its specificity sits **16.60 percentage points** above the pooled figure.

That inclusion rate deserves its own sentence. **Of 3,642 studies screened, 8 were good enough to pool.** The evidence base for certified TB AI products, as of 2023, was eight studies.

---

## 30. Lima: The Study That Breaks The Number

**[P5] — *PLOS Global Public Health*, 2024. Lima, Peru.**

A prospective study in a tertiary hospital, enrolling **578** patients into two cohorts: **387** with cough or TB risk factors (triage) and **191** without (screening).

In the triage cohort, against culture as reference standard, **qXR v4**:

- **Sensitivity 0.91** — 59 of 65
- **Specificity 0.32** — 103 of 322

**219 false positives out of 322 negatives. A false-positive rate of 68.01%.**

Recomputed from the published counts, sensitivity is **0.908** and specificity is **0.320**; the case and control counts sum exactly to the triage cohort of 387.

The authors found no AUC difference between qXR v3 and v4 under either reference standard, found a high background rate of radiographic abnormality in this population (opacities 81%, consolidation 62%, nodules 58%), and concluded that the findings "further support the need for population and setting-specific thresholds for CAD programs."

In the screening cohort, only **one** patient had a positive Xpert result — so the diagnostic yield of screening people without cough or risk factors in that setting was essentially nil.

**Nothing went wrong here.** The device did what a high-sensitivity triage tool does in a population where nearly everyone has an abnormal chest X-ray for reasons other than TB. It caught almost all the cases. It also flagged two-thirds of the people who did not have it.

---

## 31. The Specificity Spread

Put the three independent settings side by side.

| Setting | Sensitivity | **Specificity** |
|---|---:|---:|
| Bangladesh screening centres [P1] | 90.00% | **74.30%** |
| Pooled meta-analysis [P4] | 94.40% | **69.20%** |
| Lima hospital triage [P5] | 90.80% | **32.00%** |
| **Spread** | **4.40 pp** | **42.30 pp** |

```
 Specificity, same product family, same indication
 80% |
     |   74.30
  70 |     █        69.20
     |     █          █
  60 |     █          █
     |     █          █
  50 |     █          █
     |     █          █
  40 |     █          █
     |     █          █      32.00
  30 |     █          █        █
     |     █          █        █
  20 |     █          █        █
     +---------------------------------
      Bangladesh   pooled     Lima
       screening    meta      triage
```

**Specificity varies 9.61 times more than sensitivity across settings.** The worst setting delivers **43.07%** of the best setting's specificity. The mean across the three is **58.50%**, which describes none of them.

This is the finding that matters most to anyone actually buying this software, and it generalises far beyond Qure.ai:

> **Sensitivity is close to a property of the model. Specificity is a property of the model and the population together.** A screening population and a hospital triage population differ in how many people have abnormal chest X-rays for reasons unrelated to the target disease — and that background rate, not the algorithm, drives the false positive count.

Every FDA clearance in §10 reports **one** specificity, from **one** test set. `verify.py` records `clearances_reporting_multi_setting_specificity` as **0**.

The regulator requires one population. The literature supplies many. **Only the literature answers the procurement officer's question.**

---

## 32. Four Summaries That Contradict Themselves

Day 87's §26 described an SEC reviewer catching a company claiming two algorithmic tests on page 9 and three on page 30. That is what adversarial review looks like when it works.

Day 88 records the other case. **Four of the nine 510(k) summaries — 44.44% — state the same statistic twice, with two different values, inside the same document.** All four are cleared. None was caught.

Here they are.

---

## 33. K230899: An AUC With Two Upper Bounds

The pneumothorax AUC confidence interval appears twice in [F4].

In the predicate comparison table:

> AUC: 0.9894 (95% CI: [0.9829, **0.9980**])

In the results table and the narrative:

> 98.94 (98.28 – **99.82**)

**99.80 versus 99.82.** A discrepancy of **0.02** percentage points on the upper bound, and **0.01** on the lower (0.9829 rendering as 98.29 against a stated 98.28).

This is small. It changes no conclusion and would alter no clearance decision — `verify.py` asserts `the_four_inconsistencies_change_any_clearance_decision` as **False**. It is included because it is the mildest member of a family, and the family is the point.

---

## 34. K231149: Confidence Intervals That Disagree With Their Own Table

The cardiothoracic ratio clearance [F5] reports RMSE for two measurements on **435** scans. The narrative and Table 2 give the same point estimates and different intervals.

| Measurement | Point | Narrative CI | Table 2 CI | Upper gap |
|---|---:|---|---|---:|
| Cardiac diameter | 7.55 mm | 6.95 – **8.34** | 6.96 – **8.38** | **0.04 mm** |
| Thoracic diameter | 5.43 mm | 4.95 – **6.11** | 4.94 – **6.09** | **0.02 mm** |

The point estimates agree exactly. Only the intervals move, and they move in **opposite directions** — the table's cardiac interval is wider than the narrative's, while the table's thoracic interval is narrower.

Against the predicate, the device is a real improvement: **14.30%** better on cardiac diameter RMSE (7.55 against 8.81 mm) and **62.29%** better on thoracic diameter (5.43 against 14.4 mm). Those are the numbers that justify clearance, and neither is in dispute.

---

## 35. K240740: A Confidence Interval That Cannot Exist

The lung nodule quantification clearance [F7] studied **118** chest CT scans from **104** subjects — **1.13** scans per subject — ground-truthed by three expert radiologists.

Its predicate comparison table states:

> Median Absolute Normalized Average Diameter Error [95% CI]: **11.1 (9.1 – 11.1)**

**The upper bound of the confidence interval equals the point estimate.**

A two-sided 95% confidence interval cannot have its upper bound sit exactly on the estimate unless the interval is degenerate. `verify.py` asserts `k240740_degenerate_ci_is_arithmetically_impossible` as **True**.

The results table, four pages later, gives the correct figure:

| Measurement | Normalized error % | Interval |
|---|---:|---|
| Short axis diameter | 14.3 | 13.95 – 16.67 |
| Long axis diameter | **11.1** | **9.52 – 12.50** |
| Volume | 20.7 | 17.29 – 22.41 |

So the comparison table's diameter interval is wrong on the upper bound by **1.40** and on the lower by **0.42**. The volume interval is wrong too — 17.6 – 22.6 in the comparison table against 17.29 – 22.41 in the results table, a **0.19** discrepancy on the upper bound.

This is the most serious of the four. A reader who takes the comparison table at face value gets a confidence interval that is both internally impossible and materially narrower than the real one.

---

## 36. K251934: The Same Condition, Reported Twice, Differently

From the most recent clearance, [F9], cleared **2026-01-16**:

> "The overall AUC for **aided** reads was 0.8466 (0.8106 – 0.8826) whereas the **aided** reads showed AUC of 0.8720 (0.8339 – 0.9100)."

The sentence reports **aided** reads twice, with two different values.

Table 5 of the same document resolves it: 0.8466 is the **unaided** AUROC and 0.8720 is the aided one. The preceding sentence — "there was a significant improvement in the aided reads, as compared to the unaided reads" — confirms the direction.

So the error is recoverable, by a reader who reaches the table. A reader who quotes the sentence reports that an AI device improved radiologists' AUC from 0.8466 to 0.8720 **while aided in both cases**, which is not a claim about the device at all.

**This is the newest clearance in the record**, granted five and a half years into the company's regulatory history, in a document whose entire purpose is to communicate a performance result.

---

## 37. What The Four Errors Actually Mean

It would be easy to over-read this, so here is the careful version.

**What these errors are not.** They are not fraud, not material misstatement, and not evidence that the devices don't work. Every one is recoverable from elsewhere in the same document. None would change a clearance decision. Transcription and typesetting errors of this kind are common in technical documents of every industry.

**What they are.** They are evidence about the **review process**, not about Qure.ai.

A 510(k) summary is a public-facing document. It is drafted by the manufacturer, submitted to FDA, reviewed as part of a submission that runs to thousands of pages, and published verbatim. Four of nine contain a number that contradicts another number a few pages away. That means the arithmetic in these documents is **not independently recomputed by anyone** between drafting and publication.

Compare Day 87 directly. SEC staff read a draft registration statement and caught a company contradicting itself about how many products it had. That caught error is the visible output of adversarial review. Here, the analogous errors survived to publication — in **44.44%** of the documents.

**The transferable lesson is the one this series keeps arriving at from different directions:**

> A document being *regulated* is not the same as a document being *checked*. Day 87's SEC wrote, explicitly, that a company is responsible for its disclosures "notwithstanding any review, comments, action or absence of action by the staff." Day 88 shows what that looks like in a different agency: numbers that do not survive addition, published under a clearance.

`verify.py` records `fda_verified_the_summaries_are_internally_consistent` as **False**.

---

## 38. The Evidence Ledger

Five questions a buyer would want answered, and what produced the answer.

| # | Question | Status | What compelled it |
|---|---|---|---|
| 1 | Does the device detect the finding? | **Disclosed** | Device regulation |
| 2 | How well across subgroups? | **Partial** | Device regulation |
| 3 | How well in my population? | **Disclosed** | Independent research |
| 4 | How well for TB? | **Disclosed** | Independent research |
| 5 | Company financials? | **Not disclosed** | *Nothing* |

- **3 of 5 (60.00%)** fully disclosed.
- **2** answered by device regulation; **2** by independent research.
- **0** volunteered by the company.
- **80.00%** of the ledger was answered **without the company choosing to answer it.**

Day 87's equivalent ledger for Tempus AI had **2 of 5 (40.00%)** disclosed — a **20.00 percentage point** gap in Qure.ai's favour.

**The private company's evidence ledger is better answered than the public company's.** And in both cases, the number of rows the company volunteered is zero.

---

## 39. Feature Analysis

| Capability | Cleared? | Accuracy evidence | Independent evidence |
|---|:---:|---|---|
| qER — ICH triage | Yes | Yes [F1] | — |
| qER-Quant — brain volumes | Yes | Measurement error only | — |
| qER-CTA — LVO | Yes | AUC 0.959 [F8] | — |
| qXR-BT — tube position | Yes | Measurement error only | — |
| qXR-CTR — cardiothoracic ratio | Yes | RMSE only | — |
| qXR-PTX-PE — PTX/PE triage | Yes | Full [F4] | — |
| qXR-LN — lung nodules | Yes | Yes [F6] | — |
| qXR-Detect — chest ROI | Yes | Reader study [F9] | — |
| qCT LN Quant | Yes | Normalized error | — |
| **qXR — tuberculosis** | **No** | **None** | **Extensive [P1]–[P5]** |

The last row is the entire shape of the case study in one line.

---

## 40. Competitive Analysis

Unusually for this series, the competitive picture can be drawn from independent head-to-heads rather than vendor claims — because [P1], [P2], and [P3] tested the competitors **on the same data at the same time**.

| Competitor | Appears in | Relative to qXR |
|---|---|---|
| **CAD4TB** (Delft Imaging) | [P1], [P2], [P4] | 2nd in [P1] by 0.47pp; also met WHO TPP; far weaker pooled specificity (0.371) |
| **Lunit INSIGHT CXR** | [P1], [P2], [P3], [P4] | Below qXR in [P1] and [P4]; **above** qXR in [P3] |
| **Nexus** | [P3] | Near 0.9 AUC in [P3]; ahead of qXR there |
| **InferRead DR** (Infervision) | [P1], [P2] | Below qXR in [P1] |
| **JF CXR-1 / CXR-2** | [P1], [P3] | Lowest in [P1] |
| **XrayAME, RADIFY, TiSepX-TB** | [P3] | Below 0.8 AUC |
| **Delft, OXIPIT, DeepTek** | [P2] | On par with Expert Reader alongside Qure.ai |

The competitive read: **qXR is consistently in the top tier and not consistently at the top of it.** It ranked first in [P1] and first on DOR in [P4]; it ranked outside the leading pair in [P3]. Its differentiator across studies is specificity — 74.3% in [P1] against CAD4TB's 72.9%, and 0.692 pooled against CAD4TB's 0.371 in [P4], a gap that translates directly into confirmatory tests not wasted.

**The strategic observation for a PM:** in a market where twelve products can be benchmarked against each other on one dataset by researchers nobody paid, product claims stop being a marketing surface. [P3] evaluated twelve products and found three of them below 0.8 AUC. Those three are all on the market.

---

## 41. Porter's Five Forces

| Force | Assessment | Evidence |
|---|---|---|
| **Buyer power** | **High** | Twelve substitutable products benchmarked head-to-head [P3]; buyers can compare on public data |
| **Rivalry** | **High** | 12 products in one study; new entrants appearing faster than validation can keep up [P3] |
| **Threat of new entrants** | **Moderate** | 510(k) via predicate is a real but traversable barrier; Qure.ai itself cleared 9 in 5.58 years |
| **Supplier power** | **Low** | No disclosed dependency in the regulatory record |
| **Substitutes** | **High** | A radiologist. In [P1] all five algorithms beat them; in [P2] six matched an Expert Reader |

The [P3] authors' own conclusion — that "the rapid emergence of products and versions necessitates a global strategy to validate new versions" — is a statement about market structure as much as about science. Products and versions are shipping faster than independent validation can assess them, which means the buyer's information advantage is temporary and version-specific.

Note the version problem directly: [P1] tested **qXR v3**, [P4] pooled **qXR v2**, [P5] tested **v4** and v3. `verify.py` records `qxr_version_in_fda_clearances_same_as_in_tb_studies` as **False**.

---

## 42. Business Model Canvas

| Block | Content |
|---|---|
| **Key partners** | Not disclosed in the sources used |
| **Key activities** | Model development; regulatory submission; PACS integration; clinical validation |
| **Key resources** | Training data (74% India, 20.04% EU, 3.9% US by the one disclosed composition); 9 FDA clearances; predicate positions in 4 product codes |
| **Value propositions** | Triage and detection at the point of acquisition; measurement consistency; screening-cost reduction (50% fewer Xpert tests at >90% sensitivity [P1]) |
| **Customer relationships** | Not disclosed |
| **Channels** | PACS and worklist integration |
| **Customer segments** | Hospitals and imaging providers (cleared products); national TB programmes (uncleared product) |
| **Cost structure** | Not disclosed |
| **Revenue streams** | **Not disclosed** |

Three "not disclosed" rows in a canvas is normally a research failure. Here it is the finding: this is the complete public commercial picture of a company with nine FDA clearances.

---

## 43. SWOT

**Strengths**
- **9** FDA clearances across **4** product codes in **5.58** years.
- Ranked **first of five** on AUC in a 23,954-scan independent head-to-head [P1].
- Ranked **first of three** on pooled DOR in a formal meta-analysis [P4].
- One of only **3 of 12** products to significantly outperform an Intermediate Reader [P2].
- **76.47%** of its TB evidence base is independent of it.
- K230899's subgroup counts all reconcile — a well-constructed disclosure.

**Weaknesses**
- **Zero** FDA clearances for its most-studied indication.
- Specificity ranges **32.00%–74.30%** across settings — a **42.30 pp** spread with no published guidance on threshold selection by population.
- **4 of 9** clearance summaries contain an internal numeric contradiction.
- Newest clearance has the **lowest** specificity of the five (**62.19%** aided).
- No public financial information of any kind.
- Training data **18.97×** more Indian than US, tested only on US data.

**Opportunities**
- Publishing a setting-stratified specificity table would make it the only vendor in this market answering the buyer's actual question (§46, P1).
- TB clearance would align the regulatory and research records (§46, P3).
- The version-drift problem [P3] flags is an opening for whoever solves validation cadence first.

**Threats**
- [P3] shows rank is not stable across populations — a competitor leads in South Africa.
- All products degrade in older patients, prior TB, and HIV — the populations screening programmes most need.
- Buyers can now benchmark twelve products on public data.
- **Disclosure asymmetry**: a buyer can evaluate the product and cannot evaluate the company.

---

## 44. Metrics That Matter

| Metric | Why | Disclosed? | What would make it credible |
|---|---|:---:|---|
| Specificity **by setting type** | Drives confirmatory testing cost | **No** | A stratified table across published populations |
| Threshold recommendation by population | [P5]'s explicit ask | **No** | Published per-setting operating points |
| Nodule-level vs scan-level sensitivity | 9.73pp gap in the same study | **Yes** [F6] | Already credible |
| Subgroup performance in prior-TB and HIV | Where all products degrade [P3] | **No** (vendor) / **Yes** (independent) | Vendor-side confirmation |
| Version-to-version performance delta | v2/v3/v4 tested in different studies | **No** | A published version changelog with metrics |
| Real-world post-deployment performance | Drift after clearance | **Partial** | One vendor-authored study exists |

Five of six are undisclosed by the vendor. Two of those five are answered anyway, by people who do not work there.

---

## 45. North Star and Guardrails

**North Star:** *Confirmatory tests avoided per case detected.*

This is the honest North Star for a triage product, because it is the unit in which a screening programme actually spends money. [P1] gives the shape of it: a 50% reduction in Xpert tests while holding sensitivity above 90%.

**Guardrails:**

| Guardrail | Discipline |
|---|---|
| Sensitivity floor | Never trade below the WHO TPP's 90% to buy specificity |
| Specificity, **reported by setting** | No single specificity figure published without naming its population |
| Subgroup floor | Prior-TB, HIV, and older-patient performance reported every release |
| Version traceability | Every published metric carries the version that produced it |
| Internal arithmetic | Every number in a regulatory document recomputed before submission |

The second guardrail is the one this case study earns, and it is the direct descendant of Day 87's: *never publish the flattering half of a ratio without the unflattering half.* Day 88's version is **never publish a performance number without the population that produced it.**

---

## 46. Product Recommendations

**P1 — Publish a setting-stratified specificity table.**
*Gap:* §31. Specificity spans 42.30 pp across three published settings and no vendor document acknowledges the range.
*Change:* A public table giving sensitivity, specificity, and recommended threshold for each population type where qXR has been independently evaluated, citing the study behind each row.
*Why:* It is the only question procurement asks, and [P5]'s authors explicitly called for it.

**P2 — Correct the four internal inconsistencies.**
*Gap:* §32–§36.
*Change:* Issue corrected summaries; institute a recompute-before-submission step.
*Why:* Cheap, unambiguous, and the errors are in the company's own public-facing documents.

**P3 — Seek FDA clearance for the TB indication.**
*Gap:* §27. Nine clearances, zero for the most-studied use.
*Change:* Pursue a TB triage clearance on the existing independent evidence base.
*Why:* It would close the gap between what the company is regulated for and what it is known for.

**P4 — Publish a living registry of independent evaluations.**
*Gap:* §28. 13 independent studies exist and no single place collects them.
*Change:* A maintained public page listing every independent evaluation, its population, its result, and **whether a Qure.ai author was involved** — the ratio labelled, not hidden.
*Why:* Day 87 showed what happens when a company stops publishing its own independence ratio. This is the opposite move.

---

## 47. RICE Prioritisation

**Definitions.** Reach is ordinal 1–10 with the anchor stated. Impact 0.25/0.5/1/2/3. Confidence 0–1. Effort in person-months. RICE = (R × I × C) / E.

| | Reach | Reach anchor | Impact | Conf. | Effort | **RICE** |
|---|---:|---|---:|---:|---:|---:|
| **P1** Setting-stratified specificity | 8 | Every screening programme and procurement committee evaluating qXR | 3.0 | 0.90 | 0.75 | **28.80** |
| **P2** Correct the four errors | 3 | Readers of the four affected summaries | 1.0 | 0.95 | 0.25 | **11.40** |
| **P3** TB clearance | 9 | The global TB screening population | 3.0 | 0.50 | 14.00 | **0.96** |
| **P4** Independent-evidence registry | 6 | Buyers and researchers across all indications | 2.0 | 0.70 | 2.00 | **4.20** |

**Base ranking: P1 (28.80) → P2 (11.40) → P4 (4.20) → P3 (0.96).** Spread: **27.84**.

P1 leads by a wide margin. It is cheap, high-confidence, high-impact, and answers the one question the evidence shows nobody else is answering.

---

## 48. The Stress Test

The stress case applies each proposal's **actual binding constraint**.

| | Binding constraint | C mult. | E mult. | **Stressed** | Decay |
|---|---|---:|---:|---:|---:|
| **P1** | Publishing 32.00% next to 74.30% hands every competitor a procurement weapon; defending each row requires per-setting validation the company does not control | **0.12** | **6.00** | **0.58** | **−98.00%** |
| **P2** | Document control and regulatory-affairs review only | 0.95 | 1.25 | **8.66** | −24.00% |
| **P3** | Submission, evidence assembly, and review timeline | 0.85 | 1.30 | **0.63** | −34.62% |
| **P4** | Curation burden and the awkwardness of labelling vendor-authored rows | 0.75 | 1.50 | **2.10** | −50.00% |

**Stressed ranking: P2 (8.66) → P4 (2.10) → P3 (0.63) → P1 (0.58).**

**P1 goes from first to last.** The reversal is total and is asserted programmatically — `p1_leads_base` and `p1_ranks_last_under_stress` are both hard assertions in the gate.

Every other proposal gains exactly one place, because P1 falls the whole distance. The field compresses from a spread of **27.84** to **8.09**.

---

## 49. Why P1 Dies

This is the second consecutive day the stress test has killed the cheapest, most obviously correct recommendation, and the mechanism is the same both times — which is itself the finding.

P1 decays **98.00%**, more than any other proposal. The constraint is not cost; it is three-quarters of a person-month. The constraint is that **publishing the range converts a marketing asset into a liability.**

Today, Qure.ai can accurately say its software met the WHO Target Product Profile in a 23,954-scan independent study at 74.3% specificity. That is true, independently verified, and excellent. A setting-stratified table would place, immediately beneath it, the row that says 32.00% in a Lima hospital — equally true, equally independent, and a number no competitor would ever have to print unless they also published a range.

**Publishing a range is unilateral disarmament in a market where everyone else publishes a point estimate.**

And note what that implies. The honest disclosure is punished *specifically because* it is more informative. The company that publishes one flattering number and the company that publishes a range are, to a procurement committee reading quickly, the second one looks worse.

Day 87 found the same structure and confirmed it against history: Tempus's self-authorship numerator, cheap and obviously correct to publish, left the 10-K the moment nobody was reviewing. Day 88 finds the structure **before** the fact rather than after it — no vendor in this market publishes a stratified specificity table, and the model says why.

> **When a cheap, obviously correct disclosure does not happen anywhere in an entire market, the explanation is rarely that nobody thought of it. The property that makes it valuable to the reader is the property that makes it unsurvivable for the publisher.**

---

## 50. MoSCoW

| | Item | Rationale |
|---|---|---|
| **Must** | Correct the four internal inconsistencies (P2) | Highest stressed score; unambiguous; own documents |
| **Must** | Version-tag every published metric | [P1]/[P4]/[P5] tested v3/v2/v4; nothing ties them together |
| **Should** | Independent-evidence registry (P4) | Survives its constraint; converts a strength into a visible one |
| **Should** | TB clearance (P3) | Highest reach; gains a place under stress |
| **Could** | Setting-stratified specificity (P1) | Correct on the merits; needs either industry norms or a mandate to survive |
| **Won't** | Financial disclosure | No obligation, no mechanism, no realistic path |

P1 moves from first on base RICE to "Could" — because MoSCoW is an execution framework and §49 is about execution.

---

## 51. Kano

| Feature | Category | Reasoning |
|---|---|---|
| FDA clearance | **Must-be** | Absence is disqualifying in the US market |
| Sensitivity above WHO TPP | **Must-be** | Below it the product has no screening use |
| Independent head-to-head evidence | **Attractive → Must-be** | [P3] benchmarked twelve products; this is becoming table stakes |
| Setting-stratified specificity | **Attractive** | Nobody publishes it; the first to do so defines the category |
| Subgroup performance in HIV / prior TB | **Attractive** | Independently known, vendor-unconfirmed |
| Version changelog with metrics | **Indifferent → Must-be** | Invisible until a buyer is burned by a version change |

The third row has already migrated once. In 2021 an independent head-to-head was a novelty; by [P3] in 2024 there were twelve products in one. The fourth row is where the third was five years ago.

---

## 52. AARRR

| Stage | Cleared products | TB product |
|---|---|---|
| **Acquisition** | 510(k) clearance as market entry | WHO-aligned screening programmes |
| **Activation** | PACS integration; first flagged case | First screening round |
| **Retention** | Not disclosed | Not disclosed |
| **Revenue** | **Not disclosed** | **Not disclosed** |
| **Referral** | Predicate citations by later devices | **76.47% independent literature** |

The referral row is the anomaly worth naming. For most companies in this series, referral means testimonials. Here it means thirteen research teams who evaluated the product without being asked and published what they found.

---

## 53. HEART

| Dimension | Signal | Disclosed? |
|---|---|:---:|
| **Happiness** | Clinician satisfaction | One study on user perspectives exists in the TB set |
| **Engagement** | Scans processed per site | No |
| **Adoption** | Sites deployed | No |
| **Retention** | Renewals | No |
| **Task success** | **Sens/spec/AUC** | **Yes — five clearances plus five independent studies** |

Day 87's HEART table had an **empty** task-success row for a company with a $1.27bn revenue line. Day 88's is the only row that is **full**.

That single contrast is the case study.

---

## 54. What a PM Should Take From This

**1. Read the regulatory record, not the website.** FDA's 510(k) database is free, queryable through openFDA, and every clearance summary is a public PDF containing the performance data a vendor's marketing will round off. For any medical device competitor, partner, or acquisition target, it is the highest-yield hour available — the direct analogue of Day 87's SEC comment letters.

**2. Classification is destiny.** What a regulator calls your product determines what the public learns about it. Qure.ai's QIH devices report measurement error and its MYN/QAS/QFM devices report sensitivity — with **perfect** 9-of-9 correspondence. Before you ask "why won't they publish accuracy," ask what the device is classified as.

**3. A performance number without a population is not a performance number.** Sensitivity moved **4.40** points across three settings. Specificity moved **42.30**. Any vendor quoting one specificity figure is quoting the population it was measured in, whether or not they name it. **Always ask which one.**

**4. Regulated is not checked.** **44.44%** of these cleared summaries contradict themselves internally, including a 95% confidence interval whose upper bound equals its point estimate. Day 87's SEC said so in writing; Day 88 shows it in arithmetic. A document passing through a regulator has been *reviewed for a purpose*, not *audited for correctness*.

**5. The best evidence in a market often belongs to nobody.** The most useful facts about Qure.ai's product were produced by researchers in Bangladesh, South Africa, and Peru who had their own reasons to look. Neither obligation nor the company's choice produced them. **When evaluating any product, ask who has a reason to measure it that isn't commercial — and go read them first.**

---

## 55. Roadmap

**Horizon 1 — next release cycle**
- Correct the four internal inconsistencies (P2).
- Version-tag every published performance metric.
- Publish subgroup performance for prior-TB and HIV populations, confirming or contesting [P3].

**Horizon 2 — within four quarters**
- Stand up the independent-evidence registry, with vendor-authorship labelled (P4).
- Publish recommended operating thresholds by population type, answering [P5] directly.
- Begin TB clearance evidence assembly (P3).

**Horizon 3**
- Setting-stratified specificity table (P1) — contingent on either an industry norm or a procurement mandate, per §49.
- Post-deployment performance monitoring published on a fixed cadence.

---

## 56. Risks

| Risk | Basis | Severity |
|---|---|---|
| **Population transfer** | Specificity 32.00%–74.30% across settings | **High** |
| **Version drift** | v2/v3/v4 tested in different studies; no linking changelog | **High** |
| **Subgroup degradation** | All products worst in older, prior-TB, HIV [P3] | **High** |
| **Competitive rank instability** | 1st in [P1], outside the top pair in [P3] | **Moderate** |
| **Document quality** | 4 of 9 summaries self-contradictory | **Moderate** |
| **Regulatory/research divergence** | 0 TB clearances, 17 TB papers | **Moderate** |
| **Evaluability asymmetry** | Product fully evaluable, company not at all | **Structural** |

The last row is Day 88's addition to the standard list, and it is the mirror of Day 87's "disclosure decay." There, a company's numbers were public and its evidence was not. Here, a company's evidence is public and its numbers are not. **In neither case did the company choose.**

---

## 57. Open Questions

1. What is qXR's specificity in an Indian screening population — the population 74% of its training data came from?
2. Why has TB never been submitted for FDA clearance?
3. What changed between v2, v3, and v4, and by how much?
4. Do the 37 unknown-sex scans in K230899 differ clinically, or only statistically?
5. How were the four internal inconsistencies introduced, and does any recompute step exist?
6. What is the company's revenue, and does it matter to a buyer who can evaluate the product completely and the vendor not at all?
7. Would a stratified specificity table actually cost a sale, or is §49's constraint a belief rather than a fact?

Question 7 is the one worth sitting with. §49 argues from constraint structure that honest disclosure is punished. That argument is a model, not a measurement, and the model would be falsified the moment one vendor published a range and won business with it.

---

## 58. Method Notes

**What was done.** The 510(k) list came from the openFDA `device/510k` endpoint filtered on `applicant:"qure.ai"`. Each summary PDF was fetched from `accessdata.fda.gov/cdrh_docs/pdf{YY}/{K-number}.pdf` and converted with `pdftotext -layout`, which preserves table columns. Registry data came from the GLEIF API. Literature came from PubMed.

**Two fetches failed transiently.** K212690 and K231149 initially returned an HTML error page and a 401 respectively. Both succeeded on retry against the correct year directory. The retry is noted because a silent failure here would have produced a case study asserting seven clearances instead of nine.

**Counting sensitivity mentions.** A naive grep for "sensitivit" in K240740 returns one hit. Reading it shows the phrase is "conditions of image quality that diminish chest radiographic sensitivity" — a statement about radiography, not about the device. It is excluded. The gate records `k240740_sensitivity_mentions_about_device_performance` as **0**. This is the same class of error as Day 87's comment-letter miscount, caught the same way: by reading rather than pattern-matching.

**Column scrambling.** `pdftotext` can interleave adjacent table columns. Every inconsistency reported in §32–§36 was confirmed by reading the surrounding raw layout, not from a grep hit. The K230899 predicate comparison table, in particular, lists findings in **opposite order** in its two columns (predicate: pleural effusion then pneumothorax; subject: pneumothorax then pleural effusion), which makes a straight horizontal read misleading. That layout quirk is reported here as a readability observation and is **not** counted among the four inconsistencies.

**The rounding trap, twice more.** Two hand-stated expectations failed on the gate's first run: the stressed RICE spread (stated 8.08, computed **8.09**) and the Day 88 / Day 86 ratio (stated 286.44, computed **286.45**). Both are the rounded-intermediate trap this series first hit on Day 82. The Day 88/86 ratio is the more instructive: computed from rounded inputs (76.47 ÷ 0.27) it gives **283.22**, an error of 3.23. Both wrong values are now asserted in the gate so the correct one is unambiguous.

**What was not used.** No company website, press release, funding announcement, or news article. This cost real information — deployment scale, funding, and customer count are all publicly reported somewhere and none of it is here. The constraint was kept because the case study is about what *compulsion* produces, and mixing in voluntary communication would have destroyed the tier structure in §6.

**What could not be obtained.** Qure.ai's statutory financial filings with India's Registrar of Companies are not freely retrievable through the routes used here. CE marking and CDSCO status were not independently verified and are therefore **absent from this document entirely** rather than asserted from secondary sources.

**Diagram standard.** Markdown tables and ASCII only. Mermaid was dropped at Day 50.

---

## 59. Series Position

Day 88 closes the disclosure arc that Day 82 opened.

| Day | Company | Structure | Result |
|---|---|---|---|
| 82 | Doximity | Public | Material finding buried in the 10-Q; marketing claims appeared **0** times in it |
| 83 | OpenEvidence | Private | **0 of 5** headline claims independently confirmed |
| 84 | Abridge | Private | Vendor's own peer-reviewed studies reported **0** accuracy metrics |
| 85 | Eka Care | Private | National proxy and field study converged to **1.59 pp** |
| 86 | Hippocratic AI | Private | Safety claim rested on **0.27%** evidence coverage |
| 87 | Tempus AI | **Public** | Maximum disclosure obligation, **0** algorithm performance metrics |
| 88 | Qure.ai | **Private** | **Zero** disclosure obligation, **5** clearances with full accuracy data |

**The arc's hypothesis — does obligation beat choice? — resolves in two parts.**

Day 87 answered the first: yes, obligation beats choice, by roughly 59× on evidence coverage, but securities disclosure compels **process** rather than **performance**.

Day 88 answers the second: **the kind of obligation determines the kind of evidence.** Securities regulation asks "what must investors know?" and gets financial statements and a description of method. Device regulation asks "is this as safe and effective as the predicate?" and gets sensitivity, specificity, and confidence intervals.

Neither asks "how well does this work in my population?" **That question was answered by thirteen research teams who nobody required to ask it.**

The share of Qure.ai's TB evidence base that is independent, **76.47%**, is **286.45 times** Day 86's evidence coverage of **0.27%** — the two ends of the range this arc has measured.

---

## 60. What Comes Next

**Tomorrow is Gaudium IVF** — and it moves from imaging to fertility, from a company with nine regulatory clearances to a clinical services business, and from evidence that a regulator compelled to evidence that a *patient* has to evaluate without any of the machinery of the last seven days.

Day 90 closes the series with **Health in ChatGPT** — a general-purpose system used for health questions, with no device clearance, no securities obligation, and no indication-specific evidence base at all. After 89 days of asking what compels evidence, the final case asks what happens when nothing does.

---

## 61. Limitations In One Place

Stated compactly here and in full in `ASSUMPTIONS.md`.

- **One company, one method.** The general claims in §54 are supported by Qure.ai's record and by contrast with Days 82–87, not by a sample of device manufacturers.
- **The literature count is search-dependent.** 17 papers is what one documented PubMed query returned on one day. §1.3 of `ASSUMPTIONS.md` gives the query and its limits.
- **Version mismatch.** Devices cleared by FDA and versions tested in the TB literature are not the same artefacts.
- **The four inconsistencies are minor.** None changes a clearance decision. They are evidence about process, not about product safety.
- **Financials are absent, not searched-for-and-missing.** No route used here reaches them.
- **Point-in-time.** All figures as at 2026-09-26.

---

## 62. Open Data For Anyone Who Wants To Check

Every source in this case study is free and directly retrievable:

```bash
# All Qure.ai FDA clearances
curl "https://api.fda.gov/device/510k.json?search=applicant:%22qure.ai%22&limit=100"

# Any clearance summary (YY = first two digits of the K-number)
curl "https://www.accessdata.fda.gov/cdrh_docs/pdf23/K230899.pdf"

# The statutory registry entry
curl "https://api.gleif.org/api/v1/lei-records?filter%5Bentity.legalName%5D=Qure.ai%20Technologies"
```

The verification gate and cross-check in this folder reproduce every number above from those inputs.

---

## 63. Verification

`verify.py` — **344 checks, all passing.** Written and passing before the first sentence of this README existed.

Coverage: identity and statutory registration (18); the FDA clearance record (19); the partition (12); K230899 (54); internal inconsistencies (46); remaining accuracy disclosures (23); the uncleared indication (5); the independent literature (77); the specificity spread (14); the evidence ledger (13); RICE and stress test (28); series continuity (18); negative controls (12); counter-examples (5).

`crosscheck.py` confirms that every two- and three-decimal figure in `README.md` and `ASSUMPTIONS.md` traces to a value asserted in the gate.

Two hand-stated expectations failed on first run. In both cases the machine was right. §58 records them.

---

## 64. References

**FDA 510(k) summaries**, US Food and Drug Administration, Center for Devices and Radiological Health. All retrieved 2026-09-26 from `accessdata.fda.gov/cdrh_docs/`.

1. **[F1]** K200921 — qER. Decision 2020-06-17. Product code QAS.
2. **[F2]** K211222 — qER-Quant. Decision 2021-07-30. Product code QIH.
3. **[F3]** K212690 — qXR-BT. Decision 2021-12-21. Product code QIH.
4. **[F4]** K230899 — qXR-PTX-PE. Decision 2023-08-22. Product code QFM.
5. **[F5]** K231149 — qXR-CTR. Decision 2023-09-22. Product code QIH.
6. **[F6]** K231805 — qXR-LN. Decision 2023-12-22. Product code MYN.
7. **[F7]** K240740 — qCT LN Quant. Decision 2024-08-16. Product code QIH.
8. **[F8]** K251610 — qER-CTA (v1.0). Decision 2025-09-08. Product code QAS.
9. **[F9]** K251934 — qXR-Detect. Decision 2026-01-16. Product code MYN.
10. **[FDB]** openFDA device 510(k) API. `https://api.fda.gov/device/510k.json?search=applicant:"qure.ai"`
11. **[G]** GLEIF. LEI record 3358009NQ689LYF5LO48, QURE.AI TECHNOLOGIES PRIVATE LIMITED. `https://api.gleif.org/api/v1/lei-records`

**Peer-reviewed literature.** According to PubMed:

12. **[P1]** Qin ZZ, et al. Tuberculosis detection from chest x-rays for triaging in a high tuberculosis-burden setting: an evaluation of five artificial intelligence algorithms. *The Lancet Digital Health*, 2021. PMID 34446265. DOI [10.1016/S2589-7500(21)00116-3](https://doi.org/10.1016/S2589-7500(21)00116-3)
13. **[P2]** Independent evaluation of 12 artificial intelligence solutions for the detection of tuberculosis. *Scientific Reports*, 2021. PMID 34903808. DOI [10.1038/s41598-021-03265-0](https://doi.org/10.1038/s41598-021-03265-0)
14. **[P3]** Computer-aided detection of tuberculosis from chest radiographs in a tuberculosis prevalence survey in South Africa: external validation and modelled impacts of commercially available artificial intelligence software. *The Lancet Digital Health*, 2024. PMID 39033067. DOI [10.1016/S2589-7500(24)00118-3](https://doi.org/10.1016/S2589-7500(24)00118-3)
15. **[P4]** Benchmarking the diagnostic test accuracy of certified AI products for screening pulmonary tuberculosis in digital chest radiographs. *International Journal of Medical Informatics*, 2023. PMID 37549498. DOI [10.1016/j.ijmedinf.2023.105159](https://doi.org/10.1016/j.ijmedinf.2023.105159)
16. **[P5]** Accuracy of digital chest x-ray analysis with artificial intelligence software as a triage and screening tool in hospitalized patients being evaluated for tuberculosis in Lima, Peru. *PLOS Global Public Health*, 2024. PMID 38324610. DOI [10.1371/journal.pgph.0002031](https://doi.org/10.1371/journal.pgph.0002031)

Literature identified via PubMed.

**Assumptions, source conflicts, and limitations:** see `ASSUMPTIONS.md`.

---

## 65. Closing Note

Seven days ago this series started asking whether being obliged to disclose produces better evidence than choosing to. The answer turned out to depend entirely on **who is doing the obliging, and what they happen to care about.**

The SEC cares whether investors are misled, so Tempus published a beautiful description of how it validates models and not one number about whether they work.

The FDA cares whether a device is as safe and effective as its predicate, so Qure.ai published sensitivity, specificity, AUC, confidence intervals, and the counts behind them — and nothing about the company at all.

Neither regulator cares whether the number transfers to your hospital. That question got answered anyway, in Dhaka and Cape Town and Lima, by people with no stake in the answer.

**The most useful evidence about this product was produced by nobody who was required to produce it, and nobody who stood to gain from it.** That is worth remembering the next time a vendor's single, confident, perfectly accurate performance figure arrives in a slide deck.

---

*Day 88 of 90. Written by Gaurav Singh. Sources are primary and cited. Figures are computed, not asserted. Where the record is silent, this document says so.*
