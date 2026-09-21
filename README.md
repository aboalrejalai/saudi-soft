# Saudi Soft

Agent skill for building React apps with [shadcn/ui](https://ui.shadcn.com) and the Saudi Soft theme.

Primary green `#1B8354`. IBM Plex Sans Arabic. lucide icons. 10px and 12px radius. RTL. Light and dark.

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

Pass `-a` so the skill installs for one agent. Do not use `--all`.

```bash
npx skills update
```

Full steps: [INSTALL.md](INSTALL.md)

## What the skill does

- Scaffolds a project with `npx shadcn@latest init`
- Adds components with `npx shadcn@latest add`
- Applies the Soft theme (color, type, radius, RTL, dark mode)
- Uses `lucide-react` for icons

Theme source: [`skills/saudi-soft/references/theme-bridge.css`](skills/saudi-soft/references/theme-bridge.css)

```bash
node path/to/saudi-soft/scripts/evaluate-project.js
node path/to/saudi-soft/scripts/apply-theme.js
```

## License

MIT
