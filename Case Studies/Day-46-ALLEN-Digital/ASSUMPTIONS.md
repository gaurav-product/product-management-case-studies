# ASSUMPTIONS — Day 46: ALLEN Digital

**Companion to** [`README.md`](./README.md) · **Author:** Gaurav Singh · **Date:** 11 August 2026

This file exists so that a reader can separate, without effort, what ALLEN has disclosed from what I have constructed. Everything below is mine. None of it is a finding, and none of it should be quoted as ALLEN's position.

**Rule applied throughout the case study:** if a number is not in a filing, an official document, a regulator's record or a company results release, it appears here — with its basis, its load on the argument, and the observation that would falsify it.

---

## 1. What is verified, and what is not

### 1.1 Verified — used as fact in the analysis

| Fact | Value | Source | Grade |
|---|---|---|---|
| ALLEN FY25 operating revenue | ₹3,067 Cr | Entrackr, from filings | 🟡 |
| ALLEN FY25 total revenue / PAT | ₹3,307 Cr / ₹41 Cr | Entrackr, from filings | 🟡 |
| ALLEN FY24 revenue / PAT | ₹3,245 Cr / ₹136 Cr (−44%) | Entrackr, from filings | 🟡 |
| ALLEN FY25 net cash | ~₹2,000 Cr | Entrackr | 🟡 |
| Non-Kota revenue share | 64% (FY24) → 75% (FY25) | Entrackr | 🟡 |
| Campuses added FY25 | 106, incl. 62 in 17 new cities | Entrackr | 🟡 |
| Bodhi Tree investment | US$600M (2022) | PR Newswire / Business Standard | 🟢 |
| Doubtnut acquisition | Dec 2023, reported ~US$10M | Business Standard | 🟡 |
| Rakesh Ranjan appointed CEO, ALLEN Online | 24 Sep 2025 | Business Standard | 🟢 |
| ALLEN Digital module inventory (Improvement Book, Rewards gate, Leave Management, Study Drop, Mentorship, hardware floor, content-protection terms) | As described | ALLEN's own help documentation | 🟢 |
| PW FY26 revenue / online / offline | ₹3,900 Cr / ₹1,954 Cr / ₹1,774 Cr | PW results reporting | 🟢 |
| PW FY26 online ACPU / offline ARPU | ₹4,104 / ₹36,625 | PW results reporting | 🟢 |
| PW paid users / offline enrolments / centres | 5.34M / 467,500 / 353 | PW results reporting | 🟢 |
| Rajasthan Coaching Centres Bill 2025 provisions, **including that it covers physical centres only** | As described | PRS Legislative Research | 🟢 |
| NEET-UG registrations 2024 / 2025 / 2026 | ~24L / ~22.76L / >26L expected | Careers360 | 🟡 |
| JEE Main 2026 Session 1 registrations | 14.5 lakh | Careers360 (NTA) | 🟡 |
| MBBS seats, NEET-UG 2025 | ~1.26 lakh, 766 colleges | Careers360 (NMC/MCC) | 🟡 |
| ALLEN IPO status | Bloomberg reported early conversations (Apr 2026); **no DRHP filed** | IPO Market, citing Bloomberg | 🟡 |

### 1.2 Company claims — reported, not independently verifiable

Treated as claims throughout, never as evidence for a conclusion:

- 1M+ student queries resolved monthly at **98.84% accuracy** — method unpublished.
- AI system at **AIR-8-equivalent, NEET 2025** — equivalence method unpublished.
- **~5% score increase** among students using digital features — correlational; see README §29.1.
- 1,200+ IIT admissions with top-100 ranks (220 from live programmes); 647 government medical seats in 2024 — **selection-biased outcome claims** with no published denominator.
- ~360,000 full-course students (FY24); knowledge graph as platform foundation.

### 1.3 Not disclosed by ALLEN — stated as unavailable, never estimated

- A standalone P&L, contribution margin or burn figure for the digital arm.
- Actual FY25/FY26 online revenue or online student count.
- Any completion, persistence, attendance-decay, recovery or renewal metric.
- Study Drop reason distribution.
- Accessibility conformance (VPAT/WCAG) or security certifications.
- Safeguarding policy for 1:1 adult–minor mentorship.
- Public developer/partner API strategy.
- FY26 financials (not public at the time of writing).

---

## 2. Load-bearing assumptions

Ordered by how much the argument depends on them. **A1 and A2 are the two that, if wrong, take the case study with them.**

### A1 — Online lapse is common, and it is a real dynamic rather than an artefact of my reasoning
- **What I assume:** a meaningful share of ALLEN Online learners lapse from their intended study pattern during a term, and lapse is followed by further disengagement rather than by routine recovery.
- **Basis:** the *structure* of the product (README §23–25) — the recovery route from absence is points-gated and administrative — plus the general pattern of unsupervised self-paced learning. **No ALLEN data supports or contradicts this, because none is published.**
- **Load:** total. It is the premise of §46's convergence and the whole of §50.
- **Falsified by:** ALLEN's Phase 0 retrospective showing that lapse is rare, or that lapsing students recover at high rates unaided, or that lapse does not predict non-renewal once prior attainment is controlled.
- **Honest status:** this is a **hypothesis derived from product structure**, and the README says so in §22, §46 and §64. It is the single largest unverified load in the document.

### A2 — ALLEN's reported FY25 online plan figures are accurate
- **What I assume:** the April 2024 trade reporting of ~40,000–50,000 online students and ₹200–250 Cr online revenue reflects ALLEN's actual plan.
- **Basis:** YourStory, April 2024. Single secondary source. 🟠
- **Load:** carries §13.5's derived ARPU of ₹40,000–62,500 — the most striking number in the case study — and therefore line L3 of §46 and the pricing argument in §39.
- **Falsified by:** ALLEN disclosing materially different online figures; or the plan having been revised after April 2024 (entirely possible — the digital CEO changed in Sept 2025).
- **Mitigation applied:** the derivation is presented as arithmetic on a *reported plan*, dated, with the definitional mismatch against PW's ACPU stated in the same paragraph. The gap (10–15×) is large enough that plausible errors in the inputs do not reverse the direction, though they would change the magnitude.

### A3 — PW's disclosed ARPU/ACPU are a fair benchmark for category price levels
- **What I assume:** ₹4,104 online and ₹36,625 offline reasonably represent, respectively, the volume-online and value-offline price points in Indian test prep.
- **Basis:** PW is the largest disclosed-financials operator in the category; these are audited-results figures. 🟢
- **Load:** §13.2's price anchors, §13.5's comparison, §14, §39.
- **Falsified by:** evidence that PW's mix is unrepresentative — e.g. that its online figure is depressed by a large tail of very-low-price purchases that ALLEN would never serve. **This is likely true to some degree**, which is why §13.5 states the comparison is directional.
- **Definitional caveat, stated in the README:** ACPU (average collection per user) ≠ ARPU. They are not interchangeable and I have not treated them as identical, only as comparable in order of magnitude.

### A4 — Kota's decline reflects substitution toward local classrooms, not toward online
- **What I assume:** families are still buying supervision; what they stopped buying is relocation.
- **Basis:** ALLEN's own FY25 behaviour — 106 new campuses, non-Kota share 64% → 75% — read against Kota enrolment reporting. This is inference from two verified facts, not a disclosed statement.
- **Load:** line L4 of §46, and much of §11.3 and §35.
- **Falsified by:** data showing online enrolment across the category grew at least as fast as local-classroom enrolment over the same period.

### A5 — The digital arm has not published persistence metrics because they are not produced in research-grade form
- **What I assume:** the absence of published persistence data reflects a measurement gap, not merely a disclosure choice.
- **Basis:** inference only. A private company has no obligation to publish anything.
- **Load:** moderate — it shapes the framing of §30 and §32, but the proposal in §50 stands even if ALLEN measures all of this internally and simply doesn't publish it.
- **Falsified by:** ALLEN stating that it tracks these internally. In that case the correct reading of the case study is "here is an outside-in reconstruction of what you already know", which remains a legitimate exercise.

### A6 — The CEO succession signals a shift from reach to delivery
- **What I assume:** appointing an operations/supply-chain leader after a consumer-social/commerce leader reflects a change in the perceived nature of the problem.
- **Basis:** the two leaders' backgrounds only. Explicitly labelled as interpretation in README §7. 🟠
- **Load:** low. Removing it changes nothing structural.
- **Falsified by:** any statement of the actual reasons for either appointment or departure.

---

## 3. Constructed quantities

| ID | Quantity | Value | How constructed | Load |
|---|---|---|---|---|
| C1 | NEET/JEE overlap | 15% | Author estimate; no published overlap statistic exists | Low — §13.2 only |
| C2 | Share of aspirants buying paid prep | 55% | Author estimate | Low |
| C3 | Tier mix (premium 8% / local classroom 27% / online 65%) | — | Author estimate | Low |
| C4 | Premium classroom price anchor | ₹1,50,000 | Author estimate; no company discloses this | Low |
| C5 | **Method A TAM** | **~₹4,800 Cr** | C1–C4 combined | **Deliberately low — presented as one of two disagreeing methods** |
| C6 | Top-two share of organised spend | 45% | Author estimate | Low |
| C7 | **Method B TAM** | **~₹15,500 Cr** | ALLEN FY25 + PW FY26 ÷ C6 | Same |
| C8 | **Derived ALLEN planned online ARPU** | **₹40,000–62,500** | ₹200–250 Cr ÷ 40–50k students, both from reported plan | **High — see A2** |
| C9 | RICE Reach | 45,000 | Midpoint of reported 40–50k plan | Medium — §47 |
| C10 | All RICE Impact/Confidence/Effort scores | See §47.1 | Author judgment | Medium — mitigated by §47.2 stress test |
| C11 | Stress scenario (Reach 25,000; −20pt Confidence on inferential items) | — | Author-chosen severity | Medium |
| C12 | PWR threshold | ≥70% of planned blocks | Author-chosen; explicitly flagged for Phase 1 calibration | Medium |
| C13 | SFS signature (5 signals) | See §31.2 | Author-constructed; **none validated** | High for the proposal, zero for the analysis |
| C14 | SFS validation bar | recall ≥0.6 / precision ≥0.4 | Author-chosen | Medium |
| C15 | Phase durations and sample sizes (20 diaries, 12 dyads, etc.) | See §53 | Author-designed, sized for thematic saturation not statistical power | Low |
| C16 | Mentor-triage target (≥60% of contact hours triage-directed) | 60% | Author-chosen | Low |
| C17 | MDE for the Recovery Path experiment | 5pp absolute | Author-chosen; **n deliberately not computed**, because ALLEN's base rate is not public | Low |

**On C5 and C7:** these are presented in the README precisely *because* they disagree by more than 3×. Neither is offered as the TAM. The disagreement is the point — see README §13.4.

---

## 4. Constructed qualitative content

| Item | Status |
|---|---|
| Personas Ritika, Arjun, Sunita | **Composites, not research participants.** Each separates evidenced context from constructed failure mode in the README itself |
| The six-month journey drop-off shape (§22) | Hypothesis. Labelled as such in the section |
| Technical architecture (§41) and data flow (§42) | Reconstruction from observable behaviour; every node graded |
| ALLEN Pace, Pace Contract, Recovery Path, Strain Watch | Entirely mine. ALLEN has announced nothing of the kind |
| Week / Lapse / Strain Window objects (§32.2) | Mine |
| Tiering proposal — content / assessment / paced (§39) | Mine |
| Wireframes (§52) | Mine, illustrative only |
| All PM interview questions (§60) | Mine |

---

## 5. Known weaknesses of this analysis

1. **Outside-in only.** No ALLEN employee, student or internal document was consulted. The strongest claims are about product *structure* (verifiable from documentation) rather than product *performance* (not verifiable at all).
2. **Cross-period comparison.** ALLEN FY25 is set against PW FY26. This flatters the contrast. Flagged wherever used; a careful reader should discount it.
3. **Single-source dependencies.** A2 rests on one April 2024 article. If that reporting was wrong, §13.5 changes materially.
4. **The guardrail is unvalidated.** SFS is the ethical centre of the proposal and is entirely constructed. §51.5 sets a validation bar because I do not know whether the signature clears it.
5. **Kota figures conflict** across sources and years. Graded 🔴 and used for direction only — never in a calculation.
6. **Advocacy risk.** I designed a proposal and then designed experiments for it. §54's Arm D is the deliberate correction: an arm built to show the thesis is wrong. Whether that correction is sufficient is for the reader to judge.

---

## 6. What would change my mind

| Observation | What it would mean |
|---|---|
| ALLEN publishes high online completion and unaided recovery rates | A1 fails; the case study's premise collapses |
| Phase 0 shows lapse does not predict non-renewal once prior attainment is controlled | The proposal is unnecessary; stop at §39 tiering |
| Students and parents in Phase 1 attribute drop-off to price, content or teaching | The thesis is wrong; reprice rather than build |
| Arm D (value concession) matches or beats structural intervention | Same conclusion, with experimental force |
| ALLEN's actual online ARPU is near the category benchmark rather than 10–15× it | A2 fails; §13.5, §39 and line L3 of §46 all need rewriting |
| Counsel finds strain processing cannot be consented cleanly | The guardrail cannot ship, therefore the product must not ship (README §51.5, criterion 3) |

---

*Day 46 of 90 · [← Day 45 — Eternal](../Day-45-Eternal) · Day 47 →*
