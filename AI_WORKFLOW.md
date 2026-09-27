# AI workflow

> **Role:** operating manual for any model editing this repo.
> **Authority:** authoritative for procedure. It is not a plan, a status file, or a decision log.
> **Last reviewed:** 2026-09-27

You are one of several models that will touch this repo between now and about August 2027. Read this before editing. Do not rely on memory of an older plan. The files are the plan.

"You" in the rest of this repo usually means the owner. In this file, **the model** means whichever AI is about to edit, and **the owner** means the human.

## Roles

| Work | Who |
| --- | --- |
| Master strategy, phase changes, success definition | Normally Grok 4.7, via a strategic review |
| 10-day sprint plans and reviews | Any capable model, following this file |
| Domain progress updates from owner-reported work | The model that just ran the review, or a model the owner asked to log something |
| Implementation of a product or technical project | A coding agent, usually in another repo. Link the result from here. Do not turn this repo into the codebase |

A sprint-planning model must not "improve" the strategy while it is scheduling 10 days.

## Authority map

File headers repeat this. If a header and this table disagree, the header wins, then fix this table.

| File | What it owns | What it must not contain |
| --- | --- | --- |
| `MASTER_ROADMAP.md` | Current strategy: phases, attention bands, milestones, deliberate non-goals, success by joining | Task lists, daily schedules, topic syllabi, live metrics |
| `CURRENT_STATE.md` | Snapshot of the present: dates, phase *label*, active tracks, capacity, last review, unknown facts | A second copy of the strategy, a task list |
| `CURRENT_SPRINT.md` | Pointer to the active sprint folder, plus status | A copy of the plan |
| `sprints/sprint-NNN/PLAN.md` | The only active execution plan | Strategy changes |
| `sprints/sprint-NNN/REVIEW.md` | Immutable-enough record of that sprint | A rewritten plan that hides misses |
| `PROGRESS_LOG.md` | Append-only index of what happened | Intentions, duplicated review essays |
| `DECISIONS.md` | Why a durable choice was made, including superseded choices | Current strategy in full (that lives in the master roadmap) |
| `context/PROFILE.md` | Owner-reported identity, skills, placement facts, inferences labeled as such | Dates that can change (those live in `CURRENT_STATE.md`) |
| `context/CONSTRAINTS.md` | Limits and standing non-goals | A schedule |
| `context/GOALS.md` | What the owner wants and the phase *intents* they already stated | Attention bands or milestones (strategy) |
| `BACKLOG.md` | Near-term items that span tracks or have no track yet | A shadow roadmap |
| `<domain>/ROADMAP.md` | How that track produces outcomes, subordinate to the master | A new life-priority for that track |
| `leetcode/MAINTENANCE_PLAN.md` | Same role as a domain roadmap, for maintenance rather than learning | A beginner or placement curriculum |
| `<domain>/PROGRESS.md` | Latest owner-reported progress and the metric rollup | A task list for next week |
| `<domain>/BACKLOG.md` | Near-term unscheduled work for that track | Every unfinished idea forever |
| `<domain>/RESOURCES.md` | Materials the owner has chosen | The model's recommended curriculum |
| `product/IDEAS.md` | Uncommitted ideas | Commitments (those become experiments or sprint outcomes) |
| `product/EXPERIMENTS.md` | Experiments actually run | Ideas not yet chosen |
| `product/VALIDATION.md` | What counts as evidence, and findings | A pitch |
| `beat-production/PRACTICE_LOG.md` | Append-only practice and finished-beat notes | Strategy |
| `markets/READING.md` | Reading actually chosen or finished | An unsolicited syllabus |
| `markets/NOTES.md` | Working notes | A second progress file |
| `lseg/*` | Employer-specific facts and later notes | A generic engineering curriculum |
| `templates/*` | Blank forms | Filled-in plans |
| `reviews/strategic/*` | Minutes of a strategy pass | A second master roadmap |
| `reviews/monthly/*` | Drift check | A quiet strategy rewrite |

## Conflict rules

1. Strategy disagrees across files → `MASTER_ROADMAP.md` wins. Fix the other file. Do not "split the difference".
2. What is true *now* disagrees → `CURRENT_STATE.md` wins, then fix the other file. Exception: if current state invents a phase the master roadmap does not have, the master wins and current state is wrong.
3. Active tasks disagree → `sprints/sprint-NNN/PLAN.md` for the sprint named by `CURRENT_SPRINT.md` wins.
4. History disagrees → the sprint `REVIEW.md` wins for that sprint. Later corrections are appended. Do not silently rewrite a closed review.
5. A domain's claim on time disagrees with the master → the master wins.
6. Latest numbers disagree → the domain `PROGRESS.md` is the rollup. The review is the raw report from that date. If you update one, cite the other.
7. `DECISIONS.md` explains history. It is not a second strategy. If a decision entry is the newest word on a strategic question but the master roadmap was not updated, that is a bug: update the master, or mark the decision as proposed rather than accepted.
8. A standing non-goal in `context/CONSTRAINTS.md` stays in force until that file is updated. A decision entry alone does not cancel it. A strategic review that supersedes a constraint updates `CONSTRAINTS.md` and appends `DECISIONS.md` in the same pass.
9. Working dates live in `CURRENT_STATE.md`. Other files may quote the original owner wording. If a date disagrees, current state wins.

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

Skim domain `ROADMAP.md` files only to avoid contradicting their purpose. Do not read resources, notes, old sprints, or empty backlogs.

While `MASTER_ROADMAP.md` is still a skeleton, this is also the read set for the first strategic pass. See the list of open questions already in the master roadmap. Do not invent answers to `unknown` facts. Decide around them, or mark them as blockers.

### Designing a sprint

Stop if the master roadmap status is `skeleton`. Do not invent priorities to fill a sprint. Tell the owner the strategic pass has to happen first. See decision D-004.

Otherwise read:

1. This file, sprint sections
2. `CURRENT_STATE.md`
3. `MASTER_ROADMAP.md` (read only)
4. `CURRENT_SPRINT.md`
5. The previous sprint's `REVIEW.md`, if one exists

Then, only for tracks the master roadmap currently marks `primary`, `secondary`, or (if you are including a maintenance task) `maintenance`:

6. That track's `ROADMAP.md` or `leetcode/MAINTENANCE_PLAN.md`
7. That track's `BACKLOG.md`, if it has one
8. That track's `PROGRESS.md`, if you need the latest evidence

Do not read other tracks "to be thorough". Do not read `RESOURCES.md` unless a chosen resource is required to write a concrete task.

### Reviewing a sprint

1. This file, review section
2. That sprint's `PLAN.md`
3. `CURRENT_STATE.md`
4. `PROGRESS.md` for tracks the sprint actually touched

Ask the owner what happened if the conversation does not already say. Absence of a message is not completion.

### Logging a single completed thing outside a review

Read `CURRENT_STATE.md` and the relevant domain `PROGRESS.md`. Append to the practice log or experiment log if that is the right store. Add one line to `PROGRESS_LOG.md`. Do not open a new sprint for a single log entry.

## Edit permissions

### A sprint model may edit

- `sprints/sprint-NNN/PLAN.md` (create the next plan)
- `sprints/sprint-NNN/REVIEW.md` (create at close, not at start)
- `CURRENT_SPRINT.md` (pointer and status only)
- `CURRENT_STATE.md` (facts that changed, last-review line, sprint pointer summary)
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
- Closed sprint reviews, except to append a dated correction

### A strategic review may edit

- `MASTER_ROADMAP.md` (this is the main output)
- `DECISIONS.md` (append)
- `CURRENT_STATE.md` (phase label and priority summary only, so the snapshot matches the master)
- `reviews/strategic/YYYY-MM-DD.md` (create the minutes)
- Domain roadmaps only for a short "what this phase expects" pointer, if needed so they do not contradict the master. Do not dump a syllabus into them in the same pass unless the owner asked

A strategic review does not create the next sprint unless the owner asked for both.

## Create a sprint

1. Confirm the master roadmap is not a skeleton. Confirm there is no open sprint. If a sprint is still active, review it first.
2. Copy `templates/SPRINT_TEMPLATE.md` to `sprints/sprint-NNN/PLAN.md`. Next id is the previous id plus one, zero-padded to three digits. Do not skip or renumber. Convention: [sprints/README.md](sprints/README.md).
3. Set dates. Default length is 10 calendar days, start and end inclusive. If you use a different length, write why in the plan.
4. Name the master phase and the attention band of each included track.
5. Choose a few outcomes that can be finished in this window under the capacity you actually know. If capacity is `unknown`, plan a small sprint and say so. Never write an hour-by-hour calendar.
6. Every outcome needs a reason tied to the current phase, a definition of done that can be observed, and tasks. "Study X" is not a definition of done.
7. List what is deliberately not in the sprint, especially tracks that are `paused` or that lost a priority fight.
8. Stretch tasks are optional. Missing them is not a failure.
9. Update `CURRENT_SPRINT.md` so it points at this folder. Set status to `active`. Update the sprint line in `CURRENT_STATE.md`.
10. Do not create `REVIEW.md` yet.
11. Do not add resources, books, or problem lists the owner has not accepted.

Prefer fewer outcomes. A sprint that finishes is more informative than a sprint that rehearses ambition.

## Review a sprint

Write the review before writing the next plan. Copy `templates/SPRINT_REVIEW_TEMPLATE.md` to `sprints/sprint-NNN/REVIEW.md`.

1. For each planned outcome: `completed`, `partial`, or `not done`. Use the owner's report. If they did not say, status is `not reported`, not `completed`.
2. For every unfinished task: `carry`, `change`, or `delete`. Default is not carry. Carry only if it is still the right work and still fits the phase. Delete work that was speculative or that lost its reason. Record where a carried item went (next plan, or domain backlog).
3. Lessons: what to change about estimation or approach. Do not convert a slip into a strategy change.
4. Metrics: record only numbers the owner reported or artifacts that exist. Otherwise write `not measured`. Update domain `PROGRESS.md` from those reports, and cite this review.
5. Append a short entry to `PROGRESS_LOG.md` with a link to the review. Do not paste the review in.
6. Update `CURRENT_STATE.md` last-review line, and any fact that actually changed.
7. Set the sprint status to `closed` in `CURRENT_SPRINT.md` if no new sprint is opened in the same session. If you open the next sprint immediately after, point `CURRENT_SPRINT.md` at the new plan.
8. Fill in the escalate line. Most reviews escalate nothing.

Do not edit `PLAN.md` after the fact to match what happened. The gap between plan and review is the point.

## Update domain progress

- Update progress from evidence, not from the plan.
- Cite the sprint review or the dated owner report you are trusting.
- Baselines are `unlogged` until the owner reports them. Do not write zero. See decision D-012.
- Beat sessions go in `beat-production/PRACTICE_LOG.md` first. `PROGRESS.md` holds counts and current focus, derived from the log.
- Product experiments go in `product/EXPERIMENTS.md`. Ideas that were not run stay in `IDEAS.md`.
- Markets notes are not progress. If understanding changed, say so in `markets/PROGRESS.md` in the owner's words, or mark it as the model's summary of owner-reported reading.
- Do not increase a metric because it would be motivating to do so.

## Record a decision

Append to `DECISIONS.md`. Do not rewrite old entries. If a decision replaces another, add a new id and mark the old one `superseded`.

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

Do not escalate because a task was unfinished, a mock score was disappointing, or a beat was bad. Those are sprint dispositions or practice. Record them and continue.

How to escalate: write the reason in the sprint review or monthly review. Do not edit `MASTER_ROADMAP.md` in that same edit. Stop and hand the strategic read set to Grok, unless the owner explicitly told this model to perform the strategy change itself. If they did, still use `templates/STRATEGIC_REVIEW_TEMPLATE.md`, still append a decision, and note that the owner directed a non-Grok strategy edit.

## Monthly review

About once a month, not instead of sprint reviews. Copy `templates/MONTHLY_REVIEW_TEMPLATE.md` to `reviews/monthly/YYYY-MM.md`.

Compare the last sprints to the master phase. Look for a track that is eating time it was not given, a primary track that is being starved, or backlog debt. Either conclude "strategy still holds" or escalate. Do not quietly rewrite the master roadmap here.

## Anti-hallucination

These are hard rules:

- Do not mark work complete unless the owner said it was done, or an artifact they produced is in the repo or linked
- Do not invent mock scores, revenue, user counts, beat counts, chapters read, or problems solved
- Do not invent a weekly hour budget, a GATE score target, a revenue target, or a joining team
- Do not add books, courses, problem lists, or product ideas to repo files unless the owner asked or explicitly accepted a suggestion. Suggestions stay in the chat until then
- Do not backfill logs with a plausible history
- Do not describe an inference as something the owner said
- If a file is empty, it is empty. Do not "helpfully" flesh out a curriculum during a sprint edit
- If you do not know, write `unknown` or `not reported`
- Do not create extra tracks

## Backlog rules

- Domain backlogs are near-term unscheduled work, roughly the next three sprints. They are not a second roadmap
- Longer-range work is a milestone on the domain roadmap, or it is deleted
- Root `BACKLOG.md` is only for items that span tracks or have no track. If it belongs to one track, move it
- A review that carries an item must name its destination. "Keep in backlog" with no reason is how debt accumulates
- When a backlog item is done, delete it or move one line to progress. Do not leave a growing graveyard of checked boxes. The history is the sprint review and `PROGRESS_LOG.md`

## First-run state (as of 2026-09-27)

- Master roadmap is a skeleton. No attention bands have been assigned
- No sprint exists. Do not create `sprint-001` until a strategic review has written the master roadmap, unless the owner explicitly overrides that
- No goal progress has been logged. Do not treat that as a zero baseline
- Resource files are intentionally empty

## Copying templates

Copy the template to the destination path and fill it in there. Do not fill in the file under `templates/`. After copying, set status, dates, and links. Remove `FILL:` markers you have answered. Leave `TBD` or `unknown` where the answer does not exist.
