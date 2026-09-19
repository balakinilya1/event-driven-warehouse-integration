# Test Strategy

## Test Levels

### Unit / Component
Validate transformations, routing and validation logic.

### Integration
Validate event publication, subscription and consumer processing.

### End-to-End
Validate:

```text
S/4HANA business change
        -> event
        -> event backbone
        -> integration / consumer
        -> expected warehouse outcome
```

### Negative Testing

Test:

- Invalid payload.
- Missing business identifier.
- Consumer unavailable.
- Duplicate event.
- Expired/invalid credentials.
- Temporary connectivity outage.
- Unsupported event version.

### Recovery Testing

Verify that a transient failure can recover without creating duplicate business results.
