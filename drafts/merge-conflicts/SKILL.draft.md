---
name: merge-conflicts
description: Resolve an in-progress git merge or rebase conflict hunk by hunk, preserving the intent of both sides.
---

# Resolving merge conflicts

For an in-progress merge or rebase with conflicts:

1. **Understand both sides first.** For each conflicted file, look at what each branch was trying to do (`git log` both sides of the conflict, read the surrounding code) before touching a hunk. A conflict is two intents colliding; you are resolving intents, not text.
2. **Resolve hunk by hunk.** For each conflict marker: keep one side, keep both (ordered correctly), or write the merged form neither side has yet. Never resolve by wholesale picking "ours" or "theirs" for a file unless you have confirmed the other side's change is genuinely obsolete.
3. **Watch for semantic conflicts.** Code can merge cleanly and still be wrong — a renamed function one side still calls by the old name, a changed signature. After resolving the textual conflicts, build and run the tests; treat failures as remaining conflicts.
4. **Keep the resolution minimal.** No refactoring, no cleanup, no drive-by fixes inside a merge commit — it makes the merge unreviewable.
5. **Verify before concluding**: `git diff` the result against both parents to confirm nothing from either side was silently dropped, then complete the merge/continue the rebase.

If both sides changed the same logic for contradictory reasons and the right merge is not determinable from the code, stop and ask — do not guess away someone's change.
