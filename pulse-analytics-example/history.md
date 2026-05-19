# history.md — long-term operations log

Append-only record of significant events in the marketing OS. Quarterly prunings, major refreshes, agent decisions, ownership transfers, system-wide changes.

This file grows over months and years. Each entry is short — one-line for routine events, a paragraph for significant ones.

## What goes here

- Quarterly pruning ritual outputs (per `.claude/rules/maintenance.md`)
- Major refreshes of canonical files (positioning, ICP, brand voice)
- Ownership transfers (when {X} hands a skill / agent / file to {Y})
- New MCP additions or removals
- Agent fires worth flagging (especially first runs + escalations)
- System-wide changes (folder restructure, new convention adoption, etc.)

## What does NOT go here

- Routine skill invocations (those are noise at this granularity)
- Draft work or in-progress edits (those live in working files)
- Recent activity summaries (those go in [`latest.md`](./latest.md))

## Format

Newest entries at the top. Append-only — never edit or delete prior entries; if a prior entry was wrong, append a correction.

```
## 2026-{MM}-{DD} — {event title}

{event description, 1-3 lines}

Owner: {who logged this}

---
```

## Why append-only

The point of `history.md` is auditability over time. If anyone (you in 6 months, a new teammate, a quarterly review) wants to understand how the system got to its current state, this file is the answer. Editing past entries breaks that audit trail. If a past entry was wrong, append a correction with a date, don't rewrite.

## Owner

Default: whoever owns the repo overall. In practice anyone with write access can append.

## Last refreshed

2026-05-17 (V1 seed — empty body; fills as events happen)
