# ASSUMPTIONS — Day 38: Razorpay

Companion file to `README.md`. This document exists so that every load-bearing claim in the case study can be checked, challenged, or discarded by a reader who disagrees with it.

**Research date:** 3 August 2026
**Author:** Gaurav Singh

---

## 1. Evidence grading scale

| Grade | Meaning |
|---|---|
| **High** | Reported consistently by two or more independent credible outlets, or disclosed by the company directly |
| **Medium** | Reported by one credible outlet, or by several outlets that appear to share a single source |
| **Low** | Sourced only from statistics aggregators or SEO content farms; no methodology given |
| **Conflicting** | Credible sources disagree, and the conflict has not been resolved |
| **Constructed** | Created by the author for analytical purposes; not a factual claim |

---

## 2. Claim-by-claim evidence grades

### Financials

| Claim | Grade | Notes |
|---|---|---|
| FY25 revenue ₹3,783 cr, +65% YoY | **High** | Entrackr, Business Standard, YourStory converge |
| FY25 gross profit ₹1,277 cr, +41% YoY | **Medium** | Entrackr is the primary source; widely repeated but appears to trace to one report |
| FY25 loss ₹1,209 cr (post-ESOP) | **High** | Multiple outlets; attributed to reverse-flip tax and restructuring |
| FY25 loss is non-operating in origin | **High** | Consistently attributed across sources to redomiciling costs |
| Online payments business EBITDA-positive in FY25 | **Medium** | Reported; not independently verifiable |
| FY24 operating revenue ₹2,475 cr | **Conflicting** | See conflict C1 |
| FY24 PAT ₹33.5 cr; first profitable year | **Medium** | Inc42 |
| FY24 payment aggregation revenue ₹2,068 cr (83% of operating revenue) | **Medium** | Inc42 / BW Disrupt; the 83% ratio is load-bearing for §18 |
| FY25 segment revenue split | **Not disclosed** | Explicitly marked as such in §30 |
| UPI share of TPV | **Not disclosed** | The single most consequential gap in this analysis |
| Current MPAM / products-per-merchant | **Not disclosed** | |

### Derived figures (author calculation, not reported)

| Derived figure | Method | Grade |
|---|---|---|
| FY25 gross margin 33.8% | 1,277 ÷ 3,783 | **Constructed — arithmetic on High/Medium inputs** |
| FY24 gross profit ≈ ₹906 cr | 1,277 ÷ 1.41 | **Constructed** |
| FY24 gross margin 36.6% or 39.5% | 906 ÷ each of two FY24 revenue readings | **Constructed** |
| Gross margin compression of 2.8–5.7 pp | Difference of the above | **Constructed — but robust to the underlying conflict** |

**Note on the derived figures.** These are the analytical backbone of the case study. They are arithmetic, not estimates, but they inherit the uncertainty of their inputs — particularly the gross profit figure, which is Medium-graded. If Entrackr's gross profit number is wrong, the central thesis weakens substantially. It is the single point of failure in this analysis and is named as such in §64.

### Corporate and regulatory

| Claim | Grade | Notes |
|---|---|---|
| Founded 2014 by Harshil Mathur and Shashank Kumar | **High** | |
| Y Combinator W15 | **High** | |
| Series F Dec 2021, ~$375M at $7.5B valuation | **High** | Widely reported |
| Total raised ~$740M | **Medium** | Aggregator-derived; varies slightly by source |
| RBI onboarding embargo Dec 2022 – Dec 2023 | **High** | Business Standard, YourStory |
| Final PA authorisation received Dec 2023 | **High** | |
| ED searches Oct 2022; ~₹78 cr frozen | **High** | Multiple outlets |
| ED chargesheet naming Razorpay filed subsequently | **Medium** | Reported; case status as of research date not verified |
| Reverse flip completed May 2025 | **High** | |
| Reverse-flip tax cost | **Conflicting** | See conflict C2 |
| Confidential DRHP filed 12 June 2026 | **High** | Multiple outlets, consistent date |
| Bankers: Axis, Kotak, JPMorgan, Citi | **Medium** | Consistently reported, sourced to "media reports" |
| IPO target valuation $5–6B | **Conflicting** | See conflict C3 |
| PA-CB (cross-border) licence granted January 2026 | **Low** | Single aggregator source; **used cautiously in §39 and §56 and should be independently verified before being relied upon** |
| Singapore market entry March 2025 | **Medium** | |
| Curlec acquired 2022, ~$19M valuation | **Medium** | Business Standard |

### Volume and scale

| Claim | Grade | Notes |
|---|---|---|
| ~$180B annualised TPV | **Conflicting** | See conflict C4 |
| ~$400B TPV target by 2030 | **High** | Company-stated at 10-year milestone, Feb 2025 |
| 12 million+ merchants | **Low** | Aggregators only. Feeds the RICE reach input — see §47 sensitivity check |
| 94% merchant retention | **Low** | Single aggregator, no methodology. **Not used in any conclusion** |
| ~55% share of India payment gateway market | **Low / internally inconsistent** | See conflict C5. **Explicitly rejected and not used** |

### Product

| Claim | Grade |
|---|---|
| Product portfolio composition (PG, Magic Checkout, RazorpayX, Capital, Payroll, POS, Route, Smart Collect, Curlec) | **High** — company documentation |
| Magic Checkout reduces COD RTO via address/history scoring | **High** — company documentation |
| RazorpayX is the fastest-growing segment | **Medium** — reported, not quantified |
| "CFO assistant" AI positioning | **Medium** — reported; technical detail thin |
| UPI MDR is zero by government mandate since Jan 2020 | **High** |
| Parliamentary Standing Committee recommended MDR return (March 2026) | **Medium** |
| PCI urged 0.30% MDR on large-merchant UPI/RuPay | **Medium** |
| No binding RBI/CBDT notification on UPI MDR as of research date | **Medium** — absence of evidence; stated as such in §11 |

---

## 3. Source conflicts — full table with resolutions

### C1 — FY24 operating revenue

| Source | Figure |
|---|---|
| Inc42 and others | ₹2,475 cr operating revenue (₹2,501.4 cr total incl. other income) |
| Implied by FY25's reported +65% growth on ₹3,783 cr | ₹2,293 cr |
| BW Disrupt headline | ₹2,068 cr |

**Resolution: none. Both primary readings carried.** The ₹2,068 cr figure is separately identified in the same reporting as the *payment aggregation segment* revenue, not total operating revenue, so it is treated as a segment figure rather than a third conflicting total. The remaining ₹2,475 vs ₹2,293 conflict most plausibly reflects an entity-scope or consolidation-basis change around the May 2025 reverse flip, but this is a hypothesis, not a finding.

**Why the conflict did not need resolving.** The case study's conclusion — gross margin compressed — holds under both readings (39.5% → 33.8% or 36.6% → 33.8%). Both are shown in §65 Appendix A. Averaging them would have produced a single clean number that is not true under either reading.

### C2 — Reverse-flip tax cost

| Source | Figure |
|---|---|
| Entrackr, Inc42, IBS Intelligence, Compliance Calendar | ~$150M / ₹1,245–1,280 cr |
| The Head and Tale | "as high as $400 million" |

**Resolution: the ~$150M cluster is preferred and the $400M figure is retained as an outlier.** Four independent outlets converge on ~$150M, and that figure is consistent with the reported FY25 loss of ₹1,209 cr. A $400M (~₹3,400 cr) tax charge would be difficult to reconcile with a ₹1,209 cr total loss. The outlier is noted rather than deleted, because it may reflect a broader definition of total restructuring cost rather than tax alone.

### C3 — IPO valuation and raise size

| Source | Valuation | Raise |
|---|---|---|
| Business Today (April 2026) | ~$5B | $600–700M target |
| NiftyTrader | ₹50,000–60,000 cr ($5.7–6.8B) | ~₹6,000 cr |
| Various | — | ₹5,700 cr (₹2,700 cr fresh + OFS) |
| Groww blog | — | ~$600M |
| Shareholder approval (reported) | — | ~$316M fresh |
| valueforstartups.in | **$9.2B, "Series G $490M"** | — |

**Resolution: a range of $5–6B is used, and the $9.2B claim is rejected.** The $9.2B / "Series G $490M" claim appears only on a low-quality aggregator, is inconsistent with every credible outlet, and is inconsistent with the well-documented $7.5B December 2021 round being described as a markdown. No credible reporting of a Series G was found. **This claim is treated as unreliable and is not used anywhere in the case study.**

The raise-size figures are genuinely unsettled and are reported as a range. The distinction between fresh issue (~$316M / ₹2,700 cr) and total including OFS (~$600–700M) explains much of the apparent spread.

### C4 — Total Payment Volume

| Source | Figure | Attributed to |
|---|---|---|
| Inc42 / FY24 reporting | ~$180B annualised | FY24 |
| coinlaw.io / digitalinasia | ~$180B annualised | 2026 |

**Resolution: none — flagged as probably stale.** The identical figure being attributed to two years two years apart, with no intervening growth, strongly suggests one source is recycling the other without checking the date. Given Razorpay's stated $400B target for 2030 and its FY25 revenue growth of 65%, a flat TPV across FY24–FY26 is implausible.

**Consequence:** TPV is not used as a quantitative input to any conclusion in the case study. It appears only as context and is explicitly graded Conflicting in §30. The $400B 2030 target, which is company-stated and dated, is used instead where a volume reference is needed.

### C5 — Market size and market share

| Source | Claim |
|---|---|
| Mordor Intelligence | India payment gateway market ~$2.07B (2025), ~$4.01B by 2031, 11.66% CAGR |
| coinlaw.io | Razorpay holds ~55% of India's online payment gateway market |
| Razorpay FY25 revenue | ₹3,783 cr ≈ $430–450M |

**Resolution: the share figure is rejected as internally inconsistent with the market-size figure.** If the market were $2.07B and Razorpay held 55%, Razorpay's gateway revenue would be ~$1.14B — roughly 2.5× its entire reported company revenue including all non-gateway products. The two claims cannot both be true.

The most likely explanation is definitional: Mordor appears to size gateway *software/service* revenue, while Razorpay's reported revenue line includes gross processing flows and non-gateway products. Since neither definition can be confirmed, **no market-share percentage is used anywhere in this case study.** §11 states this explicitly and §13 sizes TAM/SAM/SOM in two units instead, which sidesteps the problem.

---

## 4. Everything author-constructed

Nothing in this section is a factual claim about Razorpay. All of it was created for analysis.

### Constructed analytical instruments

| Item | Where | Nature |
|---|---|---|
| **The central thesis** — that Razorpay is an adjacent-products company obliged to run a loss-leading payments business | §5 | Author's interpretation. Built on real disclosed numbers, but it is a reading, not a fact |
| **Personas** — Ananya, Rohit, Meera | §20 | Fully constructed composites. No merchant interviews were conducted. Their specific revenue figures, UPI mix percentages and frustrations are illustrative |
| **User journey scores** | §22 | Author-assigned. No satisfaction data exists |
| **User flow Nodes J and L** | §23 | Author's model of where expansion fails. Not observed in telemetry |
| **UX / UI / Accessibility audits** | §25, §26, §27 | Author assessment from public product surfaces. No formal audit, no WCAG testing, no usability sessions |
| **Pain points P1–P8 and severity ratings** | §45 | Inferred from product structure and IA, not from support data or research |
| **Opportunity scoring O1–O6** | §46 | Author judgement |
| **All RICE inputs** — reach, impact, confidence, effort | §47 | **Entirely invented.** Razorpay's actual figures are not public. The ordering is defensible; the numbers are not accurate. The sensitivity table exists to make this explicit |
| **Kano categorisations** | §49 | Author judgement, no survey |
| **MPAM as North Star Metric** | §31 | Author's proposal. Razorpay has not stated a North Star Metric publicly |
| **The entire feature proposal — Cashboard** | §50, §51, §52 | **Wholly author-constructed.** Razorpay has not announced anything resembling this. The wireframes, requirements, and all numbers within them are illustrative |
| **All success criteria and targets** | §51 | Invented. No baselines are disclosed, so no target can be calibrated |
| **Rollout dates and durations** | §53 | Illustrative sequencing only |
| **A/B test arms, effect sizes and the 40% decision rule** | §54 | Constructed. The 40% threshold is a judgement about what would justify the cost differential, not a statistically derived figure |
| **KPI dashboard composition** | §55 | Author's proposal |
| **Roadmap** | §56 | Author's proposal |
| **Risk likelihood and impact ratings** | §57 | Author judgement |
| **Future scenarios A and B** | §58 | Speculative by construction |
| **Technical architecture and data flow diagrams** | §41, §42 | **Reconstructions** from public API documentation and standard industry patterns. Not descriptions of Razorpay's actual systems. Treat as a plausible model, not as fact |
| **Take-rate table** | §18 | Approximate, based on published merchant-facing pricing ranges; realised margins are inferred |

### Constructed but grounded

The following are author constructions that rest directly on disclosed data rather than on judgement, and should be treated as more reliable than the rest of this section:

- The gross margin calculation and the compression finding (§65 Appendix A) — arithmetic on reported figures
- The observation that revenue grew 65% while gross profit grew 41% — this is simply reading two reported numbers together
- The argument that TPV is a hazardous North Star for a zero-MDR business (§31) — logical, not empirical

---

## 5. What would materially improve this analysis

Ranked by expected improvement per unit of effort.

| # | What | Why it matters |
|---|---|---|
| 1 | **Ten interviews with payment-only Razorpay merchants**, asking what they did the last time they needed working capital | Would validate or destroy §50's entire premise in a single afternoon. The cheapest high-value research available |
| 2 | **UPI share of TPV, FY24 vs FY25** | The single number that would confirm or refute the central thesis directly |
| 3 | **FY25 segment revenue split** | Would settle Reading A vs Reading B in §18 — currently the weakest inference in the document |
| 4 | **The public DRHP, once filed** | Would replace most of this document's inferences with audited fact, including the FY24 conflict (C1) |
| 5 | **Current products-per-merchant** | Would convert §31 from a proposal into a measurable claim |
| 6 | **Support ticket taxonomy or merchant NPS verbatims** | Would ground §45's pain points in evidence rather than inference |
| 7 | **Independent confirmation of the PA-CB licence** | Currently Low-graded and feeding into §39 and §56 |
| 8 | **A formal accessibility audit of Razorpay Checkout** | §27 is the thinnest section in the document and covers a genuinely large surface |
| 9 | **Competitor gross margin comparison (PayU, Cashfree)** | Would establish whether margin compression is Razorpay-specific or industry-wide — a materially different conclusion |

**Item 9 deserves emphasis.** This case study argues that margin compression is structural to Indian payments. If PayU or Cashfree show *stable* gross margins over the same period, that argument is wrong and the compression is a Razorpay execution issue instead. That comparison was not performed, and its absence is the most significant unaddressed threat to the thesis.

---

## 6. Methodology note

**Research date:** 3 August 2026. All figures are as reported at that date.

**Method.** Desk research only. Sources were gathered via web search across financial press (Business Standard, Business Today), Indian startup media (Entrackr, Inc42, YourStory), company documentation (razorpay.com, Razorpay Docs), market research aggregators (Mordor Intelligence), and general-purpose statistics aggregators.

**Cross-checking rule applied.** Every financial and usage figure was checked against at least two sources where two existed. Where sources conflicted, both were retained and the conflict documented in section 3 above. **No conflicting figures were averaged.** Where a conflict could not be resolved, the figure was either excluded from conclusions (C4, C5) or the conclusion was constructed so as to hold under both readings (C1).

**Source credibility handling.** Four sources encountered during research — coinlaw.io, valueforstartups.in, bayelsawatch.com, digitalinasia.com — display characteristics of automated statistics-aggregation content: unattributed figures, no methodology, and in at least one case (the $9.2B valuation, C3) claims contradicted by all credible reporting. These were used only to identify claims worth verifying elsewhere, never as sole evidence for anything used in a conclusion.

**What was not done.** No primary research. No merchant interviews. No usability testing. No accessibility audit. No access to Razorpay's DRHP, which is confidentially filed and therefore not public. No independent verification of any financial figure — all financials are as reported by third parties and are unaudited from this document's perspective.

**Standing correction policy.** Where a figure could not be verified, it is marked "not disclosed" rather than estimated. Where a number appeared plausible but unsourced, it was excluded. Corrections to any claim in this document are welcome and will be reflected here.

---

*Companion to `README.md` · Day 38 of 90 · Gaurav Singh · 3 August 2026*
