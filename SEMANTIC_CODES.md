# Semantic `code` Convention (Blossom ↔ elc-operations)

## Purpose

This document defines the canonical convention for **semantic **``** identifiers** used to reference real-world assets across systems.

These codes are the **stable, human-legible identity** for physical entities such as pumps, wells, buildings, and parcels.

They are designed to:

- Be readable by humans and AI
- Be stable across time
- Survive system changes
- Serve as the bridge between Blossom and `elc-operations`

> **IDs identify rows.**\
> **Codes identify things.**

---

## Relationship to Other Identifiers

Every persistent real-world entity should have **three distinct identifiers**:

| Identifier      | Role                            | Mutability          |
| --------------- | ------------------------------- | ------------------- |
| `id` (int)      | Database primary key (Blossom)  | Immutable           |
| `code` (string) | Semantic, cross-system identity | Immutable by policy |
| `name` (string) | Human-friendly display label    | Mutable             |

Example:

```
id:   17
code: bog3_main
name: Bog 3 Main Pump
```

Rules:

- `id` is internal to the database
- `code` is used everywhere outside the database (YAML, AI reasoning, audits)
- `name` is for UI and human display only

---

## Which Entities Require a `code`

Add a `code` identifier to tables or asset types that represent **persistent, real-world entities**.

### MUST have `code`

**Infrastructure / Assets**

- Pumps
- Equipment
- Wells
- Tanks
- Reservoirs
- Generators
- Boilers
- Buildings
- Vehicles / Machines

**Land / Spatial**

- Fields
- Parcels
- Bogs / Blocks (if distinct)
- Operational zones

**Organizational (if long-lived)**

- Farms
- Sites / Locations

These entities:

- Exist independently of software
- Are referenced across systems
- Are discussed in audits, planning, and AI reasoning
- Must remain intelligible years later

---

### MUST NOT have `code`

Do NOT add `code` identifiers to entities that represent **events, logs, state, or relationships**, including:

- Irrigation events
- Runtime logs
- Sensor readings
- Alerts
- Forecasts
- Tasks
- Measurements
- Join tables
- Derived or temporary records

If the identity of a row is defined by *what happened and when*, it does not get a code.

---

## Naming & Syntax Rules (Canonical)

### Allowed characters

- Lowercase letters (`a–z`)
- Numbers (`0–9`)
- Underscore (`_`)

### Disallowed

- Spaces
- Hyphens
- CamelCase
- Special characters
- Leading or trailing underscores

---

## Structural Pattern

```
<location>_<role>[_<qualifier>]
```

Where:

- **location** = physical place, field, bog, building, or area
- **role** = what the thing does
- **qualifier** (optional) = main, aux, east, west, backup, etc.

### Examples (valid)

**Pumps**

- `bog3_main`
- `bog3_aux`
- `north_reservoir_transfer`

**Equipment**

- `irrigation_gen_1`
- `shop_wood_boiler`
- `diesel_transfer_pump`

**Wells**

- `well_north_deep`
- `well_bog7_shallow`

**Buildings**

- `main_shop`
- `pump_house_bog3`
- `north_house`

**Fields / Parcels**

- `bog3`
- `bog7_west`
- `north_parcel_12`

---

## Stability & Change Policy

- Codes are **write-once by policy**
- Codes must be **globally unique**
- Codes must **never be reused**, even after retirement
- Changing a code is a **breaking change**

### Replacement rules

- Same role, same location → keep the code
- Repurposed or relocated asset → create a new code
- Retired assets → code remains reserved forever

Treat codes like:

- DNS names
- Kubernetes resource names
- Accounting account codes

---

## Cross-System Usage Rules

- Blossom **creates and owns** asset records and codes
- `elc-operations` **reuses those codes**
- YAML files in `elc-operations` reference **codes only**
- Integer database IDs must never appear in Git-tracked files

Example (`elc-operations`):

```yaml
pump_code: bog3_main
fuel_type: diesel
criticality: high
```

---

## Transitional Note

Until Blossom has native `code` columns:

- Codes may be defined and maintained here as canonical intent
- These codes should be treated as **future Blossom identifiers**
- When Blossom is updated, these codes should be backfilled verbatim

This document is authoritative for naming and identity semantics during the transition period.

---

## One-Line Rule (for humans and AI)

> **If humans or AI will ever talk about it as a thing, it gets a **``**.**\
> **If it’s just something that happened, it does not.**

