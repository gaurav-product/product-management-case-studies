# Day 89 — Gaudium IVF: Assumptions, Conflicts, and Limitations

Companion to `README.md`. Every judgement that is not itself a primary-source fact, every place the sources disagree or fall silent, and every thing a reader should not conclude.

Five parts:

1. **Assumptions** — judgements made where the evidence did not decide
2. **Source conflicts** — where sources disagree, and how each was resolved
3. **Absences** — what the record does not contain, stated as findings
4. **Limitations** — what this case study cannot support
5. **Verification record** — what the gate checks and what it asserts is false

---

## Part 1 — Assumptions

### 1.1 "The registry publishes nothing" means the public surface only

**Assumption:** India's National ART & Surrogacy Registry publishes no clinic-level outcome data and no public clinic directory.

**Basis:** the live portal at `registry.artsurrogacy.gov.in`, fetched 2026-09-27, presents signup and login for four roles — Clinics/Banks, NOC Applicants, State Appropriate Authority, Officials — plus registration instructions. A `/search` path returns an error. No public directory, search, or outcome page was found.

**What this claim covers.** The surface reachable by an unauthenticated visitor on one day.

**What it does not cover.** Whether such data exists behind the login; whether publication is planned; whether some other government page republishes registry content. `verify.py` records `registry_content_behind_login_was_accessed` as **False**.

**Confidence:** high for the claim as scoped. The distinction between "does not publish publicly" and "does not hold" is maintained throughout §20 of the README, and the README states it explicitly.

**What would change it.** A public outcome page existing on a path not tried, or a publication launched after the observation date. Both are possible and neither would make the observation wrong on its date.

### 1.2 The UK implied counts are reconstruction

**Assumption:** approximately 44 of the 53 reporting UK clinics gave a pregnancy rate and approximately 27 gave a live birth rate.

**Basis:** [L1] reports these as percentages of the 53 reporters — 83% and 51% — not as counts.

**The judgement involved.** Multiplying a rounded percentage by 53 gives **43.99** and **27.03**. These are reconstructions from published percentages, not the paper's own counts, and the true counts are whatever integers the authors rounded from — almost certainly 44 and 27.

**How this is handled.** The README quotes the **percentages**, which are the paper's own figures. The reconstructed values are gated so that the arithmetic is traceable, and are labelled here. No argument depends on them.

### 1.3 "51 measures across 53 clinics" is read as near-universal idiosyncrasy

**Assumption:** the ratio of 51 distinct outcome measures to 53 reporting clinics — **0.962** — supports the statement that "to a first approximation, every clinic invented its own definition of success."

**The judgement involved.** The ratio does not establish a one-to-one mapping. It is arithmetically possible for a handful of clinics to share two or three common measures while a long tail each uses something unique, producing the same ratio. The paper does not publish the distribution.

**Why the reading survives.** Whatever the distribution, 51 distinct measures among 53 reporters means comparison across clinics is impossible for almost any pair chosen at random, which is the claim the README actually makes. The phrase "to a first approximation" is doing real work and is not decorative.

### 1.4 The denominator demonstration uses one arm of one trial

**Assumption:** the swing from **22.8%** to **34.1%** in [L4] is a fair illustration of how much the choice of outcome measure moves a headline.

**The judgement involved.** This is one RCT, in two Danish public fertility clinics, in women under 40, with day-2 single embryo transfer planned. The magnitude of the fresh-versus-cumulative gap depends on freezing policy, embryo yield, and patient age, and would differ elsewhere.

**What is claimed and what is not.** The README claims that choosing the outcome changes the headline, that neither number is wrong, and that both describe the same patients. It does **not** claim that 11.28 percentage points is the typical gap, or that any specific clinic's numbers would move by that amount.

**Why this study.** It is unusually clean: the comparison is within one trial, both figures are published by the same authors for the same women, and the cumulative figures carry their numerators and denominators (182/534, 161/516) so they can be recomputed. `verify.py` recomputes both and confirms they match the reported values to one decimal place.

### 1.5 Transferring audit findings across countries

**Assumption:** UK and Brazilian clinic-website audits are relevant to a case study about an Indian clinic.

**The judgement involved.** They are relevant to the **market structure** argument and not to Gaudium. Three uses are made of them, and each is scoped:

| Use | Scope |
|---|---|
| Publication by a regulator does not standardise the clinic's own channel | UK — a market where the regulator does publish |
| Clinics publish success rates without their own data | Brazil — a market where the regulator does not |
| Harms are near-universally omitted | UK, both audits |

**What is explicitly not done.** No finding from [L1], [L2], [L3] or [L6] is applied to Gaudium. `verify.py` asserts `uk_or_brazil_findings_apply_to_gaudium` as **False** and `indian_clinics_were_audited_here` as **False**.

**The honest weakness.** No equivalent audit of Indian fertility clinic websites was found. The README says so in §50 and treats it as an open question rather than assuming Indian clinics resemble Brazilian ones.

### 1.6 Observing a named private company's website

**Assumption:** recording what Gaudium's public pages do and do not contain is legitimate and proportionate.

**The reasoning.** On Days 87 and 88 company statements were excluded entirely, because the question was what compulsion produces. Today the company's own channel **is** the object of study, because it is the only source available to the person making the decision. Excluding it would mean writing a case study about an information gap while refusing to look at the only thing in the gap.

**The constraints applied.**

- Only presence and absence of specific elements is recorded — percentages, denominators, counts, citations, registration numbers.
- The observation is labelled a patient-facing artefact, never evidence of performance.
- No inference is drawn about clinical quality. `verify.py` asserts `this_case_study_measures_gaudium_clinical_quality` as **False**.
- Lawfulness is affirmed, not merely left unstated: `gaudium_breaks_any_disclosure_rule` is **False** and `gaudium_publishes_a_misleading_success_rate` is **False**.
- §58 of the README states the fairness reasoning in the open rather than leaving it to this document.

### 1.7 The 2009 / 2015 year difference

**Assumption:** the difference between the founding year on the website (**2009**) and the incorporation year in the CIN (**2015**) is an observation, not a contradiction.

**Basis:** a medical practice can operate for years before the company that now runs it is incorporated; restructurings, conversions and group reorganisations are ordinary. GLEIF also records a previous legal name ending "PRIVATE LIMITED", confirming at least one corporate change.

**Why it is recorded at all.** A reader comparing the two records will notice a six-year gap and may over-read it. Recording it with its innocent explanation is more honest than omitting it. `verify.py` asserts `year_difference_is_an_observation_not_a_contradiction` as **True**.

### 1.8 Refining the Day 88 NIC finding

**Assumption:** Day 88's statement that "India's statutory company classification has no code for medical AI" was too broad, and Day 89 narrows it.

**Basis:** Gaudium is registered under NIC **85100, Hospital activities** — a real healthcare class. India's register plainly has health codes.

**The refined claim.** The register classifies by **activity**. Writing software that reads medical images is not a hospital activity, so Qure.ai and Eka Care fell to **74999**, the residual class. The register is not blind to health; it is organised on an axis that cannot see an industry defined by its technology.

**Why this is stated as a correction.** A series that corrects itself where the evidence warrants is more trustworthy than one that does not. `verify.py` records both `india_register_does_have_a_health_code` and `day88_finding_refined_not_reversed` as **True**.

### 1.9 The four-market ladder

**Assumption:** the United States, United Kingdom, Brazil and India are a fair set for the ladder in §30.

**The judgement involved.** They were selected because each has a documented position on the two axes that matter — whether the regulator publishes, and whether the clinic's own channel is standardised — from primary or peer-reviewed sources used in this case study. They are not a representative sample of world markets, and no claim about global prevalence is made.

**What is robust.** The bottom row. **No** market in the set has standardised what a clinic says on its own website, and that is the column the README builds its conclusion on.

### 1.10 RICE parameters

**Assumption:** the Reach, Impact, Confidence and Effort values in §46 and the stress multipliers in §47 are the author's estimates.

**They are not derived from Gaudium's internal data**, because none is public. Reach is ordinal 1–10 with each anchor stated so a reader can substitute their own.

**What is soft and what is not.** The individual scores are soft. **The reversal is not.** P1 leads the base case and ranks last under stress across a wide range of parameter choices, because the reversal is driven by the structure of its binding constraint — the absence of a benchmark against which an honest number can be read — rather than by the multipliers.

**The weakness, stated plainly and consistently with Day 88.** This cannot be checked against observed behaviour. No Indian clinic publishes a stratified live birth rate, which is consistent with §48's argument but does not prove it; the same observation would follow if nobody had thought of it. §50's question 7 leaves it open. Unlike Days 87 and 88, Day 89 at least identifies a **testable** consequence: if the benchmark argument is right, publication by several clinics simultaneously should be survivable where publication by one is not.

---

## Part 2 — Source Conflicts

### 2.1 "Public record system" versus a login wall

**The conflict.** The government portal [P] describes the registry as "a online public record system of ART Clinics/Banks and Surrogacy Clinics in India". The live registry [R] exposes only signup and login.

**Resolution.** Both observations stand; they describe different things. "Public record system" is plausibly used in the administrative sense of an official record maintained by the state, not in the sense of publicly readable. The README reports the description and the observed behaviour side by side in §19 and §20 and does not accuse the portal of misdescribing itself.

**Why it is in the case study.** Because a patient reading "public record system" would reasonably expect to be able to read it, and cannot. The gap between the two meanings of "public" is the finding, not a drafting error to be scored.

### 2.2 The ART Act text could not be read

**The conflict.** Two primary routes to the statute failed. `indiacode.nic.in` returned HTTP 504 repeatedly and is disallowed to the fetching tool by its robots handling; `egazette.nic.in` is outside this environment's egress allowlist and returned a proxy rejection.

**Resolution.** **No claim about the Act's sections is made anywhere in this case study.** Everything said about the Act's effect is sourced to the government portal's description of the registry, to the registry's observed behaviour, or to [L5], a peer-reviewed survey of practitioners. `verify.py` asserts `art_act_text_was_read_in_full` as **False**.

**What this costs.** Materially: the Act may contain a publication provision not yet implemented, an advertising restriction, or a success-rate reporting clause. Any of those would sharpen or complicate §21 and §32. A reader should treat the India column of the ladder as describing **what is observably published**, not what the statute requires.

This is the most significant limitation in the case study and it is stated in the README's method notes as well as here.

### 2.3 Corporate record year versus marketing year

Covered in 1.7. Both records can be correct; recorded as an observation.

### 2.4 Legal name versus previous legal name

**The conflict.** GLEIF records the current legal name as "GAUDIUM IVF AND WOMEN HEALTH LIMITED" and a previous legal name of "GAUDIUM IVF AND WOMEN HEALTH PRIVATE LIMITED".

**Resolution.** Not a conflict — a recorded conversion from private limited to public limited. The CIN's `PLC` segment is consistent with the current name. The README reports the conversion as a fact and draws one inference from it: that PLC status brings heavier company-law obligation while the leading `U` confirms the company remains unlisted.

### 2.5 A false lead that was discarded

**What was searched.** Whether Gaudium is listed on an Indian SME exchange, which would have restored a securities-disclosure obligation and changed the case study entirely. The legal name ending in "LIMITED" rather than "PRIVATE LIMITED" made this worth checking.

**What was found.** The CIN begins with **U** — unlisted. Public limited status is a company-law class, not a listing.

**Why it is recorded.** Because assuming "Limited" meant "listed" would have produced a case study asserting a disclosure regime that does not exist. The check took one field of one record and it changed the entire framing.

### 2.6 HFEA clinic-level publication

**What is claimed.** That the HFEA publishes clinic-level data through a public "Choose a Fertility Clinic" service.

**How it is sourced.** Indirectly but firmly: [L1] and [L3] both state that they identified their study populations *using* the HFEA's Choose a Fertility Clinic facility. Two peer-reviewed papers using a public service to enumerate clinics establishes that the service exists and lists clinics.

**What is not claimed.** The specific outcome measures HFEA displays per clinic. A direct fetch of the HFEA clinic search returned only a rating interface and did not confirm which metrics are shown. The README's ladder therefore marks the UK as "regulator publishes" — which the papers support — without specifying the measure set.

---

## Part 3 — Absences

| # | Absent | Where it would appear | Compelled by anything? |
|---|---|---|---|
| 1 | Any clinic-level outcome figure for any Indian clinic | The National ART Registry | Collected, **not published** |
| 2 | A public directory of registered Indian ART clinics | The National ART Registry | Collected, **not published** |
| 3 | A national benchmark live birth rate for India | The ART authority | **No** |
| 4 | Live birth rate on the clinic's own site | [W] | **No** |
| 5 | Any denominator, n, or reporting period | [W] | **No** |
| 6 | Multiple birth rate | Anywhere in India | **No** |
| 7 | Adverse events | Anywhere in India | **No** |
| 8 | Cancellation rate before transfer | Anywhere | **No** |
| 9 | ART registration number on the clinic site | [W] | **No** |
| 10 | Revenue, pricing, cycle volume | A financial filing | **No** |
| 11 | Any published audit of Indian clinic websites | Peer-reviewed literature | **No** |
| 12 | The ART Act's text, to this case study | indiacode / egazette | Blocked — see 2.2 |

Items 1 and 2 are the case study. They are the only rows where the data demonstrably **exists and is held by a public authority**, and the only rows where the fix requires no new collection, no new burden on clinics, and no new science — only a decision about who may read.

Item 11 is the gap in this case study's own evidence: the behaviour of Indian clinic websites as a class has not been measured by anyone, so the README uses Brazilian and UK audits for the market argument and declines to extrapolate.

---

## Part 4 — Limitations

### 4.1 The statute was not read

Stated in 2.2 and repeated here because it bounds everything. **This case study describes what is published, not what is required.** If the ART Act contains a publication mandate that has not been implemented, the README's characterisation of India's regime as a registration mandate rather than a publication mandate would need revising — though the observed outcome for a patient today would be unchanged.

### 4.2 One company, one market, one day

Day 89 examines one company's public record and one market's registry surface, on one date. The §44 lessons are supported by this case and by contrast with Days 82–88. They are not established across a sample of clinics, countries, or registries, and no claim in this document is a statistical claim about Indian healthcare.

### 4.3 This is not a clinical assessment

Nothing here bears on the quality of care at Gaudium IVF or at any clinic. The absence of published outcome data is not evidence of poor outcomes, and the README says so directly. A clinic that publishes nothing may be excellent; that is precisely the problem being described, since a patient cannot tell either way.

### 4.4 Website observation is a snapshot

[W] was observed on 2026-09-27 through a fetching tool that renders page text. Content behind interaction, in images, in PDFs, or on pages not visited would not have been captured. A success rate published as an image, for instance, would not appear as text. The claim is scoped to what the observation covered.

### 4.5 The comparators are not like-for-like on measure

The CDC publishes success rates per ART cycle or per transfer; the UK publishes through HFEA; Brazil's SisEmbrio and India's registry collect but do not publish to the public. These regimes differ in what they measure as well as in what they publish. The ladder in §30 compares them only on **whether the regulator publishes at all** and **whether the clinic's own channel is standardised** — two binary axes on which the sources are clear — and does not compare their numbers.

### 4.6 No Indian clinic audit exists

The single most useful missing input. Everything the README says about what clinics publish comes from the UK and Brazil. Whether Indian clinic websites resemble either is unknown, and §50 records it as an open question rather than an assumption.

### 4.7 The benchmark argument is a model

§48's conclusion — that no clinic publishes because the regulator does not publish — is reasoned from constraint structure, not measured. It is consistent with the observation that no Indian clinic publishes, and consistent with the US and UK having published clinic data only after a regulator did. It is not proven, and 1.10 above states the test that would settle it.

---

## Part 5 — Verification Record

### 5.1 The gate

`verify.py` contains **242 checks**, all passing. It was written and passing **before the first sentence of `README.md` existed**.

Rounding is half-up to two or three decimals via `Decimal.quantize`, not Python's banker's rounding. Tolerance on floating comparisons is 0.005. Derived values are computed from **unrounded** inputs throughout.

### 5.2 What failed on first run

**Nothing.** Zero of the hand-stated expectations were wrong, the first day in this arc where that has happened. `verify.py` records `hand_stated_values_that_failed_first_run` as **0**.

This is reported as an observation rather than an improvement in care. Days 82, 86, 87 and 88 each caught hand-stated errors, and in every case the culprit was the rounded-intermediate trap — a figure computed from values that had already been rounded. Today's arithmetic is mostly ratios of small integers drawn straight from published counts (53/79, 1/79, 19/54, 182/534), which is the arithmetic least exposed to that trap. The gate's value today lay in reconciliation rather than correction.

### 5.3 What the gate reconciles

Several checks confirm that published counts add up, which is the check most likely to catch a misreading of a source:

- [L1]: 81 clinics identified − 2 without websites = **79** analysed.
- [L1]: 53 reporting + 26 silent = **79**.
- [L1]: 31 pregnancy measures + 9 live birth measures = 40, leaving **11** of the 51 outside those two families.
- [L4]: 534 + 516 = **1,050** women allocated; 1,050 − 1,023 started = **27**.
- [L4]: 182/534 recomputes to **34.08%** against a reported 34.1%, and 161/516 to **31.20%** against a reported 31.2%.
- CIN: all six segments of a 21-character identifier parsed and asserted individually.

The [L4] recomputation is the most important of these. It confirms that the cumulative live birth rates in the README are the paper's own figures and not a transcription, which matters because the entire denominator argument in §27 rests on them.

### 5.4 Negative controls

Eleven checks assert that something is **False**, so no sentence can quietly imply it:

`gaudium_publishes_a_misleading_success_rate`, `gaudium_breaks_any_disclosure_rule`, `this_case_study_measures_gaudium_clinical_quality`, `uk_or_brazil_findings_apply_to_gaudium`, `indian_clinics_were_audited_here`, `art_act_text_was_read_in_full`, `registry_content_behind_login_was_accessed`, `any_gaudium_outcome_figure_is_known`, `company_financials_known`, `day89_uses_mermaid`, `day89_fabricates_any_figure`.

The first four are the fairness controls. The easiest way to write this case study badly would be to let audits of Brazilian and British clinics bleed into implications about a named Indian company, and these four assertions are what prevent a later edit from doing that silently.

The next two are the reachability controls. A reader must be able to distinguish "the registry does not publish this" from "this case study could not reach it", and two of the sharpest-sounding statements in the README depend on that distinction holding.

### 5.5 The RICE assertion

The requirement that the base-case leader rank **last** under stress is enforced programmatically:

```python
chk_eq("p1_leads_base", base_rank[0], "P1")
chk_eq("p1_ranks_last_under_stress", stress_rank[-1], "P1")
chk_eq("p1_rank_reversal_is_total", base_rank[0] == stress_rank[-1], True)
```

P1 decays **98.57%**, more than any other proposal, asserted via `p1_decays_more_than_every_other_proposal` rather than observed.

Three further checks record the conclusion the stress test produces rather than the ranking itself: `no_published_national_benchmark_in_india`, `an_honest_number_alone_reads_as_a_bad_number`, and `the_fix_is_a_publication_mandate_on_the_regulator`. These are the case study's argument, written into the gate so that the prose cannot drift away from them.

### 5.6 Cross-check

`crosscheck.py` extracts every two- and three-decimal figure from `README.md` and `ASSUMPTIONS.md` and confirms each traces to a value asserted in `verify.py`. Figures quoted at source precision — the 22.8% and 23.8% fresh-transfer live birth rates, the 87.8% egg-freezing cycle share, the 98% CDC cycle coverage — are allow-listed with their source reference. Derived figures are never allow-listed; where the cross-check flagged one, it was added to the gate.

---

*Companion to `README.md`. Day 89 of 90.*
