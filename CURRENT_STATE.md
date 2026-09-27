# Current state

> **Authority:** authoritative snapshot of what is true right now.
> **Not authoritative for:** strategy. If this file and [MASTER_ROADMAP.md](MASTER_ROADMAP.md) disagree about priorities or phases, the master roadmap wins and this file should be corrected.
> **Update rule:** any model may update facts, the phase *label* (to match the master, not to invent one), the active sprint id, capacity, and review dates. Do not copy plans, calendars, or metric tables into here.
> **Last reviewed:** 2026-09-27

If you only read one file before acting, read this one, then follow its links. Do not treat empty progress files as proof that prior skill is zero.

## Snapshot

- As of: 2026-09-27
- Planning status: scaffolded. Master roadmap is a skeleton. No strategic review has been held
- Active sprint: none
- Phase label: TBD (no phase adopted)
- Attention bands: not assigned

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

Bands are not assigned. "Not started" means this repo has no logged work. It does not mean the owner has no prior skill. See [context/PROFILE.md](context/PROFILE.md).

| Track | Repo status | Attention | Latest evidence |
| --- | --- | --- | --- |
| GATE | not started in this repo | TBD | none logged |
| System design | not started in this repo | TBD | none logged |
| Product | not started in this repo | TBD | none logged |
| Beat production | not started in this repo | TBD | none logged |
| Markets | not started in this repo | TBD | none logged |
| LeetCode | not started in this repo | TBD | owner reports existing DSA ability; no maintenance log yet |
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
| Strategic | none | — |
| Monthly | none | — |
| Sprint | none | — |

## Unknown facts

Do not invent these. Do not let a domain file answer them locally. If one becomes known, update it here and note the date.

- Name, city. Working calendar timezone is `Asia/Kolkata` (see above). That does not identify a city
- Weekly time actually available, and what else occupies the next eleven months
- Degree status, college, branch. The timeline is compatible with a delayed joining after a campus placement. That is an inference, not a fact. See profile
- GATE paper, exact exam date, current preparation level, materials already owned or used
- Whether "approximately ₹14 LPA" is CTC, and what the role, team, office, and exact joining date are
- Whether an internship will be offered, in which team, and when
- Music setup: DAW, samples, monitoring, experience so far
- Existing depth in system design, markets, or production engineering beyond the skills listed in the profile
- Budget for exams, cloud, software, or music tools
- Any constraint that would make a 10-day sprint unrealistic (travel, exams other than GATE, family)

## Assumptions in force

Planning-system choices, not life strategy. Full text: [DECISIONS.md](DECISIONS.md).

- One integrated sprint, not per-track sprints (D-001)
- The open sprint is the `current-sprint/` directory, then moved into `sprints/` (D-016). That directory does not exist yet
- Timed work lives in `CALENDAR.ics`, not in the plan (D-017)
- No sprint until the master roadmap leaves skeleton status (D-004)
- Attention will be expressed in bands, not percentages, once assigned (D-005)
- Resource lists stay empty until the owner accepts them (D-006)

## Next planning action

Grok 4.7 writes the first master roadmap using the read set at the top of [MASTER_ROADMAP.md](MASTER_ROADMAP.md).

Until that happens, do not create `current-sprint/` or `sprints/sprint-001/`.

## Recent changes

- 2026-09-27 — Repository created. No goal work logged.
- 2026-09-27 — Sprint execution switched to `current-sprint/` plus `CALENDAR.ics`. No sprint opened. Working calendar timezone set to `Asia/Kolkata`.
