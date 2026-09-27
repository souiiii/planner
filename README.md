# Planner

Personal planning repo for September 2026 through LSEG joining, around August 2027.

This is a set of Markdown files plus a sprint calendar, not an app. More than one AI model will read and update it over about eleven months. The structure exists so those models share one strategy, one picture of the present, and one active 10-day sprint — instead of each inventing a new plan.

## Horizon

Roughly 2026-09-27 → around August 2027. Joining date and exam date are approximate. Canonical dates and the working timezone: [CURRENT_STATE.md](CURRENT_STATE.md).

## Goals

Intents, not the ranking. Ranking lives in [MASTER_ROADMAP.md](MASTER_ROADMAP.md).

| Track | What you want |
| --- | --- |
| [GATE](gate/ROADMAP.md) | A serious backup attempt around February 2027, then largely drop it |
| [System design](system-design/ROADMAP.md) | Backend and production depth, using the Node/TypeScript stack you already know |
| [Product](product/ROADMAP.md) | A real attempt at independent software income, through small validated experiments |
| [Music](beat-production/ROADMAP.md) | Rap-first music-making: beats, vocals, and finished songs. A personal craft, not a career plan |
| [Markets](markets/ROADMAP.md) | Slow practical understanding of markets. Personally interesting, also relevant to LSEG |
| [LeetCode](leetcode/MAINTENANCE_PLAN.md) | Stay sharp. Not another placement grind |

[lseg/](lseg/README.md) is notes about the employer. It is not a seventh goal and not a second software curriculum.

Who you are, what you refuse to do, and the goal writeups: [context/PROFILE.md](context/PROFILE.md), [context/CONSTRAINTS.md](context/CONSTRAINTS.md), [context/GOALS.md](context/GOALS.md).

## Hierarchy

```text
MASTER ROADMAP
      ↓
DOMAIN ROADMAPS
      ↓
current-sprint/
   PLAN.md          what this 10 days is for
   CALENDAR.ics     when to work on that
      ↓
REVIEW.md           what actually happened
      ↓
archive the whole directory
      ↓
sprints/sprint-NNN/
      ↓
fresh current-sprint/
```

A domain file cannot decide that its track gets half your time. That decision belongs to the master roadmap.

The calendar cannot decide it either. More events do not make a track more important. `PLAN.md` is the sprint. `CALENDAR.ics` is only the schedule. How to write one: [templates/CALENDAR_GUIDE.md](templates/CALENDAR_GUIDE.md).

Sprints are global. There are no per-track sprint folders, and there is never a second active sprint. The open sprint is the `current-sprint/` directory. Its number lives inside `PLAN.md`, not in the folder name.

## Which file wins

| Question | Authoritative file |
| --- | --- |
| What is the strategy? | [MASTER_ROADMAP.md](MASTER_ROADMAP.md) |
| What is true right now, including which sprint is active? | [CURRENT_STATE.md](CURRENT_STATE.md) |
| What should this sprint accomplish? | `current-sprint/PLAN.md` |
| When should that work happen? | `current-sprint/CALENDAR.ics`, subordinate to the plan |
| What happened in the sprint just closed, before it is archived? | `current-sprint/REVIEW.md` |
| What happened in an archived sprint? | `sprints/sprint-NNN/REVIEW.md` |
| Why was a durable choice made? | [DECISIONS.md](DECISIONS.md) |
| What happened, in order? | [PROGRESS_LOG.md](PROGRESS_LOG.md) — index only; detail stays in reviews |

There is no pointer file. If `CURRENT_STATE.md` and `current-sprint/PLAN.md` disagree about the sprint id, fix current state to match the plan. Do not open a second sprint to resolve it.

Operating rules for humans and models: [AI_WORKFLOW.md](AI_WORKFLOW.md).

## Workflow

1. Strategy changes only in a strategic review. That is normally Grok 4.7. See [templates/STRATEGIC_REVIEW_TEMPLATE.md](templates/STRATEGIC_REVIEW_TEMPLATE.md).
2. Execution is one 10-day sprint in `current-sprint/`. The plan says what. The calendar says when. One sprint covers every track that is active.
3. At the end, write `REVIEW.md` in that same directory. For each unfinished item, carry it, change it, or delete it. Do not copy the whole list forward. Do not edit the calendar to pretend the schedule was followed. The `PROGRESS_LOG.md` entry is written once, with the permanent path `sprints/sprint-NNN/REVIEW.md`, so the later archive move never requires rewriting the append-only log.
4. When the next sprint starts, move the whole `current-sprint/` directory to `sprints/sprint-NNN/`, then create a fresh `current-sprint/`. Archived sprints stay put. They are not rewritten to look cleaner.
5. Record what happened. Do not record intentions, or calendar events, as progress.

Monthly and strategic writeups go in [reviews/](reviews/README.md). Sprint reviews do not.

## Where to put something new

| You have… | Put it in |
| --- | --- |
| A fact about the present (date, phase label, which sprint is active, capacity) | [CURRENT_STATE.md](CURRENT_STATE.md) |
| A change of strategy | strategic review, then master roadmap + [DECISIONS.md](DECISIONS.md) |
| Outcomes for the current 10 days | `current-sprint/PLAN.md` |
| A change to when you will do that work | `current-sprint/CALENDAR.ics` |
| Proof that something was finished | sprint `REVIEW.md`, then that domain's `PROGRESS.md`, then one line in [PROGRESS_LOG.md](PROGRESS_LOG.md) |
| Near-term work with no sprint slot yet | that domain's `BACKLOG.md`, or [BACKLOG.md](BACKLOG.md) if it spans tracks |
| A book, course, or tool you have actually chosen | that domain's `RESOURCES.md` |
| A product idea you have not committed to | [product/IDEAS.md](product/IDEAS.md) |

Empty resource and idea files mean "none chosen yet", not "fill me with suggestions".

## Status of this repo

Scaffolded on 2026-09-27. First strategy adopted the same day: phase `gate-window`. No sprint has been started. `current-sprint/` does not exist yet, on purpose. No progress on the goals has been logged, and absence of a log is not a claim that prior knowledge is zero.

If this paragraph disagrees with [CURRENT_STATE.md](CURRENT_STATE.md), current state wins.

## Next step

The strategy exists. The next useful pass is domain planning for the current primary and secondary tracks (GATE, system design, product), using [MASTER_ROADMAP.md](MASTER_ROADMAP.md) as the constraint. Do not create `current-sprint/` or `sprint-001` unless you explicitly ask. Do not turn those passes into syllabi the master roadmap refused to write.
