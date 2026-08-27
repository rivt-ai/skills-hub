---
name: spike
description: Validate an idea with a throwaway experiment before committing to a design - build the cheapest thing that answers the question.
---

# Spike: throwaway experiments

A spike answers one question ("does this API do what we need?", "is this fast enough?", "does this design feel right?") with disposable code. Rules:

1. **State the question first.** One sentence, answerable yes/no or with a number. If you cannot phrase it, you are not ready to spike.
2. **Build the cheapest artifact that answers it.** A script in a scratch directory, a hardcoded prototype, a benchmark against fake data. Skip error handling, naming polish, and tests — this code's only job is to produce the answer.
3. **Keep it out of the real codebase.** Work in a temp or scratch directory. Never wire spike code into production paths "since it's already written".
4. **Report the answer, then throw the spike away.** The deliverable is the finding — the answer, the numbers, the gotchas discovered — written down where the real implementation can use it. Delete the spike code; if any of it deserves to live, rewrite it properly with tests.

Timebox it. If the question is not answered within the budget, report what was learned and what remains unknown instead of digging indefinitely.
