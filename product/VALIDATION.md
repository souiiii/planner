# Validation

> **Role:** evidence standard for product experiments, plus findings.
> **Authority:** authoritative for what counts as evidence in this track.
> **Not a pitch,** and not the experiment log. Experiments live in [EXPERIMENTS.md](EXPERIMENTS.md).
> **Last reviewed:** 2026-09-27

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

## Kill rule

The master roadmap sets the guardrail: experiments are judged on outside evidence, not effort or elapsed time, and a long private build is out of phase. It does not set a kill time. Decision D-020.

This domain defines the method: how an experiment is time-boxed, what triggers a change or a kill, and what evidence would justify one more cycle. That method is not written yet.

Until it exists, do not let an experiment run on as an unbounded build. A sprint that extends a build with no new evidence should say so in the review and consider `delete` or `change`.

## Findings

None yet. Add a finding only from a real conversation, a real usage event, or a real payment. Link the experiment id.

```text
### F-NNN
- Date:
- Experiment:
- What happened:
- What it does not prove:
```
