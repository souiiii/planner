# GATE input for Sprint 001

> **Status:** accepted candidate input for the later integrated Sprint 001 planner (owner-accepted 2026-09-29; accepted resources are recorded in [RESOURCES.md](RESOURCES.md)). Not an active sprint plan.
> **Prepared:** 2026-09-29. **Accepted:** 2026-09-29.
> **Purpose:** candidate input for the later integrated, approximately 10-day Sprint 001. This is not an active sprint plan.
> **Authority:** [MASTER_ROADMAP.md](../MASTER_ROADMAP.md), [CURRENT_STATE.md](../CURRENT_STATE.md), [AI_WORKFLOW.md](../AI_WORKFLOW.md), [ROADMAP.md](ROADMAP.md), and [PREP_METHOD.md](PREP_METHOD.md). [PROGRESS.md](PROGRESS.md), [BACKLOG.md](BACKLOG.md), and [RESOURCES.md](RESOURCES.md) were also read.

## Recommendation

**Start with propositional logic, then the recurring first-order logic patterns.** Include the light Stage 0 setup and a little General Aptitude logical reasoning. Treat **sets and basic relation properties as a conditional extension**, admitted only if the logic loops leave room for its own solving and checkpoint. Do not aim to complete Discrete Mathematics.

This follows the existing Engineering Mathematics → Discrete Mathematics opening. Propositional logic supports quantified statements; both support reasoning about relations and later TOC/database work. Recent questions require more than recognizing symbols: implication direction, quantifier scope, counterexamples, and uniqueness all matter. These are coherent, bounded learning outcomes for a first slice whose capacity is still unknown.

Owner-reported in this conversation: college curriculum and online exam preparation are the prior exposure; no GATE materials are owned; either English or Hindi/English teaching is acceptable. This does **not** establish a strong or weak topic baseline. The resource recommendations below are free; no purchase is proposed.

The [official GATE 2027 CS syllabus](https://gate2027.iitm.ac.in/static/doc/GATE2027_Syllabus/CS_GATE2027_Syllabus.pdf) includes propositional/first-order logic and sets/relations. Use it as the proposed Stage 0 coverage source. Researching it does not change the roadmap or the repo's exam-date facts.

### Scope boundary

| Candidate component | Include | Depth required in this slice |
| --- | --- | --- |
| Core A: propositional logic | Connectives, precedence, truth tables, implication/biconditional, necessary/sufficient conditions, converse/inverse/contrapositive, translation, equivalence, tautology/contradiction/satisfiability, basic inference and invalid arguments | Explain the reasoning and handle changed statements, rather than memorize truth-table answers |
| Core B: first-order logic | Predicates and domains; free/bound variables and scope; universal/existential quantification; negation; nested quantifier order; translation; implication/equivalence and countermodels; existence versus uniqueness | Handle the mapped quantified-expression and translation questions; include the small induction prerequisite exposed by 2025 CS2 Q15 |
| Conditional extension: sets → basic relations | Membership versus inclusion, empty set, power set, cardinality, Cartesian product, union/intersection/difference/complement; binary relations, reflexive/symmetric/antisymmetric/transitive properties; equivalence relations and basic classes/partitions | Justify properties or refute them with counterexamples, including a property defined inside a question |
| Light companion: GA logical reasoning | Implication and inference from the stated information | Transfer the logic work to a small real-GATE GA set; no separate aptitude course |

## What the real questions establish

This is a **research map, not a solving record or study note**. Recent official papers were inspected for scope, with older GATE questions used to expose recurring variations. No preparation, scores, or completion are being logged.

**Numbering:** `official Q` below refers to the master paper including GA. `GO Q` is the number in the linked GATE Overflow entry. In the recent papers these can differ by ten; always match the stem and session before using an answer key. Do not apply that offset blindly to older papers.

### Core practice and checkpoint pool

| Real GATE question | Pattern / reason for inclusion | Proposed use |
| --- | --- | --- |
| [2017 CS1, GO Q1](https://gateoverflow.in/118698/gate-cse-2017-set-1-question-01) | Implication equivalence and contrapositive | Propositional practice |
| [2017 CS2, GO Q11](https://gateoverflow.in/118151/gate-cse-2017-set-2-question-11) | Translate a compound English statement | Propositional practice |
| [2021 CS1, GO Q7](https://gateoverflow.in/357445/gate-cse-2021-set-1-question-7) | Distinguish tautology from its reversed implication; 1 mark | Propositional practice |
| [2024 CS2, official Q12 / GO Q2](https://gateoverflow.in/422895/gate-cse-2024-set-2-question-2) | Translate a grading condition with negation; 1-mark MCQ | Propositional practice |
| [2021 CS2, GO Q15](https://gateoverflow.in/357525/gate-cse-2021-set-2-question-15) | Nested implication, equivalence, and all correct MSQ choices; 1 mark | Reserve for cold propositional checkpoint |
| [2017 CS1, GO Q2](https://gateoverflow.in/118701/gate-cse-2017-set-1-question-02) | Quantifier order, implication, and negation over a nonempty domain | First-order practice |
| [2020 CS, GO Q39](https://gateoverflow.in/333192/gate-cse-2020-question-39) | Quantifier scope and a formula with no free occurrence of the quantified variable; 2 marks | Reserve for cold first-order checkpoint |
| [2023 CS, official Q26 / GO Q16](https://gateoverflow.in/399295/gate-cse-2023-question-16) | Decide which statements imply a quantified conjecture; 1-mark MSQ | First-order practice |
| [2025 CS1, official Q48 / GO Q38](https://gateoverflow.in/460042/gate-cse-2025-set-1-question-38) | Formalize existence and uniqueness together; 2-mark MSQ | First-order practice after uniqueness teaching |
| [2025 CS2, official Q15 / GO Q5](https://gateoverflow.in/460830/gate-cse-2025-set-2-question-5) | Identify a valid induction assertion, including its base and direction; 1-mark MCQ | Practice after the short induction bridge |
| [2026 CS2, official Q11 / GO Q1](https://gateoverflow.in/523146/gate-cse-2026-set-2-question-1) | Quantified English translation with a directed predicate; 1-mark MCQ | Reserve for cold first-order checkpoint |

The pattern is recurring across years, but its direct marks are modest and variable. The recent mapped logic items are one- or two-mark questions; this is a dependency-led opening, not a claim that logic dominates the paper. MSQs also require rejecting every incorrect option. That is why concise theory must include conditions and counterexamples.

Do not turn this sample into a predicted annual weightage or the owner's paper-analysis record. In particular, the broader “Set Theory & Algebra” category also includes functions, orders, and groups; its aggregate marks are not the importance of basic sets/relations alone.

### Conditional extension map

| Real GATE question | What it tests | Proposed use |
| --- | --- | --- |
| [2015 CS3, GO Q23](https://gateoverflow.in/8426/gate-cse-2015-set-3-question-23) | Quantified claims about subsets, complement, difference, and cardinality | Sets practice |
| [2016 CS2, GO Q26](https://gateoverflow.in/39603/gate-cse-2016-set-2-question-26) | A relation on ordered pairs; checking reflexivity/transitivity from its actual definition | Relations practice |
| [2021 CS1, GO Q43](https://gateoverflow.in/357408/gate-cse-2021-set-1-question-43) | Combine a newly defined circular property with familiar relation properties; 2-mark MSQ | Relations practice |
| [2026 CS2, official Q26 / GO Q16](https://gateoverflow.in/523130/gate-cse-2026-set-2-question-16) | Classify an arithmetically defined relation; 1-mark MSQ | Reserve for cold relations checkpoint |

These justify basic relations after logic. They do not justify adding all adjacent material: [2023 official Q49](https://gate2026.iitg.ac.in/doc/download/2023/cs_2023.pdf) also needs functions on equivalence classes; [2025 CS2 official Q42](https://gate2026.iitg.ac.in/doc/download/2025/CS22025.pdf) needs partial orders and lattices. Both are deferred in full.

## Teaching resources — proposed portions only

### Primary: Neso Academy, Discrete Mathematics

Use the free [YouTube playlist](https://www.youtube.com/playlist?list=PLBlnK6fEyqRhqJPDXcvYlLfXPh37L89g3). The [provider's chapter catalogue](https://www.nesoacademy.org/cs/07-discretemathematics) identifies the corresponding topics. Use YouTube for the selected public lessons; a Neso Fuel subscription is unnecessary.

**Why this primary:** it provides a continuous explanation from connectives to quantifiers, with translation examples, counterexamples, and worked GATE problems. Its modular lessons make a precise patch possible after a miss. The selected theory is followed by independent PYQs; watching the playlist is not the outcome.

Positions below were checked against the public playlist on the research date. Titles and chapter boundaries identify the material if positions later change.

| Topic | Exact portions | Approximate playback, excluding pauses |
| --- | --- | --- |
| Propositional logic | Positions **2–12, 15–20, 24–27, 29–31**. Start at [Motivation & Introduction](https://www.youtube.com/watch?v=IZpvlR5J7FQ); include implication Parts 1–3, translation, classifications/equivalence, and inference through *The Limitation of Propositional Logic*. | About 2 h 50 min |
| First-order logic | Positions **32–47, 52–63, 68–72**. Start at [Introduction to First Order Logic](https://www.youtube.com/watch?v=ARywou8HLQk); cover quantifiers, restricted domains, equivalence/negation, translation, nested examples/negation, fallacies and quantified inference. Position 47 is a worked 2013 GATE example. | About 2 h 30 min |
| Sets, only if extension admitted | Positions **73–79, 81–82, 85–93**. Start at [Basics of Sets](https://www.youtube.com/watch?v=Ql7pHnavYSA); finish the selected set identities. | About 1 h 45 min |
| Basic relations, only if extension admitted | Chapter 4: **Introduction to Relations; Types of Relations Parts 1–2; Types of Relations (Solved Problem); Representation of Relations; Equivalence Relation; Equivalence Relation (Solved Problems); Equivalence Classes; Equivalence Classes and Partitions**. [Starting video](https://www.youtube.com/watch?v=4Caxyh0zt_o). | About 1 h 10 min |

Skip puzzles, duplicate solved-problem runs, and the resolution block on the initial pass. Use a skipped example only to repair an actual gap. Worked PYQs seen in teaching are **exposed examples**, not fresh evidence; do not reuse them as cold checkpoint questions.

Research limit: lesson titles, ordering, durations, and selected descriptions were verified; the full videos were not watched end to end. Suitability is a recommendation to validate through the first learning loop, not an owner-tested result.

### Narrow teaching gaps

| Resource | Portion and specific reason |
| --- | --- |
| [GO Classes — Discrete Mathematics, Deepak Poonia](https://www.goclasses.in/courses/Discrete-Mathematics-Course/) | **Module 4 → OPTIONAL Lecture 3 — Uniqueness Quantifier (27 minutes).** Include before the 2025 uniqueness PYQ: the Neso catalogue does not explicitly establish this coverage. Its “optional” course label does not make the mapped skill optional here. Free signup is required; enrolment was not performed. |
| [TrevTutor — Mathematical Induction](https://www.youtube.com/watch?v=Tm2PJPvAULs) | One approximately **14-minute video**, covering the principle and basic examples, before 2025 CS2 Q15. Induction is a concrete gap in the selected Neso logic lessons, not a request to study a proof-techniques course. |

For an actual scope/free-variable miss, GO Classes Module 4 **Lecture 21 — Free Variable Vs Bounded Variable** or **Lecture 24 — Scope of a Quantifier** is a targeted fallback, chosen by the error. Do not preassign both or the full module. Check understanding of scope in the primary's examples before independent solving.

The GO compact alternative was considered: its listed propositional and first-order teaching alone totals about 13.5 hours. Its [catalogue](https://www.goclasses.in/courses/Discrete-Mathematics-Summary-GATE_PYQs-Practice-Course-625613d10cf2ad8d82475130) is useful, but the whole course is not proposed for this opening slice. The selection above rests on coverage plus a full solving loop, not video length alone.

## PYQ source and answer handling

**Proposed source arrangement:** official master papers/keys for question and answer authority; GATE Overflow for topic navigation and worked explanations. This is one practice pool with two complementary roles.

- [Official archive](https://gate2026.iitg.ac.in/download.html): paper-wise historical downloads, including papers/keys for 2021–2025 and a bulk paper archive for 2007–2025. The bulk-paper link does not by itself promise keys for every old year.
- [Official 2026 master papers/keys](https://gate2026.iitg.ac.in/QPs-answer-keys.html): both CS sessions.
- [GO Mathematical Logic index](https://gateoverflow.in/questions/mathematics/discrete-mathematics/mathematical-logic?sort=gate) and [GO Set Theory & Algebra index](https://gateoverflow.in/questions/mathematics/discrete-mathematics/set-theory%26algebra?sort=gate): topic discovery only. Use the exact mapped entries, avoiding memory-based duplicates, other exams, unrelated tags, and automatic AI summaries.

Direct official pairs needed for the recent map:

| Paper | Question paper | Answer key | Relevant official IDs |
| --- | --- | --- | --- |
| 2023 CS | [Paper](https://gate2026.iitg.ac.in/doc/download/2023/cs_2023.pdf) | [Key](https://gate2026.iitg.ac.in/doc/download/Answer_keys2023/CS_ANS_GATE2023.pdf) | Q26 |
| 2024 CS2 | [Paper](https://gate2026.iitg.ac.in/doc/download/2024/CS224S6.pdf) | [Final key](https://gate2026.iitg.ac.in/doc/download/2024/CS2FinalAnswerKey.pdf) | Q12 |
| 2025 CS1 | [Paper](https://gate2026.iitg.ac.in/doc/download/2025/CS12025.pdf) | [Key](https://gate2026.iitg.ac.in/doc/download/2025_Key/CS1_Keys.pdf) | Q48 |
| 2025 CS2 | [Paper](https://gate2026.iitg.ac.in/doc/download/2025/CS22025.pdf) | [Key](https://gate2026.iitg.ac.in/doc/download/2025_Key/CS2_Keys.pdf) | Q15; GA Q6 |
| 2026 CS1 | [Paper](https://gate2026.iitg.ac.in/doc/download/2026/QPs/CS1.pdf) | [Key](https://gate2026.iitg.ac.in/doc/download/2026/Keys/CS1_Keys.pdf) | GA Q5 |
| 2026 CS2 | [Paper](https://gate2026.iitg.ac.in/doc/download/2026/QPs/CS2.pdf) | [Key](https://gate2026.iitg.ac.in/doc/download/2026/Keys/CS2_Keys.pdf) | Q11, Q26 |

Official keys give accepted options/ranges, usually not derivations. After an attempt, compare with the matching official key, then use the linked GO explanation to resolve reasoning. GO answers are community explanations, not official solutions. Older entries in this proposal were inspected on GO; their official keys were not all independently checked. If an older answer is disputed or its key cannot be matched, flag it and use a question with a verified key for the checkpoint.

Preserve the reserved questions: mapping their pattern is enough now. During execution, use stems without solutions and do not open answer discussions until after attempting. If a reserve appears in teaching or was previously studied, replace it with an unexposed real PYQ of the same pattern; otherwise label the later attempt a re-solve, not fresh evidence.

### Extra practice: conditional, not a question-bank commitment

The mapped core pool has eleven distinct PYQs before teaching examples. It is an opening set, not all relevant historical PYQs or a daily quota. Use additional older real GATE questions from the same topic index if a pattern has too few unexposed examples.

If that still leaves a genuine practice gap, the free **GO Classes compact course → “Practice Questions — First Order Logic”** is the proposed fallback, at the [course link above](https://www.goclasses.in/courses/Discrete-Mathematics-Summary-GATE_PYQs-Practice-Course-625613d10cf2ad8d82475130). Select only questions matching the failed pattern, with worked solutions, after owner acceptance. The public listing was verified; individual exercises behind login were not audited. Do not assign the whole set, buy a test series, or make supplemental drills replace real-PYQ validation.

## Intended learning sequence

These are ordered candidate work packages for integration, not dated tasks or calendar blocks.

1. **Light Stage 0 setup.** When execution is opened, record the official syllabus and PYQ source, establish the empty notes location, error log and revision register, and record the existing starting order. Use the roadmap's fields. No diagnostic, mock, or pre-assessment. This preparation document does not complete M0.
2. **Core A loop.** Inspect the nonreserved propositional stems and map their patterns → study the selected primary lessons and worked examples → create first-pass notes during execution from theory plus that map → solve the mapped real PYQs independently.
3. **Diagnose and repair A.** Log every miss as concept, recall, application, misread/carelessness, or timing as appropriate → revisit the exact explanation → tighten the notes → add practice only if needed → cold-test using the reserved propositional question after a gap.
4. **Core B loop.** Repeat mapping → theory → execution-time first-pass notes → independent PYQs for quantification and translation. Include uniqueness teaching and the short induction bridge before their corresponding attempts. Split this into smaller topic loops if quantifier scope needs more attention.
5. **Diagnose and repair B.** Patch the specific causes, tighten notes, and cold-test with the reserved first-order items after intervening work. Require a reason for accepting/rejecting options. A failed checkpoint leaves the affected pattern open; it does not trigger a full-course restart.
6. **Light GA alongside.** Use official 2026 CS1 GA Q5 and 2025 CS2 GA Q6 for conditional statements/inference. Map first; reuse the relevant implication/inference teaching, then follow the same notes–attempt–review–retest loop in short sessions. Keep GA evidence separate from Discrete Mathematics. These examples do not complete GA.
7. **Conditional sets/relations loop.** Admit only after the logic work is stable and the integrated sprint has room for theory, notes, the extension PYQs, repair, and a later cold checkpoint. Otherwise defer it as a whole. A lecture-only start is not the intended extension outcome.
8. **End checkpoint.** Revisit the selected patterns without notes or solution prompts. Record what solved independently, what still needs a cue, and unresolved causes. This is a checkpoint for the selected slice, not a Discrete Mathematics subject-completion claim or M1 exit.

At each notes step, follow the canonical section bundle in the roadmap. **No actual notes, formula sheets, worked solutions, or log scaffolds are generated in this preparation pass.**

## Workload and approximately 10-day fit

Capacity remains **unknown**. Playback estimates describe the material, not available study hours or an assumed daily budget. The core teaching plus the two narrow bridges is about **six hours of playback**, before pauses, notes, attempts, diagnosis and re-testing. Sets/basic relations would add about **three more hours of playback** plus a third complete practice loop.

| Relative portion of the window | Candidate emphasis |
| --- | --- |
| Opening | Small setup/scoping pass, then Core A theory and practice |
| Middle | Core A repair/cold revisit; Core B theory and independent attempts |
| Later | Core B repair, note tightening and delayed checkpoint; retain slack |
| Alongside | Short GA reasoning sessions using the same conceptual groundwork |
| Only if genuine room remains | The complete sets/basic-relations extension |

The base is a substantial first primary-track slice: two connected concept clusters with real independent evidence. First-order reasoning is the likely larger effort, but the owner's actual misses decide that. **Recommend integrating the base first; do not assume the extension fits.** This leaves the later planner room for system-design continuity, other domains at their existing bands, and ordinary unproductive days.

If clean solves compress the loops, admit the extension rather than deepen logic academically. If the base expands, drop the extension first and preserve repair and cold re-testing. Do not spend all ten days watching theory or use other tracks' time as an implicit buffer. No hours, percentages, dates, or calendar density are assigned here.

## Explicitly deferred

- Completing Discrete Mathematics, Engineering Mathematics, or the whole logic section. Less-common model-size reasoning such as [2018 CS GO Q28](https://gateoverflow.in/204102/gate-cse-2018-question-28) remains for later logic coverage; it is not erased from the syllabus.
- Functions and composition; counting functions/relations; advanced equivalence-class applications; relation closures and Warshall's algorithm; partial orders/Hasse diagrams/lattices; monoids/groups; combinatorics/recurrences/generating functions; graph theory.
- Probability/statistics, linear algebra, calculus, and subsequent subject clusters. The default order remains intact.
- Long formal proof courses, predicate-resolution machinery, advanced model theory, or a Digital Logic/K-map detour.
- Full GA coverage, mixed-subject tests, full papers/mocks, and purchasing a test series.
- The disputed [2019 logic question, GO Q35](https://gateoverflow.in/302813/gate-cse-2019-question-35) as first-sprint validation: its interpretation discussion makes it an inefficient clean checkpoint.

## Acceptance (2026-09-29)

Accepted by the owner:

1. The **logic core plus light GA** as the GATE candidate scope for the first slice, with sets/basic relations **conditional** rather than promised.
2. The **selected Neso lessons**, the **GO uniqueness lesson**, the **short induction video**, and the **official-paper/GO source arrangement**. Optional repairs and the extra-practice fallback remain **conditional proposals**.

Still needed before integrated Sprint 001 is created: actual capacity/commitments so the planner can decide whether the extension fits. No additional diagnostic is required.

Owner acceptance is recorded here and in [RESOURCES.md](RESOURCES.md); conditional resources remain conditional. Strategy, milestones, attention bands, progress, the roadmap, and the preparation method are unchanged by this acceptance. Sprint 001 has not been created, and no study notes were generated in this pass.
