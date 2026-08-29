# ASSUMPTIONS — Day 63, BookMyShow (Big Tree Entertainment)

This document separates what was **reported**, what was **derived**, and what I **constructed**. Every derived figure is verified programmatically in `verify.py` (79 checks, all passing). Nothing here is a forecast of BookMyShow's results.

**Evidence grading:** 🟢 High — primary or directly reported. 🟡 Medium — reliable secondary, consistent across sources. 🟠 Low — single source. 🔴 Conflicting or unavailable.

---

## Part 1 — Assumptions

### A1 (load-bearing) — That Live Nation's segment structure says something about BookMyShow's future

**The whole case study rests on this.** Live Nation FY2025 earns **3.29%** on concerts and **35.48%** on ticketing (§14). I treat that gap as evidence about the economics BookMyShow is moving *into* as live grows from 31.82% to 40.45% of income (§20).

**Why I think it holds:** the gap is not a Live Nation artefact, it is the price of absorbing variance (§26). A promoter commits before demand is observable; a ticketing agent does not. That asymmetry is structural and does not depend on geography.

**Why it might not:** Live Nation's revenue is **128.09×** BookMyShow's income. Indian live entertainment is earlier, less contested for the biggest tours, and possibly less guarantee-driven — which is exactly what makes guarantees cheaper and margins potentially better today. Scale also cuts the other way: Live Nation's ticketing margin benefits from Ticketmaster's near-monopoly position, which BookMyShow does not have in equivalent form.

**What I did about it:** nothing in this case study forecasts an Indian margin. §53's first success criterion is that FY26 either shows live margin converging toward 3.29% or holding — and §60 states plainly that if it holds, my thesis was wrong.

### A2 (load-bearing) — That implied PBT is a fair reading of the tax line

Total income minus total expenses gives PBT (§19, Appendix A-2). **"Total income" may not be the exact statutory base**, so the derived ₹165 Cr / ₹110 Cr carry that uncertainty.

**Why it holds well enough:** the conclusion does not depend on the precise figure. **FY25 PAT margin (10.27%) exceeds FY25 PBT margin (8.83%)** — a company cannot earn more after tax than before it on operations. Something below the operating line contributed, and the direction is not in question even if the magnitude shifts.

**What I am explicitly not claiming:** that anything is irregular. A deferred-tax credit is normal for a company turning durably profitable. The claim is narrow — **₹27 Cr is 14.06% of PAT, it is not an operating gain, and it is unlikely to repeat.**

### A3 (medium) — That the FY25 segment figures are accurate as reported

Ticketing ₹828 Cr / ₹741 Cr and live ₹756 Cr / ₹455 Cr come from **secondary coverage of MCA filings**, not from the filing read directly 🟡. Every mix, growth-attribution and crossover figure in §17, §20 and §21 depends on them.

**Mitigation:** the four reported figures reconcile against total income to within the **₹285 Cr residual** that §62 flags as undisclosed. They are internally consistent, which is weak evidence but not none.

### A4 (medium) — That extending each segment at its own FY25 rate is a legitimate illustration

§20's crossover — live ₹1,256.1 Cr overtaking ticketing ₹925.2 Cr — extends **one year at each segment's own observed rate**.

**This is not a forecast and is not presented as one.** It is a statement about what the current rates imply if nothing changes, and one year is the shortest horizon that makes the point. Live's **+66.15%** almost certainly decelerates; the illustration would be dishonest at three years and I did not run it that way.

### A5 (author-constructed, explicitly unverified) — That BookMyShow's pre-purchase signal is usable

§28 asserts that notification sign-ups, waitlists, reminders and pre-sale registrations constitute a demand signal available **before** the promoter's commitment locks. **I have no disclosure confirming this is captured, retained, or usable**, and none confirming the timing relationship.

**This is the assumption most likely to be false**, which is why §53's Phase 0 costs 2 analyst-weeks rather than a quarter of engineering, and why **K2 — the commitment happens before any signal exists — is named as the kill criterion most likely to fire.**

### A6 (low, non-load-bearing) — That ₹95/USD is adequate for the KKR conversion

Used only in §29 and Appendix A-3. The **25% spread in the reported deal amount** dominates any plausible FX error by an order of magnitude, so precision here would be false precision.

---

## Part 2 — Derivations

Every figure below is computed in `verify.py`. Nothing in this section was reported; everything was calculated from figures that were.

**D1 — Growth and its attribution.** Total income **+30.70%**; ticketing **+11.74%**; live **+66.15%** (**5.63×** ticketing's rate). Of **₹439 Cr** of income growth: live **₹301 Cr / 68.56%**, ticketing **₹87 Cr / 19.82%**, residual **₹51 Cr / 11.62%**. Live contributed **3.46×** ticketing's rupees.

**D2 — Mix and the crossover.** Ticketing **51.82% → 44.30%** (−7.52pp); live **31.82% → 40.45%** (+8.63pp). FY25 gap **₹72 Cr** in ticketing's favour. Extended one year at their own rates: ticketing **₹925.2 Cr**, live **₹1,256.1 Cr** — live overtakes.

**D3 — The tax line.** Implied PBT **₹110 Cr → ₹165 Cr = +50.00%**, against reported PAT **+76.15%** — a **26.15pp** gap. PBT growth is **65.66%** of PAT growth. Implied FY24 tax charge **₹1 Cr** (effective rate **0.91%**); implied FY25 credit **₹27 Cr = 14.06% of PAT**.

**D4 — Operating leverage.** Expenses **+29.09%** against income **+30.70%** — **1.61pp** of real operating leverage. PBT margin **7.69% → 8.83%** (+1.14pp). **PAT margin 10.27% exceeds PBT margin 8.83%.**

**D5 — KKR implied valuation.** 6% at $40–50 Mn ⇒ **$666.7–833.3 Mn** ⇒ **₹6,333–7,917 Cr** at ₹95/USD ⇒ **33.0×–41.2× FY25 PAT**, **3.39×–4.24× FY25 income**. Reported amount spread: **25%**.

**D6 — Live Nation structure.** Concerts margin **3.29%**; ticketing **35.48%**; ratio **10.80×**. Revenue shares: concerts **82.94%**, ticketing **12.30%**. AOI shares: concerts **28.63%**, ticketing **45.83%**. Ticketing earns **3.73×** its revenue share in profit; concerts **0.35×**. Group AOI margin **9.52%**. Live Nation revenue is **128.09×** BookMyShow's income.

**D7 — RICE under stress.** Stress multiplier **19.82%** (ticketing's share of income growth, D1h). Baseline: ticketing optimisation **220.80**, live slate **170.10**, Demand Gate **40.05**, venue lock-ins **34.50**. Stressed: **43.76 / 33.71 / 7.94 / 34.50 (exempt)**. **The proposal falls from 3rd to 4th — last.**

**D8 — Phase 0.** 2 analyst-weeks; 200 events; ±20% accuracy band; 12pp R1 threshold on GRE/100; 25% new-artist floor.

---

## Part 3 — Constructs

These are mine. They are not BookMyShow's language, not industry-standard, and should not be attributed to any source.

**The Demand Gate** (§50) — a published, pre-commitment demand threshold with post-event forecast scoring. My proposal.

**GRE/100 — Gated Risk Events per 100 company-risk events** (§31). The denominator is the design: it counts only events where BookMyShow's own capital is at risk, so taking on more risk without gating it lowers the metric mechanically. The four-part conjunctive definition (gated before commitment · realised within ±20% · contribution positive · no override) is constructed to close four specific gaming routes.

**NAS-90 — New-Artist Share at the 90th percentile of gate-rejection intensity** (§52). Measured at the 90th percentile rather than the mean because the gate's failure mode — squeezing out unproven artists — appears only in the periods when it rejects hardest. The average would look fine throughout.

**The stress rule** (§47) — multiplying growth-dependent initiatives by **19.82%**, ticketing's share of FY25 income growth. Derived from the company's own disclosure, not chosen for effect. The exemption for venue lock-ins is a judgement: they pay from the installed base, not from next year's growth mix.

**"The promoter is paid to absorb variance"** (§26) — my framing of why the 10.80× margin gap exists. It is an interpretation of the structure, not a quotation from anyone.

---

## Part 4 — What Would Change My Mind

**If Phase 0's K2 fires** — the commitment is made before any demand signal exists — the proposal is wrong at the root. The remedy would be contractual (move the commitment point, shift to revenue share), not a product. **This is the outcome I consider most likely.**

**If FY26 live margin holds or improves**, A1 was doing too much work and the Indian structure genuinely differs from Live Nation's. That would not make the pivot risk-free, but it would remove my central evidence.

**If the ₹285 Cr residual (15.25% of income)** turns out to be a distinct high-margin business rather than a rounding bucket, the two-businesses framing in §20 is materially incomplete.

**If FY26's effective tax rate normalises and PAT still grows strongly**, R2 was noise and I under-read an operating story that was genuinely strong.

**If a demand gate already exists internally**, the contribution here is at most the metric design, and §36's gap was my ignorance rather than the company's.

---

## Part 5 — What Could Not Be Found Out

- Any breakdown of the **₹285 Cr residual** — 15.25% of FY25 income, entirely unallocated. 🔴
- Whether a **demand gate or equivalent decision rule already exists** inside the live business. 🔴
- The **split between company-risk and fee-only live events** — the denominator GRE/100 requires. 🔴
- **Per-event economics** of any kind: guarantees, contribution, attendance against plan. 🔴
- The **actual disclosed tax line**, as against the derived one in Appendix A-2. 🔴
- Which of the two **reported KKR amounts** — $40 Mn or $50 Mn — is correct. 🔴
- Any disclosure on **crowd safety, accessibility or sustainability** (§40–42). 🔴
- Whether **quarterly volatility** exists in the live business, since reporting is annual only. 🔴

---

*Day 63 of 90. `verify.py` — 79 checks, all passing.*
