# .claude/ — Claude Code runtime directory

Everything Claude Code needs to run sits here: skills, agents, hooks, rules, configuration. Three of the four systems in this repo's framework (action / orchestration / integrations) have their definitions in this folder.

## What's in here

| Path | Purpose |
|---|---|
| [`skills/`](./skills/) | The 8 pre-seeded research skills (`brand-kit`, `competitor-aggregate`, `competitor-research`, `funnel-strategy`, `icp-research`, `positioning`, `product-messaging`, `tov-guidelines`) — the producers (system of action) |
| [`agents/`](./agents/) | Ready for your custom agents — the coordinators (system of orchestration) |
| [`hooks/`](./hooks/) | Ready for your custom hooks — also part of orchestration |
| [`rules/`](./rules/) | Repo-level discipline: [`one-page-rule.md`](./rules/one-page-rule.md) (every CLAUDE.md stays one page) + [`quarterly-maintenance.md`](./rules/quarterly-maintenance.md) (90-day review ritual) |
| [`connections.md`](./connections.md) | 12-connector setup guide — pairs with `.mcp.json` at the repo root (system of integrations) |
| `settings.local.json.example` | Claude Code per-machine settings template — copy to `settings.local.json` (gitignored) for machine-specific config |

## How `.claude/` relates to the 4 systems

| System | Where it lives |
|---|---|
| **1. Context** | `marketing/` (at root — your data) + `pulse-analytics-example/` (the example) |
| **2. Action** | `.claude/skills/` |
| **3. Orchestration** | `.claude/agents/` + `.claude/hooks/` |
| **4. Integrations** | `.claude/connections.md` (the setup guide) + root-level `.mcp.json` + `env` (the wiring, root by tooling requirement) |

## Owner

Default: whoever owns the repo overall (named in the root [`README.md`](../README.md)).
