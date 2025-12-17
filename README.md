# Elm Lake Cranberry Operations Handbook

This is the Operations Handbook for Elm Lake Cranberry.

**Start here if you're unsure where to look.** This handbook documents **how work is done**—the procedures, checklists, and systems that keep daily operations running.

---

## What This Handbook Contains

- **SOPs** – Step-by-step procedures for recurring tasks
- **Checklists** – Practical execution aids for daily and seasonal work
- **Systems** – Documentation for tools, software, and vendors we use
- **Runbooks** – Situation-based guides for time-sensitive scenarios
- **Templates** – Blank forms for creating new procedures

## What This Handbook Does NOT Contain

- Authority or decision rights
- Policies or governance documents
- Budgets or financial plans
- Scorecards or performance metrics
- Strategic decisions

Those belong to management. This handbook covers execution, not governance.

## Relationship to Management

Management decides **what** we do and **who** decides. This handbook documents **how** we carry it out.

If there is ever a conflict between this handbook and a management decision, defer to management. Management decisions take precedence over procedures documented here.

This handbook may reference policies (e.g., "per the safety policy") but does not restate them.

## How This Handbook Works

- Procedures are expected to change frequently
- Clarity and practicality matter more than elegance
- Each SOP must have an owner responsible for keeping it current
- Deprecated procedures move to `/archive/`, not deleted
- Templates exist to maintain consistency

## Folder Structure

```
/operations
├── sops/                # Standard operating procedures
│   ├── safety/
│   ├── equipment/
│   ├── irrigation/
│   ├── frost-protection/
│   ├── harvest/
│   └── maintenance/
├── checklists/          # Execution aids and daily checklists
├── systems/             # Tool and software documentation
│   ├── accounting/
│   ├── payroll-hr/
│   ├── file-storage/
│   ├── communications/
│   └── gis-mapping/
├── runbooks/            # Situation-based response guides
├── templates/           # Blank templates for new procedures
└── archive/             # Deprecated procedures (preserved)
```

## Who This Handbook Is For

Managers and operators who need to know how things work. Not executives reviewing strategy. Not auditors checking compliance. People doing the work.

## Contributing

- Use the templates in `/templates/` when creating new procedures
- Assign an owner to every SOP
- Review procedures periodically—at minimum, annually
- When a procedure is no longer valid, move it to `/archive/`
- Keep it practical. Write like you're explaining to someone who will do this tomorrow.

---

## Technical Notes (for maintainers)

This handbook is stored as a Git repository. Changes are tracked through version control, which preserves history and allows rollback if needed. The folder structure above reflects the actual directory layout in the repository.
