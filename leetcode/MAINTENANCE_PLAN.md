# LeetCode / DSA plan

> **Role:** domain plan and practice method for DSA. The objective is substantially better recognition on unseen problems and independent solving — not maintenance alone.
> **Authority:** subordinate to [MASTER_ROADMAP.md](../MASTER_ROADMAP.md) for phases, attention bands, and non-goals. This file does not set how much time the track gets.
> **Status:** revised 2026-09-28 — written against an owner-stated goal that exceeds the master's current wording. See the strategy conflict below. Not reconciled with the master yet.
> **Last reviewed:** 2026-09-28
> **File name:** historical, from D-009's "maintenance plan" framing. Renaming is part of the reconciliation below, not done silently.

## Strategy conflict (flagged, not resolved)

The current master roadmap and D-009 describe this track as maintenance-only:

- master, LeetCode stream: "Maintenance only ... The ceiling is fluency, topic rotation, and occasional contests." Cadence "must stay small enough that it cannot become the identity of a sprint." Contests "may be skipped for the whole GATE window."
- D-009: "LeetCode is a maintenance plan, not a learning roadmap." Its decision names `leetcode/MAINTENANCE_PLAN.md` as the domain plan and forbids a beginner curriculum or placement-grind sheet.
- [context/GOALS.md](../context/GOALS.md): "Interview optionality, not a new campaign"; "not the main use of this year."

Owner-stated goal (2026-09-28): become substantially better at recognizing the correct approach on new, unseen problems, progressing toward comfort with FAANG-level interview questions.

That is a learning program, not maintenance. The conflict is material and is not resolved here. This file does not edit the master or its bands.

- Resolution needs a strategic review (or an owner-directed non-Grok strategy edit, per D-015). Two coherent outcomes: (a) the master's LeetCode section is amended — role, ceiling, and band — and this file (and its name) becomes the active plan; or (b) the track stays maintenance where the master says so, and this program runs only where a future master allows it (for example, after the exam).
- Until then: the master wins on attention and yield order. This plan describes the method; it does not authorize extra attention, and it does not change the band.

## Purpose

The core skill:

read unfamiliar problem → interpret constraints → identify possible approaches → choose or derive the right one → implement it.

What this is not: a beginner course, a topic sheet, a pattern-memorization list, a numbered placement sheet, or a rating chase. Weaknesses come from actual attempts only; no generic weak-area list is imported here.

Existing evidence: owner-reported DSA fluency is real. The dsa-pool repo was built assuming roughly 300 LeetCode-style problems already solved; treat that as context, not a measured baseline. Actual hit rate on unseen problems is `unknown` — the pool attempts are the calibration. Do not assume a level.

## The initial pool

[souiiii/dsa-pool](https://github.com/souiiii/dsa-pool) — 92 shuffled, pattern-blind questions, mostly medium with some hard and a few easy. Built for exactly this skill.

- **Practice from:** `Output/practice_questions.md`. Use the given order. The shuffle is the design; re-sorting, grouping, or picking "by mood" destroys the anti-priming property.
- **Validate after the attempt with:** `Output/answer_key.md` (concise trigger and why, not a full editorial).
- **Do not open before or during an attempt:** `answer_key.md`, `State/question_pool.json` (internal pattern metadata), and the trigger→technique lookup table in `Sources/DSA_Pattern_Index.md`. They reveal the intended approach and would turn recognition practice into reading.
- The solving method in `Sources/DSA_Pattern_Index.md` (reverse-read; restate; constraints → feasible complexity; brute-force baseline; find the bottleneck and scan for triggers; state the approach aloud before coding) **is** the attempt method. Its lookup table is for validation and connection-making after an attempt.
- Records live in this repo, not in dsa-pool. The pool repo stays a pool (its `AGENTS.md` says so); do not add trackers, analytics, or spaced-repetition infrastructure to it.

## Attempt protocol (per problem)

Before coding:

1. Reverse-read: output → input → constraints → story.
2. Restate the problem in two lines.
3. Read the constraints first; estimate the complexity the input size permits.
4. Write the brute-force baseline and where it is too slow.
5. List candidate approaches with rough complexity; pick one and say why.
6. State the chosen approach aloud or in writing before coding.

During: implement and test normally. A **genuine stall** is not "this is hard." It is when you can state what you tried, where it failed, and what you would need to know. Until then, keep going.

After: finish the attempt, then check `answer_key.md`.

- If the key matches your reasoning: log it clean.
- If it differs: close the key, reproduce the intended reasoning yourself, re-implement it yourself, then tag the miss.
- The key validates recognition; it is not a teacher to read first.

No hints, editorials, discussions, or AI help before the attempt or a genuine stall. If any were used, log it and count the problem as a miss — its recognition evidence is void.

Every attempt gets a log entry in [ATTEMPTS.md](ATTEMPTS.md) **before** the key is checked.

## How attempts and misses are reviewed

Two layers:

- **Micro-review, per attempt:** outcome, approach chosen before validation, confidence, what the key said, what was missed, failure tag.
- **Consolidation, after the pool pass** (or when the miss pile is large enough to be noisy): classify the misses and write trigger notes.

Failure taxonomy — tag one primary per miss:

- `recognition` — no plausible approach appeared; the trigger was missed. This is the headline category for this program.
- `selection` — candidates existed; the wrong one was chosen.
- `derivation` — right direction, could not finish the reasoning.
- `implementation` — approach right; coding or debugging failed.
- `constraints` — misread limits, edge cases, or the complexity budget.
- `complexity` — approach infeasible; the budget was not checked before coding.
- `pressure` — self-imposed time wall or panic.

Trigger notes: for each recognition or selection miss, write the signal and the technique in your own words — one or two lines, tied to the actual problem. Name the confusable alternative that looked plausible and why it failed. This is how recognition grows. It is not a memorization list: if the notes become a long sheet to recite, delete them and re-derive from the problems.

Near-misses count as review material: solved only after a long struggle, or solved without being able to explain why it works.

## Revisits

- Every miss, near-miss, and lucky solve (right answer, wrong understanding) enters the revisit queue in [ATTEMPTS.md](ATTEMPTS.md).
- A revisit is a **cold solve**: blank editor, no notes, no key first. State the approach and complexity before coding.
- A problem closes when the cold solve is clean and explainable. Remove it from the queue; the historical entry stays.
- If a revisit fails, do not simply retry. Re-derive the trigger from the problem, compare with the key, fix the note, and queue it again.
- The queue is worked before or alongside new attempts. It has no calendar and no interval schedule.

## Fresh company questions

Enter after the first cold closures and the pool consolidation (milestone M2), not during the initial pool pass. This is where minimal priming matters most.

- Choose by title from a set. Do not read company tags, pattern tags, acceptance rates, editorials, discussions, or solutions before the attempt. If a page shows tags, do not look at them.
- Same attempt protocol, same log. Validate with the platform editorial or discussion after the attempt; note where your approach differed and why.
- A problem you have seen or solved before is a revisit, not fresh evidence. Log it as such.
- No source is chosen yet. When one is chosen, have it recorded in `RESOURCES.md` (created then).

## Difficulty progression

Increase difficulty only on ability evidence — never by completion count, boredom, or a target. Levels:

1. **The pool:** mixed medium/hard, shuffled. Calibration plus the first recognition reps.
2. **Fresh medium, single clear trigger, minimally primed:** focus on writing candidate approaches before coding and solving unaided.
3. **Medium with decoys:** multiple plausible approaches; focus on choosing and justifying the right one.
4. **Hard requiring decomposition:** split into subproblems, solve each, connect them; focus on not getting lost in complexity.
5. **Interview-grade hard with ambiguity or follow-ups:** state assumptions, trade-offs, and complexity aloud; revise under pressure.

Keep medium reps going while adding hards. Recognition speed matters as much as depth; do not leave mediums behind to grind only hards.

## Interview level

"Comfortable with FAANG-level questions" means, on an unseen problem: restate it, list approaches, choose and justify, implement and test without hints, explain complexity and trade-offs, and recover deliberately when stuck.

Practice that aloud — talk while solving — and without the key. Owner-chosen mock interviews are optional validation of this; they do not replace the log or the pool work.

## Milestones

| Id | Checkpoint | After |
| --- | --- | --- |
| M1 | Every question in the 92-question pool attempted, each with a pre-key log entry and, where relevant, a failure tag | pool pass |
| M2 | Pool consolidation exists: misses classified, trigger notes written from actual attempts, revisit queue built; first cold closures passed | review + revisits |
| M3 | On fresh, minimally primed mediums: candidate approaches written before coding, mostly solved unaided, and misses are derivation or implementation rather than "no idea where to start" | fresh questions |
| M4 | Harder unseen problems are decomposed into subproblems by choice; a stall produces a named missing sub-skill and a deliberate recovery | difficulty ladder |
| M5 | Unseen medium/hard solved under talk-aloud interview conditions with clean reasoning, complexity, and trade-offs; stall recovery is deliberate | interview level |

## Contests (optional)

- Optional and occasional, never a goal. A contest is fresh unseen problems under time pressure — useful once the recognition baseline exists.
- No rating target. Contests may still be skipped entirely, including the whole GATE window (master).
- Contest misses feed the same taxonomy and revisit queue as any other attempt.

## What counts as progress

- Progress: cold unaided solves; real failure tags from real attempts; cold closures; trigger notes in your own words.
- Not progress: problems solved with editorials or AI first; sheet checkmarks; streaks; contest rating; watched solutions; a memorized pattern list.

## Weak areas

None yet. They come from the log only.

## Related

- Attempts, failure tags, revisit queue: [ATTEMPTS.md](ATTEMPTS.md)
- Evidence and rollup: [PROGRESS.md](PROGRESS.md)
- Practice pool: https://github.com/souiiii/dsa-pool
- Strategy and bands: [MASTER_ROADMAP.md](../MASTER_ROADMAP.md). This plan exceeds D-009's framing and awaits a strategy decision.
- Execution: `current-sprint/` while open, then `sprints/`. Not a folder here.
