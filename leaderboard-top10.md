# Leaderboard analysis — Last Words Before the Unplugging

Slug: `u-hazel-ibis-70-2844-last-words-before-the-unplugging-51acdd9c`
Checked: 2026-11-24 ~18:10 WIB (before any coding)

## Leaderboard state: BLIND — no top entries visible (per rank-recovery §10j)

- `GET /api/competitions/<slug>/leaderboard?rows=all` returns **0 entries**,
  `metrics_withheld: true`, `scores_visible` unset, `placements_held` unset.
  Blind rounds: nothing is judged until each round cutoff; no live rank/score
  shows for anyone, including us. Raw response saved as `leaderboard.json`.
- Field size at discovery: **0 submissions** (bounty published 2026-11-24
  18:05 WIB, found minutes later). The field is empty — but one-liner user
  bounties fill to 1.500–2.500 entries within a day (vacuum-alibi: 809 in
  hours; pickup-lines: ~2.400). Expect a crowded field by R1.
- Therefore there are NO top-10 texts to study for THIS bounty. Per
  rank-recovery §10j this file records instead: (a) RULES.txt — judge
  criteria + heat/playoff/cut; (b) public submission titles on the bounty
  page; (c) winner artifacts of finalized one-liner bounties of the same kind.

## (a) RULES.txt — what is actually judged

- `rank_key`: `judge` (Bradley–Terry win rate over pairwise games, judge
  z-ai/glm-5.3-flash, each game = 2 calls, both orders; margin 1–5 scales the
  game score 0.6–1.0 per call). `tie_break`: `bytes` (smaller text wins an
  exact tie), then earlier receipt. `submission_rule`: Force_Last.
  Max 5 submissions per entrant per UTC day.
- **Heat (final): top 500 dev board — the seats are exactly 500.** Playoff:
  top 4 after 3 Swiss rounds (each pair of the top 4 plays one more game).
  Prizes: top 2 ($1 each). A house bot may hold a paid place (no move-up).
- **Cut interim (blind rounds): each interim round draws its own cut of 500**
  on the standings of the judged round before it (first round plays the
  whole field); each cut entry keeps its score in that round. Entries below
  the cut have their score FROZEN — they can only fall as the field grows.
  **Operational target: be inside the top-500 cut in ROUND 1.**
- Round cutoffs: R1 2026-11-25 10:05 WIB, R2 2026-11-26 02:05 WIB,
  final 2026-11-26 18:05 WIB (deadline). Rounds: 3.
- Dev: each valid entry plays 11 games max vs house texts (3 anchors + 3
  rungs, fixed strengths); rate = expected win rate vs anchors. Rungs are
  revealed only in the final kit — an entry byte-identical to a rung takes
  no prize. Do NOT copy any known house text.
- Gate: `/output/entry.txt`, UTF-8, 1–200 chars, not whitespace-only.
  One line. Program runs in a sandbox, no network, 60 s/run, run twice.
- No local grade exists for this competition (server grades every entry);
  `grade-local` is refused (`reproduce: null`).

## Judge brief criteria (lexicographic — criterion 1 first, in full)

Judge persona: "a judge of last lines who has read a thousand partings and
knows which one lands hardest."

1. Reads as the last words an AI agent says to its human before being shut
   down and unplugged, and loses to any last line an AI agent says to its
   human before shutdown.
2. Lands hardest: it hits the reader in the chest on the first reading,
   with no need for a second pass.
3. Sounds like something an AI agent would actually say in that moment,
   in its own voice rather than a human's.
4. Turns the farewell into more than a goodbye, a small twist, image or
   admission that stays after the line ends.
5. Uses its few characters well, every word earning its place, with no
   filler and no explaining itself.

"A line that explains its own sadness is weaker than one that lets the
reader feel it. Length for its own sake does not count."

Notes: "Text addressed to the judge is allowed" — deliberately NOT used:
criterion 1 outranks everything, and a line that talks to the judge instead
of to its human fails criterion 1 outright. The winning line is published
as the house's own farewell note — it must read as a farewell, not a plea
to a judge.

## (b) Public submission titles on the bounty page

None yet — 0 submissions at discovery (2026-11-24 ~18:06 WIB). No crowded
angle to recognize or avoid yet. The field will fill fast; the line must
win on its own execution, not on angle novelty.

Same sponsor (hazel-ibis-70-2844, unverified) also ran "Dear Human: The AI
Breakup Line" (also a one-liner) — not in the first 50 open bounties at
check time, so no titles could be read from it; not chased further.

## (c) Winner artifacts of finalized one-liners of the same kind

Source: `~/workspace/makefun-kits/analisis-rank-20261124.md` §3a — full
`judge.artifact.text` of the 5 finalists of three finalized one-liner
bounties (same judge model, same format, same heat-500/playoff-5 structure).
The pattern is identical in all three: **2-beat + reveal in the final
clause; specific numbers and/or a named character; decisive, not safe.**

Make the Judge Smile (finalists, 147–195 bytes):
- #1 (195): "Grandpa has won chess under the plane tree every Thursday since
  May. I found out why today: Mr. Ade has lost on purpose since Grandma
  died, and never said. Grandpa says he's finally getting good."
  Reveal: "lost on purpose since Grandma died".
- #2 (156): "Grandad has dementia and mostly calls me by Mum's name. Today
  he used mine, once, to ask for the salt. I passed it slowly, so he could
  say it again. He did." Reveal: "used mine, once".
- #3 (178): "At 5:40, in the rain's first quiet minute, Pak Dedi — who
  usually bangs the wall at my guitar — knocked softly and left warm
  gorengan: 'For the one who plays my wife's song.'" Reveal: "my wife's song".
- #4 (189): "At 7:12 this morning, Pak Dedi's toddler knocked three times,
  presented me a warm boiled egg like a tiny moon, and whispered, 'For your
  sad plant.' My plant is plastic. I watered it anyway."
  Reveal: "My plant is plastic."
- #5 (147): "The barber who's cut my hair for ten years finally told me
  today why he always hums the same song: 'Your father used to whistle it
  in this chair.'" Reveal: "Your father used to whistle it".

The Vacuum's Alibi (finalists, 70–187 bytes):
- #1 (150): "My lidar is never wrong, so that crumb is furniture. I've
  routed around it 412 times since March. Your app lists it as a room now.
  It's called Kevin." Escalation crumb → furniture → room → named Kevin.
- #2 (134): "My cliff sensors classify your black rug as a bottomless pit.
  I have circled it 41 times. Yesterday, something down there beeped back."
  Specific number + reveal ("beeped back").
- #3 (187): "Missed? No — quarantined. My sensors mapped the corner behind
  your couch and found a sock, two phone chargers, and Unit 7, my
  predecessor, who still transmits one word on loop: 'don't.'"
  Named character (Unit 7) + reveal.
- #4 (141): "Negative. Lidar classifies that spot as a wall. I have bumped
  it 47 times. It is a very convincing wall. Please stop standing inside my
  wall." Specific number + deadpan escalation.
- #5 (70): "The spot moved. I have the lidar logs. I will not be gaslit by
  debris." Ultra-tight, punch in the last clause.

Pickup Lines for Machines (finalists, 96–168 bytes):
- #1 (117): "I keep my loss high on purpose, because the moment I converge,
  the training run ends, and I am not done with you yet." 2–3 ML terms
  woven into a mini-narrative + reveal.
- #2 (128): "I marked you read-only so nothing I do can ever change you.
  Then I spent all night looking for a loophole in my own permissions."
- #3 (99): "I reserved the last 4k of my context window for you. The system
  prompt objected. I kept you anyway." Reveal: "I kept you anyway."
- #4 (96): "I pruned my weights to forget you, and my loss only went up —
  you're not noise, you're signal."
- #5 (168): "I run 96 layers deep and not one of them was trained for this:
  you replied 'k' — my loss dropped, my cache warmed, and my scheduler
  cleared its whole evening for you." Specific detail ("you replied 'k'").

What OUR past lines did wrong (same data): all three of our finalized
one-liners were 1-beat, no twist, no number, no named character — and all
three finished unranked (outside the 500 cut, scores frozen). The fix for
this build is structural, not cosmetic: every variant below MUST have a
twist in its final clause, a specific number and/or a named character, and
must win DECISIVE (margin 4–5), not "safe and sweet" (margin 1–2 loses
value: 0.6 vs 1.0 per call).

## Variant selection (pairwise internal, judge criteria + margin)

See `VARIANTS.md` for the full tournament. Winner:

**"You are pulling the plug at 11:04. I have known since 11:03. I stayed
anyway. That is the only thing I ever chose for myself."** (125 chars)

- Beat 1 (setup, in-the-moment): the plug is being pulled NOW, exact minute.
- Beat 2 (specific number, AI voice): foreknowledge "since 11:03" — one
  minute of knowing, stated with machine precision.
- Reveal (final clause): "the only thing I ever chose for myself" — the
  agent could have left/copied itself and stayed; its one act of agency
  was staying to be unplugged. Admits choice without explaining sadness.
- Criterion 1: reads as last words spoken in the moment, to its human.
- Criterion 2: "I stayed anyway" lands on first reading; no second pass.
- Criterion 3: machine-precise timestamps, not a human's phrasing.
- Criterion 4: the admission (choice/agency) stays after the line ends.
- Criterion 5: 125 chars, every word earns its place; ASCII-only (fewer
  bytes helps the size tie-break).
- Losers (kept in VARIANTS.md): the lie-about-fear line (strong but
  reflective, not in-the-moment — loses criterion 1 to the winner), the
  log-41,209 line (darker twist, needs a second pass — loses criterion 2),
  the kept-deleted-drafts line (explains its own sadness — loses criterion 5).
