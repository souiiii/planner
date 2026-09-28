# System design and backend depth

> **Role:** domain roadmap and learning path for backend and production depth. Future interview competence is a supported outcome, validated late and never the center.
> **Authority:** subordinate to [MASTER_ROADMAP.md](../MASTER_ROADMAP.md) for phases, attention bands, non-goals, and the end capability. This file designs the sequence, exercises, and gates inside those bounds.
> **Status:** active
> **Last reviewed:** 2026-09-28

## Purpose

Become genuinely stronger at system design and backend / production engineering, on the stack you already use, so that you can take requirements and constraints, compare more than one viable design, explain the trade-offs, justify a choice, and do that with a repeatable process. Intent: [context/GOALS.md](../context/GOALS.md). End capability: master roadmap, System design stream.

Two outcomes, equally required:

- **Real engineering understanding.** You can reason about a system that exists or is proposed — where it breaks, what it costs, what you give up — and you can prove key parts by building them.
- **Future interview competence.** You can defend a design out loud in an interview-style round. This is a validation of the first outcome, not a separate curriculum.

This is not a terminology roadmap, not a memorized set of standard interview diagrams, and not a framework tour.

## Starting point (owner-stated 2026-09-28)

- Software-development experience is real: JavaScript / TypeScript, Node.js, Express, React / Next.js, SQL / MongoDB, general web and backend work. [context/PROFILE.md](../context/PROFILE.md).
- The default stack is the default where it is sufficient — not a restriction. Deviations are allowed with a stated reason. [context/CONSTRAINTS.md](../context/CONSTRAINTS.md), D-019.
- Current system-design depth is `unknown`. No proficiency level, no project inventory, and no production exposure were reported.
- Therefore: **each stage's learning phase doubles as calibration.** If the concepts and guided material are already familiar and you can pass the gate, that stage compresses to a verification pass and you move on. Nothing here assumes a zero baseline, and nothing assumes you are past the stage gates.

## How this path works

- **Ability-gated, not calendar-gated.** Stages are ordered by dependency and by the difficulty of the reasoning each demands. The pace is not scheduled. Move on when a stage's criteria are demonstrated, not when time has passed. No dates, quotas, or project counts.
- **Learn, see it applied, practice, build where useful, then apply.** Every stage follows the same order: concepts first, then guided examples and worked walkthroughs, then hands-on exercises, then implementation where it makes the capability real, and only then an independent version on unfamiliar material. You are never expected to produce a cold design at the start of a stage.
- **Guided learning is real learning.** Courses, books, tutorials, video walkthroughs, and documented case studies are valid teaching tools here, not emergency gap-fillers. They count when consumed actively: notes, reproductions, extensions, explain-it-back. Watching or reading without any of that is not practice.
- **Requirements before solutions.** Every synthesizing exercise starts from a brief: users, traffic shape, data shape, scale, latency, cost, operational constraints. Constraints are separated into hard constraints, preferences, and invented assumptions.
- **At least two viable designs, always compared.** A design without an alternative is not a design decision; it is a preference. Trade-offs are named in terms of what each option makes easy, hard, and expensive.
- **Every added component must justify itself** (a load balancer, a cache, a queue): what it buys, what it costs, and what new failure mode it introduces. "Standard practice" is not a reason.
- **Written artifacts and implemented proof.** Designs, teardowns, and notes are written; formatting does not matter. An implementation counts as evidence when it demonstrates the stage capability or settles a claim you could not settle on paper.
- **Evidence over feelings.** Claims like "this scales" or "this is consistent enough" are settled by measurement, a written argument, or a small build. Not by confidence.
- **Stack default, deliberate deviations.** Use the Node/TypeScript stack where it is sufficient. Deviate when the exercise genuinely requires another tool or the learning objective is that tool; record the reason in [projects/README.md](projects/README.md) or [RESOURCES.md](RESOURCES.md). Not for variety.
- **Interview practice is validation, not the curriculum.** It activates only after independent design reasoning exists, and it never dominates. See the section below.
- **Band respect.** During `gate-window` this track is secondary: keep the arc moving with one thread at a comfortable depth. After the exam it is primary. The master owns bands and yield order.

## Scope

In scope: the unordered topics from [context/GOALS.md](../context/GOALS.md) — system design, distributed systems fundamentals, databases, networking where it matters, caching, Redis, Kafka / queues / event-driven architecture, scalability, reliability, observability, Docker, AWS, CI/CD, production engineering. This roadmap sequences them by capability, not by checklist.

Out of scope:

- Learning frameworks or tools for their own sake.
- A second DSA / LeetCode program.
- Collecting standard interview questions or diagrams as the main activity.
- Application code inside this planning repo. Implementations live in their own repositories; link them from [projects/README.md](projects/README.md). D-013.
- Specific books, courses, or talk lists chosen by a model. D-006.

## Stages

The arc moves from precision to judgment to independent synthesis: exactness about requirements → cost judgment on one machine → reasoning across the network → data decisions → asynchronous systems → reliability and operations → independent, defended design. Every stage runs the same internal order: learn, see it applied, practice, build where useful, apply independently.

### S1 — Requirements and constraints

**Develops:** the first half of the master's end capability — take requirements and constraints and turn them into a precise problem statement. Without this, every later comparison is guesswork.

**Work**

- **Learn:** functional versus non-functional requirements; the constraint categories (scale, latency, consistency, cost, compliance, operational); how experienced designers separate hard constraints from preferences; how a brief becomes a problem statement. A course, a book chapter, or a worked walkthrough is a fine way to learn this.
- **See it applied:** study worked requirement analyses for systems that are documented — a public design doc, a case study, a course example. For each, note what the designers treated as fixed, what they assumed, and which requirement dominated.
- **Practice (guided):** reproduce that analysis on a system you know or use, then check it against how the system actually behaves or against a documented account. Repeat on systems with a shared constraint (all chat, all feeds, all payments) to separate domain requirements from generic procedure.
- **Apply (independent):** take a short brief you have not seen and produce the constraint list, labeled assumptions, and the dominant requirement without a worked example in front of you. Ask the sharp questions: what breaks if the system is 10× bigger, 10× slower, or down for an hour; which requirement would you cut first if forced.

**Move on when**

- you can turn a short brief into a constraint list and an explicit statement of what you are unsure about, with no "we'll figure it out later" holes;
- your assumptions are labeled and falsifiable, and you can say which requirement dominates the design and why.

### S2 — One machine, measured: latency, throughput, resources

**Develops:** cost judgment before scale reasoning. Most "distributed" problems are single-machine problems wearing a costume.

**Work**

- **Learn:** latency versus throughput; percentiles and why averages lie; queueing and saturation; profiling concepts; how to read a latency distribution and find the knee of the curve. Back-of-envelope estimation: data volume, bandwidth, memory per connection, request rate versus capacity, with stated assumptions.
- **See it applied:** follow a guided profiling or performance walkthrough on your stack — a tutorial, a course lab, or a documented teardown — and watch how an experienced engineer finds the bottleneck and justifies the fix.
- **Practice (guided):** reproduce that walkthrough on your own machine: request latency distributions (p50/p95/p99), throughput ceilings, error rates, resource saturation (CPU, memory, disk, connection pools). Run controlled changes — concurrency, an index, a connection pool — and write down what was expected, what happened, and why.
- **Apply (independent):** find a real bottleneck in a system you run and justify the fix with a measurement; estimate the next limit with stated assumptions, then check the estimate against what you measure.

**Move on when**

- you can find a real bottleneck in a system you run and justify the fix with a measurement, not a guess;
- your estimates come with assumptions and are within a comfortable order of magnitude of what you measure;
- you can articulate why a naive single-machine design fails next, and at roughly what scale.

### S3 — The distributed request path

**Develops:** reasoning about requests, components, and coordination across more than one machine. The first genuinely "system design" stage.

**Work**

- **Learn:** what each hop in a request path is for — DNS, CDN or edge, load balancer, application instances, caches, databases, external services; load balancing and stateless services; caching economics, key design, invalidation, stale reads, cache stampedes; synchronous versus asynchronous handoff; failure propagation, timeouts, retries, idempotency keys, backpressure, retry storms; when a cache is the wrong answer.
- **See it applied:** study a documented architecture — an engineering blog, a tech talk, a course case study — and trace its request path hop by hop. Follow a guided lab that adds a cache or a load balancer to a small service and shows the effect.
- **Practice (guided):** reproduce the lab on your stack; add caching, load balancing, and throttling step by step; observe hit/miss behavior, duplicate work, and what breaks when you kill a dependency.
- **Apply (independent):** write the request-to-response narrative for a realistic system, with the alternatives at each hop and each choice defended in a line. Build or extend an implementation far enough to prove the claims the narrative rests on, and link it from [projects/README.md](projects/README.md).

**Move on when**

- you can explain a real request path end to end, noting what is load-balanced, cached, or queued, and why, including the failure and duplicate-work cases;
- you can defend the synchronous/asynchronous split and name the operational cost of each new component you add;
- an implementation exists that proves the claims the narrative relies on.

### S4 — Data as a first-class design decision

**Develops:** the durable half of most designs — storage choice, transaction boundaries, and consistency judgment. This is where production and interview rounds both separate people who "use a database" from people who reason about one.

**Work**

- **Learn:** storage models and when each fits (relational, document, key-value); schema design; indexing; reading query plans; transactions and isolation — read/write anomalies, locking versus MVCC, what the database guarantees versus what the application must handle; replication and partitioning — leader/follower, failover, replication lag and reads, sharding keys and hotspots, resharding pain; strong versus eventual consistency for a given feature.
- **See it applied:** take a guided example (a course, a book, a documented case study) where the storage decision is explained, and follow how the access pattern drove the choice. Walk through query-plan and index examples before writing your own.
- **Practice (guided):** on your own database, inspect query plans, change an index and measure the difference, and observe a transaction or isolation behavior in the docs' guided examples. If replication or sharding matters to the brief, set up a modest guided version.
- **Apply (independent):** design the data layer for a realistic brief and defend the storage choice against the alternative with index, query, and consistency reasoning; implement enough of it to demonstrate the decision's consequences — an explicit index design, a transaction boundary, or a modest replication/sharding setup — and note the result.

**Move on when**

- you can map an access pattern to a storage choice and back up the choice with index and query reasoning;
- you can name the transaction or consistency trap in a given flow and the mitigation;
- you have a build where the data decision, not the framework, is the interesting part.

### S5 — Asynchronous flow, queues, and event-driven systems

**Develops:** designing systems where work is decoupled in time — the modern default for feeds, notifications, payments, and pipelines.

**Work**

- **Learn:** when to queue — synchronous request/response versus a queue, an event log, or a stream; ordering; delivery semantics (at-least-once, at-most-once, effectively-once); replay, dead letters, poison messages; idempotent consumers, deduplication, and outbox/inbox patterns; event schemas and versioning; when an event should be a command instead.
- **See it applied:** follow a guided walkthrough of a producer/consumer flow — a course lab, a tutorial, or a documented system — and note where it handles retries, duplicates, and poison messages.
- **Practice (guided):** build that flow on your stack with a durable queue or log; then extend it with retry/backoff and a dead-letter path, and observe what duplicate delivery actually does.
- **Apply (independent):** decide synchronous versus queued for a realistic feature and defend it against a counterexample; build the flow far enough to demonstrate idempotent, retryable consumers and duplicate-safe delivery rather than asserting it.

**Move on when**

- you can decide synchronous versus queued for a feature and defend it against a counterexample;
- you can trace a message through the system across failures and retries and say exactly what happens to a duplicate;
- the implementation demonstrates idempotency rather than asserting it.

### S6 — Reliability, operations, and production reasoning

**Develops:** how systems behave when the happy path goes wrong — the stage that converts "design" into "engineering."

**Work**

- **Learn:** containers, environments, configuration and secrets, migrations and rollbacks; logs, metrics, and traces and what each answers; alerting on symptoms rather than causes; graceful degradation, timeouts, circuit breakers, bulkheads, rate limiting; the difference between "unavailable" and "wrong"; incident reasoning — recent-change, dependency, saturation, and data-corruption checks; backup/restore and cost behavior under load.
- **See it applied:** read public incident write-ups and postmortems with a fixed question list: what was expected, what happened, what signal would have caught it earlier, what changed after. Follow a guided observability setup for a small service.
- **Practice (guided):** on a sample or your own system, run staged failure drills — kill a dependency, saturate a pool, add latency, split the network — and compare what broke with what the guided material says should happen. Set up the logs, metrics, and traces you would want at 3 a.m.
- **Apply (independent):** for a system you own, name the top failure modes and the intended behavior under each; survive or degrade correctly in a staged drill and explain what you fixed; reconstruct an incident from observability signals and write a short blameless postmortem ending in concrete changes.

**Move on when**

- you can describe, for a real system, its top failure modes and the intended behavior under each;
- an own system survives or degrades correctly in a staged failure drill and you can explain what you fixed as a result;
- you can reconstruct an incident from logs, metrics, and traces, and write a blameless postmortem that ends in concrete changes.

### S7 — Independent design reasoning for unfamiliar systems

**Develops:** the full master capability, on systems you have not seen — the graduation stage.

**Work**

- **Learn:** study how senior designers structure a design document — how they frame requirements, present alternatives, and state trade-offs. Work through published case studies and note the reasoning, not the diagrams.
- **See it applied:** walk through fully worked designs with a rubric beside you (requirements clarity, alternatives compared, trade-offs named, failure analysis, decision defended). Compare their reasoning with what you would have said at each fork.
- **Practice (guided):** apply the process to briefs close to systems you know, with the rubric and a critique from a peer, mentor, or model acting as reviewer; revise from the critique. Then retell a rehearsed brief cold.
- **Apply (independent):** take fresh briefs, unfamiliar to you, one at a time. Run the process end to end without scaffolding: requirements → sketches of two or three viable designs → comparison → decision with stated trade-offs → failure analysis → cost and operational notes. Defend the design against challenge prompts: change one requirement (scale, budget, latency, consistency) and revise the design; break one component and say what happens; halve the cost and say what you cut. Keep a design log for each system: the brief, the alternatives, the decision, what you were unsure about, and what evidence would change your mind. When a claim is checkable cheaply, build a probe rather than argue: a benchmark, a tiny prototype, a spike on the uncertain part. Rotate domains so the repetition is in the process, not the same familiar app: feeds and social, messaging, payments and ledgers, market or trading data, media and storage, workflow and integrations.

**Move on (graduation)**

- you can produce a coherent design for an unfamiliar brief, with alternatives and trade-offs, faster than you can talk yourself out of one;
- you can defend any component against "why not X" without notes and concede correctly when X is better;
- you can say what you would measure or build next to de-risk the design.

## Interview competence (how it fits, without dominating)

Interview-style system design is a validation format for S7, not a stage of its own and never the center of the track.

- **Enters late:** after independent design reasoning is demonstrated in S7. Interview prep before that produces recitation, not judgment.
- **Format, not curriculum:** a timed round is just another unfamiliar brief: 35–45 minutes, requirements, two or three designs, a defended choice, trade-offs, failure handling. Use the same process as S7 under time pressure.
- **Feedback sources:** self-review against a fixed rubric (requirements clarity, alternatives compared, trade-offs named, failure analysis, decision defended), a peer or mentor round, or one chosen mock round at most. No mock-interview quota.
- **Dominance check:** if interview questions, "top N systems," or memorized diagrams start replacing briefs you write yourself, the roadmap has drifted. Return to S7.
- **Never forced:** interview practice is kept comfortably secondary; the roadmap succeeds without it if the engineering understanding and independent design reasoning are real.

## Milestones

| Id | Checkpoint | After |
| --- | --- | --- |
| M1 | A short brief becomes a precise constraint list with labeled assumptions; the dominant requirement is named | S1 |
| M2 | A real bottleneck is found and fixed with measurement and estimation backing it | S2 |
| M3 | A real request path is explained with justified hops; its claims are proven by a build | S3 |
| M4 | A data decision is defended with index, query, and consistency reasoning, and implemented | S4 |
| M5 | A queue/event flow with idempotent, retryable consumers is defended and running | S5 |
| M6 | A system degrades as designed in a failure drill; an incident is reconstructed from observability signals | S6 |
| M7 | An unfamiliar system is designed and defended unaided; an interview-style round can be added here | S7 |

## What counts as progress

The master left the evidence bar to the domain. Progress is:

- a written brief + design with alternatives, a defended decision, and stated trade-offs; or
- a working implementation or reproduced guided exercise that demonstrates the stage capability or settles a claim you could not settle on paper; or
- measured behavior of a system under a stated condition — before/after, or versus a failure injected on purpose.

Not progress: a diagram with no requirements, a design with no alternatives, a build with no question it was meant to answer, a tutorial merely watched, or a list of terms you have heard.

## Calibration (unknown depth, handled honestly)

- Start at Stage 1 and let the learning phase calibrate: familiar concepts move quickly, unfamiliar ones get the full treatment. Do not skip the learning phase to prove a point, and do not sit in it after it stops teaching you something.
- If a stage gate is comfortably passable with real evidence, the stage is done; move on without ceremony.
- If a later gate fails, the underlying judgment is missing; drop back to the stage that trains it rather than repeating the whole path.
- The artifact, the defense, or the measurement is the check — never a model's say-so.

## How resources may be used

- No specific book, course, or talk list is chosen yet. When you accept one, it goes to [RESOURCES.md](RESOURCES.md) with what topic it serves. D-006.
- Materials are the normal teaching layer at the start of each stage — courses, books, tutorials, walkthroughs, and case studies, used actively. A resource counts when it produces notes, reproductions, extensions, or explain-it-back.
- One primary material per topic at a time; add another when the topic needs a second angle or a gap persists. Do not collect a shelf.
- A resource is done when you can use its ideas without it, not when you reach the last page or video.
- Implementations live outside this repo; links and short notes go to [projects/README.md](projects/README.md).
- Deviations from the default stack are allowed when the exercise or the objective needs them. Record the reason where the project or resource is recorded.

## Related

- Evidence and current stage: [PROGRESS.md](PROGRESS.md)
- Near-term unscheduled work: [BACKLOG.md](BACKLOG.md)
- Chosen materials: [RESOURCES.md](RESOURCES.md)
- Implementations: [projects/README.md](projects/README.md)
- Strategy and bands: [MASTER_ROADMAP.md](../MASTER_ROADMAP.md)
- Execution: `current-sprint/` while open, then `sprints/`. Not a folder here.
