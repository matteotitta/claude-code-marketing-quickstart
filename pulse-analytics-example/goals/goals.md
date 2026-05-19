# PulseAnalytics — goals (canonical, locked example)

> **Note on this file:** PulseAnalytics is a fictional B2B SaaS analytics platform used as the running example throughout this quickstart. The KPIs below are illustrative — they're a realistic set for a growth-stage B2B SaaS marketing team. **Replace this file with your own company's KPIs.** Keep the structure; replace the content.

---

## Quarterly goal — Q3 2026

**Drive $1.2M of new ARR through marketing-sourced pipeline.**

That headline number breaks down into 4 KPIs across the funnel. Each KPI has a baseline, a target, a measurement source, and an owner.

## KPIs

### 1. Marketing-sourced pipeline

**What:** ARR attributed to marketing-originated leads (i.e., the first touch was a marketing channel, not sales outbound or referral).

**Baseline (Q2 2026):** $740K.

**Q3 2026 target:** $1.2M (+62%).

**Measurement source:** PulseAnalytics dashboard, "marketing-sourced pipeline" view. Pulled weekly into `marketing/latest.md`.

**Owner:** VP Marketing.

**Cadence:** weekly tracking, monthly review with CEO.

### 2. Trial-to-paid conversion rate

**What:** % of free-trial signups that convert to paid within 30 days.

**Baseline:** 8.2%.

**Q3 2026 target:** 12% (+46%).

**Measurement source:** PulseAnalytics dashboard, "trial conversion" view. Cross-checked against Stripe new-subscriptions data.

**Owner:** Head of Growth (PLG motion lead).

**Cadence:** weekly tracking. Sub-targets per traffic source so we know which channels convert better.

### 3. Demo-to-close rate

**What:** % of demos held with FANT-qualified prospects that close-won within 60 days.

**Baseline:** 28%.

**Q3 2026 target:** 35% (+25%).

**Measurement source:** Salesforce — Opportunities filtered by "Demo Held" stage entry date, cross-referenced with close date.

**Owner:** VP Marketing (shared with VP Sales — marketing owns the quality of the lead handed off; sales owns the close).

**Cadence:** weekly tracking. Monthly win/loss review surfaces patterns.

### 4. AEO citation rate on top-20 buyer queries

**What:** % of our top-20 buyer queries (e.g., "best marketing analytics for B2B SaaS", "Bizible alternative", "how to attribute B2B SaaS pipeline") where PulseAnalytics is cited in the AI answer (ChatGPT, Claude, Perplexity, Google AI Overviews).

**Baseline:** 22% (citation rate, averaged across 4 engines × 20 queries).

**Q3 2026 target:** 50%.

**Measurement source:** Manual weekly check (until we wire an automated tracker via Ahrefs Brand Radar in week 4 — see `marketing/seo-aeo/strategy/`).

**Owner:** Head of Content.

**Cadence:** weekly tracking. Citation gains map directly to article publishes — one article published per gap per week.

## Anti-goals

What we're explicitly NOT optimizing for this quarter:

- **Total website traffic.** We don't care about pageviews. We care about ICP-fit pageviews that convert. Traffic without conversion is a vanity metric.
- **Total trial signups.** Same logic — signups from non-ICP companies waste activation effort and drag the trial-to-paid rate. We'd rather have 200 ICP-fit signups than 600 mixed ones.
- **Brand awareness on LinkedIn.** We post on LinkedIn, but the goal is pipeline-conversion-from-LinkedIn, not impression count. Follower growth is fine but not a KPI.
- **Article output volume.** We're not publishing 30 articles a quarter for the sake of it. Each article maps to an AEO citation gap or a buyer-funnel question. Quality over throughput.

## How these KPIs roll up to the company goal

CEO's company-level Q3 goal: **$2M new ARR.** Marketing sources $1.2M of it (60%); sales-outbound + referrals source the other $0.8M.

If we hit the 4 KPIs above, the $1.2M is mechanical:
- 12% trial-to-paid × ~1,800 trials/quarter × $14K ACV = $604K from PLG path
- 35% demo-close × ~120 demos/quarter × $42K ACV = $529K from SLG path
- The remaining $70K comes from expansion-on-existing-accounts (post-close stage, see funnel-strategy.md).

If any KPI misses badly, the $1.2M misses too. The monthly CEO review focuses on the leading indicator that's drifting + the corrective action.

## Refresh cadence

Quarterly. Re-set at the start of every quarter based on:
1. Last quarter's actual results
2. Company-level revenue plan
3. Major channel/product changes that shift the funnel

## Owner

VP Marketing. Sub-KPI owners listed per KPI.
