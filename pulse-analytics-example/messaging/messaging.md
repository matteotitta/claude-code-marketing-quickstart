# PulseAnalytics — messaging library (canonical example)

> **Note on this file:** PulseAnalytics is the fictional B2B SaaS analytics platform used throughout this quickstart. The 10-component messaging library below is illustrative — generic enough to apply across analytics tools, specific enough to feel real. **Once you have your own data you Replace this with your own messaging library (run `/product-messaging` against your website + positioning). Keep the 10-component structure; replace the content.

Reads from [`marketing/positioning/positioning.md`](../positioning/positioning.md) for upstream context. Every downstream content / paid / outbound / lifecycle skill reads from this file.

---

## 1. Positioning statement

PulseAnalytics is the marketing analytics layer that traces revenue back to specific campaigns without an engineering quarter.

## 2. Value propositions (in priority order)

1. **Stop owning the pipeline-review prep.** Get back 4-6 hours a week of personal time before Monday standup. The template generates the same chart-set every week from one connected data source.
2. **Stop being defensive in Monday reviews.** Answer the CEO's "what's driving pipeline?" question with specific data, not "let me get back to you."
3. **Stop debating attribution with sales.** One model, same numbers in both dashboards. The first-touch vs. last-touch culture war ends.
4. **Make QBRs and board decks compound.** Same data flows into Monday review, QBR, and board deck without re-stitching.

## 3. Key differentiators

- Implementation in days, not quarters
- Built around the questions a VP Marketing asks, not generic funnels
- Pipeline reviews as a first-class feature (templated output, not a screenshot)
- No data team required

## 4. Status quo alternatives (what the buyer does today)

- Spreadsheet stitch from Salesforce + GA4 (most common, brittle)
- Mixpanel / Amplitude / Heap (product analytics, not marketing)
- Custom warehouse + BI tool (4-6 months + engineering)
- Bizible / Dreamdata / HockeyStack (enterprise tier, interpretation burden)
- Live without it (defensive Monday reviews)

## 5. Taglines

Working tagline: **"Stop stitching the Monday review."**

Alternates:
- "Marketing analytics that answers the CEO's question."
- "Pipeline attribution your VP Marketing can actually run."

## 6. CTA variants

- **Primary:** "See your pipeline attribution in 30 minutes."
- **Secondary:** "Book a 15-minute walkthrough."
- **Footer:** "Try the pipeline-review template."

## 7. Proof points

- Pre-built connectors for Salesforce / HubSpot / Marketo / Stripe
- Templated revenue-tracing model ships configured for B2B SaaS by default
- Most customers see first useful attribution within 2 weeks of starting
- [Customer count] — populate when real customers ship; do NOT invent

## 8. Messaging hierarchy (by audience)

- **VP Marketing (champion):** Lead with "stop owning the pipeline-review prep" — their daily pain
- **CEO / CRO (economic buyer):** Lead with "defensible answer to 'what's driving pipeline?'" — their oversight question
- **Sales (internal stakeholder):** Lead with "one model, same numbers" — their attribution-debate pain
- **Marketing team (end users):** Lead with "no data team required" — their access friction

## 9. What we are NOT (anti-positioning)

- Not a CRM. Not a marketing automation platform. Not a product analytics platform.
- Not for early-stage startups under $1M ARR.

## 10. Headlines (per channel)

- **Homepage hero:** "Stop stitching the Monday review."
- **Pricing-page hero:** "Pipeline attribution priced for growth-stage teams."
- **LinkedIn-content hook:** "Most VP Marketing weeks die on a Sunday-evening spreadsheet."
- **Cold email subject:** "Your Sunday pipeline-stitching ritual"

---

## How this file gets used

Every execution skill reads this file when it needs marketing copy:

- `/landing-page-copy` pulls headlines + value props + CTAs
- `/linkedin-content` pulls hooks + proof points
- `/outreach-emails` pulls subject lines + opener variants
- `/ad-creative-brief` pulls headlines + CTAs
- `/lifecycle-marketing` pulls value props in priority order per email

**Editing this file changes every downstream output on next run.** Single source, propagates everywhere.

## Refresh cadence

Quarterly. Trigger sooner if positioning refreshes (messaging depends on positioning) or a value prop stops landing in customer conversations.

Last refreshed: 2026-05-18 (V2 example seed)
Owner: VP Marketing
