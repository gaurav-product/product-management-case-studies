# Day 74 — Medi Assist: Selling the Capability to the People Who Might Replace You

> Medi Assist administers health insurance claims on behalf of insurers, and this quarter it administered **26.8% more premium** than a year ago. Revenue grew **24.1%**, EBITDA **14.3%**. Run those against each other and the cascade is exact: revenue per rupee of premium fell **2.13%**, EBITDA per rupee of revenue fell **7.90%**, and the two compound to **EBITDA per rupee of premium down 9.86%**. More premium, less economics from each rupee of it. Reported profit rose 21.9%, but **₹3.12 Cr of that — 11.30% — was a one-time derivative gain** from buying more of a subsidiary; adjusted, profit grew **8.17%**, and the reported figure is **2.69×** the underlying one. Underneath sits the structural question. Medi Assist's customers are insurers, and insurers are increasingly able to bring claims administration in-house. Its answer is to **license its technology to those same insurers** — a hedge currently worth **3.3% of revenue**. The defence against being disintermediated is one-thirtieth of the business.

---

## 1. Cover

**Product:** Medi Assist — third-party administration of health insurance claims; MAtrix platform; Mayfair international
**Legal entity:** Medi Assist Healthcare Services Limited · **CIN:** L74900KA2000PLC027229
**Domain:** Healthtech — health benefits administration
**Period examined:** Q1 FY27 (quarter ended 30 June 2026), results 8 August 2026
**Written:** 9 September 2026
**Author:** Gaurav Singh · Day 74 of 90

---

## 2. Repository Metadata

| Field | Value |
|---|---|
| Legal entity | Medi Assist Healthcare Services Limited |
| CIN | L74900KA2000PLC027229 |
| Incorporated | **7 June 2000, as "Net Logistics Private Limited"** |
| Registrar | RoC Karnataka at Bengaluru |
| Renamed | Medi Assist Healthcare Services Private Limited, 21 November 2012 |
| Converted to public limited | Fresh certificate of incorporation, 20 March 2018 |
| Registered & corporate office | Tower D, 4th Floor, IBC Knowledge Park, 4/1 Bannerghatta Road, Bengaluru 560029, Karnataka |
| Listing | NSE **MEDIASSIST** |
| NIC code | **74900 — "Business activities n.e.c."** |
| CEO & Whole-Time Director | Satish V. N. Gidugu |
| Chairman (Non-Executive) | Dr. Vikram Jit Singh Chhatwal — promoter; demitted Whole-Time Director office 8 August 2026 |
| Key subsidiaries | Medi Assist Insurance TPA · Raksha TPA · Paramount Health Services and Insurance TPA · Mayfair We Care |
| Authorised / paid-up capital | ₹45.35 Cr / ₹35.10 Cr 🟡 |

**Two registry notes.** The company was incorporated as **Net Logistics Private Limited** — a logistics name for what became India's largest health-claims administrator, twelve years before the name changed. And the NIC code is **74900, "business activities not elsewhere classified"**: a residual category, for a company processing a large share of India's group health claims. Across eleven consecutive case studies this series has now found **nine codes that do not describe the business and two that do** — Akums on Day 71 and Rainbow on Day 73. The register is wrong most of the time, not all of the time, and both halves get reported.

---

## 3. Badges

`Day 74/90` · `Healthtech` · `Health benefits administration (TPA)` · `Listed (NSE)` · `Q1 FY27 primary` · `EBITDA per rupee of premium −9.86%` · `107 programmatic checks, all passing` · `Zero fabricated figures`

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

Medi Assist reported the quarter ended 30 June 2026 on 8 August, with the earnings call on 10 August. Consolidated revenue from operations was **₹236.52 Cr, up 24.12%**. EBITDA was ₹48.0 Cr, up 14.3%, at a **20.29%** margin against 22.0% a year earlier. Reported profit after tax was ₹27.60 Cr, up **21.94%**. Consolidated EPS rose 16.67% to ₹3.71. The company is debt-free, declared a ₹2 final dividend for FY26, and the stock fell **5.32%** to ₹345.55 on the day.

The operating achievement is real. Group market share reached **37.6%**, India health premiums under management grew **26.8%**, the Paramount integration is effectively complete with **over 95% of group claims and over 80% of retail claims** migrated to the MAtrix platform, and this was the fourth consecutive quarter of sequential margin improvement. Technology revenue grew **55.5%**, with seven AI contracts signed. None of that is manufactured.

But three things sit uncomfortably together.

**First, the economics per unit of the thing being administered are compressing.** A TPA earns a fee against premium. Premium under management grew 26.8%; revenue grew 24.12%; EBITDA grew 14.3%. So revenue per rupee of premium fell **2.13%**, EBITDA per rupee of revenue fell **7.90%**, and the two compound exactly to **EBITDA per rupee of premium down 9.86%**. Because the stages multiply to the whole, all three disclosed growth rates check against one another — this is arithmetic, not interpretation.

**Second, the profit growth is mostly not operational.** Reported PAT rose 21.94%, but ₹3.12 Cr of it was a one-time gain on remeasuring a derivative liability when Medi Assist bought an additional 31.75% of Mayfair We Care. That is **11.30% of reported PAT**. Excluding it — as the company itself does in its adjusted figure — profit grew **8.17%**. The reported number is **2.69×** the adjusted one. And EPS grew 16.67% against PAT's 21.94%, implying a share count roughly **4.52%** larger.

**Third, and the reason this is a product case study rather than an earnings note: the customer can become the competitor.** Medi Assist's clients are insurers. Claims administration is exactly the function a large insurer can build internally, and management acknowledged that pressure directly. The company's answer is to **license its technology to insurers** — to sell the capability to the parties most likely to replace it. That business is growing 55.5% and is **3.3% of consolidated revenue**. The hedge against disintermediation is currently one-thirtieth of the business, and the core TPA franchise is **92.43%**.

This is not a company in difficulty. It is debt-free, gaining share, and executing an integration well. It is a company whose unit economics are drifting in the wrong direction while its strategic answer is small — and whose most defensible asset may not be the one it is productising. The proposal, *Network Ledger*, argues for the other asset. It is designed, costed, and then ranked last by a wide margin.

---

## 6. Product Overview

Medi Assist is a third-party administrator: it sits between health insurers and their policyholders, and between insurers and hospitals. It enrols members, issues cards, runs pre-authorisation, adjudicates and settles claims, manages the cashless hospital network, and handles fraud, waste and abuse detection. It is paid a fee by the insurer, typically as a percentage of premium administered.

The structural feature that defines this analysis is that **Medi Assist has two distinct assets and only one of them is hard to replicate.** Claims processing is software and process — buildable by a determined insurer. The hospital network, with its negotiated tariffs and settlement history accumulated across many insurers at once, is not something any single insurer can reconstruct alone.

---

## 7. Company Background

The entity was incorporated on 7 June 2000 as Net Logistics Private Limited, renamed Medi Assist Healthcare Services Private Limited in November 2012, and converted to a public limited company in March 2018. It listed on the NSE in January 2024. Dr. Vikram Jit Singh Chhatwal is the promoter and, from 8 August 2026, Non-Executive Chairman, having stepped back from the Whole-Time Director role; Satish Gidugu is CEO and Whole-Time Director.

Growth has been substantially inorganic within the TPA franchise: Raksha TPA was acquired in August 2023 and Paramount Health Services and Insurance TPA subsequently, with the Paramount integration reaching completion in the quarter examined. Alongside sit two newer tracks — technology licensing, and an international platform through Mayfair We Care, in which the company acquired an additional 31.75% effective 1 July 2026.

---

## 8. Product Timeline

| Date | Event |
|---|---|
| 7 Jun 2000 | Incorporated as Net Logistics Private Limited, RoC Bengaluru |
| 21 Nov 2012 | Renamed Medi Assist Healthcare Services Private Limited |
| 20 Mar 2018 | Converted to public limited company |
| 25 Aug 2023 | Raksha TPA acquired |
| Jan 2024 | IPO; listed on NSE |
| 4 Apr 2025 | Enforcement Directorate search and seizure at Medi Assist Insurance TPA offices, Ranchi — auditor emphasis of matter |
| FY26–FY27 | Paramount Health Services and Insurance TPA integration; migration to MAtrix |
| 1 Jul 2026 | Additional 31.75% of Mayfair We Care acquired; ₹3.12 Cr derivative remeasurement gain |
| 8 Aug 2026 | Q1 FY27 results; Dr. Chhatwal demits Whole-Time Director office; Gaurav Bhatnagar joins as Chief TPA Officer |
| 10 Aug 2026 | Earnings call: seven AI contracts, Thailand deployment live, margin recovery guided to end FY27 |

---

## 9. Vision & Mission

Management describes a three-horizon strategy: extract operating leverage from the post-Paramount India TPA platform; scale AI licensing across contracted insurers; and build an international platform through Mayfair. Both growth tracks are explicitly funded from internal cash flows without recourse to external capital, and management expects EBITDA margin to recover toward the historical **23%** level by end FY27.

The framing is disciplined and the funding constraint is a genuine mark of quality. What the vision does not address is the tension this case study examines: **horizon two sells the company's core capability to the customers of horizon one.** That may be exactly right — better to be paid for the disintermediation than to suffer it — but it is a strategic choice worth naming rather than presenting as a straightforward growth track.

---

## 10. Problem Statement

**For Medi Assist:** its fee is a share of premium, and its economics per rupee of premium fell 9.86% while premium grew 26.8%. Scale is arriving faster than the value captured from it.

**For the insurer:** claims administration is a cost centre with real strategic content — pricing, fraud detection, member experience — and the larger the insurer, the more attractive it becomes to own that capability rather than rent it.

**The intersection:** Medi Assist's most replicable asset is the one it is currently licensing, and its least replicable asset — a hospital network and tariff history assembled across many insurers simultaneously — is bundled into the fee rather than sold on its own terms. **The company is productising the half that can be copied.**

---

## 11. Market Research

Indian health insurance is growing quickly, and Medi Assist's own figures show it: group premiums under management up **29.5%**, India health premiums up **26.8%**, and group market share at **37.6%**. A TPA's addressable market is a function of insured premium, and that base is expanding.

The structural feature that matters is who the TPA's customer is. **The buyer is the insurer, not the patient** — which means the TPA's competitive position depends entirely on insurers preferring to outsource. That preference is not fixed. It reflects a build-versus-buy calculation that shifts as insurers scale, as claims technology commoditises, and as regulators take more interest in claims outcomes. Day 66 of this series examined an insurer refusing risk it was paid to carry; Day 67 examined a hospital whose tariffs were set by insurers. **Medi Assist sits precisely between those two, adjudicating the boundary.**

---

## 12. Industry Analysis

TPA economics are fee-on-premium and therefore volume-scaled but price-taking. The fee rate is negotiated with insurers who have every incentive to compress it, and the compression shows: revenue per rupee of premium fell 2.13% this quarter alone.

The industry's defining hazard is **customer-driven vertical integration**. Unlike most B2B services, a TPA's client possesses both the motive and the raw material to replicate it — the insurer already owns the policy, the premium and the member relationship. Management explicitly flagged competitive pressure from insurers developing internal capabilities, and named technology offerings as the mitigation. That is a coherent response, and it means the company's medium-term position depends on a business currently generating **3.3% of revenue**.

---

## 13. TAM / SAM / SOM

*Framework note: run in restricted form. No primary-sourced Indian TPA market size was located that is not a vendor estimate, so this is sized from Medi Assist's own disclosed revenue and mix, annualised.*

| Layer | Definition | Size | Basis |
|---|---|---|---|
| TAM | Annualised revenue at the Q1 run rate | **₹946.08 Cr** | ₹236.52 Cr × 4 🟢 |
| SAM | Core TPA franchise | **92.43%** of revenue | Derived, D4f |
| SOM | Technology licensing — the hedge | **3.3%** of revenue, **₹31.22 Cr** annualised | Derived, D4c 🟢 |
| *The exposure* | Group market share administered | **37.6%** | 🟢 |

The bottom two rows are the strategic position stated as numbers: a franchise administering more than a third of the group market, defended by a business one-thirtieth its size.

---

## 14. Competitor Analysis

*Framework note: the comparison here is **internal — the core TPA franchise against the two growth tracks** — rather than against a listed peer, and that is a disclosure constraint rather than a preference. Medi Assist is the only listed pure-play TPA of scale in India; the competitors that matter most are its own customers' in-house teams, which publish nothing at all. What Medi Assist does disclose is segment growth and revenue share for technology and international alongside consolidated figures, which allows the three tracks to be separated exactly.*

| Track, Q1 FY27 | Core TPA | Technology | International (Mayfair) |
|---|---|---|---|
| Share of revenue | **92.43%** | **3.3%** | **4.27%** |
| Revenue | — | **₹7.81 Cr** | **₹10.10 Cr** |
| Growth | Consolidated **+24.12%** | **+55.5%** | **−5.2%** |
| Growth vs consolidated | — | **2.30×** | Negative |
| Contracts / status | 37.6% group market share | 7 AI contracts signed | Thailand deployment live |

Three readings. **The growth track is real but small.** Technology at 55.5% growth is running at **2.30×** the consolidated rate, which is what a successful new line should do — but ₹7.81 Cr in a quarter is **16.26%** of EBITDA and **₹1.12 Cr per signed contract**. At current scale it changes the narrative long before it changes the P&L.

Second, **the international track is going backwards**: Mayfair revenue fell 5.2% and is 4.27% of the company. Management attributed it to industry-wide moderation in student, leisure and marine volumes, which is plausible and outside the company's control. But the two hedges against core-business risk are, together, **7.57%** of revenue, and one of them shrank.

Third, and cutting against this case study's framing: **the core is not weak.** It gained share to 37.6%, grew premiums 26.8%, and completed a major integration with over 95% of group claims migrated. A reading that treats the TPA franchise as a melting ice cube has to account for a business taking share in a growing market. The compression is in the *rate*, not the volume — and rate compression on rising volume is an entirely survivable condition for years.

---

## 15. SWOT

| | |
|---|---|
| **Strengths** — 37.6% group market share; India health premiums up 26.8%; Paramount integration effectively complete with >95% of group claims on MAtrix; debt-free with positive operating cash flow; fourth consecutive quarter of sequential margin improvement; technology growing at 2.30× the consolidated rate | **Weaknesses** — EBITDA per rupee of premium down 9.86%; margin 2.70 points below the historical 23%; 11.30% of reported PAT is a one-time derivative gain; adjusted PAT growth of 8.17% against reported 21.94%; EPS growing 5.28 points slower than PAT |
| **Opportunities** — technology licensing at roughly double core-TPA margins; ₹6.40 Cr of EBITDA recoverable this quarter alone at the historical margin; hospital network and tariff history not currently productised; 20% of retail claims still to migrate | **Threats** — insurers in-sourcing the TPA function, acknowledged by management; fee-rate compression by clients who are also potential competitors; Mayfair revenue declining; ED search and seizure at a subsidiary with an auditor emphasis of matter |

---

## 16. Porter's Five Forces — run twice

*Framework note: run as a double pass on the two assets Medi Assist owns — **claims administration**, which an insurer could build, and the **hospital network and tariff book**, which it could not. The seam is chosen because the forces invert almost completely across it, and because the company is currently productising the left column while the right column sits inside the bundled fee.*

| Force | CLAIMS ADMINISTRATION (92.43% of revenue) | THE HOSPITAL NETWORK AND TARIFF BOOK |
|---|---|---|
| **Buyer power** | **Very high.** The insurer can build this, and every renewal is a build-versus-buy decision. Revenue per rupee of premium fell 2.13% | **Low.** No single insurer can assemble tariff and settlement history across all the others' volumes |
| **Rivalry** | Against other TPAs on fee rate, and against clients' own internal teams | Against nobody comparable — the asset is a by-product of administering 37.6% of the group market |
| **Substitutes** | An insurer's in-house claims team. Management named this explicitly | Building a hospital network from scratch, at a fraction of the leverage |
| **New entrants** | Software plus process; the barrier is falling as claims technology commoditises | **Effectively barred.** The asset accretes only with multi-insurer scale over years |
| **Supplier power** | Hospitals, moderate and diffuse | Hospitals, but **inverted** — Medi Assist negotiates with the aggregate volume of many insurers behind it |
| **What Medi Assist is licensing** | **This one** — the AI and MAtrix stack, 3.3% of revenue | **Not productised** |

The inversion is the finding and it is unusually stark. **The left column has weak defences and is where 92.43% of the revenue sits; the right column has strong defences and is not sold separately at all.** Licensing the left column is a rational response to disintermediation — better to be paid than displaced — but it accelerates the commoditisation of the thing being licensed. The right column has the opposite property: the more insurers Medi Assist serves, the more valuable and less replicable it becomes, because it is built precisely from serving many of them at once. §50 is an argument for moving the moat.
---

## 17. Business Model Canvas

| Block | Medi Assist |
|---|---|
| Value proposition | Administer health claims accurately, fast, at lower cost than an insurer can internally |
| Customer segments | **Insurers** — who pay the fee; corporates and policyholders are users, not buyers |
| Channels | MAtrix platform, hospital network, member apps and helplines |
| Revenue streams | TPA fee on premium (92.43%), technology licensing (3.3%), international (4.27%) |
| Key resources | MAtrix platform, claims data across 37.6% of the group market, **hospital tariff and settlement history** |
| Key activities | Enrolment, pre-authorisation, adjudication, settlement, fraud detection, network management |
| Key partners | Hospitals — and, uncomfortably, the insurers who are both customers and potential competitors |
| Cost structure | People-heavy claims operations, platform development, integration costs |
| **The unpriced asset** | **Multi-insurer hospital tariff and settlement history** |

The last two rows are §50. The partner row contains the strategic tension; the unpriced-asset row contains the answer to it.

---

## 18. Revenue Model

Medi Assist earns a fee as a share of premium administered, which makes revenue a function of insured volume and negotiated rate. Volume is going well — India health premiums up 26.8%, market share 37.6%. Rate is not: revenue per rupee of premium fell **2.13%**.

Below revenue the operating leverage ran backwards this quarter. EBITDA grew 14.3% against revenue's 24.12%, so EBITDA per rupee of revenue fell **7.90%** and margin landed at 20.29% against a historical 23.0%. **At the historical margin this quarter's revenue would have produced ₹54.40 Cr of EBITDA rather than ₹48.0 Cr — ₹6.40 Cr foregone in a single quarter.** Management attributes the gap to integration and expects recovery by end FY27, which is a specific and falsifiable claim.

The higher-margin line is technology, which management describes as carrying roughly double core-TPA margins. It is 3.3% of revenue and **16.26% of EBITDA** — already contributing disproportionately, and still small.

---

## 19. Target Users

Medi Assist's paying customer is an insurer's operations and claims leadership, buying on cost per claim, turnaround, fraud recovery and member satisfaction. Corporates buying group cover are influencers; policyholders are users who did not choose the TPA and cannot switch it.

The user this case study is most interested in is the one with no commercial relationship at all: **the hospital**. Medi Assist negotiates its tariffs, routes its cashless volume and settles its bills, across the business of many insurers simultaneously — and the hospital is a counterparty rather than a customer. That relationship is the company's least replicable asset and its least monetised one.

---

## 20. Personas

**A claims head at a mid-size insurer.** Buys TPA services today, and every renewal runs a build-versus-buy model. Medi Assist's technology licensing is aimed squarely at her, which is either a way to keep her or a way to help her leave.

**A hospital billing manager in a tier-2 city.** Deals with Medi Assist across several insurers' patients. Negotiates tariffs with it, chases settlements from it. Has no contract with Medi Assist and no bill from it — and is the counterparty in the asset §50 proposes to productise.

**A policyholder awaiting pre-authorisation.** Did not choose Medi Assist, cannot change it, and experiences it as the reason a cashless approval is fast or slow. The most affected party with the least power, which is why §40 puts adjudication quality before the proposal.

---

## 21. Jobs To Be Done

*Framework note: JTBD is used because the insurer hires Medi Assist for two jobs that are becoming separable, and only one of them is safe.*

| Job | Who | Current solution | Adequacy |
|---|---|---|---|
| "Process my claims cheaply and accurately" | Insurer | Core TPA service | **Well served — and increasingly replicable.** Fee rate down 2.13% per rupee of premium |
| "Give me claims technology I can run myself" | Insurer | Technology licensing, 7 contracts | Growing 55.5%, at 3.3% of revenue |
| "Get me hospital tariffs I could not negotiate alone" | Insurer | **Bundled into the TPA fee, not sold separately** | **Not served as a product** — the §50 gap |
| "Pay me fairly and on time" | Hospital | Network agreement | Served operationally, monetised not at all |
| "Approve my treatment quickly" | Policyholder | Pre-authorisation | Not measured publicly — §40 |

Rows one and three are the strategic pair. Row one is what Medi Assist sells and what an insurer can eventually build. **Row three is what an insurer cannot build and is not currently charged for separately.**

---

## 22. User Journey

| Stage | Policyholder experiences | Insurer experiences | Medi Assist earns |
|---|---|---|---|
| Enrolment | Card issued | Member data loaded | Fee on premium |
| Cashless request | Pre-authorisation wait | Exposure flagged | Same fee |
| Treatment | Care delivered | Liability incurred | Same fee |
| Settlement | Nothing to pay, if approved | Claim paid at network tariff | Same fee |
| Renewal | New card | **Build-versus-buy decision** | Fee renegotiated downward |

The last row is where the business model is decided, and the fee moves one way. Every other row is service delivery; that one is the commercial reality, and it is why rate compression appears as a steady 2.13% rather than a shock.

---

## 23. User Flow

The claims flow is: request → eligibility check → clinical adjudication → tariff applied → approval or denial → settlement. Medi Assist's platform work has concentrated here, and the migration numbers show it — over 95% of group claims and over 80% of retail claims now on MAtrix.

**The tariff step is the one with a moat.** Applying the right rate to the right procedure at the right hospital requires a negotiated tariff book built across many insurers' volumes. Every other step in the flow is process automation an insurer could buy or build; that one is an accumulated asset. It sits in the middle of the flow and nowhere in the price list.

---

## 24. Information Architecture

Disclosure is reasonable and improving: Medi Assist publishes premium under management, market share, segment revenue shares for technology and international, migration progress, and both reported and adjusted PAT — the last of which is what allows §5 to strip the derivative gain without estimating anything.

What is absent is anything about the network: no disclosed hospital count, tariff coverage, settlement turnaround, or the share of claims settled at negotiated versus ad-hoc rates. **The company reports the size of what it administers and nothing about the asset that makes administering it defensible.**

---

## 25. UX Audit

The experience that matters most is not the insurer's but the policyholder's, at the moment of a cashless pre-authorisation request. That is where a TPA is either invisible or infuriating, and it is not publicly assessable in any systematic way.

The observable gap is disclosure rather than design: **no turnaround time, approval rate, denial rate or appeal-overturn rate is published.** For a company whose entire function is adjudicating between an insurer's money and a patient's treatment, the absence of any published decision-quality measure is the most striking hole in the reporting, and §31 is partly an attempt to fill it.

---

## 26. UI Audit

MAtrix, the member apps and the hospital-facing portals are not disclosed in enough detail to audit, and this section does not invent one.

The point that bounds §50: **the interface that would carry the proposal already exists** — Medi Assist has authenticated relationships with insurers and hospitals through the same platform. The proposal is a commercial and governance construction, not an interface project.

---

## 27. Accessibility

The genuine access contribution is cashless treatment. A TPA that approves quickly converts an insurance policy into care a family can actually use without finding money first, and Medi Assist performs this across 37.6% of the group market.

The counterpoint is structural and unresolved: **the party whose access depends on the decision has no relationship with the decider.** The policyholder cannot choose the TPA, cannot switch it, and cannot see its record. Any strengthening of the TPA's position — including §50 — should be measured against whether that access improves, which is why §31's guardrail sits where it does.

---

## 28. Feature Breakdown

| Area | Current state |
|---|---|
| Core TPA | 92.43% of revenue; 37.6% group market share; premiums +26.8% |
| MAtrix platform | >95% of group claims, >80% of retail claims migrated |
| Technology licensing | 3.3% of revenue, +55.5%, 7 AI contracts signed |
| International | Mayfair, 4.27% of revenue, −5.2%; Thailand deployment live |
| Balance sheet | Debt-free; positive operating cash flow; ₹2 final dividend |
| Recent corporate | Additional 31.75% of Mayfair acquired 1 Jul 2026; ₹3.12 Cr derivative gain |
| **Network tariff product** | **Does not exist** |
| **Published adjudication-quality data** | **Does not exist** |
| **Hospital-side revenue line** | **Does not exist** |

The three absences at the bottom are the subject of §50, §31 and §46. All are verifiable from disclosure rather than assumed: nothing in the results, presentation or earnings-call coverage describes a network or tariff product, any published claim-decision metric, or any revenue earned from hospitals.

---

## 29. AI Capabilities

Medi Assist describes an AI stack that has moved from investment to early monetisation, with seven contracts signed with insurers, and technology revenue growing 55.5%. Management expects it to carry roughly double the margin of core TPA contracts.

The strategic observation, rather than a technical one: **the AI stack is trained on claims data generated by administering insurers' business, and is being sold back to insurers.** That is a reasonable monetisation of a by-product — the same shape this series examined at Akums on Day 71. The difference is that Akums's clients could not use the insight to replace Akums, whereas an insurer buying claims-adjudication AI is buying a component of the thing it currently outsources.

---

## 30. Product Metrics

| Metric | Q1 FY27 | Note |
|---|---|---|
| Revenue from operations | ₹236.52 Cr | **+24.12%** computed |
| EBITDA | ₹48.0 Cr | +14.3%; margin **20.29%** vs 22.0% and historical 23.0% |
| Reported PAT | ₹27.60 Cr | **+21.94%** computed |
| **Adjusted PAT** | **₹24.48 Cr** | **+8.17%** — reported is **2.69×** adjusted |
| Derivative gain | ₹3.12 Cr | **11.30%** of reported PAT |
| EPS | ₹3.71 | +16.67%; **5.28 pp** below PAT growth, implying **+4.52%** shares |
| India health premiums | +26.8% | Group market share **37.6%** |
| **Revenue per rupee of premium** | **−2.13%** | Derived |
| **EBITDA per rupee of revenue** | **−7.90%** | Derived |
| **EBITDA per rupee of premium** | **−9.86%** | Derived; the two stages compound exactly |
| Technology | 3.3% of revenue, +55.5% | ₹7.81 Cr; **16.26%** of EBITDA |
| Mayfair | 4.27% of revenue, −5.2% | ₹10.10 Cr |
| Standalone PAT | ₹13.15 Cr | +63.99%; **47.66%** of consolidated PAT |

**The cascade is the finding and it is self-checking.** (revenue ÷ premium) × (EBITDA ÷ revenue) = EBITDA ÷ premium, and −2.13% compounded with −7.90% gives −9.86% exactly. Three separately disclosed growth rates validate one another.

---

## 31. North Star Metric

Medi Assist's implied north stars are premium under management and market share. Both rose strongly while the economics per rupee of premium fell 9.86% — which is precisely the failure a volume metric cannot detect.

**Proposed North Star — NLC/1k: Network-Licensed Covered lives per 1,000 covered lives administered.**

A covered life counts in the numerator only if **all four** hold:
1. the insurer holds a **separate, separately-priced licence** to the network and tariff product, distinct from any TPA administration contract;
2. the licence is live and billing, not a pilot;
3. the insurer's claims for those lives are being adjudicated against the licensed tariff book;
4. the licence would survive the insurer terminating its TPA administration contract.

**The denominator is the design choice.** It is *covered lives administered* — so winning more administration work without licensing the network **lowers** the metric. Medi Assist cannot improve NLC/1k by doing more of the thing that is being commoditised. Condition 4 is the whole point: it counts only revenue that survives disintermediation, which is the exact risk the metric exists to measure.

**Guardrail — TDR-90: Tariff Dispersion at the 90th percentile of hospital concentration.** In the decile of districts where Medi Assist's share of a hospital's insured volume is highest, the dispersion of negotiated tariffs across the insurers it serves, measured per procedure and reported **by district, never in aggregate**. **A collapsing dispersion is the alarm**, because convergence of rates across competing insurers mediated by a single intermediary is what price coordination looks like from the outside. Owned by compliance with no revenue target, with automatic suspension of tariff-sharing in any district that breaches.

That guardrail is not decoration. A single party negotiating hospital rates on behalf of a third of the group market, and then selling that rate book to those insurers, sits close to a competition-law problem. §40 sets out why it has to be engineered against before the product exists.

---

## 32. Product Analytics

Medi Assist holds, per claim, the hospital, the procedure, the negotiated rate, the approval decision, the turnaround and the settlement date — across the business of many insurers at once. That is the raw material for both §50's product and §31's guardrail, and it exists as an operational by-product.

The analytics gap is that **none of it is reported in any form.** No network size, no tariff coverage, no settlement turnaround, no decision-quality data. A company whose defensibility rests on a network asset publishes nothing about that asset, which is the disclosure point §55 turns into a tracked metric.

---

## 33. AARRR

*Framework note: applied to the insurer relationship, because that is the funnel where the business is won and lost.*

| Stage | Reading |
|---|---|
| Acquisition | Strong — 37.6% group market share, premiums +26.8%, share gained through acquisition and organic wins |
| Activation | Strong — Paramount integration complete, >95% of group claims migrated to MAtrix |
| **Retention** | **The strategic question** — every renewal is a build-versus-buy decision; rate down 2.13% per rupee of premium |
| Revenue | +24.12%, but EBITDA per rupee of premium −9.86% |
| Referral | Not applicable in a concentrated B2B market |

Every stage reads well except the one that decides the company's future. **Retention here is not churn — it is the risk that a retained client keeps the volume and takes the function**, which no conventional retention metric would show. NLC/1k's fourth condition exists to measure exactly that.

---

## 34. HEART

| Dimension | Medi Assist |
|---|---|
| Happiness | Not disclosed; no policyholder satisfaction or NPS published |
| Engagement | Not applicable in the usual sense; claims volume is not a preference |
| Adoption | MAtrix migration >95% group, >80% retail; 7 AI contracts |
| Retention | Not disclosed at insurer level; market share is the proxy |
| **Task success** | **Not defined** — no approval rate, turnaround or appeal-overturn data published |

Task success is the meaningful absence, and in this business it is unusually consequential. For a TPA, task success is whether a valid claim was approved quickly — which is simultaneously the insurer's cost question, the patient's access question, and the regulator's fairness question. None of it is published.

---

## 35. Growth Strategy

The stated strategy is three horizons: operating leverage from the integrated India TPA platform, AI licensing to insurers, and an international platform through Mayfair — with both growth tracks funded from internal cash flow and margin recovery to **23%** guided by end FY27.

**Checking whether the proposal already exists, from the company's own disclosures.** Nothing in the Q1 FY27 results, investor presentation or earnings-call coverage describes a separately-licensed network or tariff product, any revenue earned from hospitals, or any published adjudication-quality data. The technology being licensed is the claims and AI stack. The §50 instrument does not exist today.

**The arithmetic worth recording.** Recovering the historical 23% margin on this quarter's revenue is worth **₹6.40 Cr of EBITDA in a single quarter** — comfortably more than technology's entire ₹7.81 Cr of quarterly revenue, and requiring no customer to buy anything. That is why §47 ranks integration leverage first by a very large margin.

---

## 36. Growth Loops

The intended loop works and is visible in the numbers: **more insurers → more premium administered → more scale in claims operations → lower unit cost → more competitive fee → more insurers.** Market share at 37.6% is the output.

There is a second loop the strategy has deliberately started, and its direction is worth naming. **Technology licensing → insurers gain in-house capability → the outsourced function becomes more replicable → fee pressure on the core → more need for technology revenue.** That is not necessarily wrong — being paid for the transition beats being displaced by it — but it is self-reinforcing in a way the growth framing does not acknowledge. The loop that would run the other way is the network one: **more insurers served → richer multi-insurer tariff book → more valuable to each insurer → harder to leave.** That loop exists operationally and is not monetised, which is the whole argument of §50.

---

## 37. Network Effects

Medi Assist has a genuine, and genuinely under-used, network effect. Each additional insurer served adds volume to the hospital negotiation, which improves tariffs for every other insurer served, which makes the proposition stronger for the next one. **That is a real increasing-returns dynamic and it is the only part of the business an insurer cannot replicate alone.**

The claims-processing side has no such property: a bigger TPA processes claims more cheaply, which is scale economics, not a network effect. **The company is licensing the side with scale economics and bundling the side with network effects into a fee that is being negotiated down 2.13% a year.** §50 proposes reversing that.

---
## 38. Product Strategy

Medi Assist's strategy is competently executed and, on one axis, arguably pointed at the wrong asset. The core franchise is winning — 37.6% share, premiums up 26.8%, a major integration delivered. The balance sheet is clean and both growth tracks are funded internally, which is a real discipline.

The strategic gap is what is being productised. **Technology licensing sells the replicable half of the business to the parties most able to replicate it**, while the non-replicable half — a multi-insurer hospital tariff and settlement book — is bundled into a fee falling 2.13% per rupee of premium per year. Both moves can be right; only one of them gets stronger as insurers get more capable. §50 argues for the second.

---

## 39. Monetization

Medi Assist monetises premium administered. That base grew 26.8% while revenue grew 24.12% and EBITDA 14.3%, so the take rate fell at every stage — **9.86% compounded on EBITDA per rupee of premium**.

The monetisation constraint is that **the fee is negotiated with a counterparty that has an alternative.** Price rises are not available; the insurer's fallback is to build. The two escapes are cost (integration leverage, worth ₹6.40 Cr a quarter at the historical margin) and a second revenue line the insurer cannot substitute. Technology is the second line today at 3.3% of revenue; §50 proposes a third that is structurally harder to replace.

---

## 40. Trust & Safety

*Placed before §50 deliberately, because the proposal would have one intermediary sell a hospital rate book to competing insurers, and that is a competition-law and patient-access question before it is a revenue one.*

**Tariff coordination is the serious risk.** A single party negotiating hospital rates on behalf of insurers holding a third of the group market, then licensing that rate book back to those insurers, is close to a mechanism by which competitors' input prices converge. The harm lands on hospitals first and patients second. The mechanic: **TDR-90 monitors tariff dispersion across insurers per procedure, by district, at the 90th percentile of Medi Assist's share of a hospital's insured volume — and a collapsing dispersion triggers automatic suspension of tariff-sharing in that district.** Compliance owns the threshold; no one with a revenue target may vary it.

**Hospital squeeze.** The same aggregated leverage that makes the asset valuable could be used to push tariffs below sustainable levels, particularly at smaller hospitals with no alternative volume. The mechanic: licensing covers **historical settlement and quality data plus tariff bands**, never a coordinated rate floor or ceiling, and hospitals may see and contest their own data — §48 places any single group-wide rate out of scope permanently.

**Patient access is the unmeasured party.** The policyholder cannot choose the TPA, cannot switch it, and has no visibility of its decision record. Strengthening Medi Assist's position without measuring adjudication quality would make an already asymmetric relationship worse. The mechanic: **§51 makes publication of approval rate, turnaround and appeal-overturn rate a precondition of the product**, not a later refinement — the proposal buys its own accountability.

**The governance context is live, not hypothetical.** The statutory auditors recorded an emphasis of matter regarding an Enforcement Directorate search and seizure at Medi Assist Insurance TPA offices in Ranchi in April 2025. Management stated there is no adverse impact and no adjustment was required, and the auditors issued an unmodified review report — so nothing here suggests wrongdoing. It does mean this is a company whose conduct is already under external scrutiny, which raises rather than lowers the bar for any product that concentrates market power.

**The incentive that must be excluded, stated plainly.** If NLC/1k is targeted without TDR-90 gating it, the fastest route to the metric is licensing the richest possible rate data to the largest possible number of insurers — which is exactly the direction that produces coordination. §53 makes the TDR-90 baseline a precondition of licensing in each district.

---

## 41. Technical Architecture

The relevant systems are MAtrix — now carrying over 95% of group claims and over 80% of retail claims — plus the network management, tariff and settlement systems, and the AI stack being licensed.

What §50 requires is not new infrastructure but a **separable tariff and settlement data product**: the ability to expose network data to a licensee without exposing any individual insurer's claim-level book, and without the licence depending on the licensee also being an administration client. Condition 4 of NLC/1k is a technical requirement as much as a commercial one — the product must work for an insurer that has left.

---

## 42. Data Flow

Today: claim → adjudication → tariff applied → settlement → data retained operationally. The tariff book accretes as a by-product and never leaves the building as a product.

Under the proposal: the same operational flow, plus a governed branch — settlement history → insurer-identity stripped at ingestion → aggregated to procedure and district → **TDR-90 dispersion check** → published tariff bands and quality data to licensees. The critical constraint is directional and absolute: **no individual insurer's negotiated rate may be inferable by another, and the dispersion thresholds are writable only by compliance** — enforced by access control and build-pipeline test.

---

## 43. API Ecosystem

Medi Assist already operates authenticated interfaces with both sides: insurers through MAtrix and the licensing contracts, hospitals through network and settlement systems. The delivery surface for §50 exists.

The asymmetry worth naming: **Medi Assist has a commercial relationship with one side of its network and an operational one with the other.** Insurers pay; hospitals are negotiated with. Every rupee of revenue comes from the side that could replace it, and none from the side that cannot.

---

## 44. Privacy & Security

Claims data is health data, and it is the most sensitive category under India's DPDP framework. Any network product must be built from settlement and tariff information rather than patient records, and §51 makes that a hard requirement rather than a design preference.

The second sensitivity is commercial confidentiality between competing insurers. **An insurer's negotiated rates and claims patterns are commercially confidential from its rivals**, and Medi Assist holds all of them. The design position is that licensing exposes aggregated bands and dispersion, never an identifiable competitor's position — which is the same constraint that TDR-90 measures from the other direction.

---

## 45. Pain Points

| # | Pain point | Evidence |
|---|---|---|
| P1 | EBITDA per rupee of premium down 9.86% | Derived, D2c 🟢 |
| P2 | Revenue per rupee of premium down 2.13% | Derived, D2a 🟢 |
| P3 | Adjusted PAT grew 8.17% against reported 21.94% | Derived, D1d, D1e 🟢 |
| P4 | 11.30% of reported PAT is a one-time derivative gain | Derived, D1f 🟢 |
| P5 | Margin 2.70 points below the historical 23% | Derived, D3c 🟢 |
| P6 | Insurers in-sourcing the TPA function | Management commentary 🟡 |
| P7 | The hedge against in-sourcing is 3.3% of revenue | Derived, D4a 🟢 |
| P8 | Mayfair revenue down 5.2% | Company disclosure 🟢 |
| P9 | EPS growing 5.28 points slower than PAT | Derived, D1h 🟢 |
| P10 | No network, tariff or adjudication-quality data published | Absence across all Q1 FY27 disclosures 🟢 |
| P11 | ED search and seizure with auditor emphasis of matter | Auditor's report 🟡 |

---

## 46. Opportunity Mapping

| Opportunity | Annualised revenue addressed | Requires |
|---|---|---|
| Complete migration and extract operating leverage | ₹946.08 Cr | Nobody outside the company |
| Post-integration cost rationalisation | ₹946.08 Cr | Nobody outside the company |
| Technology licensing scale-up | ₹946.08 Cr | Insurers to buy — and to become more capable |
| Network Ledger | ₹946.08 Cr | Insurers to license, hospitals to accept, compliance to clear |
| Publishing adjudication-quality data | Not revenue-generating | Nobody outside the company |

The last row is worth a sentence because it is not modelled in §47 and probably should be considered anyway: publishing approval rates and turnaround costs nothing, requires no counterparty, and is the single move that would most improve the position of the one party in this business with no power at all.

---

## 47. RICE

*Framework note: run with a sensitivity pass. Initiatives requiring an insurer or an overseas market to adopt something new are multiplied by a stress rule; those delivering value inside operations Medi Assist already controls are exempt.*

**The stress rule comes from the company's own segment disclosure.** Technology licensing — the hedge against insurers in-sourcing — is **3.3% of consolidated revenue**. That is Medi Assist's own demonstrated ability to earn from something other than administering claims for insurers, and it is the right discount for any initiative that depends on an insurer choosing to buy something new. Two alternatives were computed and not used: technology plus international at **7.57%** would have been more generous, and technology's **16.26%** share of EBITDA would have flattered a line that is 3.3% of revenue.

| Initiative | Reach (₹ Cr p.a.) | Impact | Conf. | Effort | **Base** | **Stressed** |
|---|---|---|---|---|---|---|
| Complete migration, extract leverage | 946.08 | 1.00 | 0.90 | 10 | **85.15** | **85.15** (exempt) |
| Technology licensing scale-up | 946.08 | 2.00 | 0.60 | 30 | **37.84** | **1.25** |
| **Network Ledger (PROPOSED)** | **946.08** | **1.00** | **0.35** | **40** | **8.28** | **0.27** |
| Post-integration cost rationalisation | 946.08 | 0.25 | 0.80 | 30 | **6.31** | **6.31** (exempt) |

**Network Ledger falls from 3rd of 4 at baseline to 4th and last under stress**, behind an initiative this case study did not propose. The winner beats it by **311.69×** — the most decisive demotion in this series to date. `verify.py` asserts programmatically both that the proposal finishes last and that it is the **weakest stressed initiative at baseline**.

The margin of defeat is itself the finding, and it is not an artefact of harsh inputs. **Finishing what is already underway is worth ₹6.40 Cr of EBITDA per quarter at the historical margin, needs no customer's agreement, and is nearly done.** Nothing requiring an insurer to buy a new product can compete with that on a one-year view. The proposal is a five-year argument being scored on a one-year board, and the correct conclusion is to finish the integration first and treat §50 as the thing to design while that happens.

---

## 48. MoSCoW

| | |
|---|---|
| **Must** | TDR-90 baselined per district before any tariff licensing; compliance owning dispersion thresholds; insurer identity stripped at ingestion; publication of approval rate, turnaround and appeal-overturn rate as a precondition |
| **Should** | Licence separable from the administration contract and surviving its termination; hospitals able to see and contest their own data; separate contracting and invoicing |
| **Could** | Quality-adjusted tariff bands; extension to corporate buyers; settlement-speed benchmarking for hospitals |
| **Won't** | Any single group-wide rate floor or ceiling; any licence conditioned on holding an administration contract; any use of patient-level records in the product; any commercial ownership of the TDR-90 thresholds |

The "Won't" row closes the four routes by which a network product becomes the coordination mechanism §40 describes — and the second entry matters most, because bundling the licence with administration would make NLC/1k's fourth condition unmeasurable and the whole metric meaningless.

---

## 49. Kano

| Feature | Category | Note |
|---|---|---|
| Accurate, fast claims settlement | Basic | The function; failure ends the contract |
| Lower cost per claim | Performance | Where the fee is negotiated down 2.13% a year |
| **Licensed claims technology** | **Performance → Reverse, over time** | Solves the insurer's problem today and reduces its need for Medi Assist tomorrow |
| **A tariff book no single insurer could build** | **Attractive**, and unsold | Gets stronger as more insurers are served |
| Published adjudication-quality data | **Attractive** to regulators and corporates, and unbuilt | Nobody in Indian TPA publishes it |

Row three is the uncomfortable one, and it is not an argument against licensing — being paid during a transition is better than being displaced without payment. It is an argument for making sure something else is being built at the same time, which is what row four represents.

---

## 50. Feature Proposal — *Network Ledger*

**What it is.** A separately-contracted, separately-priced licence to Medi Assist's hospital network asset: tariff bands by procedure and district, settlement history, and provider quality indicators, aggregated across every insurer Medi Assist serves and stripped of individual insurer identity. Priced per covered life. Explicitly **decoupled from the administration contract** — an insurer that brings claims processing in-house can still license the network, and that is the point.

**Why this shape.** §16 shows Medi Assist owns two assets with opposite competitive properties, and is monetising the replicable one. §37 shows the network asset has a genuine increasing-returns dynamic — it strengthens with every additional insurer served, which is exactly what no single insurer can reproduce. **Network Ledger converts the by-product of administering 37.6% of the group market into a product that survives the loss of administration.** It is the only revenue line available that gets more defensible as insurers become more capable.

**What it is not.** It is not a rate-setting mechanism — no group-wide floor or ceiling, ever. It is not built from patient records. It is not conditioned on holding an administration contract. And it is not a substitute for the integration leverage §47 ranks first by 311×.

**North Star:** NLC/1k, per §31, with covered lives administered as the denominator and the survives-termination condition.
**Guardrail:** TDR-90, per §31, by district, owned by compliance.

---

## 51. PRD

**Problem.** Medi Assist earns 92.43% of revenue from a function its customers can build, at a fee falling 2.13% per rupee of premium. Its hedge is 3.3% of revenue and consists of selling that same function as software. Its least replicable asset — a multi-insurer hospital tariff and settlement book — generates no separate revenue.

**Goals.** Create a revenue line that survives an insurer in-sourcing administration; make the network asset visible and priced; and publish adjudication-quality data so that concentrating market power is accompanied by accountability.

**Non-goals.** Setting hospital rates. Coordinating pricing between insurers. Using patient-level records. Replacing the integration work that §47 ranks first.

**User stories.**
- As an insurer, I license tariff and provider-quality data I could not assemble alone, and keep it whether or not you administer my claims.
- As a hospital, I can see and contest the settlement and quality data held about me.
- As compliance, I can see tariff dispersion by district and stop licensing where rates are converging.

**Functional requirements.** Insurer-identity stripping at ingestion; aggregation to procedure and district with minimum-insurer thresholds; TDR-90 dispersion computation per district against a published threshold with automatic suspension; licence contracting separable from administration; hospital data-access and dispute workflow; NLC/1k measurement against the four §31 conditions.

**Non-functional.** Dispersion thresholds writable only by compliance, enforced by access control and build-pipeline test; no patient-level data in any pipeline; **publication of approval rate, turnaround time and appeal-overturn rate as a launch precondition.**

**Acceptance criteria.** A covered life counts toward NLC/1k only if all four §31 conditions hold, including survival of administration-contract termination. No district licenses before its TDR-90 baseline is established.

**Success metrics.** NLC/1k at the R1 threshold in §54; TDR-90 within threshold in every district measured separately; adjudication-quality data published quarterly.

---

## 52. Wireframes

```
THE CASCADE  (three disclosed growth rates; the ratios are not reported)
+--------------------------------------------------------------+
|  India health premiums under management .......... +26.8%     |
|  Revenue ......................................... +24.1%     |
|  EBITDA .......................................... +14.3%     |
|  ----------------------------------------------------------  |
|  Revenue per rupee of premium ....................  -2.13%    |
|  EBITDA per rupee of revenue .....................  -7.90%    |
|  ----------------------------------------------------------  |
|  EBITDA per rupee of premium .....................  -9.86%    |
|      the two stages compound exactly to the whole             |
+--------------------------------------------------------------+

WHAT IS BEING LICENSED, AND WHAT IS NOT
+--------------------------------------------------------------+
|                        Replicable?   Licensed?   % of revenue |
|  ----------------------------------------------------------  |
|  Claims administration     YES          -           92.43%    |
|  AI / MAtrix stack         YES         YES           3.30%    |
|  Hospital tariff book      NO          NO            0.00%    |
|      ^ the asset that strengthens with every insurer added    |
+--------------------------------------------------------------+

COMPLIANCE - NLC/1k AND THE GUARDRAIL
+--------------------------------------------------------------+
|  Covered lives administered (denominator) ....... X,XXX,XXX   |
|  ...under a separately-priced network licence ...   XXX,XXX   |
|  ...live and billing, not piloting ..............   XXX,XXX   |
|  ...adjudicated against the licensed tariff book    XXX,XXX   |
|  ...licence survives TPA contract termination ...   XXX,XXX   |
|  ----------------------------------------------------------  |
|  NLC/1k .........................................       XXX   |
|  ----------------------------------------------------------  |
|  TDR-90, narrowest district dispersion ..........     X.XX%   |
|      ^ CONVERGENCE is the alarm, not divergence               |
|      ^ breach suspends tariff-sharing in that district        |
+--------------------------------------------------------------+
```

---

## 53. Rollout Plan

**Phase 0 — three analyst-weeks on data Medi Assist already holds, designed to kill the proposal cheaply.**

Establish whether the network asset is separable, and whether it would clear competition review.

- **K1 — named as the most likely to fire.** Existing administration contracts prohibit any use of negotiated tariff data outside the administering relationship. Insurers negotiate rates through Medi Assist but the rates are arguably theirs, and a well-advised insurer would have said so in the contract. If so, the product cannot be built from the existing book at all.
- **K2.** Competition counsel finds that licensing aggregated tariff data across competing insurers is not defensible at 37.6% market share, whatever the dispersion safeguards. That is a legal answer, not a product one, and it ends the proposal.
- **K3.** No willingness to pay. Insurers already receive network access as part of the administration fee and will not pay separately for something they consider bundled — in which case the asset is real but not separately monetisable.

**Phase 1 (Q3 FY27).** TDR-90 baselined across districts; contract review complete; adjudication-quality data published for the first time. No product launched. **Phase 2 (Q4 FY27).** Licence piloted with two insurers in high-dispersion districts only. **Phase 3 (FY28).** Expansion only under §54's rule.

**Running in parallel and contingent on nothing above:** the migration completion and cost work that §47 ranks first and fourth. Both are underway and both are worth more than this proposal on any near-term view.

---

## 54. A/B Testing

*Framework note: a randomised split is not available across a small number of insurer clients, so this is a matched-cohort comparison and is described as such.*

| Arm | Design |
|---|---|
| A — control | Insurers on standard administration contracts, network access bundled as today |
| B — falsification arm | **Reporting only** — the insurer receives a periodic network and tariff benchmarking report, free, inside the existing administration contract. No separate licence, no separate price, no decoupling |
| C — treatment | Network Ledger as specified: separately priced, separately contracted, surviving termination |

**Arm B is built to kill the thesis.** It delivers the informational value of the network asset without creating a separable product, without decoupling from administration, and without the competition exposure of a licensed rate book. If B produces the same retention and share-of-wallet effect as C, then the network asset is a **retention feature rather than a revenue line**, and Medi Assist should ship a report rather than build a licensing business. That is far cheaper and carries none of §40's coordination risk.

**Pre-registered decision rule (R1).** Arm C proceeds to Phase 3 only if it generates **NLC/1k above 50** across two consecutive quarters with at least one licence held by an insurer not using Medi Assist for administration, **and** TDR-90 is within threshold in every district measured separately, **and** competition counsel has cleared the licensing structure in writing. Failing any of the three, the programme reverts to Arm B or stops.
---

## 55. KPI Dashboard

| KPI | Baseline (Q1 FY27) | Target | Early warning |
|---|---|---|---|
| **EBITDA per rupee of premium** | **−9.86%** | Positive | **A second consecutive quarter negative means scale is arriving without economics, whatever revenue does** |
| Revenue per rupee of premium | −2.13% | Flat or better | Falls below −3% |
| EBITDA margin | 20.29% | 23.0% by end FY27 | Not recovered by Q4 FY27 |
| Adjusted PAT growth | 8.17% | Above revenue growth | Below 5% |
| Technology share of revenue | 3.3% | Rising | Flat for two quarters |
| NLC/1k | 0 (not built) | R1 threshold, §54 | Below 50 at two quarters |
| TDR-90, narrowest district | Not measured | Above threshold | Any district converging |
| Adjudication quality published | Not published | Quarterly | Not published by Q4 FY27 |

The first row is the discipline and it costs nothing. Medi Assist publishes premium growth and EBITDA growth every quarter; **dividing one by the other is the whole of this case study's central finding**, and it takes seconds.

---

## 56. Product Roadmap

| Period | Focus |
|---|---|
| Q2 FY27 | Complete MAtrix migration — the remaining 5% of group and 20% of retail claims; cost rationalisation begins |
| Q3 FY27 | Adjudication-quality data published; TDR-90 baselined; contract and competition review (Phase 0) |
| Q4 FY27 | Margin recovery to 23% tested against guidance; Network Ledger piloted with two insurers in high-dispersion districts |
| FY28 H1 | §54 decision rule evaluated; Ledger scaled, reduced to Arm B reporting, or stopped |
| FY28 H2 | Technology licensing scale-up continues on its own track |

The proposed product sits third deliberately, behind migration completion and disclosure, because that is where §47 put it — and because piloting a market-power product before publishing any accountability data would be the wrong order.

---

## 57. Risks & Mitigation

| Risk | Mitigation |
|---|---|
| Tariff licensing facilitates price coordination | TDR-90 per district monitoring dispersion **collapse**; automatic suspension; compliance owns thresholds |
| Hospitals squeezed by aggregated leverage | Bands and history only, never a group-wide rate; hospitals can see and contest their own data |
| Existing contracts prohibit secondary use of tariff data | K1 in Phase 0, named most likely to fire, tested before any build |
| Competition review fails at 37.6% share | K2; a written clearance is a precondition in R1, not an afterthought |
| Insurers in-source and the core erodes faster than the hedge grows | Tracked in §55; the whole case for §50 |
| Margin recovery to 23% is missed | Guided by management to end FY27; §55 makes it a tracked commitment rather than an assumption |
| Reputational and regulatory exposure | ED matter recorded in §40; it raises the bar for any concentration-increasing product |

---

## 58. Future Vision

The plausible good outcome is a company that finishes its integration, recovers the historical margin, publishes what it decides and how fast — and converts the multi-insurer network into a priced product that an insurer would keep even after building its own claims engine. That is a narrower business than "the TPA for a third of India" and a considerably more durable one.

The bad outcome is not distress. This is debt-free, share-gaining, cash-generative and well run. It is that the fee rate keeps compressing a couple of points a year, the largest insurers gradually in-source, the technology line grows quickly from a small base but never fast enough to replace what it is helping to erode, and a company with a genuinely rare network asset never gets paid for the one thing nobody could copy.

---

## 59. PM Lessons

1. **Divide the growth rates by each other.** Premiums +26.8%, revenue +24.1%, EBITDA +14.3% each look fine. The ratios — −2.13%, −7.90%, −9.86% compounded — are the finding, and the two stages multiply to the whole, which self-checks all three.
2. **Strip the one-time item before believing the profit growth.** Reported PAT +21.94% becomes +8.17% adjusted. The company discloses both; most coverage quoted the first.
3. **Check EPS against PAT.** A 5.28-point gap says the share count grew 4.52%, which no PAT figure reveals.
4. **Ask which of your assets your customer could rebuild.** Claims processing: yes. A multi-insurer tariff book: no. Medi Assist is licensing the first.
5. **A network effect and scale economics are not the same thing.** Processing more claims more cheaply is scale. Serving more insurers making the tariff book better for each of them is a network effect — and only one of them is defensible.
6. **When the customer is the competitor, retention metrics lie.** The risk is not that a client leaves; it is that a client stays and takes the function. NLC/1k's fourth condition — revenue that survives termination — exists for exactly that.
7. **Design the guardrail against the harm your own proposal creates.** A rate book sold to competing insurers is a coordination mechanism. TDR-90 watches for dispersion *collapsing*, which is the opposite of what a normal quality metric watches for.
8. **Report the register honestly.** Nine of eleven NIC codes in this series don't describe the business. Two do. Both numbers get published.

---

## 60. PM Interview Questions

1. Premiums grew 26.8%, revenue 24.1%, EBITDA 14.3%. What single number do you compute, and what does it tell you that none of the three does?
2. Reported profit grew 21.9%; adjusted profit grew 8.2%. Which do you take to the board, and what do you say about the other?
3. Your biggest customers can build what you sell. Argue for and against licensing them your own technology.
4. Distinguish a network effect from scale economics using this business, and say which one you would price separately.
5. Design a metric that measures revenue surviving disintermediation. What is the denominator, and what does it punish?
6. You propose selling an aggregated hospital rate book to competing insurers holding a third of the market. Name the harm and the mechanic — not the principle — that prevents it.
7. Your sensitivity analysis beats your proposal by 311×. Is the analysis wrong, the proposal wrong, or the time horizon wrong?

---

## 61. References

**Primary**
1. Medi Assist Healthcare Services Limited, unaudited Q1 FY27 consolidated and standalone results, 8 August 2026 — revenue, EBITDA, reported and adjusted PAT, EPS, derivative gain, auditor's emphasis of matter.
2. Medi Assist Healthcare Services Limited, Q1 FY27 investor presentation and press release, 8 August 2026 — segment mix, premium under management, market share, migration progress.
3. Medi Assist Healthcare Services Limited, Q1 FY27 earnings call, 10 August 2026 — technology growth, in-sourcing pressure, margin recovery timeline, Mayfair and Thailand.
4. Medi Assist Healthcare Services Limited, Red Herring Prospectus and Prospectus, January 2024 — incorporation as Net Logistics Private Limited, name changes, registered office, promoter.
5. Medi Assist board and Regulation 30 disclosures, August 2026 — Mayfair stake acquisition, directorate changes, dividend.
6. Ministry of Corporate Affairs registry — CIN L74900KA2000PLC027229.

**Secondary** (corroboration; flagged where single-sourced)
7. Indian Pharma Post — Q1 FY27 revenue, EBITDA, margin, Paramount integration and migration percentages.
8. Yahoo Finance / GuruFocus — Q1 FY27 earnings call highlights: group revenue and premium growth, market share, technology share, in-sourcing pressure, margin recovery timing.
9. Investing.com — Q1 FY27 slides summary, stock reaction, fourth consecutive quarter of sequential margin improvement.
10. The Globe and Mail / TipRanks — Q1 FY27 summary, AI contracts, Mayfair and Thailand deployment.
11. ScanX, Whalesbook, Multibagg — Q1 FY27 consolidated and standalone figures in ₹ million, dividend, ED emphasis of matter, Mayfair stake.
12. CXOToday — Q1 FY27 press summary: Mayfair segment revenue and decline, management commentary, Chief TPA Officer appointment.
13. Tracxn, TheCompanyCheck — entity, NIC classification and capital records (Appendix A-3, A-6).

---

## 62. About the Author

Gaurav Singh — Product Manager. Day 74 of a 90-day public case-study series applying structured PM frameworks to real products, under a zero-fabrication standard: every figure is cited, labelled as an estimate, flagged as single-sourced, or recorded as not publicly disclosed.

---

## 63. License

Analysis and original text © 2026 Gaurav Singh, released for non-commercial use with attribution. All company figures belong to their sources and are cited in §61. No affiliation with Medi Assist Healthcare Services Limited.

---

## 64. Self Review

**What is strong.** The central cascade is self-checking: three separately disclosed growth rates, and the two derived ratios compound exactly to the third. The adjusted-PAT correction uses the company's own adjustment rather than one I constructed. The §16 seam — replicable versus non-replicable asset — is a structural distinction rather than an analytical framing, and it is what makes the proposal follow from the diagnosis. And the proposal loses by 311×, asserted programmatically, which is the most decisive demotion in this series.

**What is weak, stated plainly.** The in-sourcing threat is **management commentary and my inference, not a measured trend.** I have no data on how many insurers have in-sourced, how much premium has moved, or how quickly. The fee compression of 2.13% in one quarter is consistent with in-sourcing pressure and equally consistent with ordinary competitive renegotiation or mix shift toward larger, lower-rate accounts. **A single quarter's rate movement cannot distinguish those**, and the whole strategic argument rests on a direction I can observe only once.

**A second weakness.** The claim that the hospital network is Medi Assist's least replicable asset is **an argument, not a measurement.** The company discloses nothing about network size, tariff coverage or settlement performance, so I cannot size the asset I am proposing to productise. §32 states this and K1 and K3 in Phase 0 exist to test it, but a reader is entitled to note that I have proposed monetising something I cannot measure.

**A third, and it is about the proposal itself.** §50 may simply be illegal. Licensing an aggregated tariff book across competing insurers at 37.6% market share is close enough to a coordination mechanism that K2 is a genuine possibility rather than a formality. I have written the guardrail first and made written competition clearance a precondition, but I should be clear that this is a proposal that competition counsel might correctly kill outright.

**What I could not establish.** Network size, tariff coverage or settlement turnaround; approval, denial, turnaround or appeal-overturn rates; the number of insurer clients or concentration among them; how much premium has moved in-house at any insurer; technology revenue in absolute terms as disclosed rather than derived from a percentage share; the terms of existing contracts regarding tariff-data use; and any detail of the ED matter beyond the auditor's emphasis of matter.

**One thing I would do differently.** I built the case study around the cascade, which is the cleanest arithmetic. But the more useful entry point is §16 — a company with two assets of opposite competitive character, licensing the wrong one. The cascade explains the pressure; the asset distinction explains what to do about it, and it should have led.

---

## 65. Appendix

### A. Source conflicts

| # | Conflict | Handling |
|---|---|---|
| A-1 | **NIC code 74900, "business activities n.e.c."** — a residual category for a health-claims administrator | Stated in §2 with the running tally: nine misclassified of eleven, two correct |
| A-2 | **Reported PAT growth of 21.9% against adjusted growth of 8.17%.** Most secondary coverage quoted the reported figure without the adjustment the company itself discloses | Both stated throughout. The adjusted figure is treated as the operating result and the derivative gain is quantified at 11.30% of reported PAT |
| A-3 | CIN appears as **U74900KA2000PLC027229** in pre-listing records and aggregators, and **L74900KA2000PLC027229** post-listing. One aggregator also gives incorporation as 6 June 2000 against the prospectus's 7 June 2000 | Post-listing CIN and the prospectus date used. The one-day discrepancy is noted and affects nothing |
| A-4 | One outlet reported the company as **"meeting revenue forecasts exactly at ₹246 crore"** while the filing reports **₹236.52 Cr** | 🔴 **Resolved in favour of the filing.** ₹236.52 Cr reconciles with the reported 24.1% growth on ₹190.56 Cr; ₹246 Cr reconciles with neither. Not used |
| A-5 | Several outlets headline the quarter as **"Q1FY26"** when reporting figures for the quarter ended 30 June 2026, which is Q1 FY27 | Q1 FY27 used throughout, consistent with the company's own presentation |
| A-6 | One aggregator lists **MediBuddy and Mangala Hospital as legal entities of Medi Assist Healthcare Services** | 🔴 **Incorrect and not used.** MediBuddy is Phasorz Technologies Private Limited (CIN U72300TN2013PTC092385), examined as Day 56 of this series. The entities are unrelated |
| A-7 | Technology revenue is disclosed as a **percentage share (3.3%)**, not an absolute figure; the ₹7.81 Cr used here is derived | Derived and flagged wherever used. Rounding in the disclosed share gives roughly ±₹0.12 Cr of sensitivity |
| A-8 | Figures appear in both **₹ million and ₹ crore** across sources (₹2,365.19 mn = ₹236.52 Cr) | ₹ crore used throughout; conversions asserted in `verify.py` |

### B. Evidence grades

🟢 **High** — Q1 FY27 consolidated and standalone results, EPS, derivative gain, disclosed segment shares and growth rates, premium and market-share figures, MCA registry, prospectus.
🟡 **Medium** — earnings-call commentary (in-sourcing pressure, margin recovery timing, technology margin profile), capital snapshots, the ED emphasis of matter as characterised in secondary coverage.
🟠 **Low** — none relied upon.
🔴 **Conflicting** — A-4 (contradictory revenue figure, excluded) and A-6 (incorrect entity attribution, excluded).

### C. Author-constructed content

*Network Ledger*, NLC/1k, TDR-90, the RICE inputs, the replicable-versus-non-replicable seam in §16, the two growth loops in §36, the Phase 0 kill criteria and the §54 arms are the author's constructions, not Medi Assist disclosures or plans. **The claim that the hospital network is the least replicable asset is an argument, not a measurement** — the company discloses nothing about network scale. Technology revenue in rupees is derived from a disclosed percentage share. See ASSUMPTIONS.md Part 3 for the full inventory.

### D. Asset status

| Asset | Status |
|---|---|
| README.md | Complete, 65 sections |
| ASSUMPTIONS.md | Complete, Parts 1–5 |
| verify.py | 107 checks, all passing — delivered, not committed |
| LinkedIn carousel + caption | To follow |

---

*Day 74 of 90 · [← Day 73 — Rainbow Children's Medicare](../Day-73-Rainbow-Children's-Medicare) · Day 75 →*
