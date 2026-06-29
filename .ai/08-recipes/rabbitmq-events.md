# Recipe: RabbitMQ Integration Events
1. Write event to an outbox table in the same transaction as the state change.
2. A relay publishes outbox rows to the topic exchange after commit, marks them sent.
3. Consumers are idempotent (dedupe by `eventId`), manual-ack on success.
4. DLQ + bounded retry with backoff for failures.
Rules: `01-rules/rabbitmq/README.md`, `01-rules/architecture/events.md`.
