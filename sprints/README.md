# Sprints

> **Role:** convention for archived global sprints, and for how a sprint gets here.
> **Authority:** naming and archive rules. The active sprint, when one exists, is the directory `current-sprint/` at the repo root. It is not a file in this folder.
> **Which sprint is active:** stated in [CURRENT_STATE.md](../CURRENT_STATE.md) and inside that sprint's `PLAN.md`. Those two must match. There is no pointer file.
> **Last reviewed:** 2026-09-27

Sprints integrate every track that is currently active. Do not create `gate/sprints`, `product/sprints`, or any other per-track sprint tree. Decision D-001. Where the open sprint lives is decision D-016.

## Lifecycle

```text
current-sprint/
├── PLAN.md
├── CALENDAR.ics
└── REVIEW.md          created only at close

        move the whole directory once, when the next sprint starts

sprints/sprint-001/
├── PLAN.md
├── CALENDAR.ics
└── REVIEW.md
```

Then create a fresh `current-sprint/` for the next id.

There is never more than one active sprint. `current-sprint/` is that sprint. This folder holds sprints that have already been closed and archived.

If no sprint has been created yet, `current-sprint/` does not exist. Do not add it as a placeholder.

## Naming

Archived folders:

```text
sprints/sprint-001/
sprints/sprint-002/
sprints/sprint-003/
```

- Ids start at `001` and increase by one
- Zero-pad to three digits
- Do not skip numbers
- Do not renumber
- Do not encode the date in the folder name. The id and the dates live in `PLAN.md`
- The active directory is always `current-sprint/`, never `current-sprint-003/` or `sprints/sprint-003/` while it is still open
- A gap in calendar dates is fine. An id gap is not

About thirty sprints fit in this scheme if the horizon is continuous. Fewer is more likely. Do not pre-create them.

## What a sprint contains

| File | While active (`current-sprint/`) | After archive (`sprints/sprint-NNN/`) |
| --- | --- | --- |
| `PLAN.md` | Created at start. Holds the sprint id. Not edited later to hide misses | The plan as it stood. Do not tidy it |
| `CALENDAR.ics` | Created at start. Latest schedule. Edit in place if life moves | The final schedule that was in force, including mid-sprint edits. Not a rewritten "what I actually did" calendar |
| `REVIEW.md` | Absent until close | The review. Append a dated correction if needed. Do not silently rewrite it |

Copy plans and reviews from [templates/SPRINT_TEMPLATE.md](../templates/SPRINT_TEMPLATE.md) and [templates/SPRINT_REVIEW_TEMPLATE.md](../templates/SPRINT_REVIEW_TEMPLATE.md). Write the calendar using [templates/CALENDAR_GUIDE.md](../templates/CALENDAR_GUIDE.md).

The hourly schedule does not go in `PLAN.md`.

## Length

Default is 10 calendar days, start and end inclusive. A different length must be written in that plan, with the reason. Decision D-017, which keeps this rule from D-014.

## Opening, closing, archiving

Procedure: [AI_WORKFLOW.md](../AI_WORKFLOW.md).

Close writes `REVIEW.md` and leaves the directory at `current-sprint/` until the next sprint is requested. The archive step is a move of the whole directory, not a copy, and it happens before the new `current-sprint/` is created.

After that move, the archived folder stays put. There is no `sprints/archive/` and no second move. Do not rewrite an archived sprint to make the history look cleaner. Decision D-016.

[PROGRESS_LOG.md](../PROGRESS_LOG.md) links to reviews. Do not keep a second index in this file. If a link still points at `current-sprint/REVIEW.md` after the move, fix the link. Do not fix history by editing the review.

## First sprint

Do not create `sprint-001`, and do not create `current-sprint/`, while the master roadmap is a skeleton. Decision D-004.

## Current

Look at [CURRENT_STATE.md](../CURRENT_STATE.md). Do not keep a second "current sprint" line here.
