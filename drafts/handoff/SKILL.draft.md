---
name: handoff
description: Compact the current session into a handoff document another agent or a future session can resume from.
---

# Handoff

Write a handoff document capturing this session's state for whoever picks the work up — a fresh agent with none of your context. Include, in order:

1. **Goal**: what the overall task is and who asked for it.
2. **State**: what is done and verified, what is in progress, what has not been started. Name branches, files touched, and commands that prove the done parts work.
3. **Decisions**: every non-obvious choice made and *why* — the alternatives rejected matter as much as the winner.
4. **Gotchas**: dead ends already explored, surprising behavior discovered, things that look wrong but are intentional.
5. **Next step**: the single concrete action to take first, then the remaining steps in order.

Rules: write facts, not narrative — the reader was not there and does not care about the journey. Use absolute references (full paths, commit hashes, issue numbers), never "the file from earlier". Anything you looked up that the reader would have to re-look-up goes in the document. Save it where the work lives (repo docs dir or the location the user names).
