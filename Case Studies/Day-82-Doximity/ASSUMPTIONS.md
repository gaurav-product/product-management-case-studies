# ASSUMPTIONS — Day 82, Doximity, Inc. (NYSE: DOCS)

Companion to `README.md`. This file separates what was **disclosed** from what was **derived**, **constructed**, **unavailable**, or **deliberately excluded**. Series rule: a reader must be able to tell, for any statement in the case study, which of these five categories it belongs to.

Period analysed: Q1 FY2027, the three months ended 30 June 2026.
Verification: `verify.py`, **310 checks, all passing**.

---

## Part 1 — Disclosed facts

Taken directly from primary sources, with no derivation. If a figure appears in this part, it appears in a filing.

### 1.1 From the Form 10-Q (accession 0001516513-26-000040)

| Fact | Value |
|---|---|
| Revenue | $156,618 thousand |
| Cost of revenue | $23,692 thousand |
| Gross profit | $132,926 thousand |
| Research and development | $38,477 thousand |
| Sales and marketing | $45,049 thousand |
| General and administrative | $15,756 thousand |
| Income from operations | $33,644 thousand |
| Other income, net | $6,719 thousand |
| Provision for income taxes | $16,048 thousand |
| Net income | $24,315 thousand |
| Subscription revenue | $146,300 thousand |
| Other revenue | $10,318 thousand |
| Total stock-based compensation | $36,752 thousand |
| Depreciation and amortisation | $4,287 thousand |
| Total assets | $1,083,845 thousand |
| Total liabilities | $167,775 thousand |
| Total stockholders' equity | $916,070 thousand |
| Accumulated deficit | $(119,044) thousand |
| Shares issued and outstanding | 179,849 thousand |
| Liquidity (cash, equivalents, marketable securities) | $687.8 million |
| Customers with ≥$500k TTM subscription revenue | 127 (prior year 119) |
| Share of revenue from that cohort | approximately 83% |
| Net revenue retention rate | 107% (prior year 118%) |
| Quarterly unique active providers, YoY change | approximately 32% |
| Increase in accounts receivable | $33,334 thousand |
| Revenue recognised from opening deferred revenue | $69.5 million |
| Web hosting commitment, annual, through 31 Dec 2027 | $7 million |
| Second vendor remaining commitment, through June 2028 | $6 million |
| Securities class action settlement | $31 million, insurer-funded |
| Derivative lawsuits outstanding | 7 |
| Shares repurchased under the Feb 2026 programme | 4,759,886 |
| Aggregate repurchase price | $99.1 million |
| Remaining authorised | $400.9 million |

### 1.2 Narrated in 10-Q MD&A

These are management's own attributions, stated in the filing:

- Cost of revenue increased **$7.9 million**, "primarily driven by a $4.9 million increase in hosting and software costs and a $1.5 million increase related to amortization of an acquired intangible and internally-developed software. **Both increases were incurred to support our AI initiatives.**"
- Gross margin "decreased 4%... primarily due to the increased cost of revenue incurred to support our AI initiatives."
- Revenue increased **$10.7 million**, of which **$8.4 million** subscription; of that, **$7.1 million** from new subscription customers and **$1.3 million** from expansion of existing customers.
- R&D increased $11.7 million, including a **$9.6 million** increase in stock-based compensation and a **$1.1 million** increase in hosting and software costs.
- G&A increased $3.3 million, including a **$2.2 million** increase in legal expenses.
- Tax increase "primarily driven by reduced tax deductions from stock award activities and lower research and development tax credits."

### 1.3 From Exhibit 99.1 (accession 0001516513-26-000038)

| Fact | Value |
|---|---|
| Adjusted EBITDA | $74,773 thousand (prior year $79,772) |
| Adjusted EBITDA margin | 47.7% vs 54.7% |
| Net income margin | 15.5% vs 36.5% |
| Operating cash flow | $41,987 thousand vs $62,101 |
| Free cash flow | $39,603 thousand vs $60,135 |
| Diluted EPS | $0.13 vs $0.27 |
| Q2 FY2027 revenue guidance | $170–171 million |
| Q2 FY2027 adjusted EBITDA guidance | $80.5–81.5 million |
| FY2027 revenue guidance | $671–681 million |
| FY2027 adjusted EBITDA guidance | $309–329 million |
| Network coverage | more than 85% of U.S. physicians |

**CEO quote, reproduced in full and attributed:**

> "We're proud that our clinical AI assistant, Doximity Ask, was the top-performing U.S.-based model in the NOHARM benchmark while we delivered another quarter of record engagement... In Q1 we had accelerated revenue growth along with workflow active prescriber growth of more than 30% year-over-year and AI Search query growth of over 25% quarter-over-quarter."
> — Jeff Tangney, co-founder and CEO

### 1.4 From the Form 10-K (accession 0001516513-26-000025)

| Fact | Value |
|---|---|
| FY2026 total revenue | $570,399 thousand |

### 1.5 Mechanical term counts

Computed by case-insensitive count against the parsed full text of each document. These are measurements of the documents, not interpretations:

| Term | 10-Q | 10-K | Press release |
|---|---|---|---|
| NOHARM | 0 | 0 | 1 |
| AI Search | 0 | 0 | 1 |
| prescriber | 0 | 0 | 1 |
| Doximity Ask | 0 | 0 | 1 |

---

## Part 2 — Derived figures

Computed by `verify.py` from Part 1 inputs. Every one is reproducible by running the gate. None is estimated.

### 2.1 Growth and margins

| Figure | Value |
|---|---|
| Revenue growth | 7.34% |
| Cost of revenue growth | 50.02% |
| Gross profit growth | 2.16% |
| Operating expense growth | 31.32% |
| Net income change | −54.40% |
| Adjusted EBITDA change | −6.27% |
| Free cash flow change | −34.14% |
| Stock-based compensation growth | 68.09% |
| R&D stock compensation growth | 134.01% |
| Gross margin | 84.87% vs 89.18% (−4.31pp) |
| Operating margin | 21.48% vs 37.36% (−15.88pp) |
| Net margin | 15.53% vs 36.54% (−21.01pp) |
| Adjusted EBITDA margin | 47.74% vs 54.67% (−6.93pp) |
| Free cash flow margin | 25.29% vs 41.21% (−15.92pp) |
| Effective tax rate | 39.76% vs 16.88% (+22.88pp) |

### 2.2 The AI cost findings

| Figure | Value |
|---|---|
| Disclosed AI cost of revenue | $6.40M |
| Share of the cost-of-revenue increase | 81.01% |
| Share of Q1 revenue | 4.09% |
| Share of the revenue increase | 59.79% |
| Gross margin excluding disclosed AI cost | 88.96% |
| **AI share of the gross-margin contraction** | **94.95%** |
| Total hosting increase (COGS + R&D) | $6.00M |
| Hosting increase as share of revenue increase | 56.05% |

### 2.3 Adoption versus monetisation

| Figure | Value |
|---|---|
| Adoption growth minus revenue growth | 24.66pp |
| Adoption growth as a multiple of revenue growth | 4.36× |
| New-customer share of subscription growth | 84.52% |
| Expansion share of subscription growth | 15.48% |
| NRR change | −11.00pp |
| Decline in expansion above par | 61.11% |

### 2.4 Earnings decline decomposition

| Driver | Share of the $29.005M decline |
|---|---|
| Increase in stock-based compensation | 51.33% |
| Disclosed AI cost of revenue | 22.07% |
| Increase in tax provision | 18.00% |

### 2.5 Guidance arithmetic

| Figure | Value |
|---|---|
| FY2027 revenue guidance midpoint | $676.00M |
| Implied FY2027 growth | 18.51% |
| Revenue implied for the remaining nine months | $519.38M |
| Actual prior-year comparable nine months | $424.49M |
| Required growth, remaining nine months | 22.35% |
| Acceleration required vs Q1 | +15.02pp (3.05×) |
| Implied Q2 sequential growth | 8.86% |

### 2.6 Capital allocation

| Figure | Value |
|---|---|
| Implied average repurchase price | $20.82 |
| Repurchases as a share of free cash flow | 231.30% |
| Equity change | −3.66% |
| Accumulated deficit widening | $67.982M |
| Deficit widening plus earnings ÷ cash repurchases | 1.01× |
| AR increase growth | +149.11% |
| AR increase as a multiple of net income | 1.37× |

### 2.7 A note on rounded intermediates

Three derived figures — `implied_accel_vs_q1_pp` (15.02), `implied_accel_multiple` (3.05) and `ai_share_of_gm_contraction_pct` (94.95) — are computed from **unrounded** inputs. Deriving them from the two-decimal values published elsewhere in the README produces different answers (15.01, 3.04 and 94.90 respectively). The gate carries explicit comments at each of these three checks. The unrounded computation is authoritative.

One figure, the Guardrail 1 headroom, lands exactly on a rounding boundary: $10.705M − $6.400M = **$4.305M**. It is asserted at three decimal places and written as $4.305M throughout, so that no ambiguously rounded two-decimal value enters the document.

---

## Part 3 — Author constructs

**None of the following is disclosed data.** All of it is the author's own analytical work, presented as argument rather than fact.

### 3.1 Frameworks applied

RICE, MoSCoW, Kano, JTBD, AARRR, HEART, Porter's Five Forces, Business Model Canvas, SWOT and the PRD in section 37 are analytical frameworks applied by the author. Doximity does not publish any of these.

### 3.2 RICE inputs

Every Reach, Impact, Confidence, Effort and stress value in section 34 is an author estimate:

| ID | R | I | C | E | Stress |
|---|---|---|---|---|---|
| P1 | 127 | 3.0 | 0.85 | 4.0 | 0.90 |
| P2 | 127 | 2.5 | 0.80 | 6.0 | 0.85 |
| P3 | 127 | 2.0 | 0.90 | 3.0 | 0.95 |
| P4 | 127 | 2.0 | 0.75 | 5.0 | 0.80 |
| P5 | 127 | 3.0 | 0.60 | 12.0 | 0.45 |

Reach is held at 127 — the disclosed count of customers with ≥$500k TTM revenue — because every proposal is a disclosure or pricing change whose audience is that buyer set. This is a modelling choice, not a disclosed reach figure.

The stress factors encode the author's judgment about how much of each proposal's value depends on claims that are currently quote-only, plus execution risk. **P5 ranks last under stress by 71.88%**, and that ranking is asserted programmatically by the gate rather than argued in prose, per series rule. The ordering is stable between base and stressed rankings.

### 3.3 Personas

Dr. Anita R., Marcus T. and Priya S. are **composite constructions**. They are not real individuals, not customer research, and not drawn from any Doximity disclosure. Their jobs-to-be-done are inferred from the product descriptions in 10-Q Note 3 and from the revenue model. They are a device for reasoning about a two-sided network in which the user and the payer are different people.

### 3.4 Proposed North Star and guardrails

"Audited AI-attributable subscription revenue per active AI provider" is the author's proposal. The gate asserts `north_star_computable_today = False` precisely because it cannot be computed from disclosure — that is the argument for it, not a defect.

Guardrail 1 (AI cost as a share of incremental revenue, breach at 100%), Guardrail 2 (expansion share floor at 30%) and Guardrail 3 (gross margin excluding AI cost) are author constructs. Guardrail 1's **current value of 59.79%** is derived from disclosed figures; the **100% threshold** is the author's.

### 3.5 Scenario parameters

All three scenarios in section 47 are author constructs applying arithmetic to filed inputs:

- **Scenario A** assumes AI cost of revenue doubles with the revenue delta unchanged. The doubling is arbitrary and illustrative.
- **Scenario B** assumes the Q1 growth rate persists for the full year. This is explicitly noted as likely to understate the outcome, because Doximity's revenue is seasonally back-half weighted.
- **Scenario C** applies the author's own 30% expansion-share floor.
- The sensitivity figure (**14.67%** revenue growth needed to absorb doubled AI cost at a constant guardrail) is arithmetic on author-chosen parameters.

None of these is a forecast. None reflects company guidance beyond the disclosed ranges.

### 3.6 Eval plan, failure modes, human-in-the-loop design

Sections 28, 29 and 30 are entirely the author's product judgment. Doximity discloses no evaluation methodology, no failure-mode analysis and no review-loop instrumentation. The failure-mode ranking is by the author's estimate of expected harm. No clinical expertise is claimed and none of this should be read as a clinical assessment.

### 3.7 Recommendations and roadmap

All seven recommendations, the MoSCoW allocation, the three-horizon roadmap and its sequencing logic are the author's. Doximity has not proposed, commented on or adopted any of them.

### 3.8 The disclosure ladder

The three-rung ladder in section 41 is the author's framing of a pattern observed across Days 80, 81 and 82. It is an interpretation, not a disclosed relationship between three unrelated companies.

---

## Part 4 — Unavailable information

Stated explicitly rather than estimated. The series rule is that a gap is reported as a gap.

| Not disclosed | Consequence |
|---|---|
| AI-attributable revenue | Return on AI investment cannot be computed |
| Absolute count of active providers | Only the growth rate is given; no denominator exists |
| Count of Ask / Scribe / PeerCheck users specifically | AI adoption cannot be separated from fax and Dialer usage |
| Cost per AI interaction | Every numerator is available; no denominator is |
| Any clinical accuracy, safety or time-saved outcome | Product efficacy is unassessable from filings |
| NOHARM benchmark methodology, date or comparator set | The claim cannot be independently situated |
| Definition of "prescriber" | The CEO's 30% figure cannot be reconciled to the filing |
| AI Search query base | A 25% QoQ figure on an undisclosed base |
| Whether AI sessions generate advertising impressions | The highest-value unknown in the business model |
| Remaining performance obligations | ASC 606 practical expedient elected; no backlog to check guidance against |
| FY2026 quarterly revenue splits | Seasonality analysis is qualitative, not quantitative |
| Workflow Solutions revenue separately | AI is bundled inside it |
| FDA classification discussion for "clinical decision support" | Regulatory positioning is not addressed in the 10-Q |

**No figure in this case study fills any of these gaps by estimation.** Where the README discusses these subjects, it states that the information is unavailable.

---

## Part 5 — Deliberate exclusions

Information that exists and was not used, with the reason.

| Excluded | Reason |
|---|---|
| Prepared remarks and "Modeling Considerations" appendix | Not an SEC filing; outside this series' primary-source rule |
| Earnings conference call commentary | Same |
| Share price, market capitalisation, valuation multiples | This series does not use market data |
| Analyst estimates and price targets | Not primary sources |
| News coverage and commentary | Not primary sources |
| Third-party data aggregators | Not primary sources |
| Product screenshots | The case study concerns disclosure, not interface |
| 10-K risk-factor text | Searched for AI term counts only; not otherwise analysed |
| Prior-quarter 10-Qs | Scope is the June 2026 quarter |
| Competitor filings | Day 83 covers OpenEvidence separately and on its own evidence |

### 5.1 On the Day 80 and Day 81 comparators

The comparator figures used in section 42 — Hims & Hers' **59.43%** acquisition share, Hinge Health's **3.00%** residual and **97%** human-hour reduction — are **recomputed inside this case study's own `verify.py`** rather than carried across as prose assertions from earlier documents. This is a series rule: no case study asserts a number that its own gate has not verified.

---

## Verification statement

`verify.py` contains **310 checks** and exits non-zero on any failure. It asserts:

- internal consistency of every as-filed statement (gross profit, operating expenses, operating income, pre-tax income, net income, revenue disaggregation, stock-compensation components, the balance-sheet identity, the free-cash-flow bridge, and the adjusted EBITDA reconciliation rebuilt from its components);
- every growth rate, margin and ratio quoted in the README and in this file;
- the four AI term counts, in all three documents;
- the RICE base and stressed scores, both rankings, the identity of the proposal ranking **last** under stress, and the margin by which it ranks last;
- the scenario and sensitivity arithmetic;
- the Day 80 and Day 81 comparators.

`crosscheck.py` independently extracts every two-decimal figure from `README.md` and `ASSUMPTIONS.md` and confirms each traces to a value the gate computed. A figure in the prose that the gate does not produce is a build failure, not a rounding difference.

**Fabricated figures in this case study: 0.**

---

*Day 82 of 90. Doximity, Inc. (NYSE: DOCS). Q1 FY2027, quarter ended 30 June 2026.*
