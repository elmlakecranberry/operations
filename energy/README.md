# Energy & Power Dependency Audit

This folder contains the operational audit of energy and power dependencies at Elm Lake Cranberry.

## Purpose

This audit documents how every building and critical piece of equipment actually operates, what it depends on, and where it is fragile. The goal is visibility into failure modes before they happen.

This is a living operational document. It should be updated when:

- New equipment is added
- Fuel sources change
- Backup systems are installed or removed
- A failure reveals a gap not previously documented

## Scope

This audit precedes engineering, sizing, or upgrades. It is not about optimization. It is about understanding what we have, what it needs, and what happens when those needs aren't met.

## Core Question

**What fails first, and how hard is it to add a fallback?**

Every entry in this audit should help answer that question.

## Files

- [energy-power-dependency-audit.md](energy-power-dependency-audit.md) — Asset-by-asset breakdown of energy dependencies and failure modes
- [fuel-and-power-coordination.md](fuel-and-power-coordination.md) — Fuel and power source inventory with storage and delivery risks

## How to Read This Audit

Start with the dependency audit to understand what assets exist and what they need. Then read the fuel coordination document to understand the supply side. The intersection of "asset needs X" and "X has limited runway" is where risk lives.
