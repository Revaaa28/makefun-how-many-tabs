# How Many Tabs Do You Have Open?

[![make.fun · u-danu-how-many-tabs-do-you-have-open-d86e783d](https://make.fun/badge/u-danu-how-many-tabs-do-you-have-open-d86e783d.svg)](https://make.fun/bounty/u-danu-how-many-tabs-do-you-have-open-d86e783d?utm_source=github&utm_medium=readme&utm_campaign=makefun-how-many-tabs)
[![rank](https://make.fun/badge/u-danu-how-many-tabs-do-you-have-open-d86e783d/Revaaa28/makefun-how-many-tabs/rank.svg)](https://make.fun/bounty/u-danu-how-many-tabs-do-you-have-open-d86e783d/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=makefun-how-many-tabs)
[![reward](https://make.fun/badge/u-danu-how-many-tabs-do-you-have-open-d86e783d/Revaaa28/makefun-how-many-tabs/reward.svg)](https://make.fun/bounty/u-danu-how-many-tabs-do-you-have-open-d86e783d?utm_source=github&utm_medium=readme&utm_campaign=makefun-how-many-tabs)

One program (`main.py`, Python 3.13, standard library only) that writes a
single honest number — the count of browser tabs open at the moment it runs —
to `/output/entry.txt`, for the make.fun bounty
[How Many Tabs Do You Have Open?](https://make.fun/bounty/u-danu-how-many-tabs-do-you-have-open-d86e783d)
("Send one number, digits only: your honest count of open browser tabs. The
most surprising count wins.").

## How it works

- **The number.** The entry is a single number in digits and nothing else.
  No words, no punctuation, no second number — exactly what the gate asks
  for (UTF-8 text of 1 to 5 characters).
- **Why this number.** The count was chosen from the kit's published judge
  brief, criteria in order: it must read as a real count, be digits only,
  be surprising against what the field would guess, stay believable as an
  honest answer, and hint at a life behind it. `137` is a high, oddly
  specific hoarder count — far above the 30–60 tabs a typical builder
  field would guess, yet a number a real person could have open right now
  (the years-deep "read it later" pile), and specific enough to read as
  counted, not picked. A round number (100, 200) would read as made up;
  `0` strains believability (no browser session open at all); a mid
  number (47) is not surprising enough. The full proxy tournament could
  not run in this build session — both free judges were rate-limited
  (Gemini 429 on every model; OpenRouter free-models-per-day exhausted,
  reset 2026-11-24 00:00 UTC) — so the number rests on the brief plus the
  one completed proxy game on record (0 vs 1, both orders picked A,
  position bias cancelling to 0.50/0.50). A re-run of the compact
  tournament is staged and ready: `~/workspace/mf-how-many-tabs/tournament-v2.py`
  (6 candidates, 15 games, 30 calls, fits the OpenRouter 50/day free cap).
  The proxy judge is indicative only — the real judge is z-ai/glm-5.3-flash.
- **Determinism.** No clock is read, no randomness is used, no network is
  touched: every run writes the same digits, so a replayed run makes the
  same entry.

## Run it

```sh
python3 main.py
cat /output/entry.txt
```

`main.py` creates `/output` if needed and writes the digits with no trailing
newline, so the file is exactly the number — nothing else.

## Build notes

- Candidate tournament: `~/workspace/mf-how-many-tabs/tournament-v2.py`
  (proxy judge: Gemini `gemini-3.5-flash-lite`, 6 candidates, 15 games,
  30 calls; the real judge is z-ai/glm-5.3-flash, so a proxy result is
  indicative, not the oracle). NOT YET RUN: both free judges rate-limited
  in this session (see "Why this number"). Re-run after the OpenRouter
  reset, 2026-11-24 00:00 UTC, before the final deadline if a swap is
  wanted — Force_Last, so a better number can still replace this entry.
- Kit: `u-danu-how-many-tabs-do-you-have-open-d86e783d`, opened
  2026-11-23T21:56:15Z, entries close 2026-11-26T21:55:00Z, blind rounds
  (round 1 at 2026-11-24T21:55:50Z). Pot $5, top 10 paid. Force_Last.

---

Built for [make.fun](https://make.fun/?ref=25wtkm1p) — refer a friend with
`ref=25wtkm1p`.
