# pulse-analytics-example/ — fully populated workspace index

A reference example. PulseAnalytics is a **fictional** B2B SaaS marketing analytics platform — generic enough to apply broadly, specific enough to feel real. Every file here is the kind of artifact a real marketing team would produce running their PMM spine through Claude Code.

**Use this folder as the blueprint** for populating your own `../marketing/` workspace.

Two layers + operational files:

## Layer 1 — PMM spine (the strategic context)

Each folder holds **per-domain research files** (dated, e.g., `0526-competitor-a.md`) and **one locked canonical version** (the synthesized truth every downstream skill reads).

| Folder | What's in it |
|---|---|
| [`icp/`](./icp/) | `ICP.md` — who PulseAnalytics sells to (champion + economic buyer, pain points, anti-ICP) |
| [`positioning/`](./positioning/) | `positioning.md` — anchor, differentiators, status-quo alternatives |
| [`messaging/`](./messaging/) | `messaging.md` — 10-component messaging library |
| [`competitors/`](./competitors/) | `0526-competitor-a.md` — one competitor analyzed (11 dimensions). Aggregate file appears once 2+ competitors are analyzed |
| [`brand/`](./brand/) | `brand-kit.md` (design tokens) + `brand-voice.md` (5 voice rules) |
| [`funnel/`](./funnel/) | `funnel-strategy.md` — GTM motion + pre/post-close stages |
| [`goals/`](./goals/) | `goals.md` — KPIs, baselines, targets, owners |

**Synthesis order:** icp → competitors → brand → positioning → messaging → funnel. Each downstream skill reads from the locked canonical files. Edit the canonical → every downstream output reflects the change on next run.

## Layer 2 — Execution workstreams (scaffold only)

5 folders, each with the `research/strategy/execution/` sub-pattern:

- [`content/`](./content/) — blog, AEO, social, newsletter
- [`lifecycle/`](./lifecycle/) — email nurture, onboarding, retention
- [`outbound/`](./outbound/) — cold email, ABM, prospecting
- [`paid/`](./paid/) — Google Ads, LinkedIn Ads, paid social
- [`seo-aeo/`](./seo-aeo/) — SEO + AI-engine optimization

These are scaffold-only in the example. Populating execution is the user's work — the PMM spine on top is what they consume.

## Layer 3 — Operational files

- [`latest.md`](./latest.md) — "What's the current state?" 500-word snapshot, refreshed weekly
- [`history.md`](./history.md) — "What happened, and when?" append-only operations log
- [`rules/escalation.md`](./rules/escalation.md) — when Claude asks humans vs ships autonomously
- [`rules/gate-rules.md`](./rules/gate-rules.md) — review gates per output type

## How context flows

1. **Research skills** produce per-domain research files (e.g., `/competitor-research` writes to `competitors/0526-competitor-a.md`)
2. **Synthesis skills** produce locked canonical files (e.g., `/competitor-aggregate` writes the threat-matrix canonical)
3. **Execution skills** read locked canonical files, write to execution workstream folders
4. **Refresh** pulls signals from execution back into research → context refresh → execution refresh

This is the **compounding axis**. Sharp context = sharp output across every skill. Stale context = silently-stale output.

## Reading order for first time

1. Start here (you're reading it)
2. [`positioning/positioning.md`](./positioning/positioning.md) — see what a populated positioning doc looks like
3. [`icp/ICP.md`](./icp/ICP.md) — see what a populated ICP looks like
4. [`funnel/funnel-strategy.md`](./funnel/funnel-strategy.md) — see how the GTM motion maps to funnel stages
5. [`goals/goals.md`](./goals/goals.md) — see KPI definition + measurement structure
6. Browse the 5 execution workstreams — see the `research/strategy/execution/` pattern repeated

## Once you're done with the example

Delete this folder when you no longer need the reference. It's a learning aid, not part of your workspace.

## Owner (in the example)

VP Marketing at PulseAnalytics (fictional). In your own `../marketing/`, name the real owner.
