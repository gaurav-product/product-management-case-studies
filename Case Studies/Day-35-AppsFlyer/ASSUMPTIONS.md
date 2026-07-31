# ASSUMPTIONS — Day 35: AppsFlyer

Companion file to `README.md`. This document exists so that the case study can be audited rather than trusted. It records what is evidenced, what is inferred, what is invented, and what conflicts remain unresolved.

**Research date:** 31 July 2026
**Case study:** Day 35 of 90 — AppsFlyer
**Author:** Gaurav Singh

---

## 1. How to read this file

The case study makes one central claim: **AppsFlyer's product is refereeing rights — a trust asset — not measurement accuracy, and the June 2026 Series E is the first time that asset has been priced explicitly.**

That claim is an *interpretation*. It is built on facts that are mostly well-evidenced, but the interpretation itself is mine and is not something any source states. This file separates the two.

Three grades of content appear in the case study:

| Type | Meaning |
|---|---|
| **Sourced fact** | Something a source states. Graded High / Medium / Low / Conflicting below |
| **Derivation** | Arithmetic or triangulation I performed on sourced facts. Reasoning is always shown |
| **Author construction** | Personas, scores, targets, proposals, scenarios. Not evidence of anything about AppsFlyer |

---

## 2. Evidence grades by claim

### High confidence

| Claim | Sources |
|---|---|
| Series E: over $1B raised, $2.7B valuation, June 2026 | CTech/Calcalist (22 Jun 2026); Mobile Dev Memo (22 Jun 2026); PPC Land; Axios (via MDM) |
| Investors: Moloco, Google, Meta, Unity | CTech; Mobile Dev Memo; PPC Land |
| Round was largely **secondary** — shareholder liquidity, not primary capital | CTech, explicitly |
| Terms: minority, non-controlling, non-exclusive; no preferential access to APIs, measurement signals, attribution logic, or commercial terms | CTech; CEO blog quoted verbatim in Mobile Dev Memo |
| Investors publicly committed to continue working with multiple measurement providers | CTech |
| Apollo / Fortissimo acquisition talks at **$1.9B collapsed** (March 2026) after Apollo sought additional protection clauses; board advised by Goldman Sachs | CTech; PocketGamer.biz; Mobile Marketing Reads |
| Founded 2011 by Oren Kaniel (CEO) and Reshef Mann (CTO) | CTech; Sacra |
| AppLovin acquired Adjust in 2021 | Mobile Dev Memo; Singular; multiple |
| Nov 18 2025: eight-product "Modern Marketing Cloud" release | AppsFlyer newsroom; BusinessWire; PPC Land; TechAfrica; Intelligent CIO |
| Google retired Privacy Sandbox APIs (incl. Attribution Reporting, Topics, Protected Audience), Chrome and Android, October 2025 | AdExchanger; Usercentrics; Google Privacy Sandbox status pages |
| The MMP category originated in a Meta (Facebook) programme authorising third parties to interface with its measurement API | Mobile Dev Memo |
| General Atlantic led the Series D and retains board representation | CTech; Sacra; TechCrunch (2020) |

### Medium confidence

| Claim | Sources | Why not High |
|---|---|---|
| ARR ~$500M, profitable, positive cash flow | CTech; PocketGamer | Company-reported via press, not audited; and conflicts with C1 below |
| ~1,300 employees after a ~7% reduction (~100 roles) in 2025 | CTech (Jun 2026); CTech (2025 layoffs) | Single outlet, though internally consistent across two reports |
| General Atlantic holds an estimated 15–20% | CTech | Explicitly described as an estimate |
| AppsFlyer + Adjust ≈ 45% of global MMP revenue (2024) | IntelMarketResearch | Single market-research source; used as the basis for a derivation, so weakness propagates |
| AdAttributionKit has negligible traction; no meaningful WWDC 2026 update | Mobile Dev Memo; Singular; Kochava | Practitioner assessment rather than measured adoption data — but three independent practitioners agree |
| ~$42k implied average revenue per paying customer | Derived from Sacra ($395M / ~12,000) | Derivation from two Medium inputs |
| IPO explored at a reported $4–5B (2024); PE talks at ~$3.5B (2025) | Bloomberg via secondary; CTech | Reported ranges, not confirmed terms |
| Only ~12% of top-1000 Chrome-spend advertisers completed ARA integration testing (March 2026) | PerfxAd | Single source; see conflict C9 |

### Low confidence

| Claim | Why Low |
|---|---|
| **All pricing figures** — $0.07/install Growth; $0.03–$0.05 enterprise; Zero tier 12,000 free conversions; 12-month minimum contract | Third-party pricing aggregators (Metacto, Grovs, Vendr, businessofapps), not company disclosure. Enterprise pricing is negotiated and these are indicative at best |
| **Entire accessibility section (§27)** | No VPAT located, no audit run. The table is reasoned expectation for a product of this class, explicitly labelled as such in the case study |
| **UX / UI / IA assessments (§24–§26)** | Derived from product documentation, release notes and category norms. No hands-on use of the AppsFlyer console informed these sections |
| Pain point P5 (fraud dispute workflow friction) | Inferred from how cross-party evidentiary disputes work generally; no direct evidence |
| Pain point P8 (event misconfiguration surfacing late) | Category norm; no AppsFlyer-specific evidence |
| Technical architecture internals (§41–§42) | Reconstructed from product surface area and public documentation. AppsFlyer publishes no architecture reference |
| Partner integration count | Range of 9,000–12,000+; see C6 |

---

## 3. Source conflict table

**No conflict below has been averaged away.** Where I formed a view, the reasoning is given; where I did not, both readings stand.

### C1 — Annual recurring revenue

| Source | Figure | Date |
|---|---|---|
| Sacra | ~$395M ARR | 2023 |
| GetLatka | ~$508.4M est. ARR | 2024 |
| CTech / PocketGamer | ~$500M ARR | 2026 |

**Resolution: unresolved, both trajectories retained.** If Latka's 2024 estimate is right, revenue has been roughly flat for two years. If Sacra's 2023 figure is the better anchor, the company has grown ~27% over three years. These imply materially different stories about the business, and I cannot adjudicate between them. The case study uses "~$500M" for the current figure (best-sourced, most recent, two outlets) and **explicitly describes growth as flattened rather than asserting a growth rate**. Note that Latka figures are modelled estimates, which is a reason to weight them lower — but not a reason to discard them.

### C2 — Customer count

| Source | Figure |
|---|---|
| Sacra | ~12,000 paying customers; 80,000+ apps supported |
| AppsFlyer / CTech | 15,000+ brands |
| AppsFlyer | 80,000+ companies helped |

**Resolution: not a genuine conflict — three different denominators.** "Paying customers," "brands," and "companies helped" (which likely includes free-tier and historical users) are not the same population. The case study reports all three with their denominators attached rather than picking one. Anyone citing a single customer number for AppsFlyer without specifying the denominator is over-claiming.

### C3 — ATT opt-in rate

| Source | Figure | Period |
|---|---|---|
| Adjust | ~35% | Q2 2025 |
| Business of Apps / panels | ~38% | Q1 2026 |
| AppsFlyer panel | ~50% | early 2024 |

**Resolution: fully retained — this conflict is load-bearing evidence, not noise.** Two MMPs measuring the same industry metric report figures ~15 points apart. Plausible explanations include panel composition (each vendor's customer mix skews the sample), vertical mix, geographic mix, and differing definitions of the denominator. I did not resolve it and I would argue resolving it would be a mistake: the disagreement demonstrates that this market has **no observable ground truth**, which is the foundation of the case study's argument that legitimacy beats accuracy (§11, §59 lesson 3).

### C4 — Valuation

| Point | Figure |
|---|---|
| Series D / extension (2020) | ~$2B |
| IPO ambition reported (2024) | $4–5B |
| PE acquisition talks (Aug 2025) | ~$3.5B |
| Apollo / Fortissimo offer (Mar 2026, collapsed) | $1.9B |
| Series E (Jun 2026) | $2.7B |

**Resolution: all retained as a sequence.** The 2.6x spread within roughly twenty-four months is treated in the case study as a finding in its own right (§7) rather than a data problem — it indicates the market could not agree on what kind of asset this is.

### C5 — Series D structure

| Source | Account |
|---|---|
| CTech / TechCrunch | $210M, January 2020, led by General Atlantic |
| Sacra | Series D extension in late 2020 bringing the round to ~$225M, Salesforce Ventures participating |
| Secondary search result | "$300M Series D at $2B valuation, January 2021" |

**Resolution: source 3 rejected.** It conflicts on amount and date with two independent contemporaneous reports. Sources 1 and 2 are compatible — an initial round plus a later extension — and both are used. Total funding is reported as "$294M (2020)" by Sacra's funding field and "more than $300M since founding" in Sacra's narrative; that internal inconsistency within one source is noted but is immaterial to any argument.

### C6 — Partner integration count

| Source | Figure |
|---|---|
| AppsFlyer Partner Marketplace | 9,000+ |
| Techmagnate (2025) | 11,000+ tech and media partners |
| Commonly cited industry figure | 12,000+ |

**Resolution: reported as a range (9,000–12,000+).** Likely reflects different dates and different definitions of "integrated partner" (active vs. available vs. certified). No argument in the case study depends on which is correct.

### C7 — Headquarters

Sacra lists San Francisco, CA. Israeli business press covers AppsFlyer as an Israeli company with Israeli operations and Israeli founders. **Resolution: both correct.** Treated as US commercial HQ with Israeli engineering base, not flagged as a conflict in the body text beyond a note in §7.

### C8 — MMP market size

| Estimate | 2025 | 2032 | CAGR |
|---|---|---|---|
| A | $3.5B | $7.8B | 12.2% |
| B | $1.85B | $4.1B | 12.3% |
| C | $320M | $639M | 12.5% |

**Resolution: Estimate C rejected on arithmetic grounds.** If AppsFlyer alone is ~$500M ARR and AppsFlyer plus Adjust is ~45% of global MMP revenue, the global pool cannot be $320M. Estimates A and B both survive; B is favoured because it is closer to the ~$2.0–2.5B implied by triangulation. **The tell across all three is that they agree on ~12% CAGR while disagreeing 10x on the base** — a signature of assumed growth rates applied to differently-scoped bases. The case study uses a derived SAM of ~$2.0–2.5B and shows the derivation rather than citing any published figure.

### C9 — Privacy Sandbox timeline

| Source | Claim |
|---|---|
| AdExchanger, Usercentrics, Google status pages | Remaining Privacy Sandbox APIs including Attribution Reporting retired; Privacy Sandbox on Android deprecated as of 17 October 2025 |
| PerfxAd | April 2026 announcement delaying Attribution Reporting API general availability from Q1 to Q3 2026 |

**Resolution: conflicting and unresolved.** These are difficult to reconcile — an API cannot straightforwardly be both retired in October 2025 and have its GA rescheduled in April 2026. Possible explanations: staged deprecation with different timelines for Chrome and Android; a web-standards continuation distinct from the retired product; or a reporting error in one source. **The case study uses "retired October 2025" as the primary reading** because it has multiple independent sources including Google's own status pages, and flags the inconsistency explicitly rather than omitting the awkward second source. A reader who cares about the exact Android timeline should verify independently.

### C10 — Adjust acquisition price

Reported as "approximately $1BN" by Mobile Dev Memo and repeated elsewhere. **Never officially disclosed by AppLovin.** Always written as "a reported ~$1B" in the case study.

### C11 — Employee count

CTech (June 2026) reports ~1,300 employees after a ~7% workforce reduction; CTech (2025) reports ~100 employees laid off. **These corroborate rather than conflict** — 100 is ~7% of ~1,400. Used as mutual verification.

---

## 4. Derivations (arithmetic I performed)

Each of these is my calculation, not a sourced figure. Reasoning is shown so the arithmetic can be checked.

| Derivation | Method | Result | Weakest input |
|---|---|---|---|
| **Global MMP revenue pool** | AppsFlyer ~$500M + Adjust (unknown, assumed smaller) ≈ 45% of market → market ≈ $2.0–2.5B | ~$2.0–2.5B | The 45% figure (single source); Adjust's revenue is unknown |
| **SAM** | Equals the derived pool above | ~$2.0–2.5B | Inherits the above |
| **SOM as % of SAM** | $500M ÷ $2.0–2.5B | ~20–25% | Inherits both |
| **Implied ARPC** | Sacra $395M ÷ ~12,000 paying customers | ~$42,000/year | Blends a long tail with a concentrated head; near-meaningless as a typical value |
| **Revenue per employee** | ~$500M ÷ ~1,300 | ~$385,000 | Both inputs Medium |
| **Series E premium over failed offer** | ($2.7B − $1.9B) ÷ $1.9B | ~42% | Both figures High confidence; this is the most reliable derivation in the document |

---

## 5. Author-constructed content

**None of the following is evidence about AppsFlyer.** All of it is analysis, and it should be read as one person's reasoning, not as reporting.

### The central thesis
The claim in §5 — that neutrality rather than accuracy is AppsFlyer's product, that the Series E prices that asset, and that this creates a product obligation to make neutrality verifiable — is **my interpretation**. Oren Kaniel makes a related claim ("neutrality isn't a feature, it's the foundation") and Eric Seufert makes a related claim ("too big to let fail"). Neither states the product implication I draw from it. That step is mine and is the most contestable thing in the document.

### Personas (§20)
Nikhil (UA manager, Bengaluru), Rachel (VP Growth, New York), Daniel (data engineer, Berlin), Priya (counsel, Mumbai) are **composites**. They are not research subjects, no interviews were conducted, and every quotation attributed to them is an invented illustration of a reasoning pattern. Their value is as analytical tools; they carry zero evidentiary weight.

### The feature proposal (§50–§53)
**"Provenance" is entirely author-constructed.** AppsFlyer has not announced, hinted at, or (so far as I can determine) discussed anything like it. This includes:

- All four components (methodology registry, changelog, change-attribution diff, uncertainty encoding, attestation, provenance receipts)
- All eleven requirements (R1–R11) in the PRD
- All three ASCII wireframes in §52 — including the specific numbers shown (124,880 installs, +4.2%, v14.2, seven networks), which are illustrative fabrications
- The rollout Gantt and all its dates
- The monetisation structure in §39 (free changelog, included diff, enterprise receipts)

### Scores and prioritisation
- **RICE** (§47): Reach 9, Impact 4, Confidence 70%, Effort 7 person-months → 3.6. Every input is my judgement. The pessimistic sensitivity case (7 / 3 / 45% / 12 → 0.79) is also mine, as is the argument that a low score is acceptable for an insurance-type investment
- **MoSCoW** (§48) and **Kano** (§49): entirely author-assigned
- The effort estimate of 7 person-months is **a guess with no basis in AppsFlyer's actual codebase or team structure**

### Metrics and targets
- The **North Star metric** (§31) — "monthly ad spend reconciled across three or more networks by accounts that took action on the result" — is proposed, not AppsFlyer's
- **Every target in §51 and §55** (−30% tickets, <60s explanation, −20% review cycle, −50% objection rate) is invented. Note that **every corresponding baseline is marked "not disclosed"**, which means these targets are directionally illustrative and cannot be validated
- The instrumentation recommendations in §32 are mine

### Experiments (§54)
The three-arm A/B design, the decision rules, and the pre-committed kill criteria are all author-constructed. The contamination limitation I identify (a public changelog cannot be randomised) is a real methodological problem with my own design that I chose to state rather than hide.

### Strategic assessments
- The three future scenarios in §58
- The critique of the "Modern Marketing Cloud" positioning in §38
- The sequencing opinion in §56 that depth on the November 2025 release should precede the proposal
- All nine risks and mitigations in §57
- All twelve interview questions in §60
- The seven PM lessons in §59

### Qualitative product assessments
All of §24 (IA), §25 (UX audit), §26 (UI audit) and §27 (accessibility) are reasoned from documentation, release notes and category norms. **No hands-on use of the AppsFlyer console informed any of them.** The specific claim I am least confident in is that discrepancy investigation has no in-product home — that is inference from IA structure and support-load patterns, not observation, and a current AppsFlyer user could reasonably contradict it.

---

## 6. What would materially improve this analysis

In rough order of how much each would change the conclusions:

1. **Access to AppsFlyer's console.** Roughly a quarter of this document (§24–§28, parts of §45) is reasoned rather than observed. Hands-on use would either confirm or substantially rewrite the UX argument that the feature proposal partly rests on.
2. **Net revenue retention and module attach rate.** These are the two undisclosed numbers that would most change the analysis. NRR would settle the C1 growth ambiguity; attach rate would show whether the November 2025 release is landing, which determines whether the §56 sequencing recommendation is right.
3. **Interviews with five to ten actual UA managers**, specifically asking whether the Series E has changed how they think about AppsFlyer. This is the single cheapest way to test the central thesis, and it would take a week. Without it, P7 in §45 is an inference from a news event.
4. **Adjust's revenue and customer-count trajectory since the 2021 acquisition.** The Adjust natural experiment is the strongest evidence for the thesis, and I am relying on qualitative reporting about team absorption rather than on numbers. If Adjust grew normally post-acquisition, the neutrality argument weakens considerably.
5. **AppsFlyer's own churn analysis by reason code.** If "chose a competitor for independence reasons" is a category that exists in their CRM, its historical rate would be decisive.
6. **The primary CEO blog post**, fetched directly rather than quoted through two secondary sources.
7. **Audited financials.** Everything financial here is press-reported or analyst-estimated.
8. **A second independent source for the 45% MMP market-share figure**, since three derivations depend on it.
9. **Clarification of C9** — the Privacy Sandbox timeline inconsistency — from Google's own changelog rather than trade press.
10. **Six to twelve months of elapsed time.** The Series E closed roughly six weeks before publication. The thesis is about consequences that have not had time to occur.

---

## 7. Known limitations of the research process

- **Retrieval:** AppsFlyer's CEO blog post could not be fetched directly in this session. It is quoted via CTech and Mobile Dev Memo, which quote it at length and consistently with each other. Several AppsFlyer product and pricing pages were accessed through search summaries rather than full page retrieval.
- **Recency bias:** the June 2026 Series E dominates this analysis because it is recent and dramatic. A case study written in March 2026 would have emphasised the collapsed Apollo deal and reached a gloomier conclusion; one written in 2024 would have emphasised the IPO track. I have tried to guard against this by grounding the thesis in the 2021 Adjust precedent rather than only in the 2026 event, but the bias is real and worth naming.
- **Practitioner-source concentration:** Mobile Dev Memo is cited three times and is the single most influential secondary source on this document's framing. Eric Seufert is an unusually well-informed analyst, but he is one analyst with a point of view.
- **Competitor-published data:** ATT opt-in figures come from Adjust and AppsFlyer, who are competitors with commercial incentives around how signal loss is perceived. I treated this as a feature of the evidence rather than a defect — see C3 — but readers should hold those numbers loosely.
- **No financial modelling.** I did not build a revenue or valuation model. The valuation discussion is descriptive.
- **Single-day research.** This is a 90-day-challenge case study researched and written in one day. Depth is bounded accordingly.

---

## 8. Methodology note

**Research date:** 31 July 2026. All figures are as of that date.

**Approach**

1. Establish corporate and financial facts from contemporaneous business press (CTech/Calcalist) and analyst company profiles (Sacra, GetLatka), cross-checking every material figure across at least two sources
2. Establish industry framing from practitioner analysis (Mobile Dev Memo) and competitor-published research (Adjust, Singular, Kochava) — anticipating that competitor-published data on shared metrics would be where conflicts appeared, which it was (C3)
3. Establish platform state (ATT, SKAdNetwork, AdAttributionKit, Privacy Sandbox) from platform documentation and specialist trade press
4. Treat market-sizing reports with explicit scepticism; triangulate against known company revenues rather than accepting published totals (C8)
5. Preserve every conflict rather than resolving silently; where a view was formed, show the reasoning
6. Mark every undisclosed figure as "not disclosed" rather than estimating it

**Standing rules applied throughout**

- No invented baselines. If a number was not disclosed, the case study says so.
- No averaging of conflicting sources.
- No image assets referenced. All diagrams are Mermaid; all wireframes are ASCII.
- Author constructions labelled as such, both in-line and in §5 above.

**On the central thesis specifically.** It is falsifiable, and the case study says how: if AppsFlyer's renewals, cross-network usage breadth and enterprise win rates are unaffected over the next four quarters, the thesis is wrong and neutrality was a narrative wrapper around ordinary switching costs. §54 Arm A ≈ Control is a genuinely possible outcome. I would rather publish a claim that can be shown wrong than one that cannot be evaluated.

---

*Companion to `README.md` — Day 35 of 90 · [Repository](https://github.com/gaurav-product/product-management-case-studies)*
