# Daily Curiosity

A scheduled agent that sends Przemek one curiosity every weekday at 09:00
Europe/Warsaw, and learns from whether he liked it.

## How it works

A Routine fires a fresh Claude session each weekday morning. That session:

1. Clones this repo and checks out `claude/daily-curiosity-agent-u8hjuo`.
2. Reads `BRIEF.md` (the taste), `TASTE.md` (learned refinements) and
   `log/sent.md` (what's already been sent, so nothing repeats).
3. Researches and verifies one curiosity, then delivers it in chat.
4. Asks for a 1–5 rating and waits.
5. On reply: records the rating in `log/sent.md`, updates `TASTE.md`, pushes.

## The files

| File | What it's for |
|---|---|
| `BRIEF.md` | The standing editorial brief. Taste, format, hard rules. |
| `TASTE.md` | Learned preferences from ratings. Overrides `BRIEF.md`. |
| `FEEDBACK.md` | How to ask for and process the rating. |
| `log/sent.md` | Every curiosity sent, with its rating. Repeat-check + training data. |

## Changing it

Edit `BRIEF.md` and push — the next morning's run picks it up automatically.
No need to touch the schedule.

Schedule changes (time, days, pausing) are made on the Routine itself, not here.
