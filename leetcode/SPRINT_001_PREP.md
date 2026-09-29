# LeetCode / DSA input for Sprint 001

> **Status:** proposal pending owner acceptance; D-006 applies.
> **Prepared:** 2026-09-29.
> **Purpose:** candidate input for the later integrated, approximately 10-day sprint. No sprint is opened.
> **Authority:** [MASTER_ROADMAP.md](../MASTER_ROADMAP.md), [CURRENT_STATE.md](../CURRENT_STATE.md), [AI_WORKFLOW.md](../AI_WORKFLOW.md), [MAINTENANCE_PLAN.md](MAINTENANCE_PLAN.md), [PROGRESS.md](PROGRESS.md), [ATTEMPTS.md](ATTEMPTS.md), and D-023/D-024 in [DECISIONS.md](../DECISIONS.md).

## Recommended scope and mix

**Propose 12 new questions: six randomly drawn pool entries plus six company OA/interview questions.** This is 6 + 6 by new-question attempt count, not a share of sprint time. Cold revisits are additional review work. LeetCode remains maintenance while GATE is primary. No attempt is logged yet, and unseen-problem performance remains unknown.

Twelve genuine attempts provide a meaningful first qualitative sample of recognition, selection, derivation, and implementation behavior: enough opportunities to compare reasoning across problems and notice repeated difficulties, without claiming a statistically stable weakness profile. The company set contains five Medium questions and one Hard; it emphasizes constraint interpretation, comparison, and derivation rather than difficulty alone. The pool draw has no difficulty or topic filter. This remains a bounded candidate workload, subordinate to GATE, not a new quota or attention band.

## Exact random pool draw

Source: `Output/practice_questions.md` in [souiiii/dsa-pool](https://github.com/souiiii/dsa-pool), inspected in the local checkout at `/home/celestia/Documents/dsa-pool/Output/practice_questions.md`.

| Pool ID | Problem |
| --- | --- |
| P32 | [Shortest Bridge](https://leetcode.com/problems/shortest-bridge/) |
| P16 | [Smallest Range Covering Elements from K Lists](https://leetcode.com/problems/smallest-range-covering-elements-from-k-lists/) |
| P6 | [Minimum Interval to Include Each Query](https://leetcode.com/problems/minimum-interval-to-include-each-query/) |
| P59 | [4Sum II](https://leetcode.com/problems/4sum-ii/) |
| P78 | [Count Subarrays Where Max Element Appears at Least K Times](https://leetcode.com/problems/count-subarrays-where-max-element-appears-at-least-k-times/) |
| P17 | [Replace Non-Coprime Numbers in Array](https://leetcode.com/problems/replace-non-coprime-numbers-in-array/) |

**Draw procedure:** with no attempts reported or logged, all 92 entries remained eligible; earlier proposed entries were not treated as completed. On 2026-09-29, Python's OS-backed `secrets.SystemRandom().sample` selected six entry indices uniformly without replacement. The selection operated only on indices; titles and URLs were printed after selection. The table preserves that single draw's returned order. There was no reroll, difficulty adjustment, topic balancing, company-tag filtering, or intended-technique inspection.

The owner's explicit random-selection instruction governs this proposal. No fixed solving order is imposed, and company attempts may be interleaved. Only the public practice list supplied the draw; the answer key, internal state, and pattern index were not opened. No pool or governing file is changed.

## Company selection

Open the **problem links** to practice. The provenance links document selection; reserve those reports for after the attempt because interview accounts and their comments can reveal approaches.

| ID and clean problem link | Company, round, period | Provenance and confidence | Recognition value, without a solution |
| --- | --- | --- | --- |
| C1 — [Maximum Length of a Concatenated String with Unique Characters](https://leetcode.com/problems/maximum-length-of-a-concatenated-string-with-unique-characters/description/) — LC 1239, Medium | Microsoft, SDE-2/L61 recruitment, Codility OA; January 2021 according to the report body, February 2021 in its title | [First-person candidate report](https://leetcode.com/discuss/post/1114687/microsoft-l61-feb-2021-reject/) explicitly names this as OA question 2. **Moderate confidence:** specific candidate account, not employer confirmation. The indexed report excerpt was available; direct retrieval of the full post failed. | The compact statement leaves room for several plausible approaches. It rewards using the actual constraints to justify feasibility and explaining why a proposed choice handles all valid inputs. |
| C2 — [Minimum Deletions to Make Character Frequencies Unique](https://leetcode.com/problems/minimum-deletions-to-make-character-frequencies-unique/description/) — LC 1647, Medium | Plume Design, Staff SWE recruitment, Codility OA, 1 August 2023 | [First-person interview report](https://leetcode.com/discuss/post/4005345/plume-design-staff-swe-hyderabad-india-august-2023-online-test-5-rounds-rejected/) identifies this problem as OA question 3, with **numbers instead of characters**. **Moderate confidence:** detailed dated report and explicit problem mapping, but no employer verification or complete original constraints. This selection is the public practice equivalent, not a claim of verbatim OA text. | Producing a valid result and justifying the minimum are different demands. The problem supports comparison of plausible choices and a correctness argument without requiring obscure mathematics. |
| C3 — [Maximum Number of Events That Can Be Attended](https://leetcode.com/problems/maximum-number-of-events-that-can-be-attended/description/) — LC 1353, Medium | Goldman Sachs, Associate recruitment, round 3 DSA/projects interview; interview year not established by the accessible report | [First-person offer report](https://leetcode.com/discuss/post/1069708/Goldman-Sachs-Associate-or-3%20-Years-Experience-or-Offer/) names this exact question in round 3. **Moderate confidence:** detailed completed interview account, not employer verification. | Several initially plausible choices need to be compared against the precise rules and input size. A convincing explanation matters beyond making the examples pass. |
| C4 — [Sum of Subarray Minimums](https://leetcode.com/problems/sum-of-subarray-minimums/description/) — LC 907, Medium | PhonePe, SDE-1 campus recruitment, technical round 2, August 2022 | [First-person selected-candidate report](https://leetcode.com/discuss/post/3227140/PhonePe-or-SDE-1-or-Bangalore-or-Aug-2022-or-Selected/) gives the exact problem link and describes an optimization request followed by counterexample-driven correction. **Moderate confidence:** specific round and dated event, self-reported. | Provides a substantive step from an understandable baseline to a feasible approach. It also tests whether reasoning survives edge cases and a deliberate revision after a failed first implementation. |
| C5 — [Most Stones Removed with Same Row or Column](https://leetcode.com/problems/most-stones-removed-with-same-row-or-column/description/) — LC 947, Medium | Google, backend engineering, Bangalore onsite round 3; interview year not established by the accessible report | [First-person rejected-candidate report](https://leetcode.com/discuss/post/1138514/google-bangalore-onsite-backed-engineer-rejected/) explicitly identifies this exact problem and distinguishes explaining an approach from completing its implementation. **Moderate confidence:** direct candidate account, not independently verified. | The short rules leave substantial modeling work to the solver. It is useful for separating recognition and derivation from the ability to turn a justified approach into working code. |
| C6 — [Split Array Largest Sum](https://leetcode.com/problems/split-array-largest-sum/description/) — LC 410, Hard | PhonePe, SDE-1 campus recruitment, DoSelect OA, 3 August 2022 | The [same PhonePe report](https://leetcode.com/discuss/post/3227140/PhonePe-or-SDE-1-or-Bangalore-or-Aug-2022-or-Selected/) maps OA question 1 to this problem, reporting different, harder-to-interpret wording but the same underlying task. **Moderate confidence:** reported equivalent, not a recovered verbatim assessment. | A justified occasional Hard: the objective demands careful restatement, comparison of plausible approaches, and derivation under the constraints. It supplies a deeper reasoning attempt without making the company set a hard-only grind. |

All six public LeetCode statement pages were inspected and are available without opening an editorial. Difficulty labels come from those pages; the recognition-value judgments are planning assessments. No selection rests only on a company tag. The role seniority in a report does not establish this owner's level or the question's difficulty. C1 and C2 are retained; C3–C6 expand the set without a topic-balancing pass. These are public reports about completed recruitment processes, not confidential active assessments or answer-dump sources.

Research stops at this six-question company set. No extra company bank, alternative shortlist, or paid resource is proposed. Freshness is still owner-dependent: a previously seen or solved question is a revisit, not fresh-transfer evidence. If a company selection is already familiar, propose a replacement before counting it as a fresh attempt; do not silently relabel it. If a drawn pool question is confirmed familiar, record that fact and propose a blind replacement from the remaining unseen IDs; perceived ease, difficulty, or topic is never grounds for replacement. No such replacement is assumed now.

## Execution and logging

Use the same protocol for both sources:

1. Open only the statement. Reverse-read **output → input → constraints → story**, then restate the task in two lines.
2. Estimate feasible complexity; state the brute-force baseline and its bottleneck.
3. List plausible candidate approaches with rough complexity. Choose and justify one; state it aloud or in writing **before coding**.
4. Implement independently and test normally. A genuine stall means being able to explain what was tried, where it failed, and what is missing; difficulty alone is not a stall.
5. **Log in `ATTEMPTS.md` before consulting the key, editorial, discussion, or other outside reasoning.** Capture source/ID, date, outcome, pre-validation approach, confidence, stall details, and help used. Leave post-validation fields pending until validation actually happens.
6. Validate afterward: the pool's answer key for the drawn pool entries; the platform editorial or an explanatory discussion for C1–C6. Compare reasoning, not just acceptance by the judge. Close outside material and independently reconstruct/re-implement when repair is needed; then complete the validation fields.

No hints, tags, acceptance rates, solutions, discussions, or AI assistance before a genuine attempt or genuine stall. Any assistance must be recorded; an assisted solve is a miss for independent-recognition evidence, even if the submitted code passes. Do not inspect related-question recommendations. No solution or intended technique is supplied in this document.

## Misses and revisits

- Use the existing primary failure tags: `recognition`, `selection`, `derivation`, `implementation`, `constraints`, `complexity`, or `pressure`. Infer weaknesses only from actual attempts.
- Queue every miss, near-miss, and lucky solve in the existing `ATTEMPTS.md` revisit queue. Preserve the original entry.
- Revisit cold: blank editor, no notes or key, approach and complexity stated before coding. Close only after a clean, explainable solve. After a failed revisit, repair the reasoning and queue it again.
- Work revisits before or alongside new attempts, without fixed intervals. Any trigger notes are written during execution, in the owner's words, from actual misses; no pattern sheet is prepared now.

The candidate is **12 new-question attempts, split 6/6**. Misses generate additional cold-review work; revisits do not count as new questions or fill the twelve slots. If capacity becomes tight, they may displace unstarted new questions. Reduce the retained new-question selection across both sources to preserve approximately 50/50, allowing a difference of one for an odd total. Review follows actual misses and need not itself be balanced. Do not fabricate review work or add questions to satisfy a ratio; unresolved review may remain queued for the next slice.

## Pacing and observable evidence

Spread the 12-question candidate workload across roughly ten days alongside the other tracks. Some days can contain no LeetCode; others can contain more than one question. Interleave the sources without regrouping by topic. There is no daily quota, hourly schedule, assumed time per question, or completion streak.

Reserve room for validation, repairs, and cold revisits. Twelve is the requested candidate workload, not permission to sacrifice GATE or disregard actual capacity. If the combined new work and review becomes too large, defer unstarted questions while preserving the approximate new-question mix; unattempted pool entries remain unseen. Do not replace a difficult drawn question with an easier one. No contest, interview timer, or automatic expansion beyond twelve is added.

Expected evidence is up to twelve honest pre-validation logs, candidate approaches and complexity judgments stated before coding, independently attempted implementations, and a justified revisit queue or cold closures where achieved. This first sample should help distinguish repeated recognition/selection difficulties from derivation or implementation failures, while retaining problem-level context and help disclosures. A question count alone does not pass a milestone or establish a stable hit rate. No weakness, solve, closure, or progress is recorded during preparation.

## Deferred and awaiting acceptance

Deferred: further pool draws, additional company research, difficulty escalation, contests, mock interviews, broad consolidation, new trackers, pattern catalogs, and study notes or solutions generated in advance.

The owner has requested the 12-question, 6/6 candidate shape and blind pool draw. The final drawn set and company selections/sources remain proposals pending acceptance—especially C1's partially retrievable provenance and the reported-equivalent mappings for C2/C6. Actual capacity and prior familiarity determine final integration. No execution authorization or source acceptance is inferred from writing this file.

Only this candidate document is revised. `MAINTENANCE_PLAN.md`, `PROGRESS.md`, `ATTEMPTS.md`, `DECISIONS.md`, all master/strategy files, and the pool remain unchanged. No `leetcode/RESOURCES.md`, `current-sprint/`, `PLAN.md`, `CALENDAR.ics`, solutions, notes, or progress entries are created.
