# Master roadmap

> **Authority:** authoritative for strategy.
> **Owner of edits:** strategic reviews only, normally Grok 4.7. Sprint planning must not edit this file.
> **Status:** active
> **Last reviewed:** 2026-09-27
> **Review minutes:** [reviews/strategic/2026-09-27.md](reviews/strategic/2026-09-27.md)
> **Procedure:** [AI_WORKFLOW.md](AI_WORKFLOW.md)
> **Decisions:** D-018, D-019

This is the high-level plan from 2026-09-27 until LSEG joining, around August 2027. It decides phases, attention, and what a good end to the period looks like.

It is not a syllabus, a reading list, a weekly schedule, or a sprint. Domain roadmaps turn a phase outcome into milestones later. They do not get to change the bands below.

Facts and dates: [CURRENT_STATE.md](CURRENT_STATE.md). Intents: [context/GOALS.md](context/GOALS.md). Limits: [context/CONSTRAINTS.md](context/CONSTRAINTS.md). Do not restate those files here until a sentence would otherwise be misunderstood.

## Band meanings

Bands are not percentages and not weekly quotas. Capacity is unknown. A band is a ceiling and a priority, not a promise that the track appears in every sprint.

| Band | Meaning |
| --- | --- |
| `primary` | The phase is organized around this. A sprint that drops it needs a reason written in the plan. |
| `secondary` | Should show up across the phase. Yields to a primary when the week is actually too small. |
| `maintenance` | Keep it alive. A single sprint may omit it. A whole phase that omits it is off-strategy. |
| `paused` | Do not schedule it. Not a quiet permission to do it anyway. |
| `closed` | Leave active planning. Do not revive it without a strategic review. |

`lseg/` is not a track and has no band. Decision D-010.

## How priorities change

Two phases, plus a contingency that is not a phase.

1. **gate-window** — now until the GATE exam. GATE is the temporary priority. Other tracks continue only at the bands below, so the exam does not erase the rest of the year and the rest of the year does not erase the exam.
2. **post-gate** — after the exam, until joining. GATE leaves. System design and the income attempt become the center. Markets and beat production get more room. Neither becomes a new exam.

An LSEG internship, if it appears, is an overlay. It does not have a reserved block of time now. See below.

A strong GATE result does not retarget this plan toward higher studies or away from LSEG. That would be a new review, and only if you ask.

## Current phase

**gate-window.**

Started 2026-09-27. Ends on the GATE exam day, or earlier if you explicitly withdraw. The exam is owner-reported as around February 2027. The day is `unknown`. Do not invent it. When the day is known, update [CURRENT_STATE.md](CURRENT_STATE.md). A shift of more than about a month is a review trigger. A smaller correction is only a date update.

## Phases

| Phase | From | Until | Why it exists |
| --- | --- | --- | --- |
| `gate-window` | 2026-09-27 | Exam day, around February 2027 | GATE is a temporary priority and a backup attempt, not the career plan |
| `post-gate` | The day after the exam | Joining, around August 2027 | GATE should largely disappear. The professional and income work needs a real window |

Post-gate may include one close-out for GATE: write down that the attempt happened, or that you withdrew. That close-out is not a study plan. After it is written, or after one sprint has passed, GATE is `closed` for this horizon.

If joining moves into the GATE window, stop and review. Do not quietly compress post-gate out of existence.

## Attention

### gate-window (current)

| Track | Band | Role in this phase |
| --- | --- | --- |
| GATE | primary | A serious attempt at the paper you are actually sitting. Not a score chase |
| System design | secondary | Keep the learning arc moving. Conceptual continuity. Not a second full-time program |
| Product | secondary | Discovery and small tests only. Not a multi-week private build |
| Beat production | maintenance | The craft stays alive through finishes, not through a second syllabus |
| Markets | maintenance | Slow-burn stays warm. Not another exam |
| LeetCode | maintenance | Stay fluent. No sheet, no quota, no required contest |

### post-gate

| Track | Band | Role in this phase |
| --- | --- | --- |
| GATE | paused, then closed | Close-out only, then gone. No new study |
| System design | primary | Move from concepts into guided practice and independent application |
| Product | primary | The real income attempt: ship, price, distribute, or kill on evidence |
| Beat production | secondary | More room for finishes and technique. Still not a career track |
| Markets | secondary | Broader practical understanding. Still not a syllabus, and not team-specific |
| LeetCode | maintenance | Same ceiling as before. Contests stay occasional and optional |

A domain file copies the current band from this table. It does not edit the table.

## When the week is too small

Capacity is `unknown`. Do not invent hours. If a sprint cannot hold every band, yield in this order. Do not change the bands themselves. That is a review.

**gate-window**

1. Keep GATE.
2. Keep some system-design continuity. The arc should not go to zero for months.
3. Beat production, markets, and LeetCode may be omitted for a sprint. Omitting them for the whole phase is not allowed.
4. Product discovery yields before system-design continuity. It does not yield before GATE.

**post-gate**

1. Keep system design and the product attempt if both can be real. They are both primary on purpose.
2. If both cannot fit, do not silently demote one. Escalate to a strategic review.
3. Beat production and markets yield before either primary is dropped.
4. LeetCode yields first.

Unknown capacity is not a reason to mark ordinary weeks Intensive. A mock week, the exam week, or a real deadline may justify Intensive. Ordinary weeks should not. Calendar mode is still chosen in the sprint plan, not here.

## Streams

Detailed content is a later domain pass. This section is role, timing, and maturity only.

### GATE

Backup and security, not the main direction. Primary only in gate-window.

A serious attempt, with no score target, means all of the following:

- The paper is the one you are registered for. It is `unknown` here. Do not assume CS.
- You can sit the whole paper, not a symbolic registration.
- You have used past questions or mocks under exam conditions enough to know your weak areas from evidence.
- You sit the exam, unless you explicitly withdraw.

"Good" is not a number. It means you prepared as a real candidate. Current level and materials are `unknown`. The domain pass must get a baseline from you. It must not invent one, and it must not start from a fake zero.

After the exam, the track closes. A result, good or bad, does not by itself change LSEG joining or the other bands.

### System design

This is the main professional depth track of the horizon. The goal is skill, not familiarity with terms and not a memorized set of interview diagrams.

The arc, in order, and comfortably paced:

1. Conceptual understanding.
2. Guided or hands-on learning.
3. Implementation and independent application.

End capability by joining: take requirements and constraints, compare more than one viable design, explain the trade-offs, justify a choice, and do that with a repeatable process. That should be enough for the kind of system-design interview expected after some professional experience, and it should also be real engineering understanding, not only interview prep.

gate-window: secondary. Keep one thread moving, mostly in the conceptual stage unless you already know you are past it. Do not open several implementation projects beside the exam. Existing depth is `unknown`. Do not assume a beginner start.

post-gate: primary. Move into guided practice and then independent application. Success is the capability above, plus at least one implementation that forced a constraint to be real. Not a count of topics covered.

Topic order, resources, and project choice belong in the domain pass. The unordered scope already listed in [context/GOALS.md](context/GOALS.md) is not a sequence and is not repeated here.

Stack: default to the stack you already know, where it is sufficient. Deviation is allowed when the system or the learning objective actually needs it. See [context/CONSTRAINTS.md](context/CONSTRAINTS.md) and D-019. Do not switch for variety. Do not treat Node/TypeScript as a ban.

### Product

One real attempt at independent software income before joining. The work is discovery, validation, shipping, pricing, distribution, paying users, and iteration. "Build projects" does not count. No idea is chosen here.

gate-window: secondary, and only as discovery and small tests. A build that needs weeks of private work is out of phase, unless a tiny test is already validated and stays small.

post-gate: primary. This is the window to ship and charge if the evidence says to continue.

Kill rule, so a hidden build cannot happen by drift: if an experiment runs about three sprints without the evidence bar in `product/VALIDATION.md` moving, kill it or change it. Do not extend it by default. Outside evidence beats a finished private build. No revenue target is set. An honest kill counts. A repo nobody else touched does not.

Acceptable shapes remain the ones you already named. None are selected.

### Beat production

A serious craft. Not a career, an audience, or an income track. Decision D-011.

gate-window: maintenance. The point of the band is that the craft is not dropped and not turned into a program. Finished pieces matter more than tutorials. No beats-per-week quota. Skipping one sprint is allowed. Going the whole phase with no finishes is not.

post-gate: secondary. More room. Same non-goals.

"Genuinely good" is your judgment only. Setup is `unknown`. The domain pass must not assume a DAW or buy a stack of tools on your behalf.

### Markets

Slow practical understanding. Personal interest is enough. LSEG relevance is real and is not a guess about your team. Team, role, and business line are `unknown`.

gate-window: maintenance. Warm, not a second syllabus.

post-gate: secondary. Still general. Do not specialize to a guessed desk.

Enough, by joining: you can explain in your own words how the main pieces fit — what the major instruments are for, how a trade becomes a settled position, what market data and risk are doing, and where a markets-infrastructure firm can sit. Not a license, a forecast record, or every subtopic mastered. Deeper, team-specific study waits until a team is known, and even then only after a review.

No reading list in this file.

### LeetCode

Maintenance only. Decision D-009. You already know DSA. The ceiling is fluency, topic rotation, and occasional contests. No beginner course, no placement sheet, no daily quota, no rating target.

Both phases: maintenance. Contests are optional in both, and may be skipped for the whole GATE window without that counting as abandoning the track. Weak areas must come from problems you actually missed, not from a generic list. Cadence is a domain detail, and it must stay small enough that it cannot become the identity of a sprint.

### LSEG notes

Not a stream. No curriculum. Internship notes and joining logistics go in `lseg/` only when there is something real to put there.

## If an internship happens

None is offered or accepted. Do not hold time empty for one.

When an offer exists, update [CURRENT_STATE.md](CURRENT_STATE.md) and hold a strategic review before changing bands. Until that review, this default applies:

- Internship hours are fixed commitments. They are not sprint achievements and not a new study track.
- If it falls in gate-window: GATE stays primary. Shrink system design and product first. Do not cancel the exam attempt to make the internship comfortable.
- If it falls in post-gate: system design stays at least secondary, so the arc does not go to zero. Product may have to drop from primary; a live experiment with evidence is time-boxed harder, not automatically killed. Beat production drops to maintenance, not to nothing. Markets and LeetCode may pause.
- Refused even then: a framework tour, a placement grind, a secret product build, or an `lseg/` folder that becomes a second engineering curriculum.

## Checkpoints

These are transitions, not tasks.

| When | What changes |
| --- | --- |
| GATE paper becomes known | Date update in current state, plus the domain plan. Strategy does not assume the paper |
| Exam date becomes known | Date update. Review only if it moves by more than about a month |
| Exam day | gate-window ends. Next sprint uses post-gate bands, plus at most a GATE close-out |
| You withdraw from GATE | Same transition as exam day. Record the withdrawal. Do not invent a replacement exam |
| Internship offer | Strategic review. Do not improvise the bands in a sprint |
| Team, role, or joining date becomes known | Update current state. Light logistics may go in `lseg/`. Do not rewrite markets or engineering around a guess. Review only if joining moves into the GATE window, or the team fact actually changes what "enough" markets means |
| About monthly | Drift check, not a new strategy. See the monthly review template |

## Success by joining

Around August 2027, this period went well if you can point at the following. No numeric targets were set, so none are implied.

- GATE: you sat the exam, or you explicitly withdrew. There is a short record of which. No score goal.
- System design: faced with an unfamiliar problem, you can name requirements and constraints, compare more than one design, and justify a choice, including what you give up. At least one implementation exists that you can explain. A finished playlist is not this.
- Product: at least one experiment met the evidence bar. It ended in real outside use, payment, or a written kill that cites the evidence. A private build alone does not count.
- Beat production: finished beats exist, and you have named some you consider genuinely good. Tutorial time does not count.
- Markets: you can give the explanation under "enough" above, in your own words.
- LeetCode: you are not starting DSA over. No rating goal.
- The LSEG path is intact, unless a later review records that you changed it on purpose.

## What should not receive attention

Standing non-goals in [context/CONSTRAINTS.md](context/CONSTRAINTS.md) stay in force, including: no framework tourism, no placement grind, no beat-production career plan, no second engineering curriculum in `lseg/`, no hidden six-month product, no extra tracks.

Also out, for this horizon:

- Score targets, revenue targets, beat quotas, and problem quotas
- A reserved empty block for a hypothetical internship
- Specializing markets to an unknown LSEG team
- Treating a good GATE result as an automatic change of career plan
- Life after joining, except light logistics once a date or team is real
- Certifications, licenses, and day-trading, unless you later ask
- Filling ordinary weeks as if capacity were known

gate-window specifically: no second exam out of markets or LeetCode, and no product build that crowds the attempt.

post-gate specifically: no lingering GATE schedule, and no promotion of beats or markets into the new primary just because the exam is over.

## Assumptions

Labeled so a later review can drop them.

- The exam stays around February 2027 and joining stays around August 2027. Both are owner-reported and approximate.
- No internship will be scheduled until one exists.
- Unlogged skill is not zero. Domain passes must not invent a beginner baseline.
- The GATE paper is not CS until you say it is.
- Two post-gate primaries are intentional. If life cannot hold them, the response is a review, not a quiet cut.
- Node/TypeScript remains the default practical foundation, not a cage. D-019.

## Unresolved

Decided around, not invented:

- Exact exam day, joining day, team, role, office, whether the package figure is CTC
- Weekly capacity and other obligations. Sprints stay small until you report this. It blocks a honest sprint more than it blocks a domain pass
- GATE paper and current preparation level. These block a GATE syllabus. They do not block the other domain passes. The GATE domain pass should start by establishing the paper and a coarse baseline, and should stop there until you supply them
- Music setup, budget, and existing depth in system design or markets. Domain passes ask or work with what you have. They do not shop, and they do not assume zero

Nothing else in the unknown list needs an answer before domain planning begins.

## Explicitly not in this file

- Topic order, book lists, course lists, problem lists
- Product ideas
- Sprint tasks and calendars
- Live metrics and hour budgets

## Changelog

- 2026-09-27 — Skeleton created. No strategic decisions.
- 2026-09-27 — First strategy adopted. Phases `gate-window` and `post-gate`. Minutes: [reviews/strategic/2026-09-27.md](reviews/strategic/2026-09-27.md). D-018, D-019.
