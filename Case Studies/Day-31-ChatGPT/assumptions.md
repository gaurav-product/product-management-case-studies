# Assumptions Log — Day 31: ChatGPT

**Case study:** ChatGPT (OpenAI Group PBC)
**Author:** Gaurav Singh
**Date:** July 27, 2026
**Companion to:** `README.md`

## Purpose

OpenAI is a private company. It files no 10-Q, publishes no audited revenue, and discloses no advertising revenue at all. Almost every quantitative claim about its business in circulation is either a company statement made in a blog post or interview, or a press report of leaked internal documents. This file records which is which.

**Standard applied:** every figure in the case study that is not a Tier 1 or Tier 2 source is labelled `ASSUMPTION — VALIDATION REQUIRED` at the point of use and logged here with its tier, its origin, and what would be needed to verify it.

## Confidence tiers

| Tier | Definition | Treatment |
|---|---|---|
| 1 | Company statement, official documentation, court filing | Used directly, attributed |
| 2 | Reputable news organization or established measurement firm | Used directly, attributed, source named |
| 3 | Secondary aggregator, single-sourced, or internally inconsistent | Used illustratively only, flagged inline |
| 4 | Not disclosed — figure does not exist publicly | Absence recorded; no estimate substituted |

## Tier 1 — Company-stated

| # | Claim | Source | Note |
|---|---|---|---|
| 1 | 900M weekly active users | OpenAI announcement, Feb 27, 2026 | Not refreshed publicly since February |
| 2 | India ~100M weekly actives, second-largest market | Sam Altman, Times of India column, Feb 2026 | First India-specific figure OpenAI disclosed |
| 3 | 9M+ paid business users, Feb 2026 | OpenAI | 4x increase from Sept 2025 per same source |
| 4 | 1M+ business customers, Nov 2025 | OpenAI | — |
| 5 | Ads launched Feb 9, 2026, US Free and Go, adults 18+ | OpenAI | Announced Jan 16, 2026 |
| 6 | Ads excluded from health, mental health, politics, dating, financial services | OpenAI ad policy | — |
| 7 | Ads do not influence answers; conversation content not given to advertisers | OpenAI | Stated position; not externally verifiable |
| 8 | GPT-5.6 Sol / Terra / Luna released July 9, 2026 | OpenAI, CNBC, TechCrunch, Axios | Limited release from June 26 at US government request |
| 9 | 1.05M token context, 128K max output; Sol API $5/$30 per 1M tokens | OpenAI documentation | — |
| 10 | ChatGPT Go launched India Aug 2025 at ₹399/month; free 12 months from Nov 4, 2025 | OpenAI, Reuters | Basis of the November 2026 expiry analysis |
| 11 | Recapitalization Oct 28, 2025 into OpenAI Foundation + OpenAI Group PBC | OpenAI | — |
| 12 | Confidential S-1 acknowledged June 8, 2026 | OpenAI blog post | Company stated timing undecided |
| 13 | Age prediction system, Jan 2026; parental controls, Sept 2025 | OpenAI | — |

## Tier 2 — Reputable third-party

| # | Claim | Source | Note |
|---|---|---|---|
| 14 | ChatGPT app passed 1B monthly active users, June 2026 | Sensor Tower via Reuters | Fastest app in history to the mark |
| 15 | 1.11B monthly users, May 2026 | Sensor Tower | Different denominator from WAU |
| 16 | Web-visit share 79.0% (May 2025) → 53.9% (May 2026); Gemini 27.9%, Claude 9.2% | Similarweb | Vendor-measured; see caveat #30 |
| 17 | US web-visit share May 2026: ChatGPT 58.3%, Gemini 19.3%, Claude 13.4% | Similarweb | — |
| 18 | Enterprise LLM API spend: Anthropic ~40%, OpenAI 27%, Google 21% | Menlo Ventures | — |
| 19 | ~$25B annualized revenue, ~$2B/month, March 2026 | Multiple outlets incl. TechCrunch, Reuters | Run-rate, not recognized revenue |
| 20 | 2025 recognized revenue $13.1B; 2030 revenue target ~$280B | CNBC, Feb 20, 2026 | Conflicts with "$20B+ 2025" aggregator claims — see #31 |
| 21 | Compute spend target reset to ~$600B by 2030 from $1.4T commitments | CNBC | Sequential revision, not contradiction |
| 22 | Private valuation ~$852B, March 2026 | Multiple financial outlets | — |
| 23 | Anthropic filed confidentially June 1, 2026 (~$965B); SpaceX IPO June 12, 2026 (~$1.77T) | Multiple outlets | Context for IPO window |
| 24 | Instant Checkout: ~30 Shopify merchants live by Feb 2026 | Forrester (Emily Pfeiffer) | Against "1M+ coming" announcements |
| 25 | Walmart: in-chat checkout converts ~3x worse than click-through; ~2x new-customer rate | Reported measurement | Directional; single retailer |
| 26 | Raine v. OpenAI, Lacey v. OpenAI allegations; FTC 6(b) inquiry Sept 11, 2025 | Court filings, Tech Policy Press, NBC | — |
| 27 | Florida AG sued OpenAI and Altman personally, June 1, 2026 | CNN | First state action |
| 28 | Musk suit dismissed May 18, 2026 on statute-of-limitations grounds | Multiple outlets | — |
| 29 | Generative AI web visits 9.5B/month avg Jun 2025–May 2026, +70% YoY | Similarweb | Category growth context |
| 30 | Similarweb share is distorted by Gemini's Android/Workspace pre-installation; Cloudflare shows ChatGPT #1 continuously | Similarweb, Cloudflare Radar, analyst commentary | **Measurement conflict carried, not resolved** |

## Tier 3 — ASSUMPTION, VALIDATION REQUIRED

Every item below is flagged inline in the case study.

| # | Claim | Where used | Why flagged | What would verify it |
|---|---|---|---|---|
| 31 | 2026 projected loss ~$14B; operating margin ~-55%; burn 57% of revenue 2026–27; $1.69 spent per $1 earned | §5, §10, §15, §18 | Press reports of internal documents; no audited figure exists | Public S-1 financials |
| 32 | Revenue mix ~$17B subscriptions / ~$6.5B API / ~$1.5B other | §6, §18 | Third-party estimate, single analyst source | OpenAI segment disclosure |
| 33 | ~50M paying consumer subscribers → ~5% conversion on ~1.11B MAU | §5, §10, §15, §19 | Subscriber count is secondary-sourced; conversion is my own derivation from two figures with different denominators | OpenAI disclosure of paid consumer count and MAU on the same basis |
| 34 | Ads appear in 51.0% of US replies, early July 2026; peak 26.5% late May, collapse to ~0.05% mid-June | §25, §45, §65 | Single low-quality aggregator citing "Cloro" tracking I could not verify; **conflicts with PPC Land's 26% for the same month** | Independent panel measurement or OpenAI disclosure |
| 35 | Premium ad placement CPM ~$60 | §39 | Reported in a single secondary piece; no rate card published | Advertiser-side confirmation or OpenAI Ads Manager documentation |
| 36 | Anthropic $47B annualized run-rate, May 2026 | §14 | Single-source, and materially larger than OpenAI's ~$25B, which is surprising enough to warrant caution | Anthropic disclosure or S-1 |
| 37 | API processes ~15B tokens/minute; ~4M developers | §43, §6 | Aggregator-sourced | OpenAI developer-day disclosure |
| 38 | 92% of Fortune 500 use ChatGPT; 7M workplace seats, 9x YoY | §15 | Company marketing research ("State of Enterprise AI 2025"), methodology not published | Independent enterprise survey |
| 39 | ~$4B annual talent cost | §17 | Press estimate | S-1 |
| 40 | HSBC estimate of ~$207B funding gap to 2030 | §16 | Analyst projection with undisclosed model | HSBC published research |
| 41 | Prediction-market odds on IPO timing (Polymarket ~54%, Kalshi 59% by Mar 2027) | §7 | Sentiment prices, not information; thin markets | N/A — treat as sentiment only |
| 42 | TAM $300–500B by 2030; SAM $120–180B | §13 | **My own synthesis** across inconsistent analyst ranges. No single source supports these numbers | Commissioned market study |
| 43 | Correlation between ad discontent and Claude's share growth / OpenAI's Ramp share drop | §14 | Correlational only; the same window contained several unrelated controversies | Cohort-level switching survey |
| 44 | 250M "consistent weekly returners" | §30, §33 | Reported figure without published definition of "consistent" | OpenAI metric definition |
| 45 | Consequential turns underperform on click-through relative to eligibility (basis of §54 hypothesis) | §54, §57 | **My hypothesis, entirely untested.** The suppression revenue model depends on it | Shadow-mode measurement in Phase 2 |
| 46 | Classifier latency budget <40ms and >90% suppression precision | §51, §55 | Asserted product targets, not derived from benchmarking | Prototype evaluation |

## Tier 4 — Not disclosed

| # | Figure | Status |
|---|---|---|
| 47 | ChatGPT advertising revenue | Never published. No estimate substituted anywhere in this document |
| 48 | Commerce take-rate revenue | Never published |
| 49 | Any trust, reliance, or task-success metric | Does not exist publicly — this absence is the case study's central finding |
| 50 | Ad-load ceiling or target penetration | Not published |
| 51 | Retention behaviour of ad-relevant derived signals after memory deletion | Not documented; raised as an open question in §44, not as an allegation |

## Analytical positions that are mine, not sourced

Recorded separately so a reader does not mistake argument for evidence:

1. That advertising in an assistant is categorically different from advertising in search, because the ad and the advice share a surface with no comparison set (§26, §59)
2. That OpenAI's measurement asymmetry structurally predicts over-monetization regardless of intent (§32, §59)
3. That the India promotional expiry around November 2026 constitutes a dated product deadline (§19, §35, §56) — the expiry date is derived from the Nov 4, 2025 start plus the stated 12-month term, not from an OpenAI statement about expiry
4. That the failure of in-chat checkout made advertising the surviving option rather than the chosen one (§28)
5. That building Compass Holdout creates discoverable documentation, and that this is a real argument against it (§50, §57)
6. The entire Compass proposal, its RICE override, and the Weekly Trusted Task Completions metric (§31, §47, §50)

## Corrections

None at publication. Corrections will be appended here with date and reason rather than edited silently into the body.

---

**90 Days Product Management Challenge — Day 31 of 90**
