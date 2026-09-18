# ASSUMPTIONS — Day 80: Hims & Hers Health, Inc.

This file is the audit trail for the Day 80 case study. It separates what the company disclosed from what the author computed, constructed or could not establish. Every figure in `README.md` falls into exactly one of Parts 1 through 3, and `crosscheck.py` confirms that no two-decimal figure appears in the deliverables without a corresponding computation in `verify.py`.

**Standing principle of this series: zero fabrication.** Where a figure is unavailable it is stated to be unavailable. Where a company states a bound, the bound is carried as a bound and never sharpened into a point estimate.

---

## Part 1 — What the company disclosed

Every figure in this part is transcribed directly from a primary source. Nothing here is computed.

### 1.1 From the Form 10-Q for the quarter ended 30 June 2026 (filed 10 August 2026, accession 0001773751-26-000163)

| Item | Q2 2026 | Q2 2025 | H1 2026 | H1 2025 |
|---|---|---|---|---|
| Revenue ($k) | 753,214 | 544,833 | 1,361,318 | 1,130,843 |
| Cost of revenue ($k) | 272,411 | 128,637 | 483,728 | 283,958 |
| Gross profit ($k) | 480,803 | 416,196 | 877,590 | 846,885 |
| Marketing ($k) | 262,236 | 217,862 | 484,239 | 449,097 |
| Operations and support ($k) | 95,481 | 66,490 | 191,984 | 129,523 |
| Technology and development ($k) | 54,901 | 37,848 | 101,837 | 67,762 |
| General and administrative ($k) | 165,377 | 67,273 | 275,045 | 115,883 |
| Total operating expenses ($k) | 577,995 | 389,473 | 1,053,105 | 762,265 |
| (Loss) income from operations ($k) | (97,192) | 26,723 | (175,515) | 84,620 |
| Net (loss) income ($k) | (86,290) | 42,505 | (178,405) | 91,990 |
| United States revenue ($k) | 621,830 | 537,286 | 1,151,739 | 1,115,978 |
| Rest of the World revenue ($k) | 131,384 | 7,547 | 209,579 | 14,865 |

**Balance sheet as at 30 June 2026 ($k):** cash and cash equivalents 609,811; goodwill 1,101,720 (against 278,325 at 31 December 2025); intangible assets net 422,809; total assets 3,628,814; total liabilities 3,304,742; total stockholders' equity 324,072 (against 540,928); convertible senior notes net 1,365,299; deferred acquisition payable 537,381 current and 165,624 non-current; accumulated deficit (292,177).

**Shares as at 30 June 2026:** Class A 224,920,310 issued and outstanding; Class V 8,377,623.

**Eucalyptus acquisition, June 2026 — preliminary purchase price allocation ($k):** purchase price for accounting purposes 968,539; cash paid upfront 225,000; deferred payments 683,900 over six quarterly instalments through the 18-month anniversary of closing; contingent consideration at acquisition-date fair value 59,600 against a potential aggregate earn-out of up to 96,600. Allocation: trade name 93,796; developed technology 56,564; customer relationships 35,084; goodwill 790,333; other net liabilities (7,238). Post-combination compensation of 6,000 recognised at closing within G&A, with up to 131,300 remaining to be recognised over the service periods. Acquisition costs of 10,200 recorded in G&A. No Class A shares were issued at closing.

**Eucalyptus revenue contribution as disclosed:** approximately 5% of total consolidated revenue for the three months ended 30 June 2026, and less than 5% for the six months. On a pro forma basis, approximately 15% of consolidated revenue for each of the three and six months ended 30 June 2026 and approximately 10% for each of the comparable 2025 periods.

**Technology and development increase, Q2, as decomposed by the company:** depreciation, amortisation and technology costs $7.9 Mn; product development costs $3.3 Mn; professional services $3.2 Mn; stock-based compensation $1.4 Mn. For the six months: depreciation, amortisation and technology costs $14.0 Mn; product development $6.0 Mn; employee compensation excluding stock-based compensation $4.4 Mn; professional services $3.5 Mn; stock-based compensation $3.3 Mn.

**Cost of revenue increase drivers, Q2:** product and packaging costs +141%; shipping costs +56%; costs associated with medical consultation services +30%. H1 cost of revenue included $28.5 Mn of non-recurring restructuring charges consisting of inventory write-downs in connection with the 2026 US WL Announcement.

**Litigation:** FTC Civil Investigative Demand issued October 2023 regarding privacy, advertising, subscription and cancellation practices. On 29 July 2026 the FTC, the Utah Division of Consumer Protection and Los Angeles County on behalf of the People of the State of California filed a complaint in the United States District Court for the Northern District of California alleging violations of Section 5 of the FTC Act and certain provisions of ROSCA and analogous state statutes. **Accrual of approximately $60 million** recorded as at 30 June 2026. A putative class action followed in the same court under ECPA, CIPA, CMIA and other theories. Separately, the Australian Therapeutic Goods Administration issued compulsory notices to Eucalyptus subsidiaries between September 2023 and August 2025 concerning alleged non-compliance with prescription-medicine advertising laws; the company is entitled to indemnification from certain warrantors.

**Brand mix:** Hers represented over 40% of United States revenue in Q2 2026, against approximately 35% in Q2 2025, and approximately 40% in each of the six-month periods. A majority of total United States revenue came from non-GLP-1 offerings in both the three and six months ended 30 June 2026.

### 1.2 From Exhibit 99.1 to the Form 8-K filed 10 August 2026 (accession 0001773751-26-000161)

| Key business metric | Q2 2026 | Q2 2025 | H1 2026 | H1 2025 |
|---|---|---|---|---|
| Subscribers, end of period (thousands) | 2,891 | 2,439 | 2,891 | 2,439 |
| Monthly Revenue per Average Subscriber | $92 | $76 | $84 | $81 |

**Stated highlights:** gross margin 64% for Q2 2026 against 76% for Q2 2025; net loss $86.3 Mn against net income $42.5 Mn; Adjusted EBITDA $60.3 Mn against $82.2 Mn; net cash used in operating activities $(35.9) Mn against $(19.1) Mn; free cash flow $(68.2) Mn against $(69.4) Mn.

**Adjusted EBITDA add-backs, Q2 2026 ($k):** legal contingencies 47,500; stock-based compensation 42,116; depreciation and amortisation 29,477; acquisition and transaction-related costs 28,835; restructuring and other related charges 4,626; change in fair value of liabilities 4,223; payroll tax expense related to stock-based compensation 2,022; impairment of long-lived assets 1,148.

**Guidance:** Q3 2026 revenue $880–900 Mn and Adjusted EBITDA $75–95 Mn; full-year 2026 revenue $3.1–3.3 Bn and Adjusted EBITDA $275–325 Mn. Stated long-term targets of at least $6.5 Bn revenue and $1.3 Bn Adjusted EBITDA by 2030.

**Quoted statements relied on in the README:** CEO Andrew Dudum, "As we rebuild the consumer health experience from the ground up with a doctor-led AI clinical engine…"; CFO Yemi Okupe, "This momentum, combined with the meaningful efficiencies we're generating from our investments in AI and technology…"

### 1.3 Definitional language relied on in §30

Quoted from the 10-Q and the press release, and load-bearing for the central finding:

> "'Subscribers' are customers who have one or more 'Subscriptions'… **Customers who have made one-time purchases are not considered Subscribers.**"

> "'Monthly Revenue per Average Subscriber' is defined as **total revenue** divided by 'Average Subscribers'…"

> "This metric includes revenue contributed by customers who made one-time purchases and therefore were not considered Subscribers. If the revenue contribution of customers who made one-time purchases was excluded from this metric, Monthly Revenue per Average Subscriber for each of the three and six months ended June 30, 2026 **would have been lower by approximately $10**, and… for each of the three and six months ended June 30, 2025 **would have been lower by less than $5**."

> "If Eucalyptus revenue and Average Subscribers were excluded from this metric, Monthly Revenue per Average Subscriber for the three months ended June 30, 2026 would have been **$90**."

---

## Part 2 — What the author computed from disclosed figures

Every figure in this part is derived arithmetically from Part 1 and is computed in `verify.py` to two decimal places with a tolerance of 0.005. **151 checks, all passing.** No figure here is an estimate.

**Growth composition.** Total revenue increase $208,381k; United States increase $84,544k; Rest of the World increase $123,837k. RoW share of the increase **59.43%**; US share **40.57%**. US growth **15.74%** in the quarter and **3.20%** across the half; total growth **38.25%** and **20.38%**. Gap between headline and US growth **22.51 pp**. US share of revenue fell from **98.61%** to **82.56%**, a shift of **−16.06 pp**.

**Margins.** Gross margin **63.83%** against **76.39%**, a fall of **12.56 pp**; H1 **64.47%** against **74.89%**. Gross profit growth **15.52%** against revenue growth **38.25%**, a wedge of **22.72 pp**. Gross profit forgone to margin compression, computed as Q2 2026 revenue at the Q2 2025 margin less actual Q2 2026 gross profit: **$94,574.51k**. Operating margin **−12.90%** against **+4.90%**; net margin **−11.46%** against **+7.80%**.

**Operating leverage.** Total operating expenses **76.74%** of revenue against **71.48%**, deleverage of **5.25 pp**. Marketing **34.82%** against **39.99%**, levering down **5.17 pp**. Operations and support **12.68%** against **12.20%**, **+0.47 pp**. Technology and development **7.29%** against **6.95%**, **+0.34 pp**. G&A **21.96%** against **12.35%**, **+9.61 pp**; G&A grew **145.83%** and supplied **52.04%** of the total operating expense increase.

**The AI spend line.** Technology and development increase $17,053k, **+45.06%** in the quarter and **+50.29%** across the half. Named drivers total $15,800k, **92.65%** of the increase. Depreciation, amortisation and technology costs **46.33%**; product development **19.35%**; professional services **18.77%**; stock-based compensation **8.21%**. Depreciation plus professional services **65.09%**. Marketing spend is **4.78×** technology and development in Q2 2026, against **5.76×** in Q2 2025.

**The unit metric.** Subscriber growth **18.53%**, an increase of 452k. Reported MRAS growth **21.05%**. One-time revenue as a share of the reported metric: **10.87%** in Q2 2026 and at most **6.58%** in Q2 2025. Subscriber-only MRAS approximately **$82** in 2026 and above **$71** in 2025. Adjusted growth bounded between **7.89%** and **15.49%**; the reported rate exceeds the maximum adjusted rate by **5.56 pp**. Eucalyptus contributed **$2.00** of the reported $92. Implied annualised revenue per average subscriber on the reported basis **$1,104.00**.

**The acquisition.** Goodwill **81.60%** of the Eucalyptus price; trade name **9.68%**; developed technology **5.84%**; customer relationships **3.62%**. Trade name is **1.66×** developed technology; goodwill is **13.97×** developed technology. Identifiable intangibles **19.15%** of the price. Cash paid upfront **23.23%**; deferred and contingent **76.77%**. Remaining acquisition compensation is **2.32×** the developed technology acquired. Balance-sheet goodwill grew **295.84%**, and stands at **30.36%** of total assets and **3.40×** total stockholders' equity.

**Litigation in context.** The $60 Mn accrual is **99.50%** of Q2 2026 Adjusted EBITDA, **7.97%** of Q2 revenue and **1.09×** Q2 technology and development spend. Legal contingencies added back in Adjusted EBITDA are **6.31%** of revenue.

**Adjusted EBITDA.** Margin **8.01%** against **15.09%**, a fall of **7.08 pp**; Adjusted EBITDA fell **26.64%**. Listed add-backs total $159,947k, **2.65×** the Adjusted EBITDA reported and **21.24%** of revenue. The gap between net loss and Adjusted EBITDA is **$146,590k**. Free cash flow margin **−9.05%** against **−12.74%**; operating cash flow margin **−4.77%**.

**Guidance arithmetic.** FY2026 revenue midpoint $3,200,000k, implying H2 revenue of **$1,838,682k**, **+35.07%** over H1. Q3 midpoint $890,000k, **+18.16%** over Q2 actual, implying Q4 of **$948,682k**, **+6.59%** over the Q3 midpoint. Guided FY2026 Adjusted EBITDA margin at midpoints **9.375%**. The 2030 revenue target is **2.03×** the FY2026 midpoint and the Adjusted EBITDA target **4.33×**; the target margin is **20.00%**, requiring **10.625 pp** of expansion.

**2030 subscriber arithmetic.** At the reported MRAS of $92, the 2030 revenue target implies **5,887.68k** subscribers, **2.04×** today's base. At the subscriber-only MRAS of approximately $82 it implies **6,605.69k** — **718.01k more subscribers**. Today's subscriber base at today's reported MRAS annualises to **49.10%** of the 2030 target.

---

## Part 3 — What the author constructed

These are the author's own designs and models. **None of them is a company figure.** They are labelled in the README at the point of use.

**3.1 The upper-bound AI cost per interaction (§29).** The company discloses no AI interaction count, no adoption rate and no inference cost. The figures of **$18.99** per subscriber per quarter, **$6.33** per subscriber-month, **6.88%** of reported MRAS and **7.72%** of subscriber-only MRAS are computed by attributing the **entire** technology and development line to AI. That attribution is knowingly false — the line also covers the digital platform, websites, mobile applications, third-party software and hosting, data science and related depreciation. The figures are therefore **ceilings, not estimates**, and are presented as such. Their analytical purpose is to establish that even the maximum conceivable AI cost is small relative to the margin movement in the quarter.

**3.2 The RICE model (§47).** All four initiatives, and every Reach, Impact, Confidence and Effort input, are author constructs. Reach uses the disclosed subscriber count of 2,891k. Impact and Confidence are judgements. Effort is in person-months and is an author estimate.

The **stress multiplier is 40.57%** — the share of Q2 revenue growth that came from the United States rather than from acquisition, which the author takes as the share of growth the existing product created. Applying it to the proposal's Reach models the case in which the proposal can only reach the population the existing product actually grew.

**The exemption rule, stated explicitly:** the stress multiplier is applied only to initiatives whose reach depends on the existing clinical apparatus — providers, labs, acquired platforms and regulators. The metric split, the cancellation remediation and the AI logging harness are exempt because their reach is internal and depends on no external party. Care Ledger is stressed because it depends on all four.

`verify.py` asserts, programmatically, that the proposal ranks **last of four** both under stress and at baseline before the multiplier is applied. If a future revision changed an input such that the proposal led, the gate would fail and the case study would not build. This is the series' standing discipline: the conclusion is enforced by the code, not by the prose.

**3.3 LCP/1k and CCR-90 (§31, §55).** The North Star metric, its four numerator conditions, the guardrail and its 90th-percentile construction are the author's design. No company metric of this kind exists or is claimed to exist.

**3.4 The Care Ledger proposal (§50, §51, §52, §53).** Entirely the author's. The schema, the mandatory AI fields, the schema-level exclusion of retention systems, the rollout phases, the success bars and the wireframes are proposals, not descriptions. The model version `care-routing-4.2`, the provider identifier `PRV-1182`, the subscriber identifier and the event identifier in §52 are **illustrative placeholders** and correspond to nothing real.

**3.5 The SQL in §32.** The schema is hypothetical. Table and column names are invented for the illustration. Both queries are written in PostgreSQL dialect and were parsed with `sqlglot` before delivery; parsing confirms syntactic validity only and says nothing about whether such tables exist.

**3.6 Personas (§20).** Priya, Dan, Alia and Tom are constructs derived from disclosed mix — the membership programme, cadence ranges, the one-time purchaser disclosure and the Eucalyptus contribution. They are not research subjects, and no user research was conducted.

**3.7 TAM/SAM/SOM (§13).** Built backwards from the company's own 2030 target rather than forwards from a third-party market estimate, precisely because no third-party market size could be verified to this series' standard. It is arithmetic on a company statement, not a market sizing.

**3.8 The eval plan, failure-mode ranking and human-in-the-loop rules (§29).** Author constructs. The pass bars — 95% routing agreement, 100% contraindication recall, pre-registered non-inferiority — are proposed standards, not observed performance, and the company has published no performance against which to compare them.

**3.9 Kano, HEART, AARRR and Porter classifications (§16, §33, §34, §49).** Analytical judgements applying standard frameworks to disclosed facts.

---

## Part 4 — What could not be established

Named explicitly rather than filled in.

1. **Any AI performance metric whatsoever.** No adoption rate, no accuracy, no deflection rate, no escalation rate, no inference cost, no model name, no vendor name, no fine-tune. The absence is the finding of §29 and is asserted as an absence, never as a low number.
2. **Any clinical outcome metric.** The company reports no measure of whether treatment works, for any condition.
3. **Membership programme adoption.** Launched at the end of March 2026; no subscriber, revenue or attach figure disclosed in the Q2 filings.
4. **Cohort retention.** The company states it expects to retain "a significant majority" of revenue from subscribers past two years. No curve, no rate and no cohort table is disclosed.
5. **Customer acquisition cost.** Marketing spend is disclosed; new subscriber additions by channel are not, so CAC cannot be computed and is not asserted anywhere in the README.
6. **The FTC complaint itself.** This case study relies on the company's characterisation of the complaint in its own 10-Q. The complaint as filed in N.D. Cal. was not read. This is a real limitation and is named in §64.
7. **Eucalyptus standalone financials.** Only percentage-of-consolidated contributions are disclosed. No Eucalyptus revenue, margin or subscriber figure is asserted.
8. **The split of technology and development between AI and everything else.** Not disclosed, which is why §29's cost figure is a bound.
9. **Any user-side evidence.** No interviews, no usability testing, no review-corpus analysis. §25, §26 and §27 are correspondingly thin, and §64 says so.
10. **Market share.** No verifiable DTC telehealth market share figure was found to this series' standard; none is asserted.

---

## Part 5 — Method, precision and what a future revision should do

**Sources.** Two SEC filings made on the same day by the same registrant carry the entire financial argument. Secondary sources are used only for product naming and dates — MedMatch, Labs, the Doximity comparison — and are graded 🟡 at the point of use.

**Precision policy.** All derived figures are computed to two decimal places with a tolerance of 0.005. Where an input is itself rounded or approximate — Adjusted EBITDA stated to $0.1 Mn, the FTC accrual stated as "approximately $60 million", the MRAS adjustments stated as "approximately $10" and "less than $5" — every ratio derived from it inherits that imprecision. Such ratios are presented to two decimals for consistency with the series, and this paragraph is the standing qualification on all of them.

**Bounds are never sharpened.** The 2025 one-time contribution to MRAS is disclosed as "less than $5". It is carried as an upper bound throughout, which is why §30 reports adjusted growth as a range of 7.89% to 15.49% rather than a single figure, and why `verify.py` asserts that the *maximum* adjusted growth rate is below the reported rate. Asserting a point estimate here would have produced a sharper headline and a false one.

**Rounding differences with the company are documented, not resolved silently.** The press release states 64% gross margin, 38% revenue growth and 19% subscriber growth. The computed figures are 63.83%, 38.25% and 18.53%. The README uses the computed figures and Appendix A records the difference.

**What a future revision should add.**

1. Read the FTC complaint as filed and replace the company's characterisation of it.
2. Add user-side evidence on the cancellation flow — the single change that would most improve §25 and lift the self-rating.
3. Re-examine after Q3 2026 results, when a full quarter of Eucalyptus will be in the base and the US organic growth line will be readable without the acquisition distortion.
4. Track whether the one-time contamination of MRAS rises above 10.87%, and whether the company restates or redefines the metric.
5. Track whether any AI metric appears in a subsequent filing. Day 82's Doximity is the comparator that shows it is possible.

---

*Day 80 of 90 · Verified with `verify.py` — 151 checks, all passing · Cross-checked with `crosscheck.py`*
