# PulseAnalytics — positioning (canonical, locked example)

> **Note on this file:** PulseAnalytics is a fictional B2B SaaS analytics platform used as the running example throughout this quickstart. The positioning below is illustrative — generic enough to apply across SaaS verticals, specific enough to feel like a real product. **Replace this file with your own company\'s positioning.** Keep the structure; replace the content.

---

## Anchor

PulseAnalytics is **the marketing analytics layer that traces revenue back to specific campaigns without an engineering quarter.**

Not just another dashboard. Not another Mixpanel-vs-Amplitude tradeoff. A different category — purpose-built so marketing operators can answer "what drove that pipeline?" the same week the deal closed, instead of waiting for the data team to build a custom report.

## Target customer

VP Marketing or Head of Demand Gen at a growth-stage B2B SaaS company ($5M-$50M ARR, 20-150 employees). The kind of operator whose CEO asks "what's driving pipeline this quarter?" in Monday standup and who has spent the last 18 months stitching together Salesforce + GA4 + a spreadsheet to answer the question.

See [`ICP.md`](./ICP.md) for the full profile.

## Status-quo alternatives

The world this customer lives in today, and why each existing path falls short:

- **Spreadsheet stitch from Salesforce + GA4** — most common. Brittle, fragile to changes in either source. Costs the VP 4-6 hours a week of personal time before the Monday review.
- **Mixpanel / Amplitude / Heap** — built for product analytics, not marketing. Pipeline attribution is bolted on, never first-class. Most marketing teams use them for funnel metrics but bypass them for revenue-tracing.
- **Custom-built data warehouse + BI tool (Snowflake + Looker, Redshift + Tableau)** — works, eventually. Takes 4-6 months and an engineering team to implement. By the time the dashboard is live, the original question has changed.
- **Bizible / Dreamdata / HockeyStack** — closest competitors. Strong on attribution; weaker on the "what should I do about it?" layer. Tend to assume the customer is sophisticated enough to interpret raw attribution data and decide actions independently.
- **Live without it** — give up on revenue-tracing, run on instinct + last-touch attribution. Many teams do. The cost shows up in defensive Monday reviews where the VP can't answer the CEO's question.

## Key differentiators

- **Implementation in days, not quarters.** Pre-built connectors for Salesforce / HubSpot / Marketo / Stripe + a templated revenue-tracing model that ships configured for B2B SaaS by default. Most customers see their first useful attribution within 2 weeks of starting.
- **Answers questions, not just metrics.** The product is built around the questions a VP Marketing actually asks ("which campaigns drove enterprise pipeline last quarter?" "is the ABM program paying back?") instead of generic funnels you have to interpret yourself.
- **Pipeline reviews as a first-class feature.** Built-in templates for the weekly pipeline review, the QBR pipeline section, and the board-deck pipeline slide. The output IS the deliverable, not a dashboard you screenshot.
- **No data team required.** A VP Marketing with no engineering support can stand up and run the system. That's the user persona we test against; that's the success criterion.

## Value propositions (per priority)

1. **You stop owning the pipeline-review prep.** Get back the 4-6 hours a week you spend stitching the same report. Time goes to actual marketing decisions instead.
2. **Your Monday reviews stop being defensive.** When the CEO asks "what's driving pipeline?", you can answer specifically with the data already in the deck. No "let me get back to you on that."
3. **Your attribution stops being a debate.** First-touch vs. last-touch vs. weighted-multi-touch isn't a culture war when the model is templated and consistent. Sales sees the same data Marketing sees.
4. **Your QBRs and board decks get sharper.** The same data flows into all three downstream artifacts (Monday review, QBR, board deck) without re-stitching. Story compounds across cycles.

## What we are NOT

- **Not a CRM.** We integrate with Salesforce / HubSpot; we don't replace them.
- **Not a marketing automation platform.** We don't send emails or run ad campaigns. We measure what those tools produced.
- **Not a product analytics platform.** We measure marketing-to-revenue contribution; if you need session-level product behavior data, you still need Mixpanel/Amplitude/Heap.
- **Not for early-stage startups under $1M ARR.** Below that revenue level, the pipeline-review problem isn't yet pronounced enough to justify the platform.

## Pricing positioning

Mid-market SaaS pricing. Lower than Bizible/Dreamdata enterprise tiers; higher than self-serve product analytics. Priced per tracked revenue volume + per active marketer seat. The customer should feel the implementation-time savings pay for the platform in the first 90 days.

## Tagline candidates

- "Marketing analytics that answers the CEO's question."
- "Pipeline attribution your VP Marketing can actually run."
- "Stop stitching the Monday review."

Working tagline: **"Stop stitching the Monday review."** — anchors the most painful daily ritual the ICP recognizes immediately.

---

## How this file gets used

Every downstream skill in this repo reads this file when it needs to know "how do we describe PulseAnalytics?":

- `/product-messaging` reads positioning as upstream input to build the messaging library
- Any future content skill (linkedin-post, blog-draft, sales-deck-section) reads from here
- Any future paid skill reads positioning for status-quo alternatives + key differentiators
- Any future outbound skill reads positioning for wedge framing

**This is the compounding axis.** Edit this file → next run of every downstream skill reflects the change. Don't edit ad-hoc copy in 12 places; edit the source here and let the system propagate.

---

## Refresh cadence

Quarterly refresh recommended. Trigger conditions to refresh sooner:
- A new direct competitor enters the market or makes a major move
- Win/loss patterns shift (see future `/win-loss-analysis` outputs)
- ICP feedback indicates positioning is landing differently than expected

Last refreshed: 2026-05-17 (V1 example seed)
Owner: VP Marketing
