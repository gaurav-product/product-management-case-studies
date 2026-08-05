# The Company That Charges You When Its AI Tries

### What happens when one half of a business meters what customers accumulate, and the other half meters what they want less of

One software company charges $0.49 every time its AI attempts to solve a customer's problem. Its closest competitor charges $0.99 — but only when the problem is actually solved.

The first price looks better. It is not. It is half the price because it is selling half the thing.

The company is Freshworks, which reported Q2 results on Monday. Going through the numbers, I found one of the cleanest examples I have seen of a pricing decision quietly determining a product strategy.

## Two companies, one brand

Freshworks reported $237.4 million in revenue last quarter, up 16%, its first GAAP-profitable quarter of the year and its eighth straight quarter clearing the Rule of 40. Solid, unremarkable, good execution.

Split it in half and it stops being unremarkable.

The Employee Experience business — IT service management, the service desk your own company uses when your laptop breaks — reached $567 million in annual recurring revenue, growing 24%. The Customer Experience business — Freshdesk, the ticketing product the company was founded on and named after — sat at just over $395 million, growing 6%. Management has told investors to expect low single digits from CX all year.

Same company. Same AI. Same engineers. One half compounding, one half flat.

The easy explanation is competition: Zendesk and Intercom are strong, customer service is crowded, ITSM is more winnable. All true, and I think incomplete.

## Look at the price lists

Here is what changed my mind. Both halves have solved the hard problem of AI monetisation — both have a way to charge that is not a per-seat licence. But they picked different units.

In IT service management, the unit is the **Asset Unit**, sold in packs of 500, metered against the assets in a customer's estate. In customer service, it is the **AI Agent session**, sold at $49 per 100.

Those look like the same kind of thing on a price sheet. In a budget meeting they are opposites.

Assets accumulate. A company hires, opens an office, buys laptops, spins up cloud instances — and the asset count rises without anyone at Freshworks selling anything. The meter grows on the customer's side of the table, as evidence of their own growth. Nobody resents that invoice.

AI sessions are something a customer actively wants fewer of, and a session is billed whether or not it resolved anything. So the customer gets a bill for a number they are trying to reduce, measuring an outcome they cannot verify.

One meter grows by itself. The other is a line item to negotiate down at every renewal.

## The part that makes it worse

Freshworks' AI works. The company's own marketing cites resolution rates up to 80%, with named customers reporting 54% and 30% of queries handled without a human.

Now notice what that does. Customer service is priced per human agent, per month. Every ticket the AI handles well is pressure on the number of agents the customer needs. The compensating meter — sessions — charges 49 cents for an attempt the customer cannot audit.

So in customer service, the better the AI gets, the smaller the meter runs.

In IT service management the same technology does the opposite, because the meter is not primarily the human. It is the asset. And the biggest growth motion there is extending the service desk into HR, facilities and finance, which *adds* teams and seats faster than automation removes them.

Same AI. Opposite effect. The difference is what each side decided to count.

You can see it in what the company reports. Every headline AI number Freshworks publishes is a Copilot number — the $29-per-agent-per-month product that makes a human faster, now attached to over 71% of new enterprise deals. Copilot is the easiest AI money in enterprise software, and it is a bet that human agents keep existing.

Meanwhile Intercom charges $0.99 when its AI resolves something and nothing when it does not. Zendesk charges roughly $1.50 to $2.00 per automated resolution, and its CEO used a stage this year to declare the deflection era over. Freshworks is the last major vendor here still billing for the attempt.

## The open question

I want to be honest about the limit of this argument. The mechanism is real and points the right way. I have not proved how much of the 24-versus-6 gap it explains — saturation and strong competitors explain some of it, and I cannot tell you the split.

There is also a counter-argument I take seriously: human support agents are not disappearing quickly, and Freshworks may simply be pragmatic while competitors take the pricing risk. If agent headcounts prove stickier than I assume, its position is better than I have described.

## What I would build

One thing, and it is smaller than it sounds: make a verified resolution a real object in the product.

Define it strictly — no human ever touched it, the customer did not come back within seven days, no negative satisfaction score. Then show customers a ledger: what your AI actually resolved, what it attempted and failed, and why it failed, broken down by question type.

That gives a support director something they can put in front of a CFO, and gives the product team a signal about which topics are failing. Only then, once you can prove a resolution happened, can you charge for one.

I would ship the ledger first and treat the pricing change as a separate decision, tested against a control group. If the reporting alone changes behaviour, the expensive billing rework is unnecessary — worth discovering before spending the money rather than after.

## What I am taking with me

**The metering unit is a product decision, and it usually gets made without a PM in the room.** What you charge for determines what your product must become. It is not downstream of strategy. It is strategy.

**Meter what your customer accumulates, not what they are trying to reduce.** Two usage-based meters can look identical on a price sheet and point in opposite directions in a budget meeting. Ask which side of the table the number grows on.

**Be suspicious of any metric that measures an absence.** "Containment" counts tickets no human touched. It cannot tell a customer who was helped from a customer who gave up. Metrics that measure what did not happen are usually hiding the difference between success and abandonment.

---

Full case study, with all 65 sections and the evidence grading: [Day 40 — Freshworks](https://github.com/gaurav-product/product-management-case-studies/tree/main/Case%20Studies/Day-40-Freshworks)

**Day 40 of 90.**

*A note on the data: Freshworks discloses total revenue and banded customer counts, but not total ARR or the EX/CX split. Those figures come from earnings commentary, so I have graded them Medium confidence, and the Q2 CX figure is my own arithmetic. Two sources report different FY2025 ARR totals — $907 million and $917 million — and I kept both rather than picking one. The Intercom and Zendesk prices come from pricing analyses, not those vendors' own price lists. Full conflict log is in ASSUMPTIONS.md.*
