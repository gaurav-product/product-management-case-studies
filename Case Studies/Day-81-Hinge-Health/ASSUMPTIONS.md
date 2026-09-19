# ASSUMPTIONS — Day 81: Hinge Health, Inc.

This file is the audit trail for the Day 81 case study. It separates what the company disclosed from what the author computed, constructed, or could not establish. Every figure in `README.md` falls into exactly one of Parts 1 through 3, and `crosscheck.py` confirms that no two-decimal figure appears in the deliverables without a corresponding computation in `verify.py`.

**Standing principle of this series: zero fabrication.** Where a figure is unavailable it is stated to be unavailable. Where a company states an approximation, the approximation is carried as stated and never sharpened.

---

## Part 1 — What the company disclosed

Every figure in this part is transcribed directly from a primary source. Nothing here is computed.

### 1.1 From the Form 10-Q for the quarter ended 30 June 2026 (filed 6 August 2026, accession 0001628280-26-054327) and Exhibit 99.1 to the Form 8-K filed 4 August 2026 (accession 0001628280-26-052558)

**Condensed consolidated statements of operations ($k):**

| Item | Q2 2026 | Q2 2025 | H1 2026 | H1 2025 |
|---|---|---|---|---|
| Revenue | 212,817 | 139,098 | 395,124 | 262,923 |
| Cost of revenue | 28,868 | 41,335 | 56,942 | 64,927 |
| Gross profit | 183,949 | 97,763 | 338,182 | 197,996 |
| Research and development | 34,057 | 279,962 | 64,395 | 303,462 |
| Sales and marketing | 81,408 | 147,228 | 150,210 | 193,944 |
| General and administrative | 28,044 | 251,244 | 51,068 | 268,125 |
| Total operating expenses | 143,509 | 678,434 | 265,673 | 765,531 |
| Income (loss) from operations | 40,440 | (580,671) | 72,509 | (567,535) |
| Other income, net | 3,990 | 4,694 | 7,863 | 9,695 |
| Provision for (benefit from) income taxes | 740 | (326) | 1,554 | 672 |
| Net income (loss) | 43,690 | (575,651) | 78,818 | (558,512) |

**Non-GAAP reconciliation — gross profit ($k):** stock-based compensation 1,128 / 16,441 / 1,965 / 16,441; employer payroll tax on stock compensation 45 / 893 / 150 / 893; amortisation of intangible assets 224 / 225 / 449 / 406. Non-GAAP gross profit 185,346 / 115,322 / 340,746 / 215,736. Stated GAAP gross margin 86% / 70% / 86% / 75%; stated non-GAAP gross margin 87% / 83% / 86% / 82%.

**Non-GAAP reconciliation — income from operations ($k):** stock-based compensation 19,092 / 590,983 / 30,784 / 590,990; employer payroll tax on stock compensation 1,316 / 14,227 / 2,800 / 14,227; amortisation 224 / 225 / 449 / 406; acquisition-related expenses 440 / 1,337 / 1,134 / 2,968. Non-GAAP income from operations 61,512 / 26,101 / 107,676 / 41,056. Stated GAAP operating margin 19% / (417)% / 19% / (216)%; stated non-GAAP operating margin 29% / 19%.

**Cash flow ($k):** free cash flow 99,559 / 32,627 / 141,112 / 36,793, with stated free cash flow margin 47% / 23% / 36% / 14%. Net cash provided by operating activities stated as $101.4 Mn (Q2 2026) and $20.2 Mn (Q2 2025).

**Balance sheet at 30 June 2026 ($k):** cash and cash equivalents 286,224 (207,995 at 31 December 2025); short-term marketable securities 103,167 (155,867). Cash, cash equivalents, marketable securities and restricted cash stated as $475.6 Mn.

**Per share:** GAAP diluted net income per share $0.52 (Q2 2026) against a GAAP diluted net loss per share of $13.10 (Q2 2025). Non-GAAP diluted net income per share $0.59 against $0.30.

**Key business metrics:** clients 2,929 at 30 June 2026 against 2,359 at 30 June 2025, stated as +24%. LTM calculated billings $861.8 Mn against $568.4 Mn, stated as +52%. Contracted lives 25 million as at 31 December 2025. Twelve-month client retention 97% as at 31 December 2025. "Over 60 partners," including "the five largest national health plans by self-insured lives, and the top three PBMs by market share." Average contract term three years. Typical sales cycle five months, over 12 months for larger enterprise clients. Implementations completed in a 40–100 day period.

### 1.2 The AI disclosure, quoted in full

This sentence is load-bearing for the entire case study and is reproduced exactly as filed:

> "According to our estimates based on data from 2025, our platform reduced the number of human care team hours associated with traditional physical therapy by approximately 97%."

The same sentence appears in the Form 10-K for the fiscal year ended 31 December 2025.

**Disclosed AI systems and uses:** **TrueMotion**, "our proprietary AI-powered motion tracking technology," which "allows us to deliver highly scalable care remotely and reduce the human hours associated with traditional physical therapy" and which replaced wearable sensors for members. **HingeConnect**, "our proprietary AI-driven database for real-time care interventions and external provider coordination." The care team is described as "our AI-supported care team of licensed physical therapists, physicians, and board-certified health coaches."

**Stated uses of AI Technologies:** "to support our care team and to assist with developing personalized exercise therapy plans, providing real-time feedback on an exercise form, identifying high-risk members for targeted interventions, and generally enhancing our operational efficiency and competitiveness."

**Stated technology dependence:** "In addition to our proprietary AI Technologies, we use AI Technologies licensed from third parties in our platform and programs… We cannot control the availability or pricing of such third-party AI Technologies."

**Named AI regulation:** Utah's Artificial Intelligence Policy Act; the Texas Responsible Artificial Intelligence Governance Act (TRAIGA), "which requires disclosures to patients when AI systems are used"; California laws including a provision "prohibiting AI systems from using professional terminology, interface elements or branding that suggest or imply medical authority or licensed professional involvement when no such oversight exists"; CCPA automated-decision-making regulations effective 1 January 2026 with compliance required by 1 January 2027; and the EU AI Act.

### 1.3 Business model mechanics

Revenue is recognised "ratably over the 12 months after an eligible life becomes a member." Clients "only pay for the members that engage with our programs." Most clients are billed "through an engagement-based pricing model based on an annual upfront platform fee per member plus a fee per each completed billable session." Performance guarantees "may include engagement thresholds, member reported outcomes, and return on investment, where we put a portion of our fees at risk," and the company states: "We have historically paid an immaterial amount related to these performance guarantees." Calculated billings show seasonality and are "highest in the second quarter"; free cash flow "is typically highest in the second or third quarter."

### 1.4 Acquisition, capital return and guidance

**Cylinder Health:** definitive agreement announced 4 August 2026, **$105 million in cash consideration**, expected to close in Q3 2026, with an integrated Gastrointestinal Care Program "expected to launch in 2027."

**Share repurchases:** programme authorised 10 November 2025 for up to **$250.0 million**. **$196.5 million** repurchased as at 29 July 2026. On 29 July 2026 the board approved an increase "resulting in $300.0 million of our Class A common stock available for future repurchase, for a total aggregate amount authorized under the program of $496.5 million."

**Guidance:** Q3 2026 revenue $223–225 million (stated +45% at midpoint); Q3 non-GAAP income from operations $61–63 million (stated +104%, 28% margin at midpoint). Full year 2026 revenue $856–860 million (stated +46% at midpoint); full year non-GAAP income from operations $236–244 million (stated +101%, 28% margin at midpoint).

### 1.5 From the Form 10-K for the fiscal year ended 31 December 2025 (filed 3 March 2026, accession 0001628280-26-013808)

Revenue $587,860k (FY2025), $390,404k (FY2024), $292,730k (FY2023). Cost of revenue $119,638k, $90,502k, $98,551k. Gross profit FY2025 $468,222k.

### 1.6 From the SEC EDGAR submissions index (CIK 0001673743)

SIC **7374 — Services-Computer Processing & Data Preparation**. State of incorporation Delaware. Fiscal year end 31 December. Exchange NYSE, ticker HNGE. Business address San Francisco, California.

---

## Part 2 — What the author computed from disclosed figures

Every figure in this part is derived arithmetically from Part 1 and computed in `verify.py` to two decimal places with a tolerance of 0.005. **144 checks, all passing.** No figure here is an estimate.

**Growth and its decomposition.** Revenue growth **53.00%** (Q2) and **50.28%** (H1); the increase was **$73.72 Mn**. Client growth **24.16%**. Revenue per client **$72.66k** against **$58.96k**, growth **23.22%**. Compounding client growth with revenue-per-client growth gives **53.00%**, matching reported revenue growth with a residual of **0.00 pp**. Acquired revenue in the quarter: **$0** — Cylinder had not closed. Full-year history: FY2025 growth **50.58%**, FY2024 growth **33.37%**.

**The margin headline.** GAAP gross margin **86.44%** against **70.28%**, a change of **+16.15 pp**. Non-GAAP gross margin **87.09%** against **82.91%**, a change of **+4.18 pp**. The wedge is **11.97 pp**, which is **74.09%** of the GAAP expansion; the operating improvement is **25.91%** of it. Cross-checked from the reconciliation lines: gross-profit adjustments were **12.62%** of revenue in Q2 2025 and **0.66%** in Q2 2026, a wedge of **11.97 pp**. Stock compensation alone in Q2 2025 cost of revenue was **11.82%** of that quarter's revenue.

**The cost of delivering care.** GAAP cost of revenue fell **30.16%** (Q2) and **12.30%** (H1). Non-GAAP cost of revenue **rose 15.54%**, from **$23.78 Mn** to **$27.47 Mn**, and fell as a share of revenue from **17.09%** to **12.91%**. Revenue grew **3.41×** faster than non-GAAP delivery cost, a gap of **37.46 pp**. Delivery cost per client **$9.38k** against **$10.08k**, down **6.94%**. GAAP gross profit grew **88.16%**; non-GAAP gross profit grew **60.72%**. FY2025 cost of revenue grew **32.19%** and FY2025 GAAP gross margin was **79.65%**.

**The automation ceiling.** Residual human care hours **3.00%** of the traditional baseline. Implied leverage **33.33×**. The harvested pool is **32.33×** the remaining pool. Halving the residual recovers **1.50 pp** of the original baseline. Maximum further gross margin available if delivery cost went to zero: **12.91 pp**; the non-GAAP expansion already achieved is **0.32×** that maximum. Disclosed clinical outcome metrics: **0**. Disclosed AI accuracy or evaluation metrics: **0**. Disclosed inference or AI cost metrics: **0**.

**Operating margin and the IPO charge.** GAAP operating margin **19.00%** against **−417.45%**. Non-GAAP operating margin **28.90%** against **18.76%**, a change of **+10.14 pp**; non-GAAP income from operations grew **135.67%**. Stock compensation was **424.87%** of revenue in Q2 2025 and **8.97%** in Q2 2026, a fall of **96.77%**. Total operating expenses fell **78.85%**. As a share of Q2 2026 revenue: sales and marketing **38.25%**, research and development **16.00%**, general and administrative **13.18%**. Net margin **20.53%**.

**Cash.** Free cash flow grew **205.14%**, a multiple of **3.05×**. Free cash flow margin **46.78%** (Q2 2026), **23.46%** (Q2 2025), **35.71%** (H1 2026). Operating cash flow margin **47.65%**. Implied capital expenditure **$1.84 Mn**, or **0.87%** of revenue.

**Capital allocation.** Repurchases to date are **1.87×** the Cylinder price and **1.39×** H1 2026 free cash flow. Total authorisation is **4.73×** the Cylinder price and **104.39%** of cash, securities and restricted cash. The authorisation identity closes: $196.5 Mn repurchased plus $300.0 Mn available equals $496.5 Mn authorised. The **actual increase** in total authorisation was **$246.5 Mn**, which is **$53.5 Mn** below the headline "$300 million increase" and **82.17%** of it.

**Billings, clients and penetration.** LTM calculated billings grew **51.62%**. Billings per client **$294.23k** against **$240.95k**, growth **22.11%**. Guided FY2026 revenue per contracted life **$34.32**.

**Guidance arithmetic.** FY2026 midpoint **$858.00 Mn**, growth **45.95%** over FY2025 — **7.04 pp** below the Q2 actual growth rate. Implied H2 2026 revenue **$462.88 Mn**, **+17.15%** over H1. Q3 midpoint **$224.00 Mn**, **+5.25%** over Q2 actual; implied Q4 **$238.88 Mn**, **+6.64%** over the Q3 midpoint. Guided FY2026 non-GAAP operating margin **27.97%**; H1 actual **27.25%**; implied H2 **28.59%**.

**Scale arithmetic.** A $1 Bn annual run-rate requires **3,440.75** clients at the current revenue per client — **511.75** more than today — or, holding clients flat, revenue per client of **$85.35k**, an uplift of **17.47%**.

**Register tally.** **70.59%** of companies examined since Day 46 carry a classification that does not describe the business (12 of 17), up **1.84 pp** from Day 80.

---

## Part 3 — What the author constructed

These are the author's own designs and models. **None is a company figure.** Each is labelled in the README at the point of use.

**3.1 The AI cost bound (§29).** The company discloses no AI interaction count, no care-hour count and no inference cost. The figures of **$9.38k** per client per quarter, **$3.13k** per client per month and **$4.40** per contracted life per year attribute the **entire** non-GAAP cost of revenue to care delivery. That attribution is knowingly generous — the line also covers fulfilment of the Enso device, platform hosting and other delivery costs. They are **ceilings, not estimates**, and their analytical purpose is to establish that even the maximum conceivable figure is small relative to the sales and marketing line.

**3.2 The residual-pool arithmetic (§29).** The 3.00% residual, 33.33× leverage, 32.33× harvested-to-remaining ratio and 1.50 pp halving figure are arithmetic consequences of the company's stated "approximately 97%." They inherit that approximation exactly and should be read as carrying the same imprecision. They are not independent measurements of anything.

**3.3 The RICE model (§47).** All four initiatives, and every Reach, Impact, Confidence and Effort input, are author constructs. Reach uses the disclosed client count of 2,929. Impact and Confidence are judgements. Effort is in person-months and is an author estimate.

The **stress multiplier is 3.00%** — the residual human care hours. The proposal measures outcome per retained human hour, so its reach is bounded by the hours that still exist.

**The exemption rule, stated explicitly:** the stress multiplier is applied only to initiatives whose reach depends on the residual human-hour pool. Publishing the denominator, reporting an outcome metric and instrumenting care hours are exempt because their reach is the whole client base and depends on no external party. Escalation Yield is stressed because it can only act where human hours remain.

`verify.py` asserts programmatically that the proposal ranks **last of four** both under stress and at baseline before the multiplier is applied. If a future revision changed an input such that the proposal led, the gate would fail and the case study would not build.

**3.4 OPH and MED-90 (§31, §55).** The North Star metric, its four numerator conditions, the guardrail and its 90th-percentile construction are the author's design. No company metric of this kind exists or is claimed to exist.

**3.5 The Escalation Yield proposal (§50, §51, §52, §53).** Entirely the author's. The schema, the trigger-provenance fields, the held-out arm, the schema-level denial to cost-objective systems, the rollout phases, the success bars and the wireframes are proposals, not descriptions. The identifiers in §52 — episode 55120388, member 88104, condition MSK-LBP-02, model version `escalation-risk-6.1`, and the clinician name "Sarah K." — are **illustrative placeholders** and correspond to nothing real.

**3.6 The SQL in §32.** The schema is hypothetical; table and column names are invented for the illustration. Both queries are PostgreSQL dialect and were parsed with `sqlglot` before delivery; parsing confirms syntactic validity only and says nothing about whether such tables exist.

**3.7 Personas (§20).** Renu, Marcus, Dana and Ellie are constructs derived from disclosed mechanics — the automated pathway, the high-risk flagging described in the AI disclosure, the performance-guarantee structure and the 2026 migraine launch. They are not research subjects, and no user research was conducted.

**3.8 TAM/SAM/SOM (§13).** Built from the company's own disclosed contracted lives and guidance rather than a third-party market estimate, because no third-party figure could be verified to this series' standard. The $1 Bn run-rate arithmetic is a framing device, not a forecast, and the company has issued no such target.

**3.9 The eval plan, failure-mode ranking and human-in-the-loop rules (§29).** Author constructs. The pass bars — ≥90% escalation precision, ≥95% form-feedback agreement, pre-registered non-inferiority — are proposed standards, not observed performance, and the company has published no performance against which to compare them.

**3.10 Kano, HEART, AARRR and Porter classifications (§16, §33, §34, §49).** Analytical judgements applying standard frameworks to disclosed facts.

---

## Part 4 — What could not be established

Named explicitly rather than filled in.

1. **The absolute human-hour denominator behind the 97%.** Neither the hours removed nor the hours remaining is disclosed, so the figure has a ratio and no magnitude.
2. **The "traditional physical therapy" baseline.** The counterfactual is company-defined and undisclosed. A 97% reduction is only as meaningful as the baseline it is measured against, and that baseline cannot be inspected.
3. **Any clinical outcome metric in the filings.** No pain score, function measure, surgery-avoidance rate or endpoint attainment figure appears. This is a precise claim about the SEC filings and **not** a claim that no outcome evidence exists — see Part 5.
4. **Automation rate by condition.** The 97% is stated for physical therapy. Migraine launched in 2026 and GI has not launched. No per-condition figure is disclosed.
5. **Member-level retention and engagement.** Client retention is disclosed at 97%; member retention, adherence, session counts and completion rates are not, despite completed sessions being the revenue trigger.
6. **Contracted lives at 30 June 2026.** Disclosed only as at 31 December 2025, so every per-life figure here is computed on a denominator up to six months stale and is labelled accordingly.
7. **Performance guarantee thresholds.** The company states it has "historically paid an immaterial amount." Whether that reflects comfortable outperformance or conservatively set thresholds cannot be determined from the filings.
8. **AI model names, vendors, or the split between proprietary and licensed technologies.** Disclosed only as a category.
9. **The allocation logic for residual human hours.** HingeConnect is described as identifying high-risk members; the criteria, thresholds and outcomes of that flagging are not disclosed.
10. **Cylinder Health standalone financials.** Only the $105 Mn price is disclosed; no revenue, margin or client figure.
11. **Any user-side evidence.** No interviews, usability testing or review-corpus analysis. §25, §26 and §27 are correspondingly thin, and §64 says so.

---

## Part 5 — Method, precision and what a future revision should do

**Sources.** Two SEC filings made within two days of each other by the same registrant carry the financial argument, with the FY2025 Form 10-K for trend. There are **no secondary sources** in this case study; every figure traces to an SEC filing or to arithmetic on one.

**Precision policy.** All derived figures are computed to two decimal places with a tolerance of 0.005. Where an input is itself rounded or approximate — "approximately 97%", operating cash flow stated to $0.1 Mn, "over 60 partners", "25 million" contracted lives — every figure derived from it inherits that imprecision. Such figures are presented to two decimals for consistency with the series, and this paragraph is the standing qualification on all of them.

**Approximations are carried, not sharpened.** The 97% is the clearest case. It is a company estimate, on a company-defined baseline, from 2025 data, reported in an August 2026 filing. The entire residual-pool arithmetic in §29 rests on it. Presenting "3.00%" as though it were measured would overstate what is known; the README's §29 states all five qualifications explicitly before any of that arithmetic is used, and Appendix C repeats the caveat.

**The two 97%s are never conflated.** The automation figure and the client retention figure share a number and nothing else. Appendix D exists solely to prevent that error, and every reference in the README specifies which is meant.

**Roundings are documented, not silently adopted.** The company states 86% GAAP gross margin, 53% revenue growth, "$100 million" free cash flow and "up 3x". The computed figures are 86.44%, 53.00%, $99.56 Mn and 3.05×. Appendix A records every such difference.

**One presentation point is flagged rather than treated as a finding.** The release headlines a "$300 million increase" to the buyback where the actual increase in total authorisation was $246.5 Mn, the $300.0 Mn being the amount available. Both figures are the company's own and the identity closes. Appendix B sets it out; the body does not treat it as a business finding, because it is not one.

**What a future revision should add.**

1. **Read the published clinical literature alongside the filings.** Hinge publishes peer-reviewed outcome research outside its SEC disclosures. Incorporating it would let the case study distinguish *not measured* from *not disclosed in filings* — a materially different and fairer critique, and the single change that would most improve this piece.
2. Member-side evidence on the automated pathway, which would fix §25 and §26.
3. Re-examine after Q3 2026, when Cylinder will have closed and the growth decomposition will need an acquired-revenue line for the first time.
4. Track whether a per-condition automation rate appears as migraine and GI scale, and whether the platform-wide 97% is extended to them.
5. Track whether any clinical outcome metric enters the filings, and whether a member-facing AI-disclosure surface appears ahead of the 1 January 2027 CCPA compliance date.

---

*Day 81 of 90 · Verified with `verify.py` — 144 checks, all passing · Cross-checked with `crosscheck.py`*
