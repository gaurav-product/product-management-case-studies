# Day 65 — Vodafone Idea: The Company That Counts What It Cannot Reach

> Vodafone Idea's June 2026 quarter was reported as a turnaround, and parts of it are: EBITDA crossed ₹5,000 Cr, revenue grew 6.04%, and the company announced its first net subscriber addition since the 2018 merger. But in that same quarter its **active** subscriber base fell 2.30 million while its connection count rose 0.30 million — **7.67 active users lost for every connection gained**. TRAI puts 16.02% of Vi's connections outside the network on the peak activity date, against 0.73% at Airtel and 0.93% at Jio. Every metric Vi led with — subscribers, market share, ARPU — is a count or a ratio computed over a base of which one in six is not there. The company is not primarily losing a contest for customers. It has become India's **second** SIM, and a second SIM is a different product with a lower ceiling, a costless exit, and — on Vodafone's own evidence filed with the regulator — a 90% chance of never coming back once it has been quiet for sixty days.

---

## 1. Cover

**Product:** Vi (Vodafone Idea) — mobile network, prepaid and postpaid, 2G/4G/5G
**Legal entity:** Vodafone Idea Limited · **CIN:** L32100GJ1996PLC030976
**Domain:** Telecommunications — the first telecom case study in this series
**Period examined:** Q1 FY27 (quarter ended 30 June 2026), reported 10 August 2026
**Written:** 31 August 2026 — eight years to the day since the entity was renamed Vodafone Idea Limited
**Author:** Gaurav Singh · Day 65 of 90

---

## 2. Repository Metadata

| Field | Value |
|---|---|
| Legal entity | Vodafone Idea Limited |
| CIN | L32100GJ1996PLC030976 |
| Incorporated | 14 March 1995, as **Birla Communications Limited** |
| Registrar | RoC Ahmedabad |
| Renamed | Vodafone Idea Limited, fresh certificate of incorporation **31 August 2018** |
| Registered office | Suman Tower, Plot No. 18, Sector 11, Gandhinagar 382011, Gujarat |
| Corporate office | Birla Centurion, 10th Floor, Century Mills Compound, Pandurang Budhkar Marg, Worli, Mumbai 400030 |
| Listings | BSE **532822** · NSE **IDEA** |
| NIC code | **3210 — "Manufacture of electronic valves and tubes and other electronic components"** |
| CEO | Abhijit Kishore (from 19 Aug 2025, three-year term to 18 Aug 2028) |
| Non-executive Chairman | Kumar Mangalam Birla (returned May 2026) |
| Largest shareholder | Government of India, **48.99%** |

Two details there are worth a sentence each. The **CIN embeds 1996 while the registry records incorporation on 14 March 1995** — logged as a conflict rather than silently reconciled (Appendix A-1). And India's industrial classification files the country's third-largest telecom operator under the manufacture of vacuum tubes, an artefact of a 1995 registration nobody has updated in thirty-one years. This is the third consecutive case study in this series whose NIC code does not describe the business.

---

## 3. Badges

`Day 65/90` · `Telecom` · `Listed (BSE/NSE)` · `Q1 FY27 primary` · `Regulator-published counter-evidence` · `139 programmatic checks, all passing` · `Zero fabricated figures`

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

On 10 August 2026 Vodafone Idea reported the quarter ended 30 June 2026. Revenue from operations was ₹11,689 Cr, up 6.04% year on year. EBITDA was ₹5,034 Cr, up 9.15%, at a computed 43.07% margin. Net loss narrowed from ₹6,608 Cr to ₹3,754 Cr. Customer ARPU rose 10.2% to ₹195. And the company led with a milestone: **its first quarter of positive net subscriber addition since the Vodafone–Idea merger.**

The network investment behind some of that is real and should be credited before anything is criticised. Vi added more than 15,600 unique broadband towers in twelve months to reach roughly 205,000; 4G population coverage reached 87%; 5G is live in more than 200 cities across 17 circles; data traffic grew 27.9% to 88.4 petabytes per day. CRISIL and ICRA both upgraded the company to A- (Stable) during the period. These are not accounting artefacts.

But three things sit underneath the print. First, **₹1,611 Cr of net exceptional gain supplied 56.45% of the entire loss narrowing**; excluding exceptionals and tax the loss improved 18.95%, not 43.19% — the headline narrowing is **2.28×** the underlying one. Second, the subscriber milestone dissolves on inspection: the connection count rose 0.30 mn while the **active** base fell from 169.3 mn to 167.0 mn. Third, and most consequential for a product manager, TRAI's Visitor Location Register data shows **83.98% of Vi's connections were active on the peak date in June 2026, against 99.27% at Airtel and 99.07% at Jio.**

That last figure is the case study, because the regulator publishes it rather than the company, and because it makes the convenient explanations testable. Vi carries **31.85 million connections that did not register on the network** — **3.86×** Airtel's and Jio's inactive pools *combined*, on a base 20.08% of their size. It is not machine-to-machine SIMs: Airtel carries 1.56× Vi's M2M intensity and still runs 99.27%. It is not the regulator: the same 90-day non-usage rules bind all three operators.

What it is, this case study argues, is a **product-position** finding. Vi has become the number Indians keep rather than the number they use — the secondary SIM retained because a bank, an Aadhaar record or a WhatsApp account is attached to it. That position explains the low ARPU, the low VLR ratio, the low data intensity and the ability to add connections while losing users, all at once. It also caps the business, because a secondary SIM's exit costs nothing: the user does not port out, they simply stop recharging, and no system anywhere records the decision.

The proposal, *Vi Anchor*, follows from that diagnosis rather than from the financials. It is examined, costed — and then, correctly, ranked last.

---

## 6. Product Overview

Vi is a mobile network operator serving 22 telecom circles with 2G, 4G and 5G access, sold prepaid and postpaid, alongside an enterprise arm (Vi Business) covering connectivity, IoT and managed services. The consumer product is functionally a commodity — voice, data, SMS and a bundle of OTT entitlements attached to price points — differentiated mainly by coverage, speed and price.

The distinguishing product fact for this analysis is structural rather than featural: Vi holds 5G spectrum in 17 circles and mmWave in 16, and launched 5G only in 2025, roughly three years after Jio and Airtel. It arrives into every category as the third mover with the smallest capital base.

---

## 7. Company Background

Vodafone Idea Limited was incorporated on 14 March 1995 as Birla Communications Limited, became Idea Cellular, and merged with Vodafone India in 2018, taking its present name on 31 August 2018. The merged entity was, at formation, India's largest mobile operator; it has lost subscribers in almost every month since.

The shareholding is now the most unusual feature of the business. Following the conversion of ₹36,950 Cr of deferred spectrum and interest liabilities into equity in March 2025, **the Government of India holds 48.99% and is the largest shareholder**, alongside Vodafone Group and the Aditya Birla Group as promoters. Kumar Mangalam Birla, who stepped down as chairman in August 2021, rejoined the board in 2023 and returned as non-executive chairman in May 2026.

Leadership turned over in August 2025: Abhijit Kishore, previously Chief Operating Officer and before that Chief Enterprise Business Officer, succeeded Akshaya Moondra as CEO for a three-year term running to 18 August 2028. Kishore has been with the company since March 2015. His predecessor's three years saw the subscriber base fall by roughly 37 million.

---

## 8. Product Timeline

| Date | Event |
|---|---|
| 14 Mar 1995 | Incorporated as Birla Communications Limited |
| Aug 2018 | Vodafone India–Idea Cellular merger completes; renamed 31 Aug 2018 |
| 2019 | Supreme Court AGR judgment; liabilities crystallise |
| Aug 2021 | Kumar Mangalam Birla steps down as chairman |
| Mar 2025 | ₹36,950 Cr of dues converted to equity; Government reaches 48.99% |
| Aug 2025 | Abhijit Kishore becomes CEO |
| Oct 2025 | Supreme Court permits DoT to reconsider a ₹9,450 Cr additional AGR demand |
| Jan 2026 | Ten-year AGR moratorium; DoT reassessment; reported relief ~₹54,200 Cr 🟡 |
| Feb 2026 | First net subscriber addition month since merger (+21,927) |
| Mar–Jun 2026 | Four further months of net additions; the VLR ratio falls across them |
| May 2026 | CRISIL upgrade to A- (Stable); Birla returns as chairman; Bombay HC quashes a ₹2,113 Cr OTSC demand |
| Jun 2026 | ICRA upgrade to A- (Stable) |
| 10 Aug 2026 | Q1 FY27 results: "first subscriber addition since merger" |

---

## 9. Vision & Mission

Vi's stated framing for FY27, in the CEO's words on the results call, is that this is "the year of execution" — the argument being that the financial overhang has been resolved and the remaining task is network and competitiveness. The company points to a planned ₹45,000 Cr capital programme over FY27–FY29 as the expression of that.

The gap this case study examines is that execution is being measured with instruments that cannot detect the failure mode. A company whose stated goal is winning customers back is reporting progress in a unit — connections — that can rise while customers leave.

---

## 10. Problem Statement

**For Vi:** the company cannot distinguish, from the metrics it publishes and leads with, between acquiring a customer and acquiring a connection. In Q1 FY27 it did more of the second than the first, and reported the result as the first.

**For the user:** a Vi subscriber who has made Jio or Airtel their primary line faces a charge of roughly ₹199 a month to keep alive a number they use only to receive OTPs and incoming calls. No product is priced for that job, so the rational choice is to let the SIM lapse — eventually losing a number that a bank, an insurer and a UPI handle are all keyed to.

**The intersection:** Vi holds 31.85 million connections in exactly this state. It cannot monetise them, cannot report them honestly, and — under DoT's VLR-based number-series allocation rules — cannot fully reuse the numbering capacity they occupy.

---

## 11. Market Research

India had 1,282.38 million wireless (mobile) subscribers at the end of June 2026, of which 1,201.06 million — **93.66%** — were active on the peak VLR date. The market is a three-private-operator structure with a state incumbent: Jio 39.27% of connections, Airtel 37.96%, Vi 15.50%, BSNL and MTNL the remainder.

Measured on *active* users the ranking is the same but the distances are not: Jio 41.54%, Airtel 40.23%, **Vi 13.90%**. Vi's connection share overstates its active share by 1.60 percentage points, or **11.53% in relative terms**; Airtel's and Jio's active shares each *exceed* their connection shares by 2.27 points. The market-share number the industry quotes flatters exactly one of the three players.

---

## 12. Industry Analysis

Indian mobile is a capital-intensive oligopoly in which pricing power has returned — tariff increases through 2024–2026 lifted ARPU across all operators — but where the capital required to compete has risen faster than the cash any operator except Jio and Airtel generates. Vi's Q1 FY27 capex was ₹1,930 Cr, 16.51% of its own revenue; Airtel's India revenue alone was **3.53× Vi's total revenue** and its India EBITDA **4.92× Vi's total EBITDA**, at a 60.13% margin against Vi's 43.07% — a gap of 17.06 percentage points.

Two structural features matter for the argument that follows. Numbering capacity is allocated by DoT on a **VLR basis** rather than an HLR basis, a change made in July 2011, so an operator's inactive connections directly constrain its ability to acquire. And the regulatory floor on disconnection — no deactivation for non-usage inside 90 days, none at all while ₹20 of balance remains — applies identically to all three private operators, which is why it cannot explain why one of them sits at 83.98% and the other two above 99%.

---

## 13. TAM / SAM / SOM

*Framework note: run in restricted form. No primary-sourced Indian mobile market-size figure was located that is not a vendor estimate, so this is sized from disclosed subscriber counts only, and expressed in connections rather than rupees.*

| Layer | Definition | Size | Basis |
|---|---|---|---|
| TAM | All active Indian wireless users | **1,201.06 mn** | TRAI, peak VLR, Jun 2026 🟢 |
| SAM | Vi's own connection base | **198.82 mn** | TRAI, Jun 2026 🟢 |
| SOM | Vi connections actually active | **166.97 mn** | TRAI base × 83.98% 🟢 |
| *The gap* | Vi connections held but not active | **31.85 mn** | Derived, D2a |

The unusual feature is that SAM minus SOM is not a growth opportunity in the normal sense — it is Vi's existing property, already acquired and already paid for. Applying the stress discount developed in §47, only **3.19 mn** of it is realistically addressable.

---

## 14. Competitor Analysis

*Framework note: restricted to operators that file. Bharti Airtel is listed and reports quarterly. Reliance Jio reports through RIL, and Jio Platforms filed its DRHP with SEBI during the quarter under examination. BSNL is state-owned and does not publish comparable quarterly ARPU or segment data; it is named here rather than estimated.*

| Metric, Q1 FY27 / Jun 2026 | Vi | Bharti Airtel | Reliance Jio |
|---|---|---|---|
| Connections (TRAI) | 198.82 mn | 486.80 mn | 503.58 mn |
| Active on peak VLR | 166.97 mn | 483.23 mn | 498.89 mn |
| **VLR ratio** | **83.98%** | **99.27%** | **99.07%** |
| Inactive connections | **31.85 mn** | 3.57 mn | 4.69 mn |
| ARPU (reported) | ₹195 | ₹264 | ₹215.6 |
| ARPU per *active* subscriber | ₹225.47 | ₹265.95 | — |
| Data per user, monthly | 21.7 GB | 34.4 GB | 43.7 GB |
| 5G FWA subscribers | not reported | 3.82 mn | 9.11 mn |
| M2M as % of own base | 10.87% | 17.00% | 5.12% |

Three readings follow. **Vi's inactive pool exceeds Airtel's and Jio's combined by 3.86×**, on a base 20.08% of theirs; its inactive *share* is **21.84×** Airtel's and **17.20×** Jio's.

**The M2M explanation dies here.** Airtel carries 1.56× Vi's M2M intensity and still registers 99.27% of its base — and even crediting every one of Vi's 21.62 mn M2M connections as non-registering, the unexplained residual of 10.23 mn is *still* 1.24× Airtel and Jio's total inactive pools.

And the number that cuts against this case study's own argument, included because it should be: restating both operators' ARPU per *active* subscriber, Vi earns ₹225.47 against Airtel's ₹265.95. The headline deficit of 26.14% falls to 15.22% — meaning **41.77% of Vi's apparent ARPU gap to Airtel is a denominator effect, not a pricing or product failure.** Vi's real customers pay considerably closer to Airtel's than the print suggests. That is genuinely good news for Vi, and it is the strongest argument for fixing the base rather than the tariff.

*Caveat on the data row: the denominators differ. Vi's 21.7 GB is per 4G/5G subscriber, Airtel's 34.4 GB per customer, Jio's 43.7 GB per capita. Vi's is measured on the narrowest and therefore most flattering base of the three, so the true engagement gap is wider than the table shows, not narrower.*

Vi is also absent from the fastest-growing new access category: Jio and Airtel hold **99.92%** of India's 12.94 mn 5G fixed-wireless subscribers between them.

---

## 15. SWOT

| | |
|---|---|
| **Strengths** — 5G spectrum in 17 circles, mmWave in 16; ~205,000 broadband towers with 15,600 added in a year; 87% 4G population coverage; ARPU per active subscriber within 15.22% of Airtel's; enterprise assets including a 1.3 Tbps data-centre corridor and a live network-verification partnership with Meta | **Weaknesses** — 16.02% of connections inactive; data per user 63.08% of Airtel's and 49.66% of Jio's on a more flattering base; EBITDA margin 17.06 points below Airtel India; capex 16.51% of revenue against rivals investing multiples more in absolute terms; no FWA presence |
| **Opportunities** — 31.85 mn dormant connections already owned; 63.0 mn non-4G/5G connections (32.63% of base) available to upgrade; enterprise IoT including a stated 12 mn smart-meter programme; government shareholding aligning policy interest with survival | **Threats** — deferred obligations of ₹156,058 Cr, 7.75× annualised EBITDA; D&A plus finance cost at 90.57% of revenue; VLR-based numbering allocation penalising the inactive base; competitors who grew active users in the same months Vi lost them |

---

## 16. Porter's Five Forces — run twice

*Framework note: run as a double pass on the two positions Vi actually occupies — the **primary** connection in a household and the **secondary** one. This seam is chosen because the same company, network and tariff sheet face genuinely inverted forces depending on which slot the SIM occupies, and because the inversion explains the VLR gap that no single-pass analysis does.*

| Force | Vi as the PRIMARY SIM | Vi as the SECONDARY SIM |
|---|---|---|
| **Rivalry** | Brutal and symmetric — Jio and Airtel compete on coverage, speed and bundles, and both outspend Vi | Almost none. Nobody markets against a SIM that sits in a drawer; the competitor is disuse |
| **Buyer power** | Moderate. Porting costs the user time and the re-linking of bank and Aadhaar records | **Near-total.** Exit requires no port, no call, no form — the user simply stops recharging, at zero cost and with no record created |
| **Substitutes** | Other networks; OTT calling erodes voice value | **Nothing at all.** The substitute for a secondary SIM is not having one, which is free |
| **New entrants** | Effectively barred by spectrum and capital | Irrelevant — the slot is being vacated, not contested |
| **Supplier power** | High — spectrum is priced by the state, which is also the largest shareholder and largest creditor | High but immaterial; a dormant connection consumes numbering capacity, not network capacity |

The inversion is the finding. On the primary line Vi is losing a fair fight it is underfunded for. On the secondary line **there is no fight**: buyer power is absolute, exit is frictionless and invisible, and the only force acting is decay. Vi's headline strategy — network investment — addresses the first column. Its 31.85 mn inactive connections live entirely in the second, where a better network changes nothing, because the phone the SIM is in is switched off.

---

## 17. Business Model Canvas

| Block | Vi |
|---|---|
| Value proposition | Nationwide voice and data at a price point below Airtel's |
| Customer segments | Prepaid consumers (majority), postpaid (31.9 mn), enterprise, IoT/M2M (21.62 mn) |
| Channels | Retail distribution, Vi app, digital recharge, enterprise direct sales |
| Revenue streams | Prepaid recharges, postpaid rentals, enterprise contracts, IoT connectivity |
| Key resources | Spectrum across 22 circles, ~205,000 towers, the numbering series itself |
| Key activities | Network build, spectrum management, distribution, collections |
| Key partners | Meta (network verification), Spotify, PhysicsWallah, tower and equipment vendors |
| Cost structure | D&A ₹5,467 Cr, finance cost ₹5,120 Cr, network and IT ₹2,344 Cr, roaming and access ₹1,334 Cr |
| Government | Largest shareholder (48.99%), largest creditor (₹156,058 Cr deferred), and the regulator |

The last row is the anomaly. The same counterparty owns half the equity, holds the deferred liabilities, sets the spectrum price and — through TRAI — publishes the VLR figure that contradicts the company's subscriber narrative.

---

## 18. Revenue Model

Revenue from operations of ₹11,689 Cr in Q1 FY27 is overwhelmingly core service revenue — ₹11,662 Cr, or **99.77%**. Customer ARPU of ₹195 applied to the reported 193.1 mn base for three months implies ₹11,296.35 Cr of mobile service revenue, leaving ₹392.65 Cr — **3.36% of revenue** — for everything else, which is a reasonable internal consistency check and a small enterprise contribution for a company describing enterprise as a growth pillar.

The model's problem is not the top line but what sits under it: **D&A plus finance cost together are ₹10,587 Cr, or 90.57% of revenue and 2.10× EBITDA.** Vi can grow service revenue at 6% indefinitely without reaching profit, because the capital structure consumes more than nine rupees in ten before a single operating cost is counted.

---

## 19. Target Users

Vi's addressable user is the price-conscious Indian mobile subscriber, weighted toward circles where the legacy Vodafone and Idea brands retained distribution — Gujarat, Maharashtra, Kerala, Delhi, UP East. The company reported June 2026 additions across nine circles including these.

The user this case study is concerned with is narrower and unnamed in any Vi disclosure: the person who holds a Vi number but uses another network. There are, on TRAI's arithmetic, about 31.85 million of them, and Vi's product organisation has no artefact addressed to them.

---

## 20. Personas

**Rajesh, 34, Ahmedabad, delivery fleet supervisor.** Primary line is Jio; his Vi number from 2016 is on his bank records, his LIC policy and his Aadhaar. He recharges Vi roughly twice a year, when a bank OTP fails, at ₹199 a time. He is VLR-inactive most months and appears in Vi's subscriber count every month.

**Sunita, 41, Kanpur, schoolteacher.** Single Vi SIM, 4G handset, recharges ₹299 monthly. She is the customer the ₹225.47 active ARPU describes, and the reason Vi's activity-adjusted economics are better than the headline implies.

**Vi Business account manager, Pune.** Sells connectivity, IoT and managed services; carries the smart-metering pipeline. Compensated on contracted connections — a unit that does not distinguish a meter SIM from a person.

---

## 21. Jobs To Be Done

*Framework note: JTBD is used here specifically because the dormant base has a job that Vi's product catalogue does not name.*

| Job | Who | Current solution | Adequacy |
|---|---|---|---|
| "Get me online cheaply and reliably" | Primary-line user | Vi prepaid packs from ~₹199 | Adequate but outgunned on network |
| "Keep my number alive so my bank can reach me" | Dormant-base holder | Minimum recharge ~₹199/month, or lapse | **Badly served** — the price of existing is set by the price of consuming |
| "Connect a machine and bill me per SIM" | Enterprise / utility | Vi Business IoT | Adequate |
| "Prove this number belongs to this person" | Bank, platform, insurer | Vi–Meta silent mobile verification, live Q1 FY27 | **New, and the relevant precedent** |

The mismatch is in row two. India priced the number and the service as one bundle; the OTP economy then made the number itself a piece of identity infrastructure with value entirely independent of consumption. A user who wants only the second is charged for both, and 31.85 million of them have concluded that is not worth ₹199 a month.

---

## 22. User Journey

The dormant-base journey has an unusual property: it contains no decision point. A user does not choose to leave Vi; they choose, once, to make another SIM primary, and then a series of non-events follows — a pack expires, a month passes, another passes.

| Stage | What happens | What Vi records |
|---|---|---|
| Dual-SIM | User adds Jio or Airtel as a second line | A retained subscriber |
| Inversion | Data and calls migrate to the new line | ARPU declines slightly |
| Lapse | Pack expires, no recharge | Still a subscriber; now VLR-inactive |
| Drift | Months pass; occasional OTP recharge | Subscriber; intermittently active |
| Silence | 90 days, then disconnection | A subscriber loss, dated long after the actual loss |

The gap between "Inversion" and "Silence" can run for years, and Vi's reported subscriber number treats the whole of it as retention.

---

## 23. User Flow

A dormant user's entire interaction is: OTP fails → realise the SIM is dead → find the handset → recharge ₹199 → wait for reactivation → receive the OTP. Six steps to solve a problem the user did not know they had until a bank transaction failed.

Vi's app supports none of this well for a user who has not opened it in eight months and whose number is no longer receiving the login OTP the app itself requires.

---

## 24. Information Architecture

The Vi app is organised around consumption — recharge, usage, plans, entitlements — with account and profile secondary. That is correct for the primary-line user and structurally wrong for the dormant one, whose relationship to Vi is custodial rather than consumptive.

Nothing in the hierarchy exposes the two facts a dormant holder actually needs: how long until the number is deactivated, and what the minimum is to prevent it.

---

## 25. UX Audit

The single largest UX failure is a circular dependency: the account most at risk of loss is the one that cannot be recovered, because recovery is gated on an OTP sent to the number that has lapsed. Vi is not unique in this, but Vi has roughly six times more users exposed to it than either rival.

Second, the deactivation countdown — the most consequential state a dormant connection has — is communicated by SMS to a handset that is switched off, and nowhere else. TRAI requires a minimum of three SMS between the 31st day of non-usage and the deactivation date; on a powered-down device, all three are notifications into a void.

---

## 26. UI Audit

Vi's consumer surfaces are competent and unremarkable — the recharge flow, plan grid and entitlement cards are at parity with Airtel's and Jio's. There is no visible design deficit driving the VLR gap.

Worth naming explicitly because it constrains any proposal: **the UI is not the problem here, so no UI change will fix it.** The dormant user does not open the app.

---

## 27. Accessibility

Vi serves a base skewed to 2G and feature phones — **63.0 mn connections, 32.63% of the reported base, are not on 4G or 5G** — which means a meaningful share of users cannot be reached through an app at all. Any intervention that assumes a smartphone excludes a third of the customer base by construction.

Regional-language SMS and IVR remain the practical accessibility surface for that third, and both are cheaper than app work.

---

## 28. Feature Breakdown

| Area | Current state |
|---|---|
| Prepaid packs | Full ladder from ~₹199 to annual plans; service-validity extension packs exist |
| Postpaid | 31.9 mn base, up from 30.1 mn QoQ — the one segment growing cleanly |
| 5G | 200+ cities, 17 circles; no FWA offering |
| OTT bundles | Spotify (postpaid), SonyLIV, Disney+ Hotstar on selected packs |
| Education | Vi edu+ with PhysicsWallah, UP and Rajasthan |
| Enterprise | Vi Business, 1.3 Tbps data-centre corridor, 12 mn smart-meter programme stated |
| Security | Vi Protect; ~2 billion suspected spam calls identified |
| **Network verification** | **Silent mobile verification with Meta across WhatsApp, Facebook and Instagram — launched in the quarter examined** |

That last row is the asset the proposal is built on, and it is worth stating plainly what it demonstrates: **Vi has already sold the fact that a number is live and belongs to a person, to a third party, as a product.** It did so for the first time in Q1 FY27.

---

## 29. AI Capabilities

Vi's disclosed AI work is concentrated in network operations and fraud: the SPARC cyber-resilience platform was upgraded with AI-led early detection during the quarter, and Vi Protect applies detection to spam and suspected fraud calls at scale.

No consumer-facing AI product of consequence has been disclosed, and none is proposed here — the failure this case study identifies is a metrics and pricing failure, and applying a model to it would be decoration.

---

## 30. Product Metrics

| Metric | Q1 FY27 | Comparator |
|---|---|---|
| Reported subscribers | 193.1 mn (company) / 198.82 mn (TRAI) | — |
| **Active (VLR)** | **166.97 mn** | Airtel 483.23 mn, Jio 498.89 mn |
| **VLR ratio** | **83.98%** | Airtel 99.27%, Jio 99.07% |
| Customer ARPU | ₹195 | Airtel ₹264, Jio ₹215.6 |
| Blended ARPU | ₹177 | — |
| ARPU per active subscriber | ₹225.47 | Airtel ₹265.95 |
| 4G/5G subscribers | 130.1 mn (67.4% of base) | — |
| Data per 4G/5G subscriber | 21.7 GB/month | Airtel 34.4, Jio 43.7 |
| EBITDA margin | 43.07% | Airtel India 60.13% |

**Vi publishes two ARPUs that differ by 10.17%** — customer ARPU ₹195 and blended ARPU ₹177 — and the coverage of the quarter used the higher one. If the blended figure is computed on the reported base, the implied "customer" base is 175.28 mn, leaving 17.82 mn connections that earn revenue but are not counted as customers, against a disclosed M2M base of 21.62 mn. The two do not reconcile exactly and are not forced to (Appendix A-3).

---

## 31. North Star Metric

Vi's implied north star is the subscriber count, and Q1 FY27 is the demonstration of why that is the wrong choice: it rose while the business shrank.

**Proposed North Star — AVC/1k: Anchor-Verified Connections per 1,000 dormant connections held.**

A connection counts in the numerator only if **all four** hold in the period:
1. it registered on the network on the peak VLR date;
2. verification revenue was received against it from an enterprise counterparty;
3. the subscriber gave, and had not withdrawn, explicit consent under the DPDP framework;
4. it was not reactivated by a Vi-funded promotional recharge.

**The denominator is the design choice.** It is *dormant connections held* — so acquiring more connections that go dormant, or delaying the release of dead ones, **lowers** the metric. A company cannot improve AVC/1k by growing the thing this case study says it is wrongly growing.

**Guardrail — SSR-90: Subscriber Suspension Rate at the 90th percentile of verification intensity.** In the decile of numbers most heavily queried by enterprise counterparties, the rate at which subscribers withdraw consent or ask to be removed, measured over a rolling three-quarter window and reported **by circle rather than in aggregate**, so a good metro result cannot mask a bad rural one. Owned by a function with no enterprise revenue target. A breach triggers automatic suspension of verification on the affected cohort — release is the default, not a decision someone must argue for.

---

## 32. Product Analytics

Vi holds, and does not appear to publish, the one dataset that would settle the diagnosis: per-connection VLR registration history joined to recharge history. That would separate a genuinely departed user from a dormant-but-attached one, which is the distinction the whole strategy turns on.

The absence of any such segmentation in disclosure is itself evidence — the company reports connections and ARPU, not activity cohorts.

---

## 33. AARRR

*Framework note: applied to the dormant base rather than to the whole business, because the funnel's shape there is the anomaly.*

| Stage | Reading |
|---|---|
| Acquisition | Working — five consecutive months of net additions, Feb–Jun 2026, **+463,129** |
| Activation | **Failing** — the VLR ratio fell across the same five months, 85.24% → 83.98% |
| Retention | Ambiguous by construction; a dormant connection is retained and lost simultaneously |
| Revenue | ₹195 headline, ₹225.47 per active user, ₹0 across 31.85 mn connections |
| Referral | Not material |

The finding is that **the streak and the deterioration are the same five months.** Over Feb–Jun 2026 Vi's connection base rose 0.44 mn while its active base fell 2.13 mn — **4.83 active users lost per connection added.** Jio's VLR ratio moved the other way over the same window, up 0.78 points.

---

## 34. HEART

| Dimension | Vi |
|---|---|
| Happiness | Not disclosed; no NPS or CSAT published |
| Engagement | 21.7 GB per 4G/5G subscriber, up 25.2% — real improvement, still 63.08% of Airtel's on a more flattering base |
| Adoption | 4G/5G mix 64.4% → 67.4%; postpaid 30.1 → 31.9 mn |
| Retention | Connection retention positive; **active retention negative** |
| Task success | Not disclosed |

HEART is included mainly to show what is missing: four of five rows have no published figure or a contradictory one, which is why this analysis leans on the regulator's data rather than the company's.

---

## 35. Growth Strategy

Vi's stated growth strategy is network-led: ₹45,000 Cr of capex across FY27–FY29, of which ₹25,000 Cr is expected from bank borrowing and ₹10,000 Cr from non-funded facilities, aimed at 4G densification and 5G expansion. Q1 FY27 capex of ₹1,930 Cr annualises to roughly ₹7,720 Cr against a plan averaging ₹15,000 Cr a year.

**Checking whether the proposal already exists, from Vi's own published terms.** Vi does sell service-validity extension packs — its own site describes them as minimum-recharge options to extend validity and maintain incoming calls. So a low-cost number-retention product exists. What does not exist anywhere in Vi's catalogue is a retention product **paid for by someone other than the subscriber.** Every current option asks the dormant user — the person who has already decided the number is not worth ₹199 a month — to pay. That distinction is the whole of the proposal, and it survives the check.

There is a further irony in the record. In its own submission to TRAI's consultation on deactivation for non-usage, Vodafone proposed exactly a number-retention facility, "through specific recharge(s) with an option of retaining for either 6 months or 12 months," with charges left to market forces. The company designed the subscriber-pays version of this more than a decade ago. It is now carrying 31.85 million people who will not buy it.

---

## 36. Growth Loops

Vi's intended loop is: capex → coverage → subscriber additions → revenue → capex. The loop is currently broken at the second arrow, because additions are arriving as connections rather than as active users, and connections do not generate revenue.

There is also an adverse loop specific to the dormant base, and it is documented in a primary source. DoT's July 2011 guidelines changed number-series allocation from an HLR basis to a **VLR basis** — Vodafone's own filing to TRAI states this and adds that "any unused MSISDN makes an impact on our capabilities in new acquisitions." Holding 31.85 mn inactive connections therefore constrains the numbering capacity available for acquiring new ones. **The ghost base is not merely uncounted; it is actively taxing the acquisition it flatters.**

---

## 37. Network Effects

Mobile access has weak direct network effects in a market with full interconnection — a Vi user calls a Jio user at no penalty — so Vi's subscriber scale confers little defensive value.

The one genuine effect runs through identity rather than calling: the more institutions key their records to a number, the higher the cost of losing it. That effect is strong, it is the reason the dormant base exists at all, and Vi currently captures none of its value.
---

## 38. Product Strategy

Vi's strategy is coherent for the company it is trying to be — a credible third network — and mis-specified for the company it currently is. Network investment competes for the primary line, which is the right long-run fight and the one Vi is underfunded for; nothing in the disclosed strategy addresses the 31.85 mn connections sitting in the secondary slot, where a faster network is invisible because the handset is off.

The strategic error is not the capex. It is that the **measurement system cannot tell the two populations apart**, so capital allocated to winning primary lines is judged by a metric that a secondary-line addition also moves. A company that cannot distinguish its two customer populations will keep buying the cheaper one by accident.

---

## 39. Monetization

Vi monetises consumption: a recharge buys validity plus an allowance. The floor for participating at all has risen to roughly ₹199 a month at the private operators, which is the price of the cheapest bundle rather than the price of the underlying service the dormant user wants.

The consequence is a monetisation hole exactly the shape of the dormant base. A user who values only reachability is offered only consumption, declines, and generates ₹0 — while still occupying a number, a row in the subscriber count, and a slice of DoT-allocated numbering capacity. **The only current monetisation of pure reachability at Vi is the enterprise verification partnership with Meta, and it is not connected to the dormant base at all.**

---

## 40. Trust & Safety

*Placed before §50 deliberately, because the proposal that follows creates a harmful incentive if it is built without the constraints specified here, and stating that after proposing it would be the wrong order.*

A product that pays Vi when a third party queries whether a number is live creates three specific risks, and each needs a mechanic rather than a principle.

**Surveillance by aggregation.** A verification API answers a narrow question but a stream of queries reveals a pattern — which institutions are checking a person and when. The mechanic: responses are limited to a boolean liveness and match result with no timestamps, no location, no query history returned, and enterprise counterparties receive no ability to enumerate or subscribe to a number.

**Fraud surface.** A dormant SIM that a third party keeps alive is precisely the target profile for SIM-swap attacks, because the legitimate holder is not watching it. The mechanic: any anchored connection undergoing a SIM replacement is removed from the anchored cohort automatically, verification is suspended for a fixed cooling period, and the subscriber is notified through a channel other than the number itself.

**Consent that is not real.** A user who has not opened the Vi app in eight months cannot meaningfully consent through it. The mechanic: enrolment is opt-in, evidenced, revocable by a single free SMS or IVR action, and re-confirmed annually — and a connection whose consent lapses leaves the numerator of AVC/1k immediately, which is why the metric is defined conjunctively in §31.

**The incentive that must be excluded, stated plainly.** If verification revenue funds the connection's validity, Vi acquires a financial reason to keep numbers alive that the user has abandoned — and, worse, a reason not to release them, which is the exact behaviour this case study criticises. §48 therefore places verification-linked targets for the retention or growth of the dormant base permanently out of scope, and §53 makes automatic release on consent lapse a build requirement rather than a policy.

---

## 41. Technical Architecture

The relevant architecture here is not the radio network but the subscriber data layer: the HLR/HSS holding subscription state, the VLR recording where a device is currently registered, and the billing and provisioning systems that decide validity. VLR registration — the thing TRAI publishes a monthly snapshot of — is generated continuously and is available to Vi at far finer resolution than the peak-date figure the regulator prints.

That asymmetry is the technical basis of the proposal: Vi already knows, per connection per day, what the regulator learns once a month.

---

## 42. Data Flow

A verification event flows: enterprise counterparty → Vi API gateway → consent check against the enrolment register → liveness lookup against HLR/VLR state → boolean response → metered billing record. No customer-identifying payload leaves Vi, and no enterprise identity enters the subscriber record.

The critical flow constraint is the reverse direction: **query volume must not become an input to any retention, marketing or collections system**, enforced by pipeline test rather than by policy, on the same pattern as Day 61's firewall between measurement and marketing.

---

## 43. API Ecosystem

Vi's live precedent is the silent mobile verification integration with Meta covering WhatsApp, Facebook and Instagram, which validates a user through network capability rather than an SMS OTP. This is the same primitive the proposal generalises — network-attested identity sold to a party that needs it.

The addressable counterparty set beyond Meta is the Indian OTP economy itself: banks, NBFCs, insurers, UPI apps and government services, all of which currently pay for SMS delivery to numbers that may or may not be reachable.

---

## 44. Privacy & Security

India's DPDP framework makes consent, purpose limitation and withdrawal enforceable obligations rather than good practice, with substantial penalties. Any product built on subscriber identity has to treat the enrolment register — not the API — as the primary compliance artefact.

The design position taken here is that **data minimisation is a product constraint, not a compliance footnote**: the response payload is deliberately impoverished (boolean, no metadata) because a richer response would be more valuable to sell and would convert a verification service into a tracking service. This is the second consecutive case study in this series where a privacy limit is written into the mechanics before it is asked for.

---

## 45. Pain Points

| # | Pain point | Evidence |
|---|---|---|
| P1 | 16.02% of connections do not register on the network | TRAI VLR, Jun 2026 🟢 |
| P2 | Subscriber additions and active users move in opposite directions | +0.3 mn vs −2.3 mn, Q1 FY27 🟢 |
| P3 | Reported market share overstates active share by 11.53% relative | Derived, D3d 🟢 |
| P4 | ARPU is depressed 41.77% of the way to Airtel's by the denominator alone | Derived, D5e 🟢 |
| P5 | No product priced for reachability without consumption | Vi published tariffs 🟢 |
| P6 | Inactive connections constrain numbering capacity for acquisition | DoT VLR-based allocation, Vodafone's TRAI filing 🟢 |
| P7 | Capital structure consumes 90.57% of revenue before operating cost | Q1 FY27 P&L 🟢 |
| P8 | Absent from 5G FWA, which Jio and Airtel hold 99.92% of | TRAI, Jun 2026 🟢 |

---

## 46. Opportunity Mapping

| Opportunity | Population | Requires |
|---|---|---|
| Upgrade non-4G/5G connections | 63.0 mn (32.63% of base) | Device financing, customer behaviour change |
| Monetise dormant connections | 31.85 mn | A payer other than the subscriber |
| Release dormant connections and report honestly | 31.85 mn | Nobody's cooperation |
| Spectrum refarm / capacity on existing sites | 167.0 mn active | Nobody's cooperation |
| Enter FWA | Market of 12.94 mn and growing | Capital Vi does not have |

The final column is the one that decides §47. Two of these five require someone outside Vi to change their behaviour; two require nobody to; and one requires money.

---

## 47. RICE

*Framework note: run with a sensitivity pass. Initiatives that need a customer or counterparty to change behaviour are multiplied by a stress rule; those that deliver value on connections and assets that already exist are exempt, because they need no one's cooperation.*

**The stress rule comes from the company's own filed evidence.** In its submission to TRAI's consultation on deactivation of SIMs for non-usage, Vodafone told the regulator that **90% of customers who have not used a SIM for sixty continuous days do not use the SIM at all.** The complement — **10.00%** — is the reach discount applied to any initiative that depends on waking a dormant connection. The harsher figure available from the same submission (80% at thirty days, implying 20.00%) is *not* used; the generous one is.

| Initiative | Reach (mn) | Impact | Conf. | Effort | **Base** | **Stressed** |
|---|---|---|---|---|---|---|
| Spectrum refarm / 4G capacity | 167.0 | 1.00 | 0.85 | 22 | **6.45** | **6.45** (exempt) |
| 2G-to-4G device-financed upgrade | 63.0 | 2.00 | 0.60 | 26 | **2.91** | **0.29** |
| **Vi Anchor (PROPOSED)** | **31.85** | **1.50** | **0.55** | **26** | **1.01** | **0.10** |
| Dormancy release + reconciliation | 31.85 | 0.75 | 0.90 | 26 | **0.83** | **0.83** (exempt) |

**Vi Anchor falls from 3rd of 4 at baseline to 4th and last under stress**, behind an initiative this case study did not propose. `verify.py` asserts programmatically both that Anchor finishes last and that it is the **weakest stressed initiative at baseline** — the only configuration in which the demotion can honestly occur, rather than being arranged.

The result should be read as the answer, not as a caveat. A company that has spent five months adding connections while losing users, and whose own filed evidence says nine in ten dormant SIMs never return, should first do the thing that requires nobody's cooperation: **release the dead connections and publish the reconciliation.** That is worse in absolute score than the upgrade play and better than the clever one, and it is available immediately.

---

## 48. MoSCoW

| | |
|---|---|
| **Must** | Per-connection VLR-plus-recharge cohorting; explicit revocable consent register; automatic release on consent lapse or SIM replacement; published reconciliation of connections to active users |
| **Should** | Enterprise verification metering and billing; circle-level SSR-90 reporting; IVR and SMS enrolment for non-smartphone users |
| **Could** | Extension to insurers and government services; subscriber-visible liveness status in the Vi app |
| **Won't** | Any verification-linked target for retention or growth of the dormant base; any response payload beyond boolean liveness and match; any use of query volume in retention, marketing or collections systems |

The "Won't" row is load-bearing rather than decorative — each entry closes a specific route by which this product becomes the thing §40 warns about.

---

## 49. Kano

| Feature | Category | Note |
|---|---|---|
| Network coverage and speed | Basic | Absence loses the primary line outright |
| OTT bundles | Performance | Competitive parity, weakly differentiating |
| Number retention at ₹199 | **Reverse** | For the dormant user, the price of the bundle is why they left |
| Reachability with no consumer charge | **Attractive** | Nobody offers it; nobody has been asked for it |
| Verification as an enterprise service | Performance (enterprise) | Already demonstrated with Meta |

The reverse classification in row three is the point. Vi's existing answer to the dormant user's job actively repels them, because it prices a service they do not want in order to deliver one they do.

---

## 50. Feature Proposal — *Vi Anchor*

**What it is.** An enterprise-funded liveness tier for dormant connections. A subscriber whose connection has gone inactive may opt in to Anchor at no charge. Vi keeps the connection registered and reachable for incoming SMS and calls. Enterprise counterparties — banks, insurers, UPI apps, platforms — pay Vi per verification query against anchored numbers, on the primitive Vi already sells to Meta. **The verifier pays for the connection's liveness; the subscriber pays nothing.**

**Why this shape.** Every existing option in the Indian market asks the person who has already decided the number is not worth ₹199 a month to pay ₹199 a month. Anchor changes the payer, not the price. It is the only structure in which the dormant base can generate revenue without first requiring the dormant user to become a paying customer again — which, on Vodafone's own filed evidence, nine in ten of them will not do.

**What it is not.** It is not a cheap tariff — that exists and is not the constraint. It is not a data or voice allowance. It is not a way of holding numbers longer: consent lapse, SIM replacement or the subscriber's own request removes a connection from the programme immediately and automatically.

**North Star:** AVC/1k, per §31, with dormant connections held as the denominator.
**Guardrail:** SSR-90, per §31, by circle, owned outside the enterprise revenue line.

---

## 51. PRD

**Problem.** 31.85 mn Vi connections are held but inactive. They generate no revenue, distort every reported metric, and consume VLR-allocated numbering capacity. No product exists for the job their holders actually have.

**Goals.** Convert a measurable share of the dormant base into consented, network-registered, revenue-generating connections; and, independently of Anchor's success, give Vi the cohorting needed to report connections and active users separately.

**Non-goals.** Increasing the reported subscriber count. Retaining connections whose holders have not consented. Selling any attribute of a subscriber beyond boolean liveness and match.

**User stories.**
- As a dormant-base holder, I can keep my number reachable for bank OTPs without a monthly charge, and withdraw at any time with one free SMS.
- As a bank, I can confirm a customer's number is live and unchanged before relying on it for an OTP.
- As Vi's finance team, I can report active and total connections separately with an auditable reconciliation.

**Functional requirements.** Consent register with evidenced opt-in, annual re-confirmation and single-action withdrawal; per-connection daily VLR state; boolean verification API with metering; automatic removal on SIM replacement, consent lapse or 90-day continuous non-registration; circle-level SSR-90 reporting.

**Non-functional.** DPDP-compliant consent storage; response payload restricted by schema, not by convention; query-volume data physically separated from retention and marketing systems, enforced by build-pipeline test.

**Acceptance criteria.** A connection appears in AVC/1k only if all four §31 conditions hold. Any breach of SSR-90 suspends verification on the affected cohort automatically within one reporting cycle.

**Success metrics.** AVC/1k at the R1 threshold in §54; SSR-90 no worse than baseline in any circle; reconciliation of total to active connections published quarterly.

---

## 52. Wireframes

```
DORMANT-HOLDER SMS ENROLMENT (works on a feature phone)
+------------------------------------------------------+
|  Vi: Your number 98XXXXXX12 is not active.            |
|  Banks and apps may not reach you.                    |
|                                                       |
|  Reply ANCHOR to keep this number reachable           |
|  for incoming calls and OTPs at NO CHARGE.            |
|  Reply STOP any time to leave. Free.                  |
|                                                       |
|  What we share: only whether the number is live       |
|  and unchanged. Never your calls, location or data.   |
+------------------------------------------------------+

ENTERPRISE CONSOLE — VERIFICATION
+------------------------------------------------------+
|  Query: 98XXXXXX12                                    |
|  ---------------------------------------------------- |
|  Live on network ................................ YES |
|  SIM unchanged since ....................... 90+ days |
|  Consent on file ................................ YES |
|  ---------------------------------------------------- |
|  Returned: 3 booleans. No timestamps. No history.     |
|  Billed: 1 query.                                     |
+------------------------------------------------------+

INTERNAL — BASE RECONCILIATION (published quarterly)
+------------------------------------------------------+
|  Connections reported ....................  198.82 mn |
|  Active on peak VLR ......................  166.97 mn |
|  Dormant, consented (anchored) ...........       X mn |
|  Dormant, unconsented ....................       Y mn |
|  Released this quarter ...................       Z mn |
|  ---------------------------------------------------- |
|  AVC/1k = anchored & verified & registered per 1,000  |
|           dormant connections held                    |
+------------------------------------------------------+
```

---

## 53. Rollout Plan

**Phase 0 — two analyst-weeks, on data Vi already holds, designed to kill the proposal cheaply.**

Join per-connection VLR registration history to recharge history for one circle over 24 months, and answer three questions.

- **K1.** Fewer than 15% of dormant connections show *any* network registration in a rolling 90-day window — i.e. the handsets are not merely unused but gone. Anchor cannot keep alive a SIM that is not in a powered device.
- **K2 — named as the most likely to fire.** The dormant base and the OTP-dependent base do not overlap. If the connections that lapsed were never the ones institutions had on file — because users updated their bank records to the new primary number years ago — then the identity attachment Anchor monetises does not exist, and the entire diagnosis in §21 is wrong.
- **K3.** Enterprise verification demand cannot be separated from existing SMS-OTP spend in a way any counterparty would pay incrementally for.

**Phase 1 (Q3 FY27).** One circle, SMS and IVR enrolment only, one enterprise counterparty, no app dependency. **Phase 2 (Q4 FY27).** Three circles, three counterparties, SSR-90 reporting live. **Phase 3 (FY28).** National, subject to §54's decision rule.

**Running in parallel and not contingent on any of the above:** the dormancy release and published reconciliation that §47 ranks above Anchor under stress. It should start immediately and does not need Phase 0 to succeed.

---

## 54. A/B Testing

| Arm | Design |
|---|---|
| A — control | Dormant connections handled as today: SMS reminders, ₹199 minimum recharge |
| B — falsification arm | A free 12-month Vi-funded validity extension, no enterprise verification, no consent apparatus |
| C — treatment | Vi Anchor as specified |

**Arm B is built to kill the thesis.** It delivers the *benefit* — the number stays alive at no cost to the user — without the enterprise apparatus, the consent register or the verification revenue. If B matches C on reactivation and subsequent recharge behaviour, then Anchor's machinery is theatre and Vi should simply subsidise validity, which is far cheaper to build.

**Pre-registered decision rule (R1).** Arm C proceeds to Phase 3 only if it beats Arm B by **more than 8 percentage points on AVC/1k** across two consecutive quarters including one non-festival quarter, **and** SSR-90 is no worse than control in every circle measured separately, **and** Arm C's verification revenue exceeds the cost of the validity Vi funds. Failing any of the three, the programme reverts to Arm B or stops.
---

## 55. KPI Dashboard

| KPI | Baseline (Q1 FY27) | Target | Early warning |
|---|---|---|---|
| **VLR ratio** | 83.98% | +200 bps in 4 quarters | **A further fall while net adds stay positive kills the "quality customer" narrative outright** |
| AVC/1k | 0 (not yet built) | R1 threshold, §54 | Below 8 pp over Arm B at two quarters |
| SSR-90, worst circle | not measured | ≤ control | Any circle worse than control |
| Connections − active gap | 31.85 mn | falling | Rising in any quarter |
| ARPU per active subscriber | ₹225.47 | maintained | Falls while headline ARPU rises |
| Reported vs active market share | 15.50% / 13.90% | gap narrowing | Gap widens |

The first row is the discipline. Vi publishes net additions monthly and TRAI publishes the VLR ratio monthly, so this thesis is falsifiable within four weeks of publication by anyone who reads both.

---

## 56. Product Roadmap

| Period | Focus |
|---|---|
| Q2 FY27 | Dormancy release begins; base reconciliation designed; Phase 0 analysis run |
| Q3 FY27 | First published connections-to-active reconciliation; Anchor Phase 1 in one circle |
| Q4 FY27 | Anchor Phase 2, three circles; SSR-90 live; 2G-to-4G upgrade programme scoped |
| FY28 H1 | §54 decision rule evaluated; Anchor scaled or stopped |
| FY28 H2 | Upgrade programme at scale — the initiative RICE actually favours after the exempt ones |

The sequencing deliberately puts the proposed feature third, behind release-and-report and behind capacity work, because that is where §47 put it.

---

## 57. Risks & Mitigation

| Risk | Mitigation |
|---|---|
| Releasing dormant connections produces a large reported subscriber loss | Publish the reconciliation *before* the release, so the fall is pre-explained rather than discovered |
| Anchor becomes a reason to hold dead numbers | §48 excludes verification-linked base targets permanently; automatic release is a build requirement |
| SIM-swap fraud concentrates on anchored numbers | Automatic removal on SIM replacement plus a cooling period; out-of-band notification |
| DPDP exposure on consent quality | Evidenced opt-in, annual re-confirmation, single-action free withdrawal |
| Capital structure overwhelms any operating improvement | Acknowledged and not solved here — ₹156,058 Cr of deferred obligations is 7.75× annualised EBITDA |
| Enterprise counterparties will not pay incrementally | K3 in Phase 0 tests exactly this before any build |

---

## 58. Future Vision

The plausible good outcome for Vi is not that it wins back the primary line at scale — Airtel's India EBITDA alone is 4.92× Vi's total EBITDA, and that gap compounds through capex. It is that Vi becomes an honest, smaller, solvent third network whose reported numbers describe its actual business, with an enterprise and identity layer that monetises the one asset its scale still confers: 198.82 million numbers that Indian institutions have on file.

The bad outcome is not collapse — with the government holding 48.99% that is now a political question rather than a commercial one. The bad outcome is a company that keeps reporting connection growth for several more years while its active base drains, and discovers the problem when the numbering runs out.

---

## 59. PM Lessons

1. **When the regulator publishes a metric the company does not lead with, that metric is the case study.** TRAI's VLR ratio turned "first subscriber addition since merger" from a claim into a testable proposition, and it failed the test.
2. **A headline ratio's denominator is a product decision.** Vi's subscriber count, market share and ARPU are all computed over a base that includes 31.85 mn non-users — inflating two of them and deflating the third.
3. **Test the convenient explanation with the competitor's own data.** M2M looked like it might explain the VLR gap until Airtel turned out to carry 1.56× the M2M intensity at 99.27% activity.
4. **Include the number that weakens your argument.** 41.77% of Vi's ARPU gap to Airtel is denominator, not price — which makes Vi's real customers look much better and makes the case for fixing the base rather than the tariff.
5. **Search the company's regulatory filings for its own past position.** Vodafone told TRAI that 90% of sixty-day-dormant SIMs never return, and argued for disconnection on the sixtieth day with no grace period. That number became this case study's stress rule and its most damaging fact, and it came from the company itself.
6. **Check whether the metric distortion has an operational cost, not just a reporting one.** DoT allocates numbering on a VLR basis, so the ghost base is taxing the acquisition it flatters — a fact available only in a primary filing.
7. **When the ranked answer is boring, publish the boring answer.** RICE put "release the dead connections and publish the reconciliation" above the designed proposal, and the honest thing is to say so rather than re-weight the inputs.

---

## 60. PM Interview Questions

1. Vi reports 193.1 mn subscribers; TRAI reports 198.82 mn connections of which 166.97 mn are active. Which number would you put on a board slide, and what would you say about the other two?
2. Your headline metric rose 0.16% while the metric you did not publish fell 1.36%. Design the counter-metric that would have caught this a year earlier.
3. Airtel runs a 99.27% VLR ratio while carrying more M2M than Vi. What does that rule out, and what does it leave?
4. You are asked to price a product for a user who wants reachability and no consumption. What breaks if you simply cut the price of the existing pack?
5. A proposal you designed ranks last under your own sensitivity analysis. What do you do, and what would make it dishonest to re-run the analysis?
6. Vi's own filing says 90% of sixty-day-dormant SIMs never return. Does that argue for or against building anything for the dormant base?
7. Design the guardrail that stops an enterprise-funded liveness product from becoming a surveillance product. Name the mechanic, not the principle.

---

## 61. References

**Primary**
1. TRAI, *Telecom Subscription Data, June 2026*, Press Release No. 104/2026, released 28 July 2026 — subscriber counts, VLR ratios, M2M, FWA.
2. TRAI monthly subscription data, January–May 2026 — Vi monthly net additions and VLR ratios.
3. Vodafone, response to *TRAI Consultation Paper on Deactivation of SIMs due to Non-usage*, trai.gov.in — the 80%/90% dormancy figures and the HLR-to-VLR allocation change. Pre-merger vintage; see Appendix A-4.
4. Vodafone Idea Limited, Q1 FY27 results and press release, 10 August 2026.
5. Bharti Airtel Limited, Q1 FY27 media release, 4 August 2026.
6. Reliance Industries Limited, Q1 FY27 results (Jio Platforms), 17 July 2026.
7. Ministry of Corporate Affairs registry — CIN L32100GJ1996PLC030976.
8. TRAI, Telecom Consumer Protection Regulations, 6th amendment — 90-day non-usage and ₹20 retention provisions.
9. Vodafone Idea published tariffs, myvi.in — service-validity extension plans.

**Secondary** (used for corroboration, flagged where single-sourced)
10. Business Today, Free Press Journal, Indian Television, Storyboard18 — Q1 FY27 results detail.
11. TelecomTalk, FoneArena, Medianama — TRAI monthly data reporting.
12. Outlook Business, Business Standard, Light Reading, Mobile World Live — AGR relief and government shareholding.
13. Supreme Court Observer — AGR payment schedule.
14. afaqs, Mediabrief, TelecomTalk — CEO transition, August 2025.
15. Cashify, PlanCompare, paidfreedroid — 2026 minimum-recharge pricing across operators.

---

## 62. About the Author

Gaurav Singh — Product Manager. This is Day 65 of a 90-day public case-study series applying structured PM frameworks to real products, with a zero-fabrication standard: every figure is cited, labelled as an estimate, flagged as single-sourced, or recorded as not publicly disclosed.

---

## 63. License

Analysis and original text © 2026 Gaurav Singh, released for non-commercial use with attribution. All company figures belong to their sources and are cited in §61. No affiliation with Vodafone Idea Limited, Bharti Airtel Limited or Reliance Industries Limited.

---

## 64. Self Review

**What is strong.** The thesis rests on a regulator-published metric that the company does not lead with, which makes it independently checkable and monthly-falsifiable. The M2M falsification using Airtel's own intensity is the cleanest single argument in the piece. The stress rule comes from the company's own filing rather than from an assumption. And the proposal loses to an initiative that was not proposed, verified programmatically rather than asserted.

**What is weak, stated plainly.** The secondary-SIM diagnosis in §21 is an *interpretation* of the VLR gap, not a measurement of it. TRAI publishes the gap; nobody publishes why. The rival reading — that these are simply churned customers awaiting the 90-day disconnection, with no identity attachment at all — is given equal weight in ASSUMPTIONS Part 1 and is exactly what Phase 0's K2 is built to test. If K2 fires, the diagnosis is wrong and Anchor should never be built.

**What I could not establish.** Whether Vi's 193.1 mn and TRAI's 198.82 mn differ because of M2M treatment or something else; the exact composition of the ₹1,816 Cr settlement-asset remeasurement; and Vi's monthly M2M additions, without which the "additions are machines" hypothesis could be raised but not tested — so it is raised and left open rather than asserted.

**One thing I would do differently.** The double Porter's run in §16 is the sharpest section, and I reached it late. The primary-versus-secondary seam should have organised the analysis from §11 onward rather than arriving at §16.

---

## 65. Appendix

### A. Source conflicts

| # | Conflict | Handling |
|---|---|---|
| A-1 | CIN embeds **1996**; registry records incorporation **14 March 1995** | Both stated in §2; CIN cited in full, never the name alone |
| A-2 | **Vi's own base 193.1 mn vs TRAI's 198.82 mn** on the same date, a 5.72 mn / 2.96% gap — while Jio's company figure (533.3 mn) runs *above* TRAI's (503.58 mn) | Unresolved. Both reported. Company figures used for company-basis derivations, TRAI figures for TRAI-basis, never mixed within one calculation; `verify.py` runs D1 on both bases and the finding survives at 7.67× and 6.88× respectively |
| A-3 | Customer ARPU ₹195 vs blended ARPU ₹177 imply 17.82 mn non-customer connections; disclosed M2M is 21.62 mn | Not forced to reconcile. Both reported; the residual is labelled derived and is load-bearing nowhere |
| A-4 | The 80%/90% dormancy figures come from **Vodafone pre-merger**, in a consultation whose internal references (DoT July 2011, MNP Regulation 2009, "periodic SMS from Aug 2011") date it to circa 2012 | Vintage stated wherever used. It is the company's predecessor's own filed evidence, not a current disclosure, and is used as a *stress discount* — the direction is what matters, and a fourteen-year-old estimate is used conservatively |
| A-5 | Bank debt reported as **₹211 Cr** in the press release and **₹3,708 Cr** in the financial statements (the latter including interest accrued but not due) | Both stated; the difference is a definitional one, not a discrepancy |
| A-6 | Paid-up capital differs across MCA aggregators (₹32,118 Cr to ₹108,343 Cr) as snapshots of different dates | No figure quoted in the analysis; authorised and paid-up capital omitted rather than guessed |
| A-7 | Reported AGR relief of ~₹54,200 Cr and the "27% cut" appear in secondary coverage; no DoT order text was located | 🟡 Single-sourced, flagged, load-bearing nowhere |

### B. Evidence grades

🟢 **High** — TRAI subscription data, company results releases, MCA registry, primary regulatory filings.
🟡 **Medium** — AGR relief quantum, the ~₹45,000 Cr capex plan's phasing, Vi's blended-ARPU denominator.
🟠 **Low** — none relied upon.
🔴 **Conflicting** — A-2 (two subscriber bases) and A-5 (two debt figures), handled as above.

### C. Author-constructed content

*Vi Anchor*, AVC/1k, SSR-90, the RICE inputs, the Phase 0 kill criteria and the §54 arms are the author's constructions, not Vi disclosures or plans. See ASSUMPTIONS.md Part 3 for the full inventory and the reasoning behind each input.

### D. Asset status

| Asset | Status |
|---|---|
| README.md | Complete, 65 sections |
| ASSUMPTIONS.md | Complete, Parts 1–5 |
| verify.py | 139 checks, all passing — delivered, not committed |
| LinkedIn carousel + caption | Delivered, not committed |

---

*Day 65 of 90 · [← Day 64 — Zypp Electric](../Day-64-Zypp-Electric) · Day 66 →*
