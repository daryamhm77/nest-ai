# RabbitMQ Rules
- Topic exchanges; explicit routing keys = `<context>.<event>` past tense.
- Durable queues + persistent messages for integration events.
- Consumers are idempotent; dedupe by `eventId`. Manual ack after success.
- Dead-letter queues + retry with backoff; cap retries then park to DLQ.
- Publish via the outbox after commit (see `architecture/events.md`).
