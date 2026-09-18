# Integration Pattern

## Pattern: Event-Driven Publish/Subscribe

The primary integration pattern is asynchronous publish/subscribe.

```text
SAP S/4HANA
     |
     | publish
     v
Event Backbone
  /    |    \
 /     |     \
WMS   3PL   Process Automation
```

### Characteristics

- Producer and consumer are loosely coupled.
- Consumers can evolve independently.
- One event can serve multiple consumers.
- Asynchronous processing reduces direct runtime dependency between systems.

## When Integration Suite Is Used

SAP Integration Suite can be positioned between the event infrastructure and consumers when transformation, routing, enrichment, protocol conversion or consumer-specific mediation is required.

It should not automatically be inserted into every event path if direct event consumption is sufficient.

## Failure Model

The architecture assumes that transient failures can occur after an event has been published. Consumers therefore need controlled retry and duplicate handling.
