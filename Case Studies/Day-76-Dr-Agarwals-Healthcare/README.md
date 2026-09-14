# Day 76 — Dr Agarwal's Health Care: the network grew faster than the surgery

> Q1 FY27 reads as compounding growth: revenue up 25.97%, profit up 44.6%, a record sixteen new surgical facilities. But surgeries grew 15.47% while the facility count grew 22.09%, so **surgeries per facility fell 5.42%** — and revenue per facility rose just 3.18% despite revenue per surgery rising 9.10%. The quarter was bought with two things money can buy, locations and a richer procedure mix, and none of it came from the one lever that compounds: more surgery out of each location already open. The mix lever is thinner than it looks — the premium procedures the company reports by name are 3.58% of volume — while the untouched lever sits in plain sight: 89.67% of the 882,000 patients served did not have surgery, and **one percentage point of surgical conversion is worth more revenue than 29 average facilities produce in a quarter.**

**Author:** Gaurav Singh · **Day 76 of 90** · Written 11 September 2026
**Subject:** Dr Agarwal's Health Care Limited (NSE: AGARWALEYE), quarter ended 30 June 2026
**Verification:** `verify.py` — 117 programmatic checks, all passing

---

## 1. Cover

| | |
|---|---|
| **Product** | Dr Agarwal's Eye Institute — a hub-and-spoke single-specialty eye care network |
| **Company** | Dr Agarwal's Health Care Limited |
| **Domain** | Healthtech — single-specialty hospital services (ophthalmology) |
| **Period examined** | Q1 FY27, quarter ended 30 June 2026; results approved 4 August 2026 |
| **Primary comparator** | Dr Agarwal's Eye Hospital Limited (BSE: 526783), the group's own separately listed and separately audited subsidiary |
| **Proposed feature** | *Agarwal Indicated* — a clinically gated register of indicated-but-deferred surgery |
| **Evidence grades** | 🟢 High · 🟡 Medium · 🟠 Low · 🔴 Conflicting |

---

## 2. Repository Metadata

**Legal entity:** Dr Agarwal's Health Care Limited. **CIN L85100TN2010PLC075403** — cited rather than the name alone, because the group contains a second, similarly named listed company. Incorporated **19 April 2010**, RoC Chennai, with a certificate for commencement of business dated **29 May 2010**. Registered office: 1st Floor, Buhari Towers, No. 4 Moores Road, Off Greams Road, Chennai. Authorised capital **₹90.00 Cr**; paid-up **₹31.6158357 Cr** at a ₹1 face value — a ratio of **2.85×**, leaving the headroom a serial acquirer wants. 🟢

The CIN's activity code is **85100 — human health activities**. After eleven consecutive case studies in which the register's classification contradicted the business, this one is right. The tally across the series now stands at **nine wrong of thirteen**, which is still a statement about the register rather than about any company in it.

The name is the trap. **Dr Agarwal's Eye Hospital Limited** (CIN-bearing entity listed on BSE since long before the parent, founded 1957, incorporated 1994) is **72.67%** owned by Dr Agarwal's Health Care Limited and files its own audited results. An NCLT Chennai scheme of amalgamation is pending, with shareholder and creditor approvals obtained **2 July 2026** and a hearing listed for **19 August 2026**. Until it completes, two sets of numbers circulate under nearly the same name, and most coverage does not say which one it is quoting. §14 turns that hazard into the case study's best comparator. 🟢

---

## 3. Badges

`Day 76/90` · `Healthtech` · `Single-specialty hospitals` · `NSE: AGARWALEYE` · `Q1 FY27` · `65 sections` · `117 verified checks` · `0 fabricated figures` · `Zero Mermaid — tables and ASCII only`

---

## 4. Table of Contents

<details>
<summary><b>All 65 sections</b></summary>

| Group | | |
|---|---|---|
| **Context** | [1. Cover](#1-cover) · [2. Repository Metadata](#2-repository-metadata) · [3. Badges](#3-badges) · [4. Table of Contents](#4-table-of-contents) · [5. Executive Summary](#5-executive-summary) | [6. Product Overview](#6-product-overview) · [7. Company Background](#7-company-background) · [8. Product Timeline](#8-product-timeline) · [9. Vision & Mission](#9-vision--mission) |
| **Market & Competition** | [10. Problem Statement](#10-problem-statement) · [11. Market Research](#11-market-research) · [12. Industry Analysis](#12-industry-analysis) · [13. TAM / SAM / SOM](#13-tam--sam--som) | [14. Competitor Analysis](#14-competitor-analysis) · [15. SWOT](#15-swot) · [16. Porter's Five Forces](#16-porters-five-forces) · [17. Business Model Canvas](#17-business-model-canvas) |
| **Business & Users** | [18. Revenue Model](#18-revenue-model) · [19. Target Users](#19-target-users) · [20. Personas](#20-personas) · [21. Jobs To Be Done](#21-jobs-to-be-done) · [22. User Journey](#22-user-journey) | [23. User Flow](#23-user-flow) · [24. Information Architecture](#24-information-architecture) · [25. UX Audit](#25-ux-audit) · [26. UI Audit](#26-ui-audit) · [27. Accessibility](#27-accessibility) |
| **Product & Metrics** | [28. Feature Breakdown](#28-feature-breakdown) · [29. AI Capabilities](#29-ai-capabilities) · [30. Product Metrics](#30-product-metrics) · [31. North Star Metric](#31-north-star-metric) · [32. Product Analytics](#32-product-analytics) · [33. AARRR](#33-aarrr) | [34. HEART](#34-heart) · [35. Growth Strategy](#35-growth-strategy) · [36. Growth Loops](#36-growth-loops) · [37. Network Effects](#37-network-effects) · [38. Product Strategy](#38-product-strategy) · [39. Monetization](#39-monetization) |
| **Risk, Prioritisation & Proposal** | [40. Trust & Safety](#40-trust--safety) · [41. Technical Architecture](#41-technical-architecture) · [42. Data Flow](#42-data-flow) · [43. API Ecosystem](#43-api-ecosystem) · [44. Privacy & Security](#44-privacy--security) · [45. Pain Points](#45-pain-points) | [46. Opportunity Mapping](#46-opportunity-mapping) · [47. RICE](#47-rice) · [48. MoSCoW](#48-moscow) · [49. Kano](#49-kano) · [50. Feature Proposal — *Agarwal Indicated*](#50-feature-proposal--agarwal-indicated) · [51. PRD](#51-prd) |
| **Execution** | [52. Wireframes](#52-wireframes) · [53. Rollout Plan](#53-rollout-plan) · [54. A/B Testing](#54-ab-testing) · [55. KPI Dashboard](#55-kpi-dashboard) | [56. Product Roadmap](#56-product-roadmap) · [57. Risks & Mitigation](#57-risks--mitigation) · [58. Future Vision](#58-future-vision) |
| **Reflection & Sources** | [59. PM Lessons](#59-pm-lessons) · [60. PM Interview Questions](#60-pm-interview-questions) · [61. References](#61-references) · [62. About the Author](#62-about-the-author) | [63. License](#63-license) · [64. Self Review](#64-self-review) · [65. Appendix](#65-appendix) |

</details>

---

## 5. Executive Summary

Dr Agarwal's Health Care is India's largest eye care provider by revenue, running a hub-and-spoke network of **304 facilities across ten countries** as at 30 June 2026. Q1 FY27 was, on every headline the company and its analysts led with, an excellent quarter: revenue from operations **₹614.02 Cr against ₹487.42 Cr**, up **25.97%**; profit after tax **₹55.02 Cr**, up **44.6%**; operating EBITDA **₹177 Cr**, up 25.2%; net debt down from ₹278 Cr to **₹62 Cr**; and the largest quarterly surgical-facility expansion in the company's history, sixteen new surgical sites inside three months. 🟢

Four disclosed integers complicate it. Surgeries went **78,882 → 91,082**, up **15.47%**. Facilities went **249 → 304**, up **22.09%**. Divide one by the other in each year and **surgeries per facility fell from 316.80 to 299.61, a decline of 5.42%**. Revenue per facility rose only **3.18%** — from ₹1.9575 Cr to ₹2.0198 Cr a quarter — even though revenue per surgery rose **9.10%**, to ₹67,414. The arithmetic closes to within two hundredths of a point: a 9.10% price-and-mix gain multiplied by a 5.42% throughput loss reconstructs the 3.18% revenue-per-site gain almost exactly. **Growth came from opening sites and selling a richer procedure at each surgery. Throughput at an average site went backwards.**

Both of those levers have visible limits. The mix lever is thin: femtosecond cataract and lenticular procedures — the two premium lines the company reports by name and by growth rate — together number **3,260, or 3.58% of surgeries**, up from an implied 3.06% a year earlier, a shift of **0.51 percentage points** that supplied **6.91%** of the quarter's 12,200 additional surgeries. Cataract, the commodity, is **74.05%**. The site lever is expensive and slow: FY26's new greenfield branches lost about **₹30 Cr**, which is **17.86% of FY26 profit**, and the FY27 plan is sixty more facilities, **20.83%** of the network in a single year.

The profit growth, meanwhile, came mostly from below EBITDA. PAT grew 44.6% while EBITDA grew 25.2% — a gap of **19.40 percentage points** — against a **₹216 Cr, 77.70%** reduction in net debt funded by the January 2025 IPO. That lever is nearly spent: only ₹62 Cr of net debt remains, **28.70%** of the reduction already banked. And on the revenue-from-operations basis, EBITDA growth of 25.2% came in **0.77 points below** revenue growth, so the margin on operating revenue slipped about **17.8 bps** — a movement small enough to sit inside reporting rounding, but a rounding band that runs from **−32.98 to −2.63 bps and never crosses zero**.

The lever nobody is measuring publicly is the funnel. Dr Agarwal's served **more than 882,000 patients** in the quarter and performed 91,082 surgeries: a surgical conversion of **10.33%**, meaning **89.67%** of the people who walked in did not have a procedure. One percentage point of that conversion is **8,820 surgeries**, **9.68%** of the quarter's surgical volume, **₹59.46 Cr** of revenue at the quarter's own realisation — **the quarterly revenue of 29.44 average facilities, or 1.84× the sixteen surgical facilities the company was congratulated for opening.** Nothing in the disclosure suggests this ratio is managed, owned or reported.

It is also, and this matters more than the arithmetic, the one lever that cannot be pushed without a guardrail. In ophthalmology the gap between footfall and surgery is mostly *deferral*, not refusal — cataract is progressive, and a patient told to come back in a year is a dated clinical fact, not a lost sale. But an organisation that starts measuring conversion has just created an incentive to operate on eyes that do not need operating. §40 therefore precedes the proposal rather than following it, and the guardrail is specified before the metric.

**The proposal, *Agarwal Indicated*,** turns the clinical record the company already creates into an owned obligation: at the index visit the examining surgeon records the indication and a review window; the facility that made the diagnosis owns the return; conversion is reported per facility against indications registered *before* any recall activity; and an independent clinical audit function with no revenue target publishes the rate at which recalled patients were operated below the indication threshold. **In the RICE table it ranks third of four at baseline and falls to fourth and last under the stress rule** — behind a greenfield commissioning gate that requires no patient to do anything, which beats it **8.60×** once stressed. That is the correct answer, and §47 argues why.

---

## 6. Product Overview

The product is a network, not an app: tertiary hubs carrying surgical theatres and sub-specialty consultants, secondary facilities carrying routine surgery, and primary clinics doing consultation, refraction and diagnostics that feed the hubs. Revenue comes from surgery, from consultations and diagnostics, and from products — opticals, contact lenses and pharmacy — which were **21.4% of operating revenue** in the comparable quarter a year earlier. 🟢

The clinical range spans cataract, refractive, retina, cornea, glaucoma, squint and oculoplasty, with femtosecond-assisted cataract and lenticular refractive procedures as the premium tier. 🟢

---

## 7. Company Background

Dr Agarwal's Eye Hospital was founded in **Chennai in 1957** by Dr Jaiveer Agarwal and Dr Tahira Agarwal; Dr Amar Agarwal chairs the group today. The holding company examined here was incorporated in 2010 to carry the expansion, and took institutional capital repeatedly — ₹215 Cr from CDC in 2019, over ₹1,000 Cr from TPG Growth and Temasek in 2022, a further $80 Mn from the same investors in 2023 — before listing. 🟢

Management is family-executive and institutionally governed: **Dr Adil Agarwal** is CEO (since January 2019, holding 5.85%), **Dr Anosh Agarwal** COO (6.98%), **Yashwant Venkal** CFO, with Ranjan Ramdas Pai, Nachiket Mor, Ankur Nand Thadani, Sanjay Dharambir Anand, Venkatraman Balakrishnan, Ved Prakash Kalanoria and Archana Jayaraman Bhaskar on the board. Statutory auditor: S.R. Batliboi & Associates LLP. 🟢

---

## 8. Product Timeline

| Date | Event |
|---|---|
| 1957 | First eye care centre, Chennai 🟢 |
| 2010 | Holding company incorporated, 19 April; Telangana and Karnataka entry 🟢 |
| 2012 | International operations begin, Africa 🟢 |
| Mar 2024 | DRHP base: 26 hubs including 3 centres of excellence, 139 spokes, 15 African facilities 🟢 |
| Sep 2024 | DRHP filed with SEBI 🟢 |
| 29–31 Jan 2025 | IPO at ₹402, **₹3,027.26 Cr**, 7,53,04,968 shares, subscribed **1.55×** (QIB 4.64×, retail 0.41×, NII 0.40×) 🟢 |
| 4 Feb 2025 | Listing, BSE and NSE 🟢 |
| FY26 | Total income ₹2,125 Cr; first year above ₹2,000 Cr 🟢 |
| 2 Jul 2026 | Shareholders and creditors approve amalgamation of the listed subsidiary 🟢 |
| 4 Aug 2026 | Q1 FY27 results; 304 facilities; 16 new surgical facilities in one quarter 🟢 |
| 19 Aug 2026 | NCLT Chennai hearing on the scheme 🟢 |
| 16–18 Sep 2026 | Analyst and institutional roadshow, Gurgaon and Mumbai, with Jefferies and Kotak 🟡 |

---

## 9. Vision & Mission

The company's stated mission is the elimination of avoidable blindness, expressed operationally as bringing advanced ophthalmic care within reach of more people through density rather than centralisation. 🟢

The commercial translation is a premiumisation thesis: as insurance penetration and disposable income rise, a larger share of an essentially fixed clinical need is met with a more expensive version of the same procedure. Everything in Q1 FY27's realisation improvement is that thesis working. 🟡

---

## 10. Problem Statement

Two problems sit on top of each other, and only one is being worked on.

**The company's stated problem** is access: India's eye care need is enormous, under-served outside metros, and addressable by putting clinics closer to patients. The response is legible and fast — 249 facilities in June 2025, 288 at the March 2026 close, 304 at June 2026, sixty planned for FY27. 🟢

**The problem the numbers pose** is throughput. If the network grows 22.09% and surgical volume grows 15.47%, the average facility is doing **less** surgery than it was, and the quarter's revenue-per-site gain of **3.18%** is being carried entirely by a **9.10%** realisation increase that rests on a procedure mix representing **3.58%** of volume. A network can be extended indefinitely; a mix shift of half a percentage point a year cannot carry it indefinitely.

**The product problem underneath both** is that the step between a patient presenting and a procedure happening is unowned. **89.67%** of patients served in the quarter did not have surgery. Some fraction of them were told, correctly, to come back — and nothing in the company's published operating metrics distinguishes a patient who needed nothing from a patient who needed something later. That distinction is the asset. It is being created 882,000 times a quarter and discarded.

---

## 11. Market Research

Indian eye care demand is real and largely unmet, but the market a private chain can address is a slice of it, not the whole. The load-bearing public fact: under the National Programme for Control of Blindness and Visual Impairment, India performed **more than 98 lakh cataract surgeries in FY25**, the highest in five years, with **1,17,55,185 people** benefitting from the programme in that year. The five-year series — 35,50,765 (FY21), 61,98,830, 83,44,824, 90,29,242, 98,00,000+ — is a **28.89% compound annual rate**, and **8.54%** in the last step. Source: a Rajya Sabha written reply by the Minister of State for Health, 30 July 2025. 🟢

Against that, Dr Agarwal's Q1 FY27 cataract volume of 67,444 annualises to **269,776** — **2.75%** of the public programme's FY25 output, which performs **36.33×** as many cataract surgeries, free. 🟡 (period mismatch flagged, Appendix A-4)

The conclusion is not that the chain is small. It is that **cataract volume is not the contested resource — willingness to pay for a better version of it is.** That is exactly where the company is competing, and it is why realisation, not volume, is doing the work in this quarter's numbers.

---

## 12. Industry Analysis

Single-specialty ophthalmology has become the most heavily capitalised niche in Indian healthcare: ASG Eye Hospitals raised ₹15 bn from General Atlantic and Kedaara and has publicly signalled an IPO; Maxivision took ₹13 bn from Quadria and has appointed bankers for a 2027 listing; Sharp Sight took InvAscent money. 🟡

The economics explain the interest. Cataract is high-volume, day-care, protocol-driven and equipment-led — the closest thing in medicine to a manufacturing line — which makes it scalable in a way that multi-specialty hospital beds are not. The risk it creates is uniform: every operator's growth plan is a rollout plan, and rollouts compete for the same surgeons in the same cities.

---

## 13. TAM / SAM / SOM

*Framework selection rationale: run in restricted form. No primary-sourced Indian ophthalmology market size exists in the filings examined, and third-party market estimates for this sector conflict widely. Rather than quote one, the market is sized from the company's own disclosed base and from a government-reported national volume.*

| Layer | Basis | Figure |
|---|---|---|
| Reference national volume | NPCB&VI cataract surgeries, FY25, Rajya Sabha reply | **98,00,000+** 🟢 |
| Reference national reach | NPCB&VI beneficiaries, all eye conditions, FY25 | **1,17,55,185** 🟢 |
| Company served base (annualised) | Q1 FY27 patients × 4 | **3,528,000** = **30.01%** of NPCB&VI beneficiaries 🟡 |
| Company cataract base (annualised) | Q1 FY27 cataract × 4 | **269,776** = **2.75%** of the public programme 🟡 |
| Obtainable, near term | One percentage point of surgical conversion on the existing served base | **8,820 surgeries/quarter**, **₹59.46 Cr** 🟡 |

The last row is the point of the exercise. The realistic near-term prize is not a share of a national volume the state supplies free; it is a fraction of a funnel the company already owns and does not report.

---

## 14. Competitor Analysis

*Framework selection rationale: restricted to entities that actually file. **ASG Eye Hospitals and Maxivision are the two nearest competitors and neither publishes audited financial statements** — ASG is private with an IPO announced but no DRHP on file as examined; Maxivision is private, Quadria-backed, carrying a CRISIL BBB+/Stable rating and a stated FY26 revenue ambition above ₹500 Cr. They are named here and **no estimate is constructed for either**. This is the fourth consecutive case study using that restriction.* 🟡

The comparator that does file is inside the group. **Dr Agarwal's Eye Hospital Limited** (BSE: 526783) is 72.67% held, separately listed, separately audited by the same auditor, and concentrated in the oldest markets — Tamil Nadu, Kerala, Rajasthan. It is, in effect, the mature half of the same company reporting on itself.

| Q1 FY27 | Group (consolidated) | Listed subsidiary (standalone) |
|---|---|---|
| Revenue from operations | ₹614.02 Cr, **+25.97%** | ₹142.97 Cr, **+22.28%** |
| Share of group revenue | — | **23.28%** |
| EBITDA | ₹177 Cr | ₹45.22 Cr |
| EBITDA margin on own revenue | **28.83%** | **31.63%** |
| Reported operating margin | 28.5% (on total income) | **30.26%**, down **148 bps** YoY |
| PAT | ₹55.02 Cr, +44.6% | ₹23.38 Cr, **+35.46%** |
| Effective tax rate | not disclosed at this level | **24.48%** (₹30.96 Cr PBT less ₹7.58 Cr tax reconciles exactly to PAT) |
| EPS | — | ₹48.38 from ₹36.72, **+31.75%** |
| Sequential on Q4 FY26 | — | revenue **+19.13%**, PAT **+43.97%** |

Three readings come out of this table, and the third is the one that matters.

First, the mature entity earns a **2.80 percentage point** better margin on its own revenue than the group does — the cleanest available measure of what the greenfield drag costs, and consistent with management's own statement that FY26's new branches lost about ₹30 Cr.

Second, it grew revenue more slowly (22.28% against 25.97%) and profit more slowly (35.46% against 44.6%) than the group. Maturity buys margin, not growth. That is the expected shape and it is reassuring.

Third — and this is the finding — **the mature entity's operating margin fell 148 bps while the group reported margin improvement.** Whatever produced the group's headline, it was not the oldest assets getting better. A rollout story is normally defended on the grounds that the mature core is compounding underneath the drag. In this quarter the core compressed. 🟡 (definitional caveat: the subsidiary's 30.26% is a third-party operating-margin computation, the group's 28.5% is the company's own operating-IndAS-EBITDA measure on total income, and the 31.63% above is computed here on revenue from operations — three bases, Appendix A-2)

---

## 15. SWOT

| Strengths | Weaknesses |
|---|---|
| Largest Indian eye care provider by revenue; 1,057 doctors 🟢 | Surgeries per facility **−5.42%** YoY 🟡 |
| Hub-and-spoke design; 304 facilities, ten countries 🟢 | Premium mix only **3.58%** of volume 🟡 |
| Net debt ₹62 Cr from ₹278 Cr 🟢 | Greenfield losses ~₹30 Cr = **17.86%** of FY26 PAT 🟢 |
| Realisation per surgery **+9.10%** 🟡 | Paramedical attrition **21–25%** 🟡 |
| **Opportunities** | **Threats** |
| 89.67% of served patients unconverted 🟡 | Public programme supplies **36.33×** the cataract volume, free 🟢 |
| Insurance penetration lifting premium cataract 🟡 | ASG, Maxivision and Centre for Sight competing for the same surgeons 🟡 |
| Amalgamation simplifies a confusing two-entity structure 🟢 | Deleveraging lever largely spent — **28.70%** of the reduction remains 🟡 |

---

## 16. Porter's Five Forces

*Framework selection rationale: run twice and merged into one table, because the business has two genuinely inverted halves. **Cataract is indication-driven, insurance-adjacent and competes with a free public alternative; refractive is elective, self-pay and competes with doing nothing.** Management's own FY26 commentary — that refractive grew more slowly than cataract — is the seam this double run explains.*

| Force | Cataract (74.05% of surgeries) | Refractive (4.39% of surgeries) |
|---|---|---|
| Buyer power | Low on need, high on price: the state performs 36.33× the volume free, capping the base price 🟢 | Very high: the procedure is optional and the alternative is spectacles 🟡 |
| Supplier power | High — IOL and femtosecond platform vendors sell the premiumisation the margin depends on 🟡 | High, and narrower: a handful of laser platforms 🟡 |
| New entrants | Moderate: protocolised, equipment-led, financeable — hence ASG, Maxivision, Sharp Sight 🟡 | Low: needs brand trust for an elective procedure on healthy eyes 🟡 |
| Substitutes | Government camps, charitable hospitals, standard-IOL surgery at any price point 🟢 | Spectacles and contact lenses — free-ish, reversible, and winning 🟡 |
| Rivalry | Intense on price, muted on outcome, because outcome is undisclosed 🟡 | Intense on marketing; growth is the slowest in the portfolio 🟡 |

The inversion is the insight. On cataract, demand exists and the company competes to be chosen and to upgrade the patient. On refractive, the company must create demand for a procedure nobody needs — and this is the segment management flagged as slowing. **The premiumisation thesis is working in the half where need is given, and stalling in the half where willingness must be manufactured.**

---

## 17. Business Model Canvas

| Block | Content |
|---|---|
| Value proposition | Advanced ophthalmic surgery, close by, with a premium tier 🟢 |
| Customer segments | Cataract patients 50+, refractive 18–35, retina and cornea referrals, spectacle and pharmacy buyers 🟢 |
| Channels | 304 owned facilities; primary clinics as feeders; referral networks 🟢 |
| Key activities | Surgery, consultation, diagnostics, retail; site commissioning 🟢 |
| Key resources | 1,057 doctors; surgical platforms; the brand; the clinical record 🟢 |
| Key partners | IOL and equipment vendors; insurers; international JV partners 🟡 |
| Cost structure | Clinical payroll, consumables, leases, D&A; greenfield ramp losses 🟢 |
| Revenue streams | Surgery, consultation, products (21.4% of revenue a year earlier) 🟢 |
| Customer relationships | Episodic and largely unmanaged between episodes — the gap the proposal addresses 🟡 |
---

## 18. Revenue Model

Three streams: surgical procedures, priced by technique and implant; services (consultation, refraction, diagnostics, non-surgical treatment); and products (opticals, contact lenses, pharmacy), which were **21.4% of operating revenue** in Q1 FY26 against services at 78.6%. 🟢

Total revenue per surgery — total operating revenue divided by surgeries — was **₹67,414** in Q1 FY27, up **9.10%**. That is not the company's own ARPS metric and is not comparable to it (§30, Appendix A-1). 🟡

---

## 19. Target Users

Four groups with almost nothing in common: the cataract patient over 50, usually accompanied, often price-anchored to a free alternative; the refractive patient aged 18–35 buying an elective outcome; the retina or cornea patient arriving on referral in a clinical hurry; and the spectacle or drop buyer, who is frequently the same person as the first group, later. 🟡

---

## 20. Personas

| Persona | Situation | What decides it |
|---|---|---|
| **Lakshmi, 61, Coimbatore** | Told at a primary clinic that one eye has an early cataract; vision is workable | Whether anyone contacts her when it stops being workable 🟡 |
| **Arjun, 27, Bengaluru** | Considering lenticular refractive surgery; has worn lenses for nine years | Price, recovery time, and fear — the segment management says is slowing 🟡 |
| **Mr Rao, 68, Hyderabad** | Cataract confirmed; choosing between standard and premium IOL | A ten-minute counselling conversation with no standard script 🟡 |
| **Dr Sneha, 34, consultant at a new spoke** | Site opened six weeks ago; her clinic list is thin | Whether the hub sends her surgery or she waits for footfall 🟡 |

---

## 21. Jobs To Be Done

| When… | I want to… | So that… |
|---|---|---|
| my vision has become annoying but not disabling | find out whether it is time yet | I neither operate early nor go blind waiting 🟡 |
| I am told to come back in a year | not have to remember | the decision happens when it should 🟡 |
| I am offered a ₹1.2 lakh lens over a ₹25,000 one | understand what I am buying | I am not upsold on my own eye 🟡 |

The middle job is the unserved one, and it is the only one whose completion the company could measure today with data it already holds.

---

## 22. User Journey

```
DISCOVER ──► CONSULT ──► DIAGNOSE ──► DECIDE ──────► SURGERY ──► FOLLOW-UP
(footfall,    (refraction, (indication  (price, fear,   (91,082)    (unmeasured
 referral,     diagnostics) recorded)    timing)                     publicly)
 walk-in)         │             │            │
 882,000 ────────►│────────────►│───► 89.67% EXIT HERE ◄─── no owner,
                                              │              no window,
                                              └──► ??? ◄──── no record published
```

The journey has a measured entrance (882,000), a measured exit through theatre (91,082), and an unmeasured leak of **790,918 patients** between them. Some of that leak is correct medicine. None of it is currently distinguished.

---

## 23. User Flow

Walk-in or referral → registration → vision testing and refraction → consultant examination → diagnosis recorded → either treatment, surgical scheduling, or advice to review later. 🟡

The terminal state "advice to review later" has no system consequence in anything disclosed: no owner, no date, no follow-up metric. 🟡

---

## 24. Information Architecture

Clinically the record is per patient per visit per facility; commercially the reporting unit is the facility and the quarter. The two do not meet, which is why a patient can be counted in footfall at one site and, a year later, counted as a new surgical case at another with no link between the two events. 🟡

---

## 25. UX Audit

The physical experience is the product, and its weakest moment is the exit interview that does not exist: a patient leaves with a verbal instruction and, at best, a paper prescription. 🟡

Everything about the in-visit experience is optimised for the visit; nothing is built for the interval between visits, which for a progressive disease is where the decision actually happens. 🟡

---

## 26. UI Audit

The digital surface is appointment booking and information, not care continuity; there is no published patient-facing artefact that carries a dated clinical indication forward. 🟠

---

## 27. Accessibility

The patient population is the one most poorly served by digital-first design — older, frequently low-vision by definition, often accompanied by a relative who makes the arrangements. Any recall mechanism that assumes the patient holds a smartphone excludes the majority of the cataract cohort; the accompanying relative is the real recipient. 🟡

---

## 28. Feature Breakdown

| Capability | Present | Evidence |
|---|---|---|
| Cataract surgery, standard and premium IOL | Yes; 67,444 in the quarter, **74.05%** of volume | 🟢 |
| Femtosecond-assisted cataract | Yes; **1,548**, +33.4% | 🟢 |
| Lenticular refractive | Yes; **1,712**, +36.2% | 🟢 |
| Refractive (all) | Yes; **3,998**, **4.39%** of volume | 🟢 |
| Retinal surgery | Yes; **3,861**, +30.0% | 🟢 |
| Anterior segment reconstruction | Yes; **286**, +15.8% | 🟢 |
| Corneal transplant | Yes; **589**, +10.1% | 🟢 |
| Optical and pharmacy retail | Yes; 21.4% of revenue a year earlier | 🟢 |
| Dated, owned clinical recall | **Not evidenced in any disclosure examined** | 🟠 |

Two things fall out of this table. The separately named specialised procedures total **7,996 — 8.78%** of surgeries; and once cataract, refractive and all five named lines are removed, **14,904 surgeries, 16.36%** of the quarter, are unclassified in public reporting. The disclosure is rich about the premium tip and silent about a sixth of the volume.

**The asset that is present but unused is the indication itself.** Eight hundred and eighty-two thousand examinations a quarter, performed by 1,057 doctors, each producing a clinical judgement about whether and when an eye needs surgery. The company sells the surgery. It does not appear to manage the judgement.

---

## 29. AI Capabilities

Nothing in the disclosures examined evidences a deployed AI capability in screening, triage or recall at this company; the tele-ophthalmology and AI-screening language in the sector belongs mostly to competitors' fundraising narratives. 🟠

This is worth stating plainly rather than inventing: **the company has not publicly disclosed an AI product.** The proposal in §50 deliberately requires none — it needs a record, an owner and a date.

---

## 30. Product Metrics

| Metric | Q1 FY27 | Q1 FY26 | Change |
|---|---|---|---|
| Revenue from operations | ₹614.02 Cr | ₹487.42 Cr | **+25.97%** 🟢 |
| Surgeries | 91,082 | 78,882 | **+15.47%** 🟢 |
| Facilities | 304 | 249 | **+22.09%** 🟢 |
| **Surgeries per facility** | **299.61** | **316.80** | **−5.42%** 🟡 |
| **Revenue per facility** | **₹2.0198 Cr** | **₹1.9575 Cr** | **+3.18%** 🟡 |
| **Revenue per surgery** | **₹67,414** | **₹61,791** | **+9.10%** 🟡 |
| Patients served | 882,000+ | not disclosed in sources examined | — 🟠 |
| **Surgical conversion** | **10.33%** | **not computable** | — 🟡 |
| Doctors | 1,057 | — | +9.19% on FY26's 968 🟢 |
| Surgeries per doctor | 86.17 | — | — 🟡 |
| Patients per doctor | 834.44 | — | — 🟡 |
| Net debt | ₹62 Cr | ₹278 Cr | **−77.70%** 🟢 |

**The internal consistency check that makes the thesis safe.** A 9.10% gain in revenue per surgery multiplied by a 5.42% fall in surgeries per facility predicts a **3.19%** change in revenue per facility; the directly computed figure is **3.18%**. The two differ by **0.0046 of a point** — which is the rounding of the published inputs, not a modelling error — and that means the decomposition is not an artefact of picking denominators.

**Two honest gaps.** The prior-year patient count is not disclosed in any source examined, so **the conversion rate cannot be trended** — the 10.33% is a level, not a direction, and the case study does not claim otherwise. And the company's own ARPS metric (**₹42,900** for FY26, up 8.5%) is **not** the same quantity as the ₹67,414 derived here: the derived figure is **1.57×** it, a residual of **₹24,514** per surgery representing consultation, diagnostics and retail revenue that the company's metric excludes. They are not forced to reconcile (Appendix A-1).

---

## 31. North Star Metric

**Proposed: ICR/1k — Indicated Conversions per 1,000 indicated deferrals.**

A deferral counts in the denominator when the examining surgeon records, at the index visit, both a clinical indication and a review window. A conversion counts in the numerator only if **all four** hold:

1. the indication and window were recorded **before** any recall activity on that patient;
2. surgery occurred **within** the recorded window;
3. the pre-operative grade **meets the published indication threshold** recorded at index — no upgrade;
4. the indication was **not reclassified** after the fact.

**The denominator is the design choice, as it has been every time in this series.** It is indicated deferrals — not footfall, not bookings, not surgeries. Recording more deferrals without converting them *lowers* the metric, so the register cannot be padded. Withholding a deferral to protect the ratio is the opposite failure, and it is caught by the guardrail in §40 and by the audit function's sampling of index records, not by this metric.

**Guardrail, carried from here to §55: UPI-90 — Unindicated Procedure Incidence at the 90th percentile of recall intensity.** In the decile of facility-quarters where the recall engine fires hardest, the share of surgeries whose pre-operative grade did not meet the published indication threshold. Reported **by facility and by surgeon cohort, never in aggregate**, because an aggregate can absorb one bad site indefinitely.

---

## 32. Product Analytics

The instrumentation required already exists clinically and is missing commercially: indication, grade, review window, recall attempt, outcome. Nothing in it needs new hardware. 🟡

What is genuinely hard is not capture but **provenance** — proving a conversion was against a pre-registered indication rather than one written after the recall call. That is a build-time constraint, specified in §51.

---

## 33. AARRR

*Framework selection rationale: used in modified form. For a surgical provider, "activation" is not a sign-up — it is the first correctly indicated procedure, and "retention" is the second eye, the second condition, or the spectacle purchase.*

| Stage | Reading |
|---|---|
| Acquisition | 882,000 patients a quarter; **2,901 per facility** 🟡 |
| Activation | 91,082 surgeries — **10.33%** 🟡 |
| Retention | Not publicly reported; second-eye and repeat-condition rates undisclosed 🟠 |
| Revenue | ₹67,414 per surgery, **+9.10%** 🟡 |
| Referral | Undisclosed; the strongest asset in the model and the least measured 🟠 |

---

## 34. HEART

| Dimension | Signal and status |
|---|---|
| Happiness | No published NPS or CSAT 🟠 |
| Engagement | Visits per patient undisclosed 🟠 |
| Adoption | Premium mix **3.58%** of surgeries 🟡 |
| Retention | Second-eye conversion undisclosed 🟠 |
| Task success | Surgical outcome rates undisclosed 🟠 |

Four of five dimensions cannot be filled from public disclosure. For a clinical business that is not unusual, and it is the reason a proposal built on published, audited conversion reporting is a governance change as much as a product one.

---

## 35. Growth Strategy

The strategy is explicit and consistent: add facilities, premiumise procedures, and let insurance penetration lift realisation. FY27's plan is **sixty new facilities — 20.83% of the 288-site network** at the FY26 close — funded partly by acquisition, with cash outflow for acquisitions guided down from **₹85 Cr in FY26 to ₹60–65 Cr** (midpoint **₹62.5 Cr**, **−26.47%**). 🟢

Q1 delivered eighteen gross additions, two closures, sixteen of them surgical — an annualised gross pace of **72**, which is **1.20×** the stated plan. The company is running ahead of a plan that is itself the most aggressive in its history, while surgeries per facility decline. 🟡

**And the strategy is silent on the funnel.** Nothing in the published growth narrative addresses the 89.67%.

---

## 36. Growth Loops

The intended loop is geographic: a new spoke generates footfall → footfall feeds hub surgery → surgical cash funds the next spoke. It works only if footfall per spoke and conversion per patient hold, and the disclosed data says throughput per site is falling. 🟡

The loop the proposal would add is temporal: an examination produces a dated indication → the indication produces a recall → the recall produces surgery at the right time → the surgery produces a second-eye indication. It compounds without capex. 🟡

---

## 37. Network Effects

There are none in the classic sense; there are density effects. More sites in a city shorten travel and raise brand salience, but they also cannibalise, which is one plausible reading of the **−5.42%** throughput move and is given equal weight in ASSUMPTIONS Part 1. 🟡

---

## 38. Product Strategy

Two coherent strategies are available and only one is being pursued.

**Extend the network.** Buy footfall by being nearer. Known cost, known drag (₹30 Cr in FY26, **4.89%** of EBITDA and **17.86%** of PAT), known lag, and — critically — a lever that does not care whether the patient in front of you converts.

**Convert the network.** Take the 882,000 patients already arriving and raise the fraction who get the procedure they need, when they need it. **One point is ₹59.46 Cr a quarter, 9.68% of revenue, the output of 29.44 average facilities and 1.84× the sixteen surgical facilities opened in the quarter** — with no leases, no commissioning ramp and no greenfield loss.

The second is cheaper by an order of magnitude and harder by two, because it requires a clinical governance apparatus that does not exist and creates a hazard that does not currently exist either. The honest recommendation is not "stop expanding" — expansion is defensible and the balance sheet supports it. It is that **a company adding 20.83% to its network in a year should be able to state what happened to the other 89.67% of its patients, and it currently cannot.**

---

## 39. Monetization

Monetisation of a conversion improvement needs no new pricing: it is the existing procedure at the existing price, performed for a patient who would otherwise have drifted. That is what makes it attractive and also what makes it dangerous, because the same mechanism monetises a procedure that should not have happened. 🟡

The pricing change worth considering is the opposite direction — publishing indication thresholds, which constrains revenue and is the concession that makes the rest credible (§40). 🟡
---

## 40. Trust & Safety

**This section is placed before the feature proposal deliberately, because the proposal creates a harmful incentive and the guardrail has to be specified before the metric that needs it.** In this series that reordering has been made when a proposal displaced a walk-up buyer (Day 60) or when measurement could become marketing (Day 61). This one is more serious than either: the failure mode is **surgery on an eye that did not need surgery**, on a patient population that is elderly, frequently accompanied rather than self-advocating, and structurally deferential to the surgeon in the room.

Indian ophthalmology has a documented history here. The public-programme literature is explicit that cataract surgery counted as volume, with quality treated as a secondary consideration, can add to the burden of blindness rather than reduce it. Any private operator that starts reporting a conversion ratio is standing exactly where that failure occurred, with better equipment and a stronger commercial incentive. 🟡

Five constraints, all of which are build requirements in §51 and not aspirations:

1. **The indication is recorded before the recall exists.** A conversion only counts against an indication registered at the index visit. Technically this is an append-only record with a server-side timestamp, and the recall system is denied write access to the indication field. Without this the metric is self-certifying.
2. **The threshold is published.** The clinical grade at which each indication justifies surgery is published externally. A private threshold is a policy, and policies get waived the first time a quarter is short.
3. **UPI-90 is owned by a function with no revenue target.** A Clinical Indication Audit function reporting to the board's clinical governance committee, sampling operated cases against their index records, publishing by facility and surgeon cohort.
4. **Breach suspends the recall engine automatically.** At a facility in breach, recall stops by default rather than continuing while someone argues for an exception. Release is the decision that requires a case, not suspension.
5. **The under-reporting failure is audited, not metricated.** A surgeon can protect ICR/1k by not recording a deferral at all. No ratio catches that; index-record sampling does, and that is the audit function's second job.

Two further constraints belong here. **Recall contact goes to the accompanying relative where the patient nominates one** — the §27 finding — and **no recall may be initiated by anyone with a variable component tied to surgical volume at that facility.**

---

## 41. Technical Architecture

Nothing about the network's clinical stack is publicly disclosed in the documents examined; the architecture below is what the proposal requires, not a description of what exists. 🟠

Three components: an append-only indication ledger keyed to patient and index visit; a scheduling and recall service that can read indications but never write them; and an audit extract that joins operated cases to their index records without either system being able to alter the other. 🟡

---

## 42. Data Flow

```
EXAMINATION ──► INDICATION LEDGER (append-only, surgeon-signed, timestamped)
                        │                    ▲
                        │  read-only         │  NO WRITE PATH
                        ▼                    │
                 RECALL SERVICE ─────────────┘
                        │
                        ▼
                  SCHEDULING ──► THEATRE ──► OPERATED-CASE RECORD
                                                     │
                        ┌────────────────────────────┘
                        ▼
             CLINICAL INDICATION AUDIT (joins operated case to index record)
                        │
                        ▼
             PUBLISHED: ICR/1k per facility · UPI-90 per facility and cohort
```

The single architectural fact that makes the metric honest is the absent arrow: the recall service cannot write to the ledger it is measured against.

---

## 43. API Ecosystem

No public API is disclosed. 🟠 The proposal's only external interface is a published indication-threshold document and a published per-facility report, both of which are documents rather than endpoints. 🟡

---

## 44. Privacy & Security

An indication register is a longitudinal record of progressive disease across millions of identified individuals — a higher-sensitivity asset than a visit log, and one that is attractive to insurers. 🟡

Under India's Digital Personal Data Protection framework, health data of this kind requires purpose limitation that the proposal must state narrowly: the register exists to schedule the patient's own care, recall consent is separately captured and revocable, and the register is not a marketing list and may not be shared with an insurer or a pharmaceutical partner. Aggregate conversion statistics leave; individual indication histories do not. 🟡

---

## 45. Pain Points

| # | Pain point | Evidence |
|---|---|---|
| 1 | **Throughput per facility is falling** while the network expands | 316.80 → 299.61 surgeries per site, **−5.42%** 🟡 |
| 2 | Revenue per site is carried entirely by realisation | +3.18% site revenue against +9.10% realisation 🟡 |
| 3 | The realisation lever is thin | premium lines **3.58%** of volume; mix shift **0.51pp** YoY 🟡 |
| 4 | Refractive — the discretionary, self-pay half — is the slowest-growing segment | management's own FY26 commentary 🟢 |
| 5 | **89.67% of patients served do not convert, and nobody owns it** | 91,082 of 882,000 🟡 |
| 6 | The prior-year conversion rate cannot even be computed from disclosure | patient count not disclosed for Q1 FY26 🟠 |
| 7 | Profit growth leaned on deleveraging, now largely spent | PAT +44.6% vs EBITDA +25.2%, a **19.40pp** gap; **28.70%** of headroom left 🟡 |
| 8 | The mature core's margin **fell 148 bps** while the group reported improvement | subsidiary's own filing 🟡 |
| 9 | Greenfield drag is material and scaling with the plan | ~₹30 Cr = **17.86%** of FY26 PAT; sixty sites planned 🟢 |
| 10 | **16.36% of surgeries are unclassified** in public reporting | 14,904 of 91,082 🟡 |
| 11 | Paramedical attrition of 21–25% undermines any new operating protocol | management commentary 🟡 |
| 12 | Two near-identically named listed entities confuse the public record | pending NCLT amalgamation 🟢 |

---

## 46. Opportunity Mapping

| Opportunity | Cost | Ceiling |
|---|---|---|
| Open more facilities | High capex, ~₹30 Cr/yr drag, 12–18 month ramp | Large but slow; dilutes throughput while ramping 🟡 |
| Premiumise further within cataract | Low capex, vendor-dependent | Constrained: **0.51pp** mix shift per year 🟡 |
| Grow refractive | Marketing-led | Weakest segment by management's own account 🟡 |
| Attach optical and pharmacy | Low | Real but small per head 🟡 |
| **Convert the existing funnel** | **Governance-heavy, capex-free** | **₹59.46 Cr per point per quarter = 29.44 facilities' output** 🟡 |

---

## 47. RICE

*Framework selection rationale: run with a stress rule drawn from the company's own evidenced conversion rate. Reach is expressed in thousands of patients touched per quarter. The stress rule multiplies the Reach of every initiative that requires a patient to do something by **10.33%** — the rate at which, on this company's own Q1 FY27 numbers, a patient-facing proposition actually lands. One initiative is exempt because it requires no patient to do anything at all.*

| Initiative | Reach (k) | Impact | Confidence | Effort | **Baseline** | **Stressed** |
|---|---|---|---|---|---|---|
| Optical and pharmacy attach at existing footfall | 882.0 | 0.25 | 0.60 | 4.0 | **33.08** | 3.42 |
| High-end IOL counselling standardisation | 67.4 | 1.00 | 0.80 | 3.0 | **17.99** | 1.86 |
| ***Agarwal Indicated* (PROPOSED)** | 88.2 | 0.80 | 0.60 | 4.0 | **10.58** | **1.09** |
| Greenfield commissioning gate and ramp playbook — **EXEMPT** | 52.2 | 0.50 | 0.90 | 2.5 | **9.40** | **9.40** |

**Baseline order:** attach → IOL counselling → **proposal (3rd of 4)** → greenfield gate.
**Stressed order:** **greenfield gate → attach → IOL counselling → proposal (4th and last).**

`verify.py` asserts all four of these programmatically: that the proposal is third at baseline, that it is last under stress, that the exempt initiative wins under stress, and — the constraint that makes the exercise honest rather than staged — **that the proposal is the weakest of the stressed initiatives at baseline**, which is the only configuration in which it can finish last. The exempt initiative beats it **8.60×** once stressed; the proposal loses **89.67%** of its score, which is precisely the non-conversion rate, because that is what the stress rule is.

**A harsher stress rule was available and was not used.** The premium-procedure share, **3.58%**, is arguably the better read of how often a *new* proposition lands at this company, and it would have made the demotion more severe. The generous multiplier is used, and the proposal still loses.

**Why losing is the right answer.** The greenfield commissioning gate — published readiness criteria a site must clear before opening, and a standard ramp playbook with a named owner — needs no patient, no surgeon behaviour change and no clinical governance apparatus. At a company whose surgeries per facility just fell **5.42%** while it opened sites at **1.20×** its own record plan, the intervention that improves the sites it is already committed to opening should be sequenced ahead of one that asks 1,057 doctors to change how they document. **Do the thing that requires nobody's cooperation first.** The proposal is where the compounding lives, and it is still second in line.

---

## 48. MoSCoW

| | Scope |
|---|---|
| **Must** | Append-only surgeon-signed indication ledger; published thresholds; UPI-90 with automatic suspension; audit function with no revenue target |
| **Should** | Relative-nominated recall contact; per-facility ICR/1k publication; second-eye indications inside the same register |
| **Could** | Insurer-facing aggregate reporting; recall in regional languages by facility catchment |
| **Won't** | Any recall incentive tied to surgical volume; any sharing of individual indication histories; any AI triage in v1 |

The "Won't" row is the load-bearing one, and the first item in it stays excluded permanently rather than for v1.

---

## 49. Kano

| Feature | Category |
|---|---|
| Surgery happening at the right time | Basic — patients assume it, the system does not deliver it 🟡 |
| Being contacted when the eye is ready | Attractive today; will become Basic once any competitor does it 🟡 |
| Published indication thresholds | Attractive, and unusually so: nobody in the sector publishes them 🟡 |
| Premium IOL options | Performance — more choice, more realisation, diminishing delight 🟡 |

---

## 50. Feature Proposal — *Agarwal Indicated*

**What it is.** A clinically gated register of indicated-but-deferred surgery, and an obligation attached to it.

At the index visit, the examining surgeon records two things alongside the diagnosis: the **indication** (condition, eye, clinical grade) and the **review window** (the interval after which this eye should be re-examined, in the surgeon's judgement). Both are signed and timestamped into an append-only ledger that the recall system can read and can never write. The **facility that made the diagnosis owns the return** — not a central call centre, not the hub, the site whose consultant made the judgement. When the window opens, the patient is contacted, at the nominated relative's number where one is given, and offered re-examination, not surgery.

Conversion is then reported per facility as **ICR/1k** against indications registered *before* any recall activity, and the **Clinical Indication Audit** function publishes **UPI-90** — the share of surgeries in the hardest-recalling decile of facility-quarters whose pre-operative grade failed the published threshold — by facility and surgeon cohort, with automatic recall suspension on breach.

**Why this and not something else.** Because the asset already exists and is being destroyed 790,918 times a quarter. The company employs 1,057 doctors who each make dozens of judgements a day about when an eye will need surgery. Those judgements are the highest-value forward-demand signal in the business — better than any marketing funnel, because they are clinical, dated and specific to an individual — and the published operating metrics contain no evidence that any of them survives the patient leaving the building.

**Why it is not already there.** The company's own published disclosure reports footfall and surgeries as separate absolute numbers and never as a ratio; there is no disclosed recall metric, no disclosed deferral register, and no disclosed indication threshold. Verifying from a company's own published material that the thing you are proposing does not already exist is a standing rule of this series, and in this case the absence is the finding: **a business whose growth depends on realisation per patient does not publish anything about the patients who did not convert.** 🟠

**The shape, and how it differs from the last eight proposals.** Day 55 captured a signal that was being lost; Day 56 priced an outcome; Day 57 made an intermediary carry risk; Day 58 subtracted negative-contribution volume; Day 59 built a comparison layer; Day 60 sold forward commitment; Day 61 metered a claim; Day 62 imposed a disclosed constraint on itself. This is a **latent-demand conversion instrument with a clinical gate** — it converts a record the company already creates into a time-bound obligation, and pairs it with a published threshold whose only function is to limit what the obligation can be used for. The gate is not a compliance footnote; it is half the mechanism.

**What it is not.** It is not a marketing CRM, not a reminder SMS campaign, and not a screening-camp programme. Those all increase footfall. This increases the fraction of existing footfall that receives correctly timed care, which is a different quantity with a different failure mode.

---

## 51. PRD

**Problem.** 89.67% of patients served in Q1 FY27 did not have surgery. An unknown but material fraction were clinically indicated for later intervention. No owner, window, record or metric exists for them in anything the company publishes.

**Goals.** Raise correctly timed surgical conversion on the existing served base; make the conversion rate a reported, audited, per-facility figure; keep unindicated intervention flat or lower while doing it.

**Non-goals.** Raising footfall. Raising premium mix. Increasing surgical volume as an end in itself — which is explicitly excluded, because volume is the metric whose pursuit created ophthalmology's historical quality failure.

**Success metrics.** ICR/1k as North Star; UPI-90 as guardrail; surgeries per facility as the business-level read-through, since the whole point is throughput on assets already built.

**User stories.**
- As an examining surgeon, I record an indication and a review window in under fifteen seconds, because anything slower will not survive a full clinic list.
- As a patient's daughter, I get a call when my mother's eye is due for re-examination, from the clinic that saw her.
- As the audit lead, I can pull every operated case in a facility-quarter and join it to the index record that justified it.
- As a facility head, I see my own ICR/1k and UPI-90 monthly and know that a UPI-90 breach stops my recalls without my involvement.

**Functional requirements.** Indication capture at the point of examination; append-only signed ledger with server-side timestamps; review-window scheduling; facility-owned recall queues; relative-nominated contact; per-facility reporting; audit extract joining operated cases to index records.

**Non-functional requirements.** Sub-fifteen-second capture; ledger immutability enforced at the database layer, not in application code; recall service has read-only credentials on the indication table, verified by an automated test in the build pipeline that fails the build if a write path exists; audit extract independently credentialed.

**Acceptance criteria.** No conversion can be counted against an indication whose timestamp post-dates the first recall event on that patient. No user with a surgical-volume-linked variable component can initiate a recall. A UPI-90 breach suspends recall at that facility within one reporting cycle without human action. Published thresholds are versioned and a change is visible.

**Risks.** Documentation burden at the point of care; attrition of 21–25% among paramedical staff eroding protocol adherence; and the central risk, that the metric drives volume — addressed in §40 and tested in §54.

---

## 52. Wireframes

**Index-visit capture (consultant view, embedded in the existing examination screen)**

```
┌──────────────────────────────────────────────────────────────┐
│ LAKSHMI R · 61 F · MRN 88421 · Coimbatore (Spoke)            │
├──────────────────────────────────────────────────────────────┤
│ Diagnosis   [ Nuclear sclerosis, R eye            ▾ ]        │
│ Grade       [ NS2 ▾ ]   Published threshold for surgery: NS3 │
│                                                              │
│ ● Surgery now      ○ No intervention indicated               │
│ ○ INDICATED, DEFERRED  ← review window [ 12 ] months         │
│                                                              │
│ Recall contact   ○ Patient   ● Relative  [ Priya · 98xxx ]   │
│                                                              │
│ [ SIGN AND CLOSE ]        signed entries cannot be edited    │
└──────────────────────────────────────────────────────────────┘
```

**Facility scorecard (facility head view, monthly)**

```
┌──────────────────────────────────────────────────────────────┐
│ COIMBATORE SPOKE · Aug 2026                                  │
├──────────────────────────────────────────────────────────────┤
│ ICR/1k              412   ▲ 38    (of 1,000 due deferrals)   │
│ Deferrals registered 1,204 ▲ 96                              │
│ Windows open, not yet contacted  63   ⚠                      │
│                                                              │
│ UPI-90               1.8%  ▲ 0.4   THRESHOLD 3.0%            │
│ Recall status        ACTIVE                                  │
│                                                              │
│ ⓘ A UPI-90 breach suspends recall automatically.             │
└──────────────────────────────────────────────────────────────┘
```

---

## 53. Rollout Plan

**Phase 0 — two analyst-weeks, on records the company already holds, and it must be able to kill the proposal cheaply.**

Take 5,000 historical index visits across three mature facilities where a deferral-equivalent note exists in the clinical record, and follow each patient forward twelve to twenty-four months.

- **K1:** fewer than 20% of deferral-equivalent patients were subsequently operated anywhere in the network. If they mostly never came back and never appear again, the register has nothing to convert and the proposal dies.
- **K2 — named as the one most likely to fire:** the deferral note is not reliably recorded in the existing clinical record, so there is no historical population to measure and no evidence the capture behaviour will survive a full clinic list. This is the honest weak point: the proposal assumes documentation discipline that has never been measured at this company.
- **K3:** operated cases cannot be joined to index records at all, because the patient identifier does not persist across facilities — the §24 architecture risk. If the join fails, the metric cannot be audited and must not be published.

Phase 0 proceeds to pilot only if usable joins are achieved on **at least 4,000 of the 5,000** records.

**Phase 1 — pilot, two quarters, six facilities in two clusters.** Capture, ledger, facility-owned recall, published thresholds, audit function stood up before the first recall is made.
**Phase 2 — scale by cluster, gated on UPI-90 holding under 3.0% in every pilot facility, not on the cluster average.**
**Phase 3 — external publication of per-facility ICR/1k, which is the point at which the mechanism becomes credible rather than internal.**

---

## 54. A/B Testing

Three arms, and the second exists to kill the proposal.

| Arm | Design |
|---|---|
| **A — control** | Existing practice: verbal advice, no register, no owner |
| **B — falsification arm** | A generic reminder programme: undated, un-indicated, centrally run SMS and call recall to *all* non-converting patients at 9–12 months. This delivers the *benefit* (contact) without the *apparatus* (indication, window, ownership, threshold, audit). **If B matches A+ on conversion, the apparatus is theatre and the proposal should be cancelled in favour of a campaign.** |
| **C — full proposal** | Indication ledger, surgeon-set window, facility-owned recall, published threshold, audit |

**Pre-registered decision rule.** Arm C proceeds only if it beats Arm B by **more than 8 percentage points on ICR/1k across two full booking cycles including one non-peak quarter**, with **UPI-90 no worse than control in every individual facility** — measured per facility, not pooled, because pooling is how one bad site hides.

A second pre-registered rule constrains the win: if Arm B raises surgical volume *more* than Arm C while UPI-90 rises in B, that is the expected signature of untimely surgery and B must not be adopted on volume grounds.

---

## 55. KPI Dashboard

| KPI | Owner | Current | Target |
|---|---|---|---|
| **ICR/1k** (North Star) | Facility head | Not measured | Pilot baseline + 8pp vs Arm B |
| **UPI-90** (guardrail) | Clinical Indication Audit | Not measured | < 3.0% per facility |
| Surgeries per facility | COO | **299.61**, −5.42% | Positive YoY |
| Revenue per surgery | CFO | **₹67,414**, +9.10% | Hold |
| Premium mix | CMO | **3.58%** | Monitor; not a target |
| Greenfield drag | CFO | ~₹30 Cr FY26 | Falling as a share of EBITDA from **4.89%** |
| Net debt headroom used | CFO | **77.70%** of the reduction banked | Disclose the remaining lever |
| Windows open, uncontacted | Facility head | Not measured | < 5% of due |

**Early warning row, and it is the first one.** The thesis says throughput per facility is falling because the network is outgrowing surgical demand creation. **If Q2 FY27 shows surgeries per facility flat or rising while the facility count keeps growing above 20%, the thesis is wrong** — the ramp was simply young, and the company will have demonstrated it. Both numbers are published quarterly by the company itself.
---

## 56. Product Roadmap

| Window | Focus |
|---|---|
| Q3 FY27 | Phase 0 backtest on 5,000 index visits; audit function chartered; thresholds drafted |
| Q4 FY27 | Six-facility pilot; Arms A/B/C running; nothing published externally yet |
| Q1 FY28 | Decision gate on the pre-registered rule; scale by cluster or cancel in favour of Arm B |
| FY29 | Per-facility ICR/1k published; second-eye indications inside the register |

---

## 57. Risks & Mitigation

| Risk | Severity | Mitigation |
|---|---|---|
| **Conversion metric drives unindicated surgery** | Severe | Pre-registered indications, published thresholds, UPI-90 with automatic suspension, audit function with no revenue target (§40) |
| Deferrals go unrecorded to protect the ratio | High | Index-record sampling by the audit function; no ratio can detect this |
| Documentation burden defeats capture | High | Sub-fifteen-second requirement; K2 tests it before scale |
| Paramedical attrition of 21–25% erodes protocol | Medium | Capture sits with the consultant, not support staff 🟡 |
| Patient identifier does not persist across facilities | Medium | K3 kills the metric rather than publishing an unauditable one |
| Greenfield drag scales with the sixty-site plan | Medium | The exempt RICE initiative addresses precisely this 🟡 |
| Deleveraging tailwind is spent | Medium | **28.70%** of the reduction remains; profit growth must come from operations 🟡 |
| Register becomes an insurer asset | High | Purpose limitation in §44; aggregates leave, histories do not |

---

## 58. Future Vision

The version of this company worth owning in five years is not the one with the most clinics. It is the one that can say, of every person who walked through its doors, whether they needed something, when, and whether they got it — and can prove the answer was not inflated. 🟡

That is also the only defensible position against a competitor with cheaper capital, because a rival can copy a rollout plan in a quarter and cannot copy a decade of dated clinical indications. 🟡

---

## 59. PM Lessons

**1. Divide two disclosed growth rates before believing either.** Revenue +25.97% and surgeries +15.47% are both good numbers. Facilities +22.09% turns them into a throughput decline. The case study is three divisions of four integers the company published itself.

**2. Reconstruct the headline from its components as a self-check.** A 9.10% realisation gain times a 5.42% throughput loss predicts the 3.18% revenue-per-site move to within 0.0046 of a point. If it had not closed, the decomposition would have been an artefact of denominator choice, and there would have been no case study.

**3. When a group and its own listed subsidiary both file, you have a controlled experiment.** The mature entity's margin fell 148 bps in the quarter the group reported improvement. No outside comparator could have produced that, and Day 62 learned the same lesson from two rating rationales on one company.

**4. Size the premium story before repeating it.** Femto +33.4% and lenticular +36.2% are real and they are 3.58% of volume, supplying 6.91% of the quarter's additional surgeries. Growth rates on small bases are the most quotable and least load-bearing numbers in any results release.

**5. Look for the funnel step nobody owns.** The most valuable sentence in this case study — one conversion point is worth 29.44 facilities' quarterly revenue — comes from dividing two numbers that appear in the same press release and are never divided.

**6. If your proposal could hurt someone, design the guardrail before the metric.** A conversion target in ophthalmology is a target on elderly eyes. Putting §40 before §50 is not a formatting choice.

**7. Report the gap you could not close.** The prior-year patient count is not disclosed, so the conversion rate has no trend. Saying so costs the case study its most dramatic possible claim and is the reason the rest can be trusted.

---

## 60. PM Interview Questions

1. Revenue per facility rose 3.18% while revenue per surgery rose 9.10%. What do you need to know before calling that good or bad?
2. You are handed a 10.33% surgical conversion rate and no prior-year figure. What do you do first?
3. Design a conversion metric for a surgical business that cannot be gamed by operating on people who do not need it. Name the failure your metric cannot catch.
4. The group's margin improved and its most mature subsidiary's fell 148 bps. Which one do you believe, and what would settle it?
5. Your proposal ranks last under your own stress test, behind an initiative you did not propose. Do you ship it? Defend the sequencing.
6. Premium procedures grew 33–36% and are 3.58% of volume. Write the one-sentence version a CEO should hear.
7. The public system performs 36.33× your cataract volume, free. Is that a threat, a floor, or irrelevant?

---

## 61. References

**Company and results disclosure**
1. Dr Agarwal's Health Care Limited, Q1 FY27 results and earnings-call disclosure, 4 August 2026 — revenue ₹614.02 Cr, PAT ₹55.02 Cr, EBITDA ₹177 Cr, 304 facilities, 91,082 surgeries, procedure-level volumes, net debt.
2. Dr Agarwal's Health Care Limited, FY26 results and earnings call, May 2026 — total income ₹2,125 Cr, PAT ₹168 Cr, EBITDA ₹614 Cr and 28.9% margin, ~₹30 Cr greenfield loss, FY27 plan of 60 facilities, acquisition outflow guidance, ARPS ₹42,900, paramedical attrition.
3. Dr Agarwal's Eye Hospital Limited (BSE: 526783), Q1 FY27 standalone unaudited results, board meeting 3 August 2026 — revenue ₹142.97 Cr, EBITDA ₹45.22 Cr, PBT ₹30.96 Cr, tax ₹7.58 Cr, PAT ₹23.38 Cr, EPS ₹48.38.
4. Dr Agarwal's Eye Hospital Limited, Q1 FY26 standalone results — revenue ₹116.92 Cr, PAT ₹17.26 Cr, OPM 31.76% (Capital Market).
5. Dr Agarwal's Health Care Limited, DRHP, September 2024 — network composition at 31 March 2024, IPO structure, selling shareholders.
6. Dr Agarwal's Health Care Limited, Q1–Q4 FY26 quarterly disclosures — facility counts at 249 / 258 / 269 / 288, H1 FY26 surgeries 157,281, Q3 FY26 surgeries 81,002.
7. Corporate announcements, June–September 2026 — amalgamation approvals, NCLT listing, subsidiary stake at 72.67%, analyst roadshow 16–18 September 2026.

**Government and regulatory**
8. Rajya Sabha, written reply of the Minister of State for Health and Family Welfare, 30 July 2025 — NPCB&VI cataract surgeries FY21–FY25 and beneficiary counts.
9. Ministry of Health and Family Welfare / PIB, NPCB&VI and Netra Jyoti Abhiyan programme material — mission-mode cataract campaign and targets.
10. Ministry of Corporate Affairs registry data — CIN L85100TN2010PLC075403, incorporation 19 April 2010, authorised and paid-up capital, directors.

**Sector and comparator context**
11. Published coverage of ASG Eye Hospitals' and Maxivision's IPO preparations and funding, January–July 2026 — used only to establish that neither files audited results.
12. Brokerage coverage of Dr Agarwal's Health Care, March 2025 – June 2026 — used for the FY26 ARPS figure and flagged where undated (Appendix A-5).

---

## 62. About the Author

**Gaurav Singh** — Product Manager, New Delhi. Background in yoga therapy and behavioural science; product experience across digital mindfulness and wellness platforms. Writing one evidence-based product case study a day for ninety days, all of the remaining ones in healthtech.

The interest here is specific: eye care is the clearest example in Indian healthcare of a funnel that is clinically well-understood and commercially unmanaged.

---

## 63. License

Analysis and commentary released for non-commercial, educational use with attribution. All financial and operating figures belong to their sources and are cited in §61. No company logo, marketing asset or copyrighted image is reproduced. Derived figures are the author's own and are reproducible from `verify.py`.

---

## 64. Self Review

**What is strong.** The thesis rests on four integers the company published — 91,082, 78,882, 304, 249 — and two divisions anyone can repeat. The decomposition self-checks to 0.02 of a point. The comparator is the company's own separately audited subsidiary, which is a stronger instrument than any outside peer. The proposal's central hazard is identified before the proposal is specified, and the falsification arm is built to kill it.

**What is weak, stated plainly.**

- **The conversion rate has no trend.** Q1 FY26 patient volume is not disclosed in any source examined. The 10.33% is a level. Every claim built on it is a claim about scale, not about deterioration.
- **The 882,000 is a floor.** The company said "over 8.8 lakh". If the true figure is 920,000, conversion is 9.90% and every conversion-derived figure moves. The direction of that error makes the opportunity *larger*, so the estimate is conservative against the argument — but it is an estimate.
- **The −5.42% throughput move has an innocent reading** and it is given equal weight in ASSUMPTIONS Part 1: sixteen surgical facilities opened inside the quarter, and a site that opened in June contributes a full facility to the denominator and almost no surgery to the numerator. The mature-network throughput number that would settle this is not disclosed.
- **The margin compression sits inside rounding.** EBITDA is reported to the nearest ₹1 Cr and growth to 0.1 of a point, giving a band of **−32.98 to −2.63 bps**. The band never crosses zero, so the direction holds; the level does not.
- **Three margin bases appear in §14** and are not forced to agree.
- **The proposal's Reach is an author construct**, set at 10% of quarterly footfall because the size of the indicated-deferral pool is not disclosed. It is declared in ASSUMPTIONS Part 3 and the RICE conclusion is insensitive to it within a wide range.

**Rating: 8.5/10.** It loses a point for the missing conversion trend and half for the construct in the RICE Reach.

---

## 65. Appendix

### A. Source conflicts

| # | Conflict | Handling |
|---|---|---|
| **A-1** | The company's **ARPS of ₹42,900 (FY26)** and the **₹67,414 revenue per surgery** derived here are different quantities — the derived figure is **1.57×** it, a residual of **₹24,514** per surgery covering consultation, diagnostics and retail. | Both reported, **not reconciled**. The derived figure is used only against its own prior-year self. |
| **A-2** | **Three margin bases**: the company's 28.5% on total income; a third-party 30.26% OPM for the subsidiary; 31.63% and 28.83% computed here on revenue from operations. | All four stated with their basis; comparisons made only on like bases. |
| **A-3** | PAT growth reads **44.6%** as reported and **44.79%** computed on the rounded ₹38 Cr base, implying a true base of **₹38.05 Cr**. A spread of **0.19 of a point**. | Reported growth used in prose; both printed in `verify.py`. |
| **A-4** | The NPCB&VI comparison sets **FY25** public volumes against **annualised Q1 FY27** company volumes. | Period mismatch stated at the point of use; the multiple is an order-of-magnitude claim, not a precise one. |
| **A-5** | Coverage attributing **"24% growth in patients served"** and **"high-end cataract at 26% of cataract volume vs 20%"** to the company is **undated** in the sources examined and could belong to any of four quarters. | **Not used anywhere.** Excluded rather than assigned to a period. |
| **A-6** | One outlet reported the subsidiary's standalone financials alongside the group's operating metrics in the same paragraph, without distinguishing them. | Entity separation enforced throughout; CIN cited in §2 for this reason. |
| **A-7** | Q1 FY26 revenue appears as **₹487.42 Cr** (revenue from operations) and **₹501 Cr** (total income) in different sources. | Treated as the two different line items they are; growth computed on operations only. |

### B. Evidence grades

🟢 **High** — company results disclosure, audited subsidiary filings, MCA registry, Rajya Sabha reply.
🟡 **Medium** — figures derived here from disclosed inputs; management commentary; period-mismatched comparisons.
🟠 **Low** — absences ("not evidenced in disclosure examined"), undisclosed metrics, undated third-party coverage.
🔴 **Conflicting** — none unresolved in this case study.

### C. Author-constructed content

Personas (§20), wireframes (§52), the *Agarwal Indicated* mechanism and its metrics (§31, §50, §51), the four RICE initiatives and all their Reach/Impact/Confidence/Effort inputs (§47), the Phase 0 kill criteria and the A/B decision rules (§53, §54). Full inventory in `ASSUMPTIONS.md` Part 3.

### D. Asset status

| Asset | Status |
|---|---|
| README.md | Complete, 65 sections |
| ASSUMPTIONS.md | Complete, Parts 1–5 |
| verify.py | **117 checks, all passing** — delivered, not committed |
| crosscheck.py | Run; deliverables reconciled against the gate — delivered, not committed |
| LinkedIn carousel + caption | Slide content and caption delivered; Gamma build to follow |

---

*Day 76 of 90 · [← Day 75 — Cipla](../Day-75-Cipla) · Day 77 →*
