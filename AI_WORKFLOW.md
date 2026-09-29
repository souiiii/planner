# AI workflow

> **Role:** operating manual for any model editing this repo.
> **Authority:** authoritative for procedure. It is not a plan, a status file, or a decision log.
> **Calendar file format:** [templates/CALENDAR_GUIDE.md](templates/CALENDAR_GUIDE.md). If this file and that guide disagree about ICS syntax, the guide wins.
> **Last reviewed:** 2026-09-27

You are one of several models that will touch this repo between now and about August 2027. Read this before editing. Do not rely on memory of an older plan. The files are the plan.

"You" in the rest of this repo usually means the owner. In this file, **the model** means whichever AI is about to edit, and **the owner** means the human.

## Roles

| Work | Who |
| --- | --- |
| Master strategy, phase changes, success definition | Normally Grok 4.7, via a strategic review |
| 10-day sprint plans, calendars, and reviews | Any capable model, following this file and the calendar guide |
| Domain progress updates from owner-reported work | The model that just ran the review, or a model the owner asked to log something |
| Implementation of a product or technical project | A coding agent, usually in another repo. Link the result from here. Do not turn this repo into the codebase |

A sprint-planning model must not "improve" the strategy while it is scheduling 10 days. The calendar must not invent a priority either.

## Authority map

File headers repeat this. If a header and this table disagree, the header wins, then fix this table.

| File | What it owns | What it must not contain |
| --- | --- | --- |
| `MASTER_ROADMAP.md` | Current strategy: phases, attention bands, milestones, deliberate non-goals, success by joining | Task lists, daily schedules, topic syllabi, live metrics |
| `CURRENT_STATE.md` | Snapshot of the present: dates, phase *label*, which sprint id is active, timezone, capacity, last review, unknown facts | A second copy of the strategy, a task list, a second plan |
| `current-sprint/PLAN.md` | The only active execution plan, including the sprint id | Strategy changes, the hourly schedule |
| `current-sprint/CALENDAR.ics` | When work and known commitments sit in this sprint. Latest schedule | A new goal, proof of completion, a second copy of the whole plan |
| `current-sprint/REVIEW.md` | What happened. Created at close, not at start | A rewritten plan that hides misses |
| `sprints/sprint-NNN/` | Permanent archive of a closed sprint: plan, final calendar, review | The active sprint. Do not tidy these files to make history look cleaner |
| `PROGRESS_LOG.md` | Append-only index of what happened | Intentions, duplicated review essays |
| `DECISIONS.md` | Why a durable choice was made, including superseded choices | Current strategy in full (that lives in the master roadmap) |
| `context/PROFILE.md` | Owner-reported identity, skills, placement facts, inferences labeled as such | Dates or the working timezone (those live in `CURRENT_STATE.md`) |
| `context/CONSTRAINTS.md` | Limits and standing non-goals | A schedule |
| `context/GOALS.md` | What the owner wants and the phase *intents* they already stated | Attention bands or milestones (strategy) |
| `BACKLOG.md` | Near-term items that span tracks or have no track yet | A shadow roadmap |
| `<domain>/ROADMAP.md` | How that track produces outcomes, subordinate to the master | A new life-priority for that track |
| `gate/PREP_METHOD.md` | The method for executing GATE preparation (topic loop, resource rules, validation) | A syllabus, a resource list, or a plan change |
| `leetcode/MAINTENANCE_PLAN.md` | Same role as a domain roadmap: a recognition-first DSA progression (D-023) | A beginner or placement curriculum |
| `<domain>/PROGRESS.md` | Latest owner-reported progress and the metric rollup | A task list for next week |
| `<domain>/BACKLOG.md` | Near-term unscheduled work for that track | Every unfinished idea forever |
| `<domain>/RESOURCES.md` | Materials the owner has chosen | The model's recommended curriculum |
| `product/IDEAS.md` | Uncommitted ideas | Commitments (those become experiments or sprint outcomes) |
| `product/EXPERIMENTS.md` | Experiments actually run | Ideas not yet chosen |
| `product/VALIDATION.md` | What counts as evidence, and findings | A pitch |
| `beat-production/PRACTICE_LOG.md` | Append-only music practice and finished-piece notes (beats and songs). Folder name is historical | Strategy |
| `markets/READING.md` | Reading actually chosen or finished | An unsolicited syllabus |
| `markets/NOTES.md` | Working notes | A second progress file |
| `lseg/*` | Employer-specific facts and later notes | A generic engineering curriculum |
| `templates/*` | Blank forms, including the calendar guide | Filled-in plans or a live sprint calendar |
| `reviews/strategic/*` | Minutes of a strategy pass | A second master roadmap |
| `reviews/monthly/*` | Drift check | A quiet strategy rewrite |

There is no `CURRENT_SPRINT.md`. Do not recreate it.

`CURRENT_STATE.md` names the active sprint. It is not a pointer file you maintain beside the plan. While a sprint is open it should read:

```text
Active sprint: sprint-003
Plan: current-sprint/PLAN.md
Calendar: current-sprint/CALENDAR.ics
```

When none is open:

```text
Active sprint: none
```

After a review, before the next sprint is created, the closed sprint still occupies `current-sprint/`. State that. Do not call it active, and do not create a second directory:

```text
Active sprint: none
Awaiting archive: sprint-001
Plan: current-sprint/PLAN.md
Calendar: current-sprint/CALENDAR.ics
Review: current-sprint/REVIEW.md
```

## Conflict rules

1. Strategy disagrees across files → `MASTER_ROADMAP.md` wins. Fix the other file. Do not "split the difference".
2. What is true *now* disagrees → `CURRENT_STATE.md` wins, then fix the other file. Exception: if current state invents a phase the master roadmap does not have, the master wins and current state is wrong. Exception: if current state says there is no sprint but `current-sprint/PLAN.md` exists and `REVIEW.md` does not, the directory is the active sprint and current state is stale. Fix current state. Do not open another sprint.
3. Active tasks disagree → `current-sprint/PLAN.md` wins. The sprint id inside that file is the id. `CURRENT_STATE.md` must match it.
4. The calendar disagrees with the plan about what matters or what is in scope → the plan wins. Fix the calendar. More events do not raise a track's importance.
5. History disagrees → the archived sprint `REVIEW.md` wins for that sprint. Later corrections are appended. Do not silently rewrite a closed review, and do not rewrite an archived plan or calendar to make the record prettier.
6. A domain's claim on time disagrees with the master → the master wins.
7. Latest numbers disagree → the domain `PROGRESS.md` is the rollup. The review is the raw report from that date. If you update one, cite the other.
8. `DECISIONS.md` explains history. It is not a second strategy. If a decision entry is the newest word on a strategic question but the master roadmap was not updated, that is a bug: update the master, or mark the decision as proposed rather than accepted.
9. A standing non-goal in `context/CONSTRAINTS.md` stays in force until that file is updated. A decision entry alone does not cancel it. A strategic review that supersedes a constraint updates `CONSTRAINTS.md` and appends `DECISIONS.md` in the same pass.
10. Working dates and the working timezone live in `CURRENT_STATE.md`. If a date or timezone disagrees, current state wins.
11. A calendar event is not completion. `REVIEW.md` and the owner's report win. Do not mark an outcome done because its block was on the calendar.

## Words to use

| Word | Meaning |
| --- | --- |
| `unknown` | A fact the owner has not reported. Leave it unknown |
| `TBD` | A decision not yet made. Do not pretend it is made |
| `assumption` | A working belief. Label it, and say what would change it |
| `owner-reported` | The owner said this. Date it |
| `inference` | The model concluded this. Never store it as a fact |
| `skeleton` | The file exists on purpose, and the real content is not written yet |
| `primary` / `secondary` / `maintenance` / `paused` | Attention bands. Not percentages |
| `Light` / `Structured` / `Intensive` | Calendar density. Not a priority system |
| `closed` | Finished or deliberately dropped |

Do not use fake precision. "About half" is already a smell. Bands are the planning language. See decision D-005.

## Read sets

Read the smallest set that can do the job. Do not open the whole repo.

### Strategic review (normally Grok 4.7)

1. This file, strategic review section below
2. `MASTER_ROADMAP.md`
3. `CURRENT_STATE.md`
4. `context/PROFILE.md`
5. `context/CONSTRAINTS.md`
6. `context/GOALS.md`
7. `DECISIONS.md`
8. `templates/STRATEGIC_REVIEW_TEMPLATE.md`

Skim domain `ROADMAP.md` files only to avoid contradicting their purpose. Do not read resources, notes, old sprints, or empty backlogs. Do not read the calendar guide unless the owner asked the strategy pass to change how scheduling works.

While `MASTER_ROADMAP.md` is still a skeleton, this is also the read set for the first strategic pass. See the list of open questions already in the master roadmap. Do not invent answers to `unknown` facts. Decide around them, or mark them as blockers.

### Designing a sprint

Stop if the master roadmap status is `skeleton`. Do not invent priorities to fill a sprint. Tell the owner the strategic pass has to happen first. See decision D-004. Do not create `current-sprint/` in that case.

Otherwise read:

1. This file, sprint and calendar sections
2. `CURRENT_STATE.md`
3. `MASTER_ROADMAP.md` (read only)
4. `templates/CALENDAR_GUIDE.md`
5. The previous review, if one exists. That is `current-sprint/REVIEW.md` if the last sprint has not been archived yet, otherwise the latest `sprints/sprint-NNN/REVIEW.md`

Then, only for tracks the master roadmap currently marks `primary`, `secondary`, or (if you are including a maintenance task) `maintenance`:

6. That track's `ROADMAP.md` or `leetcode/MAINTENANCE_PLAN.md`. If GATE study is in the sprint, also read `gate/PREP_METHOD.md` before choosing GATE tasks or resources. Planning chooses GATE topics and resources; it must not generate GATE study notes — note creation is study-execution work defined in that file.
7. That track's `BACKLOG.md`, if it has one
8. That track's `PROGRESS.md`, if you need the latest evidence

Do not read other tracks "to be thorough". Do not read `RESOURCES.md` unless a chosen resource is required to write a concrete task or a calendar description.

If `current-sprint/PLAN.md` exists and `REVIEW.md` does not, a sprint is already active. Do not create another. Reschedule the calendar or review the sprint first.

### Reviewing a sprint

1. This file, the close section
2. `current-sprint/PLAN.md`
3. `current-sprint/CALENDAR.ics`, as the schedule that was in force, not as a log of what was done
4. `CURRENT_STATE.md`
5. `PROGRESS.md` for tracks the sprint actually touched

Ask the owner what happened if the conversation does not already say. Absence of a message is not completion. A calendar block is not completion.

### Logging a single completed thing outside a review

Read `CURRENT_STATE.md` and the relevant domain `PROGRESS.md`. Append to the practice log or experiment log if that is the right store. Add one line to `PROGRESS_LOG.md`. Do not open a new sprint for a single log entry. Do not add a calendar event to commemorate it.

## Edit permissions

### A sprint model may edit

- `current-sprint/PLAN.md` (create when a sprint starts)
- `current-sprint/CALENDAR.ics` (create with the plan; edit in place if the owner reschedules)
- `current-sprint/REVIEW.md` (create at close, not at start)
- The archive move: `current-sprint/` → `sprints/sprint-NNN/` when the next sprint is requested, after the review exists
- `CURRENT_STATE.md` (facts that changed, timezone if the owner changes it, sprint id and paths, last-review line)
- `PROGRESS_LOG.md` (append only)
- `DECISIONS.md` (append an execution decision that later sprints must respect; do not append strategy)
- `BACKLOG.md` and domain `BACKLOG.md`
- Domain `PROGRESS.md`, and the specialized logs (`PRACTICE_LOG.md`, `EXPERIMENTS.md`, `READING.md`, `NOTES.md`) when the owner reported something
- A domain `ROADMAP.md` only to record that an already-approved milestone is done, or to fix a factual error. Not to change scope or attention

### A sprint model must not edit

- `MASTER_ROADMAP.md`
- Attention bands, phase definitions, or success criteria anywhere
- `context/GOALS.md`, except to fix a misquote of the owner
- `templates/*`, except when the owner asks to improve a blank form
- Archived `sprints/sprint-NNN/PLAN.md` or `CALENDAR.ics`, except to fix a broken link elsewhere. Do not tidy them
- Closed sprint reviews, except to append a dated correction
- `CALENDAR.ics` at close, if the edit would make the schedule look like it was followed
- Any generator script, sync job, or shadow JSON/YAML calendar

### A strategic review may edit

- `MASTER_ROADMAP.md` (this is the main output)
- `DECISIONS.md` (append)
- `CURRENT_STATE.md` (phase label and priority summary only, so the snapshot matches the master)
- `reviews/strategic/YYYY-MM-DD.md` (create the minutes)
- Domain roadmaps only for a short "what this phase expects" pointer, if needed so they do not contradict the master. Do not dump a syllabus into them in the same pass unless the owner asked

A strategic review does not create the next sprint unless the owner asked for both.

## Create a sprint

Do this only when a new sprint is requested, and only after the master roadmap has left skeleton status, unless the owner explicitly overrides that.

1. If `current-sprint/` exists and has no `REVIEW.md`, stop. Review it first. There must never be two active sprints.
2. If `current-sprint/REVIEW.md` exists, archive that directory before creating anything new. Use the move in "Archive, then open the next sprint" below. The next id is the id inside that plan, plus one.
3. If `current-sprint/` does not exist, the next id is one higher than the highest `sprints/sprint-NNN/`, or `sprint-001` if none exist. Zero-pad to three digits. Do not skip or renumber.
4. Create `current-sprint/`. Copy `templates/SPRINT_TEMPLATE.md` to `current-sprint/PLAN.md`. Write the sprint id in the plan. The folder name stays `current-sprint/`.
5. Set dates. Default length is 10 calendar days, start and end inclusive. If you use a different length, write why in the plan.
6. Name the master phase and the attention band of each included track.
7. Choose a few outcomes that can be finished in this window under the capacity you actually know. If capacity is `unknown`, plan a small sprint and say so.
8. Every outcome needs a reason tied to the current phase, a definition of done that can be observed, and tasks. "Study X" is not a definition of done.
9. List what is deliberately not in the sprint, especially tracks that are `paused` or that lost a priority fight.
10. Stretch tasks are optional. Missing them is not a failure. Leave them off the calendar unless there is spare capacity.
11. State the calendar mode and why, plus known fixed commitments. Do not invent commitments.
12. Write `current-sprint/CALENDAR.ics` from `templates/CALENDAR_GUIDE.md`. The hourly schedule does not go in `PLAN.md`.
13. Update `CURRENT_STATE.md` to the active-sprint form. Do not create a pointer file.
14. Do not create `REVIEW.md` yet.
15. Do not add resources, books, or problem lists the owner has not accepted.

Prefer fewer outcomes. A sprint that finishes is more informative than a sprint that rehearses ambition.

## Generate the calendar

Read `templates/CALENDAR_GUIDE.md` and follow it. Short version, not a substitute for the guide:

- `PLAN.md` is what. `CALENDAR.ics` is when. The calendar cannot add scope or raise a priority.
- Mode is Light, Structured, or Intensive, as the plan states. Unknown capacity → Light. Intensive only with a named reason. Never Intensive just to fill the grid.
- Work-event titles are concise (`GATE — DBMS PYQ Set`). Descriptions carry purpose, what to do, and the definition of done for that block. Do not paste the whole plan into every event.
- Protect breaks, buffers, meals, free time, and wind-down when the mode includes them. A buffer is not catch-up time.
- Timezone comes from `CURRENT_STATE.md` (`Asia/Kolkata` until that file changes). `TZID` on timed `DTSTART` and `DTEND`. UTC `DTSTAMP`. Stable UIDs. CRLF. RFC 5545 escaping.
- Every meaningful work event maps to a plan outcome or task. Not every task needs an event.
- Do not write a script to do this.

## Mid-sprint calendar changes

Real life will move. If the owner asks to reschedule:

- Edit `current-sprint/CALENDAR.ics` in place
- Keep the same UID for a moved block. Increment `SEQUENCE`
- Keep sprint goals unless the owner is explicitly changing scope
- Do not treat a moved block as failure
- Do not rewrite `PLAN.md` because Tuesday moved to Wednesday
- Do not pour missed work into `Rest / Buffer` or `Free Time`
- Do not keep `CALENDAR-v2.ics` or any other parallel schedule. Git history is the earlier version
- A manual Google Calendar import does not sync. If only a few events change, update them manually there and in `CALENDAR.ics`. Verify duplicate handling before re-importing the whole file. See [templates/CALENDAR_GUIDE.md](templates/CALENDAR_GUIDE.md)

If the calendar repeatedly cannot fit the plan, leave that for the review. Do not silently shrink the plan to match a pretty week, and do not silently grow the calendar to absorb every unfinished task.

## Close a sprint

1. Read `current-sprint/PLAN.md`.
2. Ask or use what the owner actually reported. Read `CALENDAR.ics` only as the schedule that was in force.
3. Create `current-sprint/REVIEW.md` from `templates/SPRINT_REVIEW_TEMPLATE.md`.
4. For each planned outcome: `completed`, `partial`, or `not done`. If the owner did not say, `not reported`. A calendar event is not a completed outcome. Fixed commitments are not achievements.
5. Update domain progress from real evidence, not from the plan or the calendar.
6. Append a short `PROGRESS_LOG.md` entry that links to the review using its eventual permanent path, `sprints/sprint-NNN/REVIEW.md`, even though the file is still at `current-sprint/REVIEW.md`. Write the link this way once. The archive move makes it valid without any later edit, which keeps the log append-only. Do not paste the review in.
7. Update `CURRENT_STATE.md`: active sprint `none`, this id awaiting archive, paths still under `current-sprint/`.
8. For every unfinished item: `carry`, `change`, or `delete`. Default is not carry. Name the destination of anything carried. Do not turn leftovers into extra calendar blocks.
9. Do not alter `CALENDAR.ics` to pretend the original schedule was followed.
10. Do not edit `PLAN.md` after the fact to match what happened.
11. Fill in the escalate line. Most reviews escalate nothing.
12. Leave `current-sprint/` where it is until the next sprint is requested.

## Archive, then open the next sprint

When a new sprint is requested, and a reviewed `current-sprint/` is in the way:

1. Read the sprint id from `current-sprint/PLAN.md`. The destination is `sprints/` plus that id.
2. If `sprints/sprint-NNN/` already exists, stop. Do not overwrite it and do not invent a new id.
3. Move the whole directory in one step. Prefer `git mv current-sprint sprints/sprint-NNN` so history follows. If the files are not tracked, `mv current-sprint sprints/sprint-NNN`. Do not copy and leave the original.
4. Confirm `current-sprint/` is gone and the destination contains `PLAN.md`, `CALENDAR.ics`, and `REVIEW.md`. If the move failed, stop. Do not create a new `current-sprint/`.
5. Only then create the new `current-sprint/` using "Create a sprint".
6. Update `CURRENT_STATE.md` to the new active sprint. Do not edit the `PROGRESS_LOG.md` entry for the sprint you just moved. It was written with the permanent path at close, so the move has already made it valid.

The archived calendar is the final schedule that was in force. Do not regenerate it during the move.

## Update domain progress

- Update progress from evidence, not from the plan or the calendar.
- Cite the sprint review or the dated owner report you are trusting.
- Baselines are `unlogged` until the owner reports them. Do not write zero. See decision D-012.
- Music sessions go in `beat-production/PRACTICE_LOG.md` first. Beats and vocals both count. `PROGRESS.md` holds counts and current focus, derived from the log.
- Product experiments go in `product/EXPERIMENTS.md`. Ideas that were not run stay in `IDEAS.md`.
- Markets notes are not progress. If understanding changed, say so in `markets/PROGRESS.md` in the owner's words, or mark it as the model's summary of owner-reported reading.
- Do not increase a metric because it would be motivating to do so.

## Record a decision

Append to `DECISIONS.md`. Do not rewrite old entries. If a decision replaces another, add a new id and mark the old one `superseded`. Do not follow the body of a superseded decision. D-014's old line "do not schedule by hour" is not in force. D-004's old mention of `CURRENT_SPRINT.md` is not a reason to recreate that file. The no-sprint-until-strategy rule in D-004 still stands.

Use a new id when a later sprint would otherwise relitigate the choice. Do not log ordinary task completion.

Strategic decisions are accepted only inside a strategic review, then reflected in `MASTER_ROADMAP.md` in the same pass. An execution model may append a *proposed* decision, clearly marked `proposed`, and escalate. Proposed is not in force.

Minimum fields: id, date, status, owner of the decision (strategic review or execution), decision, why, what it changes, what it supersedes.

## When to escalate to Grok

Escalate to a strategic review when any of these are true:

- The owner asks to change direction, add a track, or drop a track
- A phase boundary arrived: GATE is done, an internship is offered or started, a joining date is fixed, a track's reason disappeared
- The current phase cannot be executed as written (not "a task slipped" — the phase itself is wrong)
- The same primary outcome has failed for reasons of priority or scope, not a single bad estimate
- An internship or other new obligation would pause a primary track
- Success-by-joining needs to be redefined
- A monthly review finds drift between how time is actually going and the bands in the master roadmap

Do not escalate because a task was unfinished, a block moved, a mock score was disappointing, or a piece of music came out badly. Those are sprint dispositions or practice. Record them and continue.

How to escalate: write the reason in the sprint review or monthly review. Do not edit `MASTER_ROADMAP.md` in that same edit. Stop and hand the strategic read set to Grok, unless the owner explicitly told this model to perform the strategy change itself. If they did, still use `templates/STRATEGIC_REVIEW_TEMPLATE.md`, still append a decision, and note that the owner directed a non-Grok strategy edit.

## Monthly review

About once a month, not instead of sprint reviews. Copy `templates/MONTHLY_REVIEW_TEMPLATE.md` to `reviews/monthly/YYYY-MM.md`.

Compare the last sprints to the master phase. Look for a track that is eating time it was not given, a primary track that is being starved, or backlog debt. Either conclude "strategy still holds" or escalate. Do not quietly rewrite the master roadmap here.

Calendar density is not evidence of importance. A track with more events is not a track that won a priority fight.

## Anti-hallucination

These are hard rules:

- Do not mark work complete unless the owner said it was done, or an artifact they produced is in the repo or linked
- Do not treat a calendar event as proof the work happened
- Do not invent mock scores, revenue, user counts, music finish counts, chapters read, or problems solved
- Do not invent a weekly hour budget, a GATE score target, a revenue target, or a joining team
- Do not invent classes, labs, exams, interviews, travel, or other fixed commitments
- Do not add books, courses, problem lists, or product ideas to repo files unless the owner asked or explicitly accepted a suggestion. Suggestions stay in the chat until then
- Do not backfill logs with a plausible history
- Do not describe an inference as something the owner said
- If a file is empty, it is empty. Do not "helpfully" flesh out a curriculum during a sprint edit
- If you do not know, write `unknown` or `not reported`
- Do not create extra tracks
- Do not create a second active sprint, a pointer file, or a calendar-generator script

## Backlog rules

- Domain backlogs are near-term unscheduled work, roughly the next three sprints. They are not a second roadmap
- Longer-range work is a milestone on the domain roadmap, or it is deleted
- Root `BACKLOG.md` is only for items that span tracks or have no track. If it belongs to one track, move it
- A review that carries an item must name its destination. "Keep in backlog" with no reason is how debt accumulates
- When a backlog item is done, delete it or move one line to progress. Do not leave a growing graveyard of checked boxes. The history is the sprint review and `PROGRESS_LOG.md`
- Carried work does not automatically become calendar blocks in the next sprint

## First-run state (historical, 2026-09-27)

The skeleton condition below was true at scaffolding and was lifted the same day by the first strategic review. Do not treat the roadmap as a skeleton. Current phase and bands: `CURRENT_STATE.md` and `MASTER_ROADMAP.md`.

- No sprint exists. `current-sprint/` does not exist. Do not create it, and do not create `sprint-001`, unless the owner asks
- No goal progress has been logged. Do not treat that as a zero baseline
- Resource files are intentionally empty
- Working calendar timezone is `Asia/Kolkata`, recorded in `CURRENT_STATE.md`

## Copying templates

Copy the template to the destination path and fill it in there. Do not fill in the file under `templates/`. After copying, set status, dates, and links. Remove `FILL:` markers you have answered. Leave `TBD` or `unknown` where the answer does not exist. The calendar is not a copy of a template. Write it from the guide.
