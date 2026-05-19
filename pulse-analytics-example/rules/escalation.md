# Escalation rules — when agents pause for human review vs. ship autonomously

When your agents (System of orchestration) start running, every decision they make is one of two flavors:

1. **Autonomous ship.** The agent's output goes live without a human reviewing it first.
2. **Escalate to human.** The agent pauses, surfaces the output for review (Slack, email, Claude Code session), waits for a thumbs-up before proceeding.

This file documents which decisions are autonomous and which escalate. Without explicit rules, agents either over-escalate (waste your time on routine decisions) or under-escalate (ship things you wish they hadn't).

## The structure

Each escalation rule names:

- **The action** the agent might take
- **The decision** — autonomous or escalate
- **The threshold** — what shifts a normally-autonomous action into an escalated one (e.g., "autonomous below $1K spend, escalate above")
- **The route** — if escalating, where does the surface go (Slack channel, email, Claude Code session)
- **The fallback** — what happens if the escalation isn't reviewed within {timeout} (default: hold, don't ship)

## Default V1 rules (empty starter — populate in this repo)

```
## Action: {description}

- **Default decision:** {autonomous / escalate}
- **Escalation threshold:** {condition that flips it}
- **Escalation route:** {Slack channel / email / Claude Code prompt}
- **Timeout fallback:** hold (don't auto-ship)
- **Owner:** {who reviews}
```

Example templates for common cases (populate in this repo):

- LinkedIn post drafted by content agent → escalate (always, in V1)
- Cold email sent by outbound agent → escalate (always, in V1)
- Internal Slack notification (e.g., weekly drift report) → autonomous
- Context refresh skill run → autonomous
- New skill / agent build / config change → escalate (always)
- Anything spending external credits (MCP rate-limited calls, paid API queries) → escalate above defined threshold

## Why this file exists

Two failure modes prevented:

1. **Over-escalation** wastes the human reviewer's time on routine decisions; the team stops paying attention to escalations because most are noise.
2. **Under-escalation** ships bad output without anyone catching it; the team loses trust in the agents and reverts to manual workflows.

The right escalation rules are how agents earn the right to run.

## Refresh cadence

Quarterly. Review which escalations have been over-firing (route changing from escalate → autonomous), which have been under-firing (route changing from autonomous → escalate), which routes are no longer used (delete the rule).

## Owner

Default: the agent owner (whoever wrote the agent the escalation applies to).

## Last refreshed

2026-05-17 (V1 seed — empty body)
