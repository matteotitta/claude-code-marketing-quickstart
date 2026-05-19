# marketing/ — your workspace

This is **your** marketing operating system. Fill these files with your company's data. The structure mirrors `../pulse-analytics-example/` — read that first to see what populated content looks like, then replace each placeholder file with your own.

## How to populate

1. **Read [`../pulse-analytics-example/`](../pulse-analytics-example/)** end-to-end. It's a fictional B2B SaaS analytics company called PulseAnalytics — generic enough to apply broadly, specific enough to feel real.
2. **Start at PMM core** — populate in this order: `icp/` → `positioning/` → `messaging/` → `competitors/` → `brand/` → `funnel/` → `goals/` → `rules/`. Each one feeds the next.
3. **Then the execution lanes** — `content/`, `lifecycle/`, `outbound/`, `paid/`, `seo-aeo/`. Each lane follows `research/` → `strategy/` → `execution/`. Populate research first, then strategy, then ship execution artifacts.
4. **Run the skills** to produce the content. Each subfolder has a one-line CLAUDE.md naming the skill to run.

## When you're done with the example

Once your `marketing/` is populated and you don't need the reference anymore, delete `../pulse-analytics-example/`. It's a learning aid, not part of your workspace.

## Folder map

**PMM core** (the strategic spine — populate first):
- [`icp/`](./icp/) — who you sell to
- [`positioning/`](./positioning/) — how you're positioned in the market
- [`messaging/`](./messaging/) — how you talk about it
- [`competitors/`](./competitors/) — who you're up against
- [`brand/`](./brand/) — how you look + sound
- [`funnel/`](./funnel/) — your GTM motion
- [`goals/`](./goals/) — your KPIs
- [`rules/`](./rules/) — project guardrails

**Execution lanes** (populate as you ship work):
- [`content/`](./content/) — blog, AEO, social, newsletter
- [`lifecycle/`](./lifecycle/) — email nurture, onboarding, retention
- [`outbound/`](./outbound/) — cold email, ABM, prospecting
- [`paid/`](./paid/) — Google Ads, LinkedIn Ads, paid social
- [`seo-aeo/`](./seo-aeo/) — SEO + AI-engine optimization
