# ASSUMPTIONS — Day 56, MediBuddy (Phasorz Technologies Private Limited)

This document separates what is **verified** from what is **assumed**, **derived** or **constructed** in the Day 56 case study. Every figure in the README is traceable to one of the four categories below. Nothing was invented.

**Research boundary.** Public sources only: MCA registry records, trade-press reporting of filed accounts, the company's own website and press releases, and the CII–MediBuddy report of 31 July 2026. No MediBuddy employee, internal document, customer contract or authenticated product session was consulted. Audited financials run to **FY25**; FY26 exists only as company-stated press-release figures.

---

## Part 1 — Assumptions

### A1 — Load-bearing. The ₹1,500 Cr figure is an annualised Q4 exit run rate, and MediBuddy's demand is concentrated into employer-scheduled campaign windows.

**What is fact, not assumption:** the three company-stated claims — ₹1,500 Cr, ~20% YoY growth, ~6× over five years — cannot all describe audited operating revenue against a FY25 base of ₹724.6 Cr. That is arithmetic (§13.2). It is also fact that PTI's wire copy says "annual revenue run rate" while several outlets rendered the same figure as annual revenue.

**What is assumed:** that the reconciling explanation is a Q4-annualised exit run rate (reading R1), rather than a gross platform-value measure (R2) or a consolidation change (R3). R1 implies Q4 FY26 at roughly ₹375 Cr — about **43.1% of the year in one quarter, 1.73× a uniform quarter**.

**Why it is assumed rather than known:** MediBuddy has published no quarterly revenue split and no basis note for the ₹1,500 Cr figure.

**Supporting (not proving) evidence:** the company's own operating disclosures of **100,000+ unique consumers in a single day against 10 lakh+ annually** — 10% of the year's uniques on one day, **36.5× a uniform day**. This is an independent, non-financial corroboration of concentrated demand, but a single large day could in principle be one unusually big employer campaign rather than a quarterly pattern.

**What it supports in the README:** line 4 of the six converging lines (§46), the idle-capacity feasibility argument (§38.3), and the framing of Q4 profitability as coinciding with peak demand rather than proving structural change.

**What it does not support:** the proposal itself. §50 rests on the 52%-inaction finding and the 25%/46% concentration, both of which are independent of A1. If A1 is wrong, Close is still worth testing; only the capacity argument falls away.

**Kill / falsification:** MediBuddy disclosing a quarterly revenue split, or stating the basis of the ₹1,500 Cr figure. The **peak-day-to-uniform-day ratio** is placed on the §55 dashboard specifically as an early-warning metric for this assumption.

### A2 — The CII–MediBuddy report's findings are representative of MediBuddy's own corporate book.

The 52%-inaction figure and the 25%/46% claims concentration come from a study of 10,551 employees across 459 corporate benefit programmes in seven industries. This document assumes the sample is broadly representative of the population MediBuddy serves. It may not be: the study spans multiple providers' programmes, and MediBuddy's own accounts could differ in either direction. **This is the assumption §53's Phase 0 exists to test** — K1 kills the programme if baseline 90-day closure in MediBuddy's own book is already above 50%.

### A3 — No closure workflow with an owner and an SLA currently exists in the product.

This is an absence-of-evidence claim. Public product surfaces, the corporate page and press coverage describe a service catalogue, an HR utilisation platform and a fraud system, with no described care-coordination pathway. MediBuddy may operate one internally without publicising it. If it does, the correct case study is about why that pathway is not priced or reported — a different document with the same conclusion about the contract.

### A4 — "1 million+ covered lives" and "10 lakh+ unique customers annually" describe overlapping populations.

The two figures come from different disclosures (the corporate page and the May 2026 announcement) and are treated in §13.3 as effectively the same number, supporting the conclusion that the standalone consumer business is small. If the annual-uniques figure includes a material consumer population distinct from covered lives, that inference weakens — though the >75% B2B revenue share would still hold.

### A5 — The employer would pay for closure evidence at renewal.

The proposal assumes an HR buyer values a cohort closure rate enough to change a renewal decision. Evidence for: buyer power is high and catalogues are undifferentiated (§16), so there is currently nothing else to compete on. Evidence against: **73% of organisations sit in the two lowest workplace-health maturity stages** per the same CII report, and a low-maturity buyer may simply want the cheapest compliant vendor. This is why §53 Phase 4 is an outcome-priced *pilot* with three employers rather than a repricing of the book.

---

## Part 2 — Derivations

All 39 derived figures were recomputed programmatically before publication (`verify.py`, 39 checks, all passing). The load-bearing ones:

| # | Derivation | Inputs | Result |
|---|---|---|---|
| D1 | 20%-growth implication | ₹724.6 Cr × 1.20 | **₹869.5 Cr**; ₹1,500 Cr is **1.73×** that |
| D2 | ₹1,500 Cr as growth on FY25 | 1,500 ÷ 724.6 | **2.07×**, i.e. **+107.0%** |
| D3 | Sixfold-in-five-years CAGR | 6^(1/5) − 1 | **43.1%/yr** |
| D4 | ₹1,500 Cr against FY22 | 1,500 ÷ 234.1 | **6.41×** — consistent with the 6× claim |
| D5 | Q4 share under reading R1 | (1,500 ÷ 4) ÷ 869.5 | **43.1% of the year**, **1.73×** a uniform quarter |
| D6 | Margin path | −14.19% + 15pp | **+0.81%** full-year EBITDA |
| D7 | Peak-day concentration | 100,000 ÷ 1,000,000 × 365 | **36.5×** a uniform day |
| D8 | Commissions intensity | 155.47 ÷ 724.6 | **21.5%** of operating revenue |
| D9 | Cost of materials | 333 ÷ 724.6; 333 ÷ 879 | **46.0%** of revenue; **37.9%** of expenses |
| D10 | Cost per rupee earned | 879 ÷ 724.6 | **₹1.21** |
| D11 | Revenue per covered life | 724.6 Cr ÷ 1,000,000 | **₹7,246/yr** (**₹15,000** at ₹1,500 Cr) |
| D12 | Lives per corporate | 1,000,000 ÷ 990 | **1,010** |
| D13 | Users per network doctor | 1,000,000 ÷ 140,000 | **7.14/yr**, 0.60/month |
| D14 | Network composition growth, 2022→2026 | see §35 | doctors **+55.6%**, hospitals **+7.1%**, diagnostics **+156.7%**, pharmacies **+300%** |
| D15 | Claims concentration | 46 ÷ 25; 43 ÷ 25 | **1.84×** claims, **1.72×** payouts |
| D16 | Hospitalisation multiple | 7.27 ÷ 2.41 | **3.02×** |
| D17 | Loss narrowing FY24→FY25 | 1 − 137/215.7 | **−36.5%** |
| D18 | Audited CAGR FY22→FY25 | (724.6/234.1)^(1/3) − 1 | **45.7%/yr** |
| D19 | FY24 growth | 645.4 ÷ 297.7 − 1 | **+116.8%** |

D14 is derived from company-stated network counts at two points in time (Feb 2022 Series C coverage; 2026 company pages) and is only as reliable as those counts; it is graded 🟡.

---

## Part 3 — Constructs

Author-created content, clearly labelled as such in the README and not attributable to MediBuddy:

- **The three personas** (§20) — Ramya, Arun, Fatima. Composite illustrations built from the CII report's population statistics, not real people.
- **The current-state journey map** (§22).
- **The architecture and data-flow diagrams** (§41, §42) — reconstructions from public service descriptions. MediBuddy has published no architecture; the "no return path" edge is the author's characterisation of an absence, not a documented design.
- **All RICE inputs and both runs** (§47). Reach figures are author estimates against the 1M covered-lives base; Impact, Confidence and Effort are author judgements. The 47% stress factor is *not* a construct — it is the company's own published Gen Z participation figure.
- **Acceptance criteria** (§51.5), **both wireframes** (§52), the **four-arm experiment design and its 10-percentage-point pre-registered rule** (§54), the **KPI dashboard and its illustrative values** (§55), and the **pricing shape** (§39.3).
- **MediBuddy Close**, the **flag** object, **CF/1k**, and **Flag Precision** — none of these are MediBuddy products, features or metrics. They are proposals.

---

## Part 4 — What would change my mind

- **A quarterly revenue split, or a basis note on the ₹1,500 Cr figure.** If it is gross platform value with no quarterly concentration behind it (reading R2), A1 falls and with it the idle-capacity line in §46. The proposal survives; the file gets less interesting.
- **A Phase 0 retrospective showing baseline 90-day closure already above 50%** (K1). That would mean the 52% figure does not describe MediBuddy's own book, and this case study would be arguing for a solution to someone else's problem.
- **Evidence of an existing care-coordination workflow with a named owner and an SLA.** A3 would fail, and the correct question becomes why it is neither priced nor reported.
- **A flag rate below 15% of check-ups** (K2). The volume would be too thin to carry a contract line, and Close becomes a feature rather than a business-model change.
- **E4 beating E3 by less than 10 percentage points** (§54). That would mean a reminder campaign inside the existing model recovers most of the gain, and the expensive machinery — flag object, workflow, contract change — is not justified. The pre-registered rule was written before any data exists precisely so this outcome cannot be argued away afterwards.

---

## Part 5 — What could not be found out

Figures that would materially sharpen this analysis, which are not public. Every one of them is held by MediBuddy or by its auditors.

| Missing | Why it matters | Who holds it | What it would settle |
|---|---|---|---|
| FY26 filed accounts | The entire FY26 discussion rests on a press release | Company / MCA | Whether ₹1,500 Cr is revenue at all |
| Quarterly revenue split | A1 is an inference without it | Company | Reading R1 vs R2 vs R3 |
| Basis of the ₹1,500 Cr figure | Three claims are mutually inconsistent | Company | §13.2 entirely |
| Revenue split by service line | Which of 13+ services actually earns | Company | Whether diagnostics or consults drive the P&L |
| Abnormal-flag rate per check-up | The size of the addressable problem | Company | K2 |
| Baseline 90-day follow-through rate | Whether the 52% describes this book | Company | K1, and whether the proposal is needed |
| Contribution margin by service | Whether closure work is affordable | Company | The Phase 4 pricing model |
| Organic vs inorganic split of FY24's +116.8% | Whether growth was bought | Company | Appendix A-3 |
| Renewal and churn rate by employer | Whether price is really the deciding factor | Company | A5 |
| Peak-day date and cause | Whether 100,000 was a pattern or one campaign | Company | A1 directly |
| Competitor FY25 revenue (Plum, Onsurity, Loop Health, ekincare) | Relative scale in §14 | Those companies / MCA | Whether MediBuddy's lead is as large as it appears |
| MediBuddy's own Aetna India acquisition terms | The FY24 step-change | Company | Appendix A-3 |

**Because none of these could be verified, no competitor revenue figure and no TAM figure appears anywhere in the README.** Stating an unverifiable number would have been the easier way to fill §13.4 and §14; leaving them empty is the honest one.

---

**The single-sentence version:** MediBuddy's own research says 52% of employees do nothing after a health check-up, and MediBuddy's own contract pays it whether they do or not — so this case study proposes making the step in between a thing the company is paid for and accountable to.
