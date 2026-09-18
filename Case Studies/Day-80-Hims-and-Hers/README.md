# Day 80 — Hims & Hers: the AI clinical engine that has no denominator

> Hims & Hers told the market in August 2026 that it is "rebuilding the consumer health experience from the ground up with a doctor-led AI clinical engine," and that it is generating "meaningful efficiencies… from our investments in AI and technology." The 10-Q for the same quarter discloses **not one AI metric** — no adoption rate, no accuracy measure, no deflection rate, no inference cost. The only number the company attaches to AI is an input: technology and development expense of **$54.90 Mn**, up **45.06%**. And **46.33%** of that increase is depreciation, amortisation and technology costs — accounting for capex already spent — while new product development is **19.35%**. Meanwhile the efficiency claim inverts on the page it is printed: operating expenses rose from **71.48%** to **76.74%** of revenue, **5.25 points** of deleverage, and gross margin fell from **76.39%** to **63.83%**. The celebrated **38.25%** revenue growth is largely bought: **59.43%** of the $208.38 Mn increase came from Rest of the World, which the company attributes to acquisitions, against United States growth of **15.74%**. And when this company buys, it does not buy technology — of Eucalyptus's **$968.54 Mn** price, developed technology was **$56.56 Mn**, or **5.84%**, while the trade name was valued at **1.66×** the technology and goodwill at **81.60%**. Underneath all of it sits the subscription mechanism the FTC sued over on 29 July 2026, against which the company has accrued **$60 Mn** — **99.50%** of the quarter's Adjusted EBITDA. **The AI PM question: what can an AI clinical engine optimise, when the company's headline unit metric counts revenue from people the metric's own denominator excludes?**

**Author:** Gaurav Singh · **Day 80 of 90** · Written 18 September 2026
**Subject:** Hims & Hers Health, Inc. (NYSE: HIMS, CIK 0001773751), Q2 2026 Form 10-Q and the Eucalyptus acquisition of June 2026
**Verification:** `verify.py` — 151 programmatic checks, all passing

---

## 1. Cover

| | |
|---|---|
| **Product** | The Hims & Hers platform — Hims, Hers, the membership programme, MedMatch routing, Labs, and the AI-enabled clinical workflows layered on them |
| **Company** | Hims & Hers Health, Inc., San Francisco, California |
| **Domain** | Healthtech — direct-to-consumer telehealth with owned pharmacy and an AI personalisation layer |
| **Period examined** | Q2 2026 (three months ended 30 June 2026) and H1 2026, against the comparable 2025 periods |
| **Why it matters** | The largest consumer telehealth platform to stake its strategy publicly on AI while disclosing no AI metric of any kind — the clearest available test of the gap between an AI narrative and an AI product |
| **Proposed feature** | *Care Ledger* — a per-subscriber, per-condition outcome record that every AI-assisted interaction must write to, making the clinical engine measurable and auditable |
| **Series arc** | Third of 13 closing case studies on AI health products; the US telehealth counterpart to the wearables pair of Days 78–79, and the setup for Day 82's Doximity, which does disclose an AI adoption number |
| **Evidence grades** | 🟢 High · 🟡 Medium · 🟠 Low · 🔴 Conflicting |

---

## 2. Repository Metadata

**Legal entity:** Hims & Hers Health, Inc., a Delaware corporation. **SEC Central Index Key 0001773751.** Listed on the New York Stock Exchange under **HIMS**. Class A common stock, par value $0.0001, with **224,920,310** shares issued and outstanding as at 30 June 2026, alongside **8,377,623** Class V shares. Principal executive offices in San Francisco. 🟢

**Standard Industrial Classification.** The company files under **SIC 5912 — Retail-Drug Stores and Proprietary Stores.** 🟢

**The register misclassification, continued — and this time it is instructive.** The series has tracked register misclassification since Day 46 as a systemic problem rather than a failure by any individual company. Hims & Hers files as a drug store. It operates wholly-owned pharmacies, a peptide manufacturing facility, laboratory testing facilities, telehealth consultation infrastructure across seven countries, and what it describes as a doctor-led AI clinical engine. "Retail drug store" captures the fulfilment end and nothing else. The tally, which stood at **ten wrong of fifteen** after Day 79, now stands at **eleven wrong of sixteen**.

What makes this case different from the Indian NIC codes examined on Days 66–77 is that **the misclassification and the company's own metric problem have the same shape**: an entity whose economics run on subscriptions is described by the system that measures it as a seller of individual products. The register says drug store. The headline metric, as §30 shows, quietly agrees with the register — and the company discloses that it does. 🟢

**Corporate structure caution.** Clinical services are delivered by Affiliated Medical Groups, which the company explicitly states it **does not own**, because the corporate practice of medicine doctrine prohibits non-physicians from employing physicians to provide clinical services. Providers are typically engaged as independent contractors. Any claim about "doctor-led" AI must be read against this: the doctors leading it are not the company's employees, and the company's relationship with them is contractual and, by its own risk disclosure, not guaranteed to continue. 🟢

---

## 3. Badges

`Day 80/90` · `Healthtech` · `AI-enabled telehealth` · `SEC-sourced` · `65 sections` · `151 verified checks` · `0 fabricated figures` · `AI eval plan in §29 and §51` · `Runnable SQL in §32` · `Zero Mermaid — tables and ASCII only`

---

## 4. Table of Contents

<details>
<summary><b>All 65 sections</b></summary>

| Group | Sections |
|---|---|
| **Context** | [1. Cover](#1-cover) · [2. Repository Metadata](#2-repository-metadata) · [3. Badges](#3-badges) · [4. Table of Contents](#4-table-of-contents) · [5. Executive Summary](#5-executive-summary) · [6. Product Overview](#6-product-overview) · [7. Company Background](#7-company-background) · [8. Product Timeline](#8-product-timeline) · [9. Vision & Mission](#9-vision--mission) |
| **Market & Competition** | [10. Problem Statement](#10-problem-statement) · [11. Market Research](#11-market-research) · [12. Industry Analysis](#12-industry-analysis) · [13. TAM / SAM / SOM](#13-tam--sam--som) · [14. Competitor Analysis](#14-competitor-analysis) · [15. SWOT](#15-swot) · [16. Porter's Five Forces](#16-porters-five-forces) · [17. Business Model Canvas](#17-business-model-canvas) |
| **Business & Users** | [18. Revenue Model](#18-revenue-model) · [19. Target Users](#19-target-users) · [20. Personas](#20-personas) · [21. Jobs To Be Done](#21-jobs-to-be-done) · [22. User Journey](#22-user-journey) · [23. User Flow](#23-user-flow) · [24. Information Architecture](#24-information-architecture) · [25. UX Audit](#25-ux-audit) · [26. UI Audit](#26-ui-audit) · [27. Accessibility](#27-accessibility) |
| **Product, Metrics & Analytics** | [28. Feature Breakdown](#28-feature-breakdown) · [29. AI Capabilities](#29-ai-capabilities) · [30. Product Metrics](#30-product-metrics) · [31. North Star Metric](#31-north-star-metric) · [32. Product Analytics](#32-product-analytics) · [33. AARRR](#33-aarrr) · [34. HEART](#34-heart) · [35. Growth Strategy](#35-growth-strategy) · [36. Growth Loops](#36-growth-loops) · [37. Network Effects](#37-network-effects) · [38. Product Strategy](#38-product-strategy) · [39. Monetization](#39-monetization) |
| **Risk, Prioritisation & Proposal** | [40. Trust & Safety](#40-trust--safety) · [41. Technical Architecture](#41-technical-architecture) · [42. Data Flow](#42-data-flow) · [43. API Ecosystem](#43-api-ecosystem) · [44. Privacy & Security](#44-privacy--security) · [45. Pain Points](#45-pain-points) · [46. Opportunity Mapping](#46-opportunity-mapping) · [47. RICE](#47-rice) · [48. MoSCoW](#48-moscow) · [49. Kano](#49-kano) · [50. Feature Proposal — Care Ledger](#50-feature-proposal--care-ledger) · [51. PRD](#51-prd) |
| **Execution** | [52. Wireframes](#52-wireframes) · [53. Rollout Plan](#53-rollout-plan) · [54. A/B Testing](#54-ab-testing) · [55. KPI Dashboard](#55-kpi-dashboard) · [56. Product Roadmap](#56-product-roadmap) · [57. Risks & Mitigation](#57-risks--mitigation) · [58. Future Vision](#58-future-vision) |
| **Reflection & Sources** | [59. PM Lessons](#59-pm-lessons) · [60. PM Interview Questions](#60-pm-interview-questions) · [61. References](#61-references) · [62. About the Author](#62-about-the-author) · [63. License](#63-license) · [64. Self Review](#64-self-review) · [65. Appendix](#65-appendix) |

</details>

---

## 5. Executive Summary

Four findings, each computed from the Q2 2026 filings and each verified in `verify.py`.

**1. The growth is bought, and the company's own segment table says so.** Revenue grew **38.25%** to **$753.21 Mn**. Of the **$208.38 Mn** increase, **$123.84 Mn** — **59.43%** — came from Rest of the World, which the MD&A attributes to "geographic expansion from our recent acquisitions, including our acquisition of Eucalyptus, which closed in the last month of the second quarter." United States revenue, **82.56%** of the business, grew **15.74%** in the quarter and **3.20%** across the half. The gap between the headline number and the domestic number is **22.51 points**. 🟢

**2. The efficiency claim inverts on inspection.** The CFO attributed "meaningful efficiencies" to AI and technology investment. Operating expenses moved from **71.48%** of revenue to **76.74%** — **5.25 points** of deleverage. Marketing did lever down by **5.17 points**, but general and administrative deteriorated by **9.61 points** and supplied **52.04%** of the entire operating expense increase. Gross margin fell **12.56 points** to **63.83%**, costing **$94.57 Mn** of gross profit at the prior year's margin. Operating margin went from **+4.90%** to **−12.90%**. 🟢

**3. The AI line is mostly depreciation.** Technology and development — the only line the company ties to AI — rose **$17.05 Mn**, or **45.06%**. The company names the drivers: depreciation, amortisation and technology costs **$7.9 Mn**, product development **$3.3 Mn**, professional services **$3.2 Mn**, stock-based compensation **$1.4 Mn**. So **46.33%** of the "AI investment" increase is the amortised cost of things already built and bought, and **65.09%** is depreciation plus outside consultants. Employee compensation for engineering does not appear in the quarterly list at all. Marketing outspends the entire technology line by **4.78×**. 🟢

**4. The headline unit metric counts people it excludes.** Monthly Revenue per Average Subscriber rose from **$76** to **$92**, **+21.05%**. The company discloses, in the MD&A, that this metric "includes revenue contributed by customers who made one-time purchases and therefore were not considered Subscribers," and that excluding them the 2026 figure would be about **$10** lower and the 2025 figure lower by "less than $5." That is **10.87%** of the reported 2026 metric coming from outside its own denominator, against at most **6.58%** a year earlier. Correcting for it, growth falls to somewhere between **7.89%** and **15.49%** — at best **5.56 points** below the reported rate. A further **$2** of the $92 is one month of Eucalyptus. 🟢

**The synthesis.** These are not four problems. They are one. A personalisation engine can only act on people it can identify and follow — subscribers with a condition, a plan and a next step. The company's headline metric mixes those people with one-time purchasers; its growth increasingly comes from businesses acquired rather than cohorts retained; its AI spend is dominated by amortisation rather than capability; and the subscription relationship that would give the AI its denominator is the subject of a federal enforcement action. **There is a doctor-led AI clinical engine in the narrative and no clinical denominator in the disclosure.** §50 proposes the smallest object that would create one.

---

## 6. Product Overview

Hims & Hers sells access to telehealth consultations and the products that follow from them, on a subscription that auto-renews at a cadence the customer chooses — from 30 days to 360 days. Two consumer brands, **Hims** and **Hers**, address overlapping specialities: sexual health, hair loss, dermatology, mental health, and, dominantly since 2024, weight loss. Providers employed or contracted by Affiliated Medical Groups conduct consultations by video, phone or store-and-forward. Fulfilment runs increasingly through wholly-owned pharmacies, laboratory testing facilities and a peptide manufacturing facility, with the stated goal of fulfilling "a majority" of orders internally. 🟢

At the end of March 2026 the company launched a **membership programme** for US weight loss, granting access to a range of weight loss medications plus unlimited provider support. Memberships auto-renew monthly and must be active for a customer to obtain weight loss medication through a separate subscription — so a customer can hold a membership with no medication plan. 🟢

The AI layer is described but not specified: MedMatch intelligent routing, Labs biomarker tracking connected to "doctor-developed action plans," and AI-enabled workflows for diagnosis and treatment recommendation. 🟡

---

## 7. Company Background

Founded in 2017 by Andrew Dudum, who remains co-founder and CEO. Public via SPAC in January 2021. Yemi Okupe is Chief Financial Officer. 🟡

The company has been acquisitive at pace. Within thirteen months it acquired **Zava** (Germany, July 2025), **Medici Technologies**, now Hims & Hers Canada (November 2025), **YourBio Health**, a capillary blood-sampling technology company (January 2026, $153.0 Mn), and **Eucalyptus** (June 2026, $968.54 Mn). It also made a **C S Bio Co.** asset acquisition. Goodwill on the balance sheet grew **295.84%** between December 2025 and June 2026, from **$278.33 Mn** to **$1,101.72 Mn**, and now stands at **30.36%** of total assets and **3.40×** total stockholders' equity. 🟢

---

## 8. Product Timeline

| Date | Event | Grade |
|---|---|---|
| 2017 | Founded by Andrew Dudum | 🟡 |
| Jan 2021 | Public listing via SPAC, NYSE: HIMS | 🟡 |
| Oct 2023 | FTC issues Civil Investigative Demand on privacy, advertising, subscription and cancellation practices | 🟢 |
| Nov 2023 | MedMatch launched — "intelligent diagnostic services," intelligent routing | 🟡 |
| 2024–2025 | Weight loss becomes the dominant growth driver; compounded GLP-1 offerings scale | 🟢 |
| Jul 2025 | Zava acquired — Germany, UK, EU | 🟢 |
| Nov 2025 | Medici acquired — Canada | 🟢 |
| Jan 2026 | YourBio Health merger, $153.0 Mn — capillary blood sampling | 🟢 |
| Q1 2026 | **2026 US WL Announcement** — strategic shift to branded GLP-1s, compounded only "on a limited scale"; $28.5 Mn of inventory write-downs in H1 cost of revenue | 🟢 |
| Mar 2026 (end) | US weight loss membership programme launches | 🟢 |
| Jun 2026 | **Eucalyptus acquired, $968.54 Mn** — Australia, UK, Germany, Ireland, Canada, Japan | 🟢 |
| 29 Jul 2026 | **FTC, Utah DCP and Los Angeles County file suit** in N.D. Cal. under FTC Act §5 and ROSCA | 🟢 |
| Post-filing | Putative class action filed on substantially the same facts, under ECPA, CIPA and CMIA | 🟢 |
| 10 Aug 2026 | Q2 2026 results: revenue $753.21 Mn, net loss $86.29 Mn, gross margin 64% | 🟢 |

---

## 9. Vision & Mission

The company states a mission "to help the world feel great through the power of better health," and describes itself as "the leading global health and wellness platform." The CEO's Q2 2026 framing adds the strategic layer: "rebuilding the consumer health experience from the ground up with a doctor-led AI clinical engine." The 2030 targets are **at least $6.5 Bn of revenue and $1.3 Bn of Adjusted EBITDA** — a **20.00%** Adjusted EBITDA margin, against a guided **9.375%** for FY2026. That is **10.625 points** of margin the company must add in four years. 🟢

---

## 10. Problem Statement

The consumer problem is real and the company addresses it credibly: care for embarrassing, chronic or aesthetic conditions is hard to access, slow, and socially costly to seek. Telehealth plus mail-order fulfilment collapses that.

The **product** problem this case study examines is different, and it is one the filings state rather than imply. The company is building an AI clinical engine on a data substrate with three defects:

1. **The unit of measurement is contaminated.** The headline per-user metric includes revenue from non-users of the subscription (§30).
2. **The unit of relationship is contested.** The mechanism by which someone becomes and stays a subscriber — sign-up, billing, cancellation — is the subject of a federal enforcement action with a **$60 Mn** accrual (§40).
3. **The unit of outcome does not exist.** Nowhere in the 10-Q does the company report whether anyone got better. There is no disclosed clinical outcome measure, and therefore nothing for a clinical engine to be graded against.

---

## 11. Market Research

US direct-to-consumer telehealth consolidated hard through 2025–2026 around GLP-1 weight loss economics. Three structural facts drive the category, all visible in this filing:

- **Product mix moves margin violently.** Branded GLP-1s carry materially lower gross margin than compounded or generic offerings. Hims & Hers' shift, announced in Q1 2026, coincides with a **12.56 point** gross margin fall. 🟢
- **Shipping cadence moves both revenue recognition and margin.** The company states that a shift to shorter, more frequent cadences has impacted gross margins, because shipping and fulfilment costs are incurred more times per year. It expects the shift to continue. 🟢
- **Geographic expansion is being bought, not built.** Four acquisitions in thirteen months. 🟢

---

## 12. Industry Analysis

| Force | State in 2026 | Evidence |
|---|---|---|
| Supply of the core drug | Branded GLP-1 manufacturers hold pricing power; the 2026 US WL Announcement moved the company toward branded access | 🟢 |
| Regulatory posture | Sharply more active: FTC suit on subscription practices; Australian TGA investigation inherited with Eucalyptus; evolving AI rules in the US, Canada and Australia named in risk factors | 🟢 |
| Clinical labour | Constrained and contractual; providers are independent contractors of groups the company does not own | 🟢 |
| AI capability | Available to all entrants from the same third-party vendors; the company's risk factor concedes dependence on "third-party technologies and infrastructure, including AI models, cloud computing services, and processing hardware" | 🟢 |
| Consumer switching cost | Low. Subscriptions can be cancelled or snoozed between billing periods | 🟢 |

The AI PM reading: **every input to the AI clinical engine is rented, and every output is discretionary for the consumer.** Neither end of that sentence describes a moat.

---

## 13. TAM / SAM / SOM

*Author construct built on disclosed figures only; no third-party market size is asserted.* The company's own 2030 target is the cleanest available statement of its addressable ambition, so this section works backwards from it rather than forwards from an analyst estimate.

| Layer | Basis | Figure |
|---|---|---|
| **Company-stated 2030 revenue target** | Q2 2026 earnings release | **$6,500 Mn** |
| **FY2026 guidance midpoint** | $3.1–3.3 Bn range | **$3,200 Mn** |
| **Multiple required** | Target ÷ midpoint | **2.03×** |
| **Subscribers implied at current reported MRAS** | $6.5 Bn ÷ ($92 × 12) | **5,887.68 k**, or **2.04×** today's 2,891 k |
| **Subscribers implied at MRAS excluding one-time purchasers** | $6.5 Bn ÷ ($82 × 12) | **6,605.69 k** |
| **The metric's cost, in subscribers** | Difference of the two rows above | **718.01 k additional subscribers** |

That last row is the whole case study in one number. **Because the headline metric is inflated by revenue from non-subscribers, planning against it understates the subscriber base the 2030 target requires by roughly 718,000 people.** A metric definition is not a reporting detail when it sizes the hiring, the capacity and the AI's training population.

---

## 14. Competitor Analysis

| Company | Position | The AI disclosure | Grade |
|---|---|---|---|
| **Hims & Hers** | Largest US DTC telehealth by revenue; owned pharmacy; multi-country after four acquisitions | **None.** No adoption, accuracy, outcome or cost metric in the Q2 2026 10-Q | 🟢 |
| **Doximity** | Clinical network; incumbent reach into prescribers | Reports AI product adoption — "AI Scribe and DoxGPT users grew more than 50% sequentially" | 🟡 |
| **Teladoc / BetterHelp** | Virtual care and mental health at scale | Capacity-constrained; AI not the strategic frame | 🟡 |
| **Ro** | Private DTC telehealth, GLP-1-heavy | No public filings | 🟠 |
| **LifeMD** | Smaller listed DTC telehealth | Discloses financials; AI not central | 🟠 |

**The comparison that matters.** Doximity is a smaller company by revenue and it publishes a number for AI product adoption. Hims & Hers, which has made AI the centrepiece of its CEO's strategic narrative, publishes none. This is not a disclosure-regime difference — both file with the SEC. It is a choice. Day 82 takes Doximity as the mirror of this one: the company that discloses its AI adoption and shows what it costs, against the company that discloses neither.

---

## 15. SWOT

| | |
|---|---|
| **Strengths** | Brand recall and marketing machinery of genuine scale; marketing levered down **5.17 points** as a share of revenue; owned pharmacy, lab and peptide manufacturing reduce third-party dependence; **2,891 k** subscribers with a recurring billing relationship; $609.81 Mn of cash |
| **Weaknesses** | Gross margin down **12.56 points**; operating margin **−12.90%**; headline unit metric contaminated by non-subscriber revenue; no disclosed clinical outcome or AI metric; goodwill at **3.40×** equity |
| **Opportunities** | Membership programme creates a true recurring relationship distinct from product shipment; Labs and YourBio blood sampling create a longitudinal biomarker record — the raw material a clinical engine actually needs; international footprint now spans seven-plus markets |
| **Threats** | FTC and state action against the subscription mechanism itself, **$60 Mn** accrued; putative class action under ECPA, CIPA and CMIA; inherited Australian TGA advertising investigation; branded GLP-1 supplier pricing power; AI regulation named as a risk in three jurisdictions |

---

## 16. Porter's Five Forces

| Force | Intensity | Reasoning |
|---|---|---|
| **Supplier power** | **High** | Branded GLP-1 manufacturers set the price of the dominant growth category; the AI model vendors are third parties the company names as a dependency |
| **Buyer power** | **High** | Subscriptions can be cancelled or snoozed between billing periods; switching cost is a form and a shipping address |
| **Threat of substitutes** | **High** | Retail pharmacy, employer benefits, direct manufacturer programmes, and traditional primary care |
| **Threat of new entrants** | **Moderate** | Capital and regulatory barriers are real, but the AI capability is rented from the same vendors by everyone |
| **Competitive rivalry** | **High** | Marketing-led category with a Super Bowl campaign in both comparative periods |

The structural conclusion: **four of five forces are high, and the one that is not is moderate.** In that configuration the only durable advantage is a proprietary data asset that improves the product for the customer who generated it. The company has begun assembling the inputs to one — Labs, YourBio blood sampling, longitudinal subscriber history — and has not built the ledger that would turn them into an asset. That is the gap §50 addresses.

---

## 17. Business Model Canvas

| Block | Content |
|---|---|
| **Customer segments** | US consumers seeking weight loss, sexual health, hair, derm and mental health care; increasingly international consumers via acquired platforms |
| **Value proposition** | Discreet, fast, subscription access to consultation plus medication, delivered |
| **Channels** | Owned websites and mobile applications; brand marketing at national scale |
| **Customer relationships** | Recurring subscription, now layered with a membership tier; provider relationship mediated by Affiliated Medical Groups |
| **Revenue streams** | Subscription product sales; one-time purchases; membership fees; services including consultation, post-consultation support and lab results |
| **Key resources** | Brand; wholly-owned Pharmacies, Facilities and peptide manufacturing; subscriber base; accumulating biomarker data |
| **Key activities** | Marketing (**34.82%** of revenue); fulfilment; clinical operations; acquisition and integration |
| **Key partners** | Affiliated Medical Groups (not owned); Partner Pharmacies; Manufacturing Suppliers; third-party AI model and cloud vendors |
| **Cost structure** | Cost of revenue **36.17%** of revenue; marketing **34.82%**; G&A **21.96%**; operations and support **12.68%**; technology and development **7.29%** |

---

## 18. Revenue Model

Revenue is "primarily" subscription-based online sales of prescription and non-prescription products, plus services. One-time purchases are included in revenue but their purchasers are excluded from the Subscriber count — the asymmetry §30 examines.

| Line | Q2 2026 | Q2 2025 | Change |
|---|---|---|---|
| United States revenue | $621.83 Mn | $537.29 Mn | **+15.74%** |
| Rest of the World revenue | $131.38 Mn | $7.55 Mn | **+1,640.88%** |
| **Total revenue** | **$753.21 Mn** | **$544.83 Mn** | **+38.25%** |
| US share of revenue | **82.56%** | **98.61%** | **−16.06 pp** |
| Gross profit | $480.80 Mn | $416.20 Mn | +15.52% |
| **Gross margin** | **63.83%** | **76.39%** | **−12.56 pp** |

Two observations the table makes plain. First, **gross profit grew 15.52% while revenue grew 38.25%** — a **22.72 point** wedge, which is margin compression stated as a growth rate. Second, **United States revenue growth (15.74%) and gross profit growth (15.52%) are within a quarter of a point of each other.** The domestic business grew its revenue and its gross profit at the same rate; everything else in the headline is geography and mix.

Within the US, the Hers brand moved from approximately 35% to over 40% of United States revenue, driven by weight loss and dermatology. A majority of total US revenue came from **non-GLP-1** offerings in both the quarter and the half. 🟢

---

## 19. Target Users

Adults seeking treatment for conditions with a social cost to seeking it in person, and — since 2024 — adults seeking weight loss pharmacotherapy. The Hers brand's rise to over 40% of US revenue marks the centre of gravity moving toward women's weight loss and dermatology.

The population the AI must serve is narrower than the population the company reports on, and that distinction is the point: a personalisation engine can act on a **subscriber with a plan and a history**. It cannot meaningfully act on a one-time purchaser, who by construction has no next interaction to personalise.

---

## 20. Personas

*Author construct, grounded in disclosed mix and mechanics.*

**Priya, 34 — the membership subscriber.** Joined the US weight loss membership in April 2026. Holds an active membership plus a separate medication subscription. Interacts with providers repeatedly; generates labs. **This is the only persona the AI clinical engine can fully serve** — she has a condition, a plan, a history and a next appointment. Her risk is the cadence shift: shorter shipping intervals mean more billing events, more decision points at which to cancel.

**Dan, 41 — the long-cadence derm subscriber.** On a 180-day cadence for hair loss. Billed twice a year, consults rarely. High gross margin, low engagement. The AI sees him twice a year. He is in the denominator of MRAS and contributes little to its numerator per month.

**Alia, 28 — the one-time purchaser.** Bought a non-prescription product once. **She is in the MRAS numerator and not in its denominator.** She has no subscription to personalise, no plan to follow and no next interaction. She is, per the company's disclosure, roughly **$10 of the reported $92**.

**Tom, 45 — the acquired international subscriber.** Arrived via Eucalyptus in June 2026. Sits on a different platform, with a different clinical protocol, in a different regulatory regime. He is **$2 of the reported $92** and none of the US product.

---

## 21. Jobs To Be Done

| When… | I want to… | So I can… | Does the AI serve it today? |
|---|---|---|---|
| I am embarrassed to raise a condition in person | get assessed privately and quickly | start treatment without a waiting room | Partly — MedMatch routes 🟡 |
| I am on a long treatment course | know whether it is working | decide to continue, switch or stop | **No disclosed capability or metric** 🟠 |
| My labs come back | understand what they mean for my plan | act on them | Labs connects results to "doctor-developed action plans" 🟡 |
| I want to stop | cancel without friction | not be billed again | **Subject of the FTC action** 🟢 |
| I am prescribed a branded GLP-1 | afford it | stay on treatment | Membership programme addresses access, not price 🟢 |

The second row is the one that matters. **The highest-value job a doctor-led AI clinical engine could do — tell a patient on a long course whether it is working — is the job for which the company discloses neither a capability nor a measure.**

---

## 22. User Journey

```
DISCOVER        ASSESS          PRESCRIBE       FULFIL          CONTINUE        STOP
Super Bowl  ->  Online intake   Provider        Owned pharmacy  Auto-renew at   Cancel or
+ brand         questionnaire   review via      ships;          chosen cadence  snooze
marketing       -> MedMatch     Affiliated      shorter         (30-360 days)   between
34.82% of       routing         Medical Group   cadences now    + membership    billing
revenue                         (not owned)     compress margin auto-renews     periods
                                                                                  |
  ^                                                                               |
  |   Measured: traffic, conversion, subscriber count, revenue                    |
  |   Not measured (publicly): whether the condition improved -------------------+
                                                                    FTC ALLEGES THIS
                                                                    STEP IS THE PROBLEM
```

The journey has a measurement gap exactly where clinical value would be created, and a legal exposure exactly where the subscriber relationship ends.

---

## 23. User Flow

```
  Landing -> Condition selected -> Intake questionnaire -> [AI: MedMatch routing]
      -> Provider review (async, store-and-forward typical)
      -> Approved? --no--> Alternative offered / declined
             |yes
             v
      Plan + cadence selected (30/60/90/180/360-day)
      -> Payment -> Fulfilment from owned Pharmacy or Partner Pharmacy
      -> [Optional: Labs / YourBio blood draw -> biomarker record]
      -> Auto-renewal loop ------------------------------+
             |                                            |
             +--> Cancel / snooze  <-- FRICTION ALLEGED --+
```

The bracketed AI steps are the only two points where the clinical engine is publicly described as acting. Neither has a disclosed success measure.

---

## 24. Information Architecture

Brand-first (Hims / Hers), then condition, then plan. Consequence for the AI: **the architecture is organised around acquisition, not around a patient's longitudinal record.** A subscriber with three conditions across two brands has three plans and, so far as anything disclosed indicates, no single record the engine reasons over. §50's proposal is, structurally, the missing spine of this architecture.

---

## 25. UX Audit

| Area | Observation | Grade |
|---|---|---|
| Intake | Fast, well-optimised, conversion-tuned; the company states it "continuously tests and optimises the online experience" | 🟡 |
| Cadence selection | Genuinely flexible (30–360 days), but the company confirms a shift toward shorter cadences, which raises billing frequency and lowers gross margin | 🟢 |
| Membership comprehension | A customer can hold a membership with no medication plan, and must hold one to get medication — a two-object model that is easy to misread | 🟢 |
| **Cancellation** | **Alleged by the FTC, Utah DCP and Los Angeles County to violate ROSCA and FTC Act §5** | 🟢 |
| Outcome visibility | No disclosed surface where a subscriber sees whether treatment is working | 🟠 |

---

## 26. UI Audit

Assessment restricted to what is disclosed or publicly observable; no screenshots are asserted. The company describes websites and mobile applications as the sole channels, with continuous experimentation. The material UI question raised by the filings is the membership-plus-subscription two-object model and the cancellation path, both of which are now legal questions as well as design questions. 🟡

---

## 27. Accessibility

No accessibility disclosure appears in the Q2 2026 filings. For a platform whose customers include people managing chronic conditions and whose stated mission is removing barriers to care, the absence of any published accessibility standard, audit or conformance claim is a gap worth naming rather than inferring around. 🟠

---

## 28. Feature Breakdown

| Feature | What it does | Disclosed metric | Grade |
|---|---|---|---|
| Brand storefronts (Hims / Hers) | Acquisition and intake | Hers >40% of US revenue | 🟢 |
| Async provider consultation | Clinical review and prescribing | None | 🟢 |
| Subscription with variable cadence | Recurring fulfilment, 30–360 days | Cadence shortening, margin impact stated | 🟢 |
| **Membership programme (US weight loss)** | Access to a range of weight loss medications + unlimited provider support | Launched end of March 2026; no adoption figure | 🟢 |
| Owned Pharmacies and Facilities | Internal fulfilment, peptide manufacturing, labs | Goal of "a majority" of orders internal | 🟢 |
| **MedMatch** | AI intelligent routing to provider and treatment | **None** | 🟡 |
| **Labs** | Biomarker tracking connected to action plans | **None** | 🟡 |
| YourBio capillary blood sampling | At-home blood collection technology | Acquired Jan 2026, $153.0 Mn | 🟢 |

---

## 29. AI Capabilities

The section this case study exists for.

**What is disclosed, in full.** 🟢

| Item | Disclosure |
|---|---|
| Strategic framing | CEO: "rebuilding the consumer health experience from the ground up with a doctor-led AI clinical engine" |
| Claimed effect | CFO: "meaningful efficiencies we're generating from our investments in AI and technology" |
| Named products | MedMatch (routing, launched Nov 2023), Labs (biomarker tracking), unnamed "AI-enabled workflows" |
| Model vendors | **None named.** Risk factor concedes dependence on "third-party technologies and infrastructure, including AI models, cloud computing services, and processing hardware" |
| Spend | Technology and development **$54.90 Mn**, **+45.06%** — not AI-specific |
| Adoption metric | **None** |
| Accuracy or eval metric | **None** |
| Clinical outcome metric | **None** |
| Inference cost | **None** |
| Human-in-the-loop design | Not described, though providers review prescriptions |
| Risk disclosure | A full dedicated risk factor, ~600 words, covering inaccuracy, bias, regulation, talent and vendor dependence |

**The asymmetry.** The company has written approximately 600 words about how its AI might fail and published zero numbers about how it performs. That is a rational posture for a securities lawyer and an untenable one for a product organisation, because **a capability with no measure cannot be improved, prioritised against, or defended in a budget round.**

**What the spend actually bought.** The decomposition the company itself provides for the $17.05 Mn quarterly increase:

| Driver | Amount | Share of increase |
|---|---|---|
| Depreciation, amortisation and technology costs | $7.9 Mn | **46.33%** |
| Product development costs | $3.3 Mn | 19.35% |
| Professional services | $3.2 Mn | 18.77% |
| Stock-based compensation | $1.4 Mn | 8.21% |
| **Named total** | **$15.8 Mn** | **92.65%** |
| Unnamed remainder | $1.25 Mn | 7.35% |

Depreciation and outside consultants together are **65.09%** of the increase. Employee compensation for engineering appears in the six-month decomposition at **$4.4 Mn of $34.1 Mn** and does not make the quarterly list at all. **The single largest driver of the AI-and-technology investment line is the amortised cost of assets already acquired — including, from June 2026, Eucalyptus's $56.56 Mn of developed technology and $93.80 Mn trade name.** The line is going up substantially because of what the company bought, not because of what it is building.

**AI cost per interaction.** *Author construct; the company discloses no interaction count, so this is an upper bound, not an estimate.* If the **entire** technology and development line were AI — which it is not, since it also covers the digital platform, websites, mobile applications, hosting and data science — then:

| Bound | Calculation | Value |
|---|---|---|
| Technology spend per subscriber, Q2 | $54.90 Mn ÷ 2,891 k | **$18.99** |
| Per subscriber per month | ÷ 3 | **$6.33** |
| As % of reported MRAS ($92) | — | **6.88%** |
| As % of MRAS excluding one-time purchasers ($82) | — | **7.72%** |

The true AI figure is some unknown fraction of **$6.33** per subscriber-month. The point of computing the ceiling is that **it is small**: even the maximum conceivable AI cost is a rounding error against the **12.56 points** of gross margin the product mix gave away. AI is not what broke the economics, and on this evidence it is not yet fixing them either.

**The eval plan this strategy requires.** *Author construct.* A doctor-led clinical engine that routes patients to treatments needs the following before it can be called a clinical engine at all.

| Eval layer | What it measures | Method | Pass bar |
|---|---|---|---|
| **Routing appropriateness** | Does MedMatch route to the treatment a reviewing clinician would choose? | Blinded clinician adjudication on a stratified sample, by condition and brand | ≥95% agreement, published by condition |
| **Contraindication recall** | Does the engine catch the interactions and exclusions it must? | Adversarial red-flag set built from the Affiliated Medical Groups' own decline reasons | **100%** recall on the hard set; anything less halts release |
| **Escalation precision** | When the engine defers to a human, was deferral warranted? | Provider labelling of escalations | Tracked; over-escalation is a cost, under-escalation is a harm — both published |
| **Outcome attribution** | Do AI-routed subscribers reach their condition's endpoint at a rate no worse than clinician-routed? | Held-out control arm, never removed | Non-inferiority, pre-registered |
| **Cohort fairness** | Does performance hold across brand, condition, geography and acquired platform? | Stratified performance reporting | No stratum below the global bar by more than a stated margin |
| **Cost** | Inference cost per completed consultation | Routing logs | Tracked and published internally per condition |

**Failure modes, ranked by damage to this specific business.**

1. **A missed contraindication at scale.** The company does not employ the prescribing doctors, and the Affiliated Medical Group structure means liability and control are split. An AI-routing error that reaches a prescription is a clinical harm arriving through a corporate structure explicitly designed to keep the company out of clinical decisions. This is the ranked-first risk and it has no disclosed control.
2. **AI-assisted retention colliding with the FTC action.** The engine's most commercially obvious use is reducing churn. The company is being sued over how it retains subscribers. **Any AI that makes cancellation less likely is now operating inside an active enforcement perimeter**, and "the model did it" is not a defence under ROSCA.
3. **Optimising against a contaminated metric.** If MRAS is the objective, the engine learns to maximise a number that includes one-time purchasers it cannot serve. Optimising a metric whose numerator and denominator describe different populations produces confident, well-measured drift.
4. **Protocol divergence across acquired platforms.** Four platforms in thirteen months, each with its own clinical protocol and regulator. One engine reasoning across all of them without stratified evaluation will be right on average and wrong somewhere specific.
5. **Model vendor dependence.** Named as a risk by the company. Every input is rented, so every capability is replicable by a competitor renting the same input.

**Human-in-the-loop design.** *Author construct.* Three rules follow from the structure. First, **the engine may narrow but never widen** — it can present a reviewing provider with fewer options, never a treatment the provider did not already consider appropriate. Second, **no AI output may act on the cancellation or retention surface** while the FTC matter is live; that surface is legally frozen. Third, **every AI-assisted decision writes an immutable record** naming the model version, the inputs and the reviewing provider — which is precisely what §50 proposes.

---

## 30. Product Metrics

| Metric | Q2 2026 | Q2 2025 | Change | Grade |
|---|---|---|---|---|
| Revenue | $753.21 Mn | $544.83 Mn | **+38.25%** | 🟢 |
| United States revenue | $621.83 Mn | $537.29 Mn | **+15.74%** | 🟢 |
| Rest of the World revenue | $131.38 Mn | $7.55 Mn | +1,640.88% | 🟢 |
| **RoW share of the revenue increase** | — | — | **59.43%** | 🟢 derived |
| Gross margin | 63.83% | 76.39% | **−12.56 pp** | 🟢 |
| Operating margin | −12.90% | +4.90% | −17.81 pp | 🟢 |
| Net margin | −11.46% | +7.80% | −19.26 pp | 🟢 |
| Adjusted EBITDA | $60.3 Mn | $82.2 Mn | −26.64% | 🟢 |
| Adjusted EBITDA margin | 8.01% | 15.09% | −7.08 pp | 🟢 |
| Free cash flow margin | −9.05% | −12.74% | +3.68 pp | 🟢 |
| Subscribers | 2,891 k | 2,439 k | +18.53% | 🟢 |
| **MRAS, as reported** | **$92** | **$76** | **+21.05%** | 🟢 |
| **MRAS, excluding one-time purchasers** | **~$82** | **>$71** | **+7.89% to +15.49%** | 🟢 derived |
| Technology and development | $54.90 Mn | $37.85 Mn | +45.06% | 🟢 |
| **AI adoption / accuracy / outcome** | **Not disclosed** | **Not disclosed** | — | 🟠 |

### The metric problem, stated precisely

The company defines Subscribers as "customers who have one or more Subscriptions," and states plainly that "customers who have made one-time purchases are **not** considered Subscribers." It then defines Monthly Revenue per Average Subscriber as **total revenue** divided by Average Subscribers, divided by months.

Total revenue includes one-time purchases. Average Subscribers excludes one-time purchasers.

The company discloses the size of the gap:

| | Q2 2026 | Q2 2025 |
|---|---|---|
| Reported MRAS | $92 | $76 |
| Company-stated one-time contribution | ~$10 | <$5 |
| Implied subscriber-only MRAS | ~$82 | >$71 |
| **One-time share of the reported metric** | **10.87%** | **≤6.58%** |

Reported growth is **+21.05%**. On the bounds the company itself supplies, true subscriber-only growth is between **+7.89%** and **+15.49%** — **at best 5.56 points lower**, and possibly less than half the reported rate. A further **$2** of the $92 is a single month of Eucalyptus.

**Why this is a product finding and not an accounting one.** A per-user metric is a steering instrument. Teams set targets against it, experiments are judged by it, and — if the AI clinical engine is pointed at it — a model optimises it. A metric whose numerator draws on a population its denominator excludes cannot be steered by, because the two ways of moving it are opposite in kind: sell more to subscribers, or sell more one-off items to people who never subscribe. The first builds the longitudinal record a clinical engine needs. The second actively dilutes it. **The metric cannot tell the two apart, and the contamination roughly doubled year over year.**

---

## 31. North Star Metric

**Proposed: LCP/1k — Ledgered Care Progressions per 1,000 active subscriber-months.**

A subscriber-month enters the **denominator** only if the subscriber held an active subscription or membership for the whole month. One-time purchasers never enter it. It enters the **numerator** only if **all four** hold:

1. the subscriber has a **condition record** with a stated clinical endpoint — a target, a titration step, a resolution criterion;
2. a **measured progression** toward that endpoint was recorded in the month, from a lab result, a validated instrument, or a provider-confirmed observation — not from self-report alone;
3. every **AI-assisted step** that contributed to the month wrote to the ledger with its model version, inputs and reviewing provider;
4. the subscriber's **cancellation path was unobstructed** throughout the month, evidenced by the §55 guardrail.

**The denominator is the design choice.** Active subscriber-months, not customers, not revenue, not MRAS. This does three things at once. It excludes the one-time purchasers that contaminate the current headline metric. It makes the AI's contribution **countable** — condition 3 means an AI-assisted interaction that leaves no record simply does not score. And condition 4 makes the metric impossible to inflate by the mechanism the FTC is litigating, which converts a legal exposure into a product constraint the organisation can actually act on.

**Guardrail, carried to §55: CCR-90 — Cancellation Completion Rate at the 90th percentile.** Among the decile of subscriber cohorts with the **highest** retention — the cohorts a retention model would most want to touch — the share of initiated cancellations that complete within one billing cycle without an intervening offer, retention flow or provider contact. Reported by cohort and by surface, never in aggregate, because an average across easy cohorts would conceal exactly the cohorts where retention pressure is strongest.

The pairing is deliberate: **the North Star rises only when care progresses, and the guardrail falls the moment the company makes leaving harder.** Together they describe the business the company says it is building.

---

## 32. Product Analytics

*Author construct. The schema is hypothetical. Both queries are written in PostgreSQL dialect and were parsed with `sqlglot` before delivery.*

**Query 1 — decompose the reported unit metric into its two populations.** This is the query that would have surfaced the §30 finding internally, before it reached an MD&A footnote.

```sql
WITH monthly_revenue AS (
    SELECT
        date_trunc('month', o.order_date)            AS month,
        CASE
            WHEN s.subscription_id IS NOT NULL THEN 'subscriber'
            ELSE 'one_time'
        END                                          AS revenue_population,
        SUM(o.net_revenue_usd)                       AS revenue_usd
    FROM orders o
    LEFT JOIN subscriptions s
           ON s.subscription_id = o.subscription_id
          AND o.order_date BETWEEN s.started_at
                               AND COALESCE(s.ended_at, o.order_date)
    WHERE o.order_date >= DATE '2025-01-01'
    GROUP BY 1, 2
),
active_subscribers AS (
    SELECT
        date_trunc('month', d.as_of_date)            AS month,
        COUNT(DISTINCT s.customer_id)                AS subscriber_count
    FROM subscription_daily_snapshot d
    JOIN subscriptions s
      ON s.subscription_id = d.subscription_id
    WHERE d.is_active = TRUE
    GROUP BY 1
)
SELECT
    r.month,
    SUM(r.revenue_usd)                                                   AS total_revenue_usd,
    SUM(r.revenue_usd) FILTER (WHERE r.revenue_population = 'subscriber') AS subscriber_revenue_usd,
    SUM(r.revenue_usd) FILTER (WHERE r.revenue_population = 'one_time')   AS one_time_revenue_usd,
    a.subscriber_count,
    ROUND(SUM(r.revenue_usd) / NULLIF(a.subscriber_count, 0), 2)         AS mras_as_reported,
    ROUND(SUM(r.revenue_usd) FILTER (WHERE r.revenue_population = 'subscriber')
          / NULLIF(a.subscriber_count, 0), 2)                            AS mras_subscriber_only,
    ROUND(100.0 * SUM(r.revenue_usd) FILTER (WHERE r.revenue_population = 'one_time')
          / NULLIF(SUM(r.revenue_usd), 0), 2)                            AS one_time_pct_of_metric
FROM monthly_revenue r
JOIN active_subscribers a
  ON a.month = r.month
GROUP BY r.month, a.subscriber_count
ORDER BY r.month;
```

The final column is the contamination rate. Watching it move from under 6.58% to 10.87% over four quarters is the early warning the company published only as a parenthetical.

**Query 2 — the AI ledger coverage and outcome query.** This is what §50 makes possible and what nothing in the current disclosure could answer.

```sql
WITH ai_touched AS (
    SELECT
        l.subscriber_id,
        date_trunc('month', l.occurred_at)   AS month,
        l.condition_code,
        BOOL_OR(l.model_version IS NOT NULL) AS ai_assisted,
        COUNT(*)                             AS ledger_events,
        COUNT(*) FILTER (WHERE l.reviewing_provider_id IS NOT NULL)
                                             AS provider_reviewed_events
    FROM care_ledger l
    GROUP BY 1, 2, 3
),
progressions AS (
    SELECT
        p.subscriber_id,
        date_trunc('month', p.measured_at)   AS month,
        p.condition_code,
        BOOL_OR(p.progressed_toward_endpoint) AS progressed
    FROM condition_progression p
    WHERE p.measurement_source IN ('lab', 'validated_instrument', 'provider_confirmed')
    GROUP BY 1, 2, 3
)
SELECT
    a.month,
    a.condition_code,
    a.ai_assisted,
    COUNT(*)                                                       AS subscriber_months,
    ROUND(100.0 * AVG(CASE WHEN p.progressed THEN 1 ELSE 0 END), 2) AS progression_rate_pct,
    ROUND(100.0 * SUM(a.provider_reviewed_events)
          / NULLIF(SUM(a.ledger_events), 0), 2)                     AS provider_review_coverage_pct
FROM ai_touched a
LEFT JOIN progressions p
       ON p.subscriber_id  = a.subscriber_id
      AND p.month          = a.month
      AND p.condition_code = a.condition_code
GROUP BY a.month, a.condition_code, a.ai_assisted
ORDER BY a.month, a.condition_code, a.ai_assisted;
```

Split by `ai_assisted`, this is the non-inferiority test from §29's eval table, computed continuously rather than in a study.

---

## 33. AARRR

| Stage | State | Evidence |
|---|---|---|
| **Acquisition** | Strong and expensive; marketing **34.82%** of revenue, levering down **5.17 pp** | 🟢 |
| **Activation** | Optimised continuously; no disclosed activation rate | 🟡 |
| **Retention** | The company expects to retain "a significant majority" of revenue from subscribers past two years; **no retention number is disclosed**, and the mechanism is under FTC challenge | 🟢 |
| **Revenue** | MRAS $92 reported, ~$82 on subscribers only; growth mostly acquired | 🟢 |
| **Referral** | Revenue described as "highly dependent on… positive recommendations"; no referral metric | 🟢 |

The AARRR reading: **the company measures the top of the funnel precisely and the bottom of it not at all in public.** Retention — the stage where an AI clinical engine would earn its cost — is described qualitatively and litigated federally.

---

## 34. HEART

| Dimension | Signal available | Gap |
|---|---|---|
| **Happiness** | None disclosed | No NPS, CSAT or outcome satisfaction |
| **Engagement** | Subscriber count; cadence shifting shorter | No consultation or app engagement metric |
| **Adoption** | Membership launched end March 2026 | No membership adoption figure |
| **Retention** | Qualitative statement only | No cohort curve |
| **Task success** | None disclosed | **The clinical task — did treatment work — has no measure at all** |

---

## 35. Growth Strategy

Stated strategy: accelerate domestic growth, expand internationally, invest in AI and technology, and expand fulfilment in-house. Observed strategy, from the numbers: **acquire platforms in new geographies and market heavily in the US.**

The two are reconcilable only if the acquisitions are integrated into one clinical and data platform. That is what "rebuilding from the ground up with a doctor-led AI clinical engine" would have to mean operationally — one engine, one record, across Zava, Medici, YourBio and Eucalyptus. Nothing in the Q2 2026 filings describes that integration or measures it, and the Eucalyptus allocation suggests it was not what was bought (§37).

---

## 36. Growth Loops

**Loop 1 — Marketing → subscriber → recurring revenue → marketing.** Functioning, expensive, and levering down. This is the loop the company actually runs.

**Loop 2 — Subscriber → biomarker data → better routing → better outcomes → retention → more subscriber data.** This is the loop the AI narrative describes. **It cannot be verified to be running, because neither its input coverage nor its output is disclosed.** It is the loop §50 is designed to close.

**Loop 3 — Acquisition → geography → revenue → equity and cash for further acquisition.** Running hard: four acquisitions in thirteen months, **76.77%** of the Eucalyptus price deferred or contingent, and goodwill now **3.40×** equity. This loop compounds obligations rather than capability.

---

## 37. Network Effects

There are none of the classic kind — no user-to-user value, no marketplace. The only candidate is a **data network effect**: each subscriber's longitudinal record improves routing for the next subscriber with the same profile.

The Eucalyptus purchase price allocation is the clearest evidence available on whether the company is building that asset:

| Component | Amount | Share of $968.54 Mn |
|---|---|---|
| Goodwill | $790.33 Mn | **81.60%** |
| Trade name | $93.80 Mn | 9.68% |
| **Developed technology** | **$56.56 Mn** | **5.84%** |
| Customer relationships | $35.08 Mn | 3.62% |
| Other net liabilities | −$7.24 Mn | −0.75% |

**The brand was valued at 1.66× the technology. Goodwill was 13.97× the technology.** Identifiable intangibles of every kind were **19.15%** of the price. And the retention compensation for Eucalyptus's continuing employee shareholders — up to **$131.3 Mn** remaining, recognised over the service periods — is **2.32× the developed technology the deal delivered.**

Read plainly: **this was a purchase of market access and the people who hold it, not of an AI clinical engine.** Which is a defensible acquisition thesis. It is simply not the thesis the CEO's narrative describes.

---

## 38. Product Strategy

The strategy contains a genuine, unresolved tension, and naming it is the useful PM act.

- **The narrative strategy** is a proprietary, doctor-led AI clinical engine — a capability play, defensible only if it produces measurably better care.
- **The capital-allocation strategy** is brand, marketing, fulfilment and geographic acquisition — a distribution play, defensible on scale and cost.

The FY2026 spend settles which is being executed: marketing is **4.78×** technology and development. The 2030 target requires **10.625 points** of Adjusted EBITDA margin expansion, and distribution plays do not usually deliver that from a base where gross margin is falling **12.56 points**. **The margin arithmetic requires the capability strategy; the spending executes the distribution strategy.** That is the strategic gap, and it is arithmetic, not opinion.

---

## 39. Monetization

| Stream | Mechanics | Health |
|---|---|---|
| Subscription product sales | Auto-renewing, 30–360 day cadence | Core; cadence shortening compresses margin |
| Membership (US weight loss) | Monthly auto-renew, required for medication access | New; no adoption disclosed |
| One-time purchases | Non-recurring | **~10.87% of the reported unit metric** |
| Services | Consultation, post-consultation support, lab results | Bundled; not separately disclosed |

The membership programme is the most interesting monetisation move in the filing, and it is underdiscussed by the company. A membership that must be active to obtain medication creates a **true recurring relationship independent of shipment**, which is exactly the object a clinical engine needs and exactly the object MRAS fails to isolate. **The company built the right primitive and kept the wrong metric.**

---

## 40. Trust & Safety

The most consequential section of this case study, because it is where product, AI and law intersect.

**The FTC action.** On **29 July 2026**, the FTC, the Utah Division of Consumer Protection and Los Angeles County on behalf of the People of the State of California filed in the **United States District Court for the Northern District of California**, alleging violations of **Section 5 of the FTC Act** and provisions of **ROSCA** and analogous state statutes, concerning the company's **privacy, advertising, subscription and cancellation practices**. They seek a permanent injunction, unspecified monetary relief, civil penalties and other relief. The matter began as a Civil Investigative Demand in **October 2023**; settlement negotiations failed. 🟢

**The accrual, in context:**

| Comparison | Value |
|---|---|
| Accrued as at 30 June 2026 | **$60 Mn** |
| As % of Q2 2026 Adjusted EBITDA ($60.3 Mn) | **99.50%** |
| As % of Q2 2026 revenue | 7.97% |
| As multiple of Q2 technology and development spend | **1.09×** |
| Legal contingencies added back in Q2 Adjusted EBITDA | $47.5 Mn, **6.31%** of revenue |

**The company has accrued more against the way it retains subscribers than it spent building technology in the quarter.**

**The follow-on class action.** A putative class action was filed in the same court on substantially the same facts, asserting claims under the **Electronic Communications Privacy Act**, the **California Invasion of Privacy Act**, the **California Confidentiality of Medical Information Act** and other state theories, on behalf of a nationwide class and a California subclass. 🟢

**The inherited matter.** Between September 2023 and August 2025 the Australian **Therapeutic Goods Administration** issued compulsory notices to Eucalyptus subsidiaries investigating alleged non-compliance with advertising laws governing online advertising of prescription medicines. The company is indemnified by certain warrantors. 🟢

**The product consequence.** Three live matters — US subscription practice, US health-data privacy, Australian prescription advertising — all concern **how the company acquires and retains subscribers, and how it handles their health data.** Those are precisely the surfaces an AI clinical engine would touch. §29's second-ranked failure mode follows directly: **the most commercially attractive use of the engine is the use that is currently under federal challenge.** That is not a compliance footnote; it is a binding constraint on the product roadmap, and §50 is built to respect it.

---

## 41. Technical Architecture

Disclosed at a high level only: websites and mobile applications; wholly-owned Pharmacies, laboratory testing facilities and a peptide manufacturing facility; third-party cloud and AI model infrastructure; four acquired platforms operating in seven-plus countries. 🟢 / 🟡

The architectural fact that matters for the AI thesis is stated in a risk factor rather than a strategy slide: the company depends on "third-party technologies and infrastructure, including AI models, cloud computing services, and processing hardware." **There is no disclosed owned model, no disclosed fine-tune, and no disclosed proprietary clinical training corpus.** 🟢

---

## 42. Data Flow

```
   INTAKE                 CLINICAL                FULFILMENT           LONGITUDINAL
   questionnaire   ->     Affiliated Medical  ->  owned Pharmacy  ->   Labs / YourBio
   + MedMatch             Group provider          or Partner           biomarker record
   routing                (not employed by         Pharmacy                 |
       |                   the company)                                    |
       |                        |                                          |
       v                        v                                          v
   [third-party AI models, cloud, processing hardware - all rented]        |
       |                                                                   |
       +---------------> NO DISCLOSED UNIFIED RECORD <---------------------+
                                  |
                        NO DISCLOSED OUTCOME MEASURE
                                  |
                  4 acquired platforms, 7+ countries, separate protocols
```

The diagram's centre is empty, and that emptiness is the case study. Every ingredient of a clinical data asset is present. The ledger that would join them is not disclosed to exist.

---

## 43. API Ecosystem

No public API, developer programme or partner integration surface is disclosed. For a company describing a platform strategy across seven-plus countries and four acquired technology stacks, the absence of any disclosed internal or external interface layer is itself the integration risk: four platforms with no stated common contract. 🟠

---

## 44. Privacy & Security

The company collects and transmits healthcare information "which may be assisted by artificial intelligence tools in certain instances," and states that if data or AI-aided suggestions "are incorrect or incomplete… we could be subject to claims of liability." It names HIPAA plus federal, state and foreign regimes, and flags evolving AI-specific regulation in the **United States, Canada and Australia** by name. 🟢

The privacy exposure is not hypothetical: the FTC complaint covers privacy practices, and the follow-on class action pleads ECPA, CIPA and CMIA. **A company litigating health-data privacy while expanding AI processing of health data is carrying two risks that compound rather than add.**

---

## 45. Pain Points

| # | Pain point | Evidence | Severity |
|---|---|---|---|
| 1 | Headline unit metric mixes populations; contamination up from ≤6.58% to 10.87% | 10-Q MD&A 🟢 | **Critical** |
| 2 | No clinical outcome measure of any kind | Absence across 10-Q 🟢 | **Critical** |
| 3 | No AI adoption, accuracy or cost metric | Absence across 10-Q 🟢 | **Critical** |
| 4 | Subscription and cancellation mechanism under federal challenge, $60 Mn accrued | 10-Q contingencies 🟢 | **Critical** |
| 5 | Gross margin −12.56 pp on product mix and cadence | 10-Q 🟢 | High |
| 6 | Operating deleverage of 5.25 pp against a stated efficiency claim | 10-Q 🟢 | High |
| 7 | Growth 59.43% acquired; US growth 3.20% across the half | 10-Q 🟢 | High |
| 8 | Four platforms, no disclosed unified record or protocol | 10-Q 🟡 | High |
| 9 | AI spend increase 46.33% depreciation and amortisation | 10-Q MD&A 🟢 | Medium |
| 10 | Goodwill 3.40× equity | 10-Q 🟢 | Medium |

---

## 46. Opportunity Mapping

| Opportunity | Pain addressed | Requires cooperation from | Reversible? |
|---|---|---|---|
| **Split the reported metric** into subscriber revenue and one-time revenue | 1 | **No one — internal definition change** | Yes |
| **Remediate the cancellation flow** ahead of the court | 4 | Legal, and ultimately the court | Yes |
| **Instrument every AI interaction** with model version, inputs and reviewer | 3 | Engineering only | Yes |
| **Care Ledger** — a per-subscriber, per-condition outcome record | 2, 3, 8 | Affiliated Medical Groups, labs, four acquired platforms, regulators | Partially |
| Own the inference layer | 9 | Vendors, capital | Partially |

The column that decides the ordering is the third. **Three of these require no one's cooperation. The proposal requires four parties the company does not control, one of which it is explicitly prohibited from controlling.**

---

## 47. RICE

Scores computed and asserted in `verify.py`. Reach is in thousands of subscribers per quarter. The **stress multiplier is the company's own evidenced dependency**: the share of Q2 revenue growth that came from the existing product rather than from acquisition — **40.57%**. Initiatives whose reach does not depend on the existing product's clinical apparatus are exempt from the stress rule, and the exemption is declared in ASSUMPTIONS Part 3.

| Initiative | Reach (k) | Impact | Confidence | Effort (pm) | Stressed | **RICE** |
|---|---|---|---|---|---|---|
| **Subscriber-only revenue metric split** | 2,891 | 2.0 | 0.95 | 2 | No | **2,746.45** |
| **Cancellation flow remediation** | 2,891 | 1.5 | 0.90 | 6 | No | **650.48** |
| **AI interaction logging and eval harness** | 2,891 | 1.5 | 0.80 | 8 | No | **433.65** |
| **Care Ledger (the proposal)** | 2,891 → 1,173 | 2.5 | 0.60 | 18 | **Yes** | **97.74** |

**The proposal ranks last, by 28.10×, and this is the correct answer.**

The house rule of this series is that the proposal must finish last under stress, and the reason it holds here is unusually clean. Care Ledger is the right long-term object — it is the only initiative that creates the denominator the AI strategy is missing. But it requires the Affiliated Medical Groups, which the company is legally barred from owning; the acquired platforms, which were bought three months ago; the labs; and regulators in three jurisdictions.

**A company whose metric is contaminated, whose retention mechanism is being litigated, and whose AI leaves no trace should first do the three things that require no one's permission.** Split the metric. Fix the cancellation flow. Instrument the model. Each is cheap, each is reversible, and each is a precondition of the ledger working at all — you cannot build a clinical outcome record on a population you have not yet defined, through a subscription mechanism a court may enjoin, with a model that logs nothing.

The stress test is not an argument against the proposal. It is the sequencing argument for it.

---

## 48. MoSCoW

| Priority | Items |
|---|---|
| **Must** | Split MRAS into subscriber and one-time revenue, and restate the prior year; instrument every AI-assisted interaction with model version, inputs and reviewing provider; remediate the cancellation flow |
| **Should** | Publish membership adoption; publish a cohort retention curve; stratified AI performance reporting by condition and platform |
| **Could** | Care Ledger pilot in one condition and one geography; inference cost reporting per completed consultation |
| **Won't (this cycle)** | Owning the model layer; cross-platform protocol unification; any AI applied to the retention or cancellation surface while the FTC matter is live |

The final "Won't" is not a resourcing decision. It is a legal perimeter, and writing it into the roadmap is how a product organisation makes a constraint visible rather than discovering it in discovery.

---

## 49. Kano

| Feature | Category | Note |
|---|---|---|
| Discreet, fast access to prescription | **Must-be** | Table stakes; absence is fatal, presence delights no one |
| Flexible cadence | **Performance** | More flexibility, more satisfaction — and lower gross margin |
| Frictionless cancellation | **Must-be** | Currently a legal liability rather than a feature |
| Biomarker tracking connected to a plan | **Attractive** | Present but unmeasured |
| **Being told whether your treatment is working** | **Attractive → Must-be** | Nobody offers it, so it delights today; the moment one competitor ships it, it becomes table stakes for all |
| AI routing | **Indifferent** | Invisible to the user; matters only through its outcome |

The last row is the strategic one. **AI routing is Kano-indifferent by itself.** Users do not want AI; they want to know the treatment is working. An AI investment that never surfaces as an outcome the user can see is an investment in an indifferent attribute — which is precisely how a company ends up spending 45% more on technology and reporting no change anyone can point to.

---

## 50. Feature Proposal — *Care Ledger*

**One line.** A per-subscriber, per-condition, append-only clinical record that every AI-assisted interaction must write to, with the model version, the inputs, the reviewing provider and the measured progression — so that the clinical engine has, for the first time, a denominator.

**The problem it solves.** The company has assembled every input of a clinical data asset — subscribers, providers, labs, YourBio blood sampling, four platforms of longitudinal history — and has no disclosed object that joins them into a record a model can be graded against. Without that record: MRAS cannot be corrected (§30), AI contribution cannot be measured (§29), outcomes cannot be reported (§34), and the 2030 margin target has no mechanism behind it (§38).

**What it is, concretely.**

| Element | Specification |
|---|---|
| **Grain** | One row per subscriber, per condition, per clinical event |
| **Written by** | Every intake, routing decision, provider review, fulfilment, lab result and progression measurement |
| **Mandatory fields on AI-assisted rows** | `model_version`, `input_hash`, `recommendation`, `reviewing_provider_id`, `provider_accepted` (boolean), `deviation_reason` |
| **Progression field** | `progressed_toward_endpoint`, sourced only from lab, validated instrument or provider confirmation — never self-report alone |
| **Immutability** | Append-only; corrections are new rows referencing the superseded row |
| **Access** | The subscriber can read their own ledger in full, in plain language — this is the user-facing surface that turns a Kano-indifferent capability into an attractive one |
| **Boundary** | The ledger is **read-only to any retention, pricing or cancellation surface.** It may never be used to decide whether to make leaving harder |

**Why the boundary is in the spec and not the policy document.** §40 establishes that the company's retention mechanism is the subject of a federal enforcement action. A clinical record that could be read by a retention system is a clinical record that will eventually be read by a retention system. Encoding the prohibition as a schema-level access boundary — not a guideline — is what makes the ledger defensible in front of the court that is currently examining this company's subscription practices.

**What it changes, measurably.** LCP/1k (§31) becomes computable. §32's Query 2 becomes runnable. §29's non-inferiority test runs continuously rather than as a study. The MRAS split (§30) becomes structural rather than a footnote. And the subscriber sees, for the first time, whether the thing they are paying for is working.

**Why it ranks last, and should.** See §47. It requires the Affiliated Medical Groups the company cannot own, four platforms acquired within thirteen months, the labs, and regulators in three jurisdictions. The three initiatives that outrank it are its preconditions. **The correct roadmap is not "build the ledger." It is "earn the right to build the ledger, in that order."**

---

## 51. PRD

**Title:** Care Ledger v1 — single condition, single geography pilot
**Owner:** Product, Clinical Data Platform
**Status:** Proposal

**Problem.** The company has no unified, per-subscriber clinical record. Consequently no AI capability can be evaluated, no clinical outcome can be reported, and the headline unit metric cannot be corrected.

**Goal.** Establish a ledger for one condition in one geography such that, within two quarters, **LCP/1k** is computable and the AI non-inferiority test from §29 runs continuously.

**Non-goals.** Cross-platform unification. Model ownership. Any application to retention, pricing or cancellation — explicitly out of scope and blocked at the schema level.

**Scope — v1.**
1. Ledger schema, append-only, as specified in §50.
2. Write-path instrumentation for intake, routing, provider review, fulfilment and lab result.
3. Mandatory AI fields enforced at write time; an AI-assisted interaction that cannot write is an interaction that must not proceed.
4. Held-out control arm: a fixed share of subscribers routed without AI assistance, never removed.
5. Subscriber-facing plain-language ledger view.
6. Schema-level access control excluding retention, pricing and cancellation systems.

**Success criteria.**

| Criterion | Bar |
|---|---|
| Write coverage of AI-assisted interactions | **100%** — enforced, not measured |
| Provider review coverage of AI-assisted clinical decisions | 100% |
| Progression measurements from qualifying sources | ≥80% of active subscriber-months in the pilot condition |
| AI-routed vs control progression | Non-inferiority, pre-registered before launch |
| Contraindication recall on the adversarial set | **100%**; below this, release halts |
| Retention-surface reads of the ledger | **Zero.** Any non-zero value is a P0 incident |

**Eval plan.** As §29's six-layer table, run against the pilot condition, with results reported to the Affiliated Medical Group's clinical leadership monthly and stratified by cohort.

**Dependencies.** Affiliated Medical Group participation agreement; lab result ingestion; legal sign-off given the live FTC matter; pilot-geography regulatory review.

**Risks.** Provider adoption is the binding constraint — providers are independent contractors who can work on competitors' platforms and cannot be compelled. Mitigation: the ledger must reduce provider work at first contact, not add to it, or it will not be used.

---

## 52. Wireframes

*ASCII, illustrative.*

**Subscriber-facing ledger view — the surface that makes the AI visible as an outcome**

```
+--------------------------------------------------------------+
|  Your care record                          Hers · Weight loss |
+--------------------------------------------------------------+
|  Goal set with Dr. M. on 12 Apr 2026                          |
|  Endpoint: sustained titration to target dose                  |
|                                                                |
|  PROGRESS          [####################------]  4 of 5 steps  |
|                                                                |
|  This month                                                    |
|   * 02 Jun  Lab result received ............... on track       |
|   * 11 Jun  Dose step reviewed by Dr. M. ...... approved       |
|              (suggested by care engine v4.2 - reviewed)        |
|   * 24 Jun  Shipment sent                                      |
|                                                                |
|  What the care engine suggested, and what your doctor decided  |
|   +--------------------------------------------------------+  |
|   | Suggested: advance to next dose step                   |  |
|   | Dr. M.: approved, with a 2-week check-in               |  |
|   | [ See all 7 suggestions and decisions ]                |  |
|   +--------------------------------------------------------+  |
|                                                                |
|  [ Download my record ]        [ Manage or cancel my plan ]    |
+--------------------------------------------------------------+
```

The cancel affordance sits on the same screen, at the same weight, with no intervening flow. That placement is a legal position as much as a design one.

**Internal — AI decision audit row**

```
+------------------------------------------------------------------+
| ledger_event 8842193       subscriber 44219    condition WL-01    |
|------------------------------------------------------------------|
| model_version      care-routing-4.2                               |
| input_hash         a91f...c30                                     |
| recommendation     advance_dose_step_3                            |
| reviewing_provider PRV-1182 (Affiliated Medical Group - West)     |
| provider_accepted  TRUE                                           |
| deviation_reason   -                                              |
| control_arm        FALSE                                          |
| retention_read     BLOCKED BY SCHEMA POLICY                       |
+------------------------------------------------------------------+
```

---

## 53. Rollout Plan

| Phase | Duration | Content | Gate to proceed |
|---|---|---|---|
| **0 — Preconditions** | Weeks 1–6 | Metric split shipped; AI interaction logging live; cancellation remediation filed with legal | All three complete; none is optional |
| **1 — Schema and write path** | Weeks 7–14 | Ledger schema; write-path instrumentation; enforcement that AI cannot proceed without writing | 100% write coverage in staging |
| **2 — Shadow** | Weeks 15–22 | Ledger written, nothing surfaced; control arm established; eval harness running | Non-inferiority test executes end to end |
| **3 — Provider surface** | Weeks 23–30 | Ledger visible to reviewing providers; measured for time saved at first contact | Provider time-to-review does not increase |
| **4 — Subscriber surface** | Weeks 31–38 | Plain-language ledger view; cancel affordance co-located | Zero retention-surface reads; cancellation completion unchanged or better |
| **5 — Second condition** | Weeks 39+ | Extend to a second condition in the same geography | Phase 4 bars held for two consecutive months |

Cross-platform extension to Zava, Medici and Eucalyptus is deliberately absent. Four platforms acquired in thirteen months is not a foundation to build a clinical record on; it is a reason to prove the record in one place first.

---

## 54. A/B Testing

| Test | Arms | Primary metric | Guardrail | Decision rule |
|---|---|---|---|---|
| **Ledger visibility to subscribers** | Ledger view vs current | LCP/1k | CCR-90 must not fall | Ship only if LCP/1k rises and CCR-90 holds |
| **AI routing vs clinician routing** | AI-assisted vs held-out control | Condition progression rate | Contraindication recall 100% | **Non-inferiority, pre-registered.** Never superiority-only |
| **Provider ledger surface** | Ledger at review vs current | Time to review | Provider acceptance rate of AI suggestions must not rise artificially | Ship if time falls and acceptance is stable |
| **Cancel affordance placement** | Co-located vs current | Cancellation completion rate | — | **Ship if completion rises.** This is the only test in the series where the "worse" business outcome is the required one |

The last row deserves its note. A test that increases cancellation completion would fail an ordinary growth review. Under an active ROSCA action, it is the test the company most needs to run and be seen to have run.

---

## 55. KPI Dashboard

| Tier | Metric | Source | Cadence |
|---|---|---|---|
| **North Star** | **LCP/1k** — Ledgered Care Progressions per 1,000 active subscriber-months | Care Ledger | Monthly |
| **Guardrail** | **CCR-90** — Cancellation Completion Rate, top retention decile | Billing + cancellation logs | Weekly |
| Metric integrity | One-time revenue as % of reported per-user metric (**10.87%** today) | Revenue system | Monthly |
| AI | Write coverage of AI-assisted interactions | Ledger | Daily |
| AI | Contraindication recall on adversarial set | Eval harness | Per release |
| AI | AI-routed vs control progression gap | Ledger | Monthly |
| AI | Inference cost per completed consultation | Routing logs | Monthly |
| Business | Gross margin, by condition and geography | Finance | Quarterly |
| Business | Operating expense ratio (**76.74%** today) | Finance | Quarterly |
| Business | US organic revenue growth, excluding acquisitions (**15.74%** in Q2) | Finance | Quarterly |

The third row is the one a growth-stage company would not think to put on a dashboard, and the one this company most needs there. **Metric integrity is a KPI.**

---

## 56. Product Roadmap

| Horizon | Focus | Why here |
|---|---|---|
| **Now (0–2 quarters)** | Metric split and restatement; AI interaction logging; cancellation remediation | Highest RICE; require no external cooperation; preconditions for everything else |
| **Next (2–4 quarters)** | Care Ledger phases 1–3, one condition, one geography; publish membership adoption and a cohort retention curve | Builds the denominator; makes AI measurable |
| **Later (4–8 quarters)** | Second condition; subscriber-facing ledger; inference cost reporting; stratified AI performance by platform | Compounds only once phase 4 bars hold |
| **Not yet** | Cross-platform unification; model ownership; any AI on the retention surface | Legal perimeter and integration risk |

---

## 57. Risks & Mitigation

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| FTC action results in injunctive relief reshaping the subscription flow | High | High | Remediate ahead of the court; make cancellation completion a published KPI |
| A missed contraindication reaches a prescription | Medium | **Severe** | 100% recall gate on the adversarial set; release halts below it; engine may narrow, never widen |
| AI applied to retention, deliberately or by drift | Medium | **Severe** | Schema-level access exclusion; any read is a P0 incident |
| Metric restatement damages market credibility | Medium | Medium | Restate proactively with the prior year, before an analyst does it |
| Provider non-adoption of the ledger | High | High | Ledger must reduce review time at first contact; providers are contractors and cannot be compelled |
| Integration failure across four platforms | High | Medium | Deliberately deferred; prove in one geography first |
| Goodwill impairment (goodwill at 3.40× equity) | Medium | High | Outside product control; noted for completeness |
| Branded GLP-1 supplier pricing | High | High | Mix diversification; a majority of US revenue is already non-GLP-1 |

---

## 58. Future Vision

The plausible good outcome is specific. Hims & Hers has, uniquely among consumer telehealth companies, assembled owned pharmacy, owned labs, at-home blood sampling technology, a large recurring subscriber base and a membership primitive that decouples the relationship from the shipment. **Nobody else in DTC telehealth has all five.** A clinical record built on top of them, with an AI graded against measured progression, would be a genuine data asset — the only one available in this category.

The plausible bad outcome is equally specific, and it is the default path: the AI narrative continues, the technology line keeps rising on amortisation of acquired intangibles, the metric keeps drifting, the court reshapes the subscription flow, and the 2030 margin target meets a business that grew by purchase rather than by capability.

The distance between those two outcomes is not a technology gap. **It is a measurement gap, and measurement gaps are the cheapest gaps in product management to close.**

---

## 59. PM Lessons

1. **A metric that mixes populations cannot steer a product, and it certainly cannot steer a model.** Numerator and denominator must describe the same people. Check this on the metrics you inherited, not just the ones you designed.
2. **When a company narrates a capability and discloses only its cost, read the cost decomposition.** Here, 46.33% of the "AI investment" increase was depreciation. The decomposition is where the narrative meets the ledger.
3. **Growth rates hide their own composition.** 38.25% and 15.74% are the same quarter. Always ask which segment supplied the increase, not just what the increase was.
4. **Purchase price allocation is a strategy document.** A company that pays 81.60% goodwill and values the brand at 1.66× the technology has told you what it thinks it is buying, whatever the press release says.
5. **A legal exposure can be a product constraint you can act on.** The FTC matter converts "don't use AI for retention" from an ethics slide into a schema-level access rule with a P0 incident attached.
6. **The right proposal can still be the wrong next move.** Sequencing is a PM deliverable. Ranking your own proposal last, honestly, is more useful than defending it.

---

## 60. PM Interview Questions

1. Hims & Hers reports Monthly Revenue per Average Subscriber of $92, and discloses that roughly $10 of it comes from customers who are not subscribers. You are the PM who owns this metric. What do you ship first, and what do you tell the exec who has been reporting the $92 for four quarters?
2. Revenue grew 38.25%; the US business grew 15.74%. Which number goes in the board deck, and how do you present the other one?
3. The CEO says the company is building a doctor-led AI clinical engine. There is no AI metric in the 10-Q. What are the first three metrics you instrument, and in what order?
4. The company is being sued over its cancellation flow. Your AI team proposes a churn-prediction model to trigger retention offers. Write the two-sentence answer you give them.
5. Eucalyptus cost $968.54 Mn, of which developed technology was $56.56 Mn. Argue both sides: is this consistent with an AI strategy?
6. Design a non-inferiority test for AI-assisted clinical routing. What is your control arm, and why must it never be removed?
7. The company must add 10.625 points of Adjusted EBITDA margin by 2030 while gross margin is falling 12.56 points. Where does the margin come from, and what would you need to believe?

---

## 61. References

**Primary sources**

1. Hims & Hers Health, Inc., **Form 10-Q** for the quarterly period ended 30 June 2026, filed 10 August 2026, accession 0001773751-26-000163. *(Income statement, segment revenue, MD&A, Note 3 Acquisitions, contingencies, risk factors.)* 🟢
2. Hims & Hers Health, Inc., **Exhibit 99.1 to Form 8-K** filed 10 August 2026, accession 0001773751-26-000161 — "Hims & Hers Health, Inc. Reports Second Quarter 2026 Financial Results." *(Key business metrics, guidance, CEO and CFO statements, balance sheet, Adjusted EBITDA reconciliation.)* 🟢
3. Hims & Hers Health, Inc., **Form 10-K** for the fiscal year ended 31 December 2025, filed 23 February 2026, accession 0001773751-26-000022. 🟢
4. SEC EDGAR submissions index, CIK 0001773751. 🟢

**Secondary sources**

5. Nasdaq, "Hims & Hers Expands Data-Driven, AI-Enabled Care and Personalization." *(MedMatch and Labs description; Doximity AI adoption comparison.)* 🟡
6. BusinessWire, "Hims & Hers Introduces MedMatch: The Next Generation of Intelligent Diagnostic Services," 6 November 2023. 🟡
7. Pulse 2, "Hims & Hers International Revenue Grows More Than 17-Fold As It Builds Doctor-Led AI Clinical Engine." 🟡

---

## 62. About the Author

**Gaurav Singh** — Product Manager, New Delhi. Writing a 90-day series of evidence-based product management case studies on real products, published daily to GitHub and LinkedIn. Background in yoga therapy and behavioural science. Every figure in this case study is computed from primary sources and verified programmatically before publication.

Repository: `github.com/gaurav-product/product-management-case-studies`

---

## 63. License

This case study is published for educational and portfolio purposes. All financial figures are drawn from public SEC filings. Company names, trademarks and product names are the property of their respective owners. No affiliation with Hims & Hers Health, Inc. is claimed or implied. Analysis, proposals, metric designs and constructs are the author's own and are labelled as such in ASSUMPTIONS.md.

---

## 64. Self Review

**Rating: 9.0 / 10.**

**What this case study does well.** The central finding — that the headline unit metric draws its numerator from a population its denominator excludes, and that the contamination roughly doubled year over year — is taken from the company's own MD&A parenthetical and turned into a product argument with a quantified consequence (718,010 additional subscribers required for the 2030 target). The AI spend decomposition is the sharpest evidence in the piece: 46.33% depreciation is a fact the company published and nobody framed. The Eucalyptus allocation, read as a strategy document, is the second. And §47's stress test produces a genuinely useful sequencing argument rather than a ritual one.

**What is weaker.** The user-facing sections — §25, §26, §27 — remain thin, because the underlying research reads filings rather than users. This is the standing critique of the series and it is not yet fixed. Personas in §20 are constructs derived from disclosed mix, not from interviews. The AI cost-per-interaction figure in §29 is an upper bound on a line that is not AI-specific, and it is labelled as such but it is still the least satisfying number in the piece.

**What would make it a 10.** Primary evidence from subscribers on the cancellation flow, and a read of the actual FTC complaint rather than the company's characterisation of it in its own 10-Q. Both were out of reach this session and both are named in ASSUMPTIONS Part 5.

---

## 65. Appendix

### A. Source conflicts

No material numerical conflict was found. All financial figures in this case study come from two documents filed on the same day by the same registrant, and they agree.

| Item | Form 10-Q | Press release | Resolution |
|---|---|---|---|
| Gross margin, Q2 2026 | 63.83% computed from $480,803 / $753,214 | "64%" as stated | The press release rounds. This case study uses the computed figure and says so. |
| Revenue growth, Q2 | 38.25% computed | "38%" as stated | Rounding only. |
| Subscriber growth | 18.53% computed from 2,891 / 2,439 | "19%" as stated | Rounding only. |
| Adjusted EBITDA, Q2 2026 | — | "$60.3 million" | Stated to $0.1 Mn; ratios using it inherit that precision and are noted in ASSUMPTIONS Part 2. |

### B. Bounded figures carried as bounds, never sharpened

| Figure | Company language | Treatment here |
|---|---|---|
| 2025 one-time contribution to MRAS | "lower by less than $5" | Carried as an **upper bound**. Adjusted 2025 MRAS is stated as a range, >$71, and the resulting growth rate as a range, 7.89%–15.49%. Never point-estimated. |
| 2026 one-time contribution to MRAS | "lower by approximately $10" | Carried as approximate; the 10.87% share is computed from it and labelled derived. |
| Eucalyptus revenue contribution | "approximately 5%" of Q2 consolidated revenue | Not used to derive any figure; cited as disclosed. |
| FTC accrual | "approximately $60 million" | Ratios using it are stated to two decimals but inherit an approximate input, noted in ASSUMPTIONS Part 2. |

### C. The register tally, Days 46–80

| | |
|---|---|
| Companies examined for register classification | **16** |
| Classifications that do not describe the business | **11** |
| Current rate | **68.75%** |
| This entry | Hims & Hers files under SIC 5912, Retail-Drug Stores — wrong |

### D. Figures computed but not used in prose

`verify.py` computes 151 values. Those not asserted in this README are retained in the gate so that any future revision has them available and pre-checked, and so that `crosscheck.py` can confirm no prose figure exists outside the gate.

---

*Day 80 of 90. Verified with `verify.py` — 151 checks, all passing. Next: Day 81, Hinge Health — AI care delivery that is actually working, and what that costs.*
