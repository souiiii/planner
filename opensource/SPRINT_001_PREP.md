# Open Source — Sprint 001 preparation

> **Status:** proposal pending owner acceptance.
> **Prepared:** 2026-09-30.
> **Context:** `gate-window`; maintenance. GATE remains primary; capacity is unknown.
> No sprint, calendar, repository selection, or contribution has been created by this proposal.

## Small candidate slice

**Learn the workflow, enter one healthy repository, and trace one useful piece of work.** Attempt a contribution if the issue and remaining capacity make it sensible. No merge or PR is required to make the slice worthwhile.

Bound the work to one active JS/TS/Node/React-aligned repository, one issue/change, and at most one replacement repository if the first is unsuitable. Most effort goes into local work. No broad repo hunt, bootcamp, new framework, or parallel contributions.

## Learn, then use it

1. **Workflow refresher:** use the [exact Piyush selections](RESOURCES.md): repository fit **00:35–03:00**; crash course **08:40–20:15** and **24:30–30:15**. Total **19:45**. Explain upstream versus fork versus local branch, what a PR proposes, and who decides to merge. Use a local branch/diff to check understanding; do not submit a practice-only change to someone else's project.
2. **Choose deliberately:** start with a tool/library the owner uses or understands. Check current activity, contribution guide, runtime/setup requirements, issue quality, and maintainer responsiveness. Read roughly two recent issue discussions and two merged PRs, enough to see scope, testing, and review norms. Write a short keep/drop judgment with links. A `good first issue` label is a clue, not the selection criterion. No repository in a 2023 video is automatically suitable now.
3. **Run and trace:** follow that repository's setup instructions in a separate checkout. Run the relevant app/example and baseline checks. Follow one small issue or change from its entry point through relevant code and tests. Explain the path and reproduce the reported behavior, or identify a concrete unmet need. Keep commands, revision, and a small amount of evidence; do not map the entire architecture.
4. **Contribute if warranted:** check existing work and claiming rules, clarify scope when appropriate, then make the smallest useful change. Validate it and prepare an explanation of the problem, reasoning, and checks. Submit only if ready and consistent with project norms. Respond to any review that arrives; do not manufacture a deadline for maintainers.

Use [CONTRIBUTION_METHOD.md](CONTRIBUTION_METHOD.md) for the real loop and AI boundaries. A tutorial or model may unblock a specific question; neither should replace the owner's code trace or explanation.

## Evidence and stop rules

The normal checkpoint is a running repository, a grounded suitability judgment, and one understood code path/reproduction. A local tested fix, PR, or review response adds evidence; a merge is unnecessary.

If setup is unreasonable, the issue is already handled, no useful scoped change is available, or maintainer guidance prevents proceeding, stop or use the single replacement. Preserve the commands/errors or linked reasons and what was learned. This is a valid outcome to review, not permission to claim the running-repository or fix checkpoint. A substantive reproduction or test improvement can be useful without a production-code PR; do not force busywork.

Record actual evidence later in [PROGRESS.md](PROGRESS.md). Finish with a brief owner explanation: where the behavior lives, what was attempted, what the evidence supports, and whether to continue, narrow, or drop it. Do not claim progress from watching the videos.

This is input for the eventual integrated approximately ten-day sprint. Scheduling waits for acceptance and integrated planning. Open Source yields to GATE, system design, and product during this phase and may be omitted for a sprint. An unfinished attempt creates no automatic catch-up quota.
