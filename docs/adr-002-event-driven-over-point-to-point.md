# ADR-002: Event-Driven over Point-to-Point

## Status
Accepted

## Decision
Prefer asynchronous event-driven integration for warehouse-relevant business changes where near-real-time propagation is required.

## Rationale
Point-to-point interfaces increase coupling as consumers grow. Publish/subscribe allows the producer to publish once while consumers evolve independently.

## Consequence
Consumers must tolerate asynchronous delivery and implement appropriate resilience.
