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
- Therefore: **the early stages double as calibration, not as beginner teaching.** If the evidence says you already reason at a stage's level, that stage becomes a short compression pass and you move on. Nothing here assumes a zero baseline, and nothing assumes you are past the stage gates.

## How this path works

- **Ability-gated, not calendar-gated.** Stages are ordered by dependency and by the difficulty of the reasoning each demands. The pace is not scheduled. Move on when a stage's criteria are demonstrated, not when time has passed. No dates, quotas, or project counts.
- **Conceptual first, implementation when it forces a claim.** You reason about a mechanism before you build it, and you build to settle a question that reasoning alone could not settle — "would this hold," "what does this actually cost," "how does this fail." Implementation is not deferred to the end, and it is never "build an app to have built one."
- **Requirements before solutions.** Every synthesizing exercise starts from a brief: users, traffic shape, data shape, scale, latency, cost, operational constraints. Constraints are separated into hard constraints, preferences, and invented assumptions.
- **At least two viable designs, always compared.** A design without an alternative is not a design decision; it is a preference. Trade-offs are named in terms of what each option makes easy, hard, and expensive.
- **Every added component must justify itself** (a load balancer, a cache, a queue): what it buys, what it costs, and what new failure mode it introduces. "Standard practice" is not a reason.
- **Written artifacts and implemented proof.** Designs and teardowns are written and formatting does not matter. An implementation is proof only when it tests a specific claim from the design.
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

The arc moves from precision to judgment to independent synthesis: exactness about requirements → cost judgment on one machine → reasoning across the network → data decisions → asynchronous systems → reliability and operations → independent, defended design.

### S1 — Requirements and constraints

**Develops:** the first half of the master's end capability — take requirements and constraints and turn them into a precise problem statement. Without this, every later comparison is guesswork.

**Work**

- Take briefs from systems you know or use. Before any design, write down: who uses it; read/write shape; latency and consistency needs; scale as an estimate with a stated basis; cost ceiling if one exists; operational constraints.
- Separate hard constraints (physics, money, compliance, team) from preferences. Mark anything you invented as an assumption, and say what would falsify it.
- Reuse the sharp question list on fresh briefs: what breaks if the system is 10× bigger, 10× slower, or down for an hour? Which requirement would you cut first if forced?
- Batch systems with a shared constraint (all chat, all feeds, all payments) to see which requirements are specific to the domain and which are generic procedure.

**Move on when**

- you can turn a short brief into a constraint list and an explicit statement of what you are unsure about, with no "we'll figure it out later" holes;
- your assumptions are labeled and falsifiable, and you can say which requirement dominates the design and why.

### S2 — One machine, measured: latency, throughput, resources

**Develops:** cost judgment before scale reasoning. Most "distributed" problems are single-machine problems wearing a costume.

**Work**

- Build a measurement habit on systems you can actually run: request latency distributions (p50/p95/p99), throughput ceilings, error rates, resource saturation (CPU, memory, disk, connection pools).
- Read and reason about execution paths: what happens to one request from socket to response, which outbound calls exist, where memory is allocated, what all the queues are.
- Run deliberate experiments on your stack: increase concurrency until behavior degrades, add an index, add a pool, find the knee of the curve. Write down what was expected, what happened, and why.
- Back-of-envelope estimation as a practical skill: data volume, bandwidth, memory per connection, request rate versus capacity. Estimates carry stated assumptions, orders of magnitude are enough, and they get checked against measurement when possible.

**Move on when**

- you can find a real bottleneck in a system you run and justify the fix with a measurement, not a guess;
- your estimates come with assumptions and are within a comfortable order of magnitude of what you measure;
- you can articulate why a naive single-machine design fails next, and at roughly what scale.

### S3 — The distributed request path

**Develops:** reasoning about requests, components, and coordination across more than one machine. The first genuinely "system design" stage.

**Work**

- Teardown real request paths: from client through DNS and CDN or edge, load balancer, application instances, cache, database, external services, back. Every hop gets a reason and a cost.
- Load balancing and capacity: stateless services, session handling, health checks, draining, autoscaling behavior. What changes when instances are ephemeral.
- Caching as a layer: client, edge, application, database. Hit/miss economics, key design, invalidation, stale reads, cache stampedes. When a cache is the wrong answer.
- Communication choices: synchronous request/response versus asynchronous handoff — name when each is appropriate; failure propagation, timeouts, retries, idempotency keys, backpressure, retry storms, and where duplicate work is acceptable.
- Write, for one realistic system, the request-to-response narrative with alternatives at each hop and the choice defended in one line. Prove one critical claim with a small implementation (a cache, a queue handoff, a throttling layer), linked from [projects/README.md](projects/README.md).

**Move on when**

- you can explain a real request path end to end, noting what is load-balanced, cached, or queued, and why, including the failure and duplicate-work cases;
- you can defend the synchronous/asynchronous split and name the operational cost of each new component you add;
- a small implementation exists that tests one claim you could not settle on paper.

### S4 — Data as a first-class design decision

**Develops:** the durable half of most designs — storage choice, transaction boundaries, and consistency judgment. This is where interviews and production both separate people who "use a database" from people who reason about one.

**Work**

- Storage selection from access patterns: relational, document, key-value, and when each fits; schema design; indexing; query plans and why a query is slow.
- Transactions and isolation: read/write anomalies, locking versus MVCC, what your database guarantees and what your application must handle.
- Replication and partitioning: leader/follower, failover, replication lag and reads, sharding keys and hotspots, resharding pain.
- Consistency judgment: strong versus eventual for a given feature; idempotency; what "correct enough" means in the brief.
- Hands-on: one implementation in which the storage decision is defensible (an explicit index design, a transaction boundary, or a modest replication/sharding setup), plus a written version of the same design with the alternative storage choice argued against.

**Move on when**

- you can map an access pattern to a storage choice and back up the choice with index and query reasoning;
- you can name the transaction or consistency trap in a given flow and the mitigation;
- you have a build where the data decision, not the framework, is the interesting part.

### S5 — Asynchronous flow, queues, and event-driven systems

**Develops:** designing systems where work is decoupled in time — the modern default for feeds, notifications, payments, and pipelines.

**Work**

- When to queue: synchronous request/response versus a queue, an event log, or a stream. Ordering, delivery semantics (at-least-once, at-most-once, effectively-once), replay, dead letters, poison messages.
- Idempotent consumers, deduplication, and outbox/inbox patterns as practical mechanisms, not trivia.
- Streaming and event-driven design: event schemas, versioning, producer/consumer evolution, and when events should be commands instead.
- Hands-on: an implementation with a producer, a durable queue or log, and an idempotent consumer, including a retry/backoff policy and a dead-letter path. Prove duplicate delivery is safe.

**Move on when**

- you can decide synchronous versus queued for a feature and defend it against a counterexample;
- you can trace a message through the system across failures and retries and say exactly what happens to a duplicate;
- the implementation demonstrates idempotency rather than asserting it.

### S6 — Reliability, operations, and production reasoning

**Develops:** how systems behave when the happy path goes wrong — the stage that converts "design" into "engineering."

**Work**

- Delivery pipeline: containers, environments, configuration, secrets, migrations, rollbacks, and what deploys look like when something in the schema changes.
- Observability: the difference between logs, metrics, and traces; recording what you would need at 3 a.m.; alerting on symptoms rather than causes; dashboards that answer a real question.
- Failure design: graceful degradation, timeouts and circuit breakers, bulkheads, rate limiting, and the difference between "unavailable" and "wrong."
- Incident reasoning: from an alert or an outage to a hypothesis to a mitigation — recent-change check, dependency check, saturation check, data corruption check. Failure drills: kill a dependency, saturate a pool, add latency, split the network, and write down what broke versus what you expected.
- Operational readiness for a system you own: backup/restore, migration safety, on-call runbook basics, and cost behavior under load.

**Move on when**

- you can describe, for a real system, its top failure modes and the intended behavior under each;
- an own system survives or degrades correctly in a staged failure drill and you can explain what you fixed as a result;
- you can reconstruct an incident from logs, metrics, and traces, and write a blameless postmortem that ends in concrete changes.

### S7 — Independent design reasoning for unfamiliar systems

**Develops:** the full master capability, on systems you have not seen — the graduation stage.

**Work**

- Take fresh briefs, unfamiliar to you, one at a time. Run the process end to end without scaffolding: requirements → sketches of two or three viable designs → comparison → decision with stated trade-offs → failure analysis → cost and operational notes.
- Defend the design against challenge prompts: change one requirement (scale, budget, latency, consistency) and revise the design; break one component and say what happens; halve the cost and say what you cut.
- Keep a design log for each system: the brief, the alternatives, the decision, what you were unsure about, and what evidence would change your mind. Written form is fine; formatting does not matter.
- Rotate domains deliberately so the repetition is in the process, not in the same familiar app: feeds and social, messaging, payments and ledgers, market or trading data, media and storage, workflow and integrations. Revisit an earlier brief later with a different technology assumption and note what changes.
- When a claim is checkable cheaply, build a probe rather than argue: a benchmark, a tiny prototype, a spike on the uncertain part.

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
| M3 | A real request path is explained with justified hops; one claim is proven by a small build | S3 |
| M4 | A data decision is defended with index, query, and consistency reasoning, and implemented | S4 |
| M5 | A queue/event flow with idempotent, retryable consumers is defended and running | S5 |
| M6 | A system degrades as designed in a failure drill; an incident is reconstructed from observability signals | S6 |
| M7 | An unfamiliar system is designed and defended unaided; an interview-style round can be added here | S7 |

## What counts as progress

The master left the evidence bar to the domain. Progress is:

- a written brief + design with alternatives, a defended decision, and stated trade-offs; or
- a working implementation that settles a specific claim from a design; or
- measured behavior of a system under a stated condition — before/after, or versus a failure injected on purpose.

Not progress: a diagram with no requirements, a design with no alternatives, a build with no question it was meant to answer, or a list of terms you have heard.

## Calibration (unknown depth, handled honestly)

- Start at the earliest stage whose gate you cannot already pass by producing the artifact, not by feeling sure.
- If an early gate is passed immediately with real evidence, the stage is done; move on without ceremony.
- If a later gate fails, the fix is to drop back to the stage that trains the missing judgment, not to repeat the whole path.
- A stage is never "checked off" from a model's syllabus. The artifact, the defense, or the measurement is the check.

## How resources may be used

- No specific book, course, or talk list is chosen yet. When you accept one, it goes to [RESOURCES.md](RESOURCES.md) with what topic it serves. D-006.
- One material per topic at a time. A second is added only to unblock a demonstrated gap.
- Reading about a system is useful only when turned into a written teardown or a build. Passive video consumption is not practice.
- Implementations live outside this repo; links and short notes go to [projects/README.md](projects/README.md).
- Deviations from the default stack are allowed when the exercise or the objective needs them. Record the reason where the project or resource is recorded.

## Related

- Evidence and current stage: [PROGRESS.md](PROGRESS.md)
- Near-term unscheduled work: [BACKLOG.md](BACKLOG.md)
- Chosen materials: [RESOURCES.md](RESOURCES.md)
- Implementations: [projects/README.md](projects/README.md)
- Strategy and bands: [MASTER_ROADMAP.md](../MASTER_ROADMAP.md)
- Execution: `current-sprint/` while open, then `sprints/`. Not a folder here.
