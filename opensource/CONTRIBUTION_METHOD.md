# Contribution method

> **Role:** practical workflow for real repository work, subordinate to [ROADMAP.md](ROADMAP.md).
> **Last reviewed:** 2026-09-30.

Use this loop on one issue at a time. It is a working guide, not paperwork to complete before touching code.

1. **Choose and evaluate a repository.** Prefer software you use or can understand, in the existing stack. Check its purpose/license, recent substantive development, a small sample of merged PRs and issue discussions, maintainer responses, contributor guidance, and setup requirements. Stars and labels do not establish health. Choose a tractable component; decline a poor fit with a concrete reason.
2. **Read the rules.** Read README, CONTRIBUTING, code of conduct, issue/PR templates, test instructions, and any applicable repository/AI policies. Notice branch, commit, formatting, and signing conventions. Check whether the issue is current, already claimed, solved, or covered by another PR.
3. **Set up locally.** Use the documented runtime, package manager, and lockfile. Work outside this planning repo. Record the revision, run the relevant application/example and baseline checks, and retain setup failures accurately. Do not silently introduce unrelated dependency updates to make setup work.
4. **Understand and reproduce.** Read the report and recent related discussions. Trace the entry point to relevant implementation and tests; explain the path yourself. Establish expected versus actual behavior with minimal steps or a failing regression test. For improvements without a bug, identify the user need and existing behavior. Read enough surrounding code to understand the contract; do not read the whole repository first.
5. **Communicate when appropriate.** Follow the project's claiming/discussion norm. For unclear or larger work, explain the reproduction and proposed scope before investing heavily. Do not post repetitive “assign me” messages or duplicate another contributor's work. If maintainers have not responded, continue only work that their guidelines permit; waiting is not a reason to force a PR.
6. **Make the smallest coherent change.** Start a task branch from the appropriate updated upstream base. Limit the diff to the problem, preserve local conventions, and avoid opportunistic refactors. If scope expands beyond the slice, narrow it or stop with evidence.
7. **Validate and document.** Run the relevant tests and required checks. For a regression fix, show that the test exposes the original fault and passes with the fix when feasible. Update user-facing docs when behavior requires it. Separate pre-existing failures from new failures; report commands and actual outcomes, including checks not run.
8. **Prepare a clean commit/PR.** Inspect the staged diff for unrelated files, accidental lockfile churn, generated artifacts, and secrets. Follow the repository's commit/PR conventions. Explain the problem, before/after behavior, approach and reasoning, issue link, validation, and limitations. A UI change may need a screenshot. Submit only work you understand and can defend; a local reviewable patch is preferable to a forced PR.
9. **Respond to review.** Read the concern, clarify uncertainty, make scoped revisions, and rerun affected checks. Explain disagreements calmly. Respect the project's pace; avoid repeated pings. A rejection or requested redesign is information, not an invitation to resubmit unchanged elsewhere.
10. **Learn and return.** Record the outcome and one lesson in [PROGRESS.md](PROGRESS.md). Distinguish local progress, submission, feedback, and merge. Prefer the next useful task in a healthy repository already understood; carry or drop unfinished work deliberately.

## AI assistance

AI may help find relevant files, explain unfamiliar code, suggest reproduction/test cases, critique a diff, or edit a PR explanation. Verify its claims against code, execution, and project rules. The owner must understand the problem, each meaningful change, and the test results before submission. Follow any project restrictions or disclosure requirements for AI use.

Do not use AI to manufacture issues, spray PRs across repositories, invent tests/results, or substitute a generated explanation for understanding. Maintainer-facing messages and final changes remain the owner's responsibility. Keep assistance scoped to the current problem.
