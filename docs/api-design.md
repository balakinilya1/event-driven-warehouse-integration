# Interface Design

## Interface Types

The architecture contains two broad interface categories:

### 1. Event Interface

```text
S/4HANA -> Event Backbone
```

Purpose: publish a business event asynchronously.

### 2. Consumer Integration Interface

```text
Event Backbone -> Integration Suite -> Consumer
```

Purpose: transform, route or mediate the event where the consumer requires additional integration logic.

## Design Considerations

- Avoid exposing internal producer implementation details.
- Prefer stable business identifiers.
- Include correlation information.
- Version contracts explicitly.
- Keep consumer-specific transformation outside the producer where possible.

No concrete endpoint URLs are defined because they are tenant/environment-specific.
