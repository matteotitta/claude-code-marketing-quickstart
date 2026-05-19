# Sustainability rules

The marketing OS only compounds if someone maintains it. These three rules are the discipline that keeps it alive — adapted from Carl Vellotti's "Team OS" article (see [README.md](../../README.md) "Inspirations").

---

## Rule 1 — Every artifact has a named owner

Not a team. A person. Skills, agents, MCP connections, context files, voice rules — each has one human who's accountable for whether it still works, still gets used, still matches reality.

### Ownership table

| Artifact | Owner | Notes |
|---|---|---|
| `marketing/positioning/positioning.md` | {Name} | |
| `marketing/icp/ICP.md` | {Name} | |
| `marketing/competitors/aggregate.md` | {Name} | Canonical; per-competitor files have their own owners |
| `marketing/brand/brand-kit.md` | {Name} | |
| `marketing/brand/brand-voice.md` | {Name} | |
| `marketing/messaging/messaging.md` | {Name} | |
| `marketing/rules/gate-rules.md` | {Name} | |
| `marketing/rules/escalation.md` | {Name} | |
| `marketing/goals/` (KPIs + measurement) | {Name} | |
| `.claude/skills/competitor-research/` | {Name} | Pre-seeded |
| `.claude/skills/competitor-aggregate/` | {Name} | Pre-seeded |
| `.claude/skills/icp-research/` | {Name} | Pre-seeded |
| `.claude/skills/positioning/` | {Name} | Pre-seeded |
| `.claude/skills/product-messaging/` | {Name} | Pre-seeded |
| `.claude/skills/tov-guidelines/` | {Name} | Pre-seeded |
| `.claude/skills/brand-kit/` | {Name} | Pre-seeded |
| `.claude/skills/{your skill}/` | {Name} | (populated in this repo + onward) |
| `.claude/agents/{your agent}/` | {Name} | (populated in this repo) |
| `.mcp.json` + `.claude/connections.md` | {Name} | Integrations layer overall |
| The repo overall + root CLAUDE.md | {Name} | |

Edit this table in this repo with real names. Update it whenever ownership transfers (someone leaves, someone takes over a domain).

---

## Rule 2 — Coach contributors, don't gatekeep

When someone submits a skill with an API key hardcoded, a SKILL.md without frontmatter, a context file that violates the voice rules, or a folder structure that breaks the one-page-rule discipline — don't reject and move on. Help them clean it up.

Two reasons:

1. **The first time someone contributes to a shared repo is high-stakes for them.** Reject without help and they don't try again. The repo becomes one person's project, not the team's.
2. **The teaching moment compounds.** Coaching one person on "here's how SKILL.md frontmatter works" means the next 5 SKILL.md files from that person are correctly shaped. Rejecting just produces a corrected file once; coaching produces a corrected contributor forever.

What this looks like in practice:

- Pair on the fix when possible (15 minutes, screenshare or async with comments)
- Leave specific feedback in the PR / commit comments — not just "this is wrong," but "here's the convention + here's the example to follow"
- Update the relevant CLAUDE.md or rule file if the contributor's mistake suggests the doc was unclear
- Reserve actual rejection for cases where the contributor has refused coaching multiple times, or the work fundamentally doesn't fit the repo's purpose

---

## Rule 3 — Quarterly 30-minute pruning ritual

Once a quarter (calendar it now), spend 30 minutes auditing the repo:

### What to check per artifact

- **Still used?** Has this skill / agent / MCP / rule file been invoked or referenced in the last 90 days?
- **Still has an owner?** Is the named owner still on the team + still owns this artifact?
- **Still works?** Does it run cleanly when invoked, or does it error / produce stale output?

### What to do

- **Yes to all 3** → leave it. Healthy artifact.
- **No to "still used"** → consider archiving (move to `archive/` folder or delete with a one-line history.md entry explaining why)
- **No to "still has an owner"** → assign a new owner OR archive
- **No to "still works"** → fix or archive; don't leave broken artifacts in the active set

### Output of each pruning ritual

A short markdown entry appended to `marketing/history.md`:

```
## Quarterly pruning — 2026-{MM}-{DD}

Archived (no longer used):
- {artifact} — reason
- {artifact} — reason

Re-owned (owner change):
- {artifact} — {old owner} → {new owner}

Fixed (broken, repaired):
- {artifact} — what was broken + the fix

Reviewed + kept as-is: {count}
```

Calendar the next pruning ritual 90 days out before you close the laptop.

---

## Why these three rules together

Each rule prevents one of three failure modes:

- **Rule 1 (named owner)** prevents the "orphan" failure mode — artifacts that no one updates because no one specifically signed up to update them
- **Rule 2 (coach, don't gatekeep)** prevents the "one person's project" failure mode — the repo becomes high-friction for newcomers, contributions dry up, the repo decays
- **Rule 3 (quarterly pruning)** prevents the "calcification" failure mode — old artifacts accumulate, become harder to distinguish from current ones, the repo loses signal

Skip any one rule and the marketing OS still works for a few months. Skip all three and it doesn't survive year one. The discipline isn't optional.

## Last refreshed

V2 template — populated 2026-05-18 (course Week 4.5 will fill in real names + cadence).

## Where this discipline came from

The three rules + the quarterly pruning ritual are adapted from Carl Vellotti's "Team OS" article ([`org-os-starter`](https://github.com/carlvellotti/org-os-starter) and `faculty-products-org-os`). Re-implemented for the marketing OS context per the cite-and-defer license posture (Vellotti's repos lack LICENSE files). See [README.md](../../README.md) "Inspirations" section.
