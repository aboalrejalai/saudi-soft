# AGENTS.md

This repository is a **distributable agent skill**, not a React app. Do not scaffold Vite/Next here, do not run `shadcn init` in this repo, and do not add `package.json` / `src/` at the root.

When the user is **using** Saudi Soft in some other project, follow `skills/saudi-soft/SKILL.md`. This file is only for **editing this repo**.

## What it is

Saudi Soft wraps upstream [shadcn/ui](https://ui.shadcn.com) with a fixed identity:

- Primary `#1B8354` (hover `#166A45`) via CSS variables — never `bg-green-*`
- IBM Plex Sans Arabic as `--font-sans`
- `lucide-react` only (`iconLibrary: lucide`)
- Radius: controls ≈ 10px, cards/dialogs ≈ 12px
- RTL (`dir="rtl"`) + logical spacing (`ms`/`me`/`ps`/`pe`)
- Light + `.dark` tokens from the theme bridge

The skill is **self-contained**. Do not add a dependency on other skill folders.

## Layout

```
README.md                         Human install + overview (single source)
skills.sh.json                    skills.sh grouping
.claude-plugin/marketplace.json   Skill picker metadata
skills/saudi-soft/
  SKILL.md                        Agent entry — read this first for skill behavior
  cli.md                          shadcn CLI flags (never invent flags)
  customization.md                How the theme is applied
  mcp.md / registry.md            Optional MCP + registry notes
  rules/                          Critical UI rules (styling, forms, composition, icons, chat)
  references/
    identity.md                   Color / type / radius / RTL tables
    theme-bridge.css              Injected CSS (markers # saudi-soft-theme)
    recipes.md                    Composition recipes
  scripts/
    evaluate-project.js           Mode A / B / C against cwd
    apply-theme.js                Inject or replace the bridge in the target app CSS
  evals/evals.json                Prompt evals for the skill
```

Install target for humans: `npx skills add aboalrejalai/saudi-soft -a <agent>`. Always pass `-a`. Never document `--all`.

## Edit rules

1. **Behavior lives in `SKILL.md`.** Keep it the single agent entry. Rules, CLI, identity, and recipes stay in the linked files — do not paste those tables back into `SKILL.md`.
2. **Theme source is `references/theme-bridge.css`.** `apply-theme.js` injects that file between `/* # saudi-soft-theme:start */` and `/* # saudi-soft-theme:end */`. Change colors/radius/dark tokens there, then keep `identity.md` in sync.
3. **Scripts are CommonJS** (`require`) so they run in any target project. Keep that. They operate on `process.cwd()` of the **consumer app**, not this repo.
4. **Marketplace / skills.sh** — if you rename the skill folder or description, update `.claude-plugin/marketplace.json` and `skills.sh.json` together.
5. **Do not split install docs.** Install commands belong in `README.md` only.
6. **Do not commit** `.env*`, `skills-lock.json`, `.claude/`, or `node_modules/`.

## Soft identity (do not change unless the user asks)

| Token | Value |
| --- | --- |
| Primary | `#1B8354` |
| Primary hover | `#166A45` |
| Font | IBM Plex Sans Arabic 400–700 |
| Icons | lucide only |
| Radius | `--radius` 12px; `rounded-md` 10px; `rounded-sm` 8px |

Forbidden: `platformscode-new-react`; swapping Soft primary for a random shadcn preset; adding a second icon library.

## When the user asks to build UI

You are then in **consumer mode**. `cwd` is their app, not this repo.

1. Run `node <skill>/scripts/evaluate-project.js` and pick Mode A / B / C from `SKILL.md`.
2. Use the consumer's package runner: `npx shadcn@latest`, `pnpm dlx shadcn@latest`, or `bunx --bun shadcn@latest`.
3. Never guess component APIs — `npx shadcn@latest docs <name>`.
4. Never invent CLI flags — see `skills/saudi-soft/cli.md`.
5. Never `--overwrite` shadcn files without explicit approval.
6. After a preset that rewrites CSS, re-run `apply-theme.js` unless the user opted out of Soft colors.

## Quick commands (consumer app)

```bash
node path/to/saudi-soft/scripts/evaluate-project.js
npx shadcn@latest init --rtl
node path/to/saudi-soft/scripts/apply-theme.js
npx shadcn@latest add button card dialog
npx shadcn@latest docs button
```
