# Error Handling & Resilience

## Failure Categories

| Failure | Recommended Response |
|---|---|
| Temporary connectivity failure | Retry with controlled backoff |
| Consumer unavailable | Retry / hold for later processing |
| Invalid payload | Reject and route to controlled error handling |
| Duplicate event | Detect through event ID / business key |
| Contract incompatibility | Reject, alert and investigate version compatibility |
| Permanent business error | Business exception workflow / manual resolution |

## Idempotency

Event-driven architectures must assume that duplicate delivery can occur.

A consumer should maintain a processed-event or business-key strategy so that processing the same event again does not create an unintended duplicate business outcome.

## Dead-Letter Concept

Events that cannot be successfully processed after defined retry attempts should be moved into controlled error handling rather than silently discarded.

The exact retry counts, backoff values and dead-letter configuration are implementation decisions to be validated for the target environment.
