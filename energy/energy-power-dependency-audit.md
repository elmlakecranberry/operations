# Energy & Power Dependency Audit

This document catalogs every building and critical piece of equipment at Elm Lake Cranberry, documenting what each asset depends on to function and what happens when that dependency fails.

## Guidance for Filling Out This Table

### What qualifies as an Asset?

An asset is anything that:

- Is required for farm operations (irrigation, harvest, frost protection, etc.)
- Supports buildings people work or live in
- Would cause operational disruption if it failed

Include buildings, pumps, motors, heating systems, refrigeration, and any equipment that cannot be easily replaced or worked around.

### How to think about Failure Mode

Failure mode describes what happens when the primary energy source is unavailable. Be specific:

- "Pipes freeze within 24 hours"
- "Cannot irrigate"
- "Building uninhabitable"
- "Harvest stops"

Avoid vague descriptions like "doesn't work." The failure mode should make the consequence obvious.

### How to estimate Days Until Failure

This is not about equipment breakdown. It's about how long you can operate without the primary energy source before the failure mode occurs.

- A propane heater with a full tank might have 7 days of runtime
- A building with no backup heat in winter might have 0.5 days before pipes freeze
- An irrigation pump with no backup might have 0 days (immediate failure)

Use realistic assumptions. Assume winter conditions unless otherwise noted.

### Empty Secondary Energy Source

If the Secondary Energy Source column is empty, that asset has no fallback. This is not necessarily bad, but it is a fragility that should be documented and understood.

---

## Asset Dependency Table

| Asset | Type | Primary Function | Primary Energy Source | Secondary Energy Source | Electricity Required? | Backup Power Today | Failure Mode | Days Until Failure | Fallback Difficulty | Notes |
|-------|------|------------------|----------------------|------------------------|----------------------|-------------------|--------------|-------------------|--------------------| ------|
| | | | | | | | | | | |

---

## How to Use This Table

This table is used to prioritize upgrades and identify critical gaps.

**Prioritization criteria:**

1. **Days Until Failure** — Assets with the shortest runway are the most urgent
2. **Failure Mode severity** — Some failures are inconvenient; others are catastrophic
3. **Fallback Difficulty** — Easy fallbacks should be implemented first
4. **Seasonal timing** — Winter failures are more dangerous than summer failures

**Review process:**

1. Sort by Days Until Failure (ascending)
2. For each asset with less than 3 days runway, ask: "What would it take to extend this?"
3. Document the answer in a separate planning document
4. Repeat quarterly or after any significant change

This table is for visibility. Planning and engineering decisions happen elsewhere.
