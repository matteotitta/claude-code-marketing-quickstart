---
name: competitor-research
version: '1.0'
last_updated: 2026-05-19
author: genesys-growth
description: Run deep research on a single competitor. Produces a dossier with executive summary, position + messaging, status-quo alternatives, key differentiators, pricing position, where-they-win / where-they-lose, threat assessment, and what to watch. Writes to marketing/competitors/MMYY-{competitor-slug}.md. Triggers - "competitor research", "competitive analysis", "research competitor X", "battlecard prep", "analyze [competitor name]"
goal: Produce a deep dossier on a single competitor: positioning, messaging, status-quo, differentiators, pricing, where-they-win/lose, threat assessment.
outcome: marketing/competitors/MMYY-{competitor-slug}.md with executive summary + 11 dimensions of analysis.
primitive: research
ontology_type: competitor-intel
review_gate: 2
inputs:
  required: []
  recommended:
    []
outputs:
  - type: competitor-intel
    feeds_into:
      - positioning
      - product-messaging
      - competitor-aggregate
      - sales-enablement
owned_by_agent: researcher
mcps_used:
  - exa
triggers:
  slash_commands:
    - /competitor-research
status: draft
---

# competitor-research — Stage 1 research skill

The first skill in the article's Example 1 chain. Reads a competitor URL + name, produces a structured dossier, writes the file to `marketing/competitors/MMYY-{slug}.md`. Run once per competitor (3-5 competitors is typical for the first cycle). After all per-competitor files exist, run `/competitor-aggregate` to synthesize the canonical threat matrix.

---

## When to use

- Day 1 of the article's Example 1 ("foundational workflow"): you have a list of 3-5 competitors and need structured intel on each
- Before refreshing `/positioning` — positioning must read from current competitor intel
- Before writing battlecards or comparison pages
- Quarterly refresh of any specific competitor that's made a major move (funding, launch, executive change)

## When NOT to use

- Aggregating across multiple competitors (use `/competitor-aggregate` after this skill produces per-competitor files)
- Building battlecards (use `/sales-enablement` — different shape, sales-team-facing)
- ICP research (use `/icp-research`)
- General company background unrelated to competition (use `/company-context`)

## How it works

1. Inputs: competitor name + competitor URL (required). Optional: industry context, key differentiator hypothesis you want to test.
2. Reads (optional Exa MCP for fresh web data): competitor homepage, pricing page, about page, recent blog posts, recent LinkedIn activity.
3. Produces a 12-section dossier (matching the PulseAnalytics example at `marketing/competitors/0526-competitor-a.md`):
   - Executive summary (3-4 sentences)
   - Anchor + category
   - Position + messaging
   - Status-quo alternatives they position against
   - Key differentiators (claimed)
   - Pricing position
   - Where they win
   - Where they lose (your wedge)
   - Threat assessment (PRIMARY / DIRECT / STEALTH / LOW / DEFUNCT)
   - Win-loss patterns (from your deal history if available)
   - What to watch
   - Refresh cadence + owner
4. Every claim tagged with confidence per `.claude/rules/ontology.md`: `[VERIFIED: source, url, date]`, `[INFERRED: from X + Y]`, `[ESTIMATED: reasoning]`, `[UNAVAILABLE]`.
5. Writes the file to `marketing/competitors/MMYY-{competitor-slug}.md`. MMYY is current month+year (e.g., `0526` for May 2026).

## Invoke

```
/competitor-research Bizible — https://bizible.com
```

Or open-ended:
```
/competitor-research analyze our top competitor — Bizible — and write the dossier
```

## Example output (against the PulseAnalytics example seed)

See [`marketing/competitors/0526-competitor-a.md`](../../../marketing/competitors/0526-competitor-a.md) for a fully-populated example of what this skill produces. Notice:

- Anchor + threat level surfaced in the executive summary
- Claims tagged with confidence levels
- `[UNAVAILABLE]` notation where real data isn't accessible to the skill (e.g., your private win-loss data)
- Refresh cadence + owner at bottom

## Dependencies

- **Reads from:** `marketing/positioning/positioning.md` (optional — gives the skill context on what differentiation matters); `marketing/icp/ICP.md` (optional — informs "where they win vs. lose" framing).
- **Reads via Exa MCP (optional):** competitor's website, recent news, public reviews on G2/Reddit/Trustpilot.
- **Writes to:** `marketing/competitors/MMYY-{slug}.md`

## Customization

Change the dimension count or section structure by editing this SKILL.md body. The 12-section default tracks the Genesys ontology (`.claude/rules/ontology.md` § competitor-intel). Add a custom dimension (e.g., "Open-source posture" if you're in a category where that matters) by appending a new section after section 8.

## Where this fits in the Example 1 chain

```
Day 1-3: /competitor-research × N (this skill) → per-competitor files in marketing/competitors/
Day 4:   /competitor-aggregate → synthesizes per-competitor files into the canonical threat matrix
Day 5:   /icp-research → reads competitor outputs to inform ICP
```

After all 3 competitor files exist, run `/competitor-aggregate` to lock the canonical version.

## Refresh cadence

Per competitor: quarterly minimum. Trigger sooner on funding, launch, or repositioning. Use the `--refresh` flag (when you implement it) to update an existing dossier rather than create a new file.
