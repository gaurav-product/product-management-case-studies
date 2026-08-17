# Ola — The Company That Lost the Commission War

### Day 51 of 90 · Product Management Case Study Series

> **The thesis of this case study:** Ola was India's ride-hailing pioneer and, for over a decade, its market leader. In FY25, its ride-hailing arm's revenue fell 42% to ₹1,171 Cr, its standalone loss doubled to ₹662 Cr, its consolidated loss reached ₹1,975 Cr, Moody's downgraded its parent's credit rating, and its own annual report disclosed months-late filings and an auditor change — and the company is preparing an IPO anyway. The conventional read is competitive intensity: Uber and now Rapido out-executed Ola on the rider side. The evidence points somewhere more specific. In November 2022, a small Bengaluru open-network experiment called Namma Yatri proved that autorickshaw drivers would rather pay a flat daily fee than a 20–30% per-ride commission — and would work harder, cancel less, and stay loyal to whichever platform let them keep 100% of the fare. Rapido copied the model, scaled it nationally, and in barely two years went from a bike-taxi niche player to India's largest ride-hailing app by monthly active users — reportedly ~74 million by February 2026, more than Uber and Ola's user bases combined. Ola and Uber both still run the commission model that built them. This case study's finding: **Ola's crisis is a supply-side economics problem wearing a demand-side costume.** Riders didn't leave Ola because the app got worse. Drivers left first, ETAs got worse, and riders followed the drivers to Rapido. The fix Ola has not tried at scale is the one its ex-driver base already voted for with its feet.

---

## 2. Repository Metadata

| Field | Value |
|---|---|
| **Case study** | Day 51 of 90 |
| **Product** | Ola (Ola Consumer / ANI Technologies) — ride-hailing, mobility, and financial services app |
| **Company** | ANI Technologies Pvt. Ltd. (Ola Consumer), Bengaluru; sister company Ola Electric Mobility Ltd. (listed, Aug 2024) |
| **Domain** | Mobility / ride-hailing |
| **Primary competitors** | Uber, Rapido, Namma Yatri / open-network apps, BluSmart, inDrive |
| **Analysis type** | Research-led product teardown + financial reconstruction + a feature proposal |
| **Proposed system** | **Ola Fair Fare** — a driver-choice commission-vs-subscription toggle piloted in high-Rapido-penetration micro-markets |
| **Author** | Gaurav Singh |
| **Date of analysis** | 17 August 2026 |
| **Research boundary** | Public sources only — RoC/annual-report filings coverage, trade press, market trackers. No Ola employee, internal document, or authenticated session was consulted. |
| **Latest financials available** | FY25 (year ended 31 March 2025), disclosed in ANI Technologies' annual report filed with the RoC in May 2026 |

---

## 3. Badges

![Case Study](https://img.shields.io/badge/Case%20Study-Day%2051%20of%2090-blue)
![Domain](https://img.shields.io/badge/Domain-Mobility-orange)
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

Ola (ANI Technologies, trading as Ola Consumer) was India's first big ride-hailing success story — founded in 2010 by Bhavish Aggarwal and Ankit Bhati, and the undisputed market leader until Uber overtook it in 2023. Since then the decline has been steep and is now visible in audited numbers, not just app-store rankings.

FY25 standalone revenue fell **42% year-on-year to ₹1,171 Cr**, down from over ₹2,000 Cr. Mobility-segment revenue specifically fell from ₹1,761 Cr to about ₹925 Cr — nearly a 47% drop. Standalone loss **doubled to ₹662.4 Cr** from ₹328.7 Cr. Consolidated losses reached **almost ₹1,975 Cr**, swollen further by a markdown of over ₹1,300 Cr on the value of ANI Technologies' stake in its sister company Ola Electric between August 2024 and March 2025. Moody's downgraded ANI Technologies' credit rating with a negative outlook in November 2025, citing weakening operating performance and liquidity strain. The FY25 annual report itself was filed months after the statutory deadline, alongside an auditor change — governance signals that compound, rather than merely accompany, the financial ones. Despite all of this, the board approved and the company began formal steps toward an IPO in 2026.

The standard explanation is "Ola lost to better competitors." That's true, but it skips the mechanism. In November 2022, Namma Yatri — a small, ONDC-backed, Beckn-protocol open-network app for Bengaluru autorickshaws — proved something specific: drivers who could pay a flat daily fee (₹25 for autos, ₹90 for cabs) and keep 100% of every fare, instead of paying a platform 20–30% commission per ride, were dramatically happier, cancelled fewer rides, and stayed loyal. Rapido, which had built its early business the same commission way Ola and Uber did, noticed, piloted the subscription model, and by 2023–24 had rebuilt its cab and auto business on top of it. The results compounded: by early 2024, Rapido had already overtaken Uber in monthly active users; by February 2026, industry trackers put Rapido at roughly **74 million MAUs**, ahead of Uber's ~38 million and Ola's ~26–27 million — meaning Rapido's user base alone now reportedly exceeds Uber's and Ola's combined. Segment-level share estimates (which vary by tracker and should be read as bands, not precise figures — Appendix A) put Ola around 26–34% in cabs and autos, well behind Uber, with Rapido closing fast or already ahead depending on the city and vehicle category.

This case study's argument: the causal arrow runs supply-to-demand, not demand-to-supply. **Drivers moved first**, because the subscription model let them keep more of what they earned. Once drivers moved, ETAs on Ola got longer and acceptance rates got worse, and *that* is what riders actually experienced and responded to — not a features gap, a marketing gap, or a pricing gap on the rider side. Ola's own growth playbook in FY24–25 (Prime Plus premium rides, Ola Coin cross-platform rewards, an aborted expansion into quick commerce that it has since exited) has been aimed almost entirely at the rider side of the marketplace, while the supply side kept eroding underneath it.

The proposal in §50 — **Ola Fair Fare** — does not ask Ola to abandon commissions everywhere at once (a national switch that size would be reckless given the company's current liquidity position, per Moody's own concern). It proposes piloting a driver-choice toggle between the existing commission model and a flat-subscription alternative, starting in the specific micro-markets — auto and bike-taxi corridors in cities where Rapido's share has grown fastest — where the supply-side bleed is most acute and cheapest to test.

---

## 6. Product Overview

Ola is a mobile app offering on-demand rides across cars (Micro, Prime, Prime Plus, Rentals, Outstation), autorickshaws, and bike taxis, alongside financial-services and rewards features (Ola Coin, launched August 2024, spanning mobility, e-commerce, and logistics use). The company has cycled through several adjacent-category bets — cloud kitchens, quick commerce (entered, then exited) — none of which became a durable second pillar, in contrast to how the core ride-hailing business itself has structurally weakened.

---

## 7. Company Background

Founded 2010 in Mumbai (later headquartered in Bengaluru) by Bhavish Aggarwal and Ankit Bhati as Olacabs. Grew via aggressive city expansion and driver acquisition to become India's largest ride-hailing platform through the 2010s, fending off Uber's India entry for years. Diversified into electric vehicles from 2017, acquiring Dutch e-scooter maker Etergo BV in 2020 and building Ola Electric into India's largest e-scooter manufacturer by market share; Ola Electric listed on NSE/BSE in August 2024. The core ride-hailing business rebranded from "Ola Cabs" to **"Ola Consumer"** around 2024–25 to reflect the (short-lived) expansion into financial services, cloud kitchens, and quick commerce — the company has since exited quick commerce. Uber overtook Ola as India's top ride-hailing app by user metrics in 2023; Rapido overtook both in MAUs by 2024–2026 (§14).

---

## 8. Product Timeline

| Year | Milestone |
|---|---|
| 2010 | Founded as Olacabs |
| 2017 | Enters EV two-wheeler segment (Ola Electric) |
| 2020 | Acquires Etergo BV (Netherlands) |
| 2021 | Raises $500M term loan; enters quick commerce (later exited) |
| 2022 (Nov) | Namma Yatri launches in Bengaluru with a flat-fee, zero-commission driver model (not an Ola product, but the structural turning point for the whole category) |
| 2023 | Uber overtakes Ola as India's #1 ride-hailing app by user metrics; Rapido enters cab aggregation (Dec) |
| 2024 (Jan) | Rapido overtakes Uber in Android MAUs |
| 2024 (Feb) | ANI Technologies FY24 results: Ebitda-positive mobility + financial-services segments, revenue down 21% |
| 2024 (Aug) | Ola Electric IPO; Ola Coin rewards programme launched |
| 2025 (Nov) | Moody's downgrades ANI Technologies, negative outlook |
| 2026 (May) | FY25 annual report filed (late) with ROC: revenue −42%, standalone loss doubles, consolidated loss ≈₹1,975 Cr; board approves IPO process |
| 2026 (Feb) | Rapido reportedly reaches ~74M MAUs, ahead of Uber (~38M) and Ola (~26–27M) combined |

---

## 9. Vision & Mission

Ola's public positioning has historically centred on being India's homegrown mobility platform — "building for India" — expanding beyond cabs into the full spectrum of urban mobility and, through Ola Electric, into vehicle manufacturing itself. The FY24 rebrand to "Ola Consumer" signalled an ambition to become a broader consumer platform (mobility + financial services + commerce), an ambition this case study's evidence suggests was pursued at the expense of defending the core ride-hailing marketplace.

---

## 10. Problem Statement

**For the company:** Ola is losing the two-sided marketplace competition on the side that matters more structurally — driver supply — while its strategic attention and product investment (Prime Plus, Ola Coin, adjacent categories) has gone almost entirely to the rider side.

**For the user (rider):** longer wait times and lower ride availability versus Rapido in the exact categories (autos, bike taxis, and increasingly cabs) where Rapido's driver-friendly economics have pulled supply away.

**For the user (driver):** a commission structure that, per Rapido's own account of the shift, left many drivers "working 12–14 hours a day just to maintain earnings" — a real cost that a subscription-fee alternative directly addresses.

---

## 11. Market Research

Market-size estimates for India's taxi/ride-hailing sector vary widely by methodology and scope: Mordor Intelligence puts the India taxi market at $13.75B in 2026 (growing to $31.4–34.3B by the early 2030s per different Mordor-family reports); Persistence Market Research estimates $23.7B in 2026 growing to $49.9B by 2033; a narrower India-specific ride-hailing-only estimate puts the market closer to $950M (FY24) growing at ~19% CAGR. These are not reconcilable without knowing each report's exact scope (offline taxis included or not; ride-hailing vs. total taxi; corporate/institutional included or not) — treated here as a wide directional band, not a precise figure (Appendix A).

---

## 12. Industry Analysis

What is *not* ambiguous across sources: the two-player duopoly (Ola + Uber, once >90% combined share) has broken down to roughly 60–70% combined, with Rapido taking the balance and growing fastest of the three. Rapido's rise tracks almost exactly with its 2023–24 adoption of the Namma Yatri-style subscription model — first in autos and bike taxis, then extended into cabs from December 2023. Other open-network apps (Namma Yatri itself, Yatri Saathi, Odisha Yatri, Kerala Savaari) remain regionally significant but have not achieved Rapido's national scale, suggesting the model needed Rapido's existing driver base and marketing muscle to generalise — not just the model itself.

---

## 13. TAM / SAM / SOM

### 13.1 TAM
India taxi/ride-hailing market, 2026: **a wide band, roughly $13.75B–$23.7B**, depending on scope (Appendix A-1). This document uses the band rather than a single figure.

### 13.2 SAM
Ola's addressable share given its current segment presence (cabs, autos, some bike-taxi): using the cabs/autos share bands from §14 (Ola ~26–34% of cabs, ~26% of autos, depending on tracker), Ola's realistic served-addressable market sits well below its historic near-50% share of the pre-Rapido duopoly.

### 13.3 SOM — financial reconstruction

| Metric | FY23 | FY24 | FY25 |
|---|---|---|---|
| ANI Technologies standalone revenue | ₹2,135 Cr | ₹1,906 Cr | ₹1,171 Cr (per Ola Consumer parent-level reporting, down 42% YoY) |
| Ola Consumer revenue (segments incl. other income) | ₹3,000 Cr | ₹2,368 Cr | (see standalone above) |
| Mobility-segment revenue | — | ₹1,761 Cr | ₹925 Cr |
| Standalone net loss | — | ₹328.7 Cr | ₹662.4 Cr |
| Consolidated net loss | — | Ebitda-positive (mobility + fin. services) | ≈₹1,975 Cr |
| Full-year Ebitda (excl. discontinued ops) | ₹87 Cr | ₹271 Cr | Not confirmed positive in FY25 reporting reviewed |

### 13.4 The Ola Electric stake markdown
Roughly **₹1,300 Cr** of ANI Technologies' FY25 consolidated loss is attributable to a markdown in the value of its Ola Electric shareholding between August 2024 and March 2025 — a reminder that the parent's headline loss figure is not purely an operating story; it is partly a mark-to-market story about a *different*, also-struggling business (§13.5, ASSUMPTIONS.md A2).

### 13.5 Ola Electric, for context (a related but distinct listed entity)
FY24 revenue ₹5,010 Cr, loss ₹1,584 Cr → FY25 revenue ₹4,514 Cr (down), loss ₹2,276 Cr (up). Auditors flagged going-concern language given FY25 negative operating cash flow of ₹2,391 Cr. Q1 FY26 showed the first signs of operational improvement: revenue still down ~50% YoY to ₹828 Cr, but auto-segment EBITDA turned positive (+11.6%) on the back of a cost-cutting programme ("Project Lakshya") that cut monthly auto opex from ₹178 Cr to ₹105 Cr.

---

## 14. Competitor Analysis

| Dimension | Uber India | Rapido | **Ola** |
|---|---|---|---|
| MAUs (~Feb 2026, Ascendants/India Dispatch chart) | ~38M | **~74M** | ~26–27M, flat-to-declining |
| Driver economics | Commission model | **Flat subscription / zero-commission** (Namma Yatri-inspired, adopted 2023) | Commission model |
| Cabs share (est., varies by tracker) | ~50% | ~14–18% (Motilal Oswal) or ~14% (Equentis) | ~14–18% or ~34% depending on tracker — flagged conflict |
| Autos share (est.) | ~40% | Fast-growing, second-largest | ~26% |
| Bike taxis | Smaller presence | **Dominant**, origin category | Smaller presence |
| Listed / IPO status | Global public co. | Private, Prosus-backed | IPO process begun 2026 amid weak financials |

The two cab-share figures for Ola (14–18% vs 34%) come from different trackers using different methodologies (Motilal Oswal brokerage estimate vs a separate industry blog citing "recent industry estimates") and are carried as a genuine open conflict rather than resolved (Appendix A-2) — but every source agrees on direction: Ola has fallen from co-leader to a clear third.

---

## 15. SWOT

| Strengths | Weaknesses |
|---|---|
| Long-standing brand recognition, first-mover legacy | Revenue collapsing (−42% FY25), losses doubling |
| Vertically integrated with Ola Electric for EV fleet strategy | Driver-side economics actively pushing supply to a competitor |
| Financial-services segment showed EBITDA profitability in FY24 | Governance concerns: late filings, auditor change, credit downgrade |
| Diversified brand (mobility + EV) gives optionality | Diversification (quick commerce) already tried and abandoned |

| Opportunities | Threats |
|---|---|
| Driver-side model largely unexplored by Ola at scale | Rapido's MAU lead compounding — network effects favour whoever has denser driver supply |
| IPO capital, if raised, could fund a genuine supply-side fix | Moody's downgrade raises cost of capital right when it's needed most |
| Financial-services cross-sell to existing large rider base | Uber has resources to also adopt subscription economics if Ola doesn't move first |

---

## 16. Porter's Five Forces

| Force | Intensity | Note |
|---|---|---|
| Competitive rivalry | Very high | Three-plus credible players, converging on the same categories |
| Threat of new entrants | Medium | BluSmart (EV-only), inDrive (haggling model), regional open-network apps continue to enter |
| Bargaining power of suppliers (drivers) | **High and rising** | Namma Yatri/Rapido proved drivers will move for better take-home economics — this is the central force this case study addresses |
| Bargaining power of buyers (riders) | High | Zero switching cost; riders follow availability and price, not brand loyalty |
| Threat of substitutes | Medium | Personal vehicles, public transit, and (in some cities) state-backed platforms (e.g., BHARAT TAXI, launched Jul 2026 in Maharashtra) |

---

## 17. Business Model Canvas

| Block | Summary |
|---|---|
| Key Partners | Drivers/fleet operators, financial-services partners, Ola Electric (vehicle supply) |
| Key Activities | Ride matching, pricing, driver onboarding/incentives, financial-services cross-sell |
| Value Propositions | Broad vehicle-type coverage (cars, autos, bikes), integrated rewards (Ola Coin), premium tiers (Prime Plus) |
| Customer Relationships | App-native; driver relationship historically commission-based, increasingly adversarial per trade coverage of driver sentiment |
| Customer Segments | Urban riders across price tiers; drivers/captains as a distinct, currently under-served segment |
| Channels | Mobile app |
| Key Resources | Brand, historical driver network (eroding), rider base, capital (constrained per Moody's) |
| Cost Structure | Driver incentives/subsidies, technology, marketing, corporate overhead |
| Revenue Streams | Ride commissions, convenience fees, financial-services fees, advertising |

---

## 18. Revenue Model

Ola's "sale of services" line — ride commissions and convenience fees — was reported at roughly ₹1,093 Cr in FY25, the core of its standalone revenue. The commission model is also, per this case study's central argument, the specific mechanism actively driving supply away. This is a structurally uncomfortable position: **the revenue line and the retention problem are the same line.** Any fix that reduces commission take-rate to retain drivers directly reduces near-term revenue — which is exactly why Ola has not made the switch on its own, and exactly why a bounded pilot (§53) rather than a blanket change is the responsible way to test it.

---

## 19. Target Users

- **Price- and time-sensitive urban commuters** (bike taxi, auto) — the segment where Rapido's model has already won decisively.
- **Premium/comfort riders** (Prime Plus) — the segment Ola has invested in most, and the smallest by volume.
- **Drivers/captains** — the segment this case study argues has been under-served relative to its structural importance to marketplace health.

---

## 20. Personas

**Persona — Suresh, 34, Bengaluru, auto driver (Construct)**
Previously exclusive to Ola/Uber under commission. Switched primary allegiance to Rapido after trying the flat-fee model; reports keeping the full fare instead of ~20–25% commission, and working fewer hours for similar take-home pay. Still keeps Ola installed as a backup, not a primary earning source.

**Persona — Priya, 27, Pune, daily office commuter (Construct)**
Opens whichever app shows the shortest ETA and best price at the moment of booking — genuinely multi-homing across Ola, Uber, and Rapido. Has no loyalty to any one brand; her behaviour is a direct read-out of wherever driver supply is currently strongest.

**Persona — Bhavish's dilemma, as a stand-in for Ola's internal decision-maker (Construct, illustrative not a real individual)**
Aware that a commission cut would help supply but hurt already-fragile near-term revenue and investor confidence right before an IPO — the exact tension this case study's proposal is designed to de-risk through a bounded pilot rather than a full switch.

---

## 21. Jobs to Be Done

- Rider: "Get me a ride, fast, at a fair price, right now." (served best by whichever platform has denser driver supply at that moment — currently, increasingly, not Ola)
- Driver: "Let me keep more of what I earn without working longer hours." (served by Rapido/Namma Yatri-style subscription; **not currently served by Ola**)
- Ola (company): "Grow revenue without further destabilising an already-downgraded balance sheet." (in direct tension with the driver JTBD, since commission is Ola's main revenue line)

---

## 22. User Journey (driver side, current)

`Onboard → accept rides → pay ~20–25% commission per ride → income variable, hours long → notice Rapido's flat-fee alternative → trial Rapido → migrate primary allegiance → keep Ola only as backup`

---

## 23. User Flow

`Rider opens app → requests ride → matched to nearest available driver → driver accepts/declines → ride completed → Ola takes commission → driver paid net of commission`

**Gap:** no branch exists for a driver to opt into a flat-fee-instead-of-commission model within Ola's own flow (Construct — this is what §50 proposes adding).

---

## 24. Information Architecture

`Home → Book a ride (Car / Auto / Bike) → Prime Plus / Rentals / Outstation → Ola Coin → Wallet / Payments → Driver app (separate)`

**Gap:** the driver-side app's earnings/incentive settings, as publicly described, do not surface a subscription-vs-commission choice.

---

## 25. UX Audit

| Area | Observation |
|---|---|
| Rider booking flow | Category-standard, no major public complaints distinct from peers |
| ETA reliability | Reported by multiple trade sources as having degraded relative to Rapido in bike-taxi/auto categories, consistent with a supply-side (not app-quality) explanation |
| Driver earnings transparency | Commission-based; less transparent take-home visibility than a flat daily-fee model by construction |

---

## 26. UI Audit

Not independently screenshot-audited (public-sources-only boundary; Appendix D).

---

## 27. Accessibility

Not independently tested in this analysis; flagged as a research-boundary gap.

---

## 28. Feature Breakdown

| Feature | Status | Notes |
|---|---|---|
| Prime Plus (premium rides) | Live | Rider-side investment |
| Ola Coin (cross-platform rewards) | Live, since Aug 2024 | Rider-side investment |
| Quick commerce | **Exited** | A diversification bet that did not stick |
| Driver subscription/flat-fee option | **Does not exist** | The gap this case study's proposal fills |

---

## 29. AI Capabilities

Public product coverage does not describe a defining consumer-facing AI feature inside the Ola ride-hailing app itself in the research window (Ola founder Bhavish Aggarwal's separate AI venture, Krutrim, is a distinct company and out of scope for this app-focused analysis).

---

## 30. Product Metrics

| Metric | FY24 | FY25 |
|---|---|---|
| Standalone revenue | ₹1,906 Cr | ₹1,171 Cr (−42%) |
| Mobility-segment revenue | ₹1,761 Cr | ₹925 Cr (−47%) |
| Standalone net loss | ₹328.7 Cr | ₹662.4 Cr (+102%) |
| Consolidated net loss | Ebitda-positive core segments | ≈₹1,975 Cr |
| Tech infrastructure spend | — | ₹303 Cr |
| MAUs (industry tracker estimate, Feb 2026) | — | ~26–27M, down from prior-year levels |

---

## 31. North Star Metric

**Driver Take-Home Parity Rate** *(Construct — does not exist at Ola)*: the share of active drivers on Ola whose effective take-home per hour is at or above what a comparable driver earns on Rapido's flat-fee model in the same city and vehicle category. A North Star deliberately built around the supply side, on the theory (A1, ASSUMPTIONS.md) that rider-side metrics (bookings, GMV) are lagging indicators of a driver-side cause.

---

## 32. Product Analytics

Three analytics objects this proposal would require (Constructs, do not currently exist publicly):
1. **Subscription Opt-In Rate** — share of eligible drivers in a pilot micro-market choosing flat-fee over commission.
2. **Driver Retention Delta** — 30/60/90-day driver retention, subscription cohort vs commission cohort.
3. **Rider ETA Delta** — average rider wait time in pilot zones, before vs after driver-side change.

---

## 33. AARRR Framework

| Stage | Current state | Gap this proposal targets |
|---|---|---|
| Acquisition (riders) | Multi-homing, low loyalty | Indirectly improved via better ETAs |
| Activation | Standard booking flow | Not targeted |
| Retention (drivers) | **Actively eroding**, per MAU and share trends | **Directly targeted** |
| Referral | Not a major public feature | Not targeted |
| Revenue | Commission-dependent, shrinking | Trade-off explicitly modelled in §57 |

---

## 34. HEART Framework

| Dimension | Current (driver side) | With Ola Fair Fare |
|---|---|---|
| Happiness | Reported driver dissatisfaction with commission hours (Rapido's own account of the shift) | Targeted improvement via take-home control |
| Engagement | Declining primary-platform allegiance | Subscription opt-in as a new engagement signal |
| Adoption | N/A (feature doesn't exist) | Tracked from pilot launch |
| Retention | Eroding to Rapido | Direct target metric |
| Task success | Ride completion rate | Add cancellation-rate delta by cohort |

---

## 35. Growth Strategy

Ola's disclosed growth activity in FY24–25 (Prime Plus, Ola Coin, quick commerce) was rider- and adjacency-facing. This case study does not argue those bets were wrong in themselves — it argues they were prioritised over a cheaper, more directly causal fix on the supply side, and that the IPO process now underway is the moment to correct that ordering before, not after, more capital is raised on the strength of a growth story that hasn't addressed its root cause.

---

## 36. Growth Loops

**Current (broken) loop:** Commission funds rider incentives → incentives attract riders → riders need drivers → drivers leave for better take-home elsewhere → fewer drivers → worse ETAs → riders leave too.

**Proposed loop (Construct):** Flat-fee option retains/attracts drivers → denser driver supply improves ETAs → better ETAs attract/retain riders without needing rider-side subsidy → higher ride volume offsets lower per-ride take, at least in pilot zones where the take-rate is already being lost to Rapido anyway.

---

## 37. Network Effects

Ride-hailing marketplaces have classic two-sided network effects: denser driver supply improves rider experience, which increases ride volume, which improves driver utilisation. Ola's current trajectory is this loop running in reverse. The core strategic insight of this case study is that **the loop can only be reversed from the supply side** — no amount of rider-side spend (Prime Plus, Ola Coin) fixes an ETA problem caused by driver attrition.

---

## 38. Product Strategy

| Position | Description | Assessment |
|---|---|---|
| A — Defend rider side | More rider incentives, premium tiers, rewards | Current default; addresses a symptom, not the cause |
| B — Full commission-to-subscription switch, nationally | Match Rapido's model everywhere at once | High-risk given Ola's current liquidity and credit position (Moody's downgrade) |
| **C — Bounded driver-choice pilot (recommended)** | Offer flat-fee as an *option* in specific high-Rapido-penetration micro-markets first | Cheapest to test, directly addresses the causal mechanism, protects revenue elsewhere |

---

## 39. Monetization

### 39.1 Current
Ride commissions (~20–25% per ride, standard industry range, per Forbes India's account of the pre-Rapido model), convenience fees, financial-services fees, advertising.

### 39.2 The tension this proposal is explicit about
A flat driver fee is, per ride, a *smaller* revenue line for Ola than a percentage commission on all but the lowest-fare rides — which is exactly why this is not proposed as a blanket switch. It is proposed as an option **only where Ola is already losing effectively 100% of the commission it would otherwise earn**, because the driver has already left for Rapido. In those specific micro-markets, a smaller flat fee from a retained or won-back driver is strictly better than 25% of nothing.

### 39.3 Ola Fair Fare pricing construct
Drivers in pilot zones choose, per week: (a) standard commission (~20–25%, unchanged), or (b) a flat daily fee (city-and-vehicle-type calibrated, deliberately priced in line with what Namma Yatri/Rapido already charge locally, so the choice is genuinely about Ola vs. the competitor rather than about Ola undercutting the category).

---

## 40. Trust & Safety

Not a major distinct public controversy area for Ola's rider-side product in this research window; the governance concerns identified (late filings, auditor change, credit downgrade) sit at the corporate-financial level (§57, R1) rather than the product-safety level.

---

## 41. Technical Architecture *(Construct — reconstructed from public description)*

```
Rider App → Matching Engine → Driver App
                  ↓
        Pricing/Commission Engine
                  ↓
      Driver Earnings & Payout Service
```

Ola Fair Fare would add a **Driver Compensation Preference Service** feeding the Pricing/Commission Engine, letting the matching and payout logic branch per driver based on their chosen model — an incremental addition to existing payout infrastructure, not a rebuild.

---

## 42. Data Flow *(Construct)*

`Driver selects weekly compensation preference → preference stored → each completed ride checks preference → commission deducted OR flat-fee ledger updated → weekly settlement reflects chosen model`

---

## 43. API Ecosystem

No major public developer-facing API programme is a defining part of Ola's rider-facing product surface in this research window.

---

## 44. Privacy & Security

Not independently audited in this analysis. A driver-compensation-preference feature would need standard payout-and-earnings data handling; no Ola-specific practice was evaluated here (public-sources-only boundary).

---

## 45. Pain Points

1. **Driver attrition to a structurally better-paying competitor** — the root cause this case study focuses on.
2. **Revenue and loss both deteriorating badly in the same year** (§13.3) — not a growth-investment story like some peers in this series; a genuine share-loss story.
3. **Governance overhang** (late filings, auditor change, credit downgrade) arriving at the same time as an IPO push — a credibility problem layered on a financial one.
4. **No product response yet to the specific mechanism (commission vs. subscription) that reporting consistently identifies as Rapido's structural advantage.**

---

## 46. Opportunity Mapping

Four independent lines of evidence converge: (1) the financial line (revenue and loss both worsening sharply, unlike a "growth investment" story); (2) the competitive line (Rapido's rise tracks specifically with its subscription-model adoption, not general execution); (3) the MAU line (Ola's user base is flat-to-declining while Rapido's has grown fastest of any player); (4) the product-gap line (no driver-side compensation choice exists in Ola's public product surface, despite this being the exact lever competitors used to win supply).

---

## 47. RICE Prioritisation

| Feature | Reach | Impact | Confidence | Effort | RICE | Stressed RICE* |
|---|---|---|---|---|---|---|
| **Ola Fair Fare (driver-choice pilot)** | 6 | 9 | 6 | 6 | 54 | 32.4 |
| More rider-side incentives (status quo) | 8 | 4 | 8 | 4 | 64 | 38.4 |
| Full national commission-to-subscription switch | 10 | 9 | 3 | 9 | 30 | 18 |
| Expand Prime Plus premium tier | 4 | 5 | 7 | 5 | 28 | 16.8 |

*Stress rule (Construct, consistent with the series' methodology): reach × 0.6, confidence − 20pp.

Status-quo rider incentives score highest on stressed RICE precisely because they're cheap and familiar to execute — which is exactly why they've been the default despite not addressing the root cause. Fair Fare is recommended on strategic grounds (§46), not because it wins the prioritisation exercise outright.

---

## 48. MoSCoW

| Must | Should | Could | Won't (v1) |
|---|---|---|---|
| Weekly compensation preference toggle | Local-market-calibrated flat-fee pricing | Driver dashboard comparing take-home under each model | National rollout (v1 = pilot zones only) |
| Payout logic supporting both models | Migration path back to commission if a driver changes their mind | Gamified incentives for high performers under flat-fee | Blending both models within a single ride |

---

## 49. Kano Analysis

| Feature | Category |
|---|---|
| Ride matching, ETA | Basic (expected) |
| Ola Coin rewards | Performance |
| Driver compensation choice | **Attractive to drivers, currently unique to Ola if shipped before Uber matches it** |
| Rider-visible "committed driver supply" indicator | Attractive, second-order effect of the above |

---

## 50. Feature Proposal — Ola Fair Fare

**What it is:** a driver-facing weekly toggle between the existing commission model and a locally calibrated flat daily/weekly fee, piloted first in micro-markets (specific city + vehicle-category combinations) where Rapido's share has grown fastest and where Ola's commission revenue from those drivers is already effectively lost to attrition.

**Why now:** every line of evidence in §46 converges on the same mechanism, and Ola's own diversification bets have not touched it. The IPO process gives the company a natural moment to show investors it understands the causal story, not just the symptom.

**What it is not:** a national commission cut, a rider-side discount programme, or a claim that Rapido's entire success is attributable to this one lever (execution, marketing, and timing matter too — flagged in ASSUMPTIONS.md A3).

**User impact:** drivers in pilot zones gain a genuine choice and, per the Rapido/Namma Yatri precedent, likely better take-home for comparable hours; riders in those zones should see improved ETAs as supply stabilises.

**Business impact:** near-term revenue-per-ride likely falls in the pilot cohort; the bet is that retained/won-back ride *volume* more than offsets this specifically in zones where the alternative is currently zero revenue from an already-departed driver.

**Trade-offs:** cannibalises existing commission revenue from drivers who would have stayed anyway without the option; requires new payout infrastructure; success is not guaranteed to generalise beyond the specific micro-markets tested.

---

## 51. PRD — Ola Fair Fare v1

### 51.1 Problem
Ola's driver base is migrating to a flat-fee competitor faster than rider-side incentives can compensate for, and no product response currently exists.

### 51.2 Goals
- Pilot in 2–3 cities, in the specific vehicle categories (auto, bike taxi) where Rapido's share gains have been steepest.
- Reach a Subscription Opt-In Rate of ≥15% of eligible drivers within 60 days.
- Reduce Driver Retention Delta gap versus estimated Rapido retention by a measurable margin within 90 days (exact target set after Phase 0 baseline, §53).

### 51.3 Non-goals (v1)
Not a national rollout; not extended to premium car categories (Prime Plus) where commission economics are least contested; not a permanent one-way switch — drivers can revert.

### 51.4 User stories
- As a driver, I can choose a flat weekly fee instead of commission and see clearly what I'll owe either way before committing.
- As a driver, I can switch back to commission the following week if the flat fee doesn't work for me.
- As Ola, I can measure, per pilot zone, whether driver retention and rider ETAs improve.

### 51.5 Acceptance criteria (Constructs — author-set bars)
- A1: Payout accuracy for flat-fee drivers ≥ 99.5% (no earnings-calculation disputes above baseline).
- A2: Rider ETA in pilot zones improves measurably (direction, not a specific percentage, set as the bar pending Phase 0 baseline).
- A3: No degradation in commission-cohort driver experience in the same zones (the pilot must not make things worse for drivers who don't opt in).

---

## 52. Wireframes *(ASCII, Constructs)*

```
┌─────────────────────────────────┐
│  How would you like to earn      │
│  this week?                      │
│                                   │
│  ( ) Commission — 20% per ride    │
│      Pay only when you earn       │
│                                   │
│  ( ) Flat Fee — ₹99/day           │
│      Keep 100% of every fare      │
│                                   │
│  [   Confirm my choice   ]        │
└─────────────────────────────────┘
```

---

## 53. Rollout Plan

| Phase | Scope | Gate |
|---|---|---|
| Phase 0 | Baseline driver-attrition and ETA data in 2–3 candidate cities, before any product change | If attrition isn't concentrated in the categories this proposal targets, re-scope |
| Phase 1 | Launch driver-choice toggle, 2–3 cities, auto + bike taxi only | §51.5 acceptance criteria |
| Phase 2 | Extend to cabs in the same cities if Phase 1 holds | Retention and ETA deltas hold |
| Phase 3 | Expand city list based on where Rapido share is highest | Net revenue-per-zone impact assessed before any national decision |

---

## 54. A/B Testing

**Arm A (control):** commission only, unchanged. **Arm B:** driver-choice toggle offered. **Arm C (falsifier, Construct):** offer drivers a straightforward commission *discount* (e.g., 15% instead of 20–25%) with no subscription structure at all — designed to test whether drivers actually value the flat-fee *structure* (predictability, 100%-of-fare framing) or simply want a lower number, in which case a much simpler fix (just cut commission) would work without new payout infrastructure.

---

## 55. KPI Dashboard *(Construct)*

| KPI | Target |
|---|---|
| Subscription Opt-In Rate | ≥15% of eligible drivers, pilot zones, 60 days |
| Driver Retention Delta | Directional improvement vs. baseline, 90 days |
| Rider ETA (pilot zones) | Directional improvement vs. baseline |
| Payout accuracy | ≥99.5% |

---

## 56. Product Roadmap

`Q1: Phase 0 baseline → Q2: Phase 1 pilot (2–3 cities, auto/bike) → Q3: Phase 2 (extend to cabs) → Q4: Phase 3 decision gate, evaluate broader rollout ahead of/alongside IPO process`

---

## 57. Risks & Mitigation

| # | Risk | Mitigation |
|---|---|---|
| R1 | Revenue-per-ride decline compounds an already-downgraded credit position right before an IPO | Bound the pilot tightly (§53); measure net zone-level revenue, not just per-ride take |
| R2 | Drivers value a lower number, not the subscription structure (tested by Arm C, §54) | If Arm C wins, re-scope to a simpler commission cut |
| R3 | Cannibalisation — drivers who'd have stayed on commission anyway switch, reducing revenue with no retention gain | Target pilot zones specifically where attrition is already highest, minimising this risk |
| R4 | Governance/credibility concerns (late filings, auditor change) undermine investor confidence regardless of product fixes | Outside this proposal's scope; flagged as a separate, likely larger risk to the IPO than any single feature |

---

## 58. Future Vision

If Fair Fare works in pilot zones, its natural extension is a fully driver-choice-native compensation system across all vehicle categories, positioning Ola's core differentiation not as "which app has better rider features" but as "which platform genuinely competes for driver loyalty" — the axis this case study argues actually determined the last three years of category leadership.

---

## 59. PM Lessons

The lesson this case study keeps returning to: in a two-sided marketplace, a demand-side symptom (falling bookings, worse ETAs) can have a supply-side cause, and product teams that only have levers for the side they can see (the rider-facing app) will keep pulling those levers long after the evidence points elsewhere.

---

## 60. PM Interview Questions

1. Ola's bookings are falling. How would you determine whether this is a demand problem or a supply problem, using only data you could plausibly access?
2. Design an experiment to test whether drivers value a lower commission or a *differently structured* payout, holding expected take-home roughly constant.
3. A company's core revenue line is also its biggest retention risk (commission = revenue AND driver attrition driver). How do you sequence a fix without destabilising the business you're trying to save?

---

## 61. References

- ANI Technologies / Ola Consumer FY25 results: The Tech Portal, India IPO, Outlook Business (May 2026, citing RoC filings)
- ANI Technologies FY24 results: Business Standard (Feb 2025)
- Ola Electric FY24/FY25/Q1FY26 results: Autocar Professional, Business Standard (2025–2026)
- Rapido / Namma Yatri model and market-share reporting: Forbes India (Jul & Sep 2025), Storyboard18, Equentis, Ascendants, BIBS, AckoDrive, TechCrunch
- India taxi/ride-hailing market sizing: Mordor Intelligence, Persistence Market Research, TechSci Research, MarketsandData, Statista, Coherent Market Insights, Straits Research (various, 2025–2026)

---

## 62. About the Author

Written by Gaurav Singh as part of a 90-day product management case study series, applying a consistent research-led teardown methodology across Indian and global consumer products.

---

## 63. License

This document is an independent analysis for educational purposes. It is not affiliated with, endorsed by, or reviewed by Ola/ANI Technologies. All company names and trademarks belong to their respective owners.

---

## 64. Self Review

| Check | Status | Note |
|---|---|---|
| No fabricated data | ✅ | Every figure sourced or explicitly derived; constructed content in Appendix C |
| Facts separated from assumptions | ✅ | ASSUMPTIONS.md |
| Conflicts disclosed | ✅ | Appendix A |
| Falsification designed | ✅ | §53 Phase 0, §54 Arm C |
| Recommendation shown against a prioritisation framework rather than engineered to win | ✅ | §47 — Fair Fare does not top stressed RICE |

**Where this case study is weakest.** The causal claim — that driver attrition to Rapido's subscription model is the *primary* driver of Ola's rider-side decline, rather than one contributing factor among several (pricing, app quality, marketing spend, general competitive intensity) — is the load-bearing assumption of the entire document, and it rests on secondary reporting and directional MAU/share trackers rather than any data internal to Ola. Second, cab-share estimates for Ola conflict outright between sources (14–18% vs 34%) and this document could not resolve which is closer to correct. Third, the financial-services segment, which showed EBITDA profitability in FY24, receives almost no independent treatment here despite plausibly being relevant to how Ola could fund a driver-side pilot.

**What would change my mind.** Ola disclosing its own driver-retention data showing attrition is not concentrated where Rapido has gained share; a Phase 0 baseline (§53) finding no meaningful attrition-to-Rapido pattern; or Arm C (§54) showing drivers respond just as well to a simple commission cut, which would make the more complex dual-model proposal unnecessary.

---

## 65. Appendix

### Appendix A — Source Conflicts

| # | Conflict | Resolution |
|---|---|---|
| A-1 | India taxi/ride-hailing market size: estimates range from ~$13.75B (Mordor, 2026) to ~$23.7B (Persistence, 2026) to a much narrower ~$950M–$3.8B "ride-hailing only" estimate (MarketsandData) | Carried as a wide band throughout; likely reflects differing scope (taxi vs. ride-hailing, online vs. total) rather than genuine disagreement |
| A-2 | Ola's cab-market-share estimate: 14–18% (Motilal Oswal, via Forbes India) vs 34% (Equentis, citing "recent industry estimates") | Unresolved; both stated, direction (Ola well behind Uber, contested with Rapido) holds under either figure |
| A-3 | Ola Consumer FY24 total revenue: ₹2,368 Cr (segments incl. other income, Business Standard) vs standalone ANI Technologies revenue ₹1,906 Cr (same article, different line item) | Not a true conflict — different reporting scopes within the same filing; both stated with their scope labelled |

### Appendix B — Evidence Grades

| Grade | Meaning | Applied to |
|---|---|---|
| 🟢 High | RoC/annual-report filing, credit-rating action | FY25 revenue/loss figures, Moody's downgrade, Ola Electric audited results |
| 🟡 Medium | Trade press citing filings, consistent across sources | FY24 figures, Rapido/Namma Yatri model adoption timeline |
| 🟠 Low | Single-tracker MAU/share estimate | Cab/auto share percentages, MAU chart figures |
| 🔴 Conflicting | Sources materially disagree | Market size estimates, Ola cab-share figures |

### Appendix C — Author-Constructed Content

| # | Construct | Where |
|---|---|---|
| C1 | Ola Fair Fare — the entire proposal | §50 |
| C2 | Driver Take-Home Parity Rate (North Star) | §31 |
| C3 | Subscription Opt-In Rate, Driver Retention Delta, Rider ETA Delta | §32 |
| C4 | Personas Suresh, Priya, and the illustrative "Bhavish's dilemma" framing | §20 |
| C5 | All RICE inputs and the stress rule | §47 |
| C6 | Acceptance-criteria bars | §51.5 |
| C7 | The three-arm A/B design including Arm C as falsifier | §54 |
| C8 | Technical architecture and data-flow reconstructions | §41, §42 |
| C9 | The reading of Ola's rider-side investment as prioritised over supply-side fixes | §35, §46 |

### Appendix D — Asset Status

| Asset | Status |
|---|---|
| ASCII wireframes | ✅ Authored (§52) |
| Product screenshots | ❌ Not included — no authenticated session was used |
| UI/accessibility audit | ❌ Not independently tested — flagged as a research-boundary gap |

---

*Day 51 of 90 · ← [Day 50 — Zepto](../Day-50-Zepto) · [Day 52 →](../Day-52-Lenskart)*
