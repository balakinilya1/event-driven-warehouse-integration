# ADR-004: Govern Event Contracts

## Status
Accepted

## Decision
Treat business events as governed integration contracts.

## Rationale
Multiple consumers depend on event structure. Uncontrolled breaking changes can affect the entire subscriber landscape.

## Rules

- Version contracts.
- Document mandatory fields.
- Avoid unnecessary producer-specific fields.
- Communicate breaking changes.
- Validate consumer compatibility before promotion.
