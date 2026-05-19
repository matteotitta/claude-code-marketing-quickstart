# marketing/content/ — content workstream

LinkedIn posts, blog drafts, newsletter issues, AEO articles. The execution workstream that reads from `marketing/messaging/` + `marketing/icp/` and writes shipped content.

## Sub-pattern

Three subfolders, each holds a different phase:

| Subfolder | Holds | When you fill it |
|---|---|---|
| [`research/`](./research/) | Content audits, gap analysis, competitor content scans | Before planning a new content cycle |
| [`strategy/`](./strategy/) | Content strategy doc, editorial calendar, channel plan | Quarterly planning |
| [`execution/`](./execution/) | Shipped posts, drafts, published artifacts | Continuous |

## Empty in V1

All three subfolders ship with `.gitkeep` placeholders. They fill as you produce content. Your first shipped piece lands in `execution/`.

## What upstream context this workstream reads

- `marketing/messaging/messaging.md` — pulls hooks + value props + CTAs
- `marketing/icp/ICP.md` — pulls champion JTBD + voice triggers
- `marketing/brand/brand-voice.md` — applies voice rules
- `marketing/positioning/positioning.md` — pulls anchor + status quo alternatives

## What integrations route the output

- Substack / Beehiiv (newsletter)
- LinkedIn / Buffer / Hypefury (social)
- Ghost / WordPress / Framer (blog)

## Owner

Content lead or VP Marketing.
