# Interceptors

Use for cross-cutting concerns only:
- Response shaping / serialization (`ClassSerializerInterceptor`).
- Logging + request timing.
- Caching (`CacheInterceptor`) for safe idempotent GETs.
- Transaction-per-request only if your model genuinely needs it (prefer explicit UoW).

Do NOT put business rules in interceptors. Keep them generic and reusable.
