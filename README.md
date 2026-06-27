# skills

Claude Code skills installed in this repository.

## Available skills

### `ui-ux-pro-max`

UI/UX design intelligence for web and mobile — 67 styles, 161 color palettes,
57 font pairings, 99 UX guidelines, and 25 chart types across 15+ tech stacks
(React, Next.js, Vue, Svelte, Astro, SwiftUI, React Native, Flutter, Tailwind,
shadcn/ui, and more). Sourced from
[nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill)
(MIT).

Installed at [`.claude/skills/ui-ux-pro-max/`](.claude/skills/ui-ux-pro-max/):

- `SKILL.md` — skill definition and model-facing instructions
- `scripts/` — `search.py` / `core.py` / `design_system.py` (priority-based
  search over the bundled databases; requires `python3`)
- `data/` — CSV databases of styles, palettes, typography, UX guidelines,
  charts, and per-stack guidance
- `LICENSE` — upstream MIT license, preserved for attribution

## How skills are used

Claude Code auto-discovers any skill under `.claude/skills/<name>/SKILL.md`
relative to where it runs, so every session started in this repo picks up the
skills above automatically. A skill triggers when your request matches its
`description` — for `ui-ux-pro-max`, that covers planning, building, designing,
reviewing, or refactoring UI/UX (websites, landing pages, dashboards, mobile
apps, components, color/typography systems, etc.). You can also invoke it
explicitly with `/ui-ux-pro-max`.

## Installing elsewhere

The skill is scoped to **this repo** by default. To make it available in other
projects or on your local machine:

- **User-level (all your projects)** — copy the skill folder into your global
  skills directory:

  ```bash
  cp -r .claude/skills/ui-ux-pro-max ~/.claude/skills/
  ```

- **From the upstream source** — clone and run the official installer:

  ```bash
  git clone https://github.com/nextlevelbuilder/ui-ux-pro-max-skill.git
  cd ui-ux-pro-max-skill && npx uipro-cli init --ai claude
  ```

> Note: `ui-ux-pro-max` runs Python scripts to search its databases, so
> `python3` must be available for full functionality.
