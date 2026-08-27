---
name: code-review
description: Review a diff or branch for correctness, clarity, and scope creep, reporting concrete findings ranked by severity.
source: "Adapted from mattpocock/skills (engineering/code-review), https://github.com/mattpocock/skills"
---

# Code review

Review the requested changes (a diff, a branch against its base, or named files) and report findings — do not edit anything.

For each file changed, check in this order:

1. **Correctness**: broken edge cases, off-by-ones, unhandled errors, race conditions, resource leaks. For every suspected bug, state the concrete input or state that triggers it — a finding without a failure scenario is a guess, drop it.
2. **Scope**: changes unrelated to the stated purpose. Flag drive-by edits; they belong in their own commit.
3. **Clarity**: names that mislead, comments that restate the code, functions doing more than their name says.
4. **Tests**: does new behavior have a test that would fail without the change? Are the tests asserting outcomes, not implementation details?

Report findings ranked most-severe first, each with `file:line`, a one-sentence claim, and the failure scenario. If nothing survives scrutiny, say so plainly — an empty review is a valid result. Do not pad with style nitpicks the project's linter already enforces.
