# System Design input for Sprint 001

> **Status:** accepted candidate input for the later integrated Sprint 001 planner (owner-accepted 2026-09-29; accepted materials are recorded in [RESOURCES.md](RESOURCES.md)). Not an active sprint plan.
> **Prepared:** 2026-09-29. **Accepted:** 2026-09-29.
> **Purpose:** candidate input for the later integrated, approximately 10-day Sprint 001. This is not an active sprint plan.
> **Authority read:** [MASTER_ROADMAP.md](../MASTER_ROADMAP.md), [CURRENT_STATE.md](../CURRENT_STATE.md), [AI_WORKFLOW.md](../AI_WORKFLOW.md), [ROADMAP.md](ROADMAP.md), [PREP_METHOD.md](PREP_METHOD.md), [PROGRESS.md](PROGRESS.md), [BACKLOG.md](BACKLOG.md), and [RESOURCES.md](RESOURCES.md).

## Recommended slice

**Stay within S1 — Requirements and constraints.** Learn to turn an imprecise brief into a precise problem statement, then use its constraints to compare and defend a small decision. The candidate outcome is one complete guided reasoning loop and a short independent S1 checkpoint, not completion of a broad system-design syllabus.

This is the recorded starting stage; no stage has passed. Existing backend experience is real, but design depth is unknown. Let the learning and explain-back reveal what needs attention: compress familiar material without assuming either a beginner baseline or demonstrated mastery.

Focus on three connected capabilities:

- Distinguish functional requirements, quality requirements, hard constraints, preferences, and assumptions; identify users and stakeholders.
- Make requirements specific enough to judge: workload and data shape, scale, latency, acceptable stale or incorrect behavior, cost, privacy/compliance where relevant, and operating responsibilities. Identify which requirement dominates and which facts remain unknown.
- Derive decision criteria, compare at least two viable approaches, defend a choice, and reconsider it after a changed constraint or failure.

These are requirements-level judgments. Performance engineering, database guarantees, and distributed mechanisms remain in their later stages. System Design stays **secondary during `gate-window`**; GATE remains primary, and actual capacity is unknown.

## Primary teaching material

**Propose arc42's free English documentation, restricted to the portions below.** Its connected explanations and worked examples suit this small S1 slice without a course commitment. Use the prose to learn the ideas, not as a mandate to fill a twelve-section architecture template. The repo's preparation method remains the learning method.

| Reading order | Exact portion | Purpose |
| --- | --- | --- |
| 1 | [1. Introduction and Goals](https://docs.arc42.org/section-1/): sections 1.1–1.3; stop before the Practical Tips list | Connect essential behavior, quality goals, and stakeholder expectations |
| 2 | [2. Architecture Constraints](https://docs.arc42.org/section-2/): Content, Motivation, and Form | Recognize limits on the available choices, including organizational limits |
| 3 | [10. Quality Requirements](https://docs.arc42.org/section-10/): opening Content/Motivation and 10.2 Quality Scenarios | Turn vague qualities into observable acceptance conditions; use the short scenario form |
| 4 | [Tip 1-13: Make assumptions explicit](https://docs.arc42.org/tips/1-13/): main explanation | Handle missing stakeholder requirements honestly |
| 5 | [9. Architecture Decisions](https://docs.arc42.org/section-9/): Content through the Context/Decision/Status/Consequences table; [Tip 9-2: Document decision criteria](https://docs.arc42.org/tips/9-2/): opening explanation and first example table only | Connect a decision to its criteria and consequences; distinguish mandatory criteria from preferences |

Skip the linked standards, quality-model catalog, scoring matrices, training advertisements, other template sections, and additional examples. A short plain-language comparison is sufficient; no ADR tooling or formal scoring system is required.

**No second teaching source proposed.** The selected pages and case were inspected during this research. They are concise reference-style teaching, so the case and explain-back are essential. If an explanation remains unclear during execution, first revisit that exact passage with a study assistant; propose another source only for the identified gap.

## Worked case: HtmlSanityCheck

Use **one small documented system**, Gernot Starke's [HtmlSanityCheck case](https://examples.arc42.org/systems/htmlsc/), in two passes. It concerns checking generated documentation, which needs little new domain knowledge. The published example is a historical snapshot, not a recommendation to adopt its Java/Groovy tools.

1. **From purpose to constraints:** read [Introduction and Goals, 1.1–1.3](https://examples.arc42.org/systems/htmlsc/01-introduction-and-goals/), the [short constraints list](https://docs.arc42.org/examples/constraints-1/), and [quality scenarios, 10.2](https://docs.arc42.org/examples/quality-htmlsc-2/). Follow how desired behavior becomes prioritized, checkable requirements. Include the maintainer's review note under Quality Goals; the example can be critiqued rather than copied.
2. **From criteria to a decision:** read only [9.2, HTML Parsing with jsoup](https://docs.arc42.org/examples/decision-htmlsc/). This explicitly supplies the goal, selection criteria, alternatives, and rationale. Follow that chain back to the requirements. Skip the other decisions and implementation details.

During execution, reconstruct the chain **requirement → constraint → alternatives → trade-off → decision** in your own words. Distinguish the author's stated rationale from your inference. Ask what downside or missing evidence you would want clarified; the short decision record is not an exhaustive evaluation. Do not install the tool, reproduce its code, or study its framework.

## Proposed execution-time exercises — no solutions

All briefs and numbers below are hypothetical exercise inputs, not facts about the owner. Notes, analyses, comparisons, and choices are to be produced by the owner during execution.

### A. Explain back after the readings and worked case

Without copying definitions, explain the differences among a feature, a quality requirement, a hard constraint, a preference, and an assumption. Give examples from a web application you know. Turn one vague quality claim into an acceptance condition, and say what evidence would disprove one assumption.

Then explain when explicit requirements and decision records help, what effort they cost, and when adding more detail would not improve the decision. Identify a concrete case where the worked example's criteria would be the wrong criteria for another system.

### B. Guided scenario: a small documentation publishing workflow

**Brief:** A college technical club publishes a static handbook of roughly 120 pages, maintained by 20 contributors with a few updates each week. It includes internal links, local images, and references to external sites. A volunteer maintains an existing publishing workflow. Contributors want useful feedback before publishing; the editor wants publishing to remain quick and dependable. There is no budget for another hosted service or a dedicated operator. The acceptable delay, handling of uncertain link results, and whether checks must work offline have not been agreed.

With the selected material available:

1. Identify users, essential behavior, scope boundaries, and relevant constraint categories. Separate given facts from preferences and assumptions. Ask the questions that would most change a decision; for unanswered questions, label a provisional assumption and how to verify it.
2. Write observable acceptance conditions and name the dominant requirement with a reason. Cover traffic/data shape and operating effort without inventing a benchmark result.
3. Propose **two viable approaches** to incorporating checks and handling results. Include the simplest workable approach. Compare them against the same requirements: feedback delay, correctness, failure behavior, maintenance, and cost where relevant. Do not manufacture an alternative that knowingly violates a hard constraint.
4. Defend one choice, state what it gives up, and name evidence that would change your mind. Every component proposed must have a specific job, cost, and new failure mode. A workflow sketch and short argument suffice.
5. **Challenge:** an external site becomes unreachable for an hour while an urgent handbook correction needs publishing. Walk through the behavior of your chosen approach. Revise the requirements or choice where necessary, and explain the consequence. Do not assume unreachable and incorrect mean the same thing.

The decision is deliberately bounded to the publishing/checking workflow. It does not require designing a crawler service, selecting a queue, or implementing a checker.

### C. Independent S1 checkpoint: transfer to another brief

Attempt later, with the worked case and teaching pages closed.

**Brief:** A campus club lends 40 pieces of equipment to about 150 members. Requests currently arrive in chat; one volunteer confirms bookings and hands out equipment on weekdays. Members want to see availability and request a slot. Two members must not receive confirmed overlapping bookings for the same item. The club wants little recurring administration and has no agreed uptime target, retention policy, or software budget.

Produce a precise constraint list, labeled and falsifiable assumptions, important unresolved questions, and the dominant requirement. Identify two plausible service/workflow approaches and defend one at a high level. Do not descend into database isolation, schema design, or infrastructure selection. Then consider **ten times as many members with the same volunteer availability**: which assumption or requirement needs revisiting, and what would you revise or cut first?

This is independent application, not an interview round. If this brief has already been rehearsed, a study assistant should supply a fresh brief of comparable size at execution time, without a worked answer. The assistant critiques only after the owner's attempt.

**Evidence for M1:** the owner can turn the brief into explicit constraints and uncertainty, explain why a requirement dominates, and describe how assumptions could be invalidated. Reading completion does not pass the gate. If reasoning has holes, patch the relevant concept and repeat a small check; record no milestone as passed during this preparation pass.

## Intended learning sequence and workload

| Relative position within the later integrated sprint | Learning step and expected effort |
| --- | --- |
| Opening, compact | Read the bounded primary material and the two passes through the single case. Familiar ideas can move quickly. |
| After learning | Explain back; revisit only the specific ideas that cannot yet be explained or applied. First notes are written here by the owner. |
| Main System Design effort | Work the guided brief through requirements, alternatives, comparison, and defense. This should take more attention than collecting or polishing notes. |
| Later return | Apply the failure challenge, revise the decision, then attempt the independent checkpoint after some separation from the guided work. |

This is **one concept cluster, one worked case, one guided decision with a revision, and one short transfer check** across approximately ten days. These are work packages for integration, not daily assignments or a quota. No hours, percentages, or availability are assumed.

The scope is intentionally much smaller than a second course alongside GATE. Leave substantial room for GATE and the other domains; no daily System Design block is implied. If capacity is too small, keep the guided loop coherent and defer the independent checkpoint rather than rush it or claim M1. If learning is faster than expected, use the checkpoint to demonstrate that; do not automatically add S2 work to this proposal.

## Implementation and probes

**None proposed.** The uncertain claims here concern requirements, acceptability, priorities, and decision reasoning. A comparison and failure walkthrough can expose them; a code benchmark cannot establish stakeholder priorities. No build, scaffold, deployment, or test is needed in this preparation pass or required by this S1 slice. A future probe needs a specific empirical claim that the owner actually encounters.

## Explicitly deferred

- S2 profiling, latency distributions, throughput, saturation, and measured bottleneck work; no automatic stage advance after ten days.
- S3–S6 mechanisms: distributed request paths, caching, detailed database/consistency decisions, queues, retries, observability, and reliability implementations. Requirements about these behaviors may be discussed without studying their mechanisms yet.
- S7 full independent architecture synthesis, timed interviews, memorized systems, and comprehensive design documents.
- Tool/framework study, the remaining arc42 template, additional case collections, purchases, and backend projects.
- Owner notes, completed requirement analyses, option comparisons, designs, decisions, and answers: all remain execution-time artifacts.

## Acceptance (owner-accepted 2026-09-29)

Accepted:

1. The bounded **S1 requirements-and-constraints slice**, including the guided loop. The independent checkpoint (section C) stays **conditional on capacity** — kept only if the guided loop stays coherent; deferred rather than rushed, never claimed without passing.
2. The **selected arc42 readings and HtmlSanityCheck excerpts** as the teaching and case material. No paid material or additional source was proposed or accepted.
3. The exercise briefs (A, B, C) as **candidate work** for the later integrated planner — not as completed work, notes, or solutions.

Still open at integrated planning: actual capacity and commitments, which decide how much fits. This does not block preparing the candidate document.

D-006 remains in force: acceptance is recorded here and in [RESOURCES.md](RESOURCES.md). No sprint, calendar, progress claim, execution artifact, note, design, or solution is created, and no strategy, stage, milestone, attention band, or learning method is changed.
