# ASSUMPTIONS — Day 72, Entero Healthcare Solutions Limited

**Case study:** Day 72 of 90 · Entero Healthcare Solutions Limited (CIN L74999HR2018PLC072204)
**Period examined:** Q1 FY27, quarter ended 30 June 2026, board approved 7 August 2026
**Verification:** `verify.py`, 117 checks, all passing
**Written:** 7 September 2026

Part 1 states what is assumed and gives the rival reading equal weight. Part 2 shows the arithmetic. Part 3 lists what the author invented. Part 4 states what would falsify the thesis. Part 5 records what could not be found out.

---

## Part 1 — Assumptions

### A1 (load-bearing) — that the rising minority share is structural and will continue

**The assumption.** Minority interest at 26.68% of consolidated PAT, up from 7.86%, reflects a deliberate and continuing acquisition structure — buying 70–80% of distributors — and will keep rising while that structure is used for growth.

**What supports it.** The subtraction is exact: consolidated PAT ₹52.05 Cr minus PAT attributable to owners ₹38.16 Cr leaves ₹13.89 Cr. The stake percentages are disclosed in the FY26 annual report — Ramson 70%, Sai RK 70%, Well Wisher 70%, Anand Medilink 80% — so the mechanism is documented, not inferred. And the direction of travel is stated by the company itself: **53.40% of the quarter's growth was inorganic**, with a dual organic-and-inorganic strategy explicitly reaffirmed.

**The rival reading, given equal weight.** The jump from 7.86% to 26.68% in one year may be a **timing artefact** rather than a trend. FY26 was an unusually heavy acquisition year — seven deals — so Q1 FY27 is the first quarter carrying a full load of newly consolidated, majority-owned entities. As those entities' contribution normalises, and if future growth tilts organic (management guides ~23% growth *excluding* new acquisitions), the minority share could stabilise or fall. More importantly, **the acquired entities are profitable**: this is dilution of a rising number, and owners' PAT still grew 37% with consolidated EPS up 37.25%. A reading that treats 26.68% as value destruction would be wrong.

**Why the case study proceeds anyway, and where it stops.** It proceeds because the *disclosure* point holds under either reading: a company whose headline profit growth is 1.95× its shareholders' profit growth should be read on the second line, and most coverage of this quarter reported only the first. **It stops short of claiming the strategy is wrong.** §14, §36 and §58 all state that the structure is the price of the acquisitions working, not a flaw in them, and §55's first row makes the trajectory a multi-quarter test rather than a verdict.

**What would settle it.** Two more quarters of the same subtraction. If the minority share stabilises below 25% while organic growth carries the top line, A1 is wrong.

### A2 — that Entero operates as a federation rather than an integrated network

The §16 seam, the §22 journey and the §37 network argument all rest on the claim that a pharmacy served by one subsidiary cannot transact across the others. **Entero does not disclose its degree of operational integration.** This is an inference from the acquisition structure — 48 subsidiaries, majority stakes, founders retained — and from the absence of any described unified customer product in the results, presentation or call coverage. **It is entirely possible integration is further along than assumed**, in which case §50 proposes something that partly exists. K1 and K2 in §53 are written to establish this before any build, and it is flagged in §24, §64 and Appendix A-4.

### A3 — that the prior-year minority interest can be derived from the reported growth rate

Prior-year PAT attributable to owners is computed as ₹38.162 Cr ÷ 1.37 = ₹27.86 Cr, giving prior-year minority interest of ₹2.38 Cr and a 7.86% share. **The 37% growth figure is rounded**, so the derived base carries sensitivity: at 36.5% the prior share is roughly 7.6%, at 37.5% roughly 8.1%. The trajectory from under 8% to nearly 27% survives that range comfortably, but the precise figure is approximate and is labelled as derived wherever used.

### A4 — that Q1 margins are not a one-quarter peak

EBITDA margin of 5.0% matched the full-year guidance in the first quarter, and gross margin expanded 147 basis points. This case study does not extrapolate either. Management attributed the gross margin gain to scale-led procurement, MedTech mix and exit from low-margin business — the first two of which should persist and the third of which is one-off. No projection in this analysis assumes 5.0% is a floor.

---

## Part 2 — Derivations

Every figure below is asserted in `verify.py`. Tags map to that file.

### D1 — The headline

| Measure | Value | Tag |
|---|---|---|
| Consolidated PAT growth, computed | **+72.17%** | D1a |
| Total income growth, computed | **+38.44%** | D1b |
| Implied prior-year revenue | **₹1,404.12 Cr** | D1c |
| Consolidated EPS growth | **+37.25%** | D1d |
| PAT margin on revenue | **2.68%** | D1e |
| Non-operating income implied | **₹3.01 Cr** | D1f |

### D2 — Minority interest

Minority interest **₹13.89 Cr** (D2a) — **26.68%** of consolidated PAT (D2b). Prior-year owners' PAT **₹27.86 Cr** (D2c) implies prior-year minority interest of **₹2.38 Cr** (D2d), a **7.86%** share (D2e). The increase is **18.82 points** (D2f), a **3.39×** rise (D2g). Minority interest itself grew **484.43%** (D2j). Consolidated PAT growth exceeds owners' PAT growth by **35.17 points** (D2h); owners captured **51.27%** of the headline growth rate (D2i).

### D3 — Standalone versus consolidated

Standalone PAT is **6.64%** of consolidated PAT (D3a) and **9.06%** of PAT attributable to owners (D3b). Standalone EPS fell **50.63%** (D3c) while consolidated EPS rose 37.25% — a spread of **87.87 points** (D3h). Standalone total income is **5.48%** of consolidated revenue (D3d) at a **4.33%** PBT margin (D3e); income minus expenses reconciles exactly to the reported PBT (D3f), with implied tax of **₹1.15 Cr** (D3g).

### D4 — Bought versus built

Organic 17.8% plus inorganic 20.4% reconciles exactly to the reported 38.2% (D4a). Inorganic was **53.40%** of growth, organic **46.60%** (D4b, D4c). Like-for-like organic growth of 19.6% ran at **1.42×** market growth (D4d), a **5.80-point** premium (D4e). Reported growth was **2.77×** the market (D4f) and **15.20 points** above FY27 guidance (D4g).

### D5 — Margins

EBITDA is **43.86%** of gross profit (D5a). Gross profit **₹221.22 Cr**, EBITDA **₹97.02 Cr** (D5b, D5c). Prior-year gross margin **9.93%** (D5d). EBITDA grew **55.80 points** faster than revenue (D5e), **2.46×** as fast (D5f), and the Q1 margin equals full-year guidance exactly (D5g). FY26 EBITDA margin was **4.04%** (D5h), so Q1 FY27 is **0.97 points** ahead (D5i); FY26 PAT margin **2.21%** (D5j).

### D6 — Network

Quarterly revenue per warehouse **₹14.06 Cr** (D6a); per retail customer **₹2.70 lakh** (D6b). **27.80** SKUs per manufacturer (D6c); **521.74** retail customers per warehouse (D6d); **25.0** districts per state (D6e); **151.58** retail customers per district (D6f). Total customers **74,300** (D6g); **2.53** subsidiaries per state (D6h). The MedTech target is **12.88%** of annualised revenue (D6i).

### D7 — Stress rule

**6.64%**, standalone PAT as a share of consolidated PAT (D7a). Alternatives computed and not used: organic share of growth at **46.60%** (D7b) and owners' share of consolidated PAT at **73.32%** (D7c), both far more generous.

### D8 — RICE

| Initiative | Base | Stressed |
|---|---|---|
| Integration of past acquisitions (exempt) | 137.45 | **137.45** |
| MedTech scale-up | 112.50 | 7.47 |
| **Entero One (PROPOSED)** | **58.21** | **3.87** |
| Working capital reduction (exempt) | 51.75 | 51.75 |

Proposal ranks **3rd at baseline, 4th and last under stress** (D8b, D8c). `verify.py` asserts it is the **weakest stressed initiative at baseline** (D8d) and that it finishes last (D8e). The stressed winner beats it by **35.56×** (D8f).

---

## Part 3 — Constructs

Everything here is the author's invention. None is an Entero disclosure, plan or statement.

| Construct | What it is |
|---|---|
| **Entero One** | The proposed product: one group-level customer account, catalogue and credit line spanning all subsidiaries |
| **UOR/1k** | Proposed North Star — unified-order retailers per 1,000 *active retail customers*, four conjunctive conditions |
| **CLR-90** | Proposed guardrail — credit loss rate at the 90th percentile of centralised exposure, by district, against a pre-unification baseline |
| The network / federation seam | The §16 double Porter's framing; an inference, not a disclosed segmentation (A2) |
| The dilution loop | §36 — an analytical construction from the disclosed stake percentages |
| Prior-year minority interest | Derived from the reported 37% owners' growth (A3) |
| RICE inputs | All reach, impact, confidence and effort values in §47 |
| Stress rule application | 6.64% is computed from disclosed figures; using it as a RICE multiplier is the author's construction |
| Phase 0 kill criteria | K1, K2, K3 in §53, including the judgement that K1 is most likely to fire |
| §54 arms and R1 rule | The falsification design and the 8-point threshold |
| Personas | §20 — illustrative, not researched individuals |
| Internal transfer-price mechanic | §40 and §48; no such arrangement is disclosed |

---

## Part 4 — What would change my mind

1. **Minority share stabilising below 25% over the next two quarters** while organic growth carries the top line. That would make Q1 FY27 a timing artefact of a heavy FY26 acquisition year rather than a structural trend, and A1 would be wrong.
2. **Disclosure that the 48 subsidiaries are already operationally integrated** — a shared catalogue, single customer identity or group credit facility. A2 dies, and §50 proposes something that already exists.
3. **A disclosed minority buy-up programme.** If Entero is systematically acquiring the outstanding 20–30%, the leakage is a transitional financing cost rather than a permanent claim, and the whole framing softens.
4. **K1 firing in Phase 0** — systems fragmentation requiring replatforming rather than a master-data layer. The proposal is then not merely last in the ranking but wrongly scoped.
5. **Evidence that customer overlap between subsidiaries is negligible.** If pharmacies genuinely buy from one district's distributor and want nothing from elsewhere, the unified catalogue solves a problem that does not exist, and the network-effect critique in §37 loses its force.

---

## Part 5 — What could not be found out

- **The degree of operational integration across the 48 subsidiaries** — how many order, inventory and credit systems are in use, and whether a customer can be resolved across them. The most consequential gap; it forces A2 to remain an inference.
- **Customer overlap between subsidiaries**, which determines whether a unified catalogue has demand.
- **Any minority buy-up programme**, valuation basis, or the split of minority interest between individual subsidiaries. Because none of this is disclosed, buying out minorities is named as an opportunity in §46 but deliberately **not modelled** in §47 — every RICE input would have been invented.
- **Prior-year minority interest as a reported figure**; it is derived here from a rounded growth rate (A3).
- **Fill rate, on-time delivery, order completeness** or any service-quality metric — the things a pharmacy actually buys on.
- **The split of the 147 basis point gross margin expansion** between procurement scale, MedTech mix and exit from low-margin business; management named all three without quantifying them.
- **MedTech segment revenue and margin for the quarter**, disclosed only as a full-year FY27 target.
- **The financial terms of the Qurovia Lifesciences retail chemistry venture**, and whether it will source from Entero's own distribution network.
- **A filed transcript** of the Q1 FY27 earnings call in the sources used; call detail comes from coverage and is graded 🟡 accordingly.
