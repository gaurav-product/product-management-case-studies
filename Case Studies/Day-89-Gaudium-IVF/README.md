# Day 89 — Gaudium IVF: When the Patient Is the Auditor

**A Product Management case study on a regulator that collects outcomes and publishes none of them — and what a person is left to decide on.**

*Part of a 90-day series of evidence-based product case studies. Day 89 of 90.*

---

## 1. At a Glance

| | |
|---|---|
| **Legal entity** | GAUDIUM IVF AND WOMEN HEALTH LIMITED |
| **Previous name** | Gaudium IVF and Women Health **Private** Limited |
| **Registered office** | Janakpuri, Delhi |
| **LEI** | 894500Q78I5CP8ZLV929 (ISSUED) |
| **CIN** | U85100DL2015PLC278296 |
| **NIC activity code** | **85100 — Hospital activities** |
| **Company class** | Public limited (**PLC**) — but **unlisted** |
| **Securities disclosure obligation** | **None** |
| **Device regulation obligation** | **None** |
| **Health-service obligation** | Registration under the ART (Regulation) Act 2021 |
| **Outcome figures published by the regulator** | **0** |
| **Outcome figures published by the clinic** | **0** |
| **Verification** | `verify.py` — **242 programmatic checks, all passing** |

---

## 2. Why This Company, Today

Two days ago this series looked at a Nasdaq-listed company with the maximum securities-disclosure burden available, and found **zero** published performance metrics for its clinical algorithms. Yesterday it looked at a private Indian company with no securities obligation whatsoever, and found nine FDA clearances, five of them carrying full sensitivity, specificity and confidence intervals.

The conclusion of those two days was that **the kind of obligation determines the kind of evidence**. Securities regulation asks what investors must know and produces financial statements and a description of method. Device regulation asks whether a product is as safe and effective as its predicate, and produces accuracy figures.

Day 88 closed by naming what came next:

> Tomorrow is Gaudium IVF — and it moves from imaging to fertility, from a company with nine regulatory clearances to a clinical services business, and from evidence that a regulator compelled to evidence that a **patient** has to evaluate without any of the machinery of the last seven days.

Gaudium IVF is a fertility clinic group. It sells a service, not a device. Nobody clears a consultation. It is unlisted, so no one audits its accounts in public. And the decision in front of its customer is one of the most consequential and expensive a person ever makes on the basis of a success rate.

There **is** a regulator. India's Assisted Reproductive Technology (Regulation) Act, 2021 created a National ART & Surrogacy Registry, and the government's own description of that registry says it collects "details of all the clinics and banks of the country including nature and types of services provided by them, **outcome of the services** and other relevant information."

So the outcomes are collected.

**They are not published.** The registry portal, observed live, offers signup and login and nothing else. There is no public search, no public directory, no clinic-level outcome page. A prospective patient in India cannot look up a single number about a single clinic.

That is Day 89.

---

## 3. How to Read This Case Study

This is not an audit of Gaudium IVF, and it is important to say so at the top. It is an examination of an **information structure**, with one company as the specimen.

The finding is not that this clinic does anything wrong. It publishes no outcome figures, which is lawful in India, and which — as §26 shows from a peer-reviewed audit of 161 Brazilian clinics — is close to universal. The finding is that **nothing in the system produces the number a patient needs**, and that this is true even in the two markets where the regulator does publish.

Three reading paths:

- **The structural finding**: §18 through §24.
- **What clinics publish when nobody makes them**: §25 through §30.
- **Why the obvious fix never happens**: §49 through §51.

Every figure carrying two or three decimal places here is produced by `verify.py`. Nothing is estimated or inferred unless the sentence says so.

---

## 4. Evidence Standard

Unchanged since Day 1, tightened across 88 prior case studies:

1. **No fabrication.** No metric, date, or relationship appears unless it is in a cited primary source.
2. **Facts and inferences are separated at the sentence level.**
3. **Arithmetic is executed, not asserted.** Every derived figure is computed in `verify.py` from unrounded inputs before any prose exists.
4. **Absences are findings.** What a source does not say is recorded as a fact about the source.
5. **The gate precedes the prose.**

There is a sixth rule that matters more today than on any previous day:

6. **A named private company is a specimen, not a defendant.** Where this case study records what Gaudium's website does and does not contain, it records it factually, marks it as a patient-facing artefact rather than evidence of performance, and does not generalise findings from audits of other countries' clinics onto it. `verify.py` asserts `uk_or_brazil_findings_apply_to_gaudium` as **False**.

---

## 5. Source Inventory

All sources retrieved 2026-09-27.

**Registry and corporate record**

| Ref | Source |
|---|---|
| **[G]** | GLEIF LEI record 894500Q78I5CP8ZLV929 |
| **[R]** | National ART & Surrogacy Registry portal, `registry.artsurrogacy.gov.in` — observed live |
| **[P]** | National ART & Surrogacy Portal, `artsurrogacy.gov.in` — registry description |
| **[C]** | CDC National ART Surveillance System and ART Success Rates |
| **[W]** | Gaudium IVF public website — home and `/about` |

**Peer-reviewed literature.** According to PubMed, with DOIs as required by that source:

| Ref | Study | PMID | DOI |
|---|---|---|---|
| **[L1]** | Wilkinson J, Vail A, Roberts SA. *Direct-to-consumer advertising of success rates for medically assisted reproduction: a review of national clinic websites.* BMJ Open 2017 | 28082363 | [10.1136/bmjopen-2016-012218](https://doi.org/10.1136/bmjopen-2016-012218) |
| **[L2]** | Carneiro MM, et al. *Quality of information provided by Brazilian Fertility Clinic websites.* JBRA Assist Reprod 2023 | 35916465 | [10.5935/1518-0557.20220026](https://doi.org/10.5935/1518-0557.20220026) |
| **[L3]** | van de Wiel L, Wilkinson J, Athanasiou P, Harper J. *The prevalence, promotion and pricing of three IVF add-ons on fertility clinic websites.* Reprod Biomed Online 2020 | 32888824 | [10.1016/j.rbmo.2020.07.021](https://doi.org/10.1016/j.rbmo.2020.07.021) |
| **[L4]** | Toftager M, et al. *Cumulative live birth rates after one ART cycle including all subsequent frozen-thaw cycles in 1050 women.* Hum Reprod 2017 | 28130435 | [10.1093/humrep/dew358](https://doi.org/10.1093/humrep/dew358) |
| **[L5]** | Tank J, Kotiswaran P, et al. *Voices from Health Care Providers: Assessing the Impact of the Indian ART (Regulation) Act, 2021.* J Obstet Gynaecol India 2023 | 37701091 | [10.1007/s13224-023-01815-2](https://doi.org/10.1007/s13224-023-01815-2) |
| **[L6]** | Gürtin ZB, Tiemann E. *The marketing of elective egg freezing.* Reprod Biomed Soc Online 2020 | 33336090 | [10.1016/j.rbms.2020.10.004](https://doi.org/10.1016/j.rbms.2020.10.004) |

---

## 6. Evidence Tiers

Day 87 tiered by *what compelled the statement*, and Day 88 kept that axis because it was the only one that explained the data. Day 89 keeps it, and the table is shorter than on any previous day.

| Tier | Description | What it means | Present here? |
|---|---|---|---|
| **T1 — Regulator-published** | Outcome data a regulator publishes | Anyone can read it | **No — for India** |
| **T2 — Independent peer-reviewed** | Researchers with no stake measured it | Real evidence | Yes, about **markets** |
| **T3 — Regulator-collected, unpublished** | Compelled, filed, invisible | Exists, unreachable | **Yes — the finding** |
| **T4 — Statutory registry** | Facts a company must file to exist | Corporate, not clinical | Yes |
| **T5 — Company statement** | Whatever the clinic chooses to say | Liability only | Yes — **and it is all a patient has** |

On Days 87 and 88, T5 was excluded by design. Today it cannot be, because **T5 is the entire evidence base available to the person making the decision.** That inversion is the case study.

---

## 7. Company Overview

From [G], the statutory record establishes the following and nothing more:

- **GAUDIUM IVF AND WOMEN HEALTH LIMITED**, registered in Delhi, legal address at Janakpuri.
- LEI **894500Q78I5CP8ZLV929**, status **ISSUED**, entity status **ACTIVE**, LEI first registered in 2024 and last updated in 2026.
- CIN **U85100DL2015PLC278296**.
- A recorded previous legal name of **Gaudium IVF and Women Health Private Limited** — the entity converted from private limited to public limited.

From the company's own website [W]: a fertility clinic group describing **36** centres across **6** Indian states, with a founding narrative dated **2009**.

That is the complete verifiable picture. There is no revenue figure, no cycle count, no outcome figure, and no registry number in the public record.

---

## 8. Reading the CIN

Day 85 established GLEIF as a free route into Indian corporate registry data. Day 88 used it again. Day 89 uses it a third time, and the result **corrects something this series said yesterday**.

```
U 85100 DL 2015 PLC 278296
│ │     │  │    │   │
│ │     │  │    │   └── registration number
│ │     │  │    └────── company class: PUBLIC Limited Company
│ │     │  └─────────── year of incorporation: 2015
│ │     └────────────── state: Delhi
│ └──────────────────── NIC activity code: 85100 — HOSPITAL ACTIVITIES
└────────────────────── listing status: U = Unlisted
```

Two things here matter.

**First, the NIC code is a real one.** Day 85 found Eka Care at `U74999KA2020PTC141864` and Day 88 found Qure.ai at `U74999MH2016PTC283891` — both under **74999**, "Other professional, scientific and technical activities **n.e.c.**", the residual bucket. Day 88 drew the conclusion that "India's statutory company classification has no code for medical AI."

That conclusion was too broad, and Day 89 refines it. India's register **does** have health codes. Gaudium sits under **85100, Hospital activities**. The two AI companies landed in the residual bucket not because the register ignores health, but because the register classifies by **activity**, and writing software that reads medical images is not a hospital activity. `verify.py` records `india_register_does_have_a_health_code` as **True** and `day88_finding_refined_not_reversed` as **True**.

The sharper version of the finding is this: **a register that classifies by activity cannot see an industry defined by its technology.** Qure.ai and a hospital are not doing the same activity, and the register is right about that — which is precisely why it cannot tell you how many medical-AI companies India has.

**Second, PLC does not mean listed.** Gaudium is a **public limited company**, which in Indian company law brings heavier filing and governance requirements than a private limited. But the CIN still begins with **U** — unlisted. There is no exchange, no prospectus, no quarterly result, no analyst.

So Gaudium carries **more** company-law obligation than either Day 85's or Day 88's subject, and **less** disclosure that reaches the public than either. Company class and public visibility are different axes, and confusing them is the single easiest mistake to make when reading an Indian corporate record.

---

## 9. What Regulates This Business

| Regulator | Applies? | What it compels | What reaches the public |
|---|:---:|---|---|
| Securities regulator (SEBI) | **No** | — | — |
| Device regulator (CDSCO / FDA) | **No** | — | — |
| Company law (MCA) | **Yes** | Incorporation, filings, governance | Name, CIN, class, state, year |
| **ART (Regulation) Act 2021** | **Yes** | Registration; submission of service outcomes | **Nothing** |

Three of the four rows produce nothing a patient can use. The fourth produces the company's name and the year it was incorporated.

The ART Act row is the one this case study is about, and §18 takes it apart.

---

## 10. Business Model

| Element | What can be established from the public record |
|---|---|
| Revenue | **Not disclosed** |
| Pricing | **Not disclosed** |
| Cycles performed | **Not disclosed** |
| Patients treated | **Not disclosed** — the website says "thousands" |
| Funding | **Not disclosed** |
| Headcount | **Not disclosed** |
| Centres | **36**, across **6** states — company statement [W] |

Day 88's subject published everything about how well the product worked and nothing about the company. Day 89's publishes nothing about either.

That is not an accusation. There is no filing regime that would require any of it, and a private business is under no obligation to volunteer commercial information. It is simply the state of the record.

---

## 11. Problem Statement

Stated from the evidence:

> A couple deciding where to have IVF is choosing between providers on the basis of a number that, in most of the world, no one is required to publish, no one verifies, and which each provider is free to define for itself. The treatment is expensive, physically demanding, time-limited by biology, and emotionally loaded in a way that makes comparison shopping difficult even when the data exists. The decision is made once or a small number of times, so the buyer never develops expertise.

Every element of that paragraph makes the information asymmetry worse than in an ordinary market. A buyer who purchases repeatedly learns. A buyer who purchases once, under time pressure, on an emotionally overwhelming question, does not.

---

## 12. Jobs to Be Done

| Job | Who hires it | Alternative | "Done well" looks like |
|---|---|---|---|
| "Tell me whether this clinic is any good" | Prospective patient | Word of mouth, reviews, rankings | A live birth rate with a denominator and an n |
| "Tell me how it compares to the one across town" | Prospective patient | Guesswork | The same measure, defined the same way, for both |
| "Tell me what could go wrong" | Prospective patient | Nothing | Multiple-birth rate, adverse events |
| "Tell me if this add-on is worth it" | Prospective patient | The clinic's own page | Evidence grading with harms stated |
| "Tell me this clinic is lawfully registered" | Prospective patient | Corporate record | A registration number, verifiable |

**Row 5 is the only one the public record answers**, and only partly — the corporate record proves a company exists, not that a clinic is ART-registered. The other four are unanswered, and §29 shows they remain largely unanswered even where the regulator publishes.

---

## 13. User Personas

Two personas, both constructed from what the sources establish about who is deciding and what is in front of them. No invented quotes, no synthetic biographies.

---

## 14. Persona 1: The Person Choosing a Clinic

**Basis:** [R], [P], [W], and the audits at [L1] and [L2].

**Context.** Has been trying to conceive, has been referred or has self-referred, and is now choosing between providers. Will pay largely out of pocket. Is comparing on outcomes, price, distance, and whatever signal can be found.

**What they need.** One number, defined the same way across clinics, with the denominator stated and the sample size attached: *of patients like me who started a cycle here, what proportion took home a baby?*

**What they can get in India.** From the regulator: nothing. From the corporate record: that a company called Gaudium IVF and Women Health Limited exists, is registered in Delhi, was incorporated in 2015, and is an active public limited company. From the clinic: qualitative claims — "unequalled success rates", "high success rates" — and no percentage anywhere.

**What they will therefore use instead.** Rankings, awards, testimonials, referrals, and the impression made by a website. `verify.py` records `patient_can_look_up_a_clinic_outcome_in_india` as **False**.

---

## 15. Persona 2: The Clinic Operator

**Basis:** [L1], [L2], [L5].

**Context.** Runs a clinic in a market where competitors publish either nothing or self-defined figures. Genuinely may be good. Has real outcome data internally, because the registry requires submitting it.

**What they face.** If they publish an honest live birth rate per cycle started — the strictest and least flattering denominator — it will sit next to a competitor's pregnancy rate per embryo transfer, which is a larger number describing a smaller and more favourable population. A patient comparing the two sees a worse clinic.

**This is not hypothetical.** [L1] found UK clinics using **51 different outcome measures** across **53** clinics, and [L2] found that of **54** Brazilian clinics publishing a success rate, only **19** used their own data. In both markets, the honest operator's problem is real.

§51 is about what that does to the obvious recommendation.

---

## 16. User Journey: Choosing a Clinic in India

```
  Patient                  Sources available            What they get
     |                            |                          |
 [1] | "is this clinic good?"     |                          |
     |                            |                          |
 [2] |--> National ART Registry   |                          |
     |    registry.artsurrogacy   |--> LOGIN WALL ---------> | nothing
     |    .gov.in                 |    4 login roles,        |
     |                            |    0 public routes       |
     |                            |                          |
 [3] |--> Corporate record        |--> CIN, class, state --> | company exists
     |    (GLEIF / MCA)           |    year, LEI status      | (not clinical)
     |                            |                          |
 [4] |--> The clinic's website    |--> "unequalled success   | no number
     |                            |     rates", 36 centres,  |
     |                            |     awards, rankings     |
     |                            |                          |
 [5] |--> Rankings, reviews,      |--> third-party opinion   | not outcomes
     |    word of mouth           |                          |
     |                            |                          |
 [6] | DECIDES on [4] and [5]     |                          |
```

Step 2 is the one that should work. The data is there — the registry collects it. The wall is not a technical limitation; it is a design decision about who the registry is for.

---

## 17. User Journey: The Same Question in the United States

```
  Patient                  Sources available            What they get
     |                            |                          |
 [1] | "is this clinic good?"     |                          |
     |                            |                          |
 [2] |--> CDC ART Success Rates   |--> clinic-specific ----> | a live birth
     |    cdc.gov                 |    AND national rates    | rate, by age,
     |                            |    ~500 clinics          | with context
     |                            |    ~98% of all cycles    |
     |                            |    live births confirmed |
     |                            |    9-10 months after     |
     |                            |    year end              |
     |                            |                          |
 [3] | compares clinics on the    |                          |
     | same measure               |                          |
```

The difference between these two diagrams is not technology, wealth, or medical sophistication. It is a single clause in a statute passed in **1992**.

---

## 18. The Central Question

> **Does compelling a clinic to report its outcomes help the person choosing the clinic?**

Day 87 asked whether obligation beats choice and found that securities disclosure compels process rather than performance. Day 88 asked whether device regulation compels results and found that it does, for the indications it covers, in one population at a time.

Day 89 finds a third thing, and it is the one that should worry a product manager most:

**Obligation can compel collection without compelling publication, and when it does, the data exists, is complete, is in the regulator's hands, and is worth nothing to anyone outside it.**

India's ART Act created a registry that collects outcomes. Nothing about the resulting record reaches a patient. From the outside, a regime that collects everything and publishes nothing is indistinguishable from no regime at all — except that it costs clinics real compliance effort, and it creates the impression that someone is watching.

---

## 19. What the Registry Collects

The government's own description of the National ART & Surrogacy Registry [P] states it is "a online public record system of ART Clinics/Banks and Surrogacy Clinics in India" and a "Central Database of all the ART Clinics, Banks and Surrogacy Clinics in the country", holding "details of all the clinics and banks of the country including nature and types of services provided by them, **outcome of the services** and other relevant information."

Three phrases in that description deserve attention.

**"Public record system."** That is the registry describing itself as public.

**"Outcome of the services."** The outcomes are in scope. This is not a licensing database that happens to lack clinical data — it is a database that says it holds clinical outcomes.

**"Central Database."** One place, national coverage.

On paper, this is the architecture the CDC operates in the United States. The difference is entirely in what happens next.

---

## 20. What the Registry Publishes

The live registry portal [R], observed on 2026-09-27, presents:

- **Signup** for Clinics/Banks and for NOC Applicants.
- **Login** as Clinics/Banks, as NOC Applicants, as State Appropriate Authority, and as Officials — **4** roles.
- Instructions for clinics on how to register.

It presents **no** public search, **no** public clinic directory, and **no** outcome data. A `/search` path returns an error.

`verify.py` records:

| Check | Value |
|---|---|
| `registry_exists` | **True** |
| `registry_collects_outcome_of_services` | **True** |
| `registry_login_roles` | **4** |
| `registry_public_search_routes` | **0** |
| `registry_publishes_clinic_level_outcomes` | **False** |
| `registry_publishes_clinic_directory_publicly` | **False** |
| `patient_can_look_up_a_clinic_outcome_in_india` | **False** |

Every one of the four login roles is a role within the system — a clinic, an applicant, a state authority, an official. **The patient is not a role.**

That is the whole finding, and it is a product decision, not a legal one. Someone designed a registry and enumerated its users, and the person the registry exists to protect was not among them.

---

## 21. The Comparator That Publishes

The United States has required this since 1992.

The **Fertility Clinic Success Rate and Certification Act of 1992** requires fertility clinics performing ART to report annually to the CDC [C]. The resulting National ART Surveillance System covers approximately **500** clinics and an estimated **98%** of all ART cycles performed in the United States. Non-reporting clinics are named as non-reporters.

CDC then publishes **clinic-specific and national success rates**, calculated per ART cycle or per transfer, with live births confirmed approximately nine to ten months after the reporting year ends.

| | India | United States |
|---|---|---|
| Statute year | **2021** | **1992** |
| Registration compelled | **Yes** | Yes |
| Outcomes collected | **Yes** | Yes |
| Outcomes **published** | **No** | **Yes** |
| Clinic-level comparison possible | **No** | **Yes** |
| Non-reporters named | — | Yes |

**India's statute is 29 years newer and publishes less.**

The distinction that matters is between a **registration mandate** and a **publication mandate**. India compels clinics to register and to report. The United States compels the same — and then compels the agency to publish. `verify.py` records `us_mandate_includes_publication` as **True** and `india_mandate_includes_publication` as **False**.

One clause. Twenty-nine years apart.

---

## 22. The Mechanism, Named

Here is the general form, because it is not specific to fertility medicine and a product manager will meet it repeatedly:

> **A disclosure regime has two halves: who must report, and who may read. Regulators are reliably good at the first half, because it is enforceable against a small number of identifiable parties. The second half benefits a large, diffuse, unorganised group who were not in the room.**

Day 87 found securities regulation compelling a description of process instead of a result. Day 88 found device regulation compelling a result from one population. Day 89 finds health-service regulation compelling a result that reaches nobody.

In all three cases the regime did exactly what it was designed to do. In all three cases what it was designed to do was not what the reader needed.

---

## 23. What Happens Where the Regulator Does Publish

If publication were sufficient, the UK would be the counterexample. It has the Human Fertilisation and Embryology Authority, the oldest and strictest dedicated fertility regulator in the world, which publishes clinic-level data through a public "Choose a Fertility Clinic" service.

So: in the best-regulated fertility market on earth, what do clinics say on their own websites?

Wilkinson, Vail and Roberts audited exactly that [L1]. They identified clinics offering IVF using the HFEA's own service — **81** clinics, of which **2** had no website, leaving **79** analysed.

**53 of 79 (67.09%)** reported their performance.

Those 53 clinics used **51 different outcome measures.**

---

## 24. Fifty-One Measures, Fifty-Three Clinics

That ratio is **0.962** distinct measures per reporting clinic. To a first approximation, **every clinic invented its own definition of success.**

The breakdown:

| | Count |
|---|---:|
| Clinics analysed | 79 |
| Reporting any performance measure | **53 (67.09%)** |
| Reporting nothing | 26 (32.91%) |
| **Distinct outcome measures used** | **51** |
| Distinct ways of reporting **pregnancy** | **31** |
| Distinct ways of reporting **live birth** | **9** |
| Measures outside those two families | 11 |

There were **3.44 times** as many ways of reporting pregnancy as of reporting live birth. That is the more flattering measure attracting the greater inventiveness, and it is visible in the mix: **83%** of reporting clinics gave a pregnancy rate, **51%** gave a live birth rate — a **32.00 percentage point** gap in favour of the measure that counts something short of a baby.

The authors record that "it was usual for clinics to present results without relevant contextual information such as sample size, reporting period, the characteristics of patients and particular details of treatments."

So: a number, with no denominator you can check, no n, no period, and no description of who was counted. Fifty-one different such numbers.

Their conclusion: **"Binding guidance is required to ensure consistent, informative reporting."**

Publication by the regulator did not fix the clinic's own channel. It is not clear that anything short of binding guidance could.

---

## 25. The Harms Column

In the same audit, of **79** clinic websites:

**1 provided information on adverse events.**

That is **1.27%**. **98.73%** of UK fertility clinic websites said nothing about what can go wrong.

**11 (20.75% of reporters, 13.92% of all)** reported a multiple birth or multiple pregnancy rate — multiple pregnancy being the principal iatrogenic risk of IVF, and the thing single-embryo-transfer policy exists to reduce.

The ratio of clinics reporting success to clinics reporting harm is **53 to 1**.

A second study makes the same point from a different angle. van de Wiel and colleagues examined how UK clinics advertise three IVF add-ons [L3] — **87** clinics, **72** unique websites. Time-lapse imaging was advertised by **67%**, PGT-A by **47%**, assisted hatching by **28%**.

Websites stating that the add-on's effectiveness was in doubt: **4**, **2** and **1** respectively — **5.56%**, **2.78%** and **1.39%** of the 72.

Websites raising the possibility that an add-on might have **negative** effects: **0**.

Zero. Out of seventy-two. In the market with the HFEA.

And a third: Gürtin and Tiemann analysed the **top 15** UK clinics by egg-freezing volume, together **87.8%** of all UK egg freezing cycles from 2008 to 2017 [L6]. Their finding was that **none** adhered adequately to HFEA guidelines on advertising and information provision — **0.00%** adherence among the clinics doing the overwhelming majority of the work.

Guidance without enforcement produced zero adherence. That is not an argument against guidance; it is an argument about which half of a disclosure regime actually binds.

---

## 26. The Same Pattern Where There Is No Mandate

Carneiro and colleagues audited **161** fertility clinics registered with Brazil's SisEmbrio system [L2]. **153 (95.03%)** had working websites. **7 (4.35%)** were public clinics.

| | Count | Share of 161 |
|---|---:|---:|
| Published a success rate | 54 | **33.54%** |
| Used **their own data** | 19 | **11.80%** |
| Published rates by age | 7 | 4.35% |
| **Published a live birth rate** | **0** | **0.00%** |
| Showed a registered director | 49 | 30.43% |
| Showed patient photos | 85 | 52.80% |
| Advertised prices | 0 | 0.00% |

Two numbers on that table are worth stopping on.

**Of the 54 clinics that published a success rate, only 19 used their own data.** The other **35 — 64.81% of everyone publishing a success rate — were publishing someone else's numbers** on a page about their own performance. Whatever those figures were, they were not a measurement of that clinic.

**Not one of the 161 clinics published a live birth rate.** Zero. The single outcome that corresponds to what a patient is actually buying.

And **more clinics showed photographs of patients (85) than showed the name and registration of their own medical director (49)** — a ratio of **1.73** to 1. Emotional proof outranked credentialing proof by three-quarters.

---

## 27. The Denominator, Demonstrated

Why does "51 different measures" matter so much? Because the choice of measure moves the headline more than the quality of the clinic does.

Toftager and colleagues ran a randomised trial in **1,050** women, **1,023** of whom started treatment [L4]. It is an unusually clean demonstration because the same patients, in the same trial, generate two very different "success rates" depending only on what gets counted.

| Measure | Antagonist arm | Agonist arm |
|---|---:|---:|
| Live birth rate after the **first fresh transfer** | **22.8%** | 23.8% |
| **Cumulative** live birth rate including all frozen-thaw cycles from the same retrieval | **34.1%** (182/534) | 31.2% (161/516) |

Recomputed from the published counts, 182/534 is **34.08%** and 161/516 is **31.20%** — matching the reported figures.

**Same women. Same retrievals. 22.8% or 34.1%.**

A difference of **11.28 percentage points**, a multiple of **1.49**, and *neither number is wrong*. Both describe the same patients accurately. They answer different questions: "did this transfer work?" and "did this egg collection eventually produce a baby?"

Now put that next to [L1]'s finding that UK clinics used **9 different ways of reporting live birth** and **31 different ways of reporting pregnancy**. A clinic free to choose its own measure has, from a single honest dataset, a range of headline numbers at least this wide to pick from — before it has chosen which patients to include, which years to cover, or whether to report pregnancy instead of birth.

> **This is the mirror image of Day 87's lesson.** There, a ratio's denominator was a marketing asset and its numerator was a liability. In fertility, the *denominator is the product being sold*. Choose "per embryo transfer" and you have quietly excluded every patient who never reached transfer — the ones for whom treatment failed earliest and hardest.

---

## 28. What a Patient Actually Sees

Recorded from the company's own public website [W] on 2026-09-27, as a patient-facing artefact and **not** as evidence about clinical performance:

| Element | Present? |
|---|:---:|
| Any success rate **percentage** | **0** |
| Any denominator stated | **0** |
| Cycle counts | **0** |
| Live birth counts | **0** |
| Citations or data sources for outcome claims | **0** |
| ART registry number displayed | **0** |
| Qualitative success language | **Yes** — "unequalled success rates", "high success rates" |
| Centres | **36**, across **6** states |
| Founding year claimed | **2009** |
| Awards and rankings | Several, including one carrying a named source and year |

The pattern here is worth stating precisely, because it is easy to misread.

**Gaudium does not publish a misleading success rate. It publishes no success rate at all.** `verify.py` asserts `gaudium_publishes_a_misleading_success_rate` as **False** and `gaudium_breaks_any_disclosure_rule` as **False**.

That is lawful in India, and per [L2] it is close to the global norm — not one of 161 Brazilian clinics published a live birth rate either. The absence is structural, not particular.

It is worth noting one small thing carefully. The corporate record gives an incorporation year of **2015**; the website's founding narrative gives **2009**, a difference of **6** years. These are not in conflict — a medical practice can operate for years before the company that now runs it is incorporated, and conversions and restructurings are ordinary. `verify.py` records this as `year_difference_is_an_observation_not_a_contradiction` = **True**. It is recorded because a reader comparing the two records will notice it, and should know it has an innocent explanation.

---

## 29. What Can and Cannot Be Established

For **any** Indian IVF clinic, not just this one:

**Establishable** — 6 items, all from company law:
legal name · corporate identity number · state of registration · year of incorporation · company class · LEI status

**Not establishable** — 7 items, all clinical:
live birth rate · pregnancy rate · cycles performed · outcomes by age band · multiple birth rate · adverse events · how the clinic compares to any other clinic

**Everything a patient can establish is corporate. Nothing a patient can establish bears on whether the treatment works.** `verify.py` asserts both.

Of the thirteen things a patient might want to know, **53.85%** are clinical and none of those is available.

---

## 30. The Four-Market Ladder

Ranked by what the regulator **publishes**, not by what it collects:

| Market | Collects outcomes | Regulator publishes | Clinic's own channel standardised |
|---|:---:|:---:|:---:|
| United States | **Yes** | **Yes** | **No** |
| United Kingdom | **Yes** | **Yes** | **No** |
| Brazil | **Yes** | **No** | **No** |
| India | **Yes** | **No** | **No** |

- **100.00%** of these markets collect outcome data.
- **50.00%** publish it.
- **0.00%** have standardised what the clinic says on its own website.

That third column is the uncomfortable one. Publication by the regulator is necessary — the difference between the US and Indian patient journeys in §16 and §17 is entirely that column. But it is demonstrably **not sufficient**: the UK publishes, and still produced 51 measures across 53 clinics, one website in seventy-nine mentioning adverse events, and zero of the top fifteen adhering to guidance.

**Publication fixes what the regulator says. Only binding guidance fixes what the seller says.** No market in this table has done the second thing.

---

## 31. The Evidence Ledger

Five questions a patient would want answered, and what produced the answer.

| # | Question | Status | What compelled it |
|---|---|---|---|
| 1 | Does this clinic work? | **Not disclosed** | *Nothing* |
| 2 | How does it compare? | **Not disclosed** | *Nothing* |
| 3 | What are the risks? | **Not disclosed** | *Nothing* |
| 4 | Is it lawfully registered? | **Partial** | Company law |
| 5 | Who owns and runs it? | **Disclosed** | Company law |

- **1 of 5 (20.00%)** fully disclosed.
- **3 of 5 (60.00%)** not disclosed at all.
- **0** volunteered by the company.
- **Every answered row came from company law, not health law.**
- **No clinical row is answered.**

Set against the two preceding days:

| Day | Company | Ledger answered |
|---|---|---:|
| 87 | Tempus AI (public, securities-regulated) | **40.00%** |
| 88 | Qure.ai (private, device-regulated) | **60.00%** |
| **89** | **Gaudium IVF (neither)** | **20.00%** |

Day 88's ledger is **3.00 times** better answered than Day 89's. The private, unlisted, device-regulated company is the best-documented of the three; the clinical services business is the worst.

---

## 32. What Would Actually Fix This

Four interventions, ordered by who has to act and how much has to change.

| # | Intervention | Who acts | Precedent | Fixes |
|---|---|---|---|---|
| 1 | **Open the registry's public surface** — a directory and clinic-level outcomes | The ART authority | CDC, since 1992 | Rows 1 and 2 of the ledger |
| 2 | **Publish a national benchmark by age band** | The ART authority | CDC, HFEA | The §48 problem — an honest number gains something to be read against |
| 3 | **Bind the measure** — one definition, mandatory on clinics' own materials | The ART authority | Nowhere yet | The 51-measure problem |
| 4 | **Require harms alongside outcomes** | The ART authority | Nowhere yet | The 1-in-79 problem |

Every row names the same actor, and that is the finding rather than a coincidence.

Interventions 1 and 2 are **already solved problems** — the United States has done both since 1992 and the United Kingdom does both now. They require no new thinking, only the decision that the registry's readers include the public.

Interventions 3 and 4 have **no precedent anywhere**. No market in the four-country ladder has standardised what a clinic says on its own website, and none requires harms to be published beside outcomes. [L1]'s authors called for binding guidance in 2017; §25 records what the absence of it produced.

There is no row in this table a single clinic can execute alone. A clinic can display its registry number and it can fix its own measure — both are in §45 — but neither creates a directory, a benchmark, a standard, or a norm. **Three of the four fixes are public goods, and the fourth is a rule.** That is why §48 concludes the unit of intervention is the regulator.

---

## 33. Feature Analysis

Assessed as an information product — what the patient-facing surface offers.

| Capability | Present in India | Present in US | Present in UK |
|---|:---:|:---:|:---:|
| Public clinic directory | **No** | Yes | Yes |
| Clinic-level live birth rate | **No** | Yes | Yes |
| Outcomes by patient age | **No** | Yes | Yes |
| National benchmark to compare against | **No** | Yes | Yes |
| Non-reporting clinics identified | **No** | Yes | — |
| Standardised measure across clinics' own sites | **No** | **No** | **No** |
| Adverse event disclosure | **No** | **No** | **No** (1 of 79) |

The bottom two rows are blank everywhere. That is the frontier.

---

## 34. Competitive Analysis

The competitive dynamic here is unusual and worth drawing out, because it explains §48.

In a market where **no** competitor publishes a verifiable outcome, publishing one is not a differentiator — it is an **exposure**. The publishing clinic's number stands alone. There is no national benchmark to read it against, no competitor figure computed the same way, and no regulator-published average to say whether 34% is good.

A patient seeing one clinic's "live birth rate per cycle started: 31%" next to four clinics saying "unequalled success rates" does not conclude that the first clinic is honest. They conclude that the first clinic is 31%, and the others might be better.

| Competitive condition | Effect on honest disclosure |
|---|---|
| No regulator-published benchmark | An honest number has nothing to be read against |
| Competitors use self-defined measures | The strictest measure looks worst |
| Buyer purchases once, under stress | No expertise develops to correct the misreading |
| Emotional proof is available and cheap | Testimonials outcompete statistics |

[L2] quantifies the last row: **52.80%** of Brazilian clinics showed patient photographs, against **30.43%** showing their registered director.

---

## 35. Porter's Five Forces

| Force | Assessment | Evidence |
|---|---|---|
| **Buyer power** | **Very low** | One-time purchase, no comparable data, high emotional stakes, no repeat learning |
| **Rivalry** | **High but non-informational** | Competition on brand, rankings, awards — not on published outcomes |
| **Threat of new entrants** | **Moderate** | ART Act registration is a real barrier; clinical reputation takes time |
| **Supplier power** | Not establishable | No disclosure |
| **Substitutes** | **Moderate** | Adoption, other clinics, cross-border treatment |

The buyer power row is the analytically important one. Classical competitive analysis assumes buyers can evaluate. Here the buyer structurally cannot — and the market has organised itself around that fact rather than against it.

---

## 36. Business Model Canvas

| Block | Content |
|---|---|
| **Key partners** | Not disclosed |
| **Key activities** | ART cycles; clinical consultation; laboratory work; regulatory compliance |
| **Key resources** | 36 centres across 6 states [W]; clinical staff; ART registration |
| **Value propositions** | Fertility treatment; per [W], emphasis on complex and previously failed cases |
| **Customer relationships** | Consultation-led; not otherwise disclosed |
| **Channels** | Clinics; website; rankings and awards |
| **Customer segments** | Individuals and couples seeking fertility treatment |
| **Cost structure** | Not disclosed |
| **Revenue streams** | **Not disclosed** |

Five of nine blocks are "not disclosed". On Day 88 there were three, and that was noted as unusual. This is the least documented canvas in the series.

---

## 37. SWOT

**Strengths**
- Registered under a real healthcare NIC class (**85100**), not a residual code.
- Public limited company — heavier company-law governance than a private limited.
- **36** centres across **6** states [W] — real operational scale.
- Operating since at least incorporation in **2015**, with a founding narrative from **2009**.

**Weaknesses**
- **0** outcome figures published — no rate, no denominator, no n.
- **0** citations for outcome claims.
- No ART registry number displayed on the public site.
- Nothing published permits comparison with any other provider.

**Opportunities**
- Publishing a live birth rate per cycle started, by age band, with n, would make this the only Indian clinic a patient could evaluate — **if** the benchmark problem in §51 can be solved.
- Displaying the registry number is near-zero cost and immediately verifiable.
- The **51-measure** problem in [L1] is an unclaimed standard-setting position.

**Threats**
- If India's registry ever publishes, every clinic's numbers become comparable at once, with no transition period.
- Rankings and awards are a substitute signal that can be withdrawn or discredited.
- An audit of Indian clinic websites on the [L1]/[L2] model has not been published — but nothing prevents one, and the two that exist found what they found.

---

## 38. Metrics That Matter

| Metric | Why | Published by the clinic | Published by the regulator |
|---|---|:---:|:---:|
| Live birth rate per **cycle started** | The measure that matches what is bought | **No** | **No** |
| Live birth rate by **age band** | The single largest determinant of outcome | **No** | **No** |
| Cycles performed per year | Volume, and the denominator's denominator | **No** | **No** |
| **Multiple birth rate** | The principal iatrogenic harm | **No** | **No** |
| Adverse events | What can go wrong | **No** | **No** |
| Cancellation rate before transfer | Where "per transfer" figures hide failures | **No** | **No** |

Six rows, twelve cells, **zero** filled.

The last row deserves its own note: the gap between "per cycle started" and "per transfer" **is** the cancellation rate. A clinic reporting per transfer has removed from its denominator precisely the patients for whom things went worst. That is why §27's 22.8%-versus-34.1% demonstration matters, and why a measure without a denominator is not a measurement.

---

## 39. North Star and Guardrails

**North Star:** *Live births per 100 cycles started, by age band, published annually with n.*

That is deliberately the least flattering available formulation. It is also the only one that maps onto what a patient is buying: they are not buying a transfer, and they are not buying a positive pregnancy test.

**Guardrails:**

| Guardrail | Discipline |
|---|---|
| Denominator always stated | No rate published without "per what", the n, and the period |
| Age stratification mandatory | A pooled rate conceals the variable that matters most |
| Harms published alongside | Multiple birth rate and adverse events in the same table |
| Add-ons graded | Efficacy uncertainty stated where it exists; harms stated where known |
| No measure switching | The measure, once chosen, is not changed to flatter a year |

The last guardrail is the discipline this series has arrived at three times from three directions. Day 87: never publish the flattering half of a ratio without the unflattering half. Day 88: never publish a performance number without the population that produced it. Day 89: **never change the measure between reporting periods** — because with 51 measures available, drift is indistinguishable from improvement.

---

## 40. AARRR

| Stage | What is measurable publicly |
|---|---|
| **Acquisition** | Rankings, awards, search, referral — none outcome-based |
| **Activation** | First consultation — not disclosed |
| **Retention** | Repeat cycles — not disclosed, and ambiguous: a second cycle means the first failed |
| **Revenue** | Not disclosed |
| **Referral** | Testimonials; **52.80%** of Brazilian clinics used patient photos [L2] |

The retention row is a genuine analytical trap in this category and worth flagging for any PM entering it. In most businesses a repeat purchase is a success signal. In fertility treatment, a second cycle means the first one did not work. A naive retention metric would score a failing clinic as a high-retention one.

---

## 41. HEART

| Dimension | Signal | Publicly available? |
|---|---|:---:|
| **Happiness** | Patient experience | Testimonials only |
| **Engagement** | Cycles per patient | **No** |
| **Adoption** | New patients | **No** |
| **Retention** | Return for further cycles | **No** — and see §40 |
| **Task success** | **Live birth** | **No** |

Day 87's task-success row was empty for a $1.27bn-revenue company. Day 88's was the only full row. Day 89's is empty again — and here task success is a *baby*.

---

## 42. The Trust Substitutes

When outcome data is absent, the decision still gets made. Something fills the gap, and it is worth naming what.

From the Brazilian audit [L2], across 161 clinics:

| Signal | Clinics using it | Share |
|---|---:|---:|
| Patient photographs | 85 | **52.80%** |
| Published success rate of any kind | 54 | 33.54% |
| Registered medical director shown | 49 | **30.43%** |
| Success rate using the clinic's own data | 19 | 11.80% |
| Rates broken down by age | 7 | 4.35% |
| **Live birth rate** | **0** | **0.00%** |

The ordering is the point. **Photographs of patients outrank the medical director's registration by a ratio of 1.73 to 1**, and both outrank every form of outcome data. The signals that require no evidence are the most widely deployed; the signal that requires the most evidence is deployed by nobody.

This is not clinics behaving cynically. It is a market allocating effort to the signals that work, and in a category where the buyer cannot verify an outcome, an emotionally legible signal genuinely does work better than a statistic they cannot contextualise.

Gaudium's own public pages [W] sit in the same pattern: awards, rankings, a founding narrative, scale figures — **36** centres across **6** states — and **0** outcome percentages. Every element present is one a reader can absorb without a denominator.

The transferable observation for a product manager: **trust substitutes are not a marketing failure, they are a demand signal.** People reach for testimonials because they need a basis for confidence and have been given none. Supplying a real basis does not compete with the substitutes on their own terms — which is exactly the trap §48 describes.

---

## 43. Kano

| Feature | Category | Reasoning |
|---|---|---|
| ART registration | **Must-be** | Unregistered operation is unlawful |
| Clinical competence | **Must-be** | Assumed, unverifiable by the buyer |
| Published live birth rate by age | **Attractive** | Nobody does it; the first mover defines the category |
| Published multiple birth rate | **Attractive** | 13.92% of UK clinics; effectively unheard of elsewhere |
| Adverse event disclosure | **Indifferent → Attractive** | 1 of 79 UK websites; patients do not yet expect it |
| Registry number on the website | **Indifferent** | Cheap, verifiable, nobody asks |

The third row is where Day 88's Kano table also pointed. Categories migrate: the first company to publish a stratified, honest outcome rate converts it into a Must-be for everyone else — and captures the differentiation on the way through.

---

## 44. What a PM Should Take From This

**1. A disclosure regime has two halves, and only one of them is usually built.** "Who must report" is enforceable against a small number of identifiable parties. "Who may read" benefits a diffuse group who were not in the room. India's ART registry enumerated **4** login roles — clinic, applicant, state authority, official — and the patient was not one of them. **When you design any system that collects data on behalf of users, check whether the user is in the role list.**

**2. Collection without publication is indistinguishable from nothing — and costs more.** Clinics bear real compliance effort. The public gets no benefit. The only thing produced is the *impression* that someone is watching, which is worse than transparent absence because it discourages the search for alternatives.

**3. The denominator is the product.** Same trial, same women: **22.8%** per fresh transfer or **34.1%** cumulative. Neither is false. When a seller is free to choose the measure, they are choosing the number, and 53 UK clinics chose **51 different ones**. Ask "per what, out of how many, over what period" before you read any rate — and notice that "per transfer" has already removed the patients for whom things went worst.

**4. Publication by the regulator is necessary and not sufficient.** The UK publishes clinic-level data and still produced 51 measures across 53 clinics, **1 of 79** websites mentioning adverse events, **0 of 72** mentioning add-on harms, and **0 of 15** top clinics adhering to guidance. Fixing the regulator's channel does not fix the seller's channel. Only binding guidance does.

**5. Watch for markets where the buyer cannot develop expertise.** One-time purchase, high emotional load, time pressure, no comparable data. Ordinary competitive dynamics do not apply, because the correcting mechanism — buyers learning — never runs. In those markets, information asymmetry is not a temporary friction. It is the equilibrium.

---

## 45. Product Recommendations

Four, each addressing a documented gap.

**P1 — Publish live birth rate per cycle started, by age band, with n and period.**
*Gap:* §38. Zero of twelve metric cells are filled.
*Change:* One table, updated annually: age band, cycles started, live births, rate, and the reporting period. Per cycle started, not per transfer.
*Why it matters:* It is the only number that answers what a patient is buying, and no Indian clinic publishes it.

**P2 — Display the ART registry number on every page.**
*Gap:* §28. No registration number appears on the public site.
*Change:* Registration number in the footer, alongside the medical director's name and registration.
*Why it matters:* Near-zero cost, immediately verifiable, and [L2] found only **30.43%** of Brazilian clinics showed a registered director against **52.80%** showing patient photos.

**P3 — Adopt and publish a standard reporting template.**
*Gap:* §24. 51 measures across 53 clinics.
*Change:* Commit publicly to a fixed measure set — per cycle started, by age, with n — and do not change it between periods.
*Why it matters:* [L1]'s authors concluded binding guidance is required. A clinic can bind itself first.

**P4 — Publish multiple birth rate and adverse events.**
*Gap:* §25. **1 of 79** UK websites mentioned adverse events; **0 of 72** mentioned add-on harms.
*Change:* Harms table published beside the outcomes table.
*Why it matters:* It is the disclosure no competitor anywhere makes.

---

## 46. RICE Prioritisation

**Definitions.** Reach is ordinal 1–10 with the anchor stated. Impact 0.25/0.5/1/2/3. Confidence 0–1. Effort in person-months. RICE = (R × I × C) / E.

| | Reach | Reach anchor | Impact | Conf. | Effort | **RICE** |
|---|---:|---|---:|---:|---:|---:|
| **P1** Live birth rate by age | 9 | Every prospective patient choosing a clinic | 3.0 | 0.85 | 1.00 | **22.95** |
| **P2** Registry number displayed | 4 | Patients verifying the clinic is lawfully registered | 1.0 | 0.95 | 0.25 | **15.20** |
| **P3** Standard reporting template | 7 | Patients comparing clinics; the whole market | 2.0 | 0.60 | 3.00 | **2.80** |
| **P4** Harms published | 6 | Patients weighing risk, especially multiple birth | 2.0 | 0.75 | 1.50 | **6.00** |

**Base ranking: P1 (22.95) → P2 (15.20) → P4 (6.00) → P3 (2.80).** Spread: **20.15**.

P1 leads. It answers the central question, it costs one person-month, and the data already exists internally because the registry requires submitting it.

---

## 47. The Stress Test

Each proposal meets the constraint that actually binds it.

| | Binding constraint | C mult. | E mult. | **Stressed** | Decay |
|---|---|---:|---:|---:|---:|
| **P1** | With no published national benchmark, an honest number stands alone against competitors' self-defined ones; needs defending patient by patient, forever | **0.10** | **7.00** | **0.33** | **−98.57%** |
| **P2** | Document control; a footer change | 0.95 | 1.20 | **12.03** | −20.83% |
| **P3** | Requires internal agreement on a measure and giving up the option to change it | 0.80 | 1.40 | **1.60** | −42.86% |
| **P4** | Publishing harms invites the question no competitor has to answer | 0.55 | 2.00 | **1.65** | −72.50% |

**Stressed ranking: P2 (12.03) → P4 (1.65) → P3 (1.60) → P1 (0.33).**

**P1 goes from first to last.** The reversal is total and asserted programmatically — `p1_leads_base` and `p1_ranks_last_under_stress` are both hard assertions in the gate. The field compresses from a spread of **20.15** to **11.71**.

---

## 48. Why P1 Dies — And Why This Time Is Different

This is the third consecutive day the stress test has killed the cheapest, most obviously correct recommendation. On Day 87 the mechanism was legal exposure; on Day 88 it was competitive disarmament. Both times, the property that made the disclosure valuable to the reader was the property that made it unsurvivable for the publisher.

Day 89's mechanism is different, and it is the most important of the three, because **it identifies who can actually fix it.**

P1 decays **98.57%**. The constraint is not cost — it is one person-month, and the data already exists. The constraint is that **an honest number published alone has nothing to be read against.**

On Day 88, a vendor publishing a specificity range faced competitors publishing point estimates. Bad, but at least the numbers were the same *kind* of thing. Here, a clinic publishing "live birth rate per cycle started, age 35–37: 31%, n=284" is competing against "unequalled success rates" and against a competitor's "70% success rate" that might mean pregnancy per transfer in a selected cohort.

There is no national average. There is no regulator-published benchmark. There is nothing that tells a patient whether 31% is good, bad, or excellent for that age band.

**So the honest clinic does not look honest. It looks like a 31% clinic.**

And that produces the conclusion this case study exists to reach:

> **The reason no clinic publishes is that the regulator does not publish.** A benchmark is a public good. No individual seller can create one, because a benchmark composed of one participant is not a benchmark — it is just that participant's number, standing alone and unflattering.

This is why P1 cannot be fixed by exhorting clinics to be more transparent, and why every "clinics should be more transparent" recommendation in this category has failed for thirty years. The unit of intervention is wrong. **The fix is a publication mandate on the regulator, not a disclosure norm for the seller** — `verify.py` records `the_fix_is_a_publication_mandate_on_the_regulator` as **True**.

The United States worked this out in 1992.

---

## 49. MoSCoW

| | Item | Rationale |
|---|---|---|
| **Must** | Display the registry number (P2) | Highest stressed score; near-zero cost; immediately verifiable |
| **Must** | Fix an internal measure and stop changing it | Costs nothing externally; prevents drift being read as improvement |
| **Should** | Publish harms (P4) | Survives stress better than P1; genuinely unclaimed |
| **Should** | Adopt a standard template (P3) | Standard-setting position available |
| **Could** | Publish live birth rate by age (P1) | Correct on the merits; needs a benchmark to survive, per §48 |
| **Won't** | Financial disclosure | No obligation, no mechanism, no path |

P1 moves from first on base RICE to "Could" — not because it is wrong, but because MoSCoW is an execution framework and §48 is about execution.

---

## 50. Roadmap

**Horizon 1 — immediate**
- Registry number and medical director registration on every page (P2).
- Fix the internal outcome measure; record it; stop changing it.

**Horizon 2 — within four quarters**
- Publish multiple birth rate alongside any outcome claim (P4).
- Commit publicly to a fixed reporting template (P3).
- Grade any advertised add-on for evidence and state harms where known.

**Horizon 3 — conditional**
- Publish live birth rate per cycle started by age band with n (P1) — **conditional on a published national benchmark existing**, or on a credible multi-clinic commitment to publish on the same basis simultaneously.

The conditionality in Horizon 3 is the honest output of §48, not a hedge. A single clinic publishing alone is worse off; several publishing together on one definition are not.

---

## 51. Risks

| Risk | Basis | Severity |
|---|---|---|
| **Unevaluable market** | 0 of 12 metric cells filled; patient decides on brand | **Structural** |
| **Measure drift** | 51 measures exist [L1]; nothing prevents switching | **High** |
| **Harms invisible** | 1 of 79 UK sites; 0 of 72 on add-ons | **High** |
| **Benchmark absence** | No national average published in India | **High** |
| **Regulatory switch-on** | If the registry publishes, all clinics become comparable at once | **Moderate** |
| **Third-party ranking dependence** | Awards and rankings substitute for outcome data | **Moderate** |

The last row is a genuine strategic exposure. Where outcome data is absent, ranking and award signals carry the differentiation — and those are controlled by third parties, can be discredited, and can be withdrawn.

---

## 52. Open Questions

1. What is Gaudium's live birth rate per cycle started, by age band? **Unknown, and unknowable from the public record.**
2. Why does India's registry not publish, when its own description calls it a "public record system"?
3. Has any audit of Indian fertility clinic websites on the [L1]/[L2] model been published? None was found.
4. Would a benchmark alone be enough, or does the clinic's own channel need binding guidance too? [L1] and [L6] suggest the second.
5. How many ART clinics are registered in India? The registry holds the number; it does not publish it.
6. Does the 2009-versus-2015 year difference reflect a predecessor practice, a restructuring, or something else? Both records can be correct.
7. If a single clinic did publish honestly, would it lose business — or would it win on trust? §48 argues the first. It is an argument, not a measurement.

Question 7 is the one that would settle §48, and nothing in the public record answers it.

---

## 53. Method Notes

**What was done.** The corporate record came from the GLEIF API. The registry's self-description came from the government portal; its actual public surface was established by fetching the live registry portal and observing what it exposes. The US comparator came from CDC. All literature came from PubMed.

**Two sources could not be obtained.** The full text of the ART (Regulation) Act 2021 was not read. `indiacode.nic.in` returned HTTP 504 on repeated attempts and is disallowed to the fetching tool; `egazette.nic.in` is outside this environment's egress allowlist. **This case study therefore makes no claim about what the Act's sections say.** Every statement about the Act's effect is sourced to the government portal's description of the registry or to the live portal's behaviour, never to the statute. `verify.py` records `art_act_text_was_read_in_full` as **False**. This is a material limitation and Part 4 of `ASSUMPTIONS.md` treats it fully.

**What "the registry publishes nothing" means, precisely.** It means the portal exposes no public search, directory, or outcome page to an unauthenticated visitor, and that `/search` errors. It does **not** mean no such data exists behind the login, and it does not mean no publication is planned. `verify.py` records `registry_content_behind_login_was_accessed` as **False**.

**Tier 5 was used deliberately.** Days 87 and 88 excluded company statements entirely. Today the company's own website is examined, because it is the only source a patient has. It is recorded as a patient-facing artefact and never as evidence of performance.

**On naming a private company.** The findings from [L1], [L2], [L3] and [L6] concern UK and Brazilian clinics and are **not** transferred onto Gaudium; the gate asserts this as a negative control. What is recorded about Gaudium is what its own public pages contain, stated factually, plus its corporate record.

**The gate passed on the first run.** 242 checks, zero failures — the first day in this arc where no hand-stated expectation was wrong. That is recorded as an observation, not a boast: today's arithmetic is mostly ratios of small integers, which is exactly the arithmetic least prone to the rounded-intermediate trap that caught Days 82, 86, 87 and 88.

**Diagram standard.** Markdown tables and ASCII only. Mermaid was dropped at Day 50.

---

## 54. Series Position

Day 89 closes the regulatory arc.

| Day | Company | Regulator | What it compelled |
|---|---|---|---|
| 87 | Tempus AI | Securities (SEC) | **Process**, not performance — 0 algorithm metrics |
| 88 | Qure.ai | Device (FDA) | **Performance** — 5 of 9 clearances (55.56%), one population each |
| 89 | Gaudium IVF | Health service (ART Act) | **Collection**, not publication — 0 figures reach the public |

Three companies, three regulators, three different answers to the same question.

The arc's hypothesis was whether obligation beats choice. The answer across eight days is: **obligation produces whatever the obliging body was built to care about, and nothing else.**

The SEC cares whether investors are misled, and produced a beautiful description of method with no result in it. The FDA cares whether a device matches its predicate, and produced sensitivity and specificity from a single test set. India's ART authority cares whether clinics are registered and compliant, and produced a complete national outcome database that no patient can open.

None of the three cares whether the person at the end of the chain can make a decision. On Day 88 that gap was filled anyway, by thirteen research teams in Dhaka, Cape Town and Lima who measured a product because they wanted to know. Day 89 has no such teams — there is no published audit of Indian fertility clinic websites at all.

**When neither obligation nor choice nor independent curiosity produces the evidence, there is no fourth mechanism.** The patient decides on a website.

---

## 55. What Comes Next

**Tomorrow is Day 90: Health in ChatGPT** — and it is the right ending, because it removes the last piece of machinery.

A general-purpose conversational system used for health questions has no device clearance for any indication, no securities disclosure tied to clinical performance, no registry, no clinic-level outcome data, and no indication-specific evidence base. It is also, plausibly, where a large share of the people in §11 — the ones who cannot evaluate a clinic — now take their questions first.

After eighty-nine days of asking what compels evidence, the final case asks what happens when **nothing does**, and the thing answering is used by more people than every product in this series combined.

---

## 56. Limitations In One Place

- **The ART Act text was not read.** Two primary routes failed. No claim about the statute's sections is made.
- **The registry's login-gated content was not accessed.** "Publishes nothing publicly" is a statement about the public surface only.
- **No Indian clinic audit exists.** The [L1]/[L2]/[L3]/[L6] findings are from the UK and Brazil and do not transfer.
- **One company, one market.** The §44 lessons are supported by this case and by contrast with Days 82–88, not by a sample.
- **Website observation is point-in-time.** [W] as observed on 2026-09-27; websites change.
- **This is not a clinical assessment.** Nothing here bears on the quality of care at any clinic.
- **Financials are absent, not searched-for-and-missing.** No route used here reaches them.

---

## 57. Anyone Can Check This

```bash
# The corporate record
curl "https://api.gleif.org/api/v1/lei-records/894500Q78I5CP8ZLV929"

# The registry's public surface — observe what a patient can reach
curl -sSL "https://registry.artsurrogacy.gov.in" | grep -io "login\|signup\|search"

# The US comparator
open "https://www.cdc.gov/art/success-rates/index.html"
```

The gate and cross-check in this folder reproduce every number above from these inputs and the cited literature.

---

## 58. Verification

`verify.py` — **242 checks, all passing**, written and passing before the first sentence of this README existed.

Coverage: identity and registration; the registry that collects and does not publish; the comparator that does publish; what clinics publish when nobody makes them; the same pattern in an unmandated market; what is left out; the denominator demonstrated; what a patient actually sees; the four-market ladder; the evidence ledger; RICE and stress; series continuity; negative controls; counter-examples.

`crosscheck.py` confirms every two- and three-decimal figure in `README.md` and `ASSUMPTIONS.md` traces to a value asserted in the gate.

---

## 59. Eleven Negative Controls

Asserted **False** in the gate so no sentence can quietly imply them:

`gaudium_publishes_a_misleading_success_rate` · `gaudium_breaks_any_disclosure_rule` · `this_case_study_measures_gaudium_clinical_quality` · `uk_or_brazil_findings_apply_to_gaudium` · `indian_clinics_were_audited_here` · `art_act_text_was_read_in_full` · `registry_content_behind_login_was_accessed` · `any_gaudium_outcome_figure_is_known` · `company_financials_known` · `day89_uses_mermaid` · `day89_fabricates_any_figure`

The first four exist because the easiest way to write this case study badly would be to let audits of other countries' clinics bleed into claims about a named Indian company. The next three exist because the ART Act and the registry's interior were not accessible, and a reader must know the difference between "does not publish" and "was not reached".

---

## 60. A Note on Fairness

It would be possible to write this case study as an exposé of a fertility clinic that markets with superlatives and publishes no data. That version would be easy, would perform better, and would be wrong.

Wrong because the audits show the behaviour is structural: **0 of 161** Brazilian clinics published a live birth rate, **53 of 79** UK clinics used **51 different measures**, **0 of 15** top UK egg-freezing clinics adhered to their own regulator's guidance. A clinic that publishes no number in a market where publishing an honest one is punished is behaving rationally.

And wrong because it would aim the recommendation at the wrong party. §48 shows that the intervention that works is a publication mandate on the regulator. Blaming individual sellers for not solving a public-goods problem is how thirty years of "clinics should be more transparent" produced a market where one website in seventy-nine mentions what can go wrong.

---

## 61. The Numbers That Matter Most

| | |
|---|---:|
| Distinct outcome measures used by 53 UK clinics | **51** |
| UK clinic websites mentioning adverse events | **1 of 79 — 1.27%** |
| UK clinic websites mentioning add-on harms | **0 of 72 — 0.00%** |
| Top UK egg-freezing clinics adhering to HFEA guidance | **0 of 15 — 0.00%** |
| Brazilian clinics publishing a live birth rate | **0 of 161 — 0.00%** |
| Brazilian success-rate publishers using their own data | **19 of 54 — 35.19%** |
| Headline swing from one dataset, by measure choice | **22.8% → 34.1%** |
| Public outcome figures for any Indian clinic | **0** |
| Login roles in India's ART registry | **4** — none of them the patient |

---

## 62. Business Model of the Information Gap

Worth stating explicitly, because it is the transferable structure.

The gap is not an accident anyone profits from deliberately. It is sustained by four forces that each act independently:

1. **The regulator** optimises for compliance, not for readership.
2. **The clinic** faces a competitive penalty for unilateral honesty (§48).
3. **The patient** buys once, under time pressure, and never develops expertise.
4. **Third-party signals** — rankings, awards, testimonials — are cheap to produce and fill the vacuum.

Remove any one and the others still hold. Remove force 1 — make the regulator publish — and force 2 collapses, because a benchmark exists and honesty stops being unilateral. That is why §48 identifies the regulator as the load-bearing element, and why the US fix was a clause about publication rather than a code of conduct for clinics.

---

## 63. If You Are Building In This Category

Six checks, from this case and the seven before it:

1. **Is the user in the role list?** India's registry has 4 roles and the patient is not one.
2. **Does your regulator publish, or only collect?** The answer changes what your honest disclosure is worth.
3. **Can your buyer learn from repeat purchase?** If not, asymmetry is the equilibrium, not a friction.
4. **What is your denominator, and what does it exclude?** "Per transfer" excludes everyone who never reached transfer.
5. **Would your best number survive being published next to a competitor's best number?** If not, you need a benchmark, not a disclosure policy.
6. **Who benefits from the data you collect?** If the answer is only you and the regulator, you have built India's registry.

---

## 64. References

**Registry, corporate and government sources**, all retrieved 2026-09-27.

1. **[G]** GLEIF. LEI record 894500Q78I5CP8ZLV929, GAUDIUM IVF AND WOMEN HEALTH LIMITED. `https://api.gleif.org/api/v1/lei-records/894500Q78I5CP8ZLV929`
2. **[R]** National ART & Surrogacy Registry portal. `https://registry.artsurrogacy.gov.in`
3. **[P]** National ART & Surrogacy Portal, Department of Health Research, Ministry of Health & Family Welfare. `https://artsurrogacy.gov.in`
4. **[C]** US Centers for Disease Control and Prevention. National ART Surveillance System and ART Success Rates. `https://www.cdc.gov/art/php/nass/index.html` and `https://www.cdc.gov/art/success-rates/index.html`
5. **[W]** Gaudium IVF public website, home and `/about`. `https://www.gaudiumivfcentre.com`

**Peer-reviewed literature.** According to PubMed:

6. **[L1]** Wilkinson J, Vail A, Roberts SA. Direct-to-consumer advertising of success rates for medically assisted reproduction: a review of national clinic websites. *BMJ Open* 2017;7(1):e012218. PMID 28082363. DOI [10.1136/bmjopen-2016-012218](https://doi.org/10.1136/bmjopen-2016-012218)
7. **[L2]** Carneiro MM, Koga CN, Mussi MCL, Fradico PF, Ferreira MCF. Quality of information provided by Brazilian Fertility Clinic websites: Compliance with Brazilian Medical Council (CFM) and American Society for Reproductive Medicine (ASRM) Guidelines. *JBRA Assist Reprod* 2023;27(2):169-173. PMID 35916465. DOI [10.5935/1518-0557.20220026](https://doi.org/10.5935/1518-0557.20220026)
8. **[L3]** van de Wiel L, Wilkinson J, Athanasiou P, Harper J. The prevalence, promotion and pricing of three IVF add-ons on fertility clinic websites. *Reprod Biomed Online* 2020;41(5):801-806. PMID 32888824. DOI [10.1016/j.rbmo.2020.07.021](https://doi.org/10.1016/j.rbmo.2020.07.021)
9. **[L4]** Toftager M, Bogstad J, Løssl K, Prætorius L, Zedeler A, Bryndorf T, Nilas L, Pinborg A. Cumulative live birth rates after one ART cycle including all subsequent frozen-thaw cycles in 1050 women. *Hum Reprod* 2017;32(3):556-567. PMID 28130435. DOI [10.1093/humrep/dew358](https://doi.org/10.1093/humrep/dew358)
10. **[L5]** Tank J, Kotiswaran P, Tank P, Tank D, Tank J. Voices from Health Care Providers: Assessing the Impact of the Indian Assisted Reproductive Technology (Regulation) Act, 2021 on the Practice of IVF in India. *J Obstet Gynaecol India* 2023;73(4):301-308. PMID 37701091. DOI [10.1007/s13224-023-01815-2](https://doi.org/10.1007/s13224-023-01815-2)
11. **[L6]** Gürtin ZB, Tiemann E. The marketing of elective egg freezing: A content, cost and quality analysis of UK fertility clinic websites. *Reprod Biomed Soc Online* 2020;12:56-68. PMID 33336090. DOI [10.1016/j.rbms.2020.10.004](https://doi.org/10.1016/j.rbms.2020.10.004)

Literature identified via PubMed.

**Assumptions, source conflicts, and limitations:** see `ASSUMPTIONS.md`.

---

## 65. Closing Note

Eight days ago this series started asking whether being compelled to disclose produces better evidence than choosing to.

The answer has turned out to be a question about who is doing the compelling. A securities regulator produced a description of method with no result in it. A device regulator produced a result from one population. A health regulator produced a national database of outcomes that the people those outcomes describe cannot open.

Every one of those regimes works. Each does precisely what it was built to do.

None of them was built for the person at the end.

A couple in Delhi choosing where to spend a large amount of money and a limited number of years has, in front of them: a company registration number, an award, a ranking, a testimonial, and the phrase "unequalled success rates". The number that would actually help them exists. Their clinic submitted it. It is in a government database, behind a login screen with four roles, none of which is theirs.

**That is not a failure of transparency. It is a failure of product design, in a system nobody thought of as a product.**

---

*Day 89 of 90. Written by Gaurav Singh. Sources are primary and cited. Figures are computed, not asserted. Where the record is silent, this document says so — and where a source could not be reached, it says that too.*
