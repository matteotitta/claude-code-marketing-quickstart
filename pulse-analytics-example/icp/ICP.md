# PulseAnalytics — ICP (canonical, locked example)

> **Note on this file:** PulseAnalytics is a fictional B2B SaaS analytics platform used as the running example throughout this quickstart. The ICP below is illustrative — generic enough to apply broadly, specific enough to feel real. **Replace this file with your own company\'s ICP.** Keep the structure; replace the content.

---

## Firmographics

- **Company type:** B2B SaaS
- **Revenue stage:** $5M-$50M ARR (growth-stage; past product-market fit, pre-scale)
- **Team size:** 20-150 employees total; marketing team of 3-12
- **Funding:** Series A through Series C, with at least one institutional investor
- **Geography:** primarily North America + UK + Australia (English-first markets where the marketing-ops vocabulary lands clean)
- **Industry:** horizontal SaaS (devtools, fintech, HR tech, sales tech, marketing tech itself) — vertical SaaS works but tends to have different attribution patterns

## Champion persona

**Title:** VP Marketing / Head of Demand Gen / Senior Director of Marketing
**Tenure:** 18+ months in role (long enough to own the pipeline-review ritual)
**Reports to:** CEO or CRO
**Owns:** marketing budget ($500K-$5M annual), attribution model, pipeline contribution targets

**Their week:**
- 4-6 hours stitching last week's pipeline data from Salesforce + GA4 + a Google Sheet
- 1-2 hours preparing the Monday revenue review for the CEO + CRO
- The rest split between: campaign planning, vendor management, team 1:1s, board prep when QBR season rolls around
- The pipeline-review prep is the most personally painful part of their week. Not the work they want to be doing.

**JTBD (job-to-be-done):** "Give my CEO a defensible answer to 'what's driving pipeline?' without losing my entire Sunday to it."

**Job-context triggers:**
- "I'm tired of explaining first-touch vs. last-touch every Monday."
- "Our last QBR took me 3 days to prep because nothing was in one place."
- "When the board asks about marketing's contribution to pipeline, I want to point at a number, not a story."
- "I keep losing arguments with sales about attribution because they have their own dashboard."

**Pain points (in priority order):**
1. **Manual pipeline-review stitching** — Mondays consumed by spreadsheet plumbing
2. **Attribution debates with sales** — Marketing's view of pipeline contribution differs from Sales's; debates eat meeting time
3. **Slow time-to-insight** — by the time the data team builds a custom report, the question has moved on
4. **Defensive Monday reviews** — when CEO asks specific questions, the answer is "let me look into that" instead of a specific data point
5. **Board / QBR sprint** — quarterly attribution prep dominates the two weeks before each board meeting

**Decision criteria (how they buy):**
- Implementation time < 30 days (they've been burned by 6-month BI implementations)
- Doesn't require an engineer (they don't have one on the marketing team, and waiting for shared engineering is the original problem)
- Has templated pipeline-review output, not just "another dashboard"
- Vendor has worked with similar-sized B2B SaaS companies before
- Total spend < 5% of marketing budget (gut feel threshold for "tool spend, not strategic bet")

## Economic buyer persona

**Title:** CEO or CRO (depending on org structure)
**Tenure:** founder or 2+ years into role
**Reports to:** Board / themselves
**Owns:** the question "is marketing working?"

**Buying motivation:** doesn't care about the platform; cares about getting a defensible answer to the pipeline question without having to wait for marketing to assemble it. Approves the PulseAnalytics purchase because the VP Marketing can articulate: "this gets me 4-6 hours back per week + my Monday answer becomes specific instead of hand-wavy."

**Decision criteria:**
- Total cost < 5% of marketing budget
- Implementation time < 1 quarter (doesn't want to commit to something the VP won't have running by next board meeting)
- Marketing-Sales attribution alignment is a deal-maker — if PulseAnalytics produces ONE set of numbers both teams trust, that's the actual win

## Anti-ICP (who NOT to sell to)

- **Companies under $1M ARR.** Pipeline-review pain isn't pronounced enough; cost feels disproportionate.
- **Companies over $250M ARR.** They've already built (or are committed to) custom warehouse + BI stacks; switching cost is too high; their needs have outgrown templated solutions.
- **Marketing teams of 1.** Solo marketers are doing creative + execution; they don't need an analytics platform yet.
- **Companies with a dedicated marketing analyst already in seat.** PulseAnalytics solves the problem that role solves; competing for the same headcount budget is a losing pitch.
- **Vertical SaaS with custom attribution requirements.** E.g., insuretech with regulatory attribution rules, or HR tech with multi-stakeholder buying committees PulseAnalytics's default model doesn't account for. Possible to serve, but slow.

## Where they hang out (acquisition channels)

- **LinkedIn** — primary content channel. VP Marketing reads operators (e.g., Kyle Poyar / Growth Unhinged, Lenny Rachitsky, founder accounts of similar SaaS companies). High-engagement format: contrarian takes on attribution debates.
- **Newsletters** — Growth Unhinged, Lenny's Newsletter, Marketing Brew, The Marketing Millennials. Pieces about attribution / pipeline / marketing-ops measurement land here.
- **Conferences** — SaaStr Annual, B2B Marketing Exchange, smaller demand-gen-focused gatherings. Sponsorship + speaking are both valid.
- **Peer communities** — Pavilion (formerly Revenue Collective), Wynter, smaller VP-Marketing Slack groups. Word-of-mouth from peers is the strongest acquisition signal.
- **NOT events:** late-funnel paid retargeting works (LinkedIn ABM ads); top-of-funnel Google search rarely does (they don't search for solutions, peers point them at vendors).

## Customer proof points

(Empty in V1 example seed. As you onboard real customers and get permission to name them, this section grows: customer name, ARR tier, use case, time-to-value, headline outcome. Feeds the case-study skills + sales-deck skill + competitor-battlecard skill.)

## Voice of customer (VoC)

(Empty in V1 example seed. As you run win/loss-analysis on real call transcripts, this section grows: verbatim quotes by theme, organized by champion-persona JTBD, with attribution to source call. Feeds positioning refresh + messaging library + cold-email opener generation.)

---

## How this file gets used

Every downstream skill reads this when it needs to know "who is the audience?":
- `/positioning` synthesizes positioning from ICP + competitor aggregate
- `/product-messaging` reads pain priority order to construct value props in priority order
- Future content skills (LinkedIn-post, blog-draft) read this for audience targeting
- Future outbound skills (cold-email opener, ABM brief) read pain points + job-context triggers

**Editing this file changes the audience targeting across every downstream output.** Single source, propagates everywhere.

## Refresh cadence

Quarterly refresh recommended. Trigger conditions to refresh sooner:
- Major shift in win/loss patterns
- New segment entered (vertical, geography, company-size tier)
- Major change in champion-persona vocabulary (e.g., "AI-native marketer" becomes a real persona shift, not just hype)

Last refreshed: 2026-05-17 (V1 example seed)
Owner: VP Marketing
