# Product Management Case Studies — 90 Days

**One product taken apart every day for 90 days. What the numbers actually say, what the company would rather you read instead, and what I would ship next as a PM.**

![Status](https://img.shields.io/badge/status-complete-2ea44f) ![Case studies](https://img.shields.io/badge/case%20studies-90%2F90-blue) ![License](https://img.shields.io/badge/license-MIT-lightgrey)

---

## At a glance

| | |
|---|---|
| **Case studies** | 90, one per day, finished on Day 90 |
| **Companion `ASSUMPTIONS.md` files** | 63 (Days 28–90) |
| **Programmatic checks stated** | 4,499 across Days 60–90, from 79 to 344 per study |
| **Coverage** | Consumer apps, Indian fintech, SaaS, AI, adtech, commerce, mobility, logistics, aviation, telecom, consumer hardware, B2B infrastructure and a 25-day healthcare run |
| **Format** | A fixed 65-section structure, Markdown only |

---

## Start here

- **The finished method:** [Day 90 — Health in ChatGPT](Case%20Studies/Day-90-Health-in-ChatGPT), [Day 88 — Qure.ai](Case%20Studies/Day-88-Qure-ai) or [Day 72 — Entero Healthcare](Case%20Studies/Day-72-Entero-Healthcare).
- **The method without the company:** read any `ASSUMPTIONS.md` on its own. It is the part that makes each analysis checkable.
- **For hiring or evaluation:** sections 45–56 of any recent study are the PM core: pain points → opportunity → prioritisation → proposal → PRD → rollout → experiment → KPIs → roadmap.

---

## What one case study contains

Each day is a folder under `Case Studies/`.

**`README.md`** is the case study itself, in a fixed 65-section format:

- **Context:** cover, company background, market sizing, competitor analysis, SWOT, Porter's Five Forces, Business Model Canvas.
- **Users:** personas, JTBD, user journey, IA, and UX/UI/accessibility audits.
- **Metrics:** product metrics, North Star, AARRR, HEART.
- **Strategy:** growth loops, monetisation, trust & safety, architecture, privacy.
- **Prioritisation and proposal:** pain points, opportunity mapping, RICE, MoSCoW and Kano, then a concrete feature proposal with PRD, wireframes, rollout plan, A/B test design, KPI dashboard and roadmap.
- **Close:** risks, PM lessons, interview questions, references, a self review, and an appendix of source conflicts.

**`ASSUMPTIONS.md`** (Days 28 onward) has five parts, always in the same order:

1. **Assumptions:** what supports each one, the rival reading given equal weight, why the analysis proceeds anyway, and what would settle it
2. **Derivations:** the arithmetic, shown
3. **Constructs:** every persona, number or scenario the author invented, named
4. **What would falsify the thesis**
5. **What could not be found out**

A few early folders also hold charts or images (Days 7, 9, 27). Day 40 includes a `NEWSLETTER.md`.

---

## How the series evolved

The format hardened over time. Early entries are left as published rather than retrofitted, because the drift is part of the record.

| Days | What changed |
|---|---|
| 01–27 | Shorter studies, lighter on primary sources; Mermaid diagrams throughout |
| 28–32 | A companion `ASSUMPTIONS.md` appears |
| 33–49 | `ASSUMPTIONS.md` on every study; the 65-section structure and the five-part format settle in by the mid-40s |
| 50 onward | Mermaid dropped in favour of Markdown tables and static charts (Days 56 and 66 are the exceptions) |
| 60 onward | Every figure asserted by a `verify.py` script against the filings before writing; each study states its check count |
| 66–90 | A continuous healthcare run: insurance, hospitals, diagnostics, pharmacy, devices, pharma, then digital and AI health |

The `verify.py` scripts were delivered alongside each study but are not committed to this repository. The check counts are as recorded in each study.

---

## Rules the series follows

- **No fabricated figures.** Every number comes from a filing, a disclosure, an official release or a named source. Anything derived says so and shows the working. Anything invented lives in Part 3 of `ASSUMPTIONS.md`.
- **The rival reading gets equal weight.** Each load-bearing assumption is written alongside the strongest case against it.
- **Scores are argued, not tuned.** RICE inputs are justified in the open. Where an override is applied, the argument is stated rather than the score quietly adjusted. Day 75, for example, scores its own proposal last under stress.
- **Confidence is marked inline.** 🔴 flags a material limitation or an unresolved conflict; 🟡 flags a figure that carries sensitivity.
- **The self review is honest.** Section 64 states what is weak, what could not be established, and what I would do differently.

---

## The index

### Days 01–27 · Consumer, SaaS and AI

| # | Company | Domain | Focus |
|---|---|---|---|
| 01 | [Practo](Case%20Studies/Day%2001%20-%20Practo) | Healthtech | Doctor discovery and teleconsultation |
| 02 | [Spotify](Case%20Studies/Day%2002%20-%20Spotify) | Media & Audio | Personalisation and the discovery engine |
| 03 | [WhatsApp](Case%20Studies/Day%2003%20-%20WhatsApp) | Messaging | Simplicity as a product strategy |
| 04 | [Notion](Case%20Studies/Day%2004%20-%20Notion) | Productivity SaaS | Blocks, templates and the power-user gap |
| 05 | [Airbnb](Case%20Studies/Day%2005%20-%20Airbnb) | Travel & Marketplaces | Trust as the core marketplace primitive |
| 06 | [Duolingo](Case%20Studies/Day%2006%20-%20Duolingo) | EdTech | Streaks, gamification and habit design |
| 07 | [PhonePe](Case%20Studies/Day%2007%20-%20PhonePe) | Fintech — Payments | UPI distribution and life beyond payments |
| 08 | [Blinkit](Case%20Studies/Day-08-Blinkit) | Quick Commerce | Dark stores and the 10-minute promise |
| 09 | [Swiggy](Case%20Studies/Day-09-Swiggy) | Food Delivery | One app, many businesses |
| 10 | [LinkedIn](Case%20Studies/Day-10-LinkedIn) | Professional Network | An AI career companion strategy |
| 11 | [Google Maps](Case%20Studies/Day-11-Google-Maps) | Consumer Mapping | Data moats and local commerce |
| 12 | [Netflix](Case%20Studies/Day-12-Netflix) | Streaming | Content economics and retention |
| 13 | [Amazon](Case%20Studies/Day-13-Amazon) | E-commerce | The flywheel, examined honestly |
| 14 | [Canva](Case%20Studies/Day-14-Canva) | Design SaaS | Prosumer design and template network effects |
| 15 | [Perplexity](Case%20Studies/Day-15-Perplexity) | AI Search | The answer engine challenging search |
| 16 | [Cursor](Case%20Studies/Day-16-Cursor) | Developer Tools | The bet that code editors are the new platform war |
| 17 | [Figma](Case%20Studies/Day-17-Figma) | Design SaaS | From a rejected buyout to IPO to the "AI loser" narrative |
| 18 | [Linear](Case%20Studies/Day-18-Linear) | Developer Tools | The issue tracker as a system for teams and agents |
| 19 | [Lovable](Case%20Studies/Day-19-Lovable) | AI App Builder | Prompt-to-app and the durability question |
| 20 | [Cult.fit](Case%20Studies/Day-20-Cult.fit) | Health & Fitness | Offline unit economics under a digital brand |
| 21 | [CRED](Case%20Studies/Day-21-CRED) | Fintech | A premium audience in search of a business model |
| 22 | [Zerodha](Case%20Studies/Day-22-Zerodha) | Fintech — Broking | Profitable, ad-free, and structurally exposed |
| 23 | [Rapido](Case%20Studies/Day-23-Rapido) | Mobility | Bike taxis and the commission war |
| 24 | [Meesho](Case%20Studies/Day-24-Meesho) | E-commerce | Zero-commission social commerce |
| 25 | [Urban Company](Case%20Studies/Day-25-Urban-Company) | Services Marketplace | Supply quality as the product |
| 26 | [Emergent](Case%20Studies/Day-26-Emergent) | AI Agents | Agentic software building in public |
| 27 | [Slack](Case%20Studies/Day-27-Slack) | Collaboration SaaS | Enterprise messaging after the acquisition |

### Days 28–49 · Platforms, fintech and India's consumer internet

| # | Company | Domain | Focus |
|---|---|---|---|
| 28 | [Apollo 24\|7](Case%20Studies/Day-28-Apollo-24-7) | Healthtech | Omnichannel healthcare and the pharmacy engine |
| 29 | [Google Ads](Case%20Studies/Day-29-Google-Ads) | AdTech | Auctions, automation and advertiser control |
| 30 | [Meta Ads](Case%20Studies/Day-30-Meta-Ads) | AdTech | Signal loss and the ranking machine |
| 31 | [ChatGPT](Case%20Studies/Day-31-ChatGPT) | AI Consumer | The assistant becoming a platform |
| 32 | [Sarvam AI](Case%20Studies/Day-32-Sarvam-AI) | AI — India | Indic language models as public infrastructure |
| 33 | [PharmEasy](Case%20Studies/Day-33-PharmEasy) | Healthtech | The e-pharmacy that burned through its valuation |
| 34 | [Zoho](Case%20Studies/Day-34-Zoho) | SaaS | Bootstrapped breadth against funded depth |
| 35 | [AppsFlyer](Case%20Studies/Day-35-AppsFlyer) | MarTech | Attribution in a post-IDFA world |
| 36 | [Paytm](Case%20Studies/Day-36-Paytm) | Fintech | Regulatory risk as a product constraint |
| 37 | [Amaha](Case%20Studies/Day-37-Amaha) | Mental Healthtech | Care pathways, not sessions |
| 38 | [Razorpay](Case%20Studies/Day-38-Razorpay) | Fintech — Payments | From gateway to full-stack business banking |
| 39 | [Myntra](Case%20Studies/Day-39-Myntra) | Fashion E-commerce | Curation, returns and the margin problem |
| 40 | [Freshworks](Case%20Studies/Day-40-Freshworks) | B2B SaaS | Mid-market land-and-expand |
| 41 | [InMobi](Case%20Studies/Day-41-InMobi) | AdTech | Mobile advertising from India, globally |
| 42 | [Groww](Case%20Studies/Day-42-Groww) | Fintech — Investing | Simplicity that became a distribution moat |
| 43 | [Stripe](Case%20Studies/Day-43-Stripe) | Fintech — Infrastructure | Developer experience as go-to-market |
| 44 | [Nykaa](Case%20Studies/Day-44-Nykaa) | Beauty E-commerce | The brand business hiding inside the platform |
| 45 | [Eternal](Case%20Studies/Day-45-Eternal) | Food & Quick Commerce | One holding company, four different businesses |
| 46 | [ALLEN Digital](Case%20Studies/Day-46-ALLEN-Digital) | EdTech | Rebuilding supervision as a product |
| 47 | [Healthify](Case%20Studies/Day-47-HealthifyMe) | Health & Fitness | Selling the off-ramp |
| 48 | [Snitch](Case%20Studies/Day-48-Snitch) | D2C Fashion | The chain that stopped building stores |
| 49 | [River Mobility](Case%20Studies/Day-49-River-Mobility) | EV / Consumer Hardware | The ownership business hiding inside a shipment business |

### Days 50–65 · Listed India, read from the filings

| # | Company | Domain | Focus |
|---|---|---|---|
| 50 | [Zepto](Case%20Studies/Day-50-Zepto) | Quick Commerce | Profitable stores, unprofitable company |
| 51 | [Ola](Case%20Studies/Day-51-Ola) | Mobility | The company that lost the commission war |
| 52 | [Lenskart](Case%20Studies/Day-52-Lenskart) | Retail / Eyewear | Priced for the 943 million it hasn't met yet |
| 53 | [PhysicsWallah](Case%20Studies/Day-53-PhysicsWallah) | EdTech | The affordability company is rebuilding Kota |
| 54 | [Dream11](Case%20Studies/Day-54-Dream11) | Gaming / Fantasy Sports | 95% of revenue, gone by act of Parliament |
| 55 | [Mamaearth](Case%20Studies/Day-55-Mamaearth) | D2C / FMCG | The D2C brand that doesn't sell D2C anymore |
| 56 | [MediBuddy](Case%20Studies/Day-56-MediBuddy) | Healthtech | Paid for the test, not the follow-through |
| 57 | [Policybazaar](Case%20Studies/Day-57-Policybazaar) | InsurTech | The underwriter that gets paid like a shop window |
| 58 | [Delhivery](Case%20Studies/Day-58-Delhivery) | Logistics | The density worked. The price gave it back. |
| 59 | [ixigo](Case%20Studies/Day-59-ixigo) | Travel / OTA | Three businesses wearing one growth number |
| 60 | [IndiGo](Case%20Studies/Day-60-IndiGo) | Aviation | The cost base that grows at 13% no matter what you do |
| 61 | [Atomberg](Case%20Studies/Day-61-Atomberg) | Consumer Hardware | The metric that cannot see a factory |
| 62 | [CtrlS Datacenters](Case%20Studies/Day-62-CtrlS) | B2B Infrastructure | The growth that stopped at the interest line |
| 63 | [BookMyShow](Case%20Studies/Day-63-BookMyShow) | Entertainment / Ticketing | Growing into the cheaper half of its own industry |
| 64 | [Zypp Electric](Case%20Studies/Day-64-Zypp-Electric) | EV / Logistics | The asset company that stopped buying assets |
| 65 | [Vodafone Idea](Case%20Studies/Day-65-Vodafone-Idea) | Telecom | The company that counts what it cannot reach |

### Days 66–90 · Healthcare

| # | Company | Domain | Focus |
|---|---|---|---|
| 66 | [Star Health](Case%20Studies/Day-66-Star-Health) | Insurance | The turnaround that happened somewhere else |
| 67 | [Max Healthcare](Case%20Studies/Day-67-Max-Healthcare) | Healthtech — Hospitals | The metric its biggest competitor retired |
| 68 | [Dr. Lal PathLabs](Case%20Studies/Day-68-Dr-Lal-PathLabs) | Healthtech — Diagnostics | Growth that did not come from more patients |
| 69 | [MedPlus](Case%20Studies/Day-69-MedPlus) | Healthtech — Pharmacy Retail | The cohort curve is the disclosure |
| 70 | [Poly Medicure](Case%20Studies/Day-70-Poly-Medicure) | Healthtech — Medical Devices | The growth was bought and the profit was not |
| 71 | [Akums](Case%20Studies/Day-71-Akums) | Healthtech — Contract Manufacturing | The factory is theirs, the prescription is not |
| 72 | [Entero Healthcare](Case%20Studies/Day-72-Entero-Healthcare) | Healthtech — Distribution | A quarter of the profit belongs to someone else |
| 73 | [Rainbow Children's Medicare](Case%20Studies/Day-73-Rainbow-Children's-Medicare) | Healthtech — Hospitals | Two-thirds of the beds earn nothing |
| 74 | [Medi Assist](Case%20Studies/Day-75-Medi-Assist) | Healthtech — Health Benefits Administration | Selling the capability to the people who might replace you |
| 75 | [Cipla](Case%20Studies/Day-74-Cipla) | Pharmaceuticals | Record revenue, collapsing profit ¹ |
| 76 | [Dr Agarwal's Health Care](Case%20Studies/Day-76-Dr-Agarwals-Healthcare) | Healthtech — Eye Hospitals | The network grew faster than the surgery |
| 77 | [NephroPlus](Case%20Studies/Day-77-NephroPlus) | Healthtech — Dialysis | The growth is real, the dose is not |
| 78 | [Oura](Case%20Studies/Day-78-Oura) | Health Wearables — AI | The ring pays for the AI, and nothing yet shows the AI pays for the ring |
| 79 | [Ultrahuman](Case%20Studies/Day-79-Ultrahuman) | Health Wearables — AI | The AI is free, and so is almost everything else |
| 80 | [Hims & Hers](Case%20Studies/Day-80-Hims-and-Hers) | Healthtech — Telehealth | The AI clinical engine that has no denominator |
| 81 | [Hinge Health](Case%20Studies/Day-81-Hinge-Health) | Healthtech — Digital Care | The automation metric is 97%, and that is the problem |
| 82 | [Doximity](Case%20Studies/Day-82-Doximity) | Healthtech — Physician Platform | The cost of AI is audited. The claims about it are not. |
| 83 | [OpenEvidence](Case%20Studies/Day-83-OpenEvidence) | Clinical AI | There is no filing to check, so the claims get tested in court |
| 84 | [Abridge](Case%20Studies/Day-84-Abridge) | Clinical AI — Ambient Documentation | The evidence exists. The vendor didn't produce it. |
| 85 | [Eka Care](Case%20Studies/Day-85-Eka-Care) | Healthtech — Digital Health Records | 93.95 crore accounts. About a quarter of them get used. |
| 86 | [Hippocratic AI](Case%20Studies/Day-86-Hippocratic-AI) | Clinical AI — Agents | "No safety issues" in 115 million interactions |
| 87 | [Tempus AI](Case%20Studies/Day-87-Tempus-AI) | Precision Medicine — AI | What a company says when it has to |
| 88 | [Qure.ai](Case%20Studies/Day-88-Qure-ai) | Medical Imaging AI | The company with no investors and all the numbers |
| 89 | [Gaudium IVF](Case%20Studies/Day-89-Gaudium-IVF) | Healthtech — Fertility Care | When the patient is the auditor |
| 90 | [Health in ChatGPT](Case%20Studies/Day-90-Health-in-ChatGPT) | AI Consumer — Health | What happens when nothing compels |

¹ The Day 75 `README.md` is currently empty; its `ASSUMPTIONS.md` is complete.

---

## Repository layout

```
.
├── Case Studies/
│   ├── Day 01 - Practo/
│   │   └── README.md
│   ├── …
│   └── Day-90-Health-in-ChatGPT/
│       ├── README.md
│       └── ASSUMPTIONS.md
├── LICENSE
└── README.md
```

## Author

**Gaurav Singh**, Associate Product Manager, New Delhi. My background is in yoga therapy and behavioural science, which is why the user-behaviour sections tend to run longer than the market-sizing ones.

I also write **The Teardown**, a weekly LinkedIn newsletter: one product taken apart every week. What broke, why it broke, and what I would ship next as a PM.

Corrections are welcome and wanted. If a figure here is wrong, open an issue with the source, and I will fix the study and say what changed.

## License

MIT; see [LICENSE](LICENSE). The analysis is mine. The company figures belong to their filings and are cited in each study's references section.
