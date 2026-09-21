# Install

**https://github.com/aboalrejalai/saudi-soft**

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

Do not use `--all`. It installs into every agent.

## List

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
