# Scalability Review
1. Stateless services (state in DB/Redis), enabling horizontal scale.
2. Async for slow/cross-context work (queues, events).
3. Read scaling via read models/replicas/caching where measured.
4. Idempotency for retried operations.
5. Backpressure + rate limiting under load.
6. Partitioning/sharding strategy if data growth demands it.
7. Graceful degradation when a dependency is down.
