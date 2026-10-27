# Saudi Soft

Agent skill for building React apps with [shadcn/ui](https://ui.shadcn.com) and the Saudi Soft theme.

**https://github.com/aboalrejalai/saudi-soft**

Primary green `#1B8354`. IBM Plex Sans Arabic. lucide icons. 10px and 12px radius. RTL. Light and dark.

| Path | Role |
| --- | --- |
| `skills/saudi-soft/` | Skill (shadcn, Soft theme, lucide, RTL, dark mode) |
| `skills.sh.json` | skills.sh grouping |
| `.claude-plugin/marketplace.json` | Skill picker |

## Prerequisites

- Node.js 18+
- Cursor, Claude Code, Codex, or another agent supported by the Skills CLI

## Install

```bash
npx skills add aboalrejalai/saudi-soft -a cursor
```

```bash
npx skills add aboalrejalai/saudi-soft -a claude-code
```

```bash
npx skills add aboalrejalai/saudi-soft -a agents
```

```bash
npx skills add aboalrejalai/saudi-soft --skill saudi-soft -a cursor
```

Pass `-a` so the skill installs for one agent. Do not use `--all`. It installs into every agent.

```bash
npx skills add aboalrejalai/saudi-soft --list
```

## Local clone

```bash
git clone https://github.com/aboalrejalai/saudi-soft.git
cd saudi-soft
npx skills add . -a cursor
```

## Update

```bash
npx skills update
```

```bash
npx skills add aboalrejalai/saudi-soft --skill saudi-soft -a cursor
```

## What the skill does

- Scaffolds a project with `npx shadcn@latest init`
- Adds components with `npx shadcn@latest add`
- Applies the Soft theme (color, type, radius, RTL, dark mode)
- Uses `lucide-react` for icons
- Preferred Soft recipes for app shell, page header, KPI cards, and hub cards (only when those surfaces apply)

Theme source: [`skills/saudi-soft/references/theme-bridge.css`](skills/saudi-soft/references/theme-bridge.css)

Composition recipes: [`skills/saudi-soft/references/recipes.md`](skills/saudi-soft/references/recipes.md)

Identity tables: [`skills/saudi-soft/references/identity.md`](skills/saudi-soft/references/identity.md)

Rebrand (explicit request): [`skills/saudi-soft/references/rebrand.md`](skills/saudi-soft/references/rebrand.md)

Agent entry: [`skills/saudi-soft/SKILL.md`](skills/saudi-soft/SKILL.md)

```bash
node path/to/saudi-soft/scripts/evaluate-project.js
node path/to/saudi-soft/scripts/apply-theme.js
```

## License

MIT
