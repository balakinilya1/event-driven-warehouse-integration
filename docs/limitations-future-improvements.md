# Limitations & Future Improvements

## Current Limitations

1. Concrete SAP event identifiers require validation against the target S/4HANA release.
2. Exact payload fields require access to the selected event definition.
3. Consumer interfaces are represented logically rather than against a named customer WMS/3PL contract.
4. Performance and capacity figures are not asserted without a target landscape.
5. Tenant-specific security configuration is outside the scope of this repository.

## Future Improvements

- Add a validated SAP event catalog.
- Add concrete event schemas after target-system validation.
- Add sequence and interaction diagrams for key scenarios.
- Add sample consumer mappings.
- Add CI/CD and transport governance details.
- Add operational runbooks.
- Add performance test results from a real or sandbox environment.
