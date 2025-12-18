# Assets

This folder contains inventories of physical assets at Elm Lake Cranberry.

## Purpose

These inventories exist to:

- Provide a single source of truth for what we own and operate
- Support maintenance scheduling and tracking
- Feed into the energy audit and other operational planning
- Help with insurance, compliance, and replacement planning

## What belongs here

Physical things that:

- Require maintenance
- Have significant replacement cost
- Are critical to operations
- Need to be tracked for compliance or insurance

## What does NOT belong here

- Consumables (fuel, chemicals, supplies)
- Office equipment and furniture
- Personal tools
- Items tracked elsewhere (e.g., IT assets in a separate system)

## Files

- [buildings.yaml](buildings.yaml) — Structures, shops, storage
- [vehicles.yaml](vehicles.yaml) — Trucks, tractors, ATVs, trailers
- [equipment.yaml](equipment.yaml) — Implements, harvesters, sprayers
- [pumps.yaml](pumps.yaml) — Irrigation and drainage pumps
- [wells.yaml](wells.yaml) — Water supply wells
- [tanks.yaml](tanks.yaml) — Fuel, water, and chemical storage
- [parcels.yaml](parcels.yaml) — Land parcels owned or leased
- [tax-assessments.yaml](tax-assessments.yaml) — Property tax and assessment records

## Relationship to Other Documents

These inventories are referenced by:

- **Energy audit** — Assets listed here should appear in the energy dependency audit if they have power/fuel requirements
- **Maintenance SOPs** — Procedures reference specific assets by name
- **Checklists** — Daily and seasonal checks reference assets

When adding a new asset, consider whether it needs an entry in the energy audit.
