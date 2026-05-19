# marketing/rules/ — gate + escalation rules

Cross-cutting rules that downstream agents + custom gate skills enforce. **Voice rules live in [`marketing/brand/brand-voice.md`](../brand/brand-voice.md)** (per the Genesys convention — voice is a brand artifact, not a separate "rules" concern).

## What's in here

| File | Purpose | Read by | Status |
|---|---|---|---|
| [`gate-rules.md`](./gate-rules.md) | Rules extracted from the Manager Prompt — what to always check, red flags, missing context, positive/negative recent examples. | Future agents + custom gate skills you write | Empty — fill in this repo |
| [`escalation.md`](./escalation.md) | When the orchestration layer should pause for human review vs. ship autonomously. | Future agents in this repo | Empty — fill in this repo |

## How to add a new rule file

When you find a pattern worth enforcing that doesn't fit `gate-rules` / `escalation` / `brand-voice`, add a new file:

1. Decide if it's a **cross-cutting rule** (here) or a **brand artifact** (`marketing/brand/`)
2. Create `marketing/rules/{rule-name}.md` (or `marketing/brand/{rule-name}.md` for voice/visual rules)
3. Add a row to the table above (or to `marketing/brand/CLAUDE.md`)
4. Write or update the agent / skill that reads it

## Owner

Each rule file has its own owner named at the bottom of the file. Default: the Manager whose judgment was extracted (gate-rules) or the agent owner (escalation).

## Refresh cadence

- **As-needed** for `gate-rules.md` (when the Manager Prompt is re-run, typically once per year per manager)
- **As-needed** for `escalation.md` (when the orchestration layer creates an incident that suggests a rule change)
