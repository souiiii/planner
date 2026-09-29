# GATE

> **Role:** domain roadmap and preparation path for GATE CS/IT.
> **Authority:** subordinate to [MASTER_ROADMAP.md](../MASTER_ROADMAP.md) for phases, attention bands, and non-goals. This file designs the preparation path inside those bounds.
> **Status:** active
> **Last reviewed:** 2026-09-28
> **Paper:** CS/IT (owner-stated 2026-09-27)
> **Target:** AIR < 400 (owner-stated 2026-09-27), to keep PSU opportunities open

## Purpose

A serious, exam-oriented attempt at GATE CS/IT, targeting AIR < 400, as a backup that keeps PSU options open. Not the main career direction. Primary only during `gate-window`; the track closes after the exam (master roadmap). This roadmap makes the attempt real without turning GATE into a permanent study identity.

Preparation is PYQ-driven and built for fast syllabus coverage without overlearning. Real GATE PYQs decide what to study, how deep to go, and when a subject is done. The detailed preparation and resource-selection methodology — including the default topic loop, the theory depth bar, and how notes are built — lives in [PREP_METHOD.md](PREP_METHOD.md), which sprint planners and study assistants must follow for GATE work.

Reconciliation note: paper CS/IT and target AIR < 400 are owner-stated (2026-09-27) and now recorded in the master roadmap (D-022). No wording gap remains.

## Scope

The official GATE CS/IT syllabus: its ten sections plus General Aptitude.

1. Engineering Mathematics
2. Digital Logic
3. Computer Organization and Architecture
4. Programming in C and Data Structures
5. Algorithms
6. Theory of Computation
7. Compiler Design
8. Operating Systems
9. Databases
10. Computer Networks

General Aptitude carries a fixed share of the paper and is treated as a first-class section, not an afterthought.

Internal priority within subjects comes from actual recent PYQ weightage, not from assumptions. The per-year marks must come from the owner's own paper analysis. No exact figures are invented here.

## Out of scope

- Academic completeness; textbook depth beyond what the exam asks.
- Long concept-first study before touching PYQs.
- Overlearning strong areas.
- AI-generated PYQ substitutes where real GATE PYQs and official answers exist.
- Textbook-style notes.
- Treating the result as a career plan or a reason to change the LSEG path.
- Post-exam study. The track closes.
- Multiple resources per subject collected upfront.
- Dates, weekly schedules, and quotas. This file has none.

## Starting point (no diagnostic overhead)

Not in the repo, not to be invented:

- current level per subject (strong / partial / weak / never studied);
- prior exposure: college coverage, previous attempt, coaching or self-study history;
- materials already owned or used;
- actual weekly capacity (master roadmap: `unknown`).

There is no diagnostic test gate before starting. No full-paper baseline, no scaled subset, no provisional score is required to begin Stage 1. Level is revealed by PYQ attempts inside the loop, not by testing overhead upfront. Do not assume zero and do not assume a strong start.

Stage 0 sets up the syllabus, the real-PYQ source, and the notes/log system only. Evidence accumulates from Stage 1 onward.

## How this path works

- **PYQs are the primary learning and validation tool.** They establish scope before studying and validate after solving — not a license to attempt blind or to skip theory.
- **Theory depth is the minimum needed to solve real PYQs and nearby variants.** If a concept has no PYQ footprint, it gets a thin pass.
- **Strong areas get compressed treatment; weak areas expand only when evidence demands it.** Evidence means missed PYQs, failed checkpoints, or mock analysis — never a feeling or a generic hard-topics list.
- **Real GATE PYQs and official answers where possible, not AI-generated substitutes.** AI material, if ever used, is at most a stopgap for extra drills — never the spine.
- **Notes are living, compact exam notes, not textbook-style material.** First-pass from theory + mapped PYQ patterns (both inputs), then tightened on every miss.
- **Subject completion means syllabus sections covered + relevant PYQs attempted + unresolved weaknesses recorded,** not "finished all lectures."
- **Progression is independent PYQ solving → mixed/sectional practice → full papers/mocks.** Each step is gated by the previous step's evidence.
- **Errors are the curriculum.** Every miss is logged by cause, and patching targets the log.
- **Cold recall over re-reading.** A topic is closed by answering fresh questions, not by reading again.
- **Ability-gated sequence.** The stage gates below are based on demonstrated PYQ and test performance. The only external date is the exam itself (`unknown` in the repo; around February 2027).
- **Band respect.** During `gate-window`, other tracks continue at their bands. A tight week yields per the master order, not by silently dropping the attempt.
- **After the exam, close.** A result, good or bad, does not retarget the career plan.

## Subject order strategy (default)

Rationale: dependencies first, then PYQ weightage, then evidence from the loop.

**Cluster A — Engineering Mathematics.** Discrete Mathematics first (logic, sets, relations, functions, combinatorics, graph theory; it underpins Theory of Computation, Algorithms, and database theory), then Probability and Statistics, Linear Algebra, Calculus.

**Cluster B — Programming and core CS.** Programming in C and Data Structures, then Algorithms. The overlap is heavy; do data structures before or alongside algorithms.

**Cluster C — Hardware.** Digital Logic, then Computer Organization and Architecture. COA builds on digital logic.

**Cluster D — Systems.** Operating Systems, then Databases, then Computer Networks. These are largely independent; the default order follows typical weightage and can be reordered from PYQ evidence.

**Cluster E — Theory.** Theory of Computation, then Compiler Design. Parsing and languages depend on TOC.

**General Aptitude.** Short, light sessions throughout; PYQ-driven; a modest dedicated push during consolidation.

Adaptation rules:

- The default order stands until PYQ evidence changes it. Subjects whose section PYQs solve cleanly get a compressed pass and release their time. Subjects with repeated PYQ misses get expanded patching — topic by topic, cause by cause.
- Dependencies above are fixed: discrete math before TOC, digital logic before COA, data structures before algorithms, TOC before compiler design.
- When two subjects compete for the next slot, the one with higher recent PYQ weightage goes first.
- Within a subject, PYQ frequency and weightage decide section order, not chapter numbers.

## Stages

### Stage 0 — Light setup, no testing overhead

**Work**

- **Official syllabus:** record the source. This is the coverage checklist.
- **Real PYQ source:** secure one source of real GATE CS/IT PYQs with official keys/answers. Record what it covers (years, subject-wise vs paper-wise). Prefer materials you already own. Buy nothing until a concrete gap shows.
- **Living notes system:** create one compact exam-notes location per subject/section. Empty at start is fine.
- **Weakness/error log:** create it with fields: date, source, subject/topic, cause (concept / recall / application / silly / timing / misread), correction, re-test result.
- **Revision register:** create it with fields: topic, status (learning / consolidating / closed), last cold test, next check.
- **Subject order:** write the default order from above, or note the owner's preferred start point. No baseline scores are needed to write it.

No diagnostic test. No mock. No topic pre-assessment.

**Exit criteria**

- official syllabus source recorded;
- real-PYQ source with official keys recorded;
- notes, error log, and revision register exist;
- starting subject order written in this file or in [PROGRESS.md](PROGRESS.md).

### Stage 1 — PYQ-driven subject coverage (the core loop)

For each subject in the order, run the canonical topic loop from [PREP_METHOD.md](PREP_METHOD.md), which governs the detailed method. In outline, per topic:

1. Map the topic's real GATE PYQs first — scope and depth come from what GATE actually asks, not from attempting blind.
2. Learn concise-but-sufficient theory from the topic's chosen primary teaching resource (video preferred when suitable; text fine when clearer).
3. Prepare first-pass compact notes from that theory + the mapped PYQ patterns.
4. Solve the topic's real PYQs independently.
5. Diagnose misses by cause; patch the specific theory/application gaps.
6. Update and tighten the notes.
7. Add extra good GATE-level practice only when PYQ volume is insufficient.
8. Cold re-test on a fresh PYQ or variant, record weaknesses, and continue.
9. Finish the subject with its subject-level PYQ checkpoint; carry unresolved weaknesses forward.

Rules inside the loop:

- **PYQ-first means scoping, not blind attempting.** Map first, solve after learning.
- **PYQ-focused does not mean theory-light:** enough theory to understand the concept, know when/why it applies, and solve standard variants without memorized tricks.
- **Theory resources are valid primary teaching resources for near-term topics,** one coherent primary per topic, supplements only for genuine gaps — and selected only for near-term topics.
- **Section note bundle (explicit):** for each section, the living notes hold: (1) section, (2) compact required theory (minimum to solve its PYQs), (3) formulas/patterns/traps, (4) mapped real PYQs, (5) solutions/explanations with official keys, (6) note patches from mistakes. No textbook expansion.
- Strong sections compress: clean PYQ solves mean short notes and move on. No extra theory.
- Weak sections expand only on evidence: a miss triggers a targeted patch, then a re-test on a fresh PYQ or variant.
- Log every miss with its cause.
- Aptitude runs in short, light PYQ sessions alongside.

**Exit criteria**

- every syllabus section visited at least once;
- relevant real PYQs attempted for every subject;
- a checkpoint result recorded for each subject;
- unresolved weaknesses recorded in the log/register, not left as a feeling.

Subject completion = sections covered + PYQs attempted + weaknesses recorded. Lecture completion alone completes nothing.

### Stage 2 — Independent solving, mixed/sectional practice, first revision

- Independent PYQ solving: re-solve without notes, prioritizing sections missed in Stage 1.
- Mixed-topic practice within subjects to break section isolation.
- Sectional timed practice across subjects. Record a timing baseline (time per question, skipped vs attempted).
- Structured revision from the weak-topic list and the error log only. Cold re-tests. Close topics that pass. Tighten the notes; do not expand them into textbook material.

**Exit criteria**

- the chosen recent-year PYQs are completed independently;
- the top error causes are closed or clearly reduced;
- the weak-topic list is reduced with cold re-test evidence;
- a sectional timing baseline is recorded.

### Stage 3 — Mock-driven consolidation

- Full-length papers/mocks under exam conditions. Prefer real GATE papers first, then one chosen mock source.
- The cycle, not the count: mock → complete question-by-question analysis → repair session on the causes → notes and revision-register update → next mock. Do not take the next mock until the previous repair is done.
- Analysis taxonomy per question: concept gap / recall gap / application error / silly / time pressure / misread. Track accuracy, attempts, and time per subject.
- Second revision cycle driven entirely by the error log.
- Paper strategy: question selection, attempt order, time boxing, and when to leave a question.
- **Improvement rule:** if two consecutive mocks show no improvement in the dominant failure category, change the intervention (a targeted topic drill, accuracy work, or timing work). Do not simply take more mocks.
- The owner sets the working mock-score band that corresponds to AIR < 400 and reviews it against results. No band is invented here.

**Exit criteria**

- mock results are stable or improving against the owner's working band;
- the dominant error causes are reduced;
- every section is being exercised in mocks;
- the revision register holds only stubborn items.

### Stage 4 — Exam-mode consolidation

- **Trigger:** the exam is approaching and the Stage 3 exit criteria are met. The switch belongs to the owner's calendar; this file sets no dates or durations.
- Revision only: formula sheet, personal notes, error log, high-yield topics. No new resources, minimal new topics.
- Maintain a mock rhythm at reduced load, taper before the exam, protect sleep.
- Exam logistics: admit card, ID, reporting instructions, travel.

**Exit criteria**

- the exam is written. Then close the track per the master roadmap. Do not start a post-exam study plan.

## Milestones

| Id | Checkpoint | After |
| --- | --- | --- |
| M0 | Syllabus, real-PYQ source, notes/log system, starting order — no diagnostic | Stage 0 |
| M1 | Full sections covered, section PYQs attempted, subject checkpoints, unresolved weaknesses recorded | Stage 1 |
| M2 | Independent PYQs done, weak list reduced, timing baseline | Stage 2 |
| M3 | Mocks stable or improving, dominant causes reduced | Stage 3 |
| M4 | Exam written, attempt recorded | Stage 4 |

## Weak areas: diagnosis and revision

- Weakness is diagnosed from evidence: section-PYQ misses, checkpoint results, mock analysis. Never from a generic "hard topics" list or a feeling. There is no pre-study test to manufacture it.
- Strong performance compresses: clean solves mean shorter notes and faster movement, not deeper study.
- The error log is the diagnosis instrument. Causes, not just topics: a concept gap and a silly error need different fixes.
- The revision register drives revisits. Intervals grow with success and reset on failure. No fixed calendar intervals in this file.
- A topic closes only after a later cold re-test passes, ideally on a fresh question. Re-reading is not closure.
- Revisit order: highest-weightage weak topics first; within that, the causes costing the most marks.
- Notes stay living and compact: each patch adds the missing pattern or fix, not a textbook section.

## Tests, PYQs, and mocks

- PYQ progression: section PYQs inside the loop → subject-level PYQ checkpoint → independent re-solving → mixed and sectional → full papers/mocks.
- Real GATE PYQs and official answers are the spine at every step. Do not substitute AI-generated questions for them.
- Every test gets an analysis pass. Record: accuracy by subject, attempted vs skipped, time per question, error-cause totals, mock results over time.
- Track in [PROGRESS.md](PROGRESS.md). Keep it honest and coarse; no fabricated percentages.
- Mock count is set by capacity and the exam date, not by a quota in this file.

## Resources: policy without overload

- Real PYQs plus official keys and the official syllabus are the spine.
- **Theory resources are valid primary teaching resources for near-term topics** — one coherent primary per topic, chosen when the topic becomes near-term, not collected upfront. Video preferred when suitable; text fine when clearer or more efficient.
- Supplements are only for genuine gaps or unclear explanations, and they go to [RESOURCES.md](RESOURCES.md) once the owner accepts them. Decision D-006.
- Avoid: multiple standard books per subject, lecture binges, passive video watching, AI question banks presented as PYQs, and switching resources when a topic feels hard.
- Mock series: needed by Stage 3. Choose one and use it properly. Do not subscribe to several.

The detailed resource-selection rules (what "suitable" means, how quality is judged) live in [PREP_METHOD.md](PREP_METHOD.md).

## Assumptions and unknowns

- Paper CS/IT and target AIR < 400 are owner-stated and now recorded in the master roadmap (D-022).
- Current level per subject is `unknown` and is revealed by PYQ attempts in Stage 1, not by a diagnostic. Also unknown: prior exposure, materials, capacity.
- Exact exam date is `unknown`; roughly February 2027 per the repo. The owner's calendar holds the real date.
- Capacity `unknown` affects mock cadence and how long the stages take; it does not change the sequence.

Nothing here should be treated as evidence that preparation is at zero, or that any subject is already strong.

## Related

- Coverage, PYQs, and scores: [PROGRESS.md](PROGRESS.md)
- Near-term unsolved items: [BACKLOG.md](BACKLOG.md)
- Chosen materials: [RESOURCES.md](RESOURCES.md)
- Strategy and bands: [MASTER_ROADMAP.md](../MASTER_ROADMAP.md)
- Official syllabus and previous papers: owner's chosen sources, recorded in [RESOURCES.md](RESOURCES.md)
- Execution: `current-sprint/` while open, then `sprints/`. Not a folder here.
- How preparation is executed: [PREP_METHOD.md](PREP_METHOD.md)
