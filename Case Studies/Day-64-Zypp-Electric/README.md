# Day 64 — Zypp Electric: The Asset Company That Stopped Buying Assets

> Zypp Electric is described, funded and about to be listed as an EV-as-a-Service company. Its FY25 filings describe something else. The vehicle-rental line that carries that description is **25.35% of operating revenue and falling**, and supplied **18.53%** of the year's growth. The delivery-services line that supplied **79.85%** carries a direct rider cost of **₹355 Cr against ₹323 Cr of revenue** — a ratio above 100% in both FY25 and FY24. The fleet the story rests on compounded at **21.35% a year** while revenue grew **49.61%**. And the mechanism now being used to fund the fleet — FOCO, in which outside owners buy the vehicles and are paid an **assured ₹1,600–1,900 per vehicle per month for 36 months** — converts the one genuinely variable cost in an asset business into a fixed one, at a company that spends **₹1.27 to earn ₹1**.

---

## 1. Cover

| | |
|---|---|
| **Case Study** | Day 64 of 90 |
| **Product** | Zypp Electric |
| **Legal entity** | Bycyshare Technologies Private Limited |
| **CIN** | U63000HR2017PTC070227 |
| **Sector** | EV fleet-as-a-service · last-mile delivery |
| **Geography** | India (Delhi-NCR, Bengaluru, Mumbai, Hyderabad, Jaipur) |
| **Latest audited year** | FY2024-25 (RoC filings) |
| **Author** | Gaurav Singh |
| **Date** | 30 August 2026 |

---

## 2. Repository Metadata

The operating entity is **Bycyshare Technologies Private Limited, CIN U63000HR2017PTC070227**, incorporated **8 August 2017**, registered with **RoC Delhi**, registered office at Tower 16 Flat 1201, The South Close, Sector 50, Gurugram, Haryana 122018. Authorised capital is **₹12.54 lakh** and paid-up capital **₹2.65 lakh** — a paid-up base of under three lakh rupees for a company with ₹438 Cr of revenue, which tells you the balance sheet is built on securities premium and debt, not share capital.

Two registry details are worth recording. The **NIC code embedded in the CIN is 630 — supporting and auxiliary transport activities, activities of travel agencies**, a classification inherited from the 2017 bicycle-sharing business and never updated for a vehicle-leasing and manpower-supply operation. And an **older CIN, U74999HR2017PTC070227, still appears on several aggregators** with the same registration number and incorporation date; it is a stale pre-reclassification snapshot. Cite the CIN, never the aggregator page.

---

## 3. Badges

`Domain: EV fleet-as-a-service` · `Stage: Series C, IPO-track` · `Filing basis: RoC (private)` · `Evidence: 🟢 High on FY25 P&L, 🟡 Medium on fleet, 🟠 Low on FOCO terms` · `Sections: 65` · `Programmatic checks: 145/145`

---

## 4. Table of Contents

<details>
<summary>Expand all 65 sections</summary>

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
| 13 | TAM/SAM/SOM | 46 | Opportunity Mapping |
| 14 | Competitor Analysis | 47 | RICE |
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

Zypp Electric closed FY25 with operating revenue of **₹437.9 Cr, up 49.61%**, and a net loss of **₹107.5 Cr, up 20.11%**. Total expenditure reached **₹556.5 Cr**, so the company spent **₹1.2708 to earn each rupee**. It has appointed Axis Capital, SBI Capital Markets and DAM Capital for a **$150–200 Mn IPO targeted at FY28**.

The headline reading is a fast-growing EV-as-a-Service platform approaching profitability. The segment disclosure does not support it. **Delivery services — supplying riders and taking a cut of each delivery — was 73.76% of operating revenue and supplied 79.85% of the year's growth.** Vehicle rental, the line that actually corresponds to "EV-as-a-Service," was **25.35%, down from 28.73%**, and supplied **18.53%**. The asset business is the minority business and it is shrinking as a share.

The direct cost of the majority business exceeds its revenue. **Rider-related expenses were ₹355 Cr against ₹323 Cr of delivery revenue — 109.91%**, against 115.07% in FY24. It is improving, by 5.16pp, and that improvement is real. It has not yet crossed one.

Underneath both lines is a fleet that has not grown the way the revenue has: **17,000 (Nov 2023) → 22,000 (May 2024) → 20,000 (Nov 2025) → 26,700 usable (Mar 2026)**, an annualised **21.35%** against revenue growth of **49.61%**, a factor of **2.32×**. Against the 100,000 vehicles promised in November 2023 for 12–18 months out, the November 2025 count is a **20.00% realisation** — the most generous of three expired targets.

The funding mechanism is where this becomes a product question rather than a financial one. Under **FOCO**, launched July 2025, outside investors buy vehicles at roughly **₹45,000 each**, hold title in their own name, and receive **₹1,600–1,900 per vehicle per month for 36 months** as an assured **40–50%** return. Set against what a vehicle demonstrably earns — ₹111 Cr of rental across a 20,000 fleet implies **₹152.05 per vehicle-day against a ₹250 list price** — the assured payout consumes **37.84%** of realised rent before insurance, maintenance, swap, hub cost or a single idle day. **An asset business whose receipts are set by third parties is funding itself with obligations that are not.**

**Recommendation:** *Zypp Ledger* — replace the fixed assured payout with one indexed to a published, attested per-vehicle contribution measure, and let outside owners price the variance instead of Zypp absorbing it. North Star **CVD/1k**, Contribution-Verified vehicle-Days per 1,000 **deployed** vehicle-days. Guardrail **RIS-90**. Under a stress rule set by Zypp's own 20.00% fleet-target realisation, the proposal falls from 3rd of four initiatives to **last**, behind finishing the battery-swap conversion — which is the correct answer, and §47 says why.

---

## 6. Product Overview

Zypp Electric operates a fleet of electric two-wheelers and three-wheeler loaders that it puts under gig delivery riders, then sells the resulting delivery capacity to quick-commerce, food-delivery and e-commerce platforms. Riders access a vehicle through the **Zypp Pilot** app with no deposit and no EMI, paying a daily rental that bundles insurance, maintenance and battery swapping. Client platforms include **Zomato, Swiggy, Zepto, Blinkit, Amazon, Flipkart, BigBasket, Rapido, Porter and Uber**.

The company describes itself as a technology platform, and the operating stack is real: **FleetEase.ai** tracks vehicle assignment, KYC, spare parts and uptime, which the company puts at **85–90%**. It runs **20 hubs** and **220 mechanics on payroll**. Battery swapping is outsourced to **Indofast Energy** (an IndianOil–SUN Mobility joint venture) and Mooving; vehicles are sourced from **Odysse Electric** and **e-Sprinto**.

---

## 7. Company Background

Founded in **August 2017** as **Mobycy**, India's first dockless bicycle-sharing app, by **Akash Gupta** and **Rashi Agarwal**. The company pivoted to electric scooters in 2019 and to B2B last-mile delivery thereafter. **Tushar Mehta** joined the leadership team as co-founder and COO in 2021.

Total disclosed funding is **$76.5 Mn** across twelve rounds, led at Series B (Nov 2022, $25 Mn) by Taiwan's **Gogoro** and at Series C by Japan's **ENEOS Group** ($15 Mn, May 2024), with Goodyear Ventures, Venture Catalysts, Indian Angel Network, 100Unicorns, We Founder Circle and IvyGrowth among the register. Valuation was approximately **$331 Mn as of March 2025**. The board comprises Akash Gupta, Rashi Agarwal, Bruce Morrison Aitken and Madhav Sikka.

---

## 8. Product Timeline

| Date | Event |
|---|---|
| Aug 2017 | Incorporated as Bycyshare Technologies; launches Mobycy dockless bicycle sharing |
| 2019 | Pivots to electric scooters; Zypp brand |
| 2021 | Expands to Bengaluru and Pune; Tushar Mehta joins as co-founder/COO |
| Sep 2022 | Fleet ~6,000; states target of 1.5 lakh scooters across 18 cities by 2025 |
| Nov 2022 | $25 Mn Series B led by Gogoro; states target of 200,000 vehicles and 30 cities by Dec 2025 |
| Nov 2023 | Fleet 17,000; states target of 100,000 in 12–18 months, 200,000 in 24–36 |
| May 2024 | $15 Mn Series C led by ENEOS; fleet 22,000; Southeast Asia plans announced |
| Feb 2025 | Announces 1 lakh battery-swappable EVs with Indofast over 12–18 months |
| Feb–Mar 2025 | Headcount cut from ~1,300 to ~1,150 ahead of a planned listing |
| Jul 2025 | **FOCO launched** — outside ownership of vehicles, company operation |
| Jul 2025 | Advertising vertical launched (branded scooters and helmets) |
| Nov 2025 | Fleet 20,000 across three cities; claims operational profitability from July 2025 |
| Feb 2026 | FY25 RoC figures reported: revenue ₹438 Cr, loss ₹107.5 Cr |
| Jun 2026 | Appoints Axis Capital, SBI Capital, DAM Capital for a $150–200 Mn IPO targeted FY28 |

---

## 9. Vision & Mission

The stated mission is **"Mission Zero Emission"** — making India's last-mile logistics carbon-free through an ecosystem of electric vehicles and EV-based technology. The commercial articulation is narrower and more useful: give a delivery rider access to a vehicle with no capital, no EMI and no fuel bill, and sell the resulting capacity to platforms that need it.

The tension this case study examines is that the mission is stated in terms of an asset — vehicles deployed — while the business has grown in terms of labour supplied.

---

## 10. Problem Statement

A gig delivery rider in urban India faces a capital problem disguised as an income problem. The vehicle is the largest fixed cost of the job and the rider cannot finance it: no formal credit history, income that varies week to week, and a job with no tenure. Zypp's CEO has put a petrol rider's spend on fuel, maintenance and vehicle financing at roughly **one-third of monthly earnings**. Zypp removes the capital requirement entirely and charges a daily rent instead.

The platform side has a matching problem. Quick-commerce and e-commerce companies need delivery capacity that flexes hourly and seasonally, and increasingly need it to be electric — not as a preference but as a licence condition. Owning that fleet would put a depreciating, low-utilisation asset on a balance sheet built for software multiples.

Zypp sits between the two, and the structural question is which of those two problems it is actually being paid to solve. The FY25 segment split says: mostly the second, through labour rather than assets.

---

## 11. Market Research

India's EV-sector funding rose from **$40.6 Mn in 2017 to $1.67 Bn in 2025**, with **$418 Mn** invested in 2026 to date. The demand pull under Zypp is quick commerce, whose expansion into tier-2 cities is the stated basis for Zypp's Jaipur entry and its plan to reach 15–25 cities.

The regulatory pull is more concrete than the market pull, and it is the single most important external fact in this case study. Under the **Delhi Motor Vehicle Aggregator and Delivery Service Provider Scheme, 2023** (notified 29 November 2023), delivery service providers operating 25 or more vehicles in Delhi must electrify **100% of new two- and three-wheeler onboarding within four years** and their entire fleet by **2030**. On top of that, the **Commission for Air Quality Management directed that from 1 January 2026, no new petrol or diesel vehicles may be added to the fleets of cab aggregators, delivery companies or e-commerce firms anywhere in Delhi-NCR** — only electric or CNG.

Zypp's largest market therefore has a legal floor under EV demand. §12 explains why that is a smaller advantage than it first appears.

---

## 12. Industry Analysis

Three structurally different business models share one label. **Asset-yield operators** (Yulu) own vehicles and earn rent. **Labour-supply operators** earn a margin on delivery volume and treat the vehicle as an enabling cost. **Infrastructure operators** (Indofast, Battery Smart) sell energy access to whoever owns the vehicle. Zypp does all three and reports the first two together as "EV-as-a-Service." Category economics are set by utilisation rather than price, and utilisation is set by demand the operator does not control — which makes every operator a levered bet on someone else's demand curve.

**The regulatory point cuts both ways.** A mandate that every delivery fleet must be electric guarantees the category's volume and simultaneously destroys its differentiation. When "we are the electric option" becomes the legal minimum rather than a choice, the buying criterion collapses to price, reliability and uptime. Zypp's founding pitch was that EV last-mile was cheaper and cleaner; by 2030 in Delhi it will be the only thing that is legal, and being the incumbent EV supplier is worth less in that world than being the cheapest one. This is the same structural move that mandatory efficiency labelling made against Atomberg on Day 61: **a regulator did not attack the differentiator, it universalised it.**

---

## 13. TAM/SAM/SOM

*Framework note: run in restricted form. No primary-sourced market size for Indian EV fleet leasing could be verified, so this is sized from the company's own disclosed base rather than from a third-party market estimate.*

| Layer | Basis | Figure |
|---|---|---|
| **TAM** | Not sized. No primary-source market estimate located. | Not disclosed |
| **SAM** | Company-stated ambition: 10–15% of all deliveries in India's top 25 cities | Company target, not a market measurement |
| **SOM** | Company-stated share: **12–13% of last-mile deliveries in Delhi, 6–7% Bengaluru, ~4% Mumbai** (all vehicle types); **60–65% on an EV-only basis** in those cities | 🟡 Medium — management commentary, not independently verified |

The EV-only share figure is the honest one to attend to. A 60–65% share of a market that regulation is about to make universal is a strong position *and* a warning: the share was won when EV supply was scarce, and the mandate ends the scarcity.

---

## 14. Competitor Analysis

*Framework note: restricted to competitors whose financials are filed and reported. Yulu files consolidated accounts with the RoC and is used in full. Alt Mobility, EVeez, Baaz and Magenta Mobility operate in the same category; no comparable FY25 filings were located for them, so no estimates are constructed and they are named rather than sized.*

**Yulu is the mirror, and it is inverted on exactly the axis this case study is about.**

| FY25 | Zypp Electric | Yulu |
|---|---|---|
| Operating revenue | ₹437.9 Cr | ₹237.4 Cr |
| Revenue growth | +49.61% | +98.00% |
| **Vehicle rental share of revenue** | **25.35%** | **84.67%** |
| **Labour/manpower share of revenue** | **73.76%** | **5.58%** |
| Net loss | ₹107.5 Cr | ₹126.0 Cr |
| **Loss direction** | **+20.11% (widened)** | **−11.76% (narrowed)** |
| EBITDA margin | −15.98% | −15.29% |
| Cost per rupee of revenue | ₹1.27 | ₹1.48 |
| Cash and bank | ₹72.5 Cr | ₹9.65 Cr |

Two companies in the same category, in the same fiscal year, landed **0.69pp apart on EBITDA margin** while building revenue in almost exactly opposite proportions. Yulu earns **3.34×** the revenue share from rental that Zypp does. Yulu grew twice as fast and cut its loss; Zypp grew half as fast and widened its. The company whose revenue actually looks like EV-as-a-Service is the other one.

**The numbers that weaken this reading, kept in.** Zypp is **1.84×** Yulu's size and materially more cost-efficient per rupee of revenue — ₹1.27 against ₹1.48. Yulu's improvement came off a catastrophic base: its EBITDA margin improved **64.82pp** from −80.11%, which is a recovery, not an achievement. And Yulu's cash fell **93.24%** to ₹9.65 Cr, against Zypp's ₹72.5 Cr — **7.51×** more. On liquidity, Zypp is in the better position by a wide margin. The finding is about revenue construction, not about which company is healthier.

---

## 15. SWOT

| Strengths | Weaknesses |
|---|---|
| 12–13% of Delhi last-mile deliveries; 60–65% of EV-only volume in core cities | Rider cost at **109.91%** of delivery revenue; loss widened 20.11% |
| Client roster covering essentially every major Indian delivery platform | Rental line **25.35%** of revenue and falling 3.38pp |
| Real operating leverage: rider cost +49.0% and employee cost +43.0% against revenue +49.61% | Fleet compounding at **21.35%** against revenue at 49.61% |
| Cash ₹72.5 Cr, **7.51×** the nearest filed comparator | Repeated, dated fleet targets realised at **10.00–20.00%** |
| FleetEase.ai is a genuine operating asset with 85–90% uptime | Paid-up capital ₹2.65 lakh; ₹119.04 Cr of open charges |

| Opportunities | Threats |
|---|---|
| CAQM's 1 Jan 2026 NCR ban on new ICE fleet additions is a legal demand floor | The same mandate universalises the differentiator (§12) |
| Three-wheeler cargo: 750 → 900 units, a higher-revenue-per-asset segment | Client concentration in quick commerce, whose payout rates Zypp does not set |
| FOCO removes fleet capex from the balance sheet before an IPO | FOCO replaces variable capex with a **fixed 36-month obligation** |
| FleetEase.ai converts operating know-how into third-party revenue | Gig-worker welfare levies now live in Karnataka from 13 Feb 2026 |

---

## 16. Porter's Five Forces

*Framework note: run twice, because Zypp's two revenue lines face genuinely different force structures. This is the seam the case study is built on — an external event (the electrification mandate) hits one half and not the other.*

| Force | **Vehicle rental** (25.35% of revenue) | **Delivery services** (73.76%) |
|---|---|---|
| **Buyer power** | Moderate. The rider has no capital and few substitutes, but rent is already indexed downward against his earnings, which is buyer power exercised by formula. | **High.** Zomato, Zepto and Blinkit set per-order economics; Zypp is a vendor of substitutable labour capacity. |
| **Supplier power** | **Rising.** Batteries are outsourced to Indofast/Mooving; OEM supply concentrated in Odysse and e-Sprinto. | **High and rising.** Riders are the supply, and their alternative is any other platform, at zero switching cost. |
| **New entrants** | **Falling barriers.** FOCO proves outside capital will buy the assets; anyone can rent them out. Zypp is licensing FleetEase.ai to the entrants. | Low barriers. Manpower supply needs no asset base at all. |
| **Substitutes** | Rider-owned EVs, financed as EV credit deepens; rent-to-own erodes the rental base by design. | Platforms in-housing their own rider fleets. |
| **Rivalry** | Moderate: Yulu, EVeez, Baaz, Alt Mobility, Magenta. | **Intense and price-led**, because the service is undifferentiated once every fleet is electric. |

The two columns invert on new entrants. In the asset business Zypp is actively *lowering* the barrier to entry — by demonstrating to outside capital that the assets are financeable, and by selling its operating software to smaller fleets as customers. That is a defensible commercial decision and a genuine structural risk in the same move.

---

## 17. Business Model Canvas

**Key partners:** Indofast Energy and Mooving (swapping), Odysse Electric and e-Sprinto (vehicles), HDFC Bank and Axis Bank (fleet debt), Shell Foundation, FOCO asset owners. **Key activities:** fleet deployment, rider onboarding and KYC, maintenance, client settlement. **Key resources:** 26,700 usable vehicles, 20 hubs, 220 mechanics, FleetEase.ai, the client roster. **Value propositions:** to riders, a job without capital; to platforms, compliant electric capacity on demand; to FOCO investors, an assured yield on a real asset. **Channels:** Zypp Pilot app, enterprise contracts, franchise sales. **Customer relationships:** transactional and daily on the rider side, contractual on the platform side. **Cost structure:** rider expenses ₹355 Cr (63.79% of total), employee ₹67 Cr, depreciation ₹38.5 Cr. **Revenue streams:** delivery ₹323 Cr, rental ₹111 Cr, other operating ₹4 Cr, other income ₹11 Cr.

The canvas exposes the asymmetry directly: three of the four value propositions are promises to somebody else about money, and only one of them — the FOCO yield — is fixed.

---

## 18. Revenue Model

| Line | FY25 | Share | FY24 | Growth | Share of FY25 growth |
|---|---|---|---|---|---|
| Delivery services | ₹323.0 Cr | 73.76% | ₹207.05 Cr | +56.0% | **79.85%** |
| Vehicle rental | ₹111.0 Cr | 25.35% | ₹84.09 Cr | +32.0% | **18.53%** |
| Other operating | ₹4.0 Cr | 0.91% | ₹1.56 Cr | — | 1.68% |
| **Operating revenue** | **₹437.9 Cr** | 100% | **₹292.7 Cr** | **+49.61%** | 100% |
| Other income | ₹11.0 Cr | — | ₹9.8 Cr | — | — |
| **Total income** | **₹449.0 Cr** | — | **₹302.5 Cr** | +48.4% | — |

Delivery growth contributed **4.31×** the rupees that rental did. The reported segment lines sum to ₹438.0 Cr against operating revenue of ₹437.9 Cr — a **₹0.10 Cr rounding residual, 0.02% of revenue**, immaterial and disclosed rather than smoothed.

Two new lines started in FY26: **advertising** on scooters and helmets (launched July 2025, ₹30 lakh in FY26 to date) and **FleetEase.ai** licensed to third-party fleets at ₹149–₹499 per vehicle per month (expected ≥₹60 lakh for FY26). Combined, **₹0.90 Cr — 0.15% of the ₹600 Cr FY26 revenue target.** At that rate it would take **119 years** of new-vertical revenue to cover one year of FY25's loss. They are real products and they are not yet a diversification.

---

## 19. Target Users

Three distinct users with three different currencies. The **rider** is a migrant or first-job urban worker, typically 18–30, without capital or credit, whose currency is daily take-home after rent. The **client platform** is a quick-commerce or e-commerce operations team whose currency is fill rate, cost per delivery and now regulatory compliance. The **FOCO investor** is an HNI, family office or institution whose currency is monthly yield on a titled asset.

Only the first two appear in Zypp's product surfaces. The third has been added to the business without being added to the product, and §50 argues that is the gap.

---

## 20. Personas

**Karim, 24, Blinkit rider, East Delhi.** Arrived from Bihar with no vehicle and no savings. Rents a Zypp scooter daily; rent is bundled with insurance, maintenance and swaps. Earns ₹30,000–35,000 a month. His decision each morning is whether the day's expected orders clear the day's rent, and his rent falls when his earnings rise.

**Priya, 34, city operations lead at a quick-commerce platform.** Buys delivery capacity by the shift. Needs compliant electric vehicles in NCR from January 2026, cares about fill rate at 7pm on a Friday, and can move volume to a rival supplier within a week.

**Mr. Shah, 52, Ahmedabad, family office.** Put ₹45 lakh into 100 Zypp scooters titled in his name. Expects ₹1.6–1.9 lakh a month for 36 months. Has no visibility into whether the specific vehicles he owns are earning, and no contractual exposure to whether they are.

---
## 21. Jobs To Be Done

| Actor | Job | Current solution | Where it fails |
|---|---|---|---|
| Rider | "Let me start earning today without owning anything" | Zypp daily rental, no deposit, no EMI | Rent is highest on the days he earns least |
| Rider | "Don't let a breakdown cost me a day's income" | 20 hubs, 220 mechanics, swap network | Downtime lands entirely on the rider's income |
| Platform | "Give me compliant capacity that flexes by the hour" | Zypp delivery contracts | Undifferentiated once every supplier is electric |
| Platform | "Prove my last-mile emissions position" | Zypp's EV fleet | No per-delivery attested record is published |
| Asset investor | "Yield on a real, titled asset I don't have to run" | FOCO, assured ₹1,600–1,900/vehicle/month | Yield is assured by the operator, not by the asset |

The last row is the whole case study. The FOCO investor's job is "let the asset pay me," and the product delivers "let the company pay me." Those are different instruments with different risk, sold under the same name.

---

## 22. User Journey

The rider's journey is genuinely short: Aadhaar KYC and a selfie, vehicle selection, client ID activation, first delivery — advertised as five minutes. The friction is not at onboarding; it is at day 40, when the rider discovers that a slow week raises his effective rent per delivery, and at day 200, when the rent-to-own path requires a **52-week continuous commitment** he may not be able to sustain.

The FOCO investor's journey ends at the point of purchase. There is no disclosed post-purchase surface reporting the deployment, utilisation or contribution of the specific vehicles titled in his name.

---

## 23. User Flow

Rider flow: install Zypp Pilot → KYC → select vehicle type → assign hub → activate client ID → daily ride, swap, return → daily rent debit. Client flow: contract → API integration → shift-level capacity request → rider allocation → settlement.

The two flows meet at a vehicle and never meet at a ledger. Nothing in either flow produces a per-vehicle statement of what that vehicle earned and cost.

---

## 24. Information Architecture

Three surfaces exist: the rider app, the client merchant panel, and FleetEase.ai for internal and now third-party fleet management. FleetEase.ai already holds the data model a per-vehicle contribution ledger would need — assignment, uptime, spares, total cost of ownership.

The missing node is an owner-facing surface. FOCO created a fourth stakeholder without creating a fourth view.

---

## 25. UX Audit

The rider experience is strong on the things that block a first shift — no deposit, instant KYC, unlimited kilometres — and thin on the things that determine whether a rider stays. Rent is the central variable in the rider's economics and its determination is opaque: the marketing states that higher daily earnings mean lower daily rent, without publishing the schedule.

Zypp has not publicly disclosed the rent formula, its bands, or how often it is revised.

---

## 26. UI Audit

Zypp Pilot is built for low-literacy, low-bandwidth, high-frequency use, and its information density reflects that correctly. The public marketing surface carries a savings calculator that models rent against petrol cost.

No public surface shows a rider his rolling rent-to-earnings ratio, which is the number that actually governs whether the job works for him.

---

## 27. Accessibility

The product's real accessibility achievement is financial rather than interface-level: removing the capital requirement admits riders with no credit history to a job that otherwise requires ₹80,000–1,20,000 of vehicle. Aadhaar-based KYC and vernacular support are appropriate to the user base.

Zypp has not publicly disclosed WCAG conformance or screen-reader support for the Pilot app.

---

## 28. Feature Breakdown

| Feature | What it does | Strategic weight |
|---|---|---|
| Daily/weekly rental, no deposit | Removes rider capital barrier | The original insight; now table stakes |
| Earnings-linked rent | Rent falls as daily earnings rise | Rider-friendly framing, revenue-variance source |
| Battery swapping via Indofast/Mooving | 90-second swaps, unlimited range | Converts range risk to an operating fee |
| Delivery allocation via Zypp Pilot | Connects riders to client platforms | 73.76% of revenue originates here |
| FleetEase.ai | Assignment, uptime, TCO, spares | The asset the ledger proposal is built on |
| Rent-to-own | 52-week commitment converts rider to owner | Structurally shrinks the rental base |
| FOCO | Outside ownership, company operation | Moves capex off balance sheet, adds fixed obligation |
| Advertising | Branded scooters and helmets | ₹9.36 per vehicle per month |

**The asset the proposal needs already exists.** FleetEase.ai tracks vehicle-level assignment, uptime, maintenance and total cost of ownership, and Zypp is confident enough in it to license it to third parties at ₹149–₹499 per vehicle per month. A company that sells other operators a per-vehicle economics tool has the data to publish per-vehicle economics on its own fleet.

---

## 29. AI Capabilities

FleetEase.ai is described as an AI-enabled platform processing operational data to optimise uptime and utilisation, and Zypp reports 85–90% uptime against it. Zypp has not publicly disclosed model architectures, training data, or measured lift attributable to the AI components as distinct from the operational process.

Treated here as a real operating system with unverified AI-specific contribution.

---

## 30. Product Metrics

| Metric | FY25 | FY24 | Note |
|---|---|---|---|
| Operating revenue | ₹437.9 Cr | ₹292.7 Cr | +49.61% |
| Delivery revenue | ₹323.0 Cr | ₹207.05 Cr | +56.0% |
| Rental revenue | ₹111.0 Cr | ₹84.09 Cr | +32.0% |
| Rider expenses | ₹355.0 Cr | ₹238.26 Cr | 63.79% of total cost |
| **Rider cost ÷ delivery revenue** | **109.91%** | **115.07%** | improving 5.16pp |
| Total expenditure | ₹556.5 Cr | ₹392.0 Cr | +41.96% |
| Cost per rupee of revenue | ₹1.2708 | ₹1.3392 | improving |
| Net loss | ₹107.5 Cr | ₹89.5 Cr | +20.11% |
| EBITDA margin | −15.98% | — | Entrackr basis |
| EBITDA margin (company-stated) | −13.20% | −19.30% | 2.78pp apart from the above |
| Cash and bank | ₹72.5 Cr | — | 8.09 months of FY25 loss |
| Usable fleet | ~22,000 | ~20,000 | 26,700 stated for Mar 2026 |

**Two EBITDA margins exist for the same year and they differ by 2.78pp** — ₹12.17 Cr of implied EBITDA. Both are negative, so the direction survives either reading, but the level does not, and §65 Appendix A logs it rather than picking one.

---

## 31. North Star Metric

**Proposed: CVD/1k — Contribution-Verified vehicle-Days per 1,000 *deployed* vehicle-days.**

A vehicle-day counts only if all four hold: the vehicle was deployed and available; revenue attributable to it that day exceeded its directly attributable cost including a financing accrual; the figures are settled rather than accrued; and the attribution was not reallocated between segments after the period closed.

**The denominator is the design choice.** It is *deployed* vehicle-days, not earning vehicle-days and not vehicles owned. Add a vehicle that does not earn and CVD/1k **falls**. That is the opposite of every metric Zypp currently communicates — fleet size, deliveries completed, cities entered — all of which rise when you add an asset regardless of whether it pays. A fleet of 26,700 running a full year is **9,745,500 deployed vehicle-days**, so one point of CVD/1k represents **9,745.5 vehicle-days**: a unit small enough to manage weekly and large enough to matter annually.

**Guardrail: RIS-90 — Rider Income Stability at the 90th percentile of rent-repricing intensity.** In the decile of weeks where the earnings-linked rent formula moves most, the share of active riders whose take-home after rent stays within a published band. Reported **by city and by client platform, never in aggregate**, because the failure mode is concentrated: a contribution target is easiest to hit by repricing rent against the riders earning least, in the cities with the fewest alternatives. Owned by a Rider Economics function with no revenue target.

---

## 32. Product Analytics

Zypp's instrumentation is genuinely good at the vehicle layer — IoT-connected scooters, assignment logs, swap events, spare-part consumption, uptime. It is thin at the joint layer, where a vehicle, a rider and a client settlement meet.

Zypp has not publicly disclosed whether client settlements are attributable to individual vehicles, and §53 makes that the first thing Phase 0 tests.

---

## 33. AARRR

*Framework note: run on riders, since riders are the supply constraint and rider retention is what actually determines fleet utilisation.*

| Stage | Mechanism | Observation |
|---|---|---|
| **Acquisition** | Referrals, hub walk-ins, client platform onboarding funnels | Instant Aadhaar KYC; five-minute start is a real advantage |
| **Activation** | First delivery on a Zypp vehicle | Fast; capital barrier genuinely removed |
| **Retention** | Daily rent vs daily earnings | The pressure point; no published rent schedule |
| **Revenue** | Daily rent + delivery commission share | Rent realises at an implied **60.82%** of list (§39) |
| **Referral** | Rider referral support in-app | Present; effectiveness not disclosed |

Retention is the stage that carries the model, and it is the stage with the least public evidence. A rider who leaves takes a vehicle out of service until it is reassigned, which converts a churn problem directly into an asset-yield problem.

---

## 34. HEART

**Happiness:** rider testimonials report ₹30,000–40,000 monthly earnings; no NPS or CSAT disclosed. **Engagement:** ~20,000 riders using vehicles daily against a 26,700 usable fleet. **Adoption:** advertised 500K+ delivery partners onboarded historically against the daily active base. **Retention:** not disclosed at rider level — the most important gap. **Task success:** 85–90% vehicle uptime is disclosed and is a real operating number.

The gap between a cumulative onboarding figure and a daily active figure is the metric Zypp does not publish and the one an IPO prospectus will have to contain.

---

## 35. Growth Strategy

The stated strategy is to follow quick commerce into tier-2 India, expand from five cities to 15–25, and grow the fleet from 26,700 to 100,000 — requiring **73,300 additional vehicles, 3.75× the current usable fleet**. Funding is shifting from fully leased vehicles to roughly half leased and half bank-financed, plus FOCO.

The track record on exactly this promise is documented in §5 and §13: three dated fleet targets, realised at **10.00%, 14.67% and 20.00%**. The strategy is not new; the funding mechanism is.

---

## 36. Growth Loops

The intended loop is: more vehicles → more delivery capacity → more platform contracts → more revenue → more vehicles. It has a leak at the fourth arrow, because in FY25 more revenue did not become more vehicles — revenue grew **2.32×** faster than the fleet compounded.

FOCO is an attempt to repair that arrow by sourcing the capital from outside. It repairs the flow and adds a fixed claim against it.

---

## 37. Network Effects

There are no meaningful network effects here, and it is worth saying so plainly rather than manufacturing one. More riders do not make the service better for other riders; more client platforms do not make it better for existing clients. What exists is **scale economics** — hub density, swap-station proximity, spares purchasing, and a data advantage in vehicle assignment.

Licensing FleetEase.ai to smaller competitors converts the only defensible advantage into a product those competitors can buy.

---

## 38. Product Strategy

Zypp's strategy is legible and internally coherent: be the compliant electric capacity layer for Indian last-mile, get to scale before the mandates bite, and list. The three FY26 moves — FOCO, advertising, FleetEase.ai — all point the same way, toward asset-light revenue that supports a technology multiple rather than a leasing multiple.

The strategic problem is that the three moves have different sizes. Advertising and SaaS together are **0.15%** of the FY26 revenue target. FOCO is the only one large enough to change the balance sheet, and it is the one that does so by adding a fixed liability. **A company can be asset-light or obligation-light; FOCO chooses the first at the cost of the second**, and the choice has not been publicly framed as a choice.

---

## 39. Monetization

| Instrument | Price | Realisation |
|---|---|---|
| Vehicle rental (list) | ~₹250 per vehicle-day | ₹7,604.17 per vehicle-month |
| Vehicle rental (derived) | ₹111 Cr ÷ 20,000 vehicles | **₹152.05 per vehicle-day, 60.82% of list** |
| Delivery commission | Share of per-delivery fee | ₹323 Cr, direct rider cost ₹355 Cr |
| FleetEase.ai | ₹149–₹499 per vehicle-month | ≥₹60 lakh expected FY26 |
| Advertising | Not disclosed | ₹9.36 per vehicle-month implied |
| **FOCO payout (outflow)** | **₹1,600–1,900 per vehicle-month, assured** | **37.84% of derived realised rent** |

**The realisation gap is the number to sit with.** ₹111 Cr of rental across a 20,000 fleet implies ₹152.05 per vehicle-day against a ₹250 list price. Across a defensible fleet band of 17,000–22,000, realisation runs **55.29% to 71.56%** — a 16.27pp band, and below 75% on every assumption in it.

There are two honest readings and both are given weight. The first: idle days, discounts and the earnings-linked rent rule mean a substantial share of list rent is never collected. The second, which is at least as likely: **most vehicles do not earn through the rental line at all** — they earn through the delivery line, where the vehicle is bundled into a per-delivery price and the rent never appears as rent. Under the second reading the "rental" line describes only the minority of the fleet let directly to independent riders, and the gap is an artefact of the denominator.

Either reading supports the same conclusion, which is why the finding survives: **the rental line cannot be reconciled to the fleet at list price, and the arithmetic that cannot be made to work is the arithmetic FOCO's assured payout is drawn against.**

---

## 40. Trust & Safety

*Placed before §50, deliberately, for two reasons. The first is that the proposal in §50 creates a mechanism that could be used to reprice rent against the riders least able to absorb it. The second is more serious and is about FOCO as it exists today.*

**On riders.** Rent is inverse to earnings — so a rider earning less pays more, in the week he can least afford it, with no published schedule and no cap. Zypp has also reportedly linked team-lead pay to three-day targets, pushing short-horizon pressure down the chain toward exactly this lever. Any contribution-linked instrument must cap the lever before it ships, not after; §51 does that.

**On outside asset owners.** FOCO is marketed to individuals, HNIs, family offices and institutions as **assured returns of 40–50% over 36 months**, and in one account **59% to 100%**. Two things follow.

The first is an **inconsistency inside the offer**. ₹1.6–1.9 lakh a month on 100 vehicles over 36 months produces **₹57.6–68.4 lakh**; the stated three-year total is **₹60–66 lakh**. The ranges do not reconcile — small in a marketing description, material in a return promise.

The second is a **question this case study raises without answering**. Under Section 11AA of the SEBI Act, an arrangement pooling contributions managed on investors' behalf, with no day-to-day investor control, is a collective investment scheme; the Securities Laws (Amendment) Act, 2014 deems any unregistered pooling of **₹100 Cr or more** to be one; and CIS operators may not offer assured returns. SEBI has acted on this basis before, including a January 2024 interim order against an agri platform offering an 11–14% assured profit share.

**The reading that favours Zypp is strong and comes first.** FOCO titles each vehicle in the investor's own name. No funds are pooled into a common corpus; each investor owns identified assets. That is the standard structure for sitting outside the definition, and fractional-ownership commentary supports it where returns are not, in substance, fixed.

**The reading that does not favour Zypp is that the return is described as assured** — and that commentary also holds that where the substance is a fixed rate rather than a share of actual yield, the label may not survive scrutiny. **This is a question, not a finding.** Nothing here asserts Zypp is operating an unregistered scheme, and no regulatory action against Zypp was located. But a DRHP will have to answer it in writing, and §50 is partly designed to make the answer easy.

**The arithmetic that makes it live.** At ₹45,000 a vehicle, **₹100 Cr of FOCO capital is 22,222 vehicles**, while the stated plan needs **73,300 more — 3.30× that ceiling**. Only **30.32%** of the required fleet is FOCO-fundable below the threshold. Today's 500 vehicles are **2.25%** of it: not a present-tense problem, a ceiling on the strategy.

---

## 41. Technical Architecture

Zypp's stack is an IoT and fleet-operations system rather than a marketplace: connected vehicles reporting location and state, a rider app handling identity and assignment, a hub-side maintenance and spares system, and FleetEase.ai as the operating layer over all three. Battery energy is an outsourced dependency, not owned infrastructure.

Zypp has not publicly disclosed its cloud provider, service architecture or telemetry cadence.

---

## 42. Data Flow

Vehicle telemetry and swap events flow to FleetEase.ai; rider identity and activity flow through Zypp Pilot; client platforms integrate by API for capacity requests and settlement. Financially, the flows converge only at the entity level, not at the vehicle level.

That convergence gap is the single technical dependency of the §50 proposal, and it is what Phase 0 exists to test.

---

## 43. API Ecosystem

Client integration is via API for order allocation, rider tracking, multi-order support and merchant panels. FleetEase.ai is now sold externally to operators including Rilox E-Mobility and Zevo, with international discussions reported.

No public developer documentation or partner API specification was located.

---

## 44. Privacy & Security

Rider onboarding collects Aadhaar, PAN and bank details, and the fleet is continuously location-tracked, which makes Zypp a processor of identity-linked movement data for a low-bargaining-power workforce. The **Digital Personal Data Protection Rules, notified 14 November 2025**, bring enforcement obligations with penalties up to ₹250 Cr.

Zypp has not publicly disclosed a data retention schedule for rider location history, which is the specific disclosure this workforce has the most at stake in.

---

## 45. Pain Points

| # | Pain point | Whose | Evidence |
|---|---|---|---|
| 1 | Rider cost exceeds the revenue it generates | Company | 109.91% FY25, 115.07% FY24 |
| 2 | The asset line is shrinking as a share of revenue | Company | 28.73% → 25.35% |
| 3 | Fleet growth badly trails revenue growth | Company | 21.35% vs 49.61% annualised |
| 4 | Repeated fleet targets missed by large margins | Credibility | 10.00%, 14.67%, 20.00% realisation |
| 5 | Rent rises when rider earnings fall | Rider | Earnings-linked rent, no published schedule |
| 6 | Assured payout is fixed against variable receipts | Company | ₹1,600–1,900 fixed vs 60.82% realisation |
| 7 | Asset owner has no view of his own vehicles | Investor | No disclosed owner-facing reporting |
| 8 | Diversification lines are immaterial | Company | ₹0.90 Cr = 0.15% of FY26 target |
| 9 | Differentiation is being universalised by mandate | Company | CAQM 1 Jan 2026; DMVADSPS 2030 |
| 10 | Two EBITDA margins for one year | Disclosure | −15.98% vs −13.20% |

---
## 46. Opportunity Mapping

| Opportunity | Underlying pain | Why now |
|---|---|---|
| Make per-vehicle contribution computable and published | #1, #6, #7 | FleetEase.ai already holds the data and is sold on that basis |
| Index the FOCO payout to contribution instead of fixing it | #6, #7 | FOCO is 500 vehicles; the structure is still cheap to change |
| Publish the rent schedule and cap the repricing lever | #5 | Precedes any contribution-linked incentive, not follows it |
| Finish the battery-swap conversion | #3 | Half the fleet still converting; no new behaviour required |
| Tier-2 expansion behind quick commerce | #2, #3 | Jaipur is the live test |

The first two are one opportunity described twice, and together they are the proposal.

---

## 47. RICE

*Framework note: scored on annual reach in thousands of vehicles, impact 0.25–3, confidence 0–1, effort in person-months. A stress multiplier is then applied to every initiative whose value depends on **new behaviour** by riders, asset investors or client platforms. Initiatives whose value accrues to assets that already exist, requiring no one to change what they do, are exempt.*

**The stress rule is Zypp's own fleet-target realisation: 20.00%** — 20,000 vehicles in November 2025 against the 100,000 promised in November 2023 for 12–18 months out. This is the most generous of three expired, dated targets; the December 2025 target of 200,000 realised at **10.00%** and the 2025 target of 1.5 lakh at **14.67%**. The generous reading is used deliberately. It is the company's own answer to "how much of what you now promise have you previously delivered."

| Initiative | R | I | C | E | **Baseline** | Stressed? | **Stressed** |
|---|---|---|---|---|---|---|---|
| Earnings-linked rental pricing rebuild | 26.7 | 2.0 | 0.80 | 8.0 | **5.34** | yes | 1.07 |
| Tier-2 city expansion (Jaipur pattern) | 15.0 | 2.0 | 0.65 | 6.0 | **3.25** | yes | 0.65 |
| **Zypp Ledger — PROPOSED** | 26.7 | 2.5 | 0.60 | 16.0 | **2.50** | yes | **0.50** |
| Battery-swap conversion of remaining fleet | 13.35 | 1.5 | 0.90 | 9.0 | **2.00** | **exempt** | **2.00** |

**The proposal falls from 3rd of four to last, behind an initiative this case study did not propose.** Finishing the battery-swap conversion wins under stress at **2.00 against the proposal's 0.50 — 4.00×** — because it is the only initiative whose value requires nobody to behave differently. The vehicles exist; converting them raises kilometres per rider-day whether or not a single investor, rider or client changes their mind.

That is not a defect in the scoring. **It is the point.** A company with a 20.00% record of delivering its own stated plans should do the thing that needs no one's cooperation before the thing that needs everyone's. `verify.py` asserts programmatically that Zypp Ledger is the weakest non-exempt initiative at baseline — the only configuration in which it can honestly finish last.

---

## 48. MoSCoW

**Must have:** published per-vehicle contribution definition; independent attestation; a published rent schedule with a cap; owner-facing statement per titled vehicle. **Should have:** contribution reporting by city and client platform; a secondary transfer mechanism for FOCO holdings. **Could have:** third-party benchmarking through FleetEase.ai; contribution history at point of sale. **Won't have (deliberately excluded):** any sales or operations incentive tied to contribution improvement, permanently. If the number that determines an external payout also determines an internal bonus, the number stops being evidence. This exclusion is permanent, not phased.

---

## 49. Kano

**Basic:** vehicle availability, insurance, maintenance, swap access — absence causes immediate defection, presence earns nothing. **Performance:** uptime, hub proximity, rent level, settlement speed. **Delighters:** rent-to-own conversion; for the asset owner, per-vehicle visibility, which currently does not exist anywhere in the category.

The delighter is only a delighter until the first FOCO cohort reaches month 36, at which point it becomes basic.

---

## 50. Feature Proposal

### Zypp Ledger

**Replace the fixed assured FOCO payout with a payout indexed to a published, independently attested per-vehicle contribution measure — and let the asset owner price the variance instead of Zypp absorbing it.**

Three components:

**1. The contribution ledger.** For every vehicle in the fleet, compute daily: revenue attributable to it (direct rent, or its share of delivery settlement where it operates under a client contract) minus directly attributable cost (rider payout share, swap fees, maintenance accrual, insurance accrual, financing accrual). FleetEase.ai already carries assignment, uptime, spares and total-cost-of-ownership data, and Zypp is confident enough in that model to sell it to third parties at ₹149–₹499 per vehicle-month. The ledger is that model, pointed at Zypp's own fleet and closed to settled figures.

**2. The indexed instrument.** New FOCO cohorts are offered a **floor plus share** rather than an assured return: a floor materially below today's ₹1,600–1,900 band, plus a defined share of the attested contribution of the specific vehicles titled to that owner. The owner takes the variance and is paid for taking it. Zypp gives up upside on good vehicles and stops owing on bad ones.

**3. The published rate.** The fleet-level contribution distribution is published quarterly — including the bottom decile, not only the median — so that the instrument can be priced by someone other than the seller.

**Why this is the right shape.** Zypp does not control order volumes at Zomato, Zepto or Blinkit; those platforms set the per-order economics that determine what a rider earns, which determines what Zypp can charge in rent under its own earnings-linked rule. **Every input to a Zypp vehicle's revenue is set by someone else, and the FOCO payout is the one output set in advance.** Indexing it aligns the obligation to the thing it is drawn against.

**Why it is not already there.** Zypp's published FOCO material describes assured monthly payouts, an assured return band, and asset title in the investor's name. It does not describe per-vehicle reporting, a contribution measure, attestation, or any variability in the payout. The absence was verified against the company's own franchise and FOCO materials rather than inferred.

**What it costs Zypp.** Upside. On a vehicle earning well, Zypp currently keeps everything above ₹1,750 a month; under the ledger it shares it. That is a real cost and the proposal does not pretend otherwise. What it buys is that the loss-making vehicle stops carrying a fixed claim — and at a 60.82% implied rental realisation, the loss-making vehicle is not a tail case.

**North Star: CVD/1k.** Contribution-Verified vehicle-Days per 1,000 **deployed** vehicle-days, conjunctive on the four conditions in §31. **Guardrail: RIS-90**, Rider Income Stability at the 90th percentile of rent-repricing intensity, reported by city and client platform, owned by a function with no revenue target.

---

## 51. PRD

**Problem.** Zypp is converting variable, third-party-determined vehicle receipts into fixed 36-month external obligations, at a company spending ₹1.27 per rupee earned, with no per-vehicle economics visible to the party bearing the asset risk.

**Goals.** Fund fleet growth from outside capital without adding fixed claims. Give asset owners a priced, evidenced instrument. Make per-vehicle contribution a managed number.

**Non-goals.** Not a change to rider rent levels — §53 tests the ledger, not a repricing. Not retroactive to existing FOCO contracts. Not a securities offering; characterisation is for counsel, and the design is meant to make it easier rather than harder.

**Success metrics.** CVD/1k as North Star; secondarily capital raised per rupee of fixed obligation created, share of fleet with a computable contribution figure, and attestation coverage.

**User stories.** *As an asset owner,* I want a monthly statement for the vehicles titled to me. *As a rider,* I want to know how my rent is set and what it can rise to. *As a client platform,* I want attested per-delivery cost and emissions evidence. *As a finance lead,* I want fleet growth that creates no fixed 36-month claim.

**Functional requirements.** Daily per-vehicle contribution from settled figures; owner statements; quarterly published distribution including the bottom decile; independent attestation; a published rent schedule with an explicit ceiling.

**Non-functional requirements.** Attestation by a party with no fee contingent on the result. Published figures immutable for the period. **Rider location data aggregated before entering the ledger** — a per-vehicle contribution record is also a per-rider productivity record, and the mechanics must cap resolution so the ledger cannot become a surveillance instrument pointed at the workforce.

**Acceptance criteria.** Contribution computable for ≥90% of the deployed fleet; attested figures reproducible within a published tolerance; rent ceiling published before any contribution-linked payout ships.

**Risks.** Contribution attributable at city but not vehicle level; investors decline variability; the ledger becomes a repricing tool. Each is addressed in §53 and §57.

**Rollout.** §53.

---

## 52. Wireframes

```
┌─────────────────────────────────────────────────────┐
│  ZYPP LEDGER — OWNER STATEMENT        August 2026   │
├─────────────────────────────────────────────────────┤
│  Vehicles titled to you: 100    Deployed: 91        │
│  Contribution-verified vehicle-days: 2,418 / 2,821  │
│  CVD/1k this month:  857                            │
├─────────────────────────────────────────────────────┤
│  Floor payout            ₹  95,000                  │
│  Contribution share      ₹  71,400                  │
│  ─────────────────────────────────────              │
│  TOTAL THIS MONTH        ₹ 166,400                  │
├─────────────────────────────────────────────────────┤
│  YOUR FLEET vs PUBLISHED DISTRIBUTION               │
│   top decile     ████████████████████  ₹2,410       │
│   median         ███████████            ₹1,505      │
│   YOUR AVERAGE   ████████████           ₹1,664      │
│   bottom decile  ████                    ₹  520     │
├─────────────────────────────────────────────────────┤
│  9 vehicles not deployed  ·  reason breakdown  >    │
│  Attested by [independent firm] · 12 Sep 2026       │
└─────────────────────────────────────────────────────┘
```

The bottom decile is on the statement by design. An instrument whose published evidence shows only the median is not evidence.

---

## 53. Rollout Plan

**Phase 0 — two analyst-weeks, on data Zypp already holds. Designed to kill the proposal cheaply.**

Backtest twelve months of the Delhi fleet: vehicle telemetry, rent ledger, swap logs, maintenance records and client settlement files, reconstructing per-vehicle contribution retrospectively.

- **K1.** Per-vehicle contribution cannot be computed to a usable tolerance because rider payouts and client settlements are not attributable below the city or contract level.
- **K2 — named as the one most likely to fire.** Contribution variance is driven overwhelmingly by **city and client platform, not by vehicle**. If the vehicle explains little of the variance, an instrument indexed to vehicle-level contribution is a repriced fixed instrument wearing an expensive apparatus, and the honest response is to price by city and abandon the ledger.
- **K3.** Structured interviews with the first FOCO cohort establish that these buyers will not accept variability at any floor-plus-share combination, in which case the instrument has no buyer and the question is closed.

Phase 0 must clear all three before anything ships. **The published rent schedule and its ceiling ship first regardless**, because §40 says the repricing lever must be capped before any contribution incentive exists, not after.

**Phase 1 (months 2–4).** Ledger computation across the Delhi fleet, unpublished, reconciled monthly to the entity P&L. **Phase 2 (months 5–7).** Attestation engaged; owner statements issued to the existing 500-vehicle FOCO cohort with no change to their contractual payout — reporting first, instrument second. **Phase 3 (months 8–12).** Indexed instrument offered to new cohorts only, alongside the existing fixed product, as the A/B in §54.

---

## 54. A/B Testing

Three arms, offered to comparable new-investor cohorts.

**Arm A — control.** Today's FOCO: assured ₹1,600–1,900 per vehicle-month, no reporting.

**Arm B — the falsification arm, built to kill the thesis.** A **fixed payout at a lower rate, with no ledger, no attestation and no reporting**. This is the cheap imitation that delivers the *benefit* the proposal claims — a smaller fixed obligation — without the *apparatus*. If Arm B raises capital at an acceptable cost, then the ledger, the attestation and the publication are theatre, and the correct decision is to cut the price and skip the machinery.

**Arm C — the proposal.** Floor plus attested contribution share, with owner statements and a published quarterly distribution.

**Pre-registered decision rule.** Arm C proceeds only if it beats Arm B by **more than 10pp on capital raised per rupee of fixed obligation created**, measured across two full cohorts including at least one non-festival quarter, **with RIS-90 no worse in tier-2 cities measured separately from tier-1.** If Arm C wins on capital but RIS-90 deteriorates in tier-2, the proposal does not ship: that combination means the contribution gain was taken out of the riders with the fewest alternatives, which is the failure mode §40 exists to prevent.

---

## 55. KPI Dashboard

| KPI | Basis | Read as |
|---|---|---|
| **CVD/1k** | North Star; denominator = deployed vehicle-days | Falls when a vehicle is added and does not earn |
| **RIS-90** | Guardrail; by city and client platform | Falls when rent repricing lands on weak riders |
| Rider cost ÷ delivery revenue | 109.91% FY25 | **Crossing below 100% is the single most important event** |
| Rental share of operating revenue | 25.35%, falling | Rising means the asset business is actually growing |
| Fleet realisation vs stated target | 20.00% | Rising means guidance is becoming credible |
| Fixed obligation created per ₹ raised | New | The metric FOCO currently has no counter to |
| Capital raised per rupee of fixed obligation | New | Arm B vs Arm C decision variable |
| Cash months at current burn | 8.09 | Recomputed monthly, not annually |

**Earliest warning, first row of the dashboard:** if the FY26 filing breaks out rider cost by segment and delivery-attributed rider cost lands **below** delivery revenue, the central assumption of this case study is dead. Zypp will have to publish that breakdown in a DRHP.

---

## 56. Product Roadmap

**Now (0–3 months):** publish the rent schedule with a ceiling; run Phase 0; finish the battery-swap conversion, which §47 says outranks everything here. **Next (3–9 months):** ledger computation and attestation; owner statements to the existing cohort; the three-arm test. **Later (9–24 months):** indexed instrument at scale if and only if the §54 rule clears; per-delivery attested emissions evidence for client platforms; FleetEase.ai contribution benchmarking as a third-party product.

The battery-swap conversion sits first because the RICE result put it there, not because it is the most interesting item on the list.

---

## 57. Risks & Mitigation

| Risk | Severity | Mitigation |
|---|---|---|
| Contribution not attributable at vehicle level | **High** | K2 in Phase 0; abandon ledger, price by city |
| Ledger becomes a rider-repricing tool | **High** | RIS-90; published rent ceiling ships first; §48 permanent exclusion of contribution-linked sales incentives |
| Investors reject variability | High | K3; Arm A stays available |
| FOCO characterisation questioned by a regulator | **High** | §40; indexation removes the "assured" characteristic that creates the question |
| Fixed obligations accumulate faster than contribution | High | Fixed-obligation-per-rupee-raised on the §55 dashboard |
| Client platforms in-house their fleets | High | Not mitigable by Zypp; the reason contribution visibility matters |
| Mandate universalises the EV differentiator | Medium | Compete on attested cost per delivery, not on being electric |
| Gig-welfare levies raise rider cost | Medium | Karnataka live from 13 Feb 2026 at 1% with per-transaction caps |
| Fleet targets missed again | Medium | 20.00% realisation is already priced into §47 |

---

## 58. Future Vision

The version of Zypp that works at 100,000 vehicles is not a bigger version of today's. It is a company that owns very few vehicles, operates a very large number of them for other people, and is paid a fee for operating rather than a spread on renting — with the asset yield flowing to whoever supplied the asset, priced on published evidence.

That company has a defensible position even after electrification stops being a differentiator, because what it sells is attested cost per delivery rather than a scooter.

---

## 59. PM Lessons

**1. Ask which line the growth came from before accepting the category label.** Zypp is called EV-as-a-Service; 79.85% of its FY25 growth came from supplying labour. The label described the smaller, shrinking half.

**2. When a cost line exceeds the revenue line it maps to, that ratio is the case study.** ₹355 Cr against ₹323 Cr is one division that reframes a growth story — and running it for the prior year too, where it was worse at 115.07%, is what turns an accusation into a trend.

**3. Find the competitor built the opposite way in the same year.** Yulu earns 84.67% of revenue from rental where Zypp earns 25.35%, at EBITDA margins 0.69pp apart. That single comparison separates what is true of the category from what is true of the company.

**4. Count the targets that have already expired.** Three dated fleet targets, all matured, realised at 10.00%, 14.67% and 20.00%. Using the most generous of them makes the resulting stress rule impossible to argue with.

**5. When a company changes how it funds an asset, read the instrument as a product decision.** FOCO is presented as financing, but it is a promise with a term, a rate and a counterparty, made by a company whose receipts are set by third parties.

**6. A regulator that mandates your differentiator has not helped you.** Delhi's mandate guarantees the category's volume and destroys the reason to choose Zypp specifically — the same structure as efficiency labelling against Atomberg on Day 61.

**7. State the reading that favours the company first, and mean it.** Individual title with no pooling is the structure designed to sit outside the CIS definition; saying so first is what makes the remaining question worth reading.

---

## 60. PM Interview Questions

1. Zypp's rent falls when a rider's earnings rise. Who bears the variance, and what does that imply about which party should own the vehicle?
2. Delivery is 73.76% of revenue with a direct cost at 109.91% of it. Would you shrink it, reprice it, or keep growing it — and what evidence would settle the question?
3. FOCO converts fleet capex into a fixed 36-month payout. Under what receipt volatility does that become the wrong trade?
4. Yulu earns 84.67% of revenue from rental and Zypp 25.35%, at near-identical EBITDA margins. What does that tell you that neither company's own numbers could?
5. Design a North Star for a fleet business that cannot be improved by adding vehicles.
6. Delhi mandates 100% electric delivery fleets by 2030. Write the three-line strategy memo for a company whose entire pitch is being electric.
7. Your contribution metric could be improved by raising rent on the lowest-earning riders. What do you build before you ship it?

---

## 61. References

1. Entrackr — Zypp Electric FY25 financials from RoC filings, 18 February 2026.
2. BW Disrupt — Zypp Electric FY25 revenue and cost breakdown, February 2026.
3. Startuppedia — Zypp Electric FY25 segment revenue detail, March 2026.
4. Inc42 — "Inside Zypp Electric's Bold Diversification Drive Beyond India's Tier I," 12 November 2025.
5. Inc42 — "Zypp Electric Gears For $200 Mn IPO, Eyes Listing In FY28," 22 June 2026.
6. Business Standard — "Zypp Electric targets 5x fleet in 2-3 years," 24 November 2025.
7. Entrepreneur India — Zypp FOCO deployment of 500 EVs, October 2025.
8. Inc42 — "Zypp Electric Trims 10% Workforce Over 'Performance' Issues," 26 March 2025.
9. TechCrunch — ENEOS-led Series C and fleet detail, 26 May 2024.
10. TechCrunch — Gogoro-led Series B and 200,000-vehicle target, 8 February 2023.
11. Forbes India — Zypp fleet of 17,000 and rider-partner conditions, November 2023.
12. Autocar Professional / Outlook Business — Zypp–Indofast 1 lakh EV deployment, February 2025.
13. Entrackr — Yulu FY25 financials from RoC filings, 2 December 2025.
14. Inc42 — Yulu FY25 revenue and expenditure detail, 5 December 2025.
15. Transport Department, GNCT Delhi — Delhi Motor Vehicle Aggregator and Delivery Service Provider Scheme, 2023 (notified 29 November 2023).
16. Deccan Herald — CAQM direction barring new ICE fleet additions in NCR from 1 January 2026.
17. JMK Research — analysis of DMVADSPS electrification targets by vehicle category.
18. SCC Online / JSA — Karnataka Platform Based Gig Workers (Social Security and Welfare) Act and Rules, 2025; welfare fee effective 13 February 2026.
19. SEBI — Section 11AA, SEBI Act; Securities Laws (Amendment) Act, 2014 deeming provision; CIS investor cautions.
20. Vinod Kothari Consultants — fractional ownership schemes and the CIS boundary.
21. IndiaCorpLaw — unregistered CIS and joint-ownership structures, April 2024.
22. Zauba Corp / Tofler / Tracxn — Bycyshare Technologies Private Limited registry records, CIN U63000HR2017PTC070227.
23. Google Play — Zypp Pilot app listing, rental and earnings-linked rent description.
24. zypp.app — franchise, rent-to-own and rental product pages.
25. Startuptalky / Outlook Business / Electronics For You — IPO banker appointments and pre-IPO round, June 2026.

---

## 62. About the Author

**Gaurav Singh** — Product Manager. This is Day 64 of a 90-day series of evidence-based product management case studies, each built from primary filings and disclosures, with every derived figure verified programmatically before publication.

---

## 63. License

Released under CC BY 4.0. All financial figures are sourced from filings and public reporting as cited. Analysis, proposals and constructed scenarios are the author's own and are labelled as such throughout. Nothing here is investment advice, legal advice, or an assertion of wrongdoing by any party.

---

## 64. Self Review

**What is strongest.** The Yulu mirror. Two companies, same category, same year, near-identical EBITDA margins, inverted revenue construction — that comparison establishes the finding is about Zypp specifically rather than about EV fleet leasing generally, which no amount of single-company analysis could have done.

**What is weakest, stated plainly.** A1 rests on "rider-related expenses" being attributable primarily to the delivery line. The source describes that bucket as covering production, transportation and operational activities, which may include costs supporting the rental business too; if a material share does, 109.91% overstates the delivery line's cost. The finding survives because the ratio exceeds 100% in both years and because the §18 mix shift is independently visible — but it is one line item carrying a lot of weight, and ASSUMPTIONS Part 1 gives the rival reading equal space.

**What was cut.** An early draft treated the FOCO payout as unambiguously senior to all other claims. It is not — it is a contractual obligation to an asset owner whose asset is titled in his own name, and its priority in a stress scenario is genuinely unclear without the contract. The claim was reduced to what the arithmetic supports: fixed, external, 36 months, drawn against variable receipts.

**What I would do differently.** Reach the FOCO contract itself. Every quantitative statement about the instrument here rests on marketing descriptions and press interviews, which is why §40 flags an internal inconsistency in those descriptions rather than resolving it.

**Rating: 8.5/10** after the verification pass, up from 7 before it. The cross-check found two figures asserted in the draft that no check covered, and the RICE configuration initially failed the house constraint that the proposal must be the weakest non-exempt initiative at baseline.

---

## 65. Appendix

### Appendix A — Source Conflicts

**A-1 · Four different figures for FY25 revenue.** ₹437.9 Cr (operating revenue, RoC), ₹448 Cr (Inc42), ₹449 Cr (total income), ₹455 Cr (company statement, April 2025). The differences are basis differences — operating versus total income versus a company-communicated number — not contradictions. **Operating revenue of ₹437.9 Cr is used throughout**, and total income of ₹449 Cr is used only where explicitly labelled. 🟡

**A-2 · Two CINs in circulation.** U63000HR2017PTC070227 (current, NIC 630) and U74999HR2017PTC070227 (stale, NIC 74999), same registration number 070227, same incorporation date. **This is the fourth case study in the series to hit this pattern** — Days 57, 59, 61 and now 64 — and it is now a standing pre-publication check. The current CIN is used. 🟢

**A-3 · Two EBITDA margins for FY25.** −15.98% (Entrackr, computed on operating revenue) and −13.20% company-stated, a gap of **2.78pp** or **₹12.17 Cr** of implied EBITDA. The company also states ~+2% for the single month of September 2025, which is a monthly figure and not comparable to either. Both annual readings are negative, so direction is robust and level is not. Neither is used as load-bearing. 🔴

**A-4 · The FOCO return description does not reconcile with itself.** ₹1.6–1.9 lakh per month on 100 vehicles over 36 months implies **₹57.6–68.4 lakh**; the stated three-year total is **₹60–66 lakh**; the stated return is "40–50%"; a separate account describes "59% to 100%," and the CEO separately describes 80–100% assuming payouts are reinvested elsewhere. The monthly figures are used, and the discrepancy is reported in §40 rather than resolved. 🟠

**A-5 · Founder attribution.** Most sources name Akash Gupta and Rashi Agarwal as founders with Tushar Mehta joining in 2021; at least one names Gupta and Mehta as founders. The majority reading, which is consistent with the registry's director history, is used. 🟡

**A-6 · Total funding raised.** $76.5 Mn (Tracxn, Entrackr), $57.1 Mn (CB Insights), $56.1 Mn (Atlas-filed), ~$80 Mn (one report). The most widely corroborated figure, $76.5 Mn, is used and flagged. 🟠

**A-7 · Valuation.** ~$331 Mn (Tracxn, March 2025), ~$322 Mn (Outlook), $280 Mn (CB Insights, May 2024). Used only as approximate context. 🟠

**A-8 · Fleet counts are not a clean series.** 17,000 (Nov 2023), 22,000 (May 2024), 20,000 (Nov 2025, described as across three cities), 22,000+ (Mar 2026 reporting), 26,700 usable (stated for period ending Mar 2026). The Nov 2025 figure is city-scoped and may not be comparable to the others. The stress rule uses it because it is the count the company itself gave alongside its forward target. Sensitivity is disclosed at §47. 🟡

**A-9 · Segment lines do not sum exactly.** ₹323 + ₹111 + ₹4 = ₹438.0 Cr against operating revenue ₹437.9 Cr — a ₹0.10 Cr residual, **0.02%** of revenue, from rounding in the reported figures. Disclosed, not smoothed. 🟢

**A-10 · Rental realisation is a derived band, not a disclosure.** ₹152.05 per vehicle-day at a 20,000 fleet, ranging **55.29%–71.56%** of list across a 17,000–22,000 fleet band. Two readings of the gap are given equal weight in §39. The direction — materially below list on every assumption — is robust; the level is not. 🟠

### Appendix B — Evidence Grades

🟢 **High** — filed or officially notified: FY25 and FY24 P&L aggregates from RoC filings; registry particulars; the Delhi aggregator scheme and CAQM direction; the Karnataka gig-worker welfare fee; Yulu's FY25 filings; SEBI's statutory provisions.

🟡 **Medium** — company statements to named journalists, single-sourced but attributed: fleet counts, market-share claims, the ₹250 daily rent, the ₹600 Cr FY26 target, FleetEase.ai and advertising revenue expectations, uptime, hub and mechanic counts.

🟠 **Low** — marketing descriptions, aggregator data, or figures with wide unresolved ranges: FOCO terms and returns, total funding, valuation, the derived rental realisation band.

🔴 **Conflicting** — the two FY25 EBITDA margins.

### Appendix C — Author-Constructed Content

Author-constructed, appearing nowhere in Zypp's disclosures: the CVD/1k and RIS-90 metrics; the Zypp Ledger proposal; the RICE initiative set, scores and stress rule; the Phase 0 kill criteria; the three-arm test and decision rule; the §52 wireframe and all figures in it; and the scenario arithmetic scaling FOCO to the 100,000-vehicle target. **Zypp has not announced any intention to fund its fleet target through FOCO at scale** — that scenario sizes the obligation the mechanism would create if used as the primary route, and 500 vehicles, **1.87% of the March 2026 fleet**, is where the programme stands. Derivations in ASSUMPTIONS.md Part 3.

### Appendix D — Asset Status

`README.md` — 65 sections, published. `ASSUMPTIONS.md` — Parts 1–5, published. `verify.py` — **145 checks, all passing**, delivered but not committed. `carousel.pdf` and `LINKEDIN_CAROUSEL_CAPTION.md` — local delivery only.

---

*Day 64 of 90 · [← Day 63 — BookMyShow](../Day-63-BookMyShow) · Day 65 →*
