# Day 85 — Eka Care (Orbi Health Private Limited), India

### 93.95 crore accounts. About a quarter of them get used.

> **90-Day PM Case Study Challenge — Day 85**
> Evidence-based product teardown built only from primary sources.
> Every derived figure is produced by `verify.py` (148 programmatic checks) before a word of prose was written.
> **The series moves to India, and the method changes again — section 2 explains how.**

---

## 1. One-paragraph summary

India has built the largest digital health account system in the world. The Union Health Ministry reported **93.95 crore** ABHA numbers created as of July 2026, with **105 crore** health records linked. Eka Care is a private Bangalore company whose product sits on top of that infrastructure and claims to have created **1.2 crore** of those accounts — **1.28%** of the national total. The interesting number is not the headline. It is what happens when you look for usage rather than registration. The programme's own point-of-care instrument, Scan & Share, generated roughly **24 crore** tokens — **25.55%** of accounts created. An independent peer-reviewed field study across three tertiary hospitals, covering **537,278** OPD visits, found ABHA registration used in **23.96%** of them. Two entirely independent measurements, one administrative and one clinical, land **1.59pp** apart at about a quarter. And in that same study, **58.6%** of patients attending an ABDM-participating facility did not know what ABDM was. **Registration is not adoption, and this time the gap is measurable at national scale.**

---

## 2. Why the method changes again

Days 83 and 84 covered private American companies, where no statutory registration exists in public and the register-classification thread of this series went dark for three days.

**India restores it.** Every Indian company carries a Corporate Identity Number that encodes its industry classification, state, year of incorporation and corporate form, and the entity's legal name and status are published. That is a genuine statutory primary source — the first this arc has had since Day 82's SEC filings.

So this gate runs five tiers:

| Tier | Source | Standing |
|---|---|---|
| **1. Statutory registry** | CIN, legal name, incorporation, status | Verified fact |
| **2. Government programme** | Health Ministry and NHA figures | Official, self-reported by the programme |
| **3. Independent research** | Two peer-reviewed field studies | Highest evidentiary weight on usage |
| **4. Company claims** | eka.care product pages | Unchecked |
| **5. Unverifiable** | Revenue, MAU, retention, accuracy | Asserted so nothing is promoted silently |

```
statutory_registration_verifiable      = True
company_claims_independently_confirmed = False
unverifiable_claim_count               = 13
```

One tier distinction matters more here than in any previous day. **Tier 2 is the programme reporting on itself.** ABDM's figures are official and there is no reason to doubt their arithmetic — but a ministry counting accounts it created is structurally closer to a vendor counting downloads than to an independent trial. That is why Tier 3 carries the weight in this analysis.

---

## 3. Company identification

This is the first identification table in five days built from a statutory register rather than from a company's own website.

| Field | Value | Source |
|---|---|---|
| **Legal name** | **ORBI HEALTH PRIVATE LIMITED** | GLEIF / MCA |
| Brand name | Eka Care | Company |
| **CIN** | **U74999KA2020PTC141864** | MCA via GLEIF |
| LEI | 335800XQK6WJNULLIB28 | GLEIF |
| Registration authority | RA000394 (India, Ministry of Corporate Affairs) | GLEIF |
| Incorporated | **3 December 2020** | GLEIF |
| Registered office | Villa No 28, Windmills of Your Mind, Plot 331/A, Road No 5, EPIP, Bangalore 560066 | GLEIF |
| Entity status | **ACTIVE** | GLEIF |
| LEI registration status | **LAPSED** | GLEIF |

```
brand_matches_legal_name = False
```

The brand and the legal entity have different names, which is ordinary and worth stating once: **contracts, liabilities and statutory obligations attach to Orbi Health Private Limited, not to "Eka Care."** Anyone doing diligence on this company searching the brand name in a corporate register will find nothing.

### 3.1 The register finding, and it is a good one

The CIN decomposes into six fields, and one of them is the whole point.

| Segment | Value | Meaning |
|---|---|---|
| `U` | Unlisted | Not listed on a stock exchange |
| **`74999`** | **NIC code** | **"Other professional, scientific and technical activities n.e.c."** |
| `KA` | Karnataka | State of registration |
| `2020` | Year | Year of incorporation |
| `PTC` | Private Limited Company | Corporate form |
| `141864` | Registration number | Sequence |

```
nic_is_residual_catch_all           = True
nic_mentions_health                 = False
nic_mentions_software               = False
nic_mentions_information_technology = False
```

**NIC 74999 is the residual class.** The "n.e.c." stands for *not elsewhere classified* — it is the code you get when nothing else fits. A company holding personal health records for a claimed 1.2 crore Indians, integrated into national health infrastructure, is registered under a code that mentions neither health, nor software, nor information technology.

This is the twelfth company in this series filed under a code that materially misdescribes its business, out of **85** examined — **14.12%**.

But this one is a sharper case than the previous eleven. Those were wrong codes. **This is the absence of a code** — the company was not misfiled into an ill-fitting category, it was filed into the category that exists precisely for businesses the classification system does not contemplate.

That matters practically, not just pedantically. Industry classification drives statistical aggregation, sector policy, regulatory scoping and investment screening. A digital health sector whose companies sit under "other professional activities n.e.c." is a sector that does not appear in its own country's industrial statistics.

### 3.2 On the lapsed LEI

The Legal Entity Identifier was first registered on 29 March 2025 and came up for renewal on 29 March 2026. The record now reads LAPSED.

```
lei_lapsed_is_entity_distress_signal = False
entity_still_active_in_registry      = True
```

**This should not be over-read.** An LEI is required mainly for entities transacting in regulated financial markets; letting one lapse is an administrative choice, not a solvency signal, and the MCA entity status remains ACTIVE. It is recorded here because it is a verifiable fact about a company whose other facts are mostly unverifiable, and because a lapsed global identifier makes the company marginally harder to trace across jurisdictions.

---

## 4. What Eka Care actually does

Eka Care is a consumer health-records application. A person creates or links an ABHA number, their medical records are collected into one place, vitals are tracked, and prescriptions and reports are stored and made shareable with clinicians. There is a provider-facing side for doctors and clinics.

The company's product page carries five badges: **NHA Approved**, **Co-WIN Approved**, **ABDM Compliant**, **Official partner of Government of India**, and **FHIR, HL7, SNOMED, & LOINC enabled**.

```
claimed_badge_count             = 5
badges_that_are_outcome_metrics = 0
```

Every one of the five is a **conformance** claim — it says the product meets a standard or holds an approval. Not one is a **performance** claim. This is the fifth consecutive day on which a healthcare product's public evidence consists of certifications rather than outcomes, and the Indian variant is the purest form of it: in an ecosystem built on government standards, compliance badges substitute for results entirely.

### 4.1 The structural position

Eka Care does not own the identity layer, the consent layer, or the record-exchange protocol. ABDM does. What Eka Care owns is the interface — the app a person actually opens — and the integration work that makes a clinic's records flow into it.

That is a genuinely defensible position when the public infrastructure is good, because the state builds the rails and the company competes on experience. It is also a position with a ceiling and a dependency: **a company whose product is the front end of a government programme grows when the programme grows and stalls when it stalls.**

Which makes the adoption question in section 6 not merely interesting but existential for this business.

---

## 5. Problem statement

The problem ABDM addresses is real and enormous. Indian medical records are fragmented across private clinics, government hospitals, diagnostic labs and paper files held by the patient. A person arriving at a new doctor typically carries a plastic bag of prescriptions or nothing at all. Continuity of care, in the ordinary clinical sense, largely does not exist for most of the population.

A national health identifier with linked records addresses that directly, and the ambition is appropriate to the problem.

The question this case study examines is narrower and is the one the evidence can actually answer: **when you build the account layer at national scale, does use follow?**

---

## 6. The central finding

### 6.1 The headline

From the Union Health Ministry, at the third Mission Steering Group meeting chaired by Health Minister J.P. Nadda, 10 July 2026:

| Measure | Value |
|---|---|
| ABHA numbers created | **93.95 crore** (939.50 million) |
| Health records linked | **105 crore** (1,050.00 million) |
| Health facilities in the registry | **5.33 lakh** |
| Healthcare professionals registered | **9.85 lakh** |
| Scan & Share tokens generated | **~24 crore** |
| Facilities running ABDM software | **~2.72 lakh** |

By any measure of scale this is extraordinary. Account creation grew **23.62%** between January and July 2026, and record linkage grew **105.88%** over the same period — linkage outpacing account growth by **82.26pp**, which is the healthy direction.

| Depth measure | Jan 2026 | Jul 2026 |
|---|---|---|
| Health records per ABHA account | **0.67** | **1.12** |

Records per account crossed one. The system is moving from empty accounts toward accounts with something in them, which is exactly what should happen and is a real achievement.

### 6.2 Then look for usage

Scan & Share is the programme's own point-of-care instrument: a patient at an outpatient counter uses their ABHA to register, and a token is generated. It is the closest thing ABDM publishes to a usage metric rather than a registration metric.

| Measure | Value |
|---|---|
| Scan & Share tokens | **24 crore** |
| ABHA accounts | **93.95 crore** |
| **Tokens as a share of accounts** | **25.55%** |

Scan & Share grew **166.67%** between January and July 2026 — faster than accounts, faster than records. The direction is good. The level is about a quarter.

### 6.3 And now the independent measurement

According to PubMed, Ranjan et al., *BMC Health Services Research*, March 2026: an analytical cross-sectional study across **three tertiary care hospitals in Agra**, covering eight months from September 2024 to April 2025, with **425** OPD attendees surveyed and hospital registration records analysed.

| Measure | Value |
|---|---|
| Total OPD visits | **537,278** |
| Completed ABHA registrations | **129,007** |
| **Adoption rate reported by the authors** | **23.96%** |
| Pooled ratio, computed from the counts | **24.01%** |
| **Visits without ABHA registration** | **408,271** (**75.99%**) |

The authors describe this as a *"below average monthly adoption rate."*

### 6.4 The convergence

| Source | Method | Usage estimate |
|---|---|---|
| Health Ministry, July 2026 | National administrative proxy (Scan & Share ÷ ABHA) | **25.55%** |
| Ranjan et al., BMC HSR | Hospital records, 537,278 OPD visits | **23.96%** |
| **Gap** | | **1.59pp** |

```
both_estimates_near_one_quarter = True
```

Two measurements with nothing in common — one a national tally compiled by the programme, the other a field study at three hospitals in one city — **land within 1.59 percentage points of each other, at roughly one in four.**

That convergence is what makes this finding solid. Either number alone would be arguable: the national ratio mixes denominators across time, and the Agra study is three hospitals in one district. Together, they are hard to dismiss.

**India has created health accounts for most of its population. About a quarter of that infrastructure is being used at the point of care.**

---

## 7. The awareness gap underneath it

The same study found something more uncomfortable than the adoption rate.

| Finding | Value |
|---|---|
| Patients who **lacked adequate knowledge about ABDM** | **58.6%** |
| Patients who were aware | **41.40%** |
| Patients expressing a need for training and support | **88.00%** |

These were people **attending ABDM-participating facilities**. Nearly three in five did not know what the programme was while standing inside it.

The second field study agrees. According to PubMed, Datta et al., *Cureus*, April 2025, surveying **250** women at the obstetrics and gynaecology OPD of a tertiary centre:

| Awareness of | Share |
|---|---|
| Digital India platforms generally | 60% |
| **ABHA specifically** | **35%** |
| The Swasthya app | 20% |

| Derived | Value |
|---|---|
| Drop from general digital awareness to ABHA awareness | **25.00pp** |
| Drop from ABHA awareness to app awareness | **15.00pp** |

Awareness halves at each step down the funnel from "digital government services exist" to "this specific health account exists" to "this specific app exists."

### 7.1 Why this is the product finding, not a policy finding

An account created for someone who does not know they have it is not a user. It is a row.

This is the same failure Day 83 identified at OpenEvidence, where a 40% figure meant registered users in July and daily active users by January — and it is the same failure at a scale five hundred times larger. **The gap between a registration number and a usage number is the most consistent measurement error in this entire six-day arc**, and here it is visible in a government programme, a private company's marketing, and two independent studies simultaneously.

---

## 8. Satisfaction is measured on the survivors

Both field studies report high satisfaction. That finding needs a specific caveat.

| Measure | Value |
|---|---|
| Agreed ABDM made registration easier and was user-friendly | **over 80%** |
| Satisfaction index for ABHA registration (Cureus) | **87.9** |
| Satisfaction index for Scan & Share (Cureus) | **78.7** |
| Gap between the two | **9.20** |

```
satisfaction_measured_on_survivors_only = True
```

**These figures describe the people who got as far as using it.** In a system where 23.96% of visits involve ABHA registration and 58.6% of patients do not know the programme exists, a satisfaction score measures the experience of a self-selected quarter.

That is not a criticism of the studies, which are clear about their sampling. It is a warning about how the number travels: "over 80% satisfaction" is a true statement about ABDM that tells you almost nothing about whether ABDM is working, because the denominator is the people it already worked for.

The internal gap is informative too. Registration scores **87.9**; Scan & Share — the part that actually moves a record — scores **78.7**. **The further into the workflow you go, the lower the satisfaction.**

---

## 9. The barriers, ranked

From the BMC study:

| Barrier | Share citing it |
|---|---|
| Preference for in-person healthcare | **85.6%** |
| High data plan costs | **81.9%** |
| Difficulty using health apps | **65.6%** |
| Language difficulties | **64.0%** |
| Hesitation to share a one-time password | **60.0%** |

| Derived | Value |
|---|---|
| Mean across the five | **71.42%** |
| Range, highest to lowest | **25.60pp** |
| **Barriers outside product control** | **2 of 5** |

```
top_barrier = 'prefers in-person care'
```

### 9.1 What a product manager can and cannot fix

**Data plan cost (81.9%) and preference for in-person care (85.6%) are not product problems.** One is an infrastructure and income question; the other is a legitimate preference that a digital health record does not actually conflict with — a person can prefer seeing a doctor in person and still benefit from their records being available.

That second one is worth pausing on, because it may be a **measurement artefact rather than a barrier**. "I prefer in-person healthcare" is a sensible answer to a question about digital health that respondents may have read as "would you replace your doctor with an app." If so, the top-ranked barrier in the study is partly a framing effect.

**The three that are product problems** — difficulty using apps (65.6%), language (64.0%) and OTP hesitation (60.0%) — cluster tightly within **5.60pp** of each other, and all three are addressable. OTP hesitation in particular is a trust-and-explanation problem, not a technical one.

---

## 10. Digital health literacy, and where it is weakest

The study used the validated 21-item Digital Health Literacy Instrument.

| Measure | Score |
|---|---|
| Overall DHLI mean | **2.94** (SD 0.72) |
| Operational skills | **2.38** |
| Evaluating reliability | **2.18** |
| Protecting privacy | **2.22** |

| Derived | Value |
|---|---|
| Reliability minus operational | **−0.20** |
| Privacy minus operational | **−0.16** |

```
bmc_weakest_skill_is_judgement_not_operation = True
```

**People can operate the apps better than they can judge them.** Operational skill scores highest; the two lowest scores are evaluating whether information is reliable and protecting one's own privacy.

Gradients were significant: men scored higher than women (U = 15,922, p < .001), education showed the strongest positive correlation with literacy (ρ = 0.480, p < .001), and age a weak negative one (ρ = −0.230, p < .001).

### 10.1 The design consequence

A population that can operate but cannot evaluate is a population for whom **interface quality is not the binding constraint — explanation quality is.** Making the app easier to use does not help someone who does not know whether to trust what it does with their records.

That reframes the roadmap. The instinct in a low-literacy market is to simplify the interface. The data says to invest in comprehension: what this is, who sees it, what happens if you say no.

---

## 11. Privacy, in the year the law arrived

| Measure | Value |
|---|---|
| Felt comfortable with data privacy protection | **55%** |
| **Did not** | **45.00%** |
| Gap between "made registration easier" and "comfortable with privacy" | **25.00pp** |

India notified the **Digital Personal Data Protection Rules, 2025** on **14 November 2025**, establishing the Data Protection Board of India as enforcement authority and requiring informed, unambiguous and freely given consent, with privacy notices specifying purposes, data categories, retention periods and withdrawal mechanisms. Implementation is phased.

```
dpdp_requires_informed_unambiguous_consent = True
privacy_skill_score                        = 2.22
```

So the position is this: a consent regime requiring *informed* consent now governs a population whose measured ability to protect its own privacy scores **2.22**, in which **45.00%** are not comfortable with how their health data is protected, and **60.0%** hesitate to share an OTP — which is the exact mechanism by which consent is captured.

**OTP hesitation is not friction. It is the system's only visible expression of informed doubt**, and it is being measured as a barrier to overcome rather than as a signal to answer.

---

## 12. Eka Care's own claims

From the company's product page:

| Claim | Stated |
|---|---|
| "Trusted by more than 3Cr Indians" | 3 crore |
| "1 Cr+ Downloads" | 1 crore |
| "1.2 Cr+ ABHAs Created" | 1.2 crore |
| "30 Cr+ Vitals Stored" | 30 crore |
| "1 Cr+ Prescriptions" | 1 crore |
| "1 Cr+ Assessments" | 1 crore |
| "40 K+ Doctors" | 40,000 |

None carries a stated methodology or measurement date.

### 12.1 The internal tension

```
trusted_exceeds_downloads = True
trusted_over_downloads_ratio = 3.00
```

**Three crore Indians are said to trust a product that has one crore downloads.**

| Measure | Value |
|---|---|
| Ratio of "trusted by" to downloads | **3.00×** |
| Difference | **2.00 crore** |

For a mobile-first consumer product, downloads normally bound users from above — you cannot have more app users than app installs. Three times more is not a rounding difference.

```
claim_pair_is_internally_reconcilable_without_definitions = False
```

There are entirely legitimate explanations. "Trusted by" may count people whose records passed through the platform via a partner clinic without ever installing the app. It may count web users. It may count ABHAs created at a counter on someone's behalf. Any of those would reconcile the numbers.

**But none of them is stated**, and the two figures sit side by side on the same page under the same visual treatment, inviting the reader to understand both as measures of the same user base. This is Day 83's finding in a different alphabet: **the number is not wrong, the definition is missing.**

### 12.2 A claim that is coherent, and tells you something

| Measure | Value |
|---|---|
| ABHAs created | 1.2 crore |
| Downloads | 1 crore |
| **ABHAs per download** | **1.20** |

More ABHA numbers created than app downloads is *also* a ratio above one — and here it is readily explicable and quite informative. ABHA creation is frequently **assisted**, done at a clinic or camp counter by staff on a patient's behalf. A ratio above one is what you would expect from a company doing a lot of assisted onboarding.

That reading is consistent with the awareness data in section 7: if 58.6% of patients do not know what ABDM is, most account creation is necessarily being done *for* them rather than *by* them.

**Assisted creation is the mechanism by which a national account number reaches 93.95 crore while usage sits near a quarter.**

### 12.3 Share of the national programme

| Measure | Value |
|---|---|
| Eka Care ABHAs as a share of national total | **1.28%** |
| National ABHAs per Eka Care ABHA | **78.29** |
| Claimed doctors as a share of the national HPR | **4.06%** |

A private company that has created **1.28%** of a national identity system's accounts is a meaningful participant and not a dominant one. Its doctor footprint (**4.06%** of registered professionals) is proportionally larger than its patient footprint — which is the right shape for a company whose distribution runs through clinics.

---

## 13. What the company does not publish

```
company_publishes_any_outcome_metric = False
guardrail_records_per_account_company_published = False
```

Nationally, records per ABHA is **1.12**. Eka Care does not publish its own equivalent — and it is the single number that would say whether its accounts are fuller or emptier than the national average.

Also unpublished: monthly active users, retention, the share of accounts with any linked record, record accuracy, and any measure of whether a record retrieved through the platform was complete or correct.

**Thirteen categories are asserted as unverifiable in the gate.** For the fifth day running, the company's public evidence consists of scale claims and conformance badges, with no outcome measure of any kind.

---

## 14. User personas

### 14.1 Sunita R. — the patient who has an account and does not know it

Attends a district hospital OPD. Someone at the registration counter asked for her Aadhaar and created an ABHA. She has a health account. She does not know what it is; she is one of the **58.6%**.

**Jobs to be done:** be seen by a doctor today; not lose the prescription before the follow-up; not pay twice for the same test.

**What the system gives her:** a number. Possibly a linked record — nationally the average account holds **1.12**.

**What stands between her and value:** she is not aware the account exists, she is unsure about sharing an OTP (**60.0%**), her data plan is expensive (**81.9%**), and the interface may not be in her language (**64.0%**).

**The design implication:** every feature that assumes the user knows they are a user is built for a different person. For Sunita, the product's first job is not record retrieval — it is explaining that she has records at all.

### 14.2 Dr. Prakash M. — the clinician at a facility that may or may not be connected

Works at one of the **5.33 lakh** facilities in the registry. Whether his facility actually runs ABDM software is a coin flip: **51.03%** do.

**Jobs to be done:** see the patient's history before deciding; not retype what another clinic already recorded; finish the queue.

**What he experiences:** a patient who may present a token, at a facility that may be able to read it, producing a record that may contain something.

**The multiplication problem:** the probability that a given encounter produces a usable record exchange is the product of several independent quarters and halves — patient has an account, patient knows to use it, facility runs the software, a record exists to fetch. Each link is plausible on its own. **Multiplied, they explain why national account coverage and point-of-care usage differ by a factor of four.**

### 14.3 Meera J. — the Eka Care product manager

Runs the consumer app. Her adoption depends on a programme she does not control, in a market where her top three addressable barriers are comprehension, language and trust.

**What she can move:** explanation, language coverage, assisted onboarding, whether a linked record is actually useful when opened.

**What she cannot:** data costs, facility software deployment, the national awareness campaign.

**Her hardest strategic problem:** her company's growth metric — ABHAs created — is the metric the evidence says is least connected to value.

---

## 15. Jobs to be Done

| Job | Who | Served? | Evidence |
|---|---|---|---|
| "Find my old reports" | Patient | Partially | 1.12 records per account nationally |
| "Don't make me carry paper" | Patient | Partially | 23.96% point-of-care adoption |
| "Tell me what this is" | Patient | **No** | 58.6% lack knowledge |
| "Let me read it in my language" | Patient | **Unknown** | 64.0% cite language; no disaggregation published |
| "See history before I decide" | Clinician | Partially | 51.03% of facilities run the software |
| "Reassure me about my data" | Patient | **No** | 45.00% not comfortable |
| "Create the account for me" | Patient | **Yes** | ABHAs per download 1.20 |

The one job the system performs reliably is the one the patient did not ask for.

---

## 16. Business model

Eka Care is a private company in an ecosystem where the identity layer, the consent protocol and the exchange standards are public goods provided by the state.

**What the state provides:** ABHA identity, the Health Facility and Healthcare Professional registries, consent architecture, FHIR-based exchange standards.

**What the company provides:** the consumer interface, clinic-side integration, record organisation and vitals tracking, assisted onboarding.

**How it earns:** not disclosed in any source examined. Revenue, pricing and unit economics are all in the unverifiable list.

### 16.1 The public-infrastructure position, assessed fairly

This is a genuinely different business shape from anything in Days 80–84, and it has real advantages. The company does not have to build or defend an identity system, does not bear the cost of standards development, and inherits distribution from a national programme. Compared with Day 82's Doximity — which had to build a physician network over a decade — the barrier to reaching scale is dramatically lower.

The corresponding exposure is that **every structural advantage is also a dependency.** The rails, the standards and the adoption curve all belong to someone else. A company in this position competes on execution within a ceiling it does not set.

And the ceiling is currently the finding of this case study: if point-of-care usage is near a quarter of accounts, then the addressable market for a records interface is a quarter of the headline, not the headline.

---

## 17. Competitive analysis

| Competitor | Position |
|---|---|
| **Practo** | Established consumer health brand, discovery and teleconsult |
| **Apollo 24/7** | Hospital-chain-backed, owns supply as well as interface |
| **Tata 1mg, PharmEasy** | Pharmacy-led, records as an adjunct |
| **Government ABHA app** | Free, official, and the default |
| **Hospital HMIS vendors** | Own the provider side of the record |

### 17.1 Porter's Five Forces

**Threat of new entrants — High.** The state provides the hard parts. When identity, consent and exchange standards are public, the remaining moat is interface quality and integration effort — both replicable.

**Bargaining power of buyers — High.** The patient pays nothing and can use the official app instead. The clinic chooses among integrators.

**Bargaining power of suppliers — Concentrated in one non-commercial supplier.** ABDM sets the standards and can change them. This is a benign monopolist compared with Day 84's Epic — it does not compete for profit — but it is a single point of dependency nonetheless.

**Threat of substitutes — Very high.** Paper still works, and **85.6%** say they prefer in-person care.

**Competitive rivalry — Intense, in a market where the product is free to the user.**

### 17.2 The moat question

Day 82's Doximity owned a network. Day 84's Abridge rents distribution from Epic and owns an annotated dataset. **Eka Care owns neither the rails nor a proprietary dataset that others could not assemble.**

What it plausibly owns is **assisted-onboarding operations** — the clinic relationships and counter-level process that turn an unaware patient into an account holder. That is an operations moat rather than a technology one. It is real, and section 12.2's ABHAs-per-download ratio of **1.20** is the only public evidence for it.

---

## 18. SWOT

**Strengths.** Statutory identity verifiable and active. Integrated into national infrastructure with five conformance approvals. **1.28%** of national ABHAs created. Claimed **40,000** doctors, **4.06%** of the national professional registry. Distribution inherited from a state programme. Standards-compliant on FHIR, HL7, SNOMED and LOINC.

**Weaknesses.** No published outcome metric of any kind. "3 crore trusted" against "1 crore downloads," unreconciled. No records-per-account figure. No adoption disaggregated by language despite **64.0%** citing language as a barrier. NIC classification places the company outside its own sector's statistics.

**Opportunities.** Publish records-per-account and beat the national **1.12**. Own comprehension rather than interface — the literacy data says judgement, not operation, is the weak skill. Language coverage as a differentiator. Convert assisted onboarding into a measurable activation funnel.

**Threats.** The official ABHA app is free and default. Point-of-care usage near **25.55%** caps the addressable market. DPDP compliance costs arrive with a phased timeline. **51.03%** facility software penetration limits the supply of records to display.

---

## 19. Metrics: what exists, what does not

### 19.1 Published by the government

ABHA accounts **93.95 crore**; records linked **105 crore**; facilities **5.33 lakh**; professionals **9.85 lakh**; Scan & Share tokens **~24 crore**; facilities with software **~2.72 lakh**.

### 19.2 Measured independently

Point-of-care adoption **23.96%**; ABDM unawareness **58.6%**; privacy discomfort **45.00%**; DHLI mean **2.94**; ABHA awareness among one surveyed group **35%**.

### 19.3 Published by the company

Scale claims and five conformance badges. **No outcome metric.**

### 19.4 Measured by nobody

- Whether a record retrieved through the platform was complete or correct
- Whether consent was understood, as opposed to captured
- Adoption by language, literacy or gender at product level
- Records per account at company level
- Whether a linked record changed a clinical decision

**The fourth list decides whether any of this works.**

---

## 20. Proposed North Star metric

**Linked-record-backed monthly active users** — people who both hold at least one linked record and opened the product this month.

```
north_star_computable_by_company = True
north_star_published_by_company  = False
```

### 20.1 Why this one

It is the intersection of the two things the evidence says diverge. An account without records is a row in a database; a record nobody opens is a file in a drawer. Only the intersection is a user.

It is also computable today from data the company necessarily has, and it would immediately expose whether Eka Care's **1.2 crore** accounts behave better or worse than the national **1.12** records-per-account average.

### 20.2 Guardrails

**Guardrail 1 — records per account.** National benchmark **1.12**. Not published by the company. Floor: match the national figure, then beat it.

**Guardrail 2 — privacy comprehension.** Independent proxy: **45.00%** are not comfortable with data privacy protection, and privacy-protection skill scores **2.22**. A product operating under a consent regime that requires *informed* consent should measure whether its users can state what happens to their data.

**Guardrail 3 — language coverage of actual adoption.** **64.0%** cite language as a barrier; nobody publishes adoption disaggregated by language. Until someone does, "28 languages supported" is a feature claim, not a reach claim.

---

## 21. HEART framework

| Dimension | Measure | Reported? |
|---|---|---|
| **Happiness** | Satisfaction with registration | **Yes** — but on survivors only |
| **Engagement** | Scan & Share usage | Nationally (**25.55%**), not per product |
| **Adoption** | ABHA creation | **Yes** — and it is the weakest signal |
| **Retention** | Return use | **No** |
| **Task success** | **Record retrieved and useful** | **No — by anyone** |

Adoption is the best-measured dimension and the least meaningful. Task success is unmeasured, which is now a five-day pattern across two countries and six companies.

---

## 22. Kano analysis

| Feature | Category | Note |
|---|---|---|
| Records actually present when opened | **Must-be** | 1.12 per account nationally |
| Works in the user's language | **Must-be** | 64.0% cite it as a barrier |
| Clear explanation of data handling | **Must-be** | 45.00% not comfortable |
| Assisted account creation | **Performance** | The company's apparent strength |
| Vitals tracking, organ health rating | **Attractive** | Engaging; not the core job |
| Standards compliance | **Indifferent to the user** | Matters to partners, invisible to Sunita |

The three must-be features are the three the evidence flags as unmet. The attractive features are the ones the product page leads with.

---

## 23. User journey

| Stage | What happens | Where it leaks |
|---|---|---|
| Awareness | Patient learns ABDM exists | **58.6% never do** |
| Account creation | ABHA created, often by counter staff | Works — assisted, ratio 1.20 |
| App install | Patient downloads the app | Downloads are a third of claimed users |
| Consent | OTP shared to link records | **60.0% hesitate** |
| Linkage | Records attach to the account | **1.12** per account nationally |
| Point-of-care use | Patient presents ABHA at OPD | **23.96%** of visits |
| Clinical value | Clinician reads and acts on the record | **Measured by nobody** |

### 23.1 The funnel multiplies, and that is the whole explanation

Each stage looks survivable on its own. Multiplied, they produce the gap between 93.95 crore accounts and roughly a quarter usage.

This is why "adoption" is the wrong word for what ABDM has achieved so far. **The programme has achieved distribution.** Adoption is a later stage, and the evidence says it is around one in four at the point of care and unmeasured beyond it.

---

## 24. AARRR funnel

| Stage | Position | Evidence |
|---|---|---|
| **Acquisition** | Exceptional — 93.95 crore accounts | Health Ministry |
| **Activation** | Weak — 23.96% point-of-care use | BMC study |
| **Retention** | Unmeasured | — |
| **Referral** | Unmeasured; 88% want training, which is the opposite signal | BMC study |
| **Revenue** | Not disclosed | — |

An acquisition-heavy funnel with unmeasured retention is the classic shape of a programme optimised on the metric it reports. ABDM reports accounts. Accounts is what it has.

---

## 25. Eval plan

What should be measured continuously and is not.

**Record retrieval success.** When a clinician requests records through the system, what share of requests return something, and what share of those are clinically useful? This is the ABDM equivalent of Day 84's PDSQI-9, and nobody runs it.

**Consent comprehension.** Sample users after consent and ask what they believe they agreed to. A consent regime requiring informed consent, applied to a population scoring 2.22 on privacy-protection skill, needs this as a safety measure, not a research curiosity.

**Stratified adoption.** By language, literacy, gender, age and state. The DHLI gradients — men higher than women, education ρ = 0.480 — say the disparities are real and measurable.

**Record accuracy.** Whether the linked record matches what the encounter actually contained. Entirely unmeasured.

**Activation cohorts.** For assisted-created accounts specifically: what share are ever opened by the person they belong to? This is the single most diagnostic number in the Indian digital health system and nobody publishes it.

---

## 26. Ranked failure modes

By expected harm.

**1. A clinical decision made on an incomplete retrieved record.** A partial record can be worse than no record, because it carries authority. **1.12** records per account nationally means most accounts hold very little, and a clinician who fetches a near-empty record may reasonably infer absence of history rather than absence of linkage. Mitigation: display completeness explicitly — "3 records linked; last updated 2024" — rather than presenting what exists as the record.

**2. Consent captured without comprehension.** **45.00%** not comfortable, **2.22** privacy skill, **60.0%** OTP hesitation, under a regime requiring informed consent. Mitigation: measure comprehension; simplify to a single sentence about who sees what.

**3. Records attached to the wrong person.** Assisted creation at a busy counter using shared identifiers is exactly the workflow in which mismatches occur. No public data exists on identity-resolution error rates. Mitigation: publish the rate.

**4. Exclusion by language and literacy.** **64.0%** cite language; the gradients are significant by gender and education. A system that works for the educated and urban while nominally covering everyone entrenches a gap it appears to close. Mitigation: stratify and publish.

**5. Abandonment after assisted creation.** An account created for someone who never opens it is a stored health record with no owner exercising rights over it. Mitigation: activation cohorts.

**6. Over-reliance on the headline.** Policy and investment decisions made against 93.95 crore rather than against usage. Mitigation: report both, always adjacent.

Failure modes 1, 2 and 3 concern the record and the person. None of the three is measured by anyone.

---

## 27. Human-in-the-loop design

The human in this loop is the patient, and the loop is consent.

It is ceremonial when the person cannot evaluate what they are consenting to — which is what a **2.22** privacy-protection score and **58.6%** unawareness describe.

Three things would make it load-bearing:

**Say what happens in one sentence, in their language.** Not a policy. One sentence: who can see this, for how long, and how to stop it.

**Make refusal visible and costless.** **60.0%** hesitate at the OTP. Treating hesitation as friction to be optimised away is precisely backwards when the law now requires consent to be freely given.

**Show the record before asking to share it.** A person deciding whether to share records they have never seen is not making an informed choice. This is also a product opportunity: the moment someone first sees their own history assembled is the moment the product demonstrates its value.

---

## 28. Product recommendations

Five, each with evidence and a proof metric.

### R1. Publish record-linkage rate and monthly active users separately

**Evidence:** national records-per-account is **1.12**; the company publishes no equivalent, and "3 crore trusted" against "1 crore downloads" is unreconciled.
**Proposal:** publish accounts, accounts with at least one linked record, and monthly active users as three distinct numbers with stated definitions.
**Why first:** it costs nothing, resolves the internal tension in section 12.1, and would make Eka Care the first company in this six-day arc to publish a usage metric.
**Success:** three numbers, three definitions, held stable for a year.
**Cost:** Low.

### R2. Report adoption stratified by language and literacy

**Evidence:** **64.0%** cite language; DHLI gradients are significant by gender and education.
**Proposal:** disaggregate activation and retention by interface language and by proxy for literacy, and publish the gaps.
**Why:** a country-scale health product that works unevenly and reports only averages is reporting the experience of its most advantaged users.
**Success:** published disaggregation; gaps narrowing.
**Cost:** Moderate.

### R3. Publish consent comprehension, not just consent capture

**Evidence:** **45.00%** not comfortable; privacy skill **2.22**; DPDP Rules notified 14 November 2025.
**Proposal:** sample users post-consent, ask what they believe they agreed to, publish the share who answer correctly.
**Why:** it converts a compliance obligation into a measurable product quality, and it is the only proposed metric that directly serves the person rather than the system.
**Success:** published quarterly; comprehension rising.
**Cost:** Moderate. The first number will be uncomfortable.

### R4. Build assisted onboarding into a measured activation funnel

**Evidence:** ABHAs per download **1.20** implies substantial assisted creation; **58.6%** do not know what ABDM is.
**Proposal:** treat counter-created accounts as a distinct cohort. Measure what share are ever opened by their owner, at 7, 30 and 90 days. Design an explanation step into the creation flow.
**Why:** this is the company's apparent operational strength and its least examined one. If assisted-created accounts never activate, the growth metric is manufacturing rows.
**Success:** a published activation rate for assisted cohorts.
**Cost:** High — it requires changing a process that currently optimises for speed at the counter.

### R5. Fund an independent field study of record accuracy

**Evidence:** no study anywhere measures whether a retrieved record is complete or correct.
**Proposal:** fund an independent, pre-registered study comparing retrieved records against source encounters, committing to publish the result.
**Why:** Day 84 showed what independent measurement does for a category. Indian digital health has adoption studies and no accuracy studies.
**Success:** a peer-reviewed publication with the company as funder, not author.
**Cost:** High and slow.

---

## 29. RICE prioritisation

R, I, C, E and every stress factor are **author estimates, not disclosed data**. Reach is held at 120 (lakh — the 1.2 crore ABHAs the company claims to have created), because every proposal's audience is the people whose records the product holds. Stress discounts by dependence on uncheckable claims, execution exposure, and dependence on the state programme.

| ID | Proposal | R | I | C | E | Base | Stress | Stressed |
|---|---|---|---|---|---|---|---|---|
| P1 | Publish linkage rate and MAU separately | 120 | 3.0 | 0.90 | 3.0 | **108.00** | 0.95 | **102.60** |
| P3 | Stratify adoption by language and literacy | 120 | 2.5 | 0.85 | 4.0 | **63.75** | 0.90 | **57.38** |
| P2 | Publish consent comprehension | 120 | 3.0 | 0.75 | 5.0 | **54.00** | 0.85 | **45.90** |
| P4 | Measured assisted-onboarding activation funnel | 120 | 2.5 | 0.70 | 8.0 | **26.25** | 0.65 | **17.06** |
| P5 | Fund an independent record-accuracy study | 120 | 2.0 | 0.55 | 12.0 | **11.00** | 0.45 | **4.95** |

```
rice_base_ranking           = ('P1', 'P3', 'P2', 'P4', 'P5')
rice_stress_ranking         = ('P1', 'P3', 'P2', 'P4', 'P5')
rice_last_under_stress      = 'P5'
rice_last_under_stress_name = 'Fund an independent field study of record accuracy'
rice_last_gap_pct           = 70.98
```

### 29.1 Reading the ranking

Stable under stress, so the top proposals are robust.

**P5 ranks last, by 70.98% below P4** — asserted by the gate, not argued here. An independent accuracy study would be the most valuable single addition to the Indian digital health evidence base, and Day 84 demonstrated exactly what such a study does for a category. It ranks last because confidence is low (0.55), effort is highest (12 person-months), and the stress factor is harshest (0.45).

The reason is structural and worth naming: **a company with 1.28% of a national programme's accounts cannot fund a study of that programme's record accuracy and have the result read as independent.** The finding would be about ABDM, the funder would be a vendor inside ABDM, and the conclusion — whichever way it went — would be contested on those grounds.

**This is the one recommendation that a company genuinely should not lead on.** It belongs with the NHA, ICMR, or an academic consortium. Ranking it last is not a judgement about its value; it is a judgement about who should pay for it, and that is a real strategic distinction the framework surfaced rather than obscured.

P1 loses only **5.00%** under stress because it requires publishing numbers the company already holds. P5 loses **55.00%**.

---

## 30. MoSCoW

**Must have.** R1 (linkage rate and MAU); R3 (stratify by language and literacy).

**Should have.** R2 (consent comprehension).

**Could have.** R4 (assisted-onboarding activation funnel).

**Won't have this cycle.** R5 (independent accuracy study) — and see 29.1: it should be advocated for, not funded, by this company.

---

## 31. PRD: three numbers, three definitions (R1)

**Problem.** Eka Care publishes "3 Cr trusted," "1 Cr downloads" and "1.2 Cr ABHAs created" side by side with no definitions. The three cannot be reconciled without information the company has not provided, and none of them says how many people actually use the product.

**Objective.** Publish three separately defined figures, updated quarterly.

**Proposed metrics.**
1. **Accounts** — ABHA numbers created through the platform, cumulative.
2. **Accounts with linked records** — accounts holding at least one record, with the mean records per account alongside.
3. **Monthly active users** — distinct people who opened the product in the trailing 30 days.

**Non-goals.** Not a clinical claim. Not a substitute for record-accuracy measurement.

**Requirements.**
- R1.1 Publish each definition before publishing the first number.
- R1.2 State whether "accounts" includes assisted creation, and report that split.
- R1.3 Report mean records per account against the national **1.12** benchmark.
- R1.4 Retire "trusted by" unless it can be defined; if retained, define it.
- R1.5 Restate prior periods if a definition changes.

**Success criteria.** Two consecutive quarters under unchanged definitions. Secondary: records per account above the national average.

**Risks.** MAU will be far below 3 crore and the gap will be noticed. Records per account may be below **1.12**. The "trusted by" figure may not survive definition. **All three are reasons to do it** — a number that cannot embarrass you is not a measurement.

---

## 32. Roadmap

**Horizon 1 — next two quarters.** R1 (three numbers), R3 (stratify by language and literacy). Both use data the company already holds; both establish that it will publish figures that can move against it.

**Horizon 2 — quarters three and four.** R2 (consent comprehension), R4 (assisted-onboarding activation). R2 needs the measurement pipeline from Horizon 1; R4 is an operational change that Horizon 1 makes visible.

**Horizon 3 — year two.** Advocate for R5 rather than fund it. Contribute data to an NHA- or academic-led accuracy study.

### 32.1 Sequencing logic

Ordered by **evidence dependency and institutional appropriateness**. The last item is sequenced last not because it is least valuable but because it is least appropriate for this company to own — see 29.1.

---

## 33. Risks to this analysis

**The field study is three hospitals in one district.** Agra, 425 surveyed attendees, 537,278 OPD visits over eight months. It is peer-reviewed and well-designed, and it is one city. India is not uniform; adoption in Odisha or Andhra Pradesh — reported as leading states — may differ substantially.

**One co-author of that study is affiliated with ABDM.** `bmc_has_programme_affiliated_coauthor = True`. This does not invalidate the findings, and arguably makes the critical results more credible, since a programme-affiliated author reporting 23.96% adoption and 58.6% unawareness is reporting against interest. But it is not a fully arm's-length study and the README says so wherever its figures appear.

**The national usage proxy is a ratio of unlike things.** Scan & Share tokens are cumulative events; ABHA accounts are cumulative people. **25.55%** is a proxy, not a rate, and it would overstate usage if people use tokens repeatedly and understate it if many use it without generating tokens. It is reported as a proxy throughout, and its value lies in converging with an independently derived figure, not in its own precision.

**Government figures are self-reported by the programme.** No independent audit of ABHA counts or record-linkage counts was examined.

**Company claims are unverified and undated.** None carries a methodology or a measurement date; all are recorded as claims.

**The register finding is about classification, not conduct.** NIC 74999 is a filing choice made at incorporation, likely by a company secretary, and says nothing about the company's practices.

**RICE inputs are the author's.** Section 29 and ASSUMPTIONS.md.

---

## 34. What a product manager should take from this

**The registration number is not the usage number, and the gap is usually about four to one.** Two independent measurements of Indian digital health adoption landed **1.59pp** apart at roughly a quarter. Day 83 found the same failure at a single company. Before accepting any adoption claim, ask what event the number counts — creation, install, or use.

**Distribution is not adoption.** ABDM has achieved distribution at a scale no other country has matched. Adoption is a later, harder, differently measured thing, and conflating them makes a genuine achievement look like a different, larger one.

**When the state builds the rails, compliance badges replace outcome metrics.** Five conformance approvals, zero performance measures. In standards-driven ecosystems, "compliant" becomes the evidence, and compliance says nothing about whether the thing works.

**Check whether skill or comprehension is the binding constraint.** The literacy data says people operate better than they evaluate. In that situation, simplifying the interface is the wrong instinct — explanation is the product.

**Satisfaction surveys measure survivors.** Over 80% satisfaction in a system with 23.96% usage and 58.6% unawareness describes the quarter it already worked for.

**Read your own numbers next to each other.** Three crore trusted, one crore downloads. Somebody approved both on the same page. The definitions are probably fine; the absence of them is the failure, and it takes ten minutes to fix.

---

## 35. The six-rung ladder

| Rung | Company | Market | Model | What is disclosed about outcomes |
|---|---|---|---|---|
| 1 | **Day 80 — Hims & Hers** | US | Private sector | **No AI metric at all** |
| 2 | **Day 81 — Hinge Health** | US | Private sector | Cost metric, no outcome |
| 3 | **Day 82 — Doximity** | US | Private sector | AI cost audited; claims quote-only |
| 4 | **Day 83 — OpenEvidence** | US | Private sector | No filing; tested only in court |
| 5 | **Day 84 — Abridge** | US | Private sector | **Independent RCTs measure the outcome** |
| 6 | **Day 85 — Eka Care** | **India** | **Public infrastructure** | **The state measures scale; independents measure usage at a quarter** |

```
ladder_length            = 6
ladder_india_count       = 1
ladder_public_infra_count = 1
```

### 35.1 What the sixth rung adds

The first five rungs were all private-sector American companies, and the finding across them was that vendors disclose what obligation or competition forces them to.

India changes the variables and **the finding survives**. Here the state does the measuring, publishes at extraordinary scale, and reports honestly — and the gap between what is measured and what matters persists anyway, because **the state measures what the state built**, which is accounts.

The company inside that system publishes no outcome metric either. Six companies, two countries, two economic models, one constant: **whoever is doing the measuring measures their own contribution, and nobody measures the result.**

---

## 36. Day 83 and Day 85, side by side

| Measure | Day 83 — OpenEvidence | Day 85 — Eka Care / ABDM |
|---|---|---|
| Scale of the claim | 70.23% of US physicians registered | 93.95 crore ABHA accounts |
| What the number counted | Registration | Registration |
| The metric that shifted | "40%" moved from registered to daily active | Accounts reported as adoption |
| Independent usage estimate | One preprint | Two peer-reviewed field studies |
| Measured usage | Not measured | **23.96%** at the point of care |
| Gap, registered to used | **44.68pp** (registered share versus national usage proxy) | — |

```
registered_vs_active_gap_recurs = True
```

Day 83 found a company whose headline percentage quietly changed meaning between two press releases. Day 85 finds a national programme where the headline was never a usage number to begin with, and two independent studies had to supply one.

**The second case is more honest and produces the same misunderstanding.** Nobody at ABDM claimed 93.95 crore people use the system daily. The number is accurate and the inference is wrong, and the inference is what travels.

---

## 37. Public infrastructure as a product strategy

This deserves assessment on its own terms, because it is the most interesting structural thing in the case study and it is not a criticism.

**What India got right.** Identity, consent and exchange standards as public goods, with private companies competing on interface. The alternative — which the United States effectively chose — is proprietary networks, where Day 82's Doximity spent a decade building a physician network and Day 84's Abridge rents distribution from Epic. India's approach produced national-scale account coverage in a fraction of the time and at a fraction of the private capital.

**What it did not solve.** Building rails does not create journeys. **51.03%** of registered facilities run the software; **23.96%** of OPD visits use the identity; **58.6%** of patients do not know the system exists. Infrastructure makes a thing possible; it does not make it happen.

**The honest comparison.** American digital health has better-measured products and worse coverage. Indian digital health has extraordinary coverage and almost no outcome measurement. Neither has both, and each would be improved by the other's strength.

### 37.1 The opportunity this creates for a private company

If the state supplies rails and coverage, and nobody supplies evidence, then **evidence is the open competitive position.** The first Indian digital health company to publish records-per-account, activation rates for assisted cohorts, and consent comprehension would own a claim no competitor could match with a badge.

That is the strategic argument for section 28's recommendations, and it is stronger here than it was in any of the five American case studies — because in a market where everyone holds the same five certifications, a real number is the only differentiator left.

---

## 38. Scenario analysis

Author constructs applying arithmetic to published figures. Not forecasts.

### 38.1 If usage rose from a quarter to half

Point-of-care usage at **25.55%** of accounts. Suppose it reached 50%.

The addressable base for any records interface roughly doubles without a single new account being created. **Every private company in this ecosystem has more to gain from activation than from acquisition**, and every one of them — including Eka Care — reports acquisition.

### 38.2 If facility software penetration closed

**51.03%** of registered facilities run ABDM software; **2.61 lakh** registered facilities do not.

Facility deployment is the supply side of the record exchange. A patient who presents an ABHA at a facility that cannot read it experiences the system failing. Closing that gap is not a company's job — but a company's activation rate is capped by it, which makes it the single most important external variable in Eka Care's plan.

### 38.3 If the awareness gap closed

**58.6%** do not know what ABDM is; **88.00%** want training.

The second number is the interesting one. A population that overwhelmingly asks for help is not a population resisting the product — it is a population under-served by explanation. This is the cheapest identified intervention in the entire case study and the one least owned by anybody.

---

## 39. Sensitivity: what would change the conclusion

**On the usage estimate.** The convergence of **25.55%** and **23.96%** is the backbone. A larger multi-state field study finding materially higher adoption would move it. A study in a leading state — Odisha or Andhra Pradesh — is the obvious test, and no such published study was found.

**On the awareness finding.** **58.6%** comes from one district. Replication elsewhere would confirm or bound it.

**On the company claims.** Publishing definitions for "trusted by" would resolve section 12.1 in a sentence.

**On the register finding.** Nothing would change it. The CIN is what it is, and NIC 74999 is the residual class.

---

## 40. Counterfactual: suppose every company claim is true

Assume 3 crore Indians do trust Eka Care, 1.2 crore ABHAs were created through it, 40,000 doctors use it, and 30 crore vitals are stored.

**Most of this analysis survives.** National point-of-care usage is still **25.55%**. The field studies still find **23.96%** adoption and **58.6%** unawareness. Records per account is still **1.12**. The company still publishes no outcome metric, and "trusted by" is still undefined.

**And one thing gets sharper.** If 3 crore people really do rely on this product, then a company holding health data for 3 crore Indians publishes nothing about whether that data is complete, correct, or understood by the people it describes. **Scale is the argument for measurement, not a substitute for it.**

---

## 41. Regulatory position

Health data in India is now governed by the **Digital Personal Data Protection Act** and the **Digital Personal Data Protection Rules, 2025**, notified **14 November 2025**, with the **Data Protection Board of India** as enforcement authority and a phased implementation timeline.

Three consequences for a product in Eka Care's position.

**Consent must be informed, unambiguous and freely given.** Section 11 sets out the tension: a population scoring **2.22** on privacy-protection skill, **45.00%** uncomfortable with data privacy, and **60.0%** hesitant at the OTP step.

**Notices must state purpose, categories, retention and withdrawal.** For a records product, retention is the hard one — a health record's value is its longevity, and a retention period stated honestly may be indefinite.

**Assisted creation is the exposure.** An account created at a counter for someone who does not know what ABDM is raises the sharpest question the Rules pose. Whether that consent was informed is exactly what nobody measures, which is why R2 in section 28 is a compliance investment as much as a product one.

No public source addresses Eka Care's DPDP compliance posture and this section makes no claim about it.

---

## 42. Concentration and dependency

| Dimension | Position |
|---|---|
| Identity layer | **ABDM** — not owned |
| Consent protocol | **ABDM** — not owned |
| Exchange standards | FHIR, HL7, SNOMED, LOINC — public |
| Distribution | Clinics plus the national programme |
| Competing default | The official ABHA app, free |
| Revenue concentration | Not disclosed |
| Geographic | India |

Day 84's Abridge depends on Epic — a commercial partner that also competes. Eka Care depends on ABDM — a non-commercial standards body that does not compete for profit but does ship a free official app.

**The second dependency is more benign and less negotiable.** A commercial partner can be negotiated with. A national programme sets terms by policy, and a company's roadmap is downstream of decisions it has no counterparty to discuss.

---

## 43. Data and privacy considerations

Three obligations follow from what this product holds.

**Records created for people who do not know they have them.** The assisted-creation ratio and the awareness gap together imply a substantial number of accounts whose owners are not exercising any rights over them. Those accounts still accumulate data.

**Retention is undisclosed.** No public source states how long records persist, whether they are used for any secondary purpose, or what de-identification standard applies.

**Identity resolution is the silent risk.** Attaching records to the wrong person is failure mode 3 in section 26. In assisted creation at a busy counter, it is the most plausible error in the system and the least examined.

---

## 44. The talent and ecosystem question

This case study has no litigation section, which is itself notable.

Day 83's OpenEvidence had six federal cases in 559 days. Day 84's Abridge was a trade-secrets defendant. No litigation involving Orbi Health Private Limited was identified in the sources examined — and Indian court records are not as readily searchable as the US federal PACER system, so **absence of found litigation is not evidence of absence.** It is recorded as a gap rather than a finding.

What is observable is the ecosystem shape. A market where the state supplies the standards produces less proprietary-technology conflict, because there is less proprietary technology to fight over. That is a genuine second-order benefit of public infrastructure and it belongs alongside the costs in section 37.

---

## 45. What Eka Care does better than the American comparisons

**It reaches people the American products do not attempt.** Every company in Days 80–84 sells to insured, employed or institutionally connected populations. This one operates where the alternative is a plastic bag of prescriptions.

**It works inside open standards.** FHIR, HL7, SNOMED and LOINC conformance means records are portable by design. Day 84's Abridge runs on Epic's private APIs; Day 82's Doximity owns a closed network. Portability is a structural consumer benefit that none of the American case studies offered.

**It does assisted onboarding.** The ABHAs-per-download ratio of **1.20** suggests real operational work getting accounts to people who would not self-serve. That is unglamorous, hard, and the reason coverage exists at all.

**The state measures, and publishes.** ABDM's figures are public, regular and detailed — facilities, professionals, tokens, records, by state. Compared with the disclosure available for Days 83 and 84, that is a materially better information environment, and it is why this case study could measure a usage gap at all.

**The criticism is narrow:** the numbers published measure the system's own construction, and the company inside it publishes less than the state does.

---

## 46. Day 86 connection

Tomorrow is **Hippocratic AI** — and it returns to the United States and to the sharpest version of the question this arc keeps circling.

Hippocratic AI builds AI agents that speak to patients directly, by voice, for clinical tasks. Every company in this six-day arc has had a human between the AI and the patient: a clinician reading a note, a physician reading a reference answer, a patient reading their own record. That intermediary is the safety argument in each case.

Day 86 examines what happens when it is removed.

The method question sharpens with it. Day 84 found that independent randomized evidence existed for ambient documentation. Whether comparable evidence exists for autonomous patient-facing agents — and what "outcome" even means when the product *is* the clinical interaction — is tomorrow's central question.

---

## 47. Recommended diagrams

Per series standard from Day 50: **no Mermaid**. Markdown tables and ASCII only.

**D1 — The convergence.** Two bars from unrelated sources: national usage proxy **25.55%**, field study **23.96%**, with the **1.59pp** gap annotated and both labelled with their method.

**D2 — The funnel that multiplies.** Seven stages from awareness to clinical value, with the measured leak at each: 58.6% unaware, 60.0% OTP hesitation, 1.12 records per account, 23.96% point-of-care use, and "unmeasured" at the end.

**D3 — The CIN decoded.** The 21 characters of `U74999KA2020PTC141864` split into six labelled segments, with `74999` highlighted and captioned "other professional, scientific and technical activities, not elsewhere classified."

**D4 — Registration versus use.** A single bar of 93.95 crore accounts with roughly a quarter shaded, captioned with both independent estimates.

**D5 — The six-rung ladder.** Days 80–85 with market and model columns, Day 85 highlighted as the first outside the US and the first built on public infrastructure.

### 47.1 ASCII rendering of D1

```
   TWO MEASUREMENTS. NOTHING IN COMMON.

   Health Ministry, Jul 2026      |  BMC Health Serv Res, Mar 2026
   Scan & Share ÷ ABHA accounts   |  537,278 OPD visits, 3 hospitals
   national administrative        |  independent field study
  --------------------------------+--------------------------------
            25.55%                |            23.96%
                                  |
              \_________ 1.59pp __________/

   93.95 crore accounts created.  About one in four gets used.
```

---

## 48. Recommended screenshots and visual assets

1. The GLEIF record for ORBI HEALTH PRIVATE LIMITED showing the CIN and the MCA registration authority.
2. The Health Ministry statement of 10 July 2026 with the 93.95 crore and 105 crore figures.
3. The BMC abstract passage reporting 537,278 OPD visits and 129,007 ABHA registrations.
4. The BMC passage reporting that 58.6% lacked adequate knowledge of ABDM.
5. The eka.care product page showing "Trusted by more than 3Cr Indians" adjacent to "1 Cr+ Downloads."

Items 2 and 3 side by side are the strongest single visual: the national headline against the hospital-floor reality. Item 5 makes its own argument without commentary. All are public.

---

## 49. Is Indian digital health solved?

On the evidence, the layers divide cleanly.

**Solved.** Identity at population scale. **93.95 crore** accounts is a coverage achievement no other country has matched, and it was done in roughly four years.

**Working.** Record linkage is deepening — **0.67** records per account in January 2026, **1.12** by July. Scan & Share grew **166.67%** over the same period. The curves point the right way.

**Unresolved.** Point-of-care usage at roughly a quarter. Facility software penetration at **51.03%**. Awareness at **41.40%**.

**Unmeasured.** Whether a retrieved record is complete. Whether consent was understood. Whether any of this changed a clinical decision.

A system where the identity layer is solved and the comprehension layer is untouched is at a specific stage: **the infrastructure has outrun the explanation.** Day 84 found the engineering had outrun the measurement in American ambient documentation. This is the same shape in a different layer of the stack.

---

## 50. The state as a product organisation

ABDM is, functionally, a product organisation with **93.95 crore** registered users, and it is worth assessing as one.

**What it does well.** Ships at extraordinary scale. Publishes metrics regularly and in detail — accounts, records, facilities, professionals, tokens, by state. Sets open standards. Reports honestly: the same ministry that publishes the 93.95 crore headline also publishes the **24 crore** Scan & Share figure that undercuts it, and the **2.72 lakh** software-deployment figure against **5.33 lakh** registered facilities.

**Where it has the classic product-organisation failure.** It reports the metrics of its own construction. Accounts, registrations, facilities enrolled — these measure what the programme built. Usage, comprehension and clinical effect measure what the programme achieved, and those are supplied by academics in Agra and Guwahati.

That is not a criticism unique to government. It is the same failure this series has documented in five private companies on two continents. **The tendency to measure your own output rather than your user's outcome is not a market failure or a state failure. It is an organisational one**, and it appears wherever the person measuring is the person who built the thing.

---

## 51. Open questions for the category

**Why does nobody measure record retrieval success?** A national exchange has been built. Whether a request returns a useful record is the system's core function and no published figure describes it.

**Who is responsible for comprehension?** **88.00%** want training. The programme builds rails, companies build interfaces, and explanation belongs to neither.

**What does an unopened assisted account mean under DPDP?** Consent captured at a counter from a person who does not know what ABDM is sits at the exact centre of the new Rules.

**Should account coverage be reported next to usage, always?** The 93.95 crore figure is accurate. Reported alone, it produces a false impression that the programme's own Scan & Share number corrects.

**Does this work equally across languages?** **64.0%** cite language as a barrier, and no adoption figure anywhere is disaggregated by it.

---

## 52. A closing note on method

The most useful thing this case study did was decode a 21-character string.

`U74999KA2020PTC141864` took about a minute to parse and produced the register finding, the incorporation date, the state, the corporate form and the legal name — none of which was available for the two American private companies in Days 83 and 84 at any price.

**India's company register is a better primary source for a private company than anything available in the United States**, and it is free. For any analyst looking at an Indian company, the CIN is the first thing to read and the last thing anyone reads.

The second most useful thing was searching PubMed before the company's site — the lesson from Day 84, applied again, and it produced the two field studies that turned a scale story into a usage story.

---

## 53. What six days established

| Day | Company | Market | The finding |
|---|---|---|---|
| 80 | Hims & Hers | US | An AI narrative with no AI metric |
| 81 | Hinge Health | US | A metric measuring cost saved, not health gained |
| 82 | Doximity | US | AI cost audited; AI claims quote-only |
| 83 | OpenEvidence | US | No filing; claims tested only in litigation |
| 84 | Abridge | US | Independent trials measure the outcome; the vendor does not publish it |
| 85 | Eka Care / ABDM | India | The state measures scale; usage is about a quarter of accounts |

Six companies, two countries, two economic models, one constant: **whoever does the measuring measures their own contribution.**

Vendors measure adoption. Governments measure coverage. Academics measure outcomes — when somebody funds them.

The practical instruction after six days is unchanged and now better evidenced: **ask what event the number counts, and who benefits from counting it that way.**

---

## 54. Appendix A — source conflicts and reconciliations

Series rule: every conflict documented, never silently resolved.

### A1. Pooled ratio versus reported monthly rate

The BMC study reports a monthly adoption rate of **23.96%**. Dividing the reported totals — 129,007 ABHA registrations over 537,278 OPD visits — gives **24.01%**.

| Measure | Value |
|---|---|
| Gap | **0.05pp** |

**Resolution:** the authors report a mean of monthly rates; the pooled ratio weights by monthly volume. Both are computed in the gate and both are reported. Immaterial to any conclusion.

### A2. Facility counts across the two government reports

January 2026 (NHA) reports 16,765 hospitals and 17,229 facilities registered. July 2026 (Health Ministry) reports **5.33 lakh** facilities in the registry.

**Not reconciled, and not treated as a conflict.** These are near-certainly different measures — the January figures appear to count facilities participating in Scan & Share, the July figure counts the Health Facility Registry as a whole. The July report separately gives **2.72 lakh** facilities running ABDM software, which sits between them. All three figures are reported with their labels; no growth rate is computed across them.

### A3. The Scan & Share ratio is a proxy, not a rate

**25.55%** divides cumulative tokens by cumulative accounts. Tokens are events and accounts are people, so this is a proxy for usage intensity, not a share of accounts that have ever been used. Reported as a proxy throughout. Its evidential value is the convergence with the independently derived **23.96%**, not its own precision.

### A4. A wrong LEI, discarded

An initial search surfaced LEI 2549001QJF90TQE84W04, which resolves to **ORBINOX INDIA PRIVATE LIMITED**, a valve manufacturer in Coimbatore, unrelated to this company. It was retrieved, identified as a false match and discarded before any figure was derived from it. Recorded here because a reader repeating the search will hit the same false positive.

### A5. "Eka Software Solutions" is a different company

A financial-data page for "Eka Software Solutions" appears in searches for this company's financials. That is a commodity-trading software firm, unrelated to Orbi Health Private Limited. No figure from it is used.

### A6. Company claims carry no dates

None of the seven figures on the product page states a measurement date or methodology. They are compared against July 2026 government figures because that is the most recent government reporting available; if the company figures are older, the derived shares in section 12.3 understate the company's current position.

### A7. The BMC study's field period predates the national figures

The study ran September 2024 to April 2025; the national figures are January and July 2026. The convergence in section 6.4 therefore compares measurements roughly a year apart. Adoption has plausibly improved since — Scan & Share grew **166.67%** in the first half of 2026 alone. **The 23.96% should be read as a floor, not a current rate**, and this is the most significant limitation in the case study.

---

## 55. Appendix B — sources examined and not used

**Tracxn, PitchBook, CB Insights, Inc42, LeadIQ.** Aggregators, not primary. Consulted to locate the legal entity name; no figure used.

**Indian court records.** Not systematically searchable in the way US federal dockets are. No litigation search result is reported as a finding; section 44 records the gap.

**The ABDM public dashboard.** Returned HTTP 403 to automated retrieval. Government figures come from the Health Ministry statement of 10 July 2026 and NHA reporting of 29 January 2026 instead.

**The Health Systems & Reform assessment of ABDM.** Returned HTTP 403. Not used.

**IBEF and general news aggregation.** Used only to locate the Health Ministry statement; the figures are attributed to the ministry.

**MCA21 filings themselves.** Not retrieved. The CIN, legal name, address, incorporation date and status come from GLEIF, which validates against MCA. **Paid-up capital, directors, charges and annual filings were not examined**, and they are the obvious next source for anyone extending this analysis.

**Market data and valuation.** Excluded by series rule. The 2022 Series A is mentioned once as context and no valuation figure is used.

---

## 56. Methodology

**Source acquisition.** Statutory identity from the GLEIF public API, validated against India's Ministry of Corporate Affairs. Peer-reviewed literature through PubMed. Government figures from the Union Health Ministry statement of 10 July 2026 and National Health Authority reporting of 29 January 2026. Regulatory context from the Digital Personal Data Protection Rules, 2025. Company claims from eka.care product pages.

**Gate-first discipline.** `verify.py` was written and passing before any prose existed.

**Numbering conventions.** Indian units are used as sourced. The gate converts explicitly — 1 crore = 10,000,000 and 1 lakh = 100,000 — and never mixes conventions inside a calculation.

**Evidence tiering.** Five tiers, asserted in the gate, so that a government figure is not treated as an independent measurement and a company claim is not treated as either.

**Rounding.** Percentages to two decimals, tolerance 0.005 absolute unless stated. Derived figures computed from unrounded inputs.

**Cross-checking.** `crosscheck.py` extracts every two-decimal figure in this README and in ASSUMPTIONS.md and confirms each traces to a gate value.

**Author constructs.** RICE inputs, stress factors, personas, the North Star proposal, guardrail thresholds, the eval plan, the failure-mode ranking and all scenario parameters are the author's and are labelled as such.

**Fabrication policy.** No figure, quote, date, identifier or study result is invented. Where information is unavailable, this document says so.

---

## 57. Reproducing this analysis

```bash
# 1. Statutory identity (free, no key)
curl -A "<your contact>" --get "https://api.gleif.org/api/v1/lei-records" \
  --data-urlencode "filter[entity.legalName]=Orbi Health"

# 2. Decode the CIN
python3 - <<'PY'
cin = "U74999KA2020PTC141864"
print("listing:", cin[0], "| NIC:", cin[1:6], "| state:", cin[6:8],
      "| year:", cin[8:12], "| form:", cin[12:15], "| number:", cin[15:])
PY

# 3. The field studies (open access via PMC)
#    Ranjan A, et al. BMC Health Serv Res 2026;26(1). PMID 41787376.
#    DOI 10.1186/s12913-026-14314-7
#    Datta A, et al. Cureus 2025;17(4):e82605. PMID 40400882.
#    DOI 10.7759/cureus.82605

# 4. Run the gate. 148 checks. Non-zero exit on any failure.
python3 verify.py

# 5. Cross-check the prose against the gate.
python3 crosscheck.py
```

---

## 58. A playbook for evaluating an Indian private company

Generalised from this case study, and genuinely faster than the US equivalent.

**1. Get the CIN.** Search GLEIF by legal name, or the MCA master-data service. The CIN gives you listing status, NIC code, state, year and corporate form in 21 characters.

**2. Read the NIC code against the business.** A mismatch — or a residual code like 74999 — tells you how the company described itself at incorporation, which is often more candid than its marketing.

**3. Check brand name against legal name.** They frequently differ. Everything statutory attaches to the legal name.

**4. Pull the government programme's own numbers if the company depends on one.** ABDM publishes at a level of detail no private company matches, and it publishes the figures that undercut its own headline.

**5. Search PubMed for field studies of the programme, not the company.** Indian digital health has an adoption literature. It will tell you what share of the headline is real.

**6. Test the company's claims against each other.** Downloads against users. Accounts against downloads. The ratios reveal the definitions the company did not state.

**7. Note what the badges are.** In standards-driven markets, conformance certifications accumulate and substitute for outcome measures. Count how many badges and how many numbers.

**8. Write down what you could not verify.** Here that ran to thirteen categories — and unlike Days 83 and 84, the company's identity was not one of them.

---

## 59. Limitations

This analysis rests on one statutory record, two government reporting points, two peer-reviewed field studies, one regulatory instrument and a set of undated company claims. No financial statement was examined.

The field studies cover three hospitals in Agra and one department in Guwahati. India is not uniform.

The most significant limitation is temporal: the primary field study ran to April 2025, and the national figures are from 2026. **The 23.96% adoption figure should be read as a floor.**

No clinical assessment of Eka Care is made or implied. Nothing here asserts that any company claim is false.

The register finding concerns classification, not conduct.

---

## 60. References

**Statutory identity.** Global Legal Entity Identifier Foundation, LEI record 335800XQK6WJNULLIB28 for ORBI HEALTH PRIVATE LIMITED, CIN U74999KA2020PTC141864, registration authority RA000394 (India, Ministry of Corporate Affairs). Retrieved via the public GLEIF API, 23 September 2026.

**Government programme.** Union Health Ministry figures reviewed at the third Mission Steering Group meeting chaired by Union Health Minister J.P. Nadda, statement dated 10 July 2026. National Health Authority figures reported 29 January 2026.

**Independent research.** According to PubMed:

Ranjan A, Singh G, Singh H, Singh M. "Adoption, digital health literacy, and patient satisfaction of Ayushman Bharat Digital Mission: an analytical cross-sectional study among outpatient department attendees." *BMC Health Services Research* 2026;26(1). PMID 41787376. [DOI](https://doi.org/10.1186/s12913-026-14314-7). *Note: one co-author is affiliated with ABDM, Lucknow.*

Datta A, Kaushik JS, Malakar H. "Perceptions of Digital Health App Usage Among Women Attending Obstetrics and Gynecology Outpatient Department in a Tertiary Care Setting." *Cureus* 2025;17(4):e82605. PMID 40400882. [DOI](https://doi.org/10.7759/cureus.82605).

**Regulatory.** Digital Personal Data Protection Rules, 2025, notified by the Ministry of Electronics and Information Technology, 14 November 2025. Data Protection Board of India as enforcement authority.

**Company sources.** eka.care product pages, retrieved 23 September 2026.

**Series cross-references.** Day 80–84 comparator figures are recomputed inside this case study's own `verify.py` and are not carried across as prose assertions.

---

## 61. Document control

| Field | Value |
|---|---|
| Case study | Day 85 of 90 |
| Subject | Eka Care — Orbi Health Private Limited (India, private) |
| Method | Statutory registry + government programme + independent field studies + claim consistency |
| Primary sources | 1 statutory record, 2 government reporting points, 2 peer-reviewed studies, 1 regulatory instrument |
| Verification checks | **148**, all passing |
| Unverifiable categories asserted | **13** |
| Company outcome metrics published | **0** |
| Register misclassification tally | **12 of 85** (**14.12%**) |
| Diagrams | Markdown tables and ASCII only |
| Fabricated figures | **0** |

---

## 62. Series index

| Day | Company | Central finding |
|---|---|---|
| 80 | Hims & Hers | AI narrative with zero disclosed AI metrics |
| 81 | Hinge Health | Discloses an AI cost metric, not a clinical one |
| 82 | Doximity | AI cost is audited; every AI claim is quote-only |
| 83 | OpenEvidence | No filing exists; the only adversarial test is litigation |
| 84 | Abridge | The evidence exists — the vendor didn't produce it |
| **85** | **Eka Care** | **93.95 crore accounts; about a quarter get used** |
| 86 | Hippocratic AI | *(forthcoming — the human leaves the loop)* |

---

## 63. Standing questions for Eka Care

Ordered by how much the answer would change the assessment.

1. **How many of the 1.2 crore ABHAs created have ever been opened by the person they belong to?** The company has this number. It is the most diagnostic figure in Indian digital health.
2. **What is "trusted by more than 3Cr Indians" counting**, given one crore downloads?
3. **What is the mean records per account**, against the national **1.12**?
4. **What share of users can state what happens to their data**, under a regime requiring informed consent?
5. **What is adoption by interface language**, given **64.0%** cite language as a barrier?

---

## 64. The one-line version

India gave 93.95 crore people a health account.

Two independent measurements say about one in four of those accounts gets used at the point of care, and nearly three in five holders do not know the programme exists.

**Coverage was the hard engineering problem. Comprehension is the hard product problem, and nobody owns it.**

---

## 65. Postscript: on what a register is worth

Three days ago this series lost its oldest running thread. Days 83 and 84 covered American private companies, and the register-classification note — present in eighty-two consecutive case studies — simply could not be written, because the United States does not publish for a private company what India publishes for every company.

Today it came back from a free API call, and it produced the sharpest register finding of the series: not a wrong code, but the residual code. A national health-records company filed under *not elsewhere classified*.

There is a small lesson in that for anyone doing this kind of work. **The best primary source available on a company is often the one its own country requires it to file, and the quality of that source varies enormously by jurisdiction for reasons that have nothing to do with the company.** An Indian private company is more legible to an outside analyst than an American one — which is the opposite of what most people would assume, and it is worth knowing before you conclude that something cannot be verified.

---

*Day 85 of 90. Built from primary sources. 148 programmatic checks. Zero fabricated figures. One 21-character string that did more work than any company page.*
