# PostgreSQL

- Default DB. Use `uuid` (v7 or `gen_random_uuid()`) primary keys.
- Multi-tenant: every tenant-scoped table has `tenant_id` + Row-Level Security policies.
- Use `NUMERIC` for money, `timestamptz` for time, `text` over `varchar(n)` unless bounded.
- Constraints in the DB: NOT NULL, FK, UNIQUE, CHECK — do not rely on app code alone.
- Connection pooling (PgBouncer) for high concurrency.
- Migrations are the only way schema changes; no manual prod edits.
