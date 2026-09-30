# Decisions

> **Authority:** append-only log of durable choices and why they were made.
> **Current strategy** still lives in [MASTER_ROADMAP.md](MASTER_ROADMAP.md), once that file leaves skeleton status. This log is history and rationale, not a second roadmap.
> **Update rule:** append a new id. Never rewrite an accepted decision in place. Mark it `superseded` and point at the new id. A superseded decision is history. Follow the newer id, not the old body.
> **Last reviewed:** 2026-09-30

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
- Status: superseded by D-016
- Decided by: scaffolding
- Decision: Folders are `sprints/sprint-001/`, zero-padded to three digits. Dates live inside `PLAN.md`. Do not skip ids, do not renumber, do not move closed sprints into an archive folder. A date gap between sprints is allowed. An id gap is not.
- Why: About thirty sprints are likely. Dates slip; ids should not. Moving folders breaks links from the progress log.
- Changes: No `sprints/archive/`. Reviews sit beside plans as `REVIEW.md`.
- Supersedes: none

### D-003 — Current sprint file is a pointer

- Date: 2026-09-27
- Status: superseded by D-016
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
- Status: superseded by D-023
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
- Status: superseded by D-017
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

### D-016 — The active sprint is the `current-sprint/` directory

- Date: 2026-09-27
- Status: accepted
- Decided by: owner instruction
- Decision: While a sprint is open, `current-sprint/` is the sprint. It holds `PLAN.md` and `CALENDAR.ics`. `REVIEW.md` is added only at close. The sprint id is written inside `PLAN.md`, not in the folder name. There is no `CURRENT_SPRINT.md`. `CURRENT_STATE.md` states the active id and the paths. When the next sprint is requested, the whole `current-sprint/` directory is moved to `sprints/sprint-NNN/` and a new `current-sprint/` is created. There is never a second active sprint. After that move, the archived folder is permanent evidence: do not renumber it, do not skip ids, and do not rewrite it to make history look cleaner. There is still no `sprints/archive/` folder. If no sprint has been created, `current-sprint/` does not exist. Do not create a placeholder.
- Why: A pointer file was a second place to look, and a second place to get wrong. The owner wants the active directory itself to be the sprint, and the archive to be a move of that directory, not a copy.
- Changes: `CURRENT_SPRINT.md` is deleted. Open work is not filed under `sprints/` until the next sprint starts. D-001 remains accepted: one integrated sprint, no per-domain sprint folders. The sentence in D-001 that called `sprints/` the only execution tree is no longer how the open sprint is stored. D-004 remains accepted: do not create `current-sprint/` or `sprint-001` while the master roadmap is a skeleton, unless the owner overrides that.
- Supersedes: D-002, D-003

### D-017 — `CALENDAR.ics` is part of the sprint, and it does not set priorities

- Date: 2026-09-27
- Status: accepted
- Decided by: owner instruction
- Decision: Every real sprint has a valid iCalendar file, `CALENDAR.ics`, written by the planning model from `templates/CALENDAR_GUIDE.md`. No generator script. The plan says what; the calendar says when; the calendar is subordinate to the plan. Mode is Light, Structured, or Intensive, named in the plan. Intensive is not the default and is not chosen just because the grid can be filled. Working timezone is `Asia/Kolkata` until `CURRENT_STATE.md` says otherwise. Mid-sprint, edit the one calendar file in place. At close, do not alter it to pretend the schedule was followed. The archived file is the final schedule that was in force. Default sprint length remains 10 calendar days, start and end inclusive, unless that plan writes a different length and the reason. Do not silently stretch to 14 days. Do not put the hourly schedule in `PLAN.md`. Do not treat every free hour as work.
- Why: The owner already plans with importable calendars and wants that in the sprint, without turning the calendar into a second strategy or a claim that the work was done.
- Changes: Calendar guide and sprint templates. `CURRENT_STATE.md` records `Asia/Kolkata` as the working calendar timezone. City remains unknown.
- Supersedes: D-014

### D-018 — Two phases until joining: gate-window, then post-gate

- Date: 2026-09-27
- Status: accepted
- Decided by: strategic review
- Decision: The horizon has two phases. `gate-window` runs from 2026-09-27 until the GATE exam day (around February 2027, exact day unknown) or an explicit withdrawal. `post-gate` runs from the next day until LSEG joining, around August 2027. Bands, yield order, the meaning of a serious GATE attempt, the system-design arc, the product kill rule, the internship contingency, and success by joining are in `MASTER_ROADMAP.md`. In short: during gate-window, GATE is primary, system design and product are secondary, and beats, markets, and LeetCode are maintenance. After the exam, GATE closes after a short close-out, system design and product are primary, beats and markets are secondary, and LeetCode stays maintenance. No time is reserved for an internship that does not exist. A GATE result does not by itself retarget the career plan. No score, revenue, beat, or problem quota was set.
- Why: GATE is a temporary backup priority, not the career. The other intents have to survive the exam window without becoming a second exam or being dropped. Capacity and several facts are unknown, so the plan uses bands and a yield order instead of a timetable. Splitting system design and the income attempt into the post-exam window, while keeping both alive before it, is what "comfortably paced" and "do not secretly build for six months" can both survive.
- Changes: `MASTER_ROADMAP.md` is no longer a skeleton. `CURRENT_STATE.md` phase label is `gate-window`. Domain attention lines point here. No sprint was created.
- Supersedes: none

### D-019 — Existing stack is the default, not a ban

- Date: 2026-09-27
- Status: accepted
- Decided by: strategic review (owner instruction)
- Decision: JavaScript / TypeScript, Node.js, Express, React / Next.js, SQL, and MongoDB are the default practical foundation, because you already know them. Use them where they are sufficient. Do not switch stack for variety. A domain plan may use another language, database, infrastructure tool, or framework when the system or the learning objective genuinely benefits. Write that reason in the domain plan. An ordinary deviation does not need a strategic review. Changing the default for the whole horizon does.
- Why: A hard stack ban would block useful learning. A free choice of stack would become the framework tour you already refused. The default keeps engineering work on ground you know, without pretending every system is best built there.
- Changes: `context/CONSTRAINTS.md` stack section. Pointers in `context/PROFILE.md`, `context/GOALS.md`, and `system-design/ROADMAP.md`.
- Supersedes: none. Replaces the previous stack wording in `context/CONSTRAINTS.md`, which read as a harder restriction.

### D-020 — The master sets priority, timing, and role; domain passes set milestones and methods

- Date: 2026-09-27
- Status: accepted
- Decided by: owner instruction (cleanup after the first strategic review)
- Decision: The master roadmap decides priority, phase timing, broad role, broad maturity target, and interaction between streams. It does not decide detailed milestones, learning sequence, evidence thresholds, output cadence, implementation counts, or domain-specific teaching structure beyond the owner's stated preferences. Domain planners define those inside the master's bounds. The master may still state a guardrail taken from the owner's constraints (for example: no long private product builds, finished work over tutorials, no placement grind). Study method, kill timing, breadth boundaries, and finish cadence belong to the domain plan.
- Why: The first pass wrote some detail that the domain passes should own. Delegating it keeps the master stable, stops it from becoming a curriculum, and avoids over-constraining later domain planning.
- Changes: `MASTER_ROADMAP.md` cleanup (GATE preparation checklist, system-design phase balance and implementation count, product kill timing, beat finish cadence, markets competency enumeration loosened or removed). `product/ROADMAP.md` and `product/VALIDATION.md` pointers updated. Phases, bands, yield order, stack rule, and goals unchanged.
- Supersedes: none

### D-021 — The music stream is broader than beat production

- Date: 2026-09-27
- Status: accepted
- Decided by: owner instruction (strategic amendment)
- Decision: The stream previously called beat production is music-making. Mainly rap, with some melodic attempts. The target is finished music that sounds convincing and impressive to the owner, not knowledge of DAW tools. Making full songs over existing beats counts as valid progress. Recording, vocal processing, vocal mixing, beat tweaking and arrangement, and integrating vocals into a finished record are core parts of the stream. Beat-making, sampling, and chopping still matter as one part of it. It remains a personal craft: not a career, audience-growth, or monetization goal. No gear-buying requirement. Phase structure, attention bands (maintenance in gate-window, secondary in post-gate), and folder structure are unchanged; `beat-production/` stays the folder name.
- Why: The goal changed from making instrumentals to making finished music. Framing the stream as beats only would under-plan the vocal and song side and misread progress.
- Changes: `MASTER_ROADMAP.md` stream section, tables, yield order, success, and non-goals. `context/GOALS.md` goal 4. `context/CONSTRAINTS.md` creative constraint. `README.md` track table. `beat-production/ROADMAP.md`, `PROGRESS.md`, `PRACTICE_LOG.md`, `RESOURCES.md`. `CURRENT_STATE.md` track row and unknown facts. `AI_WORKFLOW.md` log wording. `templates/CALENDAR_GUIDE.md` example title. Strategic minutes amendment appended.
- Supersedes: none. Broadens the stream named in D-011; the no-career, no-audience, no-monetization rule in D-011 remains in force. Detailed learning sequence, resources, DAW choice, milestones, and practice cadence remain for the domain-planning pass.

### D-022 — GATE paper and target reconciled into the master

- Date: 2026-09-28
- Status: accepted
- Decided by: owner instruction (non-Grok strategy edit; owner-directed exception to D-015)
- Decision: Record the owner-stated GATE CS/IT paper and AIR < 400 target for PSU optionality in `MASTER_ROADMAP.md`, and remove the stale "no score target" / paper-unknown wording.
- Why: The owner explicitly asked for this reconciliation. The paper and target were owner-stated 2026-09-27 and already in `gate/ROADMAP.md`, but the master still said "no score target" and treated the paper as unknown.
- Changes: `MASTER_ROADMAP.md` attention row, GATE stream, success-by-joining, non-goals exception, assumptions, unresolved, changelog. `CURRENT_STATE.md` track status and next planning action (Stage 0 light setup only, no diagnostic; execution waits for sprint-001). `gate/ROADMAP.md` reconciliation note and explicit Stage 1 section note bundle. Phases, attention bands, yield order, and other non-goals unchanged.
- Supersedes: none. Clarifies wording left by D-018/D-020 without changing phases or bands.

### D-023 — LeetCode is a recognition-improvement track, not maintenance-only

- Date: 2026-09-28
- Status: accepted
- Decided by: owner instruction (non-Grok strategy edit; owner-directed exception per D-015)
- Decision: The LeetCode/DSA goal is substantially better recognition on unseen problems — read an unfamiliar problem, interpret its constraints, identify possible approaches, choose or derive the right one, and implement it — progressing toward FAANG-level interview questions. `leetcode/MAINTENANCE_PLAN.md` remains the domain plan and keeps its file name for stability; it is now an ability-gated learning progression (practice pool → review of actual misses → cold revisits → minimally primed fresh questions → harder unseen problems → interview level), with no quotas, rating targets, or dates. Weak areas still come only from actual misses. Attention bands (maintenance in both phases) and yield order are unchanged. A beginner course, a placement grind, and a numbered sheet remain refused.
- Why: The owner's goal exceeds "stay fluent". Maintenance alone would not build the recognition skill, and the flagged conflict between the master's maintenance-only wording and the domain plan needed reconciling rather than leaving the plan marked as not in force.
- Changes: `MASTER_ROADMAP.md` attention rows, LeetCode stream, success by joining, decisions header, and changelog. `DECISIONS.md`: D-009 marked superseded. `CURRENT_STATE.md` track row. `leetcode/MAINTENANCE_PLAN.md` conflict section replaced with a reconciliation note; `leetcode/PROGRESS.md` strategy note updated. `AI_WORKFLOW.md` authority-map row updated. No band, yield-order, or quota change; no sprint or calendar created.
- Supersedes: D-009

### D-024 — LeetCode uses pool + company questions in parallel, ~50/50 by attempts

- Date: 2026-09-29
- Status: accepted
- Decided by: execution (owner instruction)
- Decision: From Sprint 001 onward, LeetCode practice draws roughly half its attempts from the existing shuffled 92-question pool (kept in order, never regrouped or cherry-picked) and roughly half from genuine company OA/interview questions as fresh-transfer practice. 50/50 is counted by attempts within the sprint's LeetCode work, not by sprint time. Both sources share the same attempt protocol, logging, failure taxonomy, and cold-revisit rules. Company questions may start in Sprint 001; no pool consolidation is required first. Sources must be credible actual/reported material; leaked or confidential active-assessment material, cheating tools, answer dumps, and bypass-oriented sources are refused.
- Why: The old "pool first, company after M2" sequencing delayed transfer practice the goal depends on. Parallel practice exercises recognition on both calibrated and fresh material from the start; M1 still records the full pool pass as evidence.
- Changes: `leetcode/MAINTENANCE_PLAN.md` (parallel-sources section, ladder framing), `leetcode/PROGRESS.md` (current-stage wording, transfer metric), `leetcode/ATTEMPTS.md` (pool/company id scheme). No master, band, milestone, or goal change.
- Supersedes: the "pool first, company later" sequencing only. D-023 remains in force.

### D-025 — Pool questions are drawn randomly from remaining unseen; no fixed consumption order

- Date: 2026-09-29
- Status: accepted
- Decided by: execution (owner instruction)
- Decision: The 92-question pool is a candidate pool, not a sequence. Whenever a sprint selects pool questions, they are drawn randomly from the remaining unseen pool questions — by ID only, blind to pattern, topic, difficulty, company tags, or intended technique. The selector must not inspect hidden metadata, answer keys, or pattern labels to influence the draw. Previously attempted questions are excluded from the fresh draw unless explicitly scheduled as cold revisits. Randomness serves anti-priming and variety, not difficulty balancing: never cherry-pick, rebalance, or replace a drawn question for looking too hard or too easy. The ~50/50 pool/company split by attempts (D-024) is unchanged, and M1 still requires all 92 eventually attempted.
- Why: Treating the shuffled list as a fixed consumption order front-loads whatever the shuffle happened to place first (here, two Hards) and invites prefix-preservation habits. Random blind draws keep every slice pattern-neutral.
- Changes: `leetcode/MAINTENANCE_PLAN.md` (draw rule in pool section and 50/50 bullet), `leetcode/SPRINT_001_PREP.md` (pool side reselected as random draw P1 + P87; fixed-order language removed). `leetcode/PROGRESS.md` needed no sequencing correction. No method, milestone, band, or strategy change.
- Supersedes: the "kept in order" pool-consumption wording in D-024. D-023 and the rest of D-024 remain in force.

### D-026 — Open Source Contribution is a durable track

- Date: 2026-09-30
- Status: accepted
- Decided by: strategic review, explicitly owner-directed non-Grok edit under D-015. Minutes: [2026-09-30](reviews/strategic/2026-09-30.md).
- Decision: Add `opensource/` as a real track: maintenance in gate-window, secondary post-gate. Build a long-term habit of useful contributions in a small number of healthy repositories. Restart the contribution workflow, not programming; use the existing JS/TS/Node/React background. Capability, useful work, and learning from review are the evidence, not PR counts or guaranteed merges.
- Why: The owner explicitly wants to become a recurring useful contributor, including repository navigation, scoped fixes, validation, and maintainer collaboration. Neither product work nor employer notes substitutes for this goal.
- Changes: Master track tables, yield rules, internship contingency, and success direction; current state, goals, constraints, README, and workflow integration; five Open Source domain files. Contribution code stays in separate checkouts, with evidence linked here, consistent with D-013. Selected Piyush Garg sections are persisted at the owner's explicit request under D-006; Sprint 001 prep remains proposal pending owner acceptance. No sprint or calendar is created.
- Supersedes: none. Extends D-018's track set and adds an owner-authorized track within the no-invented-tracks constraint. Existing phases, other bands, and the rest of D-018/D-019/D-020 remain in force.

### D-027 — One integrated sprint does not require every active track

- Date: 2026-09-30
- Status: accepted
- Decided by: execution (explicit owner-directed consistency clarification; no strategy change)
- Decision: Keep one integrated sprint and no per-domain sprints. Track inclusion follows `MASTER_ROADMAP.md` bands and yield rules, actual capacity, and accepted candidate prep. An active track or accepted prep does not guarantee inclusion in a particular sprint. Record deliberate omissions and their reasons; the master's phase-level continuity requirements still apply.
- Why: D-001's original inclusion wording conflicts with the master's allowance for omitted maintenance tracks and would overfill a sprint when capacity is limited or unknown.
- Changes: `AI_WORKFLOW.md`, `README.md`, and `sprints/README.md` inclusion wording reconciled. Existing sprint templates already allow deliberate omissions. No phase, attention band, domain design, or Open Source scope/resource change; no sprint created.
- Supersedes: only D-001's requirement to cover every active track. Its one-integrated-sprint/no-per-domain-sprints rule remains in force; D-016 still governs the execution directories. D-001 is retained unchanged as history. D-026 is unchanged.

### D-028 — Sprint 001 is a moderate Structured sprint; unknown hours alone do not force Light/sparse

- Date: 2026-09-30
- Status: superseded by D-029
- Decided by: execution (owner instruction 2026-09-30; no strategy change)
- Decision: For Sprint 001 only, plan a moderate workload, not an intentionally minimal/light sprint. Use `Structured` calendar mode unless a concrete constraint makes that unrealistic. Unknown exact weekly hours, by itself, is not a reason to produce an extremely sparse Sprint 001. Still leave meaningful slack and do not fill the whole day. GATE remains primary; System Design and Product remain secondary. Seriously consider small but real continuity slices for LeetCode, Music, and Open Source rather than omitting them merely because they are maintenance; their inclusion stays subordinate to the master priorities and must not expand into equal-priority tracks. Consider Markets as well, but it may yield more readily if the integrated plan becomes crowded. Accepted domain prep remains candidate input, not a requirement to consume its full scope: for example, LeetCode's 12 accepted questions are a candidate pool, not a Sprint 001 quota.
- Why: The owner explicitly requested a moderate Structured Sprint 001. The existing `unknown capacity → Light/small` defaults would otherwise force a minimal sprint from unknown hours alone, which is not what the owner wants for this sprint.
- Changes: `AI_WORKFLOW.md` (Sprint 001 exception to the unknown-capacity small-sprint and Light defaults), `templates/CALENDAR_GUIDE.md` and `templates/SPRINT_TEMPLATE.md` (same exception), `CURRENT_STATE.md` (capacity exception pointer and next-planning-action pointer to this decision). No master, band, yield-order, roadmap, resource, or accepted-prep change; no sprint created.
- Supersedes: none. Sprint-001-scoped clarification of how to apply the unknown-capacity defaults. D-027, prior capacity wording, and all bands remain in force for other sprints.

### D-029 — Moderate Structured is the universal default; labeled 09:00–22:30 days

- Date: 2026-09-30
- Status: accepted
- Decided by: execution (owner instruction 2026-09-30; no strategy change)
- Decision: For all future sprints unless the owner later changes this or a concrete exceptional circumstance requires another mode: default to a moderate `Structured` sprint. Unknown exact weekly hours alone must not force an extremely sparse or `Light` sprint. `Light` remains available when there is a real reason; `Intensive` remains reserved for genuine short high-pressure periods such as an exam, interview, or deadline. Always follow the current `MASTER_ROADMAP.md` priorities and yield rules; this preference does not make tracks equal priority. Maintenance tracks still receive serious consideration for small real continuity work rather than being discarded mechanically for being maintenance; inclusion still depends on the current phase, actual conflicts, domain progress, and master yield rules. Accepted prep is candidate input, not a quota. Normal sprint calendar days run 09:00–22:30: no study/work before 09:00 or after 22:30 without an explicit per-day owner override; lunch 13:00–14:00 and dinner 19:30–20:30 are explicit events. Within 09:00–22:30 every period is visibly labeled (work, fixed commitment, or protected Break / Buffer / Free Time / Rest / Transition / Wind Down); no anonymous gaps. Slack exists as protected labeled blocks, never hidden catch-up; missed work never auto-consumes them. Block descriptions stay task-specific with no forced template. While the college final-year project remains active, reserve a reasonable amount of calendar-only time for it in each normal sprint. A generic `College Project` label is sufficient; `— Planning` or `— Work` may be used when useful. No separate categories, fixed count, or fixed duration are required. These are only time reservations; the planner does not manage the project or invent its content. Owner-reported fixed commitment 2026-10-08 10:00–12:00 Lab quiz is recorded in `CURRENT_STATE.md` and must be reserved with no overlapping work; no other class timetable is inferred.
- Why: The owner universalized the moderate Structured style beyond Sprint 001 and supplied concrete daily-window, labeling, college-project, and lab-quiz rules. D-028's Sprint-001-only scope would otherwise leave future sprints on the old sparse default and leave days partially unlabeled.
- Changes: `SPRINT_PLANNING_METHOD.md` (universal default, daily window, labeled window, college-project blocks), `AI_WORKFLOW.md`, `templates/CALENDAR_GUIDE.md`, `templates/SPRINT_TEMPLATE.md`, and `CURRENT_STATE.md` (capacity default, known commitments including the lab quiz) updated to D-029. No band, phase, roadmap, or resource change; no sprint created.
- Supersedes: D-028's Sprint-001-only scope. D-028 is retained as history; its intent is preserved here in universal form. D-027 remains in force.
