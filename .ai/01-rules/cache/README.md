# Caching Rules
- Cache only idempotent reads; define TTL + invalidation per key up front.
- Cache-aside by default; write-through only for hot, consistent data.
- Key includes tenant + version: `v1:tenant:entity:id`.
- Stampede protection (locks / jitter). Never cache authz decisions for sensitive data.
- Make cache optional — the system must work (slower) if cache is down.
