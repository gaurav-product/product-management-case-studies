# ASSUMPTIONS — Day 41, InMobi

Companion to `README.md`. This file documents what is sourced, what is contested, and what I made up.

**Research date:** 6 August 2026
**Author:** Gaurav Singh
**Subject:** InMobi Group — private company, pre-DRHP, no audited public disclosure

---

## 1. Why this file exists

InMobi is private and has not yet filed a Draft Red Herring Prospectus. There is no audited public financial record. What exists is a mixture of trade-press reporting, revenue-modelling services, company statements made in interviews, and market-research summaries — several of which contradict each other directly.

This matters more than usual for this particular case study, because the central argument rests on a single arithmetic operation performed on two contested inputs. That calculation is the thesis's greatest strength (it is checkable) and its greatest exposure (both inputs are uncertain). §3.1 and §3.2 below give it the scrutiny it needs.

**Rules applied throughout:**

- Where two sources conflict, **both are carried forward**. Nothing is averaged, and no conflict is silently resolved in favour of the more convenient figure.
- Where a baseline is not published, it is written as **"not disclosed"**. No baseline is invented or back-filled from a plausible range.
- Everything I constructed is listed in §4, without exception.
- The one figure I computed myself is labelled **author-computed** everywhere it appears.

---

## 2. Evidence grading by claim

**Grades:** **High** — multiple independent credible sources agree, or direct company disclosure. **Medium** — single credible source, or several sources tracing to one origin. **Low** — inference, heuristic assessment, or estimator-modelled figure. **Conflicting** — credible sources materially disagree; see §3.

### 2.1 Company history and corporate

| Claim | Grade | Notes |
|---|---|---|
| Founded 2007 in Mumbai as mKhoj, an SMS-based search engine | High | Wikipedia, YourStory, multiple India business press |
| Founders: Naveen Tewari, Mohit Saxena, Amit Gupta, Abhay Singhal | High | Consistent across sources |
| Incorporated in Singapore to widen the investor base | Medium | Reported consistently but from a small number of origins |
| 2008 pivot to mobile advertising and rebrand to InMobi | High | Well established |
| Early backing from Kleiner Perkins and Sherpalo Ventures | Medium | Widely repeated |
| Relaunch partly financed on founder credit-card debt | Low | Founder-narrative detail, repeated in profile pieces. Colourful, unverifiable, and not load-bearing in the analysis |
| International expansion sequence — South Africa and Europe before North America | Medium | Attributed to Tewari in interviews |
| SoftBank investment of USD 200M, 2011 | High | Widely reported at the time |
| India's first VC-backed unicorn (2011) | High | Consistently reported |
| Third-largest mobile advertising company (2015, per BBC) | Medium | Single original source, widely relayed, and eleven years stale |
| Roposo acquired 2019 | Medium | Aggregator and press sourced |
| Glance raised USD 145M from Google and Mithril Capital, Dec 2020 | High | BusinessWire release plus TechCrunch |
| Reverse flip from Singapore/Cayman to India in progress | High | Multiple sources; consistent with sector-wide pattern |
| InMobi's specific reverse-flip tax cost | **Not disclosed** | Comparable figures exist for Meesho (~USD 280–300M) and PhonePe. **I did not extrapolate from them** — the structures differ materially |
| IPO bankers: JPMorgan, Jefferies, Kotak Mahindra Capital, Axis Capital | Medium | Inc42 reporting, July 2026 |
| IPO size and valuation | **Conflicting** | See C3 and C4 |

### 2.2 Financial

| Claim | Grade | Notes |
|---|---|---|
| Group revenue FY25 ~₹8,650 Cr (~USD 1B), up from ₹7,950 Cr FY24 | **Medium, and Conflicting** | See C1 |
| Alternative estimate: ~USD 1.3B for FY23–24 | **Medium, and Conflicting** | See C1 |
| Group net profit ~USD 100M (FY23–24) | **Low** | Estimator-sourced; not company-disclosed |
| Group EBITDA margin ~18% | **Low** | Estimator-sourced |
| Glance FY25 revenue USD 97.6M, +33.5% | **Medium** | Dealroom, with component breakdown. The component detail (ads USD 61.7M +54%; commerce USD 32.4M) increases confidence — modelled figures rarely carry that structure |
| Glance profitability targeted ~June 2026 | Medium | Company guidance via Business Standard |
| Indian subsidiary revenue ₹100–500 Cr FY25 | Medium | Tracxn, entity-level filing. **Not comparable to group figures** — different legal scope, and I have not used it as a group proxy anywhere |
| Revenue multiple pitched at 25–30x | Medium | Reported as a banker pitch, not an agreed valuation |
| Gross vs net revenue treatment | **Not disclosed** | Material for an ad-tech business — see §3.1 |

### 2.3 Glance product and users

| Claim | Grade | Notes |
|---|---|---|
| Glance MAU | **Conflicting** | See C2 |
| Distribution via OEM pre-installation (Samsung, Xiaomi, Realme, Nothing) | High | Multiple independent sources including OEM support communities |
| Glance revenue per user per year ~USD 0.24–0.28 | **Author-computed** | See §3.1. Not a sourced figure |
| Users seek to disable Glance; some OEMs bury controls; component may be protected by system policy | **Medium** | Multiple independent how-to publications and a Samsung Community thread. See §3.5 for why I treat this cautiously |
| Complaints re data consumption, RAM usage, ad density | **Medium-Low** | Consistent across consumer-tech publications; no quantified data |
| Disable rate | **Not disclosed** | Not estimated anywhere in the analysis |
| DAU, session depth, time-on-lockscreen | **Not disclosed** | Not estimated |
| OEM contract terms, duration, renewal, revenue concentration | **Not disclosed** | The most important undisclosed set of facts in the case study |

### 2.4 Glance AI

| Claim | Grade | Notes |
|---|---|---|
| Launched May 2025 as an AI-native commerce platform | High | Company newsroom plus multiple outlets |
| Built on Google Imagen 4 | Medium | TechCrunch and retail-tech coverage |
| 400+ brands in marketplace | Medium | Consistently reported |
| Samsung Galaxy Store US partnership, June 2025 | High | Company release, Forbes, Digital Commerce 360 |
| Explicitly opt-in, contrasted with earlier ad-focused criticism | Medium | Reported in comparative coverage. **Load-bearing for the thesis** — it is the "admission" argument in §5 |
| ~1.5M weekly users (July 2025) | Medium | Single reporting origin |
| ~18 looks per user per day; ~40M cumulative style requests | Medium | Same origin |
| Planned expansion into beauty, accessories, travel | Medium | Signalled, not confirmed as shipped |
| Lock-screen-to-Glance-AI conversion rate | **Not disclosed** | §29's argument that the base is not converting is **inference from the US-first traction story**, not from data. Flagged in §64 |

### 2.5 Market and competitive

| Claim | Grade | Notes |
|---|---|---|
| Open-internet programmatic mobile advertising ~USD 400B by 2026 | **Low-Medium** | Category projection with no verifiable boundary definition |
| InMobi app monetisation mindshare 7.8%, ranked #6 | Medium | Single tracker. **Mindshare is a consideration-set proxy, not revenue share** — stated in §14 |
| Unity mindshare 22.9%, up from 16.8% | Medium | Same tracker |
| Competitor set (Google, Meta, AppLovin, Unity, Moloco, PubMatic) | High | Uncontroversial |
| AppLovin owns Adjust | High | Well established |
| Indian digital advertising is structurally low-ARPU | Medium | General market knowledge; no single figure cited, and none used in the calculation |

### 2.6 Sections that are entirely heuristic

| Section | Grade | Why |
|---|---|---|
| §24 Information Architecture | **Low** | Reconstructed from public surfaces and product descriptions. I have never used Glance on a pre-installed device |
| §25 UX Audit | **Low** | Heuristic critique from published descriptions, screenshots and criticism |
| §26 UI Audit | **Low** | Same limitation |
| §27 Accessibility | **Low** | No instrumented testing, no screen-reader session, no contrast measurement. Every row is a hypothesis |
| §41 Technical Architecture | **Low** | Author-constructed model consistent with how such systems must work. No published architecture document exists |
| §42 Data Flow | **Low** | Same |

---

## 3. Source conflict table

Conflicts preserved, not resolved. Where a working position is taken, it is labelled.

### C1 — Group revenue

| Figure | Period | Source type | Status |
|---|---|---|---|
| ~₹8,650 Cr (~USD 1B), up from ₹7,950 Cr | FY25 | IPO/trade-press reporting | Reported |
| ~USD 1.3B, with ~USD 100M net profit | FY23–24 | Estimator/aggregator | Reported |
| ₹100–500 Cr | FY25 | Indian entity filing (Tracxn) | Different legal scope |

**The problem.** The second figure describes an *earlier* period at a *higher* value than the first. Revenue does not usually travel backwards while being reported as growing. At least three explanations are available and I cannot distinguish between them:

1. **Gross versus net.** Ad-tech companies report on both bases and they can differ by a factor of two or more. If the ~USD 1.3B figure is gross billings and the ~USD 1B figure is net revenue, both can be simultaneously true and the apparent contradiction dissolves. **This is the explanation I consider most likely**, and neither source states its basis.
2. **Group versus subsidiary scope.** InMobi's structure spans multiple entities across jurisdictions mid-reverse-flip. Different sources may consolidate differently.
3. **One estimate is simply wrong.** Modelling services routinely produce figures with wide error bars presented without them.

**Resolution: none applied.** Both figures are carried in §30 and §65. The README's §5 uses "approximately $1B" for FY25 while flagging the conflict, and no argument in the document depends on the precise group figure — the thesis rests on Glance's revenue and user count, not the group's.

### C2 — Glance monthly active users

| Figure | Source context |
|---|---|
| 350 million | Consumer business including Roposo, Nostra, 1Weather |
| 370 million | IPO-related reporting |
| 400 million+ | Company/product positioning, described as "400M+ MAU lock-screen platform" |

A ~14% spread across figures published within roughly a year. Plausible explanations: different dates; different scope (lock-screen only versus all consumer properties); MAU versus reach versus devices-shipped-with. **None of the sources defines its term.**

**Resolution: none.** All three are carried in §30 and §65.

**Effect on the thesis:** the per-user calculation is run across the full range rather than on a point estimate, which is why §5 states a range. See §3.1.

### C3 — IPO valuation target

| Figure | Source |
|---|---|
| USD 5B | Whalesbook |
| USD 8–10B | Inc42 |
| USD 10B | TechCrunch (2024 reporting, "eyes $10 billion in 2025") |

A 2x spread. The TechCrunch figure is the oldest and describes an aspiration for a listing that did not occur on that timeline. **All carried; none used as a load-bearing input.** The README refers to the range rather than to any single number.

### C4 — IPO size

| Figure | Source |
|---|---|
| ~USD 1B (₹9,634 Cr) public issue | Inc42 |
| ₹3,000–4,000 Cr raise | IPO commentary sources |

These differ by roughly 2.5–3x. Possibly a total-issue-size versus fresh-issue distinction (an offer-for-sale component would account for much of the gap), but neither source is explicit. **Both carried.**

### C5 — Glance's contribution relative to the advertising business

| Claim | Source |
|---|---|
| Glance FY25 revenue USD 97.6M | Dealroom |
| Glance "currently contributing only a third" of the advertising business, expected to match it within two years | Business Standard, quoting InMobi |

**These do not reconcile.** One third of a ~USD 1B advertising business would be ~USD 330M, not USD 97.6M. Possible explanations: the "one third" refers to a different metric (gross merchandise value, gross billings, or a forward projection); the comparison excludes parts of the advertising business; or one figure is simply loose.

**Resolution: none, and this conflict is analytically important rather than incidental.** §18 flags it explicitly. Note the direction of the exposure: if Glance's true revenue were ~USD 330M rather than USD 97.6M, per-user revenue would be roughly USD 0.83–0.94 rather than USD 0.24–0.28. That is 3.4x better and **still very low for a consumer platform** — the thesis survives, though with less force. This is the single most important robustness check in this file and I want it stated plainly rather than buried.

### C6 — Attention quality evidence

Not a conflict between sources but a conflict between **types of evidence**. The claim that Glance's attention is low-quality rests on:
- Quantitative: the per-user revenue calculation (author-computed, contested inputs)
- Qualitative: prevalence of removal guides and published criticism (real but weak — see §3.5)

There is no disclosed disable rate, no engagement data, and no session data. **The thesis is therefore better supported on economics than on behaviour**, and §64 of the README concedes this.

---

## 3.1 The anchor calculation, examined

The figure that carries the most argumentative weight in this case study is not sourced. It is mine.

**Calculation:** USD 97.6M ÷ 350M–400M users = **USD 0.244 to USD 0.279 per user per year.**

**Inputs and their weaknesses:**
- *Numerator:* Glance FY25 revenue, single-sourced (Dealroom), Medium confidence. Includes Roposo and Shop101 commerce revenue (USD 32.4M), which is arguably not lock-screen revenue at all — **excluding it would make the figure worse, roughly USD 0.15–0.18.** I did not exclude it, choosing the interpretation less favourable to my own argument.
- *Denominator:* MAU, three conflicting values (C2), and a term none of the sources defines.
- *Period alignment:* The revenue figure is FY25; the user figures span roughly a year and may not correspond to the same period.

**Robustness.** The conclusion — that Glance monetises at a small fraction of a chosen consumer product — holds across the full plausible range, including under C5's most generous reading (~USD 0.83–0.94). It would only break if Glance's true revenue were several times higher than any published figure, or if the user base were an order of magnitude smaller than every published figure.

**How it is misused in the README.** §5 and §30 state the range to two decimal places, which implies a precision the inputs do not support. That is a presentational error I have left in place and flagged in §64 rather than quietly rounding, because the precision creates a false impression and a reader deserves to see both the figure and the objection to it.

---

## 3.5 A note on the removal-guide evidence

The README leans on the prevalence of "how to disable Glance" content as evidence of user sentiment. This deserves explicit scepticism, because it is the weakest load-bearing evidence in the document.

**Why it is weak:** the existence of many such articles reflects SEO economics as much as underlying demand. A query with high commercial intent and low competition attracts content farms regardless of true search volume. Eight publications writing the same guide may indicate eight publishers chasing the same keyword, not eight million frustrated users.

**Why I used it anyway:** it is corroborated by a Samsung Community support thread (users asking the manufacturer directly, which has no SEO incentive), by consistent independent criticism of ad density across consumer-tech publications, and by the structural observation that reporting describes controls as buried or policy-protected — a design choice that only makes sense if removal is common enough to matter commercially.

**What would settle it:** the disable rate, which InMobi has and has not published. §32 of the README recommends instrumenting and reporting it internally, partly because it is cheap and partly because it is the fastest way to test my own argument. If that rate is in the low single digits, a meaningful portion of §25, §40 and §45 weakens.

---

## 4. Everything author-constructed

Complete list. If it is not sourced, it is here.

### 4.1 The central thesis
The framing that Glance's audience is *leased rather than owned*, that ~USD 0.25 per user is the correct price of unconsented attention rather than a monetisation failure, and that Glance AI is best read as an admission of that — **is entirely my analysis.** No source makes this argument. No source I found performs the per-user calculation at all.

### 4.2 Personas (§20)
Ramesh, Sneha and Maya are **fictional composites.** No interviews were conducted. Their behaviours are inferred from published criticism, market structure and general consumer patterns. Specifically: Ramesh's indifference, Sneha's early disabling, and the selection effect I draw from her (that high-value users are most likely to leave) are **plausible inferences, not observed behaviour.** The selection-effect argument in particular is doing real work in the analysis and has no empirical support whatsoever.

### 4.3 The entire feature proposal (§50, §51, §52, §53, §54)
**Glance ID** — all three components, the PRD, the wireframe descriptions, the rollout plan and both tests — **is my invention.** InMobi has announced nothing like it. No user has publicly requested it. Demand is inferred from structure, not observed. §49 argues this is characteristic of Indifferent-to-Must-be features; §64 concedes it is also what a PM would say about a feature nobody wants.

### 4.4 Quantitative constructions

| Item | Section | Nature |
|---|---|---|
| Revenue per user USD 0.24–0.28 | §5, §30, §55 | **Author-computed** from two contested inputs — see §3.1 |
| SAM USD 25–40B | §13 | **Fully constructed** from my own boundary assumptions |
| SOM USD 1.3–1.8B | §13 | **Fully constructed** extrapolation |
| All RICE Reach, Impact, Confidence, Effort values | §47 | Invented. Judgement, no data |
| RICE sensitivity ranges | §47 | My own stress test of my own invented numbers |
| Kano category assignments | §49 | Judgement, no survey |
| Porter's force ratings | §16 | Judgement |
| SWOT contents | §15 | Judgement |
| Journey satisfaction scores | §22 | Invented for the Mermaid diagram |
| North Star metric (MCIU) | §31 | My proposal; InMobi has published no North Star |
| All §50 success thresholds (10% opt-in, 40% retention, 5x revenue) | §50 | Invented targets |
| §54 Test 2 falsification criterion (4% opt-in) | §54 | Invented threshold, chosen to be low enough that failing it is genuinely damning |
| All §55 targets | §55 | Directional; baselines marked not disclosed |
| Roadmap and rollout dates | §53, §56 | Entirely hypothetical |

### 4.5 Structural and qualitative constructions

- **§8 timeline** — assembled from scattered sources; the interpretive claim that every step-change came from securing distribution ahead of the market is my reading
- **§9 four-era vision periodisation** — mine, as is the observation about the word "intent" migrating between eras
- **§10 problem statement** — my framing, particularly the claim that the median user has no problem Glance solves
- **§13 the two-framings table** — my construction of the bull/bear boundary dispute
- **§14 the supplier-as-competitor finding** — my analysis
- **§17 Business Model Canvas** — my mapping
- **§18 three observations on the revenue model** — mine
- **§21 the claim that JTBD does not apply because no hiring decision occurred** — my argument
- **§29 the reading of Glance AI's US-first traction as evidence the base is not converting** — **inference, not data.** One of the weaker links in the chain
- **§31, §33, §34, §36, §37 framework applications** — mine, including the observation that HEART cannot be completed
- **§38 Option A / Option B framing and the Option B recommendation** — mine
- **§40 trust surfaces** — my structuring
- **§45 pain points and their collapse into one root cause** — my finding
- **§46 opportunity mapping** — mine
- **§58 future vision, including the three confirming developments** — speculative
- **§59 PM lessons, §60 interview questions** — mine

### 4.6 Deliberate omissions

- **No invented baselines.** Every unpublished metric in §51 and §55 reads "not disclosed."
- **No estimated reverse-flip tax cost**, despite comparable figures being available for Meesho and PhonePe. The structures differ and an extrapolation would be fabrication.
- **No group revenue point estimate used as a load-bearing input**, given C1.
- **No individual company market-share figure**, since only mindshare data exists and it measures something different.
- **No raster images.** All diagrams are Mermaid, rendering natively on GitHub.
- **No NEWSLETTER.md.** Newsletter entries are written on Tuesdays; 6 August 2026 is a Thursday.

---

## 5. What would materially improve this analysis

In descending order of value:

1. **The DRHP.** It will disclose audited financials, OEM revenue concentration, contract terms, risk factors and — most importantly — how InMobi itself characterises Glance's users. That single document would resolve C1, C3, C4, C5 and most of §2.2. It is the reason this case study is best read as a pre-filing hypothesis rather than a settled account.
2. **Glance's disable rate and cross-device retention.** InMobi has the first and structurally cannot have the second. The disable rate is the fastest test of my own argument, and §3.5 explains why I need it.
3. **Clarity on gross versus net revenue reporting.** This alone probably explains C1, and it materially affects any valuation-multiple discussion.
4. **Lock-screen to Glance AI conversion data.** §29's argument — that the 400M base is not an effective acquisition channel — is inference from a single observation about where Glance AI's traction story came from. Conversion data would confirm or destroy it, and a large chunk of §50's rationale rests on it.
5. **Primary user research.** Twenty interviews — ten Glance lock-screen users across device tiers, five who disabled it, five Glance AI users — would convert §20, §21 and §45 from inference to evidence. The specific question worth asking: *would you install this if it were not already on your phone?*
6. **OEM contract terms.** Duration, exclusivity, renewal mechanics and revenue-share structure determine how urgent the entire thesis is. Long-dated contracts with strong protections would substantially reduce the pressure §57 R1 describes.
7. **Hands-on product access on a pre-installed device.** §24–§27 are heuristic for exactly this reason. An instrumented accessibility audit alone would replace seven hypotheses with seven findings.
8. **Glance AI cohort retention.** The 18-looks-per-day figure is a snapshot of engagement intensity, not of durability. Week-4 and week-12 retention would tell us whether Glance AI is a novelty or a habit — which determines whether the intent thesis has anywhere to go.

---

## 6. Methodology note

**Research date:** 6 August 2026. Every "current" statement should be read as of that date. InMobi's DRHP had not been filed at the time of writing.

**Method.** Public web research across company and product sources, Indian and international trade press, revenue-modelling aggregators, market-research summaries, consumer-tech publications and OEM support communities. Financial and usage figures were cross-checked against at least two sources wherever two existed; where they conflicted, both were recorded in §3 and neither was averaged. Undisclosed baselines were left undisclosed.

**Reasoning sequence.** Research preceded thesis formation. The per-user calculation was performed during research, after noticing that Glance's reported revenue and reported user base had never been placed next to each other in anything I read. That juxtaposition produced the thesis; the thesis was not brought to the research. The feature proposal in §50 was written **after** §§14, 16, 21, 22, 23, 29, 30, 34, 36 and 44 had independently identified the same absence; those ten sections are named in §50 so a reader can verify the convergence rather than take it on trust.

**Known method limitations.**
- No primary research of any kind. No interviews, no surveys, no telemetry.
- No hands-on access to Glance on a pre-installed device, which caps §24–§27 at heuristic quality.
- Heavy reliance on trade press and modelling services for financials, in a pre-DRHP situation where those sources demonstrably contradict each other.
- The anchor calculation is mine, performed on contested inputs, and stated with more precision than it deserves (§3.1).
- Single-analyst work with no adversarial review. Nobody argued the bull case before the thesis was committed to — and there is a real bull case: a profitable billion-dollar ad business, 33.5% Glance growth, a genuinely loved AI product, and an Indian listing market that may reward scale narratives regardless of per-user economics.
- English-language sources only. Hindi and regional Indian business press likely carries additional detail on the IPO process.

**Diagrams.** All Mermaid, rendered natively by GitHub. No raster image files are generated or referenced.

**Disclosure.** Independent analysis. No relationship with InMobi or any company named. **Explicitly not investment advice**, and specifically not usable as an input to any decision regarding InMobi's forthcoming public offering.

---

*Companion to `README.md` — Day 41 of 90 — Gaurav Singh*
