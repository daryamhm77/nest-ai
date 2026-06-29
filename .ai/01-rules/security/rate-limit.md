# Rate Limiting

- Global throttler (`@nestjs/throttler`) + stricter limits on auth + write-heavy routes.
- Key by IP + account where possible; back with Redis in multi-instance deployments.
- Return `429` with `Retry-After`.
- Protect login/forgot-password against enumeration + brute force.
- Separate limits for public vs authenticated tiers.
