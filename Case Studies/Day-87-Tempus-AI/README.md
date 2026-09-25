# Day 87 — Tempus AI: What a Company Says When It Has To

**A Product Management case study on disclosure, obligation, and the difference between a process and a result.**

*Part of a 90-day series of evidence-based product case studies. Day 87 of 90.*

---

## 1. At a Glance

| | |
|---|---|
| **Company** | Tempus AI, Inc. |
| **Former name** | Tempus Labs, Inc. |
| **Listing** | Nasdaq: **TEM** |
| **SEC CIK** | 0001717115 |
| **Commission file number** | 001-42130 |
| **State of incorporation** | Nevada |
| **SIC code** | 7370 — Services: Computer Programming, Data Processing |
| **Headquarters** | 600 West Chicago Avenue, Suite 510, Chicago, Illinois |
| **FY2025 revenue** | $1,271.789M |
| **FY2025 net loss** | $(245.028)M |
| **Q2 2026 net income** | **$5.642M — the first GAAP-positive quarter in the disclosed record** |
| **Live transaction** | Acquisition of Personalis, Inc. (agreement 20 Jul 2026; Form S-4 filed 31 Aug 2026) |
| **Evidence base** | SEC EDGAR primary filings only — 10-K, 10-Q, 8-K, S-4, 424B4, and ten staff comment letters |
| **Verification** | `verify.py` — **265 programmatic checks, all passing** |

---

## 2. Why This Company, Today

Days 83 through 86 of this series examined four private healthcare-AI companies: OpenEvidence, Abridge, Eka Care, and Hippocratic AI. Each one published claims about its product. None of them was obliged to publish anything at all. The work of those four days was, in large part, the work of reconstructing from the outside what a company had chosen not to say from the inside — court dockets, statutory registries, preprints, national programme dashboards, peer-reviewed literature.

Day 86 closed by naming the hypothesis that the arc had been building toward:

> Days 83 through 86 have asked what private companies choose to publish. Day 87 asks what a public company **must** publish, and whether obligation produces better evidence than choice.

Tempus AI is the test case. It is listed on Nasdaq. It files audited annual reports, quarterly reports, current reports, and — because it is in the middle of acquiring another listed company — a registration statement on Form S-4 that carries obligations no ordinary filing does. It has also been, for longer than almost any company of its size, in sustained correspondence with the staff of the SEC's Division of Corporation Finance.

That correspondence is public. It is the most underused primary source in product research, and it is the reason this case study exists in the form it does. Between September 2021 and November 2023 the staff issued **ten** comment letters to Tempus containing **66** numbered comments. Each one is a question a professional reviewer thought a reader deserved an answer to. Each one is, in effect, a free external audit of what a product company was willing to tell the public about itself.

The answer to the hypothesis is **yes, and the qualification matters more than the answer**.

---

## 3. How to Read This Case Study

This is not a profile of Tempus. It is an examination of a disclosure system, with Tempus as the specimen.

The spine of the case study is a single number that exists in the public record at exactly two moments in time, appears because a regulator asked for it, and then disappears — while the sentence around it survives word for word. Everything else in these 65 sections either builds toward that finding or tests its generality.

Three reading paths:

- **If you want the finding**: §24 through §34.
- **If you want the method**: §4, §5, §6, §63.
- **If you want the product analysis**: §44 through §60.

Every figure carrying two decimal places in this document is produced by `verify.py` in this folder. Nothing in this document is estimated, modelled, or inferred unless the sentence containing it says so.

---

## 4. Evidence Standard

The standard applied here is the one this series has used since Day 1, tightened over 86 prior case studies:

1. **No fabrication.** No metric, date, quotation, or relationship appears unless it is in a cited primary source.
2. **Facts and inferences are separated at the sentence level**, not in a disclaimer at the end.
3. **Arithmetic is executed, not asserted.** Every derived figure is computed in `verify.py` from unrounded inputs and asserted against an expected value before any prose is written.
4. **Absences are findings.** When a source does not say something, that is recorded as a fact about the source, not as a gap to be filled by plausible reasoning.
5. **The gate precedes the prose.** `verify.py` was written and passing before the first sentence of this README existed.

The fifth rule is the one that does the most work. When a verification gate is written after the narrative, it verifies the narrative. When it is written first, the narrative has to survive it.

---

## 5. Source Inventory

Every source used in this case study, with its EDGAR accession number. All retrieved 2026-09-25 from `www.sec.gov` and `data.sec.gov` under CIK 0001717115.

| Ref | Document | Date | Accession |
|---|---|---|---|
| **[A]** | SEC staff comment letter — Draft Registration Statement on Form S-1 | 2021-09-30 | 0000000000-21-011937 |
| **[B1]** | SEC staff comment letter — Amendment No. 1 | 2021-11-16 | 0000000000-21-013853 |
| **[B2]** | SEC staff comment letter — Amendment No. 1 | 2021-11-29 | 0000000000-21-014324 |
| **[B3]** | SEC staff comment letter — Amendment No. 2 | 2021-12-17 | 0000000000-21-015102 |
| **[B4]** | SEC staff comment letter — Amendment No. 3 | 2022-05-11 | 0000000000-22-005176 |
| **[B5]** | SEC staff comment letter — Response Letter No. 3 | 2022-08-03 | 0000000000-22-008188 |
| **[B6]** | SEC staff comment letter — Amendment No. 4 | 2022-10-27 | 0000000000-22-011783 |
| **[B7]** | SEC staff comment letter — Amendment No. 5 | 2023-01-27 | 0000000000-23-000921 |
| **[B8]** | SEC staff comment letter — Amendment No. 6 | 2023-05-05 | 0000000000-23-004692 |
| **[B9]** | SEC staff comment letter — Amendment No. 8 | 2023-11-21 | 0000000000-23-012780 |
| **[C]** | SEC staff letter — "we have not reviewed and will not review" | 2025-03-04 | 0000000000-25-002419 |
| **[D]** | Form 424B4 — IPO prospectus | 2024-06-17 | 0001193125-24-161989 |
| **[E]** | Form 10-K — fiscal year 2025 | 2026-02-24 | 0001193125-26-066961 |
| **[F]** | Form 10-Q — quarter ended 30 Jun 2026 | 2026-07-30 | 0001193125-26-326090 |
| **[G]** | Form 8-K — Item 1.01, Personalis merger agreement | 2026-07-20 | 0001193125-26-309073 |
| **[H]** | Form S-4 — registration statement / proxy statement-prospectus | 2026-08-31 | 0001193125-26-376895 |
| **[I]** | XBRL company facts API | 2026-09-25 | `data.sec.gov/api/xbrl/companyfacts/CIK0001717115.json` |
| **[J]** | Company correspondence — acceleration requests | 2024-06-11, 2025-03-05 | 0001193125-24-159092, 0001193125-25-047163 |

No secondary source — no press release, no analyst note, no news article, no company blog — is used anywhere in this document. That is a deliberate constraint, and §63 explains what it cost.

---

## 6. Evidence Tiers

Days 83 through 86 each built a tiering scheme appropriate to what was available. Day 87 has a different problem: everything here is a primary source, so tiering by *provenance* is useless. The useful axis is **what compelled the statement**.

| Tier | Description | What it means | Sources |
|---|---|---|---|
| **T1 — Audited** | Financial statements covered by an auditor's report | An independent firm has opined | [E], [F] financial statements |
| **T2 — Certified** | Statements inside a filing signed under Sections 302/906 | Officers are personally liable | [E], [F] MD&A, risk factors |
| **T3 — Reviewer-forced** | Text that exists because the staff asked for it | A professional reader demanded it | Responses to [A], [B1]–[B9] |
| **T4 — Rule-forced** | Text that exists because a specific rule requires it in this document type | A rule, not a person, demanded it | [H] projections, background |
| **T5 — Filed but unexamined** | Statements in a filing no one reviewed and no auditor covered | Liability only | [D] business section; 2025 S-1 |

The tiers are not a quality ranking. A T5 statement can be perfectly true. They are a **provenance ranking**: they say what force, if any, was applied to the statement before it reached the reader.

The central finding of this case study is that the most valuable disclosures in Tempus's public record sit in **T3 and T4** — and that T3 is discretionary, episodic, and now switched off.

---

## 7. Company Overview

Tempus AI, Inc. is a Chicago-headquartered precision-medicine company. Per its FY2025 Form 10-K [E], it operates **five** high-throughput diagnostic testing laboratories — in Chicago, Atlanta, Raleigh, Aliso Viejo, and Minneapolis — offering anatomical and molecular next-generation-sequencing tests across solid tumour, liquid biopsy, and hereditary cancer.

The business rests on a loop that is easy to state and hard to execute:

1. Run sequencing and pathology tests for clinicians, generating molecular and clinical data.
2. De-identify and structure that data into a multimodal database.
3. License the database, and analytical services on top of it, to pharmaceutical and biotechnology customers.
4. Train algorithms on the database and deploy them back into clinical care as billable or bundled diagnostics.

Steps 1 and 3 are where the revenue is. Step 4 is where the valuation argument is. The distance between those two sentences is most of what this case study is about.

---

## 8. Corporate History and Registration

The registration history is unusually informative and is worth stating precisely, because it sets up everything in §25 through §34.

| Date | Event | Source |
|---|---|---|
| 2021-09-01 | Draft Registration Statement on Form S-1 submitted confidentially, as **Tempus Labs, Inc.** | [A] |
| 2021-09-30 | First staff comment letter — **36** numbered comments | [A] |
| 2021-11-16 → 2023-11-21 | Nine further comment letters, through **Amendment No. 8** | [B1]–[B9] |
| 2024-06-11 | Acceleration requested by company and by underwriters | [J] |
| 2024-06-17 | Form 424B4 IPO prospectus filed; listed on Nasdaq as **TEM** | [D] |
| 2025-02-25 | Follow-on registration statement on Form S-1 filed | — |
| 2025-03-04 | Staff letter: **"we have not reviewed and will not review your registration statement"** | [C] |
| 2026-02-24 | Form 10-K for FY2025 | [E] |
| 2026-07-20 | Merger agreement with Personalis, Inc. | [G] |
| 2026-07-30 | Form 10-Q for Q2 2026 — first GAAP-positive quarter | [F] |
| 2026-08-31 | Form S-4 registration statement / proxy statement-prospectus | [H] |

Two facts from this table deserve to be stated as numbers rather than dates.

The company spent **1,020 days** — **2.79 years** — between submitting its first draft registration statement and pricing its IPO. The staff's review ran for **782 days** from the first comment letter to the last.

It is also worth noting the state of incorporation. Tempus is incorporated in **Nevada**, not Delaware. The merger structure in §36 is built around that fact.

---

## 9. The Platform

Per [E] and [D], the platform has four layers:

**Data ingestion.** Direct connections to provider systems plus the company's own laboratory output. The 2021 draft described "approximately 200 direct data connections"; the staff asked, in comment 17 of [A], whether Tempus paid for that data, what it gave in exchange, and what happened to the data if a provider stopped doing business with the company. That is a product question, asked by an accountant.

**The database.** De-identified multimodal records — molecular, clinical, and morphologic — updated over time with outcome and response data.

**Models.** AI techniques described in [E] as "neural networks, deep learning, large language models, and other statistical learning techniques." Some are trained for research use; some are developed into clinical-grade algorithmic tests ("Algos") and deployed into routine care.

**Applications.** Customer-facing software — Hub for providers, Lens for research customers — plus the Insights and Therapies data products.

As of 31 December 2025, per [E], more than **123,000** molecular oncology Algos had been ordered alongside the company's genomic assays. Across **5** laboratories that is a mean of **24,600.00** Algos per lab, though the filing does not break the figure down by site and the mean should be read as arithmetic, not as a site-level fact. Most Algos are not separately billed.

---

## 10. Product Lines

The reporting structure changed between the draft registration statement and the current filings, which is itself a disclosure artefact worth noting.

In the 2021 draft, the company described **three** product lines: Genomics, Data, and Algos. Comment 4 of [A] observed that "the substantial majority of your total revenue is generated from genomics and the revenue from Algo has not been significant," and asked the company to disclose the percentage of revenue from each of the three.

By FY2025 [E], the company reports **two** segments: **Diagnostics** and **Data and applications**. Algos no longer appear as a separate revenue line at all. They are, per [E], largely bundled into the xR assay and not billed separately.

This is not concealment — bundling a feature into a test is an ordinary product decision, and the filing says so plainly. But it is an example of a reporting structure moving in a direction that makes a specific question harder to ask. In 2021 a reader could ask "how much revenue do the algorithms produce?" and the staff could demand an answer. In 2026 the question has no line to point at.

---

## 11. Business Model

| Element | Mechanism | Who pays | Evidence quality |
|---|---|---|---|
| **Clinical diagnostics** | Per-test billing to payers, health systems, patients | Medicare, commercial payers, institutions | T1 — audited revenue |
| **Data licensing (Insights)** | Multi-year subscriptions and per-file licences | Pharmaceutical and biotech customers | T1 — audited revenue |
| **Clinical trial matching (Therapies)** | Fee on notification or enrolment | Trial sponsors | T2 — described, not quantified |
| **Algos** | Bundled into assays; mostly not separately billed | — | **No revenue line** |
| **Applications** | Access fees where integration or customisation is required | Providers, researchers | T2 — described, not quantified |

The model's defining feature is that the diagnostics business is the **acquisition channel for the data business**. Tests generate data; data is licensed. This is a genuinely elegant structure and it is the reason the company can run a low-margin clinical laboratory operation as a strategic asset rather than as a cost centre.

It also creates the reimbursement exposure that the staff probed hardest in 2021. Comments 15 and 16 of [A] asked about revenue recognition when Tempus received payment on "approximately 50% and 48%" of its clinical oncology NGS tests in 2019 and 2020, and about the fact that all claims submitted to the local Medicare Administrative Contractor for NGS oncology tests performed in the Chicago lab after 25 March 2021 had been **denied** — for testing that represented 30% of clinical volume. These are the two sharpest questions in the entire correspondence, and they are accounting questions that happen to be the most important product questions in the file.

---

## 12. Revenue Composition

From [E], with FY2024 comparatives ($ millions):

| Segment | FY2024 | FY2025 | Growth | FY2025 share |
|---|---:|---:|---:|---:|
| Diagnostics | 451.749 | 955.381 | **+111.48%** | **75.12%** |
| Data and applications | 241.649 | 316.408 | **+30.94%** | **24.88%** |
| **Total net revenue** | **693.398** | **1,271.789** | **+83.41%** | **100.00%** |

The gap between the two growth rates is **80.55 percentage points**, and it is the single most important thing on this table — because a large part of it is not organic.

In February 2025 Tempus acquired **Ambry Genetics Corporation**, a hereditary cancer screening business [E]. The FY2025 10-K also names acquisitions of Paige.AI, Inc. and Deep 6 AI, Inc. among the transactions whose expected benefits the company may fail to realise.

The 10-K **does not disclose an organic-versus-inorganic split** for Diagnostics revenue growth. That is recorded here as a fact about the filing, not as a criticism: no rule requires it, and no reviewer asked for it. It is the second entry in the disclosure ledger at §43, and it is one of the two rows where nothing compelled an answer and no answer was given.

Read carefully, the table says: the segment that grew fastest is the one whose growth we cannot decompose, and the segment we can decompose grew at roughly a third of the rate.

---

## 13. Financial Performance FY2023–FY2025

From [I] and [E], all figures $ millions:

| Metric | FY2023 | FY2024 | FY2025 |
|---|---:|---:|---:|
| Revenue | 531.822 | 693.398 | 1,271.789 |
| Revenue growth | — | +30.38% | **+83.41%** |
| Operating loss | (196.083) | (691.082) | (252.872) |
| Net loss | (214.118) | (705.809) | (245.028) |
| Net margin | — | **-101.79%** | **-19.27%** |
| R&D expense | 90.343 | 149.325 | 172.924 |
| R&D as % of revenue | — | **21.54%** | **13.60%** |
| Cash and equivalents | 165.767 | 340.954 | 604.787 |

Five observations, each of which is arithmetic rather than interpretation:

1. Revenue growth **accelerated by 53.03 percentage points** between FY2024 and FY2025 — from 30.38% to 83.41%. The acceleration is inorganic in unknown proportion (§12).
2. Net margin improved by **82.52 percentage points**, from -101.79% to -19.27%. FY2024 contains the IPO-year stock-compensation charge that makes the comparison flattering.
3. **R&D intensity fell by 7.94 percentage points.** R&D grew **15.80%** while revenue grew 83.41%. For a company whose entire strategic argument rests on algorithmic capability, R&D falling from roughly a fifth to roughly an eighth of revenue is the most interesting line on this table.
4. Cash grew **77.38%** to $604.787M.
5. Cumulative net loss across the three disclosed years is **$(1,164.96)M**. There is **no profitable full year** anywhere in the disclosed record.

---

## 14. Q2 2026: The First Profitable Quarter

From [F] and [I], $ millions:

| Metric | Q2 2025 | Q2 2026 | Change |
|---|---:|---:|---:|
| Revenue | 314.635 | 382.486 | **+21.56%** |
| Net income / (loss) | (42.843) | **5.642** | **+$48.49M swing** |
| Net margin | -13.62% | **+1.48%** | +15.09pp |
| R&D expense | 41.619 | 52.637 | **+26.47%** |
| R&D as % of revenue | 13.23% | **13.76%** | +0.53pp |

This is the first GAAP-positive quarter in the disclosed record, and it deserves to be stated without inflation. Net margin is **1.48%**. A single quarter at 1.48% is a threshold crossing, not a profitability trend, and the company's own annual record (§13) shows nothing comparable.

Two things are worth pulling out.

First, **the quarterly trend reverses the annual one**. Across FY2024→FY2025, R&D grew far slower than revenue. In Q2 2026, R&D grew **26.47%** against revenue growth of 21.56% — R&D grew *faster* than revenue for the first time in the comparison. Whether that is a durable reinvestment decision or a quarter's noise cannot be determined from two data points, and this case study does not claim to know.

Second, annualising Q2 revenue gives **$1,529.94M**, or **120.30%** of FY2025 revenue. That is an illustrative scale check, not guidance, not a forecast, and not something the company has said.

---

## 15. Unit Economics and What Isn't Disclosed

This section exists to be short, because the honest answer is short.

Per-test economics are not disclosed. Cost per sequencing run is not disclosed. Data-licence contract values are not disclosed at the contract level — the 2021 draft mentioned $172 million of remaining contract value on Insights agreements, a figure the staff probed in comment 24 of [A], but no equivalent figure appears in [E]. Customer counts per product line are not disclosed, though comment 2 of [B5] asked for exactly that in August 2022. Algo revenue is not disclosed because Algos have no revenue line (§10).

A product manager reading the FY2025 10-K can determine what Tempus **earns**. They cannot determine what it **costs Tempus to earn it**, at any level below the segment.

This is entirely lawful. Segment reporting is a rule-driven minimum, and Tempus meets it. But it is the baseline against which §24 should be read: the ordinary state of a public filing is that it answers the questions the rules name and no others.

---

## 16. Problem Statement

Stated from the evidence rather than from the company's marketing:

> A treating oncologist choosing therapy for a patient with advanced cancer must integrate molecular profiling, clinical history, and current evidence, under time pressure, with tools that do not talk to each other. A pharmaceutical researcher designing a trial must find patients matching a molecular profile across a fragmented provider landscape. Both problems are, at root, the same problem: **the data required to make the decision exists, but not in one place, not in one structure, and not at the moment of decision.**

Tempus's answer is to become that place. The sequencing business creates the structured record; the software delivers it at the point of care; the data business sells the aggregate back to the industry that funds drug development.

The problem is real, large, and not seriously disputed. What this case study examines is not whether the problem is real but **what the public record permits a reader to conclude about how well it is being solved.**

---

## 17. Jobs to Be Done

| Job | Who hires the product | Current alternative | What "done well" looks like |
|---|---|---|---|
| "Tell me what is driving this patient's tumour" | Community oncologist | Send-out to a reference lab, wait | Actionable report inside the treatment window |
| "Find me patients for this trial arm" | Trial sponsor / CRO | Manual chart review across sites | Pre-matched, consented cohort |
| "Show me real-world outcomes for this molecular subgroup" | Pharma researcher | Purchase claims data, infer | Linked molecular-clinical-outcome records |
| "Tell me where this tumour came from" | Pathologist | Immunohistochemistry panel, sometimes inconclusive | A prediction with a stated error rate |
| "Tell me whether to own this company" | Institutional investor | Read the filings | Filings that answer the material questions |

The fourth and fifth rows are the ones this case study can actually evaluate, because both have a documented public answer — and in both cases the answer is that the *process* is disclosed and the *result* is not.

---

## 18. User Personas

Three personas are developed below. Each is constructed from what the filings themselves say about who buys, uses, or reads, and each is labelled with the evidentiary basis for that construction. None of them is a synthesised quote, a fabricated interview, or a composite with invented biographical detail — those are the standard failure modes of PM persona work and this series does not use them.

---

## 19. Persona 1: The Community Oncologist

**Basis:** [E] and [D] business sections; comment 11 of [A] (test volume); comment 2 of [B5] (retention among oncologists ordering more than five tests).

**Context.** Treats a broad mix of tumour types rather than sub-specialising. Orders molecular profiling when therapy selection is genuinely open. Is not a genomics specialist and will not interrogate a model's architecture.

**What they need.** A report inside the clinical decision window, in a format that survives being read in four minutes between appointments, with enough provenance that they can defend the decision later.

**What the record tells us about them.** The 2022 correspondence [B5] reveals that Tempus had told the staff its 12-month retention rate for oncologists ordering more than five tests was 92% through December 2021 — and that the staff pushed back, asking the company to disclose **how many oncologists** that rate was measured over, how it was measured, and over what period. That is a textbook metric critique: a retention rate without a denominator is a claim, not a measurement.

**What this persona cannot learn from current filings.** Whether the Algo attached to their report has a published error rate. It does not (§31).

---

## 20. Persona 2: The Pharma Data Buyer

**Basis:** [E] Data and applications segment; comments 23–25 of [A] on performance obligations; comment 1 of [B8] on data partnerships.

**Context.** Buys de-identified multimodal data under multi-year subscriptions or per-file licences. Cares about cohort size, linkage depth, outcome completeness, and refresh cadence.

**What they need.** Certainty that the cohort they licensed will still be the cohort they licensed in eighteen months, and clarity on what "updates" means contractually.

**What the record tells us about them.** The staff spent three separate comments in [A] (23, 24, 25) on whether analytical services and licence updates were **distinct performance obligations** under ASC 606. Underneath the accounting is a product question: is Tempus selling a dataset or a subscription to a living dataset? The answer determines what the buyer owns.

Comment 1 of [B8], in May 2023, went further — asking Tempus to discuss the **material terms of its data partnerships, including financial terms**, after the draft claimed partnerships with approximately 90% of the largest public pharmaceutical companies. A partnership count is a marketing metric. Material terms are a business model.

---

## 21. Persona 3: The Institutional Investor

**Basis:** [E], [F], [H]; the entire comment-letter record.

**Context.** Holds or is considering TEM. Reads risk factors as information rather than as legal furniture. Is, in the strict sense, the person the disclosure system exists to serve.

**What they need.** Enough to distinguish between a company whose algorithms work and a company whose algorithms are described well.

**What the record gives them.** Audited financials (T1). Certified MD&A (T2). A business section that was heavily reviewed in 2021–2023 (T3) and has not been reviewed since (§34). And, for a few months in 2026, an S-4 containing fifteen years of forecasts that Tempus states it would never publish voluntarily (T4, §41).

**This persona is the protagonist of §24 onward.**

---

## 22. User Journey: Ordering a Test

```
  Clinician                 Tempus                      Payer
     |                         |                          |
 [1] | order + specimen  ----->|                          |
     |                         | [2] sequencing, one of 5 labs
     |                         |     (Chicago/Atlanta/Raleigh/
     |                         |      Aliso Viejo/Minneapolis)
     |                         |
     |                         | [3] variant calling, curation
     |                         | [4] Algos run alongside assay
     |                         |     (>123,000 ordered to date;
     |                         |      mostly NOT separately billed)
     |                         |
 [5] |<----- report ---------- |
     |       + raw files       |
     |                         | [6] claim submitted ---->|
     |                         |                          |
     |                         |<-- pay / DENY -----------|
     |                         |        ^
     |                         |        |
     |                         |   In 2021 ALL Chicago-lab NGS
     |                         |   oncology claims to the local
     |                         |   MAC after 25 Mar were denied.
     |                         |   That testing was 30% of
     |                         |   clinical volume. [A] comment 16
     |                         |
     |                         | [7] de-identified record joins
     |                         |     the multimodal database
     |                         |          |
     |                         |          v
     |                         |     licensed to pharma (Persona 2)
```

Step 4 is where the strategic value is claimed. Step 6 is where the cash is. Step 7 is where the moat is. The staff's 2021 questions clustered on steps 6 and 7 — the two the company had the strongest incentive to describe loosely.

---

## 23. User Journey: Reading a Disclosure

This is the journey the case study is actually about, and it is worth drawing because product managers rarely map it.

```
  Reader                      Filing                    Force applied
    |                            |                            |
[1] | opens 10-K ------------->  |                            |
    |                            | financial statements  <--- AUDITOR (T1)
    |                            | MD&A, risk factors    <--- OFFICER CERT (T2)
    |                            | business section      <--- ??? 
    |                            |                            |
[2] | reads risk factor on       |                            |
    | peer-reviewed publications |                            |
    |                            |                            |
    |    2021 draft:  "29 of 41 self-authored"  <--- STAFF COMMENT 7 (T3)
    |    2024 IPO:    "126 ... including 93"    <--- carried forward (T3)
    |    2025 10-K:   "over 800"  + NO NUMERATOR <--- nothing (T5)
    |                            |                            |
[3] | the CONFLICT SENTENCE survives verbatim in all three     |
    | the NUMBER survives in two of three                      |
    |                            |                            |
[4] | reader concludes: ??? ---->  cannot compute the ratio    |
```

The journey degrades at step 2, and the reader cannot tell that it has degraded, because step 3 preserves the *appearance* of the disclosure. That is the finding, and the next eleven sections establish it.

---

## 24. The Central Question

> **Does the obligation to disclose produce better evidence than the choice to disclose?**

Days 83–86 established what choice produces. To summarise those four days in one line each:

- **Day 83 (OpenEvidence):** five headline claims, **0** independently confirmed — a **0.00%** confirmation rate.
- **Day 84 (Abridge):** an independent NIH-funded randomised trial produced note-quality scores the vendor's own two peer-reviewed studies did not report at all.
- **Day 85 (Eka Care):** a national programme proxy and an independent field study converged to within **1.59 percentage points** — the only clean convergence in the arc, and it required a government dashboard to produce it.
- **Day 86 (Hippocratic AI):** a marketing claim spanning 115 million interactions rested on a preprint covering 307,000 calls — **0.27%** coverage.

Against that baseline, Day 87 asks what happens when a company **cannot** choose.

The answer has three parts, and they are in tension:

1. **Obligation produced evidence that choice never produced anywhere in this arc** (§25–§30, §41).
2. **Obligation produced a description of process, not a measurement of result** (§31–§33).
3. **Obligation is discretionary, episodic, and reversible — and when it stopped, the evidence decayed while its wrapper survived** (§28, §34).

---

## 25. The Review Record

Ten comment letters. Sixty-six numbered comments. Here is the distribution, which is itself the story:

| Letter | Date | Subject | Comments |
|---|---|---|---:|
| [A] | 2021-09-30 | Draft Registration Statement | **36** |
| [B1] | 2021-11-16 | Amendment No. 1 | 6 |
| [B2] | 2021-11-29 | Amendment No. 1 | 1 |
| [B3] | 2021-12-17 | Amendment No. 2 | 3 |
| [B4] | 2022-05-11 | Amendment No. 3 | 7 |
| [B5] | 2022-08-03 | Response Letter No. 3 | 5 |
| [B6] | 2022-10-27 | Amendment No. 4 | 1 |
| [B7] | 2023-01-27 | Amendment No. 5 | 1 |
| [B8] | 2023-05-05 | Amendment No. 6 | 3 |
| [B9] | 2023-11-21 | Amendment No. 8 | 3 |
| | | **Total** | **66** |

**A counting note.** Numbered items that are financial-statement note captions — "9. Stock-Based Compensation, page F-29" and similar — are **excluded**. A naive regular expression over these documents returns a higher count because it cannot distinguish a comment number from a note heading. This distinction was made by reading each letter in full, and it changes the total.

The distribution is heavily front-loaded. The first letter carries **54.55%** of all comments on its own. The mean across all ten letters is **6.60** comments; excluding the first letter it falls to **3.33**. Over the **782-day** review the staff raised **30.83** comments per year.

That shape is normal and it is also instructive: **the overwhelming majority of what a reviewer extracts, they extract on first contact.** A company that never reaches first contact is never extracted from at all — which is the condition Days 83 through 86 examined.

---

## 26. The First Comment Letter

The 30 September 2021 letter [A] is the most valuable single document in this case study. Thirty-six comments, issued **29 days** after submission, spanning the cover page, the summary, risk factors, MD&A, the business section, the financial statements, and the exhibit list.

A selection, chosen to show the range:

- **Comment 2:** "Your disclosure on page 9 indicating that you have **two** algorithmic tests appears inconsistent with your disclosure elsewhere on page 30 indicating that you have **three** algorithmic tests."
- **Comment 5:** Instructs the company to remove the phrase "gross profit" from its cohort analyses, because it presents no gross profit measure on the face of its GAAP income statement.
- **Comment 10:** Asks Tempus to disclose **what percentage of his time** the CEO devotes to the company, given his roles at Pathos AI and Lightbank.
- **Comment 16:** The Medicare denial comment (§11).
- **Comment 28:** Asks how the company distinguishes expenses classified as "Research and Development" from those classified as "Technology" — and whether excluding technology costs from cost of revenues complies with Rule 5-03(b)(2).
- **Comment 36:** Asks for copies of **all written communications** presented to potential investors in reliance on Section 5(d).

Comment 2 is the one worth dwelling on. A regulator caught a company contradicting itself about **how many products it had**, twenty-one pages apart, in its own registration statement. That is not an accounting subtlety. It is the kind of error that survives indefinitely in any document nobody is paid to read adversarially.

And comment 5 is a small masterpiece of disclosure discipline: you may not use the words "gross profit" in a narrative exhibit when your own income statement does not compute it. The staff is policing the gap between what a chart implies and what the audited statements support — which is precisely the gap that every deck in this series' 86 prior case studies has lived in.

---

## 27. Comment 7: Self-Authorship

Comment 7 of [A], reproduced in full:

> "You disclose on page 31 that mentions in peer-reviewed journal publications are a good indicator of success. We also note your disclosure on page 163 indicating that you have self-authored 29 of 41 total articles in which you have been mentioned. Please revise your risk factor to include possible conflicts of interest related to such self-publications."

Read what that comment does.

The company had made a claim of the form *our products are validated by the scientific literature*, and had supported it with a publication count. The staff noticed that the same document, 132 pages later, disclosed that **29 of those 41 articles were written by Tempus itself** — and required the company to say so, in the risk factors, as a conflict of interest.

**29 of 41 is 70.73%.**

Days 83 through 86 of this series spent four days attempting, from the outside, to distinguish vendor-authored evidence from independent evidence:

- Day 83 found that a company's headline claims had **0** independent confirmations.
- Day 84 found that a vendor's own two peer-reviewed studies reported **0** note-accuracy metrics, and that the only independent scoring came from a trial the vendor did not run.
- Day 86 found that a safety claim spanning 115 million interactions rested on the company's own preprint covering **0.27%** of that volume.

Each of those took a day of work with court dockets, PubMed, preprint servers, and registry data. In 2021, a staff attorney and a senior staff accountant extracted the equivalent number from Tempus **in a single sentence**, and made the company print it.

That is the strongest evidence in this entire 90-day series for the proposition that obligation beats choice.

---

## 28. The Number's Life Cycle

And then it goes away.

| Filing | Date | Total articles | Self-authored | Share | Under review? |
|---|---|---:|---:|---:|---|
| Draft S-1 (per [A]) | 2021-09 | 41 | **29** | **70.73%** | **Yes** |
| 424B4 IPO prospectus [D] | 2024-06 | 126 | **93** | **73.81%** | **Yes** |
| Form 10-K FY2025 [E] | 2026-02 | **over 800** | **not disclosed** | **not computable** | **No** |

The [D] text reads: "As of March 31, 2024, our products have been mentioned in 126 peer-reviewed articles published in major journals, **including 93 that were Tempus-authored**."

The [E] text reads: "As of December 31, 2025, our products have been mentioned in **over 800** peer-reviewed articles published in major journals."

Then, in both documents, the identical next sentence: "In addition, self-authored journal publications that mention our products may present an actual, potential or perceived conflict of interest and, therefore, the number of publications in which our products are mentioned may not be indicative of the level of acceptance of our products."

**The conflict-of-interest sentence survived. The number did not.**

Three arithmetic facts follow, and each is computed in `verify.py`:

1. **The self-authorship share rose while it was being disclosed** — from 70.73% to 73.81%, an increase of **3.08 percentage points** (**3.078pp** at three decimals). It did not stop being disclosed because it had become unremarkable.
2. The article count grew **6.35×** between the two disclosures and **19.51×** between the first disclosure and FY2025. The denominator was reported enthusiastically at every step.
3. **674** articles have been added to the disclosed total since the last time the numerator was published — leaving **15.75%** of the current evidence base as the portion for which the split is on the record.

If the 2024 rate had held, the FY2025 numerator would be **590.48**. That figure is arithmetic on a counterfactual and appears here **only** so that the size of the unknown is legible. It is not a fact about Tempus, the company has not said it, and nothing in this case study relies on it.

---

## 29. What the Ratio Meant

Why does this specific number matter enough to build a case study around?

Because the company itself said it mattered. The risk factor's own logic, in all three versions, is: *mentions in peer-reviewed publications are a good barometer for general acceptance of our products.* The publication count is offered as **evidence of external validation**.

A publication count is only evidence of external validation to the extent the publications are external.

At 70.73% self-authored, the 2021 figure was not primarily a measure of external acceptance — it was primarily a measure of the company's own publishing output. At 73.81% in 2024 it was slightly less so. Above 800 articles, with no numerator, the reader has a number that **looks like** a validation metric and cannot be used as one.

This is the same structural failure this series documented on Day 84, and the comparison is exact. On Day 84, a vendor's marketing rested on a publication record in which the vendor's own two peer-reviewed studies reported **zero** note-accuracy metrics, while an independent trial did the actual measuring. The difference on Day 87 is that Tempus **was made to disclose the ratio**, twice, and the record shows precisely when and why it stopped.

Days 83–86 could not see inside. Day 87 can — and what is inside is that the disclosure existed exactly as long as someone was reading.

---

## 30. The AI Validation Comment

On 21 November 2023, reviewing Amendment No. 8, the staff issued comment 1 of [B9]:

> "We note that your proprietary software employs AI techniques such as neural networks, deep learning, and other statistical techniques. Please explain **how you developed and validated** your artificial intelligence ("AI") model. In the explanation, please include the **data quality and robustness of the relationship predicted by the model over time**, the **experience of the personnel** that developed the model, **when the model was developed**, and **how long the model has been used in a clinical setting**."

This is, as far as this series has found, the most precise public demand for AI evidence made of any company in the Day 83–87 cohort. It contains **six** distinct asks.

Tempus answered with a paragraph about its tumour origin ("TO") algorithm, which appears in [D] and survives verbatim in [E]:

> "One example of an AI model whose results are available within Hub, and which illustrates a typical development and validation process for our AI models, is our tumor origin, or TO, algorithm... We began developing our TO algorithm in 2019, and it was first deployed in a clinical setting in 2021... we explored distinct model architectures (logistic regression, random forests and neural networks) and feature selection methods, and we utilized multiple cross validation techniques using both our own and independent third-party datasets. After its launch, we continue to monitor the performance of the TO algorithm by using advanced statistical methods to detect potential model drift or degradation over time. Each TO prediction is reviewed by our board certified pathologists for consistency with underlying data..."

Scoring the answer against the six asks:

| # | The staff asked for | Addressed? | Where |
|---|---|:---:|---|
| 1 | How the model was developed | **Yes** | 3 architectures explored, feature selection described |
| 2 | How the model was validated | **Yes** | "multiple cross validation techniques", own + third-party datasets |
| 3 | Data quality and robustness over time | **Yes** | drift/degradation monitoring, pathologist review |
| 4 | **Experience of the personnel** | **No** | not addressed anywhere in [D] or [E] |
| 5 | When the model was developed | **Yes** | began 2019 |
| 6 | How long used clinically | **Yes** | first deployed 2021 |

**5 of 6 — 83.33% coverage.** One ask, personnel experience, is never addressed.

This is a genuinely good disclosure by the standards of this arc, and it should be credited as such. It is more than OpenEvidence, Abridge, Eka Care, or Hippocratic AI published about any model, in any document, voluntarily. The TO algorithm has a documented development start (**2019**), a documented clinical deployment (**2021**), a **2-year** gap between them, and **4** years of clinical use as at FY2025.

And it is still missing the only thing that matters.

---

## 31. Process vs Performance

**The TO algorithm's accuracy is not disclosed. Anywhere.**

Not in the IPO prospectus. Not in the FY2025 10-K. Not in a sensitivity, a specificity, a concordance rate, an AUC, a confusion matrix, or a single percentage of any kind. `verify.py` records the count of TO performance metrics in [E] as **0**.

What is disclosed is an exemplary account of *method*: which architectures were explored, that cross-validation was used, that drift is monitored, that a pathologist reviews each prediction. A reader finishes the paragraph knowing that Tempus developed the model the way a competent team would develop a model.

They do not know whether it works.

This is the sharpest distinction in the case study, and it generalises well beyond Tempus:

> **A description of process is not a measurement of result. Disclosure regimes are much better at compelling the first than the second.**

The staff asked "how you developed and validated." The company explained how it developed and validated. Both sides discharged their obligations completely. The reader still cannot tell you the error rate of an algorithm that has been running in clinical care since 2021 and has been ordered more than 123,000 times.

No rule was broken. That is the point.

---

## 32. What Assays Disclose That Algorithms Don't

The contrast inside the same document makes this unarguable.

Tempus's **assays** carry numbers. From [D], on the xF liquid biopsy assay: at 0.5% variant allele frequency and 30ng of DNA, sensitivity greater than 99.9% for SNVs, 98.8% for indels, greater than 99.9% for CNVs, 97.4% for rearrangements and fusions; specificity greater than 99.9% for SNVs, indels, and fusions, and 96.2% for CNVs. On the xT assay: sensitivities above 98% for SNVs, above 92% for rearrangements and fusions, above 92% for CNVs and indels, and 99.9% for MSI. `verify.py` counts **7** distinct analytical validation metrics for the assays.

| | Assays | Algorithms (Algos) |
|---|---|---|
| Development process described | Partially | **Extensively** |
| Sensitivity disclosed | **Yes** | **No** |
| Specificity disclosed | **Yes** | **No** |
| Concordance to a comparator | **Yes** (Roche AVENIO) | **No** |
| Regulatory framework | CLIA analytical validation | LDT / no equivalent requirement |
| Count of quantitative metrics | **7** | **0** |

The explanation is regulatory, not cultural. CLIA requires analytical validation — accuracy, precision, specificity, sensitivity, reference range — for laboratory-developed tests. A high-complexity lab **must** generate those numbers. There is no equivalent compulsion for an algorithm bundled into an assay and not separately billed.

**So the numbers exist exactly where a rule requires them, and nowhere else.** That sentence is the case study in miniature, and it is confirmed rather than contradicted by the fact that the same company, in the same document, does both.

---

## 33. The Glossary That Wasn't

The 21 November 2023 letter contained three AI-related comments. Comment 3:

> "Given the nature of your business, please **consider including** definitions of 'AI,' 'generative AI,' 'deep learning,' 'large language models,' 'neural networks,' and any other industry-specific terminology."

The FY2025 10-K contains **no glossary and no definitions of these terms**. It uses all of them.

Comment 2 of the same letter asked whether Tempus intended to develop proprietary technology, use open source, or license — and to revise risk disclosure accordingly. That one **was** complied with: [E] carries a risk factor addressing open-source and third-party licensed AI technologies, including the observation that such developers "may not adhere to the same or similar standards that we adhere to in the development, validation, training and maintenance of AI models."

So of three AI comments in the final letter, **2 were complied with — 66.67%**.

The one that was not is the one phrased "please consider." Comments 1 and 2 said "please explain" and "please disclose." Comment 3 said "please consider," and the company considered it.

That is not evasion; it is the system operating exactly as designed. But it isolates the mechanism cleanly: **compliance tracked the grammatical force of the request, not its usefulness to a reader.** A glossary would have cost almost nothing and helped every non-specialist holder of the stock. It was optional, so it did not happen.

---

## 34. March 2025: "We Will Not Review"

On 25 February 2025 Tempus filed a follow-on registration statement on Form S-1. On 4 March 2025 the staff replied [C]:

> "This is to advise you that we have **not reviewed and will not review** your registration statement.
>
> Please refer to Rules 460 and 461 regarding requests for acceleration. We remind you that **the company and its management are responsible for the accuracy and adequacy of their disclosures, notwithstanding any review, comments, action or absence of action by the staff.**"

Seven days from filing to no-review. **469 days** after the last substantive comment.

Two things must be said about this letter, and they point in opposite directions.

**First**, this is routine. The staff selectively reviews registration statements; a seasoned issuer filing a follow-on will often receive no review, and this is a resource-allocation decision, not a judgement about Tempus. Nothing here suggests the staff found anything wrong, because the staff did not look.

**Second**, and this is why the letter is in this case study: **it is the SEC telling you, in writing, not to treat SEC review as verification.** The second paragraph is a disclaimer, and it is unambiguous. Responsibility for accuracy is the company's, "notwithstanding any review, comments, action or **absence of action** by the staff."

Every product manager who has ever thought *it's in their 10-K, so it must be checked* should read that sentence twice. `verify.py` records, as negative controls: the SEC did not verify Tempus's disclosures; the SEC did not endorse any Tempus claim; the SEC did not review the 2025 follow-on. All three are **False**, asserted programmatically, so that nothing in these deliverables can quietly imply otherwise.

And it completes the timeline. Sustained review 2021–2023, producing 66 comments including the self-authorship ratio and the AI validation demand. No review from 2025. And in the FY2025 10-K, filed under no review at all, **the self-authorship numerator is gone.**

The causal claim is not made here. A drafting decision was taken inside a company and this case study has no visibility into it. What the record supports is the correlation, stated exactly: **the number was disclosed in both documents prepared under active staff review and absent from the first annual report prepared without it.**

---

## 35. The Personalis Acquisition

On 20 July 2026, Tempus entered into an Agreement and Plan of Merger with **Personalis, Inc.**, a Delaware corporation [G].

There is a detail here that the 2024 prospectus makes delicious. In November 2023, per [D], Tempus entered into a **Commercialization and Reference Laboratory Agreement with Personalis**, under which Tempus began marketing Personalis' Personal Dx test in the United States in non-small cell lung cancer and breast cancer, with Personalis performing the tests and billing the patients or payers.

**Three years** from reference-lab partner to acquisition target. The IPO prospectus named the company Tempus would eventually buy, in a paragraph about someone else's test.

This matters for the case study because it means the S-4 [H] — filed **42 days** after the merger agreement — is not a document about a stranger. It is a document in which two companies that have been commercially entangled since 2023 must both open their forecasts to the same reader.

---

## 36. Merger Mechanics

From [G]:

| Term | Value |
|---|---|
| Structure | Two-step: Merger Sub I (Delaware corp) into Personalis; then survivor into Merger Sub II (Nevada LLC) |
| Intended tax treatment | Reorganisation under Section 368(a) |
| Per-share cash consideration | **$16.25** |
| Floor price | **$48.42** |
| Exchange ratio at or below floor | **0.3356** |
| Maximum cash election | **50.00%** of outstanding Personalis shares |

The two legs are calibrated: **$48.42 × 0.3356 = $16.25**. The stock consideration at the floor price is worth exactly the cash consideration, to the cent. That is deliberate structuring — below the floor, a holder is indifferent between legs, which is what makes a partial cash election workable without creating an arbitrage between electing holders.

The two-step structure exists because Tempus is a **Nevada** corporation acquiring a **Delaware** one (§8). Merger Sub I is Delaware so the first merger happens under the DGCL, with appraisal rights for dissenting Personalis stockholders; the survivor then merges into a Nevada LLC. The form follows the states of incorporation, and the states of incorporation were chosen years before anyone contemplated this deal.

---

## 37. Two Managements, One Company

Now the part of the S-4 that makes Day 87 work.

Because the financial advisors relied on management forecasts in rendering fairness opinions, those forecasts must be summarised in the proxy statement-prospectus. The consequence is that [H] prints, **in one document**, two different managements' revenue projections for **the same company**.

And — this is the critical detail that removes any ambiguity — footnote (2) to the Personalis projections table records exactly what was handed over:

> "Revenue projections through 2030, based on the Preliminary Projections, were provided to Tempus in connection with due diligence. Revenue projections as provided to Tempus for (i) 2026 was $90 million, (ii) 2027 was $143 million, (iii) 2028 was $272 million, (iv) 2029 was $457 million, and (v) 2030 was $758 million."

Those five figures are **identical** to the first five years of Personalis' final Projections. Personalis' revenue view did not change between its preliminary and final forecasts. So this is not a comparison of stale numbers against fresh ones.

**Tempus received Personalis' own revenue forecast, and wrote down a lower number for every single overlapping year.**

Both sides also state, in nearly identical language, that neither company publishes long-range forecasts as a matter of course. Tempus: "Other than full year financial guidance, Tempus does not, as a matter of course, publicly disclose long-range forecasts or internal projections as to future performance." Personalis says the same of itself.

These numbers exist in public **only** because a merger rule put them there.

---

## 38. The Markdown Curve

Revenue, $ millions, as printed in [H]:

| Year | Personalis' own view (given to Tempus) | Tempus' view of Personalis | Tempus as % of Personalis | Markdown |
|---|---:|---:|---:|---:|
| 2026E | 90 | 79 | **87.78%** | **-12.22%** |
| 2027E | 143 | 115 | **80.42%** | -19.58% |
| 2028E | 272 | 172 | **63.24%** | -36.76% |
| 2029E | 457 | 242 | **52.95%** | -47.05% |
| 2030E | 758 | 333 | **43.93%** | **-56.07%** |
| **Cumulative** | **1,720** | **941** | **54.71%** | **$(779)M** |

```
 % of Personalis' own forecast that Tempus underwrote
 100 |
     |  87.78
  90 |   *
     |        80.42
  80 |          *
     |
  70 |
     |               63.24
  60 |                 *
     |                       52.95
  50 |                         *
     |                               43.93
  40 |                                 *
     +----+----+----+----+----+----+----+---
       2026 2027  2028  2029  2030
```

**The markdown widens every single year.** That monotonicity is asserted programmatically in `verify.py`, not eyeballed from the chart.

Expressed as compound growth over the overlap: Personalis' own forecast implies a **70.36%** CAGR from 2026 to 2030. Tempus underwrote **43.29%** — a gap of **27.07 percentage points**.

Over the five overlapping years, Tempus underwrote **54.71%** of the revenue Personalis' management projected for itself — a cumulative difference of **$779 million**.

There is an honest caveat and it must be stated. Tempus' projections are explicitly for Personalis **as a wholly owned subsidiary of Tempus**, and [H] warns they "do not reflect, and should not be interpreted to represent or be relied upon as, estimates of the standalone financial performance of Personalis." Integration changes a business. Some of this gap is a different asset, not a different opinion.

But not all of it. A 56.07% markdown by year five, applied to figures received in diligence from the company being bought, is a substantive disagreement about how fast that business grows. And the acquirer is the party whose money is at risk.

---

## 39. The Crossover

Extend both curves to their full published horizons and something unexpected happens.

| Year | Personalis (own, to 2039) | Tempus (to 2040) | Relationship |
|---|---:|---:|---|
| 2030E | 758 | 333 | Tempus 43.93% |
| 2035E | 2,539 | 1,484 | Tempus below |
| 2038E | 3,302 | 2,963 | Tempus **10.27% below** |
| **2039E** | **3,467** | **3,539** | **Tempus 2.08% ABOVE** |
| 2040E | — | 4,109 | no comparator |

**The crossover year is 2039.**

A first read of the two tables suggests 2038; it is not. `verify.py` locates the crossover with a loop rather than by assertion, and the loop returns 2039 — Tempus is still **10.27%** below in 2038. This is precisely the kind of error that a gate written before the prose catches and a gate written after the prose ratifies.

The shape is coherent, and it tells you what Tempus thinks it is buying. The acquirer believes the business ramps **more slowly** and **for longer** — a lower near-term trajectory that does not decelerate, eventually overtaking a forecast that front-loads its growth and then flattens. Personalis' own curve grows 70.36% compounded to 2030 and then decays toward single digits by the late 2030s. Tempus' curve never has the early spike and never needs the late fade.

Two managements, the same asset, the same document, opposite growth shapes. In no other case study in this arc has an outside reader been able to see anything remotely like this — and here it is, printed, because Regulation M-A required it.

---

## 40. Profitability Timing Disagreement

The same disagreement appears in the profitability line, with a caveat that must be carried.

Personalis' own Projections show Adj. EBITDA **excluding** stock-based compensation turning positive in **2029E** (at $17M, after $(45)M in 2028E). Tempus' projections for Personalis show Adj. EBITDA **including** SBC reaching exactly **0** in **2030E**, and positive thereafter.

**The definitions differ**, and that difference is not cosmetic — stock-based compensation is a large line for growth-stage genomics companies, and an "excluding SBC" measure will always cross zero earlier than an "including SBC" one. The two figures are **not** directly comparable, and `verify.py` records that fact explicitly so that no sentence here can imply otherwise.

What is comparable is the direction, and it is consistent with §38: the acquirer's plan reaches breakeven **later** on a **stricter** definition. Tempus' own numbers for Personalis show **8** consecutive years of negative unlevered free cash flow, turning positive only in **2034E**.

A company that expects eight years of cash burn from an acquisition, and publishes a fifteen-year forecast saying so, is being remarkably candid — because it had no choice.

---

## 41. Why These Numbers Exist

It is worth being explicit about the mechanism, because it is the cleanest demonstration of the case study's thesis.

Tempus' management prepared fifteen-year projections in June 2026 for the board's evaluation. Those projections were given to Morgan Stanley and relied upon in its fairness opinion. Personalis' management prepared fourteen-year projections, approved by its board, relied upon by Centerview and TD Cowen.

Under the disclosure regime governing merger proxies, when a financial advisor relies on management projections in rendering a fairness opinion, those projections must be summarised for the stockholders being asked to vote. So:

- **15 years** of Tempus' revenue, Adj. EBITDA, and unlevered free cash flow projections for Personalis became public.
- **14 years** of Personalis' own revenue and profitability projections became public.
- The specific revenue figures handed across in diligence became public, year by year, in a footnote.
- The entire negotiation history became public in "Background of the Mergers."

And both companies stated, in the same document, that they do not publish this kind of thing.

Set that against the four preceding days. On Day 86, a company's safety claim covering 115 million interactions rested on **0.27%** coverage from its own preprint. On Day 87, an acquirer's fifteen-year internal model for a target is printed in full, including the years it loses money.

The ratio of Day 87's evidence coverage to Day 86's is **59.00×** on the comparable measure used in `verify.py` — the fraction of the relevant claim base for which the underlying split or evidence is actually on the record (**15.75%** for Tempus' self-authorship, **0.27%** for Hippocratic AI's safety claim).

That ratio is worth one methodological note, because it is a trap this series has fallen into before. Computed from the unrounded coverages it is **59.00**. Computed from the rounded pair — 15.75 ÷ 0.27 — it is **58.33**. A single premature rounding moves the answer by 0.67. `verify.py` asserts both values so that the correct one is unambiguous and the incorrect one is documented rather than merely avoided.

**Obligation produced roughly fifty-nine times the evidence coverage that choice did.** That is the answer to §24's question, and it is not close.

---

## 42. The Reconciliation Exemption

And then, in the middle of the most compelled disclosure in the entire record, an exemption.

[H] states that the Adj. EBITDA and unlevered free cash flow figures in the projections are non-GAAP measures, and then:

> "The SEC rules, which otherwise would require a reconciliation of a non-GAAP financial measure to a GAAP financial measure, **do not apply** to non-GAAP financial measures provided to a board of directors or financial advisors in connection with a proposed business combination transaction such as the proposed Transactions if the disclosure is included in a document such as this proxy statement/prospectus. ... Accordingly, Tempus has **not** provided a reconciliation."

So the same rulebook that forced fifteen years of forecasts into public view simultaneously waived the requirement to reconcile them to GAAP.

This is not a loophole being exploited; it is an explicit carve-out, disclosed plainly, and there is a sensible rationale for it — a board evaluating a deal is not preparing an earnings release, and requiring retrospective GAAP reconciliation of internal models would discourage boards from using models at all.

But it is the necessary qualification to §41, and it keeps the finding honest:

> **Obligation is not a uniform force. It is a specific set of rules with specific edges, and the edges are where the interesting things live.** The same document is simultaneously the most forthcoming and the least reconcilable disclosure Tempus has ever made.

---

## 43. The Disclosure Ledger

Five questions a serious reader would want answered about Tempus. Their status, and what compelled the answer.

| # | Question | Status | What compelled it |
|---|---|---|---|
| 1 | What share of the supporting literature is self-authored? | **Disclosed, then withdrawn** | Staff comment 7 [A] |
| 2 | How was the AI model developed and validated? | **Disclosed** | Staff comment 1 [B9] |
| 3 | How accurate is the AI model? | **Not disclosed** | *Nothing* |
| 4 | What is the fifteen-year revenue plan? | **Disclosed** | Merger rules [H] |
| 5 | How much of Diagnostics growth is organic? | **Not disclosed** | *Nothing* |

Counting:

- **2 of 5 (40.00%)** currently disclosed.
- **2 of 5** not disclosed at all.
- **1 of 5** disclosed and then withdrawn.
- **3 of 5 (60.00%)** of the rows required a reviewer or a rule to produce an answer.
- **Every** row that has ever been answered was compelled. **Nothing material in this ledger was volunteered.**

That last line is the one to carry out of this case study. Across a company with an audited income statement, certified officers, ten comment letters, and a live registration statement, the number of material disclosures in this ledger that arrived because someone at the company decided a reader deserved them is **zero**.

---

## 44. Feature Analysis

| Capability | What it is | Disclosed evidence of effectiveness |
|---|---|---|
| **xT / xR solid tumour NGS** | Tissue-based comprehensive genomic profiling | **Yes** — analytical validation sensitivities and specificities |
| **xF liquid biopsy** | ctDNA-based profiling | **Yes** — sensitivity, specificity, concordance vs Roche AVENIO |
| **xG germline** | Hereditary cancer risk (via Ambry) | Partial — described, metrics not in [E] |
| **TO algorithm** | Predicts tumour site of origin | **Process only — no performance metric** |
| **HRD algorithm** | Homologous recombination deficiency | Named; no metrics |
| **Hub** | Provider-facing application | Described; no usage metrics |
| **Lens** | Research-facing application | Described; access sometimes charged |
| **Insights** | De-identified data licensing | Revenue disclosed at segment level only |
| **Therapies** | Clinical trial matching | Described; performance obligation probed by staff |

The pattern across the table is the pattern of §32: **regulated artefacts carry numbers; unregulated artefacts carry adjectives.**

---

## 45. Competitive Analysis

Competitors are assessed only on what can be established from Tempus' own filings and the public disclosure posture of each company. This series does not assert competitor metrics it has not verified from a primary source.

| Competitor | Overlap | Disclosure posture | Comparable evidence available? |
|---|---|---|---|
| **Foundation Medicine** (Roche) | Comprehensive genomic profiling | Subsidiary of a listed parent — no standalone SEC filings | Limited |
| **Guardant Health** | Liquid biopsy | US-listed — full SEC filing obligations | **Yes** |
| **Caris Life Sciences** | Molecular profiling + data | Private | **No** |
| **Personalis** | Tumour-informed ctDNA | US-listed — **and now being acquired, so its forecasts are public** | **Yes, exceptionally** |
| **Flatiron Health** (Roche) | Oncology real-world data | Subsidiary — no standalone filings | **No** |
| **Illumina** | Sequencing instruments — **supplier, not competitor** | US-listed | N/A |

The Illumina row is worth its own sentence. Comment 8 of [A] required Tempus to disclose the material terms of its Illumina agreement, including term and termination provisions, and asked what consideration had been given to filing it as an exhibit — because Tempus relies on Illumina as a **sole supplier** for certain sequencers and reagents. Supplier concentration in the physical layer is the structural risk underneath a business that presents itself as a software and data company.

The competitive insight that matters for Day 87 is a methodological one: **the amount you can learn about a competitor is a function of its capital structure, not its importance.** Caris and Flatiron may be more consequential to Tempus than Personalis, and they are close to invisible. Personalis is about to become the most thoroughly documented company in this entire arc — for the sole reason that someone is buying it.

---

## 46. Porter's Five Forces

| Force | Assessment | Evidence |
|---|---|---|
| **Supplier power** | **High** | Sole-supplier reliance on Illumina, flagged by staff [A] comment 8 |
| **Buyer power** | **High on the clinical side** | Medicare denials at 30% of clinical volume in 2021 [A] comment 16; payment received on approximately 50% / 48% of clinical oncology NGS tests in 2019 / 2020 [A] comment 15 |
| **Buyer power** | **Moderate on the data side** | Multi-year subscriptions; concentration probed by staff [A] comment 22 |
| **Threat of substitutes** | **Moderate** | Academic sequencing cores, in-house health system labs |
| **Threat of new entrants** | **Low to moderate** | Capital, CLIA certification, and cumulative data depth are real barriers; the FY2025 database is not replicable quickly |
| **Rivalry** | **High and consolidating** | The Personalis acquisition is itself the evidence |

The buyer-power rows are the ones a PM should sit with. A business that was collecting on roughly half its clinical oncology NGS tests, and that had an entire lab's Medicare claims denied for a period, is a business whose product-market fit with *clinicians* was strong and whose product-market fit with *payers* was contested. Those are different fits and the second one is the one that pays.

---

## 47. Business Model Canvas

| Block | Content |
|---|---|
| **Key partners** | Illumina (sole supplier, certain sequencers/reagents); Pathos AI (related party — master agreement required to be filed per [A] comment 34); Google (convertible note and Google Cloud Platform agreement, [A] comment 35); AstraZeneca (MSA incl. a $35M fee arrangement, [D]); Personalis (reference lab 2023 → acquisition target 2026) |
| **Key activities** | Sequencing; data curation; model development; payer contracting and appeals; software |
| **Key resources** | 5 laboratories; the de-identified multimodal database; CLIA/CAP certifications; direct provider data connections |
| **Value propositions** | Molecular answers inside the clinical window; linked molecular-clinical-outcome data at scale; algorithms delivered through existing ordering workflow |
| **Customer relationships** | Ordering-physician relationships; multi-year pharma subscriptions; EHR integrations |
| **Channels** | Diagnostics sales force; EHR integrations; requisition forms; online portal |
| **Customer segments** | Oncologists and health systems; pharmaceutical and biotechnology companies; trial sponsors |
| **Cost structure** | Laboratory operations; third-party laboratory costs; R&D ($172.924M FY2025); technology; SG&A |
| **Revenue streams** | Diagnostics **$955.381M** (75.12%); Data and applications **$316.408M** (24.88%) |

The related-party density in "Key partners" is itself a finding. Pathos AI appears repeatedly in the comment record: [A] comment 10 asked what percentage of his time the CEO devotes to Tempus given his Pathos role; [A] comment 34 required the Pathos master agreement to be filed as a related-party agreement; [B8] comment 2 required the same disclosure for the COO after he became Pathos' interim CEO. The staff had to ask **three separate times**, across twenty months, about executives' divided attention.

---

## 48. SWOT

**Strengths**
- Two-sided loop where the diagnostics business funds and feeds the data business.
- Genuine scale: 5 labs, over 123,000 Algos ordered, over 800 cited publications.
- **First GAAP-positive quarter** in Q2 2026 ($5.642M, 1.48% margin).
- Assay-level analytical validation is disclosed with numbers — **7** metrics in [D]/[E].
- Cash of $604.787M, up 77.38%.

**Weaknesses**
- **No algorithm performance metric has ever been published** — the strategic differentiator is the least evidenced asset.
- R&D intensity fell **7.94 percentage points** in FY2025.
- Cumulative net loss of **$(1,164.96)M** across FY2023–FY2025; no profitable full year.
- Diagnostics growth of 111.48% cannot be decomposed into organic and acquired.
- Sole-supplier dependency on Illumina.
- Historic reimbursement fragility (§46).

**Opportunities**
- Personalis brings tumour-informed ctDNA and a partner relationship already three years old.
- Ambry extends reach beyond oncology into pediatrics, rare disease, cardiology, reproductive health, immunology.
- Algos represent a category the company itself says may be "substantially larger" than existing lines.
- Publishing a single TO performance metric would differentiate Tempus from every company in the Day 83–87 cohort at near-zero cost.

**Threats**
- Payer behaviour, as 2021 demonstrated.
- LDT regulatory uncertainty — [E] notes the FDA's 2024 rule was invalidated by a federal district court in March 2025, which removes a burden and also removes a validation requirement that would have generated exactly the algorithm evidence that is missing.
- Integration risk across Ambry, Paige.AI, Deep 6 AI, and now Personalis.
- **Disclosure decay** — the risk that, absent review, quantitative disclosures continue to be replaced by qualitative ones.

---

## 49. Metrics That Matter

Six metrics, with a column this series added at Day 84 and has kept since.

| Metric | Why it matters | Disclosed? | What would make it credible |
|---|---|:---:|---|
| Self-authorship share of cited literature | Converts a publication count into a validation measure | **No** (since 2024) | Restore the numerator; publish quarterly |
| TO algorithm sensitivity / specificity | The only direct evidence the Algos work | **No** | A single confusion matrix |
| Organic Diagnostics growth | Separates execution from acquisition | **No** | One line in MD&A |
| Tests delivered per period | Volume, independent of price and mix | **No** in [E] | Was requested in [A] comment 11 |
| Data customer count and concentration | Durability of the highest-margin line | **No** | Was requested in [A] comment 22 and [B5] comment 2 |
| R&D as % of revenue | Whether the AI story is funded | **Yes** — 13.60% FY2025 | Already credible |

Five of six are undisclosed. **Three of those five were explicitly requested by SEC staff between 2021 and 2022.** They were answered then, in draft registration statements the public never saw in unamended form, and they are not in the current annual report.

---

## 50. North Star and Guardrails

If this case study were advising Tempus' leadership, the metric architecture would be:

**North Star:** *Clinical decisions changed per quarter* — the count of cases where a Tempus output (assay or Algo) altered the therapeutic path taken.

This is the honest North Star because it is the thing the company claims to do. It is also hard, and the filings do not measure it.

**Guardrails:**

| Guardrail | Threshold discipline |
|---|---|
| Algo prediction error rate | Published, with confidence intervals, every quarter |
| Self-authorship share of cited literature | Published every annual report; no disclosure of the denominator without the numerator |
| Collection rate on clinical tests | Monitored against the ~50%/48% historical baseline in [A] |
| Organic vs acquired revenue | Reported separately once acquisitions exceed a stated share of growth |
| R&D as % of revenue | Floor, not a residual |

The second guardrail is a rule about **disclosure symmetry**, and it is the specific recommendation that the rest of this case study earns: *never publish the flattering half of a ratio without the unflattering half.* Tempus published "over 800" and omitted the share that was self-authored. Both numbers were available to the company. One was chosen.

---

## 51. AARRR

| Stage | Diagnostics | Data and applications |
|---|---|---|
| **Acquisition** | Sales force, EHR integration, requisition forms | Named partnerships with large pharmaceutical companies |
| **Activation** | First ordered test returned inside the decision window | First licensed cohort delivered |
| **Retention** | 12-month retention among oncologists ordering >5 tests was reported internally as 92% through Dec 2021 — **denominator never disclosed**, and the staff asked for it [B5] | Multi-year subscription renewals; average term not disclosed |
| **Revenue** | $955.381M FY2025 | $316.408M FY2025 |
| **Referral** | Peer-reviewed publications — **73.81% self-authored at the last disclosure** | Reference customers |

Two of these five rows are where the case study's findings land. The retention row is a metric whose denominator a regulator had to demand. The referral row is a metric that is mostly the company referring itself.

---

## 52. HEART

| Dimension | Signal | Disclosed? |
|---|---|:---:|
| **Happiness** | Clinician satisfaction | No |
| **Engagement** | Tests per ordering physician per period | No |
| **Adoption** | New ordering physicians per period | No |
| **Retention** | 12-month retention (>5 tests) — 92% internally, denominator unknown | Partial |
| **Task success** | **Algo prediction accuracy** | **No** |

Task success is empty. For a diagnostics company, task success is the product.

---

## 53. What a PM Should Take From This

Five transferable lessons, stated so they survive outside healthcare.

**1. Read the comment letters.** SEC staff comment letters are free, public, indexed on EDGAR, and almost entirely unread by product people. They are a professional reviewer's list of everything a company tried not to say clearly. For any US-listed competitor, partner, or acquisition target, they are the highest-yield hour of research available. Tempus' first letter alone caught a company contradicting itself about **how many products it had**.

**2. Process disclosure is not performance disclosure.** "We validated using multiple cross-validation techniques and monitor for drift" is a genuinely good sentence that contains no result. When a vendor describes *how* they measured, ask what the measurement *was*. Tempus is better than almost anyone at the first sentence and has never published the second.

**3. A ratio's denominator is a marketing asset; its numerator is a liability.** "Over 800 peer-reviewed articles" grows forever and costs nothing. "Of which 590 are ours" costs something every time it is printed. Watch for the moment a company starts reporting one without the other — and note that Tempus' self-authorship share **rose 3.08 percentage points** over the period it was disclosed.

**4. Every disclosure has a force behind it. Identify the force.** Assays carry numbers because CLIA requires analytical validation. Algorithms carry adjectives because nothing requires anything. Fifteen-year forecasts exist because a merger rule demanded them. **Nothing material in the §43 ledger was volunteered.** When you read a competitor's claim, the useful question is not "is this true" but "what made them say it, and what happens when that force is removed."

**5. Regulatory review is not verification, and the regulator will tell you so in writing.** "The company and its management are responsible for the accuracy and adequacy of their disclosures, **notwithstanding any review, comments, action or absence of action by the staff**" [C]. Being in a 10-K means someone is liable for it. It does not mean anyone checked it.

---

## 54. Product Recommendations

Four recommendations, each addressing a specific documented gap. Each is a disclosure and measurement decision, because that is what the evidence supports; this case study has no visibility into Tempus' engineering roadmap and does not pretend otherwise.

**P1 — Restore the self-authorship numerator, and publish it every quarter.**
*Gap:* §28. The denominator grew 6.35× and the numerator vanished.
*Change:* Report "X of Y peer-reviewed articles were Tempus-authored" in every annual and quarterly report, as the IPO prospectus did.
*Why it matters:* Without it, the publication count is not a validation metric. With it, Tempus is the only company in the Day 83–87 cohort that publishes its own independence ratio.

**P2 — Publish TO algorithm clinical performance.**
*Gap:* §31. **0** performance metrics for an algorithm in clinical use since 2021.
*Change:* Publish sensitivity, specificity, and a confusion matrix for TO against pathologist-adjudicated ground truth, with confidence intervals, annually.
*Why it matters:* Tempus already reviews every TO prediction against underlying data with board-certified pathologists. The adjudication is already happening. The measurement exists internally.

**P3 — Publish a glossary of AI terms.**
*Gap:* §33. Requested in Nov 2023, phrased as "please consider," not done.
*Change:* A one-page defined-terms section in the 10-K.
*Why it matters:* Near-zero cost, helps every non-specialist reader, and closes the only outstanding staff request in the record.

**P4 — Publish a post-close reconciliation of the Personalis projection gap.**
*Gap:* §38. A **$779M** cumulative disagreement between two managements is now public, and there is no mechanism by which anyone will ever learn who was right.
*Change:* At each annual report after close, report Personalis-attributable revenue against the 2026 projection.
*Why it matters:* This is the most falsifiable forecast Tempus has ever published. Scoring it would be an extraordinary credibility asset.

---

## 55. RICE Prioritisation

**Scoring definitions.** Reach is an ordinal 1–10 anchored to disclosed counts and stated below. Impact uses the standard 0.25 / 0.5 / 1 / 2 / 3 scale. Confidence is 0–1. Effort is person-months. RICE = (R × I × C) / E.

| | Reach | Reach anchor | Impact | Confidence | Effort | **RICE** |
|---|---:|---|---:|---:|---:|---:|
| **P1** Restore self-authorship numerator | 7 | Every reader of the 10-K/10-Q risk factors; the ratio is load-bearing for the "over 800" claim | 2.0 | 0.95 | 0.50 | **26.60** |
| **P2** Publish TO performance | 9 | Over 123,000 Algos ordered; clinicians and patients downstream of each | 3.0 | 0.62 | 8.00 | **2.09** |
| **P3** AI glossary | 4 | Non-specialist readers of the same filings | 0.5 | 0.95 | 0.25 | **7.60** |
| **P4** Projection reconciliation | 8 | Personalis stockholders voting, plus TEM holders | 2.0 | 0.40 | 3.00 | **2.13** |

**Base ranking: P1 (26.60) → P3 (7.60) → P4 (2.13) → P2 (2.09).**

P1 leads by a wide margin — spread across the field is **24.51** points. It is cheap (half a person-month), high-confidence (the company has done it twice before), and directly repairs the most significant gap in the record.

Which is exactly why it must be stress-tested.

---

## 56. The Stress Test

This series applies a stress multiplier to every RICE table, for a reason Day 82 established: base RICE scores what a change is worth if nothing resists it, and something always resists it. The stress case asks what happens when each proposal meets **the constraint that actually binds it**.

| | Binding constraint | C multiplier | E multiplier | **Stressed RICE** | Decay |
|---|---|---:|---:|---:|---:|
| **P1** | Securities counsel resists re-introducing a number that invites a conflict-of-interest inference; plus perpetual audit and restatement exposure once it is a recurring disclosure | **0.15** | **6.5** | **0.61** | **-97.69%** |
| **P2** | Clinical and regulatory review of any published performance claim | 0.90 | 1.2 | **1.57** | -25.00% |
| **P3** | Drafting and legal review only | 0.90 | 1.5 | **4.56** | -40.00% |
| **P4** | Forward-looking-statement exposure; segment attribution is genuinely hard post-integration | 0.80 | 1.5 | **1.14** | -46.67% |

**Stressed ranking: P3 (4.56) → P2 (1.57) → P4 (1.14) → P1 (0.61).**

**P1 goes from first to last.** The reversal is total, and it is asserted programmatically in `verify.py` — `p1_leads_base` and `p1_ranks_last_under_stress` are both hard assertions in the gate, not observations written after the fact.

The field also compresses sharply: the spread falls from **24.51** to **3.95** under stress. When constraints are modelled, the differences between good ideas shrink and the differences between *achievable* ideas grow.

---

## 57. Why P1 Dies

This is the part of the case study where the model earns its keep, because the stress test does not merely reorder a list. **It reproduces behaviour that already happened.**

P1 — restore the self-authorship numerator — decays **97.69%** under stress, more than any other proposal. The constraint that kills it is not cost. It is half a person-month of work. The constraint is that publishing the numerator does something no other proposal does: **it creates a recurring, quantified, unflattering disclosure that the company must then carry forever, and that invites precisely the conflict-of-interest inference the risk factor already warns about in words.**

Once it is a recurring disclosure, it must be consistent year to year, defensible under audit, and restated if the methodology changes. The first year it rises materially, that becomes a story. And unlike the qualitative sentence — which costs nothing and warns of the same risk — the number can be tracked, charted, and used against the company.

Now look back at §28.

**That is what happened.** The number appeared twice, both times in documents prepared under active staff review, and disappeared from the first annual report prepared without it. The qualitative sentence — which carries none of the recurring exposure — survived verbatim.

The RICE stress test, built from the four proposals' binding constraints and no knowledge of the outcome, ranks P1 last. The historical record shows P1 was, in effect, ranked last.

The model did not predict the past by being fitted to it. It arrived there from the constraints, and that is the strongest validation of a prioritisation framework this series has produced.

**The lesson generalises and it is uncomfortable:** when a cheap, obviously correct, high-impact disclosure does not happen, the explanation is almost never that nobody thought of it. It is that the thing making it valuable — that it is quantified, recurring, and unflattering — is the same thing making it unsurvivable internally. **A recommendation's value to the reader and its cost to the publisher are frequently the same property, viewed from opposite sides.**

---

## 58. MoSCoW

| | Item | Rationale |
|---|---|---|
| **Must** | Publish TO algorithm performance (P2) | The central evidence gap; everything strategic depends on it |
| **Must** | Publish an AI glossary (P3) | Trivial cost, outstanding staff request, highest stressed score |
| **Should** | Restore the self-authorship numerator (P1) | Correct on the merits; requires executive sponsorship to survive counsel |
| **Should** | Disclose organic vs acquired Diagnostics growth | Closes ledger row 5 |
| **Could** | Post-close projection reconciliation (P4) | Highest credibility payoff, lowest feasibility |
| **Won't** | Per-test unit economics | No realistic path; competitively sensitive |

Note that P1 moves from "top of the base RICE table" to "Should" — because MoSCoW is an execution framework and execution is where the stress case applies. P3, which base RICE ranked second, becomes a Must, because it is the only proposal that survives contact with its own constraint essentially intact.

---

## 59. Kano

| Feature | Category | Reasoning |
|---|---|---|
| Assay analytical validation metrics | **Must-be** | Absence would be disqualifying; CLIA requires it |
| Turnaround inside the clinical window | **Must-be** | The product fails without it |
| Algo performance metrics | **Attractive → becoming Must-be** | No competitor in this cohort publishes them; that will not last |
| Self-authorship ratio | **Attractive** | Nobody expects it; publishing it would be genuinely differentiating |
| Fifteen-year forecast transparency | **Indifferent → Attractive** | Involuntary today; would be remarkable if maintained voluntarily |
| AI glossary | **Indifferent** | Nobody's purchase decision turns on it; its value is comprehension |

The middle row is the strategic one. Algorithm performance disclosure is currently **Attractive** — an unexpected delighter — precisely because no one in this market does it. Categories migrate. The first company to publish a confusion matrix for a clinical algorithm converts it into a Must-be for everyone else, and captures the differentiation on the way through.

---

## 60. Roadmap

A disclosure roadmap, sequenced by the stress test rather than by base RICE.

**Horizon 1 — next annual report**
- Publish the AI glossary (P3). Highest stressed score; closes the last outstanding staff request.
- Disclose organic vs acquired Diagnostics growth for FY2026.
- Restore the self-authorship numerator (P1) — *contingent on executive sponsorship, per §57.*

**Horizon 2 — within four quarters**
- Publish TO algorithm sensitivity, specificity, and confusion matrix against pathologist-adjudicated ground truth (P2).
- Reinstate tests-delivered volume, requested in [A] comment 11.
- Reinstate data customer count and concentration, requested in [A] comment 22 and [B5] comment 2.

**Horizon 3 — post-close**
- Report Personalis-attributable revenue against the 2026 projection (P4).
- Extend algorithm performance disclosure from TO to HRD and the remaining Algo suite.
- Establish the disclosure-symmetry guardrail from §50 as policy: no denominator without its numerator.

---

## 61. Risks

| Risk | Basis | Severity |
|---|---|---|
| **Reimbursement** | 2021 MAC denials at 30% of clinical volume; ~50%/48% historical collection on clinical oncology NGS | **High** |
| **Supplier concentration** | Sole-supplier reliance on Illumina [A] comment 8 | **High** |
| **Integration** | Ambry, Paige.AI, Deep 6 AI, Personalis — four in roughly eighteen months | **High** |
| **Related-party governance** | Pathos AI; three separate staff comments on executive time allocation | **Moderate** |
| **Regulatory whiplash** | FDA LDT rule finalised May 2024, invalidated March 2025 [E] | **Moderate** |
| **Evidence risk** | No published algorithm performance; self-authorship ratio no longer disclosed | **Moderate and rising** |
| **Disclosure decay** | Quantitative disclosures replaced by qualitative ones absent review | **Structural** |

The last row is the one this case study adds to the conventional list. It is not a risk to Tempus' business. It is a risk to every reader's ability to evaluate Tempus' business — and it operates silently, because the wrapper of the disclosure survives its contents.

---

## 62. Open Questions

Stated as questions because the evidence does not answer them, and this series does not answer questions its evidence cannot reach.

1. What is the TO algorithm's accuracy?
2. What share of the "over 800" cited articles is Tempus-authored?
3. How much of FY2025's 111.48% Diagnostics growth was organic?
4. Why did the self-authorship numerator leave the 10-K? A drafting decision was taken and this case study has no visibility into it.
5. Was Personalis' 70.36% CAGR or Tempus' 43.29% CAGR closer to right? Nothing in the current disclosure regime will ever tell us.
6. What experience did the personnel who built the TO algorithm have? The staff asked in 2023; it has never been answered.
7. Why did R&D intensity fall 7.94 percentage points in a year the company's entire thesis is algorithmic?

Question 5 is the one worth sitting with. Two managements published detailed, quantified, opposing forecasts for the same asset, and the disclosure system that forced both into public view contains no mechanism whatsoever for ever scoring them. **Obligation produced the evidence and simultaneously guaranteed it would never be tested.**

---

## 63. Method Notes

**What was done.** All sources were retrieved directly from SEC EDGAR under CIK 0001717115 on 2026-09-25. HTML filings were parsed to text with BeautifulSoup and lxml; the PDF comment letters were extracted with `pdftotext -layout`. Financial figures were cross-checked against the XBRL company facts API [I] rather than read from HTML tables, because XBRL carries the tagged values the company itself asserted.

**The comment counting problem.** A regular expression counting `^\s*\d+\.` across the ten letters returns a number higher than 66, because financial-statement note captions ("9. Stock-Based Compensation, page F-29") match the same pattern. The 3 August 2022 letter [B5] was the clearest case: pattern matching suggested 9 comments; reading it shows **5**. Every letter was read in full and counted by hand. The gate records **66**.

**The crossover error.** The first reading of the two projection tables put the Tempus/Personalis crossover at 2038. It is **2039**; Tempus remains **10.27%** below in 2038. `verify.py` finds the crossover with a loop rather than asserting it, which is why the error surfaced before any prose was written. This is the specific value of writing the gate first.

**The rounding trap, again.** Six hand-stated expectations failed on the gate's first run — the two projection CAGRs, their difference, FY2024 R&D intensity, the crossover year, and the Day 86 coverage multiple. In every case the machine was right. Two were the rounded-intermediate trap this series first hit on Day 82: computing the Day 87 / Day 86 coverage multiple from rounded inputs gives **58.33**; from unrounded inputs it gives **59.00**. Both are now asserted in the gate so the correct value is unambiguous and the incorrect one is documented rather than merely avoided.

**What was not used.** No press release, no analyst note, no news coverage, no company blog, no social media. This constraint cost real information — Tempus' quarterly earnings releases (furnished on Form 8-K under Item 2.02) contain operational metrics the periodic reports omit, and they were deliberately left out because a furnished release is not a filed document and carries different liability. Readers should know the constraint was a choice and that it has a cost.

**What could not be obtained.** The company's response letters to the draft registration statement comments are not public — draft registration statement correspondence is not filed on EDGAR in the way public-filing correspondence is. We can see what the staff asked and what the final prospectus said. We cannot see what Tempus argued in between. Where this matters, the text says so.

**Diagram standard.** Markdown tables and ASCII only. Mermaid was dropped from this series at Day 50 for rendering reliability on GitHub and has not returned.

---

## 64. Series Position and Tomorrow

Day 87 closes the arc that began on Day 82.

- **Day 82 (Doximity)** — a public company where the material finding was buried in the 10-Q and the marketing claims appeared **zero** times in either the 10-Q or the 10-K.
- **Days 83–86** — four private companies, four reconstructions from the outside, culminating in Day 86's **0.27%** evidence coverage.
- **Day 87 (Tempus AI)** — obligation, tested directly.

**The hypothesis was: does obligation produce better evidence than choice? The answer is yes, by roughly 59×, with three qualifications that matter as much as the answer:**

1. **Obligation compels process, not performance.** The staff asked how Tempus validated its AI, and got an exemplary description of method containing **0** results. CLIA compels assay metrics; nothing compels algorithm metrics; so there are **7** of the former and **0** of the latter, in the same document.
2. **Obligation is discretionary and episodic.** Sixty-six comments from 2021 to 2023; "we have not reviewed and will not review" in 2025. And the number that mattered most left the filings in between.
3. **Obligation has edges, and the edges are deliberate.** The same rules that forced fifteen years of forecasts into public view waived the requirement to reconcile them.

**Tomorrow is Qure.ai** — and it returns to the hardest case. Qure.ai is a private Indian company building radiology AI, which means it sits at the intersection of everything this arc has established: no filing obligation (Days 83–86), a statutory registry that can be read through GLEIF and the MCA (Day 85), and a product class where regulatory clearance — CE marking, FDA 510(k), CDSCO — generates exactly the kind of compelled performance evidence that Tempus' Algos never had to produce.

That makes Day 88 the inverse of Day 87. Tempus is a company with maximal *disclosure* obligation and minimal *performance* obligation. A regulated medical-imaging device company is the opposite: it can keep its financials private while being compelled, by device regulators rather than securities regulators, to publish sensitivity and specificity. If Day 87 showed that securities disclosure compels process, Day 88 asks whether **device regulation compels results** — and whether a company with no investors to answer to publishes better clinical evidence than a listed company with no clinical disclosure requirement.

Days 89 and 90 close the series: **Gaudium IVF**, and then **Health in ChatGPT**.

---

## 65. References

All sources are SEC filings under CIK 0001717115, retrieved 2026-09-25.

1. **[A]** SEC Division of Corporation Finance, Office of Technology. Comment letter to Eric Lefkofsky, Tempus Labs, Inc., re: Draft Registration Statement on Form S-1 submitted 1 Sep 2021. 30 Sep 2021. Accession 0000000000-21-011937.
2. **[B1]** SEC comment letter re: Amendment No. 1. 16 Nov 2021. Accession 0000000000-21-013853.
3. **[B2]** SEC comment letter re: Amendment No. 1. 29 Nov 2021. Accession 0000000000-21-014324.
4. **[B3]** SEC comment letter re: Amendment No. 2. 17 Dec 2021. Accession 0000000000-21-015102.
5. **[B4]** SEC comment letter re: Amendment No. 3. 11 May 2022. Accession 0000000000-22-005176.
6. **[B5]** SEC comment letter re: Response Letter No. 3. 3 Aug 2022. Accession 0000000000-22-008188.
7. **[B6]** SEC comment letter re: Amendment No. 4. 27 Oct 2022. Accession 0000000000-22-011783.
8. **[B7]** SEC comment letter re: Amendment No. 5. 27 Jan 2023. Accession 0000000000-23-000921.
9. **[B8]** SEC comment letter re: Amendment No. 6. 5 May 2023. Accession 0000000000-23-004692.
10. **[B9]** SEC comment letter re: Amendment No. 8. 21 Nov 2023. Accession 0000000000-23-012780.
11. **[C]** SEC letter re: Registration Statement on Form S-1, File No. 333-285186 ("we have not reviewed and will not review"). 4 Mar 2025. Accession 0000000000-25-002419.
12. **[D]** Tempus AI, Inc. Form 424B4, IPO prospectus. Filed 17 Jun 2024. Accession 0001193125-24-161989.
13. **[E]** Tempus AI, Inc. Form 10-K for the fiscal year ended 31 Dec 2025. Filed 24 Feb 2026. Accession 0001193125-26-066961.
14. **[F]** Tempus AI, Inc. Form 10-Q for the quarterly period ended 30 Jun 2026. Filed 30 Jul 2026. Accession 0001193125-26-326090.
15. **[G]** Tempus AI, Inc. Form 8-K, Item 1.01 (Agreement and Plan of Merger with Personalis, Inc.). Filed 20 Jul 2026. Accession 0001193125-26-309073.
16. **[H]** Tempus AI, Inc. Form S-4 registration statement / proxy statement-prospectus. Filed 31 Aug 2026. Accession 0001193125-26-376895.
17. **[I]** SEC XBRL company facts API, CIK 0001717115. `https://data.sec.gov/api/xbrl/companyfacts/CIK0001717115.json`
18. **[J]** Tempus AI, Inc. and underwriters, acceleration request correspondence. 11 Jun 2024 and 5 Mar 2025. Accessions 0001193125-24-159092, 0001193125-24-159099, 0001193125-25-047163.

**Verification:** `verify.py` in this folder — **265 checks, all passing**. `crosscheck.py` confirms that every two- and three-decimal figure appearing in this README and in `ASSUMPTIONS.md` traces to a value asserted in the gate.

**Assumptions, source conflicts, and limitations:** see `ASSUMPTIONS.md`.

---

*Day 87 of 90. Written by Gaurav Singh. Sources are primary and cited. Figures are computed, not asserted. Where the record is silent, this document says so.*
