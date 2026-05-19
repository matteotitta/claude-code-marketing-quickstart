# marketing/outbound/ — outbound + ABM workstream

Cold email sequences, ABM plays, account research, outbound campaign strategy. The execution workstream that reads from `marketing/icp/` (VoC + triggers + tier-1 accounts) and writes outbound sequences.

## Sub-pattern

| Subfolder | Holds | When you fill it |
|---|---|---|
| [`research/`](./research/) | Account research, signal-based account lists, win-loss patterns | Before launching a sequence |
| [`strategy/`](./strategy/) | Outbound strategy, ICP tiering, sequence framework | Quarterly planning |
| [`execution/`](./execution/) | Sequences, ABM plays, individual openers | Per campaign |

## Empty in V1

All three subfolders ship with `.gitkeep`.

## What upstream context this workstream reads

- `marketing/icp/ICP.md` — pulls VoC quotes + champion JTBD + job-context triggers
- `marketing/competitors/aggregate.md` (when canonical exists) — pulls named-incumbent vocabulary
- `marketing/messaging/messaging.md` — pulls subject-line variants + opening hooks
- `marketing/positioning/positioning.md` — pulls wedge framing

## What integrations route the output

- Smartlead / Instantly (email sequencing)
- Apollo / Clay (account + contact enrichment)
- HubSpot / Salesforce (CRM write-back)

## Owner

Demand Gen lead or Outbound SDR lead.
