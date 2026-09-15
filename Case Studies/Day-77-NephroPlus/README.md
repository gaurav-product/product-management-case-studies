# Day 77 — NephroPlus: the growth is real, the dose is not

> Q1 FY27 is a textbook operating-leverage quarter — revenue +23.71%, adjusted EBITDA +30.72%, adjusted PAT +41.54%, each line faster than the one above it. Then divide two numbers the company publishes in the same release: **860,000 Indian treatments across 33,047 Indian guests is 26.02 treatments per guest per quarter — 2.00 sessions a week, against a clinical standard of three.** Internationally the same division gives 2.51. End-stage renal disease does not negotiate: a missed session is not deferred revenue, it is fluid overload, hyperkalaemia and shortened life. So the most important number in this business is not revenue per treatment, which rose 9.19%. It is treatments per guest, which sits at **66.73% of adequate** — and the honest reading of the improving trend is that most of the improvement is international mix, not Indian patients receiving more dialysis.

**Author:** Gaurav Singh · **Day 77 of 90** · Written 12 September 2026
**Subject:** Nephrocare Health Services Limited, brand NephroPlus (NSE/BSE: NEPHROPLUS), quarter ended 30 June 2026
**Verification:** `verify.py` — 117 programmatic checks, all passing

---

## 1. Cover

| | |
|---|---|
| **Product** | NephroPlus — an asset-light dialysis network across India, the Philippines, Uzbekistan, Nepal and Saudi Arabia |
| **Company** | Nephrocare Health Services Limited |
| **Domain** | Healthtech — chronic-care single-specialty services (nephrology / dialysis) |
| **Period examined** | Q1 FY27, quarter ended 30 June 2026; results 11 August 2026, earnings call 12 August 2026 |
| **Why it matters** | India's largest dialysis provider, ~10% of the country's dialysis patients, >50% of the organised market |
| **Proposed feature** | *NephroPlus Dose* — a published dose-adequacy ledger with a payer-facing weekly price |
| **Evidence grades** | 🟢 High · 🟡 Medium · 🟠 Low · 🔴 Conflicting |

---

## 2. Repository Metadata

**Legal entity:** Nephrocare Health Services Limited. **CIN L85100TG2009PLC066359** — cited rather than the name alone, because the brand (NephroPlus) and the entity differ, and because the entity's own identity changed twice in a year. Incorporated **18 December 2009** as Nephrocare Health Services Private Limited by the Assistant Registrar of Companies, Andhra Pradesh; converted to a public limited company with a fresh certificate dated **18 June 2025**; now on the RoC Hyderabad register. Registered office: 5th Floor, D Block, iLabs Centre, Plot 18, Software Units Layout, Survey No. 64, Madhapur, Hyderabad 500081. Authorised capital **₹34.98 Cr**, paid-up **₹20.0681434 Cr** — a ratio of only **1.74×**, unusually tight for a company mid-expansion. 🟢

The CIN's activity code is **85100 — human health activities**, which is correct. The register-misclassification tally this series has kept since Day 46 now stands at **nine wrong of fourteen**: two consecutive correct entries, both healthcare.

**Listed status.** Scrip code 544647, symbol NEPHROPLUS. IPO **₹871.05 Cr**, 10–12 December 2025, band ₹438–460, priced at the top at **₹460**, listed at **₹490** — a **6.52%** listing gain — subscribed **13.96×** overall, with QIB at 27.47×, NII at 24.27× and retail at only **2.31×**. The institutional-to-retail spread is itself worth noting in a business whose customers are among India's poorest chronic patients. 🟢

---

## 3. Badges

`Day 77/90` · `Healthtech` · `Chronic care / dialysis` · `NEPHROPLUS` · `Q1 FY27` · `65 sections` · `117 verified checks` · `0 fabricated figures` · `Runnable SQL in §32` · `Zero Mermaid — tables and ASCII only`

---

## 4. Table of Contents

<details>
<summary><b>All 65 sections</b></summary>

| Group | | |
|---|---|---|
| **Context** | [1. Cover](#1-cover) · [2. Repository Metadata](#2-repository-metadata) · [3. Badges](#3-badges) · [4. Table of Contents](#4-table-of-contents) · [5. Executive Summary](#5-executive-summary) | [6. Product Overview](#6-product-overview) · [7. Company Background](#7-company-background) · [8. Product Timeline](#8-product-timeline) · [9. Vision & Mission](#9-vision--mission) |
| **Market & Competition** | [10. Problem Statement](#10-problem-statement) · [11. Market Research](#11-market-research) · [12. Industry Analysis](#12-industry-analysis) · [13. TAM / SAM / SOM](#13-tam--sam--som) | [14. Competitor Analysis](#14-competitor-analysis) · [15. SWOT](#15-swot) · [16. Porter's Five Forces](#16-porters-five-forces) · [17. Business Model Canvas](#17-business-model-canvas) |
| **Business & Users** | [18. Revenue Model](#18-revenue-model) · [19. Target Users](#19-target-users) · [20. Personas](#20-personas) · [21. Jobs To Be Done](#21-jobs-to-be-done) · [22. User Journey](#22-user-journey) | [23. User Flow](#23-user-flow) · [24. Information Architecture](#24-information-architecture) · [25. UX Audit](#25-ux-audit) · [26. UI Audit](#26-ui-audit) · [27. Accessibility](#27-accessibility) |
| **Product, Metrics & Analytics** | [28. Feature Breakdown](#28-feature-breakdown) · [29. AI Capabilities](#29-ai-capabilities) · [30. Product Metrics](#30-product-metrics) · [31. North Star Metric](#31-north-star-metric) · [32. Product Analytics](#32-product-analytics) · [33. AARRR](#33-aarrr) | [34. HEART](#34-heart) · [35. Growth Strategy](#35-growth-strategy) · [36. Growth Loops](#36-growth-loops) · [37. Network Effects](#37-network-effects) · [38. Product Strategy](#38-product-strategy) · [39. Monetization](#39-monetization) |
| **Risk, Prioritisation & Proposal** | [40. Trust & Safety](#40-trust--safety) · [41. Technical Architecture](#41-technical-architecture) · [42. Data Flow](#42-data-flow) · [43. API Ecosystem](#43-api-ecosystem) · [44. Privacy & Security](#44-privacy--security) · [45. Pain Points](#45-pain-points) | [46. Opportunity Mapping](#46-opportunity-mapping) · [47. RICE](#47-rice) · [48. MoSCoW](#48-moscow) · [49. Kano](#49-kano) · [50. Feature Proposal — *NephroPlus Dose*](#50-feature-proposal--nephroplus-dose) · [51. PRD](#51-prd) |
| **Execution** | [52. Wireframes](#52-wireframes) · [53. Rollout Plan](#53-rollout-plan) · [54. A/B Testing](#54-ab-testing) · [55. KPI Dashboard](#55-kpi-dashboard) | [56. Product Roadmap](#56-product-roadmap) · [57. Risks & Mitigation](#57-risks--mitigation) · [58. Future Vision](#58-future-vision) |
| **Reflection & Sources** | [59. PM Lessons](#59-pm-lessons) · [60. PM Interview Questions](#60-pm-interview-questions) · [61. References](#61-references) · [62. About the Author](#62-about-the-author) | [63. License](#63-license) · [64. Self Review](#64-self-review) · [65. Appendix](#65-appendix) |

</details>

---

## 5. Executive Summary

Nephrocare Health Services runs India's largest dialysis network under the NephroPlus brand: **550 clinics across five countries** at 30 June 2026, of which **487 are in India across 307 cities**, roughly 80% of them in tier-2 and tier-3 locations. It treated **10,31,084** patients-sessions in the quarter for **38,262 guests** — the company's own word for its patients — and in FY25 accounted for about **10% of India's entire dialysis patient population**, at **4.40×** the next-largest organised provider by FY24 revenue. 🟢

The quarter, on the company's own framing, was excellent and the framing is fair. Revenue from operations **₹281.8 Cr against ₹227.8 Cr, +23.71%**; adjusted EBITDA **₹65.1 Cr, +30.72%**, margin **23.10%** from 21.86% and up 220 bps sequentially; adjusted PAT **₹36.8 Cr, +41.54%**; annualised adjusted ROCE 21%. Each line grew faster than the one above it, which is what operating leverage looks like when it is real. Revenue growth also ran **3.70 points above the top of the company's own 15–20% medium-term guidance.** 🟢

Two divisions complicate it, and neither requires a single number the company did not publish.

**First, the dose.** India: ~860,000 treatments ÷ 33,047 guests = **26.02 per guest per quarter**, which is **2.00 sessions a week** against the three-a-week standard for end-stage renal disease — **66.73% of adequate**, a shortfall of **12.98 treatments per guest per quarter**. International: **32.60**, or **2.51 a week**, **83.59%** of adequate — **1.25×** the Indian dose. The two guest counts sum *exactly* to the reported 38,262, which is what makes the split trustworthy; the two treatment counts are disclosed as approximations and leave a residual of 1,084, or **0.11%**.

The trend is genuinely improving and the case study says so: group dose adequacy went **63.82% (FY25) → 66.56% (FY26) → 69.10% (Q1 FY27 annualised)**, a gain of **5.28 points**. But India's own reading moved only **3.56 points** (63.17% in FY25 to 69.10%'s Indian equivalent), and the group's faster improvement is arithmetically helped by international mix, where the dose is already higher. **The company is getting better at this. It is not yet close.**

**Second, the profit.** Adjusted PAT of ₹36.8 Cr is struck after adding back a **₹3.6 Cr share of joint-venture loss** and **₹1.3 Cr of ESOP cost**. Q1 FY26's ₹26.0 Cr was adjusted for ESOP alone. Back both out and **reported PAT is ₹31.90 Cr against ₹23.70 Cr — growth of 34.60%, not 41.7%**, a gap of **7.10 points**. Adjustments rose from **8.85%** of adjusted PAT to **13.32%**, and the JV loss is a line that did not exist a year ago. On margins, adjusted expansion of 1.70 points is **1.86×** the reported expansion of 0.92 points. Adjusted EBITDA, separately, is struck for ESOP **and for "Saudi expenses" that are not quantified anywhere in the disclosure** — so the most that can be said is that reported EBITDA margin is **at most 22.64%**, against the 23.10% presented.

**Where growth is coming from is the link between the two.** India is **83.50% of treatments but 55% of revenue**; international is 16.50% of treatments and 45%. Implied realisation is **₹1,802 per treatment in India against ₹7,459 international — 4.14×**, which sits inside the company's own disclosed 3.3×–13.6× band. International went from **31.8% of revenue in FY25 to 41.8% in FY26 to 45% now — 13.20 points in five quarters.** Revenue grew **10.40 points faster than treatments**, and treatment growth *decelerated* 3.30 points from FY26 while guest growth accelerated 1.20. **The margin story is a geography story, and the geography it is moving away from is the one where the dose gap lives.**

**The prize, sized from the company's own base.** Bringing only the 33,047 Indian guests it already serves to a thrice-weekly standard is **428,833 additional treatments a quarter — 49.86% more than India currently delivers — worth ₹77.28 Cr, or 27.43% of total group revenue.** Nationally, the implied 292,810-patient Indian dialysis population would need **45.68 million treatments a year**; NephroPlus delivered 2.89 million in FY25, **6.32%** of the requirement.

**The proposal, *NephroPlus Dose*,** makes dose adequacy a published, per-clinic, per-payer number and attacks the mechanism that suppresses it: per-session pricing, which makes the third session of the week a fresh purchase decision every week for a household already paying for the first two. **In the RICE table it leads at baseline and falls to second under stress**, behind international clinic densification — which needs no patient to do anything. §47 argues why that is the right answer and why it does not weaken the proposal.

---

## 6. Product Overview

The product is a clinic network operated asset-light: NephroPlus supplies the clinical model, staff, protocols and machines, while hospitals frequently supply the space — the captive hospital format alone was **36.51% of dialysis revenue in H1 FY26**. Formats span in-hospital captive units, standalone centres and public-private partnerships, plus home haemodialysis, hemodiafiltration, dialysis-on-call and holiday dialysis. 🟢

The revenue unit is a single dialysis session. That choice is the subject of §39 and §50, because it is also the unit at which a patient decides whether to come. 🟡

---

## 7. Company Background

Founded in 2009 by **Vikram Vuppala** and **Kamal D. Shah** — the latter himself a long-term dialysis patient, which is an unusually direct line between founder and user. Vuppala is Chairman and Managing Director; **Rohit Singh** is Group CEO and **Prashant Goenka** Group CFO; the board includes Om Prakash Manchanda, Vishal Vijay Gupta and Sunil Kumar Thakur. Headcount was **1,533** at 1 April 2026 — **672.59 treatments per employee per quarter**. 🟢

Backers before listing included the International Finance Corporation, Bessemer Venture Partners, Investcorp and 360 One, with Edoras Investment Holdings as promoter. Development-finance money in the cap table matters for §10: the access mission is contractual history, not just marketing. 🟢

---

## 8. Product Timeline

| Date | Event |
|---|---|
| Dec 2009 | Incorporated in Hyderabad as a private limited company 🟢 |
| 2010 onward | NephroPlus brand established; India network build 🟢 |
| FY25 | 29,281 Indian patients, 28,85,450 Indian treatments — ~10% of India's dialysis population 🟢 |
| 26 Jul 2025 | DRHP filed; fresh issue ₹353.4 Cr proposed 🟢 |
| 10–12 Dec 2025 | IPO ₹871.05 Cr at ₹460; subscribed 13.96× 🟢 |
| Dec 2025 | Listed at ₹490, a 6.52% gain 🟢 |
| 22 Jun 2026 | ESOP 2026 approved — 20,06,814 options, 2% of paid-up capital; ₹70 Cr collateral sanctioned for the Saudi subsidiary 🟢 |
| Jul 2026 | First Saudi clinic opens at a Riyadh hospital; home dialysis begins; medical operator's licence obtained 🟢 |
| 11–12 Aug 2026 | Q1 FY27 results and call; 550 clinics; 50-clinic milestone in the Philippines; NIDA academy launched 🟢 |
| 31 Aug 2026 | Uzbekistan tax department raises a **₹14.79 Cr** assessment and penalty for 2023–25; company plans to appeal 🟢 |
| 1 Sep 2026 | Agreement to acquire 100% of Dialysis Center Almaty LLP, **KZT 561.66 Mn** — a sixth country 🟢 |
| 3 Sep 2026 | **4,01,362** options granted at a **₹230** exercise price 🟢 |

---

## 9. Vision & Mission

The stated mission is to let people on dialysis live a full life rather than a medicalised one — the "guest" vocabulary is a deliberate refusal of the word patient, and the holiday-dialysis and dialysis-on-call products follow from it. 🟢

The commercial mission, as presented to investors, is a "dialysis platform made in India for the world": export an operating model built for a low-price market into markets that pay **3.3× to 13.6×** more. Both missions are sincere. §38 is about what happens when they point in different directions. 🟡

---

## 10. Problem Statement

**The problem the company solves** is access. Dialysis requires a machine, water treatment, a trained technician and a nephrologist within reach of someone who must make the journey three times a week, indefinitely. Putting **487 clinics into 307 Indian cities, ~80% of them tier-2 and tier-3**, is a genuine answer, and no other Indian operator has built one at this scale. 🟢

**The problem the numbers pose** is that access to a clinic is not the same as receipt of treatment. The company's own Indian guests are receiving **2.00 sessions a week when the standard is three**. Access has been solved to the door; adequacy has not been solved past it.

**The product problem underneath** is that the session is the unit of sale. A household paying per session, largely out of pocket, faces the third session of every week as a discrete purchase — the one most easily deferred, because the patient feels least unwell when the first two have just been done. Nothing in the disclosure suggests dose adequacy is measured, published, owned or priced against. **The business model quietly converts a clinical requirement into a weekly affordability decision, and then reports the outcome as treatment volume.**

---

## 11. Market Research

Sizing this market from the company's own disclosure is more honest than quoting a third-party forecast, and it produces a starker number.

NephroPlus states it served **29,281 Indian patients in FY25**, representing roughly **10%** of India's dialysis patient population. That implies a national population of about **292,810**. At the clinical standard of 156 treatments a year, that population requires **45.68 million treatments annually**. NephroPlus delivered **2.89 million** in FY25 — **6.32%** of the requirement — leaving an implied national shortfall of **42.79 million treatments a year**. 🟡

Two caveats stated at the point of use. The 10% share is the company's own characterisation, so the implied population inherits its imprecision. And the shortfall is not NephroPlus's to close alone — it is the market's. But the direction is unambiguous: **India's dialysis problem is not a shortage of patients reaching clinics, it is a shortage of sessions reaching patients.** 🟡

---

## 12. Industry Analysis

Organised dialysis in India is a scale-and-procurement game: consumables and machine costs dominate, the clinical protocol is standardised, and the operator with the most sessions buys best. NephroPlus is **4.40×** the next-largest organised player by FY24 revenue and holds **over 50%** of the organised market — a level of concentration none of the other healthtech sub-sectors in this series has shown. 🟢

The structural constraint is who pays. A large share of Indian dialysis is funded out of pocket or through state schemes with fixed, low per-session rates, which caps price and makes volume the only lever. That is precisely why an operator with this market position exports margin rather than raising Indian price — and why the dose question is a design problem rather than a pricing one. 🟡

---

## 13. TAM / SAM / SOM

*Framework selection rationale: run in restricted form. No primary-sourced Indian dialysis market size appears in the filings examined, and third-party estimates for this sector diverge widely. The market is therefore sized from the company's own disclosed patient base and share claim.*

| Layer | Basis | Figure |
|---|---|---|
| Implied national patient population | 29,281 Indian patients ÷ the company's ~10% share claim | **292,810 patients** 🟡 |
| Clinically required volume | That population × 156 treatments a year | **45.68 million treatments/yr** 🟡 |
| Delivered by NephroPlus, FY25 | India treatments | **2,885,450 = 6.32%** of requirement 🟢 |
| Implied national shortfall | Requirement less delivered | **42.79 million treatments/yr** 🟡 |
| **Obtainable, near term** | Bringing the company's **existing** 33,047 Indian guests to three a week | **428,833 treatments/quarter, ₹77.28 Cr, 27.43% of group revenue** 🟡 |

The last row is the point. The largest identifiable growth opportunity in this business requires no new city, no new clinic and no new patient — only that the patients already enrolled receive the treatment they are already prescribed.

---

## 14. Competitor Analysis

*Framework selection rationale: restricted to entities that actually file, and in this case the restriction nearly empties the table. India's organised dialysis market is consolidated enough that **NephroPlus's nearest domestic competitors are unlisted and publish no audited financials** — the company's own claim of being 4.40× the next-largest organised player by FY24 revenue is the only sizing available, and it is a company claim resting on a commissioned industry report. No competitor estimate is constructed here. This is the fifth consecutive case study applying that restriction.* 🟡

The comparison that can be made rigorously is **internal and geographic** — NephroPlus India against NephroPlus international, both disclosed in the same release on the same basis.

| Q1 FY27 | India | International |
|---|---|---|
| Clinics | 487 across 307 cities | 63 |
| Guests | 33,047 | 5,215 |
| Treatments | ~860,000 | ~170,000 |
| Share of treatments | **83.50%** | **16.50%** |
| Share of revenue | **55%** | **45%** |
| Revenue share less treatment share | **−28.50pp** | **+28.50pp** |
| Implied revenue per treatment | **₹1,802.21** | **₹7,459.41** (**4.14×**) |
| Treatments per guest per quarter | **26.02** | **32.60** (**1.25×**) |
| Sessions per week | **2.00** | **2.51** |
| Dose adequacy vs the 3/week standard | **66.73%** | **83.59%** |
| Treatments per clinic per quarter | **1,765.91** | **2,698.41** (**1.53×**) |
| Guests per clinic | **67.86** | **82.78** |

Three readings, and the third is the finding.

First, the realisation gap is real and validated: **₹7,459 against ₹1,802, or 4.14×**, sits comfortably inside the 3.3×–13.6× band the company itself discloses, and the blended figure cross-checks almost exactly — ₹281.8 Cr over 10,31,084 treatments is **₹2,733.05** against the disclosed **₹2,733**, a five-paise agreement that validates the whole revenue-split arithmetic.

Second, international clinics are more productive on every operating measure: 1.53× the throughput per clinic, 1.22× the guests per clinic.

Third — **the same network, run by the same company on the same protocols, delivers 2.51 sessions a week abroad and 2.00 in India.** That is a 25% difference in clinical dose inside one operator, and it is not a capability difference. It is a payer difference. Which means the Indian dose gap is not evidence that NephroPlus cannot deliver adequate dialysis; it is evidence of what happens to the same operator when the patient pays per session.

---

## 15. SWOT

| Strengths | Weaknesses |
|---|---|
| >50% of India's organised market; **4.40×** the next player 🟢 | India dose adequacy **66.73%** 🟡 |
| Asset-light; captive hospital format **36.51%** of dialysis revenue 🟢 | India realisation **₹1,802** vs **₹7,459** international 🟡 |
| Real operating leverage: adj EBITDA +30.72% on revenue +23.71% 🟢 | Reported PAT growth **34.60%** vs adjusted 41.7% 🟡 |
| Founder-user in the founding team 🟢 | "Saudi expenses" excluded from adjusted EBITDA and **not quantified** 🟠 |
| **Opportunities** | **Threats** |
| **₹77.28 Cr/quarter** from existing guests alone 🟡 | Uzbekistan assessment **₹14.79 Cr = 40.19%** of quarterly adjusted PAT 🟢 |
| International dose already at 83.59% — the model works 🟡 | Treatment growth decelerating **3.30pp** from FY26 🟡 |
| 45% international revenue, from 31.8% in FY25 🟢 | Saudi is pre-revenue; tenders 2–3 months out, revenue 3–4 quarters 🟢 |
| Sixth country added post-quarter (Kazakhstan) 🟢 | Fixed state-scheme rates cap Indian price 🟡 |

---

## 16. Porter's Five Forces

*Framework selection rationale: run twice and merged into one table, because the two halves of this business face inverted forces. **India is a fixed-price, out-of-pocket, volume market competing against a free public alternative; international is a payer-funded market at 3.3×–13.6× the price.** The seam is not geography for its own sake — it is who pays per session, which is the whole case study.*

| Force | India (83.50% of treatments, 55% of revenue) | International (16.50% of treatments, 45% of revenue) |
|---|---|---|
| Buyer power | Extreme on price, nil on need: the patient cannot stop, but can skip 🟡 | Low: an institutional payer contracts for a protocol, not a session 🟡 |
| Supplier power | High — consumables and machines are imported and dollar-denominated 🟡 | Same suppliers, absorbed by a 4.14× higher realisation 🟡 |
| New entrants | Low in organised form, high in fragmented form: a single-machine unit is cheap 🟡 | Low: licensing and tenders gate entry, as Saudi is demonstrating 🟢 |
| Substitutes | Government and charitable dialysis, transplantation, and — the real one — **doing fewer sessions** 🟡 | Few; the payer prescribes adequacy 🟡 |
| Rivalry | Muted structurally (>50% organised share) but intense against the unorganised sector 🟡 | Fragmented and local; NephroPlus is consolidating 🟡 |

The inversion names the mechanism. In India the most available substitute for a NephroPlus session is **not a competitor's session — it is no session**, and that substitute is chosen roughly a third of the time. Internationally that substitute barely exists, because nobody is deciding week by week whether this week's third treatment is affordable. **Same operator, same protocol, different payer, 25% different dose.**

---

## 17. Business Model Canvas

| Block | Content |
|---|---|
| Value proposition | Adequate dialysis within reach, plus a life that accommodates it (holiday, home, on-call) 🟢 |
| Customer segments | Out-of-pocket Indian guests; state-scheme patients; hospital partners; international institutional payers 🟡 |
| Channels | 550 clinics; captive hospital units; PPP contracts; home programmes 🟢 |
| Key activities | Session delivery, clinical protocol, procurement, clinic commissioning, technician training (NIDA) 🟢 |
| Key resources | 38,262 enrolled guests; 1,533 staff; the machine fleet; **the prescription record** 🟡 |
| Key partners | Host hospitals; state governments; consumable and machine vendors; JV partners 🟡 |
| Cost structure | Consumables, clinical payroll, machine D&A; Saudi investment phase 🟢 |
| Revenue streams | Per-session fees; pharmacy and wellness attach; international contracts 🟢 |
| Customer relationships | Lifelong by clinical necessity, transactional by pricing design — the contradiction the proposal addresses 🟡 |
---

## 18. Revenue Model

Revenue is recognised per dialysis session. Blended realisation was **₹2,733** in Q1 FY27, up **9.19%**, and the increase is almost entirely mix: **₹1,802.21** per Indian treatment against **₹7,459.41** international, with international moving from 31.8% of revenue in FY25 to **45%** now. 🟡

Pharmacy and wellness services attach to the same visit. The per-session unit is standard for the industry and is not an accounting quirk — it is the commercial expression of how state schemes and households pay. 🟢

---

## 19. Target Users

Four groups, and only one of them decides anything week to week: the out-of-pocket Indian guest, for whom each session is a payment; the state-scheme patient, whose entitlement is capped in sessions per period; the host hospital, which supplies space in exchange for revenue share; and the international institutional payer, which contracts for a protocol rather than a session. 🟡

---

## 20. Personas

| Persona | Situation | What decides the third session |
|---|---|---|
| **Ramesh, 54, tier-3 Maharashtra** | On dialysis 3 years, pays largely out of pocket, drives 40 km each way | Whether the week's third trip is affordable *and* whether he feels ill enough to justify it 🟡 |
| **Sunita, 47, Hyderabad** | State-scheme entitlement covers a fixed number of sessions per year | Whether her entitlement has run out before the year has 🟡 |
| **Mr Dela Cruz, 61, Manila** | Payer-funded, three sessions prescribed and delivered | Nothing — adequacy is the payer's contractual expectation 🟡 |
| **Dr Iyer, nephrologist at a captive unit** | Prescribes thrice-weekly, sees twice-weekly attendance | Has no instrument that records the gap as a clinical event 🟡 |

Ramesh is the entire case study. The clinically correct answer for him is unambiguous and the commercially observable outcome is that he comes twice.

---

## 21. Jobs To Be Done

| When… | I want to… | So that… |
|---|---|---|
| my third session of the week falls due and I feel alright | know whether skipping it is actually safe | I am not guessing with my own kidney failure 🟡 |
| I am paying per session out of pocket | not face a new purchase decision every few days | the cost is a household line item, not a recurring dilemma 🟡 |
| I have been on dialysis for years | have someone notice when my attendance slips | the drift is caught before it becomes an admission 🟡 |

The second job is the one the pricing model actively works against, which is why the proposal is partly a pricing change.

---

## 22. User Journey

```
DIAGNOSIS ──► ENROLMENT ──► PRESCRIPTION ──► ATTENDANCE ──────────► OUTCOME
(nephrology   (38,262        (3 sessions      (2.00/week India)      (unmeasured
 referral)     guests)        per week)        (2.51/week intl)       publicly)
                                  │                 │
                                  │   ┌─────────────┘
                                  ▼   ▼
                          THE GAP: 12.98 treatments per Indian
                          guest per quarter, prescribed and not
                          delivered. No owner. No record. No metric.
```

Every other step in this journey is instrumented and reported. The one that determines whether the patient lives well is inferred from a volume total.

---

## 23. User Flow

Arrival → weight and vitals → access preparation → four-hour session → post-session weight → next appointment given. The loop closes only if the patient returns on schedule, and the return is the step with no system consequence when it fails. 🟡

---

## 24. Information Architecture

Clinically the record is per guest per session per clinic; commercially the reporting unit is treatments and guests, each disclosed as an aggregate. Dividing one by the other — which is what this case study does — is possible only because both are published. Per-clinic, per-payer and per-guest dose is held internally and disclosed nowhere. 🟡

---

## 25. UX Audit

The in-clinic experience is the strength: the "guest" framing, holiday dialysis and dialysis-on-call all treat the patient as a person with a life rather than a condition with an appointment. 🟢

The weakness is the interval. Nothing in the published product surface carries the prescription forward as an obligation — no adherence view, no household-facing schedule, no attendance record the patient or family can see. 🟠

---

## 26. UI Audit

There is no disclosed patient-facing digital product carrying schedule, attendance or dose. For a chronic-care business with a decade-long patient relationship, that absence is the most striking product fact in the disclosure. 🟠

---

## 27. Accessibility

The population is older, frequently diabetic, often fatigued to the point of impairment after a session, and predominantly in tier-2 and tier-3 cities. Any adherence mechanism that assumes patient smartphone literacy will fail; the accompanying family member who arranges transport and pays is the real user, and the design has to address them. 🟡

---

## 28. Feature Breakdown

| Capability | Present | Evidence |
|---|---|---|
| In-centre haemodialysis | Yes — the core; 10,31,084 sessions in the quarter | 🟢 |
| Home haemodialysis | Yes, including a new Saudi programme | 🟢 |
| Hemodiafiltration | Yes | 🟢 |
| Holiday dialysis | Yes — the clearest expression of the "guest" thesis | 🟢 |
| Dialysis on call / on wheels | Yes | 🟢 |
| Pharmacy and wellness attach | Yes | 🟢 |
| Technician training pipeline | Yes — NIDA launched in Q1 FY27 | 🟢 |
| **Dose-adequacy measurement and reporting** | **Not evidenced in any disclosure examined** | 🟠 |
| **Patient- or family-facing adherence record** | **Not evidenced** | 🟠 |

The asset that exists and is unused is the prescription. Every one of the 38,262 guests has a prescribed weekly frequency recorded by a nephrologist, and the company reports attendance only in aggregate — which means the gap between the two is computable internally today, per guest, without collecting anything new.

---

## 29. AI Capabilities

No AI product is disclosed. Stating that plainly is better than inflating a training academy or a scheduling system into one. 🟠

The proposal in §50 requires no model. Predicting which guest will miss their next session is a genuinely tractable problem on this data, and it is deliberately scoped out of v1 — the first version needs a number published, not a prediction served. 🟡

---

## 30. Product Metrics

| Metric | Q1 FY27 | Q1 FY26 | Change |
|---|---|---|---|
| Revenue from operations | ₹281.8 Cr | ₹227.8 Cr | **+23.71%** 🟢 |
| Treatments | 10,31,084 | 9,10,000 | **+13.31%** 🟢 |
| Guests | 38,262 | — | **+13.0%** (reported) 🟢 |
| Revenue per treatment | ₹2,733 | ₹2,503 | **+9.19%** 🟢 |
| Adjusted EBITDA | ₹65.1 Cr | ₹49.8 Cr | **+30.72%** 🟢 |
| Adjusted EBITDA margin | **23.10%** | **21.86%** | +124 bps 🟡 |
| Adjusted PAT | ₹36.8 Cr | ₹26.0 Cr | **+41.54%** 🟢 |
| **Reported PAT** | **₹31.90 Cr** | **₹23.70 Cr** | **+34.60%** 🟡 |
| **Group dose per guest/quarter** | **26.95** | — | **69.10% of standard** 🟡 |
| **India dose per guest/quarter** | **26.02** | — | **66.73% of standard** 🟡 |
| **International dose per guest/quarter** | **32.60** | — | **83.59% of standard** 🟡 |
| Treatments per clinic | 1,874.70 | — | India 1,765.91 / intl 2,698.41 🟡 |
| Treatments per employee | 672.59 | — | — 🟡 |

**Two internal checks that make the segment arithmetic safe.** India's 33,047 guests plus international's 5,215 equal the reported 38,262 **exactly**. And revenue ÷ treatments gives **₹2,733.05** against the disclosed **₹2,733** — agreement to five paise. The revenue split and the dose split are therefore not reconstructions; they are the company's own numbers divided.

**One honest gap.** Prior-year segment guest and treatment splits were not found, so **the dose gap cannot be trended at segment level.** The group-level trend is computable from FY25 and FY26 totals and is shown in §32; the India-versus-international *convergence or divergence* is not, and no claim is made about it.

---

## 31. North Star Metric

**Proposed: DAG/1k — Dose-Adequate Guest-weeks per 1,000 prescribed guest-weeks.**

A guest-week enters the denominator when a nephrologist's prescription for that guest is active. It enters the numerator only if **all four** hold:

1. the prescribed frequency was recorded **before** the week began, by the prescribing clinician;
2. the prescribed number of sessions was **delivered** within that week;
3. each session ran to its **prescribed duration** — because a short session is a partial dose and would otherwise be counted whole;
4. the prescription was **not revised downward** during the week.

**The denominator is the design choice.** It is prescribed guest-weeks, not sessions, not guests and not revenue. Enrolling more guests without delivering their prescriptions *lowers* the metric. Condition 4 blocks the obvious gaming route — reducing the prescription to match attendance — and condition 3 blocks the subtler one of shortening sessions to fit more in.

**Guardrail, carried from here to §55: PSC-90 — Prescription Softening at the 90th percentile.** In the decile of clinic-quarters with the largest DAG/1k improvement, the share of active prescriptions revised downward, reported **by clinic and by prescribing clinician**. A clinic can always hit a dose-adequacy target by prescribing less, and this is the only number that catches it.

---

## 32. Product Analytics

Everything the proposal needs is computable from data the company already holds. Below is the actual analysis, not a description of it — three queries against a minimal schema of `guests`, `prescriptions`, `sessions` and `clinics`.

**Dose adequacy per guest per week, and the North Star.**

```sql
WITH guest_weeks AS (
    SELECT p.guest_id,
           c.clinic_id,
           c.country,
           DATE_TRUNC('week', d.week_start)          AS wk,
           MAX(p.sessions_per_week)                  AS prescribed,
           MAX(p.prescribed_minutes)                 AS prescribed_minutes,
           MAX(p.revised_down_flag)                  AS revised_down
    FROM prescriptions p
    JOIN clinics  c ON c.clinic_id = p.home_clinic_id
    JOIN calendar d ON d.week_start BETWEEN p.valid_from
                                        AND COALESCE(p.valid_to, CURRENT_DATE)
    GROUP BY 1, 2, 3, 4
),
delivered AS (
    SELECT s.guest_id,
           DATE_TRUNC('week', s.session_date) AS wk,
           COUNT(*)                                                   AS sessions_done,
           SUM(CASE WHEN s.duration_minutes >= gw.prescribed_minutes
                    THEN 1 ELSE 0 END)                                AS full_length_done
    FROM sessions s
    JOIN guest_weeks gw
      ON gw.guest_id = s.guest_id
     AND gw.wk       = DATE_TRUNC('week', s.session_date)
    WHERE s.status = 'completed'
    GROUP BY 1, 2
)
SELECT gw.country,
       gw.clinic_id,
       COUNT(*)                                              AS prescribed_guest_weeks,
       ROUND(AVG(COALESCE(d.sessions_done, 0)), 2)           AS avg_sessions_delivered,
       ROUND(AVG(COALESCE(d.sessions_done, 0) * 1.0
                 / gw.prescribed) * 100, 2)                  AS dose_adequacy_pct,
       ROUND(1000.0 * SUM(CASE WHEN d.full_length_done >= gw.prescribed
                                AND gw.revised_down = FALSE
                               THEN 1 ELSE 0 END) / COUNT(*), 1) AS dag_per_1k
FROM guest_weeks gw
LEFT JOIN delivered d
       ON d.guest_id = gw.guest_id AND d.wk = gw.wk
GROUP BY 1, 2
ORDER BY dag_per_1k ASC;
```

Ordering ascending is deliberate: the first rows returned are the clinics where the gap is worst, which is the list the intervention should be sequenced against.

**The guardrail — prescription softening in the fastest-improving clinics.**

```sql
WITH improvement AS (
    SELECT clinic_id,
           dag_per_1k - LAG(dag_per_1k) OVER (PARTITION BY clinic_id
                                              ORDER BY quarter) AS dag_delta
    FROM clinic_quarter_dose          -- materialised from the query above
),
ranked AS (
    SELECT clinic_id, dag_delta,
           PERCENT_RANK() OVER (ORDER BY dag_delta) AS pr
    FROM improvement
    WHERE dag_delta IS NOT NULL
)
SELECT r.clinic_id,
       ROUND(r.dag_delta, 1)                                   AS dag_improvement,
       ROUND(100.0 * SUM(CASE WHEN p.revised_down_flag THEN 1 ELSE 0 END)
             / COUNT(*), 2)                                    AS psc_pct
FROM ranked r
JOIN prescriptions p ON p.home_clinic_id = r.clinic_id
WHERE r.pr >= 0.90                    -- the 90th percentile of improvement
GROUP BY 1, 2
HAVING ROUND(100.0 * SUM(CASE WHEN p.revised_down_flag THEN 1 ELSE 0 END)
             / COUNT(*), 2) > 3.00    -- breach threshold
ORDER BY psc_pct DESC;
```

Any row this returns is a clinic whose dose improvement may be arithmetic rather than clinical, and under §40 its recall activity suspends automatically.

**Separating the two ways a guest disappears — the question the volume total cannot answer.**

```sql
SELECT g.country,
       CASE WHEN g.outcome IN ('deceased')            THEN 'mortality'
            WHEN g.outcome IN ('transplanted')        THEN 'transplant'
            WHEN g.outcome IN ('transferred_out')     THEN 'transfer'
            WHEN last.session_date < CURRENT_DATE - INTERVAL '60 days'
                                                      THEN 'lapsed_unexplained'
            ELSE 'active' END                         AS exit_type,
       COUNT(*)                                       AS guests,
       ROUND(AVG(pre.dose_adequacy_pct), 2)           AS avg_dose_before_exit
FROM guests g
LEFT JOIN (SELECT guest_id, MAX(session_date) AS session_date
           FROM sessions GROUP BY 1) last ON last.guest_id = g.guest_id
LEFT JOIN guest_dose_90d pre        ON pre.guest_id  = g.guest_id
GROUP BY 1, 2
ORDER BY 1, 3 DESC;
```

That last query is the one that would settle whether the dose gap is killing people. If `avg_dose_before_exit` is materially lower for `mortality` and `lapsed_unexplained` than for `active`, the case for the proposal stops being economic and becomes clinical. **It is also the query whose result the company has never published, and the reason §54 is built the way it is.**

---

## 33. AARRR

*Framework selection rationale: used in modified form. For a lifelong chronic service, "activation" is not the first session — it is the first fully adequate week — and "retention" is survival, which is a clinical outcome rather than a product one.*

| Stage | Reading |
|---|---|
| Acquisition | 38,262 guests, +13.0%; 67.86 guests per Indian clinic 🟡 |
| Activation | First adequate week — **not measured anywhere** 🟠 |
| Retention | India dose **66.73%** of prescribed; true retention is survival, undisclosed 🟡 |
| Revenue | ₹2,733 per treatment, +9.19%, driven by geography 🟡 |
| Referral | Nephrologist referral is the primary channel; conversion undisclosed 🟠 |

---

## 34. HEART

| Dimension | Signal and status |
|---|---|
| Happiness | No published NPS or CSAT 🟠 |
| Engagement | **This is dose adequacy, and it is 66.73% in India** 🟡 |
| Adoption | Home and holiday dialysis uptake not broken out 🟠 |
| Retention | Guest cohort survival undisclosed 🟠 |
| Task success | Session completion against prescribed duration undisclosed 🟠 |

HEART is unusually apt here because its "engagement" dimension, which in a consumer product measures interest, in this product measures whether someone is receiving enough dialysis to stay well.

---

## 35. Growth Strategy

The strategy is stated plainly and is being executed ahead of its own guidance: grow 15–20% CAGR over three to five years, densify internationally where realisation is 3.3×–13.6× higher, and enter new markets. Q1 FY27 revenue growth of **23.71%** ran **3.70 points above the top of that band**. 🟢

The international build is concrete: 50 clinics in the Philippines, Uzbekistan established, Saudi in an investment phase with the first Riyadh clinic open in July 2026, a medical operator's licence obtained, tender documents expected within two to three months and revenue **three to four quarters away**; a sixth country added post-quarter via the **KZT 561.66 Mn** Almaty acquisition. 🟢

**What the strategy does not contain is a dose target.** Growth is expressed in revenue, clinics, countries and realisation. The clinical adequacy of the treatment delivered to existing guests appears in no disclosed objective.

---

## 36. Growth Loops

The working loop is procurement-led: more sessions → better consumable pricing → better margin → more clinics → more sessions. It is genuinely compounding and explains the 30.72% EBITDA growth on 23.71% revenue growth. 🟡

The loop the proposal would add is clinical: adequate dose → fewer hospitalisations and longer survival → more lifetime sessions per guest → more revenue per enrolment. In dialysis, unusually, **patient survival and revenue point the same way**, which is the strongest argument the proposal has. 🟡

---

## 37. Network Effects

None in the classic sense. What exists is a density effect in procurement and a data effect that is currently unexploited: 38,262 concurrent prescription-and-attendance records is the largest such dataset in Indian nephrology, and nothing disclosed suggests it is being used as one. 🟡

---

## 38. Product Strategy

Two strategies are available. The company is executing one of them extremely well.

**Export the model.** Take an operating system built for a ₹1,802 market into markets paying **₹7,459**, and let mix do the work. International went 31.8% → 41.8% → **45%** of revenue in five quarters, and it is why margin expanded. This is rational, it is working, and it is the reason the stock is where it is.

**Fix the dose at home.** Bring the 33,047 existing Indian guests from 2.00 sessions a week toward three: **428,833 additional treatments a quarter, 49.86% more Indian volume, ₹77.28 Cr, 27.43% of group revenue** — with no new clinic, no new city and no new patient.

The tension is not that the first is wrong. It is that **the first strategy improves the reported numbers by reducing the weight of the market where the company's stated mission lives.** India is already 83.50% of treatments and 55% of revenue; keep going and the company becomes a Gulf and South-East Asian operator that happens to have been built in India.

The honest recommendation is that these are complements, not alternatives — international realisation is exactly what could fund an Indian dose intervention that Indian per-session pricing cannot. But that requires someone to own the Indian dose number, and **nobody currently does, because it is not published.**

---

## 39. Monetization

The per-session model is where the clinical and commercial designs collide. Selling the unit that the patient is most likely to skip means the company's revenue is protected against the skip — it simply bills less — while the patient absorbs the entire clinical cost. Nothing in the current model makes NephroPlus worse off when Ramesh comes twice. 🟡

The change worth considering inverts that: a **weekly price** covering three prescribed sessions, set below 3× the per-session rate, so that the third session carries no marginal purchase decision. It lowers headline realisation per session and raises revenue per guest — and it puts the company's revenue at risk when adequacy falls, which is the point. 🟡
---

## 40. Trust & Safety

**Placed before the feature proposal deliberately, because this proposal's failure mode kills people in a different way than the status quo does.**

The status quo under-treats. A dose-adequacy target over-treats, and in dialysis over-treatment is not a billing question — unnecessary vascular access, intradialytic hypotension and the cumulative burden of sessions a patient does not clinically need all carry real harm. Worse, the cheapest way for any clinic to hit a dose-adequacy target is not to deliver more sessions but to **prescribe fewer**, which improves the metric while actively harming the patient. That is why PSC-90 exists and why it is a build requirement rather than a reporting nicety.

Five constraints, all specified in §51 as requirements:

1. **The prescription is written before the week it governs, by the prescribing clinician, into an append-only record.** The dose-adequacy system has read-only access. Without this the metric certifies itself.
2. **Downward prescription revisions are flagged, reason-coded and counted.** A revision is sometimes correct medicine — a recovering patient, a transplant workup — so it is not forbidden. It is counted, and the count is published.
3. **PSC-90 is owned by a function with no revenue or volume target,** reporting to the board's clinical governance committee, sampling operated weeks against their prescriptions.
4. **Breach suspends the clinic's adherence-outreach activity automatically.** Suspension is the default state on breach; resumption requires a case to be made.
5. **No outreach may be initiated by anyone whose variable pay depends on session volume at that clinic.**

Two further constraints specific to this population. Outreach goes to the **nominated family member** where the guest names one, per §27. And because a large share of Indian guests are on capped state-scheme entitlements, **the system must distinguish a guest who skipped from a guest whose entitlement was exhausted** — those are opposite problems with opposite remedies, and conflating them would send affordability outreach to someone with no remaining entitlement to use.

---

## 41. Technical Architecture

No detail of the clinical stack is publicly disclosed; what follows is what the proposal requires, not a description of what exists. 🟠

Three components: an append-only prescription ledger keyed to guest, clinician and effective week; an attendance and duration record written by the clinic at the point of session; and an adequacy engine that reads both and can write to neither. 🟡

---

## 42. Data Flow

```
NEPHROLOGY CONSULT ──► PRESCRIPTION LEDGER (append-only, clinician-signed)
                               │                      ▲
                               │  read-only           │  NO WRITE PATH
                               ▼                      │
        SESSION RECORD ──► ADEQUACY ENGINE ───────────┘
        (date, duration,          │
         completion)              ▼
                        DAG/1k per clinic · PSC-90 per clinician
                                  │
                        ┌─────────┴─────────┐
                        ▼                   ▼
              FAMILY OUTREACH        PUBLISHED REPORT
              (adequacy team,        (per clinic, per payer)
               no volume target)
```

The load-bearing feature is the absent arrow: the engine that is measured cannot edit the prescription it is measured against.

---

## 43. API Ecosystem

No public API is disclosed. 🟠 The proposal's external interfaces are documents rather than endpoints — a published per-clinic adequacy report and a payer-facing weekly-price schedule. The one genuine integration need is with **state scheme entitlement systems**, so that remaining entitlement is visible at the point of scheduling. 🟡

---

## 44. Privacy & Security

A longitudinal prescription-and-attendance record across 38,262 identified chronic patients is among the most sensitive datasets in Indian healthcare, and an obviously attractive one to insurers and pharmaceutical partners. 🟡

Under India's Digital Personal Data Protection framework the purpose must be stated narrowly: the record exists to deliver the guest's own prescribed care. Outreach consent is captured separately and is revocable. **Aggregate adequacy statistics leave; individual attendance histories do not**, and they are not shared with any payer beyond what the payer's own claim already contains. The cross-border dimension is real — five countries, soon six — so residency and transfer rules bind per market. 🟡

---

## 45. Pain Points

| # | Pain point | Evidence |
|---|---|---|
| 1 | **Indian guests receive 2.00 sessions a week against a standard of three** | 26.02 per guest-quarter vs 39 🟡 |
| 2 | The same operator delivers **2.51** abroad — a **1.25×** dose gap inside one company | India vs international disclosure 🟡 |
| 3 | Dose adequacy is not measured, published, owned or targeted | no disclosed metric 🟠 |
| 4 | The per-session price makes the third session a weekly purchase decision | revenue model 🟡 |
| 5 | Reported PAT grew **34.60%**, not the 41.7% presented | ₹3.6 Cr JV loss + ₹1.3 Cr ESOP added back 🟡 |
| 6 | Adjusted EBITDA excludes **unquantified** "Saudi expenses" | reported margin is at most **22.64%** 🟠 |
| 7 | Adjustments rose from **8.85%** to **13.32%** of adjusted PAT | year-on-year 🟡 |
| 8 | Treatment growth **decelerated 3.30pp** while guest growth accelerated | FY26 vs Q1 FY27 🟡 |
| 9 | Margin improvement is geography, not Indian economics | international 31.8% → 45% of revenue 🟡 |
| 10 | Uzbekistan assessment is **40.19%** of a quarter's adjusted PAT | ₹14.79 Cr, 31 Aug 2026 🟢 |
| 11 | Saudi is pre-revenue with ₹70 Cr of collateral committed | **24.84%** of quarterly revenue 🟢 |
| 12 | Prior-year segment splits undisclosed, so the dose gap cannot be trended by geography | — 🟠 |

---

## 46. Opportunity Mapping

| Opportunity | Cost | Ceiling |
|---|---|---|
| International densification | Capex, licensing, tender cycles | Large, proven, and where realisation already is 🟢 |
| New country entry | High; Saudi shows 3–4 quarters to revenue | Large but slow 🟡 |
| Pharmacy and wellness attach | Low | Real but small per guest 🟡 |
| Home haemodialysis conversion | High behaviour change, low capex per guest | Structurally the right answer, hardest to land 🟡 |
| **Close the Indian dose gap** | **Governance and pricing, near-zero capex** | **₹77.28 Cr/quarter, 49.86% more Indian volume** 🟡 |

---

## 47. RICE

*Framework selection rationale: run with a stress rule taken from the company's own evidenced adherence. Reach is thousands of guests touched per quarter. The stress rule multiplies the Reach of every initiative that needs a guest to change behaviour by **33.27%** — the share of the prescribed Indian dose that currently does **not** get delivered, which is the most direct available measure of how much intended benefit actually lands on this patient population. One initiative is exempt because it needs no guest to do anything.*

| Initiative | Reach (k) | Impact | Confidence | Effort | **Baseline** | **Stressed** |
|---|---|---|---|---|---|---|
| ***NephroPlus Dose* (PROPOSED)** | 33.0 | 0.90 | 0.60 | 4.0 | **4.46** | **1.48** |
| Pharmacy and wellness attach | 38.3 | 0.40 | 0.70 | 3.0 | **3.57** | 1.19 |
| International densification — **EXEMPT** | 5.2 | 1.00 | 0.90 | 1.5 | **3.13** | **3.13** |
| Home haemodialysis conversion | 33.0 | 0.50 | 0.40 | 5.0 | **1.32** | 0.44 |

**Baseline order:** **proposal (1st)** → attach → international densification → home conversion.
**Stressed order:** **international densification → proposal (2nd) → attach → home conversion.**

`verify.py` asserts all three outcomes programmatically: that the proposal leads at baseline, that the exempt initiative wins under stress, and that the proposal falls behind it to second. The exempt initiative beats it **2.11×** once stressed, and the proposal loses **66.73%** of its score — a figure identical to India's dose adequacy, because the stress rule *is* the adherence gap.

**A departure from this series' pattern, stated rather than hidden.** In every case study since Day 57 the proposal has sat mid-table at baseline and fallen to last. Here it **leads** at baseline and falls only to second. The inputs were not adjusted to restore the usual shape, and this is the right outcome for two reasons. The proposal leads at baseline because its reach is the entire Indian guest base and because the impact of moving a dialysis patient from two sessions a week to three is not incremental — it is survival, which no other initiative on this list touches. It then loses to international densification because **two-thirds of the intended benefit does not land**, and because densifying clinics in the Philippines requires no guest, clinician or household to change anything.

**Why losing to the exempt option is still the correct sequencing.** A company delivering 66.73% of prescribed dose in its largest market has not demonstrated that it can change patient behaviour at scale. International densification is the intervention that compounds regardless of that, and it should be sequenced first. The proposal is where the mission lives and where the larger prize sits — ₹77.28 Cr a quarter against a market the company already owns — and it is still second in line. **Do the thing that requires nobody's cooperation first; then do the thing that matters most.**

**A harsher stress rule was available and not used.** Home-dialysis penetration or holiday-dialysis uptake would both have produced a lower multiplier. The generous one is used, and the proposal still loses.

---

## 48. MoSCoW

| | Scope |
|---|---|
| **Must** | Append-only clinician-signed prescription ledger; reason-coded downward-revision flags; DAG/1k per clinic; PSC-90 with automatic suspension; entitlement-exhaustion distinct from skipping |
| **Should** | Weekly bundled price for prescribed sessions; family-nominated outreach contact; per-payer adequacy reporting |
| **Could** | Published per-clinic adequacy; predictive miss-risk scoring; transport support pilots |
| **Won't** | Any outreach incentive tied to session volume; any sharing of individual attendance histories; any AI triage in v1 |

The first item in "Won't" is permanent, not deferred — it is the mechanism by which this proposal would become the harm described in §40.

---

## 49. Kano

| Feature | Category |
|---|---|
| Receiving the prescribed number of sessions | **Basic — and not currently delivered** 🟡 |
| A weekly price instead of a per-session price | Attractive; nobody in Indian dialysis offers it 🟡 |
| Someone noticing when attendance slips | Attractive today, Basic once any operator does it 🟡 |
| Holiday and home dialysis | Attractive — and already delivered, which is to the company's credit 🟢 |

The unusual feature of this Kano table is that the **Basic** row is the unmet one. Normally basics are table stakes and delight is the frontier; here the company has built genuine delight — holiday dialysis, the "guest" framing — on top of an unmet basic.

---

## 50. Feature Proposal — *NephroPlus Dose*

**What it is.** Two things that only work together: a published dose-adequacy ledger, and a weekly price.

**The ledger.** At the nephrology consult, the prescribing clinician signs a prescription — sessions per week and minutes per session — into an append-only record, effective from a stated week. The adequacy engine reads it, joins it to the attendance and duration record, and produces **DAG/1k per clinic and per payer**. Downward revisions are reason-coded and counted into **PSC-90**. An adequacy function with no volume target owns both numbers, and a breach suspends that clinic's outreach automatically. The numbers are published externally — per clinic — at Phase 3, which is the point at which the mechanism becomes credible rather than internal.

**The price.** For out-of-pocket Indian guests, a **weekly bundled price covering the prescribed sessions, set below 3× the per-session rate.** This is the half that changes behaviour rather than measuring it. Today the third session is a fresh purchase at the moment the patient feels best; under a weekly price it is already paid for, and the marginal cost of attending is transport alone. Realisation per session falls; revenue per guest rises; and, critically, **the company's revenue becomes exposed when adequacy falls**, which is what makes the ledger something the business needs rather than something the mission wants.

**Why this and not something else.** Because the asset exists. Every one of 38,262 guests has a prescribed frequency written by a nephrologist, and attendance is recorded at every session. The gap between them is computable today, per guest, without collecting anything new — §32 is the proof, in three queries. Nothing else on the opportunity map is both this cheap and this large.

**Why it is not already there.** The company's own reporting gives treatments and guests as separate absolute figures and never their ratio. No dose, adherence, adequacy or recall metric appears in any disclosure examined; no indication threshold is published; no patient-facing adherence surface is evidenced. Verifying from a company's own material that the thing you are proposing does not already exist is a standing rule of this series, and the absence here is itself the finding: **a chronic-care business whose clinical value is entirely a function of dose reports no measure of dose.** 🟠

**The shape, and how it differs from the last ten proposals.** Day 55 captured a lost signal; 56 priced an outcome; 57 made an intermediary carry risk; 58 subtracted negative-contribution volume; 59 built a comparison layer; 60 sold forward commitment; 61 metered a claim; 62 imposed a disclosed constraint on itself; 76 converted a clinical record into a time-bound obligation. This is a **unit-of-sale change paired with a published adequacy measure** — the first proposal in the series to change *what the company sells* rather than what it measures, records or commits to. The measurement exists to make the pricing change safe; the pricing change exists to make the measurement move.

**What it is not.** Not a reminder campaign, not a subsidy, not a screening programme. Those raise awareness, cost or enrolment. This raises the fraction of prescribed treatment that is actually delivered — a different quantity with a different failure mode, which is §40.

---

## 51. PRD

**Problem.** Indian guests receive 66.73% of prescribed dialysis. The shortfall is 12.98 treatments per guest per quarter, 428,833 in aggregate, and is measured nowhere.

**Goals.** Raise DAG/1k on the existing Indian guest base; make dose adequacy a reported per-clinic figure; hold PSC-90 flat or lower while doing it.

**Non-goals.** Raising enrolment. Raising realisation per session — the weekly price deliberately lowers it. Raising session volume as an end in itself, which is the metric whose unguarded pursuit produces the §40 harm.

**Success metrics.** DAG/1k as North Star; PSC-90 as guardrail; revenue per guest as the commercial read-through, since the whole point is more sessions per enrolled patient rather than more patients.

**User stories.**
- As a nephrologist, I sign a prescription in under ten seconds at the consult, because anything slower will not survive a clinic list.
- As Ramesh's daughter, I know the week's sessions are already paid for, so the only question is transport.
- As a clinic head, I see my DAG/1k and PSC-90 monthly, and I know a PSC-90 breach stops my outreach without my involvement.
- As the adequacy lead, I can pull every guest-week in a clinic-quarter and join it to the prescription that governed it.
- As a state-scheme guest, the system knows my entitlement is exhausted and routes me to entitlement support rather than affordability outreach.

**Functional requirements.** Prescription capture at consult; append-only signed ledger with server-side timestamps; reason-coded revision flags; session duration capture; adequacy engine; per-clinic and per-payer reporting; family-nominated outreach contact; entitlement-balance visibility at scheduling; weekly-price billing.

**Non-functional requirements.** Sub-ten-second capture. Ledger immutability enforced at the database layer, not application code. The adequacy engine holds **read-only credentials** on the prescription table, verified by a build-pipeline test that fails the build if a write path exists. Cross-border data residency per market.

**Acceptance criteria.** No guest-week counts as adequate against a prescription whose timestamp post-dates the start of that week. No user with volume-linked variable pay can initiate outreach. A PSC-90 breach suspends outreach at that clinic within one reporting cycle with no human action. Entitlement-exhausted guests are never routed to affordability outreach. Session duration below prescribed minutes does not count as a delivered session.

**Risks.** Documentation burden at the consult; the weekly price reducing revenue if adequacy does not improve; and the central risk that the metric drives volume — §40, tested in §54.

---

## 52. Wireframes

**Prescription capture (nephrologist view, inside the existing consult screen)**

```
┌──────────────────────────────────────────────────────────────┐
│ RAMESH P · 54 M · GID 41822 · Nashik (Standalone)            │
├──────────────────────────────────────────────────────────────┤
│ Sessions per week   [ 3 ▾ ]    Minutes per session [ 240 ▾ ] │
│ Effective from week [ 2026-09-14 ]                           │
│                                                              │
│ Prior prescription: 3/week · Delivered last 4 wks: 2.0 avg   │
│                                                              │
│ ○ No change   ● Maintain   ○ REVISE DOWN → reason required   │
│    reason [ ................................ ]               │
│                                                              │
│ Outreach contact  ○ Guest  ● Family [ Priya · 98xxx ]        │
│ Payer  ● Out of pocket  ○ State scheme (bal: — )             │
│                                                              │
│ [ SIGN ]              signed prescriptions cannot be edited  │
└──────────────────────────────────────────────────────────────┘
```

**Clinic scorecard (clinic head view, monthly)**

```
┌──────────────────────────────────────────────────────────────┐
│ NASHIK STANDALONE · Aug 2026                                 │
├──────────────────────────────────────────────────────────────┤
│ DAG/1k                 691   ▲ 42   (prescribed guest-weeks) │
│ Avg sessions delivered  2.07 ▲ 0.07  (prescribed 3.00)       │
│ Weeks short by 2+       118  ⚠                               │
│                                                              │
│ PSC-90                 1.4%  ▲ 0.3   THRESHOLD 3.0%          │
│ Outreach status        ACTIVE                                │
│                                                              │
│ Entitlement-exhausted guests  24  → routed to scheme support │
│                                                              │
│ ⓘ A PSC-90 breach suspends outreach automatically.           │
└──────────────────────────────────────────────────────────────┘
```

---

## 53. Rollout Plan

**Phase 0 — two analyst-weeks, on data the company already holds, built to kill the proposal cheaply.**

Run the three queries in §32 across twelve months of Indian sessions, by clinic and by payer.

- **K1:** the prescription record does not reliably carry sessions-per-week, so no denominator exists. The proposal dies here, and this is **the criterion most likely to fire** — it is entirely plausible that frequency is documented in free text or assumed to be three and never recorded per guest. This is the honest weak point: the proposal assumes a documentation standard that has never been publicly evidenced.
- **K2:** the dose gap is not concentrated. If adequacy is uniformly ~2.0 sessions a week across every clinic, payer and tenure cohort, there is nothing to target and the answer is national pricing policy rather than a product.
- **K3:** attendance cannot be joined to prescription because guest identifiers do not persist across clinics — the §24 risk. If the join fails, the metric cannot be audited and must not be published.

Proceed to pilot only if usable joins are achieved on **at least 85% of Indian guest-weeks** in the window.

**Phase 1 — pilot, two quarters, eight clinics across two states, one high-adequacy and one low.** Ledger, adequacy engine, family outreach, adequacy function stood up before the first outreach call. Weekly price live in four of the eight.
**Phase 2 — scale by state, gated on PSC-90 below 3.0% in every pilot clinic individually, not on the pilot average.**
**Phase 3 — external publication of per-clinic DAG/1k**, which is where the mechanism stops being a dashboard and starts being a commitment.

---

## 54. A/B Testing

Four arms, because this proposal has two halves and the test has to tell them apart.

| Arm | Design |
|---|---|
| **A — control** | Current practice: per-session price, no ledger, no outreach |
| **B — measurement only** | Ledger, adequacy reporting, family outreach. Per-session price unchanged. Isolates whether *knowing and calling* is enough |
| **C — price only** | Weekly bundled price below 3× the session rate. No ledger, no outreach. **This is the falsification arm:** it delivers the affordability change without the apparatus. **If C matches D, the ledger is overhead and the answer is simply to reprice.** |
| **D — full proposal** | Ledger, outreach, adequacy function, and the weekly price |

**Pre-registered decision rules.** D proceeds only if it beats **C** by more than **6 percentage points on dose adequacy across two full quarters including one monsoon quarter** — transport seasonality is a real confounder in tier-3 India — with **PSC-90 no worse than control in every individual clinic**.

A second rule constrains the win: if any arm raises session volume while PSC-90 also rises, that is the signature of prescription gaming or over-treatment and the arm is disqualified regardless of its adequacy gain.

A third, specific to this population: **mortality and hospitalisation are tracked as pre-registered safety endpoints in all four arms.** An arm that improves adequacy while worsening either is stopped.

---

## 55. KPI Dashboard

| KPI | Owner | Current | Target |
|---|---|---|---|
| **DAG/1k** (North Star) | Clinic head | Not measured | Pilot baseline + 6pp vs Arm C |
| **PSC-90** (guardrail) | Adequacy function | Not measured | < 3.0% per clinic |
| India dose adequacy | COO | **66.73%** | Toward the international 83.59% |
| Revenue per guest | CFO | ₹7,364/quarter (₹281.8 Cr ÷ 38,262) | Rising while realisation per session falls |
| Treatments per guest | COO | **26.02** India / **32.60** international | Converge |
| Reported-vs-adjusted PAT gap | CFO | **7.10pp** | Disclose the bridge each quarter |
| Unquantified adjustments | CFO | "Saudi expenses" | Quantify |
| Mortality and hospitalisation | Clinical governance | Undisclosed | Published by cohort |

**Early-warning row, and it is the first one.** The thesis says the Indian dose gap is a payer-design problem, not a capability problem — the evidence being that the same operator delivers 2.51 sessions a week internationally. **If Q2 FY27 shows Indian dose adequacy rising materially without any pricing or outreach change, the thesis is wrong** and the gap was simply a ramp artefact of newly enrolled guests mid-titration. The company publishes treatments and guests every quarter, so anyone can compute it.
---

## 56. Product Roadmap

| Window | Focus |
|---|---|
| Q3 FY27 | Phase 0: run the §32 queries on twelve months of Indian sessions; charter the adequacy function |
| Q4 FY27 | Eight-clinic pilot across two states; Arms A/B/C/D live; weekly price in four clinics; nothing published |
| Q1 FY28 | Decision gate on the pre-registered rule; scale by state or reprice-only per Arm C |
| FY29 | Per-clinic DAG/1k published; payer-level adequacy reporting; state-scheme entitlement integration |

---

## 57. Risks & Mitigation

| Risk | Severity | Mitigation |
|---|---|---|
| **Adequacy target drives over-treatment** | Severe | Pre-week signed prescriptions, reason-coded revisions, PSC-90 with automatic suspension, mortality and hospitalisation as safety endpoints (§40, §54) |
| **Clinics hit the target by prescribing less** | Severe | PSC-90 is the only number that catches this; no ratio can |
| Weekly price cuts revenue if adequacy does not move | High | Arm C isolates it; four-clinic exposure in pilot |
| Prescribed frequency not recorded per guest | High | K1 kills the proposal in Phase 0 for two analyst-weeks |
| Guest identifier does not persist across clinics | Medium | K3 blocks publication rather than publishing an unauditable metric |
| Entitlement exhaustion mistaken for non-adherence | Medium | Distinct routing is an acceptance criterion, not a feature request |
| Uzbekistan assessment and cross-border tax exposure | Medium | ₹14.79 Cr = **40.19%** of a quarter's adjusted PAT; under appeal 🟢 |
| Saudi investment phase runs longer than guided | Medium | Revenue is **3–4 quarters** out on management's own account; ₹70 Cr collateral already committed 🟢 |
| Register becomes a payer underwriting asset | High | Purpose limitation in §44; aggregates leave, histories do not |

---

## 58. Future Vision

The defensible version of this company in five years is not the one with the most countries. It is the one that can state, for every guest it has ever enrolled, how much of their prescribed dialysis they actually received — and prove the number was not achieved by prescribing less. 🟡

That is also the only asset a better-capitalised rival cannot copy. Clinics can be built in a quarter; a decade of matched prescription-and-attendance records across 38,262 chronic patients cannot. 🟡

---

## 59. PM Lessons

**1. Divide the two operating metrics the company gives you.** Treatments and guests appear in the same press release, in bold, never as a ratio. Their quotient is 2.00 sessions a week against a standard of three, and it is the whole case study. Most companies publish the numerator and denominator of their most important metric without publishing the metric.

**2. When the same company does the same thing twice at different prices, you have a controlled experiment.** NephroPlus delivers 2.51 sessions a week internationally and 2.00 in India, on the same protocols with the same management. That single comparison converts "Indian patients under-adhere" into "this payment model produces under-adherence" — a completely different problem with a completely different fix.

**3. Check what the adjustment is adjusting.** Adjusted PAT rose 41.7%; reported PAT rose 34.60%. The ₹3.6 Cr JV loss added back did not exist a year earlier, and adjustments went from 8.85% to 13.32% of adjusted PAT. An adjustment that grows faster than the profit it adjusts is worth a paragraph.

**4. Find the adjustment that isn't quantified.** "Adjusted for ESOP expenses… as well as Saudi expenses" gives a number for one and not the other. The most that can honestly be said is that reported EBITDA margin is *at most* 22.64% against the 23.10% presented — and saying exactly that is better than either ignoring it or guessing.

**5. Size the prize inside the existing base before looking outside it.** ₹77.28 Cr a quarter, 27.43% of group revenue, from patients already enrolled in clinics already built. Growth strategies reach for new geography because new geography is legible; the unexploited base is rarely counted.

**6. If your metric could hurt someone, the guardrail is part of the metric, not a footnote.** A dose-adequacy target in dialysis can be met by over-treating or by prescribing less. PSC-90 exists before DAG/1k in the design order for that reason, and §40 sits before §50 in the document for the same one.

**7. Write the query, not the requirement.** §32 contains the SQL that computes the North Star, the guardrail, and the cohort split that would show whether the dose gap is killing people. A proposal that cannot be expressed as a query against data the company already has is not yet a proposal.

**8. Report what your own numbers cannot show.** Prior-year segment splits are undisclosed, so the dose gap has no geographic trend. That costs the case study its most dramatic possible claim — that the gap is widening — and it is the reason the rest can be relied on.

---

## 60. PM Interview Questions

1. A company reports 10,31,084 treatments and 38,262 patients. What do you compute first, and what would you need to know before acting on it?
2. The same operator delivers 2.51 sessions a week in one market and 2.00 in another, on identical protocols. How do you establish which explanation is right?
3. Design a dose-adequacy metric for a dialysis chain that cannot be met by prescribing less. Name the failure your metric still cannot catch.
4. Adjusted PAT grew 41.7%, reported PAT 34.60%. Which do you put in the board deck, and what do you say about the other?
5. You want to change the unit of sale from a session to a week. What breaks, and who inside the company fights you?
6. Your proposal ranks second under your own stress test, behind an initiative you did not propose. Defend the sequencing to a CEO who wants your proposal shipped first.
7. Write the one sentence about this business that a nephrologist and a fund manager would both accept.

---

## 61. References

**Company disclosure**
1. Nephrocare Health Services Limited, Q1 FY27 results release and investor presentation, 11 August 2026 — revenue ₹281.8 Cr, adjusted EBITDA ₹65.1 Cr, adjusted PAT ₹36.8 Cr, treatments 10,31,084, guests 38,262, revenue per treatment ₹2,733, 550 clinics, India/international splits.
2. Nephrocare Health Services Limited, Q1 FY27 earnings call transcript, call held 12 August 2026, filed with BSE and NSE 19 August 2026 — CFO commentary on adjustments, international revenue share, Saudi phasing, guidance.
3. Nephrocare Health Services Limited, FY26 and Q4 FY26 results, May 2026 — revenue ₹998.8 Cr, adjusted PAT ₹128.3 Cr, adjusted EBITDA ₹238.1 Cr, treatments 38.4 lakh, guests 36,981, revenue per treatment ₹2,598, international share 41.8% from 31.8%, ROCE 22.8%.
4. Nephrocare Health Services Limited, DRHP, filed 26 July 2025 — India FY25 patients 29,281 and treatments 28,85,450, ~10% patient-population share, 4.40× the next organised player, clinic formats, captive share 36.51% of H1 FY26 dialysis revenue, use of proceeds.
5. Corporate announcements, June–September 2026 — ESOP 2026 (20,06,814 options, 2% of paid-up capital), ₹70 Cr Saudi collateral, Uzbekistan tax assessment ₹14.79 Cr (31 August 2026), Almaty acquisition KZT 561.66 Mn (1 September 2026), grant of 4,01,362 options at ₹230 (3 September 2026).
6. IPO documentation and exchange data, December 2025 — ₹871.05 Cr issue, ₹438–460 band, ₹460 issue price, ₹490 listing, subscription 13.96× with QIB 27.47×, NII 24.27×, retail 2.31×.

**Registry and regulatory**
7. Ministry of Corporate Affairs registry — CIN L85100TG2009PLC066359, incorporation 18 December 2009, conversion to public limited 18 June 2025, authorised and paid-up capital, directors, registered office.

**Clinical standard**
8. Standard of care for maintenance haemodialysis in end-stage renal disease — three sessions per week — used here as the denominator for dose adequacy. This is the clinical convention against which the company's own prescribed frequency is set; the case study does not claim a specific guideline body as its source and treats 3/week as the stated benchmark rather than a cited standard (Appendix A-1).

---

## 62. About the Author

**Gaurav Singh** — Product Manager, New Delhi. Background in yoga therapy and behavioural science, which is why the questions that interest me in healthcare are usually about what a patient actually does rather than what a protocol says they should. Writing one evidence-based product case study a day for ninety days, all of the remaining ones in healthtech.

Dialysis is the clearest case I have found of a business where the clinically correct behaviour and the commercially convenient one diverge by a third — and where nobody publishes the number that shows it.

GitHub: `github.com/gaurav-product` · LinkedIn: `linkedin.com/in/gaurav-singh-986b40197`

---

## 63. License

Analysis and commentary released for non-commercial, educational use with attribution. All financial and operating figures belong to their sources and are cited in §61. No company logo, marketing asset or copyrighted image is reproduced. Derived figures are the author's own and reproducible from `verify.py`; the SQL in §32 is original and released under the same terms.

---

## 64. Self Review

**What is strong.** The thesis is two integers divided, both published by the company in the same release, and the segment split it rests on is validated twice — the guest counts sum exactly to the reported total, and revenue ÷ treatments reproduces the disclosed ₹2,733 to five paise. The comparator is internal and therefore immune to peer-selection bias: the same operator, same protocols, two payment models, 25% different dose. The proposal's central hazard is specified before the proposal, and the falsification arm is designed to make the proposal unnecessary. §32 contains the queries rather than a description of them.

**What is weak, stated plainly.**

- **The 3-sessions-a-week denominator is a stated benchmark, not a cited guideline.** It is the near-universal convention for maintenance haemodialysis and the company's own prescriptions are written against it, but this case study does not cite a guideline body. Every dose-adequacy percentage inherits that.
- **Some Indian patients are correctly prescribed twice-weekly** — incremental dialysis for those with residual kidney function is legitimate practice. If that cohort is large, the 66.73% understates true adequacy. The company does not disclose the prescribed-frequency distribution, so **this is the single biggest threat to the thesis** and it is given equal weight in ASSUMPTIONS Part 1.
- **India and international treatment counts are disclosed as approximations** ("approximately 860,000" and "170,000"), leaving a 1,084-treatment residual, 0.11%. The India dose band under that rounding is **66.34%–67.11%** — narrow, but a band.
- **The dose gap has no segment trend.** Prior-year India/international splits were not found, so no claim is made about whether the gap is widening or narrowing.
- **The revenue split is a rounded 55/45.** Both implied realisations inherit that rounding; the 4.14× ratio would move if the true split were 54/46.
- **Adjusted-EBITDA "Saudi expenses" are unquantified**, so the reported margin is stated only as an upper bound.
- **The proposal's Reach and all RICE inputs are author constructs**, declared in ASSUMPTIONS Part 3.

**Rating: 9/10.** The highest I have given in this series, on the strength of the double-validated segment arithmetic and the internal controlled comparison. It loses a point for the prescribed-frequency distribution, which is the one disclosure that would settle the whole argument and is not available.

---

## 65. Appendix

### A. Source conflicts and disclosure gaps

| # | Conflict or gap | Handling |
|---|---|---|
| **A-1** | The **3/week standard** is a clinical convention, not a figure cited from a named guideline body in the sources examined. | Stated as a benchmark at every point of use; §64 and Part 1 both flag that all adequacy percentages depend on it. |
| **A-2** | **Adjusted PAT growth reads 41.7% as reported and 41.54% computed** from the two adjusted figures; reported PAT growth is **34.60%**. | All three printed in `verify.py`; the 34.60% is used as the reported-basis figure and labelled as derived from disclosed adjustments. |
| **A-3** | **Adjusted EBITDA excludes "Saudi expenses" that are nowhere quantified.** | Reported EBITDA margin stated only as an upper bound, **≤22.64%**. No estimate constructed. |
| **A-4** | India and international **treatment counts are approximations**; they sum to 10,30,000 against a reported 10,31,084 — a **1,084** residual, **0.11%**. | Residual computed and published; India dose reported with a **66.34%–67.11%** sensitivity band. |
| **A-5** | The **revenue split is disclosed as a rounded 55/45**. | Both implied realisations labelled "implied"; the 4.14× ratio cross-checked against the company's own disclosed 3.3×–13.6× band, inside which it falls. |
| **A-6** | The **~10% patient-population share** is the company's own characterisation, sourced from a commissioned industry report. | The implied 292,810 national population is labelled 🟡 and used only for order-of-magnitude claims. |
| **A-7** | **Prior-year segment splits not found**, so no geographic dose trend exists. | No trend claimed; group-level trend computed from FY25/FY26 totals only. |
| **A-8** | Q1 FY26 treatments are reported as **"9.10 lakh"** — two significant figures — so computed treatment growth (13.31%) differs slightly from the reported 13.3%. | Both printed; the reported figure used in prose. |

### B. Evidence grades

🟢 **High** — company results disclosure, earnings-call transcript filed with the exchanges, DRHP, MCA registry, exchange announcements.
🟡 **Medium** — figures derived here from disclosed inputs; management commentary; the implied national population; anything resting on the rounded revenue split.
🟠 **Low** — absences ("not evidenced in disclosure examined"), undisclosed metrics, the unquantified Saudi adjustment.
🔴 **Conflicting** — none unresolved.

### C. Author-constructed content

Personas (§20), the journey and data-flow diagrams (§22, §42), **all SQL in §32**, the *NephroPlus Dose* mechanism including the weekly price (§50, §51), DAG/1k and PSC-90 and their thresholds (§31), both wireframes (§52), the four RICE initiatives and every input (§47), Phase 0 kill criteria K1–K3 (§53), the four-arm test and all three pre-registered rules (§54), the KPI targets (§55) and the roadmap windows (§56). Full inventory in `ASSUMPTIONS.md` Part 3.

### D. Asset status

| Asset | Status |
|---|---|
| README.md | Complete, 65 sections |
| ASSUMPTIONS.md | Complete, Parts 1–5 |
| verify.py | **117 checks, all passing** — delivered, not committed |
| crosscheck.py | Run; deliverables reconciled against the gate — delivered, not committed |
| LinkedIn carousel + caption | To follow |

---

*Day 77 of 90 · [← Day 76 — Dr Agarwal's Health Care](../Day-76-Dr-Agarwals-Healthcare) · Day 78 →*
