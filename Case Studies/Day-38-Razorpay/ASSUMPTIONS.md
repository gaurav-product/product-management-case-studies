# ASSUMPTIONS — Day 38: Razorpay

Companion to `README.md`. This file exists so every load-bearing claim in the teardown can be checked, challenged, or discarded by a reader who disagrees with it.

**Research date:** 3 August 2026
**Author:** Gaurav Singh

---

## 1. Evidence grading scale

| Grade | Meaning |
|---|---|
| **High** | Reported consistently by two or more independent credible outlets, or disclosed by the company |
| **Medium** | One credible outlet, or several outlets that appear to share a single source |
| **Low** | Statistics aggregators or SEO content farms only; no methodology given |
| **Conflicting** | Credible sources disagree and the conflict is unresolved |
| **Constructed** | Created by the author for analytical purposes; not a factual claim |

---

## 2. Evidence grades by claim

### Financials

| Claim | Grade | Notes |
|---|---|---|
| FY25 revenue ₹3,783 cr, +65% YoY | **High** | Entrackr, Business Standard, YourStory converge |
| FY25 gross profit ₹1,277 cr, +41% YoY | **Medium** | Traces to a single Entrackr report despite wide repetition |
| FY25 loss ₹1,209 cr | **High** | Multiple outlets |
| FY25 loss is non-operating in origin | **High** | Consistently attributed to redomiciling costs |
| Online payments business EBITDA-positive in FY25 | **Medium** | Reported, not independently verifiable |
| FY24 operating revenue ₹2,475 cr | **Conflicting** | Conflict C1 |
| FY24 PAT ₹33.5 cr; first profitable year | **Medium** | Inc42 |
| FY24 payment aggregation revenue ₹2,068 cr = 83% of operating revenue | **Medium** | Load-bearing for §12 |
| FY25 segment revenue split | **Not disclosed** | Marked as such in §19 |
| UPI share of TPV | **Not disclosed** | The most consequential gap in this teardown |
| Current MPAM / products per merchant | **Not disclosed** | |

**The single point of failure.** The gross profit figure is Medium-graded and the entire central thesis rests on it. If Entrackr's ₹1,277 crore is wrong, the margin-compression finding weakens substantially. This is named in §19 and is the first thing a reader should attack.

### Derived figures (author arithmetic, not reported)

| Figure | Method | Grade |
|---|---|---|
| FY25 gross margin 33.8% | 1,277 ÷ 3,783 | Constructed — arithmetic on High/Medium inputs |
| FY24 gross profit ≈ ₹906 cr | 1,277 ÷ 1.41 | Constructed |
| FY24 gross margin 36.6% or 39.5% | 906 ÷ each FY24 revenue reading | Constructed |
| Compression of 2.8–5.7 pp | Difference of the above | Constructed — robust to conflict C1 |

**Full arithmetic**

- FY25 gross margin = 1,277 ÷ 3,783 = **33.8%**
- FY24 gross profit = 1,277 ÷ 1.41 = **₹906 cr**
- FY24 revenue, Reading 1 (derived from the 65% growth rate) = 3,783 ÷ 1.65 = ₹2,293 cr → margin = 906 ÷ 2,293 = **39.5%**
- FY24 revenue, Reading 2 (reported by Inc42) = ₹2,475 cr → margin = 906 ÷ 2,475 = **36.6%**

Compression is 5.7 points under Reading 1 and 2.8 points under Reading 2. **Directionally identical under both**, which is why conflict C1 was carried rather than resolved.

### Corporate and regulatory

| Claim | Grade | Notes |
|---|---|---|
| Founded 2014 by Harshil Mathur and Shashank Kumar | High | |
| Y Combinator W15 | High | |
| Series F Dec 2021, ~$375M at $7.5B | High | |
| Total raised ~$740M | Medium | Aggregator-derived, varies by source |
| RBI onboarding embargo Dec 2022 – Dec 2023 | High | Business Standard, YourStory |
| Final PA authorisation Dec 2023 | High | |
| ED searches Oct 2022; ~₹78 cr frozen | High | Multiple outlets |
| ED chargesheet naming Razorpay filed subsequently | Medium | Case status as of research date not verified |
| Reverse flip completed May 2025 | High | |
| Reverse-flip tax cost | **Conflicting** | Conflict C2 |
| Confidential DRHP filed 12 June 2026 | High | Consistent date across outlets |
| IPO target valuation $5–6B | **Conflicting** | Conflict C3 |
| Singapore entry March 2025 | Medium | |
| Curlec acquired 2022, ~$19M valuation | Medium | Business Standard |
| PA Cross-Border licence, January 2026 | **Low** | Single aggregator source. **Deliberately omitted from §10 and §20** rather than relied upon; mentioned only as an opportunity category |

### Volume and scale

| Claim | Grade | Notes |
|---|---|---|
| ~$180B annualised TPV | **Conflicting** | Conflict C4 — not used in any conclusion |
| ~$400B TPV target by 2030 | High | Company-stated, Feb 2025, dated |
| 12 million+ merchants | **Low** | Aggregators only. Feeds the RICE reach input — see §22 sensitivity check |
| 94% merchant retention | **Low** | Single aggregator, no methodology. **Not used** |
| ~55% share of India payment gateway market | **Low / internally inconsistent** | Conflict C5. **Explicitly rejected** |

### Product and market

| Claim | Grade |
|---|---|
| Product portfolio composition | High — company documentation |
| Magic Checkout scores COD risk on address and shopper history | High — company documentation |
| RazorpayX is the fastest-growing segment | Medium — reported, not quantified |
| UPI MDR zero by government mandate since Jan 2020 | High |
| Parliamentary Standing Committee recommended MDR return, March 2026 | Medium |
| PCI urged 0.30% MDR on large-merchant UPI/RuPay | Medium |
| No binding RBI/CBDT notification as of research date | Medium — absence of evidence, stated as such in §7 |
| India payment gateway market ~$2.07B (2025) | Medium — Mordor, but see C5 |

---

## 3. Source conflicts, with resolutions

### C1 — FY24 operating revenue

| Source | Figure |
|---|---|
| Inc42 and others | ₹2,475 cr operating revenue (₹2,501.4 cr incl. other income) |
| Implied by FY25's reported +65% on ₹3,783 cr | ₹2,293 cr |
| BW Disrupt headline | ₹2,068 cr |

**Resolution: none — both primary readings carried.** The ₹2,068 cr figure is separately identified in the same reporting as the *payment aggregation segment*, not total operating revenue, so it is treated as a segment figure rather than a third conflicting total. The ₹2,475 vs ₹2,293 conflict most plausibly reflects an entity-scope change around the May 2025 reverse flip, but that is a hypothesis.

**Why it did not need resolving.** The conclusion — margin compressed — holds under both. Averaging them would have produced one clean number that is not true under either reading.

### C2 — Reverse-flip tax cost

| Source | Figure |
|---|---|
| Entrackr, Inc42, IBS Intelligence, Compliance Calendar | ~$150M / ₹1,245–1,280 cr |
| The Head and Tale | "as high as $400 million" |

**Resolution: the ~$150M cluster preferred, the outlier retained.** Four independent outlets converge on ~$150M, consistent with a reported FY25 loss of ₹1,209 cr. A $400M (~₹3,400 cr) tax charge is hard to reconcile with that loss figure. The outlier is noted rather than deleted, since it may reflect total restructuring cost rather than tax alone.

### C3 — IPO valuation and raise size

| Source | Valuation | Raise |
|---|---|---|
| Business Today (April 2026) | ~$5B | $600–700M |
| NiftyTrader | ₹50,000–60,000 cr ($5.7–6.8B) | ~₹6,000 cr |
| Various | — | ₹5,700 cr (₹2,700 cr fresh + OFS) |
| Shareholder approval (reported) | — | ~$316M fresh |
| valueforstartups.in | **$9.2B, "Series G $490M"** | — |

**Resolution: a $5–6B range is used; the $9.2B claim is rejected.** It appears only on a low-quality aggregator, contradicts every credible outlet, and is inconsistent with the well-documented $7.5B December 2021 round being described as a markdown. No credible reporting of a Series G was found. The raise-size spread is largely explained by the distinction between fresh issue (~₹2,700 cr) and total including OFS.

### C4 — Total Payment Volume

The same ~$180B annualised figure is attributed to FY24 by Inc42-era reporting and to 2026 by aggregators, with no intervening growth. Given a stated $400B target for 2030 and 65% revenue growth, a flat TPV across FY24–FY26 is implausible; at least one source is recycling the other without checking the date.

**Resolution: none — flagged as probably stale and excluded from all conclusions.** TPV appears in §19 only as context, graded Conflicting. Where a volume reference was needed, the dated company-stated $400B 2030 target was used instead.

### C5 — Market size versus market share

If the India payment gateway market is ~$2.07B (Mordor) and Razorpay holds ~55% (coinlaw.io), Razorpay's gateway revenue would be ~$1.14B — roughly 2.5× its entire reported company revenue of ~$430–450M including all non-gateway products. These cannot both be true.

**Resolution: the share figure is rejected as internally inconsistent.** The likely explanation is definitional — Mordor appears to size gateway software/service revenue while Razorpay's reported revenue includes gross processing flows and non-gateway products. Since neither definition can be confirmed, **no market-share percentage is used anywhere in the teardown.** §7 states this, and §8 sizes TAM/SAM/SOM in two units to sidestep the problem entirely.

---

## 4. Author-constructed content

Nothing below is a factual claim about Razorpay.

| Item | Where | Nature |
|---|---|---|
| **The central thesis** — Razorpay as an adjacent-products company running a loss-leading payments business | §3 | Author's interpretation. Built on real disclosed numbers, but a reading, not a fact |
| **Personas** — Ananya, Rohit, Meera | §14 | Fully constructed composites. No merchant interviews. Revenue figures, UPI mix percentages and frustrations are illustrative |
| **User journey scores** | §16 | Author-assigned. No satisfaction data exists |
| **UX audit and severity ratings** | §17 | Author assessment from public product surfaces. No usability testing, no formal audit |
| **Take-rate table** | §12 | Approximate, from published merchant-facing pricing ranges; realised margins inferred |
| **Reading A vs Reading B on FY25** | §12 | Author inference from the gross-profit differential, explicitly labelled as inference |
| **MPAM as North Star** | §19 | Author's proposal. Razorpay has not stated a North Star publicly |
| **Pain points and evidence ratings** | §21 | Inferred from product structure and IA, not from support data |
| **All RICE inputs** | §22 | **Entirely invented.** Razorpay's actual reach, conversion and effort figures are not public. The ordering is defensible; the numbers are not accurate. The sensitivity table exists to make this explicit |
| **The entire feature proposal — Cashboard** | §23 | **Wholly author-constructed.** Razorpay has not announced anything resembling this. The wireframe and every number in it are illustrative |
| **All requirements, success criteria and targets** | §24 | Invented. No baselines are disclosed, so no target can be calibrated |
| **A/B arms and the 40% decision rule** | §25 | Constructed. The 40% threshold is a judgement about what would justify the cost differential, not a statistically derived figure |
| **Risk severity ratings** | §25 | Author judgement |
| **Business model diagram** | §11 | Author's model of the flow, not a description of internal systems |

**Constructed but grounded.** These rest on disclosed data rather than judgement and should be treated as more reliable than the rest of this section:

- The gross margin calculation and compression finding (section 2 above) — arithmetic on reported figures
- The observation that revenue grew 65% while gross profit grew 41% — simply reading two reported numbers together
- The argument that TPV is a hazardous North Star for a zero-MDR business (§19) — logical, not empirical

---

## 5. What would materially improve this analysis

Ranked by expected improvement per unit of effort.

| # | What | Why |
|---|---|---|
| 1 | **Ten interviews with payment-only Razorpay merchants**, asking what they did the last time they needed working capital | Would validate or destroy §23's premise in an afternoon. The cheapest high-value research available |
| 2 | **UPI share of TPV, FY24 vs FY25** | The one number that would confirm or refute the central thesis directly |
| 3 | **Competitor gross margin comparison (PayU, Cashfree)** | See below — the most significant unaddressed threat to the thesis |
| 4 | **FY25 segment revenue split** | Would settle Reading A vs Reading B in §12, currently the weakest inference in the document |
| 5 | **The public DRHP, once filed** | Would replace most inferences with audited fact, including conflict C1 |
| 6 | **Current products per merchant** | Would convert §19's North Star from a proposal into a measurable claim |
| 7 | **Support ticket taxonomy or merchant NPS verbatims** | Would ground §21 in evidence rather than inference |
| 8 | **Independent confirmation of the PA-CB licence** | Currently Low-graded, which is why it was kept out of the analysis |

**Item 3 deserves emphasis.** This teardown argues margin compression is structural to Indian payments. If PayU or Cashfree show stable gross margins over the same period, that argument is wrong and the compression is a Razorpay execution problem instead — a materially different conclusion. That comparison was not performed.

---

## 6. Methodology

**Research date:** 3 August 2026. All figures as reported at that date.

**Method.** Desk research only, via web search across financial press (Business Standard, Business Today), Indian startup media (Entrackr, Inc42, YourStory), company documentation (razorpay.com, Razorpay Docs), market research (Mordor Intelligence), and general statistics aggregators.

**Cross-checking rule.** Every financial and usage figure was checked against at least two sources where two existed. Where sources conflicted, both were retained and documented in section 3. **No conflicting figures were averaged.** Unresolvable conflicts were either excluded from conclusions (C4, C5) or the conclusion was constructed to hold under both readings (C1).

**Source credibility.** Four sources encountered — coinlaw.io, valueforstartups.in, bayelsawatch.com, digitalinasia.com — show the characteristics of automated statistics-aggregation content: unattributed figures, no methodology, and in one case (the $9.2B valuation, C3) claims contradicted by all credible reporting. They were used only to identify claims worth verifying elsewhere, never as sole evidence in any conclusion.

**What was not done.** No primary research. No merchant interviews. No usability testing. No accessibility audit. No access to Razorpay's DRHP, which is confidentially filed. No independent verification of any financial figure — all financials are as reported by third parties and are unaudited from this document's perspective.

**Undisclosed baselines** are marked "not disclosed" rather than estimated. Numbers that appeared plausible but unsourced were excluded. Corrections to any claim here are welcome and will be reflected in this file.

---

*Companion to `README.md` · Day 38 of 90 · Gaurav Singh · 3 August 2026*
