# Validation

> **Role:** evidence standard and decision rules for product experiments, plus findings.
> **Authority:** authoritative for what counts as evidence in this track. The master sets the guardrail (outside evidence, no long private build); this file defines the bar, the tests, and the kill method. Decision D-020.
> **Not a pitch,** and not the experiment log. Experiments live in [EXPERIMENTS.md](EXPERIMENTS.md). The loop is in [ROADMAP.md](ROADMAP.md).
> **Last reviewed:** 2026-09-29

Use this so "I built it" cannot be recorded as "people want it".

## What counts

Stronger evidence sits lower in this list. Do not skip to building because weaker signals felt good.

| Signal | Weight |
| --- | --- |
| Someone pays | strongest evidence this repo cares about |
| Someone uses it unprompted, more than once | strong |
| A specific person describes the problem in their own words and wants a solution | useful |
| A landing page or prototype produces signups from strangers | weak to moderate, depends on the ask |
| Friends say it is cool | weak. Do not treat as validation |
| You would use it yourself | a clue, not evidence |
| You finished the build | not evidence of demand |

A conversation is more useful than a compliment. Write down what they already do, what it costs them, and whether they asked to be told when it exists.

## The build bar

What justifies starting a product build:

- someone pays before the product exists (pre-order, deposit, paid pilot); or
- someone commits something scarce — money, scheduled time, their own data, a pilot slot — to something specific; or
- someone repeatedly uses a manual or prototype version unprompted.

Not enough on its own: signups, waitlist size, compliments, "I would definitely use this", your own enthusiasm, or a finished prototype with no users.

## Testing willingness to pay

Ranked from weakest to strongest, same principle as the evidence table:

1. Opinion — "would you pay?" Weak. Record it, do not act on it.
2. Costly action — a detailed conversation, sharing data, introducing a colleague. Moderate.
3. Commitment — a deposit, a signed pilot agreement, a scheduled onboarding. Strong.
4. Money now — pre-order, paid pilot, purchase order. Strongest.

Price probes:

- What they pay for substitutes today.
- What the problem costs them (time, money, risk).
- The price point where they would refuse. Ask for the refusal point, not for a comfortable number.

A price is validated only when someone acts on it. Never write a price as known before that.

## Change and kill rules

- An experiment opens with a hypothesis, a smallest test, a kill criterion, and the next piece of evidence it will produce.
- Time-boxing is by evidence, not by clock: an experiment runs until it reaches its next evidence gate or its kill criterion, whichever comes first. This file sets no dates or week counts.
- **Continue** only when the last cycle produced new outside evidence and the next cycle has a named signal to chase.
- **Change** (pivot) requires the evidence to name the variable that is wrong: problem, user, solution, price, or channel. A change is a new cycle with a new test and criterion, not an extension of the old build.
- **Kill** when: no one pays or commits after honest asks; usage does not return; the audience cannot be reached at a workable price; conversations stall; or the problem is a nice-to-have. Write the kill with what happened. Killed experiments stay in the log.
- Effort, elapsed time, sunk cost, and "it is almost ready" are never reasons for one more cycle.

Until a real experiment is running, do not let discovery drift into an unbounded build. A sprint that extends a build with no new evidence should say so in the review and consider `delete` or `change`.

## Findings

None yet. Add a finding only from a real conversation, a real usage event, or a real payment. Link the experiment id.

```text
### F-NNN
- Date:
- Experiment:
- What happened:
- What it does not prove:
```
