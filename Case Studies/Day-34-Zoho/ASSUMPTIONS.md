# ASSUMPTIONS — Day 34: Zoho

Companion file to `README.md`. Documents evidence quality, source conflicts, and everything in the case study that is the author's construction rather than a reported fact.

**Research date:** 30 July 2026
**Method:** web search across company announcements, Indian RoC filing coverage, trade press, market-research aggregators and public review platforms. No primary interviews, no product telemetry, no non-public documents.

---

## 1. The structural evidence limitation

Zoho Corporation is **privately held, bootstrapped, and has no public-market disclosure obligations**. Its only statutory disclosure is the annual RoC filing for the **Indian entity** — which is not the group. Everything else is voluntary press announcement or third-party estimate.

Practical consequences for this case study:

- There is **no 10-K to reconcile against**. Where a public-company case study can triangulate a claim against an audited filing, this one cannot.
- **RoC revenue covers the Indian entity; announced customer counts cover the group.** Any ratio combining the two (e.g. the blended ARPA in §30) is directionally illustrative, not accurate. This is flagged inline where it occurs.
- **No cohort, retention, NDR, churn or engagement data exists publicly.** All funnel and adoption analysis in §22, §23, §33 and §34 is inferred from product structure and public review sentiment, not measured.
- Market share and CRM customer counts come from **third-party trackers whose methodologies are not disclosed** and which disagree with each other.

This is not a defect in the research; it is a property of the subject. It is stated here so no reader mistakes an inference for a disclosure.

---

## 2. Evidence grades

| Grade | Meaning |
|---|---|
| 🟢 **High** | Official company disclosure or statutory filing |
| 🟡 **Medium** | Credible secondary reporting of company statements, or company statements without filing backing |
| 🟠 **Low** | Third-party trackers and analyst estimates with no disclosure basis |
| 🔴 **Conflicting** | Sources materially disagree; reported as a range, never averaged |

### Claim-by-claim

| Claim | Value used | Grade | Where used |
|---|---|---|---|
| Paying customers | 1,000,000+ | 🟢 | §5, §13, §30 |
| Users | 150,000,000+ | 🟢 | §5, §30 |
| Customer growth YoY | +32% | 🟢 | §5, §13, §30, §47 |
| FY25 operating revenue (Indian entity) | ₹12,313 crore | 🟢 | §5, §18, §30 |
| FY25 revenue growth (Indian entity) | +17.8% | 🟢 | §5, §18, §30 |
| FY25 net profit | ₹3,191 crore (−3.3% YoY) | 🟢 | §5, §18, §30, §58 |
| Zoho suite / ManageEngine revenue split | 57% / 39% | 🟢 | §18, §39 |
| Geographic revenue split FY25 | NA ~41%, Asia ~30%, EU ~23% | 🟢 | §18, §35 |
| Zoho One pricing | $37 / $45 / $90 / $105 | 🟢 | §14, §18, §39 |
| Leadership (Davey Group CEO, Vembu Chief Scientist) | Jan 2025 restructure | 🟢 | §7 |
| Offices / countries | 90+ / 28 | 🟢 | §7, §30 |
| Founding history (AdventNet 1996, WebNMS, 2001 pivot, CRM 2005, rename 2009) | as stated | 🟢 | §7, §8 |
| $700M semiconductor fab shelved May 2025 | as stated | 🟢 | §8 |
| Employees | 19,000+ | 🟡 | §5, §7, §17, §30 |
| Data centres | 18+ | 🟡 | §5, §17, §40, §41, §44 |
| Zia LLM sizes (1.3B / 2.6B / 7B), H100 cluster, 2–4T tokens | as stated | 🟡 | §5, §29, §41 |
| Zia agents (25+), Agent Studio, Marketplace, MCP | as stated | 🟡 | §6, §29, §43 |
| No customer data on AWS/Azure/GCP; own server hardware | as stated | 🟡 | §17, §40, §41, §44 |
| Application counts (50+ / 55+ / 100+) | all three scopes reported | 🟡 | §6, §30 |
| Rural hub-and-spoke, Zoho Schools, transnational localism | as stated | 🟡 | §7, §9, §35 |
| G2 quality-of-support ≈ 7.6/10 | as stated | 🟠 | §25, §34, §45 |
| Zoho CRM customers (~186,000) | as stated | 🟠 | §11, §30 |
| Zoho CRM market share (~3–4%) | as stated | 🟠 | §11, §30 |
| Salesforce CRM share (21–24%) | range | 🟠 | §11 |
| Valuation (~$12.4B) | Hurun estimate | 🟠 | §30 |
| SaaS / CRM market sizing | ranges | 🟠 | §11, §13 |
| Arattai downloads | 17M–75M range | 🔴 | §30, §37 |
| HubSpot customer count | 180k–299k | 🔴 | §11 |

---

## 3. Source conflicts (full detail)

### 3.1 Revenue growth: 17.8% vs 20%
- **17.8%** — FY25 (year ended 31 March 2025), Indian entity, per RoC filing coverage (Entrackr, MediaNama, The Arc).
- **20%** — "revenue growth of 20% in 2025," group-wide, per Zoho's February 2026 announcement.
- **Not reconcilable from public data.** Different legal scope and different periods. **Both reported in §18 and §30.** Neither is treated as the definitive figure.

### 3.2 Employee count: 19,000+ vs 15,000+
- **19,000+** — Zoho's own February 2026 announcement.
- **15,000+** — diginomica and other secondary coverage, earlier.
- **19,000+ used** as most recent and official. The gap is *probably* growth over time plus group-versus-brand scope, but that reconciliation is inference, not evidence.

### 3.3 Application count: 45 / 50+ / 55+ / 100+
Four different numbers, all defensible, all measuring different things:
- **45** — apps a reviewer (Ravenlabs) actually tested in Zoho One
- **50+** — apps bundled in Zoho One (most common 2026 figure)
- **55+** — Zoho-brand applications (corporate boilerplate)
- **100+** — products across Zoho Corporation group, including ManageEngine

Secondary coverage conflates these constantly. §30 reports all scopes explicitly rather than picking one.

### 3.4 Arattai downloads: 17M vs 75M
- **3.5 lakh** (ThePrint, early), **5M in first 10 days** (TechRadar, Sept 2025), **17M** (DemandSage), **75M** (Deccan Herald, 2026).
- These span a period of extraordinarily rapid growth, and download-counting methodology varies by source (installs vs unique devices vs cumulative store counts).
- **Reported as a 17M–75M range and flagged 🔴.** Not used for any load-bearing claim. Arattai MAU (~1M) is the more meaningful figure and is what §37 actually reasons from.

### 3.5 HubSpot customer count: ~180,000 vs ~299,458
Almost certainly a CRM-customers versus total-platform-customers definitional difference. Flagged and **deliberately excluded from any comparative claim** in §11 beyond noting the conflict.

### 3.6 FY25 revenue in USD
₹12,313 crore converts to roughly **$1.44B at ₹85.5/USD**; some outlets cite **$1.48B**; Latka cites **$1.5B ARR** (a different metric entirely). §5 and §18 report **≈$1.4–1.5B** rather than a false-precision single figure.

### 3.7 Zoho valuation
**~$12.4B** (Hurun, 2025) and **"over $10B"** (analyst commentary). Both modelled — Zoho has never raised capital, so **no transaction has ever set a price**. Every valuation is a construct.

---

## 4. Author-constructed content

None of the following are facts about Zoho. They are the author's analysis, clearly separated here so they are never mistaken for reporting.

### 4.1 Personas (§20)
Priya, Daniel, Aarti and Marcus are **composites**, constructed from documented customer segments, public review sentiment, and the structure of Zoho's partner channel. No individual was interviewed. Names, companies, locations and quotes are invented.

### 4.2 Journey and flow analysis (§22, §23)
The satisfaction curve, the "week three stall," the churn and under-activation nodes, and the three structural problems in the flow are **inferred from product structure plus public review themes**. Zoho publishes no funnel data. The specific three-week timing is illustrative, not measured.

### 4.3 Heuristic and audit scores (§25, §26, §27)
The Nielsen ratings, the 2.9/5 composite, the cognitive-load table, the UI assessments and the WCAG assessment are the **author's heuristic judgement** of publicly observable surfaces, supplemented by Zoho's published VPAT/ACR documents. No instrumented testing, no screen-reader testing, no moderated sessions were performed.

### 4.4 North Star metric (§31)
**Weekly Active Applications per Paying Organisation is a proposal.** Zoho has not disclosed a North Star metric. The counter-metric, the target framing ("median 2 → 4"), and the comparison table are all authored.

### 4.5 The entire feature proposal (§46–§56)
**"Zoho Outcomes," Blueprints, and the Zia Setup Agent do not exist.** They are this case study's proposal. Everything downstream is likewise authored:

| Section | Authored content |
|---|---|
| §46 | Opportunity impact/effort/fit ratings |
| §47 | All RICE inputs. The **9 person-month effort estimate is an outside-in guess** with no access to Zoho's engineering context or codebase |
| §48, §49 | MoSCoW and Kano classifications |
| §50 | Feature concept, impacts, trade-offs, risks |
| §51 | Entire PRD. **Every baseline in the success-metrics table is "not disclosed" because it genuinely is.** All targets (−50%, +15pp, +8pp, −25%, −35%, <5%) are illustrative and have no empirical basis |
| §52 | All five wireframe descriptions |
| §53 | Phase durations and gate criteria |
| §54 | Experiment design, variants, guardrails, the 8-week duration, the pre-registered failure condition |
| §55 | All KPI targets |
| §56 | All roadmap dates |
| §57 | Risk severities and mitigations |

### 4.6 Strategic interpretation
The central thesis — *Zoho's moat is a cost structure; its AI architecture is downstream of its pricing, which is downstream of its funding model* — is the **author's interpretation**, not a Zoho statement. It is well-supported by the sourced facts but it is an argument, not a disclosure.

Similarly authored: the "57% of Salesforce's customers on 3–4% of revenue" framing (§11), the assessment that the All-Employee/Flexible pricing gap is deliberate (§18), the "threshold problem not quality problem" reading of bimodal reviews (§34), the judgement that Zoho is "not a network-effects business" (§37), and the critique that Zoho's strategy is supply-side while its constraint is demand-side (§38).

### 4.7 Forecast (§58)
The three-year outlook is **speculative**. The claim that Zia must "stay good enough" and that frontier-model progress is the binding external variable is reasoning, not prediction backed by evidence.

---

## 5. What would materially improve this analysis

1. **Moderated usability sessions** with 3–5 genuine first-time Zoho One administrators, timed from signup — would convert §22/§23/§25 from inference to measurement.
2. **Interviews with 2–3 Zoho implementation partners** — would validate or kill the configuration-hours claim underpinning §47 and §51.
3. **Access to Zoho's actual activation funnel data** — the single largest gap. Every target in §51 is currently a guess.
4. **A quantitative ManageEngine teardown.** It is 39% of revenue and receives disproportionately little attention in this case study relative to its size — the largest scope gap in the analysis.
5. **Independent third-party attestation** of the infrastructure and AI-privacy claims in §44, which are currently reported as vendor claims.

---

## 6. Asset status

No raster image assets were generated. All diagrams are **Mermaid** (timeline, flowchart, journey, gantt), which renders natively on GitHub. Figures 1 (§8) and 2 (§22) are labelled inline. Candidates for a future rendering pass: FY25 revenue split, geographic split, RICE factor breakdown, and a Zoho-vs-competitor pricing bar chart.
