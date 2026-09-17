# ADR-005: Consumer-Specific Transformation

## Status
Accepted

## Decision
Perform consumer-specific transformation in the integration layer rather than changing the producer payload for every consumer.

## Rationale
Different consumers may require different formats or protocols. Keeping this logic outside the source business application protects producer stability and reduces coupling.

## Trade-off
The integration layer becomes responsible for additional transformation logic and therefore requires appropriate testing and monitoring.
