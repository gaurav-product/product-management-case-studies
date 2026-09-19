# Day 81 — Hinge Health: the automation metric is 97%, and that is the problem

> Day 80 asked what an AI clinical engine can optimise when the company discloses no AI metric at all. Hinge Health is the control case: it publishes the number Hims & Hers does not. Its filings state that the platform "reduced the number of human care team hours associated with traditional physical therapy by **approximately 97%**." That is a real, quantified, disclosed AI result — and the moment you have it, three things follow that nobody says aloud. **First, it is a cost metric, not a clinical one.** It tells you care became cheaper to deliver; the filings disclose no measure of whether members got better. **Second, the lever is nearly spent.** If 97% of the hours are gone, the remaining **3.00%** is the entire pool left — the harvested pool is **32.33×** the pool remaining, and halving what is left recovers **1.50 points** of the original baseline. **Third, the margin headline already shows it.** GAAP gross margin rose **16.15 points** to **86.44%**, but non-GAAP rose only **4.18** — **74.09%** of the headline expansion is the absence of last year's IPO stock compensation, not operating improvement. Strip the adjustments and cost of revenue *rose* **15.54%**. The rest of the business is genuinely excellent: revenue **+53.00%**, decomposing almost exactly into clients **+24.16%** and revenue per client **+23.22%**, with **zero** acquired revenue. And the company is behaving as if it knows the automation lever is finished — buying a GI company for $105 Mn while authorising **4.73×** that much for buybacks. **The AI PM question: what is your next metric when the automation metric reaches 97%?**

**Author:** Gaurav Singh · **Day 81 of 90** · Written 19 September 2026
**Subject:** Hinge Health, Inc. (NYSE: HNGE, CIK 0001673743), Q2 2026 Form 10-Q and the Cylinder Health agreement of 4 August 2026
**Verification:** `verify.py` — 144 programmatic checks, all passing

---

## 1. Cover

| | |
|---|---|
| **Product** | The Hinge Health platform — TrueMotion AI motion tracking, the Enso wearable, HingeConnect, HingeSelect, and the Migraine Care Program, delivered by an AI-supported care team |
| **Company** | Hinge Health, Inc., San Francisco, California |
| **Domain** | Healthtech — AI-automated musculoskeletal and migraine care sold to self-insured employers and health plans |
| **Period examined** | Q2 2026 (three months ended 30 June 2026) and H1 2026, against the comparable 2025 periods, with FY2023–FY2025 for trend |
| **Why it matters** | The company that discloses the AI metric the rest of the category does not — which makes it the only place you can see what an automation metric actually measures, and what happens when it approaches its ceiling |
| **Proposed feature** | *Escalation Yield* — measuring clinical outcome produced per human care hour retained, inverting a metric built to minimise hours into one that allocates them |
| **Series arc** | Fourth of 13 closing case studies on AI health products; the deliberate mirror of Day 80 (Hims & Hers) — AI care that works, measured, against AI care that is asserted |
| **Evidence grades** | 🟢 High · 🟡 Medium · 🟠 Low · 🔴 Conflicting |

---

## 2. Repository Metadata

**Legal entity:** Hinge Health, Inc., a Delaware corporation. **SEC Central Index Key 0001673743.** Listed on the New York Stock Exchange under **HNGE**. Principal executive offices in San Francisco, California. Fiscal year ends 31 December. Dual-class structure with Class A and Class B common stock, the Class B carrying ten votes per share and converting to Class A on certain transfers. 🟢

**Standard Industrial Classification.** The company files under **SIC 7374 — Services-Computer Processing & Data Preparation.** 🟢

**The register misclassification, continued — and this is the most interesting entry in the tally.** The series has tracked register misclassification since Day 46 as a systemic problem rather than a failure by any individual company. Hinge Health files as a data-processing services company. It employs and contracts licensed physical therapists, physicians and board-certified health coaches through consolidated professional corporations; it ships **Enso**, an FDA-cleared wearable medical device; and it delivers regulated clinical care subject to state physical-therapy practice law. "Computer processing and data preparation" describes the motion-tracking layer and nothing else.

What makes this entry instructive rather than merely wrong is that **the company's own strategy invites the misclassification.** A business whose stated vision is "to build a new health system... using technology to scale and automate the delivery of care" has spent a decade arguing it is a software company. The register believed it. The FDA clearance and the professional corporations say otherwise. The tally, which stood at **eleven wrong of sixteen** after Day 80, now stands at **twelve wrong of seventeen** — **70.59%**, up **1.84 points**. 🟢

**Corporate structure.** Clinical services run through "consolidated professional corporations," consolidated into the financial statements — a materially different arrangement from Day 80's Affiliated Medical Groups, which Hims & Hers explicitly does *not* own. That difference matters for the proposal in §50 and is examined in §16. 🟢

---

## 3. Badges

`Day 81/90` · `Healthtech` · `AI care delivery` · `SEC-sourced` · `65 sections` · `144 verified checks` · `0 fabricated figures` · `AI eval plan in §29 and §51` · `Runnable SQL in §32` · `Zero Mermaid — tables and ASCII only`

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
| **Risk, Prioritisation & Proposal** | [40. Trust & Safety](#40-trust--safety) · [41. Technical Architecture](#41-technical-architecture) · [42. Data Flow](#42-data-flow) · [43. API Ecosystem](#43-api-ecosystem) · [44. Privacy & Security](#44-privacy--security) · [45. Pain Points](#45-pain-points) · [46. Opportunity Mapping](#46-opportunity-mapping) · [47. RICE](#47-rice) · [48. MoSCoW](#48-moscow) · [49. Kano](#49-kano) · [50. Feature Proposal — Escalation Yield](#50-feature-proposal--escalation-yield) · [51. PRD](#51-prd) |
| **Execution** | [52. Wireframes](#52-wireframes) · [53. Rollout Plan](#53-rollout-plan) · [54. A/B Testing](#54-ab-testing) · [55. KPI Dashboard](#55-kpi-dashboard) · [56. Product Roadmap](#56-product-roadmap) · [57. Risks & Mitigation](#57-risks--mitigation) · [58. Future Vision](#58-future-vision) |
| **Reflection & Sources** | [59. PM Lessons](#59-pm-lessons) · [60. PM Interview Questions](#60-pm-interview-questions) · [61. References](#61-references) · [62. About the Author](#62-about-the-author) · [63. License](#63-license) · [64. Self Review](#64-self-review) · [65. Appendix](#65-appendix) |

</details>

---

## 5. Executive Summary

Five findings, each computed from the Q2 2026 filings and each verified in `verify.py`.

**1. The growth is built, not bought — and it decomposes exactly.** Revenue grew **53.00%** to **$212.82 Mn**. Clients grew **24.16%** to 2,929; revenue per client grew **23.22%** to **$72.66k**. Compounded, those two give **53.00%** — the reported growth rate, to the decimal. Cylinder Health had not closed at the balance-sheet date, so **zero** of the increase is acquired. After Day 80, where **59.43%** of growth came from acquisitions, this is what the other answer looks like. 🟢

**2. The margin headline is mostly last year's IPO.** GAAP gross margin rose **16.15 points**, from **70.28%** to **86.44%**. Non-GAAP gross margin rose **4.18 points**, from **82.91%** to **87.09%**. The difference — **11.97 points**, or **74.09%** of the headline expansion — is the absence of adjustments that sat in last year's cost of revenue, principally **$16.44 Mn** of stock compensation equal to **11.82%** of Q2 2025 revenue. The operating improvement is the 4.18 points, and it is real; it is not sixteen. 🟢

**3. Delivery cost fell on paper and rose in fact — and that is still a good result.** GAAP cost of revenue fell **30.16%**. Strip the adjustments and non-GAAP cost of revenue **rose 15.54%** against **53.00%** revenue growth. Revenue therefore grew **3.41×** faster than the cost of delivering it, a gap of **37.46 points**. Delivery cost per client fell **6.94%** to **$9.38k**. This is genuine operating leverage in a care business, stated honestly rather than flattered. 🟢

**4. The one disclosed AI metric measures inputs removed, not outcomes produced.** The filings state the platform "reduced the number of human care team hours associated with traditional physical therapy by approximately **97%**." Against that, the same filings disclose **no** clinical outcome metric, **no** AI accuracy or evaluation metric, and **no** inference or AI cost metric. The company knows precisely how much labour it took out and publishes nothing about what the remaining care achieves. 🟢

**5. The lever is nearly exhausted, and the capital allocation says so.** With 97% removed, **3.00%** remains: the harvested pool is **32.33×** the remaining one, and halving the residual recovers **1.50 points** of the original baseline. Even driving all delivery cost to zero would add at most **12.91 points** of gross margin. Meanwhile the company agreed to buy Cylinder Health for **$105 Mn** and holds a buyback authorisation of **$496.5 Mn** — **4.73×** the price of entering a new condition. 🟢

**The synthesis.** Day 80's company had an AI narrative and no AI metric. Day 81's company has an AI metric and no outcome metric. These are the same failure at different stages of maturity: **in both, what gets measured is the cost of care, not the result of it.** Hinge is further along because it actually measured something, and its reward for measuring is that it can now see the ceiling. §50 proposes the metric that comes after 97%.

---

## 6. Product Overview

Hinge Health sells digital musculoskeletal (MSK) care to self-insured employers and health plans, who make it available to their covered populations. A member enrols, is assessed, and receives exercise therapy delivered through an app, with form feedback generated by **TrueMotion**, the company's AI-powered motion-tracking technology, which replaced physical wearable sensors. Care is "designed and monitored by our AI-supported care team of licensed physical therapists, physicians, and board-certified health coaches." 🟢

Around that core sit: **Enso**, an FDA-cleared electrical nerve stimulation wearable for pain relief; **HingeConnect**, a proprietary AI-driven database for real-time care interventions and coordination with outside providers; **HingeSelect**, an in-person provider network launched in 2025; specialised programmes for women's pelvic health and fall prevention; and, new in 2026, a **Migraine Care Program** — the first expansion beyond joint and muscle pain. All programmes run in a single application, and a member can treat multiple indications at once. 🟢

On 4 August 2026 the company agreed to acquire **Cylinder Health** for **$105 Mn** in cash, entering gastrointestinal care, with an integrated GI programme expected to launch in 2027. 🟢

---

## 7. Company Background

Daniel Perez is co-founder and CEO. The company has been driving "innovations in automating care since 2014." It listed on the NYSE in 2025; the Q2 2025 comparative period in this case study contains **$590.98 Mn** of stock-based compensation, the IPO-related charge that makes every year-on-year GAAP comparison in these filings misleading unless adjusted. 🟢

Revenue history: **$292.73 Mn** (FY2023), **$390.40 Mn** (FY2024, **+33.37%**), **$587.86 Mn** (FY2025, **+50.58%**). Growth accelerated into the IPO year and is guided at **+45.95%** for FY2026. 🟢

---

## 8. Product Timeline

| Date | Event | Grade |
|---|---|---|
| 2014 | Company begins work on automating MSK care | 🟡 |
| 2022 | Women's pelvic health programme launched | 🟢 |
| 2023 | Fall prevention programme launched for Medicare Advantage lives | 🟢 |
| — | TrueMotion integrated, replacing wearable sensors for members | 🟢 |
| — | Enso launched — FDA-cleared wearable for non-addictive pain relief | 🟢 |
| — | HingeConnect developed for real-time care support and provider coordination | 🟢 |
| 2025 | **HingeSelect** launched — in-person provider network | 🟢 |
| 2025 | **IPO on NYSE**; Q2 2025 carries $590.98 Mn of stock compensation | 🟢 |
| 10 Nov 2025 | Board authorises a $250.0 Mn share repurchase programme | 🟢 |
| 31 Dec 2025 | 25 million contracted lives; 97% twelve-month client retention | 🟢 |
| 2026 | **Migraine Care Program** launched — first expansion beyond MSK | 🟢 |
| 29 Jul 2026 | Authorisation raised to **$496.5 Mn** total; $196.5 Mn already repurchased | 🟢 |
| 4 Aug 2026 | **Cylinder Health agreed for $105 Mn**; GI programme expected 2027 | 🟢 |
| 4 Aug 2026 | Q2 2026 results: revenue $212.82 Mn, +53.00%; FCF $99.56 Mn | 🟢 |

---

## 9. Vision & Mission

Stated vision: "to build a new health system that transforms outcomes, experience and costs by using technology to scale and automate the delivery of care." The company describes itself as "focused on scaling and automating the delivery of health care."

Read the sentence carefully and the measurement problem is already in it. **Three nouns are named — outcomes, experience, costs — and the mechanism named is automation.** Automation acts directly on cost. It acts on outcomes and experience only through a chain of inference the company does not publish. The **97%** figure measures the mechanism. Nothing in the filings measures the first two nouns. 🟢

---

## 10. Problem Statement

The market problem is real and Hinge addresses it well. Musculoskeletal conditions are among the largest cost lines for self-insured employers; traditional physical therapy requires repeated in-person visits, is capacity-constrained by therapist hours, and is poorly adhered to. A platform that delivers exercise therapy remotely, with automated form feedback, removes the travel, the scheduling and most of the clinician time.

The **product** problem this case study examines is what happens next. A company that has removed 97% of the human hours from a care pathway has:

1. **Exhausted its primary efficiency lever.** The remaining 3.00% cannot produce another 16 points of margin, or another 4.
2. **No published measure of what the remaining care achieves**, which means it cannot tell whether the 3% it kept is going to the right members.
3. **A strategic need to find growth elsewhere**, which is precisely what the migraine launch, HingeSelect and the Cylinder acquisition represent.

---

## 11. Market Research

Three structural facts about employer-purchased digital care, all visible in this filing:

- **The buyer is not the user.** Clients are self-insured employers and health plans; members are their employees and covered lives. The company is "typically the sole digital MSK or migraine care provider" to a client's contracted lives for an average contract term of three years. 🟢
- **Distribution runs through partners.** Over 60 partners, including "the five largest national health plans by self-insured lives, and the top three PBMs by market share." In H1 2026 and 2025 "the vast majority of our contracts were completed via our partners." Implementation completes in 40–100 days. 🟢
- **Payment is engagement-gated.** "Clients only pay for the members that engage with our programs" — most on an annual platform fee per member plus a fee per completed billable session. 🟢

That last point is the commercially important one, and §39 returns to it: **the pricing model pays for sessions completed, not conditions resolved.**

---

## 12. Industry Analysis

| Force | State in 2026 | Evidence |
|---|---|---|
| Buyer concentration | High and consolidating; partners are the five largest national health plans and top three PBMs | 🟢 |
| Switching cost | Genuinely high: sole-provider status, three-year average terms, 97% twelve-month client retention | 🟢 |
| Clinical labour | The constraint the company built its product to remove — and has removed 97% of | 🟢 |
| Regulatory posture | Sharply more active on AI specifically: Utah's AI Policy Act, the Texas Responsible AI Governance Act requiring patient disclosure when AI systems are used, the EU AI Act, and California rules restricting AI systems from implying licensed professional involvement | 🟢 |
| Capital intensity | Almost none: implied capex **0.87%** of revenue | 🟢 derived |

The regulatory row deserves emphasis because it cuts against the business model in a specific way. California law, as the company describes it, prohibits "AI systems from using professional terminology, interface elements or branding that suggest or imply medical authority or licensed professional involvement when no such oversight exists." A product whose whole proposition is that a licensed physical therapist's hours have been reduced by 97% is operating exactly where that rule bites. §40 develops this.

---

## 13. TAM / SAM / SOM

*Author construct built on disclosed figures only; no third-party market size is asserted.*

| Layer | Basis | Figure |
|---|---|---|
| Contracted lives reached | Disclosed at 31 December 2025 | **25 million** |
| FY2026 revenue guidance midpoint | $856–860 Mn range | **$858.00 Mn** |
| Implied annual revenue per contracted life | Guidance midpoint ÷ contracted lives | **$34.32** |
| Clients | At 30 June 2026 | **2,929** |
| Revenue per client, annualised at Q2 rate | $72.66k × 4 | **$290.63k** |
| Clients required for a $1 Bn run-rate at today's revenue per client | — | **3,440.75**, i.e. **+511.75** clients |
| Or, holding clients flat, revenue per client required | — | **$85.35k**, an uplift of **17.47%** |

The last two rows frame the strategic choice cleanly. A billion-dollar run-rate is roughly 512 more clients, or 17.47% more revenue from the clients already signed. The second is the cheaper path and it is the one the migraine, GI and HingeSelect expansions are built to deliver — **more conditions per existing contracted life**, not more contracts.

---

## 14. Competitor Analysis

| Company | Position | The AI disclosure | Grade |
|---|---|---|---|
| **Hinge Health** | Employer-purchased MSK and migraine care; sole-provider contracts | **Discloses an automation metric: ~97% reduction in human care hours.** No outcome, accuracy or cost metric | 🟢 |
| **Hims & Hers** (Day 80) | DTC telehealth at larger revenue scale | **Discloses nothing.** AI is strategy narrative plus a technology expense line | 🟢 |
| **Doximity** (Day 82) | Clinical network; incumbent prescriber reach | Reports AI product adoption growth | 🟡 |
| **Sword Health** | Direct digital MSK competitor, private | No public filings | 🟠 |
| **Omada Health** | Adjacent chronic-condition digital care | Public filer; MSK not the core | 🟠 |

**The three-way comparison is the point of this week's run.** Hims discloses no AI metric. Doximity discloses adoption. Hinge discloses automation. **None of the three discloses an outcome.** The category has learned to measure AI by how much it is used or how much labour it displaces, and not at all by whether the patient improved. That is a category-level measurement failure, not a Hinge failure, and naming it that way is the honest reading.

---

## 15. SWOT

| | |
|---|---|
| **Strengths** | Growth that decomposes into two working engines (**+24.16%** clients, **+23.22%** revenue per client); **97%** client retention; sole-provider status on three-year terms; **46.78%** FCF margin; capex at **0.87%** of revenue; a disclosed automation result most competitors cannot match; $475.6 Mn of liquidity |
| **Weaknesses** | The automation lever is **97%** spent; no disclosed clinical outcome metric; the 97% figure is a company estimate on a company-defined baseline using 2025 data; contracted lives disclosed only as at 31 December 2025; GAAP comparatives distorted by **$590.98 Mn** of IPO stock compensation |
| **Opportunities** | Multi-condition expansion into migraine and GI, which monetises existing contracted lives rather than requiring new clients; HingeSelect extends into in-person care; Medicare Advantage and federal plans; international |
| **Threats** | AI-specific regulation in Utah, Texas, California and the EU aimed squarely at disclosure of AI involvement in care; dependence on third-party AI technologies the company says it cannot control the pricing of; guided deceleration of **7.04 points** against Q2 actual growth; buyback authorisation at **104.39%** of total liquidity |

---

## 16. Porter's Five Forces

| Force | Intensity | Reasoning |
|---|---|---|
| **Supplier power** | **Moderate and rising** | Clinical labour has been reduced 97%, which lowers supplier power structurally. But the company states it uses "AI Technologies licensed from third parties" and "cannot control the availability or pricing of such third-party AI Technologies" — it traded therapist leverage for model-vendor leverage |
| **Buyer power** | **Moderate** | Large, sophisticated buyers with performance guarantees at risk — but three-year sole-provider terms and 97% retention blunt it |
| **Threat of substitutes** | **Moderate** | In-person physical therapy, point solutions, health-plan-owned programmes. The 97% cost advantage is a real barrier |
| **Threat of new entrants** | **Moderate** | The FDA clearance, the partner integrations and the clinical evidence base are barriers; the underlying AI is increasingly not |
| **Competitive rivalry** | **High** | Sword Health and others compete directly for the same employer contracts |

**The structural reading, and it is the opposite of Day 80's.** Hims scored high on four of five forces and had no proprietary data asset. Hinge has genuine structural protection — sole-provider contracts, switching costs, 97% retention, an FDA-cleared device. Its exposure is different and subtler: **it has converted a labour-supply dependency into a model-vendor dependency**, and it says so in its own risk factors. The moat is commercial, not technical.

---

## 17. Business Model Canvas

| Block | Content |
|---|---|
| **Customer segments** | Self-insured employers (majority), fully-insured employers, health plans, Medicare Advantage, federal insurance plans, public sector employers and labour unions |
| **Value proposition** | Lower MSK cost for the client; accessible, automated exercise therapy for the member; performance guarantees putting fees at risk |
| **Channels** | Direct sales force plus **60+** partners, including the five largest national health plans and top three PBMs |
| **Customer relationships** | Three-year average sole-provider contracts; **97%** twelve-month client retention; enrolment marketing to clients' employee bases |
| **Revenue streams** | Annual per-member platform fee plus per-completed-session fees; some full annual subscriptions; some milestone-based |
| **Key resources** | TrueMotion; Enso (FDA-cleared); HingeConnect; the consolidated professional corporations employing clinicians; partner integrations |
| **Key activities** | Automating care delivery; enrolment marketing; client implementation in 40–100 days; clinical programme development |
| **Key partners** | Health plans, TPAs, PBMs; third-party AI technology vendors |
| **Cost structure** | Non-GAAP cost of revenue **12.91%** of revenue; S&M **38.25%**; R&D **16.00%**; G&A **13.18%** |

The cost structure row contains the whole story. **Delivering the care costs 12.91% of revenue. Selling it costs 38.25%** — nearly three times as much. In a business that has automated care delivery to near-completion, the dominant cost is no longer care. It is distribution.

---

## 18. Revenue Model

| Line | Q2 2026 | Q2 2025 | Change |
|---|---|---|---|
| Revenue | $212.82 Mn | $139.10 Mn | **+53.00%** |
| GAAP cost of revenue | $28.87 Mn | $41.34 Mn | −30.16% |
| **Non-GAAP cost of revenue** | **$27.47 Mn** | **$23.78 Mn** | **+15.54%** |
| GAAP gross profit | $183.95 Mn | $97.76 Mn | +88.16% |
| Non-GAAP gross profit | $185.35 Mn | $115.32 Mn | +60.72% |
| **GAAP gross margin** | **86.44%** | **70.28%** | **+16.15 pp** |
| **Non-GAAP gross margin** | **87.09%** | **82.91%** | **+4.18 pp** |

Revenue is recognised ratably over the twelve months after an eligible life becomes a member, which the company notes makes revenue "highly predictable" while **calculated billings** carry the seasonality — highest in Q2, when most clients contracted the previous year are billed. LTM calculated billings reached **$861.80 Mn**, **+51.62%**, or **$294.23k per client**, up **22.11%**. 🟢

---

## 19. Target Users

Two distinct populations, and the distinction drives §50.

**Clients** are benefits leaders at self-insured employers and health plans. They buy on cost reduction, engagement thresholds and return on investment, and they hold performance guarantees.

**Members** are covered lives with joint, muscle or migraine conditions. They do not pay and do not choose the vendor. They choose only whether to enrol and whether to keep going.

The AI serves both but is measured against neither directly. The **97%** figure is a statement about the company's own cost structure. The client's guarantee is about engagement and ROI. **Nobody's disclosed metric is the member's recovery.**

---

## 20. Personas

*Author construct, grounded in disclosed mechanics.*

**Renu, 44 — the automated-path member.** Chronic low back pain. Enrols, completes assessment, does app-guided exercise therapy with TrueMotion form feedback three times a week. Over her twelve-month subscription she may consume almost no human care time. **She is the 97%.** Her outcome is invisible in the filings.

**Marcus, 58 — the residual-hours member.** Post-surgical rehabilitation with complications, plus a flagged fall risk. HingeConnect surfaces him for "targeted intervention." A physical therapist spends real time on him. **He is the 3%** — and nothing disclosed indicates whether the company knows his hours are better spent than Renu's would be.

**Dana — the benefits director (the client).** Buys on cost and ROI, holds performance guarantees including "member reported outcomes," and renews at a 97% rate. She is the only party with a contractual outcome claim, and the company reports it has "historically paid an immaterial amount" against those guarantees.

**Ellie, 31 — the migraine member.** New programme, 2026. The automation curve for migraine starts from scratch: the 97% applies to physical therapy hours, not to her condition.

---

## 21. Jobs To Be Done

| When… | I want to… | So I can… | Does the platform serve it? |
|---|---|---|---|
| My back hurts and PT means three trips a week | do therapy from home, correctly | stick with it | **Yes — this is the core, and it works** 🟢 |
| I am unsure I am doing the movement right | get immediate form feedback | avoid injury and progress | Yes — TrueMotion 🟢 |
| I am a benefits leader with an MSK cost problem | prove a return | defend the spend | Yes — performance guarantees, ROI reporting 🟢 |
| **I want to know whether I am actually getting better** | **see my own progress against a clinical endpoint** | **decide to continue or escalate** | **No disclosed capability or measure** 🟠 |
| My case is complicated and needs a human | reach a clinician who knows my history | get the care automation cannot give | Partly — HingeConnect flags high-risk members; the allocation logic is undisclosed 🟡 |

The fourth row is the gap. The fifth row is where §50 acts.

---

## 22. User Journey

```
  CLIENT SIGNS            MEMBER ENROLS        AUTOMATED CARE        RESIDUAL HUMAN CARE
  via partner       ->    eligible life   ->   TrueMotion form  ->   the 3.00% of hours
  40-100 day              becomes member       feedback, app          that remain
  implementation          on billable          exercise therapy            |
        |                 activity                   |                     |
        |                      |                     |                     |
        v                      v                     v                     v
   MEASURED:            MEASURED:            MEASURED:             MEASURED:
   clients (2,929)      billable sessions    97% of human hours    nothing disclosed
   retention (97%)      revenue/client       REMOVED                     |
                                                   |                     |
                                                   +----------+----------+
                                                              |
                                                   NOT MEASURED ANYWHERE:
                                                   did the member recover?
```

The diagram's right-hand column is the case study. Every stage has a disclosed metric except the two that describe clinical value.

---

## 23. User Flow

```
  Client contract (via partner) -> eligible lives identified
      -> enrolment marketing -> member enrols
      -> assessment -> personalised exercise therapy plan  [AI]
      -> app session -> TrueMotion real-time form feedback [AI]
      -> repeat sessions (billable activity triggers revenue)
             |
             +--> HingeConnect flags high-risk member       [AI]
             |          |
             |          v
             |    human care team intervention  <-- THE RESIDUAL 3.00%
             |          |
             |          v
             |    (outcome: not disclosed)
             |
             +--> Enso wearable for pain relief   [FDA-cleared device]
             +--> HingeSelect in-person referral  [launched 2025]
```

Three AI decision points are disclosed: plan personalisation, form feedback, and risk identification for targeted intervention. The third is the one that allocates scarce human time, and it is the one §50 instruments.

---

## 24. Information Architecture

Single application, multiple concurrent programmes — the company states members can "treat multiple indications at once." That is architecturally the right decision for a multi-condition platform and it is what makes the Cylinder acquisition coherent: GI care lands in an app the member already has.

The consequence for measurement: **a member with MSK and migraine generates hours and outcomes in two programmes under one identity.** Any honest measure of care delivered per member has to reconcile across programmes, which is exactly the object §50 proposes and which the Cylinder integration will make harder if it is not built first.

---

## 25. UX Audit

| Area | Observation | Grade |
|---|---|---|
| Enrolment | Engagement-gated billing means enrolment friction directly costs revenue; the company runs dedicated enrolment marketing | 🟢 |
| Form feedback | TrueMotion replaced physical sensors — a genuine reduction in setup friction | 🟢 |
| Multi-condition | One app, concurrent indications | 🟢 |
| **Progress visibility** | No disclosed surface showing the member their clinical trajectory | 🟠 |
| **AI disclosure to the member** | Texas and California law now require disclosure when AI is involved in care; no member-facing disclosure surface is described in the filings | 🟡 |

The last row is both a compliance exposure and a design opportunity, and §50 treats it as one object rather than two.

---

## 26. UI Audit

Assessment restricted to what is disclosed; no screenshots are asserted. The material UI question raised by the filings is the one §25 names: a product that has automated 97% of clinician time, operating under new state law about implying "licensed professional involvement when no such oversight exists," needs a clear, member-visible account of *when a human was involved and when a model was*. Nothing in the filings describes that surface. 🟡

---

## 27. Accessibility

The company frames remote delivery as "driving health equity by allowing members to engage in their exercise therapy sessions from anywhere." That is an access claim, and a fair one. It is not an accessibility claim: no WCAG conformance, audit or standard is disclosed, and a motion-tracking product used by people with mobility limitations and by adults aged 65+ in a fall-prevention programme has an unusually strong case for publishing one. 🟠

---

## 28. Feature Breakdown

| Feature | What it does | Disclosed metric | Grade |
|---|---|---|---|
| **TrueMotion** | AI motion tracking; real-time exercise form feedback; replaced wearable sensors | **~97% human care hour reduction** (the only quantified AI result) | 🟢 |
| **Enso** | FDA-cleared electrical nerve stimulation wearable for pain relief | None | 🟢 |
| **HingeConnect** | AI-driven database for real-time interventions and external provider coordination | None | 🟢 |
| **HingeSelect** | In-person high-performance provider network (2025) | None | 🟢 |
| **Migraine Care Program** | First non-MSK condition (2026) | "Rapid adoption" — no figure | 🟡 |
| Pelvic health / fall prevention | Specialised programmes | None | 🟢 |
| **GI Care Program** | Via Cylinder Health; expected 2027 | Not yet launched | 🟢 |

---

## 29. AI Capabilities

The section this case study exists for — and the first in this series where the answer is not "nothing."

**What is disclosed.** 🟢

| Item | Disclosure |
|---|---|
| Named AI systems | **TrueMotion** (motion tracking, form feedback), **HingeConnect** (AI-driven database for real-time intervention) |
| Disclosed AI uses | Supporting the care team; developing personalised exercise therapy plans; real-time feedback on exercise form; identifying high-risk members for targeted interventions; "generally enhancing our operational efficiency" |
| Technology mix | Proprietary AI and ML algorithms **plus** "AI Technologies licensed from third parties" |
| **Quantified AI result** | **"reduced the number of human care team hours associated with traditional physical therapy by approximately 97%"** — company estimate, based on 2025 data |
| Model names or vendors | **None disclosed** |
| Accuracy or eval metrics | **None** |
| Clinical outcome metrics | **None** |
| Inference or AI cost | **None** |
| Human-in-the-loop design | Care team described as "AI-supported"; allocation logic not disclosed |
| Risk disclosure | A dedicated AI risk factor covering hallucination, biased or poor-quality training data, third-party model dependence, and AI-specific regulation in four jurisdictions |

**Reading the 97% properly.** It is the strongest AI disclosure in this series so far, and it still carries five qualifications the company states or implies:

1. **It is an estimate** — "according to our estimates," not a measurement.
2. **The baseline is company-defined.** "Traditional physical therapy" hours are not disclosed, so the denominator is unknown. A 97% reduction against a generous baseline is a different achievement from 97% against a lean one.
3. **It is 2025 data** in an August 2026 filing.
4. **It has no absolute magnitude.** 97% of what? Neither the hours removed nor the hours remaining is published.
5. **It measures inputs, not outputs.** Removing clinician hours is the mechanism. Whether members recovered is the objective, and it is absent.

**The ceiling arithmetic.** *Derived, verified in `verify.py`.*

| Quantity | Value |
|---|---|
| Human care hours removed | **97.00%** of the traditional baseline |
| Human care hours remaining | **3.00%** |
| Implied leverage versus traditional PT | **33.33×** |
| Harvested pool as a multiple of the remaining pool | **32.33×** |
| Original baseline recoverable by halving the residual | **1.50 points** |
| Maximum further gross margin if delivery cost went to **zero** | **12.91 points** |
| Non-GAAP gross margin expansion already achieved, as a fraction of that maximum | **0.32×** |

**This is the finding.** The company has taken roughly a third of the total margin available from delivery-cost elimination, and the remaining two-thirds requires driving the cost of care to literally nothing. Automation is no longer the growth lever. It is a completed project being reported as an ongoing advantage.

**The eval plan the residual requires.** *Author construct.* If 3% of hours remain, those hours are almost certainly concentrated in the hardest cases — which makes them the highest-stakes clinical time in the business and the least studied.

| Eval layer | What it measures | Method | Pass bar |
|---|---|---|---|
| **Escalation precision** | When HingeConnect flags a member for intervention, was the flag warranted? | Clinician adjudication on a stratified sample, by condition and risk tier | ≥90% agreement, published by condition |
| **Escalation recall** | Which members deteriorated *without* being flagged? | Retrospective review of members whose outcomes worsened | **Recall on serious deterioration is the safety-critical number**; release halts below bar |
| **Form-feedback fidelity** | Does TrueMotion's correction match a physical therapist's? | Blinded PT review of recorded sessions | ≥95% agreement on corrective instruction |
| **Outcome non-inferiority** | Do automated-path members reach condition endpoints at a rate no worse than human-delivered care? | Held-out arm with conventional delivery, pre-registered | Non-inferiority, never removed |
| **Residual-hour yield** | Do the retained human hours change outcomes more than the same hours spent elsewhere? | Randomised allocation of marginal care-team capacity | The metric §31 proposes |
| **Cohort fairness** | Does performance hold across age, condition, language and device? | Stratified reporting | No stratum below the global bar by more than a stated margin |

**Failure modes, ranked by damage to this specific business.**

1. **Missed escalation.** A member who needed a human and did not get one. With 97% of hours removed, the system's default is no human, and the flagging model is the only thing standing between a deteriorating member and an app. This is the ranked-first risk and the filings disclose no control for it.
2. **Automation measured as success while outcomes drift.** The single published AI metric rewards removing hours. If outcomes degrade slowly, nothing in the disclosed measurement system would show it — and the performance guarantees, which the company says cost "an immaterial amount," would not catch a slow drift either.
3. **AI-involvement disclosure failure.** Texas requires disclosure when AI systems are used in patient interactions; California restricts implying licensed professional involvement where none exists. A 97%-automated care pathway is the precise fact pattern these laws address.
4. **Third-party model dependence.** The company states it cannot control the availability or pricing of licensed AI technologies. The cost advantage rests partly on someone else's price list.
5. **The migraine and GI automation curves start at zero.** The 97% applies to physical therapy. New conditions inherit the platform, not the achievement — and the filings do not disclose the automation rate for migraine.

**Human-in-the-loop design.** *Author construct.* Three rules follow from the structure. **The residual is a budget, not a leftover** — the 3% should be allocated deliberately to the members with the most to gain, not consumed by whoever escalates loudest. **Every automated care decision records what a human would have been shown**, so escalation recall is computable retrospectively. And **the member is told, in the session, when a model and when a clinician is acting** — which satisfies Texas and California and is simply honest.

**AI cost per interaction.** *Author construct; the company discloses no interaction count, care-hour count or inference cost.* Attributing the **entire** non-GAAP cost of revenue to care delivery gives a ceiling: **$9.38k per client per quarter**, **$3.13k per client per month**, or an upper bound of **$4.40 per contracted life per year** on the stale 25-million-lives denominator. The true AI component is an unknown fraction of that. The reason the ceiling is worth computing is the same as on Day 80: **it is small.** Delivery is already 12.91% of revenue. The expensive part of this business is selling it.

---

## 30. Product Metrics

| Metric | Q2 2026 | Q2 2025 | Change | Grade |
|---|---|---|---|---|
| Revenue | $212.82 Mn | $139.10 Mn | **+53.00%** | 🟢 |
| Clients | 2,929 | 2,359 | **+24.16%** | 🟢 |
| Revenue per client | $72.66k | $58.96k | **+23.22%** | 🟢 derived |
| LTM calculated billings | $861.80 Mn | $568.40 Mn | +51.62% | 🟢 |
| LTM billings per client | $294.23k | $240.95k | +22.11% | 🟢 derived |
| GAAP gross margin | 86.44% | 70.28% | +16.15 pp | 🟢 |
| **Non-GAAP gross margin** | **87.09%** | **82.91%** | **+4.18 pp** | 🟢 |
| Non-GAAP cost of revenue | $27.47 Mn | $23.78 Mn | **+15.54%** | 🟢 derived |
| Delivery cost per client | $9.38k | $10.08k | −6.94% | 🟢 derived |
| GAAP operating margin | 19.00% | −417.45% | — | 🟢 |
| Non-GAAP operating margin | 28.90% | 18.76% | +10.14 pp | 🟢 |
| Net margin | 20.53% | — | — | 🟢 |
| Free cash flow | $99.56 Mn | $32.63 Mn | +205.14% | 🟢 |
| Free cash flow margin | 46.78% | 23.46% | +23.33 pp | 🟢 |
| Stock compensation, % of revenue | 8.97% | 424.87% | −96.77% | 🟢 |
| Client retention (12-month) | — | 97% at 31 Dec 2025 | — | 🟢 |
| **Human care hour reduction** | **~97%** (2025 data) | — | — | 🟢 |
| **Clinical outcome measure** | **Not disclosed** | **Not disclosed** | — | 🟠 |

### The growth decomposition, stated precisely

Revenue grew **53.00%**. Clients grew **24.16%**. Revenue per client grew **23.22%**.

$$(1 + 0.2416) \times (1 + 0.2322) - 1 = 0.5300$$

The two engines multiply to the reported growth rate with no residual. That is worth pausing on for two reasons. **It means the growth is real and internally generated** — no acquisition contributed, because Cylinder had not closed. And **it means both engines are working simultaneously**, which is rare: most companies growing above 50% are doing it on one engine, usually new logos.

Set against Day 80, where **59.43%** of revenue growth came from acquired businesses and the domestic product grew **15.74%**, this is the cleanest available demonstration of what built growth looks like in the same category and quarter.

### The margin headline, stated precisely

| | Q2 2026 | Q2 2025 | Change |
|---|---|---|---|
| GAAP gross margin | 86.44% | 70.28% | **+16.15 pp** |
| Non-GAAP gross margin | 87.09% | 82.91% | **+4.18 pp** |
| **Wedge** | | | **11.97 pp** |

**74.09% of the reported gross margin expansion is the absence of last year's adjustments**, principally $16.44 Mn of stock compensation sitting in Q2 2025 cost of revenue — **11.82%** of that quarter's revenue. The operating improvement is **4.18 points**, and **25.91%** of the headline.

A PM reading a "16-point gross margin expansion" headline and concluding the care model got dramatically cheaper would be wrong by a factor of nearly four.

---

## 31. North Star Metric

**Proposed: OPH — Outcome-Positive Episodes per 1,000 Human Care Hours.**

A human care hour enters the **denominator** when a member of the care team — physical therapist, physician or health coach — spends measured time on a specific member's care. The automated path contributes no denominator, by construction.

An episode enters the **numerator** only if **all four** hold:

1. the member has a **condition record with a stated clinical endpoint** — a function score, a pain threshold, a return-to-activity criterion;
2. a **measured improvement** toward that endpoint was recorded, from a validated instrument or clinician confirmation, not from session completion alone;
3. the **human hours are attributed** to that member and episode, with the triggering decision recorded — model-flagged, clinician-initiated or member-requested;
4. the member's **automated care continued as prescribed** during the period, so the metric cannot be gamed by substituting human time for the platform.

**Why this denominator inverts the current metric.** The 97% figure is minimised by design: every hour removed improves it. OPH is *maximised* by putting the remaining hours where they produce the most clinical movement. The same 3% of hours can score high or low depending entirely on allocation — which is the decision the company currently makes with an undisclosed model and measures not at all.

It also has the property every good North Star needs: **it cannot be improved by doing more of what is already finished.** Automating another point of the residual lowers the denominator but removes whatever outcome those hours produced. The metric forces the question of whether the hour was worth keeping.

**Guardrail, carried to §55: MED-90 — Missed Escalation Detection at the 90th percentile.** Among the decile of members whose condition trajectory worsened most, the share who were *never* flagged for human intervention before deterioration. Reported by condition and by risk tier, never in aggregate — an average across a large, healthy, automated population would conceal exactly the members the system failed.

The pairing is the whole design: **OPH rises when retained human time is well spent; MED-90 rises when the system stops noticing who needs it.** Optimising the first without publishing the second is how a 97%-automated care business would hurt someone.

---

## 32. Product Analytics

*Author construct. The schema is hypothetical. Both queries are PostgreSQL dialect and were parsed with `sqlglot` before delivery.*

**Query 1 — put a denominator under the 97%.** This is the query that turns a company estimate into a measurement, and it requires no data the company does not already generate.

```sql
WITH care_hours AS (
    SELECT
        date_trunc('month', h.occurred_at)          AS month,
        h.condition_code,
        h.trigger_source,
        SUM(h.duration_minutes) / 60.0              AS human_hours
    FROM care_team_time h
    WHERE h.occurred_at >= DATE '2025-01-01'
    GROUP BY 1, 2, 3
),
automated_sessions AS (
    SELECT
        date_trunc('month', s.started_at)           AS month,
        s.condition_code,
        COUNT(*)                                    AS sessions,
        COUNT(DISTINCT s.member_id)                 AS active_members
    FROM therapy_session s
    WHERE s.delivery_mode = 'automated'
    GROUP BY 1, 2
),
traditional_baseline AS (
    -- The counterfactual must be explicit and versioned, not assumed.
    SELECT
        b.condition_code,
        b.baseline_version,
        b.pt_hours_per_episode
    FROM pt_baseline b
    WHERE b.is_current
)
SELECT
    a.month,
    a.condition_code,
    t.baseline_version,
    a.active_members,
    a.sessions,
    ROUND(COALESCE(SUM(c.human_hours), 0), 2)                        AS human_hours_actual,
    ROUND(a.active_members * t.pt_hours_per_episode, 2)              AS human_hours_traditional,
    ROUND(100.0 * (1 - COALESCE(SUM(c.human_hours), 0)
          / NULLIF(a.active_members * t.pt_hours_per_episode, 0)), 2) AS pct_hours_reduced
FROM automated_sessions a
JOIN traditional_baseline t
  ON t.condition_code = a.condition_code
LEFT JOIN care_hours c
       ON c.month          = a.month
      AND c.condition_code = a.condition_code
GROUP BY a.month, a.condition_code, t.baseline_version,
         a.active_members, a.sessions, t.pt_hours_per_episode
ORDER BY a.month, a.condition_code;
```

The `baseline_version` column is the important one. A reduction percentage without a versioned, disclosed counterfactual is a marketing number; with one it is an auditable measurement that can be recomputed when the baseline is revised.

**Query 2 — Outcome-Positive Episodes per 1,000 Human Care Hours**, the §31 metric, with the §55 guardrail computed alongside.

```sql
WITH episode_hours AS (
    SELECT
        e.episode_id,
        e.member_id,
        e.condition_code,
        date_trunc('month', e.started_at)           AS cohort_month,
        SUM(h.duration_minutes) / 60.0              AS human_hours,
        BOOL_OR(h.trigger_source = 'model_flag')    AS model_flagged
    FROM care_episode e
    LEFT JOIN care_team_time h ON h.episode_id = e.episode_id
    GROUP BY 1, 2, 3, 4
),
episode_outcomes AS (
    SELECT
        o.episode_id,
        BOOL_OR(o.improved_toward_endpoint)         AS outcome_positive,
        BOOL_OR(o.deteriorated)                     AS deteriorated
    FROM condition_outcome o
    WHERE o.measurement_source IN ('validated_instrument', 'clinician_confirmed')
    GROUP BY 1
)
SELECT
    h.cohort_month,
    h.condition_code,
    COUNT(*)                                                         AS episodes,
    ROUND(SUM(h.human_hours), 2)                                     AS human_hours,
    ROUND(1000.0 * COUNT(*) FILTER (WHERE o.outcome_positive)
          / NULLIF(SUM(h.human_hours), 0), 2)                        AS oph_per_1k_hours,
    ROUND(100.0 * COUNT(*) FILTER (WHERE o.deteriorated
                                     AND NOT h.model_flagged)
          / NULLIF(COUNT(*) FILTER (WHERE o.deteriorated), 0), 2)    AS missed_escalation_pct
FROM episode_hours h
LEFT JOIN episode_outcomes o ON o.episode_id = h.episode_id
GROUP BY h.cohort_month, h.condition_code
ORDER BY h.cohort_month, h.condition_code;
```

The final column is MED-90's engine: of the members who deteriorated, what share the model never flagged.

---

## 33. AARRR

| Stage | State | Evidence |
|---|---|---|
| **Acquisition** | Partner-led and efficient; 2,929 clients, +24.16%; implementation in 40–100 days | 🟢 |
| **Activation** | Engagement-gated billing makes activation the revenue trigger; no disclosed activation rate | 🟡 |
| **Retention** | **97%** twelve-month client retention; member-level retention not disclosed | 🟢 |
| **Revenue** | $72.66k per client, **+23.22%**; billings per client +22.11% | 🟢 derived |
| **Referral** | Partner referrals and client word-of-mouth; no metric | 🟠 |

**Client retention is 97% and member retention is undisclosed** — and in a business where the client buys and the member uses, those are different questions. The company's revenue depends on members completing billable sessions; its renewal depends on clients being satisfied. Only the second is published.

---

## 34. HEART

| Dimension | Signal available | Gap |
|---|---|---|
| **Happiness** | "improved our high member satisfaction over time" — no figure | No NPS or CSAT disclosed |
| **Engagement** | Billable sessions drive revenue; no session or adherence figure disclosed | The metric the business runs on is not published |
| **Adoption** | Migraine "rapid adoption" — no figure | No programme-level adoption rate |
| **Retention** | 97% client retention | Member retention absent |
| **Task success** | **The clinical task — did the member recover — has no disclosed measure** | The central gap |

---

## 35. Growth Strategy

The stated strategy has four pillars: grow and retain clients, expand members within existing clients, innovate into new programmes, and enter new markets (Medicare Advantage, federal plans, international).

The numbers say pillar two is now the main event. Revenue per client grew **23.22%**, nearly matching client growth of **24.16%**, and the company's own framing — "the long-term value of our platform to our clients increases as our clients' eligible lives increase adoption and usage" — points the same way. **Migraine, pelvic health, fall prevention, HingeSelect and now GI are all mechanisms for extracting more revenue per contracted life**, which §13 shows is the cheaper of the two paths to a billion-dollar run-rate.

---

## 36. Growth Loops

**Loop 1 — Partner → client → contracted lives → revenue → partner credibility.** Running well. 60+ partners including the five largest national health plans.

**Loop 2 — More conditions → more revenue per existing life → higher client ROI → renewal and expansion.** This is the loop the 2026 strategy is built on, and it is the one that does not depend on the exhausted automation lever.

**Loop 3 — Member data → better automation → lower delivery cost → price advantage → more clients.** **This loop is decelerating by construction.** At 97%, each additional increment of automation returns less than the last, and §29's arithmetic caps the total remaining benefit at 12.91 points of gross margin even in the limit. The loop that built the company is the one closest to exhaustion.

---

## 37. Network Effects

There is no user-to-user network effect. The candidate is a **data network effect**: more members produce better motion models, better risk flagging, better personalisation.

Hinge has a genuine version of this — TrueMotion replacing hardware sensors is direct evidence that accumulated data displaced physical infrastructure. But the effect is bounded by the same ceiling as everything else in §29: the observable output of the data loop is automation, automation is 97% complete, and **no disclosed metric tracks whether accumulated data is still improving anything other than cost.**

The strategically interesting question is whether HingeConnect — a database of real-time care interventions coordinated with *external* providers — is a second, less exhausted data asset. It plausibly is, and the filings publish nothing about it.

---

## 38. Product Strategy

The strategy is coherent and the company is executing it. Naming the tension is still the useful PM act.

- **The narrative strategy** is automation: "scaling and automating the delivery of health care," with a 97% proof point.
- **The operating reality** is that automation is nearly finished, delivery is 12.91% of revenue, and selling costs three times more than delivering.
- **The capital allocation strategy** is multi-condition expansion plus capital return: $105 Mn for Cylinder, **$496.5 Mn** authorised for buybacks — **4.73×** the acquisition price.

A company that believed its automation loop still had years of compounding left would plough capital into it. A company that believed growth now comes from more conditions per life would buy Cylinder. A company that believed neither could absorb much more capital would return it. **Hinge is doing the second and third simultaneously, which is the honest read of where it thinks it is.** That is a defensible position — it is simply not the position the automation narrative describes.

---

## 39. Monetization

| Stream | Mechanics | Health |
|---|---|---|
| Per-member platform fee | Annual, per enrolled member | Core |
| **Per completed billable session** | Fee per session; "clients only pay for the members that engage" | **Pays for activity, not resolution** |
| Full annual subscriptions | Some clients | Minority |
| Milestone-based | Some clients | Minority |
| Performance guarantees | Engagement thresholds, member-reported outcomes, ROI; fees at risk | "Historically paid an immaterial amount" |

**The pricing model and the automation metric point the same way, and it is the wrong way.** Revenue rises with completed sessions. The AI metric rises with hours removed. Neither rises when a member gets better faster and stops needing sessions. A member who recovers in six weeks instead of twelve is, on both the revenue line and the automation metric, a worse outcome than one who does not.

The performance guarantees are the only countervailing mechanism, and the company reports paying "an immaterial amount" against them — which can mean the guarantees are comfortably met, or that they are set where they will be. The filings do not distinguish, and §65 records that as an open question rather than resolving it.

---

## 40. Trust & Safety

**The regulatory environment has moved directly at this business model.** The company names, in its own risk factors:

- **Utah's Artificial Intelligence Policy Act** — disclosure requirements and accountability for generative AI in consumer interactions. 🟢
- **The Texas Responsible Artificial Intelligence Governance Act (TRAIGA)** — requires disclosures to patients when AI systems are used. 🟢
- **California rules** prohibiting AI systems from "using professional terminology, interface elements or branding that suggest or imply medical authority or licensed professional involvement when no such oversight exists," plus CCPA automated-decision-making rules effective 1 January 2026 with compliance required by 1 January 2027. 🟢
- **The EU AI Act**, in force since August 2024, with obligations scaled to risk. 🟢

**Why this lands harder on Hinge than on most.** A platform that has removed 97% of licensed-clinician hours and describes an "AI-supported care team" is, by construction, the case these statutes were drafted for. The California provision is the sharpest: the product's credibility rests on clinical authority, and the law now polices the gap between implied and actual clinician involvement. The company discloses no member-facing AI-involvement surface.

**The company's own stated AI risks** — hallucinatory outputs, training on "incomplete, flawed, inadequate, inaccurate, biased, or otherwise poor quality data," use "without sufficient oversight and governance" — are the standard set, but in a care-delivery context they describe clinical harm rather than reputational harm. The filings pair this candid risk language with zero published evaluation results, which is the same asymmetry Day 80 found at Hims: **extensive disclosure of how the AI might fail, none of how it performs.**

---

## 41. Technical Architecture

Disclosed at a high level: a mobile application; TrueMotion computer-vision motion tracking running against the member's camera; the Enso wearable; HingeConnect as a real-time interventions database with external provider integration; proprietary AI/ML models **plus** third-party licensed AI technologies, some consumed as hosted services. 🟢 / 🟡

The architecturally load-bearing disclosure is the dependency: the company states it "cannot control the availability or pricing" of third-party AI technologies, and that disruption of hosted services "could disrupt our operations." A 97% cost advantage that partly rests on a vendor's price list is a commercial position, not a technical moat. 🟢

---

## 42. Data Flow

```
   ENROLMENT            AUTOMATED DELIVERY          RISK LAYER           RESIDUAL CARE
   eligible life   ->   TrueMotion (camera)   ->   HingeConnect    ->   care team time
   -> member            personalised plan          flags high-risk       (the 3.00%)
       |                real-time form              members                  |
       |                feedback                       |                     |
       v                    |                          |                     v
   billable            [proprietary + third-party AI Technologies]      outcome:
   activity                 |                          |                NOT DISCLOSED
   triggers                 v                          v                     |
   revenue           97% OF HUMAN HOURS          allocation logic             |
                        REMOVED (measured)        NOT DISCLOSED               |
                             |                          |                     |
                             +------------+-------------+---------------------+
                                          |
                              NO LINK PUBLISHED BETWEEN
                              HOURS SPENT AND OUTCOMES ACHIEVED
```

The measured quantity sits on the left. The valuable quantity sits on the right. Nothing disclosed joins them, and §50 is the join.

---

## 43. API Ecosystem

HingeConnect is described as coordinating with external providers in real time, and 60+ partner integrations carry contracting and billing. No public developer API is disclosed. For a company entering its third and fourth conditions — migraine now, GI in 2027 — the integration surface between programmes is an internal contract question that the filings do not describe, and §24 notes why it matters for measurement. 🟠

---

## 44. Privacy & Security

The company processes member health information across an AI pipeline that includes third-party hosted models. It names HIPAA plus state regimes, and flags Washington State legislation and the CCPA automated-decision-making rules requiring notice, opt-out and access rights by 1 January 2027. 🟢

The specific exposure worth naming: **automated decision-making rights and AI-disclosure duties are converging on exactly the mechanism that produces the 97%.** A member has, or shortly will have, a right to know that an automated system shaped their care and to opt out of it. A care model that is 97% automated must answer what care an opted-out member receives — and that answer is the residual 3%, which is not sized for the whole population.

---

## 45. Pain Points

| # | Pain point | Evidence | Severity |
|---|---|---|---|
| 1 | No disclosed clinical outcome metric, in a company whose vision names outcomes first | Absence across filings 🟢 | **Critical** |
| 2 | Automation lever ~97% exhausted; max remaining margin 12.91 pp | Derived 🟢 | **Critical** |
| 3 | Allocation of residual human hours is model-driven and unmeasured | 10-Q 🟡 | **Critical** |
| 4 | AI-disclosure duties (TX, CA, UT, EU) target a 97%-automated care model directly | 10-Q risk factors 🟢 | High |
| 5 | Headline gross margin expansion 74.09% attributable to prior-year adjustments | Derived 🟢 | High |
| 6 | Pricing rewards completed sessions, not resolution | 10-Q 🟢 | High |
| 7 | The 97% is an estimate against an undisclosed, company-defined baseline, on 2025 data | 10-Q 🟢 | High |
| 8 | Third-party AI dependence with stated inability to control price or availability | 10-Q 🟢 | Medium |
| 9 | Contracted lives disclosed only as at 31 December 2025 | 10-Q 🟢 | Medium |
| 10 | Buyback authorisation at 104.39% of total liquidity | Derived 🟢 | Medium |

---

## 46. Opportunity Mapping

| Opportunity | Pain addressed | Requires cooperation from | Reversible? |
|---|---|---|---|
| **Publish the 97% denominator and baseline version** | 7 | **No one — internal disclosure choice** | Yes |
| **Report a clinical outcome measure beside the automation measure** | 1 | Internal; clinical leadership | Yes |
| **Instrument human care hours per member and per episode** | 3 | Engineering only | Yes |
| **Escalation Yield** — outcome per retained human hour | 1, 2, 3 | Clinicians, clients, members, regulators | Partially |
| Member-facing AI-involvement disclosure | 4 | Legal, design, and four jurisdictions | Partially |

The decisive column is the third, exactly as on Day 80. **Three of these require nobody's permission. The proposal requires four constituencies.**

---

## 47. RICE

Scores computed and asserted in `verify.py`. Reach is in clients. The **stress multiplier is the company's own evidenced constraint: 3.00%**, the residual human care hours. The proposal measures outcome per retained human hour, so its reach is bounded by the hours that still exist. Initiatives whose reach does not depend on that residual pool are exempt, and the exemption is declared in ASSUMPTIONS Part 3.

| Initiative | Reach | Impact | Confidence | Effort (pm) | Stressed | **RICE** |
|---|---|---|---|---|---|---|
| **Publish the 97% denominator and baseline** | 2,929 | 2.0 | 0.95 | 2 | No | **2,782.55** |
| **Clinical outcome metric alongside automation** | 2,929 | 2.5 | 0.85 | 8 | No | **778.02** |
| **Per-member human-hour instrumentation** | 2,929 | 1.5 | 0.85 | 6 | No | **622.41** |
| **Escalation Yield (the proposal)** | 2,929 → 88 | 3.0 | 0.60 | 16 | **Yes** | **9.89** |

**The proposal ranks last, by 281.48×, and this is the correct answer — more emphatically here than on Day 80.**

The reason is unusually clean. Escalation Yield is the right long-term metric: it is the only one that tells the company whether the hours it kept are the hours worth keeping. But its reach is 3.00% of the care pathway, because that is all the human time that exists. **The stress test is not a hypothetical here — it is the literal size of the addressable surface.**

Everything above it is cheap, internal and a precondition. You cannot compute outcome per human hour without instrumenting human hours (initiative 3). You cannot claim an outcome metric is meaningful without a disclosed outcome measure (initiative 2). And you cannot ask anyone to trust a ratio whose denominator descends from an undisclosed baseline (initiative 1).

**A company that has already automated 97% of its care should spend the next two quarters explaining the 97% before it starts measuring the 3%.**

---

## 48. MoSCoW

| Priority | Items |
|---|---|
| **Must** | Publish the absolute human-hour denominator and a versioned baseline definition; report a clinical outcome measure alongside the automation measure; instrument human care hours per member and episode |
| **Should** | Member-facing AI-involvement disclosure ahead of the TRAIGA and California deadlines; publish escalation precision and recall; disclose contracted lives at each quarter end rather than annually; publish migraine automation rate separately |
| **Could** | Escalation Yield pilot in one condition; member-level retention reporting; HingeConnect intervention effectiveness |
| **Won't (this cycle)** | Automating the residual 3%; extending the 97% claim to migraine or GI before those curves are measured separately |

The final "Won't" is the discipline the case study argues for. **Reporting a platform-wide automation figure that was earned in physical therapy, at a moment when two new conditions are being added, would convert a real achievement into a misleading one.**

---

## 49. Kano

| Feature | Category | Note |
|---|---|---|
| Remote exercise therapy | **Must-be** | Table stakes for the category now |
| Real-time form feedback | **Performance** | More accuracy, more satisfaction — and TrueMotion delivers it |
| Multi-condition in one app | **Attractive** | Genuinely differentiating; the Cylinder thesis |
| FDA-cleared pain-relief wearable | **Attractive** | Hard to copy |
| **Knowing whether you are getting better** | **Attractive → Must-be** | Nobody in the category offers it; the first to ship it makes it table stakes for everyone |
| Automation itself | **Indifferent** | Invisible to the member; matters only through price and access |

The last row is the strategic one and it mirrors Day 80 exactly. **Automation is Kano-indifferent to the person receiving care.** A member does not want fewer clinician hours; they want their back to stop hurting. The 97% is a metric for the client and the income statement. The member has no metric at all, and §50 gives them one.

---

## 50. Feature Proposal — *Escalation Yield*

**One line.** Measure the clinical outcome produced per human care hour retained — turning the residual 3% from a leftover into an allocated budget, and giving the company the metric that comes after automation is finished.

**The problem it solves.** The company has one disclosed AI metric and it is minimised by design: every hour removed improves it. That metric is now ~97% complete and cannot drive the next phase. Meanwhile the decision that matters most clinically — which members get the scarce remaining human time — is made by an undisclosed model and measured by nothing. §29's failure-mode ranking puts missed escalation first precisely because the system's default state is *no human*.

**What it is, concretely.**

| Element | Specification |
|---|---|
| **Grain** | One row per care episode, per member, per condition |
| **Denominator** | Human care team minutes attributed to that episode, by role (PT, physician, coach) |
| **Numerator** | Measured movement toward a stated clinical endpoint, from a validated instrument or clinician confirmation — never session completion |
| **Trigger provenance** | Every human hour records why it happened: `model_flag`, `clinician_initiated`, `member_requested` |
| **Counterfactual arm** | A held-out share of flagged members receives the standard automated path, so the yield of intervention is measurable rather than assumed |
| **Baseline register** | The "traditional physical therapy" baseline behind the 97% is stored as a versioned record, so the headline figure is recomputable and auditable |
| **Member surface** | The member sees their own endpoint, their trajectory, and — plainly — whether a model or a clinician acted at each step |
| **Boundary** | Escalation Yield may **never** be used to reduce total human hours as an objective. It is an allocation metric, not a cost metric, and the schema denies it to any system whose objective function includes cost |

**Why the boundary is in the specification and not the policy document.** The failure mode this product is most exposed to is optimising a yield ratio by shrinking its denominator — improving "outcome per hour" by removing hours from members who needed them. That is the same metric pathology the 97% already encodes, reproduced one level up. Encoding the prohibition as a schema-level objective constraint, rather than a guideline, is what stops the new metric from inheriting the old one's incentive.

**What it changes, measurably.** OPH (§31) becomes computable. MED-90 (§55) becomes computable, which means missed escalations become visible for the first time. §29's non-inferiority and escalation-recall evaluations run continuously rather than as studies. The 97% acquires a denominator and a version. And the member — for the first time in this series — sees whether the care is working.

**Why it ranks last, and should.** See §47. Its reach is **3.00%** of the care pathway; it needs clinicians, clients, members and four regulators; and all three initiatives above it are its preconditions. **The correct roadmap is not "measure the 3%." It is "explain the 97% first, then measure what you kept."**

---

## 51. PRD

**Title:** Escalation Yield v1 — single condition, single client cohort
**Owner:** Product, Clinical Measurement
**Status:** Proposal

**Problem.** The allocation of residual human care hours is model-driven and unmeasured, and the company's only published AI metric rewards removing hours rather than placing them well.

**Goal.** For one condition and one client cohort, make **OPH** and **MED-90** computable within two quarters, with a held-out arm sufficient to establish whether model-flagged intervention changes outcomes.

**Non-goals.** Reducing human care hours. Extending the 97% claim to migraine or GI. Any use of the metric in client-facing ROI reporting before the held-out arm reports.

**Scope — v1.**
1. Human care time capture at episode grain, with role and trigger provenance.
2. Clinical endpoint register per condition, with validated instruments.
3. Versioned traditional-PT baseline record backing the 97% figure.
4. Held-out arm: a fixed share of model-flagged members continue on the automated path, never removed.
5. Member-facing trajectory and AI-involvement surface.
6. Schema-level denial of the metric to any cost-objective system.

**Success criteria.**

| Criterion | Bar |
|---|---|
| Human-hour capture coverage | **100%** of care team time, enforced at write |
| Trigger provenance completeness | 100% of human hours carry a trigger source |
| Endpoint coverage | ≥80% of episodes in the pilot condition carry a stated endpoint |
| Outcome measurement source | 100% validated instrument or clinician confirmation; session completion never counts |
| Held-out arm integrity | Maintained for the full pilot; removal is a P0 incident |
| Escalation recall on deterioration | Published, with a bar set before launch |
| Cost-system reads of the metric | **Zero.** Any non-zero value is a P0 incident |

**Eval plan.** §29's six layers, run against the pilot condition, reported monthly to clinical leadership, stratified by risk tier.

**Dependencies.** Clinical leadership sign-off on endpoints and instruments; client agreement to outcome data collection; legal review against TRAIGA, the California provisions and CCPA automated-decision-making rules; the baseline register, which requires whoever originally computed the 97% to document it.

**Risks.** The binding constraint is clinician time — the same 3% the metric measures. Instrumentation that adds documentation burden to the scarcest resource in the business will be rejected by the people it depends on. Mitigation: capture must be passive, derived from systems clinicians already touch, and the pilot fails if it adds measured minutes per episode.

---

## 52. Wireframes

*ASCII, illustrative.*

**Member-facing trajectory and AI-involvement surface**

```
+--------------------------------------------------------------+
|  Your recovery                          Lower back · Week 7   |
+--------------------------------------------------------------+
|  Goal set with Sarah K., PT on 02 Aug 2026                    |
|  Endpoint: return to full function, pain below 3/10           |
|                                                               |
|  PROGRESS        [##################--------]  pain 4/10      |
|                  started at 7/10                              |
|                                                               |
|  This week                                                    |
|   * Mon  Exercise session ................ form checked by AI |
|   * Wed  Exercise session ................ form checked by AI |
|   * Thu  Plan adjusted .......... suggested by AI, approved   |
|            by Sarah K., PT                                    |
|   * Fri  Check-in call .......... with Sarah K., PT (18 min)  |
|                                                               |
|  +--------------------------------------------------------+   |
|  |  Who is looking after you                              |   |
|  |  Your exercise feedback is automated.                  |   |
|  |  Your care plan is reviewed by a licensed physical     |   |
|  |  therapist. Sarah K. has spent 47 minutes on your      |   |
|  |  care in the last 30 days.                             |   |
|  |  [ How we use AI in your care ]                        |   |
|  +--------------------------------------------------------+   |
|                                                               |
|  [ Message my care team ]         [ Download my record ]      |
+--------------------------------------------------------------+
```

The "47 minutes" line is the disclosure that satisfies Texas and California, and it is also the denominator of Escalation Yield shown back to the person it was spent on.

**Internal — care-hour allocation record**

```
+------------------------------------------------------------------+
| episode 55120388     member 88104     condition MSK-LBP-02        |
|------------------------------------------------------------------|
| human_minutes_total      47                                       |
|   by role                PT 39 | physician 0 | coach 8            |
| trigger_source           model_flag (risk tier 3)                 |
| model_version            escalation-risk-6.1                      |
| held_out_arm             FALSE                                    |
| endpoint                 pain_nrs <= 3 AND function_score >= 70    |
| outcome_measured         pain_nrs 7 -> 4  (validated instrument)  |
| outcome_positive         TRUE                                     |
| oph_contribution         1 episode / 0.783 hours                  |
| cost_system_read         BLOCKED BY SCHEMA POLICY                 |
+------------------------------------------------------------------+
```

---

## 53. Rollout Plan

| Phase | Duration | Content | Gate to proceed |
|---|---|---|---|
| **0 — Preconditions** | Weeks 1–8 | Publish the 97% denominator and versioned baseline; agree the clinical outcome measure; human-hour instrumentation live | All three complete; none optional |
| **1 — Capture** | Weeks 9–16 | Episode-grain care time with role and trigger provenance; endpoint register for the pilot condition | 100% capture coverage in staging; zero added clinician minutes |
| **2 — Shadow** | Weeks 17–24 | OPH and MED-90 computed, nothing surfaced; held-out arm established | Both metrics compute end to end; held-out arm stable |
| **3 — Clinician surface** | Weeks 25–32 | Allocation view for the care team; escalation precision and recall reported | Clinician review time does not increase; recall bar met |
| **4 — Member surface** | Weeks 33–40 | Trajectory and AI-involvement disclosure shipped | Zero cost-system reads; no fall in member engagement |
| **5 — Second condition** | Weeks 41+ | Extend to migraine, with its own baseline — **never inheriting the MSK 97%** | Phase 4 bars held two consecutive months |

Phase 5's caveat is the one to defend in a review. Migraine is a new automation curve; importing the MSK achievement into it would be the single easiest way to turn a real number into a false one.

---

## 54. A/B Testing

| Test | Arms | Primary metric | Guardrail | Decision rule |
|---|---|---|---|---|
| **Model-flagged intervention** | Flagged-and-escalated vs flagged-and-held-out | OPH | MED-90 must not rise | Escalate only where yield beats the held-out arm |
| **Automated vs human-delivered path** | Automated vs conventional delivery | Condition endpoint attainment | Escalation recall | **Non-inferiority, pre-registered.** Never superiority-only |
| **Member trajectory surface** | Visible vs current | Endpoint attainment | Engagement must not fall | Ship if attainment rises and engagement holds |
| **AI-involvement disclosure** | Disclosed vs current | Member trust measure | Enrolment and engagement | **Ship regardless of engagement effect where law requires it** — the test measures the cost of compliance, not whether to comply |

The last row states something a growth review would otherwise relitigate every quarter. Under TRAIGA and the California provisions, disclosure is not an optimisation; the experiment exists to size its impact, not to decide it.

---

## 55. KPI Dashboard

| Tier | Metric | Source | Cadence |
|---|---|---|---|
| **North Star** | **OPH** — Outcome-Positive Episodes per 1,000 Human Care Hours | Care-hour + outcome records | Monthly |
| **Guardrail** | **MED-90** — Missed Escalation Detection, worst-trajectory decile | Outcome + flag records | Weekly |
| Automation | Human-hour reduction **with published denominator and baseline version** | Care-hour capture | Quarterly |
| Automation | Automation rate **by condition** — MSK, migraine, GI separately | Care-hour capture | Quarterly |
| AI | Escalation precision and recall | Eval harness | Per release |
| AI | Form-feedback fidelity vs clinician | Blinded review | Per release |
| AI | Held-out arm outcome gap | Held-out arm | Monthly |
| Business | Non-GAAP gross margin, and delivery cost per client | Finance | Quarterly |
| Business | Revenue per client, split into price and programme mix | Finance | Quarterly |
| Business | Client **and member** retention | Ops | Quarterly |

The fourth row is the one this case study would most want added. **A single platform-wide automation rate will become actively misleading the moment migraine and GI reach scale**, because it will blend a mature curve with two immature ones and report the average as an achievement.

---

## 56. Product Roadmap

| Horizon | Focus | Why here |
|---|---|---|
| **Now (0–2 quarters)** | Publish the 97% denominator and baseline; agree and report a clinical outcome measure; instrument human care hours | Highest RICE; no external cooperation; preconditions for everything else |
| **Next (2–4 quarters)** | Escalation Yield phases 1–3 in one condition; escalation precision and recall published; member AI-disclosure surface ahead of the 1 January 2027 CCPA deadline | Makes allocation measurable; clears the regulatory runway |
| **Later (4–8 quarters)** | Member trajectory surface; second condition with its own baseline; HingeConnect intervention effectiveness | Compounds only once the bars hold |
| **Not yet** | Automating the residual 3%; platform-wide automation claims spanning conditions | The lever is spent and the claim would mislead |

---

## 57. Risks & Mitigation

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| Missed escalation reaches clinical harm | Medium | **Severe** | MED-90 published weekly; recall bar set before release; held-out arm never removed |
| A new metric inherits the old cost incentive | **High** | **Severe** | Schema-level denial of Escalation Yield to cost-objective systems; P0 on any read |
| AI-disclosure non-compliance (TX, CA, UT, EU) | Medium | High | Member-facing disclosure surface shipped ahead of the 1 Jan 2027 deadline |
| Automation claim extended across conditions | **High** | Medium | Per-condition automation rates; explicit "Won't" in §48 |
| Clinician rejection of instrumentation | High | High | Passive capture only; pilot fails if it adds measured minutes per episode |
| Third-party AI price or availability shock | Medium | Medium | Named in the company's own risk factors; outside product control |
| Growth deceleration below guidance | Medium | High | Guided FY growth is already 7.04 pp below Q2 actual; multi-condition expansion is the stated answer |
| Buyback consumes optionality | Medium | Medium | Authorisation is 104.39% of liquidity; noted for completeness, outside product control |

---

## 58. Future Vision

The plausible good outcome is concrete and close. Hinge has the rarest asset in this category: **an AI capability that demonstrably worked, measured well enough to publish.** Add a denominator, a baseline version and an outcome measure, and it would have the only end-to-end account in employer digital health of what automated care costs and what it achieves. That is a defensible position no competitor can assert into existence, because it requires having actually done the automation first.

The plausible bad outcome is quieter and is the default path: the 97% keeps appearing in decks after the lever is spent; it gets extended across migraine and GI where it was never earned; outcomes stay unmeasured because nothing forces them; the growth story shifts to conditions and clients while the automation story runs on as a legacy proof point; and the first real test of whether the remaining 3% is well allocated arrives as an incident rather than a metric.

The distance between them is not technology and not capital — the company has both. **It is the willingness to publish a denominator.**

---

## 59. PM Lessons

1. **An automation metric is a cost metric wearing clinical clothes.** "97% fewer human hours" tells you what you stopped paying for. It tells you nothing about what the patient got. Ask what the metric would look like if the product got worse — if the answer is "unchanged," it is not an outcome metric.
2. **Every ratio needs a published denominator and a versioned baseline.** A percentage reduction against a counterfactual the company defines and does not disclose is not auditable, however honestly it was computed.
3. **Check what share of a margin improvement is just last year's noise.** 74.09% of a 16-point expansion was the absence of an IPO charge. The real number was 4.18.
4. **When your core lever passes 90%, it is finished — do the arithmetic before the narrative.** 97% leaves 3%; the harvested pool is 32.33× the remaining one. Growth has to come from somewhere else, and the roadmap should say so out loud.
5. **Read capital allocation as a product statement.** $105 Mn into a new condition against $496.5 Mn authorised for buybacks tells you where the company thinks the returns are, whatever the strategy slide says.
6. **Growth that decomposes cleanly is a quality signal.** Clients +24.16% × revenue per client +23.22% = +53.00%, no residual, no acquisition. That is worth as much diligence attention as any single headline rate.
7. **The right proposal can still rank last — and here the stress multiplier was not hypothetical.** It was 3%, the literal size of what remained.

---

## 60. PM Interview Questions

1. Hinge Health discloses a 97% reduction in human care hours and no clinical outcome metric. You own measurement. What do you ship first, and what do you tell the executive who has used the 97% in every board deck for two years?
2. GAAP gross margin rose 16.15 points; non-GAAP rose 4.18. Which goes in the board deck, and how do you present the other?
3. Your core efficiency lever is 97% complete. Write the three-sentence version of where the next 10 points of margin come from.
4. The company is entering migraine and GI. Should the 97% automation figure be reported platform-wide or per condition? Argue both, then decide.
5. Design a metric for allocating scarce clinician hours that cannot be improved by removing those hours. What stops it from collapsing into a cost metric?
6. Texas requires patient disclosure when AI systems are used in care; California restricts implying licensed involvement where none exists. You have automated 97% of clinician time. Draft the member-facing sentence.
7. Compare this business to Day 80's Hims & Hers: one discloses an AI metric, one discloses none, neither discloses an outcome. Which is the more serious measurement failure, and why?

---

## 61. References

**Primary sources**

1. Hinge Health, Inc., **Form 10-Q** for the quarterly period ended 30 June 2026, filed 6 August 2026, accession 0001628280-26-054327. *(Income statement, business overview, the 97% automation disclosure, AI risk factors, key metrics.)* 🟢
2. Hinge Health, Inc., **Exhibit 99.1 to Form 8-K** filed 4 August 2026, accession 0001628280-26-052558 — "Hinge Health reports record second quarter 2026 financial results; signs definitive agreement to acquire Cylinder Health." *(Headline metrics, non-GAAP reconciliations, guidance, buyback, Cylinder terms.)* 🟢
3. Hinge Health, Inc., **Form 10-K** for the fiscal year ended 31 December 2025, filed 3 March 2026, accession 0001628280-26-013808. *(FY2023–FY2025 revenue and cost of revenue; contracted lives; client retention; the 97% disclosure.)* 🟢
4. SEC EDGAR submissions index, CIK 0001673743. *(SIC 7374 classification, exchange, state of incorporation.)* 🟢

**Series cross-reference**

5. Day 80 — Hims & Hers, this repository. *(The comparison that makes this case study's central question legible.)*

---

## 62. About the Author

**Gaurav Singh** — Product Manager, New Delhi. Writing a 90-day series of evidence-based product management case studies on real products, published daily to GitHub and LinkedIn. Background in yoga therapy and behavioural science. Every figure in this case study is computed from primary sources and verified programmatically before publication.

Repository: `github.com/gaurav-product/product-management-case-studies`

---

## 63. License

This case study is published for educational and portfolio purposes. All financial figures are drawn from public SEC filings. Company names, trademarks and product names are the property of their respective owners. No affiliation with Hinge Health, Inc. is claimed or implied. Analysis, proposals, metric designs and constructs are the author's own and are labelled as such in ASSUMPTIONS.md.

---

## 64. Self Review

**Rating: 9.0 / 10.**

**What this case study does well.** The central move — treating Hinge as the control case for Day 80 and asking what an automation metric actually measures — produces a finding neither company's own reporting surfaces: **the category measures the cost of AI care and not its result, and Hinge is simply far enough along to make that visible.** The ceiling arithmetic in §29 is the sharpest thing here: 97% means 3.00% remains, the harvested pool is 32.33× the remaining one, and the maximum further margin available is 12.91 points even in the limit. That reframes a proof point as a completed project. The margin decomposition (74.09% of the headline expansion is prior-year adjustments) is the second. And the growth decomposition multiplying to 53.00% with no residual is the fairest thing in the piece — it credits the company properly, and it makes the Day 80 contrast land without polemic.

**What is weaker.** The user-facing sections — §25, §26, §27 — remain thin, for the same reason as every prior day: the research reads filings, not users. This is the standing critique of the series and it is still unfixed at Day 81. Personas in §20 are constructs. The AI cost bound in §29 attributes all delivery cost to care and is therefore a ceiling on a line that is not AI-specific — labelled, but still the least satisfying number here. And I have no independent read on the clinical evidence base: Hinge publishes peer-reviewed outcome research outside its filings, and this case study deliberately confines itself to SEC sources, which means "no disclosed outcome metric" is a precise claim about the filings and a narrower claim than "no outcome evidence exists."

**What would make it a 10.** That last limitation is the one to fix: reading the published clinical literature alongside the filings would let the case study distinguish between *not measured* and *not disclosed in filings*, which is a materially different critique. Member-side evidence on the automated path would fix §25. Both are named in ASSUMPTIONS Part 5.

---

## 65. Appendix

### A. Source conflicts and roundings

No material numerical conflict was found between the 10-Q and the earnings release. Roundings are recorded rather than silently adopted.

| Item | Company statement | Computed here | Resolution |
|---|---|---|---|
| Revenue growth, Q2 | "53%" | **53.00%** | Agreement |
| GAAP gross margin, Q2 2026 | "86%" | **86.44%** | Release rounds; computed figure used |
| Non-GAAP gross margin, Q2 2026 | "87%" | **87.09%** | Release rounds |
| Non-GAAP operating margin, Q2 2026 | "29%" | **28.90%** | Release rounds |
| Non-GAAP income from operations growth | "136%" | **135.67%** | Release rounds |
| Free cash flow, Q2 2026 | "$100 million", "up 3x" | **$99.56 Mn**, **3.05×** | Headline rounds; detail table agrees with computed |
| FY2026 guided growth | "46%" | **45.95%** | Release rounds |
| Client growth | "24%" | **24.16%** | Release rounds |

### B. The buyback headline, examined

The release headlines "Board approved a **$300 million increase** to the share repurchase program." The body states that the increase resulted in "$300.0 million of our Class A common stock available for future repurchase, for a total aggregate amount authorized under the program of $496.5 million."

| Quantity | Value |
|---|---|
| Originally authorised, 10 November 2025 | $250.0 Mn |
| Repurchased as at 29 July 2026 | $196.5 Mn |
| Available for future repurchase after the increase | $300.0 Mn |
| Total aggregate authorised | $496.5 Mn |
| **Actual increase in total authorisation** | **$246.5 Mn** |
| Headline figure less actual increase | **$53.5 Mn** |
| Actual increase as % of the headline figure | **82.17%** |

The $300 Mn is the amount left *available*, not the increase. Both numbers are the company's own and the identity closes exactly ($196.5 Mn + $300.0 Mn = $496.5 Mn); the headline simply uses the more flattering of the two. Flagged here rather than in the body because it is a presentation point, not a finding about the business.

### C. Figures carried as stated, never sharpened

| Figure | Company language | Treatment here |
|---|---|---|
| Human care hour reduction | "approximately 97%" | Carried as 97.00% exactly as stated. All residual arithmetic (3.00%, 33.33×, 32.33×) inherits that approximation, and this note is the standing qualification on every one of them |
| Contracted lives | "25 million as of December 31, 2025" | Used only for the per-life bound in §13 and §29, labelled stale |
| Client retention | "97% as of December 31, 2025" | Cited as at that date; **not** the same 97% as the automation figure, and never conflated |
| Operating cash flow | "$101.4 million" / "$20.2 million" | Stated to $0.1 Mn; the implied capex figure inherits that precision |
| Partners | "over 60 partners" | Carried as a floor |

### D. The two 97%s

This filing contains two unrelated figures of 97%, and conflating them would be an easy and serious error:

- **97% human care hour reduction** — an estimate of automation against traditional physical therapy, based on 2025 data.
- **97% twelve-month client retention** — a commercial retention rate as at 31 December 2025.

They share a number and nothing else. Every reference in this case study specifies which.

### E. The register tally, Days 46–81

| | |
|---|---|
| Companies examined for register classification | **17** |
| Classifications that do not describe the business | **12** |
| Current rate | **70.59%** |
| Change from Day 80 | **+1.84 pp** |
| This entry | Hinge Health files under SIC 7374, Services-Computer Processing & Data Preparation — wrong, and instructively so |

### F. Figures computed but not used in prose

`verify.py` computes 144 values. Those not asserted in this README are retained in the gate so any future revision has them pre-checked, and so `crosscheck.py` can confirm no prose figure exists outside the gate.

---

*Day 81 of 90. Verified with `verify.py` — 144 checks, all passing. Next: Day 82, Doximity — the incumbent that reports its AI adoption, and what that adoption costs.*
