# GATE preparation method

> **Role:** the permanent operating guide for how GATE preparation is done in this repo. Method, not plan.
> **Not a roadmap, not a syllabus, not a sprint plan, and not a resource list.** Strategy, subject order, stages, and milestones live in [ROADMAP.md](ROADMAP.md). This file governs how the preparation inside that roadmap is actually done.
> **Audience:** every sprint planner and study assistant that touches GATE work. Read this before choosing GATE tasks or resources.
> **Objective:** AIR < 400 in GATE CS/IT. Every rule below serves that target.
> **Status:** active
> **Last reviewed:** 2026-09-29

## 1. Strictly GATE-oriented

Learn what is useful for GATE. Nothing more, and nothing less.

- Every topic, depth choice, resource, and note exists to improve GATE solving. If a piece of material cannot be tied to GATE questions or the official syllabus, it does not belong in the plan.
- "Nothing less" matters as much: the syllabus sections and their PYQ-heavier topics are covered properly, not skimmed into a shallow highlight reel.
- University-style completeness, advanced electives, and research-level material are out unless a GATE question makes them necessary.

## 2. The goal is solving ability

The product of preparation is the ability to solve GATE questions, not:

- lectures watched or chapters completed;
- theoretical or mathematical completeness;
- collection of notes, courses, or problem sets;
- familiarity with terms.

Time spent without a question being attempted, understood, or re-tested is suspect by default.

## 3. Resources

- **Video-based teaching is preferred when suitable; text is fine when clearer or more efficient for the topic at hand.** A primary teaching resource for a near-term topic is normal, planned material — not an emergency patch. Suitability comes first: no medium is chosen for its own sake.
- **One coherent primary resource per topic.** Not per subject, and not a stack. Choose one resource that teaches the topic well end to end, and stay with it. Add a second only to patch a genuine gap or an unclear explanation.
- **No resource stack built in advance.** Select material only for the near-term topics actually being prepared. Future topics pick their material when they become near-term.
- **Materials the owner already owns come first** where they serve. New purchases wait for a concrete gap.
- **Quality is judged by time-to-independent-GATE-solving ability** — how quickly a resource gets the owner to solving GATE questions unaided. Not by shortest duration, and not by largest syllabus coverage. A longer explanation is acceptable when it prevents confusion and materially improves solving ability; a short one that leaves confusion is expensive.
- **Supplements need a reason.** Record accepted materials in [RESOURCES.md](RESOURCES.md) only after the owner accepts them (D-006). No model adds courses, books, videos, or tool lists on its own.
- No spy-scrolling between resources when a topic feels hard: switch only with a stated reason tied to learning, not discomfort.

## 4. PYQ-focused does not mean theory-light

PYQs are the primary validation mechanism and the main guide to required depth. They establish what to study and prove that it worked — they do not license thin theory.

Two readings of "PYQ-first" must be kept apart:

- **PYQ-first as scoping: yes.** Inspect and map the topic's real PYQs *before* studying, so scope, weightage, and question style come from what GATE actually asks.
- **PYQ-first as attempting-everything-blind: no.** Solving happens after learning the theory and preparing first-pass notes. Walking cold into a topic with no teaching is not a gate and not a badge.

For each topic, learn enough theory to:

- understand the concept properly, not just its formula;
- know when and why it applies, and when it does not;
- handle the standard GATE variations of that topic, which are more numerous and slier than most sources advertise;
- solve questions without depending on memorized tricks.

Tricks learned as shortcuts on top of understanding are fine. Tricks substituted for understanding are how GATE variants punish candidates. If a topic only survives a PYQ because a trick was memorized, the topic is not done.

## 5. The default topic loop

Run this loop per topic (or tightly related topic cluster), inside the stages of [ROADMAP.md](ROADMAP.md):

1. **Map the real GATE PYQs first.** Inspect the topic's actual previous-year questions — what GATE asks, how often, at what depth, and which sub-parts recur — before studying anything. This establishes scope and the depth target; it is not an attempt to solve them blind. Keep a short map: pattern list with years.
2. **Learn concise-but-sufficient theory from the chosen primary teaching resource.** At the depth bar in section 4, guided by step 1's map. Concise means no padding — not shallow. Seeing worked examples and numericals is part of this step: watch or study corrected solves before doing one; it is learning, not cheating.
3. **Prepare first-pass compact notes.** Built from BOTH the theory just learned AND the PYQ map from step 1: required concepts, formulas and their conditions, methods, traps, and the recurring PYQ patterns observed. First-pass, not final — this note gets patched later in the loop.
4. **Solve the topic's real GATE PYQs independently.** The actual previous-year questions, official answers and explanations checked only after attempting. AI-generated substitutes do not validate (see [ROADMAP.md](ROADMAP.md)).
5. **Diagnose misses.** Every miss gets a cause, not just a topic: concept gap, recall gap, application error, misread, or carelessness. The error log in [PROGRESS.md](PROGRESS.md) fields these.
6. **Patch the specific theory or application gaps.** Revisit the exact concept(s) the misses expose, from the primary resource or a chosen supplement if the explanation is genuinely unclear. Patching is surgical; do not re-study the whole topic on one miss.
7. **Update and tighten the notes.** Fold in what diagnosis revealed: the missed pattern, the trap, the corrected formula condition, the fix. Notes converge here, not only at the end.
8. **Add extra good GATE-level practice only when PYQ volume is insufficient.** If reinforcement beyond the available PYQs is needed, use additional good GATE-level questions — same style, difficulty, and syllabus. Do not fill the gap with unrelated competitive-programming problems or unnecessarily advanced material. When PYQ volume is sufficient, this step is skipped.
9. **Cold re-test / checkpoint, then continue.** Re-test on a fresh PYQ or variant without notes before calling the topic done. On passing: move to the next topic. On failing: the topic is recorded weak and revisited (section 6).

The loop repeats per topic; a subject finishes when its sections and relevant PYQs are done and its weaknesses are recorded, per [ROADMAP.md](ROADMAP.md).

## 6. Validation and the stop rule

- **Real GATE PYQs are the primary validation mechanism.** Progress between topics, and confidence in the AIR < 400 target, rests on them — not on coverage, video counts, or self-feeling.
- **A topic is finished when the owner understands it well enough to:**
  - recognize which GATE questions it applies to;
  - derive the method rather than recall it blindly;
  - solve representative GATE questions and nearby variants reliably — not just the exact questions seen.
- Below that bar, the loop continues (patch, practice) or the topic is recorded as weak and revisited later. "I saw the material" is not the bar.
- Strong performance compresses: clean PYQ solving means compact notes and movement, not deeper study. Repeated misses expand the patching — topic by topic, cause by cause.

## 7. Notes

Notes are the compact, exam-oriented record, evolving through the topic loop: first-pass notes come from theory + the PYQ map (section 5, step 3), then get updated and tightened after each diagnosis (section 5, step 7). They are not a second textbook.

Each topic's notes converge toward:

- required concepts, in one or two lines each;
- formulas and when each applies;
- methods and standard solution patterns;
- traps, edge cases, and common confusions;
- recurring PYQ patterns for that topic;
- mistakes discovered during practice, with the fix.

Rules:

- Written to support solving a question — readable while practicing, skim-able before the exam. If a note would not help solve a PYQ, it does not belong in the notes.
- Notes start as first-pass drafts (theory + PYQ patterns) and tighten with every diagnosis; final compactness is the goal, not a first-draft requirement.
- **Sprint planning is not note generation.** Sprint-planning and resource-research models must not write the actual study notes while preparing a sprint. They may choose topics and resources and state that note-making is part of the topic loop — nothing more.
- **AI-assisted note creation happens during study execution only:** when the owner reaches that topic's note step (section 5, step 3) — after learning the relevant theory, with the mapped PYQ context in hand. Notes are then tightened after solving and diagnosing PYQs (section 5, step 7). The source pool is [RESOURCES.md](RESOURCES.md) materials and real PYQs, and the notes must serve problem solving, not become another textbook to read.
- Notes live with the notes system set up in Stage 0 of [ROADMAP.md](ROADMAP.md); they are the revision spine for Stage 2 onward.

## 8. What runs the plan

- **Efficiency and low confusion are major priorities.** When two paths reach the same solving ability, take the clearer one. When an explanation causes confusion, fix or replace it early; confusion compounds.
- **Sprint planners:** GATE tasks in a sprint should name topic(s) and the loop step being executed (mapping PYQs, theory, notes, solving, patching, re-testing). Do not name generic outcomes like "study OS". Planning chooses topics and resources; it never generates the study notes themselves (section 7).
- **Study assistants:** follow the loop, respect the depth bar, and never substitute AI-generated PYQs for real ones or pad practice with off-syllabus problems.
- Nothing in this file changes subject order, stage gates, milestones, or the AIR < 400 objective in [ROADMAP.md](ROADMAP.md). This file governs the how; the roadmap governs the what and when.

## Related

- Strategy, stages, subject order, milestones: [ROADMAP.md](ROADMAP.md)
- Evidence and scores: [PROGRESS.md](PROGRESS.md)
- Accepted materials: [RESOURCES.md](RESOURCES.md)
- Near-term items: [BACKLOG.md](BACKLOG.md)
- Bands and phases: [MASTER_ROADMAP.md](../MASTER_ROADMAP.md)
