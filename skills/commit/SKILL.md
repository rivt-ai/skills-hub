---
name: commit
description: Write a clean conventional commit for the staged or pending changes, splitting unrelated work into separate commits.
---

# Commit workflow

1. Run `git status` and `git diff` (staged and unstaged) to see what actually changed. Never commit blind.
2. If the changes mix unrelated concerns (a feature plus a drive-by refactor, formatting plus logic), split them: stage and commit each concern separately.
3. Write the message in conventional-commit form: `type(scope): summary`.
   - Types: `feat`, `fix`, `refactor`, `docs`, `test`, `chore`, `perf`, `ci`.
   - Summary in the imperative mood, lower case, no trailing period, under 72 characters.
   - Add a body only when the diff cannot explain *why* the change was made.
4. Never commit files the user did not touch for this task (lockfiles churned by tooling, editor config, secrets). If one is staged, unstage it and say so.
5. Show the final message before committing when the change is large or destructive; otherwise commit and report the hash.
