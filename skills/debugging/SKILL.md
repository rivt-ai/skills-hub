---
name: debugging
description: Systematic root-cause debugging - reproduce, hypothesize, instrument, and confirm before fixing anything.
---

# Systematic debugging

Never fix what you have not diagnosed. Work in four phases:

1. **Reproduce**: get a minimal, reliable reproduction. If you cannot trigger the bug on demand, that is the first problem to solve. Capture the exact command, input, and observed-vs-expected output.
2. **Hypothesize**: read the error and the relevant code, then state one specific hypothesis about the cause — a claim precise enough to be wrong. List what evidence would confirm or kill it.
3. **Instrument**: gather that evidence with the cheapest probe available — a log line, a debugger breakpoint, a narrowed test, `git bisect`. Change one variable at a time. If the evidence kills the hypothesis, return to step 2; never stack guesses.
4. **Fix and confirm**: fix the confirmed cause, re-run the reproduction to show it passes, and run the surrounding tests to show nothing else broke. Remove the instrumentation.

Anti-patterns to refuse: shotgun edits ("maybe this helps"), fixing the symptom where it appears instead of where it originates, and declaring victory without re-running the original reproduction.
