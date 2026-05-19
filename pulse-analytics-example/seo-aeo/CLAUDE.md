# marketing/seo-aeo/ — search + answer-engine workstream

Programmatic SEO templates, AEO-optimized articles, schema markup, citation strategy. The execution workstream that reads from `marketing/positioning/` + `marketing/competitors/` and writes search-visible content.

## Sub-pattern

| Subfolder | Holds | When you fill it |
|---|---|---|
| [`research/`](./research/) | Keyword research, citation gap analysis, competitor SEO audits | Before content production |
| [`strategy/`](./strategy/) | AEO strategy, pSEO template plan, query cluster map | Quarterly planning |
| [`execution/`](./execution/) | Published articles, pSEO pages, schema files | Continuous |

## Empty in V1

All three subfolders ship with `.gitkeep`.

## What upstream context this workstream reads

- `marketing/positioning/positioning.md` — pulls the wedge for comparison pages
- `marketing/competitors/aggregate.md` (when canonical exists) — pulls incumbent gaps
- `marketing/icp/ICP.md` — pulls audience targeting + JTBD-shaped queries
- `marketing/messaging/messaging.md` — pulls headlines + meta-description content

## What integrations route the output

- Framer / Webflow (publish destination)
- GSC MCP (measurement)
- Schema.org markup (structured data)

## Owner

SEO lead or Content lead.
