# Delhivery — The Density Worked. The Price Gave It Back.

### Day 58 of 90 · Product Management Case Study Series

> **The thesis of this case study:** Delhivery's Q1 FY27 is being read as a merger-integration quarter — express volumes up 55.2% to 322 million shipments, profit down 64.8% to ₹32 Cr, Ecom Express costs blamed. The disclosures do not support that reading. Ecom integration cost **₹17 Cr in the quarter, 28.8% of the ₹59 Cr profit decline**, and Delhivery's own ex-Ecom adjusted PAT still fell 31.9%. What actually happened is more interesting and much worse. The volume surge produced exactly the density economics a scaled logistics network exists to produce: **shipments per square foot of facility rose 35.9% and shipments per automated sorter rose 36.1%**. Every owned input — facility space, delivery centres, headcount, fleet, sorters — grew only **14.0% to 18.3%** against 55.2% more parcels. The operating leverage was real, large, and measured. It did not reach the P&L because **revenue per express shipment fell 14.2%, from ₹67.63 to ₹58.04**. Delhivery earned a genuine efficiency win and handed all of it back at the quote, one parcel at a time. In the same quarter, in the same country, Blue Dart grew shipment volumes **2%** and revenue **14.9%**, and its profit rose **85%** — earning **2.71× Delhivery's profit on 56.6% of its revenue**, at an EBITDA margin **3.12×** higher. Blue Dart's CFO attributes his own difficulty raising prices to "competitor excess capacity." Delhivery is the excess capacity, and the only input it added in line with volume was **partner agents, up 58.5% — the first year its outsourced edge became larger than its own workforce.** This case study argues Delhivery's missing product is not a way to move more parcels. It is a way to decide which parcels it should refuse.

---

## 2. Repository Metadata

| Field | Value |
|---|---|
| **Case study** | Day 58 of 90 |
| **Product** | Delhivery (Express Parcel, PTL Freight, Supply Chain Services, Delhivery Direct) |
| **Company** | Delhivery Limited, New Delhi — **CIN L63090DL2011PLC221234** |
| **Domain** | Logistics / third-party e-commerce fulfilment — the first logistics case study in this series |
| **Primary competitors** | Blue Dart, Ekart, XpressBees, Shadowfax, DTDC, India Post; captive networks of large marketplaces |
| **Analysis type** | Research-led teardown + network-productivity reconstruction + a feature proposal |
| **Proposed system** | **Delhivery Floor** — a published minimum contribution per shipment by lane class, below which volume is re-priced or deliberately released, with the released volume disclosed |
| **Author** | Gaurav Singh |
| **Date of analysis** | 24 August 2026 |
| **Research boundary** | Public sources only — exchange filings, the Q1 FY27 investor deck, MCA registry records, trade press, competitor disclosures. No employee or internal document consulted. |
| **Latest financials** | Q1 FY27 (quarter ended 30 June 2026), reported 8 August 2026 |

---

## 3. Badges

![Case Study](https://img.shields.io/badge/Case%20Study-Day%2058%20of%2090-blue)
![Domain](https://img.shields.io/badge/Domain-Logistics-orange)
![Method](https://img.shields.io/badge/Method-Research--Led%20Teardown-green)
![Sources](https://img.shields.io/badge/Sources-Public%20%26%20Cited-lightgrey)
![Fabricated Data](https://img.shields.io/badge/Fabricated%20Data-None-brightgreen)
![Assumptions](https://img.shields.io/badge/Assumptions-Declared%20in%20ASSUMPTIONS.md-yellow)

---

## 4. Table of Contents

<details>
<summary><b>Expand the full 65-section contents</b></summary>

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
| 14 | Competitor Analysis | 47 | RICE Prioritisation |
| 15 | SWOT | 48 | MoSCoW |
| 16 | Porter's Five Forces | 49 | Kano |
| 17 | Business Model Canvas | 50 | Feature Proposal |
| 18 | Revenue Model | 51 | PRD |
| 19 | Target Users | 52 | Wireframes |
| 20 | Personas | 53 | Rollout Plan |
| 21 | JTBD | 54 | A/B Testing |
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

Delhivery Limited is India's largest integrated third-party logistics provider by shipment volume, listed since May 2022. Q1 FY27 (quarter ended 30 June 2026) reported services revenue of **₹2,931 Cr (+27.8%)**, total income of ₹3,045 Cr, EBITDA of **₹156 Cr at a 5.3% margin** (from 6.5%), and **PAT of ₹32 Cr against ₹91 Cr — a 64.8% fall**. Express Parcel shipments reached **322 million, up 55.2%**.

**The standard explanation is Ecom Express, and the company's own numbers reject it.** Delhivery acquired Ecom Express for up to ₹1,407 Cr, completing on 18 July 2025 at 99.87% ownership. Integration cost **₹17 Cr in Q1 FY27**, down from ₹22 Cr the prior quarter — **28.8% of the ₹59 Cr profit decline**. Delhivery's own adjusted, ex-Ecom PAT of ₹62 Cr is still **31.9% below** last year's ₹91 Cr. Integration explains under a third of the damage.

**What the disclosures actually show is an efficiency win that never reached the P&L.** Against 55.2% more express shipments, every owned input grew far less: facility footprint **+14.2%** (20.4 → 23.3 Mn sq ft), express delivery centres **+18.3%**, headcount **+14.0%**, daily fleet **+18.0%**, automated sorters **+14.1%**. The arithmetic that follows is the finding of this case study: **shipments per square foot rose 35.9%** and **shipments per automated sorter rose 36.1%**. Density — the entire economic argument for building a national network — worked.

**And revenue per express shipment fell 14.2%, from ₹67.63 to ₹58.04.** The efficiency gain was handed to customers at the quote. Notably, this was not company policy: in the same quarter, **PTL realisation per tonne rose 5.15%**. Delhivery raised price in freight and cut it in parcels.

**The competitive mirror settles the argument.** Same quarter, same country, same industry: Blue Dart grew shipment volumes **~2%** and tonnage 7%, grew revenue **14.9%** on "pricing actions, fuel surcharge pass-through and yield improvement," and grew **profit 85% to ₹86.7 Cr**. Blue Dart earned **2.71× Delhivery's profit on 56.56% of its revenue**, at a consolidated EBITDA margin of 16.53% against Delhivery's 5.3% — **3.12×**. And Blue Dart's CFO explains his own pricing difficulty by pointing at "competitor excess capacity" in e-commerce. Delhivery is that capacity. **One firm in this market converted a small volume into a large profit; the other converted a large volume into a small one, and told the market it was integration costs.**

**One more disclosure completes the picture.** The only input Delhivery added faster than volume was **partner agents: 52,225 → 82,768, up 58.5%.** Partner agents now stand at **1.102× the company's own headcount**, having been 0.793× a year ago. This is the year Delhivery's outsourced edge became larger than Delhivery. The extra parcels were absorbed on rented feet at spot rates, which is why 36% more density per owned asset did not become 36% more margin.

This case study's proposal, §50, is deliberately **subtractive** — the first in this series that asks a company to get smaller on purpose. **Delhivery Floor** publishes a minimum contribution per shipment by lane class, re-prices what sits below it, releases what cannot be re-priced, and discloses how much revenue was walked away from. §40 states the reason this is dangerous before §50 specifies it: a contribution floor enforced by a sales organisation will be enforced against the shippers with the least negotiating power, and the guardrail is built to catch exactly that.

---

## 6. Product Overview

Delhivery sells four things. **Express Parcel** (₹1,869 Cr, 63.77% of services revenue, +33.2%) is B2C e-commerce parcel delivery — the volume business. **PTL Freight** (₹633 Cr, 21.6%, +24.5% on 542,000 tonnes, +18.4%) is part-truckload B2B freight. **Supply Chain Services** (₹199 Cr, 6.79%) is warehousing and fulfilment, and runs at a **−4.02% adjusted EBITDA margin**. **New initiatives** including Delhivery Direct contribute ₹32 Cr. These four lines sum to ₹2,733 Cr against services revenue of ₹2,931 Cr; the residual **₹198 Cr (6.76%)** covers truckload, cross-border and other services not separately broken out in the disclosure available (Appendix A-5).

Underneath sits the asset base: 23.3 Mn sq ft of facilities, 136 gateways, 48 automated sort centres with 73 sorters, 4,266 express delivery centres, 20,663 daily-average vehicles, 75,074 employees and 82,768 partner agents, serving 54,096 active customers.

---

## 7. Company Background

Incorporated **22 June 2011** at ROC Delhi as **SSN Logistics Private Limited**, later Delhivery Private Limited, then Delhivery Limited. Registered office: N24-N34, S24-S34, Air Cargo Logistics Centre-II, opposite Gate 6 Cargo Terminal, IGI Airport, New Delhi 110037. Authorised capital ₹134.25 Cr, paid-up ₹74.87 Cr.

**Sahil Barua** (DIN 05131571) is Managing Director; **Kapil Bharati** (DIN 02227607) is on the board. Independent and other directors include Srivatsan Rajan, Saugata Gupta, Anindya Ghose, Kabir Ahmed Shakir, Namita Vikas Thapar, Deepak Kapoor, Neelam Dhawan and Romesh Sobti.

Delhivery listed in May 2022. Its defining recent action is the **acquisition of Ecom Express for up to ₹1,407 Cr**, cleared by the CCI in June 2025 and completed **18 July 2025** at 99.87%. Integration involved retaining 7 Ecom facilities (1.3 Mn sq ft), exiting roughly 1.1 Mn sq ft, removing about **85% of Ecom's corporate and support functions**, and ceasing Ecom-branded volume manifestation — total integration cost guided to come in "marginally lower" than the ₹300 Cr originally forecast.

---

## 8. Product Timeline

| Year | Milestone |
|---|---|
| 2011 (Jun) | Incorporated as SSN Logistics Private Limited, ROC Delhi |
| 2022 (May) | IPO on NSE and BSE |
| 2025 (Apr) | Agreement to acquire Ecom Express for up to ₹1,407 Cr announced |
| 2025 (Jun) | CCI approval |
| 2025 (Jul 18) | Acquisition completed; 99.87% ownership |
| FY26 Q2–Q4 | Integration: 85% of Ecom corporate functions removed; ~1.1 Mn sq ft exited; Ecom volume manifestation ceased |
| FY27 Q1 | Express shipments 322 Mn (+55.2%); realisation per shipment −14.2%; PAT ₹32 Cr (−64.8%); integration cost ₹17 Cr |
| FY27 guidance | Express parcel growth 20–30%; express service EBITDA margin 16–18%; PTL exit margin near 15.5% against a 16–18% target |

---

## 9. Vision & Mission

Delhivery's stated purpose is to build the operating system for commerce in India — one national network carrying anybody's parcel, sold as infrastructure rather than as a branded courier. The strategic consequence is rarely stated: an infrastructure business is a **fixed-cost business**, and the only way a fixed-cost business earns is by filling capacity at a price above marginal cost. Delhivery has spent a decade proving it can fill capacity. Q1 FY27 is the quarter that asks whether it can price it.

---

## 10. Problem Statement

**Delhivery prices per shipment, but earns per unit of network capacity consumed.** It has no disclosed instrument that tells it the marginal cost of a specific parcel on a specific lane, and therefore no basis on which to refuse one. In a quarter where its own network became 36% more productive per owned asset, it gave 14.2% of realisation away and absorbed the overflow on partner capacity that now exceeds its own workforce. The result is 55% more parcels and a third of the profit.

Three facts make this structural rather than cyclical:

1. **The efficiency was real** — 35.9% more shipments per square foot — so this is not an operations problem.
2. **The price cut was selective** — PTL realisation rose 5.15% in the same quarter — so this is not a company-wide pricing policy.
3. **A direct competitor demonstrated the alternative in the same three months** — Blue Dart, +2% volume, +85% profit.

---

## 11. Market Research

| Fact | Value | Why it matters |
|---|---|---|
| Delhivery express shipments, Q1 FY27 | 322 Mn (+55.2%) | The volume the market noticed |
| Realisation per express shipment | **₹58.04, from ₹67.63 (−14.18%)** | The price it was bought with |
| PTL realisation per tonne | **₹11,679, from ₹11,107 (+5.15%)** | Price discipline exists inside the same company |
| Blue Dart Q1 FY27 | Volume +~2%, revenue +14.9%, PAT +85% | The alternative strategy, same quarter |
| Blue Dart consolidated EBITDA margin | 16.53% vs Delhivery's 5.3% | **3.12×** |
| Freight, handling and servicing cost | ₹2,152 Cr = **73.42% of services revenue** | The cost line the floor would govern |

**The negative observation matters most.** If Delhivery's price cut were a market-wide phenomenon, Blue Dart's realisation would have fallen too. Instead Blue Dart raised prices, said doing so was hard because of "competitor excess capacity," and doubled its profit. Two firms faced the same demand conditions and made opposite choices; only one of them has published a 36% density improvement.

---

## 12. Industry Analysis

Indian third-party logistics is a fixed-cost network industry with a variable-cost edge. Sort centres, gateways and line-haul are committed capacity; last-mile delivery is increasingly contracted to partner agents who can be scaled up or down within weeks. That asymmetry produces a specific failure mode: **a network operator can always say yes to more volume, because the marginal parcel appears to cost only its last-mile fee.** It does not — it consumes sort capacity, line-haul slots and peak headroom that are priced at zero in the moment and are the scarcest things the business owns.

Two shifts sharpen this. Quick commerce has absorbed a share of the small-basket, high-frequency demand that used to be express parcel. And marketplace captive networks continue to internalise their own volume, leaving third-party operators competing for a pool that grows more slowly than their capacity. Excess capacity in a fixed-cost industry is not a temporary state; it is a price war with a delay.

---

## 13. TAM / SAM / SOM

*Framework note: restricted. No credible primary-sourced TAM for Indian third-party express logistics could be verified, and this series does not publish market sizes it cannot trace. The opportunity is sized from Delhivery's own disclosed base instead.*

| Layer | Basis | Value |
|---|---|---|
| Express revenue at risk of mispricing | Q1 FY27 express parcel revenue | ₹1,869 Cr/quarter |
| Realisation already surrendered | 322 Mn shipments × ₹9.59 decline | **₹308.8 Cr in the quarter** |
| Annualised | × 4 | **~₹1,235 Cr** |
| For comparison | Q1 FY27 PAT | ₹32 Cr |

At last year's realisation, the same 322 million shipments would have produced roughly **₹308.8 Cr more revenue in a single quarter — 9.65× the quarter's entire profit.** No claim is made that all of it was recoverable; the point is the order of magnitude relative to what the business earns.

---

## 14. Competitor Analysis

This section is restricted to the one competitor that files comparable public accounts. Ekart, XpressBees and Shadowfax do not publish quarterly results on a comparable basis, so no estimate for them appears.

**Blue Dart, Q1 FY27 — the same three months.**

| | Delhivery | Blue Dart |
|---|---|---|
| Revenue | ₹2,931 Cr (+27.8%) | ₹1,657.7 Cr (+14.97%) |
| Shipment volume growth | **+55.2%** | **~+2%** (tonnage +7%) |
| Growth driver, per own disclosure | Volume | **Pricing, fuel surcharge pass-through, yield** |
| EBITDA margin | 5.3% | **16.53% consolidated** |
| PAT | ₹32 Cr (−64.8%) | **₹86.7 Cr (+85%)** |

**Blue Dart earned 2.71× Delhivery's profit on 56.56% of its revenue.** Its CFO, Sagar Patil, on why raising price is hard: *"We are already seen as a premium price player in the market, so it's never easy to get price increase"* — with pricing described as challenging in e-commerce specifically because of **competitor excess capacity**.

Delhivery is the competitor with the excess capacity. It has 23.3 Mn sq ft, 48 automated sort centres and 82,768 partner agents, and it converted a 55.2% volume increase into a 4.65% EBITDA increase. The comparison is not that Blue Dart is better run — its volumes are barely growing, which is its own strategic problem. It is that **the two firms show, in the same quarter, that in this industry price is a choice and volume is not a substitute for it.**

---

## 15. SWOT

| | Helpful | Harmful |
|---|---|---|
| **Internal** | Genuine, measured operating leverage — 35.9% more shipments per sq ft, 36.1% per sorter; 48 automated sort centres; PTL realisation +5.15% proves pricing capability exists; Ecom integration delivered under its ₹300 Cr budget | Express realisation −14.18%; EBITDA converts only 8.42% of volume growth; Supply Chain Services at −4.02% adjusted EBITDA; partner agents now 1.102× own headcount, up from 0.793× |
| **External** | Consolidation removed a price-cutting competitor; e-commerce parcel volumes still growing; PTL is a structurally better-priced market | Quick commerce absorbing small-basket demand; marketplace captive networks internalising volume; Blue Dart demonstrating a higher-margin alternative; excess industry capacity making price recovery collective, not unilateral |

---

## 16. Porter's Five Forces — run twice, merged

*Framework note: Delhivery's two large segments face structurally different markets. Both runs appear in one table so the divergence — which is the whole point — reads in a single pass.*

| Force | Express Parcel | PTL Freight |
|---|---|---|
| **Buyer power** | **Very high.** A handful of marketplaces and large sellers, all multi-homing, all able to shift volume weekly. This is where realisation fell 14.18%. | **Moderate.** Fragmented SME shipper base, higher switching cost. Realisation rose 5.15%. |
| **Supplier power** | Rising — partner agents grew 58.5% and are now the majority of the edge | Moderate — fleet and line-haul are more owned |
| **Substitutes** | **High.** Quick commerce, captive marketplace networks, India Post | Low. Full-truckload and rail are poor substitutes for part loads |
| **New entrants** | Low capital barrier at the edge, high at the sort layer | Higher — network density is genuinely hard |
| **Rivalry** | **Very high, and the binding constraint** — the industry has excess capacity, as Blue Dart states plainly | High but rational |

**What the double run shows:** Delhivery's pricing power is not uniformly absent — it is absent in exactly one segment, and that segment is 63.77% of services revenue. The same company that could not hold price on parcels raised it on freight in the same three months. That is evidence the express problem is a **structural buyer-power problem**, not a capability problem, and structural problems are not fixed by selling harder.

---

## 17. Business Model Canvas

| Block | Content |
|---|---|
| **Segments** | Marketplaces and large e-commerce sellers; D2C brands; SME shippers (PTL); enterprises (Supply Chain Services); 54,096 active customers |
| **Value propositions** | National reach at 4,266 delivery centres; automated sortation; single integration across express, freight and warehousing; scale pricing |
| **Key resources** | 23.3 Mn sq ft, 136 gateways, 48 automated sort centres / 73 sorters, 20,663 daily vehicles, 75,074 employees, **82,768 partner agents** |
| **Key activities** | Pickup, sortation, line-haul, last-mile delivery, returns, warehousing |
| **Revenue streams** | Per-shipment express fees; per-tonne PTL freight; supply chain contracts |
| **Cost structure** | Freight, handling and servicing ₹2,152 Cr (**73.42% of services revenue**; the disclosure states 71.4% of "revenue" without defining the base — Appendix A-5); employee benefits ₹429 Cr; contractual manpower 12.8% of revenue (from 12.2%); D&A ₹189 Cr |

**The canvas's own tension:** Key Resources are fixed and were 36% better utilised this year. Revenue Streams are priced per shipment, with no reference to which resource a shipment consumes. The business earns on capacity and charges on parcels, and nothing in the model reconciles the two.

---

## 18. Revenue Model

| Line | Q1 FY27 | Q1 FY26 | Change |
|---|---|---|---|
| Express Parcel | ₹1,869 Cr | ₹1,403.15 Cr | +33.2% |
| — shipments | 322 Mn | 207.47 Mn | **+55.2%** |
| — **realisation per shipment** | **₹58.04** | **₹67.63** | **−14.18%** |
| PTL Freight | ₹633 Cr | ₹508.43 Cr | +24.5% |
| — **realisation per tonne** | **₹11,679** | **₹11,107** | **+5.15%** |
| Supply Chain Services | ₹199 Cr | — | adj. EBITDA **−4.02%** |
| Services revenue | ₹2,931 Cr | ₹2,293.43 Cr | +27.8% |
| EBITDA | ₹156 Cr (5.3%) | ~₹149.07 Cr (6.5%) | **+4.65%** |
| PAT | ₹32 Cr | ₹91 Cr | **−64.84%** |
| PAT ex-Ecom (company adjusted) | ₹62 Cr | ₹91 Cr | −31.87% |

**The two bolded realisation rows are the case study.** One company, one quarter, two segments, opposite price directions.

---

## 19. Target Users

- **The marketplace / large seller.** Multi-homes across three or more carriers, negotiates annually, moves volume weekly. Holds the buyer power that produced the 14.18% decline.
- **The D2C brand.** Mid-size, values reliability and returns handling over the last rupee, and is the account class a contribution floor should protect rather than shed.
- **The SME shipper.** The tier-2/3 seller with no negotiating leverage — the population §40's guardrail exists to prevent the floor being enforced against.
- **The partner agent.** 82,768 of them, up 58.5%, now 1.102× Delhivery's own headcount. Not a customer, but the input whose growth outran everything else.

---

## 20. Personas

| Persona | Needs | Where the model fails them |
|---|---|---|
| **Category head at a marketplace** | Lowest cost per shipment at acceptable service | Gets it. There is no mechanism telling Delhivery when yes should have been no |
| **Ops lead at a D2C brand** | Predictable delivery and clean returns | Cross-subsidises the accounts that negotiated hardest, invisibly |
| **Tier-3 apparel seller, ~40 parcels/day** | Access at a published rate | Has no negotiating power; would be the cheapest place to enforce a floor, which is precisely the risk §40 guards |
| **Delhivery lane manager** | To know whether a lane makes money | No disclosed lane-level marginal cost exists to quote against |

---

## 21. Jobs To Be Done

| When… | I want to… | So I can… |
|---|---|---|
| I choose a carrier | compare landed cost and service credibly | ship without babysitting |
| I hit a peak | get capacity at short notice | not miss the season |
| I quote a new account | know what this lane actually costs | **price above marginal cost — the job with no tool** |
| I lose a claim or an RTO | recover cost and cause | stop it recurring |

Row 3 is the job nobody at Delhivery can currently do, and the whole of §50 is about making it possible.

---
## 22. User Journey

| Stage | What happens | Where cost is created vs priced |
|---|---|---|
| Quote / contract | Annual rate card negotiated per client, per weight slab and zone | **Priced by client. Cost is incurred by lane.** The mismatch starts here |
| Manifest | Shipper injects volume, quantity and timing of their choosing | Cost varies enormously by lane-day; price does not vary at all |
| Pickup | Partner agent or own fleet collects | Marginal cost visible only as a last-mile fee |
| Sortation | Automated sort centre, 73 sorters | **The scarcest asset. Priced at zero in the moment** |
| Line-haul | 20,663 daily vehicles | Fixed slot; a marginal parcel appears free until the slot is full |
| Last mile | Increasingly partner agents (+58.5%) | Rented at spot when own capacity is exhausted |
| RTO / return | Reverse leg | Roughly doubles the cost of a shipment already priced once |
| Invoice | Per shipment, per slab | The contribution of the individual shipment is never computed |

**Cost is created at the lane and priced at the client.** That single mismatch produces every number in this case study.

---

## 23. User Flow

The shipper flow — integrate, manifest, print label, hand over, track, reconcile — is mature and is not the problem. The flow that is missing is internal: a quote today is built from a rate card and a negotiated discount, not from the marginal cost of the lane the parcel will actually travel. There is no step at which a proposed shipment class is compared against a floor, and therefore no step at which anyone can decline it.

---

## 24. Information Architecture

Delhivery's commercial information is organised by **client and by product** (express / PTL / supply chain). Its costs are organised by **facility and lane**. No public artefact joins the two. A contribution floor is, at heart, an information-architecture change: make the **lane-weight-service class** the object that carries a price and a cost, and let clients be a rollup of it rather than the other way round.

---

## 25. UX Audit

The shipper-facing experience is not the binding constraint here, and this section is short by design. The one product observation worth making: nothing in the manifest flow tells a shipper what their choices cost. Weight declaration, address quality, pickup timing and peak-day injection all move Delhivery's cost materially and are invisible to the person making them. A network that shows shippers none of its constraints will be given all of their variance.

---

## 26. UI Audit

Not material to this analysis. The label, tracking and reconciliation surfaces are functional and heavily API-mediated in practice — most large shippers never see them.

---

## 27. Accessibility

Delhivery's genuine accessibility contribution is geographic and economic: 4,266 express delivery centres and 82,768 partner agents put national shipping within reach of sellers in towns no branded courier serves at that price. That is exactly why §50's subtractive proposal is dangerous, and why the guardrail in §40 is a *distributional* metric rather than a service one. A contribution floor that is enforced by quietly dropping tier-3 sellers would repay a margin problem by undoing the company's most defensible social and commercial achievement.

---

## 28. Feature Breakdown

| Capability | Disclosed scale | Read |
|---|---|---|
| Automated sortation | 48 centres, 73 sorters | **+36.07% shipments per sorter** — the leverage is real |
| Facility network | 23.3 Mn sq ft | **+35.88% shipments per sq ft** |
| Express delivery centres | 4,266 (+18.27%) | Grew far slower than volume |
| Partner agent network | 82,768 (**+58.48%**) | The only input that outran volume |
| Own fleet | 20,663/day (+18.01%) | Grew slower than volume |
| Workforce | 75,074 (+14.01%) | Grew slowest of all |

**Ranked by growth, the list tells the story on its own:** partner agents 58.5%, then a long gap, then everything Delhivery owns at 14–18%.

---

## 29. AI Capabilities

Delhivery has historically described machine learning across address resolution, geocoding, route optimisation, sort automation and demand forecasting, and its automated sortation footprint is the visible output. What is not evidenced in public disclosure is any **pricing** application: no disclosed model estimates the marginal cost of a specific shipment on a specific lane-day, and no disclosed system exposes such an estimate at the point of quotation. The company's analytical capability is pointed at moving parcels efficiently — demonstrated by the 36% productivity gain — and not at deciding which parcels to accept. §50 is an argument that the second is now the higher-value application of the same data.

---

## 30. Product Metrics

| Metric | Value | Evidence |
|---|---|---|
| Express shipments | 322 Mn (+55.2%) | 🟢 |
| **Realisation per express shipment** | **₹58.04 vs ₹67.63 (−14.18%)** | 🟡 Derived from disclosed revenue ÷ disclosed volume |
| **PTL realisation per tonne** | **₹11,679 vs ₹11,107 (+5.15%)** | 🟡 Derived |
| Shipments per sq ft | **13.82 vs 10.17 (+35.88%)** | 🟡 Derived |
| Shipments per sorter | **4.41 Mn vs 3.24 Mn (+36.07%)** | 🟡 Derived |
| EBITDA | ₹156 Cr, 5.3% (from 6.5%) | 🟢 |
| **Volume-growth-to-EBITDA conversion** | **8.42%** | 🟡 Derived — the RICE stress rule |
| PAT | ₹32 Cr (−64.84%); ex-Ecom ₹62 Cr (−31.87%) | 🟢 |
| Ecom integration cost | ₹17 Cr = **28.81% of the PAT decline** | 🟡 Derived |
| Partner agents ÷ employees | **1.102× (from 0.793×)** | 🟡 Derived |
| Shipments per partner agent | 3,890 vs 3,973 (**−2.07%**) | 🟡 Derived |
| Supply Chain Services adj. EBITDA | −₹8 Cr = **−4.02%** | 🟢 |
| Freight, handling, servicing | ₹2,152 Cr = **73.42% of services revenue** | 🟡 Derived; disclosure states 71.4% on an undefined base |

**The conversion number is the one to keep.** Express volumes grew 55.2%; EBITDA grew 4.65%. **8.42% of the volume growth reached EBITDA.** That figure is used as the RICE stress rule in §47, because it is Delhivery's own published evidence of what happens to a volume-led plan.

---

## 31. North Star Metric

**Current implied North Star: shipments.** It is the number the company leads with, the number the market reacted to, and the number that grew 55.2% while profit fell 64.8%. Its fatal property is simple: **it goes up when Delhivery accepts a parcel that costs more to carry than it is paid for.**

**Proposed North Star: CCF — Contribution-Covered Fill.** The share of *available own-network capacity* (sort-centre throughput hours) filled by shipments meeting **all three** conditions:

1. **Delivered within the promised window** — a cheap parcel that fails service is not a win;
2. **Realised revenue above the lane's marginal cost to serve**, computed at lane × weight slab × service class;
3. **Handled on own capacity that was genuinely available** — not peak overflow rented from partners at spot.

The denominator is **capacity, not shipments**. That is the design choice that makes CCF honest: shedding volume without shedding capacity *lowers* it, so the metric cannot be gamed by simply refusing business, and it cannot be gamed by raising price until volume leaves. It forces the actual trade-off Delhivery has been avoiding.

**Guardrail: RSC-90 — Released Shipper Concentration at the 90th percentile.** Across lanes and months, the share of released or repriced-out volume attributable to shippers in the **smallest revenue quartile**, measured at the 90th percentile. At p90 rather than the mean, because a mean across hundreds of lanes will hide the handful of lanes where small sellers were cleared out wholesale — and those lanes are the entire risk. Governance in §40; carried through §48, §51–§55 and §57.

---

## 32. Product Analytics

| Signal | Where it lives | Needed for |
|---|---|---|
| Shipment-level lane, weight slab, service class | Manifest and sortation scans | The cost object |
| Facility and line-haul cost by lane-day | Finance and network operations | Marginal cost |
| Partner agent spot rates by pin code | Last-mile settlement | Condition 3 — separating own capacity from rented |
| Own-capacity availability by sort centre-hour | Sortation systems | The CCF denominator |
| Shipper revenue quartile | Commercial systems | RSC-90 |

Every one of these exists inside Delhivery today. **None of them is disclosed as joined**, and the join — not the collection — is the whole of Initiative 1 in §47.

---

## 33. AARRR

| Stage | Current | Under Delhivery Floor |
|---|---|---|
| Acquisition | 54,096 active customers (+25.7%) | **Deliberately slower.** This is a subtractive proposal and pretending otherwise would be dishonest |
| Activation | Volume onboarded on a client rate card | Onboarded against a lane-class floor |
| **Retention** | Undisclosed by contribution class | Retention of *contribution-positive* volume becomes the measured thing |
| **Revenue** | ₹58.04 per express shipment, falling | Realisation defended lane by lane rather than negotiated client by client |

---

## 34. HEART

| Dimension | Current | Under proposal |
|---|---|---|
| Happiness | Not disclosed at shipper level | Monitored, especially in the smallest revenue quartile |
| Adoption / Engagement | 54,096 active customers | Explicitly not targets — growth in customer count is what got the company here |
| **Task success** | On-time delivery within promise | Condition 1 of CCF — a floor that degrades service is not a floor, it is a cut |

---

## 35. Growth Strategy

Management guides express parcel growth of **20–30%** for FY27 against 55.2% delivered in Q1, express service EBITDA margins of **16–18%**, and PTL exit margins near **15.5%** against a 16–18% target. The guidance is internally coherent — it implies deliberately slower volume growth and materially better margins, which is very close to what §50 proposes.

The gap is that no disclosed *mechanism* delivers it. Slower growth and better margins do not arrive by being forecast; they arrive when someone in a sales conversation has a number that lets them say no. Producing that number is Initiative 1.

---

## 36. Growth Loops

**The loop that ran this quarter:** lower price → more volume → higher density → lower unit cost → room to lower price again. It is a real loop and it works — the density gain proves it. It also has no exit condition, and Blue Dart's CFO describing the market's "competitor excess capacity" is the sound of the loop being felt from outside.

**The loop the proposal creates:** measured lane contribution → informed refusal or repricing → capacity freed for higher-contribution volume → margin → capital for automation → lower marginal cost. The difference is not speed. It is that the second loop has a floor.

---

## 37. Network Effects

Genuine but widely overstated for logistics. Density economics are real — 35.88% more shipments per square foot is the proof — but they are **local and lane-specific**, not global. Extra volume on a saturated Delhi–Bengaluru lane creates no benefit to a thin Guwahati lane, and may cost more than it earns if it arrives at peak. Treating density as a company-wide good, rather than a lane-level one, is precisely the error that lets a firm accept volume that dilutes its own economics while believing it is compounding them.

---

## 38. Product Strategy

**The strategic read.** Delhivery has spent a decade building the cheapest national network in India and has now proved it: 36% more throughput per owned asset in a single year. Its strategy problem is that it treats this as a **cost advantage to be passed on** rather than a **margin advantage to be kept**, and the only disclosed mechanism it has for capturing value is winning more volume — which requires giving the advantage away.

**A deliberate demotion.** The Ecom Express acquisition is the more newsworthy subject and this case study demotes it to context, for a stated reason: at ₹17 Cr of integration cost against a ₹59 Cr profit decline, and with the company's own ex-Ecom adjusted PAT still down 31.87%, **the acquisition explains under a third of the quarter and is measurably not the thing to write about.** Naming why the obvious story was rejected is more useful than telling it.

---

## 39. Monetization

Delhivery monetises per shipment against a client rate card negotiated annually across weight slabs and zones. Three properties of that instrument produced this quarter:

1. **The unit of pricing is not the unit of cost.** A client price cannot express that a parcel on a thin lane at peak costs multiples of the same parcel on a dense lane midweek.
2. **The discount is granted where the leverage is, not where the cost is.** The largest, most multi-homed shippers extract the deepest discounts, and they are the ones with volume concentrated on exactly the lanes that are already saturated.
3. **There is no floor.** Nothing prevents an individually rational sales decision from being collectively value-destroying, and 322 million of them compound to −14.18% realisation.

**Delhivery Floor adds the missing instrument:** a published minimum contribution per shipment by lane class, below which volume is repriced at renewal or released, with the released volume disclosed each quarter. The disclosure matters as much as the floor — an internal floor is a target and gets negotiated away; a published one is a commitment the sales organisation cannot quietly discount against.

---

## 40. Trust & Safety

**This section precedes §50 deliberately, because a contribution floor is dangerous in a specific and predictable way.**

A floor will be enforced wherever enforcement is cheapest, and enforcement is cheapest against **the shippers with no negotiating power**. A marketplace with 15% of Delhivery's volume will not accept a repricing; a tier-3 apparel seller shipping 40 parcels a day will simply be dropped. That outcome would be commercially trivial and strategically self-destructive: the sub-scale seller base reachable through 4,266 delivery centres and 82,768 partner agents is the thing Delhivery has that Blue Dart does not.

A second, subtler failure: a floor computed from *current* marginal cost will condemn thin lanes permanently, because thin lanes are expensive precisely because they are thin. Enforced naively, the floor would shrink the network to its dense core and dismantle the national coverage that is the product.

| Control | Specification |
|---|---|
| **Metric** | **RSC-90** — share of released or repriced-out volume from the smallest shipper revenue quartile, at the 90th percentile across lanes and months |
| **Owner** | A Network Access function with **no revenue claim** and no reporting line into commercial or sales |
| **Firewall** | Release decisions and their reason codes **architecturally separated** from the sales commission and incentive systems — enforced by an access-control test in the build pipeline, not by policy |
| **Thin-lane carve-out** | Lanes designated as coverage lanes are exempt from the floor and funded explicitly from a disclosed coverage budget, so that national reach is a **stated cost** rather than an accidental cross-subsidy |
| **Kill switch** | Automatic, per lane: two consecutive monthly RSC-90 breaches suspend the floor on that lane until the breach clears, with no discretionary override |
| **Disclosure** | Released volume, released revenue and RSC-90 published quarterly alongside shipment counts |

The thin-lane carve-out is the load-bearing control. Without it, a contribution floor is just a plan to become Blue Dart — which, on the evidence of §14, would be more profitable and considerably less interesting.

---

## 41. Technical Architecture

Delhivery publishes no architecture diagram; this describes only what disclosed operating metrics require.

| Layer | Evidenced by | Confidence |
|---|---|---|
| Automated sortation and scan capture | 48 centres, 73 sorters, 322 Mn shipments | 🟢 |
| Network planning and line-haul scheduling | 136 gateways, 20,663 daily vehicles | 🟢 |
| Partner agent dispatch and settlement | 82,768 partner agents | 🟢 |
| Client rate-card and billing engine | Per-shipment invoicing across weight slabs and zones | 🟡 Inferred |
| **Lane-level marginal cost service** | — | 🔴 **No evidence it exists. The one thing the Floor requires and the one thing not visible** |

That last row drives kill criterion K3.

---

## 42. Data Flow

Manifest → pickup scan → gateway scan → sort scan → line-haul → delivery-centre scan → delivery or RTO scan → settlement. Every one of these events already carries a lane, a facility, a timestamp and a weight. **The cost of the shipment is fully determined by data Delhivery already captures**, and is never assembled into a number that reaches a quote. The Floor is not a data-collection project; it is a join.

---

## 43. API Ecosystem

Delhivery's integration surface is a genuine strategic asset: large shippers integrate once and route volume programmatically. That is also why the price cut compounded — a programmatic customer reallocates volume in a day. The Floor adds one field to the quote response: **the lane class and its floor status**, so a shipper's own system can see which lanes are constrained before it manifests, rather than discovering it in a renewal negotiation.

---

## 44. Privacy & Security

Low sensitivity relative to Day 57's subject: the data involved is commercial shipment metadata, not personal health or financial records, though consignee addresses and phone numbers sit within DPDP scope and the DPDP Rules notified 14 November 2025 apply with full enforcement in 2027. The Floor introduces one genuinely new sensitivity — **shipper-level contribution data**, which is commercially explosive if it leaks across accounts. §51 requires it to be aggregated to lane class for any use outside a named account team, with the same architectural firewall that separates release decisions from sales incentives.

---
## 45. Pain Points

| # | Pain point | Whose | Evidence |
|---|---|---|---|
| 1 | Price is negotiated by client; cost is incurred by lane | Delhivery | Express realisation −14.18% while PTL rose 5.15% |
| 2 | A 36% density gain reached the P&L as 4.65% EBITDA growth | Delhivery | 35.88% shipments/sq ft; EBITDA ₹149.07 → ₹156 Cr |
| 3 | Volume overflow is absorbed on rented capacity at spot | Delhivery | Partner agents +58.48% vs owned inputs +14–18% |
| 4 | No lane-level marginal cost exists to quote against | Sales and lane managers | Not disclosed; §41 |
| 5 | Small shippers have no protection if a floor is imposed | Tier-2/3 sellers | The failure mode §40 is built for |
| 6 | Supply Chain Services loses money at scale | Delhivery | −₹8 Cr adjusted EBITDA, −4.02% margin |

---

## 46. Opportunity Mapping

Four converging lines make the contribution floor the right opportunity:

1. **The efficiency already exists and is measured.** 35.88% more shipments per square foot. Nothing has to be built to create the value — only to stop giving it away.
2. **The capability is proven inside the same company.** PTL raised realisation 5.15% in the same quarter. Delhivery can hold price; it did not in express.
3. **The data is already captured.** Every scan carries lane, facility, timestamp and weight (§42). This is a join, not a collection programme.
4. **A competitor has demonstrated the payoff in the same three months.** Blue Dart: +2% volume, +85% profit, 16.53% EBITDA margin.

**Lines 1 and 3 are the reusable method:** *look for the efficiency a company has already achieved but not kept; look for the number it could already compute but does not.*

---

## 47. RICE Prioritisation

*Framework note: run twice. The stress rule is built from Delhivery's own published evidence about what happens to a volume-led plan — express volumes grew **55.2%** and EBITDA grew **4.65%**, a **conversion of 8.42%**. It is applied to Reach for any initiative whose value depends on volume growth converting into margin. Initiatives whose value comes from variance reduction or internal measurement are not stressed.*

Score = Reach × Impact × Confidence ÷ Effort, ×100.

| Initiative | R | I | C | E | Score | Stressed R | **Stressed** |
|---|---|---|---|---|---|---|---|
| **1. Lane-level marginal cost service** — join existing scan, facility and settlement data into a cost per lane × weight slab × service class | 9 | 2.0 | 0.90 | 5 | **324.0** | not stressed | **324.0** |
| **2. Contribution at quote time** — surface lane contribution to sales inside the quoting tool, advisory only | 8 | 2.0 | 0.85 | 7 | **194.29** | not stressed | **194.29** |
| **4. Peak capacity forward booking** — large shippers reserve peak sort capacity ahead; unreserved volume prices at spot | 6 | 2.5 | 0.60 | 8 | **112.50** | not stressed | **112.50** |
| **3. Delhivery Floor** — published minimum contribution by lane class, reprice or release below it | 9 | 3.0 | 0.55 | 12 | **123.75** | 0.7576 | **10.42** |

**The stress test demotes this case study's own proposal from third to last**, behind a forward-booking mechanism it did not propose and behind two initiatives that are, respectively, a data join and a tooltip.

That is the exercise working. The Floor's value is entirely contingent on recovered contribution surviving contact with a competitive market — and Delhivery's own quarter says only **8.42%** of a volume movement reached EBITDA. Forward booking is not stressed because its benefit is **variance reduction**: it is worth having whether or not the recovered rupees stick, which is exactly the property the Floor lacks.

§53 follows the stressed order, and the reason is causal rather than deferential: **you cannot publish a contribution floor before you can compute a lane's marginal cost, and you should not impose one on a sales organisation that has not first spent two quarters seeing the number in its own quoting tool.**

---

## 48. MoSCoW

| Priority | Item |
|---|---|
| **Must** | Lane-level marginal cost service; RSC-90 instrumented and published *before* any release decision; thin-lane coverage carve-out with a disclosed budget; architectural firewall between release decisions and sales incentives |
| **Should** | Contribution surfaced at quote time, advisory only, for two full quarters; peak capacity forward booking with the ten largest shippers |
| **Could** | Published floor on a limited set of dense lanes; lane-class status exposed in the quote API |
| **Won't (this cycle)** | Network-wide floor; any floor on designated coverage lanes; sales incentives tied to contribution — **permanently excluded, not deferred**, because that is the mechanism by which small shippers get dropped |

---

## 49. Kano

| Feature | Classification |
|---|---|
| National coverage at published rates | Basic — its absence disqualifies Delhivery from being infrastructure |
| Delivery within promise | Performance — and Condition 1 of CCF |
| Lane-class visibility in the quote API | **Attractive today, Basic within ~18 months** once one carrier ships it |
| A published contribution floor | Not a customer feature at all — Kano does not apply, and forcing it here would be padding |

---

## 50. Feature Proposal — **Delhivery Floor**

**One sentence.** Delhivery computes a marginal cost per lane × weight slab × service class, publishes a minimum contribution per shipment for each lane class, reprices volume below it at renewal, releases what cannot be repriced, and discloses quarterly how much revenue it deliberately walked away from.

**This is a subtractive proposal**, and that is unusual enough to state plainly. Every prior proposal in this series adds something — a subscription, a tier, a layer, a ledger. This one asks a company growing volume 55% to grow it less, on purpose, and to say publicly how much less.

**Four components.**

1. **The cost service.** Marginal cost per lane × weight slab × service class, assembled from scan, facility, line-haul and partner-settlement data Delhivery already holds. Refreshed monthly. This is Initiative 1 and it has standalone value.
2. **The floor.** A published minimum contribution per shipment by lane class. Published, not internal — an internal floor becomes a target and is negotiated away; a published one is a commitment a sales organisation cannot quietly discount against.
3. **The release.** Volume below the floor is repriced at renewal, and released if it cannot be. Released volume, released revenue and **RSC-90** are disclosed quarterly. The disclosure is the discipline.
4. **The coverage budget.** Thin lanes that exist for national reach are exempt, funded from an explicitly disclosed coverage budget, so that reach becomes a stated cost rather than an accidental cross-subsidy paid for by the dense lanes.

**Why this and not more volume.** Delhivery already ran the volume experiment at scale this quarter. 55.2% more shipments produced 4.65% more EBITDA and 64.8% less profit. The experiment has a result.

**User impact.** Neutral for shippers above the floor. **Negative for shippers below it, and disproportionately for the smallest** — which is why §40 precedes this section, why RSC-90 exists, and why tying sales incentives to contribution is permanently excluded in §48.

**Business impact.** At last year's realisation, the same 322 Mn shipments would have earned roughly **₹308.8 Cr more in the quarter — 9.65× the quarter's PAT.** No claim is made that all of it is recoverable; the point is that the number the Floor governs is an order of magnitude larger than the number the business currently earns.

**Trade-offs.** Slower volume growth, which this market rewards in the short run. Lost density on lanes where released volume was covering fixed cost. A competitor free to take the released volume — genuinely the strongest argument against the proposal, and the reason the pilot is confined to lanes where Delhivery's cost position is strongest.

---

## 51. PRD (abridged)

| Field | Specification |
|---|---|
| **Problem** | Price is set per client, cost is incurred per lane; no instrument lets Delhivery decline a shipment that costs more than it earns |
| **Scope v1** | Ten dense express lanes, one weight slab band, one service class |
| **Out of scope, permanently** | Any floor on designated coverage lanes; sales incentives tied to contribution; shipper-level contribution data visible outside the named account team |
| **Data** | Existing scan events (lane, facility, timestamp, weight), facility and line-haul cost allocation, partner settlement rates by pin code, own-capacity availability by sort centre-hour, shipper revenue quartile |
| **Privacy** | Shipper contribution aggregated to lane class outside the account team; DPDP scope acknowledged for consignee data; firewall verified by build-pipeline test |
| **Guardrail** | RSC-90 at the 90th percentile, published quarterly, owned by Network Access, automatic per-lane kill switch on two consecutive breaches |
| **Decision rule** | §54 R1, pre-registered before the pilot begins |
| **Dependencies** | Initiative 1 shipped and reconciled to finance within ±15%; two full quarters of advisory-only contribution display before any release decision |

---

## 52. Wireframes

The one surface that matters is internal — the quoting screen a salesperson sees. Deliberately low-fidelity.

```
 QUOTE · LANE DEL→BLR · 0.5–1.0 kg · SURFACE          Lane class: A (dense)
 ┌──────────────────────────────────────────────────────────────────┐
 │  Proposed rate            ₹54.00 / shipment                      │
 │  Lane marginal cost       ₹51.20   (refreshed 01 Aug, ±9%)       │
 │  Contribution             ₹ 2.80   ·  FLOOR ₹6.50   ✗ BELOW      │
 │                                                                   │
 │  Own capacity available on this lane-day .......... 71%           │
 │  Above 85%, overflow prices at partner spot (₹63.40 avg)          │
 │                                                                   │
 │  To proceed:  [Reprice to ₹57.70]   [Request coverage exemption]  │
 │               [Escalate to Network Access]                        │
 │                                                                   │
 │  Shipper revenue quartile: Q1 (largest) — RSC-90 not affected     │
 └──────────────────────────────────────────────────────────────────┘
```

The last line is the one that makes the guardrail work in practice. A salesperson enforcing the floor sees, at the moment of decision, which quartile the shipper sits in — so that the cheapest place to enforce is also the most visible.

---

## 53. Rollout Plan

**The sequence follows §47's stressed ranking**, because the cost service is a precondition for the floor and the advisory period is a precondition for imposing it.

**Phase 0 — falsification, before anything is built. Two analyst-weeks on data Delhivery already holds.**

| Kill criterion | Test | Threshold |
|---|---|---|
| **K1** | What share of Q1 FY27 express shipments earned less than their lane's marginal cost? | **<20%** — below that there is no pool worth building an instrument for |
| **K2** | How much of the 14.18% realisation decline is explained by the acquired Ecom Express book's lower price points, rather than by price action on retained accounts? | **>70% mix** — then this is a merger accounting artefact and the pricing thesis is wrong. **This is the criterion most likely to fire, and it is named as such.** |
| **K3** | Can lane marginal cost be computed to ±15% and reconciled to reported facility and line-haul cost? | **No** — the floor is unbuildable and Initiative 1 becomes a data project, not a pricing one |

**Phase 1 (0–4 months)** Lane-level marginal cost service, internal, reconciled to finance. **Phase 2 (4–10)** Contribution shown at quote time, **advisory only** — no floor, no enforcement, no incentive change, for two full quarters. This phase exists to let the sales organisation argue with the number before the number can cost anyone a deal. **Phase 3 (8–12)** Guardrail first: RSC-90 instrumented and baselined, Network Access stood up, coverage lanes designated and budgeted, firewall test passing — all before a single release decision. **Phase 4 (12–18)** Published floor on ten dense lanes, decision rule pre-registered. **Phase 5 (18+)** Extend only on that rule.

---

## 54. A/B Testing

| Arm | Structure |
|---|---|
| **A** | Control — current client-negotiated rate cards |
| **B** | Cost service built, contribution visible internally, no floor — isolates the value of merely *knowing* |
| **C** | **Full Delhivery Floor** — published floor, reprice and release, coverage carve-out |
| **D** | Floor published but enforcement advisory — isolates publication from enforcement |
| **E** | **Falsification arm** — a flat across-the-board rate increase on the bottom revenue decile of accounts, no lane instrumentation, no floor, no disclosure |

**Arm E is built to kill the thesis.** If a blunt price rise on the worst accounts recovers most of the contribution, then the lane-level cost service, the floor, the coverage budget and the Network Access function are an expensive way to reach a result a spreadsheet and a firm letter would have produced.

**Pre-registered decision rule R1, fixed before the pilot begins:** *Delhivery Floor proceeds beyond Phase 4 only if arm C delivers more than 5% higher contribution per unit of own-network capacity than arm E across two consecutive quarters including one peak season, with RSC-90 no worse than arm A's baseline in either quarter and on-time delivery within promise not below baseline.* Failing either the RSC-90 or the service condition kills the programme regardless of the contribution result.

---

## 55. KPI Dashboard

| Tier | Metric | Read |
|---|---|---|
| **North Star** | **CCF** — contribution-covered fill of available own capacity | Cannot be gamed by refusing volume; the denominator is capacity |
| **Guardrail** | **RSC-90** — released shipper concentration, 90th percentile | Network Access owns it; kill switch on two consecutive breaches |
| **Guardrail** | On-time delivery within promise | A floor that degrades service is a cut, not a floor |
| Commercial | Realisation per express shipment | ₹58.04 today, from ₹67.63 — the number being defended |
| Commercial | Released volume and released revenue | Published quarterly; the discipline is the disclosure |
| Network | Shipments per sq ft and per sorter | 13.82 and 4.41 Mn — must not fall as volume is shed |
| Network | Partner-handled share of shipments | Rented capacity is where the margin leaks |
| **Early warning** | **Realisation on retained pre-merger accounts only** | If blended realisation falls while retained-account realisation is flat, the decline is acquired-book mix and **Assumption A1 is dead** |

The early-warning row is the most important line here: it is designed to disconfirm this case study's own central claim, and it needs only a cohort tag Delhivery already has.

---

## 56. Product Roadmap

| Horizon | Focus |
|---|---|
| **0–6 months** | Phase 0 falsification; lane marginal cost service reconciled to finance |
| **6–12 months** | Contribution advisory at quote time; RSC-90 baselined; coverage lanes designated and budgeted |
| **12–24 months** | Published floor on ten dense lanes; peak forward booking with the ten largest shippers (the initiative that beat the Floor under stress); management's own 16–18% express service EBITDA target becomes a public, dated test |
| **24+ months** | Floor extended on R1; Supply Chain Services reassessed against the same contribution discipline |

---

## 57. Risks & Mitigation

| # | Risk | Severity | Mitigation |
|---|---|---|---|
| 1 | **The floor is enforced against small shippers** because they cannot negotiate | **Critical** | RSC-90 at p90, owned outside commercial, automatic per-lane kill switch, published quarterly; contribution-linked sales incentives permanently excluded |
| 2 | **Thin lanes are shut and national coverage collapses** | **Critical** | Coverage-lane carve-out funded from a disclosed budget; reach becomes a stated cost, not an accidental subsidy |
| 3 | Released volume goes to a competitor and density falls | High | Pilot confined to lanes where Delhivery's cost position is strongest; CCF's capacity denominator makes lost density visible immediately |
| 4 | The realisation decline is acquired-book mix, not price action | High | K2 kills at Phase 0 for two analyst-weeks; §55 early-warning row tracks it continuously |
| 5 | Lane marginal cost cannot be computed credibly | Medium | K3; ±15% reconciliation to finance is a gate, not an aspiration |
| 6 | Sales organisation routes around the floor via service-class or slab reclassification | Medium | Floor defined at lane × slab × service class precisely to close that gap; reclassification rates monitored |

---

## 58. Future Vision

The interesting question for Indian logistics over the next five years is not who moves the most parcels. It is who is first able to say, at the moment of quotation, what a parcel costs. Whoever can do that can price selectively, subsidise coverage deliberately, and let a competitor take the volume that destroys value — and can prove to the market which is which.

Delhivery is closer to that than anyone else in India, because it already owns the sortation, the scans and the settlement data. Its Q1 FY27 shows it has not yet chosen to use them that way.

---

## 59. PM Lessons

1. **When volume and revenue growth diverge, divide.** 322 Mn shipments against ₹1,869 Cr is one division, and it produced the entire thesis: realisation −14.18%. Always put disclosed volume next to disclosed value before believing a growth number.
2. **Check whether the efficiency arrived and check where it went.** Shipments per square foot rose 35.88%. The leverage was real. Finding that it was real is what turns "margins fell" into "margins were given away."
3. **Test the convenient explanation and publish the result.** Ecom integration cost ₹17 Cr against a ₹59 Cr profit decline — **28.81%**. The company's own adjusted PAT still fell 31.87%. One ratio disposed of the story everyone else wrote.
4. **Look for the same company doing the opposite thing.** PTL realisation rose 5.15% in the same quarter express fell 14.18%. Internal contradiction is stronger evidence than any external benchmark, because it controls for everything.
5. **Then look for the competitor doing the opposite thing.** Blue Dart: +2% volume, +85% profit, and a CFO naming "competitor excess capacity" as his own constraint. Same quarter, same country, opposite strategy, opposite result.

---

## 60. PM Interview Questions

1. Volumes grew 55% and profit fell 65%. The company blames merger integration costs of ₹17 Cr against a ₹59 Cr decline. What do you check next, and in what order?
2. Your network became 36% more productive per square foot and your margin fell. Where did the gain go, and what instrument would have kept it?
3. Design a metric for a fixed-cost network that cannot be improved either by accepting bad volume or by refusing good volume.
4. You propose a contribution floor. Your CFO loves it and wants sales commissions tied to contribution next quarter. Explain, in one minute, why that specific step would destroy the company's most defensible asset.
5. PTL raised price 5.15% in the same quarter express cut it 14.18%. What does that single fact rule out?

---

## 61. References

Figures are attributed inline and in `ASSUMPTIONS.md`. Source classes used:

- Delhivery Limited — Q1 FY27 results and investor presentation (quarter ended 30 June 2026, reported 8 August 2026)
- Delhivery Limited — investor relations disclosures and management commentary on Ecom Express integration
- MCA registry records via aggregators — CIN, incorporation, directors, capital, previous names
- Blue Dart Express Limited — Q1 FY27 results, investor presentation and management commentary
- Trade and business press on the Ecom Express acquisition (announcement April 2025, CCI approval June 2025, completion 18 July 2025)
- DPDP Rules 2025, notified 14 November 2025

---

## 62. About the Author

**Gaurav Singh** — Product Management case study series, Day 58 of 90. Research-led product teardowns built from public sources only, with every derived figure verified programmatically and every assumption declared in `ASSUMPTIONS.md`.

---

## 63. License

Published for portfolio and educational purposes. All company names, trademarks and product names belong to their respective owners. No affiliation with Delhivery Limited, Blue Dart Express Limited or any entity named here is claimed or implied.

---

## 64. Self Review

**Strengths.** It rejects the explanation everyone else accepted and shows the arithmetic that rejects it. It finds a real efficiency gain hidden inside a bad quarter and identifies where it went. It uses an internal contradiction (PTL up, express down) before reaching for an external benchmark, and then finds an external one in the same quarter. It proposes something subtractive, which no earlier case study in this series has done, and stress-tests it into last place using the company's own conversion rate.

**Weakest point.** Assumption A1 — that the realisation decline reflects price action on retained business rather than mix from the acquired Ecom Express book — carries the argument and cannot be settled from public data. Delhivery does not publish realisation split by retained versus acquired accounts. The rival reading gets equal air in ASSUMPTIONS Part 1, K2 is built to kill the thesis at Phase 0, and §55's early-warning row tracks it.

**Left out for length.** Supply Chain Services' −4.02% margin, Delhivery Direct, the returns and RTO economics that plausibly account for a meaningful share of express cost, and quick commerce's effect on parcel mix each deserve more than they got. Scope was fixed before drafting.

---

## 65. Appendix

**A · Source conflicts (4 logged)**

| # | Conflict | Resolution |
|---|---|---|
| A-1 | **EBITDA vs adjusted EBITDA** — reported EBITDA ₹156 Cr (5.3%) sits *above* the disclosed adjusted EBITDA of ₹76 Cr (2.6%), the reverse of the usual relationship | Both reported as disclosed. All margin comparisons in this case study use the EBITDA line and its stated 6.5% prior-year margin, and no derivation mixes the two definitions |
| A-2 | **Ecom integration cost** — earlier guidance of ~₹300 Cr total, later "marginally lower", against ₹22 Cr (Q4 FY26) and ₹17 Cr (Q1 FY27) quarterly figures | Quarterly figures used for the ₹17 Cr ÷ ₹59 Cr derivation; the total-cost guidance is cited only as context |
| A-3 | **Q1 FY26 comparatives** — segment revenue and volume for the prior year are back-derived from disclosed YoY growth percentages, which are rounded | Derivations shown in `verify.py`; all bps and percentage results should be read to ~0.2pp, not to the decimal (Assumption A4) |
| A-4 | **Blue Dart PAT** — reported variously as ₹86.7 Cr and ₹88.5 Cr depending on standalone versus consolidated basis | The standalone figure (₹86.7 Cr) is used in every derivation; the ratio to Delhivery's PAT is 2.71× on that basis |
| A-5 | **Segment sum and cost base** — the four disclosed segment lines sum to ₹2,733 Cr against ₹2,931 Cr of services revenue (a ₹198 Cr, 6.76% residual), and freight/handling/servicing of ₹2,152 Cr is stated as "71.4% of revenue" but is 73.42% of services revenue and 70.67% of total income | Residual reported as unallocated rather than assigned to a segment; the cost ratio is recomputed against services revenue and the disclosed figure noted. Neither is used as a load-bearing input |

**B · Evidence grades**

🟢 **High** — stated directly in a Delhivery or Blue Dart results disclosure, an exchange filing, or a government record.
🟡 **Medium** — derived here from two or more 🟢 figures, with the derivation in `verify.py` and ASSUMPTIONS Part 2.
🟠 **Low** — single secondary source, no primary corroboration found.
🔴 **Conflicting** — sources disagree; logged above and never used as a load-bearing input.

**C · Author-constructed content**

All personas (§20), the quoting wireframe (§52), RICE inputs (§47), the Delhivery Floor proposal (§50) and its PRD (§51) are constructed by the author and are **not** Delhivery artefacts. The full list, with reasoning, is in `ASSUMPTIONS.md` Part 3.

**D · Asset status**

No screenshots, logos or diagrams are reproduced. Recommended additions if visual assets are later sourced under appropriate rights: a two-line chart of express shipment growth against realisation per shipment; a bar chart of input growth rates showing partner agents at 58.48% against every owned input at 14–18%; and the Delhivery-versus-Blue-Dart volume-and-profit contrast as a single four-bar figure. No AI-generated imitation of either company's product screens should be used.

---

*Day 58 of 90 · [← Day 57 — Policybazaar](../Day-57-Policybazaar) · Day 59 →*
