# skill hub

A collection of skills. Each skill is a `SKILL.md` instruction pack an agent
loads on demand.

## Layout

Each skill is a directory under `skills/` containing a `SKILL.md` with
`name` and `description` frontmatter followed by the instructions:

```
skills/<name>/SKILL.md
```

## Drafts

`drafts/` holds candidate skills as `SKILL.draft.md` files, not yet promoted
to `skills/`.

## Sources

Some skills are adapted from other public skill collections rather than
written from scratch here. Each adapted skill carries a `source:` field in
its frontmatter; the collections referenced so far:

- [mattpocock/skills](https://github.com/mattpocock/skills) — `grilling`,
  `tdd`, `code-review`, `drafts/handoff`, `drafts/merge-conflicts`.
- [DietrichGebert/ponytail](https://github.com/DietrichGebert/ponytail) (MIT) — `ponytail`.
- Claude Code's own built-in `/simplify` skill (Anthropic) — `drafts/simplify`.

Checked but not attributed for lack of a single confident match: `commit`,
`debugging`, `plan`, `skill-authoring`, `spike`, `drafts/pr-workflow`,
`drafts/humanizer`, `drafts/grounded-citations` — each shares a name/concept
with several independently-written public skills, but none matched closely
enough to credit one over the others.
