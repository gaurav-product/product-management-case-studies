# ASSUMPTIONS — Day 51, Ola

This file exists so that nothing in [README.md](./README.md) has to carry an unmarked assumption. Everything here is mine. None of it is an Ola/ANI Technologies statement, a finding, or a fact.

- **Assumptions (A)** — things I believe but cannot verify from public sources, which the analysis depends on.
- **Derivations (D)** — arithmetic I performed on published figures.
- **Constructs (C)** — objects, metrics, and designs I invented. Nothing in this category exists at Ola.

**Date of analysis:** 17 August 2026. **Latest financials available:** FY25, per ANI Technologies' annual report filed with the RoC in May 2026. **Research boundary:** public sources only.

---

## Part 1 — Assumptions

### A1 — Load-bearing. Ola's rider-side decline is primarily *caused* by driver attrition to Rapido's subscription/flat-fee model, not merely correlated with it.

I infer causation from timing (Rapido's user-growth inflection tracks its subscription-model adoption, not a general product improvement) and from direct driver-sentiment reporting (Forbes India's account of drivers "working 12–14 hours a day just to maintain earnings" under commission, and improved retention cited by Rapido after piloting the subscription model).

**Why it might be wrong:** correlation is not causation. Rapido's growth could equally reflect superior marketing spend, earlier bike-taxi-category dominance carrying over into cabs, general market growth benefiting the newest entrant most, or Uber/Ola-specific missteps unrelated to commission structure. I have no Ola-internal driver-attrition data confirming the mechanism.

**How it gets tested:** the Phase 0 baseline in §53 — before building anything, confirm whether driver attrition at Ola is actually concentrated in the cities/categories where Rapido's share has grown fastest. If attrition is roughly uniform everywhere, the causal story in A1 is weaker than presented.

**Confidence:** Medium-high on direction. Low-medium on how much of the effect this single mechanism explains versus other factors.

### A2 — The Ola Electric stake markdown is accounting, not operating, and should be read separately from ANI Technologies' core ride-hailing performance

I treat the ~₹1,300 Cr markdown contributing to FY25's ~₹1,975 Cr consolidated loss as a mark-to-market event on a related but distinct listed entity, not as evidence of ride-hailing operating deterioration beyond what the standalone figures already show.

**Why it might be wrong:** the two businesses share a founder, cross-brand equity, and (per DRHP-adjacent reporting patterns elsewhere in this series) sometimes shared strategic resources; a reader could reasonably argue they shouldn't be analytically separated as cleanly as I've done.

**Confidence:** Medium.

### A3 — Rapido's subscription model is the primary but not sole explanation for its MAU growth

I explicitly do not claim the flat-fee model is 100% of Rapido's success — execution quality, earlier bike-taxi-category ownership, and capital deployment plausibly all contributed.

**Confidence:** Medium — stated as a caveat throughout rather than resolved.

### A4 — A driver-choice pilot can be run without materially destabilising Ola's already-fragile balance sheet

I assume a tightly bounded 2–3-city pilot represents small enough absolute exposure not to worsen the credit/liquidity concerns Moody's flagged. I have no visibility into Ola's actual cash position or covenant terms to confirm this.

**Effect if wrong:** the entire "cheap, bounded pilot" framing of §50–53 would need re-scoping to something even smaller, or the proposal would need to be paired with a financing plan outside this document's scope.

**Confidence:** Low-medium — the softest assumption in this document.

### A5 — Drivers who have already left for Rapido represent close to zero current commission revenue for Ola in the affected zones

This is the basis for §39.2's argument that a flat fee from a won-back driver is "strictly better than 25% of nothing." If departed drivers still occasionally accept Ola rides opportunistically, the true comparison is a smaller number, not zero.

**Confidence:** Medium.

---

## Part 2 — Derivations

| # | Derivation | Inputs | Result | Where |
|---|---|---|---|---|
| **D1** | Standalone revenue decline, FY24→FY25 | (1,171−1,906)/1,906 (using the more granular parent-level FY24 figure) | **≈−39%** (reported elsewhere as −42% using a slightly different FY24 base of "over ₹2,000 Cr") | §13.3 |
| **D2** | Mobility-segment revenue decline | (925−1,761)/1,761 | **≈−47%** | §5, §13.3 |
| **D3** | Standalone loss growth | (662.4−328.7)/328.7 | **≈+102%** | §13.3 |
| **D4** | Ola Electric loss growth, FY24→FY25 | (2,276−1,584)/1,584 | **≈+44%** | §13.5 |
| **D5** | Ola Electric revenue decline, FY24→FY25 | (4,514−5,010)/5,010 | **≈−10%** | §13.5 |
| **D6** | Ola Electric Q1 FY26 auto opex reduction | (178−105)/178 | **≈−41%** monthly auto opex, per Project Lakshya | §13.5 |
| **D7** | Rapido MAU multiple vs Ola, Feb 2026 | 74M ÷ ~26.5M (midpoint of 26–27M) | **≈2.8×** | §5, §14 |
| **D8** | Combined Uber+Ola MAU vs Rapido, Feb 2026 | 38M+26.5M = 64.5M vs 74M | Rapido's user base **exceeds** Uber+Ola combined | §5 |

**The one caveat that applies to D1–D3 collectively:** two slightly different FY24 revenue baselines exist in circulation for Ola Consumer/ANI Technologies (a "total incl. other income" figure and a "standalone" figure), reported inconsistently across articles covering the same underlying filing. The direction (steep decline, loss roughly doubling) holds regardless of which baseline is used; the precise percentage varies by a few points.

---

## Part 3 — Constructs

| # | Construct | Detail | Where |
|---|---|---|---|
| **C1** | **Ola Fair Fare** | The entire proposal — driver-choice toggle, pilot design, pricing construct | §50 |
| **C2** | **Driver Take-Home Parity Rate** (North Star) | §31 |
| **C3** | **Subscription Opt-In Rate, Driver Retention Delta, Rider ETA Delta** | §32 |
| **C4** | **Personas Suresh, Priya, and the illustrative "Bhavish's dilemma" framing** | §20 — the third persona is explicitly illustrative of a decision-maker's trade-off, not a real individual's documented position |
| **C5** | **All RICE inputs and the stress rule** | §47 |
| **C6** | **Acceptance-criteria bars** | §51.5 |
| **C7** | **The three-arm A/B design, including Arm C as falsifier** | §54 |
| **C8** | **Technical architecture and data-flow reconstructions** | §41, §42 |
| **C9** | **The framing of Ola's rider-side investment as prioritised over supply-side fixes** | §35, §46 — a reading of public disclosures, not an Ola-stated prioritisation |

---

## Part 4 — What is not in this document

- **No screenshots or authenticated-session data.**
- **No Ola-disclosed driver-attrition or take-home-pay data.** All driver-economics claims are drawn from Rapido/Namma Yatri-side reporting about the *shift*, not from Ola's own numbers, which are not public.
- **No claim about the merits of Ola's auditor change or the governance concerns** beyond what was disclosed in press coverage of the annual report filing — treated as a risk (§57, R4), not adjudicated.
- **No independent verification of MAU tracker methodology** (Sensor Tower, Similarweb, or the "India Dispatch" chart cited in §14) — these are third-party estimates, not Ola/Rapido/Uber-disclosed figures.

---

## Part 5 — The single sentence version

If only one line of this file survives: **the entire case study depends on assumption A1 — that Ola's rider-side decline is primarily caused by driver migration to a flat-fee competitor rather than merely coinciding with it — and A1 is testable with a Phase 0 baseline check of where Ola's driver attrition actually concentrates, before a single line of the proposed feature is built.**

---

*Companion to [README.md](./README.md) · Day 51 of 90*
