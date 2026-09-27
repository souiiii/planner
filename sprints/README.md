# Sprints

> **Role:** convention for global 10-day execution.
> **Authority:** authoritative for naming and folder rules. The active pointer is [CURRENT_SPRINT.md](../CURRENT_SPRINT.md). The active plan is `sprint-NNN/PLAN.md`.
> **Last reviewed:** 2026-09-27

Sprints integrate every track that is currently active. Do not create `gate/sprints`, `product/sprints`, or any other per-track sprint tree. Decision D-001.

## Naming

```text
sprints/sprint-001/PLAN.md
sprints/sprint-001/REVIEW.md
sprints/sprint-002/PLAN.md
sprints/sprint-002/REVIEW.md
```

- Ids start at `001` and increase by one
- Zero-pad to three digits
- Do not skip numbers
- Do not renumber
- Do not encode the date in the folder name. Dates go in `PLAN.md`
- A gap in calendar dates is fine. An id gap is not

About thirty sprints fit in this scheme if the horizon is continuous. Fewer is more likely. Do not pre-create them.

## Length

Default is 10 calendar days, start and end inclusive. Example shape: 2026-10-01 through 2026-10-10. A different length must be written in that plan, with the reason. Decision D-014.

Do not build an hourly schedule inside a sprint.

## What each folder contains

| File | When it exists |
| --- | --- |
| `PLAN.md` | Created when the sprint starts. Not edited afterward to hide misses |
| `REVIEW.md` | Created when the sprint closes. Not created at the start |

Copy from [templates/SPRINT_TEMPLATE.md](../templates/SPRINT_TEMPLATE.md) and [templates/SPRINT_REVIEW_TEMPLATE.md](../templates/SPRINT_REVIEW_TEMPLATE.md).

## Opening and closing

Procedure: [AI_WORKFLOW.md](../AI_WORKFLOW.md).

Closed sprints stay in place. There is no archive folder. [PROGRESS_LOG.md](../PROGRESS_LOG.md) links to reviews so you do not need a second index. If this directory listing and the log disagree, the folders and the review files win; fix the log.

## First sprint

Do not create `sprint-001` while the master roadmap is a skeleton. Decision D-004.

## Current

The active sprint is whatever [CURRENT_SPRINT.md](../CURRENT_SPRINT.md) points at. Do not keep a second "current sprint" line here.
