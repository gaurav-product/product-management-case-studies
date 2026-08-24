# ASSUMPTIONS — Day 58, Delhivery (Delhivery Limited)

Companion to `README.md`. Everything in the case study that is not a directly disclosed figure appears here. Nothing in this file is a Delhivery statement unless quoted as one.

---

## Part 1 — Assumptions

### A1 (load-bearing) — that the 14.18% realisation decline reflects price action, not acquired-book mix

The thesis reads express revenue per shipment falling from **₹67.63 to ₹58.04** as evidence that Delhivery bought volume with price. Delhivery does not publish realisation split by retained versus acquired accounts, and this is the case study's weakest joint.

**Rival readings, given equal weight:**

- **Acquired-book mix.** Delhivery completed the Ecom Express acquisition on 18 July 2025, ceased Ecom-branded volume manifestation, and migrated that customer base onto its own network. Ecom competed at lower price points. If a large share of the incremental 114.5 Mn shipments arrived at Ecom's rates, blended realisation would fall by arithmetic alone, with no price cut on any retained account. **This is the strongest rival reading and it may well be right.**
- **Weight and category mix.** A shift toward lighter parcels or lower-value categories reduces realisation per shipment without any change in per-kilogram pricing. Delhivery discloses shipment counts, not express tonnage, so this cannot be tested externally.
- **Fuel and surcharge timing.** Blue Dart explicitly credits fuel surcharge pass-through for part of its revenue growth. Differences in surcharge mechanics between the two carriers could account for some of the gap in §14.

**What the case study offers against these, and its limit.** PTL realisation rose **5.15%** in the same quarter, in the same company, under the same management — which rules out a company-wide pricing policy, and rules out a purely macro explanation. It does **not** distinguish price action from acquired-book mix within express, because the acquisition affected express and not PTL. That limit is stated in §11 and is why K2 exists as a Phase 0 kill criterion rather than an argued conclusion.

**How A1 dies.** §55's early-warning row: track realisation on **retained pre-merger accounts only**. If blended realisation falls while retained-account realisation is flat, the decline is mix and the pricing thesis is wrong. Delhivery already holds the cohort tag required.

### A2 — that Q1 FY26 EBITDA can be estimated from the disclosed margin

Prior-year EBITDA is not disclosed in absolute terms. It is estimated as derived Q1 FY26 services revenue (₹2,293.43 Cr) × the disclosed 6.5% margin = **₹149.07 Cr**, giving EBITDA growth of 4.65% and the **8.42% volume-to-EBITDA conversion** used as the RICE stress rule. If the 6.5% margin was struck on total income rather than services revenue, the estimate moves by roughly 4%. The conversion figure is therefore an **approximation used as a conservatism factor**, not a precise measurement, and nothing else in the case study depends on it.

### A3 — that shipments per square foot is a meaningful productivity measure

§28 and §30 read shipments ÷ facility square footage as network productivity. The measure is crude: facility footprint includes warehousing space serving Supply Chain Services, not only express sortation, and 1.3 Mn sq ft of retained Ecom facilities entered the base mid-period. The **shipments-per-sorter** figure (+36.07%) is the cleaner of the two because sorters serve express specifically, and the two measures agreeing to within 0.2pp is the reason the case study reports both rather than either alone.

### A4 — that Q1 FY26 figures can be back-derived from disclosed growth rates

Prior-year segment revenue, shipment volume and PTL tonnage are back-derived from Q1 FY27 absolutes and disclosed YoY growth percentages, which are themselves rounded to one decimal. All derived bps and percentage results carry that rounding and should be read to roughly ±0.2pp.

### A5 — that Blue Dart is a fair comparator

§14 compares a premium air-express operator with a volume ground network. They are not the same business: Blue Dart's volumes are barely growing, which is a serious strategic weakness of its own, and its cost base and customer mix differ materially. The comparison is used for **one narrow purpose** — to show that within a single quarter and market, price and volume were separable choices with opposite outcomes. It is not used to argue that Delhivery should become Blue Dart, and §40's coverage carve-out exists precisely to prevent that reading.

---

## Part 2 — Derivations

Every figure below is reproduced in `verify.py`, which must pass before publication.

| ID | Derivation | Inputs | Result |
|---|---|---|---|
| D1 | Express realisation per shipment | ₹1,869 Cr ÷ 322 Mn; prior year back-derived | **₹58.04 vs ₹67.63 = −14.18%** |
| D2 | Network productivity | 322 ÷ 23.3; 322 ÷ 73 | **+35.88%** per sq ft; **+36.07%** per sorter |
| D3 | Input growth | Owned inputs vs partner agents | sq ft +14.22%, EDC +18.27%, team +14.01%, fleet +18.01%, sorters +14.06%, **partner agents +58.48%** |
| D4 | Volume-to-EBITDA conversion | EBITDA +4.65% ÷ volume +55.2% | **8.42%** — the RICE stress rule |
| D5 | Ecom explanatory power | ₹17 Cr ÷ (₹91 − ₹32) Cr | **28.81%** of the profit decline; ex-Ecom PAT still **−31.87%** |
| D6 | PTL realisation per tonne | ₹633 Cr ÷ 542,000 t; prior year derived | **₹11,679 vs ₹11,107 = +5.15%** |
| D7 | Partner-to-employee ratio | 82,768 ÷ 75,074; 52,225 ÷ 65,849 | **1.102× from 0.793×** |
| D8 | Shipments per partner agent | 322 Mn ÷ 82,768; prior year | 3,890 vs 3,973 = **−2.07%** |
| D9 | Blue Dart mirror | PAT ₹86.7 Cr vs ₹32 Cr; revenue ₹1,657.7 Cr vs ₹2,931 Cr | **2.71× the profit on 56.56% of the revenue**; EBITDA margin ratio **3.12×** |
| D10 | Realisation surrendered | 322 Mn × ₹9.59 | **₹308.8 Cr in the quarter = 9.65× quarterly PAT** |
| D11 | Segment mix | Express / PTL / SCS ÷ services revenue | **63.77% / 21.60% / 6.79%**; SCS adj. EBITDA **−4.02%** |
| D12 | RICE stressed scores | R × I × C ÷ E × 100, stressed R = R × 0.0842 | Floor **123.75 → 10.42**, falling from **3rd to 4th of 4** |

---

## Part 3 — Author-constructed content

Not Delhivery artefacts. Constructed by the author, with reasoning:

- **Personas (§20).** Four composite personas built from disclosed customer-count, segment and network facts. Delhivery publishes no persona research. The lane manager persona exists to make the missing internal tool visible as a human problem rather than a data problem.
- **The user journey's cost-versus-price column (§22).** The stages are inferable from disclosed operations; the attribution of *where cost is created versus where it is priced* is the author's analysis and is the mechanism of the thesis.
- **RICE inputs (§47).** Reach, Impact, Confidence and Effort are author estimates. Only the **stress multiplier (0.0842)** derives from Delhivery's own disclosures, and it inherits Assumption A2. The relative ordering, not the absolute scores, is what the section argues.
- **Delhivery Floor (§50), the PRD (§51) and the quoting wireframe (§52).** Entirely the author's proposal. Delhivery has announced nothing resembling a published contribution floor, a coverage budget, or a Network Access function.
- **CCF and RSC-90 (§31).** Author-designed metrics. Neither is a Delhivery metric and no logistics operator is known to publish either.
- **Kill criteria K1–K3 (§53), decision rule R1 (§54), and the lane-class categories in §52.** Author-set thresholds and labels, pre-registered so a later reader can check whether the proposal would have survived its own test.

---

## Part 4 — What would change my mind

1. **Delhivery disclosing realisation split by retained versus acquired accounts.** If retained-account realisation held flat, A1 collapses and the case study's central claim is wrong.
2. **Express tonnage disclosure.** If parcels got materially lighter, realisation per shipment falls for reasons that have nothing to do with price and the correct unit of analysis is revenue per kilogram.
3. **Evidence that a large share of the 55.2% volume increase was contractually committed before the acquisition** — that would make the volume unrefusable and the Floor moot for the period analysed.
4. **Delhivery hitting its own 16–18% express service EBITDA margin guidance within FY27.** That would show the margin recovers without any new instrument, and the proposal becomes unnecessary rather than merely deprioritised.
5. **Blue Dart's volumes falling materially next quarter.** That would suggest its pricing strategy trades away share at a rate that makes it the wrong comparator, weakening §14 considerably.

---

## Part 5 — What could not be found out

- **Ecom Express's own pre-acquisition shipment volumes, revenue and realisation** — without them, the mix-versus-price question (A1) cannot be settled from outside, and K2 cannot be run externally.
- **Express tonnage or average parcel weight**, in either year.
- **Lane-level or facility-level cost data** of any kind — the absence that makes §41's last row 🔴 and drives K3.
- **The share of shipments handled by partner agents versus own last-mile capacity**, which is the single number that would quantify the margin leak this case study infers.
- **Returns and RTO volumes and their cost**, which plausibly account for a material share of express cost and are not disclosed.
- **A credible primary-sourced TAM** for Indian third-party express logistics, which is why §13 is run in restricted form.
- **Comparable quarterly financials for Ekart, XpressBees or Shadowfax**, which is why §14 is restricted to the single competitor that files them.
