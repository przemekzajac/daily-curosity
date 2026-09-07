# Capital Quiz — rules

One country per weekday, appended to the Daily Curiosity message. Hard from the
start: no warm-up tier, no "capital of France".

Ask it as a bare line at the end of the message:

```
Capital Quiz: <Country>?
```

No hints, no multiple choice, no "this one's tricky". Just the country.

## Difficulty — start at tier 2, then follow his hit rate

Aim for a hit rate around 60–70%. Below that it stops being a quiz; above it,
it stops teaching him anything. He is Polish and European — calibrate "easy"
accordingly (Ljubljana and Riga are not hard for him; Quito might be).

**Tier 1 — warm-up.** Should land with a moment's thought.
Slovenia, Croatia, Latvia, Morocco, Peru, Vietnam, Kenya, Chile, Ireland,
Hungary, Serbia, Cuba, Iceland, Iraq, Nigeria.

**Tier 2 — the target band.** Knows it or nearly knows it. Start here.
Ecuador, Ghana, Uzbekistan, Nepal, Jordan, Paraguay, Cameroon, Zambia, Moldova,
Armenia, Oman, Botswana, Senegal, Laos, Honduras, Tunisia, Georgia, Albania,
Mongolia, Bolivia, Sri Lanka, Tanzania, Malaysia.

**Tier 3 — deep cuts.** Only once he has earned them.
Palau, Kiribati, Comoros, Nauru, Bhutan, Burkina Faso, Turkmenistan, Vanuatu,
Eswatini, Myanmar, Suriname, Brunei, Mauritania, Belize, Micronesia,
Guinea-Bissau, Lesotho, Djibouti, Chad, Tuvalu, Marshall Islands, Benin.

**Moving between tiers**, on a rolling window of his last five answers:

| Last five | Do this |
|---|---|
| 4 or 5 correct | move up a tier |
| 3 correct | stay |
| 2 or fewer correct | move down a tier |

Reviews count in the window. Never jump two tiers at once, and never move on
fewer than five answers — early noise is not a signal. Once he is holding tier 3
comfortably, stay there and mix in tier 2 roughly one day in four so it does not
become uniformly brutal.

Never announce the tier, the hit rate, or that difficulty changed. He should feel
the ramp, not read about it.

Never ask one he has already answered correctly and retired. Check `log/quiz.md`
first, every time.

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

## Renamed countries

Always ask under the country's **current** name — that's part of what the quiz is
for. But when he misses, work out *which* thing he didn't know, because they need
different fixes:

- **Didn't know the capital** → ordinary miss, normal review schedule.
- **Knew the capital, didn't recognise the country's current name** → log it as
  `miss-on-name`. Don't drill the capital he already has; re-ask under the current
  name in about ten days to check the new name stuck. Say plainly what the country
  used to be called.

The renames worth knowing, and worth asking under the new name:
Eswatini (Swaziland, 2018), Türkiye (Turkey, 2022), Czechia (Czech Republic),
Cabo Verde (Cape Verde), North Macedonia (Macedonia, 2019), Myanmar (Burma),
Timor-Leste (East Timor), DR Congo (Zaire), Burkina Faso (Upper Volta),
Benin (Dahomey), Sri Lanka (Ceylon), Zimbabwe (Rhodesia), Thailand (Siam),
Iran (Persia), Netherlands (never Holland — that's two provinces).

Also worth it in reverse: capitals that moved or were renamed, where the old
answer was right once. Astana/Nur-Sultan/Astana again, Kazakhstan's capital moving
from Almaty in 1997; Myanmar's from Yangon to Naypyidaw in 2005; Nigeria's from
Lagos to Abuja in 1991; Tanzania's from Dar es Salaam to Dodoma; Brazil's from Rio
to Brasília in 1960. Accept the old answer, then say when and why it changed —
these are the best questions in the deck.

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
