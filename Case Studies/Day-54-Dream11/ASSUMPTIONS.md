# ASSUMPTIONS — Day 54, Dream11

This file exists so that nothing in [README.md](./README.md) has to carry an unmarked assumption. Everything here is mine. None of it is a Dream11/Dream Sports statement, a finding, or a fact.

- **Assumptions (A)** — things I believe but cannot verify from public sources, which the analysis depends on.
- **Derivations (D)** — arithmetic I performed on published figures.
- **Constructs (C)** — objects, metrics, and designs I invented. Nothing in this category exists at Dream11.

**Date of analysis:** 17 August 2026. **Latest financials available:** FY25 (year ended 31 March 2025) — this predates the August 2025 ban; no FY26 disclosure was found publicly available. **Research boundary:** public sources only.

---

## Part 1 — Assumptions

### A1 — Load-bearing. Post-ban user disengagement (if it exists at meaningful scale) is primarily about the absence of stakes, not other confounding factors.

I infer this from the qualitative logic that real-money stakes were the defining differentiator of the pre-ban product, and from the CEO's own statement that real-money contests drove ~95% of revenue and 100% of profit — implying stakes-driven engagement was doing almost all the commercial work.

**Why it might be wrong:** disengagement, if present, could equally stem from reduced marketing spend post-ban, the loss of the national cricket team sponsorship reducing visibility, app-store ranking changes, or simply reduced habitual triggers (payment notifications, deposit reminders) that existed under the RMG model for reasons unrelated to "stakes" as a psychological driver. I have no data isolating these factors from each other.

**How it gets tested:** the Phase 0 baseline in §53, and more directly, Arm C of the A/B design in §54, which tests whether tangible reward or mere "something to strive for" structure explains any observed lift — a partial but not complete test of A1 itself.

**Confidence:** Medium on direction. Low on how much of any observed disengagement this single mechanism explains.

### A2 — The FY25 net loss is genuinely and substantially separable from the ban's financial impact

Based on Entrackr's reporting explicitly attributing the loss to a domicile-shift tax charge and director/ESOP-related expenses, and the plain fact that FY25 (ended 31 March 2025) closed before PROGA passed (August 2025).

**Why it might be wrong:** anticipatory effects (e.g., reduced user deposits or engagement in the months before the ban, as the law was debated in Parliament) could have had some FY25 impact not captured in the "domicile shift + ESOP" framing — I have no data confirming or ruling this out.

**Confidence:** Medium-high on the structural separation being real; low on whether it's 100% clean.

### A3 — A PROGA-compliant, non-cash stakes mechanic has not already been tried and quietly discontinued by Dream11

I found no public evidence of such a feature having been tried, but "no public evidence" is not the same as "did not happen" — a company navigating a fast-moving regulatory and product pivot may have run internal experiments not covered in the trade press reviewed for this analysis.

**Confidence:** Medium.

### A4 — Sponsors would be willing to fund a non-cash reward pool at meaningful scale, given genuine engagement data

Assumed based on the general logic that brands (Swiggy, Astrotalk, Tata Neu, Cred) already partnering with Dream11 for ad/sponsorship placement would plausibly value a more engagement-linked mechanic — not confirmed by any sponsor statement specific to this idea.

**Confidence:** Low-medium — the softest assumption in this document.

### A5 — The 10 million DAU figure reported in September 2025 reflects genuine post-pivot engagement rather than a short-term spike tied to launch-period curiosity or press coverage

**Confidence:** Low — this is a single point-in-time figure with no trend data around it in the sources reviewed.

---

## Part 2 — Derivations

| # | Derivation | Inputs | Result | Where |
|---|---|---|---|---|
| **D1** | Illustrative non-RMG-dependent revenue base, applied to FY25 | 5% × ₹6,759 Cr | **≈₹338 Cr** | §13.1 |
| **D2** | FY24→FY25 operating revenue decline | (6,759−7,934)/7,934 | **≈−14.8%** (reported as "15%" in source) | §13.2 |
| **D3** | Employee benefit expense growth, FY24→FY25 | (1,673−1,030)/1,030 | **≈62.4%** | §13.2 |
| **D4** | FY25 total expenditure growth, FY24→FY25 | (7,123−6,562)/6,562 | **≈8.5%** (reported as "9%" in source) | §13.2 |
| **D5** | FY25 total income vs. operating revenue gap | 7,374−6,759 | **≈₹615 Cr** of non-operating income (source states ₹601 Cr; small rounding discrepancy, both noted) | §13.2 |
| **D6** | FY23 revenue-to-FY24-revenue growth (using the higher Inc42 FY24 figure) | (8,345.9−6,384)/6,384 | **≈30.7%** | Appendix A-1 |

**The one caveat that applies to D1:** this is explicitly labelled in §13.1 as an illustrative order-of-magnitude calculation applying a single CEO statement's percentage to a pre-ban revenue base — it is not a disclosed FY26 figure and should not be read as a forecast or an official estimate.

---

## Part 3 — Constructs

| # | Construct | Detail | Where |
|---|---|---|---|
| **C1** | **Dream11 Trophy Room** | The entire proposal — non-cash stakes/reward mechanic, sponsor-funded, compliance-designed | §50 |
| **C2** | **Stakes-Adjusted Engagement Rate (SAER)** (North Star) | §31 |
| **C3** | **Pre-Ban vs. Post-Ban Retention Cohort, Stakes-Mechanic Lift, Advertiser Value Realisation** | §32 |
| **C4** | **Personas Rohan, Simran, and the illustrative marketing-lead persona** | §20 |
| **C5** | **All RICE inputs and the stress rule** | §47 |
| **C6** | **Acceptance-criteria bars** | §51.5 |
| **C7** | **The three-arm A/B design, including Arm C as falsifier** | §54 |
| **C8** | **Technical architecture and data-flow reconstructions** | §41, §42 |
| **C9** | **The explicit separation of the FY25 loss narrative from the ban narrative** | §5, §13.2 — an interpretive framing built from Entrackr's reporting, not a claim Dream11 itself has made in these exact terms |

---

## Part 4 — What is not in this document

- **No screenshots or authenticated-session data.**
- **No FY26 financial disclosure.** The actual post-ban financial impact is not directly evidenced in this document — everything about the ban's magnitude relies on the single CEO statement (~95%/100%) and the pre-ban FY25 figures used as a baseline for illustration only.
- **No independent engagement/retention data from Dream11.** All retention-risk claims are inferential (A1), not sourced from disclosed cohort data.
- **No claim about the merits of PROGA itself** — the policy debate (addiction, financial harm vs. industry/employment impact) is treated as a legitimate, contested question this document does not take a side on (§57, R1), consistent with the series' general practice of not offering personal opinions on contested policy questions.
- **No verification of whether Dream11 has already internally tested a mechanic similar to the one proposed** (A3).

---

## Part 5 — The single sentence version

If only one line of this file survives: **the entire case study depends on assumption A1 — that any post-ban user disengagement is primarily about the removal of stakes rather than other confounding factors (marketing spend, lost sponsorship visibility, habitual payment triggers) — and A1 is only partially testable via the proposed A/B design (§54), which is why this document is explicit that a null or ambiguous result would be a genuinely valid and useful outcome, not a failure of the experiment.**

---

*Companion to [README.md](./README.md) · Day 54 of 90*
