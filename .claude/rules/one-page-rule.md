# Rule — one-page CLAUDE.md

Every `CLAUDE.md` in this repo stays **one page**. Pointers to other files, not content. Folder-local CLAUDE.mds carry the navigation detail for each folder.

## Why

Two failure modes if any CLAUDE.md grows past a page:

1. **Scan friction.** A new teammate cloning the repo should be able to read it in 60 seconds and know where everything lives. If it's 3 pages, they don't read it — they ask in Slack instead. The file then becomes documentation no one references.

2. **Drift gravity.** Long CLAUDE.mds absorb content that doesn't belong. Someone adds a paragraph about positioning; later someone else adds a Slack channel list; later again someone duplicates folder navigation that exists elsewhere. Two months later the file has 800 lines of half-current information that contradicts the source-of-truth files.

The one-page rule prevents both.

## What "one page" means in practice

- Under ~80 lines of markdown when rendered on a 1080p screen
- Sections allowed: a one-line purpose statement, folder pointers, reading order, key resources, owner
- Sections NOT allowed: detailed positioning, detailed ICP, voice rules, skill catalogs, agent catalogs, MCP details. All of those go in their source files (e.g., `marketing/icp/ICP.md`, `marketing/positioning/positioning.md`, `.claude/skills/{name}/SKILL.md`).

If any CLAUDE.md creeps past 100 lines, that's the signal to extract content to the source file it's about and replace it with a one-line pointer.

## How to check

```bash
wc -l CLAUDE.md
find . -name "CLAUDE.md" -exec wc -l {} +
```

If any line count is over 80, look for content to move to a source file and leave a pointer.

## Owner

Whoever owns the repo overall.

## Refresh cadence

Each quarterly review (see [`quarterly-maintenance.md`](./quarterly-maintenance.md)) flags any creep.
