# Monitoring & Operations

## Monitoring Layers

### Event Infrastructure
- Connectivity
- Event publication
- Subscription status
- Delivery failures

### Integration Runtime
- Message processing
- Transformation failures
- Routing failures
- Retry status

### Business Processing
- Business object ID
- Event ID
- Correlation ID
- Processing status

## Correlation

A common correlation identifier should be propagated across integration components where technically possible.

Example:

```text
Business Transaction
       |
       v
eventId + correlationId
       |
       +--> Event Backbone
       |
       +--> Integration Runtime
       |
       +--> Consumer
```

## Operational KPIs

- Event processing success rate.
- Processing latency.
- Retry volume.
- Dead-letter volume.
- Consumer availability.
- Duplicate-event rate.
