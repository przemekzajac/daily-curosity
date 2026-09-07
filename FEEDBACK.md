# Feedback loop

After the curiosity, this line, verbatim:

> Hit or miss? (1–5, or just tell me what was off)

Then the Capital Quiz question per `QUIZ.md`, then **stop and wait**. Do not fill
the silence with more facts.

His reply will often answer both at once — "4, and Vaduz". Handle both: mark the
quiz, record the rating. If he answers only one, process that one and say nothing
about the other.

## When he replies

1. Interpret the reply generously. "meh" is a 2. "ha, good one" is a 4. "already
   knew it" is a 1 *on the novelty axis*, not necessarily on the topic.
2. Update that day's entry in `log/sent.md` — fill in the `rating` and `note`.
3. Update `TASTE.md`: adjust the standing preferences. Be conservative — one data
   point is a nudge, not a rule. Only promote something to a hard rule after the
   same signal shows up two or three times.
4. Commit and push both files to `claude/daily-curiosity-agent-u8hjuo`.
5. Reply with one short line acknowledging what you learned. Do not write an essay
   about your updated model of his preferences.

## If he doesn't reply

Leave the entry unrated. Silence is not a signal — don't infer dislike from it.

## What to actually learn

Track these axes separately, because they fail differently:

- **Topic** — which of the four flavours land hardest?
- **Novelty** — was it too well-known? This is the most common failure mode.
- **Depth** — too shallow to be interesting, or too much backstory?
- **Retellability** — could he actually say this to a friend, or is it only
  interesting on the page? This is the real target.

A 5 tells you less than a 2 does. Mine the low scores hardest.
