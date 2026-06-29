# Redis Rules
- Use for caching, rate-limit counters, BullMQ queues, and ephemeral sessions.
- Always set TTLs; never store the only copy of durable data in Redis.
- Namespace keys: `<service>:<entity>:<id>`. Document key schemas.
- Use `SETNX`/Redlock for distributed locks; keep lock TTL > max work time.
- Separate logical DBs/instances for cache vs queue.
