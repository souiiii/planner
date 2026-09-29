# LeetCode / DSA input for Sprint 001

> **Status:** proposal pending owner acceptance; D-006 applies.
> **Prepared:** 2026-09-29.
> **Purpose:** candidate input for the later integrated, approximately 10-day sprint. No sprint is opened.
> **Authority:** [MASTER_ROADMAP.md](../MASTER_ROADMAP.md), [CURRENT_STATE.md](../CURRENT_STATE.md), [AI_WORKFLOW.md](../AI_WORKFLOW.md), [MAINTENANCE_PLAN.md](MAINTENANCE_PLAN.md), [PROGRESS.md](PROGRESS.md), [ATTEMPTS.md](ATTEMPTS.md), and D-023/D-024 in [DECISIONS.md](../DECISIONS.md).

## Recommended scope and mix

**Propose four new attempts: the first two pool entries plus two company-reported questions.** This is 2 + 2 by attempt count, not a share of sprint time. LeetCode remains maintenance while GATE is primary. No attempt is logged yet, and unseen-problem performance remains unknown.

The pool opens with two Hard questions. Preserve that order and keep the total small; do not replace them with easier entries or add more questions to manufacture breadth. The company pair is Medium, selected for constraint interpretation and defensible reasoning rather than maximum difficulty or topic balance.

## Exact pool slice

Source: `Output/practice_questions.md` in [souiiii/dsa-pool](https://github.com/souiiii/dsa-pool), inspected in the local checkout at `/home/celestia/Documents/dsa-pool/Output/practice_questions.md`.

| Pool ID | Problem | Difficulty |
| --- | --- | --- |
| P1 | [Course Schedule III](https://leetcode.com/problems/course-schedule-iii/) | Hard |
| P2 | [Shortest Subarray with Sum at Least K](https://leetcode.com/problems/shortest-subarray-with-sum-at-least-k/) | Hard |

P1 precedes P2 even when company attempts are interleaved. No regrouping, skipping ahead, or pattern classification. Only the beginning of the practice list and its `AGENTS.md` were inspected; the answer key, internal state, and pattern index were not opened. The owner's explicit prohibition on hidden material governs this preparation task.

## Company selection

Open the **problem links** to practice. The provenance links document selection; reserve those reports for after the attempt because interview accounts and their comments can reveal approaches.

| ID and clean problem link | Company, round, period | Provenance and confidence | Recognition value, without a solution |
| --- | --- | --- | --- |
| C1 — [Maximum Length of a Concatenated String with Unique Characters](https://leetcode.com/problems/maximum-length-of-a-concatenated-string-with-unique-characters/description/) — LC 1239, Medium | Microsoft, SDE-2/L61 recruitment, Codility OA; January 2021 according to the report body, February 2021 in its title | [First-person candidate report](https://leetcode.com/discuss/post/1114687/microsoft-l61-feb-2021-reject/) explicitly names this as OA question 2. **Moderate confidence:** specific candidate account, not employer confirmation. The indexed report excerpt was available; direct retrieval of the full post failed. | The compact statement leaves room for several plausible approaches. It rewards using the actual constraints to justify feasibility and explaining why a proposed choice handles all valid inputs. |
| C2 — [Minimum Deletions to Make Character Frequencies Unique](https://leetcode.com/problems/minimum-deletions-to-make-character-frequencies-unique/description/) — LC 1647, Medium | Plume Design, Staff SWE recruitment, Codility OA, 1 August 2023 | [First-person interview report](https://leetcode.com/discuss/post/4005345/plume-design-staff-swe-hyderabad-india-august-2023-online-test-5-rounds-rejected/) identifies this problem as OA question 3, with **numbers instead of characters**. **Moderate confidence:** detailed dated report and explicit problem mapping, but no employer verification or complete original constraints. This selection is the public practice equivalent, not a claim of verbatim OA text. | Producing a valid result and justifying the minimum are different demands. The problem supports comparison of plausible choices and a correctness argument without requiring obscure mathematics. |

Both public LeetCode statement pages were inspected and are available without opening an editorial. Difficulty labels come from those pages; the recognition-value judgments are planning assessments. Neither selection rests only on a company tag. The role seniority in a report does not establish this owner's level or the question's difficulty.

These two historical reports are enough for this candidate set. No extra company bank, alternative shortlist, or paid resource is proposed. Freshness is still owner-dependent: a previously seen or solved question is a revisit, not fresh-transfer evidence. If a company selection is already familiar, propose a replacement before counting it as a fresh attempt; do not silently relabel it. A familiar pool item keeps its position and is recorded honestly as a revisit.

## Execution and logging

Use the same protocol for both sources:

1. Open only the statement. Reverse-read **output → input → constraints → story**, then restate the task in two lines.
2. Estimate feasible complexity; state the brute-force baseline and its bottleneck.
3. List plausible candidate approaches with rough complexity. Choose and justify one; state it aloud or in writing **before coding**.
4. Implement independently and test normally. A genuine stall means being able to explain what was tried, where it failed, and what is missing; difficulty alone is not a stall.
5. **Log in `ATTEMPTS.md` before consulting the key, editorial, discussion, or other outside reasoning.** Capture source/ID, date, outcome, pre-validation approach, confidence, stall details, and help used. Leave post-validation fields pending until validation actually happens.
6. Validate afterward: the pool's answer key for P1/P2; the platform editorial or an explanatory discussion for C1/C2. Compare reasoning, not just acceptance by the judge. Close outside material and independently reconstruct/re-implement when repair is needed; then complete the validation fields.

No hints, tags, acceptance rates, solutions, discussions, or AI assistance before a genuine attempt or genuine stall. Any assistance must be recorded; an assisted solve is a miss for independent-recognition evidence, even if the submitted code passes. Do not inspect related-question recommendations. No solution or intended technique is supplied in this document.

## Misses and revisits

- Use the existing primary failure tags: `recognition`, `selection`, `derivation`, `implementation`, `constraints`, `complexity`, or `pressure`. Infer weaknesses only from actual attempts.
- Queue every miss, near-miss, and lucky solve in the existing `ATTEMPTS.md` revisit queue. Preserve the original entry.
- Revisit cold: blank editor, no notes or key, approach and complexity stated before coding. Close only after a clean, explainable solve. After a failed revisit, repair the reasoning and queue it again.
- Work revisits before or alongside new attempts, without fixed intervals. Any trigger notes are written during execution, in the owner's words, from actual misses; no pattern sheet is prepared now.

The initial selection is four first attempts. At replanning, **count scheduled cold revisits on their source's side as attempts too**; reduce unstarted new work as needed to retain approximately 50/50, allowing a difference of one for an odd total. Keep the pool prefix intact. Do not fabricate review work or add questions just to balance a ratio; unresolved review may remain queued for the next slice.

## Pacing and observable evidence

Treat this as a few separated practice opportunities across the integrated ten days, not daily work. Interleave the two sources while preserving P1 → P2. Reserve attention for validation and a later cold revisit if the evidence calls for one. The two Hard pool entries may dominate the effort; four attempts is a bounded proposal, not a completion quota or assumed hourly budget.

If integration cannot comfortably hold the full set, reduce to **P1 + C1**, retaining both sources and leaving P2 as the next pool entry. Do not take time from GATE to finish the list. No contest or timer is added.

Expected evidence is a small set of honest pre-validation logs, explicit candidate approaches and complexity judgments, independently attempted implementations, and a justified revisit queue or clean closures where achieved. Four attempts cannot establish a stable weakness profile or pass M1–M5 by themselves. No progress is recorded during preparation.

## Deferred and awaiting acceptance

Deferred: P3 onward, additional company research, difficulty escalation, contests, mock interviews, broad consolidation, new trackers, pattern catalogs, and study notes or solutions generated in advance.

Owner acceptance is still needed for the four-attempt scope and the company selections/sources—especially C1's partially retrievable provenance and C2's explicitly reported variant mapping. Actual capacity and prior familiarity determine final integration. No acceptance is inferred from writing this file.

Only this candidate document is added. `PROGRESS.md`, `ATTEMPTS.md`, the pool, and the governing method remain unchanged. No `leetcode/RESOURCES.md`, `current-sprint/`, `PLAN.md`, or `CALENDAR.ics` is created.
