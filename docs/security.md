# Security Architecture

## Principles

- Least privilege.
- Strong authentication.
- Encrypted transport.
- Segregation of environments.
- Controlled access to event channels.
- No credentials in source code.
- Centralized secret/certificate management where applicable.

## Trust Boundaries

```text
SAP S/4HANA | Event Infrastructure | Integration Runtime | External Consumer
```

Each boundary should have explicitly defined authentication and authorization.

## Implementation Considerations

The exact authentication mechanism and credential objects depend on the selected SAP services, tenant configuration and consumer connectivity. Those details must be validated during implementation.
