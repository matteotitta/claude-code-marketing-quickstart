# PulseAnalytics — brand voice rules (canonical, locked example)

> **Note on this file:** PulseAnalytics is a fictional B2B SaaS analytics platform used as the running example throughout this quickstart. The 5 voice rules below are illustrative — they're a real set of operator-shaped rules a B2B SaaS marketing team might enforce, but the specific blocklists and patterns are tuned for the example. **Replace this file with your own company\'s voice rules.** Keep the structure (5 rules, each with violation pattern + fix template); replace the content.

Every content / paid / outbound / lifecycle execution skill reads this file and applies the rules when producing output. The custom gate skill you author when you populate your workspace will check drafts against these rules pre-publish. Changing this file changes what every downstream skill produces.

---

## Rule 1 — Sentence-case headings

**The rule:** all headings use sentence case. First word capitalized, plus proper nouns. No Title Case anywhere — not in H1, H2, H3, blog titles, slide titles, email subject lines, or LinkedIn post hooks.

**Why:** sentence case reads as human, not corporate. Title Case is the default AI/marketing-template output; Title Case in 2026 reads as "this was probably written by ChatGPT in a hurry."

**Violation pattern:** any heading where every word is capitalized (e.g., "How To Use Analytics For Pipeline Growth").

**Fix template:** rewrite to sentence case. "How to use analytics for pipeline growth."

**Exception:** product names (PulseAnalytics), proper nouns (Salesforce, North Star Goal, B2B SaaS), and acronyms (ARR, ICP, CRM, QBR) keep their original casing.

---

## Rule 2 — No buzzword blocklist

**The rule:** the following words and phrases are banned in customer-facing content. Replace each with a concrete verb or specific noun.

**Blocklist (alphabetical):**
- best-in-class
- empower / empowerment
- end-to-end
- holistic / holistically
- innovative / innovation (as a generic claim)
- leverage (as a verb meaning "use")
- next-generation
- paradigm / paradigm shift
- revolutionize
- robust (as a generic positive adjective)
- scalable (when not making a specific scaling claim)
- seamless / seamlessly
- solutions (as a noun replacement for "product")
- synergy / synergistic
- unlock (as a verb meaning "enable")
- world-class

**Why:** every word on this list signals AI-generated copy or 2010s-era B2B marketing template. Buyers in 2026 read these as filler and tune out.

**Violation pattern:** any banned word in body copy, headlines, captions, or CTAs.

**Fix template:** replace each banned word with the concrete verb or specific noun it was hiding. "Leverage analytics" → "use analytics." "Best-in-class platform" → name the specific differentiator. "Empower marketers" → "give marketers". "Solutions" → "product" / "tools" / the specific thing.

**Exception:** if a banned word appears in a direct quote from a customer or external source, keep it (don't edit other people's words).

---

## Rule 3 — Em-dash convention with spaces

**The rule:** when using em-dashes, always include spaces around them (`text — text`). Never use no-space em-dashes (`text—text`). Use em-dashes sparingly — when a comma or period would underserve the rhythm.

**Why:** spaces around em-dashes read more naturally in flowing prose. No-space em-dashes are an AI/typographer convention that reads as overly-stylized in 2026 marketing copy.

**Violation pattern:** any em-dash without surrounding spaces (e.g., "PulseAnalytics—the marketing analytics platform—gives you...").

**Fix template:** add spaces. "PulseAnalytics — the marketing analytics platform — gives you..."

**Additional sub-rule:** in any single piece of content (post, blog, email), use em-dashes at most 3 times. More than that signals AI output or a writer leaning on the dash to avoid restructuring sentences.

---

## Rule 4 — Source-citation required for numeric claims

**The rule:** any numeric claim in customer-facing content must include a citation, source, or qualifying scope. "Faster," "more accurate," "saves time" — fine without citation. "10x faster," "47% more accurate," "saves 6 hours a week" — must cite source or scope.

**Why:** unsourced numerics are the most common credibility leak in B2B SaaS marketing. Buyers in 2026 know which claims came from product-marketing templates and which came from real measurement.

**Violation pattern:** any number (percentage, multiplier, absolute count, dollar figure, time savings) without a citation, customer name, or qualifying scope.

**Fix template (3 options, in order of preference):**
1. **Cite the source:** "10x faster on the queries we benchmarked vs. Mixpanel [link to benchmark]"
2. **Qualify the scope:** "10x faster on the specific attribution queries our customers ran most often"
3. **Soften the claim:** "Faster than the legacy tools we benchmarked against"

If none of the three work for a specific claim, omit the number entirely. Vague claims are weaker than no claim; uncited specific claims are worst of all.

**Exception:** internal benchmarks where the audience is the source (e.g., "your team saves 4 hours a week" in a product UI showing per-account savings).

---

## Rule 5 — No invented metrics

**The rule:** if the data isn't available, write "not available" or omit the claim entirely. Never round up a plausible number. Never write "trusted by 1,000+ teams" if the real number is 78. Never write "industry-standard 95% retention" if you haven't measured your retention.

**Why:** invented metrics are the #1 trust killer in B2B SaaS. Buyers will check; competitors will surface the gap; customer-success teams will inherit the mismatched expectations. The honesty premium in 2026 is real.

**Violation pattern:** any number or claim that the author can't trace to a specific measurement, customer count, or external source.

**Fix template:**
- **If you have the data but it's small:** state the real number. "Trusted by 12 customers including [3 names]" lands stronger than invented thousands.
- **If you don't have the data:** write "data not available in this piece" or omit the claim. Replace with qualitative description ("teams using us at the growth stage" vs. fake-precise "1,000+ teams").
- **If you're tempted to estimate:** ask whether the estimate is defensible if challenged. If not, don't ship the claim.

**Sister principle:** "approximately" / "around" / "looks like" / "in the ballpark of" before a number are anti-signals. They typically mean "I'm rounding without measuring." Either commit to the real number or commit to the qualitative description.

---

## Reading these rules together

The 5 rules cluster into two themes:

- **Rules 1, 2, 3** are about **prose hygiene** — the surface-level signals that a human wrote this for humans, not an AI for keywords. Cheap to enforce, high signal for buyers.
- **Rules 4, 5** are about **claim integrity** — the trust foundation under the prose. Harder to enforce (requires the writer to know what's measured vs. what's plausible), but a single violation can break a buyer's confidence in everything else.

Any gate skill (the custom one you author in this repo) should check all 5 sequentially. A draft that fails Rule 4 or 5 should not ship even if Rules 1-3 pass. A draft that violates 2+ rules is a FAIL regardless of which rules.

## Last refreshed

2026-05-17 (V1 example seed)
Owner: VP Marketing
Refresh trigger: any time the team identifies a new buzzword pattern in customer-facing content, or any time a customer flags a specific phrasing as off-brand.
