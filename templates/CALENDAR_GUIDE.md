# Calendar guide

> **Role:** how to write a sprint `CALENDAR.ics`. Format rules in this file win over summaries elsewhere.
> **When to create or move a sprint:** [AI_WORKFLOW.md](../AI_WORKFLOW.md). This file does not decide sprint scope.
> **Last reviewed:** 2026-09-30

The planning model writes the `.ics` file directly. Do not add a generator script, a second calendar file, or a JSON copy of the schedule.

`PLAN.md` says what the sprint is for. `CALENDAR.ics` says when it makes sense to work on those outcomes. The calendar is subordinate to the plan.

## What the calendar must not do

- Invent a strategic priority, or make a track matter more because it has more events
- Treat every free hour as available work
- Fill the entire day with work. Labeling every period is visibility, not permission to pack the day; protected non-work time stays protected in every mode
- Turn unfinished tasks into extra blocks on its own
- Silently add scope that is not in `PLAN.md`
- Stand in for completion. An event is a block, not evidence the work happened. Completion is `REVIEW.md`
- Invent classes, exams, interviews, travel, or other commitments the owner has not reported
- Put secrets, passwords, tokens, or private credentials in a description
- Select Intensive mode just because the calendar can be filled

Default to a moderate Structured sprint per D-029; unknown exact hours alone do not force a sparse or Light sprint. Light needs a real reason. Do not guess a full week.

## Modes

The active `PLAN.md` must name the mode and why. One mode per sprint.

### Light

Use when there is a real reason for a lighter sprint (D-029). Unknown exact hours alone do not force Light.

Include:

- fixed commitments that are actually known and relevant
- a small number of important focus blocks
- deadlines or assessments, if a real date is known
- a few protected sessions, if something would otherwise be crowded out

Fewer work blocks and more labeled Free / Rest / Buffer time. The 09:00–22:30 labeling rule still applies: labeling is visibility, not work.

### Structured

The normal default: a moderate, organized sprint (D-029).

Include:

- planned work sessions for the outcomes that need a time
- known fixed commitments
- breaks or buffers where work would otherwise stack with no recovery
- lunch 13:00–14:00 and dinner 19:30–20:30 as explicit events
- labeled slack: every period in the 09:00–22:30 window gets an event, so unused time is a protected `Free Time`, `Buffer`, or `Rest` block rather than an anonymous gap

Do not schedule the entire day as work. Organized is not packed.

### Intensive

Only when the plan names a real reason for a genuine short high-pressure period:

- important exam preparation
- interview preparation
- a short high-pressure window
- a deadline
- another period the owner has explicitly called intensive

May include a detailed day: fixed commitments, focus blocks, meals, breaks, transition time, recovery, free time, wind-down, and hard stops. More work and detail than Structured, only for the high-pressure period.

Still not permission to delete free time. A hard stop is a hard stop. If you cannot name the circumstance in `PLAN.md`, you are not in Intensive mode.

## Daily window

Owner-provided preferences for normal sprint days, not inferred from old calendars:

- Work blocks begin no earlier than 09:00 and end by 22:30 at the latest.
- Do not schedule study/work before 09:00 or after 22:30 unless the owner explicitly overrides it for that day.
- Lunch 13:00–14:00 and dinner 19:30–20:30 are explicit calendar events.
- Within 09:00–22:30, label every period with an event. No anonymous gaps: unused time is `☕ Break`, `🧭 Buffer`, `Free Time`, `Rest / Buffer`, `Transition`, or `🌙 Wind Down`. Labeled slots are visibility, not productive hours.

## Titles

Concise, specific, and human-readable. Emoji/category prefixes are preferred where they improve scanning, consistent with the owner's previous calendars.

Work:

```text
System Design — Cache-Aside Implementation
GATE — DBMS PYQ Set
Music — Vocal Recording Practice
Product — Validate Problem #2
```

Pattern: `Track — specific block`. The title should tell you what this sitting is for without opening the plan.

Fixed commitments, so they are not mistaken for sprint goals:

```text
Fixed — DBMS class
Fixed — Interview
Exam — GATE mock
```

Use the specific name when it is clearer (`Class — DBMS`). The point is that a review can see it was not an outcome.

Non-work, labeled explicitly on Structured days:

```text
☕ Break
🧭 Buffer
Rest / Buffer
Lunch
Dinner
Transition
Free Time
🌙 Wind Down
```

Stretch, only if there is real spare capacity and the plan already lists it:

```text
Stretch — <task>
```

Missing a stretch block is not a miss.

## Descriptions

Write each description per `../SPRINT_PLANNING_METHOD.md`: only what that block needs for good execution, no fixed form. Enough to do that block without reopening five planning files. Not a paste of the sprint plan.

One possible shape, not a required one:

```text
Plan: O1
Purpose: Understand cache-aside behavior under normal and failure conditions.
What to do:
- implement the normal read path
- handle a cache miss
- simulate a Redis outage
- reason about invalidation
Output: Working implementation plus short failure-mode notes.
```

Add a field or line only when it adds value for that task; see the planning method for the field set and per-track examples.

- `Resources:` only for material already chosen in the repo. Do not introduce a book or course here

`Plan: O1` (or the task it covers) is how a work event maps back to `PLAN.md`. Fixed commitments and non-work events do not need an outcome id. Their description should say they are not sprint outcomes. A break, meal, buffer, college-project block, or simple continuation needs little or no description.

A tiny follow-up can live inside a larger block. It does not need its own event.

Not every plan task needs its own event; a small task may live inside a larger labeled block. Inside 09:00–22:30 there are no anonymous gaps: time without a work event carries a labeled non-work event. Stretch work stays unscheduled unless spare capacity is real.

## Non-work time is protected

`Rest / Buffer` is not hidden catch-up. Do not move missed work into it. Say so in the description: `Protected time. Not catch-up.`

`Free Time`, `Rest / Buffer`, and `Buffer` stay free. Do not fill them later unless the owner asks to reschedule, and even then do not assume they are the default overflow.

Account for transitions between unrelated blocks. Do not stack hard work back to back all day and call the gaps optional.

In Light mode, use fewer work blocks and more labeled Free / Rest / Buffer time. Labeling still applies: it is visibility, not work.

In Structured mode, put a buffer where two demanding blocks would otherwise touch, and label every non-work period in the 09:00–22:30 window (no anonymous gaps). Slack is protected labeled time, not invisible space.

In Intensive mode, write meals, breaks, transitions, recovery, free time, wind-down, and hard stops as events so they are not squeezed out. A buffer event still is not catch-up time.

## Fixed commitments

Include one only if the owner reported it or it is already a fact in this repo: class, exam, lab, interview, assessment, internship or work, appointment, travel, or another known obligation.

They explain why a work block cannot sit there. They are not sprint goals. Do not score them in `REVIEW.md`. Reserve owner-reported times from `CURRENT_STATE.md` with no overlapping work — e.g. when the sprint covers 2026-10-08, `🏫 Lab Quiz` 10:00–12:00 sits there and no sprint work overlaps it. Do not infer any other class timetable or college commitment from one fact or from historical calendars.

## College final-year project blocks

While the college final-year project remains active, reserve a reasonable amount of calendar-only time for it in each normal sprint, such as `🛠️ College Project` (or `🛠️ College Project — Planning` / `🛠️ College Project — Work` when that split is useful). No fixed number or duration is prescribed; choose reasonable placement around the main workload and fixed commitments. Never invent project content, tasks, technologies, milestones, deadlines, implementation steps, or study material inside them. They are time reservations, not a roadmap track and not a sprint outcome unless the owner later makes them one. The owner decides what to do during those blocks. A college-project block needs little or no description. Do not manage the project through this planner.

If the day is known and the clock time is not, use a date-only event or omit the clock time. Do not invent a clock time for it.

## How long a block should be

No single duration.

- 15–30 minutes: a real review, a buffer, a transition. Not a way to slice deep work into shards
- 60–120 minutes: normal deep work
- Longer than that only with a reason written in the description, and not as an unbroken four-hour concentration block by default

Split a task across days if that is the better way to do it. Several honest blocks beat one fantasy block.

Avoid a day of difficult work with no recovery, in any mode.

## Timezone

Read the working timezone from `CURRENT_STATE.md`. Until that file says otherwise, it is `Asia/Kolkata`.

Use that zone for `X-WR-TIMEZONE`, for every `TZID`, and for the `VTIMEZONE` block. Do not mix zones in one file. Do not write a Kolkata clock time with a `Z` suffix. `Z` means UTC and will shift the event by 5 hours 30 minutes.

If `CURRENT_STATE.md` later names a different zone, do not reuse the Asia/Kolkata offset block below. Get the right `VTIMEZONE` for that zone. Do not invent offsets.

## File rules

One file: `current-sprint/CALENDAR.ics` while the sprint is active. After archive, the same file lives at `sprints/sprint-NNN/CALENDAR.ics` and is the final schedule that was in force, including mid-sprint edits.

- UTF-8, no BOM
- CRLF line endings (`\r\n`), as RFC 5545 requires
- Fold any line longer than 75 octets. Continuation lines start with a single space. That leading space is removed when the line is unfolded, so a space you want to keep must sit before the break
- No second calendar, no `CALENDAR-old.ics`, no sidecar JSON or YAML
- Git history is the earlier version. Do not keep versioned copies in the folder

Do not rewrite the file at sprint close to match what was actually done. A missed Tuesday block stays on Tuesday.

## Required shape

```text
BEGIN:VCALENDAR
VERSION:2.0
PRODID:-//Personal Planner//Sprint Calendar//EN
CALSCALE:GREGORIAN
METHOD:PUBLISH
X-WR-CALNAME:Sprint 001
X-WR-TIMEZONE:Asia/Kolkata
BEGIN:VTIMEZONE
...
END:VTIMEZONE
BEGIN:VEVENT
...
END:VEVENT
END:VCALENDAR
```

`X-WR-CALNAME` is a useful sprint name, such as `Sprint 001` or `Sprint 001 · 1–10 Oct 2026`. Not a slogan and not a strategy statement.

`VTIMEZONE` is required when `DTSTART` uses `TZID`. Copy this block for `Asia/Kolkata`. India has no daylight-saving transition in this zone.

```text
BEGIN:VTIMEZONE
TZID:Asia/Kolkata
X-LIC-LOCATION:Asia/Kolkata
BEGIN:STANDARD
TZOFFSETFROM:+0530
TZOFFSETTO:+0530
TZNAME:IST
DTSTART:19700101T000000
END:STANDARD
END:VTIMEZONE
```

Each timed event needs at least:

```text
BEGIN:VEVENT
UID:sprint-001-20261002-01@personal-planner
DTSTAMP:20261001T043000Z
DTSTART;TZID=Asia/Kolkata:20261002T093000
DTEND;TZID=Asia/Kolkata:20261002T110000
SEQUENCE:0
SUMMARY:System Design — Cache-Aside Implementation
DESCRIPTION:Plan: O1\nPurpose: Understand cache-aside under normal and failure conditions.\nWhat to do:\n- implement the normal read path\n- handle a cache miss\nOutput: Working notes on the failure path.
END:VEVENT
```

`SEQUENCE` is required. Start at `0`. Increment by 1 when the time, title, or description of that event changes. Importers that honor `UID` plus `SEQUENCE` can update an event instead of duplicating it. Those that do not will still behave better if the UID did not change.

`DTSTAMP` is UTC, `YYYYMMDDTHHMMSSZ`, at the time you write the event. Do not reuse a stale stamp after an edit.

`DTEND` is the end instant, not inclusive. A 09:30–11:00 block ends at `110000`.

### Date-only events

Use these when the day is known and the clock time is not. `DTEND` is the next day, exclusive. A deadline on 5 October:

```text
DTSTART;VALUE=DATE:20261005
DTEND;VALUE=DATE:20261006
```

Do not also put `TZID` on a `VALUE=DATE` property.

## UIDs

Stable and deterministic. No random values.

When you create an event, assign:

```text
<sprint-id>-<original-local-date>-<sequence>@personal-planner
```

Example: `sprint-001-20261002-01@personal-planner`

- `sprint-id` matches the id inside `PLAN.md`, including the `sprint-` prefix
- `original-local-date` is `YYYYMMDD` in the calendar timezone, the day the event was first placed
- `sequence` is `01`, `02`, … among events first created for that date. Two digits is enough
- Never reuse a sequence number for a different event
- If you delete an event, retire its UID. Do not give that UID to a new block

Once assigned, the UID does not change. If Tuesday moves to Wednesday, keep the UID, change `DTSTART` and `DTEND`, and increment `SEQUENCE`. Do not "fix" the date inside the UID. Recomputing it creates a duplicate on import.

Regenerating the file with the same UIDs is how a supporting calendar avoids duplicates. It is not a promise that every importer updates in place. Still do not mint new UIDs for the same blocks.

## Importing into Google Calendar

Stable UIDs and `SEQUENCE` remain required. They are correct iCalendar practice, and importers that honor them can update an event instead of creating a duplicate. Do not weaken either requirement.

Manual Google Calendar imports should not be assumed to reliably update previously imported events without duplicates. Treat a manual import as importing events, not as syncing a calendar.

- Import `CALENDAR.ics` when the sprint begins.
- If only a few events change, update those events manually in Google Calendar, and make the same change in `CALENDAR.ics`. The two copies should not drift.
- If you want to re-import the whole `.ics`, first verify how the target calendar handles existing UIDs and duplicates. Try a test calendar before doing it on the sprint calendar.
- `CALENDAR.ics` remains the canonical planned schedule in the repo, whatever the Google Calendar copy looks like.
- Stable UIDs must still be preserved across reschedules.
- `SEQUENCE` must still increment for changed events.

## Escaping

In `SUMMARY` and `DESCRIPTION`:

| Character | Write |
| --- | --- |
| `\` | `\\` |
| `;` | `\;` |
| `,` | `\,` |
| newline | `\n` |

A real line break inside a description is the two characters `\` and `n`, not a raw newline, until you are folding a long line.

Folding example. The break is CRLF plus one space. The space at the start of the next line is not part of the text. The space you want to keep is before the break:

```text
DESCRIPTION:Plan: O1\nPurpose: Understand cache-aside.\nWhat to do:\n- implement
  the normal read path
```

Unfolded value: `Plan: O1` then a newline, then `Purpose: …`, then `- implement the normal read path`.

Prefer short lines so you fold rarely. Count octets, not characters. Skip emoji if you are near the limit and do not want to fold.

## Mid-sprint edits

The owner can reschedule. Edit `current-sprint/CALENDAR.ics` in place.

- Keep sprint goals unless the owner is explicitly changing scope
- Do not rewrite `PLAN.md` because Tuesday moved to Wednesday
- Moving a block is not failure and is not a review event by itself
- Do not occupy `Rest / Buffer` or `Free Time` automatically
- If the calendar keeps proving the plan cannot fit, leave that evidence for the review. Do not quietly delete outcomes from the plan to make the calendar look feasible

## Checklist before the file is done

- [ ] Mode in `PLAN.md` matches the density of this file
- [ ] Normal days stay inside 09:00–22:30; lunch 13:00–14:00 and dinner 19:30–20:30 are explicit events
- [ ] Every period in the window is labeled; no anonymous gaps; labeled time is visibility, not work
- [ ] Every work event maps to an outcome or task in `PLAN.md`
- [ ] No work event adds scope the plan does not have
- [ ] Stretch is unscheduled, or clearly labeled and optional
- [ ] Known fixed commitments only. None invented
- [ ] Buffers and free time are not described as catch-up
- [ ] Timezone matches `CURRENT_STATE.md`
- [ ] `VTIMEZONE` matches that zone
- [ ] Timed values use `TZID` and do not end in `Z`
- [ ] UIDs are stable, unique, and not random
- [ ] `DTSTAMP` is UTC
- [ ] Commas, semicolons, backslashes, and newlines are escaped
- [ ] Lines over 75 octets are folded
- [ ] CRLF line endings
- [ ] No secrets
- [ ] No second calendar file
