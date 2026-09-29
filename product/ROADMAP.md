# Product

> **Role:** domain roadmap and validation loop for the independent-income attempt. Small, focused products, judged on outside evidence.
> **Authority:** subordinate to [MASTER_ROADMAP.md](../MASTER_ROADMAP.md) for phases, attention bands, and the evidence guardrail. This file designs the loop, gates, and decision rules inside those bounds.
> **Status:** active
> **Last reviewed:** 2026-09-29

## Purpose

Before joining, make one serious attempt at independent software income. A serious attempt means an opportunity put in front of real people, evidence collected, and a decision made on that evidence — payment, sustained use, or a written kill. Small and focused beats big and hidden. Intent: [context/GOALS.md](../context/GOALS.md).

The skills the attempt is meant to build: problem discovery, validation, designing the smallest useful test, scoping, shipping, pricing, getting paid, distribution, learning from usage, and deciding change versus kill.

Not this: portfolio projects, a six-month private build, venture-scale planning, or a product nobody was asked about.

## Starting point

- **No idea is selected.** Nothing here invents one, and no discovery shortcut is provided. Ideas are found in the wild, not in this file.
- Building ability is real ([context/PROFILE.md](../context/PROFILE.md)). The unknown is not code; it is which problem, for whom, at what price, through which channel.
- Prior launches, users, and revenue: `not logged`, not zero. Do not invent a history.
- Acceptable shapes are the ones already named — desktop utilities, browser extensions, micro-SaaS, creator tools, developer tools, workflow tools — but none is chosen. Shape follows the problem, not the reverse.

## How this path works

- **Outside evidence or it did not happen.** Conversations, usage, and payments are evidence; a written kill is a result. Effort, elapsed time, and finished builds are not evidence. Weights: [VALIDATION.md](VALIDATION.md).
- **Cheap before expensive.** Each stage costs more than the last. The loop exists to kill weak candidates before they reach the expensive stages.
- **No long private builds.** The master's guardrail. A product build starts only after demand evidence, and scope is cut until it is small.
- **Few things at once.** One active experiment, plus very cheap discovery threads. Focus is part of the method.
- **Decisions have triggers.** Every experiment opens with a hypothesis, a smallest test, and a kill criterion. A next cycle is justified by a named new signal, never by sunk effort.
- **Phase fit.** `gate-window` (current): secondary — Stages E1–E3 only, discovery and small tests, no product build. `post-gate`: primary — the full loop, including shipping and charging. Bands and yield order belong to the master.
- **A kill can be success.** An honest kill written from what happened satisfies the attempt. A repo nobody touched does not.

## The loop

discovery → problem evidence → smallest useful test → demand decision → build → ship and charge → distribute → real usage → continue / change / kill → back to discovery.

Seven stages, each ending at an evidence gate. Repeat stages rather than pushing a weak candidate forward.

### E1 — Problem discovery (opportunity hunting)

**Develops:** a pipeline of candidate problems grounded in observed pain — outside signal or a recurring problem of your own — not imagination.

**Work**

- Hunt where problems are visible and expensive: your own real workflows; communities where people complain or ask for tools; paid tools with unhappy users; spreadsheets and manual processes that exist only because nothing better does; services sold by hand.
- Record each candidate in [IDEAS.md](IDEAS.md): who has the problem, what they do today, what it costs them (time, money, risk), and where you saw it. A recurring problem from your own workflow may enter as a hypothesis, labeled as a personal observation, even before any outside evidence exists.
- Prefer problem-shaped evidence: people already paying for a worse solution, already hacking a workaround, publicly asking for this, or visibly tolerating the pain — manual effort, time loss, risk, repeated frustration.
- **Hypotheses do not advance on their own.** Owner-observed candidates are welcome here, but they need outside evidence to pass E2 and to reach any build decision. The gates and [VALIDATION.md](VALIDATION.md) enforce this.
- Reject ideas that are only interesting to build. Delete without ceremony.

**Move on when:** a small pipeline of candidates exists, each with a named user, current behavior, and a source — not a list of features.

### E2 — Problem validation (before any build)

**Develops:** proof that the problem is real and worth someone's money or attention.

**Work**

- Talk to people who have the problem. Ask what they do now, what it costs them, what they have tried, and what would have to change. A compliment is not evidence; a behavior is.
- Understand the buyer, not only the user, when they differ. Who pays, who decides, and who suffers are often three people.
- Cheapest permissible tests: the conversation itself, a manual offer to solve the problem for someone, a waitlist with a real ask. No product yet.
- Record each finding in [VALIDATION.md](VALIDATION.md) as `F-NNN`, including what it does not prove.
- Kill candidates nobody will discuss, whose people cannot be reached, or where no one can describe a concrete cost. Absence of current spending is not by itself a kill reason: manual workarounds, tolerated pain, time loss, risk, and repeated frustration all count as problem evidence.

**Move on when:** a specific person describes the problem in their own words, says what they do today, and would notice a solution — and you know where to find more people like them.

### E3 — Smallest useful test (demand and willingness to pay)

**Develops:** demand evidence before a build, including whether anyone will pay.

**Work**

- Choose the cheapest test that can produce the evidence you need. From weakest to strongest: landing page with a real ask; manual/concierge delivery of the value; a prototype a stranger can touch; a pre-sale or paid pilot.
- Make the ask real. "Would you pay?" is an opinion; asking for money is a fact. Use a pre-order, deposit, paid pilot, purchase order, or another concrete commitment tied to something specific.
- Probe price in conversation: what they pay for substitutes today, what the problem costs them, and the point where they would refuse. Ask for the refusal point, not for a happy number.
- Watch the gap between saying and doing. Signups without activation and warm words without a follow-up are weak signals.
- Open an experiment in [EXPERIMENTS.md](EXPERIMENTS.md) as `E-NNN` with hypothesis, smallest test, and kill criterion before running it.

**Move on when:** someone pays before the product exists, commits something scarce (money, time, data, a pilot slot), or repeatedly uses a manual or prototype version unprompted. Below that bar, change the test or kill.

### E4 — Build decision and the smallest product worth shipping

**Develops:** scope discipline. Only evidence-backed builds start, and they start small.

**Work**

- Decide from the recorded evidence: build / change the test / kill. "Build" requires the E3 bar. A clear no becomes a written kill, then back to E1.
- Define the smallest product worth shipping: it delivers the core value to the specific users from E2, at the price tested in E3, without the features you want for yourself. Write the explicit not-in-v1 list.
- Cut scope until the first shippable version fits the attention the band gives it. If it does not fit, the scope is wrong — not the effort you are not spending.
- Use the stack you know unless the product genuinely requires otherwise ([context/CONSTRAINTS.md](../context/CONSTRAINTS.md), D-019). Code lives in its own repository; record the link with the experiment (D-013).
- `gate-window` note: this stage waits. During the current phase the master allows discovery and small tests only; the build opens when Product is primary.

**Move on when:** a written build decision with evidence, a one-paragraph product definition, and a not-in-v1 list exist.

### E5 — Ship, price, and charge

**Develops:** getting the smallest product into someone else's hands and to a payment.

**Work**

- Ship means someone who is not you can find it, use it, and pay. "The repo compiles" is not shipping.
- Price from the problem's cost and the substitutes' prices, not from the cost of building. Pick the model — one-time, subscription, usage — to fit how value is delivered, and write down why.
- Charge from the start unless a deliberate, named free phase is itself the test. Free users are not demand evidence by themselves.
- Make paying and cancelling trivial. Prefer a payment path the audience already uses. Keep checkout short.
- Instrument the basics: signups, activation, payments, returns. No vanity dashboards.
- Expect v1 to be worse than the pitch. The point is real use, not polish.

**Move on when:** someone who is not you has paid, or used it unprompted more than once.

### E6 — Distribution and real usage

**Develops:** a repeatable way to reach the audience, and usage evidence beyond the first users.

**Work**

- Go where the E2 people already are: communities, marketplaces, newsletters, search surfaces, integrations, app directories, direct outreach. Try a few channels; keep the ones that produce activation, not clicks.
- Prefer channels you can repeat without renting attention, and note what each costs in time or money.
- Talk to active users and payers; ask non-users why not. Read behavior (what people do) over requests (what people say).
- Watch return use and retention, not only signups. A one-time spike is a lesson, not traction.
- Record channel results, usage, and payments with the experiment; roll up in [PROGRESS.md](PROGRESS.md).

**Move on when:** at least one channel repeatedly reaches the right audience, and there is usage, retention, or payment data to judge.

### E7 — Iterate, change, or kill

**Develops:** the decision discipline that closes the loop.

**Work**

- Decide from [VALIDATION.md](VALIDATION.md) evidence at every cycle:
  - **Continue (iterate):** payments continue or repeat; active users return unprompted; users ask for more of the same value; a channel works. Iterate on what limits payment or retention, not on what is fun to build.
  - **Change (pivot):** the problem is real but the solution, segment, price, or channel is wrong. The evidence should name which variable; change that one deliberately, with a new hypothesis, smallest test, and kill criterion. A pivot is a new cycle, not a rescue of the old build.
  - **Kill:** no payment or sustained use after honest tests; conversations stall; the problem is a nice-to-have; the audience cannot be reached at a price that works. Write the kill with what happened and what it did not prove. Killed experiments stay in the log; the lesson carries into E1.
- **Iteration priority from evidence:** first what stops a willing payer from paying; then what stops an active user from returning; then what brings more of the same users through a working channel. Feature requests from non-payers are information, not instructions.
- **Never extend on effort.** If a cycle produced no new outside evidence, the next cycle needs a named signal to chase or it dies.

**Move on when:** the attempt has an outcome — a product with paying users or sustained use, or an honest change/kill written with evidence. A killed attempt returns to E1 for the next one.

## Milestones

| Id | Checkpoint | After |
| --- | --- | --- |
| M1 | Opportunity pipeline: candidates with named users, current behavior, and outside sources | E1 |
| M2 | Problem validated with a real person in their own words; more of the same people reachable | E2 |
| M3 | Demand test run with a real ask; willingness-to-pay evidence, or an honest no | E3 |
| M4 | Build decision recorded from evidence; smallest shippable scope defined | E4 |
| M5 | Shipped to someone else; price set; payment path works; first unprompted use or payment | E5 |
| M6 | Repeatable channel; usage, retention, or payment data to judge | E6 |
| M7 | Outcome decided — continue, change, or kill — written with evidence. A kill counts | E7 |

## What counts as success

Even if the attempt is eventually killed:

- The loop ran: discovery from real signal, validation with real people, a real demand test, a decision based on evidence.
- A written record: findings, experiments, and the continuation or kill with what it did and did not prove.
- New capability: finding problems, talking to users, testing demand, pricing, shipping, distributing, and killing without a sunk-cost rescue.
- Payments or sustained use are the stronger outcome, not the only one. No revenue target is set and none is implied.

Not success: a private build, a repo nobody touched, an "almost ready" launch, or a kill with no evidence.

## Phase and attention

- `gate-window` (current): secondary. E1–E3 only — discovery and small tests. No product build. Product discovery yields before system-design continuity, but not before GATE (master).
- `post-gate`: primary. The full loop to shipping and charging, if the evidence says continue.
- Stages advance when their evidence gate is met, not by date. No schedules, quotas, or idea counts in this file.
- Capacity is `unknown` ([CURRENT_STATE.md](../CURRENT_STATE.md)). Size each cycle to the attention the band actually gives it.

## Unknowns

- The idea, audience, price, and channel: none selected. This file does not choose them.
- Prior launches and revenue: `not logged`, not zero.
- Willingness to pay: unknown until E3 produces it. Never write a price as validated before someone acts on it.
- Whether any attempt reaches payment: that is what the attempt is for.

## Related

- Ideas inbox: [IDEAS.md](IDEAS.md)
- Evidence standard and findings: [VALIDATION.md](VALIDATION.md)
- Experiment log: [EXPERIMENTS.md](EXPERIMENTS.md)
- Rollup: [PROGRESS.md](PROGRESS.md)
- Chosen materials: [RESOURCES.md](RESOURCES.md)
- Strategy and bands: [MASTER_ROADMAP.md](../MASTER_ROADMAP.md)
- Execution: `current-sprint/` while open, then `sprints/`. Not a folder here.
