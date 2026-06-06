# UI/UX Pro Max (Claude Code Skill)

UI/UX design intelligence for web and mobile. A searchable, BM25-ranked database of
67 UI styles, 161 color palettes, 57 font pairings, 161 product types, 99 UX
guidelines, and 25 chart types across 15+ technology stacks, plus a reasoning engine
that generates a complete, tailored design system from a project description.

Claude loads `SKILL.md` automatically when a task involves UI structure, visual
design, interaction patterns, or UX quality control. See `SKILL.md` for the full
trigger criteria and workflow.

## Layout

```
.claude/skills/ui-ux-pro-max/
├── SKILL.md          # Skill definition (auto-loaded by Claude Code)
├── scripts/          # search.py (CLI), core.py (BM25), design_system.py
├── data/             # CSV knowledge base (styles, colors, typography, ux, stacks/…)
├── LICENSE           # Upstream MIT license
└── README.md
```

## Usage

Requires Python 3 (standard library only — no third-party dependencies). Run from the
repository root:

```bash
# Generate a complete design system (start here for new pages/projects)
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "beauty spa wellness" --design-system -p "Serenity Spa"

# Search a specific domain: style, color, typography, ux, product, landing, chart, …
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "minimalism dark mode" --domain style

# Stack-specific best practices
python3 .claude/skills/ui-ux-pro-max/scripts/search.py "list performance" --stack react
```

## Attribution

Vendored from [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill)
(MIT License, © Next Level Builder). Script invocation paths in `SKILL.md` were
adjusted to the `.claude/skills/ui-ux-pro-max/` install location.
