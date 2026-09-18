# Logical Mapping

This is a logical mapping, not a claim of a configured SAP field-level mapping.

| Logical Source | Logical Event Attribute | Consumer Usage |
|---|---|---|
| Business object identifier | `businessObject.id` | Correlation / lookup |
| Event type | `eventType` | Routing |
| Event version | `eventVersion` | Contract compatibility |
| Event timestamp | `occurredAt` | Audit / processing latency |
| Event identifier | `eventId` | Idempotency |
| Correlation identifier | `correlationId` | End-to-end tracing |
| Business payload | `data` | Consumer-specific processing |

Exact SAP-to-target field mapping should be created during implementation once the concrete event schema and target WMS/3PL contract are confirmed.
