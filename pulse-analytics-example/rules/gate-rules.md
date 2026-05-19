# Gate rules — extracted from the Manager Prompt

The Manager Prompt is a 5-question interview you run on yourself OR a peer to extract the rules-of-judgment a senior reviewer applies when checking work. The output of that interview goes here.

## The 5 questions (re-stated)

1. What are the 3-5 things you ALWAYS check first when reviewing {a piece of content / a campaign brief / an outbound list / a pricing decision / whatever you're checking}?
2. What red flags make you immediately skeptical?
3. What context do you wish people gave you upfront but rarely do?
4. Tell me about a recent example where someone surprised you positively. What did they do?
5. Tell me about a recent example where someone missed the mark. What was missing?

## The output format

Convert interview answers into rule statements + violation patterns + fix templates, same structure as `brand-voice.md`. Each rule:

```
## Rule {N} — {rule name}

**The rule:** {one-sentence statement}

**Why:** {one-sentence justification — why does this matter?}

**Violation pattern:** {what does breaking this rule look like in practice?}

**Fix template:** {how does the writer fix it?}

**Exception:** {when does this rule not apply?}
```

## How this file gets used

Future agent skills + custom gate skills will read these rules to enforce them automatically. The Manager Prompt extracts senior judgment into machine-checkable rules; this file is where that judgment lives.

Empty in V1. Run the Manager Prompt in this repo to fill it.

## Owner

Default: the senior reviewer whose judgment was extracted (you, or the manager you interviewed).

## Last refreshed

2026-05-17 (V1 seed — empty body)
