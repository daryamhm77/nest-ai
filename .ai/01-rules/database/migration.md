# Migrations

- Versioned, committed, forward-only in production; reversible in dev where feasible.
- One logical change per migration; descriptive name + timestamp.
- Expand → migrate → contract for zero-downtime schema changes.
- Never edit a shipped migration; create a new one.
- Test migrations in CI against a real Postgres, not SQLite.
- Data backfills run as separate idempotent jobs, not inside DDL migrations.
