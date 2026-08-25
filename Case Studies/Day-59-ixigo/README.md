# ixigo — Three Businesses Wearing One Growth Number

<div align="center">

**Day 59 of a 90-day Product Management case study series**
*Researched, derived and verified — not fabricated*

</div>

---

## 1. Cover

**Product:** ixigo (Confirmtkt, AbhiBus, ixigo trains/flights/hotels)
**Company:** Le Travenues Technology Limited
**Domain:** Travel & Online Travel Aggregation (OTA) — first entry in this series
**Day:** 59 of 90
**Author:** Gaurav

> Q1 FY27 read as compounding growth: GTV up 19%, revenue up 13%, profit after tax up 81%. Underneath, ixigo's own **Adjusted EBITDA — the metric its own investor deck uses to strip out non-operating income — fell 6.9%.** ₹29.15 Cr of interest and gains on a ₹1,740 Cr treasury built by the 2024 IPO and a 2025 Prosus placement was **85.1% of the quarter's profit.** And one growth number was hiding three businesses moving in three different directions: buses gained volume *and* margin, trains lost bookings but earned more per passenger, and flights — the single largest vertical — grew GTV 27% while ixigo's own disclosed gross take rate on flights compressed from 9.17% to 8.41% and flight contribution margin **fell** in absolute rupees. The tool that would let a traveller compare a train, a bus and a flight against each other, on cost and time together, in one search, has never shipped.

---

## 2. Repository Metadata

| Field | Value |
|---|---|
| Case Study | Day 59 — ixigo (Le Travenues Technology Limited) |
| CIN | **L63000HR2006PLC071540** (current, listed; see Appendix A-1 for a registry conflict) |
| Incorporated | 3 June 2006 |
| ROC | Haryana |
| Sector | Online Travel Aggregation |
| Format | 65-section README + companion ASSUMPTIONS.md |
| Diagrams | None — ASCII wireframes and tables only, per house style |
| Verification | Every derived figure checked in `verify.py` before publication |

---

## 3. Badges

`Status: Published` · `Sections: 65` · `Fabricated Data: 0` · `Verified Derivations: see verify.py` · `Day: 59/90`

---

## 4. Table of Contents

<details>
<summary>Click to expand — 65 sections</summary>

| | |
|---|---|
| 1. Cover | 34. HEART |
| 2. Repository Metadata | 35. Growth Strategy |
| 3. Badges | 36. Growth Loops |
| 4. Table of Contents | 37. Network Effects |
| 5. Executive Summary | 38. Product Strategy |
| 6. Product Overview | 39. Monetization |
| 7. Company Background | 40. Trust & Safety |
| 8. Product Timeline | 41. Technical Architecture |
| 9. Vision & Mission | 42. Data Flow |
| 10. Problem Statement | 43. API Ecosystem |
| 11. Market Research | 44. Privacy & Security |
| 12. Industry Analysis | 45. Pain Points |
| 13. TAM/SAM/SOM | 46. Opportunity Mapping |
| 14. Competitor Analysis | 47. RICE |
| 15. SWOT | 48. MoSCoW |
| 16. Porter's Five Forces | 49. Kano |
| 17. Business Model Canvas | 50. Feature Proposal |
| 18. Revenue Model | 51. PRD |
| 19. Target Users | 52. Wireframes |
| 20. Personas | 53. Rollout Plan |
| 21. JTBD | 54. A/B Testing |
| 22. User Journey | 55. KPI Dashboard |
| 23. User Flow | 56. Product Roadmap |
| 24. Information Architecture | 57. Risks & Mitigation |
| 25. UX Audit | 58. Future Vision |
| 26. UI Audit | 59. PM Lessons |
| 27. Accessibility | 60. PM Interview Questions |
| 28. Feature Breakdown | 61. References |
| 29. AI Capabilities | 62. About the Author |
| 30. Product Metrics | 63. License |
| 31. North Star Metric | 64. Self Review |
| 32. Product Analytics | 65. Appendix |
| 33. AARRR | |

</details>

---

## 5. Executive Summary

ixigo's Q1 FY27 (quarter ended 30 June 2026) print was covered as an unambiguous win: GTV ₹5,524.33 Cr (+18.9%), revenue from operations ₹356.75 Cr (+13.1%), PAT ₹34.24 Cr (+81% YoY, an all-time high). All three figures are real and correctly disclosed. What the coverage did not carry through is that ixigo's own **Adjusted EBITDA — the figure its investor materials use specifically to exclude non-operating income — fell from ₹31.4 Cr to ₹29.24 Cr, a 6.9% decline**, even as headline (unadjusted) EBITDA rose 65% to ₹53.52 Cr. The gap between those two numbers is almost entirely one line: **₹29.15 Cr of "interest income and gains on financial assets,"** disclosed separately, sitting on a **₹1,740.01 Cr** treasury built from the June 2024 IPO and a ₹1,296 Cr Prosus placement in October 2025. That single line was **85.1% of the quarter's entire profit after tax.**

Segment disclosures make the picture sharper still. Flights — ixigo's largest single vertical by GTV — grew GTV 27% while the company's own disclosed **gross take rate compressed from 9.17% to 8.41%**, and flight contribution margin **fell** from an implied ₹42.75 Cr to ₹41.04 Cr even as the vertical grew fastest in absolute rupee GTV terms after buses. Trains lost 8% of passengers but grew revenue 9%, meaning the platform earned more from each traveller who still booked. Buses grew GTV 39%, revenue 34%, and contribution margin 28%, at a healthy 53% contribution rate — the strongest unit economics of the three. Three verticals, three different stories, one blended growth number.

This case study's proposal, **ixigo Corridor**, does not try to fix flight pricing — that lever sits mostly with airlines and fuel/geopolitical costs outside ixigo's control. It tries to make the platform's own cross-modal advantage — the fact that it is the only major Indian OTA that genuinely sells flights, trains *and* buses under one roof — into something a traveller can actually use to substitute a compressed-margin mode for a healthier one, rather than a fact buried in three separate search tabs.

---

## 6. Product Overview

ixigo is a multi-modal Indian travel platform selling flight, train, bus and hotel bookings, alongside a set of assurance products (PNR confirmation prediction, "Peace of Mind" trip protection) built on top of ticketing. It operates via the flagship ixigo app, the Confirmtkt train-booking app (acquired 2021), and AbhiBus (acquired 2021) for buses. Group MAU stood at 8.54 crore in Q1 FY27, of which 0.42 crore (4.92%) transacted in the month. 94% of transactions originate from Tier II/III cities, and management describes the company as serving "the next billion users" rather than the metro traveller MakeMyTrip's brand skews toward.

## 7. Company Background

**Le Travenues Technology Limited**, CIN **L63000HR2006PLC071540**, was incorporated on 3 June 2006 and is registered with the RoC-Haryana. Its registered office is Second Floor, Veritas Building, Sector 53, Golf Course Road, Gurugram, Haryana 122002. Authorised capital is ₹50.17 Cr; paid-up capital ₹43.87 Cr. Founders **Aloke Bajpai** (Managing Director, DIN 00119037) and **Rajnish Kumar** (Director, DIN 02834454) started the company as a flights metasearch product in 2007. The board also includes Rajesh Sawhney (01519511), Rahul Pandit (00003036), Shailesh Lakhani (03567739), Arun Seth (00204434), Shubha Rao Mayya (08193276), Frederic Lalonde (00739136) — co-founder of Hopper — and Mahendra Pratap Mall (02316235). ixigo listed on the NSE and BSE in June 2024 at a reported 48.5% listing-day premium.

## 8. Product Timeline

2007 flights metasearch launch · 2014 train running-status and PNR app · Feb 2021 acquisition of **ConfirmTkt** (train confirmation prediction) · Aug 2021 acquisition of **AbhiBus** (buses) · Jun 2024 **IPO** on NSE/BSE · Oct 2025 **₹1,296 Cr Prosus preferential allotment** (~10% stake) · Aug 2026 **Brevistay acquisition** (54.66% stake, ~₹65.7 Cr, direct hotel supply in ~700 towns) alongside a first disclosed exploration of a **corporate/small-business travel product**.

## 9. Vision & Mission

ixigo states its mission as making travel planning and booking simple, especially for Tier II/III India, using AI-assisted trip planning and assurance products rather than pure metasearch. The three-vertical structure (flights, trains, buses) under one company is, on the company's own account, meant to be a structural advantage over single-mode or metro-skewed competitors — this case study is a test of whether that advantage is currently *used* as a product capability or merely *disclosed* as a segment table.

## 10. Problem Statement

ixigo's headline growth metrics (GTV, revenue, PAT) compound favourably and are read by press and investors as a single story of platform strength. That story obscures two separate and more specific problems: **(1)** a rising share of quarterly profit is non-operating interest income on IPO/placement cash rather than the underlying travel business, and **(2)** the platform's largest vertical (flights) is under active margin pressure it has only a limited ability to reverse, while the platform's own multi-modal structure — its most distinctive asset relative to single-mode rivals — is not yet surfaced to travellers as a way to route around that pressure.

## 11. Market Research

India's air passenger base is large and price-sensitive: DGCA recorded **1.20 crore domestic passengers in July 2026, down 4.8% year-on-year**, with IndiGo holding a record 67.4% domestic share. Rail remains the dominant mode by volume for budget travel, and intercity bus travel has professionalised significantly over the last five years (seat-tracking, live GPS, assured operators), the segment ixigo's own numbers show growing fastest. Domestic and international airfares rose sharply in the same period — reported at roughly **+22% domestic and +38% international year-on-year** — attributed by multiple outlets to the West Asia conflict's effect on crude and jet fuel costs and reduced capacity.

## 12. Industry Analysis

Indian OTAs monetise primarily by taking a spread (the gap between the fare/fee charged to the traveller and what is remitted to the airline, railway or bus operator), supplemented by ancillary attach (seat selection, insurance, "assurance" products) and, for a subset of listed players, treasury income on IPO proceeds. Regulatory friction has increased on the rail side specifically: Aadhaar OTP became mandatory for online Tatkal bookings from July 2025, and Aadhaar-verified-only booking windows were introduced from October 2025 — both aimed at curbing bulk/bot bookings that OTA convenience layers had previously helped route around.

## 13. TAM/SAM/SOM *(restricted form — no primary-sourced market-wide TAM was found; sized from ixigo's own disclosed base instead)*

*Framework note: rather than cite an unverifiable third-party India-travel TAM figure, this section sizes opportunity from ixigo's own funnel, which is fully disclosed.*

| Layer | Basis | Figure |
|---|---|---|
| TAM (proxy) | India's addressable online travel booking population | Not independently verifiable from public data; not asserted |
| SAM (disclosed) | ixigo's own MAU | 8.54 crore monthly active users |
| SOM (disclosed) | ixigo's own MTU | 0.42 crore monthly transacting users = **4.92% of MAU** |

The 95-point gap between MAU and MTU is the single most important number in this section: the overwhelming majority of people who open ixigo in a given month do not book anything through it that month. That gap is the basis for the RICE stress rule in §47.

## 14. Competitor Analysis *(restricted to filers)*

MakeMyTrip is the only Indian OTA whose quarterly results are directly comparable in depth (it files with the SEC as a foreign private issuer). EaseMyTrip and Yatra are also listed and do file, but a comparably deep segment reconciliation for both was out of scope for this case study; naming that gap is preferable to a shallow estimate.

**The same quarter, opposite direction.** MakeMyTrip's Q1 FY27: revenue $285.6 Mn (+6.2%), air ticketing revenue **−7.5% YoY**, gross bookings +9.4%, Adjusted EBITDA $55.5 Mn — but **net finance costs rose to $28.3 Mn from $4 Mn**, driven by interest on convertible senior notes, and net profit **fell 64.7%** to $9.1 Mn. ixigo's finance line moved the opposite way: **net finance *income*** of ₹29.15 Cr, not cost, because ixigo holds cash rather than convertible debt. Strip financing effects from both companies and a shared pattern appears: MakeMyTrip's own air revenue fell in the same quarter ixigo's flight take rate compressed — the same West Asia fare shock, hitting two different balance sheets in opposite ways.

## 15. SWOT

**Strengths:** only major Indian OTA genuinely strong across flights, trains *and* buses; ₹1,740 Cr treasury with no convertible debt overhang unlike MakeMyTrip; 94% Tier II/III transaction share, a demographic rivals underserve; healthy bus-segment economics (53% contribution rate).
**Weaknesses:** flight take rate compressing (9.17%→8.41%); Adjusted EBITDA declining even as headline numbers grow; cross-modal advantage not yet productised; hotels segment contribution-negative (≈−₹3.06 Cr this quarter, per §65 D14).
**Opportunities:** direct hotel supply via Brevistay reducing OTA-of-OTA margin leakage; rail assurance products (31% "Peace of Mind" attach rate) show travellers already pay for certainty; explored corporate/SME travel product (announced Aug 2026) is a genuinely new, less price-sensitive demand pool.
**Threats:** flight fare inflation is largely outside ixigo's control; MakeMyTrip's convertible-note overhang means it may compete more aggressively on price to defend share while servicing that debt; rail KYC tightening (Aadhaar-only Tatkal) reduces the convenience gap OTAs historically monetised.

## 16. Porter's Five Forces — double run, Flights vs Buses

*Framework note: run twice because the two verticals sit at opposite points of every force — the divergence is the finding, matching flights' 9.17%→8.41% take-rate compression against buses' 53% contribution rate in the same quarter.*

| Force | Flights | Buses |
|---|---|---|
| Supplier power | High — airlines set price and inventory; OTA take rate is a residual | Moderate — many regional operators, ixigo/AbhiBus has direct relationships |
| Buyer power | High — fare-comparison habits are entrenched, price transparency is near-total | Moderate — fewer comparison tools exist for bus fares specifically |
| New entrants | Low — GDS/NDC integration and capital requirements are real barriers | Moderate — regional aggregators can and do enter |
| Substitutes | Rising — trains and buses are increasingly real substitutes on price-sensitive routes | Low — for many routes, bus is already the cheapest option |
| Rivalry | Intense — MMT, Yatra, EaseMyTrip, airline-direct booking all compete on the same fare | Lower — fewer well-capitalised bus-focused rivals |

## 17. Business Model Canvas

Key partners: airlines, IRCTC/railways, bus operators, hotel supply (direct + Brevistay), payment providers. Key activities: fare aggregation, PNR/confirmation prediction, assurance underwriting, AI trip planning (TARA). Value propositions: price comparison, Tier II/III language and payment support, confirmation certainty on trains. Customer segments: budget-conscious multi-modal travellers, concentrated Tier II/III. Revenue streams: booking commission/spread, ancillary attach, assurance products, advertising, and (this quarter) treasury interest.

## 18. Revenue Model

Revenue is overwhelmingly a **spread on gross transaction value**, disclosed by segment: flights ₹104.56 Cr revenue on ₹2,341.84 Cr GTV (**4.47% of GTV**), trains ₹141.05 Cr on ₹2,138.86 Cr (**6.60%**), buses ₹102.55 Cr on ₹947.43 Cr (**10.82%**). Buses monetise at more than double the rate of flights per rupee of GTV moved — a fact that does not by itself argue for pushing buses over flights (they serve different trip lengths and needs) but is the clearest single number in this case study for why the mix, not just the total, matters.

## 19. Target Users

Budget and value-conscious Indian travellers, disproportionately Tier II/III (94% of transactions), who book across more than one mode depending on price and availability rather than being loyal to a single mode. A meaningfully large secondary segment (per management's own August 2026 commentary) already uses the consumer app for unmanaged small-business and GST-registered corporate travel.

## 20. Personas

*Author-constructed composites built from disclosed segment and city-tier facts — not ixigo persona research, which is not public.*

**Meena, 29, Tier III sales executive.** Books trains for personal travel, flights only when time-constrained and fares are reasonable, price-sensitive to the point of comparing modes manually across apps.
**Rajiv, 34, small-business owner.** Travels for work 2–3 times a month, currently books flights or trains on his personal ixigo account with no expense workflow — the exact profile behind the company's stated corporate-travel exploration.
**Sunita, 45, family traveller.** Books bus and train for family trips, values the "Peace of Mind" confirmation-assurance product highly and would plausibly value an explicit cost/time comparison across modes for a family of four.

## 21. JTBD

"When I need to get from A to B on a date I can't move, help me see every real option — not just the one your app defaults to — so I don't overpay for certainty I could have gotten cheaper another way." ixigo's own segment data (trains earning more per passenger even as volumes fall) suggests travellers already pay a premium for certainty within a single mode; JTBD here is extending that willingness-to-pay-for-certainty logic *across* modes.

## 22. User Journey — the cost-vs-price column

*The stages below are inferable from disclosed product structure; the attribution of where cost is created versus where the traveller sees price is the author's analysis and the mechanism of the whole thesis.*

| Stage | What the traveller does | Where cost is created | Where price is shown |
|---|---|---|---|
| Search | Picks a mode tab (flights/trains/buses) first | Nowhere yet | Not yet — mode choice precedes any price comparison |
| Compare | Compares within the chosen mode only | Opportunity cost of not seeing cheaper modes | Only intra-mode prices shown |
| Book | Confirms one option | Full trip cost locked in | Point price only, no cross-modal reference |
| Assurance upsell | Offered "Peace of Mind" / confirmation products | Underwriting cost to ixigo | Add-on price shown, isolated from base fare |
| Post-booking | Receives confirmation, no comparison retained | N/A | N/A — the traveller never sees what the trip would have cost by another mode |

The traveller chooses a mode **before** any price comparison happens, at the search-tab level. Every cross-modal saving ixigo's own segment data implies (buses monetise leaner and grow contribution 28% while flights compress) is invisible to the person who could have chosen differently.

## 23. User Flow

Search flow is mode-first: a traveller selects Flights, Trains or Buses as a tab before entering an origin/destination, and each vertical runs an independent search-to-book flow. There is no shared origin-destination entry point that fans out to all three modes simultaneously. This is a deliberate product structure inherited from ixigo's acquisition history (Confirmtkt and AbhiBus were separate products), not an oversight, but it is also precisely the gap §50's proposal targets.

## 24. Information Architecture

The app's top-level navigation is organised by mode (Flights, Trains, Buses, Hotels) rather than by trip or corridor. This mirrors most competitors, including MakeMyTrip, and is the industry-standard IA — the case study's argument is not that this IA is wrong, but that it forecloses a comparison the company's own multi-modal supply could otherwise support.

## 25. UX Audit

Within each mode, ixigo's UX is mature: fare calendars, PNR confirmation probability scoring, and live running status are genuine differentiators, particularly on trains. The audit finding here is structural rather than a within-screen defect: no screen in the current flow asks "would another mode get you there cheaper or as fast," which is a gap in scope rather than execution.

## 26. UI Audit

Visual design is consistent across the three vertical apps and the consolidated app, with a 4.8-star cumulative rating across 62.32 lakh+ ratings — a genuinely strong, independently-verifiable signal of baseline UI/UX quality that this case study does not dispute.

## 27. Accessibility

No ixigo-specific accessibility audit or WCAG conformance disclosure was found in public sources; this is stated as unavailable rather than assumed. 8-language support is disclosed and is a meaningful accessibility-adjacent investment for the Tier II/III base ixigo primarily serves.

## 28. Feature Breakdown

| Feature | Status | Vertical |
|---|---|---|
| PNR confirmation prediction | Live, mature | Trains |
| "Peace of Mind" trip protection | Live, 31% attach rate | Cross-mode |
| TARA AI assistant | Live — 92% chat / 81% voice resolution | Cross-mode |
| Direct hotel supply (Brevistay) | Newly acquired, integrating | Hotels |
| Cross-modal corridor comparison | **Does not exist** | Proposed, §50 |

## 29. AI Capabilities

ixigo's disclosed AI investment centres on **TARA**, its assistant, handling roughly 52 lakh AI queries in the quarter at 92% chat and 81% voice resolution, and on fare/PNR prediction models that power the confirmation-assurance product. Management explicitly cited AI infrastructure investment (alongside hotels expansion and marketing) as a driver of the Adjusted EBITDA decline this quarter — a rare case of a company naming its own margin-compressing investment in the same release that reports the compression.

## 30. Product Metrics

GTV ₹5,524.33 Cr (+18.9%) · Revenue ₹356.75 Cr (+13.1%) · Contribution margin ₹144.94 Cr (+13.1%, rate 40.63% vs 40.73% a year earlier) · EBITDA ₹53.52 Cr (+64.8%) · **Adjusted EBITDA ₹29.24 Cr (−6.9%)** · PAT ₹34.24 Cr (+80.8%) · MAU 8.54 Cr · MTU 0.42 Cr (4.92% of MAU).

## 31. North Star Metric

**RCJ/1k — Recommended Corridor Journeys per 1,000 corridor-eligible searches.** A search is corridor-eligible when two or more modes genuinely serve the same origin-destination pair within a comparable time window. RCJ/1k is **conjunctive**: it counts only searches where (1) a real cross-modal comparison was shown with live price and time, (2) the traveller could complete the booking for whichever mode they picked without leaving the comparison flow, (3) the booked mode was not the one the search-tab default would have shown first, and (4) no complaint or cancellation was logged against that booking within 48 hours. The denominator is **eligible searches, not bookings** — so a corridor comparison that is shown but ignored still counts against the metric, keeping the incentive on genuinely useful comparisons rather than on pushing any particular mode.

**Guardrail: GTP-90 — Genuine Time Parity at the 90th percentile.** The share of corridor comparisons whose displayed door-to-door time estimate is within a defined tolerance of the traveller's actual realised time, measured at the 90th percentile (the worst-case tail, not the average — a mean would hide exactly the failures that make a comparison untrustworthy). Owned by a **Trust & Traveller Experience** function with no revenue claim on corridor bookings; its logs are firewalled from the pricing and ranking team by a build-pipeline test, not a policy statement, and a comparison type that breaches GTP-90 for two consecutive weeks is automatically suppressed with no discretionary override.

## 32. Product Analytics

ixigo discloses MAU/MTU, repeat transaction rate (86%), and Tier II/III penetration (94%) — a stronger analytics disclosure than most Indian consumer-tech peers at this scale. What is not disclosed, and what §31's North Star would require building, is any cross-modal search or comparison metric, because no cross-modal comparison surface currently exists to instrument.

## 33. AARRR

Acquisition leans on brand and app-store presence (3.27 crore downloads this quarter); Activation and Retention are evidenced by the 86% repeat transaction rate; Revenue is the spread-based model in §18; Referral is not separately disclosed. The funnel step this case study is most concerned with — the 4.92% MTU:MAU conversion — sits at the Activation/Retention boundary and is the basis of the RICE stress rule in §47.

## 34. HEART

Happiness is evidenced indirectly by the 4.8-star rating; Engagement by MAU; Adoption by download volume; Retention by the 86% repeat rate; Task success is not separately disclosed for cross-modal use cases, because that task does not yet exist in the product.

## 35. Growth Strategy

ixigo's disclosed growth strategy for this quarter combines organic Tier II/III penetration, AI investment (TARA, fare/PNR prediction), and inorganic hotel supply expansion (Brevistay). Management's own commentary frames buses as the vertical benefiting most from "infrastructure investments and supply expansion," consistent with the segment's outsized 39% GTV growth this quarter.

## 36. Growth Loops

The clearest loop in the disclosed data is on trains: PNR-confirmation prediction accuracy drives repeat use of the assurance product, which funds continued investment in prediction accuracy. No comparable loop currently exists across modes — a traveller who discovers ixigo is competitively priced on buses has no product mechanism nudging them to also try flights or trains through ixigo, or vice versa.

## 37. Network Effects

ixigo's network effects are primarily supply-side (more direct hotel/bus supply improves price and availability for all users) rather than the classic two-sided marketplace effect, since travellers do not interact with each other. The Brevistay integration is a direct-supply play in this vein, not a network-effect play in the conventional sense.

## 38. Product Strategy

The strategic tension this quarter's numbers expose is between **reported profitability and operating profitability**. ₹29.15 Cr of interest income — a genuine, honestly disclosed, non-fabricated cash return on a real treasury — will not scale with GTV. It is a fixed-ish quarterly number (roughly ₹116.6 Cr annualised, or **96.5% of all of FY26's full-year Adjusted EBITDA of ₹120.9 Cr**, on its own) that happens to currently be large relative to a still-growing but margin-pressured operating business. As rates move or the treasury is deployed (into Brevistay, AI infrastructure, or a corporate-travel build-out), that cushion will not necessarily persist, and the operating business underneath it — the one Adjusted EBITDA is designed to isolate — is the one that just declined 6.9% year-on-year.

## 39. Monetization

| Segment | GTV | Revenue | Take rate (Rev/GTV) | Contribution Margin | CM rate |
|---|---|---|---|---|---|
| Flights | ₹2,341.84 Cr | ₹104.56 Cr | 4.47% (was 5.62%*) | ₹41.04 Cr | 39.26% |
| Trains | ₹2,138.86 Cr | ₹141.05 Cr | 6.60% | ₹52.74 Cr | 37.39% |
| Buses | ₹947.43 Cr | ₹102.55 Cr | 10.82% | ₹54.22 Cr | 52.87% |
| Hotels | n/a (GTV not disclosed) | n/a | — | **−₹3.06 Cr (derived, §65 D14)** | negative |

*Flight take rate on revenue/GTV (4.47%) differs from the disclosed **gross** take rate (9.17%→8.41%) because the disclosed figure is computed on a different, ixigo-defined base (likely gross booking value before certain pass-throughs); both are reported here rather than reconciled, per house style (Appendix A-2).

## 40. Trust & Safety

The main trust question this quarter is not a harmful incentive created by a proposal (§50's Corridor does not create one — it is an additive comparison layer, not a mechanism that profits from withholding information), so the standard section order is kept rather than reordered. The relevant trust fact already in the data: PNR confirmation prediction and "Peace of Mind" are underwriting-adjacent products sold to a price-sensitive base, and their accuracy is not independently auditable from public disclosure — noted as unavailable rather than assumed reliable.

## 41. Technical Architecture

Not independently disclosed beyond the existence of TARA (an AI assistant layer) and PNR/fare prediction models; ixigo does not publish an architecture diagram or stack disclosure, so none is asserted here.

## 42. Data Flow

Cross-modal data almost certainly exists internally (fare and schedule data for all three modes lives in the same company), which is precisely why §50's proposal is a product and UX problem more than an infrastructure one — the constraint is more likely organisational (three products built by three formerly separate teams) than technical.

## 43. API Ecosystem

Disclosed integrations include IRCTC (train data), airline GDS/NDC content for flights, and bus operator systems via AbhiBus/busGDS.ai. No public API for third-party developers is disclosed.

## 44. Privacy & Security

No ixigo-specific privacy/security certification or breach disclosure was found in public sources during this research; stated as unavailable rather than assumed.

## 45. Pain Points

| Pain point | Who feels it | Evidence |
|---|---|---|
| No cross-modal price/time comparison | Every traveller on a corridor served by 2+ modes | §22, structural |
| Flight prices rising faster than take rate can absorb | Flight travellers, and ixigo's own flight CM | Take rate 9.17%→8.41% |
| Rail booking friction (Aadhaar-only Tatkal) | Budget rail travellers | §12 |
| Assurance product value not visible pre-purchase | All travellers offered "Peace of Mind" | §40 |
| Corporate/SME travel handled as personal booking | Business travellers, per Meena/Rajiv personas | §20 |
| Hotels segment margin-negative | Hotel bookers, indirectly (cross-subsidised) | §65 D14 |

## 46. Opportunity Mapping

The highest-leverage opportunity this quarter's data points to is not "grow GTV faster" — GTV is already growing at a healthy clip across all three modes — but **routing existing demand toward the mix the company already monetises best.** Buses convert GTV to contribution margin at more than double the rate of flights; a traveller who could be shown a competitive bus or train option on a flight-compressed corridor is a lower-effort win than acquiring a new traveller entirely.

## 47. RICE

*Stress rule: Reach discounted by ixigo's own **4.92% MTU:MAU ratio** — of 8.54 crore monthly actives, only 42 lakh transact in a given month. Applied to any initiative whose value depends on travellers discovering and adopting a new behaviour rather than continuing what they already do.*

| Initiative | Reach | Impact | Confidence | Effort | RICE (baseline) |
|---|---|---|---|---|---|
| Rail PNR Confirmation Guarantee expansion | 6.0 | 2 | 0.7 | 5 | **168.0** |
| Direct Hotel Supply expansion (Brevistay) | 5.0 | 2 | 0.6 | 6 | **100.0** |
| **ixigo Corridor (this proposal)** | 8.5 | 2.5 | 0.4 | 10 | **85.0** |
| Flight NDC/direct-content take-rate recovery | 3.0 | 2 | 0.5 | 5 | **60.0** |

**Stressed** (4.92% applied to Reach for the three initiatives requiring travellers to discover new behaviour; the NDC/direct-content deal is exempt — it recovers margin on bookings travellers already make, with no new behaviour required):

| Initiative | Stressed RICE | Rank |
|---|---|---|
| Flight NDC/direct-content take-rate recovery | **60.0** | 1st (unchanged — exempt) |
| Rail PNR Confirmation Guarantee expansion | 8.26 | 2nd |
| Direct Hotel Supply expansion | 4.92 | 3rd |
| **ixigo Corridor** | **4.18** | **4th — last** |

Under a stress that treats discovery as the real constraint rather than the theoretical Reach number, **ixigo Corridor falls from 3rd of 4 to last**, behind a backend commercial initiative (flight direct-content deals) the case study did not propose. That result is kept in, not smoothed over: a prioritisation exercise that always ranks the author's own idea first isn't measuring anything.

## 48. MoSCoW

**Must:** live price and time for every corridor-eligible mode, shown before the traveller commits to a search tab. **Should:** in-flow booking without leaving the comparison (no re-search). **Could:** saved corridor preferences for repeat routes. **Won't (this phase):** dynamic re-routing after booking, or auto-switching a traveller's mode without explicit action.

## 49. Kano

The baseline expectation (a traveller can search each mode) is already met. A cross-modal price/time comparison is a **performance** feature today (more of it is better, in proportion) but has the shape of a future **delighter** if it is fast and trustworthy enough that travellers start a search on ixigo specifically because of it, rather than choosing a mode-specific app first.

## 50. Feature Proposal — ixigo Corridor

**ixigo Corridor** treats the origin-destination pair — not the mode — as the unit that gets searched, priced and compared. A traveller enters a corridor once; Corridor shows live price and door-to-door time for every mode genuinely serving it, ranked by the traveller's own stated priority (cheapest, fastest, or a blended default), and lets them book any of them without leaving the comparison. A **Ground Card** makes the time comparison honest by including realistic access/egress time (airport transfer, station approach) alongside the ticketed travel time, not just gate-to-gate or platform-to-platform duration. The top 200 highest-volume corridors get a named **corridor P&L owner** — someone accountable for RCJ/1k and contribution margin on that specific route, rather than corridors being nobody's job because they cut across three vertical teams.

## 51. PRD (abridged)

**Problem:** travellers on multi-mode corridors choose a search tab, not a corridor, and cannot see what they gave up. **Goal:** RCJ/1k above a defined floor on the top 200 corridors within two quarters, without degrading booking completion rate on any single mode. **Non-goals:** replacing mode-specific search (Corridor is additive); auto-selecting a mode for the traveller. **Success metric:** RCJ/1k (§31), guarded by GTP-90. **Out of scope for v1:** international corridors, corridors involving hotels/multi-leg trips.

## 52. Wireframes (ASCII)

```
 [ Delhi ] -> [ Jaipur ]                 Sat, 12 Sep

 GROUND CARD — total door-to-door time and cost

 FLIGHT   1h 05m air + 55m transfers  =  2h 00m   ₹4,850
 TRAIN    4h 40m + 15m station        =  4h 55m   ₹1,120
 BUS      5h 10m + 10m boarding       =  5h 20m     ₹650

 [ Book Flight ]   [ Book Train ]   [ Book Bus ]
 -- comparison stays visible until you book --
```

## 53. Rollout Plan / Phase 0

Phase 0 is a **2 analyst-week** exercise on the top 20 corridors, using data ixigo already holds (fare feeds, schedule data, historical booking mix by corridor). **K1:** if fewer than 15% of eligible searches on the pilot corridors show any engagement with the comparison view, kill. **K2 — named most likely to fire:** if the projected contribution-margin uplift from corridor-routed bookings does not exceed the cost of maintaining live, accurate cross-modal data for those corridors, kill; flight take rates are already thin, and the value case rests on volume that must first be proven. **K3:** if reliable NDC/GDS flight content, live rail PNR data and bus operator inventory cannot be secured on acceptable terms for at least 15 of the 20 pilot corridors, kill on data-availability grounds.

## 54. A/B Testing

**Arm C (Corridor):** full price/time comparison with in-flow booking, as designed. **Arm E (falsification arm):** a minimal banner on the existing single-mode search results ("this route is also served by train/bus — tap to compare") with no dedicated comparison screen, deliberately built to be far cheaper and to test whether the value is in the *comparison* or merely in the *awareness that alternatives exist*. **R1 (pre-registered decision rule):** proceed to full build only if Arm C beats Arm E by more than 8 percentage points on RCJ/1k across two full booking cycles including one non-peak month, with GTP-90 no worse than baseline in both arms.

## 55. KPI Dashboard — early-warning row

Track flight gross take rate quarter over quarter against West Asia conflict-linked fare/oil-price indicators. If take rate recovers toward 9%+ as fare inflation subsides and flight contribution margin returns to positive YoY growth, the flight-side rationale for A1 (§65 / ASSUMPTIONS Part 1) was macro, not structural — Corridor's value would then rest more on genuine cross-modal convenience than on defending margin, and should be re-scoped accordingly rather than declared a failure.

## 56. Product Roadmap

ixigo's own disclosed near-term roadmap, separate from this case study's proposal: continued Brevistay-driven direct hotel supply expansion, continued AI infrastructure investment in TARA, and — per CEO Aloke Bajpai's own August 2026 comments — active exploration of a **dedicated small-business and corporate travel product**, motivated explicitly by organic GST-registered business usage already showing up on the consumer app. That move is a real, disclosed strategic direction, not an author construct, and it sits naturally alongside Corridor rather than in competition with it: a corporate traveller is, if anything, a more valuable corridor-comparison user than a leisure traveller, since time has a harder cost for them than price does.

## 57. Risks & Mitigation

**Risk:** flight fare inflation continues or worsens, and Corridor's flight-diversification value never gets to prove itself against a recovering baseline. **Mitigation:** the falsification design in §54 tests convenience value independent of the flight-margin story, so the proposal does not depend on flights staying weak. **Risk:** corridor P&L ownership creates internal turf conflict across three formerly separate vertical teams. **Mitigation:** named ownership is scoped to the top 200 corridors only, not a reorg of the vertical teams. **Risk:** GTP-90 time estimates prove unreliable in practice (traffic, delays) and erode trust faster than the comparison builds it. **Mitigation:** the automatic suppression rule in §31 is designed precisely for this failure mode.

## 58. Future Vision

If Corridor works, the natural extension is folding hotels and the emerging corporate-travel product into the same corridor object — a business traveller comparing a same-day flight against an overnight train-plus-hotel combination is a genuinely different and richer comparison than mode-vs-mode alone, but it is out of scope for a v1 built to prove the simpler case first.

## 59. PM Lessons

**Test the disclosed number against a same-quarter comparator before writing the finding.** MakeMyTrip's own air revenue fell in the same quarter as ixigo's flight take-rate compression — a company neither controls the other, and both moved together, which is stronger evidence of a shared macro cause than either company's disclosure alone. **A "gross take rate" and a "revenue/GTV take rate" can both be true and not reconcile** — §39's flagged conflict is a reminder to report two disclosed figures side by side rather than force one number to explain both. **When management names its own explanation ("fare inflation from the West Asia conflict"), that is data, not a thing to argue past** — it became the basis of the early-warning row in §55 rather than being dismissed.

## 60. PM Interview Questions

1. How would you design a metric that only rewards a cross-modal comparison feature for showing travellers *cheaper* options, not merely different ones?
2. ixigo's Adjusted EBITDA fell while headline EBITDA rose 65%. Walk through how you would explain that gap to a board that only reads the headline number.
3. Design a Phase 0 test for a feature that requires data from three previously separate product teams. What is the cheapest way to learn if it's worth building before asking any of those teams to integrate deeply?

## 61. References

ixigo Q1 FY27 and Q1 FY26 investor disclosures and media releases (rocket.ixigo.com); Business Standard, Entrackr, Inc42, Investing.com, TourismQuest, TodaysTraveller coverage of Q1 FY27 results (all Aug 2026); Skift, "Ixigo's Next Shift: It's Exploring a Move Into Corporate Travel" (6 Aug 2026); Whalesbook coverage of the Q1 FY27 stock reaction (flagged as a partial conflict, Appendix A-3); MakeMyTrip Q1 FY27 earnings release and Entrackr/Whalesbook coverage; DGCA July 2026 domestic traffic data via Deccan Herald; thecompanycheck.com corporate filing summary for CIN verification.

## 62. About the Author

Gaurav — this is Day 59 of a 90-day series of independently researched, source-verified Product Management case studies, published to a public GitHub portfolio.

## 63. License

This case study is released for portfolio and educational use. All company data is drawn from public disclosures and is cited; no confidential information is used or implied.

## 64. Self Review

This case study leans more heavily on primary company disclosures (official investor PDFs, multi-source-corroborated press coverage) than any prior entry in the series, which is a strength — but it also means the RICE inputs and the Corridor proposal itself are more clearly the author's own construction layered on top of very solid facts, and that boundary is kept explicit throughout rather than blurred. The weakest link is A1 (§65 / ASSUMPTIONS Part 1): whether flight margin compression is temporary (macro) or durable (structural) cannot be resolved from one quarter of data, and the case study says so rather than picking the more convenient reading.

## 65. Appendix

**A — Source Conflicts.**
**A-1 (CIN).** Multiple aggregator sites show different CINs for the same entity: `L63000HR2006PLC071540` (current, listed — used throughout this document, corroborated by thecompanycheck's FY2026 profile), `U72300HR2006PTC071540` (Cleartax, appears to be a stale pre-listing/different-NIC-code snapshot), and an older `U63000HR2006PLC071540` marked "Unlisted" on some aggregators (pre-IPO record, not updated post-2024 listing). The listed CIN is used as authoritative here.
**A-2 (take rate).** Flight "gross take rate" (9.17%→8.41%, ixigo's own disclosed figure) and flight revenue/GTV (4.47%, this document's own calculation from disclosed revenue and GTV) do not reconcile to the same base and are both reported rather than forced to agree — see §39.
**A-3 (stock reaction).** One secondary source (Whalesbook) reported a 15% single-day stock decline and a "6.8% vs 9.4% expected" EBITDA-margin miss on results day; the primary business-press source used throughout this document (Business Standard) reported a 4.71% decline the same day, and no combination of this document's verified EBITDA/Adjusted EBITDA figures reconciles cleanly to 6.8%/9.4% on any disclosed base. The specific magnitude is therefore not used as a load-bearing fact; only the *direction* (a negative market reaction despite record headline profit, corroborated by both sources) is relied upon.

**B — Evidence Grades.** 🟢 High: all Q1 FY27/Q1 FY26 headline figures (GTV, revenue, PAT, EBITDA, Adjusted EBITDA, interest income, segment GTV/revenue/CM), corroborated across 3+ independent sources including ixigo's own investor PDF for the prior-year quarter. 🟡 Medium: Q1 FY26 PAT (₹18.94 Cr) — not in the official Q1 FY26 PDF (which disclosed PBT only), but converges across three independent press sources. 🟠 Low: CFO identity (carried from prior research, not independently re-verified this session); the Whalesbook margin-miss figures (A-3). 🔴 Conflicting: CIN (A-1), take-rate base (A-2), stock-reaction magnitude (A-3).

**C — Author-Constructed Content.** See `ASSUMPTIONS.md` Part 3 for the full list (personas, RICE inputs beyond the stress multiplier, ixigo Corridor and all of §50–54, RCJ/1k and GTP-90, the Kill criteria and decision rule).

**D — Asset Status.** No images or diagrams included; ASCII wireframe in §52 substitutes for a visual mockup, consistent with house style since Day 50.

---

*Day 59 of 90 · [← Day 58 — Delhivery](../Day-58-Delhivery) · Day 60 →*
