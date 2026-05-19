---
version: alpha
name: PulseAnalytics
description: Marketing analytics platform — calm, operator-flavored, designed for the marketer not the analyst

colors:
  primary: "#0B2A4A"        # Deep navy — confidence + clarity
  secondary: "#3B7DD8"      # Mid-blue — trust + action
  tertiary: "#F0A347"       # Warm amber — accent + CTA highlight
  neutral: "#F7F8FA"        # Off-white surface
  surface: "#FFFFFF"
  on-surface: "#1A1C1E"     # Near-black body text
  muted: "#6C7278"          # Secondary text
  error: "#C62828"

typography:
  display-lg:
    fontFamily: "Inter"
    fontSize: 72px
    fontWeight: 700
    lineHeight: 1.05
    letterSpacing: -0.03em
  headline-lg:
    fontFamily: "Inter"
    fontSize: 32px
    fontWeight: 600
    lineHeight: 1.15
  body-md:
    fontFamily: "Inter"
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.6
  label-sm:
    fontFamily: "Inter"
    fontSize: 12px
    fontWeight: 600
    lineHeight: 1
    letterSpacing: 0.05em

rounded:
  sm: 4px
  md: 8px
  lg: 12px
  full: 9999px

spacing:
  base: 8px

components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.surface}"
    rounded: "{rounded.md}"
    padding: 12px 24px
  card:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.lg}"
    padding: 32px
---

# PulseAnalytics — brand kit (canonical, example)

> **Note on this file:** PulseAnalytics is the fictional B2B SaaS analytics platform used throughout this quickstart. The brand kit above is illustrative — operator-flavored, generic enough to swap for any B2B SaaS, specific enough to feel real. **Once you have your own data you Replace this with your own brand kit (extract via `/brand-kit` from your real product screenshots or website). Keep the YAML token structure; replace the values.

---

## Overview — what this brand expresses

PulseAnalytics's brand reads as **calm + operator-flavored**. Not consumer-app playful. Not enterprise-stiff. Designed for the marketer staring at a pipeline review at 9pm Sunday, not the analyst reading dashboards from 9-to-5.

The visual identity supports the messaging: deep navy as the anchor color signals confidence + clarity; mid-blue carries trust + action (CTA primary); warm amber breaks the cool palette where the brand needs a moment of energy (CTA accent, signal lights, key metric callouts).

## Colors

- **Primary navy (`#0B2A4A`).** Headers, primary buttons, brand-defining surfaces. Used once per screen.
- **Secondary blue (`#3B7DD8`).** Secondary CTAs, links, info-state UI.
- **Tertiary amber (`#F0A347`).** Highlights, accent on key metrics, "look here" moments. ≤10% coverage per screen.
- **Neutral off-white + pure white.** Body surfaces. The dominant visual mass.
- **Muted gray (`#6C7278`).** Secondary text, meta information.
- **Error red (`#C62828`).** Reserved for actual errors. Not for emphasis.

## Typography

Inter for everything. Two weights per screen maximum (400 + 600 for most contexts; 700 only for the largest display sizes). Sentence case across all headings, body, captions.

## Layout

8-pt spacing base. Generous whitespace — the brand says "calm + premium," so density follows. Section spacing 64-96px on desktop, 32-48px on mobile.

## Shapes

8px default radius. Square corners forbidden (signals brutalist; not the PulseAnalytics voice). Pill (`9999px`) reserved for tags/badges only.

## Components

- **Button primary** — navy bg, white text, 8px radius, 12px × 24px padding
- **Card** — white surface, 12px radius, 32px padding, no border, subtle shadow OK
- **Input** — neutral bg, 8px radius, 16px padding

## Do's and Don'ts

**Do:**
- One primary button per screen
- Two font weights max per screen
- Amber for emphasis only, ≤10% coverage
- Generous spacing — let layouts breathe

**Don't:**
- Mix rounded and sharp corners in the same view
- Use gradients on text (the universal AI-template tell)
- Stack three nested cards (cardocalypse)
- Center body prose (centered text is for headlines only)

---

## How this file gets used

Every downstream visual skill reads this file when producing a designed artifact:

- `/landing-page-wireframe` consumes the YAML tokens for layout spec
- `/landing-page-copy` consumes the voice rules (in `brand-voice.md`) + visual tokens
- `/ad-creative-brief` cites these exact hex codes + typography in designer briefs
- Any future content skill that produces visual output reads here

The YAML tokens are **machine-authoritative**. The prose explains why; the tokens are what gets rendered. When prose and tokens conflict, tokens win.

## Refresh cadence

Quarterly. Trigger sooner if visual identity refreshes or a major brand update lands.

Last refreshed: 2026-05-18 (V2 example seed)
Owner: VP Marketing or Brand Lead
