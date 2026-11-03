# Brand voice skill

A template for turning a brand book into an AI writing skill that produces on-brand copy, not just plausible copy.

It's a blank template: fill in the brackets with your own brand's principles, rules and examples. It covers blogs, social, PR pitches, emails, agency briefs and web pages.

## What's in here

- [`SKILL.md`](SKILL.md) - the skill itself. Fill in the `[brackets]`.
- [`checklist.md`](checklist.md) - the final review every draft goes through before it's delivered. This is where most of the quality comes from.

## How to set it up

1. **Write three principles, not ten.** Each one should be a tension the writer has to balance, with a bad and a better example. A principle that's just an adjective ("friendly") won't change anything.
2. **Pick two reference writers.** It gives the model, and your team, a register to aim for that's more specific than "warm but professional". Use them for calibration only, never quote them in published copy.
3. **List your banned words with swaps.** A ban without a replacement just produces a different cliché.
4. **Add format notes for each channel.** Word counts, where the brand name goes, what a headline looks like.
5. **Make your own writing outrank the rules.** If you paste an example of copy you love, the skill matches it over anything in the reference files.

## Using it with Claude

Save the folder as a skill (Settings, then Capabilities, then Skills in the Claude app, or `~/.claude/skills/` in Claude Code). It loads when you ask for copy for your brand. Without Claude, paste `SKILL.md` and `checklist.md` into the start of a chat as a brief.
