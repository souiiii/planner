# Planner

Personal planning repo for September 2026 through LSEG joining, around August 2027.

This is a set of Markdown files, not an app. More than one AI model will read and update it over about eleven months. The structure exists so those models share one strategy, one picture of the present, and one active 10-day sprint — instead of each inventing a new plan.

## Horizon

Roughly 2026-09-27 → around August 2027. Joining date and exam date are approximate. Canonical dates: [CURRENT_STATE.md](CURRENT_STATE.md).

## Goals

Intents, not a ranked plan. Ranking is **not decided yet**. It will live in [MASTER_ROADMAP.md](MASTER_ROADMAP.md).

| Track | What you want |
| --- | --- |
| [GATE](gate/ROADMAP.md) | A serious backup attempt around February 2027, then largely drop it |
| [System design](system-design/ROADMAP.md) | Backend and production depth, using the Node/TypeScript stack you already know |
| [Product](product/ROADMAP.md) | A real attempt at independent software income, through small validated experiments |
| [Beat production](beat-production/ROADMAP.md) | Sampled beatmaking as a craft. Finished beats, not a career plan |
| [Markets](markets/ROADMAP.md) | Slow practical understanding of markets. Personally interesting, also relevant to LSEG |
| [LeetCode](leetcode/MAINTENANCE_PLAN.md) | Stay sharp. Not another placement grind |

[lseg/](lseg/README.md) is notes about the employer. It is not a seventh goal and not a second software curriculum.

Who you are, what you refuse to do, and the goal writeups: [context/PROFILE.md](context/PROFILE.md), [context/CONSTRAINTS.md](context/CONSTRAINTS.md), [context/GOALS.md](context/GOALS.md).

## Hierarchy

```text
MASTER_ROADMAP.md             strategy: phases, attention, milestones, non-goals
        |
domain roadmaps               what each track is trying to produce
        |
sprints/sprint-NNN/PLAN.md    the only active task list (all tracks, one sprint)
        |
sprints/sprint-NNN/REVIEW.md  what actually happened
```

A domain file cannot decide that its track gets half your time. That decision belongs to the master roadmap.

Sprints are global. There are no per-track sprint folders.

## Which file wins

| Question | Authoritative file |
| --- | --- |
| What is the strategy? | [MASTER_ROADMAP.md](MASTER_ROADMAP.md) |
| What is true right now? | [CURRENT_STATE.md](CURRENT_STATE.md) |
| Which sprint is active, and where is the plan? | [CURRENT_SPRINT.md](CURRENT_SPRINT.md) — a pointer, not a copy of the plan |
| What should be done in the active sprint? | `sprints/sprint-NNN/PLAN.md` |
| What happened in a closed sprint? | that sprint's `REVIEW.md` |
| Why was a durable choice made? | [DECISIONS.md](DECISIONS.md) |
| What happened, in order? | [PROGRESS_LOG.md](PROGRESS_LOG.md) — index only; detail stays in reviews |

Operating rules for humans and models: [AI_WORKFLOW.md](AI_WORKFLOW.md).

## Workflow

1. Strategy changes only in a strategic review. That is normally Grok 4.7. See [templates/STRATEGIC_REVIEW_TEMPLATE.md](templates/STRATEGIC_REVIEW_TEMPLATE.md).
2. Execution runs in 10-day sprints under [sprints/](sprints/README.md). One sprint covers every track that is active, not six competing sprint files.
3. At the end, write a review. For each unfinished item, carry it, change it, or delete it. Do not copy the whole list forward.
4. Record what happened. Do not record intentions as progress.

Closed sprints stay in `sprints/sprint-NNN/`. They are not moved to an archive. Monthly and strategic writeups go in [reviews/](reviews/README.md).

## Where to put something new

| You have… | Put it in |
| --- | --- |
| A fact about the present (date, phase label, sprint pointer, capacity) | [CURRENT_STATE.md](CURRENT_STATE.md) |
| A change of strategy | strategic review, then master roadmap + [DECISIONS.md](DECISIONS.md) |
| Work for the current 10 days | the active sprint `PLAN.md` |
| Proof that something was finished | sprint `REVIEW.md`, then that domain's `PROGRESS.md`, then one line in [PROGRESS_LOG.md](PROGRESS_LOG.md) |
| Near-term work with no sprint slot yet | that domain's `BACKLOG.md`, or [BACKLOG.md](BACKLOG.md) if it spans tracks |
| A book, course, or tool you have actually chosen | that domain's `RESOURCES.md` |
| A product idea you have not committed to | [product/IDEAS.md](product/IDEAS.md) |

Empty resource and idea files mean "none chosen yet", not "fill me with suggestions".

## Status of this repo

Scaffolded on 2026-09-27. Master roadmap is a skeleton. No sprint has been started. No progress on the goals has been logged, and absence of a log is not a claim that prior knowledge is zero.

If this paragraph disagrees with [CURRENT_STATE.md](CURRENT_STATE.md), current state wins.

## Next step

The next task is a first strategic pass by Grok 4.7. It should read only:

1. [AI_WORKFLOW.md](AI_WORKFLOW.md) — strategic review section
2. [MASTER_ROADMAP.md](MASTER_ROADMAP.md)
3. [CURRENT_STATE.md](CURRENT_STATE.md)
4. [context/PROFILE.md](context/PROFILE.md)
5. [context/CONSTRAINTS.md](context/CONSTRAINTS.md)
6. [context/GOALS.md](context/GOALS.md)
7. [DECISIONS.md](DECISIONS.md)
8. [templates/STRATEGIC_REVIEW_TEMPLATE.md](templates/STRATEGIC_REVIEW_TEMPLATE.md)

That pass writes strategy. It should not become a topic-by-topic curriculum, and it should not create `sprint-001` unless you explicitly ask.
