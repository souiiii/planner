# GATE

> **Role:** domain roadmap and preparation path for GATE CS/IT.
> **Authority:** subordinate to [MASTER_ROADMAP.md](../MASTER_ROADMAP.md) for phases, attention bands, and non-goals. This file designs the preparation path inside those bounds.
> **Status:** active
> **Last reviewed:** 2026-09-27
> **Paper:** CS/IT (owner-stated 2026-09-27)
> **Target:** AIR < 400 (owner-stated 2026-09-27), to keep PSU opportunities open

## Purpose

A serious, exam-oriented attempt at GATE CS/IT, targeting AIR < 400, as a backup that keeps PSU options open. Not the main career direction. Primary only during `gate-window`; the track closes after the exam (master roadmap). This roadmap makes the attempt real without turning GATE into a permanent study identity.

Reconciliation note: the master roadmap was written before the paper and target were known, so it still says "no score target" and lists the paper as unknown. The paper and target below are owner-stated. The next strategic review should reconcile the master's wording. No master edit was made in this pass.

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
- Treating the result as a career plan or a reason to change the LSEG path.
- Post-exam study. The track closes.
- Multiple resources per subject.
- Dates, weekly schedules, and quotas. This file has none.

## Baseline (unknown) — must be established first

Not in the repo, not to be invented:

- current level per subject (strong / partial / weak / never studied);
- prior exposure: college coverage, previous attempt, coaching or self-study history;
- materials already owned or used;
- mock or PYQ performance so far;
- actual weekly capacity (master roadmap: `unknown`).

Stage 0 establishes these from a diagnostic test and an honest self-map. Until it does, the subject order below is the default, and revision and mock intensity stay provisional. Do not assume zero and do not assume a strong start.

## How this path works

- **Exam-oriented, not academic.** Depth per subject is set by what the exam asks, not by textbook order.
- **PYQs are the spine.** Topic-wise early, subject-wise mid, mixed and full-length later. Every test gets an analysis pass; a test without analysis is practice, not preparation.
- **One primary resource per subject,** plus PYQs. A supplement is added only to unblock a stuck topic. No resource collection.
- **Errors are the curriculum.** Every mistake is logged by cause, and revision targets the log.
- **Cold recall over re-reading.** A topic is revised by answering, not by reading again.
- **Ability-gated sequence.** The stage gates below are based on demonstrated performance. The only external date is the exam itself (`unknown` in the repo; around February 2027).
- **Band respect.** During `gate-window`, other tracks continue at their bands. A tight week yields per the master order, not by silently dropping the attempt.
- **After the exam, close.** A result, good or bad, does not retarget the career plan.

## Subject order strategy (default)

Rationale: dependencies first, then PYQ weightage, then the Stage 0 baseline.

**Cluster A — Engineering Mathematics.** Discrete Mathematics first (logic, sets, relations, functions, combinatorics, graph theory; it underpins Theory of Computation, Algorithms, and database theory), then Probability and Statistics, Linear Algebra, Calculus.

**Cluster B — Programming and core CS.** Programming in C and Data Structures, then Algorithms. The overlap is heavy; do data structures before or alongside algorithms.

**Cluster C — Hardware.** Digital Logic, then Computer Organization and Architecture. COA builds on digital logic.

**Cluster D — Systems.** Operating Systems, then Databases, then Computer Networks. These are largely independent; the default order follows typical weightage and can be reordered from the baseline.

**Cluster E — Theory.** Theory of Computation, then Compiler Design. Parsing and languages depend on TOC.

**General Aptitude.** Short, light sessions throughout; PYQ-driven; a modest dedicated push during consolidation.

Adaptation rules:

- The Stage 0 baseline overrides the default. Subjects marked strong get a compressed verification pass, PYQ-heavy. Untouched subjects get the full concept path. Partial subjects get concept work only on their weak topics.
- Dependencies above are fixed: discrete math before TOC, digital logic before COA, data structures before algorithms, TOC before compiler design.
- When two subjects compete for the next slot, the one with higher recent PYQ weightage goes first.
- Within a subject, weightage and question frequency decide topic order, not chapter numbers.

## Stages

### Stage 0 — Baseline and system setup

**Work**

- **Diagnostic:** one recent full GATE CS/IT paper, closed book, timed, no preparation. Score it honestly. If a full paper is not feasible, a scaled subset covering every section is allowed and marked provisional.
- **Subject map:** mark each section strong / partial / weak / untouched, using the diagnostic plus honest recall. List topics you have never seen.
- **Error log:** create it with fields: date, source, subject/topic, cause (concept / recall / application / silly / timing / misread), correction, re-test result.
- **Revision register:** create it with fields: topic, status (learning / consolidating / closed), last cold test, next check.
- **Resources:** choose one primary resource per subject, one PYQ source with official keys, and one mock source for later. Prefer materials you already own. Buy nothing until a concrete gap shows.
- **Adapted order:** write the subject order this baseline implies (revise the list above or note the changes in this file or in [PROGRESS.md](PROGRESS.md)).

**Exit criteria**

- baseline recorded in [PROGRESS.md](PROGRESS.md);
- error log and revision register exist;
- one primary resource chosen or noted per subject;
- adapted subject order written.

### Stage 1 — First full pass, concept-first

For each subject in the adapted order:

- Learn or revise concepts at exam depth.
- Solve topic-wise PYQs immediately after each topic. This validates understanding and teaches question style.
- Log every error with its cause.
- **Subject checkpoint:** a graded set of that subject's previous-year questions. If it is below your working bar, repair the weak topics and re-test before moving on. Do not progress on coverage alone.
- Run quick cold recall checks against the revision register.

Aptitude runs in short, light sessions alongside.

**Exit criteria**

- every syllabus section visited at least once;
- a checkpoint result recorded for each subject;
- a named weak-topic list exists;
- topic-wise PYQs attempted for every subject.

### Stage 2 — PYQ mastery and first revision cycle

- Subject-wise PYQ sets from the owner's chosen year window. Record which years the window covers.
- First structured revision from the weak-topic list and the error log only. Cold re-tests. Close topics that pass.
- Mixed-topic practice to break subject isolation.
- Sectional timed practice. Record a timing baseline (time per question, skipped vs attempted).

**Exit criteria**

- the chosen recent-year subject-wise PYQs are completed;
- the top error causes are closed or clearly reduced;
- the weak-topic list is reduced with cold re-test evidence;
- a sectional timing baseline is recorded.

### Stage 3 — Mock-driven consolidation

- Full-length mocks under exam conditions.
- The cycle, not the count: mock → complete question-by-question analysis → repair session on the causes → revision register update → next mock. Do not take the next mock until the previous repair is done.
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

- **Trigger:** the exam is approaching and the Stage 3 exit criteria are met. The switch date belongs to the owner's calendar; this file sets no dates or durations.
- Revision only: formula sheet, personal notes, error log, high-yield topics. No new resources, minimal new topics.
- Maintain a mock rhythm at reduced load, taper before the exam, protect sleep.
- Exam logistics: admit card, ID, reporting instructions, travel.

**Exit criteria**

- the exam is written. Then close the track per the master roadmap. Do not start a post-exam study plan.

## Milestones

| Id | Checkpoint | After |
| --- | --- | --- |
| M0 | Baseline, error log, revision register, resources, adapted order | Stage 0 |
| M1 | Full coverage, subject checkpoints, named weak list | Stage 1 |
| M2 | Recent PYQs done, weak list reduced, timing baseline | Stage 2 |
| M3 | Mocks stable or improving, dominant causes reduced | Stage 3 |
| M4 | Exam written, attempt recorded | Stage 4 |

## Weak areas: diagnosis and revision

- Weakness is diagnosed from evidence: checkpoint results, PYQ misses, mock analysis. Never from a generic "hard topics" list or a feeling.
- The error log is the diagnosis instrument. Causes, not just topics: a concept gap and a silly error need different fixes.
- The revision register drives revisits. Intervals grow with success and reset on failure. No fixed calendar intervals in this file.
- A topic closes only after a later cold re-test passes, ideally on a fresh question. Re-reading is not closure.
- Revisit order: highest-weightage weak topics first; within that, the causes costing the most mock marks.

## Tests, PYQs, and mocks

- PYQ progression: topic-wise → subject-wise → mixed and sectional → full papers.
- Every test gets an analysis pass. Record: accuracy by subject, attempted vs skipped, time per question, error-cause totals, mock results over time.
- Track in [PROGRESS.md](PROGRESS.md). Keep it honest and coarse; no fabricated percentages.
- Mock count is set by capacity and the exam date, not by a quota in this file.

## Resources: policy without overload

- One primary resource per subject. PYQs and official keys are the spine.
- Existing materials first. A supplement is added only when a specific topic is stuck, and it goes to [RESOURCES.md](RESOURCES.md) once the owner accepts it. Decision D-006.
- Avoid: multiple standard books per subject, lecture binges, passive video watching, and switching resources when a topic feels hard.
- Mock series: needed by Stage 3. Choose one and use it properly. Do not subscribe to several.

## Assumptions and unknowns

- Paper CS/IT and target AIR < 400 are owner-stated. The target lives in this file until a strategic pass reconciles the master's wording.
- Current level per subject is `unknown`: Stage 0 establishes it. Also unknown: prior exposure, materials, capacity.
- Exact exam date is `unknown`; roughly February 2027 per the repo. The owner's calendar holds the real date.
- Capacity `unknown` affects mock cadence and how long the stages take; it does not change the sequence.

Nothing here should be treated as evidence that preparation is at zero, or that any subject is already strong.

## Related

- Baseline, coverage, and scores: [PROGRESS.md](PROGRESS.md)
- Near-term unsolved items: [BACKLOG.md](BACKLOG.md)
- Chosen materials: [RESOURCES.md](RESOURCES.md)
- Strategy and bands: [MASTER_ROADMAP.md](../MASTER_ROADMAP.md)
- Official syllabus and previous papers: owner's chosen sources, recorded in [RESOURCES.md](RESOURCES.md)
- Execution: `current-sprint/` while open, then `sprints/`. Not a folder here.
