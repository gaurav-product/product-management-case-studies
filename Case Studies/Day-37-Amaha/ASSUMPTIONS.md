# Day 37 — Amaha · Assumptions, Evidence Grades and Source Conflicts

**Research date:** 2 August 2026
**Method:** Public sources only. No affiliation with Amaha, no access to internal data, no user interviews.

---

## 1. Evidence grades by claim

| Claim | Grade | Basis |
|---|---|---|
| Founded 2016 as InnerHour by Dr. Amit Malik | High | Multiple independent sources |
| Neha Kirpal joined as co-founder 2019 | High | Company communications, press |
| Treats bipolar, schizophrenia, OCD, ADHD, addictions | High | Company materials, press release |
| Centres in Mumbai, Bangalore, Delhi | High | Multiple sources |
| 15+ languages, 600+ cities | Medium | Company-reported, not independently verified |
| 5M+ lives impacted via app | Low | Company-reported; "lives impacted" is undefined and likely counts installs |
| 700,000+ covered by workplace programmes | Medium | Company-reported |
| ~INR 50 crore round led by Fireside, Jan 2024 | High | PR Newswire, corroborated |
| Session pricing ₹1,000–₹3,500+ | Medium | Third-party review sites, not Amaha's own published rate card |
| 0.75 psychiatrists per 100,000 in India | High | Widely cited, WHO-referenced |
| ~150M Indians need mental healthcare | High | NMHS |
| Treatment gap 70–92%, overall 84.5% | High | NMHS 2015-16 |
| Category median 30-day retention 3.3% | High | Peer-reviewed literature |
| Cultural adaptation → >75% adherence, <11% dropout | High | Systematic review, JMIR 2026 |
| Amaha's own retention figures | **None** | Not disclosed anywhere |
| Amaha's clinician utilisation | **None** | Not disclosed |
| Amaha's revenue, ARPU, conversion rates | **None** | Not disclosed |

---

## 2. Source conflicts — both figures retained, none averaged

| # | Item | Source A | Source B | Resolution |
|---|---|---|---|---|
| 1 | Total funding | $11.7M (GrowthJockey roundup) | $20.6M across 5 rounds (Tracxn) | **Both retained.** Likely a vintage difference — the lower figure may predate the 2024 round. Not resolvable from public data. Neither used in any calculation. |
| 2 | Clinical team size | 150+ therapists and psychiatrists (PR Newswire, 2024) | 110+ psychiatrists and therapists (elfinahealth) | **Both retained.** May reflect different dates or different definitions of "team" (employed vs. paneled). |
| 3 | Round composition | "INR 50 crore round led by Fireside" (PR Newswire headline) | "Fireside brought in Rs 36 crore, rest from family offices and angels" (Medicircle) | **Reconcilable, not a true conflict** — 50cr total of which 36cr from Fireside. Noted for precision. |
| 4 | Treatment gap | 70–92% range; 84.5% overall (NMHS) | "up to 95%" (secondary sources) | **Both retained.** The 95% figure appears to be region- or disorder-specific rather than national. The case study uses the NMHS range as primary. |
| 5 | Reach claims | "5 Million lives globally through mobile app" | "700,000+ individuals" via workplace programmes | **Not a conflict** — different denominators (app installs vs. covered members). Flagged because they are easy to conflate. |

**Rule applied throughout:** where sources disagree, both figures appear in the case study with the conflict named. No figure was averaged, and no conflicting figure was silently dropped.

---

## 3. Everything author-constructed

Nothing in this list came from Amaha. All of it is my own construction and should be read as analysis, not fact.

**Entirely author-constructed:**

- **All three personas** (Ritu, Arjun, Sneha) — illustrative, not derived from research
- **SAM and SOM estimates** (~35–45M, ~1.5–3M) — reasoned from TAM and constraints, not from any published figure
- **The entire competitor positioning table** — my read of public positioning, not a benchmark study
- **SWOT** — my judgment throughout
- **All RICE scores** — subjective, including the Reach reinterpretation as "correctly routed"
- **The proposed North Star metric** — Amaha has not published one
- **The entire feature proposal (Guided Care Match)** — mine, not a leaked roadmap
- **The full PRD, all requirements, all priorities**
- **All success-criteria targets** (60% assessment completion, 55% route adherence, +30% retention, +20pp, <60s) — hypotheses, with baselines explicitly marked "not disclosed"
- **The rollout timeline and all dates**
- **The three-variant A/B design**
- **The risk table and mitigations**
- **The claim that Amaha's front door relies on user self-selection** — inferred from public app descriptions and review content, **not verified by walking the current onboarding flow**

That last item is the most significant limitation in this teardown and is flagged again in §5.

---

## 4. The central thesis — status

The thesis is that Amaha's binding constraint is clinician supply, making allocation rather than engagement the core product problem.

**What supports it:** the psychiatrist density figure (0.75/100k) is well established and is a hard structural constraint. Amaha's condition list confirms genuine clinical depth. Category retention data confirms that installs do not translate to treatment.

**What would falsify it:** if Amaha's clinician utilisation is in fact low — that is, if clinicians have unfilled slots — then supply is not the binding constraint, demand conversion is, and the entire proposal points the wrong way. **I could not check this.** Utilisation is not disclosed. This is the single assumption on which the argument most depends and it is unverified.

A reader inside Amaha would know this number immediately and could dismiss or confirm the thesis in one sentence.

---

## 5. What would materially improve this analysis

Ranked by how much each would change the conclusions:

1. **Clinician utilisation rate.** Would confirm or destroy the central thesis. Highest value by a wide margin.
2. **Walking the actual current onboarding flow.** The claim about self-selected entry is inferred, not observed. This is a factual claim I should have verified directly and did not.
3. **Amaha's own retention and activation funnel.** The category baseline is a poor substitute.
4. **Interviews with 5–10 users who churned in week one.** Would test whether the churn cause is mis-routing (my hypothesis) or price, stigma, or content quality.
5. **The existing self-assessment's actual content and placement.** I assume it is under-used as a routing input; it may already route more than public materials suggest.
6. **B2B contract structure.** Per-member vs. per-session economics would sharpen §12 considerably.

---

## 6. Methodology note

Research conducted 2 August 2026 via web search across company communications, press releases, funding databases (Tracxn, Crunchbase), peer-reviewed literature on digital mental health engagement, the NIMHANS National Mental Health Survey, and third-party review and comparison sites.

Clinical and epidemiological figures were prioritised from peer-reviewed and government sources. Company performance figures come from company-controlled channels and carry the corresponding reliability discount — particularly "5 million lives impacted," which is a marketing metric rather than a clinical one.

No Amaha employee was contacted. No internal document was accessed. Every quantitative claim about Amaha's product performance in this teardown is either sourced to a public figure or explicitly marked "not disclosed."

---

## 7. A note on subject matter

This teardown analyses a clinical mental health service. Two deliberate choices follow from that:

The proposal treats crisis escalation as an unconditional interrupt rather than a funnel step, and excludes it from all A/B variants. A routing system in this domain that experiments on crisis pathways would be indefensible regardless of what the data showed.

The proposal also explicitly stops short of diagnosis. It recommends a level of care and leaves clinical judgment with clinicians. That boundary is drawn for ethical and regulatory reasons, and it constrains how much of the allocation problem software can solve — a limitation I take to be correct rather than unfortunate.
