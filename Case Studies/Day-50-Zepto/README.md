# Zepto — Profitable Stores, Unprofitable Company

### Day 50 of 90 · Product Management Case Study Series

> **The thesis of this case study:** Zepto's own IPO paperwork tells a story that doesn't fit on one line. At the store level, the model works — Bernstein estimates roughly 3,600 of the top 3,800 dark stores across India's largest eight cities are individually profitable, and breakeven time per new store has fallen from about two years to about six months. At the company level, the model is losing more money every year it grows: a net loss of ₹1,214–1,249 Cr in FY24 widened to ₹3,367 Cr in FY25 and ₹5,905 Cr in FY26, even as revenue more than doubled twice in a row. Both things are true at once, which means the loss isn't really a *unit-economics* problem anymore — it's a **demand-variance and expansion-mix** problem. Zepto is spending its IPO proceeds overwhelmingly on horizontal growth (≈1,900 new dark stores, new categories, new cities) rather than on deepening utilisation of the stores that already work. Meanwhile its one live attempt at a retention lever — Zepto Pass, launched wide in 2024, quietly discontinued, and relaunched in 2026 as an invite-only, cashback-based Zepto Club — is still a rounding error next to the horizontal bet. This case study proposes **Zepto Steady**, a commitment-based subscription that trades a modest discount for a predictable weekly order, aimed not at acquiring new users but at converting existing profitable-store demand into *low-variance* demand — the one lever that improves rider utilisation, spoilage, and staffing cost without opening a single new dark store.

---

## 2. Repository Metadata

| Field | Value |
|---|---|
| **Case study** | Day 50 of 90 |
| **Product** | Zepto — quick commerce (10–15 minute grocery, FMCG, and adjacent-category delivery) |
| **Company** | Zepto (Zepto Marketplace Private Limited / Zepto Limited), Mumbai |
| **Domain** | Quick commerce / hyperlocal retail |
| **Primary competitors** | Blinkit (Eternal), Swiggy Instamart, BigBasket BB Now (Tata), Flipkart Minutes, Amazon Now |
| **Analysis type** | Research-led product teardown + financial reconstruction + a feature proposal |
| **Proposed system** | **Zepto Steady** — a demand-commitment subscription for existing profitable-store capacity |
| **Author** | Gaurav Singh |
| **Date of analysis** | 17 August 2026 |
| **Research boundary** | Public sources only — DRHP/UDRHP filings, trade press, and third-party market trackers. No Zepto employee, internal document, or authenticated session was consulted. |
| **Latest financials available** | FY26 figures as disclosed in Zepto's Updated DRHP (filed June 2026), for the year ended 31 March 2026 |

---

## 3. Badges

![Case Study](https://img.shields.io/badge/Case%20Study-Day%2050%20of%2090-blue)
![Domain](https://img.shields.io/badge/Domain-Quick%20Commerce-orange)
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

Zepto is a five-year-old Mumbai quick-commerce company, founded in 2021 by Aadit Palicha and Kaivalya Vohra (both Stanford dropouts, both around 19 at founding) after pivoting an earlier venture, KiranaKart, into a 10-minute delivery promise. As of 31 March 2026 it operates **1,139 dark stores across 66 cities**, handles roughly **2.33 million orders a day**, and counts close to **48 million annual transacting users**.

Its financial trajectory is the story of a company that keeps solving the problem in front of it while a bigger one grows behind it. Revenue (reported as total sales, including other income) went from ₹4,454 Cr (FY24) to ₹9,669–11,110 Cr (FY25, sources vary — see Appendix A) to ₹22,624 Cr (FY26): roughly 130–150% growth in each of the last two years. Net loss went from ₹1,215–1,249 Cr (FY24) to ₹3,367 Cr (FY25) to ₹5,905 Cr (FY26): widening every year, even as loss *as a share of revenue* actually improved slightly in FY26 (≈26%) versus FY25 (≈35%). Both trends are real. Zepto is getting more efficient per rupee of revenue and burning more absolute cash, at the same time, because the denominator (dark stores, cities, categories) keeps growing faster than the efficiency gain.

The part of this that is easy to miss in the topline numbers: **the existing store base mostly works.** Bernstein's store-level analysis puts roughly 3,600 of the top 3,800 stores across India's eight largest cities in profit, and the time for a new store to break even has compressed from about two years to about six months as the network has densified (§13, §45). If most of the *installed* capacity is profitable, the marginal loss is coming from somewhere else: new-store ramp-up, tier-2/tier-3 expansion, new-category investment (pharmacy, electronics, fashion), and — this case study's focus — **demand variance inside stores that are already profitable on average but not profitable in every hour.**

Zepto has one live product built to address exactly this kind of problem, and it has already failed once. Zepto Pass launched in February 2024 as a low-price (₹19–39/month), universally available membership offering free delivery and discounts. It was discontinued at some point in 2024–25. In its place, Zepto relaunched a membership programme in mid-2026 — **Zepto Club** — that is invite-only, priced at ₹99/month, and built around 5% cashback in "Z-Coins" rather than just delivery-fee removal (§39, §45). The shift from *open, cheap, delivery-fee-based* to *invite-only, pricier, cashback-based* is a shift from an acquisition tool to a retention tool — and it is small. Meanwhile, ₹1,629 Cr of the IPO's ₹8,010 Cr fresh issue is earmarked for roughly 1,900 *new* dark stores (§13.6, §53) — a horizontal bet roughly double the size of the entire existing network, while the company's only demand-shaping product remains invite-only.

This case study's finding: **Zepto is trying to fix a variance problem with a footprint solution.** New stores add new average-profitable capacity: they do not, on their own, smooth the peaks and troughs inside stores that already exist. The proposal in §50 — **Zepto Steady** — is a commitment-based subscription that pre-books a fixed weekly delivery slot and a flexible basket range in exchange for a modest discount, designed to convert unpredictable order flow into scheduled, forecastable demand inside the stores Zepto already has. It is not a replacement for the IPO growth plan. It is the cheaper lever that should be pulled first, and — per the Assumptions file — it is falsifiable in a single-city pilot before a rupee of it touches national rollout.

---

## 6. Product Overview

Zepto is a mobile-first quick-commerce app operating an **inventory-led, verticalised dark-store model**: unlike early hyperlocal players that partnered with existing kirana stores, Zepto owns or leases its own micro-warehouses (dark stores), holding 3,000–5,000 SKUs each, stocked and staffed to fulfil orders within 10–15 minutes of an app order. The core surface is a single-category-first home feed (groceries, fresh produce, FMCG) that has expanded into adjacent verticals:

- **Zepto Café** — a snacks/beverages sub-vertical positioned against Blinkit's Bistro and Swiggy's Instamart food add-ons, delivering prepared or semi-prepared food and drinks on the same 10–15 minute promise.
- **Pharmacy** — 10-minute medicine delivery, a higher-margin, higher-trust adjacency.
- **Zepto Club** — the current (2026) invite-only loyalty layer.
- Planned/DRHP-disclosed expansion into **electronics and apparel/fashion**, funded from IPO proceeds.

The backend supply chain is described in DRHP disclosures as processing an average of **~4.0 million units per day** (Q4 FY26) through automated, forecasting-assisted inventory systems.

---

## 7. Company Background

Founded in 2021 in Mumbai by Aadit Palicha and Kaivalya Vohra. The company began as **KiranaKart**, an asset-light model connecting users to local kirana stores, before pivoting mid-2021 into the verticalised, owned-dark-store model that became Zepto — a strategic reversal comparable in kind (if not in domain) to a founder team abandoning a marketplace model for an inventory model once they concluded speed and control, not asset-light scale, was the winning axis.

Zepto scaled through repeated large private rounds: from a reported $3.6B valuation round in mid-2024 (Avenir, Lightspeed, Avra and existing investors) to a $5B valuation round later in 2024, to a further pre-IPO round reported at either **$5B** (Motilal Oswal / Raamdeo Agrawal-backed tranche) or **$7B** (a CalPERS/General Catalyst-led October 2025 tranche) depending on source — flagged as a conflict in Appendix A. Board changes in December 2025 made founders Palicha and Vohra, along with CFO Ramesh Bafna, whole-time directors ahead of the IPO process.

The company confidentially filed its DRHP with SEBI on 26–27 December 2025, received a SEBI observation letter in May 2026, filed an Updated DRHP on 8–9 June 2026 seeking a fresh issue of ₹8,010 Cr plus an OFS of ~11.35 crore shares, then **paused its IPO** in late July 2026 amid a valuation gap — institutional investors reportedly pricing the company closer to $2.5–4.5B pre-money against Zepto's own $7B private mark — and instead raised roughly ₹1,000 Cr in a smaller, domestic-investor-heavy pre-IPO round.

---

## 8. Product Timeline

| Year | Milestone |
|---|---|
| 2021 | Founded as KiranaKart; pivots mid-year to owned dark-store model, rebrands Zepto |
| 2021–23 | Rapid metro dark-store rollout; store breakeven time initially ~2 years |
| 2024 | Crosses unicorn status repeatedly in successive rounds ($3.6B → $5B); Zepto Pass launched (Feb) |
| 2024 (Dec) | FY24 audited results reported: revenue ₹4,454 Cr, net loss ₹1,214.7–1,248.6 Cr |
| 2025 | Zepto Pass discontinued; Café and pharmacy verticals scale; further pre-IPO rounds ($5–7B valuation, sources vary) |
| 2025 (Dec) | Confidential DRHP filed with SEBI; FY25 audited results reported: revenue ₹9,669–11,110 Cr, net loss ₹3,367.3 Cr |
| 2026 (May) | SEBI observation letter received |
| 2026 (Jun) | Updated DRHP filed: ₹8,010 Cr fresh issue + OFS; 1,139 dark stores, 66 cities disclosed; Zepto Club (invite-only) launched |
| 2026 (Jul) | IPO paused; ~₹1,000 Cr domestic pre-IPO round raised at ~$4.5B |

---

## 9. Vision & Mission

Zepto has not published a formal mission statement in the way some peers have; its public communication consistently centres on **delivery speed as the core promise** — the 10-minute (now often 10–15 minute) grocery delivery standard it is widely credited with popularising in India. The implied mission, read from product behaviour rather than a stated line: *make near-instant delivery of everyday essentials the default way urban India shops*, expanding category-by-category (groceries → snacks → pharmacy → electronics/fashion) once density makes each new category deliverable within the same time promise.

---

## 10. Problem Statement

**For the company:** Zepto has proven it can grow revenue at 130%+ annually and that individual dark stores, once dense enough, are profitable. It has not proven it can grow *without* the loss also growing — every year of scale has come with a larger absolute loss, and the IPO's own fund-use plan continues to bet primarily on more stores rather than better utilisation of existing ones.

**For the user:** the quick-commerce value proposition (speed, breadth, low friction) is easy to obtain for a single order and hard to sustain as a habit at low churn cost — nothing currently rewards a user for making their demand *predictable*, only for making it *frequent* or *large* (via cashback thresholds).

---

## 11. Market Research

India's quick-commerce sector reached an estimated **$11.5B (~₹95,500 Cr) GOV by end of 2025**, growing over 75% YoY per Reuters/Datum Intelligence — a figure that sits in sharp tension with at least one industry-report estimate of a $3.65B 2026 market growing to $6.64B by 2031 (Mordor Intelligence), most likely reflecting a narrower revenue/GMV definition rather than a genuine disagreement about market direction (flagged in Appendix A). Order volume across the sector reached roughly 7.8 million orders/day in January 2026 (Redseer), with 40–45% projected annual growth. More than **6,000 dark stores** now operate nationally (Bernstein), concentrated overwhelmingly in the top eight metros.

---

## 12. Industry Analysis

Three players — Blinkit, Swiggy Instamart, and Zepto — account for roughly 85–90%+ of the category, with Blinkit the clear leader (~46–50% share), and Instamart and Zepto contesting a close second (~20–25% each, estimates blend GMV and order-volume trackers so treat as directional). Amazon Now and Flipkart Minutes have each scaled past 500 dark stores and are squeezing pure-play challengers from the well-capitalised-generalist side; BigBasket's BB Now holds a smaller 5–7% slice on Tata Group sourcing strength. Blinkit is the only major player to have publicly claimed cluster-level EBITDA positivity.

---

## 13. TAM / SAM / SOM

### 13.1 TAM
India quick-commerce GOV, end-2025: **~$11.5B (₹95,500 Cr)**, per Reuters/Datum Intelligence — used here in preference to the narrower Mordor Intelligence figure (Appendix A-1).

### 13.2 SAM
Zepto's addressable share, given its current concentration in the top eight-to-fifteen metro markets and current category mix (grocery, FMCG, Café, pharmacy): reasonably bounded by its own 20–25% reported share of the current market, i.e. **roughly ₹19,000–24,000 Cr of current-category GOV**.

### 13.3 SOM — revenue reported
| Year | Revenue (total sales, incl. other income) | Net loss | Loss as % of revenue |
|---|---|---|---|
| FY24 | ₹4,454 Cr | ₹1,214.7–1,248.6 Cr | ≈28% |
| FY25 | ₹9,668.8–11,110 Cr | ₹3,367.3 Cr | ≈31–35% |
| FY26 | ₹22,623.6 Cr | ₹5,905.2 Cr | ≈26% |

*Two independent figures exist for FY25 revenue (₹9,668.8 Cr per audited-filing coverage in December 2025/April 2026 reporting; ₹11,110 Cr per a July 2025 report citing regulatory filings). This document uses ₹9,668.8 Cr for FY25→FY26 growth arithmetic since both are drawn from filings coverage closest to the FY26 DRHP disclosure, and flags the discrepancy in Appendix A.*

### 13.4 Operational revenue estimate
Quick-commerce accounting convention recognises only 15–20% of GMV as operational revenue (commissions, delivery fees, ad income). Applied to FY25 total sales, analysts estimate **operational revenue of ₹1,495–1,994 Cr** — materially smaller than the "total sales" headline (D7, ASSUMPTIONS.md).

### 13.5 Store-level derivation
2.33M orders/day ÷ 1,139 dark stores ≈ **2,046 orders per store per day** (D12) — an average that, per Bernstein's store-profitability split, conceals wide variance: most top-metro stores clear this comfortably; a meaningful minority (especially tier-2) do not.

### 13.6 IPO capital allocation, as disclosed
| Use | Amount | Share of fresh issue |
|---|---|---|
| New dark stores (~1,900 stores) | ₹1,629 Cr | ~20% |
| Dark-store lease payments through FY30 | ₹1,735 Cr | ~22% |
| Technology & cloud infrastructure | ₹1,325 Cr | ~17% |
| Marketing & promotion | ₹520 Cr | ~6% |
| Inorganic growth / general corporate | Remainder | ~35% |

**Reading:** roughly 42% of the fresh issue (new stores + their leases) is committed to *horizontal* expansion before a rupee is spent on demand-shaping products for the existing 1,139-store base. This is the empirical anchor for this case study's thesis (A1, ASSUMPTIONS.md).

---

## 14. Competitor Analysis

| Dimension | Blinkit (Eternal) | Swiggy Instamart | **Zepto** | BB Now (Tata) |
|---|---|---|---|---|
| Market share (blended est.) | ~46–50% | ~20–25% | ~20–25% | ~5–7% |
| Profitability claim | Cluster-level EBITDA-positive | Adjusted EBITDA loss widening (~₹840 Cr, Q4 FY25) | Net loss widening every year | Not disclosed |
| Loyalty layer | Zomato Gold *not* extended to Blinkit | Swiggy One Blck (cross-product) | Zepto Club (invite-only, 2026) | None public |
| Category breadth | Groceries, alcohol (select cities), Bistro (food) | Groceries, Instamart snacks | Groceries, Café, pharmacy, planned electronics/fashion | Groceries, Tata-sourced FMCG |
| Listing status | Listed (via Eternal) | Listed (via Swiggy) | IPO paused, mid-2026 | Unlisted |

Blinkit's advantage is largely structural: it inherited Zomato's logistics, ad-sales relationships, and — critically — its willingness to publicly claim profitability first, which matters for investor sentiment even where the underlying unit economics across players are closer than the loss headlines suggest (loss accounting is not apples-to-apples across net loss vs adjusted EBITDA loss reporting — Appendix A-2).

---

## 15. SWOT

| Strengths | Weaknesses |
|---|---|
| Fastest order-volume CAGR among scaled players (~119.5% FY24–26, Redseer via DRHP) | Net loss widening in absolute terms every year |
| Store-level profitability largely proven in top metros | Only 20–25% share vs Blinkit's ~50% |
| Highly automated, dense supply chain (~4M units/day) | Loyalty/retention product history is inconsistent (Pass launched, killed, relaunched narrower) |
| Strong founder-led brand recognition | IPO credibility dented by the July 2026 pause and valuation gap |

| Opportunities | Threats |
|---|---|
| Demand-smoothing products largely unexplored by any player | Amazon Now, Flipkart Minutes scaling with deep pockets |
| Pharmacy/electronics as higher-margin adjacencies | FEMA-related regulatory matter disclosed in DRHP |
| IPO capital, once raised, funds real densification | Investor patience for widening losses may not survive a public listing |

---

## 16. Porter's Five Forces

| Force | Intensity | Note |
|---|---|---|
| Competitive rivalry | Very high | Three players near-equally matched on capital access; rivalry is on speed and assortment, not price alone |
| Threat of new entrants | Medium-high | Amazon Now, Flipkart Minutes entered late but at scale; barrier is capital + dark-store density, not technology |
| Bargaining power of suppliers (FMCG brands) | Medium | Brands increasingly extract ad/placement spend from all three platforms |
| Bargaining power of buyers (consumers) | High | Near-zero switching cost between apps for a single order |
| Threat of substitutes | Medium | Traditional e-commerce (slower, cheaper) and physical retail remain viable for planned, non-urgent purchases |

---

## 17. Business Model Canvas

| Block | Summary |
|---|---|
| Key Partners | FMCG brands (Coca-Cola, Colgate, Nivea, Cello, per DRHP), farmer-partner network for fresh produce, delivery-fleet partners |
| Key Activities | Dark-store operations, inventory forecasting, last-mile delivery, category expansion |
| Value Propositions | 10–15 minute delivery; broad assortment; growing category breadth (Café, pharmacy) |
| Customer Relationships | App-native, largely self-serve; nascent invite-only loyalty (Zepto Club) |
| Customer Segments | Urban, time-constrained households and individuals; skews metro, skews higher AOV categories over time |
| Channels | Mobile app (primary), performance marketing, in-app advertising as a secondary monetisation layer |
| Key Resources | Dark-store real estate, automated supply chain, brand recognition, capital |
| Cost Structure | Delivery/fulfilment cost, dark-store lease and staffing, marketing, technology |
| Revenue Streams | Commission on goods sold, delivery fees, advertising/placement revenue, (nascent) subscription |

---

## 18. Revenue Model

Zepto's revenue is a blend of (1) margin on goods sold through its own inventory, (2) delivery fees, and (3) advertising/placement fees from brands seeking shelf visibility inside the app — the same three-line structure common across inventory-led quick commerce. The gap between "total sales" (₹22,624 Cr FY26, which likely approximates GMV-adjacent recognition) and the analyst-estimated **operational revenue** band (15–20% of GMV) is the single most important number to hold onto when reading any Zepto headline: the company that says it did ₹22,624 Cr in FY26 recognised something closer to ₹3,400–4,500 Cr of that as revenue under the 15–20% convention applied consistently (D7 extended to FY26, ASSUMPTIONS.md) — though the DRHP's own revenue line, if reported net of order value per standard accounting, may already reflect this; this document treats the distinction as a live source-interpretation caution rather than a resolved fact (Appendix A-3).

---

## 19. Target Users

- **Urban, dual-income households** ordering groceries/essentials multiple times a week, price-tolerant for speed.
- **Students and young professionals** (hostel/PG, shared flats) ordering smaller, more frequent baskets, skewing Café and snacks.
- **Occasional top-up shoppers** using Zepto to fill gaps between larger weekly/monthly shops elsewhere (a segment this case study argues is the most demand-*volatile*, and the best fit for a commitment subscription).

---

## 20. Personas

**Persona — Aditi, 29, Bengaluru, product manager (Construct — not a Zepto member profile)**
Orders 4–5 times a week: dinner ingredients on weeknights, a bigger weekend top-up. Values speed over price. Already the kind of user Zepto Club (₹99/month, invite-only) is built for — but her demand is *frequent*, not *predictable*: she orders on impulse, at inconsistent times, which is exactly the pattern that makes her valuable to Zepto in aggregate and hard to staff for at the store level.

**Persona — Karan, 22, Pune, engineering student sharing a flat (Construct)**
Orders Café items and snacks late evening, irregularly, price-sensitive, uses whichever app has the best current offer. Low loyalty, low predictability, high switching.

**Persona — Meenal, 41, Delhi, working mother of two (Construct)**
Orders a genuinely repeatable weekly basket — milk, bread, staples, fruit — on a near-fixed day and time, topped up with impulse orders in between. She is the clearest candidate for a commitment subscription: her *baseline* demand is already predictable; Zepto currently captures none of that predictability as a product feature.

---

## 21. Jobs to Be Done

- "When I run out of something mid-week, help me get it in minutes, not hours." (speed job — served today)
- "When I know I'll need groceries every Sunday, let me lock that in so I don't have to think about it or pay full price for something I was always going to buy." (commitment job — **not** currently served by any major quick-commerce player)
- "When I'm loyal, let me feel and see the benefit beyond a generic discount." (status/reward job — partially served by Zepto Club)

---

## 22. User Journey

`Discover app → first order (speed-tested) → repeat impulse orders → (maybe) invited to Zepto Club → cashback accrues → redeemed on future orders → habit continues or lapses`

The journey has no branch for a user who *wants* to pre-commit to a schedule. Every touchpoint optimises for "order now," never for "order every week, on this day, without me opening the app."

---

## 23. User Flow (current)

`Open app → browse/search → add to cart → checkout → (if Club member) apply cashback → pay → track 10-min delivery → repeat`

**Node gap (Construct):** there is no flow branch for "set a standing order" or "commit to a weekly slot" — the entire flow assumes each order is a fresh, independent decision.

---

## 24. Information Architecture

`Home → Categories (Grocery / Café / Pharmacy / [planned: Electronics, Fashion]) → Search / Cart / Orders / Zepto Club → Profile`

**Dangling node (Construct):** "Zepto Club" sits as a destination inside Profile/Home, not as a scheduling or commitment surface — it rewards past behaviour, it does not shape future behaviour.

---

## 25. UX Audit

| Area | Observation |
|---|---|
| Checkout speed | Fast, minimal friction — a genuine strength consistent across the category |
| Delivery-time transparency | Live ETA is prominent and well-trusted by users, per general category sentiment |
| Loyalty visibility | Zepto Club is invite-gated, so most users never see it — a retention lever with almost no top-of-funnel visibility |
| Scheduling | Absent — no "order for later" or "recurring order" surface exists in the flow as publicly described |

---

## 26. UI Audit

Not independently screenshot-audited in this document (Appendix D) — reproducing an authenticated commerce app's UI would require an account and is out of scope for a public-sources-only analysis. Structure is described from public product coverage and app-store material instead.

---

## 27. Accessibility

Not independently tested in this analysis; flagged as an area no public source in this research covered in adequate depth to report on responsibly.

---

## 28. Feature Breakdown

| Feature | Persists after a single order? | Notes |
|---|---|---|
| 10–15 min delivery | N/A — is the core transaction | Category-standard |
| Zepto Café | Yes, ongoing vertical | Competes with Blinkit Bistro |
| Pharmacy | Yes, ongoing vertical | Higher-trust, higher-margin adjacency |
| Zepto Club | Yes, but invite-gated | Cashback (Z-Coins), free delivery, priority support |
| Standing/recurring orders | **Does not exist** | The gap this case study's proposal fills |

---

## 29. AI Capabilities

Public disclosures describe automated inventory forecasting and manpower-productivity tooling inside the supply chain (per DRHP language), consistent with category-standard demand-forecasting ML used to position stock ahead of predicted order patterns. No customer-facing conversational AI feature is a defining part of the public product surface, unlike some adjacent categories (e.g., health-app AI coaches).

---

## 30. Product Metrics

| Metric | FY24 | FY25 | FY26 |
|---|---|---|---|
| Revenue (total sales) | ₹4,454 Cr | ₹9,668.8–11,110 Cr | ₹22,623.6 Cr |
| Net loss | ₹1,214.7–1,248.6 Cr | ₹3,367.3 Cr | ₹5,905.2 Cr |
| Dark stores | — | ~900+ | 1,139 |
| Cities | — | — | 66 |
| Daily orders | — | — | 2.33M |
| Annual transacting users | — | — | ~48M |
| Cash balance (year-end) | ₹1,688 Cr | ₹7,441 Cr | ₹5,681 Cr |
| Free cash flow | — | −₹5,332 Cr | −₹4,330 Cr |

---

## 31. North Star Metric

**Held Order Predictability (HOP)** *(Construct — does not exist at Zepto)*: the share of a store's weekly order volume that arrives inside a pre-committed slot rather than as unscheduled demand. A North Star built around *when* demand arrives, not just how much of it there is — because the case study's central claim is that variance, not volume, is the residual constraint on profitability inside the existing store base.

---

## 32. Product Analytics

Three analytics objects this proposal would require, none of which currently exist in the public product (Constructs):
1. **Slot-Commitment Rate** — share of a store's active users enrolled in a standing weekly order.
2. **Demand-Variance Index** — coefficient of variation of hourly order volume, per store, pre- and post-rollout.
3. **Fill-Rate on Committed Baskets** — how often a standing order can be fulfilled from existing inventory without a substitution, a direct proxy for whether forecasting improves.

---

## 33. AARRR Framework

| Stage | Current state | Gap this proposal targets |
|---|---|---|
| Acquisition | Strong — performance marketing, brand recognition | Not targeted |
| Activation | Fast first-order experience | Not targeted |
| Retention | Zepto Club (invite-only) | **Targeted** — converts retained users into scheduled users |
| Referral | Not a major public feature | Not targeted |
| Revenue | Growing fast, unprofitable | **Targeted indirectly** — via cost reduction from lower demand variance, not price increase |

---

## 34. HEART Framework

| Dimension | Current | With Zepto Steady |
|---|---|---|
| Happiness | High for speed; unmeasured for "peace of mind" around routine restocking | Adds a "set and forget" satisfaction dimension |
| Engagement | Order frequency | Adds slot-adherence as a new engagement signal |
| Adoption | Zepto Club adoption is invite-gated and unpublished | Steady adoption tracked openly from launch |
| Retention | Not publicly reported | Direct target metric |
| Task success | Delivery-time SLA | Adds basket-fill-rate SLA for committed orders |

---

## 35. Growth Strategy

Zepto's disclosed growth strategy is overwhelmingly horizontal: ~1,900 new dark stores, new cities, new categories (electronics, fashion), funded by IPO proceeds (§13.6). This case study does not argue against that strategy — it argues it is incomplete without a parallel, much cheaper vertical strategy: increasing the useful output of the 1,139 stores that already exist, which requires no new leases, no new hiring beyond what's already needed, and no city-launch playbook.

---

## 36. Growth Loops

**Existing loop:** Discount/free-delivery acquisition → order → (maybe) invite to Club → cashback → repeat order → more cashback.

**Proposed addition (Construct):** Commit to a weekly slot → discount for commitment → store forecasts better → fill rate improves → delivery gets faster/cheaper for committed users → more users opt to commit. A loop that reinforces itself through *operational* improvement, not just financial incentive — structurally different from a pure cashback loop, and cheaper to sustain because the "reward" comes partly from cost saved rather than purely from margin given up.

---

## 37. Network Effects

Quick commerce has weak classical network effects (one user's order doesn't directly benefit another's experience) but strong **local density effects**: more committed, schedule-predictable orders in a given store's catchment lower that store's per-order fulfilment cost for *everyone* served by it, including non-subscribers. This is the closest thing to a network effect this model can produce, and it is presently unexploited.

---

## 38. Product Strategy

Three positions are available to Zepto, mirroring a classic platform-strategy choice:

| Position | Description | Assessment |
|---|---|---|
| A — Pure speed/volume player | Keep competing on footprint and marketing spend | Current default; expensive, works only if capital keeps flowing |
| B — Retention-first operator | Build Zepto Club into the primary lever, invest more in loyalty than in new stores | Underinvested currently; invite-only gating limits reach |
| **C — Demand-shaping operator (recommended)** | Add a commitment layer (Zepto Steady) alongside continued but disciplined footprint growth | Cheapest to test, complements rather than replaces the IPO plan |

---

## 39. Monetization

### 39.1 Current
Commission on goods, delivery fees, advertising/placement fees, and Zepto Club subscription (₹99/month, invite-only, 5% Z-Coin cashback).

### 39.2 Zepto Pass → Zepto Club, read as one continuous experiment (Construct interpretation)
Zepto Pass (2024): open to all, ₹19–39/month, free delivery + discounts — an acquisition/retention hybrid that appears to have been discontinued. Zepto Club (2026): invite-only, ₹99/month, cashback-based — a narrower, pricier, more exclusive second attempt at the same underlying job (keep high-value users inside the app). Read together, this looks like a company that tried broad-and-cheap first, found it didn't hold margin, and pivoted to narrow-and-premium. **Zepto Steady is proposed as a third lever that neither Pass nor Club addresses: rewarding predictability of demand, not size or frequency of spend.**

### 39.3 Zepto Steady pricing construct
₹0 sign-up; discount tiered to commitment: 5% off a standing weekly basket delivered in a pre-selected 2-hour window, rising to 8% if the user allows Zepto to auto-substitute out-of-stock items rather than cancelling the line. Funded from delivery-cost savings (fewer emergency staffing spikes, better inventory turns), not from margin given away for its own sake (A6, ASSUMPTIONS.md).

---

## 40. Trust & Safety

Not a major public controversy area for Zepto specifically in the research window, beyond the FEMA-related compliance matter disclosed in the DRHP (documents submitted to the Enforcement Directorate) — treated here as a disclosed regulatory item, not adjudicated wrongdoing (§57, R1).

---

## 41. Technical Architecture *(Construct — reconstructed from public description, not a Zepto diagram)*

```
Consumer App → Order Service → Dark Store Inventory System (real-time stock)
                     ↓
        Delivery Assignment Engine → Rider App
                     ↓
        Demand Forecasting Layer → Procurement/Replenishment
```

Zepto Steady would add a **Commitment Scheduling Service** sitting between the Order Service and the Demand Forecasting Layer, converting a user's standing commitment into a forward-looking demand signal the forecasting layer can consume before the order is even placed.

---

## 42. Data Flow *(Construct)*

`User sets standing order → Commitment Service stores schedule → T-24hr: store notified of expected committed volume → store pre-allocates stock → T-2hr: user confirmed/edits basket → order fulfilled in normal flow`

---

## 43. API Ecosystem

Public disclosures describe integration with FMCG brand partners and a farmer-partner network for fresh produce; no public developer-facing API programme is a defining part of Zepto's product surface at this time.

---

## 44. Privacy & Security

Not independently audited in this analysis (public-sources-only boundary, Appendix D). A commitment-scheduling feature would need to handle recurring-payment-adjacent data (standing basket, preferred slot) with the same care as any stored-payment-method flow — flagged as a design requirement in §51, not evaluated against Zepto's actual practices.

---

## 45. Pain Points

1. **Company-level loss widens every year despite improving loss-to-revenue ratio** (§13.3) — the headline efficiency story and the headline cash story point in different directions.
2. **Zepto Club is invisible to most users** (invite-only) — the one live retention lever with the least reach.
3. **No commitment/scheduling surface exists** — every order is treated as a fresh decision, which is the single largest source of the demand variance that makes tier-2 and off-peak store-hours unprofitable.
4. **IPO capital is heavily weighted to new footprint** (§13.6) over deepening existing footprint.

---

## 46. Opportunity Mapping

Five independent lines of evidence converge on the same gap: (1) the financial line (losses widen despite improving ratios — a variance/mix story, not a pure margin story); (2) the store-profitability line (Bernstein's split shows most stores work, some don't — variance across stores); (3) the loyalty-product line (Pass → Club shows Zepto already knows it needs a retention lever, and has not yet built a *scheduling* one); (4) the IPO fund-use line (money is going to footprint, not utilisation); (5) the category-wide pattern (no major quick-commerce competitor has shipped a commitment-based scheduling product either — a genuine white space, not a me-too feature).

---

## 47. RICE Prioritisation

| Feature | Reach | Impact | Confidence | Effort | RICE | Stressed RICE* |
|---|---|---|---|---|---|---|
| **Zepto Steady (commitment subscription)** | 8 | 8 | 6 | 5 | 76.8 | 46.1 |
| Expand Zepto Club beyond invite-only | 9 | 5 | 7 | 3 | 105 | 63 |
| New dark-store footprint (status quo) | 10 | 7 | 8 | 9 | 62.2 | 37.3 |
| Electronics/fashion category launch | 6 | 6 | 4 | 8 | 18 | 10.8 |

*Stress rule (Construct, consistent with the series' prior stress methodology): reach × 0.6, confidence − 20pp, to reflect that reach and confidence are the two softest inputs on an unlaunched feature.

Zepto Steady does not win outright on stressed RICE — expanding Club's reach scores higher, and it should probably ship in parallel, since it is a distribution fix rather than a product-gap fix. Zepto Steady is proposed here specifically because it addresses a **gap no competitor has filled**, not because it wins a prioritisation exercise on paper (a decision this case study is explicit is a strategic bet, not an arithmetic conclusion).

---

## 48. MoSCoW

| Must | Should | Could | Won't (v1) |
|---|---|---|---|
| Weekly slot commitment | Auto-substitution opt-in | Multi-week scheduling | Full subscription-box curation |
| Committed-basket discount | Push reminders before cutoff | Family/shared account scheduling | Dynamic per-user pricing |
| Fill-rate SLA tracking | Store-level variance dashboard (internal) | Loyalty-tier stacking with Zepto Club | Cross-category standing baskets (v1 = grocery only) |

---

## 49. Kano Analysis

| Feature | Category |
|---|---|
| 10–15 min delivery | Basic (expected) |
| Zepto Club cashback | Performance (more is better, linear satisfaction) |
| Standing-order commitment discount | **Attractive** — absent from the category, would differentiate rather than merely match |
| Slot-adherence guarantee | Attractive, trending toward performance if competitors copy it |

---

## 50. Feature Proposal — Zepto Steady

**What it is:** an opt-in subscription layer where a user commits to a recurring weekly (or fortnightly) order — a flexible basket within a spend range, delivered inside a pre-selected 2-hour window — in exchange for a discount funded by the operational savings of predictable demand.

**Why now:** the store base is mostly profitable; the marginal unprofitability is concentrated in demand variance and new-store ramp, not in the core model. Zepto already has the inventory-forecasting infrastructure (§41) to consume a forward demand signal; it simply has never captured one from the customer side.

**What it is not:** a subscription-box curation product, a discount-maximisation play, or a replacement for footprint growth. It is a cheap, fast-to-pilot lever that should run alongside — not instead of — the IPO's dark-store expansion plan.

**User impact:** predictable, cheaper delivery for the users whose demand was already predictable (Meenal, §20) — a segment currently earning nothing for that predictability.

**Business impact:** lower per-order fulfilment cost in participating stores via better staffing and inventory turns; a new, more durable engagement signal (slot adherence) that complements Zepto Club rather than competing with it.

**Trade-offs:** discount given away up front, before savings are proven at scale; risk of low uptake if users don't trust Zepto to fulfil a committed basket reliably; added complexity in the order/fulfilment flow.

---

## 51. PRD — Zepto Steady v1

### 51.1 Problem
Zepto's demand is almost entirely unscheduled. This is the largest unaddressed source of per-store cost variance in an otherwise largely-profitable network.

### 51.2 Goals
- Launch in one metro (Bengaluru or Pune, both mid-density) across 25–40 dark stores.
- Reach a Slot-Commitment Rate of 8% of active users in participating stores within 90 days.
- Reduce Demand-Variance Index by ≥15% in participating stores within 90 days of meaningful adoption.

### 51.3 Non-goals (v1)
Not building multi-category standing baskets; not building shared/family scheduling; not dynamic-pricing the discount per user.

### 51.4 User stories
- As a user with a predictable weekly grocery need, I can commit to a recurring order and get a discount for doing so.
- As a user, I can edit or skip a committed order up to 2 hours before the window without penalty.
- As Zepto, I can see, per store, how much of next week's demand is already committed.

### 51.5 Acceptance criteria (Constructs — author-set bars)
- A1: Fill-rate on committed baskets ≥ 85% without substitution.
- A2: Slot-adherence (delivery inside the committed window) ≥ 90%.
- A3: No measurable increase in per-order cost for *non-committed* orders in participating stores (the feature must not degrade service for everyone else).
- A4: Opt-out/edit friction tested with real users to be under 30 seconds end-to-end.

---

## 52. Wireframes *(ASCII, Constructs)*

```
┌─────────────────────────────┐
│  Zepto Steady                │
│  Your weekly essentials,     │
│  delivered on schedule.      │
│                               │
│  [ Choose your day ▾ ]       │
│  [ Choose your window ▾ ]    │
│  [ Set your basket range ]   │
│                               │
│  Discount: 5% (8% with       │
│  auto-substitution)          │
│                               │
│  [   Start my Steady order  ]│
└─────────────────────────────┘
```

```
┌─────────────────────────────┐
│  This week's Steady order    │
│  Sunday, 9–11 AM              │
│  ₹450–₹600 range              │
│                               │
│  [ Edit basket ]  [ Skip ]   │
│  Cutoff: Sat 11 PM            │
└─────────────────────────────┘
```

---

## 53. Rollout Plan

| Phase | Scope | Gate |
|---|---|---|
| Phase 0 | Data check: do enough existing Zepto users already show weekly-repeat-basket behaviour to make commitment worth offering? | If no repeat pattern exists, stop and rethink (mirrors the series' Phase 0 kill-test convention) |
| Phase 1 | 25–40 stores, one metro, opt-in only | §51.5 acceptance criteria |
| Phase 2 | Expand to 3 metros, add auto-substitution tier | Fill-rate and variance-reduction hold at scale |
| Phase 3 | National rollout, integrate with Zepto Club (stacked benefits) | Positive unit-economics delta demonstrated store-by-store |

---

## 54. A/B Testing

**Arm A (control):** no change. **Arm B:** Zepto Steady offered at 5% discount. **Arm C:** Zepto Steady offered at 8% discount with mandatory auto-substitution. **Arm D (falsifier, Construct):** offer the *same* discount for a one-time large basket instead of a recurring commitment — designed to test whether users actually value predictability, or whether they just want a bigger discount and would take it in any form. If Arm D outperforms B and C, the "predictability" premise is wrong and the feature should be re-scoped as a plain bulk-discount tool.

---

## 55. KPI Dashboard *(Construct)*

| KPI | Target |
|---|---|
| Slot-Commitment Rate | ≥8% of active users (participating stores, 90 days) |
| Demand-Variance Index reduction | ≥15% |
| Fill-rate on committed baskets | ≥85% |
| Slot adherence | ≥90% |
| Non-participant service impact | 0 (no degradation) |

---

## 56. Product Roadmap

`Q1: Phase 0 data check → Q2: Phase 1 pilot (1 metro) → Q3: Phase 2 (3 metros) → Q4: Phase 3 decision gate, integrate with Zepto Club`

---

## 57. Risks & Mitigation

| # | Risk | Mitigation |
|---|---|---|
| R1 | Discount given away before savings materialise, worsening near-term losses right before/after a public listing | Cap pilot spend; require Phase-2 gate before national spend |
| R2 | Users don't value predictability enough to opt in (validated/falsified by Arm D) | Kill or re-scope if Arm D wins |
| R3 | Fulfilment reliability damages trust if committed baskets are frequently substituted or missed | Hard acceptance criteria (§51.5) before scaling |
| R4 | Feature cannibalises Zepto Club rather than complementing it | Stack benefits explicitly in Phase 3 rather than compete for the same user attention |

---

## 58. Future Vision

If Zepto Steady works, its natural extension is a forward-demand signal strong enough to change *procurement*, not just staffing — stores that know next week's committed volume in advance can negotiate tighter, more predictable supplier terms, extending the benefit from operations into the supply chain itself.

---

## 59. PM Lessons

The lesson this case study keeps returning to: a widening loss and an improving unit economics story can both be true, and conflating them — reading "losses keep growing" as "the model doesn't work" — leads to the wrong fix (more discounting, more marketing) instead of the right one (reduce the variance the model was never designed to handle).

---

## 60. PM Interview Questions

1. How would you distinguish a "growth investment" loss from a "broken unit economics" loss using only public financials?
2. Design a feature that reduces demand variance without raising customer acquisition cost. What would you measure to know it worked?
3. Zepto tried a broad loyalty program, killed it, and relaunched a narrower one. How would you decide whether that was the right call?

---

## 61. References

- Zepto FY24/FY25/FY26 financial reporting: Business Standard, Analytics Insight, Angel One, Entrackr, TechStory, BW Retail World (audited-filings coverage, Dec 2025–Jun 2026)
- Zepto Updated DRHP coverage: Outlook Business, ShareScart, Amquest Education, IPO Platform (Jun–Aug 2026)
- Zepto IPO pause and valuation reporting: Forbes India, Kotak Neo (Jul–Aug 2026)
- Quick-commerce market sizing: Mordor Intelligence; Reuters/Datum Intelligence via StartupFeed and Digital in Asia (2026)
- Store-level profitability estimates: Bernstein, cited in StartupFeed (Jun 2026)
- Zepto Pass / Zepto Club product coverage: BW Disrupt, VYGR News, Indian Startup News, Storyboard18, BW Retail World (2024–2026)
- Zepto founding/pivot history: general trade-press coverage of Aadit Palicha and Kaivalya Vohra, KiranaKart-to-Zepto pivot

---

## 62. About the Author

Written by Gaurav Singh as part of a 90-day product management case study series, applying a consistent research-led teardown methodology across Indian and global consumer products.

---

## 63. License

This document is an independent analysis for educational purposes. It is not affiliated with, endorsed by, or reviewed by Zepto. All company names and trademarks belong to their respective owners.

---

## 64. Self Review

| Check | Status | Note |
|---|---|---|
| No fabricated data | ✅ | Every figure sourced or explicitly derived; constructed content enumerated in Appendix C |
| Facts separated from assumptions | ✅ | ASSUMPTIONS.md |
| Conflicts disclosed | ✅ | Appendix A |
| Falsification designed | ✅ | §53 Phase 0, §54 Arm D |
| Recommendation shown against a prioritisation framework rather than engineered to win | ✅ | §47 — Steady does not top stressed RICE |

**Where this case study is weakest.** The FY25 revenue figure is genuinely contested between sources (₹9,668.8 Cr vs ₹11,110 Cr) and this document had to pick one for downstream arithmetic (§13.3) — the growth-rate math would shift if the other figure is correct. Second, the "operational revenue" 15–20%-of-GMV convention is an analyst estimate applied to Zepto by third parties, not a line Zepto itself has confirmed in these terms. Third, the entire thesis rests on Bernstein's store-profitability split, a single secondary source this analysis could not independently verify.

**What would change my mind.** Zepto disclosing its own per-store demand-variance data showing the variance problem is smaller than assumed; a Phase 0 retrospective (§53) finding no meaningful weekly-repeat-basket pattern among existing users; or Arm D (§54) showing users only want a bigger discount, not predictability.

---

## 65. Appendix

### Appendix A — Source Conflicts

| # | Conflict | Resolution |
|---|---|---|
| A-1 | Quick-commerce market size: $11.5B end-2025 (Reuters/Datum) vs $3.65B in 2026 (Mordor Intelligence) | Likely different scope/definition (GOV vs a narrower revenue base); the Reuters/Datum figure is used throughout as it aligns with order-volume and dark-store-count figures reported elsewhere |
| A-2 | Loss reporting is not apples-to-apples: Zepto reports net loss; Blinkit and Instamart report adjusted EBITDA loss | Flagged wherever loss figures are compared across competitors (§14) |
| A-3 | FY24 net loss: ₹1,248.6 Cr (PTI/Business Standard, citing Tofler) vs ₹1,214.7 Cr (Analytics Insight/Angel One, citing audited MCA filings) | Both carried as a band throughout |
| A-4 | FY25 revenue: ₹9,668.8 Cr (multiple filings-based reports) vs ₹11,110 Cr (Entrackr, citing regulatory filings) | Both stated; ₹9,668.8 Cr used for FY25→FY26 arithmetic (§13.3) |
| A-5 | Pre-IPO valuation: $5B round (Motilal Oswal/Raamdeo Agrawal-backed) vs $7B round (CalPERS/General Catalyst-led, Oct 2025) | Unresolved; both may refer to different tranches within the same broader pre-IPO fundraising process |

### Appendix B — Evidence Grades

| Grade | Meaning | Applied to |
|---|---|---|
| 🟢 High | Regulatory filing / DRHP disclosure | Dark store count, city count, IPO fund-use table, FY26 revenue/loss figures |
| 🟡 Medium | Trade press citing filings, consistent across sources | FY24/FY25 revenue and loss figures, order volume, market share bands |
| 🟠 Low | Single secondary-source estimate | Bernstein store-profitability split, operational-revenue-as-%-of-GMV convention |
| 🔴 Conflicting | Sources materially disagree | FY24 loss, FY25 revenue, market size, pre-IPO valuation |

### Appendix C — Author-Constructed Content

Everything below is mine, not Zepto's. Full reasoning in [ASSUMPTIONS.md](./ASSUMPTIONS.md).

| # | Construct | Where |
|---|---|---|
| C1 | Zepto Steady — the entire proposal | §50 |
| C2 | Held Order Predictability (North Star) | §31 |
| C3 | Slot-Commitment Rate, Demand-Variance Index, Fill-Rate metrics | §32 |
| C4 | Personas Aditi, Karan, Meenal | §20 |
| C5 | All RICE inputs and the stress rule | §47 |
| C6 | Acceptance-criteria bars | §51.5 |
| C7 | The four-arm A/B design including Arm D as falsifier | §54 |
| C8 | Technical architecture and data-flow reconstructions | §41, §42 |
| C9 | The reading of Pass→Club as one continuous, still-incomplete experiment | §39.2 |

### Appendix D — Asset Status

| Asset | Status |
|---|---|
| ASCII wireframes | ✅ Authored (§52) |
| Product screenshots | ❌ Not included — no authenticated session was used |
| UI/accessibility audit | ❌ Not independently tested — flagged as a research-boundary gap |

---

*Day 50 of 90 · ← [Day 49 — River Mobility](../Day-49-River-Mobility) · [Day 51 →](../Day-51-Ola)*
