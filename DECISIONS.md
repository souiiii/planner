# Decisions

> **Authority:** append-only log of durable choices and why they were made.
> **Current strategy** still lives in [MASTER_ROADMAP.md](MASTER_ROADMAP.md), once that file leaves skeleton status. This log is history and rationale, not a second roadmap.
> **Update rule:** append a new id. Never rewrite an accepted decision in place. Mark it `superseded` and point at the new id.
> **Last reviewed:** 2026-09-27

Execution models may append execution decisions. Strategic decisions (priorities, phases, success definition) are accepted only in a strategic review. A sprint model may append a `proposed` decision and escalate; proposed is not in force.

## How to add one

```text
### D-NNN — short title
- Date:
- Status: accepted | proposed | superseded by D-NNN
- Decided by: strategic review | execution | scaffolding
- Decision:
- Why:
- Changes:
- Supersedes: none
```

Ids are never reused.

## Log

### D-001 — One integrated sprint, no per-domain sprint folders

- Date: 2026-09-27
- Status: accepted
- Decided by: scaffolding (owner instruction)
- Decision: Execution is a single 10-day sprint covering every track that is active. Domain folders hold roadmaps, progress, and near-term backlogs. They do not contain `sprints/` directories.
- Why: Separate domain sprints would compete and drift. The owner asked for one integrated sprint.
- Changes: `sprints/` is the only execution tree.
- Supersedes: none

### D-002 — Sprint ids are sequential and folders stay put

- Date: 2026-09-27
- Status: accepted
- Decided by: scaffolding
- Decision: Folders are `sprints/sprint-001/`, zero-padded to three digits. Dates live inside `PLAN.md`. Do not skip ids, do not renumber, do not move closed sprints into an archive folder. A date gap between sprints is allowed. An id gap is not.
- Why: About thirty sprints are likely. Dates slip; ids should not. Moving folders breaks links from the progress log.
- Changes: No `sprints/archive/`. Reviews sit beside plans as `REVIEW.md`.
- Supersedes: none

### D-003 — Current sprint file is a pointer

- Date: 2026-09-27
- Status: accepted
- Decided by: scaffolding
- Decision: `CURRENT_SPRINT.md` only identifies the active sprint. The plan is not copied there.
- Why: Two copies of the active plan will diverge.
- Changes: none beyond the pointer file.
- Supersedes: none

### D-004 — No sprint until a master strategy exists

- Date: 2026-09-27
- Status: accepted
- Decided by: scaffolding
- Decision: Do not create `sprint-001` while `MASTER_ROADMAP.md` has status `skeleton`, unless the owner explicitly overrides this.
- Why: The first sprint would otherwise invent priorities. The next planned task is the strategic pass, not execution.
- Changes: `CURRENT_SPRINT.md` stays at status `none` for now.
- Supersedes: none

### D-005 — Attention is bands, not percentages

- Date: 2026-09-27
- Status: accepted
- Decided by: scaffolding
- Decision: When strategy is written, each track gets `primary`, `secondary`, `maintenance`, or `paused`. Do not assign percentage shares of a week.
- Why: Percentages look exact and rot. Bands are enough to stop a domain plan from claiming half of life. Bands have not been assigned yet. Assigning them is a strategic-review job.
- Changes: Master roadmap table left as TBD.
- Supersedes: none

### D-006 — Do not commit resources or ideas the owner has not accepted

- Date: 2026-09-27
- Status: accepted
- Decided by: scaffolding
- Decision: Books, courses, problem lists, tools, and product ideas stay out of repo files until the owner asks for them or explicitly accepts a suggestion. Suggestions belong in the conversation until then. An empty `RESOURCES.md` or `IDEAS.md` means none chosen.
- Why: Otherwise every model leaves a shadow curriculum behind, and the shadow becomes the plan.
- Changes: Resource and idea files start empty on purpose.
- Supersedes: none

### D-007 — Unfinished work is not carried automatically

- Date: 2026-09-27
- Status: accepted
- Decided by: scaffolding (owner instruction)
- Decision: At sprint review, every unfinished item is marked `carry`, `change`, or `delete`. The default is not carry. Carried work must name its destination.
- Why: Automatic carry creates backlog debt and a fake sense that old plans are still binding.
- Changes: Required section in the sprint review template.
- Supersedes: none

### D-008 — Backlogs are near-term only

- Date: 2026-09-27
- Status: accepted
- Decided by: scaffolding
- Decision: A backlog item should be schedulable within about three sprints. Longer-range work belongs in a roadmap milestone, or it is deleted. Root `BACKLOG.md` is only for cross-track items or items with no track yet.
- Why: Backlogs become second roadmaps if they can hold anything.
- Changes: Domain backlog files state this rule.
- Supersedes: none

### D-009 — LeetCode is a maintenance plan, not a learning roadmap

- Date: 2026-09-27
- Status: accepted
- Decided by: scaffolding (owner instruction)
- Decision: `leetcode/MAINTENANCE_PLAN.md` is the domain plan. Do not create a beginner DSA curriculum or a placement-grind sheet.
- Why: The owner already knows DSA and explicitly rejected a restart of placement prep.
- Changes: No `leetcode/ROADMAP.md`, on purpose.
- Supersedes: none

### D-010 — LSEG folder is not a goal track

- Date: 2026-09-27
- Status: accepted
- Decided by: scaffolding (owner instruction)
- Decision: `lseg/` holds employer context: internship notes, joining prep, questions, later learnings. It does not get an attention band. It must not become a second software-engineering curriculum. Keep it lightweight until there is something real to put there.
- Why: Joining LSEG is the horizon, not a separate study program to invent now.
- Changes: Placeholder files only.
- Supersedes: none

### D-011 — Beat production is not career optimization

- Date: 2026-09-27
- Status: accepted
- Decided by: scaffolding (owner instruction)
- Decision: Beat production is a serious creative practice. Do not attach placement value, audience targets, income targets, or "transferable skills" framing unless the owner later asks. Finished beats and practiced techniques are the point. Tutorial time is not the metric.
- Why: The owner was explicit that this passion should not be converted into another optimization project.
- Changes: Domain files and metrics follow that rule.
- Supersedes: none

### D-012 — Unlogged progress is not zero

- Date: 2026-09-27
- Status: accepted
- Decided by: scaffolding
- Decision: Domain progress baselines are `unlogged`, not `0`. Do not write zero scores, zero chapters, or zero problems as if a measurement happened. Existing skill reported in the profile is real and unmeasured.
- Why: Zero would erase prior DSA and software experience, and would invite models to "catch up" from a false start.
- Changes: Progress files start at unlogged.
- Supersedes: none

### D-013 — This repo does not become the code repo

- Date: 2026-09-27
- Status: accepted
- Decided by: scaffolding
- Decision: Product and system-design implementations live in their own repositories unless the owner wants an exception. This repo stores the plan, the link, and a short note about what the project was for.
- Why: Mixing app code into the planning repo makes the plan harder for later models to read and invites an unplanned application.
- Changes: `system-design/projects/README.md` explains links-only.
- Supersedes: none

### D-014 — Default sprint length is 10 calendar days

- Date: 2026-09-27
- Status: accepted
- Decided by: scaffolding
- Decision: A sprint is 10 calendar days, start and end inclusive, unless that sprint's plan writes a different length and the reason. Do not silently stretch to 14 days. Do not schedule by hour.
- Why: The owner asked for approximately 10-day sprints and rejected fake full-day productivity schedules.
- Changes: Stated in `sprints/README.md` and the sprint template.
- Supersedes: none

### D-015 — Strategy edits only happen in a strategic review

- Date: 2026-09-27
- Status: accepted
- Decided by: scaffolding (owner instruction)
- Decision: `MASTER_ROADMAP.md` is edited only during a strategic review. That review is normally done by Grok 4.7. Another model may do it only when the owner explicitly asks for a strategy change, and must still use the strategic review template, append a decision, and say that the owner directed the exception. Sprint planning must not slip strategic edits into a plan.
- Why: Context drift across models will otherwise rewrite priorities a paragraph at a time.
- Changes: Edit rule is in the master roadmap header and in [AI_WORKFLOW.md](AI_WORKFLOW.md).
- Supersedes: none
