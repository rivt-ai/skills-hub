# skill hub

Default skill hub. Skills are `SKILL.md` instruction packs the agent loads on demand.

## Install

This hub is configured by default, so:

```
skills search            # browse what's here
skills install commit    # install one skill
skills install --all     # everything
```

In the TUI, `/skills install` opens a searchable picker.

## Layout

Each skill is a directory under `skills/` containing a `SKILL.md` with
`name` and `description` frontmatter followed by the instructions:

```
skills/<name>/SKILL.md
```

## Drafts

`drafts/` holds candidate skills as `SKILL.draft.md` files. The installer only
recognizes `SKILL.md`, so drafts are not installable until promoted: move the
directory under `skills/` and rename the file to `SKILL.md`.

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

## Adding a hub of your own

Any git repository with this layout works. Point your agent's skills config at it:

```
SKILLS_HUBS="rivt-ai/skills,you/your-skills" skills search
```
