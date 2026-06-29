# Kafka Rules
- Topics named `<context>.<event>.v<n>`; schema-registered (Avro/JSON Schema).
- Partition key = aggregate id to preserve per-entity ordering.
- Consumers idempotent + track offsets; commit after processing.
- Compaction for state topics, retention for event streams — choose deliberately.
- Backward/forward compatible schema evolution only.
