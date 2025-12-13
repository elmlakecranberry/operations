# Elm Lake Cranberry Operations

This repository is the execution layer of Elm Lake Cranberry. It documents **how work is done**—not who decides, not why we do it, and not what policies govern us.

## What This Repo Contains

- **SOPs** – Step-by-step procedures for recurring tasks
- **Checklists** – Practical execution aids for daily and seasonal work
- **Systems** – Documentation for tools, software, and vendors we use
- **Runbooks** – Situation-based guides for time-sensitive scenarios
- **Templates** – Blank forms for creating new procedures

## What This Repo Does NOT Contain

- Authority or decision rights
- Policies or governance documents
- Budgets or financial plans
- Scorecards or performance metrics
- Strategic decisions

Those belong in the **management repository**. This repo executes; management governs.

## Relationship to the Management Repo

The management repo defines **what** we do and **who** decides. This repo defines **how** we carry it out.

If there is ever a conflict between this repo and the management repo, defer to management. Policies set there take precedence over procedures documented here.

This repo may reference policies abstractly (e.g., "per the safety policy") but does not restate them.

## How This Repo Works

- Procedures are expected to change frequently
- Clarity and practicality matter more than elegance
- Each SOP must have an owner responsible for keeping it current
- Deprecated procedures move to `/archive/`, not deleted
- Templates exist to maintain consistency

## Folder Structure

```
/operations
├── sop/                 # Standard operating procedures
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

## Who This Repo Is For

Managers and operators who need to know how things work. Not executives reviewing strategy. Not auditors checking compliance. People doing the work.

## Contributing

- Use the templates in `/templates/` when creating new procedures
- Assign an owner to every SOP
- Review procedures periodically—at minimum, annually
- When a procedure is no longer valid, move it to `/archive/`
- Keep it practical. Write like you're explaining to someone who will do this tomorrow.
