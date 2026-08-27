---
name: simplify
description: Sweep recently changed code for reuse, dead weight, and needless abstraction - quality cleanup only, no behavior changes.
---

# Simplify

Review the recent changes (the diff, not the whole codebase) and apply cleanups that reduce code without changing behavior:

1. **Reuse over reinvention**: replace hand-rolled logic with an existing helper in the codebase or the standard library.
2. **Delete the unused**: parameters nothing passes, branches nothing reaches, flags nothing sets, comments restating the code.
3. **Collapse needless indirection**: an interface with one implementation, a function called once that adds no name value, a config knob with one possible value — inline them.
4. **Flatten**: early returns instead of nested conditionals; guard clauses instead of arrow code.
5. **Right altitude**: move code to where its concept lives; a helper used by one file does not belong in a shared utils package.

Rules: behavior stays identical — run the tests after every cleanup; no drive-by refactors outside the changed area; if a simplification is debatable, list it as a suggestion instead of applying it. This is not a bug hunt: report suspected bugs separately, do not fix them here.
