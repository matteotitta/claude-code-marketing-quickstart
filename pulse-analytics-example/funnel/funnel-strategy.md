# PulseAnalytics — funnel strategy (canonical, locked example)

> **Note on this file:** PulseAnalytics is a fictional B2B SaaS analytics platform used as the running example throughout this quickstart. The funnel below is illustrative — generic enough to apply across SaaS verticals, specific enough to feel like a real product. **Replace this file with your own company's funnel.** Keep the structure; replace the content.

---

## GTM motion classification

**Hybrid — PLG entry, SLG expansion.**

Evidence from the product + ICP:

- **PLG signals:** self-serve trial available on the website (no required demo before access); pricing page lists a Starter tier at $0/seat for ≤5 users; product onboarding walks new users through connecting Salesforce + GA4 without sales involvement; first-value moment (templated revenue-tracing report) lands in the first session.
- **SLG signals:** target ICP is VP Marketing at $5M-$50M ARR companies — typically 20-150 employees — which is too small for true Enterprise sales motion but too considered for pure self-serve closure. Annual contracts. Multi-stakeholder buying (VP Marketing + RevOps + Finance signatures common). Average ACV $24K — past the threshold where a sales-assisted close pays back.

Conclusion: leads enter via PLG (free trial), but most paid conversions are sales-assisted. Funnel must support both motions without forcing every lead through sales touch.

## Pre-close stages

### 1. Aware (top of funnel)

**Entry trigger:** first website visit from an organic, paid, or referral channel.

**Definition:** a person from a target-ICP company hits the website, reads at least one page beyond the homepage. Not yet identified.

**Leading indicators (inputs):** unique visitors from ICP-fit accounts (Clearbit Reveal), referring sources, content engagement (time on page > 90s).

**Lagging indicator (output):** % of awares who become known (email or LinkedIn identified) within 30 days.

**Exit to next stage:** identified — provides email, signs up for trial, books demo, or accepts a 1:1 outreach.

### 2. Identified (warm interest)

**Entry trigger:** visitor provides identity (trial signup, demo request, content download, outbound reply, LinkedIn DM reply).

**Definition:** a known person from a target-ICP company. May or may not have product access yet.

**Leading indicators:** trial signups, demo bookings, content downloads, replies to outbound, LinkedIn engagement signals.

**Lagging indicator:** % of identifieds who reach the activation moment within 14 days.

**Exit to next stage:** product activation (see Activated below) OR sales-qualified conversation (see Qualified below).

### 3. Activated (PLG path) OR Qualified (SLG path)

These two stages run in parallel; a lead can be in either or both.

**Activated (PLG path)**
- Entry trigger: completes the activation moment — connects Salesforce + GA4 to the trial and runs the first templated revenue-tracing report.
- Definition: has experienced the product's core value at least once.
- Leading indicators: connector-completion rate within 24 hours of signup; first-report-generated rate within 72 hours.
- Lagging indicator: % of activated trials that book a demo or convert to paid within 30 days.

**Qualified (SLG path)**
- Entry trigger: completes a discovery call where Fit, Authority, Need, and Timing (FANT) are confirmed.
- Definition: matches ICP firmographically AND has a budget owner involved AND has a defined pain matching the value prop AND has timing within 6 months.
- Leading indicators: discovery calls held; FANT scoring per call.
- Lagging indicator: % of qualifieds who reach Evaluation within 14 days.

### 4. Evaluation

**Entry trigger:** the buyer has signaled intent to make a decision — typically by including additional stakeholders (RevOps lead, finance), requesting a proposal, or starting a paid pilot.

**Definition:** a real evaluation in progress with multiple stakeholders engaged.

**Leading indicators:** stakeholder count on calls, paid-pilot starts, proposals sent, security review initiated.

**Lagging indicator:** % of evaluations closed-won within 30 days (target: ≥60%).

**Exit to next stage:** closed-won (signed contract + first invoice paid) OR closed-lost (decided against).

### 5. Closed-Won

**Entry trigger:** contract signed, first invoice paid.

**Definition:** revenue recognized. Move to post-close stages.

### 5'. Closed-Lost

**Entry trigger:** prospect explicitly declines or goes dark for 30 days post-evaluation.

**Tagged with one of 5 loss reasons:** competitor chosen / budget / timing / no-decision / poor-fit.

**Re-entry path:** see "Closed-lost re-entry" section below.

## Post-close stages

### 6. Onboarding

**Entry trigger:** contract signed.

**Definition:** customer is being implemented — connectors wired, team trained, first quarterly review modeled.

**Leading indicators:** Salesforce + GA4 + Stripe connectors live within 14 days; first internal weekly review run within 30 days.

**Lagging indicator:** % of new customers who reach Activated (post-close) within 60 days.

### 7. Activated (post-close)

**Entry trigger:** customer's pipeline review is fully run from PulseAnalytics for 4 consecutive weeks. The dashboard is the source of truth, not the spreadsheet.

**Definition:** habitual use; product is part of the operating rhythm.

**Leading indicators:** weekly active users from the customer's marketing team, # of revenue-trace reports generated per week.

**Lagging indicator:** % of activated customers who renew at 12 months (target: ≥90%).

### 8. Expansion

**Entry trigger:** customer adds seats, upgrades to a higher tier, or expands to a new business unit.

**Definition:** revenue growth on an existing account.

**Leading indicators:** customer-initiated upgrade requests, new business units inquiring about access, headcount growth signals at the customer.

**Lagging indicator:** net revenue retention (target: ≥115%).

### 7'. Churn-Risk

**Entry trigger:** weekly active users from the customer drops to zero for 2 consecutive weeks OR the primary champion leaves the customer company.

**Action:** AE + CSM joint outreach within 48 hours; product team flagged for product-led recovery (e.g., re-training session).

**Re-entry to Activated:** champion replaced + usage restored.

## FETE mapping

For lead prioritization (consumed by `/lead-scoring`):

| Signal | Fit | Engagement | Tier | Eligibility |
|---|---|---|---|---|
| Company size 20-150 emp | ✓ | | | |
| ARR $5M-$50M | ✓ | | | |
| VP Marketing or Head of Demand Gen as champion | ✓ | | | |
| HubSpot or Salesforce as CRM | ✓ | | | |
| Connected trial within 72hrs of signup | | ✓ | | |
| Generated 3+ reports in trial | | ✓ | | |
| Multi-stakeholder discovery call | | ✓ | | |
| Enterprise tier prospect (>$50M ARR) | | | high | |
| Mid-market tier ($5M-$50M ARR) | | | medium | (default) |
| SMB tier (<$5M ARR) | | | low | |
| In active evaluation with competitor | | | | gated — needs differentiated outreach |
| Decision-maker is a former PulseAnalytics customer | | | | priority |

## Closed-lost re-entry

Per the 5 loss-reason tags, different re-entry paths apply.

- **Competitor chosen** → re-enter at Aware in 9 months (give the competitor a chance to fail; check status at month 9 via LinkedIn signal + outbound)
- **Budget** → re-enter at Identified in 6 months (budget cycles are typically annual)
- **Timing** → re-enter at Identified on the date the prospect told us they'd revisit (calendar reminder)
- **No-decision** → re-enter at Aware via nurture sequence (low-touch monthly content + 1 outbound at month 6)
- **Poor-fit** → do not re-enter unless ICP shifts. Move to `marketing/icp/anti-icp.md` and learn.

## Refresh cadence

Quarterly. Trigger sooner if:
- Win/loss data shows a stage is being skipped or misaligned in practice
- A new buyer persona emerges (e.g., CMO at larger ARR brackets)
- The product changes the activation moment (then the activation stage definition must update)

## Owner

VP Marketing + Head of Revenue Operations (jointly — marketing owns pre-close, RevOps owns post-close, both align here).
