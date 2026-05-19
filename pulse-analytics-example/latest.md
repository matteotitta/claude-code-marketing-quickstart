# latest.md — working memory

This file is the delta cache for your marketing OS. Recent changes, drift reports, what's new since last cycle.

The visibility skill you author when you populate your workspace (e.g., a `weekly-context-refresh` skill that walks `marketing/` and surfaces stale files) writes here weekly. You also write here manually after any significant action (a refresh, a major positioning edit, a new MCP wired, an agent fired in production for the first time).

## What goes here

- Drift reports from your visibility skill (most recent at top)
- Manual delta entries: short notes on significant changes since last entry
- Recent metric movements worth surfacing
- One-week-look-back style summaries

## What does NOT go here

- Permanent canonical content (that's in `positioning.md`, `ICP.md`, etc.)
- Detailed historical records (that's in [`history.md`](./history.md))
- Skill output you'll ship externally (that's in `projects/`)

## Format

Newest entries at the top. Date-stamped. Short.

```
## 2026-{MM}-{DD} — {one-line title}

{2-5 lines of substance}

---
```

## How this file gets used

- Agents read this to see what's shifted recently when deciding actions
- Quarterly pruning ritual reads this to understand "what's been happening" before deciding what to archive
- Onboarding a new teammate reads this to catch up on recent system state

Empty by default — populate naturally over time as you produce content.

## Owner

Default: VP Marketing or whoever owns the marketing OS overall.

## Last refreshed

2026-05-18 (V2 seed — empty body; fills naturally)
