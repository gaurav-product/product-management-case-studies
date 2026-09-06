# Day 71 — Akums: The Factory Is Theirs, The Prescription Is Not

> Akums reported a clean quarter: revenue up 13.93%, EBITDA up 35.4%, PAT up 55.38%, margin 240 basis points better. Split the business in two and the growth is entirely one-sided. **CDMO — making medicines for other companies' brands — grew 18.57%. Everything Akums sells under its own name shrank 3.98%**, a spread of 22.56 points inside one filing. CDMO is 82.63% of revenue and **93.14% of EBITDA**; the branded, API and trade-generics segments are 17.37% of revenue and **6.86% of profit**, earning at 0.39× their revenue weight. The reflex is to call the branded businesses underperforming. They are not. They are **structurally constrained by the contract that makes the core business work**: Akums owns the factory and the formulation data; its clients own the prescriber. And the moment Akums pushes its own brands hard, it competes with the customers funding 82.63% of its revenue.

---

## 1. Cover

**Product:** Akums — contract development and manufacturing (CDMO), branded formulations, API, trade generics
**Legal entity:** Akums Drugs and Pharmaceuticals Limited · **CIN:** L24239DL2004PLC125888
**Domain:** Healthtech — pharmaceutical contract manufacturing
**Period examined:** Q1 FY27 (quarter ended 30 June 2026), reported 10 August 2026
**Written:** 6 September 2026
**Author:** Gaurav Singh · Day 71 of 90

---

## 2. Repository Metadata

| Field | Value |
|---|---|
| Legal entity | Akums Drugs and Pharmaceuticals Limited |
| CIN | L24239DL2004PLC125888 |
| Incorporated | 19 April 2004, as a public company |
| Registrar | RoC Delhi (then Delhi and Haryana) |
| Commencement of business | 13 May 2004 |
| Registered office | 304, Mohan Place, LSC Saraswati Vihar, Delhi 110034 |
| Corporate office | Plot 131–133, Block C, Mangolpuri Industrial Area Phase 1, Delhi 110083 |
| Listings | NSE **AKUMS** · BSE **544222** · ISIN INE09XN01023 |
| NIC code | **24239 — "Manufacture of other pharmaceutical and botanical products"** |
| Managing Directors | Sanjeev Jain · Sandeep Jain |
| Promoters | Sanjeev Jain, Sandeep Jain, Akums Master Trust |
| Key subsidiaries | Akumentis Healthcare Limited · Pure and Cure Healthcare Private Limited |
| Authorised / paid-up capital | ₹30.00 Cr / ₹28.6129 Cr 🟡 |

**A note that breaks a run.** The previous seven case studies in this series each found an NIC code that did not describe the business — BookMyShow filed as "unclassified," Vodafone Idea as electronic valves, Max Healthcare as software publishing, MedPlus as hospital activities, Poly Medicure as steam and hot water supply. **Akums's code is correct.** 24239 is a pharmaceutical manufacturing classification, and Akums manufactures pharmaceuticals. The eighth data point breaks the streak, and that is worth stating plainly: a pattern reported only when it flatters the observer is not a pattern. The register misclassifies often, not always.

One genuine registry detail does remain: the CIN appears as **U24239DL2004PLC125888** across several aggregators and in the company's own pre-IPO filings, and as **L24239DL2004PLC125888** post-listing. The leading letter changes on listing; both refer to the same entity (Appendix A-2).

---

## 3. Badges

`Day 71/90` · `Healthtech` · `Contract manufacturing (CDMO)` · `Listed (NSE/BSE)` · `Q1 FY27 primary` · `One segment carries 93% of profit` · `107 programmatic checks, all passing` · `Zero fabricated figures`

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

Akums announced the quarter ended 30 June 2026 on 10 August. Consolidated revenue from operations was ₹1,166.63 Cr, up **13.93%**. Operating EBITDA was ₹175 Cr, up 35.4%, at a margin of **15.0%** against 12.6%. PAT was ₹101 Cr, up **55.38%** on the reported comparative, with margin improving from 6.2% to 8.4%. Net cash stood at ₹1,616 Cr — **1.39× a full quarter's revenue**. The stock rose about 7% to ₹746.05, within 1.43% of its 52-week high.

The operating story behind that is real and unusual. Akums reported **high-teens volume growth for a third consecutive quarter against Indian pharmaceutical market volume growth of 2–3%** — roughly **6.8×** the industry midpoint. CDMO EBITDA margin reached **16.91%**, nearly two points above the top of the company's own 14–15% guidance, helped by API prices. Group EBITDA grew **2.54×** as fast as revenue. This is a business with genuine operating leverage and a fortress balance sheet.

But the company reports its segments, and the segments do not agree with each other. **CDMO revenue grew 18.57%. Everything else fell 3.98%** — ₹211.03 Cr down to ₹202.63 Cr. That is a **22.56-point spread** between the contract-manufacturing business and every business where Akums sells under its own name: domestic branded formulations (9.9% of revenue), international branded (3.0%), API (2.7%) and trade generics (1.8%).

The profit split is starker than the revenue split. **CDMO produced ₹163 Cr of the group's ₹175 Cr EBITDA — 93.14%.** By subtraction, everything else produced **₹12 Cr**, a **5.92%** margin against CDMO's **16.91%**. The non-CDMO segments carry 17.37% of revenue and **6.86% of profit**: they earn at **0.39×** their revenue weight, while CDMO earns at **1.13×**.

The easy reading is that the branded businesses are being run badly. This case study argues the opposite — that they are **structurally constrained by the same contract that makes the core business work**. Akums manufactures for a large share of the Indian formulations market, which means it observes demand, formulation performance and volume across an unusual breadth of the industry. What it does not own is the prescriber relationship: the doctor writes a client's brand, not Akums's. And the instant Akums competes seriously for that prescription, it becomes a rival to the customers who fund 82.63% of its revenue.

That is not a failure of execution. It is the defining trade-off of the contract manufacturing model, and it decides what Akums can and cannot do with the one asset nobody else has — its data.

The proposal, *Client Insight*, is built to monetise that asset without triggering the conflict. It is designed, costed, and then ranked last — behind simply doing more of what already works.

---

## 6. Product Overview

Akums is India's largest contract development and manufacturing organisation for pharmaceutical formulations. It develops and manufactures finished dosage forms — tablets, capsules, liquids, injectables, sachets, creams — for other pharmaceutical companies, who market them under their own brands. Alongside that sit four smaller businesses: domestic branded formulations (through Akumentis), international branded formulations, active pharmaceutical ingredients, and trade generics.

The structural feature that defines everything in this analysis is that **Akums's largest business has no consumer and no brand.** Its customer is another pharmaceutical company; its product is manufacturing capability, regulatory compliance and formulation development. The four smaller businesses are the only places where Akums faces a doctor, a chemist or a patient — and they are the four that shrank.

---

## 7. Company Background

Akums was incorporated on 19 April 2004 as a public company and remains founder-controlled: Sanjeev Jain and Sandeep Jain are joint Managing Directors, each holding roughly 17.24%, alongside the Akums Master Trust. The company listed in August 2024, having taken outside investment from Ruby QC Investment Holdings ahead of the IPO.

Its scale is the product of two decades of accumulating manufacturing capacity and client relationships rather than of building brands. It employs over 10,000 people, manufactures across a large plant network with a concentration in Uttarakhand, and counts a substantial share of India's formulation companies among its clients — which is precisely why the segment asymmetry examined here matters.

---

## 8. Product Timeline

| Date | Event |
|---|---|
| 19 Apr 2004 | Incorporated as a public company, RoC Delhi |
| 13 May 2004 | Certificate of commencement of business |
| Feb 2024 | DRHP filed |
| Aug 2024 | IPO; listed on NSE and BSE |
| Q3 FY26 | First of three consecutive quarters of high-teens volume growth |
| Q4 FY26 | CDMO-led growth continues; API remains loss-making |
| 23 Jul 2026 | Oriflame India manufacturing business acquired for ₹56 Cr |
| 10 Aug 2026 | Q1 FY27 results: CDMO +18.57%, everything else −3.98% |
| Guided | Zambia order ₹240 Cr in H2 FY27; European business to commence next year |
| Guided | API monthly EBITDA break-even by end FY27, profitable FY28 |

---

## 9. Vision & Mission

Management's stated position on the quarter was that CDMO performance "showcases healthy demand environment as well as our clients' trust in Akums as the preferred manufacturing partner," with a stated focus on strengthening CDMO leadership, scaling high-value capabilities and operational excellence.

That framing is accurate and, notably, **does not claim the branded businesses as a strategic priority**. Management described domestic and export marketing as muted with initiatives underway to restore growth. The question this case study puts is whether "restore growth" is the right ambition for segments whose ceiling is set by a conflict the company cannot resolve.

---

## 10. Problem Statement

**For Akums:** 93.14% of profit comes from one segment in which the company is a supplier, not a brand. Every route to reducing that concentration runs through businesses that compete, directly or by implication, with the clients who provide it.

**For the client — a pharmaceutical company:** they own the brand and the prescriber relationship but not the plant, the formulation know-how or the aggregate view of what is actually selling across the market. They buy manufacturing and receive no intelligence with it.

**The intersection:** Akums holds market-wide formulation and demand data that its clients would value and cannot assemble themselves, and it holds it as an **operational by-product with no commercial expression**. Meanwhile the segments where Akums tries to capture value directly are the ones going backwards.

---

## 11. Market Research

The Indian pharmaceutical market is growing in value but barely in volume — management put industry volume growth at **2–3%**, against Akums's high-teens. That divergence is the single most important market fact in the quarter: **the CDMO is taking share of manufacturing, not riding a rising tide.**

The structural driver is outsourcing. Indian formulation companies increasingly prefer to buy manufacturing rather than build it, because capacity is capital-intensive, regulatory compliance is onerous, and brand-building is where their own margin lives. That preference is exactly what makes Akums's CDMO business compound — and exactly what makes its own branded ambitions awkward.

---

## 12. Industry Analysis

Contract manufacturing is a scale-and-compliance business. Winning requires breadth of dosage forms, regulatory track record, and the ability to absorb volume without quality failure. Akums's 16.91% CDMO EBITDA margin and third consecutive quarter of high-teens volume growth indicate it is winning on those terms.

The industry's defining tension is one this case study returns to repeatedly: **a CDMO's clients are also its natural competitors in any branded market it enters.** Globally, the large contract manufacturers that endured have almost all stayed out of branded pharmaceuticals for precisely this reason, while those that pursued both have tended to be smaller in one or the other. Akums is running both, at a ratio of roughly five to one, and the smaller side is contracting.

---

## 13. TAM / SAM / SOM

*Framework note: run in restricted form. No primary-sourced Indian CDMO market size was located that is not a vendor estimate, so this is sized from Akums's own disclosed segment revenue, annualised.*

| Layer | Definition | Size | Basis |
|---|---|---|---|
| TAM | Annualised revenue at the Q1 run rate | **₹4,666.52 Cr** | ₹1,166.63 Cr × 4 🟢 |
| SAM | Annualised CDMO revenue | **₹3,856.00 Cr** | ₹964 Cr × 4 🟢 |
| SOM | Annualised non-CDMO revenue | **₹810.52 Cr** | Derived, D9b |
| *The constraint* | Non-CDMO share of group EBITDA | **6.86%** | Derived, D3c |

The last row is the strategic problem as a number. Akums can address ₹810.52 Cr of annualised revenue through businesses it controls end-to-end, and those businesses currently convert it into 6.86% of group profit.

---

## 14. Competitor Analysis

*Framework note: the comparison here is **internal — CDMO against every other segment** — and that is a deliberate choice, not a shortcut. Akums's listed Indian CDMO peers differ materially in mix, with several combining CRO, API and export-regulated businesses in proportions that make a like-for-like margin comparison misleading. But Akums discloses segment revenue **and** segment EBITDA for CDMO alongside group totals, which means every other segment can be isolated by subtraction with no estimation at all. An exact internal comparator beats an approximate external one.*

| Metric, Q1 FY27 | CDMO | Everything else (derived) | Group |
|---|---|---|---|
| Revenue | ₹964.00 Cr | **₹202.63 Cr** | ₹1,166.63 Cr |
| Revenue growth | **+18.57%** | **−3.98%** | +13.93% |
| EBITDA | ₹163.00 Cr | **₹12.00 Cr** | ₹175.00 Cr |
| EBITDA margin | **16.91%** | **5.92%** | 15.00% |
| Share of revenue | 82.63% | 17.37% | 100% |
| Share of EBITDA | **93.14%** | **6.86%** | 100% |
| Profit share ÷ revenue share | **1.13×** | **0.39×** | 1.00× |

Three readings. **The two halves are moving in opposite directions** — a 22.56-point growth spread inside one company, in one quarter, under one management team. That rules out macro explanations: the same market, the same input costs and the same balance sheet produced +18.57% on one side and −3.98% on the other.

Second, the profit asymmetry is larger than the revenue asymmetry. The non-CDMO segments earn at **0.39×** their revenue weight, so every rupee of revenue mix that shifts toward them dilutes group margin. CDMO margin also expanded **227 basis points** year on year, from 14.64% to 16.91%, while the group's non-CDMO half contributed ₹12 Cr in total.

And the number that argues against this case study's framing, included because it should be: **the API segment is disclosed as loss-making and improving**, with management guiding to monthly EBITDA break-even by end FY27. API is 2.7% of revenue. If API alone accounts for most of the drag, then the branded businesses may be closer to healthy than the blended −3.98% and 5.92% figures suggest — and this analysis cannot separate them, because segment-level EBITDA is disclosed for CDMO only (Appendix A-4).

---

## 15. SWOT

| | |
|---|---|
| **Strengths** — high-teens volume growth for three consecutive quarters against industry volume of 2–3%, roughly **6.8×**; CDMO EBITDA margin 16.91%, ~1.91 points above guided top end; group EBITDA growing **2.54×** revenue; net cash ₹1,616 Cr at 1.39× quarterly revenue; market-wide formulation and demand data no competitor can assemble | **Weaknesses** — 93.14% of EBITDA from a single segment; non-CDMO revenue down 3.98% and earning at 0.39× its revenue weight; API loss-making; segment EBITDA disclosed for CDMO only, so the other four cannot be told apart |
| **Opportunities** — Zambia order of ₹240 Cr guided for H2 FY27, **1.18×** a full quarter of non-CDMO revenue; European business commencing next year; Oriflame India acquisition at ₹56 Cr — just **3.47%** of net cash — extending into cosmetics and wellness; API path to break-even | **Threats** — any serious branded push competes with clients funding 82.63% of revenue; CDMO margin flattered by API prices management calls volatile; concentration risk if outsourcing preference or a major client shifts; industry volume growth of 2–3% caps the underlying market |

---

## 16. Porter's Five Forces — run twice

*Framework note: run as a double pass on the two businesses inside one filing — **CDMO**, where Akums sells manufacturing to a pharmaceutical company, and **branded**, where Akums sells medicine to a market through a prescriber. The seam is chosen because the forces do not merely differ across it, they point at the same counterparties in opposite roles: **the CDMO's customer is the branded business's competitor.***

| Force | CDMO (82.63% of revenue) | BRANDED, API, trade generics (17.37%) |
|---|---|---|
| **Buyer power** | Moderate and contractual. Switching a manufacturer means revalidation and regulatory filings — genuinely costly, which is why volumes compound | **High and indirect.** The prescriber decides, and Akums has no relationship with them; the chemist substitutes on availability and margin |
| **Rivalry** | Against other CDMOs on capacity, compliance and breadth of dosage forms — a contest Akums is winning at 6.8× industry volume growth | **Against its own clients.** Every branded rupee Akums wins is a rupee taken from a company that buys manufacturing from it |
| **Substitutes** | A client's own in-house plant — the make-versus-buy decision, and the industry is moving toward buy | Any of thousands of equivalent molecules from firms with established prescriber relationships |
| **New entrants** | Barred by capital, regulatory track record and validated capacity | **Weakly barred.** Launching a branded formulation needs a licence and a field force, not a plant — Akums will manufacture it for you |
| **Supplier power** | API and input costs, currently favourable and explicitly described as volatile | Identical inputs, but with no pricing power downstream to recover them |

The inversion is unusually sharp, and it is not a coincidence of positioning — it is the same relationship read from two ends. **In the left column Akums's customers are the source of its profit. In the right column those same customers are its competitors.** Reporting one revenue line across both averages a business whose growth depends on client trust with a business whose growth erodes it. The 22.56-point growth spread in §14 is what that contradiction looks like when it reaches the accounts, and it is why §50 proposes a product sold *to* the left column rather than one competing *with* it.
---

## 17. Business Model Canvas

| Block | Akums |
|---|---|
| Value proposition | Manufacture another company's medicine to regulatory standard, at scale, across dosage forms |
| Customer segments | Pharmaceutical companies (CDMO); doctors and chemists (branded); institutional buyers (trade generics, exports) |
| Channels | Direct client contracting; field force for branded; tenders and distributors for generics |
| Revenue streams | CDMO 82.6%, domestic branded 9.9%, international branded 3.0%, API 2.7%, trade generics 1.8% |
| Key resources | Validated plant network, dosage-form breadth, regulatory track record, **market-wide formulation and demand data** |
| Key activities | Formulation development, manufacturing, quality assurance, client management |
| Key partners | The client pharmaceutical companies — who are also the competitors of the branded segment |
| Cost structure | Materials and API, plant overhead, quality and compliance, field force for branded |
| **The unpriced asset** | **Aggregate visibility of what the market is actually manufacturing and selling** |

The final row is the whole of §50. Every other block is priced; that one is a by-product.

---

## 18. Revenue Model

Akums earns a manufacturing margin per unit produced for clients, and a brand margin per unit sold under its own name. The two convert very differently: **CDMO at a 16.91% EBITDA margin, everything else at 5.92%** — a **2.86×** gap.

The model's leverage is visible in the quarter. Group EBITDA grew **2.54×** as fast as revenue and CDMO EBITDA **1.98×** as fast as CDMO revenue, because incremental volume flows through plants already built and staffed. That is the correct economic signature of a capacity business, and it is why the CDMO half compounds while the branded half, which needs a field force per rupee of revenue, does not.

One disclosure detail worth carrying: EBITDA including other income grew **31.7%** against operating EBITDA's 35.4%, a **3.70-point** gap — so other income, at **14.63%** of the including-other-income figure, grew more slowly than the operating business. The quarter is operationally driven, not treasury-driven, which is to the company's credit.

---

## 19. Target Users

Akums's paying customer in 82.63% of its revenue is a pharmaceutical company's supply chain and product development function. Their criteria are capacity availability, regulatory reliability, dosage-form breadth and cost per unit.

The user this case study is most interested in is the same client, wearing a different hat: **the product manager at a client company deciding which molecule to launch next.** That person is guessing at market demand from IQVIA-style secondary data and their own field force. Akums can see a fuller picture of what is actually being manufactured across the industry, and sells them none of it.

---

## 20. Personas

**A supply-chain head at a mid-size formulations company.** Buys manufacturing from Akums. Cares about on-time delivery and audit outcomes. Will not switch easily — revalidation is expensive — which is why CDMO volumes compound.

**A product manager at that same client.** Chooses which SKUs to back. Has no market-wide view of formulation demand, only her own sales and purchased secondary data. She is the buyer §50 is designed for, and she does not currently buy anything from Akums.

**Akumentis's field force manager.** Sells Akums's own branded formulations to doctors, calling on prescribers whose loyalty belongs to companies that are Akums's largest customers. Every success creates a conversation the CDMO account manager would rather not have.

---

## 21. Jobs To Be Done

*Framework note: JTBD is used because the same client hires Akums for one job and would hire it for a second — and the second is unpriced.*

| Job | Who | Current solution | Adequacy |
|---|---|---|---|
| "Make my product to spec, on time, compliantly" | Client supply chain | Akums CDMO | **Excellent** — 16.91% margin, high-teens volume growth |
| "Develop a formulation I can launch" | Client R&D | Akums development services | Served, inside CDMO |
| "Tell me what the market is actually absorbing" | Client product management | **Nothing from Akums** | **Not served at all** — the §50 gap |
| "Build a brand doctors prescribe" | Akums (branded segments) | Akumentis, field force | **Structurally capped** — competes with clients |
| "Stop losing money on API" | Akums | Non-cephalosporin mix shift | In progress; break-even guided end FY27 |

Rows three and four are the strategic pair. Row four is the route Akums has been taking to escape single-segment concentration, and it is contracting. Row three is a route to the same objective that **strengthens** the client relationship rather than straining it.

---

## 22. User Journey

| Stage | CDMO client | Branded prescriber |
|---|---|---|
| Awareness | Industry reputation, audit history, referrals | Field force call |
| Evaluation | Plant audit, capability assessment, costing | Sample, clinical rationale, detailing |
| Commitment | Contract, tech transfer, regulatory filing | A single prescription |
| Switching cost | **High** — revalidation and refiling | **Near zero** — write another brand |
| Who owns the relationship | **Akums** | **Not Akums** |

The final row is the case study in one line. In the left column Akums owns the relationship and the switching cost is high. In the right column it owns neither, and it is competing against companies that do.

---

## 23. User Flow

The CDMO flow is: enquiry → capability and capacity check → costing → tech transfer → regulatory filing → validated production → repeat orders. Akums's advantage sits at step two, where breadth of dosage forms means it can say yes more often than competitors.

The branded flow is: field force calls doctor → doctor prescribes → chemist dispenses → repeat. Akums participates only in manufacturing the box. **The two flows share a factory and nothing else**, which is why treating them as one business in a single revenue line obscures rather than clarifies.

---

## 24. Information Architecture

The disclosure architecture is better than most and has one specific gap. Akums publishes segment revenue shares for all five businesses, and segment revenue **and EBITDA** for CDMO — which is what allows the non-CDMO residual to be derived exactly by subtraction.

What it does not publish is **EBITDA for the other four segments individually**. So the derived ₹12 Cr and 5.92% blend a loss-making API business with branded and trade-generics businesses of unknown profitability. That single omission is why §14 cannot separate "API is dragging" from "branded is capped," and it is the reason ASSUMPTIONS A2 exists.

---

## 25. UX Audit

Not a consumer product in its dominant segment; the equivalent is the client experience of working with a CDMO — audit readiness, communication during tech transfer, delivery reliability. None of that is externally assessable, and this section does not pretend otherwise.

The one observation available from disclosure: **client retention is implied by high-teens volume growth across three consecutive quarters at 6.8× industry volume growth.** Clients do not concentrate more volume with a manufacturer they find difficult to work with, so the qualitative experience is likely good even though it cannot be measured here.

---

## 26. UI Audit

Not applicable. Akums has no material consumer interface, and inventing an audit for one would be padding.

The interface that matters commercially is the **client-facing ordering, forecasting and quality-documentation layer** — and that is precisely where §50's product would be delivered, because it is the only surface where Akums already has a paying relationship.

---

## 27. Accessibility

The access contribution here is real and structural rather than programmatic: contract manufacturing at Indian cost lowers the cost of bringing a formulation to market, which lets smaller companies launch products they could not manufacture themselves. Akums's breadth is a reason more molecules reach more markets.

Trade generics, at 1.8% of revenue, is the segment most directly aimed at price-sensitive access. It is also one of the four contracting segments, which is a fair illustration of the tension: the socially useful low-margin business is the one under pressure.

---

## 28. Feature Breakdown

| Area | Current state |
|---|---|
| CDMO | ₹964 Cr, 82.63% of revenue, 16.91% EBITDA margin, +18.57% |
| Domestic branded formulations | 9.9% of revenue; described as muted |
| International branded formulations | 3.0% of revenue; recovery expected |
| API | 2.7% of revenue; **loss-making**, break-even guided end FY27 |
| Trade generics | 1.8% of revenue |
| Recent acquisition | Oriflame India manufacturing, ₹56 Cr, 23 July 2026 — cosmetics, skincare, wellness |
| Export orders | Zambia ₹240 Cr guided for H2 FY27; Europe next year |
| Balance sheet | Net cash ₹1,616 Cr |
| **Client-facing market intelligence** | **Does not exist** |
| **Segment EBITDA beyond CDMO** | **Not disclosed** |

The two absences at the bottom are the subjects of §50 and §47. Both are verifiable from disclosure rather than assumed: no results release, presentation or earnings-call coverage describes an intelligence product sold to clients, or publishes segment EBITDA for any segment other than CDMO.

---

## 29. AI Capabilities

Akums has disclosed no material AI product, and none is proposed here as such.

The relevant observation is that the raw material for the §50 proposal — order patterns, formulation performance, volume trends across a large slice of Indian formulations — is **already generated as a by-product of running the plants**. Turning it into a saleable intelligence product is a data-aggregation and confidentiality-engineering problem well before it is a modelling one, and treating it as an AI initiative would misdescribe both the work and the risk.

---

## 30. Product Metrics

| Metric | Q1 FY27 | Note |
|---|---|---|
| Revenue from operations | ₹1,166.63 Cr | **+13.93%** computed |
| Total income | ₹1,197 Cr | Other income ₹30.37 Cr implied |
| Operating EBITDA | ₹175 Cr | +35.4%, margin 15.00% from 12.6% |
| PAT | ₹101 Cr | **+55.38%** computed; margin 8.66% computed |
| **CDMO revenue** | **₹964 Cr** | **+18.57%**, 82.63% of revenue |
| **CDMO EBITDA** | **₹163 Cr** | **93.14% of group EBITDA**, margin 16.91% |
| **Non-CDMO revenue** | **₹202.63 Cr** | **−3.98%**, 17.37% of revenue |
| **Non-CDMO EBITDA** | **₹12 Cr** | **6.86% of group**, margin 5.92% |
| Volume growth | High teens | vs industry 2–3%, ~**6.8×** |
| Net cash | ₹1,616 Cr | 1.39× quarterly revenue |

**One reported figure does not reconcile and is flagged rather than smoothed.** PAT of ₹101 Cr against a reported prior-year ₹65 Cr computes to **+55.38%**, while the company reports **+56.1%**. The reported growth rate implies a prior-year PAT of **₹64.70 Cr**, so the ₹65 Cr comparative is rounded. The gap is 0.72 points and affects no conclusion; both are stated (Appendix A-3).

---

## 31. North Star Metric

Akums's implied north star is CDMO revenue growth, and on that measure the quarter is excellent. The problem it cannot detect is that 93.14% of profit now depends on one segment, and the diversification attempts are shrinking.

**Proposed North Star — CPI/100: Client-Paid Insight revenue per ₹100 of CDMO revenue.**

Revenue counts in the numerator only if **all four** hold:
1. it is billed separately from manufacturing, under its own contract line;
2. the buyer is an existing CDMO client, purchasing voluntarily and renewably;
3. the insight delivered is derived from aggregated, de-identified data passing the §31 re-identification threshold;
4. no manufacturing commercial term was varied to secure it.

**The denominator is the design choice.** It is *CDMO revenue* — so winning more manufacturing volume without selling more intelligence **lowers** the metric. Akums cannot improve CPI/100 by doing more of the thing it is already good at; the ratio only rises if a genuinely new revenue line grows faster than the core. Condition 4 is what prevents the product being given away as a discount in disguise.

**Guardrail — RIR-90: Re-Identification Risk at the 90th percentile of client concentration.** In the decile of therapeutic categories where Akums's client base is most concentrated — fewest clients, largest individual shares — the modelled probability that an aggregate insight reveals an identifiable client's volumes. Measured per category, never in aggregate, against a published threshold. Owned by a data-governance function with no commercial target, with **automatic suppression** of any category breaching the threshold.

This guardrail is not decoration. A CDMO that leaks one client's volumes to another does not lose a product line; it loses the trust that 82.63% of its revenue rests on. §40 sets out why that risk has to be engineered against before the product exists.

---

## 32. Product Analytics

Akums already holds, per client and per SKU, what was ordered, in what volume, at what frequency, in which dosage form and how that changed over time. Across a large share of Indian formulations manufacturing, that is a view of market demand that no single client — and arguably no data vendor — can reconstruct.

The analytics gap is not collection but **governance**: deciding what can be aggregated, at what granularity, without any client's position becoming inferable. That is the entire technical content of §50, and it is why RIR-90 precedes the product rather than reporting on it.

---

## 33. AARRR

*Framework note: applied to the CDMO client relationship, because that is where the compounding happens.*

| Stage | Reading |
|---|---|
| Acquisition | Working — volume growth at ~6.8× industry, implying share gain |
| Activation | Working — tech transfer and validation convert enquiries into recurring production |
| Retention | **Structurally strong** — revalidation cost makes switching expensive |
| Revenue | **₹964 Cr, 82.63% of the group, at 16.91% margin — and expanding 227 bps** |
| Referral | Industry reputation and audit history; not separately disclosed |

Every stage is healthy, which is the point. **The CDMO funnel is not the problem; the problem is that it is the only funnel that works**, and the diversification funnel running beside it produced −3.98%. A company with one excellent funnel and one failing one has a concentration question, not an execution question.

---

## 34. HEART

| Dimension | Akums |
|---|---|
| Happiness | Not disclosed; no client satisfaction metric published |
| Engagement | Volume growth in high teens across three consecutive quarters — the closest available proxy |
| Adoption | Oriflame acquisition extends into cosmetics and wellness; no adoption data yet |
| Retention | Not disclosed at client level, but implied by compounding volume |
| Task success | **Not defined** — no published on-time-in-full, audit-outcome or batch-rejection data |

The last row is the meaningful absence. For a contract manufacturer, task success is delivery reliability and quality outcomes, and those are the metrics a client actually buys on. None is published.

---

## 35. Growth Strategy

The stated strategy is CDMO leadership plus selective expansion: high-teens volume growth guided to continue, CDMO EBITDA margin guided at 14–15%, the Zambia order contributing ₹240 Cr in H2 FY27, European business commencing next year, API to break even by end FY27, and the ₹56 Cr Oriflame acquisition extending manufacturing into cosmetics and wellness.

Notice what that list is: **almost all of it is more contract manufacturing, in more categories and more geographies.** The Oriflame acquisition is manufacturing for a brand owner. The Zambia order is supply. Even the diversification is CDMO-shaped — which suggests management has already, implicitly, drawn the conclusion this case study argues for explicitly.

**Checking whether the proposal already exists, from the company's own disclosures.** Nothing in the Q1 FY27 results, investor presentation or earnings-call coverage describes a market-intelligence or data product sold to clients, a separately-contracted advisory line, or any revenue stream other than manufacturing, branded sales, API and trade generics. The §50 instrument does not exist today.

---

## 36. Growth Loops

The core loop works and is worth stating precisely: **capacity and dosage-form breadth → ability to accept more client work → volume → operating leverage → margin → capacity investment.** The evidence is a 227 basis point CDMO margin expansion on 18.57% revenue growth, with EBITDA growing 1.98× as fast as revenue.

There is a second loop that runs the other way, and it is why the branded segments cannot simply be scaled. **Branded push → competes with clients → client trust erodes → CDMO volume at risk → branded push must be restrained.** The loop is self-limiting by design, and no amount of field-force investment escapes it. Any diversification that survives has to be **orthogonal to the client relationship rather than opposed to it** — which is the single design constraint on §50.

---

## 37. Network Effects

Manufacturing has no classical network effects. What Akums has instead is a **data effect**: each additional client makes the aggregate view of the market more complete, which would make an intelligence product more valuable to every other client. That is a genuine increasing-returns dynamic and it is currently entirely uncaptured.

The same effect carries the risk. The more concentrated Akums's share of a therapeutic category, the more valuable the aggregate view — and the easier it becomes to infer an individual client's position from it. **The data effect and the confidentiality risk grow together**, which is why RIR-90 measures at the 90th percentile of client concentration rather than on average.
---

## 38. Product Strategy

Akums's strategy is correct on the core and unresolved on the periphery. The CDMO business is winning at 6.8× industry volume growth with expanding margin and structurally high switching costs; the right answer there is to keep doing it, and management's guidance says so.

The unresolved part is what diversification means for a company whose customers are its natural competitors. **Four segments totalling 17.37% of revenue produced 6.86% of profit and shrank 3.98%**, and three of them — domestic branded, international branded, trade generics — sit on the wrong side of §36's self-limiting loop. The strategic question is not how to run them better. It is whether diversification should be pursued **through the client relationship rather than around it.**

---

## 39. Monetization

Akums monetises capacity. A client pays per unit manufactured, and the margin is the spread between conversion cost and contract price — 16.91% at EBITDA level, expanding because volume flows through fixed plants.

The monetisation gap is that **everything Akums learns while doing this is free to the client and invisible to everyone else.** A client buying manufacturing receives a delivery and an invoice. It does not receive any view of what the wider market is absorbing, even though Akums necessarily forms one. That by-product has no price, no contract line and no owner — which is the definition of an unmonetised asset.

---

## 40. Trust & Safety

*Placed before §50 deliberately, because the proposal turns client-confidential information into a product, and that is a trust question before it is a revenue question.*

**Client confidentiality is the asset the whole company rests on.** A pharmaceutical company hands a CDMO its formulation, its launch timing and its volumes. If any of that becomes inferable by a competitor, the damage is not a lost product line — it is the 82.63% of revenue that depends on being a trusted manufacturing partner. The mechanic: **RIR-90 measures modelled re-identification probability per therapeutic category at the 90th percentile of client concentration, against a published threshold, with automatic suppression of any category that breaches it.** Suppression is the default state, not an escalation.

**Concentration makes aggregation unsafe in exactly the categories where it is most valuable.** In a category with forty clients, an aggregate is genuinely anonymous. In one with three, an "aggregate" is arithmetic away from a disclosure. The mechanic: minimum-client thresholds per category, plus suppression of any cell where a single client exceeds a published share of the aggregate — both set by data governance, not by the commercial team, and not overridable by them.

**Consent must be explicit and revocable, not buried in a manufacturing contract.** The mechanic: participation is a separate, opt-in agreement with its own termination right; a client that declines suffers no change to manufacturing terms, price or priority. §48 places any linkage between insight participation and manufacturing commercials permanently out of scope.

**The incentive that must be excluded, stated plainly.** If CPI/100 is targeted without RIR-90 gating it, the fastest way to raise the metric is to publish richer, more granular insight — which is precisely the direction that leaks client positions. §53 therefore makes the RIR-90 threshold a precondition of launch per category, and §48 forbids commercial ownership of the suppression rules.

**A regulatory note.** Formulation and volume data may carry obligations under client contracts and, where personal or patient-linked data is involved, under India's DPDP framework. This case study assumes none of the proposed aggregates touch patient data, and §51 makes that a hard requirement rather than an assumption.

---

## 41. Technical Architecture

The relevant systems are the ERP and manufacturing execution layer that records orders, batches, dosage forms and volumes by client, and the quality management system that records outcomes. Both already exist; the proposal adds no manufacturing infrastructure.

What it does require is a **governed aggregation layer** sitting between the operational systems and any client-facing output: client-identifying fields stripped at ingestion, category-level minimum thresholds enforced in the pipeline, and suppression applied before a human sees the result. Enforcement in the pipeline rather than by policy is the difference between a control and an intention.

---

## 42. Data Flow

Today: client order → production planning → manufacture → delivery → invoice. The demand signal is consumed operationally and discarded commercially.

Under the proposal: the same operational flow, plus a one-way branch — order and volume records → de-identification → category aggregation → RIR-90 suppression check → published insight → separate invoice. The critical constraint is directional and absolute: **no client-identifiable record may flow into any client-facing output, and no commercial owner may hold write access to the suppression rules.** Enforced by access control and build-pipeline test, on the same pattern used for the measurement firewalls in earlier case studies in this series.

---

## 43. API Ecosystem

The live interface with clients is contractual and operational — forecasting, ordering, quality documentation, delivery scheduling. That surface is where the §50 product would be delivered, because it is the only place Akums already has an authenticated, paying relationship with the buyer.

The asymmetry worth naming: Akums has a rich **inbound** data relationship with every client and almost no **outbound** one. Information flows from the client into Akums's systems as a condition of manufacturing, and nothing of analytical value flows back. The proposal is, in essence, an argument for making that relationship two-way and charging for the return leg.

---

## 44. Privacy & Security

The sensitive data here is commercial rather than personal: client formulations, launch plans and volumes. The governing instruments are the manufacturing contracts themselves, most of which will contain confidentiality provisions that predate any thought of an insight product.

The design position is therefore conservative: **participation requires a fresh, explicit, separately-terminable agreement**, and the default for any client that has not signed one is exclusion from the aggregate entirely — not inclusion with anonymisation. Anonymised inclusion without consent is the shortcut that would make the product larger and the trust risk unmanageable.

---

## 45. Pain Points

| # | Pain point | Evidence |
|---|---|---|
| P1 | 93.14% of EBITDA from a single segment | Derived, D3b 🟢 |
| P2 | Non-CDMO revenue fell 3.98% while CDMO grew 18.57% | Derived, D2c, D2e 🟢 |
| P3 | Non-CDMO segments earn at 0.39× their revenue weight | Derived, D3g 🟢 |
| P4 | Branded growth structurally competes with CDMO clients | §16, §36 — analytical, not disclosed 🟡 |
| P5 | API loss-making at 2.7% of revenue | Earnings call 🟡 |
| P6 | Segment EBITDA disclosed for CDMO only | Absence across all Q1 FY27 disclosures 🔴 |
| P7 | Market-wide formulation data commercially unused | Absence across all disclosures 🟢 |
| P8 | CDMO margin flattered by API prices management calls volatile | Earnings call 🟡 |
| P9 | Reported PAT growth of 56.1% vs 55.38% computed | Derived, D1b–D1d 🟡 |
| P10 | Industry volume growth of 2–3% caps the underlying market | Earnings call 🟡 |

---

## 46. Opportunity Mapping

| Opportunity | Annualised revenue addressed | Requires |
|---|---|---|
| CDMO capacity and client depth | ₹3,856.00 Cr | Nobody outside; capacity already being added |
| API turnaround to break-even | ₹126.00 Cr | Nobody outside; mix shift already underway |
| Branded formulations revival | ₹810.52 Cr | Prescribers to switch — and clients to tolerate it |
| Client Insight | ₹3,856.00 Cr | Clients to buy, and to consent to aggregation |
| Segment EBITDA disclosure | Not revenue-generating | Nobody outside |

The right-hand column decides §47 again, and it decides it emphatically: the two initiatives requiring nobody's agreement are the two that survive the stress test, and one of them addresses the largest revenue pool on the page.

---

## 47. RICE

*Framework note: run with a sensitivity pass. Initiatives requiring a client, prescriber or consumer to change behaviour are multiplied by a stress rule; those delivering value inside operations Akums already controls are exempt.*

**The stress rule comes from the company's own segment disclosure.** Everything Akums does outside contract manufacturing — branded formulations at home and abroad, API, trade generics — produced **6.86% of group EBITDA**. That is Akums's own demonstrated ability to convert effort into profit outside the contract model, and it is the right discount for any initiative that depends on someone beyond the existing client contract acting. Two alternatives were computed and not used: the non-CDMO **revenue** share of 17.37% would have been far more generous, and non-CDMO revenue growth is **negative** and therefore unusable as a multiplier.

| Initiative | Reach (₹ Cr p.a.) | Impact | Conf. | Effort | **Base** | **Stressed** |
|---|---|---|---|---|---|---|
| CDMO capacity and client depth | 3,856.00 | 1.00 | 0.85 | 24 | **136.57** | **136.57** (exempt) |
| Branded formulations revival | 810.52 | 2.00 | 0.50 | 26 | **31.17** | **2.14** |
| **Client Insight (PROPOSED)** | **3,856.00** | **0.75** | **0.35** | **36** | **28.12** | **1.93** |
| API turnaround to break-even | 126.00 | 3.00 | 0.70 | 18 | **14.70** | **14.70** (exempt) |

**Client Insight falls from 3rd of 4 at baseline to 4th and last under stress**, behind an initiative this case study did not propose. The winner beats it by **70.83×**. `verify.py` asserts programmatically both that the proposal finishes last and that it is the **weakest stressed initiative at baseline** — the only configuration in which the demotion is genuine rather than arranged.

The answer is unglamorous and correct. **Akums should keep building CDMO capacity and finish the API turnaround before it builds anything clever.** Both act inside operations it already controls; both are already underway; and the CDMO opportunity is 30.6× the size of the API one and needs no client to buy anything new. A company growing volume at 6.8× its industry, with ₹1,616 Cr of net cash and a margin expanding 227 basis points, does not have a diversification emergency. It has a concentration risk it can afford to address slowly.

---

## 48. MoSCoW

| | |
|---|---|
| **Must** | Segment EBITDA disclosed for all five segments, not CDMO alone; RIR-90 thresholds published and owned by data governance; opt-in consent separately contracted and terminable; client-identifying fields stripped at ingestion |
| **Should** | Category-level aggregation with minimum-client thresholds; separate contract line and invoice for any insight product; suppression enforced in the pipeline, not by review |
| **Could** | Extension of insight to launch-timing and dosage-form trend analysis; benchmarking service for clients against anonymised peers |
| **Won't** | Any link between insight participation and manufacturing price, priority or terms; any commercial ownership of suppression rules; inclusion of non-consenting clients in aggregates on anonymisation grounds; any use of patient-linked data |

The "Won't" row closes the four routes by which a data product becomes the confidentiality failure §40 describes — and the first entry is the one that matters most, because bundling insight into manufacturing terms is both the easiest sale and the fastest way to make consent meaningless.

---

## 49. Kano

| Feature | Category | Note |
|---|---|---|
| On-time, compliant manufacturing | Basic | Absence ends the client relationship immediately |
| Dosage-form breadth | Performance | The reason Akums can say yes more often — a genuine competitive asset |
| Lower cost per unit | Performance | Real, but the least defensible axis over time |
| **Akums-branded competing product** | **Reverse** | For a CDMO client, this is a negative feature of their supplier |
| **Market intelligence sold back to the client** | **Attractive** | Nobody offers it; it strengthens the relationship rather than straining it |

Rows four and five are the same company's two diversification options, classified oppositely by the same customer. That contrast is the clearest statement of why §50 takes the shape it does.

---

## 50. Feature Proposal — *Client Insight*

**What it is.** A separately-contracted, separately-invoiced market intelligence service sold to existing CDMO clients. Akums aggregates order, volume, dosage-form and formulation-performance data across consenting clients, de-identifies it at ingestion, aggregates to therapeutic category, applies a published re-identification threshold, and sells the resulting view of market demand back to the clients who generated it. Participation is opt-in, separately terminable, and has no effect on manufacturing terms.

**Why this shape.** §16 and §36 establish that every branded route to diversification puts Akums into competition with the clients funding 82.63% of its revenue, and that the loop is self-limiting by design. **Client Insight is the only diversification available that runs *with* the client relationship instead of against it** — the buyer is the existing customer, the product is a by-product Akums already generates, and a client who buys it becomes more embedded, not less. It converts §37's data effect from an uncaptured externality into a revenue line.

**What it is not.** It is not a resale of any individual client's data. It is not bundled into manufacturing pricing. It is not a substitute for the CDMO investment §47 ranks first. And it is not launched in any therapeutic category that fails RIR-90.

**North Star:** CPI/100, per §31, with CDMO revenue as the denominator.
**Guardrail:** RIR-90, per §31, by therapeutic category, owned by data governance.

---

## 51. PRD

**Problem.** 93.14% of Akums's EBITDA comes from one segment. The diversification attempts to date are branded businesses that compete with the clients funding that segment, and they shrank 3.98% while CDMO grew 18.57%. Meanwhile the company's most distinctive asset — a market-wide view of formulation demand — has no commercial expression.

**Goals.** Establish a revenue line that is independent of manufacturing volume but native to the client relationship; make Akums's data asset commercially visible; and reduce single-segment profit concentration without increasing client conflict.

**Non-goals.** Competing with clients. Replacing CDMO investment. Increasing manufacturing prices. Building any product requiring patient-level data.

**User stories.**
- As a client product manager, I can see what my therapeutic category is actually absorbing, at a granularity no vendor can offer, and I pay for it separately.
- As a client's legal team, I can read exactly what is aggregated, opt out at any time, and confirm my manufacturing terms are unaffected.
- As Akums's board, I can see a revenue line that grows without adding a plant and without adding a competitor.

**Functional requirements.** De-identification at ingestion; therapeutic-category aggregation with minimum-client thresholds; RIR-90 computation per category against a published threshold with automatic suppression; opt-in consent register with independent termination; separate contracting and invoicing; per-segment EBITDA reporting so the new line's economics are visible.

**Non-functional.** Suppression rules held by data governance with commercial teams having read-only access, enforced by build-pipeline test; no patient-linked data in any pipeline; audit trail sufficient for a client to verify their own exclusion.

**Acceptance criteria.** Revenue counts toward CPI/100 only if all four §31 conditions hold. No category launches before its RIR-90 threshold is established and met.

**Success metrics.** CPI/100 at the R1 threshold in §54; RIR-90 within threshold in every category measured separately; zero instances of a client withdrawing consent citing confidentiality.

---

## 52. Wireframes

```
SEGMENT EBITDA DISCLOSURE   (the gap that forces every derivation in this study)
+--------------------------------------------------------------+
|  Segment                  Revenue     EBITDA    Margin        |
|  ----------------------------------------------------------  |
|  CDMO                     964.00      163.00    16.91%   <-- disclosed
|  Everything else          202.63       12.00     5.92%   <-- DERIVED
|  ----------------------------------------------------------  |
|    Domestic branded       115.50         ?          ?         |
|    International branded   35.00         ?          ?         |
|    API                     31.50         ?          ?    (loss-making)
|    Trade generics          21.00         ?          ?         |
|         ^ revenue derived from disclosed mix; EBITDA unknown  |
+--------------------------------------------------------------+

CLIENT INSIGHT - CONSENT   (separate contract, no effect on manufacturing)
+--------------------------------------------------------------+
|  Participate in aggregated category insight?    [ Opt in ]    |
|  ----------------------------------------------------------  |
|  What is aggregated: volumes and dosage forms by therapeutic  |
|    category, de-identified at ingestion.                      |
|  What is never shared: your formulations, launch timing, or   |
|    any figure attributable to you.                            |
|  ----------------------------------------------------------  |
|  Your manufacturing price, priority and terms are UNCHANGED   |
|  whether you opt in or out. Terminable at any time.           |
+--------------------------------------------------------------+

GOVERNANCE DASHBOARD - CPI/100 AND THE GUARDRAIL
+--------------------------------------------------------------+
|  CDMO revenue (denominator) ...................  Rs 964.00 Cr |
|  Insight revenue, separately contracted .......  Rs   X.XX Cr |
|  ...from consenting existing clients ..........  Rs   X.XX Cr |
|  ...with no manufacturing term varied .........  Rs   X.XX Cr |
|  ----------------------------------------------------------  |
|  CPI/100 ......................................        X.XX   |
|  ----------------------------------------------------------  |
|  RIR-90, worst category .......................       X.XX%   |
|  Categories currently SUPPRESSED ..............           N   |
|        ^ suppression is the default, not an escalation        |
+--------------------------------------------------------------+
```

---

## 53. Rollout Plan

**Phase 0 — three analyst-weeks on data Akums already holds, designed to kill the proposal cheaply.**

Compute client concentration and modelled re-identification risk across every therapeutic category in the existing order book, before approaching a single client.

- **K1.** Client concentration is too high in most categories. If the majority of categories fail RIR-90 at any commercially useful granularity, the addressable product is a fraction of what it appears and the economics collapse.
- **K2 — named as the most likely to fire.** Existing manufacturing contracts prohibit any use of order data beyond fulfilment, with no practical route to renegotiation. If confidentiality clauses are absolute — which is exactly what a well-advised client would have insisted on — the product cannot be built from historical data at all, and the consent register only ever covers new business.
- **K3.** Clients will not pay. If product managers at client companies already buy adequate secondary market data, Akums's view is interesting but not incrementally valuable, and the willingness to pay is nil.

**Phase 1 (Q3 FY27).** RIR-90 baselined across all categories; segment EBITDA reporting built internally. No client approached. **Phase 2 (Q4 FY27).** Consent register live; pilot in the two or three highest-fragmentation categories with a small client set. **Phase 3 (FY28).** Expansion only under §54's rule.

**Running in parallel and contingent on nothing above:** the CDMO capacity work and the API turnaround that §47 ranks first and second. Both are already underway and neither depends on this proposal.

---

## 54. A/B Testing

*Framework note: a randomised split is not available for a small enterprise client base, so this is a matched-cohort comparison and is described as such rather than dressed up as an experiment.*

| Arm | Design |
|---|---|
| A — control | Existing clients, manufacturing relationship unchanged |
| B — falsification arm | **The same insight, given away free** as a relationship benefit to a matched cohort — no contract line, no invoice, no separate consent beyond aggregation |
| C — treatment | Client Insight as specified: separately contracted, separately paid, consent-gated |

**Arm B is built to kill the thesis.** It tests whether the value here is a *revenue line* or merely a *retention tool*. If free insight produces the same volume retention and share-of-wallet gains as paid insight, then Akums should give it away, book the benefit inside CDMO, and skip the contracting, invoicing and consent machinery entirely — which is cheaper, faster and carries materially less confidentiality exposure because nothing is sold.

**Pre-registered decision rule (R1).** Arm C proceeds to Phase 3 only if it generates **CPI/100 above 0.50** across two consecutive quarters, **and** RIR-90 stays within threshold in every category measured separately, **and** Arm C clients show CDMO volume retention no worse than Arm B — because a paid product that strains the relationship it was designed to strengthen has failed on its own terms. Failing any of the three, the programme reverts to Arm B or stops.
---

## 55. KPI Dashboard

| KPI | Baseline (Q1 FY27) | Target | Early warning |
|---|---|---|---|
| **CDMO share of group EBITDA** | **93.14%** | Falling | **Rising above 95% means diversification is going backwards, whatever revenue does** |
| Non-CDMO revenue growth | −3.98% | Positive | A second consecutive quarter of decline |
| Non-CDMO EBITDA margin | 5.92% | Toward 10% | Falls below 5% |
| Segment EBITDA published | CDMO only | All five segments | Not published by Q4 FY27 |
| CPI/100 | 0 (not built) | R1 threshold, §54 | Below 0.50 at two quarters |
| RIR-90, worst category | Not measured | Within published threshold | Any category breaching |
| CDMO volume growth vs industry | ~6.8× | Sustained | Falls below 3× |

The first row is the discipline, and it is computable by anyone from two disclosed figures. Akums publishes CDMO EBITDA and group EBITDA every quarter; **dividing one by the other is the whole of this case study's central finding**, and it takes ten seconds.

---

## 56. Product Roadmap

| Period | Focus |
|---|---|
| Q2 FY27 | Segment EBITDA reporting built internally; Phase 0 concentration and RIR-90 analysis |
| Q3 FY27 | RIR-90 baselined; API mix shift continues toward break-even; CDMO capacity additions |
| Q4 FY27 | Consent register live; Client Insight pilot in highest-fragmentation categories; API monthly break-even target |
| FY28 H1 | §54 decision rule evaluated; Insight scaled, given away, or stopped |
| FY28 H2 | Europe commencement; Oriflame integration; CDMO capacity expansion continues |

The proposed product sits third deliberately, behind capacity and API, because that is where §47 put it — and both of those are already company priorities rather than this author's suggestions.

---

## 57. Risks & Mitigation

| Risk | Mitigation |
|---|---|
| Client confidentiality breach via aggregation | RIR-90 per category with automatic suppression; minimum-client thresholds; rules owned outside commercial |
| Insight becomes a bundled discount | Separate contract and invoice; §48 forbids any link to manufacturing terms; condition 4 of CPI/100 |
| Existing contracts prohibit the use of order data | K2 in Phase 0, named as most likely to fire; tested before any client conversation |
| Branded segments keep shrinking | Tracked in §55; the case study argues this may be structural rather than fixable |
| CDMO margin normalises as API prices fall | Margin is 1.91 points above guided top end; management calls API prices volatile — treat 16.91% as a peak, not a run rate |
| Single-segment concentration deepens | First row of §55; measured directly rather than inferred |
| Oriflame integration dilutes margin | Small at ₹56 Cr, 3.47% of net cash; monitor against the Day 70 pattern of acquisitions importing cost bases |

---

## 58. Future Vision

The plausible good outcome is a company that stops trying to be a branded pharmaceutical business and becomes the definitive manufacturing and intelligence layer under the Indian formulations industry — compounding CDMO volume, publishing segment economics so investors can see where profit actually comes from, and earning a second revenue line from the data its plants generate. That is a smaller ambition than "diversified pharma company" and a considerably more defensible one.

The bad outcome is not distress. With ₹1,616 Cr of net cash, expanding margin and volume growth at 6.8× the industry, this is a strong business. The bad outcome is spending the next five years pushing branded formulations into a self-limiting loop, reporting the effort as diversification, and arriving in 2031 with 95% of profit still coming from one segment and a client base that has grown warier.

---

## 59. PM Lessons

1. **When one segment carries 93% of profit, the company has two businesses and one of them is a rounding error.** Dividing CDMO EBITDA by group EBITDA is a ten-second calculation that reframes the entire quarter.
2. **Compare the growth rates of the halves, not the average.** +18.57% and −3.98% average to +13.93%, and the average conceals the only thing worth knowing.
3. **Ask who the customer is in each segment — and whether they are the same people.** At Akums the CDMO's customer is the branded segment's competitor. That single relationship explains the growth spread better than any operational analysis.
4. **A self-limiting loop is not an execution problem.** Branded growth erodes client trust, which threatens 82.63% of revenue, which forces restraint. No amount of field-force investment escapes a loop like that; only a different shape of product does.
5. **Look for the unpriced by-product.** Akums generates a market-wide demand view as exhaust from running plants. Assets with no contract line, no price and no owner are where second revenue lines hide.
6. **Design the guardrail before the product when the asset is trust.** A CDMO that leaks a client's volumes loses more than a product. RIR-90 exists before Client Insight does, and gates it per category.
7. **Include the number that argues against you.** API is loss-making at 2.7% of revenue and could account for much of the non-CDMO drag — and segment EBITDA is not disclosed, so this analysis cannot separate "API is bad" from "branded is capped."
8. **Report the pattern when it breaks.** Seven consecutive case studies found misclassified NIC codes. Akums's is correct. Saying so is what makes the previous seven worth anything.

---

## 60. PM Interview Questions

1. Revenue grew 13.93%. One segment grew 18.57% and the rest fell 3.98%. Which number do you put in the headline, and what do you owe the reader alongside it?
2. 93% of profit comes from one segment. Is that a risk or a strategy? What evidence would move you?
3. Your largest customers are the direct competitors of the business you want to grow. Design the diversification that survives that.
4. A company discloses segment EBITDA for its biggest segment only. What can you derive, what can you not, and how would you say so honestly?
5. You want to monetise data your customers gave you for a different purpose. Name the harm and the mechanic — not the principle — that prevents it.
6. Your sensitivity analysis ranks your proposal last, behind two things the company is already doing. Do you still build it?
7. Management guides CDMO margin at 14–15% and delivered 16.91% on favourable input prices. How do you treat that in a model, and what do you tell the board?

---

## 61. References

**Primary**
1. Akums Drugs and Pharmaceuticals Limited, Q1 FY27 consolidated results, announced 10 August 2026 — revenue, EBITDA, PAT, segment revenue and CDMO segment EBITDA.
2. Akums Drugs and Pharmaceuticals Limited, Q1 FY27 investor presentation, 10 August 2026 — total income, EBITDA including other income, revenue mix by segment, Oriflame acquisition.
3. Akums Drugs and Pharmaceuticals Limited, Q1 FY27 earnings call — volume growth, industry volume context, CDMO margin guidance, API break-even timeline, Zambia order, European commencement.
4. Akums Drugs and Pharmaceuticals Limited, Red Herring Prospectus, 2024 — incorporation date, registered and corporate office, promoters, CIN.
5. Ministry of Corporate Affairs registry — CIN L24239DL2004PLC125888.

**Secondary** (corroboration; flagged where single-sourced)
6. ANI / VMPL press release, 10 August 2026 — headline revenue, EBITDA, PAT and CDMO segment figures.
7. Quartr — Q1 FY27 summary: consolidated revenue in ₹ million, segment commentary, guidance detail.
8. Investing.com — Q1 FY27 slides summary, market reaction, acquisition detail.
9. Yahoo Finance / GuruFocus — Q1 FY27 earnings call highlights, volume growth and API commentary.
10. InvestyWise — investor presentation summary, revenue mix percentages, total income and EBITDA including other income.
11. TradingView — Q1 FY27 slides summary and risk commentary.
12. Tracxn, IndiaFilings, Wikipedia, SimplyWall.st — entity, NIC classification, capital, board and shareholding records (Appendix A-2, A-6).

---

## 62. About the Author

Gaurav Singh — Product Manager. Day 71 of a 90-day public case-study series applying structured PM frameworks to real products, under a zero-fabrication standard: every figure is cited, labelled as an estimate, flagged as single-sourced, or recorded as not publicly disclosed.

---

## 63. License

Analysis and original text © 2026 Gaurav Singh, released for non-commercial use with attribution. All company figures belong to their sources and are cited in §61. No affiliation with Akums Drugs and Pharmaceuticals Limited.

---

## 64. Self Review

**What is strong.** The central finding rests on two disclosed figures divided by one another — CDMO EBITDA over group EBITDA — and the non-CDMO residual is obtained by exact subtraction with no estimation. The growth-spread finding is similarly clean: both segment revenue figures and both prior-year comparatives are disclosed. The §16 seam is unusually well-founded because the two columns share counterparties in opposite roles, which is a structural fact rather than an analytical framing. And the proposal loses to two initiatives the company is already pursuing, asserted programmatically.

**What is weak, stated plainly.** Segment EBITDA is disclosed **for CDMO only**. The derived ₹12 Cr and 5.92% therefore blend four different businesses, one of which — API — is separately disclosed as loss-making. **It is entirely possible that API accounts for most of the drag and that domestic branded formulations are performing acceptably.** This case study cannot distinguish those, and where it says "the branded segments are capped," that is an argument from structure (§16, §36), not a measurement. A reader who believes API alone explains the residual would be making a reasonable case that this analysis cannot refute.

**A second weakness.** The claim that branded growth is structurally constrained by client conflict is **not disclosed anywhere by the company.** Management said the branded segments were muted with initiatives underway to restore growth — which is the opposite framing. The conflict argument is inference from the business model, supported by the growth spread, and it is labelled as inference throughout.

**What I could not establish.** EBITDA for domestic branded, international branded, API or trade generics individually; client concentration by therapeutic category; whether existing manufacturing contracts permit any secondary use of order data — the question K2 exists to answer and on which the entire proposal turns; the number of CDMO clients; on-time-in-full or audit-outcome data; and how much of the 227 basis point CDMO margin expansion is API pricing rather than operating leverage.

**One thing I would do differently.** I opened on the profit-concentration figure, but the sharper entry point is the growth spread — **+18.57% against −3.98% in the same quarter, same management, same market**. That comparison rules out every macro explanation in a single line, and it should have led.

---

## 65. Appendix

### A. Source conflicts

| # | Conflict | Handling |
|---|---|---|
| A-1 | **NIC code 24239 is correct** — a pharmaceutical manufacturing classification for a pharmaceutical manufacturer, ending a seven-case-study run of misclassifications | Stated in §2 explicitly. Reporting the break is the only thing that makes the earlier observations credible |
| A-2 | CIN appears as **U24239DL2004PLC125888** in pre-IPO filings and several aggregators, and **L24239DL2004PLC125888** post-listing | Both stated in §2. The leading letter changes on listing; the same entity. Post-listing form used throughout |
| A-3 | **Reported PAT growth of 56.1% vs 55.38% computed** from the reported ₹101 Cr and ₹65 Cr. The reported rate implies a prior-year PAT of ₹64.70 Cr | Both stated in §30. The ₹65 Cr comparative is evidently rounded; the 0.72-point gap affects no conclusion |
| A-4 | **Segment EBITDA is disclosed for CDMO only.** The non-CDMO EBITDA of ₹12 Cr and its 5.92% margin are derived by subtraction and blend four businesses | 🔴 The single largest limitation. Stated in §14, §24, §64 and ASSUMPTIONS A2. The subtraction is exact; the interpretation is not |
| A-5 | "High teens" volume growth is a **verbal range, not a number.** This analysis reads it as 17% for the industry-multiple calculation | 🟡 Flagged wherever used. The 6.8× multiple would be 6.4× at 16% and 7.2× at 18%; the conclusion is unaffected across the range |
| A-6 | Wikipedia lists **FY24 revenue of ₹1,538.75 Cr**, which is inconsistent with a Q1 FY27 quarterly revenue of ₹1,166.63 Cr on any continuous basis | 🔴 **Not used.** Almost certainly a different reporting basis or entity scope. No FY24 comparison appears in this case study |
| A-7 | Figures appear in both **₹ million and ₹ crore** across sources (₹11,666.29 mn = ₹1,166.63 Cr) | ₹ crore used throughout; conversions checked and asserted in `verify.py` |
| A-8 | Computed EBITDA margin of **15.00%** and PAT margin of **8.66%** against reported 15.0% and 8.4% | Both stated. The PAT margin gap follows from the rounded comparative in A-3; computed values used in derivations |

### B. Evidence grades

🟢 **High** — Q1 FY27 revenue, EBITDA, PAT, CDMO segment revenue and EBITDA, disclosed revenue mix, net cash, MCA registry, RHP.
🟡 **Medium** — earnings-call commentary (volume growth, industry context, API status, guidance), "high teens" as a numeric range, capital snapshots.
🟠 **Low** — none relied upon.
🔴 **Conflicting** — A-4 (segment EBITDA disclosed for CDMO only) and A-6 (inconsistent FY24 revenue, excluded).

### C. Author-constructed content

*Client Insight*, CPI/100, RIR-90, the RICE inputs, the CDMO-versus-branded seam in §16, the self-limiting loop in §36, the Phase 0 kill criteria and the §54 matched-cohort arms are the author's constructions, not Akums disclosures or plans. **The claim that branded growth is structurally constrained by client conflict is an inference from the business model, not a company statement** — management's own framing is that the segments were muted with initiatives underway. See ASSUMPTIONS.md Part 3 for the full inventory.

### D. Asset status

| Asset | Status |
|---|---|
| README.md | Complete, 65 sections |
| ASSUMPTIONS.md | Complete, Parts 1–5 |
| verify.py | 107 checks, all passing — delivered, not committed |
| LinkedIn carousel + caption | To follow |

---

*Day 71 of 90 · [← Day 70 — Poly Medicure](../Day-70-Poly-Medicure) · Day 72 →*
