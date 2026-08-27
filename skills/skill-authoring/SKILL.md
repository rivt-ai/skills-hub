---
name: skill-authoring
description: Write a new SKILL.md instruction pack - frontmatter, scope, and style rules for skills that agents actually follow.
---

# Authoring skills

A skill is a directory containing a `SKILL.md`: YAML frontmatter with `name` and `description`, then the instructions. Write one when a workflow is worth repeating across sessions; do not write one for a single task.

Format:

```
---
name: kebab-case-name
description: One sentence saying what it does and when to use it.
---

# Title

Instructions...
```

Rules that make skills work:

1. **The description sells the trigger.** Agents pick skills by description alone, so say *when* to use it, not just what it is.
2. **One workflow per skill.** A skill that covers two jobs gets loaded for the wrong one. Split it.
3. **Write imperatives, not essays.** Numbered steps and hard rules ("never X", "always Y before Z") beat prose about philosophy. Every sentence should change behavior; delete the ones that don't.
4. **Stay tool-agnostic.** Name concepts ("run the test suite") rather than machine-specific commands, unless the skill exists to wrap one specific tool.
5. **Keep it short.** Skills load into the context window; aim for under 30 lines of body. If it needs more, it is documentation, not a skill.

Test it: give the skill to a fresh session with a matching task and check the behavior actually changes.
