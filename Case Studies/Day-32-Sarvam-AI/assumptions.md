# Assumptions Log — Day 32: Sarvam AI

**Companion to:** `README.md`
**Author:** Gaurav Singh
**Case study date:** July 28, 2026
**Research window:** July 28, 2026, public web sources only

## Purpose

This file exists so that every quantitative and material claim in the case study can be traced to a source and weighted by how much that source can bear. Nothing here is included to pad the record. If a number appears in the README, it appears here with a tier. If a number a reader would expect is absent from the README, it is listed in Section E as undisclosed rather than estimated silently.

## Tier definitions

| Tier | Meaning | How it may be used |
|---|---|---|
| **Tier 1** | Company statement, official filing, government release, or product documentation | Stated as fact, attributed |
| **Tier 2** | Established press reporting from a named outlet with editorial process | Stated as reported, attributed |
| **Tier 3** | Aggregator, secondary blog, unlisted-share site, or third-party estimator | Flagged as weak; never load-bearing for a conclusion |
| **Tier 4** | Undisclosed | Named as a gap; never estimated and presented as a figure |
| **AUTHOR** | Author's construction, arithmetic, or judgement | Labelled `ASSUMPTION — VALIDATION REQUIRED` inline in the README |

---

## A. Tier 1 — Company, government, and documentation

**A1.** Series B first close of $234 million against a $300 million target, post-money valuation $1.5 billion, announced June 15, 2026. Source: Sarvam AI announcement.

**A2.** HCLTech lead strategic investor at $150 million; Bessemer Venture Partners participating; Khosla Ventures and Peak XV Partners following on. Source: Sarvam AI announcement, corroborated by TechCrunch.

**A3.** Series B use of proceeds stated as continued research on a next frontier model for agentic, coding, and cybersecurity use cases, plus compute expansion for a forward-deployed motion across verticals. Source: Sarvam AI announcement.

**A4.** Conversational platform handling more than 2 million interactions daily. Source: company statement via press. Note: "interactions" is not defined publicly — turn, conversation, and API call would give very different numbers.

**A5.** Speech models transcribing more than 500,000 hours of audio monthly. Source: company statement via press. Same definitional caution.

**A6.** Sarvam-105B: 105 billion parameters, sparse mixture of experts, 128 experts, Multi-head Latent Attention, 128,000-token context, trained on approximately 12 trillion tokens across 22 Indian languages, Apache 2.0. Source: company model blog as reported in Forbes, March 7, 2026.

**A7.** Sarvam-30B trained on approximately 16 trillion tokens. Source: as A6. See conflict D1 on active parameters.

**A8.** Indic tokeniser fertility of 1.4 to 2.1 tokens per word across Indic scripts, against 4 to 8x for standard multilingual tokenisers. Source: Sarvam-1 tokeniser blog as cited in Forbes.

**A9.** Model weights published on Hugging Face and AI Kosh on March 6, 2026, roughly three weeks after the February 18 announcement. Source: Forbes, citing Sarvam's Hugging Face organisation.

**A10.** Self-reported benchmark results: Math500 98.6, MMLU 90.6, LiveCodeBench v6 71.7, AIME 2025 88.3, BrowseComp 49.5 against DeepSeek R1 3.2. Source: Sarvam model blog, reported in Forbes. **Explicitly self-reported and labelled as such at every occurrence in the README.**

**A11.** IndiVibe, the Indic evaluation benchmark, was designed by Sarvam, translated by Sarvam, run on Sarvam-selected prompts, and judged by Gemini. Source: Forbes, March 7, 2026. This is the single most load-bearing sourced claim in the case study and rests on one outlet's characterisation; it has not been independently confirmed against Sarvam's own methodology documentation in this pass. Treated as Tier 1-adjacent because it describes the company's own published artifact, but readers should note the single-source dependency.

**A12.** SBI Life partnership reaching more than 8 crore customers and supporting more than 3.5 lakh distributors, built on Samvaad and Arya. Source: Sarvam AI post on X, February 26, 2026, and Sarvam customer story page.

**A13.** SBI Life voice policy servicing in 11 Indian languages, covering fund value, premium due dates, and surrender calculations, designed for noisy conditions and Hinglish. Source: company and partner statements via Elets BFSI and Convergence Now.

**A14.** SBI Life pilot active in select branches in Maharashtra and Tamil Nadu; nationwide rollout targeted for August 2026. Source: Convergence Now, March 2026, quoting the deployment plan.

**A15.** Vivek Raghavan quoted on the goal that every SBI Life policyholder should be able to get questions answered instantly by a culturally fluent AI voice regardless of language or digital literacy. Source: company statement via Convergence Now.

**A16.** Pratyush Kumar quoted on research-led innovation for AI at India's scale, models that understand voices and read documents at a cost every enterprise and government can afford, and a full-stack offering for enterprises to own and operate sovereign AI. Source: Sarvam Series B announcement.

**A17.** UIDAI has integrated Sarvam technology into Aadhaar services on air-gapped, on-premise infrastructure for voice interaction in 10 languages. Source: PIB release as cited in Forbes.

**A18.** MeitY selected Sarvam in April 2025 under the IndiaAI Mission to develop an indigenous foundational model. Source: MeitY / PIB, reported widely.

**A19.** MeitY confirmed support for 12 organisations building sovereign foundational models: Sarvam AI, Soket AI, Gnani AI, Gan AI, Avataar AI, IIT Bombay Consortium (BharatGen), GenLoop, Zenteiq, Intellihealth, Shodh AI, Fractal Analytics, Tech Mahindra Maker's Lab. Source: Lok Sabha reply reported by Medianama, April 2026.

**A20.** IndiaAI Mission approved March 2024 with a budget of ₹10,372 crore. Source: government documentation, widely reported.

**A21.** IndiaAI Mission compute support to Sarvam of ₹246.72 crore, with a reported 60% counting as equity. Source: government allocation data as cited in Forbes.

**A22.** BharatGen received ₹1,058.52 crore, the largest allocation among the 12 organisations. Source: Medianama, citing the Lok Sabha annexure.

**A23.** BharatGen Param2: 17 billion parameters, mixture of experts, 22 scheduled Indian languages, multimodal, developed with NVIDIA. Source: launch coverage, Business Standard and Forbes India, February 2026.

**A24.** Sarvam-105B trained using over a thousand H100 GPUs at Yotta's Shakti cluster. Source: Forbes, March 2026. See conflict D3 on allocation versus utilisation.

**A25.** Sarvam founded July 2023 in Bengaluru by Vivek Raghavan and Pratyush Kumar. Source: company and Outlook Business.

**A26.** December 2023 raise of $41 million across seed and Series A from Lightspeed, Peak XV Partners, and Khosla Ventures. Source: TechCrunch, December 2023.

**A27.** Sarvam Startup Program launched March 2026: 6 to 12 months of scaled API credits, priority engineering support, and production infrastructure access for selected early-stage companies. Source: company announcement.

**A28.** Product line as documented on company site: Sarvam-30B and 105B, Saaras ASR, Bulbul TTS, Sarvam Vision, Samvaad conversational agents, Arya orchestration, Indus consumer assistant, Kaze smart glasses. Source: sarvam.ai product pages.

**A29.** Samvaad deploys voice AI agents in 11 Indian languages across voice, WhatsApp, and web, with air-gapped deployment for regulated industries and stated pilot-in-a-day, production-in-weeks framing. Source: Samvaad product page.

**A30.** Tata Capital testimonial from Chief Digital Officer Shallu Kaushik on scaling multilingual voice agents across consumer loan products. Source: sarvam.ai customer page.

**A31.** Indus launched on Google Play and Apple App Store, first appearing February 19, 2026 with a waitlist, with access opening February 20. Features: mid-conversation language switching, voice input, document upload and analysis, web-grounded answers, India-hosted infrastructure. Source: Play Store listing, Business Today, Croma Unboxed.

**A32.** Kaze smart glasses announced February 2026, supporting 10+ Indian languages for voice interaction and translation, launch planned May 2026. Demonstrated by the Prime Minister at the summit expo. Source: Wikipedia entries citing launch coverage; company communications.

**A33.** Sarvam stated that 30 to 50 per cent of the $300 million round is allocated to procuring compute and GPU capacity. Source: company statement to ThePrint, June 2026.

**A34.** Anthropic suspended access to two of its most capable models in June 2026 following a US Department of Commerce export control action, with controls lifted at the end of June and access restored July 1, 2026. Source: Anthropic statement. Used only as market context.

---

## B. Tier 2 — Established press reporting

**B1.** Sarvam's annual revenue reported at approximately ₹29 crore, about $3.5 million. Source: The Ken, as cited in Forbes, March 2026. **Single-source, and roughly four months stale relative to the Series B.** This is the weakest load-bearing number in the case study and is flagged as such in §13 and §64.

**B2.** Total venture funding of approximately $54 million before the Series B. Source: Forbes citing TechCrunch.

**B3.** Sarvam-M released May 2025, 24 billion parameters, post-trained on Mistral Small; criticised publicly, with Menlo Ventures investor Deedy Das calling it embarrassing and citing 23 downloads in two days; Sridhar Vembu of Zoho publicly defended the company. Source: Forbes, citing NewsBytes and YourStory.

**B4.** Sarvam's models did not appear on the Hugging Face Open LLM Leaderboard v1 or v2, had no Arena ranking, and had no formal arXiv paper with methodology, ablations, or peer review as of the March 7, 2026 assessment. Source: Forbes. **Time-bounded to early March 2026; may have changed and was not re-verified in this pass.**

**B5.** Indus recorded approximately 50,000 downloads in its first week. Source: TechCrunch via Forbes.

**B6.** Sarvam selected from a pool of 67 applicants for the IndiaAI Mission foundational model award. Source: reported in multiple outlets including valueforstartups summary; treated as Tier 2 rather than Tier 1 because the primary MeitY document was not read directly.

**B7.** Tamil Nadu committed ₹10,000 crore for a Sovereign AI Research Park. Source: The Ken as cited in Forbes.

**B8.** Odisha signed a reported $2.3 billion MoU for a sovereign AI capacity hub, February 2026. Source: India TV as cited in Forbes.

**B9.** Three sovereign models unveiled at the India AI Impact Summit 2026: Sarvam's twin LLMs, Gnani.ai's Vachana voice stack, BharatGen's Param2. Source: Business Standard, Free Press Journal, February 2026.

**B10.** Gnani.ai voice model covering 12 Indian languages under low-bandwidth conditions, with a reported word error rate below 5%. Source: Business Today and summit coverage.

**B11.** Gnani.ai partnered with Razorpay on an AI platform for managing payment collections during live calls, announced February 26, 2026. Source: Business Today.

**B12.** Krutrim, from Ola / ANI Technologies, was India's first AI unicorn and released a family of Indian-language LLMs. Source: Inc42, Rest of World, DEV community summary.

**B13.** Sarvam announced work with Bosch on in-car AI assistants and with HMD on AI for Nokia feature phones, with limited detail disclosed. Source: TechCrunch, Business Today.

**B14.** India AI Impact Summit 2026 reportedly drew $250 billion in infrastructure pledges, per IT minister Ashwini Vaishnaw. Source: Business Today. Treated as a pledge total, not committed capital, and used only as context.

**B15.** OpenAI and Anthropic have both publicly described India as their second-largest market after the United States. Source: TechCrunch, June 2026.

**B16.** India has more than 800 million internet users. Source: Forbes, March 2026.

**B17.** Reported Indus usability gaps in beta: inability to delete individual chats with account deletion as the only removal path, and no option to disable reasoning mode. Source: Business Today first-look review, February 2026. Single review; not independently retested and may since have changed.

**B18.** Existing Indic evaluation efforts named as insufficient in scale or independence: AI4Bharat Indic LLM-Arena, Microsoft Research India PARIKSHA, MILU, IndicGLUE, IndicIFEval. MILU and IndicGLUE were created by AI4Bharat, whose founders now lead Sarvam. Source: Forbes, March 2026.

**B19.** Sarvam conversational interaction volume reportedly doubled over the two months preceding the June 2026 round. Source: press coverage of the Series B, company-sourced.

**B20.** Pratyush Kumar co-founded AI4Bharat and carries a citation record above 8,200. Source: Forbes citing Google Scholar.

**B21.** Indian coverage of the Series B explicitly linked Sarvam's unicorn round to the Anthropic model access suspension as a sovereignty catalyst. Source: ThePrint, The AI Insider, June 2026.

---

## C. Tier 3 — Weak sources, flagged and never load-bearing

**C1.** Indus cumulative Android installs of approximately 230,000 as of mid-May 2026. Source: AppBrain, a third-party install estimator. Used in the README only to characterise order of magnitude relative to incumbents, and explicitly attributed as an aggregator estimate. Not used to support any conclusion on its own.

**C2.** HCLTech taking a 10.46% stake. Source: TechTimes. Not corroborated in the company announcement read for this study; mentioned nowhere in the README's analytical claims.

**C3.** Sarvam headcount of approximately 200, with 63 open positions of which 25 are engineering, July 2026. Source: careers-page aggregator OwnYourCareer. Used to characterise team size in arguments about surface discipline; the specific figures are weak and the argument does not depend on precision.

**C4.** Reported deployments at CRED, IDFC, and LIC in addition to SBI Life and Tata Capital. Source: Analytics India Magazine via a careers aggregator. Named in the README as "reported engagements" and not treated as confirmed logos.

**C5.** Gujarat MoU on March 18, 2026 for a Sovereign AI Park. Source: a secondary blog. Not used in the README.

**C6.** Reported talks for a $320–350 million round at $1.5 billion with NVIDIA and Amazon participation, April 2026. Source: Outlook Business and an unlisted-share site. Pre-announcement reporting that the actual June close does not fully match; recorded here for completeness and used in the README only in the conflict table.

**C7.** Claims that Indus achieves 98.6% on Math500 and is optimised for Indian educational and legal contexts, plus a Nvidia Nemotron Coalition membership claim. Source: a promotional blog. The Math500 figure traces to Sarvam's own model claim (A10); the coalition claim is uncorroborated and is not used in the README.

**C8.** Bhashini-v2 deployment across MyGov with 140 million users. Source: a secondary analysis blog. Used only as directional context on the public translation layer; not cited as a figure in the README.

**C9.** Sarvam product page claims of sub-100ms latency and 99.9% uptime SLA. Marketing copy rather than measured performance; listed in the README metrics table explicitly as company marketing.

---

## D. Source conflicts — recorded, not resolved

**D1.** Sarvam-30B active parameters per forward pass: Forbes reports approximately 2.4 billion; Wikipedia citing Fortune India reports approximately 1 billion. Not resolved. The primary model card was not read in this pass. Flagged in README §65.

**D2.** Sarvam-105B active parameters: approximately 9 billion in one report, approximately 10.3 billion in another. Reported as a range.

**D3.** GPU figures: allocation reported variously as 4,096 and 4,086 H100s under the mission, while training utilisation is described as "over a thousand" H100s at Yotta's Shakti cluster. Allocation and utilisation are different quantities and both are retained rather than reconciled into a single number.

**D4.** Total pre-Series B funding: $41 million across seed and Series A, versus $54 million total venture capital. Both figures are used in their correct contexts.

**D5.** Series B size: $234 million first close against a $300 million target, against earlier reporting of $320–350 million in talks. First close treated as fact; target as stated intent; larger figures as superseded pre-announcement reporting.

**D6.** Sarvam-30B context window: 32,000 tokens per one source, unspecified in others. Treated as 32k with the ambiguity noted.

**D7.** Indus install figures span two different time windows (first week versus cumulative to mid-May) and two source tiers. Both are reported with their windows stated.

**D8.** SBI Life scale expressed as both "8 crore" and "80 million" and both "11 languages" and "more than 11 languages." Same underlying figures in different notation; standardised in the README.

**D9.** Open-sourcing date: the February 18, 2026 announcement versus the March 6, 2026 weight publication. Both retained because the three-week gap is analytically relevant to the verification argument.

---

## E. Tier 4 — Undisclosed, and therefore not estimated

The following are absent from public disclosure. None has been estimated and presented as a figure anywhere in the README.

Indus DAU, MAU, D7 and D30 retention, and session frequency. Current revenue as of the Series B close. Enterprise ACV, gross margin, net revenue retention, logo churn, and revenue concentration by customer. Inference cost per conversation and cost per resolved conversation. Per-language task accuracy, word error rate, escalation rate, refusal rate, and hallucination rate. Any per-language breakdown at all. Training data provenance, licensing, and consent basis for the Indic corpora. Enterprise conversation log retention periods and whether customer data influences model updates. Kaze shipping status against the May 2026 target. Whether the August 2026 SBI Life nationwide rollout is on schedule. Utilisation rate of the mission GPU allocation. Commercial terms of the HMD and Bosch partnerships. Aadhaar deployment interaction volumes. Startup Program cohort conversion after credit expiry. Any independent reproduction of the published benchmarks completed after March 2026.

---

## F. AUTHOR constructions — labelled inline in the README

**F1.** TAM of $4–8 billion annually for Indian enterprise and government language-and-voice AI. Built by taking Indian enterprise IT and software spend as a base and assuming conversational and document AI reaches a low single-digit share by 2028. The band is wide because the denominator is contested and because Indian enterprise "AI spend" reporting frequently reclassifies existing automation budgets. Labelled `ASSUMPTION — VALIDATION REQUIRED` in §13.

**F2.** SAM of $1.0–3.2 billion, derived as 25–40% of TAM by restricting to BFSI, government, healthcare, and defence workloads with hard residency or air-gapping requirements and non-English primary interaction language. Labelled in §13.

**F3.** SOM of $40–90 million revenue by mid-2028, requiring roughly 12–25x growth off the reported ₹29 crore base. Labelled in §13. Depends entirely on B1, which is stale and single-sourced.

**F4.** Implied valuation multiple of approximately 400x revenue, from $1.5 billion against ₹29 crore. Arithmetic is sound; the inputs are four months apart. Labelled in §13 as directionally useful and numerically unreliable.

**F5.** All RICE inputs in §47 — reach, impact, confidence, and effort for ten initiatives. Entirely author-constructed. The relative ordering is the argument; the absolute values are not evidence. The override of the highest-scoring option is disclosed in the section itself.

**F6.** All Kano classifications in §49, including the judgement that per-language verification evidence is currently Attractive and will convert to Basic within roughly 18 months. The 18-month figure is a judgement, not a forecast with a method.

**F7.** UX and UI audit ratings in §25 and §26. Author judgement from published reviews and product documentation, not structured usability testing. No accessibility audit was performed.

**F8.** All five personas in §20. Composites constructed to represent documented user classes. No user research was conducted and no named individual is depicted.

**F9.** Every number in the two §52 wireframes — accuracy, WER, escalation, hallucination, sample sizes, cost, and latency figures in both the Pramaan Card and Shadow Verification mockups. **These are invented for layout demonstration and are labelled as illustrative at both occurrences.** The Santali 61% and Hindi 88% figures referenced in §50 are hypothetical illustrations of a gap, not measured values, and no reader should attribute them to Sarvam.

**F10.** The Pramaan proposal in its entirety, including the two surfaces, the FR table, the escalation-reason taxonomy, the success criteria, the rollout sequencing, and the three experiments. Author's design work.

**F11.** The Verified Resolved Conversations north star definition in §31, including the four qualifying conditions.

**F12.** All risk likelihood and impact ratings in §57.

**F13.** The central analytical claim of the case study — that verifiability rather than capability or capital is Sarvam's binding constraint over the next four quarters, and that verification is a commercially aligned product opportunity rather than a compliance burden. This is the author's argument. Its supporting facts are sourced above; the inference from those facts is not sourced and is open to dispute. The strongest counterargument is stated in §50.

**F14.** The strategic recommendation to reduce Indus to maintenance status and gate Kaze. Author's judgement, resting on C1 install estimates and C3 headcount, both Tier 3.

**F15.** The characterisation of state MoUs as political commitments rather than revenue. This is analytically standard but is the author's framing, not a company or press characterisation.

---

## G. Known limitations of this study

1. No primary research. No interview with any Sarvam employee, customer, investor, or competitor.
2. No independent model testing. Weights are publicly available under Apache 2.0 and were not downloaded or evaluated. A study whose central argument is that claims require verification did not itself verify the claims, and that irony is disclosed rather than hidden.
3. Time-bounded verification claims. B4 describes the state of leaderboard and Arena presence as of March 7, 2026. Independent evaluation may have progressed since; one source notes an independent tracker had begun monitoring Sarvam models around mid-2026, which was not confirmed in this pass.
4. Single-source dependency on two material claims: the revenue figure (B1) and the IndiVibe methodology characterisation (A11). Both are flagged where used.
5. Revenue staleness. The financial analysis in §13 rests on a figure that predates the funding round it is compared against.
6. No regulatory review. DPDP Act obligations, IRDAI guidance on AI in insurance servicing, and RBI model-risk expectations are referenced conceptually and were not read in primary form. Any reader applying this study to a real procurement decision should treat the compliance framing as unverified.
7. Language limitation. All sources consulted were in English. Coverage in Hindi and other Indian languages was not searched and may contain material this study missed, which is a real limitation for a case study about Indic AI.

---

*Companion to `README.md` · Day 32 of 90 · PM Case Study Challenge · Gaurav Singh*
