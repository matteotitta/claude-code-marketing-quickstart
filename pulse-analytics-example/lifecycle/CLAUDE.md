# marketing/lifecycle/ — lifecycle + retention workstream

Onboarding nurtures, activation sequences, retention flows, expansion campaigns. The execution workstream that reads from `marketing/icp/` (champion JTBD) + `marketing/messaging/` (proof points + value props in priority order) and writes lifecycle communications.

## Sub-pattern

| Subfolder | Holds | When you fill it |
|---|---|---|
| [`research/`](./research/) | Cohort analysis, churn-cause patterns, activation funnel audit | Before designing a new flow |
| [`strategy/`](./strategy/) | Lifecycle strategy, segment map, trigger event design | Per major lifecycle moment |
| [`execution/`](./execution/) | Onboarding emails, retention campaigns, expansion sequences | Continuous |

## Empty in V1

All three subfolders ship with `.gitkeep`.

## What upstream context this workstream reads

- `marketing/icp/ICP.md` — pulls champion JTBD + decision criteria
- `marketing/messaging/messaging.md` — pulls value props in priority order + proof points
- `marketing/brand/brand-voice.md` — applies voice rules to lifecycle copy

## What integrations route the output

- Klaviyo (B2C-flavored lifecycle)
- Customer.io / Braze (B2B SaaS lifecycle)
- HubSpot / Pardot (marketing automation)

## Owner

Lifecycle Marketing Manager or VP Marketing.
