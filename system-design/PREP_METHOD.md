# System design preparation method

> **Role:** the permanent operating guide for how System Design is learned and practiced in this repo. Method, not plan.
> **Not a roadmap, not a sprint plan, not a syllabus, and not a resource list.** Stages, sequence, and gates live in [ROADMAP.md](ROADMAP.md). This file governs how the learning inside that roadmap is actually done.
> **Audience:** every sprint planner and study assistant that touches System Design work. Read this before choosing tasks or resources.
> **Objective:** better engineering thinking and better use of system-design ideas — not memorized architectures, and not implementation volume.
> **Status:** active
> **Last reviewed:** 2026-09-29

## 1. The goal is design judgment

The product of this track is the ability to:

- take unfamiliar requirements and identify the constraints that actually matter;
- produce multiple reasonable designs, not one remembered diagram;
- explain the trade-offs between them — failure modes, operational cost, complexity, scale, consistency, latency;
- choose one and defend the choice from the stated requirements;
- revise it when assumptions or constraints change.

Not the goal:

- memorizing architectures or standard interview diagrams;
- writing lots of implementation code;
- term familiarity or syllabus completion;
- interview-format drills. Interview competence is a later consequence of genuine design judgment, not the format to optimize for now (see [ROADMAP.md](ROADMAP.md)).

Your existing JavaScript/TypeScript, Node, and SQL/Mongo experience is familiar grounding: use it for examples, scenarios, and probes. Do not re-teach basic application development.

## 2. Requirements and constraints before components

- Every design starts from a brief: users, traffic shape, data shape, scale, latency, consistency, cost, operational constraints. Separate hard constraints from preferences, and label invented assumptions.
- **No component enters without a stated problem it solves.** Never add a cache, queue, database, load balancer, or replication because it is "standard." For each one, say what it buys, what it costs, and what new failure mode it introduces.
- Reason in this order: **requirements → alternatives → trade-offs → decision.** Jumping straight to one architecture is not a design decision.
- Always compare at least two viable options — including the simpler or boring one (single machine, one database) when it is genuinely viable.
- Explicitly reason about failure modes, operational cost, complexity, scale, consistency, and latency — whichever constraints the brief makes relevant.

## 3. The depth bar

A concept is learned when you can say:

- when it applies, and why it helps;
- what it costs — complexity, operations, money, failure surface;
- when it is the wrong choice, with a concrete counter-case;
- how it behaves under failure and at the scale the brief states.

A concept you can only name, or only apply in the one example you saw, is not learned.

## 4. The default learning loop

Run this loop per concept (or tightly related concept cluster), inside the stages of [ROADMAP.md](ROADMAP.md):

1. **Learn the concept** from the chosen primary teaching resource, at the depth bar in section 3.
2. **See good worked examples and case studies** — how experienced engineers applied it, and what they rejected and why.
3. **Explain it back in your own words** — short written notes. If you cannot explain it, return to step 1.
4. **Apply it to a guided scenario** — a brief where the concept is relevant, worked with the material beside you.
5. **Compare multiple possible choices** for that scenario, including doing less or nothing.
6. **Defend one choice from the stated requirements** — in writing or aloud, with the trade-offs named.
7. **Challenge the design** — change a constraint (scale, budget, latency, consistency), inject a failure, and revise. State what breaks and what you would do about it.
8. **Use a small implementation or measurement only when it materially proves or clarifies something** — see section 5.

This loop is how a roadmap stage is worked, not a replacement for it. It maps onto the stages' internal order: learn → see it applied → practice → build where useful → apply independently.

## 5. Implementation is supporting evidence, not the objective

- Code, prototypes, and benchmarks are **small and targeted**: used when a claim is easier to understand or verify by building it — a bottleneck, a consistency behavior, an idempotency claim, a failure mode.
- If the important lesson can be demonstrated through a design argument, comparison, calculation, diagram, failure walkthrough, or case analysis, **do not require substantial code merely to produce an artifact.**
- System Design sprints must not become backend coding projects. A sprint task that is mostly application code is off-method, even if it produces a repository.
- Where the roadmap's stage gates genuinely require a build (S3–S5, milestones M3–M5), the build stays: it validates the capability. It must not become the dominant activity of the track or of a sprint.
- Probes and builds live in their own repositories; link and note them in [projects/README.md](projects/README.md). D-013.

## 6. Planning versus execution (who does what)

**Sprint-planning and resource-research AI may:**

- select the concepts and scenarios for the sprint, within the roadmap's stage order;
- propose resources, case studies, worked designs, and reasoning exercises — recorded only after owner acceptance (D-006, [RESOURCES.md](RESOURCES.md));
- propose justified small probes, naming the claim each one would settle.

**It must not:**

- pre-solve the exercises, scenarios, or briefs;
- produce the owner's design reasoning, comparisons, or decisions in advance;
- generate the owner's notes or explanations during planning.

**Study-time AI may:** teach, supply worked examples, generate challenge prompts, and review or critique the owner's reasoning *after* the owner has attempted it. Notes and explanations are execution artifacts, produced when the owner reaches that step of the loop.

The actual reasoning, comparisons, and design decisions happen during execution — by the owner.

## 7. Resources and exercises: how to choose

- **Guided learning is legitimate primary teaching material:** courses, videos, articles, case studies, worked designs, and explanations. Nothing here is emergency-only.
- Optimize for **understanding, reasoning, transfer, and low confusion** — not syllabus completion or quantity of content. A resource that prevents confusion is worth more than a shorter one that leaves it.
- One coherent primary per topic at a time; a second only for a genuine gap or an unclear explanation. No shelf-collecting.
- Exercises should force comparison and defense, not recall: briefs with real constraints, "why not X" challenges, changed-assumption revisions, failure walkthroughs, case analyses.
- Judge a resource by whether it produces explain-back, comparison, and defense — not by length or coverage.
- Nothing is selected in this file. Accepted materials are recorded in [RESOURCES.md](RESOURCES.md). D-006.

## 8. What runs the plan

- **Sprint planners:** name the concept(s), the loop step, and the scenario type — not generic outcomes like "study caching." Keep any build small and justified per section 5.
- **Study assistants:** follow the loop, respect the depth bar, keep component justification explicit, and never hand the owner a finished design they were meant to reason out.
- **Bands:** `gate-window` secondary, `post-gate` primary. The master owns bands and yield order; nothing here changes them.
- Nothing in this file changes the roadmap's stages, order, gates, or milestones. This file governs the how; [ROADMAP.md](ROADMAP.md) governs the what and when.

## Related

- Stages, gates, milestones: [ROADMAP.md](ROADMAP.md)
- Evidence and current stage: [PROGRESS.md](PROGRESS.md)
- Accepted materials: [RESOURCES.md](RESOURCES.md)
- Implementations and probes: [projects/README.md](projects/README.md)
- Near-term items: [BACKLOG.md](BACKLOG.md)
- Strategy and bands: [MASTER_ROADMAP.md](../MASTER_ROADMAP.md)
