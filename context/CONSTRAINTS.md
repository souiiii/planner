# Constraints

> **Role:** standing limits. These stay in force across phases unless a strategic review supersedes one and records a decision.
> **Authority:** authoritative for non-goals and planning limits listed here.
> **Not a schedule.** Capacity is unknown; see [CURRENT_STATE.md](../CURRENT_STATE.md).
> **Last reviewed:** 2026-09-27
> **Stack rule:** revised in the first strategic review. Decision D-019.

## Horizon

Plan from September 2026 until LSEG joining, around August 2027. Do not build a system that assumes life after joining is in scope, except for light joining prep when that becomes timely.

## How this repo is allowed to work

- Markdown and light structure only. Not an application, not a database, not a pile of scripts
- One integrated 10-day sprint, not a sprint per track
- Plans must leave slack. Do not schedule every hour, and do not assume every day is productive
- Capacity is unknown until the owner reports it. Small plans beat fantasy plans
- Unfinished sprint tasks are not copied forward automatically
- Several models will edit this repo. They must follow [AI_WORKFLOW.md](../AI_WORKFLOW.md) so they do not each create a private plan

## Standing non-goals

These came from the owner. They are not optional style advice.

- Do not make the main engineering activity "learn random new frameworks"
- Do not restart a placement-style DSA grind. Maintenance is the ceiling unless the owner later asks otherwise
- Do not turn music-making into career optimization, audience growth, or an income project
- Do not turn `lseg/` into a second generic software curriculum
- Do not treat GATE as the main career direction. It is a backup attempt
- Do not spend months secretly building a product nobody has been asked about. Fast experiments beat a hidden six-month build
- Do not invent extra life tracks to make the system look complete
- Do not accumulate endless TODO lists that are never deleted

## Stack constraint

The default practical foundation is the stack you already know: JavaScript / TypeScript, Node.js, Express, React / Next.js, SQL, and MongoDB. Use it where it is sufficient. Do not switch language, framework, database, or infrastructure for variety. That would be the framework tour this repo already refuses.

This is not a hard ban. A domain plan may use another language, technology, database, infrastructure tool, or framework when there is a genuine reason: the system cannot be understood or built honestly on the default stack, or the learning objective is that different tool, not novelty. Write the reason in the domain plan. An ordinary deviation does not need a strategic review.

A new default for the whole horizon does need a strategic review and a decision.

Docker, AWS, CI/CD, Redis, Kafka, and similar production topics are allowed when they serve backend depth. They are not a required checklist, and adopting one of them is not "switching stacks for variety." The domain pass decides whether any of them belongs in a given phase. This file does not sequence them.

## Creative constraint

Music-making is a personal passion and a serious craft. Finished music matters more than watching tutorials or collecting tools. Models must not reframe it as "personal branding", "content pipeline", or "useful for interviews" unless the owner asks, and must not push gear purchases. The planning language covers the whole craft: beat-making, vocals, recording, and mixing into finished songs, not beats alone. Decision D-021.

## Product constraint

Independent income is a real goal before joining, not a slogan. The bias is small products with obvious utility: desktop utilities, browser extensions, micro-SaaS, creator tools, developer tools, workflow tools, and similar. The skills to practice are problem discovery, validation, shipping, pricing, distribution, getting paying users, and iterating. "Build projects" by itself does not count.

## What is not known, and must not be filled in

Time available, other obligations, GATE paper, budget, music setup, LSEG team. Canonical list: [CURRENT_STATE.md](../CURRENT_STATE.md).

## Superseding a constraint

Requires a strategic review and a decision entry. A sprint plan cannot suspend a standing non-goal for convenience.
