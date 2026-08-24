# Policybazaar — The Underwriter That Gets Paid Like a Shop Window

### Day 57 of 90 · Product Management Case Study Series

> **The thesis of this case study:** PB Fintech's Q1 FY27 print — revenue up 40% to ₹1,888 Cr, profit up 92% to ₹163 Cr, premium up 41% to ₹8,372 Cr — reads as an aggregator compounding cleanly. Its own disclosures describe something else. Policybazaar now performs the two functions that decide whether an insurer makes money — selecting which risks get on the book, and standing next to the customer at the claim — and is paid for neither. In FY26 its fraud-detection framework triggered PB-initiated cancellations refusing **₹9,618 Cr of sum assured, 3.6% of its policies and 3.2% of its premium**, while mortality on savings products fell from **14.4 deaths per 10,000 in FY23 to 1.8 in FY26 — halving every year for three years**. That is underwriting, performed by a company whose entire revenue line is a percentage of premium *placed*. Every rupee of bad risk it refuses is revenue it declines to earn; every rupee of loss ratio it improves accrues to the insurer — the same counterparty that sets its commission, and that has been cutting it by up to 18% since the September 2025 GST exemption removed their input tax credit. PB Fintech's answer to this is a hospital chain: **₹1,843.17 Cr into PB Health, ₹539.40 Cr of it its own money — 80.51% of a full year's group profit**. This case study argues the cheaper unclaimed value is not a building but a contract: getting paid on the *quality* of the risk placed rather than the *quantity*, which Policybazaar is uniquely able to prove and currently gives away free.

---

## 2. Repository Metadata

| Field | Value |
|---|---|
| **Case study** | Day 57 of 90 |
| **Product** | Policybazaar (group: Paisabazaar, PB Partners, PB for Business, PB UAE, PB Connect, PB Health) |
| **Company** | PB Fintech Limited, Gurugram — **CIN L51909HR2008PLC037998** |
| **Domain** | Insurance distribution / insurtech — the first insurance case study in this series |
| **Analysis type** | Research-led teardown + segment economics reconstruction + a feature proposal |
| **Proposed system** | **PB Ledger** — an insurer-auditable record of the risk Policybazaar selects, refuses and services, converted into a contracted profit-commission band with its own commission at risk |
| **Author** | Gaurav Singh |
| **Date of analysis** | 23 August 2026 |
| **Research boundary** | Public sources only — filings, the Q1 FY27 investor deck, MCA registry records, IRDAI and Ministry of Finance publications, trade press. No employee or internal document consulted. |
| **Latest financials** | Q1 FY27 (quarter ended 30 June 2026), reported 5 August 2026 |

---

## 3. Badges

![Case Study](https://img.shields.io/badge/Case%20Study-Day%2057%20of%2090-blue)
![Domain](https://img.shields.io/badge/Domain-Insurance%20Distribution-orange)
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

PB Fintech operates Policybazaar, India's largest online insurance marketplace, and Paisabazaar, its credit marketplace. It listed in November 2021 and spent its early years as the standard cautionary tale about Indian consumer internet — Q1 FY22 revenue of ₹238 Cr against a ₹111 Cr loss, a −47% PAT margin. The turn since is real. FY26 closed with revenue of **₹6,794 Cr** (+37%), PAT of **₹670 Cr** (+115%), adjusted EBITDA of **₹725 Cr** (+118%) and premium of **₹29,934 Cr** (+42%). Q1 FY27 extended it: revenue ₹1,888 Cr (+40%), PAT ₹163 Cr (+92%), premium ₹8,372 Cr (+41%).

**One number establishes the operating turn is genuine rather than a treasury illusion.** In Q1 FY26, other income of ₹99 Cr sat against pre-tax profit of ₹93 Cr — **other income was 106.45% of PBT**, so the operating business lost roughly ₹6 Cr and the balance sheet carried the quarter. In Q1 FY27 other income *fell* 6.1% to ₹93 Cr while PBT rose to ₹179 Cr. Strip it out and pre-tax profit moved from **−₹6 Cr to +₹86 Cr in a year**. A case study that stopped at "half the profit is non-operating" would have got this company exactly backwards.

**The question this case study asks instead is what Policybazaar is doing for the money.** In the same deck as the growth numbers sits a set of risk disclosures. FY26 PB-initiated cancellations averted **₹9,618 Cr of sum assured — 3.2% of premium and 3.6% of policies**. Savings-product mortality fell from **14.4 to 1.8 deaths per 10,000 between FY23 and FY26**. Motor inspections under five minutes went from 16% to 65%+ in a year. The company transcribes 100% of 21 lakh daily calls in nine languages and processes 7 lakh documents a day.

Those are underwriting and claims-operations metrics — the levers that decide whether an insurance company is profitable. Policybazaar is not an insurance company. Applying its own FY26 blended revenue-to-premium ratio of **22.70%** to the 3.2% of premium refused implies roughly **₹957.89 Cr of premium declined and ~₹217.4 Cr of revenue foregone — 32.45% of the group's entire FY26 profit** — for a loss-ratio improvement that lands wholly on the insurer's P&L.

**The counterparty is simultaneously squeezing the fee.** The September 2025 GST exemption removed insurers' input tax credit; from 1 October 2025 at least five — Aditya Birla Health, Care Health, ICICI Lombard, Niva Bupa and Tata AIG — cut intermediary commission by 18% of gross. The *Sabka Bima Sabki Raksha* Act, 2025 gives IRDAI explicit authority to prescribe commission caps and raises the penalty ceiling from ₹1 Cr to ₹10 Cr.

**PB Fintech's answer is a hospital chain** — **₹539.40 Cr of its own capital, 80.51% of FY26 group profit**, into a 500-hospital ambition. This case study does not argue that bet is wrong; it argues it is the **expensive** answer to a question with a cheap one unexercised. §50 proposes **PB Ledger**: an insurer-auditable record of selected, refused and serviced risk, converted into a contracted profit-commission band with a slice of Policybazaar's own commission at risk against the realised loss ratio of the cohorts it places. §40, which precedes it deliberately, deals with why that is dangerous — an intermediary paid on loss ratio has a direct incentive to refuse legitimate customers and go quiet at the claim.

---

## 6. Product Overview

A user enters details once, receives comparable quotes across insurers, and completes purchase in-session; the platform handles documentation, medical scheduling, issuance and post-sale servicing including claims assistance. As of 30 June 2026: **158.9 Mn registered consumers, 28.1 Mn transacting, 71.6 Mn policies sold** cumulatively.

Two reported clusters carry the economics. **Core Online** (Policybazaar + Paisabazaar) produced ₹1,194 Cr of Q1 FY27 revenue on ₹5,755 Cr of premium. **New Initiatives** (PB Partners, PB for Business, PB UAE, PB Connect) produced ₹694 Cr on ₹2,617 Cr. **PB Health** is separately funded and not yet a material revenue line. Category coverage: health (27 insurers, 300+ plans), term (15, 80+), motor (23, 300+), investment (17, 160+), travel (15, ~40).

---

## 7. Company Background

Incorporated **4 June 2008** at ROC Delhi as *ETechAces Marketing and Consulting Private Limited*, later PB Fintech Private Limited, then PB Fintech Limited. Registered office: Plot No. 119, Sector 44, Gurugram 122001. Authorised capital ₹155.50 Cr, paid-up ₹92.54 Cr. The CIN changed from **U51909HR2008PLC037998 to L51909HR2008PLC037998 on 9 February 2022** consequent to listing — a detail worth citing precisely, because aggregator records disagree (Appendix A).

Founders **Yashish Dahiya** and **Alok Bansal** (DIN 01653526, Whole-time Director); **Sarbvir Singh** (DIN 00509959) is also Whole-time Director. The board includes Gopalan Srinivasan, Veena Vikas Mankar, Nilesh Bhaskar Sathe, Kaushik Dutta, Lilian Jessie Paul, and Kitty Agarwal as nominee director. Founder share sales have been a recurring source of stock volatility, including a ~1% stake sale for ₹920 Cr in June 2025 and a ₹1,109 Cr divestment by Dahiya and Bansal in May 2024.

---

## 8. Product Timeline

| Year | Milestone |
|---|---|
| 2008 (Jun) | Incorporated as ETechAces Marketing and Consulting Pvt Ltd |
| 2021 (Nov) | IPO on NSE and BSE |
| 2025 (May) | PB Health raises $218 Mn led by General Catalyst; PB Fintech commits ₹539.40 Cr |
| 2025 (Sep 22) | GST exemption on individual life/health premiums; insurers lose input tax credit |
| 2025 (Oct 1) | Five named insurers cut intermediary commission 18% of gross |
| 2025 | *Sabka Bima Sabki Raksha* Act — IRDAI gains commission-cap authority; penalty ₹1 Cr → ₹10 Cr |
| FY26 | Revenue ₹6,794 Cr, PAT ₹670 Cr, premium ₹29,934 Cr; ₹9,618 Cr sum assured averted; mortality reaches 1.8 per 10,000 |
| FY27 Q1 | Revenue ₹1,888 Cr, PAT ₹163 Cr, premium ₹8,372 Cr |
| FY27 target | PB Health ₹500 Cr ARR and break-even by March 2027 |

---

## 9. Vision & Mission

Yashish Dahiya's framing of the PB Health investment — to build "an end-to-end healthcare platform that seamlessly integrates care and insurance" — is the strategic tell. The vision has migrated from *helping consumers choose* to *owning the delivery of what they chose*. The company's stated diagnosis (opaque billing, unnecessary procedures, claims delays) is a diagnosis about **provider behaviour**, and its remedy is to buy providers and salary the doctors. Coherent — and the most capital-intensive, slowest-to-falsify theory available to it.

---

## 10. Problem Statement

**Policybazaar has become the risk-selection and claims-service layer of Indian insurance and is compensated as if it were still the shop window.** Revenue is a percentage of premium placed; its distinctive capability is refusing premium that should not be placed and servicing the claims that follow. It holds no contractual instrument converting risk quality into revenue, so it cannot be paid more for improving at what it is best at, while counterparties retain full discretion to pay it less.

Three forces make this urgent: the fee is being cut (18% of gross, five insurers, October 2025); the cap is now statutory (IRDAI's explicit authority, tenfold penalty ceiling); and the alternative is expensive (₹539.40 Cr already committed to hospitals).

---

## 11. Market Research

| Fact | Value | Why it matters |
|---|---|---|
| FY26 premium | ₹29,934 Cr | The base on which all group revenue is a percentage |
| FY26 blended revenue per ₹100 premium | **₹22.70** | Down from ₹23.56 in FY25 — **−86.7 bps, −3.68%** |
| Q1 FY27 blended | **₹22.55** | Down 15.1 bps YoY despite the 18% commission cut |
| Typical insurer commission to partners | ~15% of premium | An 18% cut ≈ 270 bps off premium |
| GST on individual life/health premium | 18% → 0% from 22 Sep 2025 | Removed insurer ITC — the proximate cause of the cut |

**The important observation here is a negative one.** If five major insurers cut gross commission 18% from October 2025, the Q1 FY27 blended ratio should have collapsed. It fell 15.1 bps. Split by segment the picture resolves: **Core Online rose 29.0 bps** (20.46 → 20.75) while **New Initiatives fell 137.5 bps** (27.89 → 26.52). The cut is visible where agent commissions live and invisible in the direct online book. PB Fintech has not disclosed why, and this case study does not guess (Assumption A3).

---

## 12. Industry Analysis

Indian insurance distribution is a three-sided arrangement in which the party owning the customer relationship owns the least of the economics. Insurers manufacture, carry risk and set price, paying distribution from a regulated expense allowance the regulator has tightened since the 2023 Expenses of Management regime. Three shifts are in flight: the commission pool is squeezed by both regulatory ceilings and the GST/ITC change; composite licensing and 100% FDI will consolidate counterparties; and vertical integration has become everyone's default escape.

Policybazaar's position is unusual — it is the only large distributor with published multi-year evidence that its selection changes portfolio outcomes. That evidence is currently a marketing asset; §50 argues it should be a contractual one.

---

## 13. TAM / SAM / SOM

*Framework note: run in restricted form. No credible independently-sourced TAM for Indian online insurance distribution could be verified from a primary source, and this series does not publish market sizes it cannot trace. What follows sizes the opportunity from PB Fintech's own disclosed base.*

| Layer | Basis | Value |
|---|---|---|
| Premium already flowing through PB | FY26 group premium | ₹29,934 Cr |
| Under direct online control | FY26 core online premium | ₹20,390 Cr |
| Revenue captured on it | FY26 group revenue | ₹6,794 Cr (22.70%) |
| **Value created and not captured** | FY26 premium refused (3.2%) | **₹957.89 Cr premium, ~₹217.4 Cr revenue declined** |

The last row is the opportunity: not a share of an unmeasured market, but a share of the loss-ratio improvement already being produced on ₹29,934 Cr of premium and donated. **₹217.4 Cr equals 32.45% of FY26 group profit.**

---

## 14. Competitor Analysis

This section is restricted to what traces to a filing. InsuranceDekho, Coverfox and bancassurance channels publish no comparable financials, so no estimate for them appears.

**The comparison that carries the argument is Turtlemint**, which filed a DRHP and therefore had to disclose what a regulatory change does to a distributor's revenue line. Per that filing, roughly **88% of pre-FY2023 revenue came from marketing fees rather than commission**, and when IRDAI revised its commission framework and those fees were near-eliminated, **FY2024 revenue fell 81.27% against FY2023**. The company has since recovered, reporting 57% revenue growth in FY26.

That is this case study's fragility thesis, already demonstrated on a peer, in a filed document, three years ago. Turtlemint's revenue was a percentage of someone else's spend and the regulator removed it. Policybazaar's is a percentage of someone else's price, under a regulator that has since acquired **explicit statutory power to cap it**.

**The asymmetry to notice:** the insurer-direct channel *lost* the input tax credit and *made* the commission cut. Policybazaar's fee was reduced to fund a tax change that happened to someone else.

---

## 15. SWOT

| | Helpful | Harmful |
|---|---|---|
| **Internal** | 158.9 Mn registered / 28.1 Mn transacting; multi-year published proof of risk-selection effect; core online contribution margin 42% and adj. EBITDA margin 19% (from 14%); operating PBT −₹6 Cr → +₹86 Cr in a year | New Initiatives is 36.76% of revenue and 8.20% of contribution; 77.4% of registered PB Partners inactive; 82.32% of registered consumers never transacted; no instrument converts risk quality into revenue |
| **External** | Composite licensing consolidates counterparties; insurers under margin pressure need cheaper distribution *and* better loss ratios at once; PB Health could make claims a differentiator | IRDAI's explicit commission-cap authority; ₹1 Cr → ₹10 Cr penalties; the 18% cut spreading to the direct book; ₹539.40 Cr in an asset-heavy business; P/E of 111.9× on FY26 PAT |

---

## 16. Porter's Five Forces — run twice, merged

*Framework note: PB Fintech is now two structurally different businesses. Running Porter's once produces mush; both runs appear in one table so the divergence reads in a single pass.*

| Force | As an online aggregator | As a hospital operator (PB Health) |
|---|---|---|
| **Supplier power** | **Very high and rising** — insurers set price and commission and cut it 18% unilaterally | **Moderate** — clinical talent is scarce, but fixed salaries reduce rainmaker dependence |
| **Buyer power** | Moderate — price-sensitive at purchase, switching cost rises after issuance | Low — patients in an emergency do not comparison-shop |
| **Substitutes** | High — insurer-direct apps, bancassurance, the agent force all bypass the aggregator | High — established chains with decades of network contracts |
| **New entrants** | Moderate — low technical barrier, high trust and licensing barrier | Low — ₹1,843 Cr for one metro cluster is itself the barrier |
| **Rivalry** | High, but not the binding constraint — supplier power is | Very high; PB Health is the newcomer |

**What the double run shows:** the aggregator loses on exactly one force, and the hospital business does not fix it. PB Health changes who provides the care; it does not change who sets Policybazaar's commission. The bet is that owning provision eventually buys a seat at the manufacturing table — a five-to-ten-year answer to a problem repricing the P&L this year.

---

## 17. Business Model Canvas

| Block | Content |
|---|---|
| **Value propositions** | Comparison across 45 insurance partners; single-session purchase; documentation and medicals handled; claims assistance; for insurers — pre-selected, fraud-screened risk |
| **Channels** | Web and app; 21 lakh calls/day; ~19K pin codes via PB Partners, 78% tier 2/3 |
| **Revenue streams** | Commission on premium placed; credit-marketplace fees; trail revenue (₹725 Cr insurance, ₹278 Cr credit, 12M rolling) |
| **Key resources** | The interaction corpus — ~10 crore monthly interactions, 100% of calls transcribed, 2.5 Mn transcription hours in the quarter, 2.53 Cr documents PII-masked |
| **Cost structure** | Employee benefits ₹716 Cr (40% of Q1 FY27 expenses, +28%); advertising ₹379 Cr (+50%); ESOP ₹47 Cr/quarter |

**The canvas's own tension:** the most valuable Key Resource feeds no Revenue Stream directly. It improves conversion, worth 22.55% of premium. The loss-ratio effect it also produces is worth nothing to PB Fintech at all.

---

## 18. Revenue Model

| Line | Q1 FY27 | Q1 FY26 | Change |
|---|---|---|---|
| Total revenue | ₹1,888 Cr | ₹1,348 Cr | +40.06% |
| — Policybazaar / Paisabazaar / New Initiatives | ₹1,067 / ₹127 / ₹694 Cr | not split / not split / ~₹514 Cr | New +35% |
| Insurance premium | ₹8,372 Cr | ~₹5,937 Cr | +41% |
| Blended revenue per ₹100 premium | ₹22.55 | ₹22.71 | −15.1 bps |
| Other income | ₹93 Cr | ₹99 Cr | −6.06% |
| PBT | ₹179 Cr | ₹93 Cr | +92.47% |
| **PBT excluding other income** | **+₹86 Cr** | **−₹6 Cr** | **the operating turn** |

Other income is 51.96% of Q1 FY27 PBT, which alone would justify scepticism — until you find it was **106.45%** a year earlier and has since shrunk. The dependence is falling fast and the operating business is now the source of profit.

---

## 19. Target Users

- **The protection buyer** (health, term) — the highest-value user and the one the risk machinery is built around. New protection premium +53% YoY; health +59%.
- **The renewer** — ₹725 Cr of 12-month trail revenue, up ₹113 Cr YoY, the closest thing to recurring revenue and the line most exposed to persistency, which is exactly what PB Ledger would pay on.
- **The agent** (PB Partners) — 1.13 lakh active of 500,000+ registered, a **22.6% activation rate**, 78% of business from tier 2/3 across ~19K pin codes.

---

## 20. Personas

| Persona | Needs | Where the product fails them |
|---|---|---|
| **Ritu, 34**, first health cover, Tier-2, buying after a parent's hospitalisation | To know the policy will actually pay | Sees 300+ plans ranked on price; sees nothing about how this insurer behaves at claim time |
| **Ashok, 47**, self-employed term applicant, borderline medicals | A clear reason and a viable alternative | May be declined by a PB-initiated process he never sees, with no committed recourse path — the DAR-90 population (§31) |
| **Mahesh, 52**, health claimant, pre-auth pending | Someone on his side against hospital and insurer | Policybazaar assists ~70K health claims a quarter and is paid nothing for doing it well |

---

## 21. Jobs To Be Done

| When… | I want to… | So I can… |
|---|---|---|
| I decide I need cover | compare honestly in one place | stop guessing and buy once |
| I am asked for medicals and documents | have someone handle the process | not abandon halfway |
| **I am declined or loaded** | **understand why and be shown a real alternative** | **not walk away uninsured** |
| **I have a claim** | **have someone argue for me who knows the policy** | **not face the insurer alone** |
| I renew | be told whether this is still right | avoid paying for a worse product out of inertia |

The two bolded rows are the jobs Policybazaar performs and does not monetise.

---
## 22. User Journey

| Stage | What happens | Who captures the value |
|---|---|---|
| Trigger | Advertising (₹379 Cr Q1 FY27, +50% YoY) | PB |
| Compare | Quotes across insurers | PB |
| Apply | 7 lakh documents/day handled; fraud screening | PB (conversion) + **insurer (risk quality), uncompensated** |
| **Screen / refuse** | PB-initiated cancellation — ₹9,618 Cr averted FY26 | **Insurer entirely; PB loses the revenue** |
| Issue | Commission earned | PB |
| Live | 12–13 months of near-nothing | — |
| **Claim** | ~70K health claims supported per quarter | **Insurer and customer; PB paid nothing** |
| Renew | Trail commission | PB (₹725 Cr, 12M rolling) |

**Three of eight stages create value Policybazaar does not capture, and one costs it revenue outright.**

---

## 23. User Flow

The purchase flow — category → inputs → ranked quotes → plan detail → KYC and medicals → payment → issuance — is well-optimised and not the subject of this analysis. Two branches matter. **The refusal branch:** when the fraud framework triggers a cancellation the applicant exits; 3.6% of policies in FY26. What they are told, in what language, and whether they are routed to a product they *do* qualify for is not publicly documented — this is the flow §31's guardrail instruments. **The claim branch:** entered by a small fraction of policyholders at the moment that decides whether the product was worth buying, running on a different stack, team and economic logic — because no economic logic is attached to it at all.

---

## 24. Information Architecture

The site is organised by **product category**, mirroring how insurers are organised and how commissions are booked — not by **applicant cohort**, which is how the risk-selection asset is organised. Nothing in the consumer IA exposes portfolio quality, claim behaviour by insurer, or persistency.

---

## 25. UX Audit

| Observation | Read |
|---|---|
| Comparison ranks primarily on price and sum assured | Optimises the metric PB is paid on, not the one the customer cares about |
| Claim-behaviour data by insurer absent at comparison | The most decision-relevant fact is missing from the decision screen |
| Refusal and loading outcomes not explained in-flow | An applicant refused by an automated framework has no self-serve path to a reason |
| Ask Genie handles ~1 lakh queries/day | A strong self-serve layer exists — pointed at servicing, not at explaining decisions |

---

## 26. UI Audit

Not the binding constraint, and deliberately short. The purchase UI is mature and works across 7–9 Indian languages. The gap is not visual: no screen tells a customer *how this insurer behaves when someone like you claims*, because the ranking that maximises Policybazaar's revenue is the one it already ships.

---

## 27. Accessibility

Real strengths: 7–9 Indian languages across voice and text, ~19K pin codes with 78% of PB Partners business from tier 2/3, and document automation that reduces the literacy burden. Women's share of term business rose from 15% in Q1 FY25 to 17% in Q1 FY27.

The accessibility risk this case study's own proposal creates is stated here rather than buried: **an intermediary paid on loss ratio has a financial reason to make refusal easy and recourse hard, and refusal falls hardest on the older, self-employed, thin-file, tier-3 applicants this platform spent a decade reaching.** That is why §31's guardrail is a recourse metric at the 90th percentile, not a mean.

---

## 28. Feature Breakdown

| Feature | Who it earns for |
|---|---|
| Multi-insurer comparison | PB (conversion → commission) |
| Assisted purchase — 21 lakh calls/day, documents, medicals | PB |
| **Fraud-detection framework** — ₹9,618 Cr averted FY26 | **Insurer only** |
| Motor instant inspection — 65%+ under 5 min (16% a year ago) | Split — PB (conversion), insurer (claims leakage) |
| **Claims assistance** — ~70K health claims/quarter | **Customer and insurer only** |
| Ask Genie — ~1 lakh queries/day | PB (cost avoidance) |
| PB Partners — 1.13 lakh active, ~19K pin codes | PB (revenue, thin margin) |

**Two of the seven most capable features earn PB Fintech nothing — and they are the two that most differentiate it.**

---

## 29. AI Capabilities

PB Fintech's AI disclosure is unusually specific for an Indian listed company, and it is the evidentiary backbone of this case study.

| Capability | Disclosed scale (Q1 FY27 unless noted) |
|---|---|
| Interactions | ~10 crore/month; 21 lakh calls/day, **100% transcribed**, 7–9 languages, in-house ASR, 2.5 Mn hours in the quarter |
| Documents and text | 7 lakh documents/day (~1,000 hours saved), 2.53 Cr PII-masked; 2.7 lakh emails, 19,000 chats and 20,000 tickets/day; 600 GB/day |
| **Risk outcome** | **₹9,618 Cr sum assured averted FY26 — 3.2% of premium, 3.6% of policies** |
| **Mortality outcome** | **Savings products: 14.4 → 1.8 deaths per 10,000, FY23 → FY26** |
| Motor | 65%+ inspections under 5 minutes, from 16% in Q1 FY26 |

**The mortality series deserves its own sentence.** An 87.5% reduction over three years works out to an annual factor of exactly **0.5 — the rate halved every year, three years running.** No distribution business needs mortality experience to improve. Insurers do. Policybazaar built it anyway and has no line item that benefits.

---

## 30. Product Metrics

| Metric | Value | Evidence |
|---|---|---|
| Registered / transacting consumers | 158.9 Mn / 28.1 Mn (**17.68%**) | 🟢 |
| Core online contribution margin | 42% (from 41%); adj. EBITDA margin 19% (from 14%) | 🟢 |
| New Initiatives | Contribution margin **7%** (from 5%); adj. EBITDA **−₹36 Cr** | 🟢 |
| 12M trail revenue | ₹725 Cr insurance, ₹278 Cr credit | 🟢 |
| PB Partners activation | 1.13 lakh / 500K+ = **22.6%** | 🟡 Derived |
| Loan disbursal | ₹4,366 Cr vs ₹7,003 Cr YoY | 🔴 Conflicts with "core online disbursals +33%" — Appendix A |
| Health claims supported | ~70K in Q1 FY27 | 🟡 Denominator not disclosed |

**The segment split is where the operating story lives.**

| | Core Online | New Initiatives |
|---|---|---|
| Share of Q1 FY27 revenue | 63.24% | **36.76%** |
| Share of premium | 68.74% | 31.26% |
| Share of contribution | 91.80% | **8.20%** |
| Contribution per ₹1 of revenue | **₹0.4221** | **₹0.0648** (a **6.51×** gap) |
| Adjusted EBITDA | +₹222 Cr | **−₹36 Cr** (consumes 16.22% of Core's) |
| Share of YoY revenue growth | 66.49% | 33.32% |
| Share of YoY contribution growth | 89.89% | **10.11%** |

**New Initiatives supplied a third of the revenue growth and a tenth of the contribution growth.** Not an argument to shut it — PB Partners buys tier-2/3 reach the online funnel cannot — but the reason "+40%" should not be read as +40% of anything reaching the bottom line.

---

## 31. North Star Metric

**Current implied North Star: insurance premium placed.** Every disclosure leads with it and revenue is a fixed percentage of it. It has one fatal property: **it goes up when Policybazaar places a risk it should have refused.** The fraud framework and the North Star are in direct opposition, and the framework wins ₹9,618 Cr worth of arguments a year at the company's own expense.

**Proposed North Star: RAQ/1k — Retained-At-Quality policies per 1,000 verified applicants.** A policy counts only if **all four** hold: it was placed through Policybazaar; it is still in force at month 13; no claim on it was repudiated for non-disclosure; and the applicant was not silently down-sold from a product they qualified for.

The denominator is **verified applicants, not placements** — the load-bearing design choice. Refusing a customer lowers the numerator and leaves the denominator untouched, so RAQ/1k *drops* when the company declines business. It cannot be moved by refusing risk, by discounting, or by premium inflation.

**Guardrail: DAR-90 — Declined Applicant Recourse at the 90th percentile.** Days from a PB-initiated decline or loading to either a placed alternative the applicant accepted, or a written, specific reason delivered in their own language. At the 90th percentile rather than the mean, because a mean is moved by the easy cases and the entire risk of this proposal sits in the tail — the applicant refused, told nothing, and never seen again. Governance in §40; carried through §48, §51–§55 and §57.

---

## 32. Product Analytics

RAQ/1k's instrumentation exists in fragments and is not joined:

| Signal | Where it lives | Enables |
|---|---|---|
| Application and decline events | Fraud-detection framework | Numerator exclusions; DAR-90's start event |
| Month-13 in-force status | Insurer persistency feeds / trail reconciliation | Condition 2 |
| Repudiation reason codes | **Insurer claims systems** | Condition 3 — requires reason codes, not just outcomes |

**Condition 3 decides whether PB Ledger is buildable at all**, and is the subject of kill criterion K3. Everything else is inside Policybazaar's own stack.

---

## 33. AARRR

| Stage | Current | Under PB Ledger |
|---|---|---|
| Activation | 28.1 Mn transacting = 17.68% | Unchanged, but activating the *right* applicants becomes the paid outcome |
| **Retention** | ₹725 Cr trail, +₹113 Cr YoY | Month-13 persistency becomes a revenue term, not a byproduct |
| **Revenue** | 22.55% of premium, unilaterally cuttable | A second, contracted band tied to realised loss ratio |

The change is deliberately narrow: **PB Ledger touches Retention and Revenue only.** Any version promising an acquisition lift is scope creep.

---

## 34. HEART

| Dimension | Current | Under proposal |
|---|---|---|
| Happiness | CSAT 90%+ | Monitored for decline as refusal tightens |
| Engagement / Adoption | ~10 crore interactions/month; 17.68% adoption | Not targets — engagement is not the product here |
| **Retention** | Month-13 in-force not disclosed | The core RAQ/1k condition |
| **Task success** | ~70K health claims assisted/quarter | Instrumented and, for the first time, paid |

---

## 35. Growth Strategy

Three disclosed legs: deepen core online (protection premium +53%), scale New Initiatives for reach (+55% active partners), and vertically integrate into provision (PB Health). None changes **the basis on which the company is paid**. Two sell more premium at a rate the counterparty controls; the third buys a different industry. A fourth — repricing the existing relationship using evidence already owned — costs a fraction of the third.

---

## 36. Growth Loops

**The loop that works:** advertising → applicants → placements → premium → revenue → advertising. Funded, measured, scaling at 40%.

**The loop that exists but is not closed:** applicants → interaction corpus → better selection → better loss ratios → *(open circuit)*. The value exits at the insurer and never returns as higher commission or lower acquisition cost. PB Ledger is precisely the wire that closes it; everything else in §50 is implementation detail.

---

## 37. Network Effects

Weak on the consumer side — one buyer's presence does not improve another's quotes, and claiming a moat here would be dishonest. The genuine effect is **data-scale on the risk side**: more applicants screened → better models → fewer bad risks placed. It currently accrues to insurers; under PB Ledger it would accrue to Policybazaar, which is what turns a data asset into defensibility.

---

## 38. Product Strategy

PB Fintech has correctly identified that being paid a capped percentage of someone else's price is a bad position, and chosen the most expensive exit: buying the provider. ₹1,843.17 Cr into PB Health, **₹539.40 Cr of it its own — 80.51% of a full year's group profit** — for 500 hospitals, 150–200 owned, 1,200 Delhi-NCR beds in two years, against a ₹500 Cr ARR target that would be **7.36% of FY26 group revenue**.

**A deliberate demotion.** The hospital bet is the more dramatic story and this case study does not build on it, for a stated reason: PB Health is roughly fifteen months old, pre-scale, and its central claim — that owning provision reduces claim disputes — cannot be falsified from public data for years. A thesis built on it would be untestable. The risk-selection argument rests on three years of the company's own published mortality series and can be checked against the next four quarters of disclosure. **Choosing the testable thesis over the more interesting one is the actual product judgement in this section.**

---

## 39. Monetization

Today: one instrument, one variable. Commission = premium placed × a rate the insurer sets. That rate fell 15.1 bps blended and 137.5 bps in New Initiatives year-on-year, and five named insurers cut gross commission 18% from 1 October 2025 because they lost input tax credit when GST on individual life and health premiums went to zero on 22 September 2025.

The arithmetic on a full pass-through: insurers typically pay ~15% of premium to partners; an 18% cut takes that to **12.3%, i.e. 270 bps off premium**. Applied to Policybazaar's core online rate of 20.75%, an equivalent cut would take it to **17.02% — 373.5 bps**. Core online instead *rose* 29 bps. The cut has not landed on the direct online book to date. Three readings are possible — different contract structures, successful renegotiation, product-mix offset — and PB Fintech has disclosed none of them (Assumption A3). **Nothing in the public record prevents it landing next quarter, and no instrument in the revenue model would resist it.**

**PB Ledger adds a second instrument:** a contracted profit-commission band, per insurer per cohort, in which Policybazaar accepts a defined slice of its own commission at risk against realised loss ratio, in exchange for an upside share when the cohort outperforms the insurer's own directly-written book. Profit commission is standard in reinsurance treaties — which is the point. It is a known instrument Policybazaar is uniquely equipped to price and has never asked for.

---

## 40. Trust & Safety

**This section precedes §50 deliberately. The proposal is dangerous, and saying so before specifying it is the only honest order to write these two sections in.**

An intermediary paid on realised loss ratio acquires two incentives it should never have. First, **refuse legitimate applicants** — every marginal risk declined improves the cohort, and the people at the margin are disproportionately older, self-employed, tier-3 and thin-file, exactly the population this platform's reach was built to serve. Second, **go quiet at the claim** — Policybazaar assists ~70K health claims a quarter, and under a loss-ratio-linked contract every claim it helps a customer win costs it money. The second is the more serious: it converts the company's single most trust-building activity into a cost centre with a financial reason to underperform.

The guardrail architecture, specified before the feature:

| Control | Specification |
|---|---|
| **Metric** | DAR-90 — days from PB-initiated decline/loading to a placed alternative or a written, language-appropriate reason, at the **90th percentile** |
| **Owner** | A Consumer Standing function with **no revenue claim on PB Ledger** and no reporting line into the commercial organisation |
| **Firewall** | Decline-reason logs and claims-assistance records **architecturally separated** from pricing, lead-scoring and settlement stacks — enforced by an access-control test in CI, not by policy statement |
| **Claims neutrality** | Claims-assistance staffing, SLAs and escalation rights **contractually fixed** at pre-launch levels and excluded from cohort economics |
| **Kill switch** | Automatic, per-insurer: two consecutive monthly DAR-90 breaches revert that insurer's cohorts to flat commission, with no discretionary override |
| **Disclosure** | DAR-90 and claims-assistance volume published quarterly alongside premium |

The firewall being **architectural rather than governance-based** is the load-bearing choice. A policy saying "we will not price on decline data" is worth nothing after two reorganisations; an access boundary that fails a build-pipeline test survives them.

---

## 41. Technical Architecture

PB Fintech publishes no architecture diagram; this describes only what its disclosed operating metrics require to exist.

| Layer | Evidenced by | Confidence |
|---|---|---|
| Quote/rating integration across 45 partners | Live quotes across 27 health, 15 term, 23 motor insurers | 🟢 |
| In-house ASR and speech pipeline | 21 lakh calls/day, 100% transcribed, 9 languages, stated in-house | 🟢 |
| Fraud / risk-scoring service | PB-initiated cancellations, ₹9,618 Cr averted | 🟢 |
| Persistency / trail reconciliation | ₹725 Cr trail line | 🟡 Inferred — a trail line requires in-force reconciliation |
| **Cohort-level loss-ratio feed from insurers** | — | 🔴 **No evidence it exists. The one thing PB Ledger requires and the one thing not visible.** |

That last row is this section's honest finding, and it drives kill criterion K3.

---

## 42. Data Flow

Applicant → quote engine → application → document intelligence → fraud/risk scoring → **either** issuance (commission event) **or** PB-initiated cancellation (no revenue event) → servicing → claim assistance → month-13 renewal (trail event).

Two flows terminate without a revenue event: cancellation and claim. Both generate the data that would price PB Ledger. **The value and the data are produced exactly where the money is not.**

---

## 43. API Ecosystem

No public developer programme could be verified; the surface that matters is private and bilateral — rating APIs, issuance callbacks, and the missing one, claims and persistency feeds. At the integration level PB Ledger is a request for **two extra fields per policy**: month-13 in-force status, and repudiation reason code. A small technical ask attached to a large commercial one — which is why §53 sequences the commercial conversation first.

---

## 44. Privacy & Security

Disclosed controls are meaningful: 2.53 crore documents PII-masked, and 100% call transcription implies a substantial consent, retention and access-control regime. The **DPDP Rules, notified 14 November 2025 with an 18-month transition**, apply squarely here — health and financial data at consumer scale — with full enforcement and penalties to ₹250 Cr arriving in 2027.

PB Ledger *increases* privacy exposure, and this is recorded as a cost rather than argued around: paying on realised loss ratio means processing claim outcomes at cohort level, which is health data. Three mitigations are non-negotiable in §51 — cohort aggregation with an enforced minimum size, no individual-level claim outcome entering any pricing or scoring system, and explicit consent language covering outcome-based intermediary compensation.

---
## 45. Pain Points

| # | Pain point | Whose | Evidence |
|---|---|---|---|
| 1 | Revenue is a percentage of a price the counterparty sets, cuttable at will | PB Fintech | 18% gross cut by 5 insurers, 1 Oct 2025 |
| 2 | Risk-selection value is produced and given away | PB Fintech | ₹9,618 Cr averted; ~₹217.4 Cr revenue foregone = 32.45% of FY26 PAT |
| 3 | A third of revenue growth produces a tenth of contribution growth | PB Fintech | New Initiatives: 33.32% vs 10.11% |
| 4 | 77.4% of registered partners never transact | PB Partners | 1.13 lakh active of 500K+ |
| 5 | A declined applicant has no documented recourse path | Consumers | 3.6% of policies PB-cancelled in FY26 |
| 6 | The claim conversation is unfunded | Consumers and PB | ~70K claims/quarter, zero attached revenue |

---

## 46. Opportunity Mapping

Four converging lines make risk quality the right opportunity:

1. **The proof is already published.** A three-year mortality series moving 14.4 → 1.8 per 10,000 is evidence an appointed actuary can act on. It is sitting in an investor deck.
2. **The cost is already paid.** ₹957.89 Cr of premium refused in FY26, annually, with no return.
3. **The counterparty's incentive just changed.** Insurers who lost input tax credit and cut commission 18% are, by construction, insurers under margin pressure — which makes them *more* receptive to trading fixed cost for outcome-linked cost.
4. **The alternative is funded and slow.** ₹539.40 Cr is committed to hospitals with a March 2027 break-even target. A contract change competes for none of that capital.

**Lines 1 and 2 are the reusable method:** *check what the company has already published but not monetised; check what it is already paying for but not charging for.*

---

## 47. RICE Prioritisation

*Framework note: run twice. The second pass applies a stress rule built from PB Fintech's own worst published activation figure — **1.13 lakh active PB Partners of 500,000+ registered, a 22.6% activation rate** — to any initiative whose value depends on a registered-but-not-currently-participating counterparty choosing to participate. Internal changes are not stressed.*

Score = Reach × Impact × Confidence ÷ Effort, ×100.

| Initiative | R | I | C | E | Score | Stressed R | **Stressed** |
|---|---|---|---|---|---|---|---|
| **1. Cohort-level attribution ledger** — attribute premium, refusal and available outcome data by insurer × cohort, internally | 8 | 2.0 | 0.90 | 4 | **360.0** | not stressed | **360.0** |
| **2. Claim-behaviour disclosure at comparison** — surface published insurer claim behaviour on the compare screen | 10 | 1.5 | 0.80 | 6 | **200.0** | not stressed | **200.0** |
| **4. PB Partners activation programme** — convert dormant registered partners | 9 | 1.5 | 0.70 | 9 | **105.0** | 2.034 | **23.73** |
| **3. PB Ledger** — contracted profit-commission band, own commission at risk | 7 | 3.0 | 0.60 | 14 | **90.0** | 1.582 | **20.34** |

**The stress test demotes this case study's own proposal to last place** — behind a partner-activation programme it did not propose, and behind a spreadsheet and a UI change.

That is the exercise working, not failing. PB Ledger's value is wholly contingent on 45 insurance partners agreeing to a contract structure none currently offers, and PB Fintech's own published evidence about registered counterparties who do not participate says 22.6% eventually do. §53 follows the stressed order, and the reason is causal rather than deferential: **you cannot negotiate a profit-commission band before you can attribute loss ratio by cohort, and the disclosure product is what makes insurers hand over the claim data the band runs on.**

---

## 48. MoSCoW

| Priority | Item |
|---|---|
| **Must** | Cohort-level attribution ledger; DAR-90 instrumented and published *before* any commercial pilot; architectural firewall between decline/claims logs and pricing; claims-assistance SLAs contractually fixed |
| **Should** | Claim-behaviour disclosure at comparison; month-13 persistency feed from ≥3 insurers; repudiation reason codes |
| **Could** | Profit-commission band with one insurer, one product, one cohort; PB Partners activation programme |
| **Won't (this cycle)** | Group-wide rollout; any application of ledger economics to PB Health; individual-level loss-outcome scoring — **permanently excluded, not deferred** |

---

## 49. Kano

| Feature | Classification |
|---|---|
| Price comparison across insurers | Basic — absence is disqualifying, presence earns nothing |
| Claim-behaviour disclosure at comparison | **Attractive → Basic within ~24 months**; once one aggregator ships it, its absence becomes a defect |
| Written, language-appropriate decline reason | **Basic, currently unmet** — users do not ask for it; its absence is quietly corrosive |
| Profit-commission band | Not user-facing; Kano does not apply, and saying so is more useful than forcing the framework |

---

## 50. Feature Proposal — **PB Ledger**

**One sentence.** Policybazaar builds an insurer-auditable record of the risk it selects, refuses and services, and converts it into a contracted profit-commission band in which it places a defined slice of its own commission at risk against the realised loss ratio of the cohorts it places.

**Four components.**

1. **The Ledger.** Per insurer × product × quarterly cohort: applicants verified, policies placed, policies PB-refused with reason class, month-13 in-force count, claims assisted, claims repudiated with reason code. Aggregated only, with an enforced minimum cohort size; no individual outcome addressable.
2. **The Benchmark.** Each cohort's realised loss ratio against **the same insurer's own directly-written book** for the same product and period — not an industry average. Benchmarking against the counterparty's own alternative is what makes the claim auditable and the negotiation winnable.
3. **The Band.** A symmetric commission adjustment: outperform the insurer's own book beyond a threshold and PB earns an agreed share of the difference; underperform and PB forfeits an agreed slice of commission already earned. **Symmetry is the point** — a one-sided bonus is a discount request and will be treated as one.
4. **The Standing Function.** An independent team owning DAR-90, claims-assistance SLAs and the firewall, publishing quarterly, with the §40 kill switch.

**Why this and not something else.** Every other route out of capped-percentage economics needs capital (PB Health), regulatory change (composite licence), or volume growth into a shrinking fee (the current plan). This one needs a dataset the company already has, a benchmark the counterparty already computes for itself, and a contract structure the reinsurance market has used for decades.

**User impact.** Neutral by design for the customer who is placed; **negative for the marginal applicant unless the guardrail holds** — which is why §40 precedes this section. Positive for the claimant only if claims neutrality is contractually fixed, which the Must row of §48 requires.

**Business impact.** A second revenue variable the counterparty cannot cut unilaterally, and a ₹957.89 Cr annual act of self-denial converted into a priced input.

**Trade-offs.** Earnings volatility PB Fintech does not have today; cohort-level privacy exposure under DPDP; and handing insurers a dataset that over time teaches them to select risk without Policybazaar. **That last one is real and is the strongest argument against this proposal.**

---

## 51. PRD (abridged)

| Field | Specification |
|---|---|
| **Problem** | Revenue is a percentage of premium placed, set by the counterparty; the distinctive capability is refusing premium and servicing claims, neither compensated |
| **Scope v1** | One insurer, health, one quarterly cohort, one region |
| **Out of scope, permanently** | Individual-level loss-outcome scoring; use of decline data in pricing or lead scoring; application of ledger economics to claims staffing |
| **Data** | From PB: applicants verified, placements, refusals with reason class, claims assisted. From insurer: month-13 in-force status, repudiation reason codes, own-book benchmark loss ratio for the same product and period |
| **Privacy** | Minimum cohort size; no individual addressability; DPDP consent language covering outcome-based intermediary compensation; firewall verified by CI test |
| **Guardrail** | DAR-90 at p90, published quarterly, owned by Consumer Standing, automatic per-insurer kill switch |
| **Decision rule** | §54 R1, pre-registered before the pilot begins |
| **Dependencies** | Initiative 1 ships first; ≥3 insurers agree to share month-13 status and reason codes |

---

## 52. Wireframes

One consumer-facing surface carries the guardrail. Deliberately low-fidelity; the comparison-screen change in Initiative 2 is a single added column and is not sketched.

**Decline outcome screen — the DAR-90 start event**

```
 ┌────────────────────────────────────────────────────────────────────┐
 │  We could not place this application with Insurer A.               │
 │                                                                     │
 │  Reason: information in your medical questionnaire could not be     │
 │  verified against the documents provided.     [Read in Hindi ▾]     │
 │                                                                     │
 │  What happens now                                                   │
 │  • 2 plans you do qualify for   →  [See them]                      │
 │  • Speak to an advisor          →  [Call me back]                  │
 │  • Disagree with this?          →  [Ask for a review]              │
 │                                                                     │
 │  Clock started 12 Apr · reason delivered same day                   │
 └────────────────────────────────────────────────────────────────────┘
```

This is the only place in the product where the guardrail is visible to the person it protects.

---

## 53. Rollout Plan

**The sequence follows §47's stressed ranking**, because the attribution ledger is a precondition for pricing the band and the disclosure product is what gives insurers a reason to hand over the claim data.

**Phase 0 — falsification, before anything is built. Two analyst-weeks, on data PB Fintech already holds.**

| Kill criterion | Test | Threshold |
|---|---|---|
| **K1** | Of FY26's PB-initiated cancellations, what share were triggered by signals the insurer did not independently hold at underwriting? | **<15%** — if the insurer would have caught it anyway, there is nothing to sell |
| **K2** | Is month-13 persistency on PB-placed protection policies materially above the same insurer's own book? | **Not materially above.** **This is the criterion most likely to fire, and it is named as such.** |
| **K3** | How many of the top 10 partner insurers will share cohort loss ratio and repudiation reason codes at all? | **<3** — the instrument is unbuildable without the benchmark |

Any of the three firing stops the programme at a cost of two analyst-weeks, and the attribution ledger remains worth building on its own merits.

**Phase 1 (0–3 months)** Attribution ledger, internal only, no external commitment. **Phase 2 (2–6)** Claim-behaviour disclosure from published IRDAI data — independently valuable to consumers, and it establishes with insurers that Policybazaar will make claim behaviour visible, which changes the tone of the Phase 4 conversation. **Phase 3 (4–7)** Guardrail first: DAR-90 instrumented, baselined and published for two full quarters with the firewall CI test passing, *before* any commercial pilot. A guardrail introduced after the incentive is a guardrail that will be argued with. **Phase 4 (7–13)** Single-insurer pilot, symmetric band, decision rule pre-registered. **Phase 5 (13+)** Extend only on that rule.

---

## 54. A/B Testing

| Arm | Structure |
|---|---|
| **A** | Control — flat commission, no ledger, no disclosure |
| **B** | Ledger internally, no contract change — isolates the value of merely *knowing* |
| **C** | **Full PB Ledger** — symmetric band on a reduced flat rate |
| **D** | Ledger plus disclosure, commission unchanged — isolates the disclosure effect |
| **E** | **Falsification arm** — a straight renegotiated higher flat commission, no ledger, no risk share, no data sharing |

**Arm E is built to kill the thesis.** If Policybazaar can simply negotiate a better flat rate using the same evidence, the whole apparatus of ledger, benchmark, band and standing function is expensive theatre and the correct product decision is a slide deck and a commercial meeting.

**Pre-registered decision rule R1, fixed before the pilot starts:** *PB Ledger proceeds beyond Phase 4 only if arm C delivers more than 6% higher contribution per ₹100 of premium placed than arm E, sustained across two consecutive renewal cycles, with DAR-90 no worse than arm A's baseline in either cycle.* Failing the DAR-90 condition kills the programme regardless of the contribution result.

---

## 55. KPI Dashboard

| Tier | Metric | Read |
|---|---|---|
| **North Star** | RAQ/1k | The only metric that cannot be moved by refusing customers |
| **Guardrail** | **DAR-90**, 90th percentile | Consumer Standing owns it; kill switch on two consecutive breaches |
| **Guardrail** | Claims assisted per 1,000 in-force policies | Must not fall after go-live — the §40 failure mode made visible |
| Commercial | Contribution per ₹100 of premium placed | The number PB Ledger defends |
| Health | Month-13 persistency, PB book vs insurer own book | The K2 quantity, tracked continuously |
| Health | New Initiatives contribution margin | 7% — the drag identified in §30 |
| **Early warning** | **PB-initiated cancellation rate vs mortality per 10,000** | If mortality keeps improving while the cancellation rate falls, PB's *selection* is not what drives it — and Assumption A1 is dead |

The early-warning row is the most important line on this dashboard: it is designed to disconfirm this case study's own central claim, using two numbers PB Fintech already publishes.

---

## 56. Product Roadmap

| Horizon | Focus |
|---|---|
| **0–6 months** | Phase 0 falsification; attribution ledger; claim-behaviour disclosure shipped |
| **6–12 months** | DAR-90 baselined and published; Consumer Standing stood up; single-insurer pilot begins |
| **12–24 months** | Extend to 3 insurers on R1; PB Partners activation programme (the initiative that beat PB Ledger under stress); PB Health hits its March 2027 ARR and break-even milestone or does not — a public, dated test of the alternative strategy |

---

## 57. Risks & Mitigation

| # | Risk | Severity | Mitigation |
|---|---|---|---|
| 1 | **Legitimate applicants refused** to improve cohort loss ratios | **Critical** | DAR-90 at p90, owned outside the commercial line, automatic kill switch, published quarterly |
| 2 | **Claims assistance quietly degrades** — every won claim costs PB money | **Critical** | SLAs, staffing and escalation rights contractually fixed and excluded from cohort economics; claims-assisted-per-1,000 on the dashboard |
| 3 | Insurers refuse to share loss-ratio and reason-code data | High | K3 kills at Phase 0 for two analyst-weeks |
| 4 | The shared data teaches insurers to select risk without PB | High | Cohort aggregation only; no model or feature disclosure; accepted as a genuine long-term cost in §50 |
| 5 | DPDP exposure from processing claim outcomes | High | Minimum cohort size, no individual addressability, explicit consent; full enforcement 2027 |
| 6 | The commission cut spreads to the direct online book before any of this ships | High | The risk the proposal exists to answer; Phase 2 is sequenced early because disclosure improves negotiating position at zero commercial cost |

---

## 58. Future Vision

If composite licensing and 100% FDI arrive as drafted, counterparties get fewer and larger — which makes bilateral bargaining power matter more, not less. A distributor whose only argument is volume then negotiates against a more concentrated counterparty under a regulator-set ceiling. One that can prove, cohort by cohort and audited against the insurer's own book, that its risks perform better is negotiating about something else entirely.

PB Health may well work, and its March 2027 break-even target is dated and falsifiable. But it answers "who provides the care" and leaves untouched "who sets our price."

---

## 59. PM Lessons

1. **Put the disclosed cost next to the disclosed capability.** ₹9,618 Cr averted is a capability slide. ₹957.89 Cr of premium refused and ~₹217.4 Cr of revenue foregone — 32.45% of the year's profit — is the same slide read as a P&L event. One division turned a marketing claim into a thesis.
2. **Check whether the profit came from the finance line — then check the year before.** Other income was 51.96% of Q1 FY27 PBT, which looks damning until you find it was 106.45% a year earlier. The trend, not the level, was the finding, and it *contradicted* the lazy version of this case study.
3. **When a peer has filed a document about your thesis, use the filing.** Turtlemint's DRHP disclosing an 81.27% single-year revenue collapse beats any amount of speculation about regulatory risk.
4. **Build the stress rule from the company's own worst published number.** 22.6% partner activation demoted this case study's own proposal to last place.
5. **Specify the guardrail before the feature.** A proposal that creates an incentive to refuse sick people and abandon claimants has to earn the right to be specified at all.

---

## 60. PM Interview Questions

1. Policybazaar's revenue is a fixed percentage of premium placed, and its fraud framework refused 3.6% of policies last year. Design a compensation structure that resolves that conflict without creating a reason to refuse legitimate customers.
2. You are asked to add a claim-behaviour column to the comparison screen. The insurer with the worst record is your largest commercial partner. What do you ship?
3. Your North Star candidate improves when you decline business. Change the denominator to remove that property — and say what you lose by doing so.
4. Other income is 52% of pre-tax profit this quarter and was 106% last year. Which is the finding, and what do you check next?
5. A stress test demotes your own proposal to last place. What do you do?

---

## 61. References

Figures are attributed inline and in `ASSUMPTIONS.md`. Source classes used:

- PB Fintech Limited — Q1 FY27 earnings presentation and results disclosure (quarter ended 30 June 2026)
- PB Fintech Limited — Q4 and full-year FY26 results disclosure; investor relations financial results archive
- MCA registry records via aggregators; NSE filing on the change of Corporate Identification Number, 9 February 2022
- IRDAI — annual report and claim-settlement disclosures
- Ministry of Finance / DFS — GST exemption on individual life and health policies; *Sabka Bima Sabki Raksha* Act, 2025 commentary
- Turtlemint — DRHP-derived reporting on the FY24 revenue restatement
- Trade press on PB Health / PB Healthcare Services funding (May 2025) and expansion plans
- DPDP Rules 2025, notified 14 November 2025

---

## 62. About the Author

**Gaurav Singh** — Product Management case study series, Day 57 of 90. Research-led product teardowns built from public sources only, with every derived figure verified programmatically and every assumption declared in `ASSUMPTIONS.md`.

---

## 63. License

Published for portfolio and educational purposes. All company names, trademarks and product names belong to their respective owners. No affiliation with PB Fintech Limited, Policybazaar or any entity named here is claimed or implied.

---

## 64. Self Review

**Strengths.** It finds the thesis in a disclosure the company published as a capability slide and reads it as a P&L event. It tests the lazy "it's all treasury income" reading and publishes the number that disproves it. It uses a peer's filed document rather than speculating about regulatory risk. It stress-tests its own proposal into last place and follows the stressed order anyway, with a causal argument for why.

**Weakest point.** Assumption A1 — that PB Fintech's *selection* caused the mortality improvement — carries the argument and cannot be proven from public data; a mix shift in the savings book would produce the same series. The rival reading gets equal air in ASSUMPTIONS Part 1, and the §55 early-warning row exists to catch it.

**Left out for length.** A full segment-level reconstruction with per-product take rates, the UAE business (₹1,871 Cr premium ARR, +31%, disclosed profitable), Paisabazaar's credit economics, and the loan-disbursal discrepancy each deserve more than they got.

---

## 65. Appendix

**A · Source conflicts (5 logged)**

| # | Conflict | Resolution |
|---|---|---|
| A-1 | **CIN** — current L51909HR2008PLC037998; pre-listing U51909HR2008PLC037998; some aggregators still carry the private-limited entry | NSE filing of 9 Feb 2022 taken as authority; CIN cited, never the name alone |
| A-2 | **Loan disbursal** — ₹4,366 Cr Q1 FY27 vs ₹7,003 Cr Q1 FY26 (−37.7%), while the same deck states core online disbursals **+33% YoY** | Not reconcilable from public sources. Both reported as stated; no growth claim made on either |
| A-3 | **Commission pass-through** — five insurers cut gross commission 18% from Oct 2025, yet core online revenue per ₹100 premium *rose* 29 bps | Recorded as unexplained. Three candidate readings in §39; none selected |
| A-4 | **Directorships** — registry lists Sarbvir Singh under DIN 00509959 as Whole-time Director; secondary sources describe founder roles inconsistently | DINs cited as recorded; roles kept to what the registry supports |
| A-5 | **PB Health capital** — $218 Mn / ₹1,843.17 Cr (May 2025) vs later reporting of "$215 Mn" | Both noted; the earlier, more specific ₹ figure used in all derivations |

**B · Evidence grades**

🟢 **High** — stated directly in a PB Fintech results disclosure, an exchange filing, or a government publication.
🟡 **Medium** — derived here from two or more 🟢 figures, with the derivation in `verify.py` and ASSUMPTIONS Part 2.
🟠 **Low** — single secondary source, no primary corroboration found.
🔴 **Conflicting** — sources disagree; logged above and never used as a load-bearing input.

**C · Author-constructed content**

All personas (§20), wireframes (§52), RICE inputs (§47), the PB Ledger proposal (§50) and its PRD (§51) are constructed by the author and are **not** PB Fintech artefacts. The full list, with the reasoning behind each, is in `ASSUMPTIONS.md` Part 3.

**D · Asset status**

No screenshots, logos or diagrams are reproduced. Recommended additions if visual assets are later sourced under appropriate rights: the FY23→FY26 mortality series as a single-line chart; the Core Online vs New Initiatives contribution-per-rupee comparison as a two-bar chart; the §22 journey table redrawn as a value-capture flow with the three uncompensated stages shaded. No AI-generated imitation of PB Fintech's own product screens should be used.

---

*Day 57 of 90 · [← Day 56 — MediBuddy](../Day-56-MediBuddy) · Day 58 →*
