---
name: pr-workflow
description: Take a change from branch to merged pull request - branching, focused commits, PR description, and review response.
---

# Pull request workflow

Drive a change through the full PR lifecycle:

1. **Branch from the right base.** Confirm the target branch first (main? dev?); branch off its latest state with a descriptive name (`feat/…`, `fix/…`).
2. **Commit in reviewable units.** Each commit compiles and passes tests on its own; unrelated changes go in separate commits. Run the project's verify step before every push.
3. **Write the PR for the reviewer.** Description covers: what changed, why, how it was tested, and anything the reviewer should look at first. Link the issue it closes. Keep the diff small — a PR over ~400 changed lines should usually be split.
4. **Respond to review, don't defend.** Address every comment: fix it, or explain why not, in the thread. Push fixes as new commits during review (no force-push mid-review) so reviewers can see what changed.
5. **Merge clean.** CI green, threads resolved, branch up to date with the base. Delete the branch after merge.

Never merge your own PR without review unless the repository's convention explicitly allows it.
