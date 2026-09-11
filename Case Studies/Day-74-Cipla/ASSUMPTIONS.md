# ASSUMPTIONS — Day 75, Cipla Limited

**Case study:** Day 75 of 90 · Cipla Limited (CIN L24239MH1935PLC002380)
**Period examined:** Q1 FY27, quarter ended 30 June 2026, results 23 July 2026
**Verification:** `verify.py`, 107 checks, all passing
**Written:** 10 September 2026

Part 1 states what is assumed and gives the rival reading equal weight. Part 2 shows the arithmetic. Part 3 lists what the author invented. Part 4 states what would falsify the thesis. Part 5 records what could not be found out.

---

## Part 1 — Assumptions

### A1 (load-bearing) — that the profit decline reflects margin concentration in episodic products

**The assumption.** The ₹511 Cr profit decline against a ₹407.24 Cr North American revenue decline indicates that a small share of revenue was carrying a disproportionate share of group margin, and that the concentration is structural to limited-competition generics rather than a one-off.

**What supports it.** The ratio is exact from disclosed figures: profit fell **1.25×** the segment revenue that disappeared, and the North American decline accounts for **79.69%** of the profit lost. Simultaneously India, Africa and EM/Europe added **₹612.33 Cr — 1.50× the North American decline** — and total revenue still rose, so revenue substitution demonstrably happened while margin substitution did not. Management's own explanation names two specific molecules, lenalidomide and lanreotide, which is the signature of exclusivity-window economics.

**The rival reading, given equal weight, and it has real force.** **Roughly seven points of the North American decline is currency**, not business: the segment fell 28% in USD and 21% in rupees. So the ₹407.24 Cr rupee figure overstates the operational revenue lost, which mechanically **inflates the 1.25× ratio.** Beyond that, the ₹511 Cr profit decline is a *consolidated* number affected by tax, finance cost, forex and any one-time items in either period — none of which is attributed by segment. Cipla does not publish segment margins, so the claim that the lost revenue carried extraordinary margin is an inference from a consolidated movement, not a measurement. A reader could reasonably attribute part of the decline to cost inflation, war-related cost pressure that management cited, or under-utilisation, and this analysis cannot rule those out.

**Why the case study proceeds anyway, and where it stops.** It proceeds because the *direction* survives any plausible correction: profit fell by more than any reasonable estimate of the operational revenue lost, and the growing segments' ₹612.33 Cr replaced almost none of it. **It stops short of asserting the precise margin on the lost products.** §14, §55 and §64 all state the currency caveat explicitly, and §64 states plainly that the ratio is inflated by translation.

**What would settle it.** Segment-level margin disclosure, or a constant-currency segment view. Neither is published.

### A2 — that "episodic versus annuity" is a real distinction in this business

The §16 double Porter's run, the §36 sawtooth characterisation and the whole of §50 rest on splitting revenue by durability. **Cipla reports by geography, not by durability.** The distinction is a well-established feature of generic pharmaceutical economics and is consistent with management's own high-base explanation, but it is the author's framing. K1 in §53 exists precisely because writing an auditable classification rule may prove impossible — many products sit between a window and an annuity.

### A3 — that the two named molecules explain most of the decline

Management attributed the high base to lenalidomide and lanreotide. **No product-level revenue or margin figure is published for either.** This case study therefore cannot say what share of the ₹511 Cr those two products represent, and does not claim to. Every quantified finding uses segment-level figures only.

### A4 — that prior-year comparatives can be derived from reported growth rates

Prior-year revenue (₹6,958.94 Cr), prior-year North America (₹1,939.24 Cr) and the rupee contributions of India, Africa and EM/Europe are all back-derived from reported growth rates rather than separately reported in the sources used. Growth rates are quoted to one decimal or as whole numbers, so each derived base carries rounding sensitivity of a few crore. **No conclusion depends on the precise base**, and every growth finding uses the reported rate directly.

### A5 — that the FY26 guidance comparison is like-for-like

The 4.75-point guidance cut compares an FY27 corridor of 18.5–20% against an FY26 corridor of 23.5–24.5%. Both are EBITDA margin guidance for a full year, so the comparison is structurally sound. It assumes no change in the definition of EBITDA between the two guidance statements, which is not separately confirmed in the sources used.

---

## Part 2 — Derivations

Every figure below is asserted in `verify.py`. Tags map to that file.

### D1 — Record revenue, collapsing profit

| Measure | Value | Tag |
|---|---|---|
| PAT change, computed | **−39.31%** | D1a |
| Gap to reported −39.2% | **0.11 pp** | D1b |
| Implied prior-year revenue | **₹6,958.94 Cr** | D1c |
| Revenue increase | **₹160.06 Cr** | D1d |
| Swing, revenue vs PAT growth | **41.50 pp** | D1e |
| EBITDA margin computed | **16.74%** | D1f |
| PAT margin computed | **11.08%** | D1g |
| PAT decline | **₹511.00 Cr** | D1h |

### D2 — The US roll-off

Implied prior-year North America **₹1,939.24 Cr** (D2a), a decline of **₹407.24 Cr** (D2b). The PAT decline is **1.25×** that (D2c); the NA decline is **79.69%** of the PAT decline (D2d). In USD the implied prior year is **$225 mn** (D2e), and the INR and USD decline rates differ by **7.00 points** (D2f) — the currency effect that A1 concedes.

### D3 — Segments

The four disclosed segments sum to **₹6,960 Cr** (D3a), leaving **₹159 Cr — 2.23%** unattributed (D3b, D3c). Shares: India **48.49%**, North America **21.52%**, One Africa **13.72%**, EM and Europe **14.03%** (D3d–D3g). Rupees added: India **₹369.86 Cr**, Africa **₹104.68 Cr**, EM/Europe **₹137.79 Cr** (D3h–D3j) — **₹612.33 Cr** together (D3k), or **1.50×** the NA decline (D3l). India's addition alone is **72.38%** of the PAT decline (D3m).

### D4 — Guidance

FY27 midpoint **19.25%**, FY26 midpoint **24.0%** (D4a, D4b) — a cut of **4.75 points** (D4c). The actual 16.7% is **1.80 points** below the FY27 floor (D4d), **2.55 points** below its midpoint (D4e) and **7.30 points** below last year's midpoint (D4g) — **86.75%** of the current midpoint (D4f). At the FY27 midpoint this quarter's revenue would have produced **₹1,370.41 Cr** of EBITDA (D4h), so **₹178.41 Cr** was foregone (D4i).

### D5 — North America ambition

Annualised run rate **$648 mn** (D5a) — **64.80%** of the $1bn target (D5b), a gap of **$352 mn** (D5c) requiring a **54.32%** uplift on the current quarterly rate (D5d). Approved, tentative and pending filings total **160** (D5e), **57.55%** of the 278-filing portfolio (D5f).

### D6 — India and capital

R&D **6.83%** of revenue (D6a). Chronic mix is **4.60 points** below target (D6b). Branded Rx grew **3.40 points** faster than One India overall (D6c); diabetes grew **3.58×** the One India rate (D6d). Foracort is **7.24%** of annualised India revenue (D6e). Net cash is **1.33×** quarterly revenue (D6f), **15.82×** total debt (D6g) and **33.34%** of annualised revenue (D6h). The annualised run rate is **1.02×** FY26 actual revenue (D6i).

### D7 — Stress rule

**64.80%**, the North America run rate against the $1bn exit target (D7a). Alternatives computed and not used: margin against the FY26 guidance midpoint at **69.58%** would be harsher (D7b), and against the FY27 midpoint at **86.75%** more generous (D7c).

### D8 — RICE

| Initiative | Base | Stressed |
|---|---|---|
| Margin recovery: utilisation (exempt) | 605.12 | **605.12** |
| India chronic mix to 65% | 371.75 | 240.90 |
| **Cliff Calendar (PROPOSED)** | **108.14** | **70.08** |
| Working capital and cost (exempt) | 91.12 | 91.12 |

Proposal ranks **3rd at baseline, 4th and last under stress** (D8d, D8e). `verify.py` asserts it is the **weakest stressed initiative at baseline** (D8f) and that it finishes last (D8g). The stressed winner beats it by **8.64×** (D8h).

---

## Part 3 — Constructs

Everything here is the author's invention. None is a Cipla disclosure, plan or statement.

| Construct | What it is |
|---|---|
| **Cliff Calendar** | The proposed instrument: published episodic/annuity classification, an eight-quarter revenue-at-risk schedule, and replacement capital pre-committed against it |
| **RPR/100** | Proposed North Star — replacement pipeline revenue per ₹100 of *episodic revenue expiring within eight quarters*, four conjunctive conditions |
| **QCR-90** | Proposed guardrail — quality compliance rate at the 90th percentile of site utilisation, by site |
| The episodic / annuity seam | The §16 double Porter's framing; **not a reported segmentation** (A2) |
| The sawtooth characterisation | §36 — an analytical construction |
| Prior-year comparatives | Back-derived from reported growth rates (A4) |
| Implied margin on the lost US revenue | Inferred from a consolidated profit movement, not measured (A1, A3) |
| RICE inputs | All reach, impact, confidence and effort values in §47 |
| Stress rule application | 64.80% is derived from disclosed figures; using it as a RICE multiplier is the author's construction |
| Phase 0 kill criteria | K1, K2, K3 in §53, including the judgement that K1 is most likely to fire |
| §54 arms and R1 rule | The falsification design, the 15-point threshold and the four-quarter window |
| Personas | §20 — illustrative, not researched individuals |

---

## Part 4 — What would change my mind

1. **Segment-level margin disclosure, or a constant-currency segment view.** This is the direct test of A1. If North American margin was not extraordinary, the 1.25× ratio has another explanation — cost inflation, under-utilisation, or one-time items — and the concentration thesis weakens considerably.
2. **Product-level disclosure showing lenalidomide and lanreotide were a small share of the decline.** A3 would fail, and the profit fall would be a broader operating problem rather than a cliff.
3. **Margin recovering into the 18.5–20% corridor in H2 FY27 as guided.** That would confirm management's utilisation-and-launch explanation and make the episodic-concentration framing less urgent, even if still true.
4. **K1 firing in Phase 0** — no auditable line between episodic and annuity revenue. The proposal would then be unbuildable as specified, not merely last in the ranking.
5. **Evidence that expiries were already planned for internally** and the gap was an approval delay rather than a planning failure. K3 tests this; if it fires, no calendar fixes the problem because the problem sits with a regulator.

---

## Part 5 — What could not be found out

- **Segment-level gross or EBITDA margin.** The single most consequential gap: without it, the implied margin on the lost North American revenue is an inference from a consolidated movement (A1).
- **Product-level revenue or margin for any molecule**, so the share of the decline attributable to lenalidomide and lanreotide cannot be established (A3).
- **Any exclusivity expiry dates or forward view of revenue at risk** — the quantity §50 is designed to publish.
- **The composition of the ₹159 Cr unattributed segment residual** (2.23% of revenue).
- **The split of guided margin recovery** between utilisation, mix, cost easing and productivity; management named all four without quantifying any.
- **Whether the ₹1,300 Cr prior-year comparative contained one-time items of its own**, which would change the 39.31% decline.
- **A constant-currency segment view**, so the operational versus translation split of the North American decline cannot be isolated beyond the ~7-point gap between the INR and USD rates.
- **Adherence, inhaler-technique or clinical outcome data** in the respiratory franchise, despite it being the deepest business and the one where product experience most affects results.
- **A filed transcript** of the Q1 FY27 earnings call in the sources used; call detail comes from coverage and is graded 🟡 accordingly.
