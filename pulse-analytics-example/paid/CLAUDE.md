# marketing/paid/ — paid workstream

Ad copy, creative briefs, paid campaign strategy. The execution workstream that reads from `marketing/messaging/` (status-quo alternatives + key differentiators) and writes paid creative.

## Sub-pattern

| Subfolder | Holds | When you fill it |
|---|---|---|
| [`research/`](./research/) | Competitor ad scans, channel-mix research, audience analysis | Before launching a campaign |
| [`strategy/`](./strategy/) | Paid strategy doc, budget allocation, campaign plan | Quarterly planning |
| [`execution/`](./execution/) | Ad copy variants, creative briefs, campaign performance logs | Per campaign |

## Empty in V1

All three subfolders ship with `.gitkeep`. They fill as you launch paid campaigns.

## What upstream context this workstream reads

- `marketing/messaging/messaging.md` — pulls headlines + CTAs + value props
- `marketing/positioning/positioning.md` — pulls key differentiators + status quo alternatives
- `marketing/icp/ICP.md` — pulls audience targeting + pain points
- `marketing/brand/brand-kit.md` — pulls visual identity tokens for creative briefs

## What integrations route the output

- Meta Ads CLI / Meta Business Manager
- LinkedIn Ads
- Google Ads

## Owner

Demand Gen lead or VP Marketing.
