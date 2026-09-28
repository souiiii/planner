# Current state

> **Authority:** authoritative snapshot of what is true right now.
> **Not authoritative for:** strategy. If this file and [MASTER_ROADMAP.md](MASTER_ROADMAP.md) disagree about priorities or phases, the master roadmap wins and this file should be corrected.
> **Update rule:** any model may update facts, the phase *label* (to match the master, not to invent one), the active sprint id, capacity, and review dates. Do not copy plans, calendars, or metric tables into here.
> **Last reviewed:** 2026-09-28

If you only read one file before acting, read this one, then follow its links. Do not treat empty progress files as proof that prior skill is zero.

## Snapshot

- As of: 2026-09-27
- Planning status: first strategic review held. Master roadmap is in force. Minutes: [reviews/strategic/2026-09-27.md](reviews/strategic/2026-09-27.md)
- Active sprint: none
- Phase label: `gate-window`
- Attention bands: see the table below. Full rules: [MASTER_ROADMAP.md](MASTER_ROADMAP.md)

## Timeline

Canonical working dates. Original wording is preserved in [context/PROFILE.md](context/PROFILE.md). When a date firms up, change it here and append a decision if the change affects strategy.

| Event | Working date | Confidence |
| --- | --- | --- |
| Planning start / repo created | 2026-09-27 | known |
| GATE 2027 exam | around February 2027 | owner-reported, month not exact, day unknown |
| LSEG joining | around August 2027 | owner-reported, not a confirmed offer date in this repo |
| Optional LSEG internship | unknown | possible only. Not offered in this repo, not scheduled |
| Horizon end | LSEG joining | approximate |

Sprint date boundaries are calendar dates. Clock times, once a sprint exists, live only in that sprint's `CALENDAR.ics`.

## Tracks

"Not started" means this repo has no logged work. It does not mean the owner has no prior skill. See [context/PROFILE.md](context/PROFILE.md). Bands are the current phase only. Post-gate bands live in the master roadmap, not here.

| Track | Repo status | Attention | Latest evidence |
| --- | --- | --- | --- |
| GATE | domain roadmap complete; Stage 0 light setup pending | primary | owner: paper CS/IT, target AIR < 400; no level logged |
| System design | not started in this repo | secondary | none logged |
| Product | not started in this repo | secondary | none logged |
| Music | domain roadmap written; no sessions logged | maintenance | owner reports tools understood; setup recorded; gap is translating ideas into convincing records. Folder is `beat-production/`. D-021 |
| Markets | not started in this repo | maintenance | none logged |
| LeetCode | not started in this repo | maintenance | owner reports existing DSA ability; no maintenance log yet |
| LSEG notes | placeholder only | not a track | no internship, no joining prep written |

## Timezone

Working timezone for sprint calendars: `Asia/Kolkata`.

Owner-instructed 2026-09-27. Use this for every `CALENDAR.ics` unless this section is later changed. City is still unknown. The timezone is not a home address, a college, or a class timetable. Do not invent those from it.

## Capacity

`unknown`.

Do not assume hours per day or that every day is productive. Until the owner reports a real constraint, sprints should be small and say that capacity is unknown. College load, a job, health, and other obligations were not stated. Do not infer a free final year.

## Last reviews

| Kind | When | Where |
| --- | --- | --- |
| Strategic | 2026-09-27 | [reviews/strategic/2026-09-27.md](reviews/strategic/2026-09-27.md) |
| Monthly | none | — |
| Sprint | none | — |

## Unknown facts

Do not invent these. Do not let a domain file answer them locally. If one becomes known, update it here and note the date.

- Name, city. Working calendar timezone is `Asia/Kolkata` (see above). That does not identify a city
- Weekly time actually available, and what else occupies the next eleven months
- Degree status, college, branch. The timeline is compatible with a delayed joining after a campus placement. That is an inference, not a fact. See profile
- GATE: exact exam date, current preparation level per subject, materials already owned or used. Paper is CS/IT and the target is AIR < 400 (owner-stated 2026-09-27)
- Whether "approximately ₹14 LPA" is CTC, and what the role, team, office, and exact joining date are
- Whether an internship will be offered, in which team, and when
- Music: sample sources, and which DAW becomes primary. Setup otherwise recorded in `beat-production/ROADMAP.md`
- Existing depth in system design, markets, or production engineering beyond the skills listed in the profile
- Budget for exams, cloud, software, or music tools
- Any constraint that would make a 10-day sprint unrealistic (travel, exams other than GATE, family)

## Assumptions in force

Planning-system choices, not life strategy. Full text: [DECISIONS.md](DECISIONS.md).

- One integrated sprint, not per-track sprints (D-001)
- The open sprint is the `current-sprint/` directory, then moved into `sprints/` (D-016). That directory does not exist yet
- Timed work lives in `CALENDAR.ics`, not in the plan (D-017)
- No sprint was allowed while the master roadmap was a skeleton (D-004). That block is lifted. Do not open `sprint-001` until the owner asks
- First strategy: `gate-window`, then `post-gate` (D-018)
- Existing stack is the default, not a ban (D-019)
- Master sets priority, timing, and role; domain passes set milestones and methods (D-020)
- Attention is expressed in bands, not percentages (D-005)
- Resource lists stay empty until the owner accepts them (D-006)

## Next planning action

Domain planning for this phase, not a sprint. Do not create `current-sprint/` or `sprint-001` until the owner asks.

1. GATE — Stage 0 light setup only (syllabus + real-PYQ source + notes/log system). No diagnostic. Path: `gate/ROADMAP.md`. Execution waits for sprint-001.
2. System design — first thread of the arc in the master roadmap. Do not assume a zero baseline.
3. Product — the experiment loop. Do not invent an idea.

## Recent changes

- 2026-09-27 — Repository created. No goal work logged.
- 2026-09-27 — Sprint execution switched to `current-sprint/` plus `CALENDAR.ics`. No sprint opened. Working calendar timezone set to `Asia/Kolkata`.
- 2026-09-27 — First strategic review. Phase is `gate-window`. No sprint opened.
- 2026-09-27 — Music stream broadened from beat production to finished songs (rap-first, vocals included). Bands unchanged. Folder name kept. D-021.
- 2026-09-27 — Music domain roadmap written: six ability-gated stages, milestones, and a finished-piece definition. No dates or quotas. No sessions logged.
- 2026-09-27 — Music roadmap cleanup: vocal/song stages moved earlier (S3, S4); beat craft is S5. Setup facts recorded. Six owner-chosen references recorded in `beat-production/REFERENCES.md`.
- 2026-09-27 — GATE domain roadmap written: Stage 0 baseline, concept pass, PYQ mastery, mock consolidation, exam mode. Paper CS/IT and target AIR < 400 recorded. No preparation logged.
- 2026-09-28 — GATE roadmap revised to PYQ-driven loop with Stage 0 as light setup only (no diagnostic). Paper CS/IT and target AIR < 400 confirmed. No preparation logged; execution waits for sprint-001.
