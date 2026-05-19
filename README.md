# Claude Code Marketing Quickstart

A fork-and-go starter repo for marketers building an AI-native marketing operating system on Claude Code. Built around the **4-systems framework**: Context · Action · Orchestration · Integrations.

**15 minutes from clone to a working marketing OS** with a populated example you can learn from + an empty workspace ready for your company's data.

Built by [Matteo Tittarelli](https://www.linkedin.com/in/matteotittarelli/) at [Genesys Growth](https://genesysgrowth.com). Questions → DM me on LinkedIn.

---

## What this repo gives you in 60 seconds

- **8 pre-seeded research skills** ready to run: ICP research, competitor research, positioning, messaging, brand kit, voice rules, funnel strategy, competitor aggregate.
- **A fully populated example** (`pulse-analytics-example/`) — a fictional B2B SaaS marketing analytics company called PulseAnalytics. Read it first to see what a working marketing OS looks like.
- **An empty workspace** (`marketing/`) — same structure as the example, ready for your company's data. Each subfolder has a one-line `CLAUDE.md` telling you what goes there + which skill to run.
- **A 12-connector setup guide** ([`.claude/connections.md`](.claude/connections.md)) — covers Exa, Firecrawl, Google Drive, Notion, Slack, Linear, Granola, Gong, Google Search Console, Ahrefs, Framer, Webflow. Split by input/output role with install instructions for Claude Code CLI, Cursor, and claude.ai.
- **A discipline layer** ([`.claude/rules/`](.claude/rules/)) — the "one page per CLAUDE.md" rule and the 90-day maintenance ritual that keep the system from rotting.

---

## Before you clone — 5-minute prerequisite

Handle these once, before the 15-minute tour:

### Required

1. **Claude Code CLI** — [install instructions](https://docs.claude.com/en/docs/claude-code/quickstart). 5 minutes.
2. **Pick your interface** — Claude Code CLI in your terminal works for everything in this repo. If you want a richer editor experience, also install [Cursor](https://cursor.com) (Claude Code integrates as MCP) or the [Claude Desktop app](https://claude.com/download). Free to pick one and stick with it.
3. **An Exa API key** — [exa.ai](https://exa.ai). Free tier covers the quickstart. Exa is the web-search + page-fetch backbone every research skill in this repo uses.

### Optional (wire when you need them)

- Google Search Console (for SEO data — once you start the seo-aeo lane)
- Granola or Gong (for meeting/call transcripts — once you start win-loss work)
- Slack (for team notifications — once you start lifecycle work)

Full setup guide for all 12 connectors lives in [`.claude/connections.md`](.claude/connections.md). Don't try to wire everything on day 1; start with Exa.

---

## The 15-minute tour

### 0:00 → 0:30 — Clone

```bash
gh repo create my-marketing-os --template matteotitta/claude-code-marketing-quickstart --private
cd my-marketing-os
```

Or click "Use this template" on the GitHub repo page.

### 0:30 → 1:30 — Configure Exa

```bash
cp env .env
# Edit .env, add your Exa API key after EXA_API_KEY=
```

The `env` file (committed) is a template. `.env` (gitignored) holds your real keys. Yes, this breaks the conventional `.env.example` pattern — done on purpose so the template file is visible at the top of your file listing instead of hidden as a dotfile.

### 1:30 → 5:00 — Read the example

Open [`pulse-analytics-example/`](./pulse-analytics-example/). Start in this order:

1. [`pulse-analytics-example/CLAUDE.md`](./pulse-analytics-example/CLAUDE.md) — the workspace index
2. [`pulse-analytics-example/positioning/positioning.md`](./pulse-analytics-example/positioning/positioning.md) — see what a populated positioning doc looks like
3. [`pulse-analytics-example/icp/ICP.md`](./pulse-analytics-example/icp/ICP.md) — see what a populated ICP looks like
4. [`pulse-analytics-example/funnel/funnel-strategy.md`](./pulse-analytics-example/funnel/funnel-strategy.md) — GTM motion + funnel stages
5. [`pulse-analytics-example/goals/goals.md`](./pulse-analytics-example/goals/goals.md) — KPI structure

This is the shape your own marketing OS will take.

### 5:00 → 7:00 — Skim the skills

Look at the 8 pre-seeded research skills in [`.claude/skills/`](./.claude/skills/). Each one has a `SKILL.md` with canonical frontmatter + a body that explains when to use it, what it produces, and an example run.

The 8 skills:

- `brand-kit` — extract design tokens + voice rules from a brand
- `competitor-research` — per-competitor 11-dimension analysis
- `competitor-aggregate` — roll N competitor docs into shared insights
- `funnel-strategy` — map GTM motion to funnel stages
- `icp-research` — TAM + champion + economic buyer + anti-ICP
- `positioning` — anchor + differentiators + statement
- `product-messaging` — 10-component messaging library
- `tov-guidelines` — voice rules with violation/fix patterns

### 7:00 → 10:00 — Run your first skill

Open Claude Code in this repo and run:

```
/competitor-research
```

Claude asks for the competitor URL + name. It does the research via Exa, writes the file to `marketing/competitors/MMYY-{competitor-slug}.md`. Repeat for 2–4 competitors, then run `/competitor-aggregate` to synthesize.

### 10:00 → 15:00 — Populate the PMM spine

The recommended order:

1. `/competitor-research` (3–4 competitors) → `/competitor-aggregate` to lock the canonical version
2. `/icp-research` → produces `marketing/icp/ICP.md`
3. `/brand-kit` + `/tov-guidelines` → produces brand kit + voice rules
4. `/positioning` → reads ICP + competitors, produces positioning
5. `/product-messaging` → reads positioning, produces messaging library
6. `/funnel-strategy` → maps your GTM motion to funnel stages

Each skill takes 5–15 minutes. By the end of week 1, your PMM spine is locked.

---

## The 4-systems framework

This repo is built around four systems that compose into a loop:

| System | What it does | Where it lives in this repo |
|---|---|---|
| **1. Context** | What Claude knows about your company | `marketing/` (your data) + `pulse-analytics-example/` (reference) |
| **2. Action** | What Claude does — the producers | `.claude/skills/` (8 pre-seeded research skills) |
| **3. Orchestration** | When + how skills fire | `.claude/agents/` + `.claude/hooks/` (empty by default — you add) |
| **4. Integrations** | What Claude can reach | `.claude/connections.md` (setup guide) + root `.mcp.json` + `env` (wiring) |

**The loop:** integrations feed context → context informs action → orchestration chains action → output becomes new context. Each cycle the system gets sharper.

---

## Repo structure

```
claude-code-marketing-quickstart/
├── README.md                          ← you are here
├── CLAUDE.md                          ← one-line pointer for Claude Code auto-load
│
├── .claude/                           ← Claude Code internals
│   ├── connections.md                 ← 12-connector setup guide
│   ├── skills/                        ← 8 pre-seeded research skills (system of action)
│   ├── agents/                        ← ready for your custom agents (orchestration)
│   ├── hooks/                         ← ready for your custom hooks (orchestration)
│   └── rules/                         ← discipline rules (one-page rule + quarterly maintenance)
│
├── marketing/                         ← YOUR workspace — fill with your company data
├── pulse-analytics-example/           ← REFERENCE — fully populated example, read first
│
├── env                                ← API key template — copy to .env
├── .mcp.json                          ← MCP registry — Exa wired by default
└── .gitignore
```

The `marketing/` and `pulse-analytics-example/` folders mirror each other structurally. The example is populated; yours starts empty with one-line `CLAUDE.md` files pointing back to the example for each subfolder.

---

## How to contribute back

If you adapt this repo and find a pattern that should live in the canonical version — open a PR.

Conventions:

- Keep every `CLAUDE.md` to one page. Pointers, not content. See [`.claude/rules/one-page-rule.md`](./.claude/rules/one-page-rule.md).
- New skills: follow the canonical frontmatter format. See any existing `SKILL.md` in `.claude/skills/`.
- New connectors: add to `.claude/connections.md` in the appropriate I/O section.
- Don't commit secrets. The `.env` file (not `env`) is gitignored by default.

Questions about whether something belongs: DM me on [LinkedIn](https://www.linkedin.com/in/matteotittarelli/).

No formal LICENSE yet — the repo is shared as-is. Reuse the patterns; credit appreciated but not required.

---

## Plan your next 3 skills

Once your PMM spine is populated, you'll feel the friction of the next 3 tasks you do manually that should be skills. Capture them here as you go:

### Skill #1

- **Name:** {your-skill-name}
- **Archetype:** Gate / Query / Visibility (pick one)
- **Problem it solves:** {one sentence — what task does this remove from your weekly groan list?}
- **Target build date:** {date — within 30 days is healthy; 60 days is the ceiling}
- **Reads from:** {which marketing/ files or MCPs?}
- **Writes to:** {what artifact does it produce?}

### Skill #2

- **Name:** {your-skill-name}
- **Archetype:** Gate / Query / Visibility
- **Problem it solves:** {one sentence}
- **Target build date:** {date}
- **Reads from:** {sources}
- **Writes to:** {output}

### Skill #3

- **Name:** {your-skill-name}
- **Archetype:** Gate / Query / Visibility
- **Problem it solves:** {one sentence}
- **Target build date:** {date}
- **Reads from:** {sources}
- **Writes to:** {output}

If you can't name 3 skills within 30 days of running the repo, the system isn't compounding yet. Diagnose: are you using it enough? Are the friction points real or imagined?

---

## Maintenance — keeping this alive

The marketing OS only compounds if someone maintains it. Three rules — adapted from Carl Vellotti's "Team OS" article — codified in [`.claude/rules/quarterly-maintenance.md`](./.claude/rules/quarterly-maintenance.md):

1. **Every artifact has a named owner** (not a team — a person).
2. **Coach contributors, don't gatekeep** — when someone's first contribution is broken, help them fix it, don't reject.
3. **Quarterly 30-minute pruning ritual** — every 90 days, audit: is each artifact still used, still owned, still working? Archive the ones that aren't.

Calendar the next pruning ritual 90 days from your fork date.

---

## Inspirations + attribution

- **Carl Vellotti** — [`org-os-starter`](https://github.com/carlvellotti/org-os-starter) and [`faculty-products-org-os`](https://github.com/carlvellotti/faculty-products-org-os) (fullstackpm.com/orgos). Patterns adopted: one-page CLAUDE.md, folder-local CLAUDE.md as navigation maps, committed `.mcp.json`, repo-as-GitHub-template, README-as-reading-order, the three sustainability rules. Both Vellotti repos lack LICENSE files as of May 2026 — every convention here is re-implemented in our own words; no file content is copied verbatim.
- **Kyle Poyar** — [Growth Unhinged](https://newsletter.growthunhinged.com). The 4-systems framing originated in an article on context engineering for marketing.

---

## Where to go next

- **Stuck on which skill to run first?** Start with `/competitor-research` against your top 3 competitors. Everything else flows from there.
- **Want a richer connector setup?** Open [`.claude/connections.md`](./.claude/connections.md) — install guide for 12 connectors split by I/O role.
- **Curious how the example was built?** Browse [`pulse-analytics-example/`](./pulse-analytics-example/) — every file is a real-shaped artifact a marketing team would produce.
- **Need help or want to share what you built?** [LinkedIn](https://www.linkedin.com/in/matteotittarelli/) or [genesysgrowth.com](https://genesysgrowth.com).
