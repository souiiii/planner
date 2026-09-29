# Markets

> **Role:** domain roadmap for practical market understanding — how markets work and how the pieces connect, explained in your own words.
> **Authority:** subordinate to [MASTER_ROADMAP.md](../MASTER_ROADMAP.md) for phases, attention bands, and non-goals. This file designs the learning sequence inside those bounds.
> **Status:** active
> **Last reviewed:** 2026-09-29

## Purpose

Build a practical understanding of financial markets as a long-term personal interest, with useful general context before joining LSEG. The outcome is explanation, not prediction: you can say how markets work, who does what, and how the major pieces connect. Intent: [context/GOALS.md](../context/GOALS.md).

Not this: an exam, a certification, a trading record, investing advice, or a forecast track record.

## Starting point

- Current markets knowledge is `unknown`. No prior study, finance background, or claimed concepts are recorded.
- Therefore: **the early stages double as calibration.** Familiar ideas move quickly; unfamiliar ones get the full treatment. Nothing here assumes zero, and nothing assumes expertise.
- Team, role, and business line at LSEG are `unknown`. Nothing here specializes around a guessed desk. Team-specific learning waits until a team is known — and even then only if it actually changes what "enough" means (master checkpoint).

## How this path works

- **Ability-gated, not calendar-gated.** Stages are ordered by dependency: each one gives the vocabulary the next one needs. Move on when you can explain the stage's mechanisms in your own words, not when time has passed. No dates, quotas, or topic counts.
- **Mechanisms before instruments, instruments before plumbing, plumbing before derivatives.** Every stage answers "what is this for and how does it work" before "what is it called."
- **Connect, don't collect.** Each stage ends by connecting back: how this piece touches the earlier ones, and where LSEG-shaped businesses (venues, data, clearing, benchmarks) sit relative to it.
- **Explain it back.** The evidence at every gate is your own wording — a short written explanation, a worked example, or an answer to "why does it work this way." Recognizing a term is not understanding it.
- **Real markets as the textbook.** Follow real events, real data, and real market behavior where they illuminate a mechanism. News is material for explanation practice, never for prediction or trading.
- **Slow-burn by design.** During `gate-window` this track is maintenance: keep it warm with small sessions. After the exam it gets more room but stays general. The master owns bands and yield order.
- **No specialization on guesses.** Anything team-specific waits for a real team fact plus a review. General context now; depth later, only if the fact demands it.

## Scope

In scope, sequenced below by dependency: why markets exist and who participates; equities, bonds, rates, FX; market structure and price formation; market data and benchmarks; clearing, settlement, and custody; derivatives and risk; then connecting the whole picture through real events.

Out of scope:

- Day-trading practice, signals, tips, and get-rich material.
- A professional certification program, unless you later ask for one.
- Pretending to know your future LSEG business line.
- A reading list the model wishes you would follow. Chosen reading goes in [READING.md](READING.md) only after you accept it (D-006).
- Forecasting, paper-trading scoreboards, or any trading-performance target.

## Stages

### S1 — Why markets exist and who participates

**Why first:** everything later is an answer to "who needs this and why." Without the participants, instruments are vocabulary without a story.

**Work**

- **Learn:** what a market does — move capital, transfer risk, discover prices, provide liquidity. Who shows up: issuers, investors (individual and institutional), intermediaries (brokers, dealers, market makers), venues, and infrastructure providers. What each one wants and what each one is paid for.
- **See it applied:** pick a company or government action you have heard of (an IPO, a bond issue, a central-bank decision) and trace who the participants were and what each got out of it.
- **Connect:** write down where an LSEG-shaped business could sit in that picture (venue, data, clearing, benchmarks) — as possibilities, not as claims about your team.

**Move on when**

- you can explain, in your own words, why a market exists for a given need and what each participant type contributes;
- you can place venues, data, clearing, and benchmarks on that map without guessing your future role.

### S2 — The core instruments: equities, bonds, rates, FX

**Why second:** these are the things being traded everywhere else in the roadmap. Structure, data, clearing, and derivatives all assume you know what the underlying claim is.

**Work**

- **Learn, one at a time, always as "what claim is this and why does it exist":** equities (ownership, dividends, voting, what a share price means); bonds (promise to pay, coupons, maturity, yield, why prices move when rates move); rates (what an interest rate is, who sets which ones, how they propagate); FX (currency pairs, why conversion and hedging exist).
- **See it applied:** for each instrument, find one real current example — a stock price move with a stated reason, a bond yield quote, a rate decision, an FX move — and explain it in your own words.
- **Practice the connections:** how a rate change reaches bond prices, equities, and currencies. Draw the causal chain yourself before checking it against any source.
- **Note what you do not need:** pricing models, valuation formulas beyond intuition, and trading strategies. This stage is "what it is and why it moves," not "how to trade it."

**Move on when**

- you can explain what each instrument is, who uses it and why, and the basic reason its price moves;
- you can trace a rate change through bonds, equities, and FX in your own words.

### S3 — How trading works: market structure and price formation

**Why third:** now that the instruments exist, this is where buying and selling actually happens — the mechanism behind every price you saw in S2.

**Work**

- **Learn:** venues (exchanges vs OTC vs dark pools, at a conceptual level); the order book — bids, asks, spread, depth; order types (market, limit, stop) and what each one risks; who provides liquidity and why (market makers, spreads as payment for risk); how a price is formed by matching, not decreed.
- **See it applied:** watch a real order book or a recorded example if accessible; otherwise work through a documented example trade by trade. Explain each fill: who wanted what, who provided it, what the spread paid for.
- **Connect back:** which instruments from S2 trade where, and why some live on exchanges while others live OTC.
- **Note what you do not need:** microstructure mathematics, execution algorithms, or latency-race detail. Understand the mechanism; leave the engineering of it alone.

**Move on when**

- you can explain how an order becomes a trade and where the price came from;
- you can say why spreads exist, who earns them, and why some markets are exchange-traded and others are not.

### S4 — Market data and benchmarks

**Why fourth:** data is what the structure in S3 produces, and it is also one of the most LSEG-shaped parts of the picture. It needs S2–S3 first to mean anything.

**Work**

- **Learn:** what market data is — quotes, trades, order-book snapshots, reference data; the difference between real-time and delayed, and why anyone pays for speed or completeness; what an index or benchmark is and how one is constructed and maintained.
- **See it applied:** pick a real index you have heard of and explain in your own words what it tracks, roughly how, and who uses it for what. Find one real example of market data mattering (a pricing dispute, a benchmark reform, a data outage story).
- **Connect:** place data and benchmarks on the S1 map — who produces them, who consumes them, where the business value sits. Keep it general; no team guesses.

**Move on when**

- you can explain what market data contains, why it has value, and what a benchmark is for;
- you can describe the data business in general terms without assuming your future team.

### S5 — After the trade: clearing, settlement, custody

**Why fifth:** the trade in S3 is not finished when it matches. This is the plumbing that makes markets trustworthy — and the other most LSEG-shaped part of the picture.

**Work**

- **Learn:** what happens after matching — clearing (novation, the clearinghouse as counterparty to both sides), settlement (delivery versus payment, T+1/T+2 as concepts), custody (who holds what for whom), and why each step exists: counterparty risk, failed trades, and what "settled" actually guarantees.
- **See it applied:** trace one real trade lifecycle end to end — order, match, clear, settle — naming who bears risk at each point. Find one real settlement failure or clearing event and explain what went wrong in your own words.
- **Connect back:** how clearing and settlement touch every earlier stage, and where they sit on the S1 map.

**Move on when**

- you can walk through a trade's full lifecycle and say who bears what risk at each step;
- you can explain why clearinghouses and custodians exist without reciting definitions.

### S6 — Derivatives and risk, conceptually

**Why sixth:** derivatives reference everything before them — instruments (S2), venues (S3), and clearing (S5). Risk is the thread that ties the whole roadmap together.

**Work**

- **Learn:** what a derivative is — a contract whose value comes from something else. Futures and forwards (agree now, settle later, why); options (the right without the obligation, premium as the price of choice); swaps (exchanging cash flows, why); margin and collateral as the safety mechanism.
- **Risk as the through-line:** market risk, credit/counterparty risk, liquidity risk, operational risk — each defined by an example, not a glossary. For each, say who bears it and how it is managed or transferred.
- **See it applied:** pick one real derivatives story (a hedge, a blowup, a margin call event) and explain what the contract was, who wanted what, and where the risk sat.
- **Note what you do not need:** pricing models (Black-Scholes and friends), Greeks beyond intuition, or any trading strategy. "What it is, who uses it, where the risk sits" is the bar.

**Move on when**

- you can explain the main derivative types, who uses each and why, and where the risk sits;
- you can name the main risk types with a real example of each.

### S7 — Connecting the picture through real markets

**Why last:** this is the graduation stage — the earlier pieces stop being chapters and become one working picture, exercised on real events.

**Work**

- **Follow real events as explanation practice:** take a current market story — a rate decision, a volatile week, an IPO, a settlement or outage event, a benchmark change — and explain it using the full picture: which instruments, which venues, what the data showed, where clearing and risk sat.
- **Write short explainers in your own words** in [NOTES.md](NOTES.md): the event, the mechanisms involved, and the connections between stages. One page beats ten pages.
- **Revisit earlier notes** and correct them where your understanding has deepened. The corrections are the evidence of progress.
- **LSEG context, still general:** explain where LSEG-shaped businesses touch the story. No team guesses, ever.

**Move on (graduation — "good enough by joining")**

- you can take an unfamiliar market story and explain the mechanisms behind it, connecting instruments, structure, data, clearing, and risk, in your own words;
- someone without a finance background could follow your explanation;
- you know specifically what you do not understand yet, and it is bounded — named topics, not fog.

## What "good enough by joining" means

The master's bar, made concrete by this roadmap: practical understanding you can explain in your own words — how markets work and how the main pieces fit together — at the breadth of S1–S7 above. It is not a license, a forecast record, deep quantitative skill, or every subtopic mastered. It is the ability to follow a market story, place it on the map, and ask intelligent questions about the parts you do not know.

## If your LSEG team becomes known

- Update [CURRENT_STATE.md](../CURRENT_STATE.md) with the fact. Do not rewrite this roadmap around a guess before that.
- Team-specific depth waits for a review, per the master checkpoint — and only if the team fact actually changes what "enough" means.
- If a review approves it: add a bounded extension (named topics, named depth, named source), not a second syllabus. General understanding stays the base; team depth is a clearly marked annex.
- If no review happens, nothing changes here. General context remains the whole track.

## Milestones

| Id | Checkpoint | After |
| --- | --- | --- |
| M1 | Participants and their motives explained; venues, data, clearing, benchmarks placed on the map | S1 |
| M2 | Each core instrument explained with a real example; a rate change traced through bonds, equities, FX | S2 |
| M3 | An order traced to a trade with price formation explained; spreads and venue types justified | S3 |
| M4 | Market data and benchmarks explained with a real example; the data business described generally | S4 |
| M5 | A full trade lifecycle walked with risk placed at each step | S5 |
| M6 | Derivative types and risk types explained with real examples | S6 |
| M7 | An unfamiliar market story explained end to end in your own words; unknowns bounded and named | S7 |

## What counts as progress

- A mechanism explained in your own words, in [NOTES.md](NOTES.md) or cited in [PROGRESS.md](PROGRESS.md).
- A real event or data point interpreted through the roadmap's concepts.
- A corrected earlier note, with what changed and why.

Not progress: terms recognized, pages read, videos watched, or a model-written summary of something you did not work through.

## Calibration (unknown depth, handled honestly)

- Start at S1 and let the early work calibrate: familiar ideas move fast, unfamiliar ones get full treatment. Do not skip the explaining step to prove a point, and do not sit in a stage after it stops teaching you something.
- If a stage gate is comfortably passable with a real explanation, the stage is done; move on without ceremony.
- A stage is never checked off from a syllabus. Your explanation is the check.

## How reading may be used

- No title is chosen. When you accept one, it goes in [READING.md](READING.md) with status and why it was chosen (D-006).
- Reading serves a stage, not the reverse. One active title at a time is plenty; add another only when a second angle is needed.
- A chapter counts when it produces an explanation, a worked example, or a corrected note — not when its last page is reached.
- Working notes live in [NOTES.md](NOTES.md). Understanding claimed lives in [PROGRESS.md](PROGRESS.md), in your words.

## Related

- Claimed understanding: [PROGRESS.md](PROGRESS.md)
- Chosen reading: [READING.md](READING.md)
- Working notes: [NOTES.md](NOTES.md)
- Strategy and bands: [MASTER_ROADMAP.md](../MASTER_ROADMAP.md)
- Execution: `current-sprint/` while open, then `sprints/`. Not a folder here.
