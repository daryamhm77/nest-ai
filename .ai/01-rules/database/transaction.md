# Transactions

- One transaction per use case, opened in the application layer (Unit of Work).
- Keep transactions short; do no I/O (HTTP, broker publish) inside them — use the outbox.
- Choose isolation deliberately; `READ COMMITTED` default, `SERIALIZABLE` for invariants at risk.
- Handle serialization failures with bounded retries.
- One aggregate per transaction (see `architecture/aggregates.md`).
