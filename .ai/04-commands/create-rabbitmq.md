# Command: create-rabbitmq

**Intent:** Wire a publisher + consumer for an event.

## Inputs
- event name, routing key, payload.

## Steps
1. Define versioned event contract (`01-rules/architecture/events.md`).
2. Publish via outbox after commit.
3. Implement idempotent consumer + DLQ + retry.

## Output
Outbox publisher + idempotent consumer with DLQ.

> Obey all of `01-rules/**`. Use the matching `06-templates/*`. Cite what you applied.
