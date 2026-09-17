# ADR-003: Idempotent Consumers

## Status
Accepted

## Decision
Consumers must implement idempotent processing.

## Rationale
Distributed event processing can result in duplicate delivery or retries. The same event must not create unintended duplicate business outcomes.

## Implementation Direction

Use an event ID, business object key, or a combination of stable identifiers as a deduplication key.

Exact implementation depends on the target consumer.
