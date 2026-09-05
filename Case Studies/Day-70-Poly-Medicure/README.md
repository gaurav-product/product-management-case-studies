# Day 70 — Poly Medicure: The Growth Was Bought and the Profit Was Not

> Poly Medicure reported consolidated revenue up 30.30% and consolidated profit down 8.39%. The company calls this its transformation from a consumables maker into a medical technology platform, built through acquisition. The parent company reports separately, and the two numbers sit one line apart in the same filing: **standalone PAT of ₹88.12 Cr against consolidated PAT of ₹85.27 Cr.** The subsidiaries — the entire acquired transformation — contributed **−₹2.85 Cr** on ₹94.28 Cr of revenue, a **−3.02%** net margin against the parent's **+20.44%**. And the mechanism is not what they sell: consolidated gross margin is *higher* than standalone at 73.4% against 71.5%, while consolidated EBITDA margin is *lower* at 24.1% against 28.0%. Gross-to-EBITDA conversion drops from 39.16% to 32.83%. Poly Medicure's whole advantage is an Indian cost base. It bought European products and imported the European cost base with them.

---

## 1. Cover

**Product:** Polymed — single-use medical devices; infusion therapy, critical care, renal, oncology
**Legal entity:** Poly Medicure Limited · **CIN:** L40300DL1995PLC066923
**Domain:** Healthtech — medical device manufacturing
**Period examined:** Q1 FY27 (quarter ended 30 June 2026), board approved 7 August 2026
**Written:** 5 September 2026
**Author:** Gaurav Singh · Day 70 of 90

---

## 2. Repository Metadata

| Field | Value |
|---|---|
| Legal entity | Poly Medicure Limited |
| CIN | L40300DL1995PLC066923 |
| Incorporated | 30 March 1995 |
| Registrar | RoC Delhi |
| Former name | Polymedicure Limited |
| Registered office | Property No. 232-B, 3rd Floor, Okhla Industrial Estate Phase III, New Delhi 110020 |
| Manufacturing | Ballabgarh and Faridabad, Haryana |
| Listings | BSE **531768** · NSE **POLYMED** |
| NIC code | **4030 — "Steam and hot water supply"** |
| Managing Director | Himanshu Baid (DIN 00014008) |
| Joint Managing Director | Rishi Baid (DIN 00048585) |
| Authorised / paid-up capital | ₹60.00 Cr / ₹50.68 Cr 🟡 |

India's industrial classification files a manufacturer of catheters and infusion sets under *steam and hot water supply*. **This is the seventh consecutive case study in this series whose NIC code does not describe the business** — after BookMyShow (99999), Atomberg (7290), Vodafone Idea (3210), Max Healthcare (722), Dr. Lal PathLabs (74899) and MedPlus (8511, "hospital activities"). Seven in a row, across seven unrelated sectors, is a finding about the register rather than about seven companies: **the NIC code embedded in a CIN is fixed at incorporation and effectively never revised**, so it records what a company was thought to be in the year it was registered, not what it does.

---

## 3. Badges

`Day 70/90` · `Healthtech` · `Medical devices` · `Listed (BSE/NSE)` · `Q1 FY27 primary` · `Standalone PAT exceeds consolidated PAT` · `114 programmatic checks, all passing` · `Zero fabricated figures`

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

Poly Medicure's board approved the June 2026 quarter on 7 August. Consolidated revenue from operations was **₹525.38 Cr, up 30.30%**. Consolidated profit after tax was **₹85.27 Cr, down 8.39%**. Consolidated EPS fell 7.6% to ₹8.5. The company presented this as evidence of "PolyMed 3.0" — a stated transformation from a consumables business into a diversified medical technology platform, targeting a doubling of revenue by 2030 through organic growth in high-complexity therapeutic areas plus acquisitions.

Several things in the quarter are genuinely strong and belong first. Standalone EBITDA margin of **28.0%** came in above the guided 25–27% range. Standalone gross margin was 71.5%. Six new products launched across infusion therapy and critical care. Cash stood at **₹854.7 Cr — 1.63× a full quarter's consolidated revenue** and 3.42× the standalone working capital debt. Domestic revenue grew 16.2%. This is a well-capitalised, profitable manufacturer with no long-term standalone debt.

The difficulty is what the consolidation contains. **Standalone PAT was ₹88.12 Cr; consolidated PAT was ₹85.27 Cr.** The parent alone earned more than the group. Subtracting gives the subsidiaries' contribution: **−₹2.85 Cr on ₹94.28 Cr of revenue — a net margin of −3.02%**, against the parent's **+20.44%**. Consolidation diluted net margin by **4.21 percentage points**.

Nor is the growth what it appears. Consolidated growth of 30.3% against organic growth of 12.4% means **17.90 points — 59.08% of the reported growth — came from acquisitions**, which contributed ₹72.3 Cr of revenue. Standalone revenue grew **12.25%**, and standalone PAT was **flat at +0.22%**. Strip the acquisitions and the underlying business grew its top line at a quarter of the headline rate and its bottom line not at all.

**The mechanism is the part worth a product manager's attention, because it is counter-intuitive.** Consolidated gross margin (73.4%) is *higher* than standalone (71.5%) — the acquired products carry better unit economics at the point of sale. But consolidated EBITDA margin (24.1%) is *lower* than standalone (28.0%). Gross-to-EBITDA conversion falls from **39.16% to 32.83%**, a gap of 6.33 points. The implied subsidiary EBITDA margin is **6.27%**, just **22.38%** of the parent's.

So the acquisitions did not bring worse products. They brought worse operating leverage. Poly Medicure's entire structural advantage is manufacturing high-quality devices at an Indian cost base and exporting to 100+ countries. Acquiring a European device maker buys the product and the cost base together, and it is the second one that shows up below the gross line.

Meanwhile the organic business is under real pressure: renal grew **3.8%** against Chinese price competition, Middle East exports fell **32%**, and employee costs rose **29%** — **2.37×** standalone revenue growth — on a 35% minimum wage increase in Haryana.

The proposal, *Licence-to-Make*, follows from that diagnosis. It is designed, costed, and then ranked last — behind fixing the entities already owned.

---

## 6. Product Overview

Poly Medicure designs and manufactures single-use medical devices: infusion therapy sets, IV cannulae, blood management and collection systems, catheters, anaesthesia and urology products, surgical drainage, and renal/dialysis consumables. Roughly 100 product families are sold into more than 100 countries, with manufacturing concentrated in Ballabgarh and Faridabad, Haryana.

The strategic direction is upward in complexity — from Class A/B consumables toward Class C/D devices including a drug-eluting stent — pursued through both internal R&D and acquisition. That upward move is the correct instinct, and it is precisely where the economics examined in this case study break.

---

## 7. Company Background

The company was incorporated on 30 March 1995 as Polymedicure Limited and remains promoter-led by the Baid family: Himanshu Baid as Managing Director, Rishi Baid as Joint Managing Director, with Jugal Kishore Baid on the board. It has grown for three decades on a single proposition — Indian manufacturing cost with export-grade quality — and reported FY25 revenue of ₹1,691.57 Cr.

The recent chapter is acquisitive. Foreign subsidiaries now include operations in Europe and Brazil, and the acquired entities contributed ₹72.3 Cr of revenue in the quarter examined. The company also participates in India's PLI scheme for renal products and frames itself within the National Medical Devices Policy 2023 ambition of a $50 Bn sector by 2030.

---

## 8. Product Timeline

| Date | Event |
|---|---|
| 30 Mar 1995 | Incorporated as Polymedicure Limited, RoC Delhi |
| FY25 | Revenue ₹1,691.57 Cr; nine-month export revenue +29% YoY |
| Feb 2025 | Regulatory approval received for drug-eluting stent |
| FY26–FY27 | European and Brazilian acquisitions integrated; "PolyMed 3.0" articulated |
| Q1 FY27 | Six new products launched in infusion therapy and critical care |
| 7 Aug 2026 | Board approves Q1 FY27 results at Jaipur; ESOP grant and allotment |
| 10 Aug 2026 | Earnings call: renal pricing pressure, Middle East disruption, tariff exposure |

---

## 9. Vision & Mission

"PolyMed 3.0" is stated as a doubling of revenue by 2030, achieved by moving into high-complexity therapeutic areas and by acquisition, transforming a consumables manufacturer into a medical technology platform. FY27 guidance is consolidated revenue of ₹2,300–2,400 Cr at a 23–25% EBITDA margin, with standalone revenue of ₹1,900–2,000 Cr at 25–27%.

The question this case study puts to that vision is not whether the destination is right — it is — but whether **acquisition is the instrument that gets there without destroying the advantage that funds the journey.** On one quarter's evidence, the acquired assets deliver 22.38% of the parent's EBITDA margin.

---

## 10. Problem Statement

**For Poly Medicure:** the company's competitive advantage is an Indian manufacturing cost base. Buying a foreign device maker acquires its products *and* its cost structure, and the consolidated accounts blend the two into figures where neither can be judged separately.

**For the customer — a hospital procurement officer or distributor:** Poly Medicure's consumables compete largely on price, and in renal that contest is now being lost to Chinese imports at 3.8% growth. Moving up-stack requires clinical evidence and brand trust that a low-cost manufacturer does not automatically possess.

**The intersection:** the route up the value chain that preserves the cost advantage is to make higher-complexity products *in India*. **Acquisition achieves the product move and forfeits the cost move**, which is exactly what a −3.02% subsidiary net margin against a +20.44% parent margin describes.

---

## 11. Market Research

The Indian medical devices market is import-dependent in high-complexity categories and increasingly self-sufficient in consumables, where Indian manufacturers have become globally cost-competitive. Poly Medicure positions itself as India's second-largest medical devices player and largest exporter of medical consumables.

Two structural forces bound the analysis. **Chinese competition is compressing price in commoditised categories** — visible directly in renal at 3.8% growth with management citing pricing pressure and a deliberate decision to hold back volume. And **the policy environment favours domestic high-complexity manufacture**, through the PLI scheme and the National Medical Devices Policy, which is what makes the make-versus-buy question in §50 a live strategic choice rather than a theoretical one.

---

## 12. Industry Analysis

Medical devices split into two economically different businesses that often sit inside one company. Consumables are a manufacturing business: high volume, price-competed, won on cost and scale. High-complexity devices are a **regulatory and evidence business**: won on clinical data, approvals, and surgeon familiarity, where cost is a minor input to the purchase decision.

Poly Medicure is excellent at the first and is buying its way into the second. The industry logic for that is sound — acquiring an approved, evidenced product is far faster than generating one — but it carries a specific cost that the Q1 numbers make visible. **You cannot acquire a European product without acquiring the European organisation that makes and sells it**, and that organisation's overhead is what turns a 73.4% gross margin into a 24.1% EBITDA margin.

---

## 13. TAM / SAM / SOM

*Framework note: run in restricted form. No primary-sourced Indian medical device market size was located that is not a vendor or policy estimate, so this is sized from Poly Medicure's own disclosed revenue and guidance, in annualised rupees.*

| Layer | Definition | Size | Basis |
|---|---|---|---|
| TAM | FY27 consolidated revenue guidance, midpoint | **₹2,350.00 Cr** | Company guidance 🟢 |
| SAM | Q1 consolidated annualised run rate | **₹2,101.50 Cr** | ₹525.38 Cr × 4, derived |
| SOM | Standalone annualised run rate — the profitable business | **₹1,724.40 Cr** | ₹431.10 Cr × 4, derived |
| *The gap* | Acquired-entity annualised revenue | **₹377.10 Cr** | Derived, D9a — at a −3.02% net margin |

The run rate sits at **89.43%** of the guidance midpoint and **₹198.50 Cr below** the bottom of the range, so the guidance implies acceleration through the year — reaching the low end requires the remaining three quarters to average **12.59% above** Q1's revenue.

---

## 14. Competitor Analysis

*Framework note: the comparison here is **internal — parent against subsidiaries** — rather than against a listed peer, and that is a deliberate choice with a reason. Poly Medicure's Indian listed peers in devices are not comparable in mix; the global majors it now competes with in high-complexity categories are an order of magnitude larger and do not disclose India-relevant segment economics. But the company files standalone **and** consolidated accounts, which means the acquired businesses can be isolated by subtraction with no estimation at all. That is a cleaner comparator than any peer would be.*

| Metric, Q1 FY27 | Parent (standalone) | Subsidiaries (derived) | Consolidated |
|---|---|---|---|
| Revenue | ₹431.10 Cr | **₹94.28 Cr** | ₹525.38 Cr |
| Revenue growth | +12.25% | — | +30.30% |
| PAT | **₹88.12 Cr** | **−₹2.85 Cr** | ₹85.27 Cr |
| Net margin | **+20.44%** | **−3.02%** | +16.23% |
| Gross margin | 71.5% | — | **73.4%** |
| EBITDA margin | **28.0%** | **6.27%** (derived) | 24.1% |
| Gross-to-EBITDA conversion | **39.16%** | — | 32.83% |

Three readings. **The parent out-earned the group**: standalone PAT is **103.34%** of consolidated PAT, so the acquired portfolio is a net drag on profit while supplying 17.95% of revenue.

Second, and the finding that reframes it: **the acquisitions have better gross margins and worse operating margins.** Consolidated gross margin runs 1.90 points *above* standalone while EBITDA margin runs 3.90 points *below*. The products are good. The cost of running the businesses that own them is not.

Third, the growth arithmetic: **59.08% of reported growth was inorganic.** Organic growth was 12.4%; the acquisitions supplied 17.90 points of the 30.3%.

And the number that cuts against this case study's own argument, included because it should be: **these are integration-mode assets in their first year of ownership.** First-year consolidation routinely carries transaction costs, purchase-price allocation effects and duplicated overhead that normalise. A −3.02% net margin on newly acquired entities is not evidence of a bad acquisition; it is evidence that the acquisition is recent. That reading is given equal weight in ASSUMPTIONS Part 1, and only a multi-quarter series can separate the two.

---

## 15. SWOT

| | |
|---|---|
| **Strengths** — standalone EBITDA margin of 28.0%, above guidance; 20.44% standalone net margin; cash of ₹854.7 Cr at 1.63× quarterly revenue; no long-term standalone debt; exports to 100+ countries; six new products in one quarter; drug-eluting stent approved | **Weaknesses** — subsidiaries at −3.02% net margin and 22.38% of the parent's EBITDA margin; 59.08% of growth inorganic; standalone PAT flat at +0.22%; renal growth 3.8%; employee costs +29%, 2.37× revenue growth; working capital cycle at 140 days |
| **Opportunities** — PLI scheme and National Medical Devices Policy favour domestic high-complexity manufacture; consolidated gross margin of 73.4% shows acquired products carry real pricing power; integration cost is addressable without any external party's agreement | **Threats** — Chinese price competition in renal and other commoditised lines; Middle East exports down 32% on the West Asia crisis; US tariffs at 10% on a small but growing exposure; guided gross margin normalisation to 68–69% implies Q1's 71.5% is not repeatable |

---

## 16. Porter's Five Forces — run twice

*Framework note: run as a double pass on the two businesses now inside one filing — the **Indian-manufactured consumables** business that generates the profit, and the **acquired high-complexity** business that generates the growth. The seam is chosen because the forces genuinely invert across it, because the company reports both separately enough to isolate them, and because the strategic question in §50 is which of the two the other should be made to resemble.*

| Force | INDIAN CONSUMABLES (the parent) | ACQUIRED HIGH-COMPLEXITY (the subsidiaries) |
|---|---|---|
| **Buyer power** | **High.** Hospitals and distributors buy on price; Chinese entrants set the ceiling, visible in renal at 3.8% growth | **Low.** Clinical evidence, approvals and surgeon familiarity make substitution slow — which is why gross margin is 73.4% |
| **Rivalry** | On cost per unit, where an Indian base is a structural weapon | On evidence and regulatory position, where Poly Medicure is the challenger, not the incumbent |
| **Substitutes** | Abundant and near-identical; the product is a specification | Scarce; switching a device carries clinical risk |
| **New entrants** | **Weakly barred** — this is the door Chinese manufacturers came through | **Strongly barred** by approvals, trial data and capital |
| **Supplier power** | Moderate; resin and polymer inputs, with scale leverage | **The binding constraint is labour and overhead**, not inputs — a European cost base the parent cannot re-price |

The inversion is the finding, and it is unusually symmetrical. **The parent has a cost advantage and no pricing power; the subsidiaries have pricing power and no cost advantage.** Each is strong exactly where the other is weak. Consolidation reports their average, which describes neither: a 73.4% gross margin that the parent cannot achieve, on a 24.1% EBITDA margin the parent comfortably beats. The strategic prize is not the average — it is **combining the two halves**, which is what §50 attempts and §47 then declines to prioritise.
---

## 17. Business Model Canvas

| Block | Poly Medicure |
|---|---|
| Value proposition | Export-grade single-use medical devices at an Indian cost base |
| Customer segments | Hospitals, distributors, government tenders, OEM partners, 100+ export markets |
| Channels | Direct sales, distributors, tenders, foreign subsidiaries |
| Revenue streams | Infusion therapy, critical care, renal, blood management, surgery, oncology |
| Key resources | Ballabgarh and Faridabad plants, ~100 product families, regulatory approvals, ₹854.7 Cr cash |
| Key activities | Manufacturing, R&D, regulatory registration, export logistics, **acquisition integration** |
| Key partners | Distributors, PLI scheme, acquired European and Brazilian entities |
| Cost structure | Materials, employee cost (+29%), plant overhead, **acquired-entity overhead** |
| **The advantage** | **Indian manufacturing cost — which acquisitions do not inherit** |

The last row is the case study compressed. Every other block scales with acquisition; that one does not, and it is the only block that explains a 20.44% net margin.

---

## 18. Revenue Model

Revenue is per-unit device sales across roughly 100 product families, split domestic (+16.2%) and international (+36.7% consolidated, +10% standalone). The gap between those two international figures is itself informative: **consolidated international growth is 3.67× standalone international growth**, because the acquired entities are almost entirely export-market businesses.

The model's economics are set by conversion, not by price. The parent converts **39.16%** of gross margin into EBITDA; the group converts **32.83%**. On the derived subsidiary figures the acquired businesses convert into an EBITDA margin of just **6.27%** — **22.38%** of the parent's. A device business can have excellent gross margins and still not be worth owning if the organisation around it consumes the difference.

---

## 19. Target Users

The buyer is institutional: hospital procurement, distributors, and government tenders, across India and 100+ export markets. In consumables the decision is dominated by price and specification compliance. In high-complexity devices it shifts to the clinician, where evidence and familiarity dominate.

The user this case study is concerned with is the one Poly Medicure is trying to reach and cannot yet reach on its own terms: **the clinician choosing a Class C/D device**, for whom an Indian cost base is not a reason to switch and published clinical outcomes would be.

---

## 20. Personas

**A hospital procurement officer, tier-2 India.** Buys IV sets and cannulae on rate contract. Compares Poly Medicure against Chinese imports on landed price. This is the buyer whose behaviour produced 3.8% renal growth.

**An interventional cardiologist.** Decides which stent to implant. Price is not his variable; trial data, registry outcomes and familiarity are. Poly Medicure has an approved drug-eluting stent and, so far as disclosure shows, no published outcomes registry.

**A plant manager at an acquired European subsidiary.** Runs a facility whose cost base is denominated in euros and set by local labour law. Nothing the parent does in Haryana reduces his overhead — which is the whole of §14's finding, stated as a person.

---

## 21. Jobs To Be Done

*Framework note: JTBD is used because the parent and the subsidiaries are hired for genuinely different jobs, and the acquisition strategy assumes one organisation can do both.*

| Job | Who | Current solution | Adequacy |
|---|---|---|---|
| "Supply a compliant consumable at the lowest landed cost" | Procurement | Indian manufacturing at 28.0% EBITDA margin | **Excellent** — this is the company's core competence |
| "Give me a device I can defend clinically" | Clinician | Acquired high-complexity portfolio | Served, at a 6.27% EBITDA margin |
| "Move up the value chain without losing the cost advantage" | Poly Medicure | **Acquisition** | **Failing on the evidence of one quarter** |
| "Reduce dependence on price-competed categories" | Poly Medicure | New product launches, PLI participation | Working slowly — six launches this quarter |

Row three is the strategic job, and acquisition is the wrong tool for it in a specific and correctable way: it delivers the product and forfeits the cost base. Row four is the same job attempted organically, and it is slower but does not carry that defect.

---

## 22. User Journey

| Stage | Consumables | High-complexity |
|---|---|---|
| Specification | Tender or rate contract defines it | Clinician preference defines it |
| Evaluation | Landed price, compliance, supply reliability | Trial data, registry outcomes, training |
| Decision | Procurement | Clinician, with procurement consenting |
| Switching cost | Near zero | High, and clinical |
| Poly Medicure's position | Structurally advantaged | Structurally a challenger |

The two columns are the same company to an investor and entirely different companies to a customer. Nothing in the reported financials distinguishes them, which is why the derived split in §14 has to be constructed by subtraction.

---

## 23. User Flow

For consumables the flow is: tender issued → specification matched → price compared → contract awarded → repeat supply. Poly Medicure wins on the third step.

For high-complexity devices the flow is: clinical need → evidence reviewed → device trialled → surgeon adopts → hospital adds to formulary. Poly Medicure currently buys its way to step four by acquiring companies that already completed steps two and three. **The proposal in §50 is an attempt to reach step four while keeping manufacturing in India.**

---

## 24. Information Architecture

Disclosure architecture is what matters here, and it is better than most. Poly Medicure files standalone and consolidated accounts, reports both gross and EBITDA margins on both bases, and states organic versus total growth and the rupee contribution of acquisitions. That combination is exactly what allows this analysis to isolate the subsidiaries without estimating anything.

What is missing is any **named, per-acquisition** reporting: which entity, at what margin, on what integration timetable. The blended subsidiary figure derived in §14 is the only view available from outside, and it aggregates assets acquired at different times in different geographies.

---

## 25. UX Audit

Not a consumer product; the equivalent audit is the clinical-user experience of the devices themselves, which is not publicly assessable and is not attempted here.

The one observation that matters commercially: in high-complexity devices **the "interface" is the evidence package** — the trial data, the instructions for use, the training programme, the registry. That is the surface on which the acquired businesses compete and the parent does not yet, and it is the asset §50 proposes building.

---

## 26. UI Audit

Not applicable in the usual sense, and worth stating plainly rather than padding: this is a business-to-business manufacturer whose products are physical consumables.

The audit that would matter — device usability, connector standardisation, packaging clarity in low-resource settings — requires access this analysis does not have and is recorded as not assessed rather than guessed at.

---

## 27. Accessibility

The genuine access contribution is price. A company manufacturing infusion sets and dialysis consumables at an Indian cost base and exporting to 100+ countries lowers the cost of care in markets that cannot afford Western device pricing, and that is a real and under-credited public good.

The tension is that the same cost advantage is what Chinese competitors are now applying against Poly Medicure in renal, at 3.8% growth. Access-through-price is a position that erodes from below, which is precisely why moving up-stack is the right strategy and why the *route* up matters so much.

---

## 28. Feature Breakdown

| Area | Current state |
|---|---|
| Product families | ~100, across infusion therapy, critical care, renal, blood management, surgery, urology |
| New launches | 6 in Q1 FY27, in infusion therapy and critical care |
| High-complexity | Drug-eluting stent approved; Class C/D expansion stated |
| Geography | 100+ countries; foreign subsidiaries in Europe and Brazil |
| Manufacturing | Ballabgarh and Faridabad, Haryana |
| Policy participation | PLI scheme for renal products |
| Acquisitions | Contributed ₹72.3 Cr revenue, **−₹2.85 Cr PAT** in the quarter |
| **Per-entity acquisition reporting** | **Not disclosed** |
| **Published clinical outcomes registry** | **Not disclosed** |
| **Licensed-design manufacturing** | **Does not exist** |

The three absences at the bottom are the subject of §47 and §50, and each is verifiable from the disclosures rather than assumed: nothing in the results, the presentation or the earnings-call coverage reports acquisition-level economics, an outcomes registry, or an in-licensing arrangement.

---

## 29. AI Capabilities

No material AI product is disclosed and none is proposed. Applying a model to this problem would be decoration; the finding is an operating-cost and make-versus-buy question.

The one adjacent observation: a manufacturer running 100 product families across 100+ markets holds substantial data on complaint rates, field actions and lot performance. That is the raw material of the outcomes evidence the high-complexity strategy needs, and it is currently a compliance artefact rather than a commercial asset.

---

## 30. Product Metrics

| Metric | Q1 FY27 | Note |
|---|---|---|
| Consolidated revenue | ₹525.38 Cr | **+30.30%** |
| Standalone revenue | ₹431.10 Cr | **+12.25%** |
| Organic growth | 12.4% | **59.08% of growth was inorganic** |
| Acquisition revenue | ₹72.3 Cr | 13.76% of consolidated revenue |
| Consolidated PAT | ₹85.27 Cr | **−8.39%** |
| Standalone PAT | **₹88.12 Cr** | **+0.22% — and above consolidated PAT** |
| Subsidiary PAT (derived) | **−₹2.85 Cr** | −3.02% net margin |
| Gross margin | 71.5% standalone / **73.4% consolidated** | Consolidated is **higher** |
| EBITDA margin | **28.0% standalone** / 24.1% consolidated | Consolidated is **lower** |
| Gross-to-EBITDA conversion | 39.16% / 32.83% | A 6.33-point gap |
| Cash | ₹854.7 Cr | 1.63× quarterly revenue |
| Working capital cycle | ~140 days | 38.36% of a year |

The two rows in bold are the whole analysis. A group in which **standalone PAT exceeds consolidated PAT** is a group whose subsidiaries destroyed profit in the period, and it is visible by subtraction in a single filing.

---

## 31. North Star Metric

Poly Medicure's implied north star is consolidated revenue growth, and this quarter demonstrates the failure: it rose 30.30% while profit fell 8.39%, because the metric cannot distinguish revenue that was built from revenue that was bought.

**Proposed North Star — LMR/100: Licence-Manufactured Revenue per ₹100 of high-complexity revenue.**

Revenue counts in the numerator only if **all four** hold:
1. the design is held under licence, not through acquisition of the owning entity;
2. the product is manufactured in a Poly Medicure facility in India;
3. gross margin on the line is at or above the standalone gross margin;
4. royalty obligations are fully paid and current.

**The denominator is the design choice.** It is *high-complexity revenue* — so acquiring a company to enter a new therapeutic area **lowers** the metric, while licensing a design into an Indian plant raises it. Poly Medicure cannot improve LMR/100 by doing more of the thing this case study identifies as margin-destructive. Condition 3 prevents the metric being gamed by licensing low-value designs.

**Guardrail — QDR-90: Quality Deviation Rate at the 90th percentile of licensed-line volume.** In the decile of licensed lines running the highest volume, the rate of quality deviations, complaints and field safety actions per million units, measured against the licensor's own pre-transfer baseline and reported **by line, never in aggregate**. Owned by a quality function with no revenue or transfer target. A breach automatically suspends manufacture on that line.

This guardrail is not decoration. Transferring production of a Class C/D device to a lower-cost facility is exactly the move that, done badly, harms patients — and the failure would be invisible in any financial metric until a field action.

---

## 32. Product Analytics

The analysis that would settle this case study is a per-acquisition margin bridge: for each acquired entity, revenue, EBITDA and net contribution against the price paid and the integration plan. Poly Medicure holds all of it; none is published.

The absence of per-entity reporting is what forces the derived, blended subsidiary figure used throughout §14 and §30. That figure is arithmetically exact but strategically coarse — it cannot tell a well-performing acquisition from a poor one, and §47 ranks fixing that first for exactly that reason.

---

## 33. AARRR

*Framework note: applied to the acquisition programme rather than to customers, because that is the funnel that decided the quarter.*

| Stage | Reading |
|---|---|
| Acquisition | Working — ₹72.3 Cr of revenue added, 13.76% of consolidated |
| Activation | **Failing** — acquired entities at a 6.27% EBITDA margin, 22.38% of the parent's |
| Retention | Not assessable; no per-entity disclosure |
| Revenue | +30.30% consolidated, of which 59.08% inorganic |
| Referral | Not applicable |

The funnel is strong at intake and weak at conversion, which is the same shape as a company that is good at buying and has not yet proved it is good at owning. That is a normal first-year position, and it is why §55's first row tracks it quarter by quarter rather than declaring it now.

---

## 34. HEART

| Dimension | Poly Medicure |
|---|---|
| Happiness | Not disclosed; no customer satisfaction metric published |
| Engagement | Not applicable to a consumables manufacturer |
| Adoption | Six new products launched; no adoption or attach data |
| Retention | Not disclosed; no repeat-order or contract-renewal metric |
| Task success | **Not defined** — no published clinical outcome or complaint-rate data |

Four blank rows, and the last one is the strategically expensive absence. A company moving into devices where clinicians decide has no published measure of whether its devices perform, which is the asset §50 argues it needs.

---

## 35. Growth Strategy

The stated strategy is PolyMed 3.0: double revenue by 2030 through organic growth in high-complexity areas plus M&A, with FY27 guidance of ₹2,300–2,400 Cr consolidated. The Q1 run rate annualises to **₹2,101.50 Cr — 89.43% of the guidance midpoint** and ₹198.50 Cr below the bottom of the range, so hitting the low end requires the remaining three quarters to average **12.59% above** Q1 revenue.

**Checking whether the proposal already exists, from the company's own disclosures.** Nothing in the Q1 FY27 results, investor presentation or earnings-call coverage describes an in-licensing arrangement, a design-transfer programme, per-acquisition margin reporting, or a published outcomes registry. The high-complexity route described is acquisition plus internal R&D. So the instrument in §50 does not exist today.

**One further disclosure worth recording.** Management guided that standalone gross margin will normalise to **68–69%**, against the 71.5% reported. That is the company telling investors that this quarter's best number is **2.50 to 3.50 points above** its sustainable level — a candid disclosure that most would leave unsaid, and one that makes the margin analysis in §14 more, not less, credible.

---

## 36. Growth Loops

The intended loop is: cash → acquisition → higher-complexity revenue → higher margin → more cash. It is functioning on the first two arrows and inverted on the third: the acquired revenue arrives at a **6.27%** EBITDA margin against the parent's 28.0%, so each turn currently dilutes the very margin the loop is supposed to raise.

There is a second loop the company has been running successfully for three decades and should not be allowed to weaken: **Indian cost base → competitive export price → volume → scale economics → lower cost base.** The renal line shows what happens when it is attacked from below — 3.8% growth against Chinese pricing. Capital spent acquiring foreign overhead is capital not spent defending this loop, and it is the trade-off the case study asks the company to make explicit.

---

## 37. Network Effects

Medical device manufacturing has no direct network effects. What it has is a **regulatory and evidence flywheel**: an approval in one market shortens approval elsewhere, and clinical usage generates data that supports the next approval. That flywheel is real, cumulative, and the actual reason high-complexity devices earn 73.4% gross margins.

Poly Medicure bought entry to that flywheel rather than building it. The distinction that matters strategically is that **the flywheel is transferable and the cost base is not** — a licensed design carries the approvals and the evidence with it, while an acquired company carries the approvals, the evidence *and* the overhead. That asymmetry is the entire argument for §50.
---

## 38. Product Strategy

The destination is right and should be said plainly: a consumables manufacturer facing Chinese price competition in its commoditised lines *must* move up the complexity curve, and Poly Medicure has the balance sheet to do it — ₹854.7 Cr of cash, no long-term standalone debt, and a 28.0% EBITDA margin funding the journey.

The strategic gap is the instrument. **Acquisition transfers the product and the cost base together, and only one of them is wanted.** The parent's advantage is an Indian cost structure; the acquired entities' advantage is approvals, evidence and clinical position. A strategy that combines them would put acquired designs into Indian plants. A strategy that merely consolidates them reports a blended margin that describes neither business — which is what the Q1 filing does.

---

## 39. Monetization

Poly Medicure monetises per unit shipped, and its two halves monetise on opposite variables. The parent earns because its cost per unit is low: a 71.5% gross margin converting at 39.16% into a 28.0% EBITDA margin. The subsidiaries earn because their price per unit is high: a consolidated gross margin of 73.4% converting at only 32.83%.

The monetisation gap is the conversion rate, not the price. **The acquired businesses capture more value per sale and retain less of it**, and no pricing action fixes that. Only cost structure does — which is why §47's top-ranked initiative is an integration cost programme rather than anything commercial.

---

## 40. Trust & Safety

*Placed before §50 deliberately, because the proposal moves manufacture of high-complexity medical devices to a different facility, and that is a patient-safety decision before it is a margin decision.*

**Transferred manufacture is where device quality fails.** A Class C/D device — a stent, a central venous catheter — has process parameters validated at a specific site with specific equipment and operators. Moving production is a well-documented source of field actions, and the harm lands on a patient in an operating theatre, not on a P&L. The mechanic: **QDR-90 measures deviations, complaints and field safety actions per million units against the licensor's own pre-transfer baseline, by line**, owned by quality with no revenue or transfer target, with automatic suspension of the line on breach. No line transfers without a baseline established first.

**Regulatory validity is not automatically portable.** A CE mark or FDA clearance attaches to a manufacturing site and process, not only to a design. Transferring production can invalidate the approval that made the product saleable. The mechanic: §53's Phase 0 tests transferability per design *before* any commercial term is agreed, and K1 is written to kill the proposal if approvals do not travel.

**Cost pressure on a quality function.** If the point of the transfer is a lower cost base, the quality organisation at the receiving site is under structural pressure to pass lines through. The mechanic: quality sign-off sits with a function reporting outside the manufacturing P&L, and §48 permanently excludes transfer-volume targets for anyone with quality authority.

**The incentive that must be excluded, stated plainly.** If LMR/100 is targeted without QDR-90 gating it, the fastest way to raise the metric is to transfer lines faster than they can be validated. §48 places transfer targets without a quality gate permanently out of scope, and §53 makes the QDR-90 baseline a precondition of launch rather than a subsequent report.

---

## 41. Technical Architecture

The relevant architecture is manufacturing and regulatory: validated production lines at Ballabgarh and Faridabad, a quality management system, design history files, and market-by-market registrations across 100+ countries.

What a licensing model requires that acquisition does not is a **design-transfer capability** — the ability to take a licensor's design history file and process parameters and reproduce them under a different quality system. Poly Medicure has done this for its own designs across two plants and 100 product families; doing it for a third party's Class C/D device is a materially harder version of a thing it already does.

---

## 42. Data Flow

Under acquisition the flow is corporate: purchase → consolidation → blended reporting. Under licensing it is technical: licensor design file → transfer protocol → process validation → regulatory variation → production → royalty settlement.

The critical constraint is directional and specific: **quality data must flow from the line to the quality function and to the licensor, never through the P&L owner.** Enforced by system access rather than policy, so that no one accountable for transfer volume can see, edit or delay a deviation record.

---

## 43. API Ecosystem

Not a software business; the equivalent interfaces are regulatory and contractual — registration dossiers, distributor agreements, tender portals, and now licence agreements.

The asymmetry worth naming: Poly Medicure has three decades of experience with the *outbound* interfaces — registering its own designs in 100+ markets — and no disclosed experience with the *inbound* one, taking someone else's design under licence. That is the capability gap the proposal creates, and K2 in §53 is built to test it.

---

## 44. Privacy & Security

Limited direct exposure: this is a device manufacturer, not a data business, and no patient data flows through the products examined.

The genuine sensitivity is **licensor intellectual property**. A design-transfer programme puts a third party's design history file inside Poly Medicure's plants. The design position is that licensed design files are segregated from internal R&D by access control and audited, because the fastest way to end a licensing strategy is a licensor concluding their design leaked into a competing own-brand product.

---

## 45. Pain Points

| # | Pain point | Evidence |
|---|---|---|
| P1 | Standalone PAT exceeds consolidated PAT by ₹2.85 Cr | Exchange filing, derived by subtraction 🟢 |
| P2 | Subsidiary net margin −3.02% against parent +20.44% | Derived, D2c, D2d 🟢 |
| P3 | Subsidiary EBITDA margin 22.38% of the parent's | Derived, D4j 🟢 |
| P4 | 59.08% of reported growth was inorganic | Derived from disclosed organic growth 🟢 |
| P5 | Standalone PAT flat at +0.22% | Exchange filing 🟢 |
| P6 | Renal growth 3.8% under Chinese price pressure | Earnings call 🟡 |
| P7 | Employee costs +29%, 2.37× standalone revenue growth | Earnings call 🟡 |
| P8 | Middle East exports −32% | Earnings call 🟡 |
| P9 | Run rate at 89.43% of guidance midpoint | Derived, D6c 🟢 |
| P10 | No per-acquisition economics disclosed | Absence across all Q1 FY27 disclosures 🟢 |
| P11 | Guided gross margin normalisation to 68–69% | Earnings call 🟡 |

---

## 46. Opportunity Mapping

| Opportunity | Annualised revenue addressed | Requires |
|---|---|---|
| Integration opex programme at acquired entities | ₹377.10 Cr | Nobody outside the group |
| Working capital reduction from 140 days | ₹2,101.50 Cr | Nobody outside the group |
| High-complexity product expansion | ₹1,724.40 Cr | Clinicians and hospitals to adopt |
| Licence-to-Make | ₹1,724.40 Cr | Licensors to agree, regulators to permit |
| Further acquisitions | Not sized | Capital, and a repeat of the Q1 economics |

The right-hand column decides §47 once more, and the top row is unusually attractive: the acquired entities are already owned, their overhead is already inside the group, and reducing it requires no counterparty's consent at all.

---

## 47. RICE

*Framework note: run with a sensitivity pass. Initiatives requiring a licensor, clinician or hospital to act are multiplied by a stress rule; those delivering value inside entities Poly Medicure already owns are exempt.*

**The stress rule comes from the company's own arithmetic.** The implied subsidiary EBITDA margin is **6.27%** against the parent's **28.0%** — the acquired assets reproduce **22.38%** of the parent's operating economics. That is Poly Medicure's own demonstrated evidence of how much of its economics an externally-sourced asset actually delivers, and it is the right discount for any initiative depending on an outside party performing to plan. Two alternatives were computed and not used: the subsidiary **net** margin is negative and therefore unusable as a multiplier, and the organic share of growth at **40.92%** would have been far more generous.

| Initiative | Reach (₹ Cr p.a.) | Impact | Conf. | Effort | **Base** | **Stressed** |
|---|---|---|---|---|---|---|
| Integration opex programme | 377.10 | 2.50 | 0.85 | 20 | **40.07** | **40.07** (exempt) |
| High-complexity product expansion | 1,724.40 | 2.00 | 0.55 | 30 | **63.23** | **14.15** |
| **Licence-to-Make (PROPOSED)** | **1,724.40** | **1.00** | **0.35** | **36** | **16.76** | **3.75** |
| Working capital reduction | 2,101.50 | 0.25 | 0.80 | 30 | **14.01** | **14.01** (exempt) |

**Licence-to-Make falls from 3rd of 4 at baseline to 4th and last under stress**, behind an initiative this case study did not propose. The winner beats it by **10.68×**. `verify.py` asserts programmatically both that the proposal finishes last and that it is the **weakest stressed initiative at baseline** — the only configuration in which the demotion is genuine rather than arranged.

The answer is uncomfortable for a strategy piece and correct. Before Poly Medicure designs a new route into high-complexity devices, it should **fix the economics of the high-complexity businesses it already bought.** Those entities exist, their overhead is already consolidated, and a 6.27% EBITDA margin against a 28.0% parent leaves a great deal of room. No licensor's signature is required and no regulator's approval — which is precisely why it survives the stress test and the clever instrument does not.

---

## 48. MoSCoW

| | |
|---|---|
| **Must** | Per-acquisition economics reported internally — revenue, EBITDA, integration cost against plan; QDR-90 baselines established before any transfer; quality sign-off held outside the manufacturing P&L |
| **Should** | Design-transfer capability assessment per licensed design; licence terms with royalty tied to transferred volume; segregated access to licensor design files |
| **Could** | Published clinical outcomes registry for own high-complexity devices; extension of licensing to renal to answer Chinese pricing |
| **Won't** | Any transfer-volume target for a person with quality authority; any line transfer without an established QDR-90 baseline; any commercial term agreed before regulatory transferability is confirmed; any use of licensed design files in own-brand development |

The "Won't" row closes the four routes by which a margin instrument becomes the patient-safety failure §40 describes.

---

## 49. Kano

| Feature | Category | Note |
|---|---|---|
| Compliant, reliable consumable at low landed cost | Basic | Absence loses the tender outright |
| Breadth of product family | Performance | ~100 families is a genuine competitive asset |
| Low price in commoditised lines | **Performance → Reverse** | Below a point, price signals doubt about quality — and it is the ground Chinese entrants now own |
| Published clinical outcomes on own devices | **Attractive**, and unbuilt | Nobody in the Indian device sector offers this as standard |
| High-complexity device made in India at Indian cost | **Attractive** | The combination that neither half of the company currently delivers |

Row three is the trap the renal line is in. Competing harder on price in a category where a lower-cost entrant has arrived does not win the category; it accelerates the erosion of the margin that funds everything else.

---

## 50. Feature Proposal — *Licence-to-Make*

**What it is.** Instead of acquiring companies that own high-complexity designs, Poly Medicure licenses the designs and manufactures them in its own Indian facilities. The licensor receives a royalty on units produced and retains ownership of the design and its approvals; Poly Medicure supplies the manufacturing, the cost base and the export distribution it already has in 100+ markets. Regulatory transferability is confirmed per design before any commercial term is agreed.

**Why this shape.** §14 shows the acquired portfolio has better gross margins and worse operating margins — good products inside expensive organisations. §37 explains why that is correctable: **the regulatory and evidence flywheel is transferable and the cost base is not.** A licence carries the approvals and the clinical evidence without carrying the European overhead. It is the only instrument available that takes the half of an acquisition Poly Medicure wants and leaves the half that produced a −3.02% net margin.

**What it is not.** It is not a distribution agreement — the point is manufacture in India, not reselling someone else's output. It is not a route to cheaper devices at the expense of validation: no line moves without a QDR-90 baseline and confirmed regulatory transferability. It is not a replacement for the integration work §47 ranks first.

**North Star:** LMR/100, per §31, with high-complexity revenue as the denominator.
**Guardrail:** QDR-90, per §31, by line, owned outside the manufacturing P&L.

---

## 51. PRD

**Problem.** Poly Medicure's advantage is an Indian cost base. Its route into high-complexity devices is acquisition, which imports a foreign cost base along with the product — producing a −3.02% subsidiary net margin against a +20.44% parent margin, and a group in which standalone profit exceeds consolidated profit.

**Goals.** Establish a repeatable design-in-licensing and transfer capability; move a measurable share of high-complexity revenue onto Indian-manufactured licensed designs; and make per-entity economics visible so make-versus-buy-versus-licence is decided on evidence.

**Non-goals.** Reducing device quality or validation rigour. Replacing internal R&D. Exiting acquisitions already made — §47 explicitly ranks fixing those first.

**User stories.**
- As a licensor, I reach export markets I cannot serve economically, without giving up my design or my approvals.
- As a clinician, the device I implant is the design I already trust, manufactured to the same validated process.
- As Poly Medicure's board, I can compare the margin of a licensed line against an acquired entity against an organic product, on the same basis.

**Functional requirements.** Regulatory transferability assessment per design; design-transfer protocol and process validation; QDR-90 instrumentation per line against the licensor's pre-transfer baseline; royalty computation on verified production volume; segregated access control on licensor design files; per-entity and per-line margin reporting.

**Non-functional.** Quality authority held outside the manufacturing P&L; deviation records inaccessible to transfer-volume owners; licensed design files auditable by the licensor.

**Acceptance criteria.** Revenue counts toward LMR/100 only if all four §31 conditions hold. No line enters production without a QDR-90 baseline and confirmed regulatory transferability.

**Success metrics.** LMR/100 at the R1 threshold in §54; QDR-90 no worse than the licensor's baseline on any line measured separately; licensed-line gross margin at or above standalone gross margin.

---

## 52. Wireframes

```
PER-ACQUISITION MARGIN BRIDGE   (the exempt initiative, built first)
+--------------------------------------------------------------+
|  Entity            Rev     EBITDA%   Net%    Integration cost |
|  ----------------------------------------------------------  |
|  Parent (standalone)  431.10    28.0%   20.44%          -     |
|  Subsidiaries (blended) 94.28    6.27%   -3.02%    not disclosed|
|      ^ today this row is the ONLY external view               |
|  ----------------------------------------------------------  |
|  Entity A            X.XX     X.X%    X.XX%        Rs X.X Cr  |
|  Entity B            X.XX     X.X%    X.XX%        Rs X.X Cr  |
|      ^ what the board needs, and does not publish             |
+--------------------------------------------------------------+

DESIGN TRANSFER GATE  (before any commercial term is agreed)
+--------------------------------------------------------------+
|  Design: [licensor product]          Class: C / D             |
|  ----------------------------------------------------------  |
|  Approval travels with design? ................ YES / NO      |
|  Process parameters transferable? ............. YES / NO      |
|  Licensor pre-transfer QDR baseline ........... X.X / mn units|
|  ----------------------------------------------------------  |
|  ANY "NO" -> no commercial term is negotiated. K1 fires.      |
+--------------------------------------------------------------+

LINE DASHBOARD - LMR/100 AND THE GUARDRAIL
+--------------------------------------------------------------+
|  High-complexity revenue (denominator) ....... Rs XXX.X Cr    |
|  ...licensed, not acquired ................... Rs XXX.X Cr    |
|  ...manufactured in India .................... Rs XXX.X Cr    |
|  ...at or above standalone gross margin ...... Rs XXX.X Cr    |
|  ...royalty current .......................... Rs XXX.X Cr    |
|  ----------------------------------------------------------  |
|  LMR/100 ..................................... XX.X           |
|  QDR-90, worst line .......................... X.X / mn       |
|        ^ breach suspends that line automatically              |
+--------------------------------------------------------------+
```

---

## 53. Rollout Plan

**Phase 0 — four analyst-weeks, mostly on documents Poly Medicure already holds, designed to kill the proposal cheaply.**

Assess regulatory transferability and cost-base arbitrage across the acquired portfolio's own designs first, before approaching any external licensor.

- **K1.** Approvals do not travel. If CE marks and market registrations are site-bound such that transferring manufacture requires full re-approval, the time and cost advantage evaporates and licensing offers nothing acquisition does not.
- **K2 — named as the most likely to fire.** Poly Medicure has no inbound design-transfer capability. Three decades of registering *its own* designs is not the same skill as reproducing a third party's design history file under a different quality system, and if that capability has to be built first, the proposal's effort estimate is wrong by a wide margin.
- **K3.** No licensor will accept the terms. A design owner with an established Western manufacturing base has limited incentive to license production to a potential future competitor, and if the commercial terms available destroy the cost arbitrage, the instrument is uneconomic.

**Phase 1 (Q3 FY27).** Transferability assessed across the acquired portfolio's existing designs — the cheapest possible test, since Poly Medicure owns both sides. **Phase 2 (Q4 FY27).** One design transferred internally from an acquired entity to an Indian plant, with QDR-90 baselined and monitored. **Phase 3 (FY28).** External licensing only if Phase 2 clears §54's rule.

**Running in parallel and contingent on nothing above:** the integration opex programme and per-entity reporting that §47 ranks first and second. Both act on assets already owned.

---

## 54. A/B Testing

*Framework note: a true randomised test is not available for a manufacturing decision, so this is a matched-pair comparison rather than a split test, and it is described as such rather than dressed up.*

| Arm | Design |
|---|---|
| A — control | An acquired design, manufactured at the acquired entity's own facility, as today |
| B — falsification arm | **The same design, same facility, with the parent's operating disciplines applied** — procurement, overhead structure and plant practices transferred to the European site, but manufacture left where it is |
| C — treatment | The same design transferred to an Indian Poly Medicure facility under Licence-to-Make conditions |

**Arm B is built to kill the thesis.** It tests whether the margin gap is really about *geography* or merely about *management*. If applying the parent's operating disciplines to the acquired site closes most of the gap between a 6.27% and a 28.0% EBITDA margin, then the problem was integration all along, the cost base was never the binding constraint, and Poly Medicure should keep acquiring and simply run its acquisitions better. That is the cheaper answer, it needs no licensor and no regulator, and §47 already ranks it first.

**Pre-registered decision rule (R1).** Arm C proceeds to external licensing only if it beats Arm B by **more than 6 percentage points of EBITDA margin** on matched designs across two consecutive quarters, **and** QDR-90 is no worse than the pre-transfer baseline on every line measured separately, **and** the realised gross margin on transferred lines is at or above standalone gross margin. Failing any of the three, the programme reverts to Arm B or stops.
---

## 55. KPI Dashboard

| KPI | Baseline (Q1 FY27) | Target | Early warning |
|---|---|---|---|
| **Standalone PAT vs consolidated PAT** | Standalone **exceeds** by ₹2.85 Cr | Consolidated above standalone | **A second consecutive quarter of standalone above consolidated turns a first-year integration story into a structural one** |
| Subsidiary EBITDA margin (derived) | 6.27% | Converging toward 28.0% | Flat or falling next quarter |
| Organic revenue growth | 12.4% | At or above consolidated growth | Falls below 10% |
| Per-entity economics published | Not disclosed | Internal by Q3 FY27 | Not built by Q4 FY27 |
| LMR/100 | 0 (not built) | R1 threshold, §54 | Below 6pp over Arm B at two quarters |
| QDR-90, worst line | Not measured | ≤ licensor baseline | Any line worse than baseline |
| Consolidated run rate vs guidance | 89.43% of midpoint | Within the guided range | Still below the bottom of the range at H1 |

The first row is the discipline and it costs nothing to compute. Poly Medicure publishes both figures every quarter; **subtracting one from the other is the whole of this case study**, and anyone can do it in four weeks' time.

---

## 56. Product Roadmap

| Period | Focus |
|---|---|
| Q2 FY27 | Per-entity margin bridge built internally; integration opex programme scoped |
| Q3 FY27 | Integration programme executing; Phase 0 transferability assessment on owned designs |
| Q4 FY27 | Arm B — parent operating disciplines applied at an acquired site; one internal design transfer with QDR-90 baselined |
| FY28 H1 | §54 decision rule evaluated; external licensing pursued or dropped |
| FY28 H2 | Working capital programme against the 140-day cycle |

The proposed instrument sits third deliberately, behind two initiatives acting on assets already owned, because that is where §47 put it.

---

## 57. Risks & Mitigation

| Risk | Mitigation |
|---|---|
| Transferred manufacture degrades device quality | QDR-90 baselined before transfer, by line, owned outside the manufacturing P&L; automatic suspension on breach |
| Approvals do not travel with the design | K1 in Phase 0 tests this first, on owned designs, before any external negotiation |
| No inbound design-transfer capability | K2, named as most likely to fire; Phase 2 is an internal transfer precisely to build the capability cheaply |
| Licensors refuse workable terms | K3; the internal-transfer phase produces the evidence a licensor would need anyway |
| Chinese pricing erodes renal further | Not solved here and not pretended otherwise; §36 states the trade-off between defending the core loop and funding the move up-stack |
| Guidance is missed | Run rate is 89.43% of midpoint; tracked in §55 rather than asserted as a failure — three quarters remain |
| Licensor IP leaks into own-brand R&D | Segregated access control, licensor audit rights, §48 exclusion |

---

## 58. Future Vision

The plausible good outcome is specific and achievable: a company that reports per-entity economics, converts its acquired portfolio toward the parent's operating margin, and — if the evidence supports it — manufactures high-complexity designs in India under licence rather than buying the organisations that own them. That preserves the cost advantage that has funded thirty years of growth while moving into categories where price is not the deciding variable.

The bad outcome is not distress. With ₹854.7 Cr of cash, no long-term standalone debt and a 28.0% standalone EBITDA margin, this company has a great deal of room. The bad outcome is directional: another two years of acquisition-led headline growth in which consolidated margin drifts down, the organic engine keeps ceding commoditised categories to cheaper entrants, and the company arrives at 2030 with doubled revenue and the margin profile of the businesses it bought rather than the one it built.

---

## 59. PM Lessons

1. **When a company files standalone and consolidated accounts, subtract them.** One subtraction — ₹88.12 Cr minus ₹85.27 Cr — isolated the entire acquired portfolio's contribution with no estimation whatsoever.
2. **A group whose standalone profit exceeds its consolidated profit is telling you something specific**: everything it owns beyond the parent destroyed value in the period.
3. **Read gross margin and operating margin in opposite directions.** Consolidated gross margin was *higher* and consolidated EBITDA margin *lower*. That single inversion says the acquisitions brought good products and bad operating leverage, which is a completely different problem from bad products.
4. **Ask what an acquisition actually transfers.** Approvals and clinical evidence are portable; a cost base is not. If your advantage is cost, buying a company imports the thing you are trying to avoid.
5. **Separate bought growth from built growth before judging either.** 59.08% of the headline was inorganic; the underlying business grew 12.25% and its profit not at all.
6. **Include the number that weakens your argument.** These are first-year, integration-mode assets, and first-year consolidation routinely looks like this. The case study says so in §14 and cannot rule it out.
7. **Credit candid guidance.** Management told investors the quarter's 71.5% gross margin will normalise to 68–69%. Volunteering that your best number is 2.50–3.50 points above sustainable makes every other disclosure more believable.
8. **Check the registry.** Seven consecutive case studies have now found an NIC code that does not describe the business — long enough to be a finding about the register itself.

---

## 60. PM Interview Questions

1. Consolidated revenue rose 30.30% and consolidated profit fell 8.39%. What is the first line of the filing you look at, and why?
2. Standalone PAT exceeds consolidated PAT. Explain what that means to someone who does not read financial statements.
3. Consolidated gross margin is higher than standalone; consolidated EBITDA margin is lower. What does that combination tell you, and what would it take to fix it?
4. Your competitive advantage is a low cost base. Argue for and against acquisition as the way to move up the value chain.
5. Design a metric whose denominator makes acquisition *lower* the score. What are you giving up by choosing that denominator?
6. You propose transferring manufacture of a Class C/D device to a cheaper facility. Name the harm, and the mechanic — not the principle — that prevents it.
7. Your own sensitivity analysis ranks your proposal last, behind fixing what the company already owns. Do you still build it, and what would change your mind?

---

## 61. References

**Primary**
1. Poly Medicure Limited, outcome of board meeting and unaudited Q1 FY27 results, 7 August 2026 — standalone and consolidated revenue and PAT in ₹ lacs.
2. Poly Medicure Limited, Q1 FY27 investor presentation — margins, geography split, guidance, cash, new product launches.
3. Poly Medicure Limited, Q1 FY27 earnings call, 10 August 2026 — organic growth, acquisition contribution, renal pricing, Middle East exports, employee costs, tariff exposure, debt position, gross margin normalisation.
4. Ministry of Corporate Affairs registry — CIN L40300DL1995PLC066923.
5. Poly Medicure Limited, investor information and board disclosures, polymedicure.com.
6. NSE archives — board meeting outcomes and director appointments.

**Secondary** (corroboration; flagged where single-sourced)
7. Quartr — Q1 FY27 summary: standalone and consolidated revenue, margins, guidance, product launches.
8. Investing.com — Q1 FY27 slide summary and "PolyMed 3.0" framing.
9. Yahoo Finance / GuruFocus — Q1 FY27 earnings call highlights, segment and cost commentary.
10. Kalkine — board meeting outcome, ESOP grant, KMP resignation, plant locations.
11. InvestyWise — investor presentation summary, cash position, geography growth.
12. Business Standard — historical quarterly results and drug-eluting stent approval.
13. Tofler, ZaubaCorp, Tracxn, TheCompanyCheck, Falcon Ebiz — entity, NIC code, capital and director records (Appendix A-4).

---

## 62. About the Author

Gaurav Singh — Product Manager. Day 70 of a 90-day public case-study series applying structured PM frameworks to real products, under a zero-fabrication standard: every figure is cited, labelled as an estimate, flagged as single-sourced, or recorded as not publicly disclosed.

---

## 63. License

Analysis and original text © 2026 Gaurav Singh, released for non-commercial use with attribution. All company figures belong to their sources and are cited in §61. No affiliation with Poly Medicure Limited.

---

## 64. Self Review

**What is strong.** The central finding requires no estimation at all — it is one subtraction between two figures in the same filing, which makes it the most directly verifiable finding in this series. The margin-paradox mechanism (higher gross margin, lower EBITDA margin) turns a generic "acquisitions are dilutive" observation into a specific and actionable diagnosis. The stress rule is derived from the company's own reported margins. And the proposal loses to fixing what is already owned, asserted programmatically.

**What is weak, stated plainly.** The subsidiaries are **first-year, integration-mode assets**, and everything this case study observes about them is consistent with normal first-year consolidation — transaction costs, purchase-price allocation, duplicated overhead. A −3.02% net margin on recently acquired entities is not proof of a bad strategy; it may simply be proof of a recent one. This analysis can show the acquired portfolio destroyed profit in *this quarter*; it cannot show it will continue to. That is why §55's first row is a two-quarter test rather than a verdict.

**A second weakness.** The subsidiary figures are **blended across every acquired entity**, because Poly Medicure discloses no per-entity economics. A single poorly-performing asset and a portfolio of uniformly weak ones look identical in these numbers, and the strategic responses to those two situations are completely different.

**What I could not establish.** Per-acquisition revenue, margin, purchase price or integration timetable; the split of subsidiary revenue between the European and Brazilian entities; renal revenue in absolute terms; the segment split of the ₹72.3 Cr acquisition contribution; and whether the acquired entities' approvals are site-bound — the question K1 in §53 exists to answer and the one on which the entire proposal turns.

**One thing I would do differently.** I framed this as an acquisition-strategy case study, but the sharpest available finding is narrower and more useful: **the gross-margin/EBITDA-margin inversion.** That single comparison diagnoses the problem precisely, and I reached it in §14 rather than opening with it.

---

## 65. Appendix

### A. Source conflicts

| # | Conflict | Handling |
|---|---|---|
| A-1 | NIC code **4030, "steam and hot water supply"**, for a medical device manufacturer | Stated in §2 with the structural explanation; CIN cited in full. Seventh consecutive instance, now treated as a finding about the register |
| A-2 | **One outlet reported consolidated revenue as ₹558.78 Cr (+25.6%) with year columns labelled "Q1FY26" and "Q1FY25"**, contradicting the exchange filing's ₹52,537.55 lacs for Q1 FY27 | 🔴 **Resolved in favour of the exchange filing.** The filing's figures reconcile internally with the reported 30.3% growth and with the investor presentation's ₹525.4 Cr; the outlet's figures reconcile with neither. Not used |
| A-3 | Subsidiary economics are **derived by subtraction**, not disclosed. Standalone and consolidated are both reported; the difference is arithmetic, but attribution of that difference to "acquisitions" is an inference | Stated wherever used. The subtraction is exact; the interpretation is labelled as interpretation in §14, §32 and §64 |
| A-4 | Paid-up capital reported as **₹50.68 Cr** and **₹44.11 Cr** across MCA aggregators, as snapshots of different dates | 🟡 No capital figure used in any derivation |
| A-5 | Subsidiary EBITDA is derived from **rounded reported margins** (28.0% and 24.1%) applied to exact revenue figures, so the ₹5.91 Cr result carries rounding sensitivity | Flagged. The finding relies on the *direction and magnitude* of the gap, which survives any plausible rounding; the precise ₹ figure should be read as indicative |
| A-6 | Earnings-call details — renal 3.8%, Middle East −32%, employee costs +29%, tariff exposure, gross margin normalisation — come from **call coverage rather than a filed transcript** in the sources used | 🟡 Marked medium confidence throughout; none is load-bearing for the central finding, which rests entirely on the filing |
| A-7 | Figures appear in both **₹ lacs and ₹ crore** across sources (₹52,537.55 lacs = ₹525.38 Cr) | ₹ crore used throughout; conversions checked and asserted in `verify.py` |
| A-8 | The USD/INR rate used to size US tariff exposure (88) is **assumed, not disclosed** | Flagged; used only in D5g, which is illustrative and load-bearing nowhere |

### B. Evidence grades

🟢 **High** — the exchange filing's standalone and consolidated revenue and PAT, investor presentation margins and guidance, MCA registry.
🟡 **Medium** — earnings-call segment and cost commentary, capital snapshots, the derived subsidiary EBITDA figure.
🟠 **Low** — none relied upon.
🔴 **Conflicting** — A-2, the contradictory revenue report, resolved decisively in favour of the filing.

### C. Author-constructed content

*Licence-to-Make*, LMR/100, QDR-90, the RICE inputs, the parent-versus-subsidiary seam in §16, the Phase 0 kill criteria and the §54 matched-pair arms are the author's constructions, not Poly Medicure disclosures or plans. The attribution of the standalone/consolidated gap to acquisition economics is an inference from the disclosed acquisition contribution, not a stated company position. See ASSUMPTIONS.md Part 3 for the full inventory.

### D. Asset status

| Asset | Status |
|---|---|
| README.md | Complete, 65 sections |
| ASSUMPTIONS.md | Complete, Parts 1–5 |
| verify.py | 114 checks, all passing — delivered, not committed |
| LinkedIn carousel + caption | To follow |

---

*Day 70 of 90 · [← Day 69 — MedPlus](../Day-69-MedPlus) · Day 71 →*
