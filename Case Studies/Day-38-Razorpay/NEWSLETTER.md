# The company that grew 65% and got poorer

### What happens when the product you sell has a regulated price of zero

---

Razorpay grew revenue 65% last financial year. In the same year, its gross profit grew 41%.

Both numbers were published together, usually in the same paragraph. Almost every headline led with the 65%. The 41% is the more interesting one, and it says something the 65% hides: Razorpay's gross margin fell while it was winning.

Roughly 34% in FY25, against somewhere between 36.6% and 39.5% the year before. The range exists because two incompatible FY24 revenue figures are in circulation. It doesn't matter much — margin compressed under either one.

A payments company whose gross profit grows 24 points slower than its revenue is telling you something precise. The incremental transaction is worth less than the average one it already had.

## Why this is happening

UPI, the rail that carries most of India's digital payments, is regulated at zero merchant discount rate. Has been since January 2020.

Every UPI payment Razorpay processes costs money to process and earns nothing. Not "earns a thin margin." Earns nothing.

So Razorpay does not have a pricing problem — a pricing problem can be fixed with a pricing page. It has volume it is legally forbidden from pricing, and that volume is the fastest-growing part of its mix. No product decision changes this. No amount of engineering excellence changes it.

## The part that took me a while to see

I started thinking of Razorpay as a payments company with a sensible adjacent-products strategy — banking, credit, payroll bolted onto a core business.

I now think that's backwards.

Razorpay is an adjacent-products company obliged to run a payments business at declining margin in order to acquire the customers and the data those products need. The gateway isn't the business anymore. It's the customer acquisition cost, paid in gross margin instead of cash.

Read that way, a lot of otherwise odd decisions line up. RazorpayX launched in 2019, years before the margin pressure became visible. The acquisitions bought product lines, not customers — Opfin for payroll, Ezetap for offline, Curlec for Malaysia. The company has plenty of customers. It doesn't have enough products per customer.

And Curlec is the sharpest tell. Malaysia and Singapore are markets where a merchant fee on real-time payments still legally exists. Razorpay is expanding into places where it's allowed to make money on payments.

## Two more pieces of evidence

**The 83% problem.** In FY24 — the last year with a clean segment disclosure — 83% of revenue came from payment aggregation. One rupee in six came from everything else. The strategy is right; the execution is early. Growing 17% of your business fast doesn't offset compression on the other 83% unless the differential is enormous and sustained.

**The RBI embargo.** From December 2022 to December 2023, the Reserve Bank prohibited Razorpay from onboarding new merchants pending final Payment Aggregator authorisation. A year with the growth engine switched off. Revenue grew anyway.

That's a useful stress test, and it points somewhere counterintuitive. If the installed base grows revenue on its own, acquiring more merchants isn't the constraint. Razorpay reportedly has 12 million of them. Adding more long-tail merchants — who transact almost entirely on UPI — makes the margin problem worse, not better.

Razorpay is one of the rare companies where acquisition growth is currently margin-dilutive.

## The open question

I can't verify the thesis directly.

The number that would settle it is UPI's share of TPV, year over year. Not disclosed. The FY25 segment revenue split would also settle it. Not disclosed either — and the DRHP containing both was filed confidentially with SEBI in June, so the most informative document about this company sits where nobody can read it.

What I have is the gross profit differential. If the revenue mix had genuinely shifted toward high-margin banking and credit, gross profit should have grown *faster* than revenue. It grew 24 points slower. That's an inference, not a fact, and it's the weakest joint in the argument.

A bigger gap: I never checked whether PayU and Cashfree show the same compression. If they don't, this isn't structural — it's a Razorpay execution problem, and I've written the wrong essay.

## What I'd build

If the moat is multi-product attach — and I think it is, because switching cost comes from accumulated financial state, not from the payment integration — then the problem isn't acquiring merchants. It's that a merchant with only the gateway never discovers anything else.

Two silent failures. Either the merchant has a cash-flow problem they've never articulated as a problem, or they've articulated it and solved it with their bank, because they don't associate Razorpay with anything beyond payments.

So: a money-position view, free, for every merchant including payment-only ones, built entirely from data Razorpay already holds. What settled, what's coming and when, what was deducted and why. Then pre-underwritten credit shown *inside* it — as an available number, not an application form — at the moment a cash gap is predicted.

Razorpay can see a small merchant's gross revenue before that merchant's own bank can. That asymmetry is the one genuinely unique asset in the company, and right now it's expressed as a credit product the merchant has to go and find.

The delighter isn't the AI. It's the absence of a form.

## What I'm taking with me

**When your headline metric and your margin metric disagree, believe the margin metric.** Ask which of your numbers would still look good if your economics were quietly deteriorating — then watch that one instead.

**Test whether your growth metric improves when your product gets structurally worse.** Razorpay's TPV rises fastest exactly when the margin-destroying input rises fastest. A metric that goes up as your business gets worse isn't neutral — it's harmful, and plenty of companies have one without knowing it.

**Build the cheap half first and let it try to kill the expensive half.** The position view costs a fraction of the forecasting engine on top of it. Ship it alone, with a decision rule committed in advance for what result means the expensive part never gets built. That turns a large bet into a small bet plus information.

**And keep conflicting data conflicting.** I had two incompatible revenue figures. Averaging them would have produced one clean number that was true under neither reading. Carrying both showed the conclusion held either way — which is a stronger result than a tidy one.

---

**Full case study:** [Day 38 — Razorpay](https://github.com/gaurav-product/product-management-case-studies/tree/main/Case%20Studies/Day-38-Razorpay) — 65 sections, plus an `ASSUMPTIONS.md` documenting every evidence grade, source conflict, and author-constructed element.

**Day 38 of 90.**

*A note on the data: the DRHP is confidential, so detailed financials aren't public. Two FY24 revenue figures are in circulation (₹2,475 cr and ₹2,293 cr) and I've carried both rather than picking one. The widely quoted "$180 billion TPV" is attributed to both FY24 and 2026 across sources, so at least one is stale and I haven't used it. The merchant count comes only from secondary aggregators. The personas, the feature proposal and every RICE score are mine, not Razorpay's.*
