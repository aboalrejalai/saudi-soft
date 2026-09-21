# Install Guide — Saudi Soft

Agent Skill package. Source of truth:

**https://github.com/aboalrejalai/saudi-soft**

Catalog page: [skills.sh/aboalrejalai/saudi-soft](https://skills.sh/aboalrejalai/saudi-soft)

Layout matches [skills.sh / Skills CLI](https://github.com/vercel-labs/skills):

| File | Role |
| --- | --- |
| `skills/saudi-soft/` | Soft skill (shadcn + Soft theme, lucide, RTL, dark) |
| [`skills.sh.json`](skills.sh.json) | Groupings for the skills.sh repo page |
| [`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json) | Interactive skill picker |

## Prerequisites

- Node.js 18+
- A supported coding agent (Cursor, Claude Code, Codex, …)

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

Explicit skill name (same result — this repo has one skill):

```bash
npx skills add aboalrejalai/saudi-soft --skill saudi-soft -a cursor
```

> **Never use `--all`.** It expands to every agent and scatters stray folders. Always pass `-a <agent>`.

## List skills

```bash
npx skills add aboalrejalai/saudi-soft --list
```

## Install from a local clone

```bash
git clone https://github.com/aboalrejalai/saudi-soft.git
cd saudi-soft
npx skills add . -a cursor
```

## Update

```bash
npx skills update
```

Or re-add:

```bash
npx skills add aboalrejalai/saudi-soft --skill saudi-soft -a cursor
```

## What this is / is not

| | |
| --- | --- |
| **Is** | Soft identity overlay on upstream shadcn (theme, lucide, RTL, dark) |
| **Is not** | Formal DGA `@dga` component registry |

For government / formal NDS work, use a separate package — not this repo.
