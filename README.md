# Daily Curiosity

A scheduled agent that sends Przemek one curiosity every weekday at 09:00
Europe/Warsaw, and learns from whether he liked it.

## How it works

A Routine fires **into this ongoing conversation** each weekday morning — not a
fresh session. That matters for two reasons: the message appears in the thread the
user is already reading, and the container has push access to this repo, so the
logs actually persist. A fresh session can clone the repo but cannot push to it,
which silently breaks dedup, spaced repetition and preference learning.

A second tiny routine fires 12 minutes later purely to raise a push notification,
since the platform only sends those for fresh-session routines.

Each morning the session:

1. Clones this repo and checks out `claude/daily-curiosity-agent-u8hjuo`.
2. Reads `BRIEF.md` (the taste), `TASTE.md` (learned refinements) and
   `log/sent.md` (what's already been sent, so nothing repeats).
3. Researches and verifies one curiosity, then delivers it in chat.
4. Asks for a 1–5 rating, then asks the day's Capital Quiz question, and waits.
5. On reply: records the rating in `log/sent.md`, updates `TASTE.md`, marks the
   quiz answer in `log/quiz.md`, pushes.

Both live in one routine because they run at the same time on the same days —
two routines would mean two containers and two notifications at the same minute.

## The files

| File | What it's for |
|---|---|
| `BRIEF.md` | The standing editorial brief. Taste, format, hard rules. |
| `TASTE.md` | Learned preferences from ratings. Overrides `BRIEF.md`. |
| `FEEDBACK.md` | How to ask for and process the rating. |
| `log/sent.md` | Every curiosity sent, with its rating. Repeat-check + training data. |
| `QUIZ.md` | Capital Quiz rules: difficulty, spelling tolerance, spaced repetition. |
| `log/quiz.md` | Every country asked, the answer given, and the review schedule. |

## Changing it

Edit `BRIEF.md` and push — the next morning's run picks it up automatically.
No need to touch the schedule.

Schedule changes (time, days, pausing) are made on the Routine itself, not here.

## Schedule

| Routine | ID | Schedule |
|---|---|---|
| Daily Curiosity + Capital Quiz | `trig_012uAaGywaqHQyFM3nZHDyQZ` | `0 7 * * 1-5` UTC = 09:00 Europe/Warsaw, Mon–Fri. Bound to the ongoing session. |
| Phone nudge | `trig_01RkHy74bzPHDCaFEe9WDskg` | `12 7 * * 1-5` UTC. Fresh session, does nothing but trigger a push. |
| DST flip | `trig_01GnyGJQsVgbyXCJEZWbAP9n` | one-shot 2026-10-25. Corrects both crons, then schedules its own successor. |

The cron is stored in UTC, so Warsaw's daylight-saving switches would drift the
delivery by an hour twice a year. The DST flip routine corrects the cron on each
switch and schedules the next flip before it exits, so it maintains itself.

The nudge must stay behind the main routine — if it ever fires first it will
announce a message that has not been written yet.
