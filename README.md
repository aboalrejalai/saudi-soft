# Saudi Soft

[![skills.sh](https://skills.sh/b/aboalrejalai/saudi-soft)](https://skills.sh/aboalrejalai/saudi-soft)

Agent Skill لحزمة **Saudi Soft**: بناء تطبيقات React كاملة بـ **upstream shadcn/ui** تحت هوية Soft — أخضر سعودي `#1B8354`، IBM Plex Sans Arabic، lucide، حواف 10/12px، RTL، وفاتح/داكن.

حزمة skill مستقلة. ليست ريجستري مكوّنات حكومي (`@dga`).

**المصدر:** [aboalrejalai/saudi-soft](https://github.com/aboalrejalai/saudi-soft) · الصفحة: [skills.sh/aboalrejalai/saudi-soft](https://skills.sh/aboalrejalai/saudi-soft)

---

## تثبيت

```bash
npx skills add aboalrejalai/saudi-soft -a cursor
```

```bash
npx skills add aboalrejalai/saudi-soft -a claude-code
```

```bash
npx skills add aboalrejalai/saudi-soft -a agents
```

تحديث بعد الـ push:

```bash
npx skills update
```

> لا تستخدم `--all` في Skills CLI — يثبّت على كل الوكلاء ويفتح مجلدات زائدة. حدّد وكيلاً بـ `-a`.

دليل أوفى: [`INSTALL.md`](INSTALL.md)

---

## ماذا تفعل المهارة؟

| البند | Soft |
| --- | --- |
| المكوّنات | `npx shadcn@latest add …` (upstream) |
| الثيم | [`skills/saudi-soft/references/theme-bridge.css`](skills/saudi-soft/references/theme-bridge.css) |
| الأيقونات | `lucide-react` فقط |
| الخط | IBM Plex Sans Arabic |
| الاتجاه | RTL-first |
| الوضع الداكن | class `.dark` + Soft bridge |

سكربتات مساعدة داخل المهارة:

```bash
node path/to/saudi-soft/scripts/evaluate-project.js
node path/to/saudi-soft/scripts/apply-theme.js
```

---

## هيكل الحزمة

```
skills/saudi-soft/     # المهارة (SKILL.md + cli/mcp/rules + theme)
skills.sh.json         # تجميع skills.sh
.claude-plugin/        # marketplace للـ picker
```

---

## License

MIT — هوية الألوان مستوحاة من لوحة SA / NDS؛ الاستخدام التجاري والشخصي مسموح ضمن شروط مشروعك.
