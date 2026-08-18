# ASSUMPTIONS — Day 53, PhysicsWallah

This file exists so that nothing in [README.md](./README.md) has to carry an unmarked assumption. Everything here is mine. None of it is a PhysicsWallah statement, a finding, or a fact.

- **Assumptions (A)** — things I believe but cannot verify from public sources, which the analysis depends on.
- **Derivations (D)** — arithmetic I performed on published figures.
- **Constructs (C)** — objects, metrics, and designs I invented. Nothing in this category exists at PhysicsWallah.

**Date of analysis:** 17 August 2026. **Latest financials available:** FY26 (year ended 31 March 2026), per PhysicsWallah's post-listing results disclosure. **Research boundary:** public sources only.

---

## Part 1 — Assumptions

### A1 — Load-bearing. PhysicsWallah's offline segment runs at a genuinely negative net margin, not merely a lower margin than online.

This is drawn entirely from a single brokerage's (SPTulsian) independent reconstruction of the FY25 DRHP filings, stating an "effective net margin of negative 20%" for offline. PhysicsWallah itself, in the sources reviewed for this document, discloses the online/offline **revenue** split but not a segment-level **profitability** breakdown.

**Why it might be wrong:** a single analyst's reconstruction, however careful, is not the same as company-disclosed segment accounting, and could rest on cost-allocation assumptions (e.g., how shared corporate overhead is split between segments) that a different, equally reasonable methodology would resolve differently — potentially showing offline as marginally profitable or only mildly loss-making rather than materially negative.

**How it gets tested:** the Phase 0 density analysis in §53 doesn't directly test this assumption; the more direct test would be PhysicsWallah itself disclosing segment-level profitability in a future results release, which this document cannot compel and can only wait for.

**Confidence:** Medium — a single credible secondary source, not independently cross-verified against a second methodology or company disclosure.

### A2 — The revenue-per-student figures (§13.1) are a fair proxy for price-point differences between online and offline, not distorted by a small number of very high-value offline outliers

I divide total segment revenue by total segment student count to get the ~11x multiple. If offline revenue is concentrated in a small number of very expensive premium programmes (e.g., long-format residential coaching) rather than evenly distributed across the 3.3 lakh offline students, the "typical" offline student's actual price point could be lower than the average implies.

**Confidence:** Medium.

### A3 — PW Vidyapeeth and PW Pathshala have meaningfully different cost structures that this document's blended "offline" treatment obscures

Pathshala is described in public sources as a hybrid format, distinct from Vidyapeeth's full-campus model. If Pathshala is already closer to the "staff-light, cheaper hybrid" concept this case study proposes, the gap identified in §45/§46 may be smaller than presented, or the proposal may already partially exist under a different name.

**Effect if wrong:** §50's "does not exist" framing for a mid-tier format would need softening to "exists in nascent form but isn't yet siting-optimised or separately margin-tracked."

**Confidence:** Low-medium — the sources reviewed did not provide enough detail on Pathshala's specific operating model to resolve this cleanly.

### A4 — A staff-light micro-centre format, without dedicated live teaching faculty, can maintain acceptable student outcomes when delivering pre-recorded/streamed content

This is the central operational bet of the proposal (§50) and is unmodelled — I have no PW-specific or category-wide data confirming outcome parity between live and streamed-with-local-mentor formats.

**Confidence:** Low-medium — the softest assumption in this document, which is why §51.5 A2 and §54's Arm C are both designed to test it directly before any scaling decision.

### A5 — PhysicsWallah's own online-enrollment data has sufficient geographic granularity (pincode or city-level) to meaningfully inform centre siting

Assumed based on the existence of a mobile app with presumably registered addresses/locations, not confirmed from any public disclosure of PW's actual data infrastructure.

**Confidence:** Medium.

---

## Part 2 — Derivations

| # | Derivation | Inputs | Result | Where |
|---|---|---|---|---|
| **D1** | Revenue-per-student multiple, offline vs online | 40,404.6 ÷ 3,682.8 | **≈11.0x** | §13.1 |
| **D2** | Offline students as share of total student base, FY25 | 3.3L ÷ (41.3L + 3.3L) | **≈7.4%** | §5, §13.1 |
| **D3** | Offline revenue as share of total revenue, FY25 | 1,351.9 ÷ (1,404.1+1,351.9) | **≈49.1%** | §5, §13.1 |
| **D4** | FY24→FY25 revenue growth | (2,886.6−1,940.7)/1,940.7 | **≈48.7%** (reported elsewhere as ~49–53% depending on exact FY24 base used) | §5, §13.3 |
| **D5** | FY25→FY26 revenue growth | (3,899.5−2,886.6)/2,886.6 | **≈35.1%** | §5, §13.3 |
| **D6** | Loss reduction, FY24→FY25 | (1,131.1−243.3)/1,131.1 | **≈78.5%** | §5, §13.3 |
| **D7** | Loss reduction, FY25→FY26 | (243.3−24.4)/243.3 | **≈90.0%** | §13.3 |
| **D8** | Offline centre count growth, FY25→FY26 | (353−198)/198 | **≈78.3%** | §5, §13.4 |
| **D9** | Offline centre count growth, FY24→FY25 | (198−126)/126 | **≈57.1%** | §13.4 (cross-referenced against the "57%" figure independently reported by Inc42) |

**The one caveat that applies to D1–D3 collectively:** these figures come from FY25 data specifically; FY26 online/offline student-count splits were not found in the sources reviewed for this document, so the 11x multiple and the 7.4%/49.1% shares are not confirmed to still hold at the same magnitude in FY26, even though FY26 revenue figures for both segments were available and used elsewhere (§13.1).

---

## Part 3 — Constructs

| # | Construct | Detail | Where |
|---|---|---|---|
| **C1** | **PW Micro-Centre** | The entire proposal — staff-light format, density-based siting, pricing construct | §50 |
| **C2** | **Cost-Adjusted Access Rate (CAAR)** (North Star) | §31 |
| **C3** | **Online-Density Heatmap, Format Margin Tracker, Stepping-Stone Conversion Rate** | §32 |
| **C4** | **Personas Ankit, Rhea, Meena** | §20 |
| **C5** | **All RICE inputs and the stress rule** | §47 |
| **C6** | **Acceptance-criteria bars** | §51.5 |
| **C7** | **The three-arm A/B design, including Arm C as falsifier** | §54 |
| **C8** | **Technical architecture and data-flow reconstructions** | §41, §42 |
| **C9** | **The "rebuilding Kota" framing and the mission-vs-growth-engine tension** | §5, §46 — an interpretive reading of public disclosures, not a PhysicsWallah-stated characterisation of its own strategy |

---

## Part 4 — What is not in this document

- **No screenshots or authenticated-session data.**
- **No PhysicsWallah-disclosed segment-level (online vs. offline) profitability data.** The negative-margin claim for offline (A1) rests on a single secondary source's reconstruction.
- **No independent verification of the SPTulsian brokerage's methodology** for the offline margin estimate.
- **No FY26 online/offline student-count split**, only revenue figures — the 11x multiple and related shares (§13.1) are FY25-specific.
- **No claim about PW Pathshala's actual operating model or cost structure** beyond what public sources describe it as ("hybrid") — A3 flags this as a real gap in this analysis.

---

## Part 5 — The single sentence version

If only one line of this file survives: **the entire case study depends on assumption A1 — that PhysicsWallah's offline segment runs at a genuinely negative net margin, based on a single brokerage's reconstruction of FY25 filings rather than company-disclosed segment accounting — and the single test that would most directly confirm or refute it is PhysicsWallah itself disclosing segment-level (not just revenue-level) profitability, which this document cannot compel and has not seen.**

---

*Companion to [README.md](./README.md) · Day 53 of 90*
