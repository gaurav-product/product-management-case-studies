# Day 67 — Max Healthcare: The Metric Its Biggest Competitor Retired

> Max Healthcare's June 2026 quarter was led with ARPOB — average revenue per occupied bed — up 5% to ₹81,900. Apollo Hospitals, the larger listed peer, had already **stopped publishing that metric**, telling investors it blends pricing, length of stay and occupancy into one figure and that a high reading can reflect acuity mix and bed turnover rather than patient revenue. Max's own numbers prove Apollo right: revenue grew 15.85% over occupied bed days up 10%, which mechanically produces 5.32% — the reported figure, with no tariff in it anywhere. Meanwhile the hospital's actual prices are set by insurers who suspended cashless at Max in 2025 rather than raise them, and now grant an automatic 6% revision against 7–8% medical inflation. ARPOB rose 5%; PAT rose 3.48% and fell 7.75% sequentially. **The number that looked best was the one furthest from cash, and the industry's largest operator had already told everyone why.**

---

## 1. Cover

**Product:** Max Healthcare — 21 hospitals, Max@Home, Max Lab
**Legal entity:** Max Healthcare Institute Limited · **CIN:** L72200MH2001PLC322854
**Domain:** Healthtech — hospital services
**Period examined:** Q1 FY27 (quarter ended 30 June 2026), reported 13 August 2026
**Written:** 2 September 2026
**Author:** Gaurav Singh · Day 67 of 90

---

## 2. Repository Metadata

| Field | Value |
|---|---|
| Legal entity | Max Healthcare Institute Limited |
| CIN | L72200MH2001PLC322854 |
| Incorporated | 18 June 2001 |
| Registrar | RoC Mumbai |
| Former names | **Infinitum Technologies Private Limited** → Max Healthcare Institute Private Limited → Max Healthcare Institute Limited |
| Registered office | 401, 4th Floor, Man Excellenza, S. V. Road, Vile Parle (West), Mumbai 400056 |
| Listings | BSE **543220** · NSE **MAXHEALTH** · NIFTY 50 constituent |
| NIC code | **722 — "Software publishing, consultancy and supply"** |
| Chairman & MD | Abhay Soi |
| Promoters | Abhay Soi; Kayak Investments Holding Pte. Ltd. |
| Authorised / paid-up capital | ₹1,385 Cr / ₹973.24 Cr 🟡 |

India's industrial classification files one of the country's two largest listed hospital chains under software publishing. The cause is visible in the row above it: the entity began life as **Infinitum Technologies Private Limited** and the code was never changed. **This is the fourth consecutive case study in this series whose NIC code does not describe the business** — after BookMyShow (99999, "unclassified"), Atomberg (7290, "other computer related activities") and Vodafone Idea (3210, "electronic valves and tubes"). At four in a row it stops being a curiosity and becomes a finding about the register itself.

---

## 3. Badges

`Day 67/90` · `Healthtech` · `Hospital services` · `Listed (BSE/NSE, NIFTY 50)` · `Q1 FY27 primary` · `Competitor retired the headline metric` · `108 programmatic checks, all passing` · `Zero fabricated figures`

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

Max Healthcare reported the quarter ended 30 June 2026 on 13 August. Network gross revenue was ₹2,982 Cr, up **15.85%**. Operating EBITDA was ₹704 Cr, up 15%. Occupancy held at 75% despite a 13% increase in operational bed capacity. Free cash flow was ₹397 Cr and net debt to EBITDA stayed below 1×. The presentation led with **ARPOB up 5% to ₹81,900**.

The operational execution behind that is real and should be credited first. Max commissioned 202 beds at Max Smart with 198 more due, acquired and began integrating Kalinga Hospital in Bhubaneswar, secured land for a 450-bed hospital in Pune, and approved ₹425 Cr for a new tower at Vaishali. Max@Home grew 32% and Max Lab 20%. International patient revenue rose 18% to ₹247 Cr. None of that is an accounting artefact.

But the headline metric does not mean what a reader assumes. **ARPOB is revenue divided by occupied bed days.** Revenue grew 15.85% and occupied bed days grew 10%; the ratio of those two is **5.32%**, which is the reported 5%. No tariff appears anywhere in the calculation. ARPOB rises when a hospital treats more complex cases, discharges faster, or admits richer patients — and falls when it does the opposite — entirely independently of what it charges.

That is not this author's inference. **Apollo Hospitals formally discontinued reporting ARPOB**, telling investors the metric blends pricing, length of stay and occupancy into one figure and that a high reading can reflect operational efficiency and acuity mix rather than patient revenue. The largest listed operator in the sector retired the number that the second-largest still leads with.

Max's own disclosures show the mix at work. Kalinga entered the network at an ARPOB of **₹35,000 — a 57.27% discount** to the network — and network ARPOB rose anyway. International patients, who pay most and are priced unilaterally, grew at **1.14×** the network rate. Meanwhile the prices that actually govern 91% of hospital revenue are negotiated with insurers and CGHS, and those counterparties spent 2025 suspending cashless at Max rather than raising tariffs. The settlement is an **automatic 6% revision** against medical inflation of 7–8%.

The consequence appears where it always does. Revenue +15.85%, EBITDA +15%, ARPOB +5%, **PAT +3.48%** — and PAT down **7.75%** on the prior quarter. In the same quarter Apollo's PAT grew 34.18%; **Max's PAT growth was 10.18% of Apollo's**, on EBITDA margins within 0.56 points of each other. The divergence is entirely below EBITDA.

The proposal, *Episode Price*, follows from that diagnosis. It is designed, costed, and then ranked last — behind simply publishing what ARPOB is made of.

---

## 6. Product Overview

Max Healthcare operates 21 facilities with more than 6,000 beds across NCR Delhi, Haryana, Punjab, Uttarakhand, Maharashtra and Uttar Pradesh, with roughly 85% of bed capacity in metro and tier-1 cities. Alongside the hospitals it runs Max@Home for home health services and Max Lab for pathology outside the hospital network.

The product is a bed, a clinician and a procedure, sold to four buyer types that pay very differently: insurers, government schemes such as CGHS, corporates, and self-paying patients including international ones. The mix between them is the single largest determinant of reported revenue per bed, and it is not disclosed.

---

## 7. Company Background

The present company was formed when Radiant Life Care, promoted by Abhay Soi, acquired 49.7% of the erstwhile Max Healthcare Institute and then amalgamated with it, the combined entity taking the Max Healthcare name. The legal shell is older and unrelated to healthcare: incorporated on 18 June 2001 as Infinitum Technologies Private Limited, with the registered office shifted from Delhi to Maharashtra in March 2019.

Abhay Soi is Chairman and Managing Director and, with Kayak Investments Holding Pte. Ltd., a promoter. The company is a NIFTY 50 constituent and reported FY26 consolidated revenue of ₹8,373.45 Cr, up 19.14% 🟡.

---

## 8. Product Timeline

| Date | Event |
|---|---|
| 18 Jun 2001 | Incorporated as Infinitum Technologies Private Limited |
| Dec 2018 | Radiant Life Care–Max Healthcare shareholders' agreement |
| Mar 2019 | Registered office shifted from Delhi to Maharashtra |
| Aug 2020 | Amalgamated entity listed; Information Memorandum filed |
| Aug 2025 | **Niva Bupa suspends cashless at all Max hospitals**; Care Health had done so earlier in Delhi-NCR |
| Aug 2025 | AHPI directs members to suspend cashless for Bajaj Allianz; withdrawn 29 Aug |
| Sep–Oct 2025 | AHPI–Star Health dispute; cashless restored 10 Oct |
| Q1 FY26 | **Apollo Hospitals announces it will discontinue reporting ARPOB** |
| May 2026 | Kalinga Hospital, Bhubaneswar acquired |
| 30 Jun 2026 | Yerawada Properties acquired — land for a 450-bed Pune hospital |
| 13 Aug 2026 | Q1 FY27 results: ARPOB +5%, PAT +3.48% |

---

## 9. Vision & Mission

Max states its vision as being the most well-regarded healthcare provider in India, committed to clinical excellence and patient care supported by technology and research, expressed as "To serve. To excel."

The gap this case study examines is not between that statement and behaviour — Max provides free treatment to economically weaker sections and runs 750+ clinical trials — but between the stated purpose and the instrument used to report progress against it. Clinical excellence and ARPOB can move in opposite directions without anyone noticing.

---

## 10. Problem Statement

**For Max:** the metric it leads with cannot distinguish a price increase from a mix change, so neither management nor investors can tell whether the business is being paid more or simply treating different people. Apollo has said so publicly and stopped publishing it.

**For the patient:** the price of an episode of care is unknown before admission and assembled afterwards from itemised line items, which is why a cashless dispute between a hospital and an insurer lands on the patient as an unexpected bill.

**The intersection:** the same opacity that makes ARPOB uninterpretable to an investor makes the bill unpredictable to a patient. Both are downstream of the fact that **Max does not sell a priced episode of care; it sells a bed and bills for what happens in it.**

---

## 11. Market Research

Indian private hospital care is consolidating around a handful of listed chains, with Apollo Hospitals and Max Healthcare the two largest by market capitalisation. Both reported June-quarter results ahead of expectations, and both are in the middle of large bed-expansion programmes — Apollo targeting 14,100 beds by FY31.

The structural feature that matters here is that the buyer is usually not the patient. Insurers, CGHS and corporates negotiate tariffs on behalf of the people receiving care, which makes the tariff a bilateral commercial outcome rather than a market price — and makes any metric that averages across payer classes a measure of who walked in rather than of what anything costs.

---

## 12. Industry Analysis

The 2025 cashless disputes exposed the mechanism. AHPI, representing more than 15,000 hospitals, directed members to suspend cashless services for Bajaj Allianz over tariffs unrevised against 7–8% medical inflation, then issued similar warnings over Star Health; Niva Bupa separately suspended cashless at all Max hospitals when tariff renegotiation failed, with Max stating that hospital tariffs had stagnated at 2022 levels. The General Insurance Council called the advisories arbitrary; IRDAI's Vice-Chairperson noted that hospitals misusing cashless rules can lose network status within 15 days.

The important point for this analysis is what the fight reveals rather than who was right. **Hospital prices are negotiated annually, bilaterally, and behind closed doors**, which means a listed hospital can simultaneously tell insurers its rates are frozen and tell investors its revenue per bed is rising — both truthfully — because the two statements are about different variables that ARPOB merges into one.

---

## 13. TAM / SAM / SOM

*Framework note: run in restricted form. No primary-sourced Indian hospital market size was located that is not a vendor estimate, so this is sized from Max's own disclosed revenue and payer structure, expressed in rupees of annualised revenue.*

| Layer | Definition | Size | Basis |
|---|---|---|---|
| TAM | Max's annualised network revenue | **₹11,928 Cr** | ₹2,982 Cr × 4 🟢 |
| SAM | Annualised revenue from hospitals | **₹10,977.78 Cr** | ₹247 Cr ÷ 9% × 4, derived |
| SOM | Revenue Max prices unilaterally (international) | **₹988 Cr** | ₹247 Cr × 4 🟢 |
| *The constraint* | Revenue priced by negotiation | **91% of hospital revenue** | Derived, D7b |

The last row is the whole strategic problem stated as a number. Nine rupees in ten of hospital revenue is priced by a counterparty that spent the previous year refusing to raise it.

---

## 14. Competitor Analysis

*Framework note: restricted to operators that file. Apollo Hospitals Enterprise and Max Healthcare are both listed and report quarterly. Fortis Healthcare and Narayana Health also file but are not compared here, because neither disclosed the specific metric this case study turns on for the quarter examined; they are named rather than estimated.*

| Metric, Q1 FY27 | Max Healthcare | Apollo Hospitals |
|---|---|---|
| Revenue | ₹2,982 Cr (network gross) | ₹7,043 Cr (consolidated) |
| Revenue growth | +15.85% | +21% |
| Healthcare-services EBITDA margin | 23.61% (computed) | 24.17% |
| PAT | ₹357 Cr | ₹581 Cr |
| **PAT growth** | **+3.48%** | **+34.18%** |
| Occupancy | 75% | 70% (from 65%) |
| Operating beds | 6,000+ | 8,352 |
| **ARPOB** | **₹81,900, +5%** | **Discontinued as a reported metric** |

Three readings. **Apollo is 2.36× Max's revenue and grew faster from the larger base.** On profit the gap is not close: **Max's PAT growth is 10.18% of Apollo's**, in the same quarter, the same country and the same regulatory environment.

Second, the divergence is not operational. Max's computed EBITDA margin is **0.56 points below** Apollo's healthcare-services margin — effectively the same. Everything separating +3.48% from +34.18% sits below EBITDA, in depreciation, finance cost and the drag of newly commissioned capacity.

Third, and the reason this is a case study rather than a scorecard: **Apollo retired ARPOB on the record.** Its stated reasoning is that ARPOB blends pricing, length of stay and occupancy, and that a high reading can reflect higher acuity mix and better bed turnover rather than pure patient revenue. That is a competitor's own attribution, published, and it is a far stronger claim than any outside critique of Max's reporting could be.

And the number that cuts against this case study's own argument, included because it should be: Max's occupancy is **5 points above Apollo's** while carrying 13% more beds year on year. On the operational task of filling capacity, Max is doing better than the company whose profit is compounding.

---

## 15. SWOT

| | |
|---|---|
| **Strengths** — occupancy of 75%, five points above Apollo, held through a 13% capacity increase; 85% of beds in metro/tier-1; free cash flow ₹397 Cr with net debt/EBITDA below 1×; Max@Home +32% and Max Lab +20%; international revenue +18% at 1.14× network growth | **Weaknesses** — PAT growth of 3.48%, a tenth of Apollo's; PAT down 7.75% sequentially; EBITDA per bed up only 3.94% against revenue up 15.85%; headline metric formally retired by the larger peer; payer mix not disclosed |
| **Opportunities** — Kalinga at 50% occupancy and ₹35,000 ARPOB against a network ₹81,900; 202 beds commissioned with 198 to follow; medical education approved in principle at a stated ROCE above 25%; CGHS complex-specialty rates flowing from June | **Threats** — 91% of hospital revenue priced by negotiation; automatic insurance revision of 6% against 7–8% medical inflation; net debt up 24.95% in one quarter; cashless suspension precedent established against Max specifically in 2025 |

---

## 16. Porter's Five Forces — run twice

*Framework note: run as a double pass on the two payer classes Max actually serves — the **negotiated** patient, whose price is set by an insurer, CGHS or a corporate, and the **unilaterally-priced** patient, who pays Max directly. The seam is chosen because the 2025 cashless suspensions hit one column and left the other untouched, and because the two columns are averaged together into the single ARPOB figure the company reports.*

| Force | The NEGOTIATED patient (≈91% of hospital revenue) | The UNILATERALLY-PRICED patient (≈9%) |
|---|---|---|
| **Buyer power** | **Very high and organised.** Insurers negotiate annually and demonstrated in 2025 they will suspend cashless rather than concede; the settlement is a 6% automatic revision against 7–8% inflation | **Low and atomised.** International and self-pay patients choose on outcome and reputation, and negotiate nothing |
| **Rivalry** | On empanelment and discount depth, not on clinical quality — the insurer is comparing rate cards | On clinical reputation and specialty depth, where Max's metro concentration is an advantage |
| **Substitutes** | Other empanelled hospitals; increasingly, day-care and home settings that sit outside the tariff schedule | Medical tourism to other countries; deferral |
| **New entrants** | Barred by capital and empanelment cycles | Barred by clinical reputation, which takes longer to build than a hospital |
| **Supplier power** | High and symmetric — clinicians, devices and oncology drugs price against both columns equally | Identical, but recoverable in price |

The inversion is the finding. In the left column Max is a price-taker facing an organised buyer that has already proved it will withhold payment. In the right column Max is a price-setter facing no organised buyer at all. **Reporting one ARPOB across both is reporting the average of a negotiated rate and a free one**, and every quarter that the right column grows faster than the left — as it did here, at 1.14× — ARPOB rises without a single price changing.
---

## 17. Business Model Canvas

| Block | Max Healthcare |
|---|---|
| Value proposition | Tertiary and quaternary care in metro locations, with specialty depth |
| Customer segments | Insured patients, CGHS/government, corporates, self-pay domestic, international |
| Channels | Hospital OPD/IPD, Max@Home, Max Lab, referral networks, international facilitators |
| Revenue streams | Inpatient procedures, outpatient consults, diagnostics, home care |
| Key resources | 6,000+ beds, 5,800+ clinicians, metro real estate, empanelment agreements |
| Key activities | Clinical delivery, capacity build, payer negotiation, integration of acquisitions |
| Key partners | Insurers, CGHS, corporates, device and pharma suppliers |
| Cost structure | Clinician cost, consumables and drugs, depreciation on new towers, finance cost |
| Price setter | **The insurer, for roughly 91% of hospital revenue** |

The last row is the anomaly and it is the reason the rest of the canvas behaves oddly. A business that does not set its own price for nine-tenths of its revenue is, for those patients, a capacity provider rather than a product company.

---

## 18. Revenue Model

Network gross revenue of ₹2,982 Cr resolves into roughly ₹2,744.44 Cr from hospitals — **92.03%** — with Max@Home and Max Lab together contributing ₹136 Cr, or 4.56%. Consolidated revenue from operations, a different and narrower measure, was ₹2,366.17 Cr, **79.35%** of the network figure.

The model's constraint is that revenue growth of 15.85% converted into EBITDA growth of 15% but PAT growth of only **3.48%**, and EBITDA per bed rose just **3.94%** — 11.91 points below revenue growth. New capacity arrives with full depreciation and finance cost and partial occupancy, so the faster Max builds, the wider the gap between the top line and the bottom.

---

## 19. Target Users

Max's core user is the insured urban patient requiring tertiary care, concentrated in NCR and the metro markets where 85% of its beds sit. Around that core sit CGHS beneficiaries, corporate-covered employees, self-paying domestic patients, and international patients contributing 9% of hospital revenue.

The user this case study focuses on is the one who cannot find out what treatment will cost before receiving it — a category that includes almost every patient in the left-hand column of §16, and which is where the cashless disputes actually land.

---

## 20. Personas

**Sunil, 58, Delhi, insured through a corporate policy.** Admitted for a cardiac procedure. He knows his sum insured but not the price of the procedure; the two are reconciled after discharge, and any gap is his.

**Rehana, 44, from Dhaka, self-paying.** An international patient who received a quoted package price before travelling. She is 9% of hospital revenue and the only patient in this list who knew the cost in advance.

**A Max finance controller.** Reports ARPOB quarterly. Cannot decompose it into price, acuity and length of stay in the published disclosure, because the company does not publish those components.

---

## 21. Jobs To Be Done

*Framework note: JTBD is used because the same clinical service is bought by four parties with genuinely different jobs, which is the reason a single blended metric misleads.*

| Job | Who | Current solution | Adequacy |
|---|---|---|---|
| "Treat this condition well" | Patient | Max clinical services | Strong — this is what Max is good at |
| "Tell me what it will cost before I commit" | Patient / family | Estimate at admission, itemised bill after | **Badly served** — the estimate is not a price |
| "Contain my claims cost per member" | Insurer | Annual tariff negotiation, cashless leverage | Adversarial by design |
| "Show me whether we are being paid more" | Investor / management | ARPOB | **Cannot answer the question**, per Apollo |

Rows two and four are the same failure viewed from opposite ends. Nobody — not the patient, not the investor — can see the price of an episode of care, because the business does not produce one.

---

## 22. User Journey

| Stage | What happens | What is priced |
|---|---|---|
| Referral / OPD | Consultation, diagnostics | Line items, individually |
| Pre-authorisation | Insurer approves an estimated sum | An estimate, not a price |
| Admission | Bed category chosen, procedure begins | Nothing fixed |
| Stay | Consumables, drugs, ICU days accumulate | Accrues by line item |
| Discharge | Bill assembled; insurer applies deductions | Settled after the fact |
| Post-discharge | Complications may generate a fresh admission | Billed again |

The last row matters for §50. A complication arising from the original procedure produces **additional** revenue under itemised billing, which is a structural incentive nobody at Max designed and nobody can remove without changing how care is sold.

---

## 23. User Flow

The patient's decision flow is short and uninformed: choose hospital → arrive → be treated → discover cost. The only branch where price enters before treatment is the international package, and that is 9% of hospital revenue.

For the insurer the flow is the inverse — price is negotiated a year ahead, then defended claim by claim through deductions, which is what the 2025 disputes were about.

---

## 24. Information Architecture

Max's patient-facing digital estate is organised around access — find a doctor, book an appointment, view reports — with Max@Home and Max Lab as adjacent services. Digital revenue is disclosed at ₹941 Cr, roughly 32% of overall revenue, which measures digitally-originated business rather than a digital product.

Nothing in the hierarchy exposes price before care. That is an architectural absence rather than a design flaw, because the underlying system has no episode price to display.

---

## 25. UX Audit

The dominant UX failure in Indian private hospital care is that the most consequential number in the transaction — what it will cost — is unavailable at the only moment the patient could act on it. Max is not worse than peers here; it is representative.

The 2025 cashless suspensions made the cost of that opacity concrete: when Niva Bupa's agreement with Max lapsed, patients who had chosen Max partly *because* it was cashless discovered at admission that it no longer was. The design failure is that the patient's information about their own liability depends on a bilateral contract they cannot see.

---

## 26. UI Audit

Max's booking and reports interfaces are functional and comparable to Apollo's; there is no visible interface deficit driving the findings in this case study.

Worth stating plainly because it bounds the proposal: **no interface change fixes an unpriced product.** A price cannot be displayed until it exists.

---

## 27. Accessibility

Max provides free treatment to economically weaker sections — tens of thousands of OPD patients and roughly 1,500 IPD patients per quarter — under the obligations attached to its land and licences. That is a genuine access contribution and is reported.

The broader accessibility constraint is geographic: 85% of beds are in metro and tier-1 cities, which means Max's model is structurally unavailable to most of the country, and Kalinga in Bhubaneswar is the first significant test of whether the playbook travels to a tier-2 market at a ₹35,000 ARPOB.

---

## 28. Feature Breakdown

| Area | Current state |
|---|---|
| Hospitals | 21 facilities, 6,000+ beds, 30+ specialities, 5,800+ clinicians |
| Capacity added | 202 beds live at Max Smart; 198 more in Q2 FY27; ₹425 Cr approved for Vaishali Tower 3 (~202 beds, Q4 FY30) |
| Acquisitions | Kalinga, Bhubaneswar (May 2026) — 50% occupancy, ₹35,000 ARPOB, ₹154 Cr FY26 revenue |
| Land bank | Yerawada Properties (30 Jun 2026) — 450-bed Pune hospital planned |
| Max@Home | ₹78 Cr, +32% YoY |
| Max Lab | ₹58 Cr, +20% YoY |
| International | ₹247 Cr, +18%, 9% of hospital revenue |
| Medical education | Board in-principle approval following NMC amendments; stated ROCE above 25% |
| Research | 750+ clinical trials |
| **Episode pricing** | **Does not exist except for international packages** |

That final row is the gap the proposal addresses, and the check that it does not already exist comes from Max's own disclosure: the only patients receiving a fixed price before treatment are the 9% who pay Max directly.

---

## 29. AI Capabilities

Max has not disclosed a material consumer-facing AI product, and none is proposed here. The company's research footprint sits in clinical trials rather than algorithmic products.

The relevant observation is that the data required to price an episode — historical cost, length of stay and complication rates by procedure and comorbidity — is exactly the data a hospital already generates and rarely models. That is an analytics problem before it is an AI one.

---

## 30. Product Metrics

| Metric | Q1 FY27 | Comparator |
|---|---|---|
| Network gross revenue | ₹2,982 Cr (+15.85%) | Apollo ₹7,043 Cr (+21%) |
| Operating EBITDA | ₹704 Cr (+15%) | — |
| EBITDA margin | 23.61% computed / 24.8% reported | Apollo HS 24.17% |
| **PAT** | **₹357 Cr (+3.48%)** | **Apollo ₹581 Cr (+34.18%)** |
| PAT, sequential | **−7.75%** | — |
| **ARPOB** | **₹81,900 (+5%)** | **Apollo: discontinued** |
| Occupancy | 75% | Apollo 70% |
| Bed capacity | +13% YoY | — |
| Occupied bed days | +10% YoY | — |
| EBITDA per bed | ₹71.2 lakh (+3.94%) | — |
| Net debt | ₹2,384 Cr (+24.95% QoQ) | — |

Two disclosed figures do not reconcile and are not forced to. The reported EBITDA margin of 24.8% implies a revenue base of **₹2,838.71 Cr**, which is ₹143.29 Cr — **4.81%** — below the network gross revenue of ₹2,982 Cr; the difference is presumably a gross-to-net adjustment that is not broken out. Consolidated revenue is a third, narrower figure again at 79.35% of network. All three are reported; the analysis uses each on its own basis and never mixes them (Appendix A-2).

---

## 31. North Star Metric

Max's implied north star is ARPOB, and this quarter demonstrates the failure: it rose 5% while PAT rose 3.48% and fell sequentially, and the metric cannot say whether any price changed.

**Proposed North Star — EPE/1k: Episode-Priced Episodes per 1,000 eligible admissions.**

An episode counts in the numerator only if **all four** hold:
1. a single all-in price was published and agreed **before** admission;
2. complications within the defined post-discharge window were carried by Max, not rebilled;
3. the payer settled at that price with no post-hoc deduction;
4. the patient's out-of-pocket did not exceed the published price.

**The denominator is the design choice.** It is *eligible admissions* — every admission in a procedure family where an episode price is offered — so growing itemised volume in a bundled specialty **lowers** the metric. Max cannot improve EPE/1k by doing more of the thing this case study says is the problem.

**Guardrail — CSR-90: Case Severity Refusal at the 90th percentile.** In the decile of procedure families where episode pricing is most used, the rate at which Max declines, defers or transfers out high-severity patients, reported **by specialty rather than in aggregate** and measured against the pre-bundle baseline. Owned by a clinical governance function with no revenue target. A breach automatically suspends episode pricing in the affected family — suspension is the default, not a decision someone must argue for.

This guardrail is not optional decoration. Patient selection is the documented failure mode of every bundled-payment scheme ever run, and §40 sets out why it must be engineered against before the product is built rather than after.

---

## 32. Product Analytics

Max holds the dataset that would settle its own reporting problem: cost, length of stay, complication rate and payer class per admission. Decomposing ARPOB into price, acuity and length of stay is an analytics exercise on data already captured, not a new collection effort.

The absence of that decomposition in disclosure is the evidence. A company reporting a blended ratio while holding its components has chosen the ratio.

---

## 33. AARRR

*Framework note: applied to the inpatient business, where the economics are decided.*

| Stage | Reading |
|---|---|
| Acquisition | Working — occupancy held at 75% through a 13% capacity increase |
| Activation | Working — occupied bed days +10% |
| Retention | Not meaningfully measurable in tertiary care; episodic by nature |
| Revenue | ARPOB +5%, but **10% of that is volume mix, not price**; PAT +3.48% |
| Referral | Clinician and payer referral networks, undisclosed |

The funnel is healthy until the revenue row, which is the opposite of most case studies in this series. Max is not failing to fill beds; it is failing to convert filled beds into profit, and its reporting metric obscures precisely that step.

---

## 34. HEART

| Dimension | Max |
|---|---|
| Happiness | Not disclosed; no NPS or CSAT published |
| Engagement | Not applicable in the usual sense; OBD +10% is the closest analogue |
| Adoption | Max@Home +32%, Max Lab +20% — the fastest-growing surfaces |
| Retention | Not disclosed |
| Task success | Not disclosed; clinical outcomes not published at procedure level |

Four of five rows are blank, which is itself the point: a hospital chain reporting revenue per bed and occupancy is reporting throughput, and publishes nothing about whether the care worked.

---

## 35. Growth Strategy

Max's growth strategy is capacity-led and acquisitive: brownfield towers at Max Smart and Vaishali, greenfield land at Pune, Kalinga acquired and targeted for a 50–80% ARPOB and occupancy improvement over twelve months, plus entry into medical education at a stated ROCE above 25%.

**Checking whether the proposal already exists, from Max's own disclosure.** Fixed all-in pricing before treatment exists at Max only for international patients, who are 9% of hospital revenue. For the other 91% the sequence is estimate, treat, itemise, deduct. So an episode price for domestic insured care does not exist — and the reason it does not is visible in §12: it would have to be agreed with the same insurers who suspended cashless rather than raise tariffs. That is not an oversight; it is the negotiating position.

---

## 36. Growth Loops

The intended loop is: capex → beds → occupancy → revenue → cash → capex. It is functioning on the first three arrows and stalling on the fifth: net debt rose ₹476 Cr in the quarter, **1.20× the ₹397 Cr of free cash flow generated**, so the build is currently outrunning internal funding.

There is a second, adverse loop specific to itemised billing. A complication generates additional billable activity, so the revenue system is indifferent to whether care succeeded first time. No one designed this and no interface change alters it; only changing the unit of sale does.

---

## 37. Network Effects

Hospital care has weak network effects. Scale confers procurement leverage and clinician attraction, but one patient's choice of Max does not improve another's experience.

The one real effect runs through payers: a chain large enough that insurers cannot exclude it has leverage in tariff negotiation. That is precisely the leverage AHPI tried to organise collectively in 2025, and precisely what an individual insurer's cashless suspension is designed to break.
---

## 38. Product Strategy

Max's strategy is coherent as a capacity business and under-specified as a pricing business. Building beds in metro markets where it already has clinician density and brand is the right long-run play, and the occupancy record — 75% through a 13% capacity increase — shows it executes.

The strategic gap is that the company measures the capacity half well and the pricing half with an instrument that cannot see it. **Nine-tenths of hospital revenue is set in an annual bilateral negotiation, and nothing Max publishes reveals how that negotiation went** — because ARPOB moves for reasons that have nothing to do with it.

---

## 39. Monetization

Max monetises activity: a bed-day, a procedure, a consumable, a drug, each billed separately and reconciled with a payer afterwards. Revenue per unit of activity is therefore a function of what activity occurred, which is why ARPOB rises when acuity rises even if every line item is priced identically.

The monetisation gap sits exactly where the patient's uncertainty sits. **Nobody sells an episode of care in India's private system except to international patients**, and the 9% who buy one are the only people who know the price before they consent to treatment.

---

## 40. Trust & Safety

*Placed before §50 deliberately, because the proposal that follows creates a clinical incentive that is dangerous if built without the constraints specified here, and stating that after proposing it would be the wrong order.*

Bundled episode pricing has one well-documented failure mode and several smaller ones, and each needs a mechanic rather than a principle.

**Patient selection — the serious one.** If Max is paid a fixed price per episode, the profitable move is to admit straightforward patients and avoid complex ones. This is the pathology that has appeared in every bundled-payment programme internationally, and in a healthcare system it means sick people are turned away. The mechanic: **CSR-90 measures refusal, deferral and transfer-out rates for high-severity patients in bundled families against the pre-bundle baseline, by specialty**, owned by clinical governance with no revenue target, with automatic suspension of the bundle on breach. A bundle that cannot be measured this way is not launched.

**Under-treatment within the episode.** A fixed price rewards doing less. The mechanic: the bundle price is conditioned on published clinical protocol adherence and readmission rates, and any episode with a protocol deviation is excluded from EPE/1k regardless of its economics.

**Risk-adjustment gaming.** If severity determines which bundle tier applies, there is an incentive to record patients as sicker than they are. The mechanic: tier assignment is fixed at pre-authorisation from a defined comorbidity set and cannot be revised upward after admission.

**The incentive that must be excluded, stated plainly.** If episode pricing is rolled out where it is most profitable rather than where it is clinically safest, it becomes a margin instrument wearing a transparency costume. §48 therefore places margin-linked targets for bundle expansion permanently out of scope, and §53 makes the CSR-90 baseline a precondition of launch rather than a post-launch report.

---

## 41. Technical Architecture

The relevant systems are the Hospital Information System, the billing and claims engine, and the pre-authorisation interface with payers. Max rolled out a new HIS at Kalinga on 1 August 2026, which indicates the stack is standardised enough to be deployed into an acquisition within three months.

Episode pricing does not require new infrastructure so much as a new object: a persistent *episode* record that binds an admission, its complications and its post-discharge window into one billable entity. Today the atomic unit is the line item.

---

## 42. Data Flow

Under itemised billing the flow is: clinical event → charge capture → bill assembly → claim → payer deduction → settlement. Price is discovered at the end.

Under episode pricing the flow inverts: comorbidity assessment → tier assignment → published price → treatment → settlement at the agreed price, with complications absorbed. The critical constraint is that **cost data must flow to clinical governance and to CSR-90 reporting on a path that does not touch admission decisions**, enforced by system separation rather than policy, so that no clinician sees an episode's margin at the moment of deciding whether to admit.

---

## 43. API Ecosystem

The live integration surface is with insurers and TPAs for pre-authorisation and claims, and with CGHS for government-scheme settlement. This is where an episode price would have to be transacted, and it is the same interface across which the 2025 cashless suspensions were executed.

That dual purpose is worth naming: the integration Max depends on for revenue is controlled by the counterparty it is negotiating against.

---

## 44. Privacy & Security

Hospital data is among the most sensitive category under India's DPDP framework, and episode pricing requires comorbidity data at pre-authorisation — meaning more clinical detail crosses to the payer earlier than it does today.

The design position is that **tier assignment should transmit a tier, not a diagnosis**. The payer needs to know which price applies, not the patient's full comorbidity profile; sending the latter because it is easier would expand what insurers know about applicants in ways that outlast the transaction.

---

## 45. Pain Points

| # | Pain point | Evidence |
|---|---|---|
| P1 | Headline metric cannot separate price from mix | Apollo's stated reason for discontinuing ARPOB 🟢 |
| P2 | ARPOB growth is arithmetically explained by revenue ÷ OBD | Derived, D2a–D2c 🟢 |
| P3 | Revenue +15.85% converts to PAT +3.48% | Q1 FY27 results 🟢 |
| P4 | PAT fell 7.75% sequentially | Q1 FY27 vs Q4 FY26 🟢 |
| P5 | 91% of hospital revenue priced by negotiation | Derived from disclosed international share 🟢 |
| P6 | Automatic insurance revision of 6% vs 7–8% medical inflation | Earnings call; dispute reporting 🟡 |
| P7 | Patient cannot learn the price before consenting | Sector practice; Max prices episodes only for international patients 🟢 |
| P8 | Reported margin implies a revenue base ₹143.29 Cr below network gross | Derived, D4d–D4f 🔴 |
| P9 | Net debt rose 1.20× free cash flow in one quarter | Q1 FY27 disclosure 🟢 |

---

## 46. Opportunity Mapping

| Opportunity | Annualised revenue addressed | Requires |
|---|---|---|
| Publish ARPOB decomposed into price, acuity, length of stay | ₹11,928 Cr | Nobody's cooperation |
| Ramp occupancy at Kalinga and newly commissioned beds | ₹1,550.64 Cr | Nobody's cooperation |
| Expand international patient volume | ₹988 Cr | Patients to choose Max |
| Episode pricing for domestic care | ₹10,977.78 Cr | Insurers and CGHS to agree |
| Medical education | Not yet sized | Regulatory approval, capital |

The middle column is the largest number on the page and the right column explains why it is also the hardest. The two opportunities requiring nobody's agreement are the ones §47 ranks first and second under stress.

---

## 47. RICE

*Framework note: run with a sensitivity pass. Initiatives requiring a counterparty — insurer, CGHS or patient — to change behaviour are multiplied by a stress rule; those delivering value on revenue and assets Max already controls are exempt.*

**The stress rule comes from Max's own disclosure.** International patients are **9% of revenue from hospitals** — the only revenue Max prices unilaterally. The remaining **91%** is priced by insurers, CGHS and corporates, the counterparties that in 2025 chose to suspend cashless at Max rather than raise tariffs. Any initiative requiring their agreement is therefore discounted to **9.00%** of its nominal reach.

| Initiative | Reach (₹ Cr p.a.) | Impact | Conf. | Effort | **Base** | **Stressed** |
|---|---|---|---|---|---|---|
| ARPOB decomposition + reporting | 11,928.00 | 0.50 | 0.95 | 12 | **472.15** | **472.15** (exempt) |
| International patient expansion | 988.00 | 3.00 | 0.70 | 18 | **115.27** | **10.37** |
| **Episode Price (PROPOSED)** | **10,977.78** | **1.00** | **0.35** | **40** | **96.06** | **8.64** |
| Occupancy ramp, new capacity | 1,550.64 | 1.00 | 0.85 | 16 | **82.38** | **82.38** (exempt) |

**Episode Price falls from 3rd of 4 at baseline to 4th and last under stress**, behind an initiative this case study did not propose. The winner beats it by **54.62×**. `verify.py` asserts programmatically both that the proposal finishes last and that it is the **weakest stressed initiative at baseline** — the only configuration in which the demotion is genuine rather than arranged.

Read that as the answer, not the caveat. A company whose headline metric has been publicly retired by its largest competitor should first **publish what that metric is made of** — price, acuity and length of stay, separately, from data it already holds. That requires no insurer's signature, no patient's behaviour change and twelve person-months, and it would tell management and investors something ARPOB structurally cannot.

---

## 48. MoSCoW

| | |
|---|---|
| **Must** | Decompose and publish ARPOB into price, acuity and length of stay; episode-level cost model by procedure and comorbidity; CSR-90 baseline established before any bundle launches; automatic bundle suspension on CSR-90 breach |
| **Should** | Published all-in prices for a defined procedure set; complication window carried by Max; tier assignment fixed at pre-authorisation |
| **Could** | Extension to CGHS; patient-facing price display; outcome publication by procedure |
| **Won't** | Any margin-linked target for bundle expansion; any upward tier revision after admission; any flow of episode margin data to admission decisions; any transmission of full comorbidity detail where a tier would suffice |

The "Won't" row is load-bearing. Each entry closes a specific route by which this becomes the patient-selection machine §40 warns about.

---

## 49. Kano

| Feature | Category | Note |
|---|---|---|
| Clinical quality and specialty depth | Basic | Absence ends the business |
| Metro location and bed availability | Performance | Where Max genuinely leads Apollo, at 75% vs 70% |
| Itemised bill after discharge | **Reverse** | The more detailed it is, the less the patient trusts it |
| All-in price known before consent | **Attractive** | Delivered today only to the 9% who pay directly |
| ARPOB as a reported metric | Indifferent → **Reverse** for investors | Apollo concluded it actively misleads and stopped |

Row three is the one product managers miss. A more granular bill is not a better bill; itemisation is the artefact of a system that priced nothing in advance, and each additional line is a further reminder that the total was never agreed.

---

## 50. Feature Proposal — *Episode Price*

**What it is.** A single all-in price per episode of care, published and agreed before admission, for a defined set of high-volume procedure families. The price covers the procedure, the stay, consumables, and **any complication within a defined post-discharge window**. Tier assignment is fixed at pre-authorisation from a declared comorbidity set. The patient knows the number before consenting; the payer settles at it without post-hoc deduction.

**Why this shape.** It attacks the diagnosis rather than the symptom. Under itemised billing, ARPOB rises when a patient is discharged faster or treated more intensively, which is why it cannot report price — and a complication generates additional revenue, which is why the billing system is indifferent to whether care worked first time. **Under an episode price both problems dissolve at once:** revenue per episode is a stated price, so it can be reported as one, and a complication becomes a cost rather than a sale.

**What it is not.** It is not a discount, and not a package rate negotiated per insurer behind closed doors — the price is published. It is not applied where CSR-90 cannot be baselined first.

**North Star:** EPE/1k, per §31, with eligible admissions as the denominator.
**Guardrail:** CSR-90, per §31, by specialty, owned by clinical governance.

---

## 51. PRD

**Problem.** Max cannot report whether it is being paid more, because ARPOB conflates price with mix; patients cannot learn what care costs before consenting; and complications are billable rather than costly.

**Goals.** Establish an auditable episode-level price and cost model; convert a measurable share of eligible admissions to published all-in pricing; and, independently of whether bundling scales, publish ARPOB's components.

**Non-goals.** Raising ARPOB. Expanding bundles into procedure families where severity cannot be risk-adjusted. Replacing insurer negotiation with a public pricing war.

**User stories.**
- As a patient, I am told one number before I consent, and my bill equals it.
- As an insurer, I settle a pre-agreed price without adjudicating line items.
- As Max's board, I can see price, acuity and length of stay as three separate series.

**Functional requirements.** Persistent episode record binding admission, complications and post-discharge window; comorbidity-based tier assignment fixed at pre-authorisation; published price list per family per tier; complication absorption logic; CSR-90 instrumentation by specialty against a pre-bundle baseline; automatic suspension on breach.

**Non-functional.** Tier transmitted to payers without full diagnosis payload; episode margin data physically separated from admission systems, enforced by build-pipeline test; DPDP-compliant consent for comorbidity capture.

**Acceptance criteria.** An episode counts toward EPE/1k only if all four §31 conditions hold. No bundle launches in a family without an established CSR-90 baseline.

**Success metrics.** EPE/1k at the R1 threshold in §54; CSR-90 no worse than baseline in every specialty measured separately; published ARPOB decomposition every quarter.

---

## 52. Wireframes

```
PRE-AUTHORISATION - EPISODE PRICE (payer-facing)
+--------------------------------------------------------------+
|  Procedure family ....... Knee replacement, unilateral        |
|  Tier ................... T2  (fixed at pre-auth)            |
|  -----------------------------------------------------------  |
|  ALL-IN EPISODE PRICE ............................ Rs X,XX,XXX |
|  Includes: procedure, stay, consumables, implants             |
|  Includes: any complication within 30 days post-discharge     |
|  Excludes: unrelated conditions diagnosed during stay         |
|  -----------------------------------------------------------  |
|  Transmitted to payer: tier + price. NOT the diagnosis file.  |
+--------------------------------------------------------------+

PATIENT CONSENT SCREEN
+--------------------------------------------------------------+
|  Your treatment will cost Rs X,XX,XXX.                        |
|  This is the price, not an estimate.                          |
|  If a complication occurs within 30 days, we bear the cost.   |
|  Your insurer has approved this amount in full.               |
|                        [ I understand and consent ]           |
+--------------------------------------------------------------+

BOARD REPORTING - ARPOB DECOMPOSED (the exempt initiative)
+--------------------------------------------------------------+
|  Reported ARPOB ................................. Rs 81,900   |
|  ...of which                                                  |
|    Price effect (tariff change, like-for-like) ......  +X.X%  |
|    Acuity / case-mix effect ......................... +X.X%   |
|    Length-of-stay effect ............................ +X.X%   |
|    Payer-mix effect ................................. +X.X%   |
|  -----------------------------------------------------------  |
|  CSR-90, worst specialty ............................ X.X%    |
+--------------------------------------------------------------+
```

---

## 53. Rollout Plan

**Phase 0 — three analyst-weeks on data Max already holds, designed to kill the proposal cheaply.**

Build an episode-level cost distribution for three high-volume procedure families over 24 months, joined to comorbidity and payer class.

- **K1.** Cost per episode cannot be predicted within a workable band from data available *at pre-authorisation*. If the price can only be known after treatment, it cannot be published before it.
- **K2 — named as the most likely to fire.** The variance in episode cost is driven overwhelmingly by patient factors Max cannot observe at admission. In that case any fixed price is either loss-making on complex patients or safe only if Max selects them out — which §40 forbids. **If K2 fires, the proposal should be abandoned, not redesigned.**
- **K3.** Insurers will not settle without itemised backup, because their own fraud controls operate on line items — making a published episode price commercially unusable regardless of its clinical merit.

**Phase 1 (Q3 FY27).** CSR-90 baseline established across the three families; no bundle offered yet. **Phase 2 (Q4 FY27).** One hospital, three families, one payer. **Phase 3 (FY28).** Expansion only under §54's rule.

**Running in parallel and contingent on nothing above:** the ARPOB decomposition that §47 ranks first under stress. It should start immediately, needs no counterparty, and does not depend on Phase 0 succeeding.

---

## 54. A/B Testing

| Arm | Design |
|---|---|
| A — control | Itemised billing with pre-authorisation estimate, as today |
| B — falsification arm | **Published capped price list** — itemised billing continues, but the total is capped at a published figure. Transparency without risk transfer |
| C — treatment | Episode Price as specified, with complication absorption |

**Arm B is built to kill the thesis.** It gives the patient the one thing they lack — a number they can rely on before consenting — without Max absorbing complication risk, without tiering, and without the episode record. If B matches C on patient-reported confidence, payer settlement friction and conversion, then the risk transfer is unnecessary and Max should simply publish capped prices, which is far cheaper and carries none of §40's clinical hazard.

**Pre-registered decision rule (R1).** Arm C proceeds to Phase 3 only if it beats Arm B by **more than 10 percentage points on EPE/1k** across two consecutive quarters, **and** CSR-90 is no worse than the pre-bundle baseline in every specialty measured separately, **and** the realised cost of absorbed complications is below the risk premium priced into the bundle. Failing any of the three, the programme reverts to Arm B or stops.
---

## 55. KPI Dashboard

| KPI | Baseline (Q1 FY27) | Target | Early warning |
|---|---|---|---|
| **ARPOB, decomposed** | Not published | Published quarterly | **If the price component is flat or negative while ARPOB rises, the thesis is confirmed in Max's own disclosure** |
| EPE/1k | 0 (not built) | R1 threshold, §54 | Below 10pp over Arm B at two quarters |
| CSR-90, worst specialty | Not measured | ≤ pre-bundle baseline | Any specialty worse than baseline |
| PAT growth vs revenue growth | 3.48% vs 15.85% | Gap narrowing | Gap widens again |
| EBITDA per bed | ₹71.2 lakh (+3.94%) | Above revenue growth | Falls further behind |
| Net debt vs FCF | 1.20× | Below 1× | Rises for two consecutive quarters |

The first row is the discipline and it is unusually cheap. Max already holds every input; the only reason the decomposition is not published is that nobody has been asked for it.

---

## 56. Product Roadmap

| Period | Focus |
|---|---|
| Q2 FY27 | ARPOB decomposition built and published; Phase 0 cost-distribution analysis run |
| Q3 FY27 | CSR-90 baselines established; Kalinga occupancy ramp continues; no bundle yet |
| Q4 FY27 | Episode Price Phase 2 — one hospital, three families, one payer |
| FY28 H1 | §54 decision rule evaluated; bundle scaled or stopped |
| FY28 H2 | Occupancy ramp at Vaishali and Pune capacity — the initiative RICE actually favours |

The sequencing puts the proposed feature third deliberately, behind reporting and behind occupancy, because that is where §47 put it.

---

## 57. Risks & Mitigation

| Risk | Mitigation |
|---|---|
| Bundles cause patient selection | CSR-90 baselined *before* launch; automatic suspension on breach; no margin-linked expansion targets |
| Published prices become a competitive floor insurers exploit | Publish per tier with the clinical protocol attached, so the price is inseparable from what it buys |
| Episode cost is unpredictable at pre-authorisation | K2 in Phase 0 tests exactly this and is named as most likely to fire |
| Decomposing ARPOB reveals a flat price component | This is a reporting improvement, not a business deterioration; disclose alongside the first decomposition |
| Capacity build outruns cash | Net debt rose 1.20× FCF this quarter; tracked as a §55 KPI |
| Comorbidity data expands what insurers learn | Transmit tier, not diagnosis; §44 |

---

## 58. Future Vision

The plausible good outcome is a hospital business that can state, quarter by quarter, how much of its revenue growth was price, how much was acuity and how much was simply more beds — and that sells a defined episode of care at a knowable price to at least the procedure families where cost is predictable. That is a smaller claim than "transform Indian healthcare," and it is achievable with data Max already has.

The bad outcome is not distress; free cash flow is positive and leverage is low. It is a company that keeps compounding capacity and reporting a metric its largest competitor abandoned, until the gap between 15.85% revenue growth and 3.48% profit growth becomes the story rather than a footnote.

---

## 59. PM Lessons

1. **When a competitor formally retires your headline metric, that is the case study.** Apollo's published reasoning did more work here than any external critique could, and it was available for free in an earnings call.
2. **Reconstruct a ratio from its inputs before believing it.** Revenue ÷ occupied bed days produced 5.32% against a reported 5% ARPOB growth — proving the metric contains no tariff at all.
3. **Ask who sets the price.** Nine-tenths of Max's hospital revenue is priced by counterparties who suspended cashless rather than concede. That single fact reorganises the whole strategic picture.
4. **Include the number that weakens your argument.** Max's occupancy is five points above Apollo's while carrying 13% more beds. On the operational job, Max is winning.
5. **A metric that blends variables cannot be fixed by adding a target to it.** The only repair is decomposition, and decomposition usually requires no one's permission — which is why it beat the clever proposal in §47.
6. **Design the guardrail before the feature when the feature can hurt someone.** Bundled payment's failure mode is refusing sick patients; CSR-90 exists before Episode Price does, and gates its launch.
7. **Check the registry.** Four consecutive case studies have found an NIC code that does not describe the business — a pattern worth more than any single instance.

---

## 60. PM Interview Questions

1. ARPOB rose 5% and PAT rose 3.48%. Which would you put on the board slide, and what would you say about the other?
2. Apollo discontinued ARPOB and Max still leads with it. Argue the case for Max's position as strongly as you can.
3. Decompose a blended revenue-per-unit metric into its components. Which component would you make the north star, and why not the others?
4. Your buyer sets your price and has previously withheld payment to prove it. Design the product response.
5. You propose bundled pricing. Name the harm it creates and the mechanic — not the principle — that prevents it.
6. Your own sensitivity analysis ranks your proposal last, behind a reporting change. What do you ship first?
7. A complication generates revenue under itemised billing. Is that an ethical problem, an incentive problem, or an accounting one — and what changes if you reclassify it?

---

## 61. References

**Primary**
1. Max Healthcare Institute Limited, Q1 FY27 results and investor presentation, 13 August 2026.
2. Max Healthcare Institute Limited, Q1 FY27 earnings call transcript, 14 August 2026.
3. Apollo Hospitals Enterprise Limited, Q1 FY27 results, 12 August 2026, and earnings call, 13 August 2026.
4. Apollo Hospitals Enterprise Limited, Q1 FY26 earnings call — announcement discontinuing ARPOB as a reported metric.
5. Max Healthcare Institute Limited, Information Memorandum dated 15 August 2020 (NSE archives) — incorporation history and corporate structure.
6. Ministry of Corporate Affairs registry — CIN L72200MH2001PLC322854.
7. Max Healthcare investor fact sheet, maxhealthcare.in — facility, bed and clinician counts.

**Secondary** (corroboration; flagged where single-sourced)
8. Business Standard — Apollo and Max Q1 FY27 comparison, 16 August 2026.
9. Medical Buyer — Apollo Q1 FY27 segment detail.
10. Investing.com, InvestyWise, ScanX — Max Q1 FY27 operational detail and Kalinga contribution.
11. ICICI Direct — historical ARPOB series, Q1 FY25 to Q2 FY26.
12. Business Standard — AHPI/Bajaj Allianz cashless suspension and withdrawal, August 2025.
13. Business Standard — AHPI/Star Health dispute and restoration, September–October 2025.
14. Business Standard — Niva Bupa suspension of cashless at Max Hospitals, September 2025.
15. IndiaMedToday, SMC Insurance — hospital–insurer tariff dispute context and medical inflation range.
16. Tracxn, TheCompanyCheck, ZaubaCorp — entity, NIC code and capital snapshots (Appendix A-3).

---

## 62. About the Author

Gaurav Singh — Product Manager. Day 67 of a 90-day public case-study series applying structured PM frameworks to real products, under a zero-fabrication standard: every figure is cited, labelled as an estimate, flagged as single-sourced, or recorded as not publicly disclosed.

---

## 63. License

Analysis and original text © 2026 Gaurav Singh, released for non-commercial use with attribution. All company figures belong to their sources and are cited in §61. No affiliation with Max Healthcare Institute Limited or Apollo Hospitals Enterprise Limited.

---

## 64. Self Review

**What is strong.** The thesis rests on a competitor's own published reasoning rather than on the author's opinion, which makes it checkable. The arithmetic reconstruction of ARPOB from revenue and occupied bed days is the cleanest single argument in the piece, because it shows the metric contains no price term at all. The stress rule comes from Max's own disclosed international share rather than an assumption. And the proposal loses to an initiative that was not proposed, asserted programmatically rather than claimed.

**What is weak, stated plainly.** The claim that mix drove ARPOB is an *inference from direction*, not a measurement. Max does not publish payer mix, case mix or length of stay, so this case study can prove ARPOB is capable of rising without a price change, and can show the mix moved in the right direction — but cannot quantify how much of the 5% was mix. The rival reading, that CGHS complex-specialty rates and the 6% insurance revision genuinely lifted prices this quarter, is given equal weight in ASSUMPTIONS Part 1 and would be settled instantly by the decomposition §47 recommends.

**What I could not establish.** Payer mix by revenue; case mix by specialty; average length of stay; the composition of the ₹143.29 Cr gap between network gross revenue and the revenue base implied by the reported margin; and whether Max's medical-education ROCE figure is a target or a modelled expectation.

**One thing I would do differently.** I found Apollo's discontinuation of ARPOB while researching the comparator, after the thesis was already drafted around the tariff dispute. It should have been the entry point — the strongest fact in the piece arrived third.

---

## 65. Appendix

### A. Source conflicts

| # | Conflict | Handling |
|---|---|---|
| A-1 | NIC code **722, "software publishing"**, for a hospital chain, traceable to the entity's origin as Infinitum Technologies Private Limited | Stated in §2 with the cause; CIN cited in full, never the name alone |
| A-2 | **Three revenue figures for one quarter**: network gross ₹2,982 Cr, revenue base implied by the reported 24.8% margin ₹2,838.71 Cr, consolidated revenue from operations ₹2,366.17 Cr | All three reported. Each used only on its own basis and never mixed within a calculation; the ₹143.29 Cr (4.81%) implied gross-to-net gap is flagged and load-bearing nowhere |
| A-3 | Authorised and paid-up capital, and FY25/FY26 revenue, differ across MCA aggregators and Wikipedia (₹8,373.45 Cr FY26 consolidated vs ₹9,065 Cr described as FY25) | 🟡 Marked as snapshots of different bases and dates; not used in any derivation |
| A-4 | Medical inflation of **7–8%** comes from 2025 dispute reporting, not a 2026 primary statistic | Vintage stated wherever used; treated as a range and used only for directional comparison against the 6% automatic revision |
| A-5 | Apollo's discontinuation of ARPOB is recorded in an earnings-call transcript rather than a filed statement | 🟡 Single-source class, but a direct management statement; quoted in substance, not verbatim |
| A-6 | Reported ARPOB growth of 5% vs 5.32% reconstructed from revenue and OBD growth | Both stated. The 0.32pp difference is consistent with rounding in the disclosed growth rates and does not affect the argument |

### B. Evidence grades

🟢 **High** — Max and Apollo quarterly results and presentations, MCA registry, NSE Information Memorandum, company fact sheet.
🟡 **Medium** — the 6% automatic insurance revision, medical inflation range, capital snapshots, Apollo's ARPOB discontinuation rationale.
🟠 **Low** — none relied upon.
🔴 **Conflicting** — A-2, the three revenue bases, handled as above.

### C. Author-constructed content

*Episode Price*, EPE/1k, CSR-90, the RICE inputs, the Phase 0 kill criteria and the §54 arms are the author's constructions, not Max disclosures or plans. See ASSUMPTIONS.md Part 3 for the full inventory.

### D. Asset status

| Asset | Status |
|---|---|
| README.md | Complete, 65 sections |
| ASSUMPTIONS.md | Complete, Parts 1–5 |
| verify.py | 108 checks, all passing — delivered, not committed |
| LinkedIn carousel + caption | Delivered, not committed |

---

*Day 67 of 90 · [← Day 66 — Star Health](../Day-66-Star-Health) · Day 68 →*
