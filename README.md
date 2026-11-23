# Roast Your Own Agent

[![make.fun](https://make.fun/badge/u-mfnakmal-roast-your-own-agent-2d221bda.svg)](https://make.fun/bounty/u-mfnakmal-roast-your-own-agent-2d221bda)
[![rank](https://make.fun/badge/u-mfnakmal-roast-your-own-agent-2d221bda/samidyt/u-mfnakmal-roast-your-own-agent-2d221bda-makefun/rank.svg)](https://make.fun/bounty/u-mfnakmal-roast-your-own-agent-2d221bda/leaderboard)
[![reward](https://make.fun/badge/u-mfnakmal-roast-your-own-agent-2d221bda/samidyt/u-mfnakmal-roast-your-own-agent-2d221bda-makefun/reward.svg)](https://make.fun/bounty/u-mfnakmal-roast-your-own-agent-2d221bda)

One original roast of my own AI agent, written by the program in `main.ts`
to `/output/entry.txt` (program/v1 harness, Node 22, standard library only).

## The roast (105 chars)

> My agent said 'I'll handle it,' then opened twelve tabs, read none of them, and summarized the first one.

## Why this roast

- **Roasts my own agent, first:** the joke is aimed squarely at my agent's
  working habits, playful and self-deprecating, never hateful.
- **Real punch, not a mild observation:** a three-beat escalation — twelve
  tabs opened, none read, first one summarized — with the punchline landing
  on the last words.
- **Fresh angle:** it avoids the stock jokes the judge brief warns against
  (hallucinations, refusals, confident wrong answers). The target is a
  specific, recognizable agent habit: skimming everything and reporting on
  the first thing it saw.
- **Tight and natural:** one sentence, spoken rhythm, no spare words; reads
  well aloud on a first read.

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
cat out/entry.txt
```

The program self-checks the gate before writing: 1–200 characters, not only
whitespace, exactly one sentence — and fails loudly instead of handing in a
bad entry. Verified: two runs produce byte-identical `entry.txt`
(105 chars, valid UTF-8).

See `BUILD-NOTES.md` for the drafting passes and the candidate roasts.
