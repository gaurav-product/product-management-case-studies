# ASSUMPTIONS — Day 85, Eka Care (Orbi Health Private Limited), India

Companion to `README.md`. Separates what was **disclosed**, **derived**, **constructed**, **unavailable** and **deliberately excluded**.

The series moves to India, and the evidence environment changes in a way that matters. Days 83 and 84 covered US private companies where no statutory identity was publicly verifiable. **India publishes a Corporate Identity Number for every company**, which restores a primary source this arc lost after Day 82.

Statutory record and company claims retrieved 23 September 2026; government figures to July 2026; field studies to April 2025.
Verification: `verify.py`, **148 checks, all passing**.

---

## Part 0 — The five evidence tiers

Every finding rests on exactly one, and the README says which.

| Tier | What it is | Standing | Example here |
|---|---|---|---|
| **1. Statutory registry** | Filed under law, published | **Verified fact** | CIN U74999KA2020PTC141864 |
| **2. Government programme** | Official, self-reported by the programme | Reliable arithmetic, interested party | 93.95 crore ABHA accounts |
| **3. Independent research** | Peer-reviewed field studies | **Highest weight on usage** | 23.96% adoption |
| **4. Company claims** | Asserted, undated, no methodology | Lowest | "3 Cr trusted" |
| **5. Unverifiable** | Asserted as such in the gate | — | Revenue, MAU, retention |

**Tier 2 needs the caveat most.** ABDM's figures are official and there is no reason to doubt their arithmetic, but a programme counting accounts it created is structurally closer to a vendor counting downloads than to an independent trial. Tier 3 therefore carries the analytical weight.

```
statutory_registration_verifiable      = True
company_claims_independently_confirmed = False
unverifiable_claim_count               = 13
```

---

## Part 1 — Disclosed facts

### 1.1 Tier 1 — Statutory registry — VERIFIED

From the GLEIF public API, validated against India's Ministry of Corporate Affairs (registration authority RA000394), retrieved 23 September 2026.

| Field | Value |
|---|---|
| Legal name | ORBI HEALTH PRIVATE LIMITED |
| CIN | U74999KA2020PTC141864 |
| LEI | 335800XQK6WJNULLIB28 |
| Incorporated | 3 December 2020 |
| Registered office | Villa No 28, Windmills of Your Mind, Plot 331/A, Road No 5, EPIP, Bangalore 560066, Karnataka |
| Entity status | ACTIVE |
| LEI registration status | LAPSED (initial 29 March 2025; renewal due 29 March 2026) |

CIN decomposition: `U` unlisted · `74999` NIC code · `KA` Karnataka · `2020` year · `PTC` private limited company · `141864` registration number.

**NIC 74999 is "Other professional, scientific and technical activities n.e.c."** — the residual class for activities not elsewhere classified. It mentions neither health, nor software, nor information technology.

### 1.2 Tier 2 — Government programme figures

**Union Health Ministry, third Mission Steering Group, chaired by Health Minister J.P. Nadda, statement dated 10 July 2026:** 93.95 crore ABHA numbers created (up from 90 crore in May 2026); 105 crore health records linked; 5.33 lakh health facilities in the registry; 9.85 lakh healthcare professionals registered; approximately 24 crore Scan & Share tokens generated for OPD registration; approximately 2.72 lakh facilities running ABDM software.

**National Health Authority, reported 29 January 2026:** 76 crore ABHA IDs; 51 crore health records linked; over 9 crore Scan & Share tokens across 19,000+ hospitals in 640 districts; 16,765 hospitals and 17,229 facilities registered. Leading states by adoption relative to population: Odisha, Andhra Pradesh, Himachal Pradesh, Rajasthan.

### 1.3 Tier 3 — Independent peer-reviewed research

**Ranjan A, Singh G, Singh H, Singh M.** *BMC Health Services Research* 2026;26(1). PMID 41787376. DOI 10.1186/s12913-026-14314-7.

Analytical cross-sectional study, three tertiary care hospitals in Agra, multistage random sampling, September 2024 to April 2025. 425 OPD attendees surveyed; hospital registration records analysed over eight months.

- **537,278 total OPD visits; 129,007 completed ABHA registrations; monthly adoption rate 23.96%**, described by the authors as "below average"
- Digital Health Literacy Instrument (21-item, validated): mean **2.94 ± 0.72**; males significantly higher than females (U = 15,922, p < .001); education strongest positive correlation (ρ = 0.480, p < .001); age weak negative (ρ = −0.230, p < .001)
- Sub-skills: operational **2.38 ± 0.64**; evaluating reliability **2.18 ± 0.66**; protecting privacy **2.22 ± 0.65**
- Over **80%** agreed ABDM made registration easier and was user-friendly
- Only **55%** felt comfortable with data privacy protection
- Barriers: prefers in-person care **85.6%**; data plan costs **81.9%**; difficulty using apps **65.6%**; language **64.0%**; OTP hesitation **60.0%**
- **88%** expressed need for training and support; **58.6%** lacked adequate knowledge about ABDM despite attending participating facilities

**One co-author is affiliated with Ayushman Bharat Digital Mission, Lucknow.** Recorded in the gate as `bmc_has_programme_affiliated_coauthor = True` and noted wherever the study's figures appear.

**Datta A, Kaushik JS, Malakar H.** *Cureus* 2025;17(4):e82605. PMID 40400882. DOI 10.7759/cureus.82605.

Cross-sectional, 250 women aged 18–80 at the obstetrics and gynaecology OPD of a tertiary centre, September 2024 to March 2025. Awareness: Digital India platforms **60%**; ABHA **35%**; Swasthya app **20%**. Satisfaction index for ABHA registration **87.9**; for Scan & Share **78.7**. Logistic regression showed no significant influence of age, education, socioeconomic status or ABHA awareness on digital health app usage.

### 1.4 Tier 4 — Company claims — NOT VERIFIED

From eka.care product pages: "Trusted by more than 3Cr Indians"; "1 Cr+ Downloads"; "1.2 Cr+ ABHAs Created"; "30 Cr+ Vitals Stored"; "1 Cr+ Prescriptions"; "1 Cr+ Assessments"; "40 K+ Doctors".

Badges: "NHA Approved"; "Co-WIN Approved"; "ABDM Compliant"; "Official partner of Government of India"; "FHIR, HL7, SNOMED, & LOINC enabled".

**None carries a stated methodology or measurement date.**

### 1.5 Regulatory

Digital Personal Data Protection Rules, 2025, notified by MeitY on **14 November 2025**. Data Protection Board of India as enforcement authority. Requires informed, unambiguous and freely given consent; privacy notices must specify purposes, data categories, retention periods and withdrawal mechanisms. Phased implementation.

---

## Part 2 — Derived figures

Computed by `verify.py`.

### 2.1 Registry

| Figure | Value |
|---|---|
| Register misclassification tally | **12 of 85** (**14.12%**) |
| Brand name matches legal name | **No** |

### 2.2 The national programme

| Figure | Value |
|---|---|
| ABHA growth, Jan→Jul 2026 | **+23.62%** |
| Records growth, Jan→Jul 2026 | **+105.88%** |
| Linkage outpaced account growth by | **82.26pp** |
| ABHA growth, May→Jul 2026 | **+4.39%** |
| Records per account, Jan 2026 | **0.67** |
| **Records per account, Jul 2026** | **1.12** |
| Scan & Share growth, Jan→Jul 2026 | **+166.67%** |
| Facilities running software ÷ registered | **51.03%** |
| Registered facilities without software | **2.61 lakh** |
| Professionals per facility with software | **3.62** |

### 2.3 The central finding

| Figure | Value |
|---|---|
| **National usage proxy** (Scan & Share ÷ ABHA) | **25.55%** |
| **Field-study adoption** (BMC) | **23.96%** |
| **Convergence gap** | **1.59pp** |
| Pooled ratio from BMC counts | **24.01%** |
| Pooled versus reported monthly gap | **0.05pp** |
| OPD visits without ABHA registration | **408,271** (**75.99%**) |

### 2.4 Awareness, literacy and privacy

| Figure | Value |
|---|---|
| Aware of ABDM (BMC) | **41.40%** |
| Not comfortable with data privacy | **45.00%** |
| Satisfaction minus privacy comfort | **25.00pp** |
| Reliability skill minus operational | **−0.20** |
| Privacy skill minus operational | **−0.16** |
| Barrier mean | **71.42%** |
| Barrier range | **25.60pp** |
| Barriers outside product control | **2 of 5** |
| Awareness drop, digital → ABHA (Cureus) | **25.00pp** |
| Awareness drop, ABHA → app (Cureus) | **15.00pp** |
| Satisfaction index gap, registration → Scan & Share | **9.20** |

### 2.5 Company claims tested

| Figure | Value |
|---|---|
| **"Trusted by" ÷ downloads** | **3.00×** |
| Difference | **2.00 crore** |
| ABHAs per download | **1.20** |
| Vitals per claimed user | **10.00** |
| Vitals per download | **30.00** |
| **Eka Care share of national ABHA** | **1.28%** |
| National ABHAs per Eka Care ABHA | **78.29** |
| Claimed doctors as share of national HPR | **4.06%** |

### 2.6 Series comparison

| Figure | Value |
|---|---|
| Day 83 registered share minus Day 85 usage proxy | **44.68pp** |

---

## Part 3 — Author constructs

**None of the following is disclosed data.**

### 3.1 Frameworks

RICE, MoSCoW, Kano, JTBD, AARRR, HEART, Porter's Five Forces, SWOT and the PRD in section 31 are applied by the author.

### 3.2 RICE inputs

| ID | R | I | C | E | Stress |
|---|---|---|---|---|---|
| P1 | 120 | 3.0 | 0.90 | 3.0 | 0.95 |
| P2 | 120 | 3.0 | 0.75 | 5.0 | 0.85 |
| P3 | 120 | 2.5 | 0.85 | 4.0 | 0.90 |
| P4 | 120 | 2.5 | 0.70 | 8.0 | 0.65 |
| P5 | 120 | 2.0 | 0.55 | 12.0 | 0.45 |

Reach held at 120 (lakh — the **claimed** 1.2 crore ABHAs, itself an unverified figure, which is a limitation of the model). **P5 ranks last under stress by 70.98%**, asserted programmatically. Base and stressed rankings are identical.

Section 29.1 argues that P5's low ranking reflects *institutional appropriateness* — a vendor holding 1.28% of a national programme's accounts cannot credibly fund a study of that programme's record accuracy. That argument is the author's interpretation of the framework output, not a disclosed constraint.

### 3.3 Personas

Sunita R., Dr. Prakash M. and Meera J. are **composite constructions** — not real people, not customer research. Sunita's parameters are drawn from the BMC study's reported findings (unaware of ABDM, OTP hesitation, data cost, language) to keep the persona tethered to evidence rather than invention.

### 3.4 North Star and guardrails

"Linked-record-backed monthly active users" is the author's proposal. The three guardrails and their thresholds are the author's. The national **1.12** records-per-account benchmark is a government figure; the proposal to hold the company to it is not.

### 3.5 Scenarios and the funnel model

Section 38's three scenarios are author constructs. **Section 23.1's claim that the funnel stages multiply is a model, not a measurement** — the true joint probability would require conditional data nobody publishes, and the multiplication is offered as an explanation of the observed gap rather than as a computed result.

### 3.6 Interpretive framings

The reading in section 9.1 that "prefers in-person healthcare" may be partly a **measurement artefact** of question framing is the author's inference, not the study's conclusion. The reading in section 12.2 that a >1 ABHA-per-download ratio indicates **assisted creation** is also inference — consistent with the awareness data, but not stated by the company.

### 3.7 Eval plan, failure modes, human-in-the-loop, playbook

Sections 25, 26, 27 and 58 are the author's product judgement. No clinical expertise is claimed. The failure-mode ranking is by the author's estimate of expected harm.

### 3.8 Recommendations, roadmap, and the ladder

All five recommendations, the MoSCoW allocation, the three-horizon roadmap, the six-rung ladder (section 35), the public-infrastructure assessment (section 37), the six-day synthesis (section 53) and the open category questions (section 51) are the author's framing.

---

## Part 4 — Unavailable information

| Not available | Consequence |
|---|---|
| Revenue, profit or loss, unit economics | No commercial assessment possible |
| Paid-up capital, directors, charges, annual filings | Not retrieved from MCA21; the obvious next source |
| Monthly active users, retention, churn | The usage question is unanswerable at company level |
| Records per account at company level | Cannot be compared against the national **1.12** |
| Funding or valuation since the 2022 Series A | Not examined; excluded by series rule |
| **Record accuracy or completeness** | **Measured by nobody, anywhere** |
| **Consent comprehension** | **Unmeasured under a regime requiring informed consent** |
| Adoption by language, literacy or gender at product level | The equity question is unanswerable |
| Data retention and secondary-use practice | Privacy position unassessable |
| Identity-resolution error rate | Failure mode 3 is unquantifiable |
| Litigation involving Orbi Health | Indian court records not systematically searchable; recorded as a gap, not a finding |

---

## Part 5 — Deliberate exclusions

| Excluded | Reason |
|---|---|
| Tracxn, PitchBook, CB Insights, Inc42, LeadIQ | Aggregators, not primary. Used only to locate the legal entity name |
| MCA21 filings | Not retrieved; identity comes from GLEIF, which validates against MCA |
| ABDM public dashboard | Returned HTTP 403 to automated retrieval |
| Health Systems & Reform ABDM assessment | Returned HTTP 403 |
| Indian court records | Not systematically searchable; see section 44 |
| Market data and valuation | Series rule |
| The product itself | Not tested by the author; no first-hand evaluation claimed |

### 5.1 Two false matches, discarded

**LEI 2549001QJF90TQE84W04** resolves to ORBINOX INDIA PRIVATE LIMITED, a valve manufacturer in Coimbatore. Retrieved during the search, identified as unrelated, discarded before any figure was derived. Documented in Appendix A4 because the same search will surface it again.

**"Eka Software Solutions"** is a commodity-trading software company, unrelated to Orbi Health. Its financial pages appear in searches for this company. No figure used.

### 5.2 On the Days 80–84 comparators

Day 80's **59.43%**, Day 81's **97%**, Day 82's **94.95%**, Day 83's **23.00%** and **70.23%**, and Day 84's **4.62** are **recomputed inside this case study's own `verify.py`** rather than carried across as prose. No case study asserts a number its own gate has not verified.

---

## Part 6 — Fairness statement

**The programme deserves credit and gets it.** ABDM built population-scale health identity in roughly four years and publishes its figures in regular public detail — including the Scan & Share and facility-software numbers that undercut its own headline. Compared with the disclosure available for Days 83 and 84, this is a materially better information environment, and it is the reason a usage gap could be measured at all.

**The critique is not that the government inflated a number.** 93.95 crore accounts is accurate. The inference that it represents usage is wrong, and the inference is what travels.

**The company is assessed on what it publishes, not on what it is.** No outcome metric appears on its public pages. That is the finding. Nothing here asserts any claim is false, and section 40 runs the counterfactual in which every claim is true — most of the analysis survives.

**The temporal limitation is the most serious one**, stated in Appendix A7 and section 59: the primary field study ran to April 2025 and the national figures are from 2026. **The 23.96% is a floor, not a current rate.**

**The register finding concerns classification, not conduct.** NIC 74999 was almost certainly chosen by a company secretary at incorporation and says nothing about how the company operates.

---

## Verification statement

`verify.py` contains **148 checks** and exits non-zero on any failure. It asserts the statutory identity and full CIN decomposition; the national programme figures at two time points and every growth rate and depth ratio derived from them; the Scan & Share usage proxy and its convergence with the independent field-study estimate; both field studies' adoption, literacy, barrier, awareness and privacy figures; the company's claims and the internal tension between them; the regulatory dates; the Days 80–84 comparators; the RICE base and stressed rankings with the proposal ranking last under stress named by the gate; and the thirteen unverifiable categories.

`crosscheck.py` independently extracts every two-decimal figure from `README.md` and `ASSUMPTIONS.md` and confirms each traces to a gate value.

**Fabricated figures: 0.**
**Company outcome metrics published: 0.**
**Independent measurements of usage: 2 — and they agree within 1.59pp.**

---

*Day 85 of 90. Eka Care — Orbi Health Private Limited, CIN U74999KA2020PTC141864. Statutory record to 23 September 2026; government figures to July 2026; field studies to April 2025.*
