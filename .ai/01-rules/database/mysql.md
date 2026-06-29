# MySQL (only if mandated)

- Use InnoDB, `utf8mb4`, strict mode (`STRICT_ALL_TABLES`).
- `DECIMAL` for money; `DATETIME`/`TIMESTAMP` with explicit timezone handling in app.
- Foreign keys + indexes enforced; avoid relying on app-side integrity.
- Beware implicit type coercion — validate types before queries.
- Prefer PostgreSQL for new services (see `postgres.md`); document why MySQL was chosen.
