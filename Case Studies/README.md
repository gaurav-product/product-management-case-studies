# Day 82 — Doximity, Inc. (NYSE: DOCS)

### The cost of AI is audited. The claims about it are not.

> **90-Day PM Case Study Challenge — Day 82**
> Evidence-based product teardown built only from primary-source filings.
> Every derived figure in this document is produced by `verify.py` (310 programmatic checks) before a word of prose was written. No figure appears here that the gate has not computed.

---

## 1. One-paragraph summary

In the quarter ended 30 June 2026, Doximity told two stories about artificial intelligence in two different documents. In the press release, the CEO said the company's clinical AI assistant was the top-performing U.S.-based model on an external benchmark, that workflow active prescribers grew more than 30% year over year, and that AI Search queries grew over 25% quarter over quarter. In the Form 10-Q filed the same week, none of those claims appear — not the benchmark, not the product name, not the search metric, not the word "prescriber." What *does* appear in the 10-Q is the bill: a **$4.9M** increase in hosting and software costs and a **$1.5M** increase in amortisation, both of which management states were "incurred to support our AI initiatives." Those two lines are **81.01%** of the entire cost-of-revenue increase and account for **94.95%** of the gross-margin contraction. Revenue grew **7.34%**. Net income fell **54.40%**. This is the first company in this series where the *cost* of AI is disclosed in a reviewed filing while every *claim* about AI performance lives only in an unaudited quote — and it completes a three-part arc that began on Day 80.

---

## 2. Why this product, on this day

Days 80, 81 and 82 were selected as a deliberate sequence, not three independent teardowns. Each company sells a healthcare product whose central marketing claim is about AI. The question asked of each was identical: **where, exactly, does the AI claim live, and what is it a claim about?**

| Day | Company | AI positioning | What the filings actually disclose |
|---|---|---|---|
| 80 | Hims & Hers | "Doctor-led AI clinical engine" | No AI metric of any kind |
| 81 | Hinge Health | AI reduces human care delivery | A **cost** metric (human care hours), no outcome metric |
| 82 | **Doximity** | AI adoption across the physician network | **Cost disclosed in the 10-Q; every performance claim quote-only** |

Doximity is the strongest case of the three because it is the only one that discloses a specific dollar cost attributable to AI. That makes the asymmetry measurable rather than rhetorical. We can say precisely what the AI cost and precisely what was claimed for it — and observe that those two things were published in different documents under different standards of legal responsibility.

---

## 3. Company identification

| Field | Value | Source |
|---|---|---|
| Legal name | Doximity, Inc. | 10-Q cover |
| CIK | 0001516513 | EDGAR |
| Exchange / ticker | NYSE: DOCS | 10-Q cover |
| State of incorporation | Delaware (April 2010, as 3MD Communications, Inc.) | 10-Q Note 1 |
| Headquarters | San Francisco, California | 10-Q Note 1 |
| Fiscal year end | 31 March | 10-K |
| SIC code | 7371 — Services-Computer Programming Services | EDGAR submissions |
| Period analysed | Q1 FY2027, three months ended 30 June 2026 | 10-Q |

### 3.1 Register classification note

Doximity is registered under SIC **7371 — Services-Computer Programming Services**. It is a two-sided network whose revenue comes overwhelmingly from pharmaceutical marketing subscriptions, with health-system workflow software as a secondary line. A code describing custom programming services captures neither the advertising economics that produce the revenue nor the clinical-software exposure that produces the risk.

This is the eleventh company in this series filed under a code that materially misdescribes its business model. The running tally now stands at **11 of 82** companies examined, across both the Indian NIC and US SIC registers. The pattern matters for a product manager because register codes drive comparable-company screens, index inclusion and, in some markets, regulatory scope. A product whose register code says "programming services" is not screened as an advertising business, and its margin structure will look anomalous to anyone who benchmarks it against one.

---

## 4. What Doximity actually sells

Doximity operates a professional network for U.S. medical professionals. Its membership includes more than 85% of U.S. physicians. Revenue comes from three subscription solutions:

**Marketing Solutions.** Pharmaceutical companies and health systems buy the ability to place sponsored content in front of targeted physicians. Contracts are generally 12 months or less. Modules are sold as Newsfeed, Workflow and Peer. Pricing is based on the number and composition of targeted members and on which modules are bought. This is the revenue engine.

**Hiring Solutions.** Recruiters buy access to the professional database to post jobs and send a fixed number of monthly messages.

**Workflow Solutions.** Health systems and hospitals buy telehealth tools, on-call scheduling (Amion), and the Clinical AI Suite — Dialer, Scribe and Ask. **This is where the AI lives, and it is bundled.**

### 4.1 The structural fact that governs everything else

The Clinical AI Suite is not a separate revenue line. It is a component of a Workflow Solutions subscription, sold for a specified number of users over the contract term, recognised ratably. There is no disclosed AI revenue, no disclosed AI ARPU, and no disclosed count of AI-specific seats.

The gate asserts this directly:

```
ai_revenue_line_disclosed                    = False
active_provider_absolute_count_disclosed     = False
only_provider_growth_rate_disclosed          = True
```

A product manager reading this should register the consequence immediately: **you cannot compute the unit economics of Doximity's AI from public disclosure.** You can compute its cost, because the cost is narrated in MD&A. You cannot compute its revenue, because the revenue is not separated. Every statement about AI paying for itself at this company is, on public information, unfalsifiable.

---

## 5. Problem statement

Doximity's AI products address a real and well-documented problem. Physicians spend substantial time on documentation, clinical reference lookup, on-call coordination and patient communication. The Clinical AI Suite targets each: Scribe for ambient note-taking, Ask for clinical reference and writing assistance, Dialer for patient contact, Amion for scheduling.

The product problem is genuine. The *disclosure* problem is the subject of this case study, and it is separate. A product can solve a real problem and still be reported in a way that makes its performance impossible for an outsider to assess. Both things are true here.

---

## 6. The central finding, stated precisely

### 6.1 The cost of AI, as filed

From the 10-Q MD&A, cost of revenue discussion:

> Cost of revenue for the three months ended June 30, 2026 increased $7.9 million as compared to the same period in 2025. The increase was primarily driven by a $4.9 million increase in hosting and software costs and a $1.5 million increase related to amortization of an acquired intangible and internally-developed software. Both increases were incurred to support our AI initiatives.

And on gross margin:

> Gross margin for the three months ended June 30, 2026 decreased 4% as compared to the same period in 2025, primarily due to the increased cost of revenue incurred to support our AI initiatives.

This is an unusually direct disclosure. Management attributes a specific dollar amount to AI and states that AI caused the margin decline. The gate quantifies it:

| Measure | Value |
|---|---|
| Disclosed AI cost inside cost of revenue | **$6.40M** |
| Share of the total cost-of-revenue increase | **81.01%** |
| Non-AI portion of that increase | **$1.50M** |
| AI cost as a share of Q1 revenue | **4.09%** |
| AI cost as a share of the *revenue increase* | **59.79%** |

That last row is the one to sit with. Revenue rose $10.705M year over year. The disclosed AI cost of revenue was $6.40M. **Roughly sixty cents of every incremental revenue dollar was matched by disclosed AI cost of revenue alone** — before any of the AI-related R&D, and before sales, marketing or overhead.

### 6.2 The gross-margin bridge

| Measure | Value |
|---|---|
| Gross margin, Q1 FY2027 | **84.87%** |
| Gross margin, Q1 FY2026 | **89.18%** |
| Contraction | **−4.31pp** |
| Gross margin excluding the disclosed AI cost | **88.96%** |
| Contraction attributable to disclosed AI cost | **4.09pp** |
| **AI share of the gross-margin contraction** | **94.95%** |

Strip out the $6.40M that management attributes to AI, and gross margin would have been 88.96% against 89.18% — essentially flat. **Almost the entire margin story of this quarter is the cost of AI.** Management says so. The filing supports it arithmetically.

### 6.3 Where the AI *claims* live

Now the other side. Four claims carried the AI narrative into the market. Here is where each appears, counted mechanically across the parsed text of all three primary documents:

| Claim / term | 10-Q | 10-K | Press release |
|---|---|---|---|
| NOHARM (the benchmark) | **0** | **0** | 1 |
| "AI Search" | **0** | **0** | 1 |
| "prescriber" | **0** | **0** | 1 |
| "Doximity Ask" | **0** | **0** | 1 |

```
audited_ai_claim_count      = 0
quote_only_ai_claim_count   = 4
ai_cost_disclosed_in_10q    = True
ai_performance_claims_in_10q = False
```

All four appear **exactly once each**, and all four appear in **the same place**: a single CEO quote in the earnings press release.

> "We're proud that our clinical AI assistant, Doximity Ask, was the top-performing U.S.-based model in the NOHARM benchmark while we delivered another quarter of record engagement... In Q1 we had accelerated revenue growth along with workflow active prescriber growth of more than 30% year-over-year and AI Search query growth of over 25% quarter-over-quarter."
> — Jeff Tangney, co-founder and CEO, Exhibit 99.1

The asymmetry is the finding. **The money AI costs is in the document reviewed by auditors and signed under Sarbanes-Oxley certification. The performance of AI is in the document that is not.**

I want to be careful about what this does and does not mean. A press release quote is a legitimate place for a CEO to characterise the business, and forward-looking-statement safe harbours exist precisely so executives can speak about performance without every sentence becoming a liability. Nothing here suggests any claim is false. The NOHARM result may be entirely accurate. The point is narrower and, for a product manager, more useful: **a claim's location tells you what standard of evidence it was held to, and these four claims were held to a different standard than the cost figure they are meant to justify.**

---

## 7. Adoption is not monetisation

The 10-Q does disclose one adoption metric, and it is a strong one:

> Quarterly unique active providers using our workflow tools increased approximately 32% year-over-year compared to June 30, 2025, reflecting continued provider engagement and adoption of our clinical workflow tools across the physician network, including the growing impact of AI suite usage.

Set that against the revenue line:

| Measure | Value |
|---|---|
| Quarterly unique active providers, YoY | **~32%** |
| Revenue, YoY | **7.34%** |
| Gap | **24.66pp** |
| Adoption growth as a multiple of revenue growth | **4.36×** |

Providers adopted the workflow tools more than four times faster than revenue grew. In a usage-priced product that gap would be a leading indicator — engagement today, revenue tomorrow. But Workflow Solutions is **not usage-priced**. It is sold "for a specified number of users throughout the subscription period" and recognised ratably. A provider who submits ten prompts on Ask instead of one generates the same revenue and more cost.

This is the structural inversion at the heart of Day 82. **Under a seat-based contract with a variable-cost AI feature, adoption is a cost event before it is a revenue event.** The 32% is not free. It is, in part, the $4.9M hosting line.

### 7.1 The metric definition itself deserves scrutiny

The 10-Q defines a "unique active provider" as one who, during the quarter, did any of the following: placed a phone or video call lasting **more than 10 seconds**; sent a voicemail; sent a secure text; sent or received a fax; submitted a prompt on Ask; researched a prescription drug; reviewed an AI response for PeerCheck; scheduled via Amion; or used Scribe for a patient visit. Each provider is counted once per quarter regardless of how many tools they use or how often.

Read that list again. **Sending a fax counts. An eleven-second phone call counts.** Amion, the on-call scheduling tool, is an established product that predates the AI suite entirely — and any Amion login counts.

So a metric that management describes as reflecting "the growing impact of AI suite usage" is a union of nine behaviours, of which three are AI, and the threshold for the largest non-AI behaviour is ten seconds. The 10-Q's own hedging is notable: it warns the metric "may fluctuate on a quarterly basis due to seasonal patterns... including weather-related variability in Dialer usage."

A metric whose movement can be explained by the weather is not an AI metric.

### 7.2 The quote metric and the filing metric are different metrics

The CEO quote says **"workflow active prescriber growth of more than 30% year-over-year."** The 10-Q says **"quarterly unique active providers... increased approximately 32%."**

```
quote_metric_population_matches_filing = False
providers_minus_prescribers_pp         = 2.00
aisearch_is_qoq_not_yoy                = True
```

These are different populations. The 10-Q defines *providers* as physicians, nurse practitioners, CRNAs, physician assistants, pharmacists and medical students. *Prescribers* is a narrower set. The filing does not disclose a prescriber metric at all — the word does not appear in it. So the quote's 30% figure cannot be reconciled to, or checked against, anything in the reviewed document.

And the third claim is a different shape again: AI Search query growth of "over 25%" is **quarter-over-quarter**, not year-over-year, in a quote where the two other figures are annual. A sequential growth rate on an undisclosed base, presented alongside annual rates, is the least checkable of the three.

---

## 8. What happened to the money

The quarter's income statement, as filed (in thousands):

| Line | Q1 FY2027 | Q1 FY2026 | Change |
|---|---|---|---|
| Revenue | 156,618 | 145,913 | **+7.34%** |
| Cost of revenue | 23,692 | 15,793 | **+50.02%** |
| Gross profit | 132,926 | 130,120 | **+2.16%** |
| Research and development | 38,477 | 26,799 | **+43.58%** |
| Sales and marketing | 45,049 | 36,365 | **+23.88%** |
| General and administrative | 15,756 | 12,439 | **+26.67%** |
| Total operating expenses | 99,282 | 75,603 | **+31.32%** |
| Income from operations | 33,644 | 54,517 | **−38.29%** |
| Other income, net | 6,719 | 9,630 | **−30.23%** |
| Provision for income taxes | 16,048 | 10,827 | **+48.22%** |
| **Net income** | **24,315** | **53,320** | **−54.40%** |

Every expense line grew faster than revenue. Every single one. Revenue grew 7.34%; the slowest-growing cost line grew 23.88%.

### 8.1 Margin cascade

| Margin | Q1 FY2027 | Q1 FY2026 | Change |
|---|---|---|---|
| Gross | 84.87% | 89.18% | **−4.31pp** |
| Operating | 21.48% | 37.36% | **−15.88pp** |
| Net | 15.53% | 36.54% | **−21.01pp** |
| Adjusted EBITDA | 47.74% | 54.67% | **−6.93pp** |
| Free cash flow | 25.29% | 41.21% | **−15.92pp** |

The compression widens at every level. Gross margin fell 4.31pp; net margin fell 21.01pp — nearly five times as much. Costs below the gross line did the greater damage.

### 8.2 Cost structure as a share of revenue

| Line | Q1 FY2027 | Q1 FY2026 |
|---|---|---|
| Cost of revenue | 15.13% | 10.82% |
| R&D | 24.57% | 18.37% |
| S&M | 28.76% | 24.92% |
| G&A | 10.06% | 8.52% |
| Total opex | 63.39% | 51.81% |

Operating expenses moved from just over half of revenue to nearly two-thirds in twelve months.

---

## 9. Decomposing the earnings decline

Net income fell by **$29.005M**. Three identifiable forces account for the bulk of it:

| Driver | Amount | Share of the decline |
|---|---|---|
| Increase in stock-based compensation | $14.887M | **51.33%** |
| Disclosed AI cost of revenue | $6.400M | **22.07%** |
| Increase in tax provision | $5.221M | **18.00%** |

Stock-based compensation is the single largest driver — larger than AI cost. This matters for how the quarter is read, and it cuts against a simple "AI destroyed the margins" narrative. It would be wrong to say AI caused the earnings decline. AI caused most of the *gross-margin* decline (94.95%); stock compensation caused most of the *net income* decline (51.33%).

Holding both findings at once is the honest reading.

### 9.1 Stock-based compensation detail

| Line | Q1 FY2027 | Q1 FY2026 | Change |
|---|---|---|---|
| Cost of revenue | 3,192 | 2,980 | +7.11% |
| Research and development | 15,559 | 6,649 | **+134.01%** |
| Sales and marketing | 12,425 | 7,710 | +61.15% |
| General and administrative | 5,576 | 4,526 | +23.20% |
| **Total** | **36,752** | **21,865** | **+68.09%** |

| Measure | Value |
|---|---|
| SBC as a share of revenue, Q1 FY2027 | **23.47%** |
| SBC as a share of revenue, Q1 FY2026 | **14.98%** |
| Change | **+8.49pp** |
| SBC share of the operating-expense increase | **61.97%** |

R&D stock compensation grew **134.01%** — more than doubling — driven by new service-based and performance-based awards to new hires and existing employees. Nearly a quarter of every revenue dollar is now paid out in stock.

### 9.2 The measure that removes the largest driver

Adjusted EBITDA excludes stock-based compensation by definition. The gate makes the consequence explicit:

```
adjebitda_excludes_pct_of_ni_decline = 51.33
```

**The non-GAAP metric management guides to excludes the single largest contributor to the earnings decline.** Adjusted EBITDA fell 6.27%; net income fell 54.40%. Both numbers are correctly calculated. They describe the same quarter. An analyst modelling off adjusted EBITDA sees a mild softening; one modelling off net income sees earnings cut in half.

This is not an accusation — the reconciliation is fully disclosed in the press release and the 10-Q, exactly as required, and the definition is stable across periods. It is an observation about which number travels. Adjusted EBITDA is the one in the guidance.

---

## 10. Where the growth came from

From the 10-Q MD&A revenue discussion:

> Revenue for the three months ended June 30, 2026 increased $10.7 million... The increase was primarily driven by a $8.4 million increase in subscription revenue. Of the increase in subscription revenue, $7.1 million was driven by the addition of new subscription customers and $1.3 million was due to the expansion of existing customers.

| Measure | Value |
|---|---|
| New subscription customers' share of subscription growth | **84.52%** |
| Existing-customer expansion share | **15.48%** |
| Subscription share of total revenue growth | **78.50%** |
| Non-subscription share of total growth | **21.50%** |

**84.52% of subscription growth came from customers who did not exist a year ago.** Expansion within the installed base — the thing a network effect is supposed to produce, and the thing an AI feature is supposed to accelerate — contributed 15.48%.

### 10.1 The Day 80 comparison

Day 80 found that 59.43% of Hims & Hers' growth was acquired rather than expanded. Doximity's figure is **84.52%** — a gap of **25.09pp**. Doximity, the company with the deeper network, the higher switching costs and the more embedded workflow products, is *more* dependent on new-logo acquisition than the direct-to-consumer telehealth company.

### 10.2 Net revenue retention

| Measure | 30 June 2026 | 30 June 2025 |
|---|---|---|
| Net revenue retention rate | **107%** | **118%** |

| Derived | Value |
|---|---|
| Change | **−11.00pp** |
| Expansion above par, FY2027 | **7.00pp** |
| Expansion above par, FY2026 | **18.00pp** |
| **Decline in expansion above par** | **61.11%** |

NRR at 107% still means the installed base grew. But the *expansion component* — the part above 100% that measures whether existing customers buy more — fell by **61.11%** in one year.

This is the finding that most directly contradicts the AI narrative. If a clinical AI suite were driving customers to buy more, it would appear here. Over the year in which provider adoption grew ~32% and the AI suite was rolled out, the rate at which existing customers expanded their spending fell by nearly two-thirds.

### 10.3 Customer concentration

| Measure | 30 June 2026 | 30 June 2025 |
|---|---|---|
| Customers with ≥$500,000 TTM subscription revenue | **127** | **119** |

Growth of **6.72%** — eight customers. This cohort accounted for approximately 83% of revenue for the trailing twelve months. No single customer represented 10% or more of revenue or accounts receivable.

So: 127 customers produce roughly 83% of revenue. The network has more than 85% of U.S. physicians on one side and about 127 economically meaningful buyers on the other. **The AI suite is consumed by the side of the network that does not pay.**

That sentence is the business model in one line, and it explains why adoption and revenue have decoupled. Doximity's AI is used by physicians. Doximity's revenue comes from pharmaceutical marketers and health systems. Physician adoption only converts to revenue if it makes the *advertising inventory* more valuable or the *Workflow contracts* larger — and in the quarter measured, expansion revenue fell.

---

## 11. Revenue disaggregation

| Line (thousands) | Q1 FY2027 | Q1 FY2026 | Change |
|---|---|---|---|
| Subscription | 146,300 | 137,876 | **+6.11%** |
| Other | 10,318 | 8,037 | **+28.38%** |
| **Total** | **156,618** | **145,913** | **+7.34%** |

"Other" revenue consists of fees from temporary staffing and permanent placement of healthcare professionals. It grew **28.38%** — more than four times the subscription growth rate — and contributed **21.50%** of the total revenue increase.

Approximately 93% of revenue came from subscription customers. The fastest-growing revenue line in the quarter was a staffing business, not a software business, and certainly not an AI business.

---

## 12. Cash flow and working capital

| Measure (thousands) | Q1 FY2027 | Q1 FY2026 | Change |
|---|---|---|---|
| Net cash from operating activities | 41,987 | 62,101 | **−32.39%** |
| Purchases of property and equipment | (62) | — | |
| Internal-use software development costs | (2,322) | (1,966) | |
| **Free cash flow** | **39,603** | **60,135** | **−34.14%** |

| Margin | Q1 FY2027 | Q1 FY2026 |
|---|---|---|
| Operating cash flow margin | 26.81% | 42.56% |
| Free cash flow margin | 25.29% | 41.21% |

### 12.1 The receivables signal

| Measure | Value |
|---|---|
| Increase in accounts receivable, Q1 FY2027 | **$33.334M** |
| Increase in accounts receivable, Q1 FY2026 | **$13.381M** |
| Growth in the receivables build | **+149.11%** |
| AR increase as a share of quarterly revenue | **21.28%** |
| AR increase as a multiple of net income | **1.37×** |

The receivables build grew **149.11%** against revenue growth of 7.34%. The quarter's increase in accounts receivable was **1.37 times the entire quarter's net income**. Management attributes this to "the timing of billings and collections."

That explanation is plausible and may well be complete. It is also the single largest reason operating cash flow fell by a third while revenue rose. A product manager should treat it as a watch item rather than a finding: one quarter of receivables timing is noise, two is a pattern, three is a collections problem.

### 12.2 Deferred revenue

| Measure | Value |
|---|---|
| Deferred revenue, current, 30 Jun 2026 | $109.061M |
| Deferred revenue, current, 31 Mar 2026 | $106.050M |
| Change | **+2.84%** |
| Revenue recognised from opening deferred revenue, Q1 FY2027 | $69.5M |
| Revenue recognised from opening deferred revenue, Q1 FY2026 | $77.8M |
| Change | **−10.67%** |

Deferred revenue grew 2.84% while revenue grew 7.34%, and the amount recognised out of the opening balance fell **10.67%**. Because the majority of contracts run twelve months or less, Doximity elects the ASC 606 practical expedient and does not disclose remaining performance obligations. **There is no RPO backlog to check the guidance against.**

---

## 13. Guidance, and the arithmetic it requires

| Guidance | Low | High | Midpoint |
|---|---|---|---|
| Q2 FY2027 revenue | $170.0M | $171.0M | **$170.50M** |
| Q2 FY2027 adjusted EBITDA | $80.5M | $81.5M | **$81.00M** |
| FY2027 revenue | $671.0M | $681.0M | **$676.00M** |
| FY2027 adjusted EBITDA | $309.0M | $329.0M | **$319.00M** |

FY2026 actual revenue was **$570.399M**. The FY2027 midpoint implies growth of **18.51%**.

Q1 delivered **7.34%**.

### 13.1 The implied acceleration

| Measure | Value |
|---|---|
| Revenue implied for the remaining nine months of FY2027 | **$519.38M** |
| Actual revenue in the corresponding nine months of FY2026 | **$424.49M** |
| **Required growth over the remaining nine months** | **22.35%** |
| Acceleration required versus Q1 actual | **+15.02pp** |
| As a multiple of the Q1 growth rate | **3.05×** |

To reach the midpoint of its own full-year guidance, Doximity must grow the remaining nine months at **more than three times** the rate it just delivered. Q2 guidance alone implies **8.86%** sequential growth off the Q1 actual.

This is not necessarily implausible. Doximity's revenue is seasonal — pharmaceutical marketing budgets concentrate in the second half of the fiscal year, and the company has historically grown into the back half. The 10-K would support a seasonality argument. But the guidance is the claim, and the claim requires a tripling of the growth rate, against a backdrop where net revenue retention fell 11.00pp and expansion revenue contributed only 15.48% of subscription growth.

### 13.2 The width of the EBITDA range

| Measure | Value |
|---|---|
| FY2027 revenue guidance range | $10.00M |
| FY2027 adjusted EBITDA guidance range | $20.00M |
| EBITDA range as a share of its own midpoint | **6.27%** |
| Implied Q2 adjusted EBITDA margin | **47.51%** |
| Implied FY2027 adjusted EBITDA margin | **47.19%** |

The EBITDA range is **twice as wide in absolute dollars as the revenue range** it sits on. Management is more certain about what it will sell than about what it will cost to sell it.

For a company whose gross margin just fell 4.31pp on AI infrastructure it does not control the pricing of, a cost range twice as wide as the revenue range is a coherent and arguably candid signal. It is the most informative thing in the guidance.

---

## 14. Capital allocation

| Measure | Value |
|---|---|
| Buyback authorisation (Feb 2026 programme) | $500.0M |
| Shares repurchased and retired under it to 30 Jun 2026 | 4,759,886 |
| Aggregate purchase price | $99.1M |
| **Implied average price** | **$20.82** |
| Remaining authorised | $400.9M |
| Programme utilised | **19.82%** |
| Prior programme shares retired (completed Q4 FY2026) | **11.59M** |

Cash used for repurchases in the quarter was $91.6M, down **25.16%** year over year.

### 14.1 Buybacks against free cash flow

| Measure | Value |
|---|---|
| Free cash flow, Q1 FY2027 | $39.603M |
| Cash used for repurchases, Q1 FY2027 | $91.6M |
| **Repurchases as a share of free cash flow** | **231.30%** |
| Ratio | **2.31×** |
| Liquidity (cash, equivalents and marketable securities) | $687.8M |
| Quarters of repurchase at this rate, from liquidity alone | **7.51** |

Doximity spent **2.31 times its free cash flow** buying back stock in a quarter when free cash flow fell 34.14%. The balance was funded from the securities portfolio — investing activities provided $112.99M, almost entirely from maturities and sales of marketable securities.

This is affordable. With $687.8M of liquidity and no debt, the company can sustain this for many quarters. But it is worth naming plainly: **in the quarter Doximity's AI costs began to bite, it returned more than twice its free cash flow to shareholders and funded the difference by liquidating investments.** That is a capital-allocation choice that assumes the margin compression is temporary.

### 14.2 The equity account

| Measure | Value |
|---|---|
| Total stockholders' equity, 30 Jun 2026 | $916.070M |
| Total stockholders' equity, 31 Mar 2026 | $950.837M |
| Change | **−$34.767M (−3.66%)** |
| Additional paid-in capital change | **+$33.594M** |
| Accumulated deficit widening | **$67.982M** |
| Net income earned in the quarter | $24.315M |
| **Deficit widening plus earnings** | **$92.297M** |
| As a multiple of cash repurchases | **1.01×** |

Equity fell **3.66%** in a quarter in which the company earned $24.315M and added $33.594M to paid-in capital through stock compensation. The accumulated deficit widened by **$67.982M** despite positive earnings, because retired shares are charged against it. Adding back the quarter's earnings gives $92.297M — **1.01 times** the cash spent on repurchases, which is the expected relationship and confirms the mechanism.

Shares outstanding fell **1.75%**; the diluted weighted-average count fell **4.97%**. Diluted EPS of $0.13 against $0.27 is a **decline of roughly half**, cushioned by a share count that fell nearly 5%. Without the buyback, the EPS decline would have been steeper.

---

## 15. Tax

| Measure | Q1 FY2027 | Q1 FY2026 |
|---|---|---|
| Provision for income taxes | $16.048M | $10.827M |
| Income before income taxes | $40.363M | $64.147M |
| **Effective tax rate** | **39.76%** | **16.88%** |
| Change | **+22.88pp** | |

The effective rate more than doubled. Management attributes this to "reduced tax deductions from stock award activities and lower research and development tax credits, partially offset by lower income before taxes."

There is an irony worth noting. Stock compensation rose **68.09%** as an expense while the *tax deductions* from stock award activity fell — because those deductions depend on the share price at vesting or exercise, not on the accounting charge. The company is expensing more equity and deducting less of it. And R&D tax credits fell in a quarter when R&D spending rose **43.58%**, which suggests a change in the mix of qualifying activity or in credit availability rather than in effort.

The tax line contributed **18.00%** of the net income decline — more than a third as much as stock compensation, and it is the least discussed item in the quarter.

---

## 16. Contractual commitments for AI infrastructure

| Commitment | Value |
|---|---|
| Web hosting arrangement, 3 years ending 31 Dec 2027, annual commitment | $7M |
| Remaining commitment on that arrangement at 30 Jun 2026 | $7M |
| Second vendor, remaining commitment ending June 2028 | $6M |
| **Total named remaining commitments** | **$13.00M** |
| As a multiple of the quarter's disclosed AI cost of revenue | **2.03×** |

Total named cloud and vendor commitments are **$13.00M** — only **2.03 times** the AI cost of revenue recognised in a *single quarter* ($6.40M).

This is a genuinely important structural observation. Doximity's AI infrastructure spending is **largely uncommitted**. It is not locked into multi-year capacity purchases the way a company building its own model infrastructure would be. That is a real strategic advantage: the cost is variable and can be throttled. It is also a real strategic exposure: **the pricing is not locked either.** If inference prices rise, or if usage grows faster than expected, the cost line moves and there is no contractual ceiling.

The gate flags the ratio so the prose cannot overstate it in either direction. $13M of commitments against $6.40M of quarterly AI cost tells you the company has roughly two quarters of committed coverage at the current run rate — not that it has a small AI bill.

---

## 17. Litigation, and why it belongs in a product case study

This section would normally be a footnote. Here it is central, because of what the litigation is *about*.

### 17.1 The securities class action

From the 10-Q, Note 12:

> The operative complaint brought securities law claims on behalf of a putative class of investors who purchased Doximity securities between June 24, 2021 and August 8, 2023 against the Company and its Chief Executive Officer, **related to disclosures regarding user count and engagement rates.**

| Measure | Value |
|---|---|
| Settlement amount (funded by insurance carriers) | **$31.0M** |
| Settlement agreed | 24 December 2025 |
| Final court approval | **11 June 2026** |
| Case terminated | 23 June 2026 |
| Settlement as a multiple of this quarter's net income | **1.27×** |
| Shareholder derivative lawsuits still outstanding | **7** |

The settlement does not constitute an admission of liability, fault or wrongdoing, and the filing says so explicitly. Seven derivative lawsuits remain outstanding on a similar factual basis, and the company is unable to estimate any loss from them.

Now place the dates side by side. The securities class action concerning **user count and engagement rate disclosures** received final court approval on **11 June 2026** — nineteen days before the close of the quarter whose headline metric is a **user count growth rate**, presented in a CEO quote, defined in the 10-Q as a nine-behaviour union with a ten-second threshold, and hedged in the same filing as weather-sensitive.

I am not suggesting any impropriety. The current metric is defined in the filing with more precision and more caveats than most companies offer, and that carefulness is very plausibly a *consequence* of the litigation — a company that has just settled a case about user-count disclosure has every reason to define its user-count metric exhaustively.

But the product-management lesson is sharp and it is the reason this section exists: **Doximity has already paid $31M to settle a dispute about how it counted users, and its principal disclosed AI indicator is a count of users.** When you are choosing which metric will carry your product narrative, the question is not only "is it true?" It is "what happens when someone litigates its definition?"

### 17.2 The OpenEvidence litigation

On 20 June 2025, Doximity, its Chief Technology Officer and its Director of AI Products were named as defendants in *OpenEvidence Inc. v. Doximity, Inc. et al.* in the U.S. District Court for the District of Massachusetts. OpenEvidence alleges the defendants gained unauthorised access to its AI medical information platform, asserting claims under the Computer Fraud and Abuse Act, breach of contract, unjust enrichment and trespass to chattels. Doximity counterclaimed for false advertising under the Lanham Act, Massachusetts consumer protection law and common-law defamation.

On 22 January 2026 the court dismissed OpenEvidence's trespass-to-chattels claim and dismissed two of Doximity's counterclaims, but denied the motions to dismiss as to all other claims. On 26 May 2026 the court granted Doximity leave to amend its counterclaims to add allegations about OpenEvidence's alleged dissemination of false and misleading statements about Doximity. On 30 June 2026 the case was temporarily stayed pending mediation.

Two things follow. First, Doximity's Director of AI Products is personally named in active litigation about AI competitive conduct — an unusual level of individual exposure for a product role. Second, **OpenEvidence is Day 83 of this series.** Tomorrow's case study is about the company suing today's, and today's company is counter-suing it for false advertising about AI. The two teardowns will be read against each other deliberately.

### 17.3 Legal cost in the P&L

G&A rose $3.317M, of which **$2.2M** was an increase in legal expenses — **66.32%** of the G&A increase. Adjusted EBITDA excludes "legal fees associated with certain non-ordinary course legal matters including the shareholder class action litigation," so this cost, like stock compensation, is outside the guided metric.

---

## 18. User personas

Three personas matter, and only one of them pays.

### 18.1 Dr. Anita R. — the practising physician (uses, does not pay)

Mid-career internist at a 400-bed health system. Signed up to Doximity years ago for the professional network and CME content. Uses Amion because her department's call schedule lives there. Recently started using Scribe for clinic notes and occasionally submits a question to Ask.

**Jobs to be done:** finish documentation before leaving the building; find a colleague's contact details quickly; check a drug interaction without opening three tabs; know who is on call this weekend.

**What she pays:** nothing. Her health system may hold a Workflow Solutions subscription; she does not experience a price.

**What she generates:** one unit of "quarterly unique active provider" — the same unit whether she submits one Ask prompt or four hundred. Her enthusiasm for Scribe increases Doximity's inference cost and does not increase its revenue within the contract term.

**The design implication:** every product decision that increases Dr. Anita's AI usage improves the adoption metric, improves retention risk, and worsens the gross margin. There is no pricing mechanism that converts her delight into revenue during the contract.

### 18.2 Marcus T. — the pharmaceutical brand lead (pays most of the bill)

Runs a specialty brand at a large pharmaceutical company. Buys Marketing Solutions modules to put sponsored content in front of a defined specialty audience. Measures reach, frequency, and script lift attributed to digital channels.

**Jobs to be done:** reach a precisely defined physician audience at a defensible cost per targeted member; demonstrate channel effectiveness to a brand team; place budget before the end of the marketing year.

**What he cares about from the AI suite:** essentially nothing directly. He cares whether AI features *increase physician time on platform*, because attention is his inventory. If Scribe brings Dr. Anita into the app daily, his sponsored content has more opportunities to be seen.

**The decisive product question:** does AI usage generate advertising inventory, or does it generate *sessions that bypass* advertising inventory? A physician who opens Scribe, dictates a note and closes the app has consumed inference cost without passing a Newsfeed module. This is the most important unanswered question about Doximity's AI, and no public disclosure addresses it.

### 18.3 Priya S. — the health system digital officer (pays, and is the expansion opportunity)

Evaluates and renews Workflow Solutions for a multi-hospital system. Holds the seat count. Is the only buyer whose spending could grow because of the AI suite.

**Jobs to be done:** reduce clinician documentation burden measurably; satisfy HIPAA and security review; justify per-seat cost against a burnout or throughput outcome; avoid adding another vendor.

**What she needs and is not given:** an outcome. Hinge Health, on Day 81, disclosed a human-care-hour reduction of approximately **97%** — a cost metric, imperfect, but a *number*. Doximity discloses no clinical or time-saved outcome for Scribe or Ask at all. Priya is asked to renew and expand on the strength of a benchmark result mentioned once in a press release.

**And the evidence says she is not expanding.** Expansion contributed **15.48%** of subscription growth. NRR fell **11.00pp**. The persona with the budget, the need and the AI product in front of her is the persona that did not spend more.

---

## 19. User journey — the AI suite

| Stage | Physician experience | Doximity cost | Doximity revenue |
|---|---|---|---|
| Discovery | Sees Scribe or Ask promoted in-app | Marketing | — |
| Activation | Submits first Ask prompt / records first note | **Inference cost begins** | — |
| Habit | Uses Scribe for most clinic days | **Inference cost scales with use** | — |
| Advocacy | Recommends to colleagues in the system | **Inference cost scales further** | — |
| Monetisation | Health system renews or expands seats | — | **Recognised ratably, annually** |

The cost curve is continuous and usage-linked. The revenue curve is a step function that moves once a year, if at all. Every stage of the journey except the last one costs money.

### 19.1 The one-way door in this journey

The activation step is irreversible in a way that matters. Once a physician adopts an ambient scribe into clinic workflow, removing it is a clinical-workflow disruption, not a feature rollback. That creates genuine switching costs — good — but it also means **Doximity cannot throttle usage to protect margin without a clinical-experience cost.** The variable-cost exposure identified in section 16 has no cheap release valve on the demand side.

---

## 20. Jobs to be Done

| Job | Who has it | How Doximity serves it | Monetised? |
|---|---|---|---|
| "Finish my notes before I go home" | Physician | Scribe | No — bundled |
| "Answer a clinical question I trust" | Physician | Ask, PeerCheck | No — bundled |
| "Know who's on call" | Physician / scheduler | Amion | Indirectly, via Workflow seats |
| "Reach cardiologists in the Midwest" | Pharma brand lead | Marketing Solutions modules | **Yes — directly** |
| "Hire a hospitalist" | Recruiter | Hiring Solutions | **Yes — directly** |
| "Reduce my clinicians' documentation burden" | Health system | Clinical AI Suite | Only at renewal |
| "Fill a locum shift next week" | Health system | Staffing (Other revenue) | **Yes — and growing 28.38%** |

The two jobs with the clearest direct monetisation are advertising and recruitment — neither of which is an AI job. The fastest-growing monetised job in the quarter was staffing.

---

## 21. Business Model Canvas

**Customer segments.** Pharmaceutical manufacturers and their agencies; health systems and hospitals; recruiters. Physicians are users, not customers.

**Value propositions.** To pharma: precise, verified physician reach. To health systems: workflow tools and a clinical AI suite. To physicians: free professional utility.

**Channels.** Direct enterprise sales; third-party media agencies (Doximity acts as principal and does not know the price the agency charges its own client).

**Customer relationships.** Annual or sub-annual subscriptions; 127 customers at ≥$500k TTM producing ~83% of revenue.

**Revenue streams.** Subscription (93% of revenue); staffing and placement fees.

**Key resources.** The verified physician network (>85% of U.S. physicians); the data asset that makes targeting precise; the AI suite.

**Key activities.** Network maintenance and verification; ad inventory management; model deployment and evaluation.

**Key partners.** Cloud hosting vendors ($13.00M in named remaining commitments); media agencies; an acquired intangible now being amortised for AI.

**Cost structure.** Stock compensation (**23.47%** of revenue); sales and marketing (**28.76%**); R&D (**24.57%**); AI hosting and amortisation (**$6.40M** this quarter).

### 21.1 The asymmetry the canvas exposes

Value is delivered to a segment that does not pay, and the cost of delivering it is variable and rising. Value is captured from a segment that buys attention, and attention is only indirectly related to AI usage. **The canvas has no arrow connecting AI cost to AI revenue,** because the filings disclose none.

---

## 22. Competitive analysis

| Competitor | Overlap | Doximity's position |
|---|---|---|
| **OpenEvidence** | Clinical reference AI for physicians | Direct, and in active litigation both ways |
| **Abridge** (Day 84) | Ambient clinical documentation | Abridge is documentation-native; Doximity bundles Scribe |
| **Nuance / Microsoft DAX** | Ambient documentation at enterprise scale | Incumbent in health-system procurement |
| **Epic (in-EHR AI)** | Documentation and inbox drafting | Distribution advantage inside the record of truth |
| **LinkedIn** | Professional network, recruiting | Doximity's verification and specialty targeting are stronger for medicine |
| **Endpoint/Veeva, IQVIA** | Pharma HCP engagement | Compete for the marketing budget that funds Doximity |

### 22.1 Porter's Five Forces

**Threat of new entrants — Low to moderate.** Rebuilding a verified network of >85% of U.S. physicians is close to impossible. But building a *clinical AI assistant* is not — that is precisely what OpenEvidence did, and the litigation exists because the competitive boundary is contested. The moat protects the network, not the AI.

**Bargaining power of buyers — High and rising.** 127 customers produce ~83% of revenue. NRR fell to 107% from 118%. Marketing Solutions contracts run twelve months or less and some are cancellable with customary notice. Pharmaceutical marketing budgets are discretionary and concentrate around product launches.

**Bargaining power of suppliers — Moderate and increasing.** Only **$13.00M** of named cloud commitments against a $6.40M quarterly AI cost of revenue. Little contractual price protection.

**Threat of substitutes — High for AI, low for the network.** A physician can use any general-purpose model for a clinical question. Doximity's differentiators are HIPAA compliance and integration into a workflow the physician already uses. Neither is unique for long.

**Competitive rivalry — Intense and now legal.** Two companies suing each other over AI conduct, with false-advertising counterclaims about AI statements, is rivalry that has left the product arena.

### 22.2 The uncomfortable read

Doximity's moat is the network. Its growth narrative is the AI. **These are not the same asset, and the AI is the one with no moat.** The quarter's numbers are consistent with that reading: the network delivered 7.34% revenue growth, and the AI delivered a 4.31pp gross-margin contraction and a claim in a press release.

---

## 23. SWOT

**Strengths.** More than 85% of U.S. physicians verified on the network. ~83% of revenue from 127 large customers with established relationships. **84.87%** gross margin even after AI cost. $687.8M liquidity, no debt. Genuine workflow embedding via Amion. AI infrastructure largely uncommitted and therefore throttleable.

**Weaknesses.** No disclosed AI revenue, AI outcome metric or AI unit economics. NRR fell **11.00pp**. Expansion contributed only **15.48%** of subscription growth. SBC at **23.47%** of revenue. Every expense line grew faster than revenue. The principal AI-adjacent metric is a user count at a company that just settled a $31.0M user-count disclosure case.

**Opportunities.** Convert Workflow Solutions to usage-aligned pricing. Disclose an audited AI outcome and turn a liability into a differentiator. Monetise AI sessions as advertising inventory. Staffing revenue growing **28.38%**. $400.9M of buyback authorisation remaining.

**Threats.** Inference cost inflation with no contractual ceiling. OpenEvidence litigation and seven outstanding derivative suits. Epic and Microsoft distribution inside the EHR. Pharmaceutical marketing budget cyclicality. A full-year guide requiring **3.05×** the delivered growth rate.

---

## 24. Metrics: what is disclosed, what is not

### 24.1 Disclosed

| Metric | Value | Where |
|---|---|---|
| Revenue growth | 7.34% | 10-Q, PR |
| Customers ≥$500k TTM | 127 (from 119) | 10-Q |
| Net revenue retention | 107% (from 118%) | 10-Q |
| Quarterly unique active providers, YoY | ~32% | 10-Q |
| AI cost inside cost of revenue | $6.40M | 10-Q MD&A |
| Adjusted EBITDA margin | 47.74% | PR |

### 24.2 Claimed but not in any reviewed filing

| Claim | Where it appears |
|---|---|
| Top-performing U.S.-based model on NOHARM | CEO quote only |
| Workflow active prescriber growth >30% YoY | CEO quote only |
| AI Search query growth >25% QoQ | CEO quote only |
| "Doximity Ask" as a named product | CEO quote only |

### 24.3 Not disclosed anywhere

- Absolute number of active providers (only the growth rate)
- Number of Ask, Scribe or PeerCheck users specifically
- AI-attributable revenue
- Any clinical accuracy, safety or time-saved outcome
- Cost per AI interaction
- Whether AI sessions generate advertising impressions

**The third list is the one that decides whether this product works, and it is empty.**

---

## 25. Proposed North Star metric

**Audited AI-attributable subscription revenue per active AI provider, per quarter.**

```
north_star_computable_today = False
```

It cannot be computed today, and that is the argument for it. It requires three disclosures Doximity does not make: AI-attributable revenue, the absolute count of AI-using providers, and a consistent quarterly definition of both. A north star that the company cannot currently calculate is a north star that forces the instrumentation.

### 25.1 Why not the metrics that exist

*Quarterly unique active providers* is a union of nine behaviours including fax and a ten-second phone call, is weather-sensitive by the company's own admission, and is disclosed only as a growth rate. It cannot be a north star because it cannot distinguish AI success from a cold January.

*Net revenue retention* is the right shape — it captures expansion, which is where AI value should land — but it is company-wide and TTM, so it cannot isolate AI.

*Adjusted EBITDA margin* excludes the largest driver of the earnings decline (**51.33%**).

### 25.2 Guardrail metrics

**Guardrail 1 — AI cost of revenue as a share of incremental revenue.** Computable today:

| Measure | Value |
|---|---|
| Disclosed AI cost of revenue | $6.40M |
| Incremental revenue YoY | $10.705M |
| **Ratio** | **59.79%** |
| Breach threshold | 100% |
| Breached this quarter? | **No** |
| Headroom before breach | **$4.305M** |

At 100%, incremental AI cost consumes the entire incremental revenue. Doximity sits at **59.79%** with **$4.305M** of headroom at this revenue delta. If AI cost keeps growing while revenue growth stays near 7%, this guardrail breaches — and it is the single most informative number a product manager could track here.

**Guardrail 2 — Expansion share of subscription growth.** Currently **15.48%**. Floor: 30%. Below it, the product is acquiring rather than deepening, and the network thesis is not operating.

**Guardrail 3 — Gross margin excluding disclosed AI cost.** Currently **88.96%**. This separates "the core business is healthy and we are investing" from "the core business is deteriorating." This quarter it says clearly: the core is healthy; the investment is expensive.

---

## 26. HEART framework applied to the Clinical AI Suite

| Dimension | Proposed measure | Disclosed? |
|---|---|---|
| **Happiness** | Physician CSAT on Scribe note quality | No |
| **Engagement** | Ask prompts per active provider per week | No |
| **Adoption** | First-time Scribe users per quarter | No — only the nine-behaviour union |
| **Retention** | Week-4 Scribe retention by cohort | No |
| **Task success** | % of Scribe notes signed without material edit | **No — and this is the one that matters** |

Task success is the entire question for an ambient scribe. A note that must be rewritten has consumed inference cost and physician time and produced negative value. Doximity discloses no edit rate, no acceptance rate, no time-to-sign. The NOHARM benchmark result, whatever its merits, is a model-level evaluation — it is not a measure of whether Dr. Anita's notes survive contact with her own review.

---

## 27. AARRR funnel

| Stage | Doximity's position | Evidence |
|---|---|---|
| **Acquisition** | Strong — >85% of U.S. physicians | 10-Q, PR |
| **Activation** | Strong and accelerating — providers +~32% | 10-Q |
| **Retention** | Weakening on the revenue side — NRR 107% from 118% | 10-Q |
| **Referral** | Network-inherent, not measured for AI | — |
| **Revenue** | +7.34%, with **84.52%** from new logos | 10-Q MD&A |

The funnel is wide at the top and narrowing where it monetises. This is the shape of a product with excellent distribution and an unresolved pricing model.

---

## 28. Eval plan for the Clinical AI Suite

A benchmark result is not an eval plan. Here is what a product manager should require before treating an ambient scribe and a clinical reference tool as production-safe.

**Offline evaluation.** A held-out set of real de-identified encounters, stratified by specialty, accent, encounter length and comorbidity count. Measure: factual error rate per note, omission rate for medications and allergies, hallucinated-finding rate. Report by stratum, not in aggregate — an aggregate figure hides the specialties where the model fails.

**Human-graded evaluation.** Board-certified reviewers scoring a sample of notes for clinical accuracy and completeness against the audio. Inter-rater reliability reported. This is expensive and there is no substitute.

**Online evaluation.** Edit distance between the generated note and the signed note. Time from encounter end to signature. Rate of notes abandoned mid-review. These are the metrics that correlate with real value, and all three are computable from telemetry Doximity already has.

**Adversarial and safety evaluation.** Drug-name confusion pairs, negation handling ("no chest pain" versus "chest pain"), dose-unit errors, pediatric weight-based dosing. Negation and dose errors are the two failure modes with the shortest path to patient harm.

**Regression gating.** No model version ships without matching the prior version on the safety suite. Benchmark performance is not a release criterion; safety-suite non-regression is.

### 28.1 What NOHARM does and does not tell you

An external benchmark is a genuinely useful signal — it is third-party, it is comparative, and it is harder to game than an internal metric. Leading it is a real achievement if accurate.

But a benchmark measures a model against a fixed set of questions. It does not measure whether this model, in this product, on this physician's audio, in this specialty, produces a note that gets signed. **Benchmark leadership and product safety are different claims, and only one of them is a product metric.** For a clinical product, the second is the one that belongs in a filing.

---

## 29. Ranked failure modes

Ranked by expected harm, not by likelihood.

**1. Medication or dose error in a generated note that is signed without catching it.** Highest harm, plausible frequency. Mitigation: hard-block generation of dose values below a confidence threshold; require explicit confirmation for all medication changes; never infer a dose from context.

**2. Negation inversion in a clinical summary.** "Denies chest pain" rendered as "chest pain." High harm, known LLM failure mode. Mitigation: dedicated negation test suite with release gating; highlight all negated findings in the review UI.

**3. Confident wrong answer from the clinical reference tool.** A physician asks Ask a drug-interaction question and acts on an incorrect answer. Mitigation: citation-required responses; refusal on questions outside the evidence base; visible confidence and source recency.

**4. Silent quality regression after a model update.** Notes get subtly worse and nobody notices because the only tracked metric is usage. Mitigation: continuous edit-distance monitoring with alerting — the cheapest high-value control on this list.

**5. Automation complacency.** Physicians review less carefully over time as trust grows. This is the failure mode that gets worse precisely as the product gets better. Mitigation: periodic blind-audit sampling; surface per-physician edit rates trending toward zero as a risk signal, not a success signal.

**6. Cost runaway.** Usage grows faster than contracted revenue and gross margin compresses further. Already visible: **94.95%** of this quarter's gross-margin contraction. Mitigation: per-seat fair-use ceilings with transparent overage, or usage-tiered pricing.

**7. Inventory cannibalisation.** AI sessions replace Newsfeed sessions, reducing advertising impressions. Mitigation: instrument impressions per session by entry point. This is not disclosed and may not be measured.

Note the structure: failure modes 1 through 5 are clinical, 6 and 7 are economic, and **only number 6 is currently visible in any public disclosure.**

---

## 30. Human-in-the-loop design

The Clinical AI Suite already has a human in the loop — the physician signs the note. The design question is whether that loop is *load-bearing* or *ceremonial*.

A loop is ceremonial when the reviewer has no practical means or incentive to dissent: when the default is accept, when the interface does not surface what changed, when reviewing carefully takes longer than rewriting, and when no one measures whether review is happening.

Three design requirements make the loop load-bearing:

**Make the model's uncertainty visible.** Highlight low-confidence spans in the note. A physician who knows which three sentences the model was unsure about will check those three sentences.

**Make dissent cheap.** One-tap rejection with a reason code. If correcting is more work than accepting, acceptance is not a judgment.

**Measure the loop itself.** Per-physician edit rates over time. A physician whose edit rate falls to zero has either received a perfect model or stopped reading. **PeerCheck — where providers review AI responses — is genuinely interesting here**, because it makes review an explicit, measurable product surface rather than an implicit assumption. It appears once in the 10-Q and no results from it are disclosed.

---

## 31. AI cost per interaction

This cannot be computed from disclosure, and the reason is itself the finding.

| Known | Value |
|---|---|
| Disclosed AI cost of revenue, Q1 FY2027 | $6.40M |
| Increase in hosting and software costs | $4.9M |
| Increase in AI-related amortisation | $1.5M |
| Additional hosting and software inside R&D | $1.1M |
| **Total identifiable hosting increase (COGS + R&D)** | **$6.00M** |
| Total hosting increase as a share of incremental revenue | **56.05%** |

| Unknown | |
|---|---|
| Number of AI interactions | Not disclosed |
| Number of AI-using providers | Not disclosed |
| Absolute provider count | Not disclosed — only growth rate |

**Every numerator is available. No denominator is.** Cost per interaction is therefore unknowable from outside, and this is not an accident of drafting — it is the direct consequence of disclosing AI cost in MD&A while disclosing AI usage only as a growth rate in a union metric.

A useful way to hold this: Doximity has given the market enough information to know that AI is expensive, and not enough to know whether it is worth it.

---

## 32. Pricing analysis

Workflow Solutions is sold per seat, annually, with the Clinical AI Suite included. This is the structural problem.

| Pricing model | Cost alignment | Adoption incentive | Doximity's current model |
|---|---|---|---|
| Per seat, AI bundled | **Poor** — cost varies, price does not | Strong — no marginal cost to user | **Current** |
| Per seat + fair-use ceiling | Moderate | Good | — |
| Usage-tiered | Good | Moderate — may suppress adoption | — |
| Outcome-based (per note signed) | Good | Strong | — |

The bundled model was the right choice for driving adoption, and it worked: providers grew ~32%. It is the wrong choice for a feature with a variable cost curve, and the gross margin shows it.

The trap is real, though, and worth stating fairly: moving to usage-based pricing would suppress the adoption metric the company currently reports, in a quarter when it needs **3.05×** its delivered growth rate. **The pricing model that protects the margin damages the narrative.** That conflict is the most interesting product-strategy problem at Doximity right now.

---

## 33. Product recommendations

Seven recommendations. Each names the evidence that motivates it and the metric that would prove it worked.

### R1. Publish one audited AI outcome metric in the 10-Q

**Evidence:** `audited_ai_claim_count = 0`. Four AI claims, all quote-only.
**Proposal:** Disclose in the 10-Q a single AI outcome metric with a stable definition — proposed: percentage of Scribe-generated notes signed without material edit, defined once and held constant.
**Why this one:** It is a task-success measure, it is computable from existing telemetry, and it is the metric Priya S. needs to justify renewal.
**Success:** The metric appears in two consecutive 10-Qs with an unchanged definition.
**Cost:** Low — the data exists. The barrier is the willingness to publish a number that can go down.

### R2. Disclose Clinical AI Suite revenue as a separate line

**Evidence:** `ai_revenue_line_disclosed = False`. Cost is disclosed; revenue is not.
**Proposal:** Break out AI suite revenue, or at minimum Workflow Solutions revenue, in the revenue disaggregation note.
**Why:** It is the only way any outsider can assess whether AI pays for itself. It also converts the current asymmetry — audited cost, unaudited claims — into symmetry.
**Success:** Positive and improving AI gross margin, disclosed.
**Cost:** Moderate. Requires allocation methodology and sets a precedent that cannot be withdrawn.

### R3. Report AI gross cost per active provider each quarter

**Evidence:** Every numerator disclosed, no denominator (section 31).
**Proposal:** Disclose the absolute count of providers using the AI suite, alongside the AI cost already in MD&A.
**Why:** This single addition makes unit economics computable without requiring revenue allocation. It is the cheapest disclosure on this list by a wide margin.
**Success:** Cost per provider flat or declining across four quarters.
**Cost:** Low.

### R4. Re-base the workflow-provider metric on a filed definition that excludes non-AI behaviours

**Evidence:** The metric counts faxes and ten-second phone calls, is weather-sensitive by the company's own admission, and is presented as reflecting AI adoption.
**Proposal:** Report an AI-specific active-user count as a distinct metric, keeping the existing union metric for continuity.
**Why:** Beyond accuracy — a company that has settled a **$31.0M** case about user-count disclosure has a specific interest in metrics that cannot be attacked on definitional grounds.
**Success:** Two consecutive quarters of an AI-specific count with an unchanged definition.
**Cost:** Moderate, and politically hard: the AI-specific number will be much smaller than ~32% growth on a nine-behaviour union.

### R5. Introduce fair-use ceilings with transparent overage on Workflow Solutions

**Evidence:** `ai_share_of_gm_contraction_pct = 94.95`; commitments of only **$13.00M**.
**Proposal:** Retain per-seat pricing; add a generous per-seat monthly interaction allowance with disclosed overage pricing above it.
**Why:** Caps the tail risk without changing the buying motion or suppressing typical use. Most seats will never hit the ceiling; the ones that do are the ones driving cost.
**Success:** Gross margin excluding AI cost stable, with AI cost growth tracking below revenue growth.
**Cost:** Moderate — contract amendments at renewal.

### R6. Instrument and disclose advertising impressions per AI session

**Evidence:** Failure mode 7. Unknown whether AI sessions generate or cannibalise inventory.
**Proposal:** Internal first. Measure impressions per session by entry point; compare AI-entry sessions against Newsfeed-entry sessions.
**Why:** If AI sessions cannibalise inventory, the AI suite has a *negative* revenue effect that is currently invisible and being funded as an investment. This is the highest-value unknown in the business.
**Success:** A clear internal answer within one quarter.
**Cost:** Low internally.

### R7. Establish and publish a model-release safety gate

**Evidence:** Failure modes 1, 2 and 4; a benchmark result presented as a quality claim.
**Proposal:** A published policy that no model version ships without non-regression on a negation, dose and medication safety suite, with the suite's composition described.
**Why:** Benchmark leadership is a marketing asset; a release gate is a product control. Publishing the policy — not the scores — is a genuine differentiator that costs nothing competitively.
**Success:** The policy is stated in the 10-K risk factors or governance discussion.
**Cost:** Low.

---

## 34. RICE prioritisation

Reach, Impact, Confidence and Effort are **author estimates, not disclosed data**. Reach is held constant at 127 — the count of customers with ≥$500k TTM revenue — because these are disclosure and pricing changes whose audience is the economically meaningful customer base.

The stress factor models the series-standard adverse scenario: value is discounted by how much of a proposal depends on claims that are currently quote-only rather than filed, and by execution exposure.

| ID | Proposal | R | I | C | E | Base RICE | Stress | Stressed |
|---|---|---|---|---|---|---|---|---|
| P1 | Publish an audited AI outcome metric in the 10-Q | 127 | 3.0 | 0.85 | 4.0 | **80.96** | 0.90 | **72.87** |
| P3 | Report AI gross cost per active provider | 127 | 2.0 | 0.90 | 3.0 | **76.20** | 0.95 | **72.39** |
| P2 | Disclose Clinical AI Suite revenue separately | 127 | 2.5 | 0.80 | 6.0 | **42.33** | 0.85 | **35.98** |
| P4 | Re-base the workflow-provider metric | 127 | 2.0 | 0.75 | 5.0 | **38.10** | 0.80 | **30.48** |
| P5 | Tie Workflow Solutions pricing to AI usage tiers | 127 | 3.0 | 0.60 | 12.0 | **19.05** | 0.45 | **8.57** |

```
rice_base_ranking    = ('P1', 'P3', 'P2', 'P4', 'P5')
rice_stress_ranking  = ('P1', 'P3', 'P2', 'P4', 'P5')
rice_last_under_stress      = 'P5'
rice_last_under_stress_name = 'Tie Workflow Solutions pricing to AI usage tiers'
rice_last_gap_pct           = 71.88
```

### 34.1 Reading the ranking

The ordering is stable under stress, which is itself informative — the top proposals are robust, not knife-edge.

**P5 ranks last, by a margin of 71.88% below P4.** This is deliberate and it is asserted by the gate rather than argued in prose. Usage-tiered pricing is the recommendation with the largest theoretical impact — it addresses the root cause of the margin compression directly. It ranks last because it has the lowest confidence (0.60), by far the highest effort (12 person-months), and the harshest stress factor (0.45), reflecting the conflict identified in section 32: repricing suppresses the adoption metric the company is currently using to tell its story, in the exact quarter it needs **3.05×** its delivered growth rate.

**The highest-impact fix is the lowest-ranked action.** That is an honest output of the framework, not a failure of it. P5 belongs on the roadmap — in a later horizon, after the disclosure changes have established an evidence base that makes repricing defensible to customers.

P3 loses the least value under stress (**5.00%**) because it depends on no claim that is currently unverified — it requires only publishing a number the company already has. P5 loses the most (**55.01%**).

---

## 35. MoSCoW

**Must have.** R1 (audited AI outcome metric); R3 (AI cost per active provider); R7 (model-release safety gate).

**Should have.** R2 (AI revenue line); R6 (impressions per AI session, internal).

**Could have.** R4 (re-based provider metric); R5 (fair-use ceilings).

**Won't have this cycle.** Full usage-based repricing of Workflow Solutions (P5). Correct sequencing, not rejection — see 34.1.

---

## 36. Kano analysis

| Feature | Kano category | Reasoning |
|---|---|---|
| Accurate ambient note capture | **Must-be** | Its absence is intolerable; its presence earns no praise |
| Clinical reference with citations | **Must-be** | Uncited answers are unusable in clinical context |
| On-call scheduling (Amion) | **Must-be** | Deeply embedded; failure is operational |
| Sub-minute note turnaround | **Performance** | More speed, more satisfaction, linearly |
| Specialty-tuned note templates | **Performance** | Value scales with fit |
| PeerCheck peer review of AI output | **Attractive** | Unexpected; builds trust in a way competitors do not |
| Confidence highlighting on generated spans | **Attractive** | Would be delightful; not offered |

Most of the Clinical AI Suite sits in must-be territory. **Must-be features do not drive expansion revenue — they prevent churn.** That is consistent with what the numbers show: adoption up ~32%, expansion revenue contributing 15.48%. The AI suite is behaving exactly as a must-be feature behaves, and it is being funded as though it were an attractive one.

---

## 37. PRD: AI outcome disclosure (R1)

**Problem.** Doximity discloses the cost of AI in a reviewed filing and the performance of AI only in a CEO quote. Health-system buyers cannot justify expansion on a quote, and expansion revenue is contributing 15.48% of subscription growth.

**Objective.** Publish one AI outcome metric in the 10-Q with a definition stable across periods.

**Proposed metric.** Percentage of Scribe-generated notes signed by the authoring clinician without material edit, where "material edit" is defined by a fixed edit-distance threshold published alongside the metric.

**Non-goals.** Not a clinical-accuracy claim. Not a safety certification. Not a replacement for the benchmark result.

**Requirements.**
- R1.1 Compute edit distance between generated and signed notes at signature time.
- R1.2 Fix the material-edit threshold before first publication and publish it.
- R1.3 Report quarterly, by specialty grouping, with an aggregate.
- R1.4 Restate prior periods if the definition ever changes, and say so.
- R1.5 Review with counsel against the disclosure history in section 17.

**Success criteria.** Published in two consecutive 10-Qs with an unchanged definition. Secondary: expansion share of subscription growth above 30%.

**Risks.** The number may be unflattering at first. It becomes a commitment that cannot be quietly withdrawn. Competitors will benchmark against it. **All three risks are arguments for publishing it, not against** — a metric that cannot embarrass you is not a metric.

---

## 38. Roadmap

**Horizon 1 — the next two quarters.** R3 (AI cost per active provider), R7 (safety gate policy), R6 (impressions per AI session, internal only). Low effort, high information yield, no pricing disruption. These build the evidence base.

**Horizon 2 — quarters three and four.** R1 (audited AI outcome metric), R4 (AI-specific active-user count). Requires the instrumentation from Horizon 1 and a decision to publish numbers that can decline.

**Horizon 3 — year two.** R2 (AI revenue line), R5 (fair-use ceilings). Both require the previous horizons to have produced a defensible evidence base. Repricing a bundled feature is only defensible once you can show the customer what they are getting.

**Deliberately not scheduled.** Full usage-based repricing (P5). Revisit once expansion revenue exceeds 30% of subscription growth — at that point customers are buying more voluntarily and repricing is a negotiation rather than a shock.

### 38.1 Sequencing logic

The roadmap is ordered by *evidence dependency*, not by impact. Every later item requires an earlier one to be credible. Publishing an AI outcome metric (R1) before instrumenting cost per provider (R3) would produce a number with no cost context. Repricing (R5) before publishing an outcome metric (R1) would be a price increase with no demonstrated value behind it.

---

## 39. Risks to this analysis

**One quarter is one quarter.** Q1 is Doximity's seasonally weakest quarter. The margin compression, the receivables build and the NRR decline may all normalise. A single quarter cannot establish a trend, and this document does not claim it does.

**The AI cost attribution is management's, not mine.** The $4.9M and $1.5M are narrated in MD&A as AI-related. I have taken that attribution at face value because management is better placed to make it — but it is a management characterisation, not an audited line item, and "primarily driven by" leaves room.

**The term counts measure location, not truth.** That NOHARM appears zero times in the 10-Q does not mean the claim is false. It means it was not made in that document. Companies are not required to put benchmark results in filings, and most do not.

**Stock compensation may be a one-time step.** The 134.01% increase in R&D stock compensation reflects new grants. If those are front-loaded, the growth rate will not persist even if the level does.

**Seasonality may fully explain the guidance gap.** The required **22.35%** for the remaining nine months is dramatic against Q1's 7.34%, but Doximity's revenue is genuinely back-half weighted. A full seasonality analysis across several fiscal years would be needed to judge this properly, and is outside this document's scope.

**RICE inputs are mine.** Reach, Impact, Confidence, Effort and every stress factor are author constructs. They are declared as such in section 34 and in ASSUMPTIONS.md, and the framework's output should be read as a structured argument, not a calculation.

---

## 40. What a product manager should take from this

**Where a claim is published tells you what evidence standard it met.** The same company said "our AI cost $6.4 million" in a reviewed filing and "our AI is the top-performing U.S.-based model" in a press release. Both may be true. Only one was held to the standard of a document filed under officer certification. When you write a metric into a deck, ask which of those two documents it would survive.

**Adoption metrics can be cost metrics in disguise.** Doximity's providers grew ~32% while revenue grew 7.34%. Under seat-based pricing with variable inference cost, that gap is not latent revenue — it is realised cost. Before celebrating an adoption number, trace the cost curve and the revenue curve separately and check whether they have the same shape.

**Check what your headline metric is made of.** A metric that counts a fax, a ten-second phone call and an AI prompt as the same event, and that the company itself warns is weather-sensitive, cannot carry an AI narrative. It is a composite, and composites move for reasons that have nothing to do with your product.

**The metric you choose is a liability you accept.** Doximity settled a **$31.0M** securities case about user-count and engagement-rate disclosures, with final approval nineteen days before this quarter closed, and seven derivative suits remain outstanding. Its headline AI-adjacent indicator is a user count. Metric selection is a legal decision as much as an analytical one.

**The highest-impact fix is often the lowest-ranked action, and that is fine.** Usage-based pricing would solve Doximity's margin problem at the root. It ranks last under stress by **71.88%** because it is expensive, uncertain, and would damage the narrative in the quarter that needs it most. Good prioritisation says *later*, not *no* — and says why.

---

## 41. The three-company disclosure ladder

Days 80, 81 and 82 form a single argument, and it can be stated as a ladder.

| Rung | Company | AI positioning | What is actually disclosed |
|---|---|---|---|
| 1 | **Day 80 — Hims & Hers** | "Doctor-led AI clinical engine" | **No AI metric at all** |
| 2 | **Day 81 — Hinge Health** | AI reduces human care delivery | A **cost** metric (~**97%** human care hour reduction) — no outcome metric |
| 3 | **Day 82 — Doximity** | AI adoption across the physician network | **Cost disclosed in the 10-Q; all four performance claims quote-only** |

Each rung is an improvement on the one below it, and none of them reaches the thing a buyer actually needs.

Hims & Hers built an entire narrative on an AI clinical engine and disclosed nothing measurable about it. Hinge Health did better — it published a real number — but that number measured how much human labour the AI removed, not whether patients got better. Doximity does something neither did: it tells you, in a reviewed filing, what AI cost. **And it is still the case that not one of the three has disclosed an AI outcome.**

### 41.1 The shape of the pattern

Read in order, the ladder shows something specific about how AI is being reported in healthcare products right now: **companies are becoming more transparent about AI economics faster than they are becoming transparent about AI efficacy.** Cost is a number your finance organisation already has. Efficacy requires you to build an evaluation apparatus, hold it constant, and publish results that might decline.

The cost disclosure arrives first because it is easier. The efficacy disclosure is the one that would change a buying decision.

---

## 42. Like-for-like comparison

| Measure | Day 80 Hims & Hers | Day 81 Hinge Health | Day 82 Doximity |
|---|---|---|---|
| Growth from acquisition vs expansion | **59.43%** acquired | — | **84.52%** acquired |
| Disclosed AI metric | None | Cost (**97%** human hour reduction) | None audited |
| AI cost disclosed | No | No | **Yes — $6.40M** |
| AI outcome disclosed | No | No | No |
| AI claims in reviewed filing | — | Yes | **Zero of four** |

Doximity's acquisition dependence exceeds Hims & Hers' by **25.09pp**. The company with the strongest network effects in the series is the most reliant on new logos. That is the single most counterintuitive number across the three days, and it is the clearest evidence that Doximity's network moat and its growth engine are not the same thing.

---

## 43. What Doximity does better than Days 80 and 81

It would be unfair to read this case study as purely critical, and inaccurate. Doximity is, on the evidence, the most transparent of the three companies.

**It attributes cost to AI explicitly.** Neither Hims & Hers nor Hinge Health told the market what AI cost them. Doximity did, in MD&A, with a dollar figure and a causal statement about gross margin. That is a real disclosure choice and it went against the company's short-term interest.

**It defines its metrics exhaustively.** The nine-behaviour definition of an active provider is criticised in section 7.1, but the criticism is only possible *because the definition is published*. Most companies disclose a user metric with a sentence. Doximity discloses it with a list, a footnote defining "provider," and a warning about seasonality.

**It warns against its own metric.** A company telling investors that its headline engagement number fluctuates with the weather is doing something unusual and creditable.

**It discloses NRR declining.** 107% from 118% is a bad number, disclosed plainly, in a table, next to the prior year.

The criticism in this document is that the AI *performance* claims did not receive the same treatment as the AI *cost* disclosure. Within one company, two different standards were applied to two halves of the same story. That is a narrower and more interesting failing than "the company is opaque," which would not be true.

---

## 44. Day 83 connection

Tomorrow's case study is **OpenEvidence** — the plaintiff in the litigation described in section 17.2, and the defendant in Doximity's false-advertising counterclaims about AI statements.

Two companies, one lawsuit, opposite sides, read back to back. Day 82 has established what Doximity discloses about AI. Day 83 will establish what OpenEvidence does. The comparison will be made on evidence, from whatever primary sources exist for a private company, and Day 82 will not be re-litigated there — its figures stand as computed here.

---

## 45. Financial summary

| Measure (thousands unless noted) | Q1 FY2027 | Q1 FY2026 | Change |
|---|---|---|---|
| Revenue | 156,618 | 145,913 | +7.34% |
| Subscription revenue | 146,300 | 137,876 | +6.11% |
| Other revenue | 10,318 | 8,037 | +28.38% |
| Gross profit | 132,926 | 130,120 | +2.16% |
| Gross margin | 84.87% | 89.18% | −4.31pp |
| Total operating expenses | 99,282 | 75,603 | +31.32% |
| Income from operations | 33,644 | 54,517 | −38.29% |
| Operating margin | 21.48% | 37.36% | −15.88pp |
| Net income | 24,315 | 53,320 | −54.40% |
| Net margin | 15.53% | 36.54% | −21.01pp |
| Adjusted EBITDA | 74,773 | 79,772 | −6.27% |
| Adjusted EBITDA margin | 47.74% | 54.67% | −6.93pp |
| Stock-based compensation | 36,752 | 21,865 | +68.09% |
| Depreciation and amortisation | 4,287 | 2,794 | +53.44% |
| Operating cash flow | 41,987 | 62,101 | −32.39% |
| Free cash flow | 39,603 | 60,135 | −34.14% |
| Effective tax rate | 39.76% | 16.88% | +22.88pp |
| Diluted EPS (USD) | 0.13 | 0.27 | — |
| Diluted weighted-average shares | 191,169 | 201,158 | −4.97% |

---

## 46. Balance sheet summary

| Measure (thousands) | 30 Jun 2026 | 31 Mar 2026 |
|---|---|---|
| Total assets | 1,083,845 | — |
| Total liabilities | 167,775 | 172,850 |
| Deferred revenue, current | 109,061 | 106,050 |
| Deferred revenue, non-current | 37 | 400 |
| Additional paid-in capital | 1,035,282 | 1,001,688 |
| Accumulated deficit | (119,044) | (51,062) |
| **Total stockholders' equity** | **916,070** | **950,837** |
| Shares issued and outstanding | 179,849 | 183,060 |

Liquidity (cash, cash equivalents and marketable securities) was **$687.8M**. Preferred stock authorised: 100,000 thousand shares; **zero issued and outstanding**. Common stock authorised: 1,500,000 thousand shares.

No customer represented 10% or more of revenue or accounts receivable in either period.

---

## 47. Scenario analysis

All three scenarios are arithmetic on filed inputs. They are **author constructs**, not company guidance.

### 47.1 Scenario A — disclosed AI cost of revenue doubles

| Measure | Value |
|---|---|
| AI cost of revenue | **$12.80M** |
| Guardrail 1 (AI cost ÷ incremental revenue) | **119.57%** |
| Guardrail breached? | **Yes** |
| Gross margin under this scenario | **80.79%** |
| Change versus actual | **−4.08pp** |

At double the current AI cost and the same revenue delta, **incremental AI cost alone exceeds all incremental revenue.** Gross margin falls to 80.79%. This is not a remote scenario: AI cost of revenue grew from a base that was effectively zero, and inference volume is growing with a provider count up ~32%.

### 47.2 Scenario B — revenue growth holds at the Q1 rate for the full year

| Measure | Value |
|---|---|
| Implied FY2027 revenue at 7.34% growth | **$612.25M** |
| FY2027 guidance midpoint | $676.00M |
| **Shortfall versus midpoint** | **$63.75M** |
| Shortfall as a share of the midpoint | **9.43%** |
| Versus the low end of guidance | **−$58.75M** |

If Q1's growth rate simply persisted, Doximity would finish **$58.75M below the bottom of its own guidance range.** The entire guidance depends on acceleration.

### 47.3 Scenario C — expansion share recovers to the proposed 30% floor

| Measure | Value |
|---|---|
| Current expansion share of subscription growth | 15.48% |
| Proposed guardrail floor | **30.00%** |
| Gap | **14.52pp** |
| Additional expansion revenue required at this growth level | **$1.22M** |

Only **$1.22M** of additional expansion revenue in the quarter would have moved expansion share to the 30% floor. The gap is small in absolute dollars and large in what it signifies — this is not a capacity problem, it is a product-value problem.

### 47.4 Sensitivity — what growth would absorb a doubling of AI cost

| Measure | Value |
|---|---|
| Revenue increase needed to hold Guardrail 1 at 59.79% with AI cost doubled | **$21.41M** |
| Implied revenue growth rate | **14.67%** |

To double AI spending without worsening the guardrail, Doximity would need to roughly double its revenue growth rate — to **14.67%** from 7.34%. That is the bar the AI investment has to clear, expressed as a single number.

---

## 48. Seasonality caveat

Doximity's fiscal year ends 31 March, so Q1 is the June quarter. Pharmaceutical marketing budgets are typically weighted toward later periods, and Marketing Solutions contracts are generally twelve months or less with launch timing controlled by the customer. The 10-Q notes that revenue recognition commences when content is first launched on the platform.

This means Scenario B (section 47.2) almost certainly understates the full year, and the implied **22.35%** nine-month growth requirement is not as extreme as it looks in isolation. A full multi-year seasonality decomposition would be needed to say by how much, and that analysis is not performed here.

**What seasonality does not explain:** the gross-margin contraction, the NRR decline from 118% to 107%, the expansion share of 15.48%, or the fact that four AI claims appear only in a press release. Those are the findings of this document, and none of them is a timing artefact.

---

## 49. Governance and share structure

Doximity has a dual-class structure — Class A and Class B common stock — presented together on the balance sheet and in the EPS calculation. Preferred stock is authorised but **zero shares are issued or outstanding**.

The CEO, Jeff Tangney, is a co-founder and is the named individual defendant in the settled securities class action and in each of the seven derivative lawsuits. The Chief Technology Officer and the Director of AI Products are named defendants in the OpenEvidence litigation.

Three of the company's senior product and technology leaders are personally named in active litigation about either disclosure practice or AI competitive conduct. For a product organisation, that is a material operating condition: it shapes what can be said publicly about product performance, and it is a plausible part of the explanation for why the AI claims live in a press release rather than a filing.

---

## 50. Concentration risk

| Dimension | Position |
|---|---|
| Customer concentration | 127 customers ≥$500k TTM produce ~83% of revenue |
| Single-customer concentration | None ≥10% of revenue or AR |
| Revenue-type concentration | ~93% subscription |
| End-market concentration | Pharmaceutical marketing budgets |
| Supply concentration | Two named hosting/vendor commitments totalling **$13.00M** |
| Geographic concentration | United States |

The customer count is the exposure that matters. Losing five of 127 large customers is a revenue event the company cannot offset quickly, and NRR at 107% means the installed base is expanding only slightly faster than it is contracting.

---

## 51. Data moat analysis

Doximity's durable asset is the verified physician network — more than 85% of U.S. physicians, verified, with specialty and practice attributes precise enough to sell targeted reach to pharmaceutical marketers. That is genuinely hard to replicate and it is what the SIC code fails to describe.

The AI suite does not extend this moat in an obvious way. Clinical notes generated by Scribe are protected health information and cannot be freely used as training data. Ask queries are a behavioural signal, but the 10-Q discloses nothing about whether or how they are used. The moat protects the advertising business; the AI sits on top of it as a retention and engagement feature.

**The strategic question this raises:** is the AI suite building a second moat, or spending the first one? On the disclosed evidence — adoption up ~32%, expansion revenue at 15.48%, NRR down 11.00pp, gross margin down 4.31pp — it is currently spending. That could change. It has not yet.

---

## 52. Regulatory exposure

The Clinical AI Suite operates in a space with real and moving regulatory boundaries. Scribe is an ambient documentation tool; Ask provides clinical reference and, per the 10-Q, "clinical decision support." That last phrase is doing significant work — clinical decision support software sits near the boundary of FDA device regulation, and where a tool falls depends on whether a clinician can independently review the basis for its recommendation.

The 10-Q describes Workflow Solutions as enabling providers to "leverage the artificial intelligence (AI) writing assistant for administrative tasks and clinical decision support." No FDA classification discussion accompanies this in the reviewed quarterly filing.

HIPAA compliance is asserted for Ask and Scribe and is a genuine differentiator against general-purpose models. State-level AI disclosure requirements in healthcare are developing and vary.

This section is descriptive, not predictive. The point for a product manager is that "clinical decision support" is a regulated term of art, it appears in the filing, and the product's positioning sits close to a boundary that will move.

---

## 53. Trust and safety considerations

Three specific obligations follow from what this product does:

**Physicians must know when they are reading model output.** PeerCheck — where providers review AI responses — suggests Doximity has thought about this. No results from it are disclosed.

**Errors must be traceable.** When a generated note contains a wrong medication, the organisation needs to know which model version produced it, on what input, and whether other notes are affected. This requires versioned logging that most products do not build until after the first incident.

**The review loop must be measured, not assumed.** Section 30 covers this. A signature is evidence of review only if reviewing was practical.

---

## 54. Recommended diagrams

Per series standard from Day 50, **no Mermaid**. Markdown tables and ASCII only. Five visual assets are recommended for the GitHub README and carousel:

**D1 — The disclosure asymmetry.** Two columns, side by side: "In the 10-Q" (AI cost $6.40M, 81.01% of the COGS increase, 94.95% of the margin contraction) versus "In the press release only" (NOHARM, Doximity Ask, AI Search +25% QoQ, prescribers +30% YoY). A single vertical rule between them labelled "officer certification." This is the case study in one image.

**D2 — Adoption versus revenue.** Two bars: providers ~32%, revenue 7.34%, with the 24.66pp gap annotated and a caption noting seat-based pricing.

**D3 — The gross-margin bridge.** Four steps: 89.18% → AI hosting (−) → AI amortisation (−) → other (−) → 84.87%, with 94.95% flagged on the two AI steps combined.

**D4 — The growth decomposition.** A stacked bar of the $8.4M subscription increase: $7.1M new logos (84.52%), $1.3M expansion (15.48%), with NRR 118% → 107% shown alongside.

**D5 — The guidance gap.** Q1 actual 7.34% against the 22.35% required for the remaining nine months, annotated 3.05×, with the seasonality caveat printed on the chart itself.

### 54.1 ASCII rendering of D1, for inline use

```
              IN THE 10-Q                  |        PRESS RELEASE ONLY
         (officer certification)           |        (CEO quote, x1 each)
   ----------------------------------------+----------------------------------
   AI cost of revenue        $6.40M        |  NOHARM benchmark leadership
   Share of COGS increase    81.01%        |  "Doximity Ask" (product name)
   Share of GM contraction   94.95%        |  AI Search queries  +25% QoQ
   Gross margin            84.87%          |  Active prescribers +30% YoY
                                           |
   AUDITED AI CLAIMS:            0         |  QUOTE-ONLY AI CLAIMS:       4
```

---

## 55. Recommended screenshots and visual assets

For the GitHub repository, five screenshots with sources captioned:

1. The cost-of-revenue MD&A paragraph from the 10-Q, with "incurred to support our AI initiatives" highlighted.
2. The full CEO quote from Exhibit 99.1, with the four AI claims highlighted.
3. The "quarterly unique active providers" definition paragraph from the 10-Q, with the nine behaviours enumerated and the ten-second threshold marked.
4. The net revenue retention table showing 107% against 118%.
5. The Note 12 paragraph describing the securities settlement, with "user count and engagement rates" highlighted.

Each should carry the accession number and page reference. All are public documents; no product screenshots are used, since the case study is about disclosure rather than interface.

---

## 56. Appendix A — source conflicts and reconciliations

Series rule: every conflict between sources is documented, never silently resolved.

### A1. The adoption metric: 30% versus 32%

| Source | Metric | Value | Basis |
|---|---|---|---|
| Exhibit 99.1, CEO quote | "workflow active prescriber growth" | "more than 30%" | YoY |
| 10-Q, Key Business Metrics | "quarterly unique active providers using our workflow tools" | "approximately 32%" | YoY |

**Not reconciled, and not reconcilable.** These are different populations. The 10-Q defines *providers* to include physicians, nurse practitioners, CRNAs, physician assistants, pharmacists and medical students. *Prescribers* is narrower and is not defined anywhere in the filing — the word does not appear in it. The gap is **2.00pp**, but the figures are not comparable, so the gap is not meaningful.

**Treatment in this document:** the 10-Q figure (~32%) is used throughout. The CEO's 30% is quoted only in the context of section 7.2, where the discrepancy is the subject.

### A2. The gross-margin decline: "4%" versus 4.31pp

The 10-Q states gross margin "decreased 4%." The computed change is **−4.31pp**, from 89.18% to 84.87%.

**Resolution:** the filing rounds to the nearest whole percentage point and uses "%" where "percentage points" would be precise. No conflict of substance. This document uses the computed **4.31pp**.

### A3. Cost of revenue increase: "$7.9 million" versus $7,899 thousand

MD&A narrates $7.9M; the statements show $7,899 thousand. Rounding only. The MD&A component figures ($4.9M, $1.5M) are narrated to one decimal and cannot be reconciled to the thousand, so all AI-cost derivations in this document use the narrated millions and are labelled accordingly.

### A4. AI Search growth: a sequential rate among annual rates

The CEO quote presents two YoY figures and one QoQ figure ("AI Search query growth of over 25% quarter-over-quarter") in a single sentence. The base is not disclosed and the metric appears nowhere else.

**Treatment:** reported as stated, used for no derivation. `aisearch_is_qoq_not_yoy = True` is asserted in the gate so the distinction cannot be lost downstream.

### A5. Buyback authorisation arithmetic

$500.0M authorised less $99.1M repurchased equals $400.9M, matching the disclosed remaining authorisation exactly. Verified as an identity with a tolerance of 0.051 to accommodate the one-decimal presentation.

### A6. Guardrail headroom rounding boundary

The Guardrail 1 headroom is $10.705M − $6.400M = **$4.305M**, which falls exactly on a two-decimal rounding boundary. The gate asserts this at three decimals and the figure is written as **$4.305M** throughout, so that no ambiguously rounded value can enter the document.

---

## 57. Appendix B — figures examined and not used

Documented so the reader knows what was considered and rejected.

**Prepared remarks and "Modeling Considerations" appendix.** The press release refers investors to prepared remarks posted on the investor relations site. These were not retrieved and nothing from them is used. They are not an SEC filing and fall outside this series' primary-source rule.

**Conference call commentary.** Not used, for the same reason.

**FY2026 quarterly revenue splits.** Only the FY2026 full-year revenue ($570,399 thousand) is used, from the 10-K. Quarterly FY2026 figures were not extracted, which is why the seasonality analysis in section 48 is qualitative rather than quantitative.

**Share price and market capitalisation.** Deliberately excluded. This series does not use market data.

**Analyst estimates.** Excluded — not primary sources.

**Risk-factor text from the 10-K.** Reviewed for AI disclosures; the four AI terms were counted across the full 10-K text and all returned zero. No risk-factor language is quoted, because the 10-K's risk factors were not the subject of this analysis.

---

## 58. Methodology

**Source acquisition.** Filings retrieved directly from SEC EDGAR by accession number over HTTPS with a declared user agent. No third-party data aggregators, no financial data APIs, no analyst summaries.

**Parsing.** Filing HTML parsed to text with BeautifulSoup and lxml, producing greppable plain text. Term counts in section 6.3 and Appendix A were computed mechanically against these parsed texts, case-insensitively.

**Gate-first discipline.** `verify.py` was written and passing **before any prose in this document existed.** Every derived figure here is produced by the gate. Prose may not introduce a derived number the gate has not computed.

**Rounding.** All percentages to two decimal places. The gate asserts against expected values with a tolerance of 0.005 absolute unless stated otherwise. Where a value falls on a rounding boundary (Appendix A6), it is asserted and written at three decimals.

**Rounded-intermediate discipline.** Derived figures are computed from unrounded inputs. Three checks in the gate — `implied_accel_vs_q1_pp`, `implied_accel_multiple`, `ai_share_of_gm_contraction_pct` — carry explicit comments noting that deriving them from the two-decimal values printed elsewhere produces different results, and that the unrounded computation is authoritative. This class of error was found and corrected in an earlier case study in this series and is now checked for deliberately.

**Cross-checking.** `crosscheck.py` extracts every two-decimal figure appearing in this README and in ASSUMPTIONS.md and confirms that each traces to a value the gate computed. A figure in the prose that the gate does not produce is a build failure.

**Author constructs.** RICE inputs, stress factors, persona details, the North Star proposal, guardrail thresholds, all scenario parameters and the eval plan are the author's own work and are labelled as such here and in ASSUMPTIONS.md. They are not disclosed data and are not presented as such.

**Fabrication policy.** No figure, quote, date or metric in this document is invented. Where information is unavailable, the document says so explicitly rather than estimating.

---

## 59. Reproducing this analysis

```bash
# 1. Retrieve the filings (CIK 0001516513)
#    10-Q  accession 0001516513-26-000040
#    EX-99.1 accession 0001516513-26-000038
#    10-K  accession 0001516513-26-000025

# 2. Run the gate. 310 checks. Non-zero exit on any failure.
python3 verify.py

# 3. Run the cross-check against the written deliverables.
python3 crosscheck.py
```

`verify.py` is self-contained: every as-filed input is declared as a named constant at the top with its source document, and every derived figure is computed from those constants. It has no dependencies beyond the Python standard library.

---

## 60. Limitations

This analysis covers **one quarter** of one company, using **three documents**. It does not include the earnings call, prepared remarks, prior-year quarterly detail, competitor filings, or any market data.

It does not evaluate Doximity's AI products. No clinical assessment of Scribe or Ask is made or implied, and none could be from filings alone.

It makes no claim that any statement by Doximity or its officers is false. The finding concerns **where** claims were published, not whether they are true.

The conclusion that AI caused **94.95%** of the gross-margin contraction rests on management's own attribution of the $4.9M and $1.5M to AI initiatives. That attribution is narrated in MD&A, is not an audited line item, and is qualified by "primarily."

The RICE output is a structured argument built on author estimates, not a calculation on disclosed data.

---

## 61. References

**Primary sources — SEC EDGAR, Doximity, Inc., CIK 0001516513**

1. Form 10-Q for the quarterly period ended 30 June 2026. Accession 0001516513-26-000040. Sections used: Condensed Consolidated Balance Sheets; Condensed Consolidated Statements of Operations; Condensed Consolidated Statements of Cash Flows; Note 1 (Organization); Note 3 (Revenue Recognition); Note 12 (Commitments and Contingencies); Note 13 (Leases); Management's Discussion and Analysis — Key Business and Financial Metrics, Results of Operations, Liquidity and Capital Resources.

2. Exhibit 99.1 to Form 8-K, earnings release for the quarter ended 30 June 2026. Accession 0001516513-26-000038. Sections used: financial highlights; CEO quote; Financial Outlook; Condensed Consolidated Statements of Operations; stock-based compensation detail; adjusted EBITDA reconciliation; free cash flow reconciliation.

3. Form 10-K for the fiscal year ended 31 March 2026. Accession 0001516513-26-000025. Used for: FY2026 total revenue ($570,399 thousand); term-count verification across the full annual report text.

4. EDGAR company submissions metadata, CIK 0001516513. Used for: exchange, ticker, SIC code, state of incorporation, fiscal year end.

**Litigation references** — all drawn from 10-Q Note 12:
*In re Doximity, Inc. Securities Litigation*, No. 5:24-cv-02281 (N.D. Cal.);
*In re Doximity, Inc. Stockholder Derivative Litigation*, No. 5:24-cv-02801 (N.D. Cal.);
*April v. Tangney et al.*, No. 3:26-cv-6201 (N.D. Cal.);
*Guttman v. Tangney, et al.*, No. 1:24-cv-01387 (D. Del.);
*Wong v. Tangney, et al.*, No. 1:25-cv-750 (D. Del.);
*Stern v. Tangney, et al.*, No. 2025-0661-NAC (Del. Ch.);
*Peter v. Tangney, et al.*, No. 2026-0220-NAC (Del. Ch.);
*OpenEvidence Inc. v. Doximity, Inc. et al.*, No. 1:25-cv-11802-RGS (D. Mass.).

**Series cross-references.** Day 80 (Hims & Hers) and Day 81 (Hinge Health) comparator figures are recomputed inside this case study's own `verify.py` from their originating gates and are not carried across as prose assertions.

**No secondary sources were used.** No news articles, analyst notes, market data or third-party databases inform any figure in this document.

---

## 62. Document control

| Field | Value |
|---|---|
| Case study | Day 82 of 90 |
| Subject | Doximity, Inc. (NYSE: DOCS) |
| Period analysed | Q1 FY2027, three months ended 30 June 2026 |
| Primary sources | 3 SEC filings |
| Verification checks | **310**, all passing |
| Files | `README.md`, `ASSUMPTIONS.md`, `verify.py`, `crosscheck.py` |
| Diagrams | Markdown tables and ASCII only (no Mermaid, per series standard from Day 50) |
| Fabricated figures | **0** |

---

## 63. Series index

| Day | Company | Central finding |
|---|---|---|
| 80 | Hims & Hers | AI narrative with zero disclosed AI metrics |
| 81 | Hinge Health | Discloses an AI cost metric, not a clinical one |
| **82** | **Doximity** | **AI cost is audited; every AI claim is quote-only** |
| 83 | OpenEvidence | *(forthcoming — plaintiff against Day 82's subject)* |

---

## 64. A closing note on method

The most useful thing this case study did was mechanical, and it took about thirty seconds: count how many times each AI claim appears in each document.

| | 10-Q | 10-K | Press release |
|---|---|---|---|
| NOHARM | 0 | 0 | 1 |
| AI Search | 0 | 0 | 1 |
| prescriber | 0 | 0 | 1 |
| Doximity Ask | 0 | 0 | 1 |

No modelling, no framework, no judgment. Four terms, three documents, `grep -c`.

That table is the case study. Everything else in this document explains why it matters. A product manager evaluating any vendor's AI claims can run the same test on any public company in an afternoon: take the claims from the marketing, search for them in the filings, and see which ones survive.

**The claims that do not appear in the filing are the claims nobody had to stand behind.**

---

## 65. Standing questions for Doximity

Five questions this analysis cannot answer from public disclosure, ordered by how much they would change the assessment:

1. **Do AI sessions generate advertising impressions, or bypass them?** If they bypass them, the AI suite is reducing the revenue of the business that funds it, and no disclosure would currently reveal this.
2. **What percentage of Scribe notes are signed without material edit?** The only measure of whether the product works.
3. **What is the absolute number of providers using the AI suite?** Only the growth rate of a nine-behaviour union metric is disclosed.
4. **What is AI-attributable revenue?** Cost is disclosed; revenue is not. Without it, no one outside the company can assess return.
5. **Why did the NOHARM result appear in a press release and not the 10-Q?** There are good, ordinary answers to this. The question is worth asking because the cost figure went the other way.

---

*Day 82 of 90. Built from primary sources. 310 programmatic checks. Zero fabricated figures.*
