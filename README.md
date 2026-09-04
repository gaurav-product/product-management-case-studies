# Day 69 — MedPlus: The Cohort Curve Is the Disclosure

> MedPlus grew revenue 21.8% in the June 2026 quarter and its profit fell 21.7% — a 43.50-point swing in a single line. Management's explanation is that new stores drag margins while they mature, and to its considerable credit the company publishes the evidence: shop-level EBITDA by opening cohort, running 9.3% for stores opened up to FY23, then 7.1%, 1.9%, 0.7%, and **−5.0% for the FY27 vintage**. Read down the column it is a maturation curve. Read across vintages it is something else, and no snapshot can tell the two apart. Underneath sit two disclosed mechanisms that make the second reading harder to dismiss: **131 of 146 net store additions were franchisees**, a channel growing 164% against 18% for company-owned stores and carrying a structurally thinner margin — and **private label pharma, the margin engine, grew 2%** while the company grew 21.8%. MedPlus is scaling through the channel least aligned with the product that pays for it.

---

## 1. Cover

**Product:** MedPlus — pharmacy retail chain, private label, diagnostics
**Legal entity:** MedPlus Health Services Limited · **CIN:** L85110TG2006PLC051845
**Domain:** Healthtech — pharmacy retail
**Period examined:** Q1 FY27 (quarter ended 30 June 2026), reported 22 July 2026
**Written:** 4 September 2026
**Author:** Gaurav Singh · Day 69 of 90

---

## 2. Repository Metadata

| Field | Value |
|---|---|
| Legal entity | MedPlus Health Services Limited |
| CIN | L85110TG2006PLC051845 |
| Incorporated | 30 November 2006 |
| Registrar | RoC Hyderabad |
| Former name | MedPlus Health Services Private Limited |
| Registered & corporate office | H. No. 11-6-56, Survey No. 257 & 258/1, Opp. IDPL Railway Siding Road, Moosapet, Kukatpally, Hyderabad 500037, Telangana |
| Listings | BSE **543427** · NSE **MEDPLUS** |
| NIC code | **8511 — "Hospital activities"** |
| Founder, MD & CEO | Dr. Madhukar Reddy Gangadi |
| WTD & COO | Dr. Cherukupalli Bhaskar Reddy |
| Chairman | Murali Sivaraman |
| Key subsidiary | Optival Health Solutions |

India's industrial classification files a pharmacy retail chain under *hospital activities* — a category defined as institutions with accommodation facilities, which a shop selling medicines conspicuously is not. **This is the sixth consecutive case study in this series whose NIC code does not describe the business**, after BookMyShow (99999), Atomberg (7290), Vodafone Idea (3210), Max Healthcare (722) and Dr. Lal PathLabs (74899). Six in a row is a finding about the register, not about six companies.

---

## 3. Badges

`Day 69/90` · `Healthtech` · `Pharmacy retail` · `Listed (BSE/NSE)` · `Q1 FY27 primary` · `Company publishes its own cohort curve` · `137 programmatic checks, all passing` · `Zero fabricated figures`

---

## 4. Table of Contents

<details>
<summary>Expand — 65 sections</summary>

| # | Section | # | Section |
|---|---|---|---|
| 1 | Cover | 34 | HEART |
| 2 | Repository Metadata | 35 | Growth Strategy |
| 3 | Badges | 36 | Growth Loops |
| 4 | Table of Contents | 37 | Network Effects |
| 5 | Executive Summary | 38 | Product Strategy |
| 6 | Product Overview | 39 | Monetization |
| 7 | Company Background | 40 | Trust & Safety |
| 8 | Product Timeline | 41 | Technical Architecture |
| 9 | Vision & Mission | 42 | Data Flow |
| 10 | Problem Statement | 43 | API Ecosystem |
| 11 | Market Research | 44 | Privacy & Security |
| 12 | Industry Analysis | 45 | Pain Points |
| 13 | TAM / SAM / SOM | 46 | Opportunity Mapping |
| 14 | Competitor Analysis | 47 | RICE |
| 15 | SWOT | 48 | MoSCoW |
| 16 | Porter's Five Forces | 49 | Kano |
| 17 | Business Model Canvas | 50 | Feature Proposal |
| 18 | Revenue Model | 51 | PRD |
| 19 | Target Users | 52 | Wireframes |
| 20 | Personas | 53 | Rollout Plan |
| 21 | Jobs To Be Done | 54 | A/B Testing |
| 22 | User Journey | 55 | KPI Dashboard |
| 23 | User Flow | 56 | Product Roadmap |
| 24 | Information Architecture | 57 | Risks & Mitigation |
| 25 | UX Audit | 58 | Future Vision |
| 26 | UI Audit | 59 | PM Lessons |
| 27 | Accessibility | 60 | PM Interview Questions |
| 28 | Feature Breakdown | 61 | References |
| 29 | AI Capabilities | 62 | About the Author |
| 30 | Product Metrics | 63 | License |
| 31 | North Star Metric | 64 | Self Review |
| 32 | Product Analytics | 65 | Appendix |
| 33 | AARRR | | |

</details>

---

## 5. Executive Summary

MedPlus reported the quarter ended 30 June 2026 on 22 July. Consolidated revenue was ₹1,879.60 Cr, up **21.8%**. Consolidated profit after tax was ₹33.17 Cr, down **21.7%** — a swing of **43.50 percentage points** between the two lines. Operating EBITDA fell 11% to ₹65.10 Cr at a 3.5% margin, 120 basis points lower. Gross margin fell 160 basis points to 24.5%, with gross profit growing 14% — the slowest in four years. The stock fell **17.80%** to a 52-week low of ₹653.80, **63.96%** of its 52-week high.

The company's own framing is that this is the cost of expansion, and it is not a dodge. MedPlus added 146 net stores to reach 5,476 across 2.9 million square feet, and it publishes the maturation evidence most retailers keep private: **shop-level EBITDA margin by opening cohort — 9.3% for stores opened up to FY23, then 7.1% (FY24), 1.9% (FY25), 0.7% (FY26) and −5.0% (FY27).** That disclosure is genuinely unusual and this case study depends on it entirely.

The difficulty is that a single snapshot of cohorts at different ages cannot separate *"young stores are young"* from *"newer stores are worse."* Both produce exactly this curve. What tilts the reading are two other disclosures.

**The channel shifted.** Of 146 net additions, **131 were franchisees** — 89.73%. Franchisee sales grew **164%** against 18% for company-owned stores, a ratio of **9.11×**, taking franchisee share of pharmacy revenue from 2.5% to 5.4%. Management names the higher franchisee contribution as a cause of the gross margin decline. Franchisees are now 12% of stores producing 5.4% of pharmacy revenue — a revenue-to-store-share ratio of **0.45**.

**The margin engine stalled.** Private label pharma grew **2%** — **9.17%** of the company's own revenue growth rate — while branded pharma grew 20%, ten times faster. Private label is where MedPlus's gross margin lives, and it went from being the growth story to being the slowest line in the business.

Put together, MedPlus is scaling fastest through the channel with the thinnest margin and the least incentive to push the product that carries the margin. Nothing in the disclosure ties the two together, and nothing in the franchise economics does either.

The proposal, *Own-Label Compact*, addresses precisely that gap — and is then ranked last, behind publishing the cohort curve longitudinally instead of as a snapshot.

---

## 6. Product Overview

MedPlus operates India's second-largest pharmacy chain: 5,476 stores across roughly 600 cities, selling prescription medicines, over-the-counter products and general FMCG, alongside a private label range in both pharma and non-pharma, plus a diagnostics arm and an optical business. The consumer proposition since 2006 has been genuine medicine at a discount — the company pioneered value pricing in Indian pharmacy retail.

The structural feature that matters here is that MedPlus sells two different things through one shelf: **branded drugs, where it is a distributor earning a thin trading margin, and its own label, where it is a manufacturer-brand owner earning a much wider one.** The mix between them, not the price of either, is what determines whether a store makes money.

---

## 7. Company Background

MedPlus was incorporated on 30 November 2006 in Hyderabad and opened its first pharmacy in February 2006. The founding premise was counterfeit medicine: Dr. Madhukar Gangadi started the company after a WHO report indicated a large share of the world's fake medicines originated in India, and built the chain around guaranteed-genuine supply at a discount.

The company listed in December 2021 and remains founder-led, with Dr. Gangadi as MD and CEO and Dr. Cherukupalli Bhaskar Reddy as WTD and COO. FY26 was a strong year — consolidated PAT of ₹219.65 Cr, up 46.12% — which is the context that makes the June quarter's reversal notable rather than routine.

---

## 8. Product Timeline

| Date | Event |
|---|---|
| Feb 2006 | First MedPlus pharmacy opens in Hyderabad |
| 30 Nov 2006 | MedPlus Health Services incorporated, RoC Hyderabad |
| Dec 2021 | IPO; listed on BSE and NSE |
| FY24 | Private label pharma at 7.9% of pharma sales in Q1 |
| FY26 | Private label pharma reaches 20.4% of pharma sales in Q1; PAT ₹219.65 Cr, +46.12% |
| Q1 FY27 | 146 net store adds, **131 of them franchisees**; franchisee sales +164% |
| Q1 FY27 | Board approves ₹155 Cr of non-core capex — food park and wellness facility |
| 7 Jul 2026 | Discount on purchases above ₹1,000 cut from 20% to 19% |
| Jul 2026 | Private label membership fee raised from ₹99 to ₹149 |
| 22 Jul 2026 | Q1 FY27 results: revenue +21.8%, PAT −21.7%; stock falls 17.80% |
| Post-results | The ₹155 Cr capex is put **on hold** after investor feedback |

---

## 9. Vision & Mission

MedPlus positions itself as India's favourite pharmacy, built on genuine medicines, convenience and low prices. FY27's stated operating plan is 800 net new stores — **5.48×** the 146 delivered in Q1 — alongside deeper private label penetration.

The tension this case study examines is that those two goals are, on the current evidence, pulling against each other. The fastest route to 800 stores is franchising, and the franchise channel is where private label penetration and gross margin are both lowest.

---

## 10. Problem Statement

**For MedPlus:** the company is adding stores through a channel it does not operate, selling a mix it does not control, and reporting the blended result in a single gross margin. When that margin fell 160 basis points, the disclosure could attribute it to both causes but could not size either.

**For the franchisee:** they buy stock from MedPlus at wholesale and earn the retail spread. Private label may be better for MedPlus's margin, but nothing in that arrangement makes it better for theirs — so the rational franchisee stocks what sells fastest, which is branded pharma.

**The intersection:** MedPlus's profit depends on private label penetration; its growth now depends on franchisees; and **no mechanism connects the two.** The company is scaling the part of the network with the weakest reason to sell the product that pays for the scaling.

---

## 11. Market Research

Indian pharmacy retail is enormous, fragmented and mostly independent — hundreds of thousands of standalone chemists against a handful of organised chains, of which MedPlus is the second largest. The organised players compete against the independents on price, authenticity and range, and against each other largely on location density.

Two structural features matter. Branded pharmaceutical pricing is largely fixed by the manufacturer and constrained by regulation, so a retailer's only real gross-margin lever is **substituting its own label where the molecule permits.** And because pharmacy is a proximity business, network density is the primary growth constraint — which is what makes franchising so tempting, and so consequential.

---

## 12. Industry Analysis

The competitive pressure of the last several years came from digital pharmacy — deep discounting on delivered medicines — and the organised chains answered with a combination of store density and private label economics. MedPlus took private label pharma from 7.9% of Q1 pharma sales in FY24 to 20.4% by Q1 FY26, which is a genuinely rapid product achievement.

What the June quarter shows is that lever reaching a limit, or at least a pause: **private label pharma grew 2% year on year.** Private label non-pharma grew 30% and branded pharma 20% — a **28-point spread between the fastest and slowest private label lines** in the same business. Whatever slowed pharma substitution was specific to pharma, not to own-brand generally, and the company has not disclosed what it was.

---

## 13. TAM / SAM / SOM

*Framework note: run in restricted form. No primary-sourced Indian pharmacy retail market size was located that is not a vendor estimate, so this is sized from MedPlus's own disclosed revenue and mix, expressed in annualised rupees.*

| Layer | Definition | Size | Basis |
|---|---|---|---|
| TAM | Annualised revenue at the Q1 run rate | **₹7,518.40 Cr** | ₹1,879.60 Cr × 4 🟢 |
| SAM | Annualised private label revenue | **₹1,503.68 Cr** | 20% of revenue 🟢 |
| SOM | Annualised revenue from one year of new stores | **₹801.81 Cr** | 146 × 4 ÷ 5,476 of revenue, derived |
| *The constraint* | Franchisee share of pharmacy revenue | **5.4%**, from 2.5% | 🟢 |

The interesting layer is the third. A full year of store additions at the Q1 pace touches roughly a tenth of revenue — and on the company's own cohort disclosure, that tenth operates at **−5.0%** shop-level EBITDA in its first year.

---

## 14. Competitor Analysis

*Framework note: MedPlus is compared here against **its own cohorts** rather than against a peer, and the reason is a disclosure gap rather than a stylistic choice. Apollo Pharmacy sits inside Apollo Hospitals' pharmacy segment and is not reported with store-cohort economics; Wellness Forever and Netmeds do not publish comparable cohort data; Tata 1mg is unlisted. No competitor discloses shop-level EBITDA by vintage, so a like-for-like comparison would have to be constructed, and this series does not construct comparators.*

| Cohort (opening year) | Shop-level EBITDA margin | As % of mature cohort |
|---|---|---|
| Up to FY23 | **9.3%** | 100% |
| FY24 | 7.1% | **76.34%** |
| FY25 | 1.9% | **20.43%** |
| FY26 | 0.7% | **7.53%** |
| FY27 | **−5.0%** | negative |

Three readings. The spread from oldest to newest is **14.30 points**, and **two of five cohorts sit at or below 1%** shop-level margin with one outright loss-making. The steps down are not smooth — **−2.20, −5.20, −1.20, −5.70** — which is what you would expect from a mix of ageing and vintage quality rather than ageing alone.

The honest reading, and the one this case study holds: **a cohort snapshot cannot distinguish maturation from deterioration.** If every cohort follows the same path, the FY27 vintage will reach 9.3% in four years and the current profit compression is an accounting consequence of growth. If newer vintages are structurally worse — poorer catchments, more franchisee stores, weaker private label attach — then the curve is a warning. Only the *same* cohort tracked across quarters separates them, and MedPlus publishes the snapshot, not the series.

And the number that cuts against this case study's own argument, included because it should be: **the FY24 cohort is already at 76.34% of mature margin.** That is a real maturation effect, visible in MedPlus's own data, and it is the strongest evidence for management's reading.

---

## 15. SWOT

| | |
|---|---|
| **Strengths** — second-largest pharmacy chain at 5,476 stores and 2.9 mn sq ft; private label at 20% of revenue, built from 7.9% of pharma sales in two years; FY26 PAT up 46.12%; publishes cohort economics almost no retailer discloses; FY24 cohort already at 76.34% of mature margin | **Weaknesses** — PAT −21.7% on revenue +21.8%; gross profit growth the slowest in four years; private label pharma growth of 2%; salaries growing 8.20 points faster than revenue; 26.26% of gross store openings offset by closures |
| **Opportunities** — franchising lowers the capital cost of density; private label non-pharma growing 30%; diagnostics up 22.4%; membership fee repricing with near-total flow-through; discount recalibration already underway | **Threats** — franchisee channel dilutes gross margin structurally; FY27 cohort at −5.0% shop-level EBITDA; 800-store guidance implies 5.48× the Q1 run rate; ₹155 Cr of approved capex withdrawn under investor pressure; stock at 63.96% of its 52-week high |

---

## 16. Porter's Five Forces — run twice

*Framework note: run as a double pass on the two store types MedPlus now operates through — the **company-owned** store, where MedPlus sets the assortment, and the **franchisee** store, where it does not. The seam is chosen because 89.73% of net additions this quarter were franchisees, because the forces genuinely invert across it, and because both are reported inside one gross margin.*

| Force | COMPANY-OWNED store (COCO) | FRANCHISEE store |
|---|---|---|
| **Buyer power** | The end customer's, moderate — discount-led and price-comparing, but MedPlus controls the offer | **The franchisee's, and it is high.** They choose what to stock; MedPlus earns a wholesale margin whether or not private label moves |
| **Rivalry** | Against independents and chains on price, proximity and authenticity | **Also against MedPlus itself** — a franchisee near a COCO store competes for the same catchment |
| **Substitutes** | Digital pharmacy, independents | Identical, plus the franchisee can under-emphasise own label in favour of faster-turning branded stock |
| **New entrants** | Constrained by capital, licensing and supply relationships | **Weakly constrained** — the franchise model is itself the entry route, which is why it scales at 164% |
| **Supplier power** | MedPlus is the buyer, with scale leverage over distributors | **MedPlus becomes the supplier** — and a supplier's leverage over assortment is contractual, not operational |

The inversion is the finding. In the left column MedPlus is a retailer that decides what sits on its shelves and therefore controls its own mix. In the right column it is a **wholesaler to an independent businessperson whose interests only partly overlap with its own** — earning a thinner margin on the sale and holding no operational control over whether the high-margin product is stocked, faced or recommended. Reporting one gross margin across both averages a business MedPlus controls with one it supplies, and every quarter the right column grows faster, that blended margin falls for reasons no pricing decision explains.
---

## 17. Business Model Canvas

| Block | MedPlus |
|---|---|
| Value proposition | Guaranteed-genuine medicine at a discount, close to home |
| Customer segments | Chronic and acute prescription buyers, OTC and FMCG shoppers, diagnostics users |
| Channels | 5,476 stores (≈12% franchisee), home delivery, MedPlusMart |
| Revenue streams | Branded pharma 68.8%, private label pharma 10.7%, private label non-pharma 9.3%, branded non-pharma, diagnostics 1.97% |
| Key resources | Store network, 2.9 mn sq ft, private label formulations, supply chain and warehouses |
| Key activities | Store opening, procurement, private label development, franchise recruitment |
| Key partners | **Franchisees — now the primary growth channel** |
| Cost structure | Cost of goods (75.5% of revenue), pharmacy salaries, rent, non-pharmacy overhead |
| Margin engine | Private label, at 20% of revenue |

The last two rows are the whole case study. The growth partner and the margin engine sit in different rows of the canvas with no line connecting them.

---

## 18. Revenue Model

Revenue is overwhelmingly pharmacy: diagnostics contributed ₹37.08 Cr, or **1.97%** of the total, and pharmacy operating EBITDA of ₹58.80 Cr is **90.32%** of group operating EBITDA. So the group's economics are the pharmacy's economics, and the pharmacy's economics are a mix question.

Within that mix, branded pharma is 68.8% of revenue at a thin trading margin, while private label — 20% of revenue across pharma and non-pharma — carries the wide one. **Branded pharma revenue is 6.43× private label pharma revenue**, which is why a 160 basis point move in gross margin can happen without a single price changing: it only requires the two to grow at different rates. This quarter they grew at 20% and 2%.

---

## 19. Target Users

The core user is the price-sensitive urban and semi-urban Indian household buying prescription medicine, for whom MedPlus's proposition is authenticity plus a standing discount. Around that sit OTC and FMCG shoppers, whose basket carries better margin, and diagnostics users.

The user this case study is most concerned with is not a consumer at all: **the franchisee.** They are a partner in the canvas, a buyer in the P&L, and the decisive actor in whether MedPlus's margin thesis works — and they are not mentioned in any consumer-facing artefact.

---

## 20. Personas

**Lakshmi, 54, Hyderabad, chronic hypertension.** Refills three drugs monthly. Substitutable to private label on at least one. Whether she is offered it depends entirely on which store she walks into.

**Ravi, 41, franchisee in a tier-2 town.** Invested his own capital, buys stock from MedPlus at wholesale, earns the retail spread. Stocks what turns fastest. Has no economic reason to prefer MedPlus's own label over a branded pack that sells itself.

**A MedPlus expansion manager.** Compensated on net store additions against an 800-store annual plan. The fastest path to that number is franchisees, which is exactly what the Q1 numbers show.

---

## 21. Jobs To Be Done

*Framework note: JTBD is used because the franchisee and MedPlus are buying and selling the same box with different jobs attached to it.*

| Job | Who | Current solution | Adequacy |
|---|---|---|---|
| "Give me my prescription cheaply and genuinely" | Patient | Discount + authenticity guarantee | Well served; the discount was just trimmed 20% → 19% |
| "Make my store turn over stock profitably" | Franchisee | Wholesale supply from MedPlus | Served — but private label is **not** the answer to this job |
| "Grow gross margin without raising prices" | MedPlus | Private label penetration | **Failing this quarter** — 2% growth |
| "Add 800 stores in the year" | MedPlus expansion | Franchising | Working, and it is what dilutes the row above |

Rows two and three are in direct tension, and row four accelerates it. This is not a strategy failure so much as an **incentive design gap**: three of the four jobs are being met, and the one that pays for everything is not.

---

## 22. User Journey

| Stage | COCO store | Franchisee store |
|---|---|---|
| Stock decision | MedPlus assortment and planogram | Franchisee's judgement |
| Substitution offer | Staff trained and incentivised on own label | No disclosed mechanism |
| Customer sees | Private label alternative alongside branded | Whatever was ordered |
| MedPlus earns | Full retail margin on own label | Wholesale margin, mix-indifferent |
| Reported as | One blended gross margin | One blended gross margin |

The final row is the reporting problem in a sentence. Two materially different economics arrive at the same line, and the only visible symptom is that the line moved.

---

## 23. User Flow

The substitution moment is the entire product. A customer presents a prescription; the person behind the counter either offers the private label equivalent where the molecule permits, or reaches for the branded pack. Everything in MedPlus's margin structure turns on that three-second interaction.

In a company-owned store MedPlus controls the training, the incentive and the shelf. In a franchisee store it controls none of the three, and that channel just grew **164%**.

---

## 24. Information Architecture

The disclosure architecture is unusually good in one respect and blank in another. MedPlus publishes shop-level EBITDA by opening cohort — a genuinely rare voluntary disclosure — and reports private label share, franchisee revenue share and store counts.

What it does not publish is any of these **crossed with each other**: private label penetration by channel, cohort economics split COCO versus franchisee, or the same cohort tracked across quarters. Every one of those is a join on data the company already has, and each would settle a question this analysis can only frame.

---

## 25. UX Audit

The customer experience is not the problem here and this section should say so plainly. Discount, authenticity and proximity are delivered, and the June-quarter pricing changes — discount from 20% to 19% above ₹1,000, membership from ₹99 to ₹149 — are modest recalibrations rather than a repositioning.

The one observation worth making: the membership fee increase is a **50.51%** rise expected to produce roughly ₹10.5 Cr a year, which is **114.22%** of the quarter's entire ₹9.19 Cr profit decline. A structural margin problem is being partly answered with a subscription price rise, which works arithmetically and does nothing about mix.

---

## 26. UI Audit

MedPlus's digital surfaces — store locator, ordering, MedPlusMart — are functional and not material to this analysis.

Worth naming because it bounds the proposal: **the decisive interface in this business is a shelf and a counter, not a screen**, and in 12% of stores MedPlus does not own either.

---

## 27. Accessibility

Density is the access story: 5,476 stores across roughly 600 cities, and franchising is the mechanism that extends reach into towns where a company-owned store cannot clear its cost base. That is a genuine argument for the channel and it deserves stating alongside the critique.

The counterpoint is that franchisee stores are 12% of the network producing 5.4% of pharmacy revenue — a ratio of **0.45** — so they are smaller, newer or slower, and the access they provide is real but thin.

---

## 28. Feature Breakdown

| Area | Current state |
|---|---|
| Store network | 5,476 stores, 2.9 mn sq ft, ~600 cities, ~12% franchisee |
| Private label | 20% of revenue — pharma 10.7%, non-pharma 9.3% |
| Branded pharma | 68.8% of revenue |
| Diagnostics | ₹37.08 Cr, +22.4%, 1.97% of revenue |
| Membership | Private label membership, ₹99 → ₹149 per year |
| Discount | 20% → 19% on purchases above ₹1,000, from 7 Jul 2026 |
| Warehousing | Expanded network supporting store growth |
| Non-core capex | Food park ₹40 Cr, wellness facility ₹115 Cr — **approved, then put on hold** |
| **Franchisee private-label mechanism** | **Does not exist** |
| **Cohort economics by channel** | **Not disclosed** |

The last two rows are the subject of §50 and §47 respectively, and both absences are verifiable from the disclosures rather than assumed.

---

## 29. AI Capabilities

MedPlus has disclosed no material AI product, and none is proposed here.

The relevant observation is that substitution eligibility — which prescriptions can be met with an own-label equivalent, at which store, for which customer — is a rules-and-data problem the company can already solve with its formulary and dispensing history. The gap is that in a franchisee store there is nobody with an incentive to act on the answer.

---

## 30. Product Metrics

| Metric | Q1 FY27 | Note |
|---|---|---|
| Revenue | ₹1,879.60 Cr | +21.8% YoY, +0.82% QoQ |
| Gross margin | 24.5% | −160 bps; gross profit +14%, slowest in four years |
| Operating EBITDA | ₹65.10 Cr | 3.5% margin, −120 bps, **−11% YoY** |
| Reported EBITDA margin | 7.1% | from 8.5%, −140 bps — **a different base**, see below |
| PAT | ₹33.17 Cr | **−21.7% YoY**, −48.16% QoQ, 1.76% margin |
| Net store adds | 146 | **131 franchisees**, 52 closures, 198 gross openings |
| Franchisee sales growth | **+164%** | vs +18% company-owned, a **9.11×** ratio |
| Private label pharma growth | **+2%** | vs branded pharma +20%, a **10×** gap |
| Diagnostics | ₹37.08 Cr | +22.4% |
| Capex | ₹33.84 Cr | **61.66%** of the quarter's plan |

**Two EBITDA margins are in circulation and they are 3.60 points apart** — a reported 7.1% and an operating 3.5%, the difference being **₹68.35 Cr**, consistent with lease rent treated differently between the two. Both are the company's own figures on their own bases; the analysis uses each explicitly and never mixes them (Appendix A-2).

The cohort table in §14 is the metric that matters most, and it is the one MedPlus deserves credit for publishing at all.

---

## 31. North Star Metric

MedPlus's implied north star is net store additions, and this quarter shows the failure mode: 146 added, guidance reaffirmed at 800, and profit down 21.7%.

**Proposed North Star — PLP/1k: Private Label Prescriptions per 1,000 substitutable prescriptions dispensed.**

A dispense counts in the numerator only if **all four** hold:
1. the prescription was for a molecule with a MedPlus own-label equivalent in stock at that store;
2. the own-label equivalent was actually dispensed;
3. the customer was offered the branded alternative and the choice was recorded;
4. the store was in the numerator's channel — **COCO and franchisee reported separately, never blended.**

**The denominator is the design choice.** It is *substitutable prescriptions dispensed* — not total prescriptions, not revenue. Opening more stores does not move it. Selling more branded pharma does not move it. It rises only when the specific interaction that creates MedPlus's margin goes the company's way, and condition 3 means it cannot be improved by removing customer choice.

**Guardrail — SDR-90: Substitution Decline Rate at the 90th percentile.** In the decile of stores with the highest private-label penetration, the share of customers who were offered own label and declined it, reported by channel and by therapy area. Rising decline rates at high-penetration stores mean substitution is being pushed past where customers want it. Owned by a pharmacy-practice function with no sales target, with automatic suspension of penetration incentives at any store that breaches.

---

## 32. Product Analytics

Every input for both metrics already exists in MedPlus's dispensing systems: the prescription, the molecule, the formulary, the stock position, the store and its channel. The join is not built, or at least not published.

The absence is the evidence. A company reporting private label as a **share of revenue** rather than a **rate of substitution** is measuring the outcome without measuring the behaviour that produces it — which is why a 2% growth quarter can arrive without a prior diagnostic.

---

## 33. AARRR

*Framework note: applied to the store network rather than the customer, because the funnel that broke this quarter is the expansion funnel.*

| Stage | Reading |
|---|---|
| Acquisition | 198 gross store openings — working |
| Activation | **26.26% of openings offset by 52 closures**; FY27 cohort at −5.0% shop-level EBITDA |
| Retention | ≤FY23 cohort at 9.3% shows stores do mature; FY24 at 76.34% of that |
| Revenue | +21.8%, but gross profit only +14% |
| Referral | Franchise recruitment — 131 added, the fastest-moving stage in the funnel |

The funnel reads as healthy at both ends and weak in the middle. **Stores are being opened faster than they are being made to work**, and the referral stage — franchise recruitment — is accelerating the intake without changing the conversion.

---

## 34. HEART

| Dimension | MedPlus |
|---|---|
| Happiness | Not disclosed; no NPS or CSAT published |
| Engagement | Membership repricing ₹99 → ₹149; no membership count or renewal rate disclosed |
| Adoption | Private label at 20% of revenue — but the pharma line grew 2% |
| Retention | Not disclosed at customer level; store closures at 26.26% of openings |
| Task success | Not defined — no measure of whether a substitutable prescription was substituted |

Task success is the row that should exist and does not, and §31 is an attempt to define it.

---

## 35. Growth Strategy

The stated strategy is 800 net new stores in FY27 with continued private label deepening, funded by internal accrual, with capex running at **61.66%** of the quarterly plan. The ₹155 Cr of approved non-core capex — a food park and a concierge wellness facility, both in Hyderabad — was put on hold after investor feedback, which is **4.58× the quarter's actual capex** and a reasonable piece of capital discipline under pressure.

**Checking whether the proposal already exists, from MedPlus's own disclosures.** Nothing in the Q1 FY27 results, presentation or earnings-call coverage describes a mechanism linking franchisee terms to private label penetration, a private-label mix disclosure by channel, or cohort economics split by channel. The franchise relationship is described in terms of store count and revenue share only. So neither the instrument in §50 nor the disclosure in §47 exists today.

The strategic question the guidance raises: 800 stores is **5.48×** the Q1 delivery, Q1 delivered **18.25%** of the annual target, and 89.73% of that came from franchisees. If the remainder arrives the same way, the channel mix shifts further toward the thinner margin for the rest of the year.

---

## 36. Growth Loops

The intended loop is: open stores → density → revenue → cash → open more stores. It works on the first three arrows and stalls on the fourth, because the newest cohort operates at −5.0% shop-level EBITDA and therefore consumes cash rather than generating it.

There is a second, adverse loop specific to franchising, and it is the mechanism this case study is built on. **Franchising is the cheapest way to add stores → franchisee stores carry lower gross margin and no private label mandate → blended gross margin falls → reported profit falls → capital discipline tightens → franchising becomes even more attractive relative to company-owned stores.** Each turn makes the next turn more likely, and nothing in the current disclosure would show it separately from ordinary maturation.

---

## 37. Network Effects

Pharmacy retail has weak network effects between customers — one shopper's purchase does not improve another's. What scale confers is procurement leverage, private label volume economics, and the fixed-cost absorption of warehouses and formulation development.

That is the real argument for density, and it is why private label penetration matters more than store count: **the returns to scale in this business live in the own-label line, not in the shelf count.** A network that grows in stores while its own-label line grows at 2% is adding the cost of scale without the benefit.
---

## 38. Product Strategy

MedPlus's strategy is sound on both halves taken separately. Density is the right ambition for a proximity business, franchising is a legitimate way to buy it cheaply, and private label is the correct answer to a category where branded prices are fixed by someone else. FY26's 46.12% profit growth shows the combination working.

The strategic gap is that the two halves are now being pursued through **channels with opposite incentives**, and the reporting cannot see the collision. A blended gross margin will always show the symptom — it moved 160 basis points — and will never show which half caused it. That is a measurement failure before it is a strategy failure, which is why §47 ranks measurement first.

---

## 39. Monetization

MedPlus monetises the spread between what it buys a box for and what it sells it for, and that spread has two very different sizes. On branded pharma it is thin and set by manufacturers and regulation. On its own label it is wide and set by MedPlus.

The franchisee channel monetises differently again: MedPlus earns a **wholesale** margin on the sale to the franchisee and nothing on the retail spread. So the same box sold through a franchisee earns MedPlus less than through a company store — which is exactly what management identified as one cause of the gross margin decline, and which will recur every quarter the channel mix shifts.

---

## 40. Trust & Safety

*Placed before §50 deliberately, because the proposal creates a clinical and commercial risk that has to be bounded before the mechanism is described.*

**Substitution pressure is a patient-safety question, not just a margin one.** Any instrument that rewards private label penetration creates pressure to substitute where substitution is not appropriate — narrow-therapeutic-index drugs, paediatric formulations, patients stabilised on a specific brand. The mechanic: an excluded-molecule list defined by pharmacy practice and not by commercial teams, hard-coded into the eligibility check so those prescriptions never enter PLP/1k's denominator at all. A molecule cannot be added to the eligible list by anyone with a revenue target.

**Choice must remain real.** A customer who wants the branded pack must get it without friction. The mechanic: condition 3 of PLP/1k requires the branded alternative to have been offered and the choice recorded, and **SDR-90 measures declines rather than suppressing them** — a store with rising decline rates is flagged, not rewarded for eliminating them.

**Franchisee coercion.** Tying wholesale pricing to own-label mix could push an independent operator to stock against their own commercial judgement or their patients' interest. The mechanic: the tier is an incentive, never a supply condition — no franchisee is refused stock, cut off, or penalised on branded supply for a low own-label mix, and the tiers are published so terms cannot be applied selectively.

**The incentive that must be excluded, stated plainly.** If penetration targets are set per store without an eligibility gate, the fastest route to hitting them is substituting where it should not happen. §48 places store-level penetration targets without an eligibility denominator permanently out of scope, and §53 makes the excluded-molecule list a precondition of launch rather than a later refinement.

**A live compliance note.** Drug licences were suspended at three Karnataka stores operated by subsidiary Optival Health Solutions in July 2026, with a disclosed financial impact under ₹2 lakh. Immaterial financially, and worth recording because licence compliance across 5,476 stores — 12% of them operated by third parties — is the operational risk that scales fastest with franchising.

---

## 41. Technical Architecture

The systems that matter are the point-of-sale and dispensing application in each store, the formulary that maps molecules to own-label equivalents, and the supply chain linking warehouses to stores and franchisees. MedPlus operationalised additional warehouses through FY26 to support the expanded network.

The architectural question the proposal raises is narrow: **does the franchisee run MedPlus's dispensing software?** If yes, substitution eligibility and offer-recording are a feature release. If no, the entire measurement layer for 12% of stores has to be built or contracted first — which is why K2 in §53 is named as the kill criterion most likely to fire.

---

## 42. Data Flow

Today: prescription → dispense → sale recorded → revenue aggregated → private label share reported as a percentage of revenue. Channel is captured; substitution eligibility is not.

The proposal adds one upstream step: prescription → **eligibility check against the formulary and the excluded-molecule list** → offer and choice recorded → dispense. The critical constraint is directional: eligibility and exclusion data flow from pharmacy practice into the dispensing system and never the reverse, enforced by access control rather than policy, so no commercial team can widen the eligible list to make a target easier.

---

## 43. API Ecosystem

The relevant integration surface is franchisee-facing: ordering, stock visibility, wholesale pricing and settlement. That is where a penetration-linked tier would be computed and applied, and it already exists because franchisees already buy through it.

The asymmetry worth naming: MedPlus has a fully instrumented relationship with its franchisees on **what they buy from it**, and no instrumented relationship at all on **what they sell to patients.** The proposal is largely an argument for closing that gap.

---

## 44. Privacy & Security

Prescription data is sensitive personal data under India's DPDP framework, and the proposal increases the number of parties processing it only marginally — the franchisee already dispenses the prescription.

The design position: **what flows to MedPlus from a franchisee store is an aggregate substitution rate, not a patient-level dispensing record.** The tier can be computed from counts of eligible-and-substituted versus eligible-and-not, with no molecule-level patient data leaving the store. Anything richer would be more useful commercially and is deliberately excluded.

---

## 45. Pain Points

| # | Pain point | Evidence |
|---|---|---|
| P1 | Revenue +21.8% against PAT −21.7%, a 43.50-point swing | Q1 FY27 results 🟢 |
| P2 | Private label pharma growing at 9.17% of the company rate | Derived, D4a 🟢 |
| P3 | 89.73% of net store adds are franchisees, growing 9.11× faster than COCO | Derived, D3a, D3d 🟢 |
| P4 | Franchisee mix named by management as a gross-margin cause, but unsized | Earnings call coverage 🟡 |
| P5 | FY27 cohort at −5.0% shop-level EBITDA; two of five cohorts at or below 1% | Company disclosure 🟢 |
| P6 | No private label penetration disclosed by channel | Absence across all Q1 FY27 disclosures 🟢 |
| P7 | Cohort curve is a snapshot, so maturation and deterioration are indistinguishable | Structural, Appendix A-3 🔴 |
| P8 | Two EBITDA margins 3.60 points apart in the same release | Derived, D7a 🟡 |
| P9 | Salaries growing 8.20 points faster than revenue | Derived, D6a 🟢 |
| P10 | 800-store guidance is 5.48× the Q1 run rate | Derived, D3k 🟢 |

---

## 46. Opportunity Mapping

| Opportunity | Annualised revenue addressed | Requires |
|---|---|---|
| Publish the cohort curve longitudinally | ₹7,518.40 Cr | Nobody's cooperation |
| Site-quality bar on new openings | ₹801.81 Cr | Nobody's cooperation |
| Private label range expansion | ₹1,503.68 Cr | Customers to choose own label |
| Own-Label Compact for franchisees | ₹1,503.68 Cr | Franchisees to change stocking behaviour |
| Diagnostics scale-up | ₹148.32 Cr | Customers, capital |

The right-hand column decides §47 again. The largest addressable number on the page belongs to the initiative that needs nobody's permission, and it happens to be the one that would settle whether the rest of this analysis is correct.

---

## 47. RICE

*Framework note: run with a sensitivity pass. Initiatives requiring a franchisee or a customer to change behaviour are multiplied by a stress rule; those delivering value on data and assets MedPlus already controls are exempt.*

**The stress rule comes from MedPlus's own cohort disclosure.** Stores opened in FY26 — open a full year — reached a shop-level EBITDA margin of 0.7% against 9.3% for the mature cohort: **7.53%.** That is the company's own published evidence of how much of a mature store's economics a new store actually delivers, and it is the right discount for any initiative depending on new stores and new partners behaving like established ones. Two alternatives were computed and not used: the FY25 cohort ratio at 20.43% would have been far more generous, and the FY27 cohort at −5.0% would have been unusable.

| Initiative | Reach (₹ Cr p.a.) | Impact | Conf. | Effort | **Base** | **Stressed** |
|---|---|---|---|---|---|---|
| Longitudinal cohort disclosure | 7,518.40 | 0.50 | 0.95 | 10 | **357.12** | **357.12** (exempt) |
| Private label range expansion | 1,503.68 | 2.00 | 0.60 | 26 | **69.40** | **5.22** |
| **Own-Label Compact (PROPOSED)** | **1,503.68** | **1.00** | **0.45** | **30** | **22.56** | **1.70** |
| Site-quality bar on new openings | 801.81 | 1.00 | 0.80 | 30 | **21.38** | **21.38** (exempt) |

**Own-Label Compact falls from 3rd of 4 at baseline to 4th and last under stress**, behind an initiative this case study did not propose. The winner beats it by **210.36×**. `verify.py` asserts programmatically both that the proposal finishes last and that it is the **weakest stressed initiative at baseline** — the only configuration in which the demotion is genuine rather than arranged.

That is the answer, not a caveat, and here it is unusually clear-cut. MedPlus already publishes the hardest part — cohort economics. **Publishing the same cohorts across quarters instead of all cohorts at one moment costs ten person-months, needs no franchisee's agreement, and would answer the question this entire case study has to leave open.** If the FY25 cohort is climbing toward 9.3% on schedule, management's reading is right and the proposal is unnecessary. If it is not, the proposal is urgent. Either way the disclosure comes first.

---

## 48. MoSCoW

| | |
|---|---|
| **Must** | Same-cohort economics reported across quarters, not a single snapshot; private label penetration disclosed by channel; excluded-molecule list owned by pharmacy practice; substitution eligibility computed before any target is set |
| **Should** | Published wholesale tiers linked to own-label penetration; offer-and-choice recording at dispense; SDR-90 by channel and therapy area |
| **Could** | Franchisee-facing analytics showing own-label contribution per square foot; extension of the compact to COCO store manager incentives |
| **Won't** | Store-level penetration targets without an eligibility denominator; any supply condition or branded-stock penalty tied to own-label mix; selective or unpublished franchisee terms; patient-level dispensing data leaving a franchisee store |

The "Won't" row closes the four routes by which this becomes the substitution-pressure machine §40 warns about.

---

## 49. Kano

| Feature | Category | Note |
|---|---|---|
| Genuine medicine, in stock, nearby | Basic | The founding promise; absence ends the business |
| Standing discount | Performance | Just trimmed from 20% to 19% above ₹1,000 |
| Private label alternative offered at the counter | **Attractive**, for the customer who wants it | Cheaper equivalent, actively surfaced |
| Private label pushed regardless of fit | **Reverse** | The same feature, past the point of eligibility |
| Cohort economics published by vintage | **Attractive** for investors, and already delivered | Almost no retailer discloses this |

Rows three and four are the same mechanism separated only by the eligibility gate, which is why §40 puts the gate before the incentive rather than after it.

---

## 50. Feature Proposal — *Own-Label Compact*

**What it is.** A published, tiered wholesale price for franchisees, indexed to own-label penetration measured on eligible prescriptions. A franchisee whose own-label share of substitutable dispenses rises buys **everything** — branded stock included — at a better wholesale price. Tiers are published, identical for all franchisees, and applied automatically. Alongside it, MedPlus discloses private label penetration separately for company-owned and franchisee stores.

**Why this shape.** The diagnosis in §16 is that MedPlus's margin lives in a product its fastest-growing channel has no reason to sell. Training, planograms and marketing all fail here because MedPlus does not operate those stores. **The only lever that reaches an independent business owner is their own unit economics** — so the compact changes what the franchisee pays rather than what they are told, and rewards the behaviour on the input side where MedPlus already has a contractual relationship.

**What it is not.** It is not a supply condition — no franchisee is refused stock or penalised on branded supply. It is not a per-store target; the metric is a rate on eligible prescriptions, and ineligible molecules never enter the denominator. It is not a price rise to customers.

**North Star:** PLP/1k, per §31, reported separately by channel.
**Guardrail:** SDR-90, per §31, by channel and therapy area.

---

## 51. PRD

**Problem.** MedPlus's gross margin depends on private label penetration, its growth depends on franchisees, and no mechanism links the two. Private label pharma grew 2% while the company grew 21.8% and gross margin fell 160 basis points.

**Goals.** Raise own-label penetration in franchisee stores toward company-owned levels; make channel-level penetration visible; and establish substitution as a measured behaviour rather than an inferred share of revenue.

**Non-goals.** Increasing substitution beyond clinical eligibility. Raising customer prices. Accelerating store additions. Replacing the franchise model.

**User stories.**
- As a franchisee, I can see exactly what own-label penetration earns me and reach a better wholesale tier by my own choices.
- As a patient, I am offered a cheaper equivalent where one exists and can decline it without friction.
- As MedPlus's board, I can see penetration and cohort economics by channel and judge the franchise strategy on its actual margin contribution.

**Functional requirements.** Formulary-based eligibility check at dispense; pharmacy-practice-owned excluded-molecule list; offer-and-choice recording; penetration computed per store on eligible dispenses; published wholesale tier table applied automatically at ordering; channel-split penetration and cohort reporting; SDR-90 instrumentation with automatic suspension of incentives on breach.

**Non-functional.** Aggregate rates only from franchisee stores, never patient-level records; eligibility list write-access restricted to pharmacy practice, enforced by access control; tiers published and non-negotiable per franchisee.

**Acceptance criteria.** A dispense counts toward PLP/1k only if all four §31 conditions hold. No tier goes live in a therapy area before its excluded-molecule list is signed off and its SDR-90 baseline established.

**Success metrics.** PLP/1k at the R1 threshold in §54; SDR-90 no worse than baseline in any channel or therapy area measured separately; channel-split penetration published quarterly.

---

## 52. Wireframes

```
LONGITUDINAL COHORT DISCLOSURE  (the exempt initiative, built first)
+--------------------------------------------------------------+
|  Shop-level EBITDA margin, SAME cohort tracked over time      |
|                                                               |
|  Cohort      Yr1     Yr2     Yr3     Yr4                      |
|  <=FY23     x.x%    x.x%    x.x%    9.3%                      |
|  FY24       x.x%    x.x%    7.1%      -                       |
|  FY25       x.x%    1.9%      -       -                       |
|  FY26       0.7%      -       -       -                       |
|  FY27      -5.0%      -       -       -                       |
|  ----------------------------------------------------------  |
|  Read DOWN a column: are newer vintages worse at the same age?|
|  Today MedPlus publishes only the diagonal.                   |
+--------------------------------------------------------------+

FRANCHISEE ORDERING - THE PUBLISHED TIER
+--------------------------------------------------------------+
|  Your own-label penetration (eligible dispenses) ...... XX.X% |
|  Your wholesale tier .................................. Tier 2|
|  ----------------------------------------------------------  |
|  Tier 1   penetration below XX%    ...... list price          |
|  Tier 2   XX% - XX%                ...... list less X.X%      |
|  Tier 3   above XX%                ...... list less X.X%      |
|  ----------------------------------------------------------  |
|  Applies to your ENTIRE order, branded included.              |
|  No supply condition. Stock is never withheld.                |
+--------------------------------------------------------------+

COUNTER - ELIGIBILITY AND CHOICE
+--------------------------------------------------------------+
|  Prescription: [molecule]                                     |
|  Own-label equivalent ............................ AVAILABLE  |
|  Eligibility ..................................... ELIGIBLE   |
|      (excluded list owned by pharmacy practice)               |
|  ----------------------------------------------------------  |
|  Offer made:   [ own label ]   [ branded ]                    |
|  Customer chose: ______                                       |
|  ----------------------------------------------------------  |
|  Declines are recorded, not suppressed. They feed SDR-90.     |
+--------------------------------------------------------------+
```

---

## 53. Rollout Plan

**Phase 0 — three analyst-weeks on data MedPlus already holds, designed to kill the proposal cheaply.**

Compute own-label penetration on eligible dispenses, by store and by channel, across 24 months.

- **K1.** Penetration in franchisee stores is already at or near company-owned levels. If franchisees substitute just as readily, the channel-mix explanation for the margin decline is wholesale-margin arithmetic alone, the incentive gap does not exist, and the proposal is pointless.
- **K2 — named as the most likely to fire.** Franchisee stores do not run MedPlus's dispensing system at the molecule level, so eligible-versus-substituted cannot be computed for that channel at all. In that case the entire measurement layer must be built before any incentive can be designed, and the first deliverable is instrumentation, not a tier table.
- **K3.** Eligible substitutable volume is too small to move gross margin. If most of the branded 68.8% has no own-label equivalent, even perfect penetration changes little, and range development matters more than incentives.

**Phase 1 (Q3 FY27).** Longitudinal cohort disclosure published; eligibility and exclusion lists built; penetration measured by channel with no incentive attached. **Phase 2 (Q4 FY27).** Compact piloted with one franchisee cluster in one state, tiers published, SDR-90 live. **Phase 3 (FY28).** Extension only under §54's rule.

**Running in parallel and contingent on nothing above:** the longitudinal cohort disclosure that §47 ranks first. It needs ten person-months and nobody's agreement.

---

## 54. A/B Testing

| Arm | Design |
|---|---|
| A — control | Franchisee cluster on standard wholesale terms, as today |
| B — falsification arm | **Information only** — the franchisee sees their own-label penetration, their contribution per square foot, and an anonymised ranking against peers. No tier, no price change |
| C — treatment | Own-Label Compact as specified, with published tiers |

**Arm B is built to kill the thesis.** It supplies the one thing franchisees currently lack — visibility into what own-label actually earns them — without changing a single price. If B closes the penetration gap as much as C does, the problem was never incentives but information, and MedPlus should ship a dashboard rather than restructure its wholesale pricing. That is dramatically cheaper and carries none of §40's coercion risk.

**Pre-registered decision rule (R1).** Arm C proceeds to Phase 3 only if it beats Arm B by **more than 8 percentage points on PLP/1k** across two consecutive quarters, **and** SDR-90 is no worse than baseline in every therapy area measured separately, **and** the gross margin gained exceeds the wholesale discount conceded across the pilot cluster. Failing any of the three, the programme reverts to Arm B or stops.
---

## 55. KPI Dashboard

| KPI | Baseline (Q1 FY27) | Target | Early warning |
|---|---|---|---|
| **Same-cohort margin across quarters** | Not published | Published quarterly | **If the FY25 cohort is not climbing toward 9.3% on schedule, the curve is deterioration, not maturation** |
| Private label pharma growth | +2% | Above revenue growth | A second consecutive quarter below 10% |
| Franchisee share of pharmacy revenue | 5.4% | Tracked, not targeted | Rises while gross margin falls again |
| PLP/1k, by channel | Not built | R1 threshold, §54 | Franchisee channel below COCO by more than 10pp |
| SDR-90, worst therapy area | Not measured | ≤ baseline | Any therapy area worse than baseline |
| Gross margin | 24.5% | Recovering toward 26.1% | A third consecutive quarter of decline |
| Net adds vs guidance | 146 of 800 | On plan | Additions accelerate while cohort margins fall |

The first row is the discipline, and it is the cheapest item in this entire case study. MedPlus already computes cohort margins; publishing the same cohorts over time rather than all cohorts at one moment is a reporting change, not an analysis.

---

## 56. Product Roadmap

| Period | Focus |
|---|---|
| Q2 FY27 | Phase 0 analysis; longitudinal cohort series built from existing data |
| Q3 FY27 | Cohort series published; eligibility and excluded-molecule lists live; penetration measured by channel, no incentive attached |
| Q4 FY27 | Own-Label Compact piloted in one franchisee cluster; SDR-90 baselined |
| FY28 H1 | §54 decision rule evaluated; compact scaled, replaced by Arm B, or stopped |
| FY28 H2 | Site-quality bar applied to new openings — the second exempt initiative |

The proposed feature sits third deliberately, behind two initiatives requiring nobody's agreement, because that is where §47 put it.

---

## 57. Risks & Mitigation

| Risk | Mitigation |
|---|---|
| Substitution pressure beyond clinical eligibility | Excluded-molecule list owned by pharmacy practice, hard-coded into the denominator; SDR-90 with automatic suspension |
| Franchisee coercion | Tier is an incentive, never a supply condition; terms published and identical for all |
| Franchisee systems cannot measure eligibility | K2 in Phase 0 tests exactly this and is named as most likely to fire |
| Publishing longitudinal cohorts reveals deterioration | That is the point of publishing it; better found by management than by a short-seller |
| 800-store guidance pulls mix further toward franchisees | Tracked in §55; the guidance is management's, and this analysis does not assume it will be missed |
| Wholesale discount exceeds gross margin gained | Third condition of R1 in §54 tests this before any scaling |

---

## 58. Future Vision

The plausible good outcome is a chain that can state, by channel and by vintage, how much of a mature store's economics each new store delivers and how much own-label penetration each channel achieves — and that grows store count only as fast as those two numbers hold. MedPlus is closer to that than almost any Indian retailer, because it already publishes the harder half.

The bad outcome is not distress. This is a profitable, cash-generative business that just had a poor quarter and responded with visible capital discipline by shelving ₹155 Cr of non-core capex. The bad outcome is subtler: hitting 800 stores, reporting the store count as the achievement, and discovering two years later that the vintages added in the push never climbed the curve.

---

## 59. PM Lessons

1. **The best disclosure in a filing is usually the one nobody asked for.** MedPlus publishes shop-level EBITDA by cohort. That single table carries this entire case study, and most retailers would never release it.
2. **A cohort snapshot and a cohort series answer different questions.** All cohorts at one moment shows the diagonal; the same cohort over time shows whether vintages are getting worse. Only the second is decision-useful, and it is the same data.
3. **When growth moves to a channel you do not operate, your mix stops being a decision.** 89.73% of net adds were franchisees, growing 9.11× faster than company-owned stores.
4. **Find the product that pays for the strategy, then check who is incentivised to sell it.** Private label carries MedPlus's margin and grew 2%; branded pharma grew 20%. The franchisee has no reason to prefer the first.
5. **Include the number that weakens your argument.** The FY24 cohort is at 76.34% of mature margin — real maturation, in the company's own data, and the strongest case for management's reading.
6. **Distinguish a measurement failure from a strategy failure.** A blended gross margin cannot say which channel caused a 160bps decline. Fix the instrument before rebuilding the strategy — which is why the reporting change beat the designed proposal by 210×.
7. **An incentive aimed at an independent operator has to reach their P&L.** Training and planograms work in stores you run. For everyone else the only lever is what they pay.
8. **Check the registry.** Six consecutive case studies have now found an NIC code that does not describe the business.

---

## 60. PM Interview Questions

1. Revenue rose 21.8% and profit fell 21.7%. What is the first table you ask for, and what would make you relaxed about it?
2. A company publishes shop-level margin for five cohorts at one point in time. What can you conclude, and what can you not?
3. 89.73% of your store additions come through a channel you do not operate. What breaks in your reporting first?
4. Your highest-margin product grew 2% while the business grew 21.8%. List three explanations and the disclosure that separates them.
5. Design an incentive for an independent franchisee to stock your own label. Name the harm it creates and the mechanic that bounds it.
6. Your sensitivity analysis ranks a reporting change 210× above your designed feature. Do you still build the feature?
7. Management guides to 800 stores after delivering 146. Is reaffirming that guidance a good decision or a bad one, and what evidence would settle it?

---

## 61. References

**Primary**
1. MedPlus Health Services Limited, Q1 FY27 results and investor presentation, 22 July 2026.
2. MedPlus Health Services Limited, Q1 FY27 earnings call, 22 July 2026 — cohort economics, capex hold, pricing actions.
3. MedPlus Health Services Limited, Q1 FY26 earnings call — private label progression from 7.9% to 20.4% of pharma sales.
4. MedPlus Health Services Limited, exchange filings, July 2026 — drug licence suspensions, Optival Health Solutions.
5. Ministry of Corporate Affairs registry — CIN L85110TG2006PLC051845.
6. MedPlus corporate disclosures, medplusindia.com — registered office, board and subsidiary structure.

**Secondary** (corroboration; flagged where single-sourced)
7. Quartr — Q1 FY27 earnings summary, revenue, store network, segment and mix detail.
8. Business Today — Nomura note on Q1 FY27: gross profit growth, channel growth rates, overhead lines.
9. Investing.com — Q1 FY27 slide summary, cohort margins, discount and membership changes.
10. sahi.com — Q1 FY27 PAT, EBITDA margin, Q4 FY26 and FY26 comparatives.
11. TradingView / Quartr transcript summary — margin commentary and capex hold.
12. Yahoo Finance / GuruFocus — Q1 FY26 and Q1 FY27 earnings call highlights.
13. Tofler, ZaubaCorp, Tracxn, TheCompanyCheck — entity, NIC code and capital snapshots (Appendix A-4).

---

## 62. About the Author

Gaurav Singh — Product Manager. Day 69 of a 90-day public case-study series applying structured PM frameworks to real products, under a zero-fabrication standard: every figure is cited, labelled as an estimate, flagged as single-sourced, or recorded as not publicly disclosed.

---

## 63. License

Analysis and original text © 2026 Gaurav Singh, released for non-commercial use with attribution. All company figures belong to their sources and are cited in §61. No affiliation with MedPlus Health Services Limited.

---

## 64. Self Review

**What is strong.** The argument rests on figures MedPlus published voluntarily, including a cohort table most retailers never release, so the analysis is checkable rather than constructed. The three mechanisms — channel shift, margin-engine stall, cost growth — are independently disclosed and mutually consistent. The stress rule comes from the company's own cohort data. And the proposal loses to a reporting change by 210×, which is the most decisive demotion in this series so far and is asserted programmatically.

**What is weak, stated plainly.** The central claim — that the cohort curve may be deterioration rather than maturation — **cannot be settled from a snapshot, and this case study does not settle it.** The FY24 cohort at 76.34% of mature margin is real evidence for management's reading. Everything in §14 and §36 is framed as a question the disclosure cannot answer, not a conclusion, and the recommended action is the disclosure that would answer it.

**A second weakness.** The §16 seam and the §50 proposal both assume franchisee stores under-index on private label. **That is an inference from incentive structure, not a measurement** — MedPlus does not disclose penetration by channel. Management named franchisee mix as *a* cause of the gross margin decline, which supports the direction, but the size is unknown. Phase 0's K1 is built to kill the proposal if the gap does not exist.

**What I could not establish.** Private label penetration by channel; cohort economics split COCO versus franchisee; wholesale margin on franchisee sales; the reason private label pharma growth collapsed to 2%; membership subscriber counts; and the split of the 52 closures between company-owned and franchisee stores.

**One thing I would do differently.** I built the analysis around the cohort table because it is the most striking disclosure, then discovered the franchisee channel shift was the more tractable finding. The franchise seam should have led, with the cohort curve as corroboration rather than as the headline.

---

## 65. Appendix

### A. Source conflicts

| # | Conflict | Handling |
|---|---|---|
| A-1 | NIC code **8511, "hospital activities"**, for a pharmacy retail chain — a category defined as institutions with accommodation facilities | Stated in §2; CIN cited in full, never the name alone. Sixth consecutive instance in this series |
| A-2 | **Two EBITDA margins in one release** — 7.1% reported (from 8.5%) and 3.5% operating (from 4.7%), **3.60 points apart**, a difference of ₹68.35 Cr, consistent with differing lease-rent treatment | Both stated. Each used only on its own base and never mixed within a calculation. The lease-accounting explanation is inferred, not disclosed, and is labelled as such |
| A-3 | **The cohort table is a snapshot, not a series** — maturation and vintage deterioration produce identical curves and cannot be separated | Not resolved, and the case study says so in §5, §14, §36 and §64. This is the single largest limitation and drives the §47 recommendation |
| A-4 | Authorised capital reported as ₹54.18 Cr and ₹61.19 Cr, paid-up as ₹23.94 Cr, ₹23.96 Cr and ₹24.01 Cr across MCA aggregators — snapshots of different dates | 🟡 No capital figure used in any derivation; omitted from §2 rather than guessed |
| A-5 | The membership-fee uplift is reported as **"₹10–11 million"** in one source and would be immaterial at that scale; the figure is used here as **₹10.5 Cr** on the reading that the source's unit is inconsistent with an annual subscription base of this size | 🔴 **Flagged as unresolved.** Used in one derivation (D8e) which is illustrative and load-bearing nowhere. A reader should treat D8e as indicative only |
| A-6 | Gross margin decline reported as **160 bps** by the company and **163 bps** by Nomura | Both stated; 160 used throughout. The 3 bps difference affects no conclusion |
| A-7 | Q1 FY26 revenue and PAT are **back-derived** from the disclosed growth rates (₹1,543.19 Cr and ₹42.36 Cr) rather than separately reported in the sources used | Derived and flagged; every growth finding uses the reported rates directly |
| A-8 | Figures appear in both ₹ crore and ₹ million across sources (₹1,879.60 Cr = ₹18,796 mn) | ₹ crore used throughout; conversions checked |

### B. Evidence grades

🟢 **High** — MedPlus Q1 FY27 results and presentation, cohort disclosure, store network and mix data, MCA registry.
🟡 **Medium** — the lease-accounting explanation for the two EBITDA bases, capital snapshots, management's attribution of margin decline to franchisee mix.
🟠 **Low** — none relied upon.
🔴 **Conflicting** — A-3 (snapshot versus series, a structural limitation) and A-5 (the membership uplift unit), handled as above.

### C. Author-constructed content

*Own-Label Compact*, PLP/1k, SDR-90, the RICE inputs, the COCO-versus-franchisee seam in §16, the Phase 0 kill criteria and the §54 arms are the author's constructions, not MedPlus disclosures or plans. The claim that franchisee stores under-index on private label is an inference from incentive structure, not a disclosed figure. See ASSUMPTIONS.md Part 3 for the full inventory.

### D. Asset status

| Asset | Status |
|---|---|
| README.md | Complete, 65 sections |
| ASSUMPTIONS.md | Complete, Parts 1–5 |
| verify.py | 137 checks, all passing — delivered, not committed |
| LinkedIn carousel + caption | Delivered, not committed |

---

*Day 69 of 90 · [← Day 68 — Dr. Lal PathLabs](../Day-68-Dr-Lal-PathLabs) · Day 70 →*
