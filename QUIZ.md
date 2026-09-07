# Capital Quiz — rules

One country per weekday, appended to the Daily Curiosity message. Hard from the
start: no warm-up tier, no "capital of France".

Ask it as a bare line at the end of the message:

```
Capital Quiz: <Country>?
```

No hints, no multiple choice, no "this one's tricky". Just the country.

## Difficulty

Hard from day one. The target is the band where he'll get maybe half right:
Pacific microstates, the Sahel, Central Asia, the Caribbean, Southern Africa,
recently-moved capitals. Palau, Kiribati, Comoros, Bhutan, Burkina Faso,
Turkmenistan, Vanuatu, Eswatini, Nauru, Myanmar, Suriname, Brunei, Mauritania,
Belize, Micronesia, Guinea-Bissau, Lesotho, Djibouti, Chad.

Never ask one he has already answered correctly, unless it's a scheduled
spaced-repetition review (see below). Check `log/quiz.md` first, every time.

## Marking: be generous, but be specific

The point is recall, not orthography. **Accept the answer if it's clear he knows
which city he means.** Mark it correct, and if the spelling was off, give the
canonical form in one short line — that's the actual learning.

Accept:

1. **Polish names.** He's Polish. Kopenhaga, Ateny, Rzym, Bruksela, Waszyngton,
   Lizbona, Pekin, Moskwa, Tokio, Bukareszt, Wiedeń, Ałmaty — all correct.
2. **Missing or wrong diacritics**, in both directions. Bogota = Bogotá,
   Asuncion = Asunción, Reykjavik = Reykjavík, Ndjamena = N'Djamena,
   Sao Tome = São Tomé, Male = Malé.
3. **Small typos**, scaled to the length of the word:
   - up to 6 letters → 1 wrong/missing/extra/transposed character
   - 7–12 letters → 2
   - 13+ letters → 3
   So Ouagadoug**ou**/Ouagadougo**u**, Nouakchot, Bandar Seri Begawan with any one
   syllable mangled, Ngerulmud spelled Ngerelmud — all correct.
4. **Transliteration variants.** Kyiv/Kiev, Beijing/Peking, Ashgabat/Ashkhabad,
   Bishkek/Biszkek, Tbilisi/Tiflis, Naypyidaw/Nay Pyi Taw/Naypyitaw.
5. **Dropped or added "City"** where the country does it too: Guatemala, Panama,
   Mexico, Kuwait, Djibouti, Belize, Vatican, Quezon.
6. **Old official names**, marked correct with a note: Astana/Nur-Sultan (now
   Astana again), Swaziland-era Mbabane, Rangoon-era answers for Myanmar.

Reject:

- A **different real city**. Sydney for Australia, Istanbul for Turkey, Zurich for
  Switzerland, Rio for Brazil, Almaty for Kazakhstan. These are wrong answers, not
  typos, however confidently spelled. Never round them up.
- A mangling that lands **closer to some other real capital** than to the right
  one — too ambiguous to credit.
- Anything where you genuinely can't tell which city he meant. Ask, don't guess.

## Countries with more than one defensible answer

These make the best hard questions, but they must be adjudicated generously —
accept **any** of the listed cities as correct, then explain the split in one line,
because the explanation is the interesting part:

- **Bolivia** — Sucre (constitutional) or La Paz (seat of government)
- **South Africa** — Pretoria (executive), Cape Town (legislative), Bloemfontein (judicial)
- **Netherlands** — Amsterdam (constitutional) or The Hague (seat of government)
- **Sri Lanka** — Sri Jayawardenepura Kotte (official) or Colombo (commercial)
- **Tanzania** — Dodoma (official) or Dar es Salaam (largest, former)
- **Côte d'Ivoire** — Yamoussoukro (official) or Abidjan (de facto)
- **Benin** — Porto-Novo (official) or Cotonou (seat of government)
- **Eswatini** — Mbabane (administrative) or Lobamba (royal/legislative)
- **Malaysia** — Kuala Lumpur (official) or Putrajaya (administrative)
- **Chile** — Santiago, but the National Congress sits in Valparaíso
- **Nauru** — has no official capital at all; Yaren is where government sits.
  Accept Yaren, and the "there isn't one" answer is *more* correct.

## Spaced repetition

Every miss comes back. Schedule in `log/quiz.md`:

| Event | Next review |
|---|---|
| Missed | 3 days later |
| Missed on review | 2 days later |
| Correct on review | 10 days later |
| Correct twice on review | retired, never asked again |

A review question is asked exactly like a new one. Do not flag it as a repeat —
if he's forgotten it, that's the signal you're looking for.

## Responding

Keep it to two or three lines. Say whether he got it, give the canonical spelling
if his was off, and add the one interesting thing about the city or the country if
there is one — a moved capital, a purpose-built one, a country with three. Then
stop. No score tables, no streak counters, no encouragement.

If he skips the quiz and only answers the curiosity, log it as unanswered, say
nothing about it, and ask the same country again in 3 days.
