# Product input for Sprint 001

> **Status:** proposal pending owner acceptance under D-006.
> **Prepared:** 2026-09-29.
> **Purpose:** candidate input for the later integrated, approximately 10-day sprint. No active sprint or product idea is created.
> **Authority:** the previously read [MASTER_ROADMAP.md](../MASTER_ROADMAP.md), [CURRENT_STATE.md](../CURRENT_STATE.md), and [AI_WORKFLOW.md](../AI_WORKFLOW.md), plus [ROADMAP.md](ROADMAP.md), [PROGRESS.md](PROGRESS.md), [IDEAS.md](IDEAS.md), [VALIDATION.md](VALIDATION.md), and [RESOURCES.md](RESOURCES.md), read for this pass. `EXPERIMENTS.md` was left unopened in accordance with the request's specific prohibition.

## Starting point and intended outcome

**E1 — Problem discovery; no idea selected and no investigation logged.** The candidate outcome is a small, evidence-backed set of problem observations worth investigating, if reality supplies them. Each should identify a person or user group, current behavior, observable friction, and a source. No minimum idea count is imposed; an honest record that nothing inspected yet qualifies is preferable to invented candidates.

Product remains secondary during `gate-window`, with E1–E3 permitted by the roadmap. **This slice is E1, with a conditional E2 conversation only.** GATE remains primary; when capacity is tight, Product discovery yields before system-design continuity. Existing software-building ability needs no new coding curriculum.

## Recommended discovery approach

Follow one narrow thread: **observe ordinary work → capture concrete behavior → check the source and recurrence → decide whether a conversation is warranted.** Do not begin with a product format or search for things to build.

Start with one recurring workflow the owner already performs. Observe it while doing real work rather than staging a problem hunt. Note interruptions, repeated manual steps, workarounds, and actual consequences when they occur. Personal inconvenience is a discovery clue; it is not outside validation.

Then inspect **one** public surface below, choosing the one whose users and context the owner understands. The second is a fallback, not another mandatory research stream. Follow a promising observation far enough to understand what happened and whether it still happens; stop browsing when a concrete follow-up is available. Do not collect a large bookmark backlog.

## Concrete discovery surfaces

These are observation locations, not selected markets or recommendations to build developer tools. Only the public listing pages were checked during preparation; no individual issue was mined into a candidate.

| Surface | Why it is useful | Bounded execution guidance and limitation |
| --- | --- | --- |
| The owner's existing workflow, observed during normal use | Direct access to the sequence of actions, recurrence, and effort; no new audience or domain needs to be invented | Choose a workflow actually repeated, not a hypothetical one. Record the occasion and what happened. Label it **owner observation only** until outside evidence exists. |
| [Next.js GitHub Discussions](https://github.com/vercel/next.js/discussions) — proposed first public surface | Public user discussions are accessible, and the owner's existing React/Next.js background can reduce the effort of understanding the context | Inspect recent user questions describing actual work, attempted remedies, or unresolved constraints. Follow the discussion through its latest response. Skip showcases, vague feature wishes, and questions resolved by a straightforward documented answer unless independent evidence shows continuing friction. Familiarity makes observation easier; it does not establish commercial demand. |
| [VS Code GitHub issues](https://github.com/microsoft/vscode/issues) — fallback if this is a tool the owner knows | Reports and follow-up comments can document affected workflows, repeated symptoms, and workarounds; the inspected listing had current September 2026 activity | Search within a familiar workflow and sort by recent updates. Read the original report and latest resolution together. Distinguish individual user accounts from maintainer/bot activity. A transient upstream defect or popular feature request is not automatically an independent product opportunity. Issue creation is restricted on the inspected listing; do not assume posting or access to affected people. |

Use dates and the current resolution status rather than upvotes to judge whether a signal remains relevant. Public posts make behavior observable; they do not guarantee that a user is reachable, willing to talk, or willing to pay. No outreach is sent during preparation.

## What evidence to look for

During execution, capture enough to answer:

- **Who:** whose workflow is affected, in what role and situation? Separate the user, decision-maker, and payer when the source supports that distinction.
- **What happens today:** what task were they trying to finish, what steps do they take, and what workaround or substitute do they actually use?
- **Recurrence:** is this a repeated event, an isolated failure, or a claim without an example? Different people repeating the same slogan is weaker than independent accounts of actual behavior.
- **Cost:** what time, money, effort, or risk is observable or explicitly reported? Preserve the source's units and context. Write `unknown` when no cost is established; do not manufacture savings or market size.
- **Source and freshness:** link the exact post/comment or record the dated personal observation. Separate the person's words, observed facts, and the owner's interpretation. Check whether a subsequent fix removed the friction.
- **What remains unproven:** recurrence elsewhere, importance, reachability, buyer identity, and willingness to pay may all remain unknown. Existing spending is useful evidence, but lack of spending does not erase a costly workaround or tolerated pain.

An unsupported request, compliment, or interesting implementation challenge should not become a candidate merely to fill the inbox. Do not convert observations into feature lists or solution sketches.

## Candidate execution activities and relative pacing

1. **Opening:** choose one familiar workflow and one public surface. Revisit the E1 section of `ROADMAP.md` and the evidence table in `VALIDATION.md`; no additional course is needed.
2. **During ordinary work:** capture concrete episodes as they happen. Use one focused public observation pass to look for accounts of current behavior, not broad startup inspiration.
3. **Later return:** check the most credible observations against the full source, current status, and any independent corroboration. Discard weak or already-resolved leads. If evidence merits it, consider the focused conversation below.
4. **Close the slice:** review what was actually learned, which candidates warrant continued discovery, and what remains unknown. If no candidate qualifies, retain an honest account of the inspected scope and why its signals were insufficient in the later sprint review; do not claim that a whole market has no problems.

These are a few small discovery activities spread across approximately ten days, with no daily quota, idea target, or assumed hourly budget. Observation can accompany existing work. Source checking and a conditional conversation should take precedence over browsing more communities. If capacity tightens, drop the fallback surface and further browsing first; do not borrow from GATE to fill an idea list.

## Recording findings during execution

Only after the owner encounters evidence, use the existing `IDEAS.md` format and next unused `I-NNN` ID. The owner must state or accept the entry; preparation does not supply one.

- Use a problem description as the name and one-sentence problem field, without naming a product.
- Identify who has it. In **Outside signal**, record the dated source, current behavior, recurrence, and known cost. If there is no outside signal, explicitly label **personal observation; outside evidence not yet established**.
- Keep observations distinct from inference and uncertainty. A small useful excerpt or faithful paraphrase plus a source link is enough; do not copy whole discussions.
- In **Why it might be small enough**, describe only the observed boundary of the problem. If that is not established, write `unknown`; do not invent a feature scope or implementation estimate.
- Keep status `inbox` while investigating. Mark a discarded candidate honestly when warranted; do not promote one simply because the sprint ended.

This pass changes neither the inbox nor its template and creates no notes or findings on the owner's behalf.

## When an E2 conversation is justified

A focused conversation is reasonable when a candidate identifies an affected person or role, a concrete recent occurrence, current behavior or a workaround, and a specific uncertainty that talking to an affected person could resolve. There should be a plausible, appropriate way for the owner to reach such a person. A recurring owner observation may justify checking whether another person shares it; it cannot validate itself.

If that evidence emerges, the later integrated sprint may include a brief owner-led conversation about the person's **last actual occurrence**, what they did, how often it happens, its consequences, and what they have already tried. Ask for behavior and context without pitching a solution or asking for hypothetical enthusiasm. Do not prepare outreach copy, a product hypothesis, or an experiment now.

The E1 gate still requires the roadmap's candidate pipeline with named users, behavior, and sources. Passing E2 requires a real person describing the problem in their own words, current behavior, evidence they would notice relief, and a way to find more affected people. A scheduled conversation, agreement with the owner, or ten elapsed days does not pass either gate.

If a conversation later occurs, retain its factual account with the candidate for review. The `VALIDATION.md` finding template asks for an experiment link even though E2 precedes an E3 experiment: do not invent an experiment to fill that field. At execution-time recording, explicitly identify it as pre-experiment E2 evidence and link the candidate. No finding or experiment is created in this preparation pass.

## Teaching material, evidence, and deferrals

**No external teaching resource is needed for Sprint 001.** The roadmap's E1/E2 guidance and validation evidence model already cover the required behavior. The public surfaces above are observation sources, not courses or a replacement method.

Observable evidence from the slice would be owner-created candidate entries supported by actual observations, clear separation of personal and outside signals, known costs and explicit unknowns, and a reasoned decision about which observation deserves follow-up. A conversation counts only if it occurs. No milestone, user, demand, or revenue is inferred from this proposal.

Explicitly deferred: choosing a product or niche; AI-generated problems; feature lists; E3 landing pages, prototypes, pricing/payment tests, and experiment design; E4–E7 work; implementation plans and builds; courses, competitor databases, and broad trend research.

## Decisions awaiting acceptance

- Accept this bounded E1 approach and choose the public observation surface that fits the owner's actual familiarity; the fallback is optional.
- Accept the linked surfaces as proposed sources. `RESOURCES.md` remains unchanged.
- At integrated planning, fit discovery around real capacity and GATE. Include an E2 conversation only if an evidence-backed candidate and reachable person naturally emerge.

Only `product/SPRINT_001_PREP.md` is added. Ideas, experiments, validation findings, progress, resources, roadmap, strategy, and active-sprint files remain unchanged. All selections remain proposals.
