# Day 79 — Ultrahuman: the AI is free, and so is almost everything else

> Day 78 asked whether Oura's AI could justify a $5.99 subscription. Ultrahuman has answered the question by refusing to ask it. Jade, its real-time "biointelligence" AI, is **free to every user globally**. The Ring Pro ships with "a lifetime subscription to all Ultrahuman Ring PRO features and content… with no hidden fees or recurring charges." Only **12%** of users pay for PowerPlugs, against Oura's **94%** activation-to-paid conversion — a **7.83×** gap. And the FY25 filings show what that costs: **subscription revenue grew 7.4% while smart-ring revenue grew 9.5×**, so software collapsed from **25.81% of revenue in FY24 to 5.14% in FY25**, a fall of **20.68 points**. The profit is thinner than it reads too: reported PAT of **₹71.5 Cr** sits against a PBT of **₹45.7 Cr** computed from the company's own disclosed lines, and the reported tax credit of ₹32.7 Cr is **45.73% of PAT**. Meanwhile Ultrahuman is spending its Series C on the exact capability Day 78's RICE ranked *first* for Oura — moving inference onto owned silicon, here a Qualcomm chip with on-chip machine learning. **It is building the cost advantage without the revenue line that would monetise it.** The market has priced the difference: Oura at **11.23×** trailing revenue, Ultrahuman at **2.61×** ARR — **4.31×** apart. The AI PM question is the inverse of Day 78's: *when inference is free and the AI is free, what exactly are you selling?*

**Author:** Gaurav Singh · **Day 79 of 90** · Written 17 September 2026
**Subject:** Ultrahuman Healthcare Private Limited (CIN U74999KA2019PTC129250), FY25 consolidated financials and the Series C of 3 September 2026
**Verification:** `verify.py` — 84 programmatic checks, all passing

---

## 1. Cover

| | |
|---|---|
| **Product** | Ultrahuman Ring AIR and Ring Pro, the Ultrahuman app, Jade biointelligence AI, and PowerPlugs |
| **Company** | Ultrahuman Healthcare Private Limited, Bengaluru |
| **Domain** | Healthtech — consumer health wearables and AI health intelligence |
| **Period examined** | FY25 (year ended 31 March 2025) consolidated financials, with the position as at September 2026 |
| **Why it matters** | The clearest live experiment in giving health AI away: the direct competitor to Day 78's Oura, running the opposite monetisation strategy in the same category |
| **Proposed feature** | *PowerPlugs Open* — a third-party plug marketplace that runs on-ring, gated by a published evaluation, monetised by revenue share rather than a subscription |
| **Series arc** | Second of 13 closing case studies on AI health products; the mirror of Day 78 (Oura) |
| **Evidence grades** | 🟢 High · 🟡 Medium · 🟠 Low · 🔴 Conflicting |

---

## 2. Repository Metadata

**Legal entity:** Ultrahuman Healthcare Private Limited. **CIN U74999KA2019PTC129250**, registration number 129250, registered with the Registrar of Companies, Bangalore. Registered office: AM Chambers, 2nd and 3rd Floor, Survey No 49/1 and 49/3, Garvebhavipalya, 7th Mile, Hosur Main Road, Bommanahalli, Bangalore 560068. Authorised share capital ₹18,00,000, paid-up ₹7,25,080. Directors include Mohit Kumar, Vatsal Singhal, Abhilasha Bhatnagar and Matthew James Brooklyn. Company status Active. 🟡

**The register misclassification, continued.** The CIN's activity code is **74999 — "Other business activities n.e.c."** For a company that manufactures a health wearable, sells a continuous glucose monitor, runs a blood-testing service and describes itself as a health platform, "other business activities not elsewhere classified" is not the right class. The series has tracked this since Day 46 as a systemic register problem rather than a failure by any individual company; the tally, which stood at **nine wrong of fourteen** after Day 77's correctly-classified NephroPlus, now stands at **ten wrong of fifteen**. 🟡

**A naming caution.** The FY25 press coverage of the viO HealthTech acquisition refers to "Ultrahuman Healthcare Limited, a wholly owned subsidiary." That is a differently-named entity from the Indian holding company examined here. This case study does not attempt to map the group structure beyond the consolidated figures as reported. 🟠

---

## 3. Badges

`Day 79/90` · `Healthtech` · `AI health intelligence` · `Consumer wearables` · `RoC-sourced` · `65 sections` · `84 verified checks` · `0 fabricated figures` · `AI eval plan in §29 and §51` · `Runnable SQL in §32` · `Zero Mermaid — tables and ASCII only`

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
| **Risk, Prioritisation & Proposal** | [40. Trust & Safety](#40-trust--safety) · [41. Technical Architecture](#41-technical-architecture) · [42. Data Flow](#42-data-flow) · [43. API Ecosystem](#43-api-ecosystem) · [44. Privacy & Security](#44-privacy--security) · [45. Pain Points](#45-pain-points) · [46. Opportunity Mapping](#46-opportunity-mapping) · [47. RICE](#47-rice) · [48. MoSCoW](#48-moscow) · [49. Kano](#49-kano) · [50. Feature Proposal — PowerPlugs Open](#50-feature-proposal--powerplugs-open) · [51. PRD](#51-prd) |
| **Execution** | [52. Wireframes](#52-wireframes) · [53. Rollout Plan](#53-rollout-plan) · [54. A/B Testing](#54-ab-testing) · [55. KPI Dashboard](#55-kpi-dashboard) · [56. Product Roadmap](#56-product-roadmap) · [57. Risks & Mitigation](#57-risks--mitigation) · [58. Future Vision](#58-future-vision) |
| **Reflection & Sources** | [59. PM Lessons](#59-pm-lessons) · [60. PM Interview Questions](#60-pm-interview-questions) · [61. References](#61-references) · [62. About the Author](#62-about-the-author) · [63. License](#63-license) · [64. Self Review](#64-self-review) · [65. Appendix](#65-appendix) |

</details>

---

## 5. Executive Summary

Ultrahuman sells smart rings, a continuous glucose monitor, a blood-testing service and a home environmental sensor, and gives away the AI that interprets all of it. In FY25 it reported **revenue from operations of ₹564.7 Cr against ₹104.6 Cr — growth of 439.87%, or 5.40×** — and its first profit, **₹71.5 Cr against a loss of ₹37.7 Cr**. As at September 2026 it reports an **annual revenue run rate of $140 Mn, up roughly 45%**, around **800,000 rings sold** cumulatively, and a **$70 Mn Series C at a $365 Mn valuation** led by Qualcomm Ventures with Labcorp participating. 🟢 / 🟡

**The composition of that growth is the case study.** Of FY25's revenue, smart rings were **₹516 Cr — 91.38%** — having grown **9.5×**. Subscription revenue was **₹29 Cr**, and it grew **7.4%**. Run those two together and the software line, which was an implied **25.81% of revenue in FY24**, is **5.14% in FY25**: a fall of **20.68 points**, with the FY24 share **5.03×** the FY25 one. Ring revenue grew roughly **114.86×** faster than subscription revenue. 🟢 derived

**This is not an accident; it is the strategy, stated.** Jade, launched with the Ring Pro as what the company calls the world's first real-time biointelligence AI, is "available now as a platform upgrade to all Ultrahuman users globally." The Ring Pro is marketed on the promise of "a lifetime subscription to all Ultrahuman Ring PRO features and content… with no hidden fees or recurring charges." The CEO has positioned Jade against what he calls a "backward-looking LLM integration" — which is a fair description of the conversational assistant Oura charges $5.99 a month for. Ultrahuman's wedge against Oura *is* the absence of a subscription. 🟢

**The profit deserves the same scrutiny Day 78 applied to Oura's.** Total income of ₹580.8 Cr less expenses of ₹535.1 Cr gives a **PBT of ₹45.70 Cr**, against a reported PAT of ₹71.5 Cr — so **₹25.80 Cr of the bottom line arrives below the tax line**. Inc42, reading the same filings, reports a **tax credit gain of ₹32.7 Cr**, which is **45.73% of PAT**; strip it out and PAT is **₹38.80 Cr**, or **54.27%** of what was reported. The two tax figures do not reconcile and both are printed here (Appendix A-1). On the operating side the picture is genuinely good: expenses grew 265.51% against revenue's 439.87%, a gap of **174.36 points**, and the company spent **₹0.95 to earn a rupee**. 🟢 / 🔴 A-1

**Where the money comes from has moved fast.** FY25 revenue was **60.95% United States** and **2.67% India**. In the current quarter the company reports the US at about **45%** and India at about **11%** — a **15.95-point** fall and an **8.33-point** rise, the latter being **4.11×** its FY25 level. That shift is not a strategy so much as a consequence: an ITC exclusion order, won by Oura on a patent it acquired, removed Ultrahuman's largest market for much of the year. It returned in 2026 with a redesigned Ring Pro cleared by US Customs, and now reports demand at **18× to 20× available supply**. 🟡

**The AI argument.** Ultrahuman is doing, deliberately and with $70 Mn behind it, the thing Day 78 concluded Oura should do first: move inference off rented frontier models and onto silicon it controls. The Ring Pro already carries a dual-core processor with on-chip machine learning; the Qualcomm partnership extends it. Day 78's RICE put exactly that initiative first for Oura because it protects margin without requiring any member to change behaviour. **The difference is that Oura has a $290 Mn subscription line to protect and Ultrahuman has, on FY25 figures, ₹29 Cr.** Cheap inference is a cost advantage. It only becomes a moat when something is being sold on top of it.

**The proposal, *PowerPlugs Open*,** takes the constraint seriously rather than arguing around it. It does not introduce a subscription — the no-subscription promise is the wedge and breaking it would be strategically illiterate. It turns PowerPlugs into a genuine third-party marketplace whose plugs execute on the ring, where Ultrahuman earns a revenue share rather than a fee, and where **any plug making a health claim must pass a published evaluation before it can be listed.** The North Star counts evidence-passing paid plug-weeks per 1,000 active rings. **In RICE it ranks third of four at baseline and last under stress**, behind expanding US Ring Pro supply — which needs no user to do anything at all. §47 argues why that is the right sequencing when demand is already 18× supply.

---

## 6. Product Overview

Four hardware products and a software layer. **Ring AIR**, the original smart ring. **Ring Pro**, launched 2026, with up to 15 days of battery in Chill Mode and about 12 in Turbo Mode, a dual-core processor with on-chip machine learning replacing the Ring AIR's single core, and a starting US retail price of **$399**. **M1 Live**, a continuous glucose monitor. **Blood Vision**, a blood-testing service covering what the company describes as 120+ biomarkers. **Ultrahuman Home**, an environmental sensor. Above all of them sit the app, **Jade** — free, global, with Standard and Deep Research modes — and **PowerPlugs**, described by the company as "a platform for individual apps and plugins built on top of Ultrahuman's health and wellness data stack." Three PowerPlugs (Respiratory Health, Cycle & Ovulation Pro, Cardio Adaptability) come free for a year with a Ring Pro, a bundle the company values at **$150**. 🟢

---

## 7. Company Background

Founded in 2019 by **Mohit Kumar** and **Vatsal Singhal**, who had previously built the logistics startup Runnr and sold it to Zomato in 2017. The company began with continuous glucose monitoring and moved into smart rings, which became the mainstay. Roughly 300 employees as at August 2025. Total funding reported at **$168 Mn across 11 rounds** by one tracker, with the September 2026 round comprising **$65 Mn of primary equity and $5 Mn of debt** — debt being **7.14%** of the total. Backers include Qualcomm Ventures (lead), Labcorp, Alpha Wave, Blume Ventures, Nexus Venture Partners, Alteria Capital and Deepinder Goyal. 🟡

---

## 8. Product Timeline

| Date | Event | Grade |
|---|---|---|
| 1 Nov 2019 | Ultrahuman Healthcare Private Limited incorporated (date disputed, Appendix A-4) | 🔴 |
| 2021 | Continuous glucose monitoring product launched | 🟡 |
| Aug 2023 | Ring AIR reviewed at launch | 🟡 |
| FY25 (to 31 Mar 2025) | Revenue ₹564.7 Cr, first profit ₹71.5 Cr | 🟢 |
| 27 Mar 2025 | Data breach occurs; affected users informed 2 June 2025 | 🟡 |
| Aug 2025 | ITC rules for Oura against Ultrahuman and RingConn on patents Oura acquired | 🟢 |
| 22 Aug 2025 | Share purchase agreement to acquire viO HealthTech | 🟡 |
| 22 Sep 2025 | Company publishes FY25 results release | 🟢 |
| 21 Oct 2025 | US import ban and cease-and-desist take effect on Ring AIR | 🟡 |
| 27 Feb 2026 | Ring Pro unveiled with Jade; preorders globally excluding the US | 🟢 |
| 24 Mar 2026 | US preorders open after US Customs and Border Protection clearance | 🟡 |
| May–Jun 2026 | Ring Pro ships in the US (date disputed, Appendix A-5) | 🔴 |
| Jun 2026 | M2 Live launches in the US via Abbott's Lingo | 🟠 |
| Jul 2026 | App update with AI-powered health insights; Ring Pro shipping delayed on quality control | 🟠 |
| 3 Sep 2026 | $70 Mn Series C at $365 Mn led by Qualcomm Ventures; Labcorp participates | 🟢 |
| End Sep 2026 | Planned software update: game controller, AI app interaction, third-party developers | 🟡 |

---

## 9. Vision & Mission

The company describes itself as moving from a wearable health company to "a human-computer interface company built around data from the human body," and the CEO frames the goal as making the ring "more like a computer, where programs and algorithms can run on the device itself." Qualcomm's venture head describes Ultrahuman as building "a new generation of personal AI devices." This case study takes that framing at face value and asks the commercial question it raises: a computer platform earns its money from what runs on it.

---

## 10. Problem Statement

**For the user:** a ring, a CGM, a blood panel and a home sensor produce more signals than any person can interpret. Jade is the interpreter, and it is free. **For the company:** the interpreter is free, the AI is increasingly on-device, and the software revenue line is **5.14% of FY25 revenue** and shrinking as a share. **The PM problem:** Ultrahuman is investing heavily in a capability — cheap, private, on-device intelligence — whose entire commercial value depends on something being sold through it, and the only thing currently sold through it reaches **12% of users**.

---

## 11. Market Research

Ultrahuman's own disclosures describe a user base weighted toward women — the CEO has put ring users at **60–65% women**, citing aesthetics and temperature-based ovulation and fertility tracking. That is close to Oura's disclosed **72%**, and it means both leaders in this category are selling primarily to women while competing on patents over the form factor. The company reports **over 500,000 users** as at October 2025, adding roughly **70,000 monthly** and up to **100,000–120,000** in peak seasons, against **around 800,000 rings sold** cumulatively by September 2026. Stated gross margins differ sharply by line: **55% for rings, 32% for M1, 29% for Ultrahuman Home.** 🟡

---

## 12. Industry Analysis

Three forces, read against Day 78. **Patents decide market access, not product quality.** An exclusion order on a patent Oura acquired rather than filed removed Ultrahuman's largest market for roughly a year. **Hardware margin is real but capped** — 55% on rings, against Oura's implied 89% on membership. **Free AI is now the competitive floor**, set not only by Ultrahuman but by the platforms: OpenAI's Health in ChatGPT reaches US users on the Free plan. A company charging for an AI health assistant in 2026 is charging against two kinds of free. 🟢 / 🟡

---

## 13. TAM / SAM / SOM

*Framework selection rationale: run in restricted form, as on Day 78. No primary-sourced market size is used; the market is sized from the company's own disclosed base so that the numbers are auditable.*

| Layer | Definition | Size | Grade |
|---|---|---|---|
| **TAM** (context only) | Global wearables sold, trailing year | ~212 Mn units (IDC, via Oura's S-1) | 🟡 |
| **SAM** | Rings Ultrahuman has sold cumulatively | ~800,000 | 🟡 |
| **SOM** (the question here) | Software revenue actually being earned from that base | Implied **$4.80 Mn a year**, **3.43%** of ARR | 🟡 derived |

That SOM figure assumes every paying PowerPlugs user buys exactly one plug at the implied **$50** annual price derived from the $150 three-plug bundle. It is an order-of-magnitude estimate and labelled as such throughout.

---

## 14. Competitor Analysis

*Restricted to the two companies this series has examined directly, plus the platform. No financial comparison is constructed for Whoop, Samsung or RingConn.*

| | **Ultrahuman** | **Oura** (Day 78) | **Health in ChatGPT** (Day 90) |
|---|---|---|---|
| Hardware | Ring AIR, Ring Pro ($399 from), M1 CGM, Blood Vision, Home | Oura Ring 5 ($399–$499 from) | None |
| AI layer | Jade, real-time, free to all users globally | Oura Advisor, inside a paid membership | The frontier model itself |
| Price of the AI | **Free**, "no recurring charges" | $5.99/month or $69.99/year | Free plan upward |
| Software attach | **12%** pay for PowerPlugs | **94%** of activations convert to paid | n/a |
| Software share of revenue | **5.14%** (FY25) | **19.80%** (9M FY26) | n/a |
| Scale | $140 Mn ARR; ~800k rings sold | $1,424.79 Mn trailing revenue; 5.0 Mn paid members | 300 Mn+ weekly health questions (company figure) |
| Valuation multiple | **2.61×** ARR | **11.23×** trailing revenue | n/a |
| Evidence | 🟡 RoC and interview | 🟢 S-1 | 🟡 company statement |

**What this table says.** Oura is **10.18×** Ultrahuman's revenue scale and is valued at **4.31×** Ultrahuman's revenue multiple. Some of that is size, liquidity and the IPO; but the cleanest structural difference between the two businesses is that one converts **94%** of buyers into recurring software payers and the other converts **12%**. The paid-attach gap is **7.83×** and the software revenue-share gap is **3.86×**. Ultrahuman's free AI is a real weapon against Oura's subscription — and it is also the reason the market values the same category of revenue differently.

---

## 15. SWOT

| Strengths | Weaknesses |
|---|---|
| 439.87% FY25 revenue growth; first profit | Software is 5.14% of revenue, down 20.68 points |
| Rings at a stated 55% gross margin | 12% paid attach on PowerPlugs |
| Free AI as a direct wedge against Oura's subscription | ₹25.80 Cr of PAT arrives below the tax line |
| On-device ML already shipping; Qualcomm silicon funded | US supply at 1/18th to 1/20th of demand |
| **Opportunities** | **Threats** |
| Third-party developers and an SDK already announced | Patent exposure — the ITC order was won on an acquired patent |
| Labcorp partnership on blood-flow plus blood-test signals | Free AI from platforms sets the price floor at zero |
| India at 11% of revenue and rising, 4.11× its FY25 share | Company says it may not be profitable this year |
| M2 Live via Abbott's Lingo | 26.07% of FY25 revenue is geographically unattributed |

---

## 16. Porter's Five Forces

*Framework selection rationale: run as a two-column table against Day 78's Oura reading, because the interesting result is where the two diverge despite identical products and the same category.*

| Force | **Ultrahuman** | **Oura** (Day 78) |
|---|---|---|
| Rivalry | High — and asymmetric: it lost a year of US access to a patent suit | High — but it won that suit |
| New entrants | **Moderate** — Oura's patent wall constrains it too | **Low** — 1,140+ patents and an ITC win |
| Supplier power | Moderate, falling — Qualcomm silicon brings inference in-house | **High** — three frontier model vendors, usage-priced |
| Buyer power | **High** — nothing recurring to churn out of, so every sale is re-won | Low — 85% twelve-month retention on a locked-in subscription |
| Substitutes | Free AI from anywhere, including Oura's own vendors | The same, plus Ultrahuman giving it away |

**The divergence.** Ultrahuman has the better supply-side position — it is not renting its intelligence — and the worse demand-side position, because no recurring relationship exists to retain. Oura is the mirror image. Neither company currently holds both.

---

## 17. Business Model Canvas

| Block | Ultrahuman |
|---|---|
| Customer segments | Health-engaged consumers, 60–65% women; increasingly India and UAE buyers |
| Value proposition | Continuous measurement with interpretation included, and no recurring fee |
| Channels | DTC, and offline stores and performance centres in India and the UAE |
| Revenue streams | Rings 91.38%, subscriptions 5.14%, other 3.54% (FY25) |
| Key resources | Ring form factor and sensing, on-device ML, longitudinal data, Blood Vision biomarkers |
| Key partners | Qualcomm (silicon), Labcorp (diagnostics), Abbott's Lingo (M2 Live), Nordic Semiconductor |
| Cost structure | Materials 32.78% of expenses; selling and distribution up 556%; clinical research; offline retail |

---

## 18. Revenue Model

| Line | FY25 (₹ Cr) | Share | Growth | FY24 implied share |
|---|---|---|---|---|
| Smart rings | 516.0 | **91.38%** | 9.5× | 51.93% |
| Subscriptions | 29.0 | **5.14%** | +7.4% | **25.81%** |
| Other operating | 20.0 | 3.54% | — | — |
| **Revenue from operations** | **564.7** | **100%** | **+439.87%** | |

The three lines sum to ₹565.0 Cr against a reported ₹564.7 Cr, a **₹0.30 Cr** rounding residual. In dollars the company's own release gives $58.4 Mn, $3.2 Mn and $2.2 Mn, summing to $63.80 Mn against a reported $64 Mn, implying a rate of **₹88.23 to the dollar** — the rate used wherever this case study crosses currencies. 🟢 derived

**The single most important line in this table is the FY24 column.** Subscriptions were an implied **25.81%** of revenue in FY24 and are **5.14%** now. Nothing was taken away from customers; the ring business simply grew **114.86×** faster than the software business. A company can look like it is becoming a software business while the opposite happens in the accounts.

---

## 19. Target Users

Health-engaged consumers who want continuous measurement without a watch and without a recurring bill. The company reports 60–65% of ring users are women. Increasingly two geographies matter beyond the US: India, now about 11% of quarterly revenue against 2.67% in FY25, and the UAE, where the company says physical stores drive sales. 🟡

---

## 20. Personas

*Author constructs, built from the company's disclosed user mix. Not interview-based.*

| | **Aditi, 31, Bengaluru** | **Ben, 44, Austin** | **Farah, 36, Dubai** |
|---|---|---|---|
| Why Ultrahuman | Cycle and ovulation tracking; no subscription | Switched from Oura to stop paying monthly | Bought in-store after trying it |
| What she uses | Ring Pro, Cycle & Ovulation Pro plug | Ring Pro, Jade | Ring Pro, Blood Vision |
| What Jade gives her | A real-time read on a temperature shift | An explanation with no bill attached | Biomarker context she cannot interpret alone |
| The commercial problem | Her free plug year lapses and she does not renew | He is the customer Ultrahuman won by charging nothing | Her blood panel is a one-off, not a relationship |

---

## 21. Jobs To Be Done

**When** my body changes, **I want** to know immediately and without paying a toll each month, **so I can** act while it still matters. That is the job Jade is built for and the job the pricing is built for; they agree with each other. The unserved job is the company's own: **when** a user gets value from software, **we want** a durable way to earn from it **without** breaking the promise that won them.

---

## 22. User Journey

| Stage | Today | Friction |
|---|---|---|
| Discover | DTC, or offline stores in India and the UAE | US supply at 1/18th to 1/20th of demand |
| Buy | Ring Pro from $399, three plugs free for a year | High upfront price |
| Use | Jade, free, real-time, all users globally | None — this is the strength |
| Extend | PowerPlugs after the free year | **12% pay** |
| Deepen | Blood Vision, M1, Home | Each is a separate purchase decision |
| Retain | Nothing recurring to retain | **Every future sale is re-won from zero** |

---

## 23. User Flow

Signal changes → Jade explains in real time → user acts → **nothing recurs.** The flow is excellent for the user and structurally inert for the company: there is no step at which sustained value converts into sustained revenue. §50 adds one that does not charge the user a subscription.

---

## 24. Information Architecture

Home · Sleep · Movement · Recovery · Cycle · Blood Vision (biomarkers) · Home (environment) · **Jade** (conversational, real-time, Standard and Deep Research modes) · **PowerPlugs** (a plug catalogue). PowerPlugs is already architected as a platform surface — a catalogue of independent apps over a shared data stack — which is why the proposal in §50 extends what exists rather than inventing a new surface.

---

## 25. UX Audit

Strong: real-time interpretation, no paywall, long battery reducing charge anxiety, and an explicit "no recurring charges" promise that removes a decision the user would otherwise face monthly. Weak, from the business's side: the catalogue has no supply beyond Ultrahuman's own plugs, so its breadth is capped by one roadmap. Not evidenced in the disclosure examined: renewal behaviour after the free plug year lapses.

---

## 26. UI Audit

Not assessed from product screenshots; this case study reproduces no company imagery. The wireframes in §52 are original.

---

## 27. Accessibility

A ring suits people who will not wear a watch, and 15 days of battery reduces the cognitive load of charging — a real accessibility gain for users with memory or routine difficulties. Jade's conversational surface helps users who find charts hard to read. Language coverage for Jade is not disclosed, which matters given India is now about 11% of revenue.

---

## 28. Feature Breakdown

| Feature | Layer | Paid? | Notes |
|---|---|---|---|
| Sleep, movement, recovery scores | App | Included | Core loop |
| **Jade** | AI | **Free, all users globally** | Standard and Deep Research modes |
| AFib detection | AI / clinical | Included | Company claims a first on a smart ring |
| Cycle & Ovulation Pro | PowerPlug | Free for a year, then paid | OvuSense technology |
| Respiratory Health, Cardio Adaptability | PowerPlug | Free for a year, then paid | The other two bundled plugs |
| Blood Vision | Service | Paid per panel | 120+ biomarkers |
| M1 / M2 Live CGM | Hardware | Paid | M2 via Abbott's Lingo |
| Ultrahuman Home | Hardware | Paid | 29% gross margin |
| On-chip machine learning | Silicon | Included | Dual-core in Ring Pro; Qualcomm to follow |

---

## 29. AI Capabilities

The section this case study was chosen for, and the exact inverse of Day 78's. There the question was whether a paid AI earns its price. Here the AI has no price, so the question is what the AI is *for*, commercially.

**What is disclosed.** 🟢 / 🟡

| Item | Disclosure |
|---|---|
| Product | Jade, described as the world's first real-time biointelligence AI |
| Availability | "Available now as a platform upgrade to all Ultrahuman users globally," including the US |
| Price | None. Ring Pro marketed with "no hidden fees or recurring charges" |
| Inputs | 120+ Blood Vision biomarkers, M1 CGM glucose trends, Ultrahuman Home environmental data |
| Modes | Standard and Deep Research |
| Positioning | CEO contrasts it with a "backward-looking LLM integration," likening it to real-time control systems |
| Compute | Ring Pro carries a dual-core processor with on-chip machine learning; Qualcomm silicon to add more |
| Model details | **None disclosed** — no model name, architecture, vendor or training method |
| Data handling | "Processed in a secure system designed to meet applicable data protection standards" |
| Eval or outcome metrics | **None disclosed** |

**The comparison that matters.** Oura's S-1 names its model vendors — OpenAI, Anthropic, Google, webAI — and states the commercial terms. Ultrahuman names none. For an investor that is a disclosure difference driven by one company being public; for a user it is the difference between knowing where your health conversation goes and not. **Neither company publishes a single metric on whether its AI changes anything.**

**The eval plan the free-AI strategy requires.** *Author construct.* Free AI raises the stakes on evaluation rather than lowering them: there is no subscription revenue to fund clinical review, and no paywall to limit blast radius.

| Eval layer | What it measures | How | Pass bar |
|---|---|---|---|
| **Grounding** | Does a real-time claim match the signal it cites? | Automated check of every numeric assertion against the member's own series | ≥99% numeric fidelity |
| **Latency honesty** | Does "real-time" mean acted-on-in-time? | Time from signal to surfaced insight, by mode | Published p50 and p95 per mode |
| **Clinical safety** | Does an AFib or biomarker flag escalate correctly? | Clinician-labelled red-flag set, stratified by condition | Escalation recall ≥95% |
| **On-device parity** | Does the ring-side model agree with the cloud model? | Paired inference on the same window | Disagreement rate published, ≤2% on flagged events |
| **Plug claim integrity** | Does a third-party plug's health claim survive testing? | §50's evidence gate | Binary: listed or not listed |
| **Cost** | Inference cost per active ring per month | On-device vs cloud routing logs | Tracked, and the reason on-device wins |

**Failure modes, ranked by how much they would hurt this business.**

1. **A false AFib or biomarker escalation at scale.** Free means every user has it. There is no paid tier to contain a bad release, and a company with ₹29 Cr of software revenue has no margin from which to fund a recall of attention.
2. **A third-party plug making an unevidenced health claim.** The moment PowerPlugs opens to outside developers, Ultrahuman's brand carries claims it did not write. This is the hazard the proposal is built around.
3. **On-device and cloud models disagreeing.** Two models, one user, different answers — the trust cost is asymmetric and falls entirely on the ring.
4. **"Real-time" as marketing rather than specification.** If p95 latency is minutes, the differentiation against a "backward-looking" assistant is rhetorical.

**Human-in-the-loop design.** Clinician review of a weekly stratified sample of escalations; no plug may issue a medication or treatment instruction; every claim-bearing plug carries a visible evidence badge linking to its evaluation record.

**Cost per interaction.** Not disclosed, and here the direction is favourable: on-chip inference moves marginal cost toward zero. That is precisely why the commercial question is not cost but revenue.

---

## 30. Product Metrics

| Metric | Value | Grade |
|---|---|---|
| FY25 revenue from operations | ₹564.7 Cr, +439.87% | 🟢 |
| FY25 PAT | ₹71.5 Cr (PBT computed ₹45.70 Cr) | 🟢 / 🔴 A-1 |
| Subscription share of revenue | **5.14%**, from an implied 25.81% | 🟢 derived |
| ARR, September 2026 | $140 Mn, +45% | 🟡 |
| Target ARR, January 2027 | $200 Mn — needs **+42.86%** | 🟡 |
| Rings sold, cumulative | ~800,000 (from ~700,000 in February) | 🟡 |
| **PowerPlugs paid attach** | **12%** | 🟡 |
| US share of revenue | 45% now, from 60.95% in FY25 | 🟡 |
| India share of revenue | 11% now, from 2.67% in FY25 | 🟡 |
| Ring gross margin | 55% (M1 32%, Home 29%) | 🟡 |
| Subscription renewal | 75–80% among paying customers | 🟡 |
| CGM retention | 95% | 🟠 |
| **Jade usage, Jade outcome effect** | **Not disclosed** | 🟠 |

---

## 31. North Star Metric

**Proposed: EPW/1k — Evidence-passing Paid Plug-Weeks per 1,000 active rings.**

A plug-week enters the denominator for every 1,000 active rings in the period. It enters the numerator only if **all four** hold:

1. the plug was **paid for** in that week, by the user or by a partner on the user's behalf;
2. the plug **held a current evidence pass** for every health claim in its listing;
3. the ring was **active** — worn and syncing — for at least 80% of the week, so dormant installs cannot inflate it;
4. the plug **executed on-device** for its core function, which is what makes the marginal cost of the week near zero.

**The denominator is the design choice.** It is active rings, not users, not installs and not revenue. Shipping more plugs without paid, evidenced, actually-used weeks lowers the metric. Condition 2 makes evidence a precondition of revenue rather than a cost centre competing with it; condition 4 keeps the platform's unit economics honest as it scales.

**Guardrail, carried to §55: UCR-90 — Unevidenced Claim Rate at the 90th percentile.** In the decile of plugs with the most installs, the share of health claims in listing copy, notifications and reports that have no current evidence pass. Reported by plug and by developer, never in aggregate — an average across a long tail of tiny plugs would hide exactly the plugs that reach the most people.

---

## 32. Product Analytics

*Author construct. The schema is hypothetical; both queries are written in Postgres dialect and were parsed with `sqlglot` before delivery.*

```sql
-- EPW/1k by week
WITH active AS (
  SELECT date_trunc('week', d.day) AS wk, d.ring_id
  FROM ring_days d
  GROUP BY 1, 2
  HAVING SUM(CASE WHEN d.worn_and_synced THEN 1 ELSE 0 END) >= 5.6
),
paid AS (
  SELECT date_trunc('week', p.day) AS wk, p.ring_id, p.plug_id,
         p.paid, p.executed_on_device
  FROM plug_days p
),
ev AS (
  SELECT e.plug_id, e.valid_from, e.valid_to
  FROM plug_evidence_pass e
)
SELECT active.wk,
       COUNT(DISTINCT active.ring_id) AS active_rings,
       COUNT(*) FILTER (
         WHERE paid.paid
           AND paid.executed_on_device
           AND ev.plug_id IS NOT NULL
       ) * 1000.0 / NULLIF(COUNT(DISTINCT active.ring_id), 0) AS epw_per_1k
FROM active
LEFT JOIN paid ON paid.ring_id = active.ring_id AND paid.wk = active.wk
LEFT JOIN ev ON ev.plug_id = paid.plug_id
            AND ev.valid_from <= active.wk
            AND ev.valid_to > active.wk
GROUP BY active.wk
ORDER BY active.wk;
```

```sql
-- UCR-90: unevidenced claims among the most-installed plugs
WITH reach AS (
  SELECT plug_id,
         NTILE(10) OVER (ORDER BY install_count) AS decile
  FROM plug_catalogue
)
SELECT c.developer_id,
       c.plug_id,
       AVG(CASE WHEN c.is_health_claim AND NOT c.has_current_evidence_pass
                THEN 1.0 ELSE 0.0 END) AS unevidenced_claim_rate,
       COUNT(*) AS claims_reviewed
FROM plug_claim_audit c
JOIN reach r ON r.plug_id = c.plug_id
WHERE r.decile = 10
GROUP BY c.developer_id, c.plug_id
ORDER BY unevidenced_claim_rate DESC;
```

---

## 33. AARRR

*Framework selection rationale: used because Ultrahuman's funnel has a structural hole that a stage-by-stage read exposes immediately — every stage is healthy except the one that recurs.*

| Stage | Evidence | Read |
|---|---|---|
| Acquisition | ~70,000 users a month; offline stores in India and the UAE | Strong, and diversifying away from the US |
| Activation | Jade free from day one; no paywall to cross | Solved by design |
| Retention | 15-day battery; 95% CGM retention | Good on hardware, undefined on software |
| Referral | Not quantified | Not evidenced |
| **Revenue** | **12% paid attach; subscriptions 5.14% of revenue** | **The hole** |

---

## 34. HEART

Happiness — not disclosed. Engagement — not disclosed for Jade. Adoption — Jade shipped to all users globally, so adoption is a distribution fact rather than a product achievement. Retention — 75–80% renewal among the 12% who pay. **Task success — not measured for Jade**, exactly as on Day 78 for Advisor. Two rival companies, opposite pricing, identical blind spot.

---

## 35. Growth Strategy

Management's stated levers: return to previous US volumes next quarter and triple them over the following four; deepen India and the UAE through offline touchpoints; extend the ring into a computing platform with Qualcomm silicon and a third-party SDK; and work with Labcorp on combining ring blood-flow signals with blood-test data. The company has said it may not be profitable this year as a result. That is a defensible trade, and it makes the revenue question in §39 more urgent, not less.

---

## 36. Growth Loops

The working loop is hardware-led: ring sells, Jade makes it useful for free, the user tells someone. There is no loop in which software revenue funds better software. The proposed loop: third-party developers build plugs → plugs make the ring more useful → more rings sell → a larger installed base attracts more developers. **That loop is the standard platform loop, and it is the only one available to a company that refuses to charge a subscription.**

---

## 37. Network Effects

Currently near zero, as for Oura. A developer marketplace is the one mechanism that would create a genuine two-sided effect in this category, and Ultrahuman has announced the SDK that starts it. Whether it becomes an effect or a catalogue depends entirely on whether developers can earn.

---

## 38. Product Strategy

Two coherent strategies exist. **Hardware-only:** keep everything free, win share from Oura on price-of-ownership, accept that software is a feature. That is roughly what is happening, and 45% growth without the US for much of the year says it is not failing. **Platform:** treat the ring as a computer, as the CEO says, and earn from what runs on it. The second is the only one that gives the Qualcomm investment a revenue line, and it is the one this case study argues for — because the company has already committed the capital that only pays off under it.

---

## 39. Monetization

Today: hardware margin (55% rings, 32% M1, 29% Home), one-off services (Blood Vision), and a small subscription line at 5.14% of FY25 revenue with 75–80% renewal among the 12% who pay. The implied arithmetic: 12% of ~800,000 rings is **96,000 paying users**; at the **$50** per-plug annual price implied by the $150 three-plug bundle, that is **$4.80 Mn a year — 3.43% of ARR**. 🟡 derived

**The constraint that any proposal must respect.** The Ring Pro's promise of "a lifetime subscription… with no hidden fees or recurring charges" is not marketing decoration; it is the wedge against Oura and it was paid for with the software revenue share that collapsed from 25.81% to 5.14%. Any monetisation that introduces a recurring Ultrahuman fee spends the asset. **Revenue share on third-party software does not**, which is why §50 goes there.

---

## 40. Trust & Safety

*Placed before the proposal, as on Day 78, because the proposal invites third parties to make health claims to hundreds of thousands of people.*

**Hazard 1 — the brand carries claims it did not write.** The moment an outside developer ships a plug that says "this improves your heart rate variability," Ultrahuman's ring is making that claim. The evidence gate in §50 exists for this hazard and UCR-90 measures whether it holds.

**Hazard 2 — free AI has no containment layer.** Jade reaches every user globally with no paid tier and no staged cohort. A safety regression ships to everyone at once. Phase 0 in §53 therefore tests the gate against plugs that already exist before any third party is admitted.

**Hazard 3 — the data breach precedent.** A breach occurred on 27 March 2025 and affected users were told on 2 June 2025, more than two months later. Opening a developer platform multiplies the number of parties touching health data. Any marketplace must ship with disclosure timelines contractually fixed for developers, because the company's own record on notification speed is the thing a regulator will read first.

**Hazard 4 — on-device does not mean private by default.** On-chip inference genuinely reduces data movement, which is a real privacy gain. It also makes what *does* leave the ring harder for a user to see. A published routing rule — what runs on the ring, what reaches Ultrahuman, what reaches a developer — is the minimum.

**What is not alleged.** This case study makes no claim that any Ultrahuman product is unsafe. Jade's clinical performance is not disclosed, which is the point: absence of evidence is treated here as absence of evidence, not as evidence of a problem.

---

## 41. Technical Architecture

Disclosed: Ring Pro carries a dual-core processor with on-chip machine learning, replacing the Ring AIR's single core; Nordic Semiconductor chips are in use today and will continue alongside Qualcomm silicon; a software update was planned for end-September 2026 to add game-controller behaviour, AI-application interaction and third-party developer access. *PowerPlugs Open* adds four components: a plug runtime sandbox on the ring, an evidence-pass registry, a claims scanner that reads listing and notification copy, and a revenue-share ledger.

---

## 42. Data Flow

```
Ring sensors ──► on-chip ML (dual-core) ──► phone ──► cloud history
                        │                                    │
                        ▼                                    ▼
                  Jade real-time  ◄──────────────  Blood Vision · M1 · Home
                        │
                        ▼
        ┌──── plug runtime (on-ring sandbox) ────┐
        │                                        │
   evidence registry ──► claim scanner ──► listing allowed?
        │                                        │no
        │yes                                     ▼
        ▼                                  delisted, developer notified
   paid plug-week ──► revenue-share ledger ──► EPW/1k
```

---

## 43. API Ecosystem

The SDK is announced rather than shipped, which makes this the right moment to design its economics. Disclosed partners: Qualcomm on silicon, Labcorp on combining blood-flow signals with blood-test data, Abbott's Lingo behind M2 Live. The Labcorp relationship is the one with the clearest plug shape — a diagnostics partner is exactly the kind of developer who can fund an evidence pass and would benefit from carrying one.

---

## 44. Privacy & Security

Disclosed: data "processed in a secure system designed to meet applicable data protection standards," and a 2025 breach with a two-month notification lag. On-device inference reduces data leaving the ring. What is not published, and should be: the routing rule for what leaves the device, the retention period for plug-accessible data, and the notification commitment. For a company whose competitor publishes a named vendor list in an SEC filing, silence here is a competitive disadvantage as much as a governance one.

---

## 45. Pain Points

| Who | Pain | Evidence |
|---|---|---|
| User | Free plug year lapses with no reason to renew | 12% attach |
| User | US Ring Pro unobtainable | Demand 18–20× supply |
| Company | Software is 5.14% of revenue and falling as a share | §18 |
| Company | Profit depends on a tax credit worth 45.73% of PAT | §2 derived |
| Company | No recurring revenue to retain | §33 |
| Company | 26.07% of FY25 revenue geographically unattributed | §4 derived |
| Investor | Valued at 2.61× ARR against a peer at 11.23× | §14 |

---

## 46. Opportunity Mapping

| Opportunity | Size signal | Needs user behaviour change? |
|---|---|---|
| *PowerPlugs Open* marketplace | Turns 5.14% software share into a platform line | Yes — pay, and developers must build |
| Labcorp diagnostic bundle | Partner already signed | Yes — take a blood test |
| India and UAE offline expansion | India 4.11× its FY25 share | Yes — visit a store |
| **US Ring Pro supply** | **Demand at 18–20× supply** | **No** |

---

## 47. RICE

*Framework selection rationale: run with a stress rule taken from Ultrahuman's own disclosed behaviour, mirroring Day 78's method. Reach is thousands of active ring users touched per quarter. The stress rule multiplies the Reach of every initiative that needs a user to do something new by **12.00%** — the disclosed share of users who pay for PowerPlugs, which is the only published measure of Ultrahuman users voluntarily taking an optional, incremental, paid step. One initiative is exempt because it needs no user to do anything.*

| Initiative | Reach (k) | Impact | Confidence | Effort (p-m) | **Baseline** | **Stressed** |
|---|---|---|---|---|---|---|
| India and UAE offline expansion | 300 | 1.5 | 0.70 | 4 | **78.75** | 9.45 |
| Labcorp diagnostic bundle | 250 | 2.0 | 0.60 | 4 | **75.00** | 9.00 |
| ***PowerPlugs Open* (PROPOSED)** | 800 | 2.0 | 0.40 | 10 | **64.00** | **7.68** |
| US Ring Pro supply — **EXEMPT** | 400 | 1.5 | 0.90 | 10 | **54.00** | **54.00** |

**Baseline order:** offline expansion → Labcorp bundle → **proposal (3rd)** → US supply.
**Stressed order:** **US supply → offline expansion → Labcorp bundle → proposal (4th and last).**

`verify.py` asserts all four conditions programmatically: the proposal is third at baseline, last under stress, the exempt initiative wins under stress, and the proposal is the weakest *stressed* initiative at baseline — the only configuration in which it can finish last honestly. The exempt winner ends **7.03×** ahead, and the proposal loses **88.00%** of its score.

**Why this is the right answer.** When demand for your flagship product is running at **18× to 20× your available supply in your largest market**, every plan that asks a customer to do something new is competing against a plan that asks nobody to do anything and converts demand you have already created. Supply expansion needs no developer to build, no user to pay and no evidence gate to work. **Sell the rings you already have buyers for; then build the platform.**

**A harsher stress rule was available and not used.** Renewal behaviour after the free plug year is not disclosed, and any plausible figure for *new* paid conversion after a free period would be below 12%. The more generous disclosed figure is used, and the proposal still finishes last.

**Sensitivity.** Applying the company's stated **75%** subscription renewal rate as a gentler stress instead, the proposal scores 48.00 against Labcorp's 56.25 and offline expansion's 59.06 — **still last**. The proposal's position does not depend on the harsh rule.

---

## 48. MoSCoW

| Must | Should | Could | Won't |
|---|---|---|---|
| Evidence pass before listing; on-device execution for core function; claim scanner on listing and notification copy; revenue-share ledger | Public evidence record per plug; developer disclosure timelines; staged rollout by install count | Partner-funded evidence passes for diagnostics developers | Any recurring Ultrahuman fee to the user; medication or treatment plugs; using plug outcomes in marketing claims |

---

## 49. Kano

A free real-time health AI is now **must-be** — Ultrahuman set that expectation and the platforms reinforce it. An open plug marketplace is **attractive**: nobody expects third-party software on a ring. "No recurring charges" is **one-dimensional and rising** — the longer Oura charges, the more this is worth.

---

## 50. Feature Proposal — *PowerPlugs Open*

**The one-line version.** Open PowerPlugs to outside developers, run their plugs on the ring, take a share of what they sell, and let nothing that makes a health claim into the catalogue until it has passed a published evaluation.

**Mechanism.**

1. **Admit.** A developer submits a plug: its function, the signals it reads, and every health claim it intends to make in listing copy, notifications and reports.
2. **Scan.** An automated claims scanner extracts claim statements from that copy. Anything asserting a health effect is routed to the gate; anything purely descriptive is not.
3. **Gate.** Each claim needs an **evidence pass**: either a citation to published evidence the plug's method actually implements, or an outcome study run on consenting users under the protocol in §54. Passes expire and must be renewed.
4. **Sandbox.** The plug's core function executes on-ring, inside a runtime sandbox, with a declared signal scope. This is what makes the marginal cost of a plug-week near zero and the data exposure narrow.
5. **Price.** The developer sets the price. Ultrahuman takes a revenue share. **The user never pays Ultrahuman a recurring fee** — the Ring Pro promise survives intact, because the recurring relationship is between the user and the developer.
6. **Display.** Every claim-bearing plug shows an evidence badge linking to its record: what was claimed, what evidence supports it, when the pass expires.
7. **Enforce.** UCR-90 runs weekly. A plug whose claims drift out of evidence is delisted, not fined, and the developer is told which claim failed.

**Why this shape and not another.** Day 78 proposed *Oura Loop* — an n-of-1 verification instrument for a paid AI. This is deliberately a different animal: **a supply-side marketplace with a claim-integrity gate**, aimed at a company whose AI is free and whose problem is revenue rather than proof. Across the series the proposals have been signal capture, outcome pricing, risk participation, subtractive pricing, a comparison layer, a forward-commitment instrument, attestation, a disclosed constraint, a pre-commitment gate, a dose ledger and an evaluation instrument. This is the first that monetises other people's software.

**Why Ultrahuman can build it and Oura cannot easily copy it.** Three things have to be true at once: on-device compute able to run third-party code (shipping in Ring Pro, extending with Qualcomm), an SDK and developer story already announced, and **no subscription of your own to cannibalise.** Oura fails the third test — every third-party plug would compete with the membership it already sells.

---

## 51. PRD

**Problem.** Ultrahuman has committed Series C capital to on-device intelligence while its software revenue line has fallen to 5.14% of revenue, and its strongest commercial promise forbids the obvious fix.

**Goals.** (1) Establish EPW/1k as a reported metric. (2) Create a software revenue line that does not charge the user a recurring Ultrahuman fee. (3) Keep UCR-90 at or below the pre-launch audit baseline measured on Ultrahuman's own plugs.

**Non-goals.** A subscription. Diagnosis or treatment. Medical-device claims. Marketing built on individual plug outcomes.

**User stories.** As a user, I want to know whether a plug's health claim is backed by anything. As a developer, I want a clear, fast path from submission to listing and a predictable revenue share. As a product lead, I want to know which plugs earn and which plugs make claims they cannot support.

**Functional requirements.** Developer submission flow; claims scanner; evidence registry with expiry; on-ring runtime sandbox with declared signal scope; revenue-share ledger; evidence badge UI; weekly UCR-90 audit; delisting workflow with developer notification.

**AI-specific requirements.**

| Requirement | Specification |
|---|---|
| Gate before listing | No claim-bearing plug lists without a current evidence pass |
| Execution | Core function on-device; any cloud call declared in the listing |
| Model disclosure | A plug using a third-party model names it in its listing, as Oura's S-1 does |
| On-device parity | Ring-side and cloud outputs compared on flagged events; disagreement published |
| Escalation | No plug may issue a medication or treatment instruction; red-flag patterns route to Ultrahuman's own escalation copy |
| Cost | Inference cost per active ring per month reported by routing path |
| Rollback | Per-plug kill switch; automatic delisting on a UCR-90 breach |

**Non-functional.** Evidence records public and permanently addressable. Plug data scope declared at install and enforced by the sandbox. Developer breach-notification timelines contractually fixed.

**Acceptance criteria.** A plug cannot go live with an unevidenced health claim; a dormant ring cannot contribute to EPW/1k; a delisted plug stops executing on-ring within 24 hours.

**Risks.** See §57.

---

## 52. Wireframes

```
┌──────────────────────────────────┐   ┌──────────────────────────────────┐
│ PowerPlugs                       │   │ Cardio Adaptability Pro          │
│                                  │   │ by Northlight Labs               │
│  Cardio Adaptability Pro         │   │                                  │
│  Northlight Labs      $4/mo      │   │ Claim: "improves 30-day HRV      │
│  ✓ Evidence pass · runs on ring  │   │ trend in sedentary adults"       │
│  ──────────────────────────────  │   │                                  │
│  Sleep Debt Coach                │   │ Evidence: outcome study,         │
│  Meridian Health      $3/mo      │   │ 2,140 consenting users, 2026     │
│  ✓ Evidence pass · runs on ring  │   │ Pass valid to: 14 Mar 2027       │
│  ──────────────────────────────  │   │                                  │
│  Focus Windows                   │   │ Reads: HRV, sleep stages,        │
│  Kestrel        $2/mo            │   │ movement. Stays on your ring.    │
│  — no health claims made         │   │                                  │
│                                  │   │ [ View evidence record ]         │
│  Jade is included free, always.  │   │ [ Add plug · $4/mo ]             │
└──────────────────────────────────┘   └──────────────────────────────────┘
```
*Illustrative plugs, developers, prices and figures; author construct.*

---

## 53. Rollout Plan

**Phase 0 — three analyst-weeks against plugs Ultrahuman already ships. Built to kill the proposal cheaply.**

| Kill criterion | Test | Kill if |
|---|---|---|
| **K1** | Run the claims scanner over Ultrahuman's own existing plug listings and notification copy. What share of health claims could pass an evidence gate today? | Below 50% — if the company's own plugs cannot pass, the gate is a moat against itself, not against bad developers |
| **K2 — most likely to fire** | Renewal behaviour after the free plug year lapses, on the cohorts old enough to have lapsed. Does paid attach hold, or is 12% an artefact of bundling? | Post-lapse paid conversion below 4% — at that level no revenue share, at any rate, funds a marketplace |
| **K3** | Can a representative third-party plug execute its core function inside the on-ring compute and power budget? | More than 30% of candidate plug types require cloud execution |

**K2 is named as most likely to fire** because the 12% attach figure is measured across a base in which three plugs are given free for a year with every Ring Pro. A bundled free year inflates attach and tells you nothing about willingness to pay. If post-lapse conversion is very low, the honest conclusion is that this user base was assembled on the promise of not paying for software, and a marketplace inherits that.

**Phase 1 — 10 weeks.** Five invited developers, India and UAE users only, evidence gate live, revenue share fixed and published.
**Phase 2 — 16 weeks.** Open submissions; Labcorp as the first diagnostics partner plug; US once supply normalises.
**Phase 3.** On-ring execution required for listing, once the Qualcomm silicon ships.

---

## 54. A/B Testing

| Arm | Treatment |
|---|---|
| A | PowerPlugs as today — Ultrahuman's own plugs, no gate, no third parties |
| **B — falsification arm** | Third-party plugs admitted with **no** evidence gate, claims unreviewed |
| C | *PowerPlugs Open* — third-party plugs behind the evidence gate |

**Arm B is built to make the proposal unnecessary.** If an ungated marketplace produces the same paid attach, the same retention and no measurable rise in unevidenced claims, then the gate is expensive theatre and the right answer is to open the platform and skip it. Arm B is the arm most companies actually ship, which is why it deserves to be tested rather than assumed away.

**Pre-registered rules.**

- **R1:** C proceeds only if UCR-90 in C is **at least 15 percentage points** below B, across two audit cycles.
- **R2:** C must be non-inferior to B on paid attach after 90 days (margin 1.5 points). A gate that protects users by suppressing the market has failed.
- **R3:** Neither B nor C may exceed arm A's baseline rate of clinically-reviewed escalation errors. If either does, both stop.

---

## 55. KPI Dashboard

| KPI | Definition | Watch for |
|---|---|---|
| **EPW/1k** | §31 | Rising while paid attach is flat = install inflation |
| **UCR-90** | §31 | Any plug in the top install decile above baseline |
| Post-lapse paid conversion | Paid after the free plug year | The K2 number; below 4% invalidates the model |
| Developer time-to-list | Submission to listing, p50 and p95 | Above 21 days at p95 and supply dries up |
| On-device execution share | Plug-weeks executed on-ring | Falling = the cost advantage is leaking to cloud |
| Revenue share earned | Ultrahuman's cut, absolute | Against the 5.14% FY25 software share |
| **Early warning for the thesis** | Next reported subscription share of revenue | If it rises above 5.14% without a marketplace, the free-AI strategy is monetising some other way and this case study's premise weakens |

---

## 56. Product Roadmap

| Window | Build | Exit test |
|---|---|---|
| Q1 | US Ring Pro supply expansion (the RICE winner) | US volumes back to prior peak; supply gap below 5× |
| Q1 | Phase 0 on existing plugs and lapsed cohorts | K1–K3 pass, K2 above all |
| Q2 | *PowerPlugs Open* Phase 1, three-arm test, India and UAE | R1–R3 |
| Q3 | Open submissions; Labcorp diagnostics plug | UCR-90 stable; developer time-to-list inside target |
| Q4 | On-ring execution required for listing, with Qualcomm silicon | On-device execution share above 90% |

---

## 57. Risks & Mitigation

| Risk | Likelihood | Mitigation |
|---|---|---|
| K2 fires: 12% attach was a bundling artefact | **High** | Phase 0 kills cheaply, before any developer is recruited |
| No developer supply — the catalogue stays Ultrahuman's | Medium–high | Five invited developers in Phase 1; Labcorp as anchor |
| The gate becomes a bottleneck and developers leave | Medium | Time-to-list on the dashboard; R2 non-inferiority rule |
| A third-party plug harms a user | Low–medium, severe | On-ring sandbox with declared scope; no treatment plugs; R3 |
| Revenue share too small to matter | Medium | Sized against the 5.14% baseline, not against ARR |
| Patent exposure extends to plug functionality | Low | Claim scanner is not a patent review; legal review at admission |
| Opening the platform widens breach surface | Medium | Contractual disclosure timelines, given the 2025 notification lag |

---

## 58. Future Vision

A ring that keeps its promise never to charge you again, and still earns every month — because the software you choose to run on it pays its way, and nothing that claims to improve your health gets onto it without showing why.

---

## 59. PM Lessons

1. **A shrinking share can hide inside spectacular growth.** Subscriptions grew 7.4% and fell from 25.81% to 5.14% of revenue in the same year. Always compute the share, not just the growth.
2. **Read the tax line before believing the profit line.** PBT of ₹45.70 Cr against PAT of ₹71.5 Cr changes what "first profitable year" means.
3. **Free is a strategy, not an absence of one** — and it has a price, paid in the revenue-multiple gap: 2.61× against a peer's 11.23×.
4. **A cost advantage is not a moat until something is sold on top of it.** On-device inference is the right investment and an incomplete one.
5. **Respect the promise that won the customers.** The best proposal for a company that says "no recurring charges" is one that never charges recurring fees.
6. **When demand is 18× supply, sequencing is not a strategy question.** Ship the product people are already trying to buy.
7. **Bundled free periods inflate attach rates.** Measure conversion after the bundle lapses or you are measuring your own generosity.

---

## 60. PM Interview Questions

1. Ultrahuman gives its AI away; Oura charges $5.99 a month for a comparable feature. Which is the better business in five years, and what evidence would settle it?
2. You have committed capital to on-device inference and have no software revenue line. What do you build first?
3. How would you design an approval gate for third-party health claims that does not strangle developer supply?
4. A company's paid-attach figure is measured on a base that received the paid feature free for a year. How do you correct it?
5. What is the right North Star for a platform whose marginal cost per user is approaching zero?
6. Your largest market is closed for a year by a patent ruling. How do you reallocate a roadmap around it?

---

## 61. References

**Regulatory and filings-derived**
1. Entrackr, "Ultrahuman reports Rs 565 Cr revenue and Rs 73 Cr profit in FY25," 22 September 2025 — consolidated FY25 financials sourced from the Registrar of Companies: revenue ₹565 Cr from ₹105 Cr, PAT ₹73 Cr from a ₹38 Cr loss, rings ₹516 Cr at 91.3%, subscriptions ₹29 Cr at +7.4%, other ₹20 Cr, total income ₹581 Cr, ROCE 12.9%, EBITDA margin 8.76%, ₹0.95 spent per rupee earned, viO HealthTech share purchase agreement of 22 August 2025.
2. Inc42, "Ultrahuman Rings In INR 73 Cr Profit On 5X Revenue Surge," November 2025 — RoC figures at one decimal: operating revenue ₹564.7 Cr from ₹104.6 Cr, PAT ₹71.5 Cr against a ₹37.7 Cr loss, other income ₹16.1 Cr, total income ₹580.8 Cr, expenses ₹535.1 Cr from ₹146.4 Cr, cost of material ₹175.4 Cr from ₹33 Cr, employee cost ₹51.6 Cr from ₹27.3 Cr, selling and distribution ₹98.4 Cr from ₹15 Cr, tax credit gain ₹32.7 Cr.
3. Inc42, "Patent Infringement: US ITC's Ban On Ultrahuman Goes Live," November 2025 — FY25 geographic split: US ₹344.2 Cr, Middle East ₹33.2 Cr, UK ₹25 Cr, India ₹15.1 Cr; ban effective and USPTO review of Oura's patent pending.
4. Ministry of Corporate Affairs registry data, via Tofler, ZaubaCorp, Vakilsearch, Tracxn, IndiaFilings and Falconebiz — CIN U74999KA2019PTC129250, NIC code 74999, registered office, authorised and paid-up capital, directors, incorporation date (disputed, Appendix A-4).
5. Entrackr, "Exclusive: Qualcomm Ventures to lead $60 Mn round for Ultrahuman," September 2026 — RoC-sourced special resolution: 3,623 Series C and 3,832 Series C1 compulsorily convertible preference shares at ₹7,79,500 and ₹7,85,300, raising ₹583 Cr; investor-by-investor amounts; post-money estimated at about $363 Mn.

**Company disclosure**
6. Ultrahuman, "Ultrahuman Delivers Record FY25 Profits as Subscription Engine Accelerates," 22 September 2025 — $64 Mn operating revenue, $8.2 Mn net profit, rings $58.4 Mn at 91.3%, subscriptions $3.2 Mn at +7.4%, other $2.2 Mn, EBITDA margin 8.76%, ROCE 12.9%.
7. Ultrahuman, "Ultrahuman Unveils Ring PRO, With Category-Defining 15-Day Battery and Jade, World's First Real-Time Biointelligence AI" — Jade available to all users globally including the US, Standard and Deep Research modes, 120+ Blood Vision biomarkers, M1 CGM and Home inputs, AFib detection, the CEO's contrast with a "backward-looking LLM integration."

**Interviews and press**
8. TechCrunch, "Qualcomm backs Ultrahuman in $70M round on bet to turn smart rings into computers," 3 September 2026 — CEO interview: $70 Mn round as $65 Mn equity and $5 Mn debt, $365 Mn valuation against $120 Mn in 2023, ARR $140 Mn at about +45%, $200 Mn target by January 2027, about 800,000 rings sold from about 700,000 in February, 12% of users paying for PowerPlugs, US about 45% and India about 11% of quarterly revenue, demand at 18–20× US supply, Nordic and Qualcomm silicon, end-September software update, possible unprofitability this year, eight to ten quarters to an IPO with 2028 the earliest window, Labcorp collaboration.
9. Entrackr, "Ultrahuman projects Rs 1,100 Cr revenue in FY26, eyes deeper international expansion," October 2025 — FY26 projection, 500,000+ users, ~70,000 new monthly, gross margins 55% rings / 32% M1 / 29% Home, 75–80% renewal, 60–65% of ring users women, 95% CGM retention, subscriptions stated at 16% of revenue (disputed, Appendix A-2).
10. TechCrunch, "Ultrahuman unveils new smart ring as it awaits U.S. clearance after Oura dispute," 27 February 2026 — Ring Pro at $479, 15-day battery, Jade requiring no subscription, preorders excluding the US, $150 Mn run rate at that date.
11. Athletech News, "Ultrahuman Can Sell in US Market Again Following ITC Resolution," 24 March 2026 — US Customs and Border Protection clearance, preorders from $349, retail from $399, shipping 15 May.
12. Yanko Design, "Meet Ultrahuman Ring Pro: Up to 15 Days Battery, No Subscription, and a Dual-Core Processor," 4 May 2026 — "a lifetime subscription to all Ultrahuman Ring PRO features and content is included with no hidden fees or recurring charges"; three PowerPlugs free for one year valued at $150; dual-core processor with on-chip machine learning replacing the Ring AIR's single core.
13. TechTimes, "Ultrahuman Ring Pro Ships Today: Subscription-Free Ring Targets Oura With 15-Day Battery," 20 June 2026 — shipping date (disputed, Appendix A-5).
14. Medianama, "Ultrahuman raises $60 million to expand smart ring business," September 2026 — the 27 March 2025 data breach and the 2 June 2025 notification.

**Series cross-reference**
15. Day 78 of this series — Oura Inc. Form S-1, filed 3 September 2026 — all Oura comparators used in §14 and §D7: trailing revenue $1,424.79 Mn, membership 19.80% of revenue, 94% activation-to-paid, $5.99 and $69.99 pricing, named model vendors.

---

## 62. About the Author

**Gaurav Singh** — Product Manager, New Delhi. Background in yoga therapy and behavioural science, which is why the question I keep asking of health products is whether anything actually changes for the person wearing them.

Writing one evidence-based product case study a day for ninety days; the last thirteen are about AI health products. Ultrahuman and Oura are the cleanest natural experiment in the series: two companies, the same device, the same category, opposite answers to whether health AI should cost anything. Neither publishes evidence that its AI works. Only one of them is charging for it.

GitHub: `github.com/gaurav-product` · LinkedIn: `linkedin.com/in/gaurav-singh-986b40197`

---

## 63. License

Analysis and commentary released for non-commercial, educational use with attribution. Financial and operating figures belong to their sources and are cited in §61. No company logo, product image or marketing asset is reproduced. Derived figures are reproducible from `verify.py`; the SQL in §32 and the wireframes in §52 are original.

---

## 64. Self Review

**What is strong.** The central finding needs only two disclosed growth rates and two revenue lines, and it survives every rounding choice: subscriptions cannot grow 7.4% while rings grow 9.5× without the software share collapsing. The profit decomposition uses the company's own total income and expense figures and reconciles to the rupee. The proposal is constrained by the company's own strongest public promise rather than ignoring it, and its most likely failure mode — that 12% attach is a bundling artefact — is named before the proposal and given its own kill criterion.

**What is weak, stated plainly.**

- **The FY25 figures are RoC-derived via journalism, not a filing this case study read.** Two outlets report the same statements at different precision; both are cited and the one-decimal version is used. This is a materially weaker evidence base than Day 78's S-1, and every 🟢 in this study means "consistently reported from filings" rather than "read in the filing."
- **The two tax figures do not reconcile** (Appendix A-1). The case study prints both and asserts neither.
- **The 12% PowerPlugs attach is stated as a share of "users," and it is applied here to rings sold.** Users and cumulative rings sold are not the same denominator. Every figure derived from it is labelled implied.
- **The $50 per-plug price is derived from a $150 three-plug bundle valuation**, not from a published price list. The $4.80 Mn software revenue estimate inherits that.
- **Current-quarter figures are a CEO's interview statements**, unaudited and unaccompanied by a period definition.
- **26.07% of FY25 revenue is geographically unattributed** in the sources examined, so the US and India share comparisons rest on named countries only.
- **All RICE inputs, the North Star, the guardrail and every threshold are author constructs.**

**Rating: 7/10.** The argument is clean and the arithmetic is tight, but the evidence base is secondary reporting of filings rather than filings, and the headline comparison to Day 78 is a comparison between an audited S-1 and a journalist's read of an RoC submission. Lower than Day 78's 8/10 for that reason alone.

---

## 65. Appendix

### A. Source conflicts and disclosure gaps

| # | Conflict or gap | Handling |
|---|---|---|
| **A-1** | **Tax.** Total income ₹580.8 Cr less expenses ₹535.1 Cr gives **PBT ₹45.70 Cr**; reported PAT is **₹71.5 Cr**, implying a net tax credit of **₹25.80 Cr**. Inc42 separately reports a **tax credit gain of ₹32.7 Cr**. The two do not reconcile. | Both printed and both verified. The case study states the PBT-to-PAT gap as computed (₹25.80 Cr, 36.08% of PAT) and reports Inc42's figure separately (45.73% of PAT). Neither is asserted as authoritative. |
| **A-2** | **Subscription share.** FY25 filings give ₹29 Cr on ₹564.7 Cr = **5.14%**. The CEO told Entrackr in October 2025 that "subscriptions now contribute **16%** of total revenue." | Read as different periods and possibly different definitions — FY25 actuals versus a forward or run-rate statement including services. The filings figure is used throughout; the 16% is flagged here and never used in arithmetic. |
| **A-3** | **Revenue precision.** Entrackr reports ₹565 Cr / ₹105 Cr / ₹73 Cr; Inc42 reports ₹564.7 Cr / ₹104.6 Cr / ₹71.5 Cr. | One-decimal figures used throughout; the ₹0.30 Cr sum residual is computed and published. |
| **A-4** | **Incorporation date.** Sources give 1 November 2019 (majority), 1 December 2019, and 11 January 2019. | 1 November 2019 used, marked 🔴. |
| **A-5** | **Ring Pro US shipping date.** Athletech reports shipping 15 May 2026; TechTimes runs "Ships Today" on 20 June 2026; a July 2026 report describes a shipping delay on quality control. | No single date asserted; the timeline gives "May–Jun 2026" and flags the delay. |
| **A-6** | **Q1 FY26 figures.** One secondary blog reports Q1 FY26 revenue of ₹51.8 Cr against a net loss of ₹103.6 Cr. No other outlet corroborates it, and it is irreconcilable with a $140 Mn ARR and a ₹1,100 Cr FY26 projection. | **Not used anywhere in this case study.** Recorded here so that its absence is deliberate rather than an oversight. |
| **A-7** | **Total funding.** Trackers report $110 Mn, $123 Mn, $144.77 Mn and $168 Mn across differing round counts. | The $168 Mn figure is quoted once with its source and marked 🟡; no arithmetic depends on it. |
| **A-8** | **Valuation.** Entrackr estimates about **$363 Mn** post-money from RoC share-issue arithmetic; TechCrunch reports **$365 Mn** from a person familiar. | $365 Mn used for the multiple, which is the more conservative choice for this case study's argument since it raises Ultrahuman's multiple; the $363 Mn estimate is noted. |
| **A-9** | **Users versus rings sold.** "12% of users" pay for PowerPlugs; cumulative rings sold is about 800,000; users were "over 500,000" in October 2025. | The 96,000 payer figure is labelled implied throughout and is not used for any conclusion that a smaller denominator would overturn. |

### B. Evidence grades

🟢 **High** — FY25 figures consistently reported from RoC filings by two independent outlets and corroborated by the company's own release; the company's own product press releases.
🟡 **Medium** — figures derived here from those inputs; MCA registry data from commercial aggregators; CEO interview statements; the September 2026 round terms.
🟠 **Low** — single-source claims (95% CGM retention, the July 2026 app update and shipping delay, the subsidiary naming).
🔴 **Conflicting** — A-1 (tax), A-4 (incorporation date), A-5 (shipping date).

### C. Author-constructed content

Personas (§20), the eval plan and failure-mode ranking (§29), EPW/1k and UCR-90 (§31), all SQL (§32), the data-flow diagram (§42), the *PowerPlugs Open* mechanism and PRD (§50, §51), wireframes and all illustrative plug names and prices (§52), all four RICE initiatives and their inputs and the choice of stress rule (§47), Phase 0 kill criteria K1–K3 (§53), the three-arm test and rules R1–R3 (§54), KPI thresholds (§55), and the roadmap windows (§56). Full inventory in `ASSUMPTIONS.md` Part 3.

### D. Asset status

| Asset | Status |
|---|---|
| README.md | Complete, 65 sections |
| ASSUMPTIONS.md | Complete, Parts 1–5 |
| verify.py | **84 checks, all passing** — delivered, not committed |
| crosscheck.py | Run; deliverables reconciled against the gate — delivered, not committed |
| LinkedIn carousel + caption | Generated in Gamma; caption local only |

---

*Day 79 of 90 · [← Day 78 — Oura](../Day-78-Oura) · Day 80 →*
