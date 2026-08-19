# Dream11 — 95% of Revenue, Gone by Act of Parliament

### Day 54 of 90 · Product Management Case Study Series

> **The thesis of this case study:** most product crises are competitive. Dream11's was legislative, and it happened almost overnight. On 21–22 August 2025, India's Parliament passed the Promotion and Regulation of Online Gaming Act (PROGA), banning all real-money gaming nationwide — fantasy sports with cashouts, rummy, poker, ludo. Dream11's own CEO, Harsh Jain, later put a number on what that meant: **real-money contests were roughly 95% of Dream Sports' revenue and 100% of its profit.** The company suspended paid contests, processed user withdrawals, lost its ₹358 Cr Indian national cricket team jersey sponsorship overnight, and pivoted — within weeks — to a free-to-play product monetised by ads and sponsorships. This case study is not about whether the ban was right or wrong; that's a genuinely contested policy question this document stays out of (§57, R1). It's about a narrower, answerable product question the company's own "Dream11 3.0" strategy has not yet publicly resolved: **does a fantasy sports product built entirely around real cash stakes retain any of its engagement once the cash is removed?** Free-to-play fantasy sports is not a smaller version of real-money fantasy sports — it is arguably a different product, competing for attention against every other free entertainment app on a phone, without the one mechanic (skin in the game) that made Dream11 different from a highlights reel. Dream Sports' response has been to diversify outward — FanCode (content), DreamSetGo (travel), DreamCricket (casual gaming), DreamMoney (fintech) — essentially betting that 250 million registered users and two decades of brand equity can be monetised across an ecosystem even if the core product's engagement structurally weakens. That may well be the right bet. What's missing from the public record is any evidence the company has tested the narrower, cheaper question first: whether a *compliant*, non-cash stakes mechanic could recover meaningfully more engagement than pure ad-supported free-to-play, before betting the company's future on four new, unproven business lines simultaneously.

---

## 2. Repository Metadata

| Field | Value |
|---|---|
| **Case study** | Day 54 of 90 |
| **Product** | Dream11 — fantasy sports platform (now free-to-play post-ban) |
| **Company** | Dream Sports (parent), Sporta Technologies Pvt Ltd (operating entity, post US-to-India domicile shift), Mumbai |
| **Domain** | Sports entertainment / gaming — post-regulatory pivot |
| **Primary competitors** | Mobile Premier League (MPL), My11Circle (Games24x7), My Circle11, and — pre-ban — the entire real-money-gaming sector, now largely wound down in India |
| **Analysis type** | Research-led product teardown + financial reconstruction + a feature proposal |
| **Proposed system** | **Dream11 Trophy Room** — a compliant, non-cash stakes and reward mechanic, piloted to test whether "something to play for" (not cash, not just ads) recovers engagement that pure free-to-play cannot |
| **Author** | Gaurav Singh |
| **Date of analysis** | 17 August 2026 |
| **Research boundary** | Public sources only — RoC filings coverage, trade press, company statements. No Dream11/Dream Sports employee, internal document, or authenticated session was consulted. |
| **Latest financials available** | FY25 (year ended 31 March 2025), per Dream11's consolidated financial statements sourced from the RoC — **this predates the August 2025 ban**; FY26 figures, which would show the ban's actual financial impact, were not found publicly disclosed as of the date of analysis |

---

## 3. Badges

![Case Study](https://img.shields.io/badge/Case%20Study-Day%2054%20of%2090-blue)
![Domain](https://img.shields.io/badge/Domain-Gaming%20%2F%20Sports%20Entertainment-orange)
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

Dream11, founded in 2008 by Harsh Jain and Bhavit Sheth, became India's first gaming unicorn and, by a 2021 funding round ($840M led by Falcon Edge and Tiger Global), was valued at **$8B**. It built a fantasy-sports business around real-money contests tied to cricket, reaching over **250 million registered users** and, at IPL peak, reportedly up to **50 million daily active users**. Financially, it scaled fast and profitably for years: FY23 revenue was ₹6,384 Cr with PAT of ₹188 Cr (up 32% YoY). FY24 revenue reportedly reached ₹7,934–8,345.9 Cr depending on source (Appendix A). FY25 — the most recent full audited year, and importantly, **the year before the ban** — showed operating revenue *declining* 15% to ₹6,759 Cr, alongside a **₹478.9–479 Cr net loss**, the company's first major loss in years.

Here is the detail that matters for reading that FY25 loss correctly: **it happened before the ban.** PROGA was passed in August 2025 — four to five months after FY25 (ended 31 March 2025) had already closed. Per Entrackr's reporting of the RoC-sourced financials, the FY25 loss was driven primarily by two items unrelated to the ban: a one-time ₹575 Cr tax expense tied to Dream Sports Inc.'s merger with Sporta Technologies (a US-to-India domicile shift), and a 62% jump in employee benefit expenses (₹1,030 Cr → ₹1,673 Cr) that included ₹778 Cr in "benefits to directors," widely understood as ESOP-related costs. **Gross Gaming Revenue (platform fees before adjustments) was actually ₹10,284 Cr in FY25** — the underlying contest business was still large. The loss was a corporate-structuring and compensation story, not (yet) a ban story.

The ban story is still unwritten in public financials. When PROGA passed, Dream11 suspended all real-money contests, processed user withdrawals, and — per CEO Harsh Jain's own account — watched roughly 95% of Dream Sports' revenue and 100% of its profit disappear essentially overnight. It lost the Indian national cricket team's jersey sponsorship (a ₹358 Cr, three-year deal signed in 2023) without a replacement sponsor immediately in hand. Within weeks it pivoted to a free-to-play model funded by advertising and sponsorships (early partners: Swiggy, Astrotalk, Tata Neu, and branded contests with Cred), reporting **10 million daily active users** on the new format. By December 2025 the positioning had shifted further, to a "second-screen sports entertainment platform" with creator-led watch-alongs. Parent company Dream Sports laid out a **"Dream11 3.0"** roadmap spanning FanCode (sports content), DreamSetGo (sports travel), DreamCricket (mobile gaming), and DreamMoney (fintech/micro-investing) — a bet that brand and reach, not the original product mechanic, can carry the company forward. By March 2026, internal restructuring into startup-style business units had led to 100+ employee exits (~15% of 700 reassigned staff).

**What this case study finds missing:** no public data yet shows whether the free-to-play product is actually holding user engagement, as opposed to just user *counts* — 10 million DAU sounds substantial until compared against the up-to-50-million DAU the real-money product drew at peak, a number this document cannot yet compare cleanly against post-ban DAU on a like-for-like basis (different measurement windows, Appendix A). More specifically: nothing public tests whether the problem is "no cash" or "no stakes at all" — a distinction with a testable, PROGA-compliant middle ground (non-cash prizes, brand-funded rewards, leaderboard status) that the current ads-only pivot skips past entirely in favour of diversifying into four new business lines at once. The proposal in §50 — **Dream11 Trophy Room** — is designed to test that narrower, cheaper question before the company commits fully to the "reach without stakes" bet its current roadmap represents.

---

## 6. Product Overview

Dream11 is a mobile/web fantasy-sports app, historically centred on cricket (with football, kabaddi, and other sports as secondary categories), where users build virtual teams of real athletes and earn points based on real-match performance. Pre-ban, its core loop was entry-fee-based contests with real-money prizes. Post-ban, the product is free-to-play: users can still build teams and compete on leaderboards, but without cash entry or cash prizes — supplemented by a growing content/entertainment layer (creator watch-alongs, banter streams) designed to keep the app relevant as a second-screen companion during live matches even without the wagering mechanic.

---

## 7. Company Background

Founded 2008 in Mumbai by Harsh Jain and Bhavit Sheth as Sporta Technologies; the flagship Dream11 product launched later and grew into India's dominant fantasy-sports platform through cricket-season virality and major sponsorships — including IPL title sponsorship rights (2020, ₹222 Cr, stepping in after Vivo withdrew) and the Indian national cricket team's lead jersey sponsorship (from July 2023, ₹358 Cr over three years). The company scaled to unicorn status and, by 2021, an $8B valuation on a $840M raise. It had already been navigating a difficult regulatory environment before PROGA: a 28% GST regime introduced in 2023 (levied on the full contest entry value rather than the platform's margin/fee) had already forced Dream11 to cut FY24 operating-profit targets by a reported 80%, and Dream Sports has faced **GST demands reportedly exceeding ₹28,000 Cr**, with the Supreme Court reserving judgment on the matter in August 2025 — the same month PROGA passed. Two separate, compounding regulatory shocks landed on the company within the same narrow window.

---

## 8. Product Timeline

| Year | Milestone |
|---|---|
| 2008 | Founded as Sporta Technologies |
| 2019 | India's first gaming unicorn |
| 2020 | Wins IPL title sponsorship (₹222 Cr) |
| 2021 | Raises $840M at $8B valuation (Falcon Edge, Tiger Global, others) |
| 2023 (Jun) | Wins Indian national cricket team jersey sponsorship (₹358 Cr, 3 years) |
| 2023 | 28% GST regime introduced; FY24 operating-profit targets cut ~80% as a result |
| FY23 | Revenue ₹6,384 Cr, PAT ₹188 Cr |
| FY24 | Revenue ₹7,934–8,345.9 Cr (source-dependent) |
| FY25 (ended Mar 2025) | Revenue from ops ₹6,759 Cr (−15% YoY); net loss ₹478.9–479 Cr, driven by domicile-shift tax charge and ESOP-linked director benefits, **not** the (not-yet-passed) ban |
| 2025 (Aug) | Supreme Court reserves judgment on the ₹28,000+ Cr GST dispute; days later, Parliament passes PROGA, banning real-money gaming nationwide |
| 2025 (Aug–Sep) | Dream11 suspends real-money contests, processes withdrawals, loses national-team sponsorship, pivots to free-to-play (ads/sponsorship model); reports 10M DAU on the new format |
| 2025 (Nov) | Global (non-India) expansion announced |
| 2025 (Nov 18–22) | Sector-wide ED raids linked to PROGA enforcement |
| 2025 (Dec) | Pivots further to "second-screen sports entertainment," launching creator-led watch-alongs |
| 2026 (Jan–Mar) | "Dream11 3.0" roadmap disclosed (FanCode, DreamSetGo, DreamCricket, DreamMoney); internal restructuring leads to 100+ employee exits |

---

## 9. Vision & Mission

Dream11's pre-ban positioning centred on turning passive sports viewership into active, skill-based participation. Post-ban, per CEO Harsh Jain's public statements ("No sports fan should ever watch a match alone"), the stated vision has shifted toward being a **second-screen companion for sports fandom broadly** — participation, content, and community, rather than specifically wagering-based participation. This is a genuine, defensible pivot in mission language; the open question this case study raises is whether the *product* has caught up to that new mission, or whether it's still functionally the old product with the cash removed.

---

## 10. Problem Statement

**For the company:** roughly 95% of revenue and 100% of profit were tied to a mechanic now illegal in its largest market, and the replacement business model (ads/sponsorship on a free product, plus diversification into four new lines) is unproven at anything like the scale of the business it's replacing.

**For the user:** the core reason many users engaged deeply with Dream11 — something real at stake — is gone, and nothing has yet visibly replaced it beyond the entertainment value of the underlying sport itself, which was always free to watch elsewhere.

---

## 11. Market Research

India's real-money gaming sector was projected, before the ban, to be worth **$3.6B by 2029** (a figure cited in coverage of the ban's shock to VC backers like Tiger Global and Peak XV). That market, for real-money formats, is now effectively zero in India following PROGA — one of the sharpest, fastest total-addressable-market collapses available to study in any consumer-tech category, anywhere. The free-to-play/ad-supported fantasy and casual-gaming market that companies are now pivoting into is comparatively immature and has no established precedent at the scale Dream11 previously operated.

---

## 12. Industry Analysis

The entire real-money-gaming sector reacted almost identically and almost simultaneously: Dream11, MPL, Games24x7, PokerBaazi, GamesKraft, Zupee, Probo, and Paytm's First Games all suspended real-money operations, enabled withdrawals, and pursued some mix of free-to-play pivots, workforce reductions, and overseas restructuring. Hike shut down entirely. This is not a story of Dream11 losing share to a competitor's better product — the entire category's core mechanic became illegal at once, meaning **every player faces the same unanswered product question this case study raises about Dream11 specifically.**

---

## 13. TAM / SAM / SOM

### 13.1 The collapse, quantified
Per CEO Harsh Jain: **~95% of Dream Sports' revenue and 100% of its profit** came from real-money contests, now banned. Applied illustratively to FY25's ₹6,759 Cr operating revenue, this implies a potential **post-ban addressable revenue base of roughly ₹340 Cr** from whatever legacy revenue wasn't RMG-dependent — before accounting for any new revenue the free-to-play/ads/sponsorship pivot generates (D1, ASSUMPTIONS.md; this is an illustrative order-of-magnitude calculation, not a disclosed FY26 figure, which was not found publicly available).

### 13.2 Full financial reconstruction (pre-ban years)

| Metric | FY23 | FY24 | FY25 |
|---|---|---|---|
| Revenue from operations | ₹6,384 Cr | ₹7,934 Cr (RoC/Entrackr) or ₹8,345.9 Cr (Inc42) | ₹6,759 Cr |
| Total income (incl. non-operating) | — | — | ₹7,374 Cr |
| Gross Gaming Revenue (pre-adjustment platform fees) | — | — | ₹10,284 Cr |
| Net profit / (loss) | ₹188 Cr | Not confirmed in sources reviewed | (₹478.9–479 Cr) |
| Employee benefit expense | — | ₹1,030 Cr | ₹1,673 Cr (of which ~₹778 Cr director/ESOP-linked) |
| One-time domicile-merger tax charge | — | — | ₹575 Cr |
| Total expenditure | — | ₹6,562 Cr | ₹7,123 Cr |

### 13.3 The GST overhang
A separate, longer-running dispute: **GST demands reportedly exceeding ₹28,000 Cr** against Dream Sports, spanning multiple financial years, with the Supreme Court having reserved judgment as of August 2025. This is not resolved as of the date of analysis and represents a large contingent liability independent of the RMG ban itself (§57, R2).

### 13.4 Post-ban user metrics (available)
250M+ registered users (pre- and post-ban, cumulative); up to ~50M DAU at IPL peak, pre-ban; **10M DAU reported post-pivot to free-to-play** (September 2025). These two DAU figures are not strictly comparable — one is a cricket-season peak, the other a point-in-time figure reported shortly after the pivot — and this document treats the comparison as directional only (Appendix A).

---

## 14. Competitor Analysis

| Dimension | **Dream11** | MPL | Games24x7 (My11Circle) | The broader RMG sector |
|---|---|---|---|---|
| Pre-ban model | Real-money fantasy sports | Real-money fantasy + casual games | Real-money rummy/fantasy | Real-money contests across formats |
| Post-ban status | Free-to-play + ads/sponsorship + ecosystem diversification | Suspended paid contests, restructuring | Suspended paid contests | Sector-wide suspension/wind-down |
| Sponsorship exposure | Lost India national cricket team jersey deal (₹358 Cr/3yr) | Smaller public sponsorship footprint | Smaller public sponsorship footprint | Varies |
| Global expansion response | Yes — announced Nov 2025 | Less publicly emphasised | Less publicly emphasised | Mixed |
| Legal challenge to PROGA | **CEO confirmed will not challenge** | Some operators reportedly explored Supreme Court challenge | Some operators reportedly explored Supreme Court challenge | Mixed, industry-wide discussions ongoing |

---

## 15. SWOT

| Strengths | Weaknesses |
|---|---|
| 250M+ registered users, strong brand recognition | Core monetisation mechanic (real-money stakes) is now illegal in its home market |
| Diversified ecosystem already partly built (FanCode, DreamSetGo) before the ban, giving a head start on the 3.0 pivot | Post-ban engagement (DAU) not cleanly comparable to pre-ban peak, and no public retention data yet |
| Willingness to comply rather than litigate may preserve regulatory goodwill | Lost a marquee national-team sponsorship without an immediate replacement |
| Genuine first-mover advantage in the free-to-play pivot versus slower-moving competitors | FY25 already showed a large loss even before the ban's financial impact is reflected |

| Opportunities | Threats |
|---|---|
| A PROGA-compliant, non-cash stakes mechanic remains untested publicly — genuine white space | Every other RMG player is pivoting simultaneously into the same free-to-play/ads space, commoditising the opportunity |
| DreamMoney (fintech) could capture some of the value users previously extracted as gaming winnings, if trust transfers | ₹28,000+ Cr GST overhang remains unresolved and could still materially impact the balance sheet |
| Global markets untouched by India's ban | User habits built entirely around cash stakes for over a decade may not transfer to a free product at all |

---

## 16. Porter's Five Forces

| Force | Intensity | Note |
|---|---|---|
| Competitive rivalry | Reduced in intensity but shared existential pressure — the whole category is pivoting at once, so rivalry is now more about who diversifies successfully than who wins engagement share |
| Threat of new entrants | Low, for now — the domestic market's core mechanic is illegal, removing the incentive for RMG-style new entrants |
| Bargaining power of suppliers (sports leagues/sponsorship rights) | Reduced — Dream11 lost a marquee sponsorship and the ad/sponsorship-only model has less to offer rights-holders than a cash-flush RMG business did |
| Bargaining power of buyers (users) | Very high — free-to-play users have zero switching cost and no financial reason to stay loyal to any one app |
| Threat of substitutes | Very high — literally any other free entertainment app now competes directly for the same attention Dream11 used to monopolise via stakes |

---

## 17. Business Model Canvas

| Block | Summary |
|---|---|
| Key Partners | Advertisers (Swiggy, Astrotalk, Tata Neu, Cred), sports leagues/broadcasters, Dream Sports ecosystem entities (FanCode, DreamSetGo) |
| Key Activities | Free-to-play contest hosting, content/watch-along production, ecosystem diversification |
| Value Propositions | Free sports engagement + fan community (post-ban); previously, real-money stakes on sports knowledge |
| Customer Relationships | App-native; historically strengthened by cash stakes, now reliant on entertainment/community value alone |
| Customer Segments | 250M+ registered cricket/sports fans, 70% aged 18–35 |
| Channels | Mobile app, in-app branded content, cross-promotion via FanCode/DreamSetGo |
| Key Resources | Brand, user base, cricket/sports partnerships, engineering/compliance infrastructure adaptable across the ecosystem |
| Cost Structure | Content production, technology, restructuring costs, unresolved GST contingent liability |
| Revenue Streams | Advertising, sponsorships, branded contests; ecosystem-level revenue from FanCode, DreamSetGo, DreamCricket, DreamMoney |

---

## 18. Revenue Model

Pre-ban, Dream11's revenue model was platform fees on real-money contests — a model that, per CEO Jain, accounted for ~95% of revenue and 100% of profit. Post-ban, the model is advertising and sponsorship revenue against a free product, which is structurally a **lower-margin-per-user model** unless engagement (and therefore ad inventory value) holds up at something close to prior levels — the exact question this case study argues is untested (§45, §46).

---

## 19. Target Users

- **Existing 250M+ registered users**, the vast majority of whose entire relationship with the app was built around real-money stakes — an unprecedented mass-retention challenge.
- **New free-to-play users**, potentially attracted by zero financial risk, who represent a genuinely different (and unproven) acquisition funnel.
- **Advertisers/sponsors**, now Dream11's primary paying customer in a real sense — a fundamental business-model inversion from "users pay to play" to "brands pay to reach users."

---

## 20. Personas

**Persona — Rohan, 27, Delhi, long-time real-money Dream11 player (Construct)**
Played weekly during IPL, deposited and withdrew real money, valued the stakes as much as the sport itself. Post-ban, opened the free-to-play app a few times, found it "pointless without anything on the line," and largely stopped. Represents the retention risk this case study is most concerned about.

**Persona — Simran, 22, Bengaluru, casual cricket fan (Construct)**
Never played real-money Dream11 (risk-averse, or simply uninterested in gambling-adjacent products), but enjoys the free-to-play format as a lightweight second-screen companion during matches, alongside the new watch-along/creator content. Represents a genuinely new segment the pivot might open up.

**Persona — Marketing lead at a challenger D2C brand (Construct, illustrative)**
Evaluating whether to advertise on Dream11's new free platform — attracted by the 250M registered user base and cricket-season reach, but needs to see engagement data (not just registered-user counts) before committing meaningful spend.

---

## 21. Jobs to Be Done

- Rohan-type user: "Give me something meaningfully at stake when I watch a match." (**not served** post-ban, per current product)
- Simran-type user: "Let me participate lightly in the match without any financial commitment." (served by the current free-to-play + content pivot)
- Advertiser: "Reach a large, engaged, young cricket audience efficiently." (partially served — reach exists, engagement depth is the open question)

---

## 22. User Journey (Rohan-type, pre- to post-ban)

`Years of real-money play → ban announced → withdraw remaining balance → app becomes free-to-play → try it a few times → find it doesn't replicate the "something at stake" feeling → disengage or reduce usage sharply`

---

## 23. User Flow (current, free-to-play)

`Open app → join free contest / watch-along → compete on leaderboard (no cash) → see ads/sponsored content → repeat or churn`

**Gap (Construct):** no branch exists between "pure free-to-play" and "watch-along content" that gives a user something tangible (non-cash) to play for — the middle ground this proposal targets.

---

## 24. Information Architecture

`Home → Live Matches → Free Contests → Watch-Alongs/Creator Content → DreamMoney / DreamSetGo / DreamCricket / FanCode (cross-ecosystem links)`

**Gap:** the ecosystem cross-links (3.0 strategy) are visible in the IA; a dedicated "what am I playing for" reward/status surface is not.

---

## 25. UX Audit

| Area | Observation |
|---|---|
| Contest participation | Functionally similar to pre-ban flow, minus payment | A reasonable transition choice, but risks feeling like "the same game with the point removed" |
| Watch-alongs/content | New, differentiated addition | Genuine attempt to build a new value proposition beyond the removed mechanic |
| Cross-ecosystem navigation (3.0) | Present | Not independently assessed for friction in this document |

---

## 26. UI Audit

Not independently screenshot-audited (public-sources-only boundary; Appendix D).

---

## 27. Accessibility

Not independently tested in this analysis.

---

## 28. Feature Breakdown

| Feature | Status | Notes |
|---|---|---|
| Free-to-play contests | Live, since Sep 2025 | Core of the pivot |
| Creator watch-alongs / banter streams | Live, since Dec 2025 | Genuine new value proposition |
| Branded contests (e.g., with Cred) | Live | Sponsorship-monetisation mechanic |
| Ecosystem cross-promotion (FanCode, DreamSetGo, DreamCricket, DreamMoney) | Live/expanding | The "3.0" diversification bet |
| **Non-cash stakes/reward mechanic (compliant "something to play for")** | **Does not appear to exist publicly** | The gap this proposal targets |

---

## 29. AI Capabilities

No major public disclosure of a distinguishing AI feature in the post-ban product surface was found in this research window; personalisation of content/watch-along recommendations is plausible but not independently confirmed.

---

## 30. Product Metrics

See §13.2 and §13.4. Key figures: FY25 revenue from ops ₹6,759 Cr (pre-ban); FY25 net loss ₹478.9–479 Cr (pre-ban, structurally unrelated to the ban per §5); post-ban DAU 10M (Sep 2025, not cleanly comparable to pre-ban peak DAU); 250M+ registered users (cumulative, unaffected by the ban itself).

---

## 31. North Star Metric

**Stakes-Adjusted Engagement Rate (SAER)** *(Construct — does not exist at Dream11)*: weekly active users normalised by session depth and repeat-contest participation, tracked separately for users exposed to any non-cash stakes mechanic versus users on pure ad-supported free-to-play. Proposed as North Star because raw DAU (§13.4) cannot distinguish "the pivot is working" from "people are still opening the app out of habit while genuinely disengaging."

---

## 32. Product Analytics

Three analytics objects this proposal would require (Constructs, not currently public):
1. **Pre-Ban vs. Post-Ban Retention Cohort** — a like-for-like comparison of the same user cohort's engagement before and after the ban, controlling for the different measurement windows flagged in Appendix A.
2. **Stakes-Mechanic Lift** — engagement delta between users in a non-cash-stakes pilot versus a pure ad-supported control group.
3. **Advertiser Value Realisation** — whether sponsors report engagement/conversion outcomes consistent with the 250M-user reach claim, or whether reach is proving to be a vanity metric for advertisers.

---

## 33. AARRR Framework

| Stage | Current state | Gap this proposal targets |
|---|---|---|
| Acquisition | Still strong — 250M+ registered base, brand recognition | Not targeted |
| Activation | Unclear — first free-to-play session engagement not publicly disclosed | Indirectly targeted |
| Retention | **The central open question** — no public data distinguishes habit from genuine engagement | **Directly targeted** |
| Referral | Not a major public feature post-ban | Not targeted |
| Revenue | Shifted entirely to advertiser-side; scale unproven | Indirectly targeted via retention data informing advertiser confidence |

---

## 34. HEART Framework

| Dimension | Current (post-ban) | With Trophy Room |
|---|---|---|
| Happiness | Unmeasured publicly | Tests whether non-cash stakes improve satisfaction versus pure free-to-play |
| Engagement | 10M DAU reported, depth unclear | Session-depth and repeat-participation tracked by cohort |
| Adoption | N/A (feature doesn't exist) | Tracked from pilot launch |
| Retention | Unmeasured publicly, the central risk | Direct target metric |
| Task success | Contest completion (aggregate) | Compared across stakes vs. no-stakes cohorts |

---

## 35. Growth Strategy

Dream Sports' disclosed strategy is broad diversification — FanCode, DreamSetGo, DreamCricket, DreamMoney — betting that ecosystem breadth substitutes for the lost core mechanic. This case study does not argue against diversification; it argues the company appears to be running four large, expensive strategic bets in parallel without first running the cheapest, most directly relevant experiment: whether a compliant stakes mechanic recovers engagement the ads-only pivot alone cannot.

---

## 36. Growth Loops

**Current loop (pure free-to-play):** Open app → free contest/watch-along → ads shown → close app → uncertain re-engagement trigger (habit, cricket schedule, notification).

**Proposed addition (Construct):** Open app → free contest with non-cash stakes (leaderboard status, brand-funded prizes) → genuine incentive to return and defend/improve standing → higher repeat engagement → more valuable ad inventory → funds larger non-cash prize pools → loop reinforces itself.

---

## 37. Network Effects

Fantasy sports has moderate network effects through leagues/private contests among friends — this dynamic is unaffected by the ban and remains a genuine strength of the free-to-play product. What the ban removed was the *individual* stakes mechanic (real money, regardless of social context), not the social layer — meaning any recovery strategy should distinguish between shoring up the social/league mechanic (likely intact) and the individual-stakes mechanic (genuinely gone).

---

## 38. Product Strategy

| Position | Description | Assessment |
|---|---|---|
| A — Pure ads/sponsorship free-to-play (current default) | Monetise reach directly, no stakes mechanic | Cheapest to run; retention risk untested |
| B — All-in ecosystem diversification (Dream11 3.0) | FanCode, DreamSetGo, DreamCricket, DreamMoney simultaneously | High-ambition, capital-intensive, doesn't address the core product's retention question directly |
| **C — Test a compliant non-cash stakes mechanic first (recommended)** | Cheap, fast pilot to answer the retention question before/alongside the 3.0 bets | Directly tests the assumption embedded in every other strategic option |

---

## 39. Monetization

### 39.1 Current
Advertising, sponsorships, branded contests — monetising reach rather than participation fees.

### 39.2 The compliance constraint this proposal is explicit about
PROGA bans real-money gaming; any proposed mechanic must involve **no cash entry fee, no cash prize, and no cash-convertible value** to remain compliant. This is a hard constraint, not a workaround to be tested cautiously — the proposal in §50 is designed around it, not against it.

### 39.3 Dream11 Trophy Room construct
A leaderboard-and-rewards layer funded entirely by sponsor partners: top performers in free contests earn verified, non-cash rewards (branded merchandise, experiences, product vouchers from advertisers like Swiggy or Tata Neu) instead of cash. Sponsors get a genuine engagement mechanic to attach their brand to (stronger than passive ad display); users get something tangible to play for; Dream11 stays compliant by design.

---

## 40. Trust & Safety

The regulatory context here (§7, §13.3) is itself a trust-and-safety-adjacent story — India's lawmakers acted on documented concerns about gaming addiction and financial harm from real-money gaming (§57, R1 discusses this directly rather than treating it as a footnote). Any proposed non-cash mechanic must be designed with the same concern in mind: a reward/status system that recreates compulsive engagement patterns without cash changing hands would not actually address the underlying policy concern, even if it were legally compliant. This is flagged as a design principle in §51.5, not an afterthought.

---

## 41. Technical Architecture *(Construct — reconstructed from public description)*

```
Match Data Feed → Contest Engine (free-to-play) → Leaderboard Service
                          ↓
              Content/Watch-Along Service (creator layer)
                          ↓
         Ad Serving & Sponsorship Attribution Layer
```

Trophy Room would add a **Non-Cash Reward Ledger** service, tracking verified leaderboard achievement against sponsor-funded reward inventory, with strict compliance checks ensuring no reward is cash-convertible.

---

## 42. Data Flow *(Construct)*

`Contest completed → leaderboard updated → top performers flagged → reward eligibility checked against sponsor inventory → non-cash reward issued and logged → engagement/retention data compared against non-eligible cohort`

---

## 43. API Ecosystem

No major public developer-facing API programme is a defining part of Dream11's product surface in this research window.

---

## 44. Privacy & Security

Not independently audited in this analysis. A non-cash reward system, as proposed in §41, would need fulfilment/logistics data handling (shipping addresses for physical rewards, etc.) with standard e-commerce-level care — a design requirement noted here, not an evaluation of Dream11's actual practices.

---

## 45. Pain Points

1. **~95% of revenue and 100% of profit disappeared by law**, and the replacement model's actual engagement durability is untested in public data.
2. **FY25's large loss predates the ban** and is frequently conflated with it in casual coverage — the two stories need to be told separately (§5).
3. **No public product yet tests the specific, cheap question of whether non-cash stakes recover engagement**, despite the company running four expensive, unproven diversification bets in parallel.
4. **DAU comparison across the ban is not apples-to-apples** (peak-season pre-ban vs. point-in-time post-ban), making it hard for outside observers — and possibly for the company itself — to know how well the pivot is really working.

---

## 46. Opportunity Mapping

Three lines converge: (1) the financial line (a business that lost ~95% of revenue by law needs the cheapest possible experiments first, not just the biggest bets); (2) the product line (free-to-play removes the one mechanic — stakes — that structurally differentiated Dream11 from any other sports content app, and no compliant substitute has been publicly tested); (3) the sponsor line (advertisers considering Dream11 need engagement proof, not just reach numbers, to justify sustained spend — a stakes mechanic funded by those same sponsors could serve both goals at once).

---

## 47. RICE Prioritisation

| Feature | Reach | Impact | Confidence | Effort | RICE | Stressed RICE* |
|---|---|---|---|---|---|---|
| **Dream11 Trophy Room (non-cash stakes pilot)** | 7 | 8 | 6 | 4 | 84 | 50.4 |
| Continue pure ads/sponsorship model (status quo) | 9 | 4 | 8 | 2 | 144 | 86.4 |
| Full "Dream11 3.0" ecosystem diversification | 6 | 7 | 5 | 9 | 23.3 | 14 |
| Global (non-India) expansion acceleration | 5 | 6 | 6 | 7 | 25.7 | 15.4 |

*Stress rule (Construct, consistent with the series' methodology): reach × 0.6, confidence − 20pp.

Status-quo scores highest on stressed RICE, unsurprisingly — it's already built and requires no new investment. Trophy Room is recommended not because it beats the status quo on paper, but because it's the cheapest way to learn whether the status quo is actually working before committing further capital to the much larger, much more expensive 3.0 diversification bets.

---

## 48. MoSCoW

| Must | Should | Could | Won't (v1) |
|---|---|---|---|
| Non-cash-only reward ledger, compliance-verified | Sponsor-funded reward inventory pipeline | Tiered leaderboard status (badges, ranks) | Any cash-convertible mechanic (hard exclusion) |
| Leaderboard/eligibility tracking | Retention-cohort comparison dashboard (internal) | Social/league-specific reward pools | Full re-launch of paid contests (illegal under PROGA) |

---

## 49. Kano Analysis

| Feature | Category |
|---|---|
| Free contest participation | Basic (expected, post-ban) |
| Watch-alongs/creator content | Performance |
| **Verified non-cash stakes/rewards** | **Attractive** — untested, potentially differentiating versus every other free-to-play pivot in the category |
| Ecosystem cross-promotion (3.0) | Performance, valuable but not itself a retention lever |

---

## 50. Feature Proposal — Dream11 Trophy Room

**What it is:** a compliant, non-cash stakes and reward layer — sponsor-funded prizes, verified leaderboard status — designed to test whether "something to play for" (short of cash) recovers meaningfully more engagement than pure ad-supported free-to-play alone.

**Why now:** the company is running several large, expensive strategic bets (3.0 ecosystem diversification, global expansion) without, as far as public evidence shows, first testing the cheapest and most directly relevant question about its own core product's post-ban viability.

**What it is not:** a workaround to reintroduce real-money mechanics, a claim that the 3.0 strategy is wrong, or a guarantee that non-cash stakes will work — it might not, and that would itself be valuable, cheaply learned information (§54).

**User impact:** users like Rohan (§20) get something to play for again, within legal bounds; users like Simran continue to be served by the existing lightweight free product regardless.

**Business impact:** if successful, strengthens the case for sponsor-funded engagement mechanics as a durable revenue-and-retention model; if unsuccessful, cheaply confirms that reach-based advertising (not stakes) is the right model to double down on, informing capital allocation toward the 3.0 bets with more confidence either way.

**Trade-offs:** requires careful compliance review to ensure no reward is cash-convertible; requires sponsor buy-in for reward inventory; risk of building a mechanic that inadvertently reproduces compulsive-engagement patterns the original ban was partly meant to address (§40).

---

## 51. PRD — Dream11 Trophy Room v1

### 51.1 Problem
No public evidence shows whether Dream11's free-to-play pivot is retaining genuine engagement or coasting on registered-user habit, and no compliant alternative to pure ads has been tested.

### 51.2 Goals
- Pilot with a defined cohort (e.g., a specific city or league segment) across one full cricket season/tournament.
- Establish a baseline Stakes-Mechanic Lift (§32) comparing pilot cohort engagement against a matched control group.
- Confirm zero compliance issues (no cash-convertible reward) across the full pilot.

### 51.3 Non-goals (v1)
Not reintroducing any cash mechanic; not replacing the ads/sponsorship model; not committing to national rollout before pilot data is in.

### 51.4 User stories
- As a user, I can compete for real (non-cash) prizes and see my standing on a leaderboard.
- As a sponsor, I can fund rewards and get visible engagement attribution stronger than passive ad placement.
- As Dream11, I can measure whether this cohort's retention differs meaningfully from the ads-only control group.

### 51.5 Acceptance criteria (Constructs — author-set bars)
- A1: 100% compliance — zero cash-convertible rewards issued, verified by legal review before and during the pilot.
- A2: Statistically meaningful engagement lift over the control cohort (exact threshold set after baseline data, per §53 Phase 0).
- A3: No increase in compulsive-use indicators (e.g., session frequency spikes inconsistent with match schedules) versus the control cohort — a safeguard consistent with §40's design principle.

---

## 52. Wireframes *(ASCII, Constructs)*

```
┌─────────────────────────────────┐
│  Trophy Room                     │
│                                   │
│  Your rank: #142 this week        │
│  Top 3 win: Swiggy vouchers,      │
│  Tata Neu credits, match tickets  │
│                                   │
│  [   View leaderboard   ]         │
└─────────────────────────────────┘
```

---

## 53. Rollout Plan

| Phase | Scope | Gate |
|---|---|---|
| Phase 0 | Baseline: current engagement/retention data for the ads-only free-to-play product, disaggregated enough to define a meaningful control group | If baseline data shows engagement is already strong and stable, the "untested retention risk" framing weakens and this proposal should re-scope |
| Phase 1 | Pilot Trophy Room in one defined cohort/season | §51.5 acceptance criteria |
| Phase 2 | Expand cohort if lift and compliance hold | Lift persists at scale, no compliance issues |
| Phase 3 | National rollout, integrated alongside (not instead of) the 3.0 ecosystem strategy | Net positive impact on both engagement and sponsor value confirmed |

---

## 54. A/B Testing

**Arm A (control):** current ads-only free-to-play, unchanged. **Arm B:** Trophy Room (sponsor-funded non-cash rewards + leaderboard). **Arm C (falsifier, Construct):** leaderboard/status only, with **no** tangible reward at all (pure recognition) — designed to test whether it's the tangible reward or simply the "something to strive for" structure that drives any observed lift. If Arm C performs comparably to Arm B, the sponsor-funded reward inventory (the more operationally complex part of the proposal) may be unnecessary, and a much simpler status-only mechanic would suffice.

---

## 55. KPI Dashboard *(Construct)*

| KPI | Target |
|---|---|
| Stakes-Mechanic Lift (Trophy Room cohort vs. control) | Statistically meaningful improvement |
| Compliance violations | Zero |
| Compulsive-use indicator delta | No meaningful increase vs. control |
| Sponsor-reported engagement value | Directional improvement vs. passive ad placement |

---

## 56. Product Roadmap

`Q1: Phase 0 baseline → Q2: Phase 1 pilot (one cohort/season) → Q3: monitor lift/compliance data → Q4: Phase 2/3 decision gate, integrated into the broader Dream11 3.0 planning cycle`

---

## 57. Risks & Mitigation

| # | Risk | Mitigation |
|---|---|---|
| R1 | Any stakes-adjacent mechanic risks perception of circumventing the spirit of a law passed specifically to address gaming-related harm | Rigorous compliance review (§51.5 A1); explicit design safeguard against compulsive-use patterns (§40, A3) |
| R2 | The unresolved ₹28,000+ Cr GST dispute could materially affect available capital for any new initiative regardless of its own merits | Flagged as an independent, unresolved contingent liability; not something this proposal can mitigate directly |
| R3 | Sponsors may be unwilling to fund a reward pool without proven engagement lift, creating a chicken-and-egg funding problem | Start with a small, low-cost pilot funded from existing sponsorship relationships rather than requiring new sponsor commitments upfront |
| R4 | Users may not distinguish "non-cash reward" from "no reward" psychologically, meaning the whole premise (tested by Arm C) could be wrong | Kill or re-scope to status-only if Arm C outperforms or matches Arm B |

---

## 58. Future Vision

If Trophy Room validates the "stakes matter, cash doesn't have to be the stakes" hypothesis, it could become a standing layer across the entire Dream11 3.0 ecosystem — DreamCricket, FanCode, and DreamSetGo could each plug into a shared, sponsor-funded reward economy, turning what started as a narrow retention experiment into a genuine cross-ecosystem loyalty currency.

---

## 59. PM Lessons

The lesson this case study keeps returning to: when a core mechanic is removed by external force (regulation, platform policy, or otherwise), the instinct to diversify broadly and quickly is understandable — but the cheapest, fastest-to-answer question (does *any* form of stakes recover engagement, short of the one now-illegal form) is often the one skipped in the rush to build several large new things at once.

---

## 60. PM Interview Questions

1. A law makes your core monetisation mechanic illegal overnight. How do you decide what to test first: cheap experiments on the existing product, or new business lines entirely?
2. Design an experiment to distinguish "users are engaging out of habit" from "users are genuinely retained" when your DAU number alone can't tell you.
3. How would you design a reward mechanic that recovers user engagement without recreating the specific harm a new regulation was designed to prevent?

---

## 61. References

- Dream11/Dream Sports FY23–FY25 financials: Entrackr (RoC-sourced filings, Feb 2026), Inc42 Datalabs, The Arc (2026), Wikipedia (historical revenue table)
- PROGA passage and industry-wide pivot coverage: Business Standard, Outlook Business, Outlook Respawn, MediaNama, Forbes India, World Casino Directory, Al Jazeera, Deccan Herald, MarketScreener (Aug–Dec 2025)
- Dream11 GST dispute and Supreme Court context: Inc42 ("Dream11's Gap Year," Jan 2026)
- Dream Sports post-ban restructuring: CB Insights (Mar 2026)
- Dream11 company history and sponsorship deals: Wikipedia, 1947 Tech newsletter (historical funding round coverage)

---

## 62. About the Author

Written by Gaurav Singh as part of a 90-day product management case study series, applying a consistent research-led teardown methodology across Indian and global consumer products.

---

## 63. License

This document is an independent analysis for educational purposes. It is not affiliated with, endorsed by, or reviewed by Dream11 / Dream Sports. All company names and trademarks belong to their respective owners.

---

## 64. Self Review

| Check | Status | Note |
|---|---|---|
| No fabricated data | ✅ | Every figure sourced or explicitly derived; constructed content in Appendix C |
| Facts separated from assumptions | ✅ | ASSUMPTIONS.md |
| Conflicts disclosed | ✅ | Appendix A |
| Falsification designed | ✅ | §53 Phase 0, §54 Arm C |
| Recommendation shown against a prioritisation framework rather than engineered to win | ✅ | §47 — Trophy Room does not top stressed RICE |

**Where this case study is weakest.** No FY26 financial disclosure was found publicly available as of the date of analysis, meaning the actual financial impact of the ban — as opposed to the pre-ban FY25 loss this document is careful to distinguish — is not yet directly evidenced here; the ~95%/100% figures are drawn from a single CEO statement, not an audited breakdown. Second, the pre-ban (~50M peak DAU) versus post-ban (10M DAU) comparison in §13.4 mixes a seasonal peak with a point-in-time figure and should not be read as a precise "user loss" calculation. Third, this entire proposal assumes users' disengagement (if it exists — not independently confirmed) is specifically about the *absence of stakes* rather than, say, reduced marketing spend, lost habit-forming payment flows, or simply reduced app-store prominence post-sponsorship-loss — alternative explanations this document cannot rule out from public data alone.

**What would change my mind.** Dream11 publicly disclosing FY26 results showing the free-to-play pivot is retaining strong, comparable engagement without any stakes mechanic; a Phase 0 baseline (§53) showing current engagement is already healthy; or Arm C (§54) showing status alone, without tangible rewards, performs just as well — in which case the more complex sponsor-funded reward system in this proposal would be unnecessary.

---

## 65. Appendix

### Appendix A — Source Conflicts

| # | Conflict | Resolution |
|---|---|---|
| A-1 | FY24 revenue: ₹7,934 Cr (Entrackr, RoC-sourced) vs ₹8,345.9 Cr (Inc42 Datalabs) | Both cited; likely different reporting bases (operating revenue vs. total income), not independently reconciled here |
| A-2 | FY25 "revenue": ₹6,759 Cr (Entrackr, explicitly "revenue from operations") vs ₹7,374.4 Cr (Inc42, labelled "revenue" but numerically matching Entrackr's separately reported "total income" figure) | Distinguished explicitly throughout this document as operating revenue vs. total income |
| A-3 | Pre-ban peak DAU (~50M, IPL season) vs. post-ban DAU (10M, Sep 2025) | Explicitly flagged as not a clean like-for-like comparison — different measurement windows (seasonal peak vs. point-in-time), not treated as a precise "80% engagement loss" calculation anywhere in this document |
| A-4 | GST demand figure: "north of ₹28,000 Cr" (Inc42) — no more precise figure found across other sources reviewed | Carried as a directional figure only |

### Appendix B — Evidence Grades

| Grade | Meaning | Applied to |
|---|---|---|
| 🟢 High | RoC-sourced filings, direct company statements | FY23/FY25 revenue and loss figures, PROGA passage date, sponsorship loss |
| 🟡 Medium | Trade press citing filings or company statements, consistent across sources | FY24 figures, post-ban pivot timeline, GST overhang |
| 🟠 Low | Single-source figures (a CEO statement, a single DAU report) | The ~95%/100% revenue-and-profit figure, 10M DAU figure |
| 🔴 Conflicting | Sources materially disagree | FY24 revenue figure precision (Appendix A-1) |

### Appendix C — Author-Constructed Content

| # | Construct | Where |
|---|---|---|
| C1 | Dream11 Trophy Room — the entire proposal | §50 |
| C2 | Stakes-Adjusted Engagement Rate (North Star) | §31 |
| C3 | Pre-Ban vs. Post-Ban Retention Cohort, Stakes-Mechanic Lift, Advertiser Value Realisation | §32 |
| C4 | Personas Rohan, Simran, and the illustrative marketing-lead persona | §20 |
| C5 | All RICE inputs and the stress rule | §47 |
| C6 | Acceptance-criteria bars | §51.5 |
| C7 | The three-arm A/B design, including Arm C as falsifier | §54 |
| C8 | Technical architecture and data-flow reconstructions | §41, §42 |
| C9 | The framing of the FY25 loss as structurally separate from the (not-yet-passed) ban's financial impact | §5, §13.2 |

### Appendix D — Asset Status

| Asset | Status |
|---|---|
| ASCII wireframes | ✅ Authored (§52) |
| Product screenshots | ❌ Not included — no authenticated session was used |
| UI/accessibility audit | ❌ Not independently tested — flagged as a research-boundary gap |

---

*Day 54 of 90 · ← [Day 53 — PhysicsWallah](../Day-53-PhysicsWallah) · Day 55 →*
