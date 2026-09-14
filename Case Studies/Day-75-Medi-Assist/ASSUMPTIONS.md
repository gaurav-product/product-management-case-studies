# ASSUMPTIONS — Day 74, Medi Assist Healthcare Services Limited

**Case study:** Day 74 of 90 · Medi Assist Healthcare Services Limited (CIN L74900KA2000PLC027229)
**Period examined:** Q1 FY27, quarter ended 30 June 2026, results 8 August 2026
**Verification:** `verify.py`, 107 checks, all passing
**Written:** 9 September 2026

Part 1 states what is assumed and gives the rival reading equal weight. Part 2 shows the arithmetic. Part 3 lists what the author invented. Part 4 states what would falsify the thesis. Part 5 records what could not be found out.

---

## Part 1 — Assumptions

### A1 (load-bearing) — that fee compression reflects structural pressure from insurers who can in-source

**The assumption.** Revenue per rupee of premium falling 2.13% is not noise. It reflects a durable bargaining shift in favour of insurers who increasingly have the option to bring claims administration in-house, and it will continue.

**What supports it.** The cascade is exact and drawn entirely from disclosed growth rates: premiums +26.8%, revenue +24.1%, EBITDA +14.3%, giving −2.13%, −7.90% and a compounded **−9.86%** on EBITDA per rupee of premium. Management named the pressure directly, describing competitive pressure from insurers developing internal capabilities and citing technology offerings as the mitigation — so the mechanism is the company's own characterisation, not an outside theory. And the strategic response is consistent with it: a licensing business aimed at insurers, growing 55.5%.

**The rival reading, given equal weight, and it is strong.** **One quarter of rate movement cannot distinguish structural compression from ordinary causes.** A 2.13% decline is fully consistent with mix shift toward larger accounts that carry lower rates by design — which is what winning share looks like — or with the Paramount book carrying different pricing, or with normal competitive renegotiation in a growing market. Nothing in the disclosure attributes the decline to in-sourcing. Meanwhile the core franchise **gained share to 37.6%** and grew premiums 26.8%, which is not what a business losing customers to vertical integration looks like.

**Why the case study proceeds anyway, and where it stops.** It proceeds because the *asset* argument in §16 does not depend on the timing: claims processing is replicable and a multi-insurer tariff book is not, whether or not any insurer in-sources this year. **It stops well short of claiming disintermediation is underway.** §14 states the core is not weak, §64 states that a single quarter's rate movement cannot separate the explanations, and §55 makes it a multi-quarter test rather than a verdict.

**What would settle it.** Three or four quarters of revenue-per-rupee-of-premium. If the rate stabilises while premium keeps growing, A1 is wrong and the compression was mix.

### A2 — that the hospital network is the least replicable asset

The §16 seam, the §37 network-effect argument and the whole of §50 rest on the claim that a multi-insurer tariff and settlement book is something no single insurer can reconstruct. That follows from the structure of the asset — it accretes only from serving many insurers at once — but **Medi Assist discloses nothing about network size, tariff coverage, settlement performance or the share of claims settled at negotiated rates.** So the asset is argued for, not measured. K1 and K3 in §53 exist to test separability and willingness to pay before anything is built, and §64 states this plainly.

### A3 — that technology revenue can be derived from a disclosed share

Technology revenue of ₹7.81 Cr is computed as 3.3% of consolidated revenue; the absolute figure is not disclosed. Rounding in the disclosed share gives roughly ±₹0.12 Cr of sensitivity. Every finding using it — 16.26% of EBITDA, ₹1.12 Cr per AI contract, ₹31.22 Cr annualised — inherits that, and none is load-bearing for the central cascade.

### A4 — that the adjusted PAT figure is the right operating measure

Adjusted PAT of ₹24.48 Cr strips the ₹3.12 Cr derivative remeasurement gain arising on the Mayfair stake purchase. **This is the company's own adjustment**, not one constructed here, and the resulting 8.17% growth is treated throughout as the operating result. The prior-year comparative is not similarly adjusted because no equivalent one-time item is disclosed for Q1 FY26; if one existed, the 8.17% would change.

### A5 — that Q1 margin is depressed by integration rather than structurally

EBITDA margin of 20.29% sits 2.70 points below the historical 23.0%, and management attributes the gap to the Paramount integration with recovery guided to end FY27. This case study accepts that attribution for the margin specifically — it is the fourth consecutive quarter of sequential improvement, which is consistent with a recovering integration — while noting that the *premium-level* compression in A1 is a separate question that integration does not explain.

---

## Part 2 — Derivations

Every figure below is asserted in `verify.py`. Tags map to that file.

### D1 — Headline and adjusted profit

| Measure | Value | Tag |
|---|---|---|
| Revenue growth, computed | **+24.12%** | D1a |
| Reported PAT growth, computed | **+21.94%** | D1b |
| Adjusted PAT | **₹24.48 Cr** | D1c |
| Adjusted PAT growth | **+8.17%** | D1d |
| Reported ÷ adjusted growth | **2.69×** | D1e |
| Derivative gain as % of reported PAT | **11.30%** | D1f |
| EPS growth | **+16.67%** | D1g |
| PAT growth minus EPS growth | **5.28 pp** | D1h |
| Implied share-count increase | **+4.52%** | D1i |
| PAT margin | **11.67%** | D1j |

### D2 — The cascade

Revenue per rupee of premium **−2.13%** (D2a); EBITDA per rupee of revenue **−7.90%** (D2b); the two compound to EBITDA per rupee of premium **−9.86%** (D2c), and the identity check confirms the compounding is exact (D2d). Premium growth exceeded revenue growth by **2.70 points** (D2e), revenue growth exceeded EBITDA growth by **9.80 points** (D2f), and premium growth exceeded EBITDA growth by **12.50 points** (D2g). At group level, premium growth exceeded revenue growth by **4.00 points** (D2h).

### D3 — Margins

EBITDA margin computed **20.29%** (D3a), down **1.70 points** year on year (D3b) and **2.70 points** below the historical level (D3c) — **88.26%** of it (D3d). Implied prior-year EBITDA **₹41.99 Cr** (D3e). At the historical 23.0% margin this quarter's revenue would have produced **₹54.40 Cr** (D3f), so **₹6.40 Cr** of EBITDA was foregone in the quarter (D3g).

### D4 — The hedge

Technology revenue **₹7.81 Cr** (D4a) — **16.26%** of EBITDA (D4b), **₹31.22 Cr** annualised (D4c). Mayfair is **4.27%** of revenue (D4d); technology plus Mayfair **7.57%** (D4e), leaving core TPA at **92.43%** (D4f). Technology grew at **2.30×** the consolidated rate (D4g), at **₹1.12 Cr** per signed AI contract (D4h).

### D5 — Holding company

Standalone revenue grew **34.96%** (D5a) and standalone PAT **63.99%** (D5b). Standalone revenue is **24.94%** of consolidated (D5c) while standalone PAT is **47.66%** of consolidated PAT (D5d) — standalone PAT growth running at **2.92×** the consolidated rate (D5e), at a **22.30%** standalone PAT margin (D5f).

### D6 — Scale

Annualised revenue **₹946.08 Cr** (D6a). Group market share **37.6%** (D6b). Retail claims still to migrate **20.0%**, group claims **5.0%** (D6c, D6d). The ₹2 dividend is **53.91%** of quarterly EPS (D6e). The stock fell **5.32%** on results day (D6f).

### D7 — Stress rule

**3.3%**, technology's share of consolidated revenue (D7a). Alternatives computed and not used: technology plus international at **7.57%** (D7b) and technology's **16.26%** share of EBITDA (D7c), both more generous.

### D8 — RICE

| Initiative | Base | Stressed |
|---|---|---|
| Complete migration, extract leverage (exempt) | 85.15 | **85.15** |
| Technology licensing scale-up | 37.84 | 1.25 |
| **Network Ledger (PROPOSED)** | **8.28** | **0.27** |
| Post-integration cost rationalisation (exempt) | 6.31 | 6.31 |

Proposal ranks **3rd at baseline, 4th and last under stress** (D8a, D8b). `verify.py` asserts it is the **weakest stressed initiative at baseline** (D8c) and that it finishes last (D8d). The stressed winner beats it by **311.69×** (D8e).

---

## Part 3 — Constructs

Everything here is the author's invention. None is a Medi Assist disclosure, plan or statement.

| Construct | What it is |
|---|---|
| **Network Ledger** | The proposed product: a separately-priced licence to the multi-insurer hospital tariff and settlement book, decoupled from administration |
| **NLC/1k** | Proposed North Star — network-licensed covered lives per 1,000 *covered lives administered*, four conjunctive conditions including survival of contract termination |
| **TDR-90** | Proposed guardrail — tariff dispersion at the 90th percentile of hospital concentration, where **convergence** is the alarm |
| The replicable / non-replicable seam | The §16 double Porter's framing; not a reported segmentation (A2) |
| The two growth loops | §36 — an analytical construction |
| Technology revenue in rupees | Derived from a disclosed percentage share (A3) |
| The in-sourcing trajectory | Management named the pressure; the direction and pace are the author's inference (A1) |
| RICE inputs | All reach, impact, confidence and effort values in §47 |
| Stress rule application | 3.3% is disclosed; using it as a RICE multiplier is the author's construction |
| Phase 0 kill criteria | K1, K2, K3 in §53, including the judgement that K1 is most likely to fire |
| §54 arms and R1 rule | The falsification design and the NLC/1k threshold of 50 |
| Personas | §20 — illustrative, not researched individuals |

---

## Part 4 — What would change my mind

1. **Revenue per rupee of premium stabilising over three or four quarters** while premium keeps growing. That would make the 2.13% decline mix rather than structural pressure, and A1 would be wrong.
2. **Disclosure attributing the fee decline to account mix** — larger accounts at lower rates, or Paramount book pricing. Same effect: the compression becomes a consequence of winning share rather than of losing bargaining power.
3. **Evidence that no material premium has moved in-house at any large insurer.** The in-sourcing threat is management commentary plus my inference; a disclosed retention figure showing it is not happening would substantially weaken §16's urgency.
4. **K1 or K2 firing in Phase 0.** If existing contracts prohibit secondary use of tariff data, or competition counsel will not clear licensing at 37.6% share, the proposal is not merely last in the ranking — it is unbuildable.
5. **Margin recovering to 23% by end FY27 as guided.** That would confirm A5, restore ₹6.40 Cr a quarter, and show the integration explanation was complete — making the case for a new revenue line much less pressing.

---

## Part 5 — What could not be found out

- **Anything about the network asset** — hospital count, tariff coverage, settlement turnaround, or the share of claims settled at negotiated rates. The most consequential gap, because §50 proposes monetising exactly this and A2 must therefore argue rather than measure.
- **Adjudication-quality data** — approval rate, denial rate, turnaround time, appeal-overturn rate. Not published by Medi Assist and, so far as this research found, not published by any Indian TPA.
- **Insurer client count and concentration**, so the exposure to any single client in-sourcing cannot be sized.
- **How much premium, if any, has moved in-house** at any insurer — the quantity A1 depends on.
- **Technology revenue in absolute terms as disclosed**; it is derived here from a percentage share (A3).
- **The terms of existing administration contracts** regarding secondary use of negotiated tariff data — the subject of K1.
- **Any detail of the Enforcement Directorate matter** beyond the auditor's emphasis of matter and management's statement of no adverse impact.
- **Mayfair's profitability**, disclosed only as revenue and a growth rate.
- **A filed transcript** of the Q1 FY27 earnings call in the sources used; call detail comes from coverage and is graded 🟡 accordingly.
