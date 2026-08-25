# ASSUMPTIONS — Day 59, ixigo (Le Travenues Technology Limited)

Companion to `README.md`. Everything in the case study that is not a directly disclosed figure appears here. Nothing in this file is an ixigo statement unless quoted as one.

---

## Part 1 — Assumptions

### A1 (load-bearing) — that flight take-rate compression is (at least partly) durable, not purely a one-quarter macro shock

The thesis treats the 9.17%→8.41% flight take-rate compression and the resulting fall in flight contribution margin as a real product-strategy problem worth building for. Management's own account, however, attributes the pressure explicitly to "fare inflation arising from the West Asian conflict" (per Inc42's Q1 FY27 coverage) — an external, plausibly temporary shock tied to crude oil and jet fuel costs, not a structural loss of pricing power.

**Rival reading, given equal weight.** If the West Asia conflict resolves and airfares normalise, flight take rate could recover toward its prior level with no product intervention required, and the flight-diversification rationale for ixigo Corridor weakens considerably — though the cross-modal convenience value would not disappear, since buses and trains remain genuinely useful substitutes on many corridors regardless of flight pricing.

**Why the case study proceeds anyway.** Two facts sit alongside the conflict-linked explanation without being explained by it. First, DGCA-reported domestic passenger traffic was already falling **before and independent of** any single conflict-linked fare spike (−4.8% YoY in July 2026 alone), suggesting industry-wide capacity and demand dynamics that predate and may outlast the current shock. Second, even if the flight-side motivation is temporary, a working cross-modal comparison tool has standing value on its own terms — it does not require flights to stay weak to be useful, only for the three modes to remain genuinely substitutable on some corridors, which they already are.

**How A1 dies.** §55's early-warning row: track flight take rate against a conflict/fuel-cost proxy over the next two to three quarters. If take rate recovers toward 9%+ as the geopolitical shock subsides and flight contribution margin turns positive YoY, A1's "durable pressure" reading is wrong, and Corridor's justification should shift explicitly from margin defence to pure convenience.

### A2 — that Q1 FY26 PAT (₹18.94 Cr) is a reliable YoY comparator

ixigo's own official Q1 FY26 media release disclosed profit **before tax** (₹28.7 Cr, +76% YoY) but did not disclose profit after tax as a headline figure. The ₹18.94 Cr Q1 FY26 PAT figure used throughout this document for YoY comparisons is not from that original release; it is the comparative figure multiple independent Q1 FY27 press reports (Entrackr, Inc42, Investing.com — three convergent, independent figures: 18.94, 18.9, 18.91) cite as the prior-year comparative, presumably drawn from ixigo's own Q1 FY27 filing's comparative column. It is graded 🟡 Medium rather than 🟢 High for this reason — convergent secondary sourcing, not a directly located primary document for that specific line.

### A3 — that "gross take rate" and "revenue as a share of GTV" are different, non-reconciling metrics

§39's flight take-rate figures (9.17%→8.41%, ixigo's own disclosed metric) and this document's own revenue/GTV calculation (4.47%) do not match. Rather than force one to explain the other, or silently pick the more flattering one, both are reported with the gap flagged as unreconciled (Appendix A-2). A plausible explanation — that "gross take rate" is computed on a different base such as gross booking value before certain pass-through costs — is offered but not confirmed.

### A4 — that the Q1 FY26 revenue baseline (used for GTV/revenue YoY math) is ₹314.5 Cr, not the ₹315.42–316.05 Cr figures some secondary sources imply

ixigo's own official Q1 FY26 media release states revenue from operations of ₹314.5 Cr. Two secondary sources computing Q1 FY27's YoY growth imply a very slightly different Q1 FY26 base (₹315.42 Cr and ₹316.05 Cr respectively) — a band of under 0.5%, immaterial to any conclusion in this document, but noted for completeness. The official, directly-disclosed ₹314.5 Cr figure is used as the primary source throughout.

### A5 — that MakeMyTrip is a fair comparator for the "same quarter, opposite direction" argument

MakeMyTrip is a larger, more metro-skewed, hotel-and-packages-weighted business than ixigo, and its Q1 FY27 profit decline was driven specifically by finance costs on convertible senior notes — a balance-sheet structure ixigo does not share. The comparison in §14 is used for one narrow purpose: to show that the same quarter's flight/air-travel fare pressure showed up in both companies' numbers independently, which is stronger evidence of a shared external cause than either company's disclosure alone. It is not used to argue the two companies are otherwise comparable in scale or model.

---

## Part 2 — Derivations

Every figure below is reproduced in `verify.py`, which must pass before publication.

| ID | Derivation | Inputs | Result |
|---|---|---|---|
| D1 | Interest income as % of PAT | ₹29.15 Cr ÷ ₹34.24 Cr | **85.13%** |
| D2 | Adjusted EBITDA YoY change | (29.24 − 31.4) ÷ 31.4 | **−6.88%** |
| D3 | Headline EBITDA YoY change | (53.52 − 32.48) ÷ 32.48 | **+64.78%** |
| D4 | Revenue YoY change | (356.75 − 314.5) ÷ 314.5 | **+13.45%** |
| D5 | GTV YoY change | (5524.33 − 4644.7) ÷ 4644.7 | **+18.94%** |
| D6 | PAT YoY change | (34.24 − 18.94) ÷ 18.94 | **+80.78%** |
| D7 | Flight take-rate compression | 9.17% − 8.41% | **0.76 pp (8.29% relative)** |
| D8 | Flight revenue/GTV take rate | 104.56 ÷ 2341.84 | **4.47%** |
| D9 | Train revenue/GTV take rate | 141.05 ÷ 2138.86 | **6.60%** |
| D10 | Bus revenue/GTV take rate | 102.55 ÷ 947.43 | **10.82%** |
| D11 | Contribution margin rate, both years | 144.94÷356.75 ; 128.1÷314.5 | **40.63% vs 40.73%** (−10 bps) |
| D12 | Total expense growth vs revenue growth | (337.76−294.35)÷294.35 vs D4 | **14.75% vs 13.45%** (expenses outgrew revenue by 1.3 pp) |
| D13 | Interest income annualised vs FY26 full-year Adj. EBITDA | 29.15×4 ÷ 120.9 | **96.53%** |
| D14 | Implied hotels contribution margin (residual) | 41.04+52.74+54.22−144.94 | **−₹3.06 Cr = −₹61.20/guest on 0.5 Mn heads-on-beds** |
| D15 | RICE stress rule | 0.42 Cr MTU ÷ 8.54 Cr MAU | **4.92%** |
| D16 | RICE stressed scores | R×I×C÷E×100, stressed R = R×0.0492 | Corridor **85.0 → 4.18**, falling from 3rd to last of 4 |

---

## Part 3 — Author-constructed content

Not ixigo artefacts. Constructed by the author, with reasoning:

- **Personas (§20).** Three composite personas built from disclosed city-tier and segment facts. No ixigo persona research is public.
- **The user journey's cost-vs-price column (§22).** The stages are inferable from disclosed product structure (three mode-first search tabs); the attribution of where cost is created versus where price is shown is the author's analysis and is the mechanism of the whole thesis.
- **RICE inputs (§47).** Reach, Impact, Confidence and Effort are author estimates. Only the **stress multiplier (4.92%)** derives from ixigo's own disclosed MAU/MTU figures. The relative ordering, not the absolute scores, is what the section argues.
- **ixigo Corridor (§50), the PRD (§51) and the Ground Card wireframe (§52).** Entirely the author's proposal. ixigo has disclosed nothing resembling a cross-modal comparison product; the company's own August 2026 disclosed roadmap move (corporate/SME travel) is a separate, real, factual item kept clearly distinct in §56.
- **RCJ/1k and GTP-90 (§31).** Author-designed metrics. Neither is an ixigo metric and no Indian OTA is known to publish either.
- **Kill criteria K1–K3 (§53), decision rule R1 (§54), and the RICE initiative set in §47** (aside from ixigo Corridor itself, the other three candidate initiatives — PNR Guarantee expansion, direct hotel supply expansion, and flight NDC/direct-content recovery — are plausible author-proposed initiatives built around real disclosed facts, not disclosed ixigo plans).

---

## Part 4 — What would change my mind

1. **ixigo disclosing flight take rate recovering to 9%+ over the next two quarters as fare inflation subsides**, with flight contribution margin turning positive YoY. That would confirm A1's "durable pressure" reading was wrong and this case study's flight-side framing overstated a temporary shock.
2. **ixigo or a credible third party publishing a genuine India OTA TAM.** §13's restricted-form treatment would no longer be necessary.
3. **Evidence that ixigo already tested a cross-modal comparison internally and it underperformed.** That would materially change the confidence behind §50's proposal.
4. **The disclosed corporate/SME travel product launching with its own dedicated comparison or itinerary tooling** — that would suggest the company is already solving an adjacent version of the problem this case study identifies, on a different flight path than proposed here.
5. **A precise reconciliation of "gross take rate" against revenue/GTV** (A3) from ixigo directly — that would resolve Appendix A-2 and might change how §39's monetisation table should be read.

---

## Part 5 — What could not be found out

- **A reconciled basis for "gross take rate" versus revenue/GTV take rate** (A-2/A-3) — ixigo does not publish the calculation methodology for the disclosed 9.17%/8.41% figures.
- **Segment-level Adjusted EBITDA** (only group-level Adjusted EBITDA is disclosed; the segment contribution margins in §39 are the finest granularity available).
- **The precise driver split within the ₹43.41 Cr YoY increase in total expenses** (§30/§38) — how much is AI infrastructure, how much is hotels integration, how much is marketing, was not broken out in any source found.
- **Hotels segment GTV** — only contribution margin (derived, D14) and heads-on-beds are disclosed; GTV for hotels specifically was not found.
- **Any credible primary-sourced TAM for Indian online travel booking**, which is why §13 is run in restricted form.
- **EaseMyTrip and Yatra's Q1 FY27 segment-level results**, which would have allowed a fuller §14 comparator set; both file but a comparably deep reconciliation for both was out of scope here.
