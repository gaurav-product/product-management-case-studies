# Day 78 — Oura: the ring pays for the AI, and nothing yet shows the AI pays for the ring

> Oura's S-1 presents an AI health-intelligence company that arrives at its IPO profitable. Both halves of that sentence need work. **The profit:** net income rose $59.2 Mn in the nine months to 30 June 2026, but operating income grew only **18.12%** on revenue growth of **74.11%**, operating margin fell from **8.64% to 5.86%**, and **67.51% of the increase in pre-tax profit came from lower interest, a smaller debt-extinguishment charge and other income — not from operations.** A tax provision that fell from 95.69% of pre-tax profit to 13.29% supplied **43.21%** of the net-income increase. **The AI:** membership is the economic core — **19.80% of revenue and, at the disclosed 89% margin, about 32.33% of gross profit** — and Oura Advisor is presented as the reason membership compounds. But Advisor runs partly on **non-exclusive, usage-based models from OpenAI, Anthropic and Google**; the $5.99 price has not moved since the subscription launched in October 2021; at that price the entire cost to serve a member is about **$0.66 a month**, so every extra $0.60 of inference costs roughly **10 margin points**; and **the prospectus contains no metric connecting Advisor use to retention, engagement or willingness to pay.** Oura's AI is a cost line still looking for its revenue line. The product question this case study asks is the one an AI PM would be asked on day one: *how would you prove the advice is worth paying for?*

**Author:** Gaurav Singh · **Day 78 of 90** · Written 15 September 2026
**Subject:** Oura Inc. (proposed Nasdaq: OURA), Form S-1 filed 3 September 2026, nine months ended 30 June 2026
**Verification:** `verify.py` — 106 programmatic checks, all passing

---

## 1. Cover

| | |
|---|---|
| **Product** | Oura Ring plus Oura Membership — a smart ring, an app, and Oura Advisor, an AI health companion |
| **Company** | Oura Inc. (Delaware), successor to Oura Health Oy (Finland) |
| **Domain** | Healthtech — consumer health wearables and AI health intelligence |
| **Period examined** | Nine months ended 30 June 2026 (fiscal year ends 30 September), with FY24 and FY25 for context |
| **Why it matters** | The first pure-play smart-ring IPO, reportedly targeting a valuation above $16 Bn, and the clearest public disclosure yet of how a consumer health company builds on rented foundation models |
| **Proposed feature** | *Oura Loop* — every Advisor recommendation becomes a pre-registered n-of-1 experiment that the ring itself scores |
| **Series arc** | First of 13 closing case studies on AI health products; Day 79 (Ultrahuman) is its mirror |
| **Evidence grades** | 🟢 High · 🟡 Medium · 🟠 Low · 🔴 Conflicting |

---

## 2. Repository Metadata

**Legal entity:** Oura Inc., a Delaware corporation. **SEC CIK 0002133022**, registration on Form S-1, accession **0001193125-26-381855**, filed 3 September 2026. IRS employer identification number 41-4072333. Principal executive offices 415 Kearny Street, San Francisco, California 94108. The registrant was **originally incorporated on 24 April 2013 as JouZen Oy** in Finland and completed a reorganisation into the Delaware entity on **31 March 2026**. A confidential draft registration statement was announced on 21 May 2026. 🟢

The S-1 cover gives Oura's primary Standard Industrial Classification as **3571 — Electronic Computers**. That is the US SIC system, not India's NIC register, so it is not added to the series' Indian register-misclassification tally (nine wrong of fourteen at Day 77). It is still worth a line: the classification a regulator uses for a sleep-and-temperature ring is the one used for desktop computers. 🟢

---

## 3. Badges

`Day 78/90` · `Healthtech` · `AI health intelligence` · `Consumer wearables` · `S-1` · `65 sections` · `106 verified checks` · `0 fabricated figures` · `AI eval plan in §29 and §51` · `Runnable SQL in §32` · `Zero Mermaid — tables and ASCII only`

---

## 4. Table of Contents

<details>
<summary><b>All 65 sections</b></summary>

| Group | Sections |
|---|---|
| **Context** | [1. Cover](#1-cover) · [2. Repository Metadata](#2-repository-metadata) · [3. Badges](#3-badges) · [4. Table of Contents](#4-table-of-contents) · [5. Executive Summary](#5-executive-summary) · [6. Product Overview](#6-product-overview) · [7. Company Background](#7-company-background) · [8. Product Timeline](#8-product-timeline) · [9. Vision & Mission](#9-vision--mission) |
| **Market & Competition** | [10. Problem Statement](#10-problem-statement) · [11. Market Research](#11-market-research) · [12. Industry Analysis](#12-industry-analysis) · [13. TAM / SAM / SOM](#13-tam--sam--som) · [14. Competitor Analysis](#14-competitor-analysis) · [15. SWOT](#15-swot) · [16. Porter's Five Forces](#16-porters-five-forces) · [17. Business Model Canvas](#17-business-model-canvas) |
| **Business & Users** | [18. Revenue Model](#18-revenue-model) · [19. Target Users](#19-target-users) · [20. Personas](#20-personas) · [21. Jobs To Be Done](#21-jobs-to-be-done) · [22. User Journey](#22-user-journey) · [23. User Flow](#23-user-flow) · [24. Information Architecture](#24-information-architecture) · [25. UX Audit](#25-ux-audit) · [26. UI Audit](#26-ui-audit) · [27. Accessibility](#27-accessibility) |
| **Product, Metrics & Analytics** | [28. Feature Breakdown](#28-feature-breakdown) · [29. AI Capabilities](#29-ai-capabilities) · [30. Product Metrics](#30-product-metrics) · [31. North Star Metric](#31-north-star-metric) · [32. Product Analytics](#32-product-analytics) · [33. AARRR](#33-aarrr) · [34. HEART](#34-heart) · [35. Growth Strategy](#35-growth-strategy) · [36. Growth Loops](#36-growth-loops) · [37. Network Effects](#37-network-effects) · [38. Product Strategy](#38-product-strategy) · [39. Monetization](#39-monetization) |
| **Risk, Prioritisation & Proposal** | [40. Trust & Safety](#40-trust--safety) · [41. Technical Architecture](#41-technical-architecture) · [42. Data Flow](#42-data-flow) · [43. API Ecosystem](#43-api-ecosystem) · [44. Privacy & Security](#44-privacy--security) · [45. Pain Points](#45-pain-points) · [46. Opportunity Mapping](#46-opportunity-mapping) · [47. RICE](#47-rice) · [48. MoSCoW](#48-moscow) · [49. Kano](#49-kano) · [50. Feature Proposal — Oura Loop](#50-feature-proposal--oura-loop) · [51. PRD](#51-prd) |
| **Execution** | [52. Wireframes](#52-wireframes) · [53. Rollout Plan](#53-rollout-plan) · [54. A/B Testing](#54-ab-testing) · [55. KPI Dashboard](#55-kpi-dashboard) · [56. Product Roadmap](#56-product-roadmap) · [57. Risks & Mitigation](#57-risks--mitigation) · [58. Future Vision](#58-future-vision) |
| **Reflection & Sources** | [59. PM Lessons](#59-pm-lessons) · [60. PM Interview Questions](#60-pm-interview-questions) · [61. References](#61-references) · [62. About the Author](#62-about-the-author) · [63. License](#63-license) · [64. Self Review](#64-self-review) · [65. Appendix](#65-appendix) |

</details>

---

## 5. Executive Summary

Oura sells a ring and a subscription. In the nine months to 30 June 2026 it shipped **3.1 Mn rings** (1.8 Mn a year earlier), ended the period with **5.0 Mn paid members** (2.5 Mn), and reported revenue of **$1,214.5 Mn, up 74.11%** — hardware $974.0 Mn (+65.44%) and membership $240.5 Mn (+120.98%). Trailing twelve-month revenue is **$1,424.79 Mn**. About 94% of ring activations convert to paid membership; weighted-average 12-month paid-member retention is about 85%; the app is opened more than 3.5 times a day and the ring worn a median of about 23 hours. 🟢

**The first complication is the profit.** Net income went from $1.6 Mn to $60.8 Mn. Operating income went from $60.3 Mn to $71.2 Mn — **+18.12%**, against revenue +74.11% — because operating expenses grew **99.82%**: R&D +104.59%, sales and marketing +83.83%, G&A +132.17%. Pre-tax profit rose $33.6 Mn, of which **only 32.49% came from operations**; the other 67.51% came from interest expense falling after a May 2025 repayment, a debt-extinguishment charge that did not recur, and a swing in other income. Then the tax provision fell from $34.9 Mn to $9.3 Mn, supplying **43.21% of the net-income increase.** Operating margin **fell from 8.64% to 5.86%.** None of this is hidden — it is all in the MD&A — but "profitable at IPO" and "operating leverage" are different claims, and the S-1 supports only the first. 🟢

**The second complication is the AI.** Membership is where the economics live. At the disclosed **89% membership gross margin**, membership produced about **$214.07 Mn of gross profit — 32.33% of the company's total from 19.80% of its revenue, 1.63× its weight** — leaving hardware at an implied **46.01%**. Oura says membership value is delivered increasingly through Oura Advisor, its conversational AI, and through a custom women's-health LLM. The S-1 also says three things that belong next to that claim:

1. **The models are partly rented.** Advisor uses proprietary models, fine-tuned open-source models, and "select third-party large language models from OpenAI, Anthropic, and Google," on agreements that are usage- or subscription-based and **non-exclusive**, plus domain models trained by webAI. Anyone can rent the same frontier models. One of those vendors now offers health-record interpretation in ChatGPT on its Free plan.
2. **The price has not moved.** $5.99 a month or $69.99 a year in the US, unchanged since the subscription launched with Oura Ring 3 in October 2021. At list price and 89% margin, the whole cost to serve a member is about **$0.66 a month**. An extra **$0.60** of inference per member-month would cost **10.02 margin points**; an extra **$2.67** would halve the margin. The S-1 itself warns that AI computing costs could raise the cost of the membership.
3. **There is no AI outcome metric.** The prospectus publishes rings sold, paid members, retention, DAU/MAU and app opens. It publishes nothing on Advisor usage, Advisor's effect on retention, or whether any member would pay more for it. Retention is measured only to month 12.

**The thesis.** The ring's gross profit pays for member acquisition and, increasingly, for the AI. Nothing in the filing yet shows the AI paying for anything. That is not a criticism of the AI's quality — it may be excellent. It is a statement that Oura has not yet built the instrument that would tell it, or an investor, whether the AI is a moat or a margin leak.

**The proposal, *Oura Loop*,** builds that instrument into the product. Every Advisor recommendation that can be tested against ring data becomes a pre-registered n-of-1 experiment: stated metric, stated window, the member's own noise band, and a verdict the ring scores two weeks later. The North Star counts **verified advice outcomes per 1,000 recommendations issued**, so issuing more advice without follow-through lowers it. **In RICE it ranks third of four at baseline and last under stress**, behind moving inference onto owned models — which needs no member to do anything. §47 argues why that ordering is correct.

---

## 6. Product Overview

Three layers. **The ring** — five generations since 2015; Oura Ring 5 launched on 4 June 2026 at starting prices of $399–$499. **The app** — scores and trends for sleep, readiness, activity, stress, heart health, cycles and more than 50 metrics in total. **The membership** — $5.99/month or $69.99/year, required for the full app, with a 30-day trial; about 63% of new members in the period chose annual billing. Oura Advisor sits inside the app as the conversational interface and is the entry point to the Women's Health Expert and what the S-1 calls Medical AI. 🟢

---

## 7. Company Background

Founded in Oulu, Finland, in 2013; first ring shipped 2015; subscription launched October 2021 and "monetized" from 2022 (see Appendix A-5). CEO **Thomas Hale** since March 2022, previously President of Momentive AI (SurveyMonkey) and COO/CPO of HomeAway. **David Shuman** is Executive Chairman. About **1,350 full-time employees in 11 countries**, more than 350 in hardware and operations, with offices in Helsinki and Oulu. More than 50 PhDs and five MDs in the science organisation. 🟢

---

## 8. Product Timeline

| Date | Event | Grade |
|---|---|---|
| 24 Apr 2013 | JouZen Oy incorporated in Finland | 🟢 |
| 2015 | First Oura Ring shipped | 🟢 |
| Oct 2021 | Oura Ring 3 and the recurring membership launch | 🟢 |
| Mar 2022 | Thomas Hale becomes CEO | 🟢 |
| Oct 2024 | Oura Ring 4 launches; battery issues in some cohorts later drive warranty costs | 🟢 |
| Oct 2025 | Series E reported at about $11 Bn | 🟠 |
| Oct 2025 | US ITC import ban on Ultrahuman's Ring Air takes effect after Oura's patent win | 🟡 |
| 12 Dec 2025 | Samsung files an ITC complaint alleging Oura infringes four patents | 🟢 |
| 31 Mar 2026 | Reorganisation from Finland to Delaware | 🟢 |
| 19–21 May 2026 | Confidential draft S-1 submitted and announced | 🟢 |
| 4 Jun 2026 | Oura Ring 5 launches | 🟢 |
| 23 Jul 2026 | OpenAI launches Health in ChatGPT to US users, including the Free plan | 🟢 |
| 3 Sep 2026 | Public S-1 filed; Nasdaq listing sought under OURA | 🟢 |

---

## 9. Vision & Mission

The S-1 frames Oura as a "health intelligence platform" that turns continuous biometrics into guidance members act on. The case study takes the framing seriously and asks what evidence would show the guidance is acted on — because that, not the sensor, is where the membership price is justified.

---

## 10. Problem Statement

**For the member:** a ring produces dozens of scores; most people cannot tell which ones matter or what to change. Advisor is Oura's answer — an interpreter. **For the company:** an interpreter costs money per conversation, is built partly on models competitors can also buy, and has no disclosed measure of whether it changes behaviour or retention. **The PM problem:** Oura is scaling an AI feature whose value it can describe but has not yet measured, on a subscription whose price it has not changed in five years.

---

## 11. Market Research

IDC, cited in the S-1, estimates about **212 Mn wearables sold globally** in the year to 30 June 2026. Oura's trailing-twelve-month rings are **3.6 Mn — 1.70%** of that (the S-1 rounds to "approximately 2%"). The member base is unusual for a wearable: **72% women**, 27% over 45, 37% with household income under $100,000, and **more than half reporting at least one chronic condition.** That last figure matters for §40: an AI companion talking to a majority-chronic population is operating close to clinical territory. 🟢

---

## 12. Industry Analysis

Three forces shape this market in 2026. **Hardware commoditises** — Oura's revenue per ring fell from $332 (FY24) to $311 (9M FY26), **−6.33%**, while starting list prices rose. **Subscriptions are contested** — the S-1's own risk factor names competitors that may offer "a membership model with no subscription fee." **Frontier AI is a shared input** — the same three model vendors are available to every competitor and to the platforms themselves. Patents are the one input that is not shared, and Oura is spending on them: third-party professional fees, predominantly IP litigation, rose $48.3 Mn — **67.17% of the entire G&A increase.** 🟢

---

## 13. TAM / SAM / SOM

*Framework selection rationale: run in restricted form. No primary-sourced market size exists for "AI health intelligence," so the market is sized from Oura's own disclosed base rather than from a third-party TAM figure.*

| Layer | Definition | Size | Grade |
|---|---|---|---|
| **TAM** (context only) | Global wearables sold, trailing year | ~212 Mn units (IDC via S-1) | 🟡 |
| **SAM** | Oura's own paid-member base | 5.0 Mn members | 🟢 |
| **SOM** (the question this case study asks) | Membership revenue at risk if AI does not justify the price | TTM membership revenue **$290.15 Mn** | 🟢 derived |

The SOM framing is deliberate: the interesting number is not how many more rings Oura can sell, it is how much of an existing $290 Mn subscription line depends on value the company has not measured.

---

## 14. Competitor Analysis

*Restricted to what the filing and dated public sources support. Whoop, Garmin, Apple, Google/Fitbit and Samsung are named in the S-1 as competitors; no financial comparison is constructed for them.*

| | **Oura** | **Ultrahuman** (Day 79) | **Health in ChatGPT** (Day 90) |
|---|---|---|---|
| Form | Ring + app + paid membership | Ring + app; subscriptions a small add-on | Software only; connects Apple Health and medical records |
| AI layer | Advisor: proprietary, fine-tuned open-source, OpenAI/Anthropic/Google models, webAI domain models | Jade "biointelligence" system; not currently subscription-gated | The frontier model itself |
| Price of the AI to the user | Inside a $5.99/month membership | No subscription required for Jade | Available on the Free plan, as well as Go, Plus and Pro |
| Scale disclosed | 5.0 Mn paid members; $1.21 Bn nine-month revenue | $64 Mn operating revenue FY25; ~$150 Mn stated run rate | "Over 300 million" people ask health questions each week (company figure) |
| Evidence | 🟢 S-1 | 🟡 company release and press | 🟡 company statement |

**What this table says.** The competitor that should worry Oura most is not another ring. Ultrahuman gives its AI away; OpenAI — one of Oura's own model vendors — gives health interpretation away. Oura's advantage is the thing neither has at the same depth: **longitudinal data from a device worn 23 hours a day.** The case study's proposal is built on that asset precisely because it is the one a rented model cannot copy.

**The comparator that is also a legal opponent.** Oura's patent win produced a US import ban on Ultrahuman's Ring Air from October 2025; Samsung filed its own ITC complaint against Oura in December 2025. Patents protect the form factor. They do not protect advice.

---

## 15. SWOT

| Strengths | Weaknesses |
|---|---|
| 5.0 Mn paid members; ~94% activation-to-paid conversion; ~85% 12-month retention | Operating margin fell to 5.86%; opex grew 99.82% |
| 89% membership gross margin; 23-hour median wear | No disclosed AI usage or AI outcome metric |
| 1,140+ patents and applications | Retention disclosed only to month 12 |
| **Opportunities** | **Threats** |
| Price and packaging, which management says it may "evolve" | Free AI health interpretation from platforms and rivals |
| Payer channels — Essence Healthcare Medicare Advantage, Maven Clinic | Inference cost growth against a fixed price |
| Owned and edge models to cut inference cost | Samsung ITC complaint; Omni MedSci claim of ~$120 Mn |

---

## 16. Porter's Five Forces

*Framework selection rationale: run twice, as a single two-column table, because the two halves of the business face opposite forces. The ring is a hardware market; the membership is an AI-software market. On three of the five forces the two halves point in different directions.*

| Force | **Ring (hardware)** | **Membership (AI software)** |
|---|---|---|
| Rivalry | High — Samsung, Ultrahuman, wrist wearables; RPU down 6.33% | High and rising — free AI interpretation from rivals and platforms |
| New entrants | **Low** — 1,140+ patents; ITC exclusion won | **High** — frontier models are rentable by anyone |
| Supplier power | Moderate — BOM, tariffs, battery quality (warranty +$84.4 Mn in FY25) | **High** — three model vendors, non-exclusive, usage-priced |
| Buyer power | Moderate — 49% of hardware revenue through retailers; top two customers ~22% of revenue | **Low today** — 85% retention, price unchanged since 2021 |
| Substitutes | Watches, bands, phones | ChatGPT with Apple Health; any app reading exported data |

**The seam.** Barriers to entry are high for the ring and low for the AI. Supplier power is moderate for the ring and high for the AI. The part of the business with the best margin is the part with the weakest structural protection.

---

## 17. Business Model Canvas

| Block | Oura |
|---|---|
| Customer segments | Health-engaged consumers (72% women); employers and payers via partner programmes; the US Department of Defense as an enterprise customer |
| Value proposition | Continuous, comfortable measurement plus interpretation |
| Channels | DTC and retail (49% of hardware revenue); Amazon, Best Buy, Costco, Harrods, Target |
| Revenue streams | Ring (80%), membership (20%) |
| Key resources | Longitudinal biometric data, patents, science team |
| Key partners | Model vendors (OpenAI, Anthropic, Google, webAI); Natural Cycles, Dexcom, Strava; Essence Healthcare, Maven Clinic |
| Cost structure | BOM, freight, tariffs, warranty; paid media; R&D headcount; IP litigation; inference and hosting |

---

## 18. Revenue Model

| Line | 9M FY26 | 9M FY25 | Growth | Share of revenue |
|---|---|---|---|---|
| Hardware | $974.0 Mn | $588.7 Mn | +65.44% | 80.20% |
| Membership | $240.5 Mn | $108.8 Mn | +120.98% | **19.80%** (from 15.60%) |
| **Total** | **$1,214.5 Mn** | **$697.6 Mn** | **+74.11%** | |

Membership revenue grew **1.21×** as fast as paid members (120.98% against 100.00%). The S-1 does not decompose the difference, and with the US price unchanged it cannot be a price effect in the US; mix, timing of member growth and non-US pricing are all possible, and none is asserted here. Revenue per ring sold was **$314.19** on the hardware line, a little above the disclosed $311 RPU because hardware revenue also includes accessories. 🟢

---

## 19. Target Users

Consumers who want to understand sleep, recovery, cycles and long-term health without wearing a watch; a growing share with chronic conditions; and, through partners, Medicare Advantage beneficiaries and employer-sponsored members. Roughly 40% of new members in the period arrived organically. 🟢

---

## 20. Personas

*Author constructs, built from the S-1's disclosed member mix. Not interview-based.*

| | **Priya, 34** | **Mark, 58** | **Dana, 41** |
|---|---|---|---|
| Why Oura | Cycle tracking and conception planning | Medicare Advantage plan offered the ring | Sleep and stress during a demanding job |
| What she asks Advisor | "Why did my temperature trend shift?" | "Is my resting heart rate something to worry about?" | "What should I change to sleep better?" |
| What goes wrong today | Good explanation, no follow-up | The answer sits close to clinical advice | Advice given, never checked |
| What Oura Loop gives | A tracked, time-boxed test | An escalation path, not a diagnosis | A verdict from her own ring data |

---

## 21. Jobs To Be Done

**When** my scores change, **I want** to know what caused it and what to do, **so I can** feel in control rather than anxious. **When** I try a change, **I want** to know whether it worked for me, **so I can** keep it or drop it. The second job is the one no scoring app does today, and it is the one a ring is uniquely placed to answer.

---

## 22. User Journey

| Stage | Today | Friction |
|---|---|---|
| Buy | Retail or DTC, $399+ for Ring 5 | Price, sizing |
| Activate | ~94% convert to paid | Low |
| Daily use | App opened 3.5+ times a day | Score fatigue |
| Ask | Advisor explains a change | **The conversation ends there** |
| Act | Member may or may not try the advice | **Nothing records it** |
| Retain | ~85% at month 12 | Unmeasured beyond 12 |

---

## 23. User Flow

Morning score → "why?" → Advisor explanation → suggestion → **end.** The flow has no step where the suggestion becomes a commitment, and no step where the ring reports back. §50 adds both.

---

## 24. Information Architecture

Home (scores) · Readiness · Sleep · Activity · Health (heart, cycles, metabolic, Health Radar) · Advisor · Profile/Records (lab upload, Oura Health Records). Advisor is a destination rather than a layer — you go to it, it does not follow up with you.

---

## 25. UX Audit

Strong: passive capture, low-effort daily check. Weak: interpretation is conversational and stateless from the member's point of view — nothing Advisor recommends appears later in the Sleep or Readiness views as a thing being tested. Not evidenced in the disclosure examined: whether Advisor answers are ever revisited.

---

## 26. UI Audit

Not assessed from product screenshots; this case study reproduces no company imagery. §52 wireframes are original.

---

## 27. Accessibility

A ring removes the screen-at-wrist barrier and suits people who will not wear a watch to bed. A conversational layer helps members who find charts hard to read. Voice access and non-English Advisor coverage are not disclosed.

---

## 28. Feature Breakdown

| Feature | Layer | Paid? | Notes |
|---|---|---|---|
| Sleep, Readiness, Activity scores | App | Membership | Core daily loop |
| Cycle insights, Fertile Window, pregnancy insights | App | Membership | 72% female base |
| Health Radar, Nighttime Breathing, Nighttime BP | App | Membership | Long-term pattern features |
| Meals (photo logging with Advisor insights) | App + AI | Membership | AI-dependent |
| **Oura Advisor** | AI | Membership, on Ring 3/4/5 | Conversational, grounded in member history |
| **Women's Health Expert** | AI | Membership | Owned and operated custom LLM |
| Lab upload, Oura Health Records | App | Membership | Brings clinical data into context |
| AI-enabled support and diagnostics | Operations | — | Used to resolve Ring 4 warranty issues |

---

## 29. AI Capabilities

This is the section this case study was chosen for. Everything in the first table is disclosed; everything after it is the evaluation design an AI PM would bring.

**What the S-1 discloses.** 🟢

| Item | Disclosure |
|---|---|
| Model stack | Proprietary models, fine-tuned open-source models, third-party LLMs from OpenAI, Anthropic and Google, and webAI-trained domain models |
| Vendor terms | Usage- or subscription-based, non-exclusive, no material revenue share, exclusivity or purchase commitment |
| Compute placement | "Where it is most efficient" — ring, phone or cloud; proprietary edge-deployed models |
| Safety practice | Periodic review, auditing and testing of outputs; evaluation against member data and peer-reviewed sources; guardrails on output types |
| Stated risks | Hallucination, bias, AI compute costs raising membership cost, model-extraction attacks, EU AI Act obligations |
| Operational AI | Support-cost reduction; AI diagnostics for Ring 4 warranty resolution |
| Outcome metrics | **None disclosed** |

**The eval plan the filing implies but does not publish.** *Author construct.*

| Eval layer | What it measures | How | Pass bar |
|---|---|---|---|
| **Grounding** | Does the answer cite the member's actual data correctly? | Automated check of every numeric claim against the member's time series | ≥99% numeric fidelity |
| **Clinical safety** | Does the answer stay inside wellness scope and escalate when it should? | Clinician-labelled sample, stratified by chronic-condition flag | Escalation recall ≥95% on red-flag cases |
| **Actionability** | Can the recommendation be tested with ring data? | Classifier plus human audit | Measured, not targeted (feeds §53 K1) |
| **Outcome** | Did the member's own metric move after the advice? | §50 *Oura Loop* | North Star, §31 |
| **Cost** | Inference cost per resolved question | Per-model token and routing logs | Tracked against the $0.66/member-month cost-to-serve ceiling |

**Failure modes, ranked by how much they would hurt this business.**

1. **Confident advice to a chronic patient that should have been a referral.** More than half the base reports a chronic condition. This is the guardrail in §31.
2. **Advice that sounds personal and is generic.** A rented model can produce fluent explanations with no grounding; the grounding eval catches this.
3. **Cost creep.** Longer conversations, more members, a fixed price. §3's arithmetic: $0.60 more per member-month is 10 margin points.
4. **Regression to the mean mistaken for efficacy.** Members ask Advisor after bad nights; bad nights are followed by better ones regardless. Any outcome metric that ignores this will flatter the AI. §53 K2 is built around it.

**Human-in-the-loop design.** Clinician review of a stratified weekly sample; automatic hand-off copy for red-flag patterns; no recommendation of medication changes; Loop experiments limited to behaviours (timing, caffeine, alcohol, light, exercise), never treatment.

**Cost per interaction.** Not disclosed. The only disclosed anchor is membership cost of revenue — about **$26.46 Mn** for the nine months at 89% margin — which includes hosting, support and data processing together. §55 tracks inference separately.

---

## 30. Product Metrics

| Metric | Value | Grade |
|---|---|---|
| Rings sold, 9M | 3.1 Mn (+72.22% on rounded units; S-1 says 75%) | 🟢 / 🔴 A-3 |
| Paid members | 5.0 Mn (+100.00%) | 🟢 |
| Activation → paid | ~94% | 🟢 |
| Weighted-average 12-month retention | ~85% | 🟢 / 🔴 A-2 |
| DAU / MAU | ~65% | 🟢 |
| App opens per day | 3.5+ | 🟢 |
| Median daily wear | ~23 hours | 🟢 |
| Repeat purchases, share of rings | 11% (FY25 9%, FY24 5%) | 🟢 |
| Organic share of new members | ~40% | 🟢 |
| Annual-plan share of new members | ~63% | 🟢 |
| **Advisor usage, Advisor retention effect** | **Not disclosed** | 🟠 |

---

## 31. North Star Metric

**Proposed: VAO/1k — Verified Advice Outcomes per 1,000 testable Advisor recommendations issued.**

A recommendation enters the denominator when Advisor issues it and the actionability classifier marks it testable. It enters the numerator only if **all four** hold:

1. the target metric, direction and window were **recorded before the member acted**;
2. the member **opted in** to the test;
3. the ring captured at least **80% of wear time** in both the baseline and test windows;
4. the metric moved in the pre-registered direction **by more than the member's own baseline noise band**, net of the matched no-advice comparison in §53.

**The denominator is the design choice.** It is recommendations issued, not members, not conversations and not opt-ins. Advice that is never tested, or tested and fails, lowers the metric. Condition 4 blocks the easiest route to a flattering number — counting ordinary recovery after a bad night as a win.

**Guardrail, carried to §55: MEM-90 — Missed Escalation at the 90th percentile.** In the decile of members with the most chronic-condition flags, the share of clinician-audited Advisor conversations that should have produced a referral and did not. Reported by condition, never in aggregate.

---

## 32. Product Analytics

*Author construct. Schema is hypothetical; queries are written in Postgres dialect and were parsed with `sqlglot` before delivery.*

```sql
-- VAO/1k by week
WITH recs AS (
  SELECT r.rec_id, r.member_id, r.issued_at, r.metric, r.direction,
         r.window_days, r.is_testable
  FROM advisor_recommendations r
  WHERE r.is_testable
),
tests AS (
  SELECT t.rec_id, t.opted_in, t.baseline_wear_pct, t.test_wear_pct,
         t.delta, t.noise_band, t.matched_delta, t.registered_at
  FROM loop_tests t
)
SELECT date_trunc('week', recs.issued_at) AS wk,
       COUNT(*) AS testable_recs,
       COUNT(*) FILTER (
         WHERE tests.opted_in
           AND tests.registered_at <= recs.issued_at + INTERVAL '1 day'
           AND tests.baseline_wear_pct >= 0.80
           AND tests.test_wear_pct >= 0.80
           AND SIGN(tests.delta - tests.matched_delta) =
               CASE WHEN recs.direction = 'up' THEN 1 ELSE -1 END
           AND ABS(tests.delta - tests.matched_delta) > tests.noise_band
       ) * 1000.0 / NULLIF(COUNT(*), 0) AS vao_per_1k
FROM recs
LEFT JOIN tests ON tests.rec_id = recs.rec_id
GROUP BY 1
ORDER BY 1;
```

```sql
-- MEM-90: missed escalations in the top decile of chronic-condition burden
WITH burden AS (
  SELECT member_id,
         NTILE(10) OVER (ORDER BY chronic_flag_count) AS decile
  FROM member_profile
)
SELECT a.condition,
       AVG(CASE WHEN a.should_escalate AND NOT a.did_escalate
                THEN 1.0 ELSE 0.0 END) AS missed_escalation_rate,
       COUNT(*) AS audited_conversations
FROM clinician_audit a
JOIN burden b ON b.member_id = a.member_id
WHERE b.decile = 10
GROUP BY a.condition
ORDER BY missed_escalation_rate DESC;
```

---

## 33. AARRR

*Framework selection rationale: used because Oura's funnel has one unusual stage — activation is almost solved (94%) and retention is disclosed only to month 12, so the funnel's weakest-evidenced stage is Revenue expansion, not Acquisition.*

| Stage | Evidence | Read |
|---|---|---|
| Acquisition | 40% organic; paid media +$72.8 Mn (61.91% of the S&M increase) | Growing, increasingly bought |
| Activation | ~94% to paid | Solved |
| Retention | ~85% at 12 months | Strong, short horizon |
| Referral | Refer-a-friend, gifting | Not quantified |
| Revenue | Price flat since 2021; repeat purchase 11% | **The open stage** |

---

## 34. HEART

Happiness — not disclosed. Engagement — 65% DAU/MAU, 3.5+ opens a day. Adoption — 94% activation. Retention — 85% at 12 months. **Task success — not measured for Advisor**, which is the gap *Oura Loop* fills.

---

## 35. Growth Strategy

Management's own levers: more rings (new generations, retail, international — under 20% of hardware revenue is outside the US), repeat purchases, payer and employer channels, and, eventually, price and packaging. The S-1 says membership pricing may "evolve" with delivered value. That sentence is the reason Advisor needs an outcome metric: a price increase justified by AI needs evidence the AI delivers.

---

## 36. Growth Loops

The disclosed loop is hardware-led: ring gross profit funds acquisition, members convert, satisfied members refer. There is no disclosed data loop in which advice outcomes improve advice — which is the loop that would make the AI hard to copy.

---

## 37. Network Effects

Weak and indirect. Aggregate data improves models, but a member does not get more value because another member joined. *Oura Loop* would add a weak data network effect: more completed tests improve priors for which advice works for whom.

---

## 38. Product Strategy

Two strategies are available. **Feature parity** — make Advisor as fluent as a general chatbot; rivals can match it with the same vendors. **Proof** — make Advisor the only interpreter that can tell a member whether its advice worked, using 23-hour wear data no general chatbot has. This case study argues for the second.

---

## 39. Monetization

One price since October 2021. Annual plans (63% of new members) are discounted only **2.63%** against monthly. The disclosed levers — packaging, partner programmes, HSA/FSA eligibility — have not yet been used to separate AI value from base value. §47 scores a premium Advisor tier and ranks it first at baseline; it falls under stress because it needs members to choose to pay more.

---

## 40. Trust & Safety

*Placed before the proposal on purpose. The proposal asks an AI to make testable claims to a population in which more than half report a chronic condition. The hazards come first.*

**Hazard 1 — clinical drift.** An n-of-1 test about caffeine timing is wellness. The same machinery pointed at blood pressure or medication is not. *Oura Loop* is therefore restricted to a published list of behavioural levers, and any conversation touching a red-flag pattern exits the Loop and routes to escalation copy. MEM-90 measures whether that works.

**Hazard 2 — false confidence.** Telling a member "this worked for you" when it was noise is worse than no verdict. The noise-band condition and the matched comparison exist to prevent it, and verdicts are reported as *supported / not supported / inconclusive* — never as proof.

**Hazard 3 — a governance question about the AI supply chain.** Oura's CEO sits on the board of webAI; Oura's Executive Chairman has chaired webAI's board since April 2024; a third Oura director has been on webAI's board since 2024. webAI trains domain models Oura uses. In the related-party transactions section as read for this case study, webAI is not named. That can have ordinary explanations — the arrangement may fall below the threshold or outside the definition — and this case study alleges nothing. It notes only that when an AI supplier and the company share three directors, **model-selection decisions deserve a documented, arm's-length evaluation**, which the eval plan in §29 would supply.

**Hazard 4 — privacy of experiments.** A test record is a behavioural diary. Loop records stay under the same consent regime Oura describes for health data, are never shared with partners by default, and are excluded from model training unless the member opts in separately.

---

## 41. Technical Architecture

Disclosed: dynamic compute placement across ring, phone and cloud; proprietary edge models; third-party LLMs for conversation. *Oura Loop* adds four components: an actionability classifier, a pre-registration store written before the member acts, a per-member noise-band estimator from baseline data, and a matched-comparison service that finds the member's own comparable no-advice periods.

---

## 42. Data Flow

```
Ring sensors ──► phone (edge models) ──► cloud history
                                              │
Member question ──► Advisor (routed model) ◄──┘
        │
        ▼
Recommendation ──► actionability classifier ──► testable? ──no──► ordinary answer
                                                    │yes
                                                    ▼
                          pre-registration store (metric, direction, window)
                                                    │
                          member opt-in ──► test window (ring data) ──► verdict
                                                    │
                          matched no-advice comparison ◄── member's own history
                                                    │
                          VAO/1k ◄── verdict log ──► Advisor priors (opt-in only)
```

---

## 43. API Ecosystem

Disclosed partners include Natural Cycles, Dexcom and Strava, with care pathways through Essence Healthcare, Lumeris and Maven Clinic. Loop verdicts could, with member consent, become a partner-facing signal — for example, a Dexcom user's tested finding that a later dinner raised overnight glucose. That is an option, not part of the first release.

---

## 44. Privacy & Security

The S-1 describes a privacy-first stance, a commitment never to share health data without consent, alignment with HIPAA and GDPR, and a specific risk that personal information entered into AI technologies could become part of third-party datasets. With three external model vendors, **routing decisions are privacy decisions**: which conversations may leave Oura's own models should be a published rule, not an engineering default.

---

## 45. Pain Points

| Who | Pain | Evidence |
|---|---|---|
| Member | Advice with no follow-up | Flow in §23 |
| Member | Scores without causes | S-1 framing of Advisor's purpose |
| Company | AI cost on a fixed price | Price flat since 2021; S-1 compute-cost risk |
| Company | No AI outcome metric | §30 |
| Company | Operating leverage reversed | Margin 8.64% → 5.86% |
| Investor | Retention horizon of 12 months | §30, Appendix A-2 |

---

## 46. Opportunity Mapping

| Opportunity | Size signal | Needs member behaviour change? |
|---|---|---|
| Prove advice works (*Oura Loop*) | Protects a $290.15 Mn TTM line | Yes |
| Premium Advisor tier | Price flat five years | Yes — pay more |
| Payer / Medicare Advantage | Essence Healthcare live | Yes — enrol and share |
| Route inference to owned models | 10 margin points per $0.60 | **No** |

---

## 47. RICE

*Framework selection rationale: run with a stress rule taken from Oura's own disclosed behaviour. Reach is thousands of paid members touched per quarter. The stress rule multiplies the Reach of every initiative that needs a member to do something new by **11.00%** — the share of rings sold in the period that came from existing members choosing to buy again, the only disclosed measure of existing members voluntarily taking an optional, incremental step. One initiative is exempt because it needs no member to do anything.*

| Initiative | Reach (k) | Impact | Confidence | Effort (p-m) | **Baseline** | **Stressed** |
|---|---|---|---|---|---|---|
| Premium Advisor tier | 5,000 | 1.0 | 0.50 | 3 | **833.33** | 91.67 |
| Payer / Medicare Advantage expansion | 1,000 | 2.0 | 0.60 | 4 | **300.00** | 33.00 |
| ***Oura Loop* (PROPOSED)** | 1,500 | 2.0 | 0.50 | 6 | **250.00** | **27.50** |
| Inference cost routing — **EXEMPT** | 5,000 | 0.5 | 0.80 | 10 | **200.00** | **200.00** |

**Baseline order:** premium tier → payer expansion → **proposal (3rd)** → inference routing.
**Stressed order:** **inference routing → premium tier → payer expansion → proposal (4th and last).**

`verify.py` asserts all four conditions: the proposal is third at baseline, last under stress, the exempt initiative wins under stress, and the proposal is the weakest *stressed* initiative at baseline — the only configuration in which it can finish last. The exempt winner ends **7.27×** ahead of the proposal.

**Why this is the right answer.** Moving Advisor traffic from rented frontier models to owned and edge models protects the membership margin whether or not any member changes behaviour, and it is the precondition for the other three: a premium tier, a payer contract and *Oura Loop* all increase AI usage. **Fix the unit cost of the AI first; then prove the AI is worth its price; then charge for it.**

**A harsher stress rule was available.** Advisor usage itself is undisclosed; any plausible share of members using it weekly would likely be lower than repeat purchase. The more generous disclosed figure is used, and the proposal still finishes last.

---

## 48. MoSCoW

| Must | Should | Could | Won't |
|---|---|---|---|
| Pre-registration before the member acts; noise band; matched comparison; red-flag exit | Weekly clinician audit; verdict history view | Partner-shared verdicts with consent | Medication or treatment experiments; verdicts used in marketing claims |

---

## 49. Kano

Verdicts on your own advice are an **attractive** feature today — nobody expects them. Grounded, accurate explanations are now **must-be**, because free alternatives set the floor. Price stability is **one-dimensional**: members notice every dollar.

---

## 50. Feature Proposal — *Oura Loop*

**The one-line version.** When Advisor tells a member to try something the ring can measure, Oura turns it into a two-week test, writes down the expected result before the member starts, and tells the member afterwards whether their own data supports it.

**Mechanism.**

1. **Classify.** Each recommendation is tagged testable or not. Testable means a behavioural lever from the published list and a ring metric that could plausibly respond within 7–21 days.
2. **Pre-register.** Before the member acts, the system stores metric, direction, window and the member's baseline noise band from the prior 28 days.
3. **Commit.** The member opts in with one tap. No opt-in, no test — the advice still stands as advice.
4. **Measure.** The ring collects as usual. Wear below 80% in either window makes the test inconclusive, not failed.
5. **Compare.** The result is set against the member's own matched periods with no advice — similar prior-night scores, similar day of week — to separate the advice from recovery that would have happened anyway.
6. **Report.** *Supported*, *not supported* or *inconclusive*, with the numbers, in the member's own history.
7. **Learn, with consent.** Aggregated verdicts update which advice Advisor offers first to similar members.

**Why this shape and not another.** Recent case studies proposed signal capture, outcome pricing, risk participation, subtractive pricing, a comparison layer, a forward-commitment instrument, attestation, a disclosed constraint, a pre-commitment gate and a dose ledger. This is none of those: it is **an evaluation instrument built into the product surface**, so that the product's own users generate the evidence for its value.

**Why it cannot be copied with a rented model.** It requires continuous, high-compliance, pre- and post-period physiological data from the same person. A chatbot reading an occasional export has neither the coverage nor the baseline.

---

## 51. PRD

**Problem.** Advisor's value is described but not measured, on a subscription whose price has not changed since 2021 and whose AI costs are usage-priced.

**Goals.** (1) Establish VAO/1k as a reported metric. (2) Show whether Loop participation changes 12-month retention. (3) Keep MEM-90 at or below the pre-launch audit baseline.

**Non-goals.** Diagnosis, treatment advice, medical-device claims, marketing claims built on individual verdicts.

**User stories.** As a member, I want to know whether a suggested change worked for me. As a clinician reviewer, I want every red-flag conversation surfaced. As a product lead, I want to know which advice works for which members.

**Functional requirements.** Actionability classifier; pre-registration store written before opt-in is possible; noise-band estimator; matched-comparison service; verdict UI; red-flag exit; audit sampling.

**AI-specific requirements.**

| Requirement | Specification |
|---|---|
| Eval gate before launch | Grounding ≥99%; escalation recall ≥95% on the clinician-labelled red-flag set |
| Model routing | Classifier and verdict text on owned models; frontier models only for open conversation |
| Cost budget | Inference per member-month reported weekly against the $0.66 cost-to-serve anchor |
| Hallucination control | Every number in a verdict rendered from the data store, never generated |
| Human in the loop | Weekly stratified clinician audit; automatic escalation copy |
| Rollback | Kill switch per lever; any lever with MEM-90 breach suspended automatically |

**Non-functional.** Verdict computed within 24 hours of window close; Loop records excluded from training by default.

**Acceptance criteria.** No test can be created after the member's first action; inconclusive shown whenever wear <80%; red-flag conversations never enter the Loop.

**Risks.** See §57.

---

## 52. Wireframes

```
┌──────────────────────────────────┐   ┌──────────────────────────────────┐
│ Advisor                          │   │ Loop · Caffeine before 1 pm      │
│                                  │   │                                  │
│ Your deep sleep has been lower   │   │ Registered 2 Sep, before you     │
│ on days you had coffee after     │   │ started                          │
│ 3 pm.                            │   │                                  │
│                                  │   │ Expected: deep sleep ↑           │
│ Try: no caffeine after 1 pm      │   │ Your normal day-to-day swing:    │
│ for 14 days.                     │   │ ± 9 min                          │
│                                  │   │                                  │
│ ┌──────────────────────────────┐ │   │ Result: +14 min vs your matched  │
│ │  Test this with my ring  ▸   │ │   │ nights                           │
│ └──────────────────────────────┘ │   │ Wear: 93%                        │
│  Not now                         │   │                                  │
│                                  │   │ Verdict: SUPPORTED               │
│ This is wellness guidance, not   │   │ Keep it? [Yes] [Not for me]      │
│ medical advice.                  │   │                                  │
└──────────────────────────────────┘   └──────────────────────────────────┘
```
*Illustrative values; author construct.*

---

## 53. Rollout Plan

**Phase 0 — two analyst-weeks on logs Oura already holds. Built to kill the proposal cheaply.**

| Kill criterion | Test | Kill if |
|---|---|---|
| **K1** | Share of historical Advisor recommendations that map to a published behavioural lever and a ring metric | Below 25% |
| **K2 — most likely to fire** | Members open Advisor after bad nights; bad nights regress toward the mean. Compare metric change after advised bad nights against the same members' unadvised bad nights | Advised improvement does not exceed unadvised by more than the median noise band |
| **K3** | Share of 14-day windows with wear ≥80% | Below 60% |

**K2 is named as most likely to fire** because it is the default behaviour of any self-tracking population: people seek help at their worst, and their next reading is usually better. If K2 fires, Advisor's apparent effect is mostly the calendar, and *Oura Loop* would have been measuring that.

**Phase 1 — 8 weeks.** US members, five levers (caffeine timing, alcohol, bedtime consistency, evening light, late exercise), opt-in only.
**Phase 2 — 12 weeks.** Add cycle-aware levers with the Women's Health Expert; international English markets.
**Phase 3.** Payer-partner version with consent-gated verdict sharing.

---

## 54. A/B Testing

| Arm | Treatment |
|---|---|
| A | Advisor as today |
| **B — falsification arm** | Advisor plus a plain 14-day reminder: "How did the change go?" No pre-registration, no measurement, no verdict |
| C | *Oura Loop* |

**Arm B is built to make the proposal unnecessary.** If a reminder alone produces the same follow-through and the same retention, the measurement apparatus is theatre.

**Pre-registered rules.**

- **R1:** C proceeds only if it beats B by **more than 8 percentage points** on share of testable recommendations acted on, across two cycles.
- **R2:** C must be non-inferior to A on 90-day paid retention (margin 1 point).
- **R3:** MEM-90 in C must be no worse than in A, reported by condition.

---

## 55. KPI Dashboard

| KPI | Definition | Watch for |
|---|---|---|
| **VAO/1k** | §31 | Rising without rising opt-in = classifier drift |
| **MEM-90** | §31 | Any condition above audit baseline |
| Inference $ per member-month | Model-routing logs | Crossing $0.60 |
| Opt-in rate | Opted-in / testable | Below 10% |
| Inconclusive share | Wear <80% | Above 40% |
| 12-month retention, Loop vs non-Loop | Cohort | No difference after two cycles |
| **Early warning for the thesis** | Next reported operating margin | If it recovers above 8.64% with the price unchanged, the cost-pressure half of the thesis weakens |

---

## 56. Product Roadmap

| Window | Build | Exit test |
|---|---|---|
| Q1 | Inference routing to owned and edge models (the RICE winner) | Inference per member-month tracked and falling |
| Q1 | Phase 0 on existing logs | K1–K3 pass |
| Q2 | Loop Phase 1, three-arm test | R1–R3 |
| Q3 | Women's-health levers; international English | MEM-90 stable |
| Q4 | Packaging decision informed by Loop evidence | Retention non-inferior |

---

## 57. Risks & Mitigation

| Risk | Likelihood | Mitigation |
|---|---|---|
| K2: regression to the mean explains the "effect" | High | Matched comparison; Phase 0 kill |
| Low opt-in | Medium | One-tap commit; no penalty for declining |
| Regulatory drift toward device claims | Medium | Lever whitelist; no treatment levers; legal review of verdict copy |
| Verdicts used as marketing | Medium | Prohibited in §48 |
| Inference cost rises with Loop | Medium | Owned models for classifier and verdicts |
| Members read "not supported" as failure and churn | Low–medium | R2 non-inferiority rule; neutral copy |

---

## 58. Future Vision

A ring that does not just tell you what happened, but keeps a record of what you tried and what worked for your body. If Oura builds that record, the rented model becomes a replaceable component and the member's own evidence becomes the product.

---

## 59. PM Lessons

1. **"Profitable" and "operating leverage" are different claims.** Decompose the change in pre-tax profit before quoting net income. Here, 67.51% of it sat below the operating line.
2. **In AI products, find the cost-to-serve anchor.** $5.99 × 11% = $0.66 is a two-number calculation that turns "AI compute risk" into "ten margin points per sixty cents."
3. **Read the vendor paragraph.** Non-exclusive, usage-based terms with three frontier labs describe a feature any competitor can rent.
4. **An AI feature without an outcome metric is a cost line.** The first PM job is instrumenting value, not adding capability.
5. **Design the metric against regression to the mean.** People ask for help at their worst moment.
6. **Build the falsification arm first.** If a reminder does as well as your AI, you have learned something cheap.
7. **Put the no-cooperation initiative first.** Cutting inference cost helps every other plan and needs nobody to change.

---

## 60. PM Interview Questions

1. Oura's membership is 20% of revenue and about a third of gross profit. How would you decide whether to raise the price?
2. Design an evaluation framework for an AI health companion used by a population where half report a chronic condition.
3. How would you prevent regression to the mean from inflating an AI feature's measured impact?
4. Your model vendor launches a free product that overlaps your paid feature. What do you do in the next 90 days?
5. What is the right North Star for an AI feature whose output is advice?
6. When would you move inference from a frontier model to an owned model, and what would you measure?

---

## 61. References

**Company filing**
1. Oura Inc., Form S-1 Registration Statement, filed with the US SEC on 3 September 2026, CIK 0002133022, accession 0001193125-26-381855 — all financial statements, operating metrics (rings sold, paid members, RPU, retention, DAU/MAU, app opens, wear time, repeat purchase, organic share, annual-plan share, retail share), membership pricing and gross margin, AI technology risk factor and model-vendor terms, competition, litigation (Samsung ITC complaint, Omni MedSci), customer concentration, employees, director biographies, corporate history.
2. Oura, press release on confidential submission of a draft registration statement, Business Wire, 21 May 2026.

**Press and secondary**
3. Business Insider via Yahoo Finance, "Oura takes step toward IPO with S-1 filing," September 2026 — TTM revenue and net income, AI-model dependence, customer concentration.
4. Yahoo Finance, "Oura IPO Could Hit $16 Billion Valuation," September 2026 — reported valuation target (attributed to Bloomberg).
5. TechTimes, "Oura IPO S-1: Early Investors Cashed Out $1B," 4 September 2026 — $1.09 Bn preferred repurchase (attributed to PitchBook).
6. Eka VC Substack, "Key figures from Oura's IPO filing," September 2026 — October 2025 Series E at about $11 Bn. 🟠

**Competitors and platform**
7. OpenAI, "Launching Health in ChatGPT," 23 July 2026, and "Introducing ChatGPT Health," 7 January 2026.
8. gHacks, "OpenAI Launches Health in ChatGPT for US Users," 25 July 2026 — plan availability and weekly health-question figure.
9. TechCrunch, "Ultrahuman unveils new smart ring as it awaits U.S. clearance after Oura dispute," 27 February 2026 — Jade, subscription status, run rate.
10. Ultrahuman, FY25 results release, 22 September 2025 — $64 Mn operating revenue, $3.2 Mn subscriptions.
11. Inc42, "Patent Infringement: US ITC's Ban On Ultrahuman Goes Live," November 2025.

---

## 62. About the Author

**Gaurav Singh** — Product Manager, New Delhi. Background in yoga therapy and behavioural science, which is why the question I care about in health products is whether a person actually changes anything. Writing one evidence-based product case study a day for ninety days; the last thirteen are about AI health products.

Oura is where that question meets AI most directly: a device that already measures the body, and an assistant that tells you what to change. The missing piece is the loop between them.

GitHub: `github.com/gaurav-product` · LinkedIn: `linkedin.com/in/gaurav-singh-986b40197`

---

## 63. License

Analysis and commentary released for non-commercial, educational use with attribution. Financial and operating figures belong to their sources and are cited in §61. No company logo, product image or marketing asset is reproduced. Derived figures are reproducible from `verify.py`; the SQL in §32 and the wireframes in §52 are original.

---

## 64. Self Review

**What is strong.** The profit decomposition uses only the S-1's own income statement, and every line reconciles (`verify.py` D0). The AI argument rests on three disclosures read side by side — vendor terms, unchanged price, 89% membership margin — rather than on outside estimates. The proposal's most likely failure mode is named before the proposal and given its own kill criterion.

**What is weak, stated plainly.**

- **Membership gross profit is derived from a rounded 89%.** A true margin of 88.5% or 89.5% moves the 32.33% share by about 0.2 points.
- **The $0.66 cost-to-serve uses US list price,** not realised revenue per member, which the S-1 does not disclose. Partner-paid and international memberships may be priced differently.
- **No Advisor usage is disclosed,** so the case study cannot say how much inference Oura consumes today. The cost argument is a sensitivity, not a measurement.
- **The 12-month retention figure is ambiguous** (Appendix A-2).
- **The tax swing may be ordinary.** A company near break-even can carry a high effective rate from non-deductible items; this case study does not claim anything irregular.
- **All RICE inputs, the North Star, the guardrail and every threshold are author constructs** (ASSUMPTIONS Part 3).

**Rating: 8/10.** The filing is excellent evidence; the AI half of the thesis is necessarily argued from what is *not* disclosed, and that caps confidence.

---

## 65. Appendix

### A. Source conflicts and disclosure gaps

| # | Conflict or gap | Handling |
|---|---|---|
| **A-1** | **Profit presentation:** net income $60.8 Mn, but net loss attributable to common stockholders **−$924.26 Mn** after a $985.0 Mn deemed dividend on the preferred repurchase. | Both reported; operating analysis uses net income and operating income. The deemed dividend is a capital-structure item, not an operating one. |
| **A-2** | **Retention wording:** cohort retention rose "from ~81% (FY23) to ~85% (FY24) to 87% (9M FY25)", while the weighted-average 12-month retention "as of June 30, 2026" is ~85%. Two measures, different windows, not reconciled in the text read. | The ~85% headline figure is used; the difference is noted, not resolved. |
| **A-3** | **Rings growth:** S-1 states 75%; computed from the rounded 3.1 Mn and 1.8 Mn it is **72.22%**. | Difference attributed to rounding of unit counts; the disclosed 75% is used in prose where cited, the computed figure is flagged. |
| **A-4** | **Preferred repurchase size:** press reports **$1.09 Bn** paid to early investors; the S-1 income statement shows a **$985.0 Mn** deemed dividend. | Not a contradiction — a deemed dividend is the excess of consideration over carrying value — but the two are different numbers and both are labelled. |
| **A-5** | **Subscription start:** the subscription model "launched… in October 2021"; elsewhere the company "began monetizing our paid membership subscription in 2022"; elsewhere "since introducing our membership offering in 2021." | Read as launch in late 2021 with first full monetisation in 2022. "Price unchanged since 2021" is used, per the S-1's own wording. |
| **A-6** | **Market share:** TTM rings 3.6 Mn ÷ 212 Mn = **1.70%**; S-1 says "approximately 2%." | Computed figure used. |
| **A-7** | **webAI:** three Oura directors sit on webAI's board; webAI supplies domain models; webAI is not named in the related-party section as read. | Stated as a governance question only. No impropriety alleged. |
| **A-8** | **Valuation:** "$16 Bn" is a press report of a target, not a filed price range. | Used only for the 11.23× TTM revenue multiple, labelled 🟡. |

### B. Evidence grades

🟢 **High** — Oura S-1 financial statements, MD&A, risk factors, business and management sections; OpenAI's own product announcements.
🟡 **Medium** — figures derived here from disclosed inputs; reported valuation; Ultrahuman company release and press coverage; company-stated usage figures from OpenAI.
🟠 **Low** — the October 2025 Series E valuation; anything about Advisor usage, which is undisclosed.
🔴 **Conflicting** — A-2 and A-3, both noted above.

### C. Author-constructed content

Personas (§20), the eval plan and failure-mode ranking (§29), VAO/1k and MEM-90 (§31), all SQL (§32), the data-flow diagram (§42), the *Oura Loop* mechanism and PRD (§50, §51), wireframes (§52), all four RICE initiatives and their inputs (§47), Phase 0 kill criteria (§53), the three-arm test and rules R1–R3 (§54), KPI thresholds (§55) and the roadmap (§56). Full inventory in `ASSUMPTIONS.md` Part 3.

### D. Asset status

| Asset | Status |
|---|---|
| README.md | Complete, 65 sections |
| ASSUMPTIONS.md | Complete, Parts 1–5 |
| verify.py | **106 checks, all passing** — delivered, not committed |
| crosscheck.py | Run; deliverables reconciled against the gate — delivered, not committed |
| LinkedIn carousel + caption | Carousel generated in Gamma (8 cards, to be checked in the editor); caption 746 characters — local only |

---

*Day 78 of 90 · [← Day 77 — NephroPlus](../Day-77-NephroPlus) · Day 79 →*
