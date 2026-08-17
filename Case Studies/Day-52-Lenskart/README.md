# Lenskart — Priced for the 943 Million It Hasn't Met Yet

### Day 52 of 90 · Product Management Case Study Series

> **The thesis of this case study:** Lenskart's IPO story and its rival Titan Eye+'s public skepticism about it are, underneath the numbers, a disagreement about where India's eyewear growth actually comes from. Titan sizes the addressable market at $3.4B — organised-sector eyeglass retail, the market Titan itself has spent two decades building. Lenskart sizes it at $9.2B, nearly three times larger, by including unorganised sales and — critically — the latent demand of roughly **943 million Indians the company's own DRHP says still need vision correction and don't have it**. Lenskart's ₹70,000+ Cr IPO valuation (and the ₹1,06,419 Cr market cap it has since grown into) is not priced for winning share from Titan. It is priced for converting people who currently own no glasses at all. And here is the tension this case study identifies: Lenskart's most visible, most reported growth metrics — store count, app downloads, eye tests conducted (13 million in FY25, rising to 9.3 million in H1 FY26 alone) — are aggregate numbers that don't distinguish a repeat urban customer getting a routine check-up from a first-time rural test-taker discovering they need glasses for the first time. The company's own FY25 profit of ₹297 Cr, meanwhile, included a **₹167.2 Cr one-time, non-cash fair-value gain** on deferred Owndays acquisition consideration — meaning more than half of the headline profit number that anchored the IPO story wasn't operating profit at all. Lenskart is a genuinely strong, cash-generative retail business (₹1,670 Cr of FY26 operating cash flow says so). The specific number the market is paying 200-plus times earnings for — conversion of India's uncorrected-vision population — is the one number the company has not yet shown it can track, let alone move, as a distinct, disclosed cohort.

---

## 2. Repository Metadata

| Field | Value |
|---|---|
| **Case study** | Day 52 of 90 |
| **Product** | Lenskart — omnichannel eyewear (prescription glasses, sunglasses, contact lenses) |
| **Company** | Lenskart Solutions Ltd. (originally Valyoo Technologies Pvt Ltd, incorporated 2008), Faridabad/Delhi-NCR HQ |
| **Domain** | D2C / omnichannel retail — eyewear and eye care |
| **Primary competitors** | Titan Eye+, EssilorLuxottica, GKB Opticals, Specsmakers, Lawrence & Mayo, the large unorganised local-optician sector |
| **Analysis type** | Research-led product teardown + financial reconstruction + a feature proposal |
| **Proposed system** | **First Pair Promise** — a disclosed, separately-tracked conversion product for first-time, previously-uncorrected eye-test takers |
| **Author** | Gaurav Singh |
| **Date of analysis** | 17 August 2026 |
| **Research boundary** | Public sources only — DRHP disclosures, quarterly shareholder letters, exchange filings, trade press. No Lenskart employee, internal document, or authenticated session was consulted. |
| **Latest financials available** | Q4 FY26 / full-year FY26 results (year ended 31 March 2026), per Lenskart's Q4 FY26 shareholders' letter (May 2026) and subsequent filings |

---

## 3. Badges

![Case Study](https://img.shields.io/badge/Case%20Study-Day%2052%20of%2090-blue)
![Domain](https://img.shields.io/badge/Domain-D2C%20Retail-orange)
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

Lenskart is an 18-year-old (founded 2008) omnichannel eyewear company — design, manufacturing, and retail of prescription eyeglasses, sunglasses, and contact lenses — that listed on the NSE/BSE in November 2025 in one of the year's largest Indian consumer-tech IPOs (₹7,278 Cr raised, priced at ₹382–402/share, valuing the company around ₹69,727 Cr / ~$7.9B at listing). Since then the stock has performed strongly: as of 17 August 2026 it trades around **₹617**, giving a market cap of roughly **₹1,06,419 Cr (~$12B)**, at a trailing P/E in the 200–277x range depending on the quarter measured — among the most expensive large-cap consumer stocks in India by that metric.

The company operates 2,723+ stores globally (2,067+ in India, growing to 2,439+ by Q3 FY26 and adding 542 net new India stores in FY26 alone, nearly double FY25's 282), centralised manufacturing in Bhiwadi and Gurugram, and international operations spanning Singapore, the UAE, and — via its stake in Owndays — Japan and Southeast Asia. FY25 revenue was ₹6,652.5 Cr (up 22.6% YoY, a deceleration from 43% growth the year before), and FY26 revenue rose a further ~32% to ₹8,814 Cr (later TTM figures show ₹9,634 Cr). FY25 marked the company's first full year of consolidated net profit — ₹297.3 Cr, against a ₹10.1 Cr loss in FY24 — and FY26 profit rose to roughly ₹494–501 Cr depending on the exact reporting cut.

**The number worth sitting with:** of FY25's ₹297.3 Cr reported profit, **₹167.2 Cr (₹1,672 million) was a one-time, non-cash fair-value gain** on the deferred consideration for Lenskart's acquisition of an additional Owndays stake — a mark-to-market accounting item with zero cash impact, which Lenskart's own Q4 FY26 shareholders' letter explicitly flags and excludes from its "adjusted" comparisons going forward, precisely because leaving it in distorts year-on-year optics. On an adjusted basis, the company reports FY26 PAT growth of ~148% rather than the ~68% headline figure — meaning the *adjusted* growth story is actually stronger than the headline one, which is a genuinely reassuring detail once it's disclosed. The issue this case study raises is not that Lenskart is hiding weak fundamentals — operating cash flow of ₹1,670 Cr in FY26 (up from ₹1,231 Cr in FY25) says the core business throws off real cash. The issue is that the company's own valuation argument (§13) depends on a TAM claim — $9.2B versus Titan Eye+'s $3.4B, a gap driven entirely by whether you count India's roughly 943 million people who reportedly still need vision correction and don't have it — that is not yet supported by any disclosed, separately-tracked conversion metric for that specific population.

Lenskart already runs the funnel that would answer this question: **13 million eye tests in FY25**, rising to 9.3 million in H1 FY26 alone, with **46% reported as first-time tests**. That is precisely the cohort — first-time test-takers discovering a vision problem they hadn't previously addressed — whose conversion-to-purchase rate would validate or undercut the $9.2B TAM claim. It is not, as far as public disclosure shows, reported as its own tracked funnel. This case study's proposal — **First Pair Promise** (§50) — is a product built to convert and *measure* exactly this cohort, because right now the market is paying a premium multiple for a number Lenskart hasn't shown it can move.

---

## 6. Product Overview

Lenskart is a direct-to-consumer, vertically integrated eyewear company spanning app/e-commerce, 2,700+ physical stores, in-house frame and lens manufacturing, and eye-testing services (in-store and increasingly at-home/community outreach). Its core loop is unusually tight for retail: a customer can get an eye test, choose frames, and receive glasses with next-day delivery in 40 Indian cities (3-day in 69 more) — a supply chain built around centralised manufacturing rather than third-party lens labs, which is the structural basis of its ~70% gross margin.

---

## 7. Company Background

Founded in 2008 by Peyush Bansal (CEO) along with co-founders, originally incorporated as Valyoo Technologies. Grew from a modest ₹967 Cr revenue base in FY20 to ₹5,428 Cr in FY24 and ₹6,652 Cr in FY25 — a trajectory that included a breakout FY23 (revenue more than doubling to ₹3,788 Cr). SoftBank-backed among other investors; converted its parent entity from private to public limited in mid-2025 ahead of listing. Filed a public DRHP (unusually, given peers in this series' Zepto and Ola case studies both filed confidentially) in July 2025, listed in November 2025, and has since pursued international expansion, notably increasing its stake in Japan's Owndays — the acquisition whose deferred-consideration accounting produced the one-time FY25 gain central to this case study's thesis (§5, §18).

---

## 8. Product Timeline

| Year | Milestone |
|---|---|
| 2008 | Founded as Valyoo Technologies |
| 2020 | Revenue ≈₹967 Cr |
| 2023 (FY23) | Revenue more than doubles to ₹3,788 Cr |
| 2024 (FY24) | Revenue ₹5,428 Cr (+43%); still net-loss-making (₹10.1 Cr loss) |
| 2025 (Jul) | Public DRHP filed with SEBI |
| 2025 (Nov) | IPO: ₹7,278 Cr raised, ₹382–402/share, ~₹69,727 Cr listing valuation; FY25 results disclosed: revenue ₹6,652.5 Cr, first full-year consolidated profit ₹297.3 Cr |
| 2026 (May) | Q4/FY26 results: FY26 revenue ₹8,814 Cr, PAT ₹493.6–500.9 Cr depending on cut; company discloses and excludes the FY25 one-time Owndays FVTPL gain from "adjusted" comparisons |
| 2026 (May–Jun) | Two large post-lock-in block deals by pre-IPO investors (₹5,313.58 Cr on May 8; ₹2,873 Cr on Jun 3) as the 6-month IPO lock-in expires |
| 2026 (Aug) | Stock trades around ₹617, market cap ≈₹1,06,419 Cr |

---

## 9. Vision & Mission

Lenskart's public narrative, reinforced in its DRHP and shareholder communications, centres on solving India's uncorrected-vision problem at scale — not just selling glasses to people who already know they need them, but *finding* the people who don't yet know, through mass eye-testing (including rural outreach via the Lenskart Foundation's "Drishti – Har Gaon, Har Ghar" programme, which the company reports has screened over 910,000 individuals across 940 villages).

---

## 10. Problem Statement

**For the company:** the valuation the market has assigned depends on a TAM claim (§13) that is contested by its nearest organised competitor and not yet validated by any disclosed conversion metric specific to the population that claim is about.

**For the user (first-time test-taker):** discovering a vision problem for the first time — often in a tier-2/3 town or rural outreach setting — is a different purchase decision than a repeat urban customer's routine reorder, with different price sensitivity, different trust barriers, and (plausibly) a much higher first-purchase abandonment rate that the current funnel doesn't appear to isolate and report.

---

## 11. Market Research

Estimates of India's eyewear market vary by an order of magnitude of scope, not just degree: Titan Eye+ sizes the *organised* market at $3.4B (FY25); Lenskart's own DRHP-cited RedSeer figure sizes the *total addressable* market, including unorganised sales and latent demand, at $9.2B (FY25), projected to reach $17.2B by FY30; a separate industry report (Custom Market Insights) pegs the India eyewear market at a narrower $6.6B (2024) growing at ~12% CAGR. Prescription eyeglasses account for roughly 73% of category value, sunglasses ~22%, contact lenses ~5%, per the RedSeer breakdown cited in Lenskart's DRHP. The organised share of the overall market is around 24%, projected by Lenskart to reach 31% by FY30.

---

## 12. Industry Analysis

The competitive landscape has two structurally different players at the top: **Lenskart** (VC-scaled, D2C-first, vertically integrated manufacturing, ~25% share of the *organised* market by the company's own account) and **Titan Eye+** (Tata Group-backed, ~900 stores, disciplined "Network Optimisation" — closing ~30 underperforming stores in 2025 to protect its ~10% EBIT margin rather than chase volume). International giant EssilorLuxottica and a long tail of regional chains (GKB Opticals, Specsmakers, Lawrence & Mayo) and thousands of unorganised local opticians make up the rest. The Titan-vs-Lenskart TAM dispute (§11) is, functionally, a proxy war over which growth strategy the market should reward: Titan's "deepen organised share" thesis versus Lenskart's "convert the uncorrected" thesis.

---

## 13. TAM / SAM / SOM

### 13.1 TAM — genuinely contested, not just estimated differently
| Source | FY25 estimate | Basis |
|---|---|---|
| Titan Eye+ | $3.4B | Organised-sector-only |
| Lenskart (DRHP, RedSeer) | $9.2B | Includes unorganised sales + latent uncorrected-vision demand |
| Custom Market Insights | $6.6B (2024 figure) | Independent third-party report, narrower scope than Lenskart's |

### 13.2 The number the whole gap rests on
Per Lenskart's DRHP-adjacent disclosures, **943 million Indians are estimated to need vision correction**, against 242 million pairs of eyewear sold in FY25 — meaning even a bottom-up, unit-based accounting shows a vast gap between correction need and units sold. Lenskart projects unit sales to reach 389 million by FY30. The $9.2B-vs-$3.4B TAM gap is, in practice, the dollar value of the delta between "people who need glasses" and "people who currently buy them from an organised retailer."

### 13.3 SAM
Lenskart's own claimed ~25% share of the organised market, applied against whichever TAM figure a reader trusts, produces wildly different SAM estimates — from roughly $850M (25% of Titan's $3.4B) to roughly $2.3B (25% of Lenskart's own $9.2B). This spread is itself the finding: **Lenskart's addressable market estimate is not a fixed number, it is a bet on which theory of growth is correct.**

### 13.4 SOM — financial reconstruction

| Metric | FY24 | FY25 | FY26 |
|---|---|---|---|
| Revenue from operations | ₹5,427.7 Cr | ₹6,652.5 Cr (+22.6%) | ₹8,814.0 Cr (+32.5%) |
| Reported net profit | −₹10.1 Cr | ₹297.3 Cr | ₹493.6–500.9 Cr (source-dependent) |
| Of which: one-time non-cash FVTPL gain (Owndays deferred consideration) | — | **₹167.2 Cr** | Excluded from FY26 base by company's own adjusted reporting |
| Adjusted (company-reported) PAT growth, FY25→FY26 | — | — | **≈148%**, vs 68% on an unadjusted comparison |
| Operating cash flow | — | ₹1,230.6 Cr | ₹1,669.6 Cr |
| Eye tests conducted | ~5M (FY23 baseline) | 13M | 9.3M in H1 alone |
| First-time eye tests | — | ~46% of total (recent quarters) | ~50.1% (India, Q4 FY26) |

### 13.5 The profit-composition finding
₹167.2 Cr of ₹297.3 Cr FY25 reported profit — **≈56%** — was the one-time, non-cash Owndays fair-value gain (D1, ASSUMPTIONS.md). This is disclosed by the company itself in its Q4 FY26 shareholder letter, which is a point in its favour on transparency; it is nonetheless the case that most press coverage of the IPO (§65 References) reported the ₹297 Cr figure as straightforwardly "first full year of profitability" without this composition detail.

---

## 14. Competitor Analysis

| Dimension | **Lenskart** | Titan Eye+ | EssilorLuxottica (India ops) |
|---|---|---|---|
| Store count (India) | 2,067+ → 2,439+ (Q3 FY26) | ~900 (post network optimisation) | Smaller footprint, brand/wholesale-led |
| Strategy | Volume + first-time-buyer conversion | Margin discipline, "profitable precision" | Premium/luxury brand distribution |
| FY25 domestic revenue | ~₹3,865 Cr (India) | ~₹786 Cr | Not separately disclosed |
| Margin profile | ~70% gross margin, thinner net margin historically | ~10–11% EBIT margin, stated explicitly as a strategic choice | Not disclosed for India specifically |
| TAM claim | $9.2B (RedSeer, DRHP) | $3.4B (organised-only) | N/A |
| Listing status | Listed Nov 2025 | Part of listed Titan Company | Listed globally (Euronext Paris) |

---

## 15. SWOT

| Strengths | Weaknesses |
|---|---|
| Vertically integrated manufacturing → ~70% gross margin | Reported profit composition includes a large one-off non-cash item (§13.5) |
| Largest store network and eye-test volume in the category | Growth rate decelerating (43%→22.6%→32.5%, not monotonic — flagged in Appendix A) |
| Strong operating cash generation (₹1,670 Cr FY26) | Extremely premium valuation (200x+ P/E) leaves little room for a growth miss |
| First-mover in mass eye-testing as an acquisition channel | ~40%+ raw-material/component sourcing tied to Chinese suppliers (tariff exposure) |

| Opportunities | Threats |
|---|---|
| 943M-person uncorrected-vision population, if convertible | Titan's disciplined, lower-multiple model could win the "trust" battle in Tier-2/3 towns |
| International expansion (Owndays/Japan, Singapore, UAE) | Post-lock-in insider selling (₹8,186 Cr+ in block deals within a month of lock-in expiry) signals early investors taking profits |
| Organised-sector share still only ~24%, rising toward a projected 31% by FY30 | Valuation risk: any growth deceleration at 200x+ P/E likely triggers a sharp re-rating |

---

## 16. Porter's Five Forces

| Force | Intensity | Note |
|---|---|---|
| Competitive rivalry | Medium-high | Two structurally different strategies (Lenskart volume vs. Titan margin) competing for the same organised-sector growth |
| Threat of new entrants | Medium | Capital-intensive (manufacturing, store network) but D2C-only entrants (smaller online-only brands) can still compete on price |
| Bargaining power of suppliers | Medium | Chinese-sourced components create geopolitical/tariff exposure |
| Bargaining power of buyers | Medium-high | Price-comparable across Lenskart/Titan/local opticians for standard prescriptions; brand and trust differentiate more than price alone |
| Threat of substitutes | Low-medium | Unorganised local opticians remain the default for most of India, which is both a threat (entrenched habit) and the opportunity (§13.2) |

---

## 17. Business Model Canvas

| Block | Summary |
|---|---|
| Key Partners | Owndays (Japan, equity stake), lens/frame component suppliers (incl. China), Lenskart Foundation (CSR/outreach) |
| Key Activities | In-house manufacturing, eye testing, omnichannel retail, international expansion |
| Value Propositions | Affordable, fast (next-day in 40 cities), tech-enabled (3D try-on, AI-assisted eye tests) eyewear |
| Customer Relationships | App + store hybrid; eye test as the primary relationship-starting touchpoint |
| Customer Segments | Urban repeat buyers; first-time/rural test-takers (the segment this case study focuses on); international (Japan/SEA via Owndays) |
| Channels | App, website, 2,700+ stores, community outreach programmes |
| Key Resources | Manufacturing facilities (Bhiwadi, Gurugram), brand, eye-test infrastructure, tech team (500+) |
| Cost Structure | Store leases (CoCo model expansion), manufacturing, technology, marketing, employee costs |
| Revenue Streams | Eyewear and lens sales (glasses, sunglasses, contacts), international retail (Owndays) |

---

## 18. Revenue Model

Lenskart's revenue mix is roughly 60% domestic / 40% international (Owndays-driven), with prescription eyewear the dominant category. The company's ~70% gross margin, driven by owning manufacturing rather than outsourcing to third-party labs, is the structural reason it can fund an eye-test-led acquisition funnel (a genuine health-service cost) without it dragging down unit economics the way a pure marketing-spend acquisition channel would. This is a real strength — but it also means the *quality* of that funnel matters more than for a company where acquisition and manufacturing are separate cost lines, because the eye test itself is not free to deliver at scale (optometrist time, equipment, outreach logistics).

---

## 19. Target Users

- **Urban repeat buyers** — already own glasses, reordering or upgrading, well-served by the existing app/store experience.
- **Urban first-time buyers** — younger, screen-time-driven vision issues, price- and brand-aware, likely to convert well already.
- **Tier-2/3 and rural first-time test-takers** — the segment this case study argues is under-measured (§13.5, §46), often discovering a vision problem through outreach (e.g., Drishti Didis) rather than self-initiated app usage.

---

## 20. Personas

**Persona — Ritika, 26, Bengaluru, software engineer (Construct)**
Second-time Lenskart buyer, orders through the app, values next-day delivery and the home try-on/3D feature. Already fully served by the existing product; not the segment this case study is concerned with.

**Persona — Manoj, 52, small-town Bihar, shop owner (Construct)**
Never owned glasses; vision has been declining for years but assumed it was just age. Gets a free eye test through a Lenskart Foundation outreach camp, is told he needs glasses for the first time. Price-sensitive, has never bought anything "prescription" online, doesn't fully trust an app-based purchase for something as personal as his eyesight. **The exact profile the $9.2B TAM claim depends on converting — and the one this case study argues the current funnel doesn't separately track.**

**Persona — Aarav, 19, Tier-2 city, college student (Construct)**
First-time test-taker via a college outreach camp, screen-time-driven myopia, price-sensitive but digitally comfortable — a "middle" persona between Ritika and Manoj, more likely to convert than Manoj but still meaningfully different from an urban repeat buyer in trust and price sensitivity.

---

## 21. Jobs to Be Done

- Repeat buyer: "Get my next pair, fast, matching my existing prescription." (well served today)
- First-time urban buyer: "Help me figure out if I actually need glasses, and make buying my first pair easy." (reasonably well served — app-native, digitally comfortable)
- **First-time rural/Tier-2/3 test-taker: "I just found out I need glasses I didn't know I needed — now what?"** (the underserved job this case study targets — trust, affordability, and follow-through are all different problems than the urban first-time buyer faces)

---

## 22. User Journey (first-time, previously-uncorrected segment)

`Outreach camp / community eye test → told correction is needed (often a surprising, sometimes unsettling moment) → [funnel currently unclear from public disclosure] → purchase or non-purchase, not separately reported`

The gap: everything after "told correction is needed" is a black box in public reporting. Aggregate eye-test and revenue figures don't show what fraction of first-time, previously-uncorrected test-takers actually complete a purchase, or how long that takes.

---

## 23. User Flow

`Eye test (in-store or outreach) → prescription generated → frame/lens selection → purchase (in-store or app) → delivery`

**Gap (Construct):** no visible branch in public disclosure differentiates "first-time, previously uncorrected" from "repeat/routine" at the point the prescription is generated — which is exactly where a differentiated flow (financing options, trust-building content, follow-up) would need to start.

---

## 24. Information Architecture

`Home → Eye Test (book/find center) → Shop (Glasses/Sunglasses/Contacts) → Try-On (3D/AR) → Cart → Orders → Foundation/CSR (separate microsite)`

**Gap:** the Foundation/outreach arm and the commercial purchase funnel appear, from public description, to be largely separate systems rather than one continuous, measured journey.

---

## 25. UX Audit

| Area | Observation |
|---|---|
| App/in-store try-on | Strong, frequently cited as a differentiator (3D try-on, AI-assisted fit) |
| Delivery speed | Genuine strength — next-day in 40 cities |
| First-time-buyer trust building | Not independently assessed here; the persona gap in §20 (Manoj) suggests this is under-addressed for the rural/Tier-2/3 segment specifically |

---

## 26. UI Audit

Not independently screenshot-audited in this document (public-sources-only boundary; Appendix D).

---

## 27. Accessibility

Not independently tested in this analysis — genuinely relevant for an eye-care company (low-vision users are a natural accessibility consideration) but outside this document's research boundary.

---

## 28. Feature Breakdown

| Feature | Status | Notes |
|---|---|---|
| 3D/AR try-on | Live | Rider-side (urban, digitally comfortable) strength |
| Community eye-test outreach (Drishti) | Live, CSR-branded | The acquisition channel for the underserved segment |
| Financing/EMI for first purchase | Not clearly documented in public sources as differentiated for first-time/low-income buyers | Gap this proposal addresses |
| Disclosed first-time-tester conversion funnel | **Does not exist publicly** | The core gap |

---

## 29. AI Capabilities

Public product coverage describes AI-assisted eye testing and 3D try-on/fit recommendation as part of the tech-enabled retail experience; a 500+ person tech team is disclosed. No public breakdown separates AI-driven diagnostic accuracy or outreach-camp equipment capability from the flagship in-store/app experience.

---

## 30. Product Metrics

| Metric | FY24 | FY25 | FY26 |
|---|---|---|---|
| Revenue | ₹5,427.7 Cr | ₹6,652.5 Cr | ₹8,814.0 Cr |
| Net profit (reported) | −₹10.1 Cr | ₹297.3 Cr | ₹493.6–500.9 Cr |
| Eye tests | ~5M (FY23) | 13M | 9.3M (H1 alone) |
| First-time test share | — | — | ~46–50% |
| India store count | — | 2,067 | 2,439+ (Q3), net +542 for the year |
| Operating cash flow | — | ₹1,230.6 Cr | ₹1,669.6 Cr |

---

## 31. North Star Metric

**Verified First-Correction Rate (VFCR)** *(Construct — does not exist at Lenskart)*: the share of first-time, previously-uncorrected eye-test takers who complete a purchase within 90 days of being told they need correction. Proposed as North Star because it is the single metric that would most directly validate or challenge the $9.2B TAM claim — a metric revenue and store-count growth alone cannot answer, since both can grow entirely from the already-converted, already-organised-market segment.

---

## 32. Product Analytics

Three analytics objects this proposal would require (Constructs, not currently public):
1. **First-Time Tester Conversion Funnel** — outreach/test → prescription → purchase, tracked as a distinct cohort from repeat buyers.
2. **Time-to-First-Purchase** for the first-time-uncorrected cohort specifically.
3. **Outreach-Channel Attribution** — which acquisition channel (in-store walk-in vs. community camp vs. app-initiated) produces which conversion rate, by cohort.

---

## 33. AARRR Framework

| Stage | Current state | Gap this proposal targets |
|---|---|---|
| Acquisition | Strong — 13M+ eye tests/year, community outreach | Not targeted directly, but better attribution needed |
| Activation | Prescription generated | **Targeted** — the moment "you need glasses" is delivered is under-designed for the first-time-uncorrected cohort |
| Retention | Repeat-buyer loop well established for existing customers | Not the focus |
| Referral | Not a major public feature for this cohort | Not targeted |
| Revenue | Strong and growing, but its composition (§13.5) needs cleaner disclosure | Indirectly targeted via better cohort transparency |

---

## 34. HEART Framework

| Dimension | Current (first-time-uncorrected cohort) | With First Pair Promise |
|---|---|---|
| Happiness | Unmeasured for this specific cohort | Trust-building content and financing targeted at reducing first-purchase anxiety |
| Engagement | Unmeasured | Tracked from pilot launch |
| Adoption | Unmeasured — folded into aggregate eye-test/purchase numbers | Disclosed as its own cohort metric |
| Retention | Unmeasured | Tracked as repeat-purchase rate within this specific cohort |
| Task success | Purchase completion (aggregate) | Purchase completion **for this cohort specifically** |

---

## 35. Growth Strategy

Lenskart's disclosed growth strategy leans on store expansion (542 net new India stores in FY26), international expansion (Owndays), and continued mass eye-testing. This case study does not argue against any of these — it argues that the company's own valuation premium depends specifically on the *conversion* leg of the eye-testing strategy, which is currently the least measured part of an otherwise well-instrumented growth machine.

---

## 36. Growth Loops

**Existing loop:** Store/outreach eye test → prescription → purchase (aggregate, cohort-blind) → repeat customer → referral/repeat purchase.

**Proposed addition (Construct):** First-time-uncorrected test → dedicated trust-building and financing flow → tracked conversion → if converted, becomes a *repeat*-cohort customer whose behaviour can then be compared against organically-acquired repeat customers, closing the loop on whether the $9.2B TAM bet is actually paying off.

---

## 37. Network Effects

Eyewear retail has essentially no classical network effects. The closest analogue is a **trust/word-of-mouth effect within under-served communities**: a successful first purchase by one member of a rural community, via outreach, plausibly increases uptake by neighbours who saw the outcome — a real but currently unmeasured dynamic that a tracked First Pair Promise cohort could surface.

---

## 38. Product Strategy

| Position | Description | Assessment |
|---|---|---|
| A — Keep scaling aggregate eye-test volume | Current default; store growth + outreach volume | Works for store-count/eye-test headlines, doesn't validate the TAM claim specifically |
| B — Shift entirely to organised-market share battle vs. Titan | Compete on trust/brand in existing organised demand | Concedes the larger TAM claim, likely a smaller long-term prize |
| **C — Instrument and convert the first-time-uncorrected cohort specifically (recommended)** | Build and disclose a dedicated funnel and product for this cohort | Directly tests the assumption the company's own valuation rests on |

---

## 39. Monetization

### 39.1 Current
Eyewear/lens/contact-lens sales, domestic and international (Owndays), at ~70% gross margin.

### 39.2 The tension this proposal is explicit about
A first-time-uncorrected, price-sensitive rural buyer is, per unit, a **lower-margin, higher-acquisition-cost customer** than an urban repeat buyer — financing, trust content, and outreach logistics all cost more per conversion than an app notification to an existing customer. This proposal does not claim First Pair Promise will be immediately margin-accretive; it claims that **knowing the true conversion and cost-to-serve for this cohort** is worth more to the company's credibility with public-market investors than continuing to report only blended, cohort-blind numbers.

### 39.3 First Pair Promise construct
A distinct, branded flow for first-time-uncorrected test-takers: a capped-price "starter pair" (single-vision, basic frame), 0%-interest short-tenure financing, and a guaranteed no-cost refit within 90 days if the prescription needs adjustment — priced to be near-breakeven on the *first* pair, on the explicit bet that a successful, trust-building first purchase converts this cohort into a normal-margin repeat customer over time (same logic as loss-leader acquisition in other categories, but transparently disclosed and separately tracked rather than blended into aggregate numbers).

---

## 40. Trust & Safety

No major public controversy specific to Lenskart's core retail product in this research window. The transparency question in §13.5 (one-time gain disclosure) is a financial-reporting matter, not a product trust-and-safety one, and Lenskart's own Q4 FY26 letter shows the company proactively disclosing and adjusting for it — a point in its favour, noted here rather than treated as a red flag.

---

## 41. Technical Architecture *(Construct — reconstructed from public description)*

```
Eye Test Capture (in-store / outreach device) → Prescription Service
                          ↓
              Purchase Flow (App / In-Store POS)
                          ↓
        Manufacturing & Fulfilment (Bhiwadi / Gurugram)
                          ↓
                 Delivery (next-day / 3-day)
```

First Pair Promise would add a **Cohort Tagging Service** at the Prescription Service layer, flagging "first-time, previously uncorrected" at the moment of test, and carrying that tag through purchase, financing, and post-purchase follow-up — enabling the cohort-specific funnel this proposal is built around.

---

## 42. Data Flow *(Construct)*

`Eye test conducted → prescription generated, cohort-tagged (first-time-uncorrected / repeat / other) → if first-time-uncorrected: routed to First Pair Promise flow → financing offered → purchase or non-purchase logged → 90-day follow-up triggered`

---

## 43. API Ecosystem

No major public developer-facing API programme is a defining part of Lenskart's product surface in this research window.

---

## 44. Privacy & Security

Not independently audited in this analysis. Prescription and vision-health data is sensitive by nature; a cohort-tagging system as proposed in §41 would need to handle it with at least the same care as existing prescription records — a design requirement noted here, not an evaluation of Lenskart's actual practices.

---

## 45. Pain Points

1. **The TAM claim underlying the company's valuation is genuinely contested** by its nearest organised competitor (§13.1), and not yet independently validated by disclosed conversion data.
2. **FY25's headline profit figure was materially inflated by a one-time, non-cash item** — disclosed by the company, but easy to miss in press coverage (§13.5).
3. **No public funnel separates first-time-uncorrected conversion from aggregate eye-test/purchase numbers**, despite this being the specific population the growth story depends on.
4. **Post-lock-in insider selling** (₹8,186 Cr+ in two block deals within a month) is a normal part of the IPO lifecycle but adds to the case for the company to proactively demonstrate the underlying growth thesis rather than rely on story alone.

---

## 46. Opportunity Mapping

Three lines converge: (1) the valuation line (a 200x+ P/E is priced for a specific, unvalidated growth thesis); (2) the disclosure line (the company already discloses eye-test volume and first-time share in aggregate — the infrastructure to disaggregate exists); (3) the competitive line (Titan's explicit public skepticism about Lenskart's TAM claim creates external pressure to demonstrate it, not just assert it).

---

## 47. RICE Prioritisation

| Feature | Reach | Impact | Confidence | Effort | RICE | Stressed RICE* |
|---|---|---|---|---|---|---|
| **First Pair Promise (cohort-tracked conversion product)** | 6 | 8 | 6 | 5 | 57.6 | 34.6 |
| Continue aggregate eye-test volume growth (status quo) | 9 | 5 | 8 | 3 | 120 | 72 |
| International expansion acceleration (Owndays+) | 5 | 6 | 6 | 7 | 25.7 | 15.4 |
| Financing/EMI expansion for all buyers (not cohort-specific) | 7 | 5 | 7 | 5 | 49 | 29.4 |

*Stress rule (Construct, consistent with the series' methodology): reach × 0.6, confidence − 20pp.

Status-quo aggregate growth wins on stressed RICE, unsurprisingly — it's cheap, proven, and already scaling. First Pair Promise is recommended on strategic grounds (§46): it is the one investment that actually tests the assumption embedded in the company's valuation, which no amount of more aggregate growth can do on its own.

---

## 48. MoSCoW

| Must | Should | Could | Won't (v1) |
|---|---|---|---|
| Cohort tagging at point of prescription | 0%-interest starter financing | Community-specific trust content (local language, testimonials) | Full separate brand/sub-app (v1 = flow within existing app/store) |
| 90-day no-cost refit guarantee | Outreach-channel attribution dashboard (internal) | Referral incentive within converted cohort | Pricing changes to the core (non-first-time) product line |

---

## 49. Kano Analysis

| Feature | Category |
|---|---|
| Eye test itself | Basic (expected) |
| 3D try-on | Performance |
| **Disclosed first-time-cohort conversion metric** | **Attractive to investors specifically** — not a consumer-facing Kano feature in the traditional sense, but a credibility feature for the market Lenskart is now accountable to |
| Starter-pair financing | Attractive to the first-time-uncorrected cohort, likely to become expected within that segment over time |

---

## 50. Feature Proposal — First Pair Promise

**What it is:** a distinct, cohort-tagged flow for first-time, previously-uncorrected eye-test takers — capped-price starter pair, short-tenure 0%-interest financing, guaranteed no-cost refit — paired with public disclosure of this cohort's conversion rate and repeat-purchase behaviour over time.

**Why now:** the company's own valuation depends on a claim (943M uncorrected, $9.2B TAM) that is currently unvalidated by any public metric, and a well-resourced competitor is actively contesting it. Demonstrating movement on this specific number is worth more to the company's credibility than any amount of additional aggregate growth.

**What it is not:** a claim that the current business is weak (operating cash flow says otherwise) or a criticism of the one-time-gain disclosure (which the company handled transparently). It is a proposal to close the one measurement gap that sits directly underneath the valuation thesis.

**User impact:** first-time, previously-uncorrected buyers — often in Tier-2/3/rural settings — get a purpose-built, lower-risk entry point into a purchase category they may have never considered before.

**Business impact:** near-term margin drag on this specific cohort (starter pricing, financing cost); long-term, either validates the TAM thesis (supporting the valuation) or reveals it needs revising (better for investors to know now than later).

**Trade-offs:** cost to build cohort-tracking infrastructure; risk that disclosed numbers, if conversion is weak, could pressure the stock in the near term — which is precisely the accountability this case study argues the current 200x+ multiple already implicitly demands.

---

## 51. PRD — First Pair Promise v1

### 51.1 Problem
The specific population Lenskart's valuation depends on converting is not separately tracked, making the company's core growth thesis unfalsifiable in its current public disclosure.

### 51.2 Goals
- Pilot cohort-tagging and the dedicated flow across a defined set of outreach programmes (e.g., a subset of Drishti camps) in 2–3 states.
- Establish a baseline Verified First-Correction Rate within 2 quarters.
- Disclose the metric (in some form) in a subsequent shareholder communication, demonstrating the company can and will measure this.

### 51.3 Non-goals (v1)
Not changing pricing for the existing, already-converting customer base; not a full rebrand of the outreach programme; not a claim of a specific target conversion rate before baseline data exists.

### 51.4 User stories
- As a first-time test-taker told I need correction, I'm offered a clear, affordable, low-risk starter pair with financing.
- As Lenskart, I can see, cohort by cohort, how many first-time-uncorrected test-takers actually convert, and how long it takes.
- As an investor, I can see a disclosed metric that speaks directly to the company's TAM claim, rather than only aggregate revenue and store-count growth.

### 51.5 Acceptance criteria (Constructs — author-set bars)
- A1: Cohort tagging correctly applied to ≥95% of eligible first-time tests in pilot regions.
- A2: Baseline VFCR established with a sample large enough to be statistically meaningful (exact threshold set after Phase 0, §53).
- A3: No degradation in existing repeat-buyer experience from the added flow.

---

## 52. Wireframes *(ASCII, Constructs)*

```
┌───────────────────────────────────┐
│  Your eye test result               │
│                                     │
│  This is your first time needing    │
│  correction. Here's how to start:   │
│                                     │
│  Starter Pair — ₹999                │
│  0% financing available             │
│  Free refit within 90 days          │
│                                     │
│  [   See my starter options   ]     │
└───────────────────────────────────┘
```

---

## 53. Rollout Plan

| Phase | Scope | Gate |
|---|---|---|
| Phase 0 | Baseline: what share of current first-time-uncorrected test-takers already convert, unmeasured, across a sample of existing outreach camps? | If baseline conversion is already high, the "unmeasured gap" framing weakens and the proposal should re-scope around disclosure alone, not a new flow |
| Phase 1 | Launch tagged flow + starter pricing in 2–3 states | §51.5 acceptance criteria |
| Phase 2 | Expand regions; begin disclosing aggregated (anonymised) cohort metrics externally | Baseline VFCR holds or improves |
| Phase 3 | National rollout across all outreach channels | Net margin impact of the cohort assessed before claiming it as a growth pillar publicly |

---

## 54. A/B Testing

**Arm A (control):** existing undifferentiated flow. **Arm B:** First Pair Promise (starter pricing + financing + refit guarantee). **Arm C (falsifier, Construct):** offer the *same* financing and refit guarantee without the "starter" price cap (i.e., full-price product, just with better terms) — designed to test whether price or trust/terms is the actual barrier for this cohort. If Arm C converts comparably to Arm B, the constraint isn't price at all, and the proposal should re-scope around trust-building rather than subsidised pricing.

---

## 55. KPI Dashboard *(Construct)*

| KPI | Target |
|---|---|
| Verified First-Correction Rate (pilot regions) | Baseline established, then directional improvement |
| Cohort tagging accuracy | ≥95% |
| Time-to-first-purchase (this cohort) | Directional reduction vs. baseline |
| Repeat-purchase rate within converted cohort (12-month) | Tracked, compared to organic repeat-buyer baseline |

---

## 56. Product Roadmap

`Q1: Phase 0 baseline → Q2: Phase 1 pilot (2–3 states) → Q3: Phase 2 (expand + begin external disclosure) → Q4: Phase 3 decision gate ahead of the following annual investor communication cycle`

---

## 57. Risks & Mitigation

| # | Risk | Mitigation |
|---|---|---|
| R1 | Disclosed conversion numbers turn out weak, pressuring an already richly-valued stock | Frame disclosure as proactive credibility-building; better to surface early than have a competitor or short-seller do it first |
| R2 | Starter pricing cannibalises would-be full-price purchases from buyers who'd have converted anyway | Restrict eligibility strictly to verified first-time-uncorrected status via the cohort tag |
| R3 | Price isn't the real barrier (tested by Arm C, §54) | Re-scope toward trust/terms if Arm C outperforms |
| R4 | Financing default risk in a lower-income cohort | Cap exposure per pilot phase; monitor default rates as an explicit gating metric alongside conversion |

---

## 58. Future Vision

If First Pair Promise validates the conversion thesis, its natural extension is using the disclosed VFCR metric as a standing part of Lenskart's investor communication — turning "we believe the TAM is $9.2B" into "here is the rate at which we are actually converting it," which is a stronger claim to sustain a premium multiple than aggregate growth alone.

---

## 59. PM Lessons

The lesson this case study keeps returning to: a company can be completely honest in its disclosures (as Lenskart's own flagging of the one-time gain shows) and still leave the single most important number implicit in its growth story unmeasured — not through concealment, but because aggregate metrics are easier to report and, until challenged, nobody asks for the cohort that would prove or disprove the thesis.

---

## 60. PM Interview Questions

1. A company's valuation rests on a TAM claim its nearest competitor publicly disputes. How would you design a metric that could settle the argument with data rather than rhetoric?
2. You discover that half of a headline profit number came from a one-time non-cash item. How do you decide whether and how to communicate that internally versus externally?
3. Design an experiment to determine whether price or trust is the bigger barrier to a first-time purchase in a low-familiarity category.

---

## 61. References

- Lenskart FY25/FY26 results and IPO coverage: Finnovate, BW Marketing World, Swastika Investmart, EarnYatra, Zerodha, Kotak Neo, Business Standard (2025–2026)
- Lenskart Q4 FY26 Shareholders' Letter (official company disclosure, May 2026) — source for the one-time FVTPL gain disclosure
- Lenskart post-listing stock performance: Univest, MarketsMojo, TickerTape, Kotak Neo (2026)
- Lenskart vs. Titan Eye+ TAM dispute: TechStory, Markhub24 (Nov 2025–Jul 2026)
- India eyewear market sizing: Ken Research, Custom Market Insights, Maximize Market Research (2025–2026)
- Titan Eye+ strategy and financials: Equentis, Research and Ranking, Chai and Charts (2025–2026)
- Lenskart screener/financial data: Screener.in (accessed August 2026)

---

## 62. About the Author

Written by Gaurav Singh as part of a 90-day product management case study series, applying a consistent research-led teardown methodology across Indian and global consumer products.

---

## 63. License

This document is an independent analysis for educational purposes. It is not affiliated with, endorsed by, or reviewed by Lenskart Solutions Ltd. All company names and trademarks belong to their respective owners.

---

## 64. Self Review

| Check | Status | Note |
|---|---|---|
| No fabricated data | ✅ | Every figure sourced or explicitly derived; constructed content in Appendix C |
| Facts separated from assumptions | ✅ | ASSUMPTIONS.md |
| Conflicts disclosed | ✅ | Appendix A |
| Falsification designed | ✅ | §53 Phase 0, §54 Arm C |
| Recommendation shown against a prioritisation framework rather than engineered to win | ✅ | §47 — First Pair Promise does not top stressed RICE |

**Where this case study is weakest.** The 943-million-uncorrected figure and the $9.2B TAM are both drawn from Lenskart's own DRHP-cited RedSeer research — the company that benefits most from a larger TAM is also the source of the estimate, which this document flags but cannot independently verify. Second, the FY26 profit figures show minor inconsistencies across sources (₹493.6 Cr vs ₹500.95 Cr vs ~₹501 Cr) likely reflecting different reporting cuts or rounding, not resolved here. Third, this analysis cannot rule out that Lenskart already tracks the cohort-specific conversion metric proposed in §50 internally and simply hasn't disclosed it publicly — in which case the proposal's real contribution is the disclosure, not the underlying measurement capability.

**What would change my mind.** Lenskart publicly disclosing a first-time-uncorrected conversion metric showing strong, TAM-validating conversion; a Phase 0 baseline (§53) finding conversion is already high and the "unmeasured gap" framing overstated; or Arm C (§54) showing price was never the real barrier, in which case a much simpler trust-focused intervention would suffice.

---

## 65. Appendix

### Appendix A — Source Conflicts

| # | Conflict | Resolution |
|---|---|---|
| A-1 | India eyewear TAM: $3.4B (Titan Eye+) vs $9.2B (Lenskart/RedSeer) vs $6.6B (Custom Market Insights, 2024) | Carried as a genuine, unresolved dispute throughout — this is the case study's central subject, not a footnote |
| A-2 | FY26 net profit: ₹493.61 Cr vs ₹500.95 Cr vs "~₹501 Cr" across different source cuts (TickerTape vs Zeebiz vs Screener) | Likely different reporting bases (standalone vs consolidated, or rounding); both/all cited, direction (≈68% unadjusted / ≈148% adjusted growth) unaffected |
| A-3 | Revenue growth rate trajectory is non-monotonic: 46% (FY23), 43% (FY24), 22.6% (FY25), 32.5% (FY26) — a deceleration followed by re-acceleration | Noted as a genuine pattern worth watching, not smoothed over; consistent with new-store ramp-up cycles but not confirmed as the cause here |

### Appendix B — Evidence Grades

| Grade | Meaning | Applied to |
|---|---|---|
| 🟢 High | Company shareholder letter / exchange filing | FY25/FY26 revenue, profit, the one-time FVTPL gain disclosure, operating cash flow |
| 🟡 Medium | Trade press citing filings, consistent across sources | Store counts, eye-test volumes, block-deal figures |
| 🟠 Low | Company-commissioned third-party market research (RedSeer) | The $9.2B TAM and 943M-uncorrected figures |
| 🔴 Conflicting | Sources materially disagree | TAM estimates (Titan vs Lenskart vs independent), FY26 profit figure precision |

### Appendix C — Author-Constructed Content

| # | Construct | Where |
|---|---|---|
| C1 | First Pair Promise — the entire proposal | §50 |
| C2 | Verified First-Correction Rate (North Star) | §31 |
| C3 | First-Time Tester Conversion Funnel, Time-to-First-Purchase, Outreach-Channel Attribution | §32 |
| C4 | Personas Ritika, Manoj, Aarav | §20 |
| C5 | All RICE inputs and the stress rule | §47 |
| C6 | Acceptance-criteria bars | §51.5 |
| C7 | The three-arm A/B design including Arm C as falsifier | §54 |
| C8 | Technical architecture and data-flow reconstructions | §41, §42 |
| C9 | The reading of the TAM dispute as the central strategic question, and the "valuation is a bet on a growth theory" framing | §13.3, §46 |

### Appendix D — Asset Status

| Asset | Status |
|---|---|
| ASCII wireframes | ✅ Authored (§52) |
| Product screenshots | ❌ Not included — no authenticated session was used |
| UI/accessibility audit | ❌ Not independently tested — flagged as a research-boundary gap |

---

*Day 52 of 90 · ← [Day 51 — Ola](../Day-51-Ola) · Day 53 →*
