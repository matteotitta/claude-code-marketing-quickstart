# marketing/brand/ — visual identity + voice rules

Holds **brand-kit** (visual identity — colors, typography, components) and **brand-voice rules** (the 5 voice rules `/tov-guidelines` produces).

## What's in here

| File | Status | Produced by |
|---|---|---|
| [`brand-kit.md`](./brand-kit.md) | EXAMPLE — PulseAnalytics visual identity; replace in this repo | `/brand-kit` |
| [`brand-voice.md`](./brand-voice.md) | EXAMPLE — 5 voice rules for PulseAnalytics; replace in this repo | `/tov-guidelines` |

## Why both live here

In the Genesys client convention, tone-of-voice is a brand artifact (not a separate "voice" folder). Visual identity + voice rules are two halves of the same brand expression. Skills consuming brand context read from this one folder.

## What downstream skills read this

- Any content skill — applies voice rules to drafts
- `/landing-page-copy` — applies brand voice + visual identity
- `/linkedin-content` — applies voice rules
- `/ad-creative-brief` — uses brand-kit tokens for designer brief

## Refresh cadence

`/brand-kit` quarterly or when the team refreshes visual identity. `/tov-guidelines` quarterly or when the team finds a new pattern to enforce.

## Owner

VP Marketing or Brand Lead.
