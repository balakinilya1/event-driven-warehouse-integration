# ADR-001: Use an Event Backbone

## Status
Accepted

## Decision
Use an event broker / event mesh as the distribution backbone for relevant warehouse business events.

## Rationale
A centralized event distribution layer reduces producer-consumer coupling and allows multiple consumers to subscribe independently.

## Consequences

### Positive
- Loose coupling.
- Easier consumer expansion.
- Reusable event distribution.
- Better alignment with event-driven architecture.

### Trade-offs
- Additional platform component.
- Requires event governance and operational monitoring.
- Consumers must handle asynchronous processing and duplicates.
