# Domain & Integration Events

- **Domain events**: raised inside aggregates, handled in-process within the same context.
- **Integration events**: published to a broker for other contexts; versioned, schema-stable.
- Naming: past tense — `InvoiceIssued`, `PaymentCaptured`.
- Events are immutable facts; include ids + a `occurredAt` + `eventVersion`.
- Publish AFTER the transaction commits (outbox pattern) to avoid ghost events.
