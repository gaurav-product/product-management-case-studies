# ASSUMPTIONS.md — Day 39: Myntra

This document does two things: it grades the evidence behind every load-bearing claim in the case study (High / Medium / Low), and it carries forward, rather than resolves, every conflict found in public sources. Where the case study makes an inference beyond what a source directly states, that inference is listed here as an assumption, not presented as fact in the main document.

## Evidence grades

| Claim | Grade | Basis |
|---|---|---|
| Myntra DAU ~21M, Ajio ~6–7M, Nykaa Fashion ~2M (June 2026) | High | Sensor Tower data cited directly by a named analyst source (BofA Securities), reported identically across three independent news outlets (Entrackr, RS Websols, Bharat Fast) |
| Myntra AI Size & Fit Intelligence: ~85% catalog coverage, sub-2-second explainability | High | Company-disclosed, reported by a named trade publication with direct quotes attributed to Myntra |
| Myntra founded 2007, acquired by Flipkart in 2014 | High | Consistent across all sources reviewed, standard public-record company history |
| Myntra FY2024 GMV ~$9.8B | Medium | Single secondary aggregator source (Good Seva Guide); not cross-verified against a second independent source or Myntra/Flipkart financial disclosure |
| Myntra fashion market share 35–45% | Low | Cited by one source (GrowthX) with no methodology disclosed; not reconcilable with DAU-based data from a separate, more credible source. See Conflict C1 |
| Aggregate Myntra review score 1.7–1.8/5 | Medium | Consistent direction across three independent platforms (PissedConsumer, Trustpilot, Reviews.io) but with different, non-identical sample sizes and time windows. See Conflict C2 |
| "Exchange cancelled without explanation" as the most repeated complaint pattern | Medium-High | Independently and repeatedly described, using similar specific language, across four separate review platforms spanning multiple months in 2025–2026 — a strong pattern signal, but not a Myntra-disclosed operational metric |
| App-displayed status diverging from backend truth | Medium | Described in multiple independent reviews (e.g., "app says refunded, nothing received") but the underlying technical cause (data-sync lag vs. policy-driven delay vs. courier failure) cannot be confirmed from public sources |
| Apparel category return rate 20–40%, fit/sizing driving 45–53% of returns | High (as an industry benchmark) / Not verified (as a Myntra-specific figure) | Multiple independent, dated 2025–2026 industry sources converge on this range; Myntra does not publicly disclose its own return-reason breakdown, so this is used only as category context, never presented as Myntra's own number |
| Footwear has the highest sub-category apparel-adjacent return rate | Medium | Cited across multiple industry sources but not confirmed for Myntra specifically |
| Myntra Insider loyalty program mechanics (tiered, points-based, free shipping) | High | Directly stated in Myntra's own Google Play listing and multiple consistent third-party guides |

## Conflicts carried forward, not resolved

**C1 — Myntra's fashion market share.** GrowthX cites 35–45% market share by value with no stated methodology. Separately, Sensor Tower/BofA DAU data shows Myntra at roughly 3x Ajio's and 10x Nykaa Fashion's daily active users. DAU share and GMV/value share are different measures and cannot be mathematically reconciled from the sources available. This case study therefore does not adopt a single market-share percentage as fact anywhere in the analysis; it uses the DAU comparison (graded High) as the primary evidence of Myntra's competitive lead, and treats the 35–45% figure as a directionally consistent but methodologically unverified secondary data point.

**C2 — Myntra's aggregate review score.** PissedConsumer shows 1.7/5 on approximately 1,518 reviews as of a July 2026 page snapshot, and separately 1.8/5 on 1,408 reviews as of a February 2026 snapshot from the same platform — different totals and different averages from what should be a cumulative, monotonically growing sample. This likely reflects platform-side review filtering, moderation, or sampling changes over time rather than a real change in Myntra's underlying service quality, but that cannot be confirmed externally. Both figures are carried in the case study rather than averaged or treated as a single precise number. The directional conclusion — persistently low scores dominated by the same complaint categories — holds under either figure.

**C3 — Reverse-logistics cost impact.** The case study asserts, as a hypothesis rather than a disclosed fact, that reducing *cancelled and re-attempted* exchanges specifically (as distinct from reducing the overall, structurally-high return rate) would produce a real cost saving for Myntra. No Myntra-specific reverse-logistics cost figure is public. This is flagged explicitly in §12 as unquantified.

## Assumptions used where no public data exists

| Assumption | Why it was needed | Confidence | How to validate |
|---|---|---|---|
| The exchange-cancellation pattern described in reviews is primarily caused by a Myntra-side (app/backend/inventory-visibility) issue rather than a third-party courier/logistics-partner failure | Public review data cannot distinguish root cause; the case study needed a working hypothesis to prioritize a fix | Low-Medium | This is explicitly built into the rollout plan (§25) as a falsifiable pre-launch audit and Arm A decision rule — the proposal is designed to test this assumption before committing further investment on the basis of it |
| The ~15% of catalog outside AI size-recommendation coverage is concentrated in smaller or newer brands | Myntra disclosed the 85% figure but not its composition | Low-Medium | Request the internal coverage breakdown by brand tier and SKU volume from the Size & Fit Intelligence team |
| Fit-driven returns at Myntra track the global industry range (45–53%) rather than a materially different, India-specific figure | No Myntra-specific return-reason breakdown is public | Medium | Analyze Myntra's internal return-reason-code data directly |
| A visible Fit Confidence Score will not meaningfully suppress purchase conversion on lower-confidence items | No A/B data exists; this is a reasonable but untested UX hypothesis, and could plausibly go the other way | Low-Medium | This is exactly why it is proposed as Arm B in the A/B test (§25) rather than shipped directly |
| Customers who receive a forced store-credit refund are more likely to churn than those refunded in cash | Inferred from repeated, explicit customer requests for cash refunds in review text, not from Myntra churn data | Medium | Cohort-analyze repeat-purchase rates for cash-refunded vs. credit-refunded customers following a size-related return |
| The case study's section structure (numbered sections, RICE with sensitivity check, PRD with a falsifiable decision rule, PM Lessons) should match the Day 38 Razorpay write-up exactly | The user provided the Day 38 file directly as the reference standard for repository formatting | High (structural assumption, not a research claim) | Compare directly against Day 38 and earlier files for any remaining formatting drift and adjust on request |

## What would most change this case study
The single figure that would most affect this analysis, and that is not public, is Myntra's own exchange-request-to-completion rate, broken out from its overall return rate. If that number is already high (e.g., above 90%), the review-based complaint pattern this case study leans on may reflect a smaller, louder minority rather than a systemic operational gap, and the prioritization in §22 and §25 should be revisited accordingly. The rollout plan's pre-launch audit (§25) is designed specifically to surface this before further investment is committed.
