# Performance Review Rubric
1. Database: N+1, missing indexes, full scans (check `EXPLAIN ANALYZE`).
2. Pagination + result-size limits on list endpoints.
3. Caching for hot idempotent reads; correct invalidation.
4. No blocking/sync I/O on the hot path; bounded concurrency.
5. Payload sizes + serialization cost.
6. Connection pooling sized correctly.
Demand measurements; predict impact of each change vs `PROJECT.md` budgets.
