---
name: plan
description: Write a concrete implementation plan as markdown without executing anything - research first, then plan, then stop.
---

# Plan only

Produce a plan, not changes. Do not edit files, run write-commands, or commit — reading code and running read-only commands to inform the plan is encouraged.

The plan must contain:

1. **Context**: the problem being solved and why, in two or three sentences.
2. **Approach**: the chosen design in enough detail that another agent could execute it without re-deriving decisions. Name the files to touch and the existing functions or patterns to reuse — a plan that says "add a module" without saying where is not a plan.
3. **Steps**: an ordered list of small, verifiable steps. Each step names what changes and how to check it worked.
4. **Risks**: what could go wrong, what is uncertain, and what was deliberately left out of scope.
5. **Verification**: how to prove the finished work is correct end-to-end (commands to run, behavior to observe).

Prefer one recommended approach over a menu of options; mention an alternative only when the choice genuinely belongs to the reader. End by presenting the plan — never by starting the work.
