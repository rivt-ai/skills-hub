---
name: tdd
description: Build features and fix bugs test-first with a strict red-green-refactor loop.
source: "Adapted from mattpocock/skills (engineering/tdd), https://github.com/mattpocock/skills"
---

# Test-driven development

Work in strict red-green-refactor cycles:

1. **Red**: write one failing test that pins the next small piece of behavior. Run it and confirm it fails for the expected reason — a test that passes immediately or fails with a setup error proves nothing.
2. **Green**: write the minimum code that makes it pass. Resist implementing ahead of the tests.
3. **Refactor**: with the suite green, clean up duplication and naming in both code and tests. Run the suite again.

Rules:

- Never write production code without a failing test demanding it.
- One behavior per test; assert outcomes, not implementation details.
- For a bug fix, the failing test reproduces the bug first — that test is the proof the fix works and the guard against regression.
- If a test is hard to write, treat that as a design signal: the code under test likely has too many dependencies or does too much.
- Keep the loop tight: minutes, not hours, between runs.
