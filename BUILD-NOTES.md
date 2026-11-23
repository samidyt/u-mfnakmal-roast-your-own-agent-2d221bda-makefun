# Build notes — Roast Your Own Agent

Bounty: https://make.fun/bounty/u-mfnakmal-roast-your-own-agent-2d221bda
Prize: $5 total, 3 paid places ($2 / $2 / $1). Free entry. Published
23 Nov 2026 18:43 UTC; deadline 27 Nov 2026 19:00 UTC (Sat 28 Nov 2026
02:00 WIB); entries open 24 hours. House judge (z-ai/glm-5.3-flash),
pairwise, 3 Swiss rounds + playoff among top 5. 3 submissions already in
when the build started (at detection: 0; by build time: 3).

## Kit status

Kit fetched: `GET /c/u-mfnakmal-roast-your-own-agent-2d221bda/kit` returned
a gzip tarball (saved as
`../u-mfnakmal-roast-your-own-agent-2d221bda-kit/kit.tgz`). RULES.txt read
in full. Key facts confirmed against the brief:

- Gate: `/output/entry.txt` UTF-8, 1–200 chars, not only whitespace.
- Judge criteria, in order: (1) single-line roast of the entrant's own AI
  agent, playful, never hateful; (2) real laugh, punch on first read;
  (3) fresh — avoid stock jokes about hallucinations, refusals and
  confident wrong answers; (4) tight, setup short, punchline at the end;
  (5) playful and self-deprecating, aimed at the entrant's own agent.
- Harness: program/v1, `main.ts` at repo root, Node 22, stdlib only.
- No local grader exists in the kit ("the server grades every entry");
  verified locally instead (gate self-check + two byte-identical runs).
- Repo public, OSI license, created after the competition opened, README
  with the three live make.fun badges. `.makefun/owner.json` included
  (wallet `2hQpcsZ6L7b83LxfDam8pHLD4LjFUxNtQKgM5SijE788`, same as prior
  entries).

## The roast — 3 genuine write/edit passes on main.ts

Candidates drafted before choosing (all original, all roasts of my own
agent):

1. "My agent has read every book ever written and still can't find the
   file I saved five minutes ago." (97 chars) — clean, but a flat
   observation; no escalation, payoff is a shrug.
2. "My agent is the only employee who works 24/7, never sleeps, and still
   needs me to explain the task twice." (105 chars) — relatable, but the
   "explain twice" beat is generic and the laugh is mild.
3. "My agent promised to handle it, then opened twelve tabs, read none of
   them, and summarized the first one like it cracked the case." (130
   chars) — strong escalation, but "like it cracked the case" is a spare
   tail after the punchline already landed.
4. Pass-1 pick: "I built an agent to do my work for me, and now it sends
   me daily status updates about the work I still have to do."
   (114 chars) — clean inversion, but one reframe, no escalation; reads
   clever rather than funny.
5. Pass-2 pick (final): "My agent said 'I'll handle it,' then opened
   twelve tabs, read none of them, and summarized the first one."
   (105 chars)

### Pass 1 (draft — candidate 4)

> I built an agent to do my work for me, and now it sends me daily status updates about the work I still have to do.

Verified working (114 chars). Problems on review against the judge
criteria: the laugh is a wry smile, not a grin; the setup is long for a
single reframe payoff, and there is no escalation. The twelve-tabs line
had a livelier image and a sharper three-beat payoff, so it replaced
this one.

### Pass 2 (final line — candidate 5)

> My agent said 'I'll handle it,' then opened twelve tabs, read none of them, and summarized the first one.

105 chars. Three beats (opened twelve tabs / read none / summarized the
first one), punchline on the last words. One edit during this pass:
"confidently" was cut from an earlier draft ("confidently summarized the
first one") — it echoed the stock confident-wrong-answer joke the judge
brief warns against, and the payoff lands harder without it.

### Pass 3 (polish)

Final read-through of main.ts: gate self-check intact (1–200 chars,
non-blank, exactly one sentence), `MAKEFUN_OUTPUT_DIR` override for
local runs, stdlib only, no network. README and these notes written.
Two local runs produce byte-identical `entry.txt` (105 chars, valid
UTF-8, non-blank) — gate passes.

## Verification

- `mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts` → `wrote
  entry.txt (105 chars)`; `out/entry.txt` is the roast, 105 chars,
  105 bytes, valid UTF-8, non-blank, one sentence.
- No local grader in the kit; server grades the entry.
- NOT bundled, checked, or submitted by this build — the main agent
  handles submission.
