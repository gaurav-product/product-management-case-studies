# ASSUMPTIONS — Day 42: Groww

Companion file to `README.md`. This document records what is evidenced, what is inferred, what is constructed, and where sources disagree. It exists because the most common failure in public product analysis is presenting inference with the confidence of fact.

**Research cut-off:** 7 August 2026. All figures are as reported by third-party sources on or before that date. Nothing here has been verified against primary company filings.

---

## 1. The structural evidence limitation

Groww listed in November 2025. That is roughly nine months of public-company disclosure at the time of writing. Three consequences shape everything below:

1. **No long time series.** Pre-IPO financials are visible only through DRHP-era reporting and secondary summaries. Trend claims spanning FY24–FY26 rest on secondary sources rather than a continuous audited series.

2. **Segment reporting is coarse.** Groww discloses revenue by stream (derivatives, MTF, float, treasury, credit) but not by user segment. The central claim of this case study — that acquisition and revenue are near-disjoint populations — is assembled from two separately disclosed facts (F&O penetration ~10% of users; equity derivatives ~55% of revenue) rather than from a disclosed segment P&L. The inference is sound but it is an inference.

3. **The most decision-relevant metrics are simply not published.** ARPU by segment, CAC by entry product, cohort retention beyond 12 months, direct-vs-regular plan split, and the overlap between SIP investors and MTF borrowers are all absent. Section 5 below lists what their disclosure would change.

A fourth limitation is specific to this analysis: **I could not access Groww's own investor presentations or annual report directly.** All financial figures are mediated through news coverage, brokerage notes and financial data aggregators. Where those intermediaries disagree, I have retained the disagreement rather than picking a winner.

---

## 2. Evidence grades

**Grading scale**

| Grade | Meaning |
|---|---|
| **High** | Reported consistently across two or more independent credible sources |
| **Medium** | Reported by a single credible source, or consistent but from related sources |
| **Low** | Inferred by the author from product behaviour, structure or general practice |
| **Conflicting** | Sources materially disagree; both retained (see §3) |

### Claim-by-claim

**Financial and market position**

| Claim | Grade | Note |
|---|---|---|
| Q1 FY27 PAT ₹735.04 crore, +94.3% YoY | **High** | Multiple outlets agree |
| Q1 FY27 revenue from operations ₹1,501.42 crore, +66% YoY | **High** | Multiple outlets |
| Q1 FY27 total income ₹1,549 crore, +63% YoY | **High** | Different line item — resolves an apparent conflict, see §3.1 |
| NSE active clients ~1.30 crore, ~28.72% share (June 2026) | **High** | Consistent across broking-data trackers |
| Industry NSE active clients ~4.42 crore (June 2026) | **Medium** | Single primary trace |
| Net client adds ~115,000 in Q1 FY27 during industry decline | **High** | Multiple outlets |
| Angel One lost ~50,390 and Zerodha ~45,971 active clients in June 2026 | **Medium** | Single aggregator source |
| Top-3 concentration ~58% | **Medium** | Consistent with the Day-22-Zerodha entry in this repo |
| Customer assets ~₹3.58–3.6 lakh crore (~15 July 2026) | **High** | Two sources, marginally different figures and dates |
| Direct MF AUM ~₹1.9 lakh crore | **Medium** | Single source (Q1 FY27 coverage) |
| MF ~53% of customer assets | **Medium** | Single source |
| ~40% of industry direct-plan SIP inflows | **Medium** | DRHP-era reporting; date of measurement unclear — see §3.5 |
| Market cap ~₹1.20 lakh crore, share ~₹192, P/E ~63.95 (6 Aug 2026) | **High** | Multiple aggregators |
| IPO ~₹6,632.30 crore, band ₹95–₹100, ~17.58x subscribed, listed +29% | **High** | Multiple sources |
| FY25 revenue ~₹4,056 crore, PAT ~₹1,818 crore | **Medium** | Secondary reporting |
| FY26 revenue ~₹5,242 crore, PAT ~₹2,440 crore | **Conflicting** | See §3.2 |

**Business mix and product**

| Claim | Grade | Note |
|---|---|---|
| F&O penetration fell to ~10% (Q4 FY26) from ~18% (Nov 2024) | **High** | Reported explicitly, twice |
| Equity derivatives ~55% of Q4 FY26 revenue, 57% year-ago | **High** | Consistent |
| FY26 mix: float ~8.1%, MTF ~8.0%, PL+LAS ~5.5%, commodities ~4.9%, treasury ~3%, other ~2.1% | **Medium** | Single detailed breakdown; components do not sum to 100% and the residual is unexplained — see §3.4 |
| MTF book ₹2,814.3 crore Q4 FY26, ~4.5x from ₹602 crore | **High** | Consistent |
| MTF advertised at 14.95% and up to 4x buying power | **High** | Groww's own product page |
| Commodity derivatives ~29% market share within ~1 year | **Medium** | Reported; the share denominator is not specified |
| GrowwMF AUM ₹5,491 crore Q1 FY27, from ₹4,170 crore | **Medium** | Single source |
| GrowwMF loss of ₹21.4 crore in Q4 FY26 | **Medium** | Single source |
| SIP inflows ₹13,023 crore Q4 FY26, +35% YoY | **High** | Consistent |
| SIP market share ~14.0%, up from ~12.3% | **Medium** | Single source |
| New SIPs "grew 61.5% YoY to 56.21 million" | **Conflicting** | Unit ambiguity — see §3.3 |
| Acquisition funnel shifting to MF/ETF over stocks | **Medium** | Management commentary via a single outlet |
| Management targeting derivatives below half of revenue | **Medium** | Single source |

**Credit and NBFC**

| Claim | Grade | Note |
|---|---|---|
| Groww Creditserv incorporated Jan 2021, RBI licence Dec 2022 | **High** | ICRA rating rationale |
| Products: personal loans, LAS, LAMF; consumer durables discontinued FY2025 | **High** | ICRA |
| NBFC gross NPA 0.29% (FY24) → 1.68% (FY25) | **Medium** | Reported in IPO analysis coverage |
| Proprietary loan book ₹965 crore as of June 2024 | **Medium** | Single source; substantially out of date by the cut-off |
| Fresh IPO proceeds partly directed to Creditserv | **Medium** | Reported IPO objects |

**Regulation**

| Claim | Grade | Note |
|---|---|---|
| SEBI True to Label circular and derivatives framework effective 1 Oct 2024 | **High** | Widely reported |
| Budget 2026: futures STT 0.02% → 0.05%; options 0.10% → 0.15% | **High** | Multiple outlets |
| Brokerage stocks fell up to ~13.5% on the STT announcement | **Medium** | Single source; "up to 15%" appears in a headline vs "up to 13.5%" in body — minor, not treated as material |

**Company background**

| Claim | Grade | Note |
|---|---|---|
| Founded 2016 by Keshre, Jain, Singh, Bansal (ex-Flipkart); operations 2017 | **High** | Multiple sources |
| Indiabulls AMC acquired 2021 for ~₹175 crore | **High** | Multiple sources |
| Equity trading launched 2020 | **Medium** | Secondary profiles |
| Groww overtook Zerodha on active NSE clients in Sept 2023 | **High** | Corroborated by the Day-22-Zerodha entry in this repo |
| 40 million+ registered users | **Medium** | Reported; definition of "registered" unclear |

**Reliability and trust**

| Claim | Grade | Note |
|---|---|---|
| January 2024 outage: login, balance and order failures | **High** | Multiple outlets |
| LAMA reporting failure with no client backup during the glitch | **Medium** | Single detailed source |
| ~₹82.98 lakh paid to settle two SEBI cases in early 2025 | **Medium** | Single source |
| Groww Invest paid ₹34+ lakh to settle a glitch-linked SEBI case | **Medium** | Business Standard |
| Complaints re: wallet balances, refunds, disappearing complaint history | **Low-Medium** | User-review aggregators and complaint forums — self-selected, unverifiable individually, but thematically consistent |

**Everything in README §41 (Technical Architecture), §42 (Data Flow), §43 (API Ecosystem) and §27 (Accessibility) is graded Low.** These are reasoned inferences from observable behaviour, regulatory requirements and documented failure modes. Groww publishes no architecture documentation and no accessibility audit. The README labels these sections as inferred; this file restates it because it is the single largest body of Low-grade content in the document.

---

## 3. Source conflicts (full detail)

Every conflict below is retained in both forms in the README. None has been averaged.

### 3.1 Q1 FY27 growth: 63% vs 66%

- **Source A:** revenue from operations ₹1,501.42 crore, **+66%** YoY (from ₹904.40 crore)
- **Source B:** total income ₹1,549 crore, **+63%** YoY

**Resolution: not a genuine conflict.** These are two different line items — revenue from operations excludes other income; total income includes it. Both are correct and they are internally consistent (₹1,549 − ₹1,501.42 = ~₹47.6 crore of other income). The README reports both explicitly in §30 and §65 so that a reader encountering either figure elsewhere can reconcile them. This is documented rather than silently dropped because the two numbers appear in headlines interchangeably.

### 3.2 FY26 growth rate: ~29% vs 19%

- **Source A:** FY25 revenue ~₹4,056 crore and FY26 revenue ~₹5,242 crore, implying **~29.2%** growth
- **Source B:** FY 2025-26 achieved **19%** revenue growth, 16% EBITDA growth, 14% PAT growth

**Resolution: unresolved, both retained.** The two cannot both be true of the same entity and period. Possible explanations, none verifiable from available sources:

- Source B may describe a different entity within the group (e.g. the broking subsidiary rather than consolidated BGV)
- Source B may be standalone rather than consolidated
- Source A's FY26 figure may be a trailing-twelve-month aggregator computation rather than an audited FY26 result
- One may simply be wrong

The README flags this in §13 and §65 rather than choosing. **Impact on the analysis: low.** No argument in this case study depends on the precise FY26 growth rate; the thesis rests on revenue *composition*, which is separately sourced. Had a conclusion depended on it, the conflict would be disqualifying.

### 3.3 New SIPs: the 56.21 million unit problem

- **Reported:** new SIPs created on the Groww platform grew 61.5% YoY to **56.21 million** in Q4 FY26
- **Same period:** SIP inflows of **₹13,023 crore**

**The arithmetic does not work as a quarterly new-SIP count.** 56.21 million new SIPs against ₹13,023 crore of *total* quarterly SIP inflow implies roughly ₹2,316 per new SIP per quarter — and that assumes all inflow came from new SIPs, ignoring the far larger existing book. The realistic implied per-SIP amount is lower still.

**Candidate readings, all retained:**

1. A cumulative count of all SIPs registered on the platform, not new ones in the quarter
2. An annualised or trailing figure mislabelled as quarterly
3. A different unit (e.g. 56.21 lakh ≈ 5.62 million, which reconciles far better)
4. Counting SIP *instalments* processed rather than SIP *mandates* created

**Resolution: none.** The README (§30) reports the growth rate (+61.5% YoY), which is likely robust to the unit question, and explicitly flags the absolute figure as ambiguous rather than using it. No argument depends on the absolute number.

### 3.4 FY26 revenue mix components do not sum to 100%

The disclosed components — equity derivatives ~55% (Q4 FY26), float ~8.1%, MTF ~8.0%, PL+LAS ~5.5%, commodities ~4.9%, treasury ~3.0%, other ~2.1% — total ~86.6%, leaving ~13.4% unattributed.

**Most likely explanation:** cash equity delivery brokerage and miscellaneous transaction charges are not separately broken out, and the ~55% derivatives figure is a Q4 FY26 datapoint while the remaining percentages are described as FY26 — mixing a quarter with a year.

**Resolution:** the README treats the residual as cash delivery brokerage and labels it "Residual" rather than assigning a number (§18, §65 Appendix B), and notes the period mismatch. **This is a real weakness.** The behaviour-based vs balance-based split in §18 — roughly 60%+ vs ~25% — is therefore approximate. The *direction* is robust (behaviour-based clearly dominates; balance-based is clearly the growing minority) but the precise percentages should not be quoted.

### 3.5 The ~40% direct-plan SIP inflow share

Reported as "Groww accounted for 40% of direct plan SIP inflows in mutual fund industry," sourced to DRHP-era reporting (September 2025 coverage).

**Concerns:** the measurement period is not stated; DRHP figures typically describe a period ending several months before publication; and the metric is *direct-plan* SIP inflows specifically, a subset of total industry SIP inflows, which makes the share much higher than Groww's ~14% overall SIP market share and is not contradictory.

**Resolution:** retained with the qualifier "DRHP-era disclosure" and the date ambiguity noted. This figure carries real weight in the README's argument (§11, §65), so its Medium grade is a genuine limitation. The argument would survive a figure of 30% or 25%; it would weaken materially below ~20%.

### 3.6 Active user definitions

Four different populations appear across sources: registered users (40M+), transacting users (2.2 crore), Groww-defined active users (1.7 crore), and NSE active clients (1.30 crore).

**Resolution: not a conflict, a definitional hazard.** All four are plausibly correct measures of different things. The README addresses this explicitly in §11 and uses NSE active clients for all competitive comparison and Groww's own figures only for internal ratios, labelling which is which. The risk of accidentally mixing them — for example computing ARPU on the wrong denominator — is high enough to warrant the explicit treatment.

### 3.7 Zerodha comparison data is thin

Zerodha is private and does not publish comparable results. Available data points — Zerodha Capital's FY26 total income of ~₹53.5 crore and PAT of ~₹14.7 crore, and Kamath's statement that broking revenue fell ~40% YoY in Q1 FY26 — describe the *lending arm* and a *single quarter* respectively, not the consolidated business.

**Impact:** README §14 and §38 use Zerodha as a strategic control case ("same shock, opposite response"). That comparison is qualitatively defensible but **quantitatively under-supported**. §64 acknowledges this as an asymmetry in the competitor treatment. A reader should treat the Zerodha contrast as an argument, not a measurement.

---

## 4. Author-constructed content

Everything in this section is mine. None of it is a Groww disclosure, and none of it should be cited as a fact about the company.

### 4.1 The central thesis

The framing that Groww's acquisition and revenue engines are "two nearly disjoint populations," and that its diversification substitutes correlated credit/cycle risk for regulatory risk, is **my interpretation**. It is assembled from disclosed facts but Groww has never characterised its business this way and would likely dispute the framing. The underlying facts (F&O ~10% of users / ~55% of revenue; MF ~53% of assets at ~0 bps) are reported; the conclusion drawn from them is not.

### 4.2 The behaviour / balance / manufacturing revenue taxonomy (§18)

My classification scheme. Groww reports revenue by product line, not by this framework. The taxonomy does real analytical work in the README and is, I think, its most useful original contribution — but it is an analytical lens imposed on the data, not a reporting standard.

### 4.3 Personas (§20)

Priya, Rohit, Anjali and Suresh are **composites**, built from disclosed segment behaviour, product surfaces and publicly reported complaint themes. No user research, interviews or surveys were conducted. Their specific details — Priya's ₹15,000 across three SIPs with 61% overlap, Rohit's expiry-day concentration, Anjali's MTF usage — are illustrative constructions chosen to make segment economics concrete.

**Priya carries disproportionate argumentative weight.** The entire feature proposal targets her, and the willingness-to-pay assumption rests on her. If real passive Groww users differ materially from this construct — for instance if they rebalance through channels invisible to this analysis, or hold single diversified funds rather than overlapping ones — the proposal's premise weakens substantially.

### 4.4 Segment size estimates (§19)

The user-share and revenue-share columns in §19 are **derived from disclosed ratios, not reported**. Only two anchors are real: F&O penetration ~10% and equity derivatives ~55% of revenue. Everything else in that table — the relative sizing of passive accumulators, dormant registrants, cash equity investors, leveraged investors and credit customers — is directional reasoning. The table is labelled as such in the README.

### 4.5 Journey, flow and IA analysis (§22, §23, §24)

Based on observable product structure and general behaviour of platforms of this type. The specific claim that Groww has **no allocation flow at all** is an inference from the absence of any publicly documented such feature; it is possible a limited feature exists that I did not surface. The Conway's Law reading of the IA (navigation mapping onto regulatory entities) is my interpretation.

### 4.6 Heuristic and audit scores (§25, §26, §27)

All scores are **author-assigned judgements**, not usability testing results:

- UX composite 3.2/5
- UI composite 3.5/5
- Accessibility: entirely hypothesis; no assistive technology testing, no WCAG audit, no verification of language coverage or text scaling

The observation that low scores cluster on unhappy paths and high scores on happy paths is a real pattern in my own scoring, which means it is at some risk of being an artifact of how I scored rather than a property of the product.

### 4.7 North Star metric — Fee-Bearing Customer Assets (§31)

**Entirely author-proposed.** Groww does not report FBCA and there is no indication it thinks in these terms. The current value of ~1.5% is my calculation: GrowwMF AUM (₹5,491 crore) as a share of customer assets (~₹3.58 lakh crore). That calculation makes a significant simplifying assumption — that GrowwMF AUM is the only fee-bearing asset — which is likely wrong at the margin. Treat 1.5% as an order of magnitude, not a figure.

### 4.8 The entire feature proposal (§46–§56)

**Groww Portfolios does not exist.** Every element is constructed:

- The concept, positioning and the free-diagnostics-as-wedge structure
- The pricing (₹99–₹249 flat, explicitly not percentage-of-AUM) — no pricing research supports these numbers
- The no-proprietary-preference constraint as a Must-have
- All RICE inputs (reach, impact, confidence, effort) and therefore all RICE scores and the sensitivity table
- The MoSCoW allocation and the Kano categorisations
- All PRD requirements, success criteria and target numbers (25% adoption, 2–4% conversion, >70% retention)
- All four wireframes, including the illustrative figures shown in them (61% overlap, 412 stocks, 38% top-10 concentration, the ₹25 lakh goal)
- The entire rollout plan, all phase durations and the go/no-go structure
- All three A/B experiment designs and the 1.5% kill criterion
- The full KPI dashboard and every threshold in it
- The roadmap and all its timings

**The RICE effort estimates are the weakest single element.** 40 person-months for the paid tier and 12 for diagnostics are professional guesses with no engineering input. Since the sensitivity analysis turns partly on effort, and the sequencing recommendation turns on the sensitivity analysis, this weakness propagates into a headline conclusion. The confidence estimate (40%) is likewise a judgement, though the README's treatment of it — testing 20% to 70% — is designed to make the conclusion robust to being wrong about the specific number.

### 4.9 Strategic paths and scenarios (§38, §58)

Paths A/B/C and Scenarios 1/2/3 are analytical constructs. The probability language attached to the scenarios ("highest on current trajectory," "moderate") is qualitative judgement, not modelling. The recommendation of Path C is my argued position; §38 states the counterargument and §64 records that the willingness-to-pay assumption underpinning it is unevidenced.

### 4.10 Technical architecture and data flows (§41, §42)

The reference architecture, both sequence diagrams and the read-path isolation conclusion are **inferred**. The specific claim that the read path and write path appear to share a failure domain is reasoned from the outage description (users could not view balances *and* could not trade) plus general architectural principles. It is plausible; it is not documented. I may be wrong about the mechanism while still being right that the symptom is a product problem.

### 4.11 Risk ratings (§57)

All likelihood and impact ratings are author-assigned. R7 (breach of the no-proprietary-preference constraint) is rated High likelihood on the basis of general organisational dynamics under P&L pressure, not on any evidence about Groww's internal culture. That should be read as a structural prediction about incentives, not a claim about this company's people.

---

## 5. What would materially improve this analysis

In rough order of value:

1. **Groww's own investor presentations, earnings call transcripts and annual report.** All financial content here is mediated through secondary sources. Direct access would resolve §3.2 and §3.4 immediately and would likely resolve §3.3.

2. **ARPU and CAC by entry product and segment.** This is the single highest-value missing dataset. It would directly test the "disjoint populations" thesis: if passive users reliably convert to monetizing behaviour within a predictable window at acceptable cost, the thesis is substantially weakened and the current strategy is better than this document credits.

3. **Cohort retention and migration curves beyond 12 months.** Would establish whether Priya-type users migrate, stall or churn — the empirical question underneath §33 and §50.

4. **Direct vs regular plan split of MF AUM.** The ~0 bps monetization claim assumes the ₹1.9 lakh crore is overwhelmingly direct. If a meaningful regular-plan book exists, the monetization gap is smaller than argued.

5. **Overlap between SIP investors and MTF/credit borrowers.** Would quantify the self-arbitrage problem in §32 and §40 and test whether O9 addresses a real population or a hypothetical one.

6. **Any willingness-to-pay research on Indian retail investors and fee-based advice.** The proposal's central assumption. Even adjacent evidence — RIA adoption rates, PMS minimums, subscription uptake on competing platforms — would move the confidence estimate off a guess.

7. **Reliability telemetry:** order success rate, p99 latency, outage frequency and duration, and read-path availability separately from order-path availability. Would confirm or refute §41.

8. **A usability study with actual passive investors.** Would replace the entirely author-assigned scores in §25–§27 and would test whether the "popularity in the recommendation slot" claim in §23 reflects how users actually read that surface.

9. **GrowwMF AUM sourced on-platform vs externally.** Determines whether the AMC is genuinely capturing custodied assets or growing through other channels — material to the §38 Path B assessment.

10. **Zerodha consolidated financials.** Would convert the §14/§38 strategic comparison from an argument into a measurement.

---

## 6. Methodology note

**Research date:** 7 August 2026. **Research method:** web search across company product pages, Indian business and technology press (Business Standard, Business Today, Inc42, Entrackr, Medianama, TechCrunch, Tradebrains), financial data aggregators (Screener, Trendlyne, Tickertape, Stockanalysis), rating agency documentation (ICRA), IPO information platforms, and user review and complaint aggregators.

**Cross-checking rule applied:** every financial and usage figure was sought in at least two independent sources. Where two sources agreed, the claim is graded High. Where only one credible source existed, it is graded Medium and the singularity is noted. Where sources disagreed, both were retained and documented in §3 — **no conflict has been resolved by averaging, and none has been silently dropped.**

**Undisclosed baselines** are marked "not disclosed" throughout the README rather than estimated. Where a number was needed for analysis and none existed, it is labelled author-constructed or author-derived at the point of use as well as in §4 here.

**Repo-internal corroboration:** two claims (Groww overtaking Zerodha in September 2023; top-3 market concentration ~58%) are corroborated by the Day-22-Zerodha entry in this repository, which was researched independently at an earlier date. This is noted for transparency; it is not fully independent verification, since both entries may share upstream sources.

**Sequencing:** all research was completed before any part of the case study was drafted. The central thesis in README §5 emerged from the research — specifically from placing the "~10% F&O penetration" and "~55% of revenue from derivatives" figures side by side — and was not a prior hypothesis that the research was assembled to support. The feature proposal in §50 was written last, after the analytical sections, and §50 names the eight sections it derives from.

**Known bias to declare:** having identified the disjoint-populations framing early, I read subsequent evidence through it. §64 of the README lists what would change my conclusions, and §3.7 flags that the Zerodha comparison received less scrutiny than it deserved because it supported the thesis. Readers should weight those admissions accordingly.

---

*Companion to `README.md` · Day 42 of 90 · 90-Day PM Case Study Challenge · Gaurav Singh*
