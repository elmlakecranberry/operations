# AI Agent Operating Rules — elc-operations

This repository contains canonical operational state for Elm Lake Cranberry.

---

## Rules

- Asset inventories are stored in YAML under `/assets/`
- Markdown is used only for audits, reasoning, decisions, and procedures
- Runtime, historical, or time-series data does not belong in Git
- Do not create Markdown tables for canonical inventories
- Do not convert YAML files to Markdown
- Do not invent asset IDs

---

## Authority

The authoritative source for storage format decisions is:

```
foundation/DATA-MODEL.md
```

When in doubt, consult that document.
