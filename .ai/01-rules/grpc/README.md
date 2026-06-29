# gRPC Rules
- Proto files are the contract; version packages, never break wire compat.
- Deadlines/timeouts on every call; propagate cancellation.
- Map domain exceptions to canonical gRPC status codes.
- Use interceptors for auth, logging, tracing.
- Keep messages flat; reference other aggregates by id.
