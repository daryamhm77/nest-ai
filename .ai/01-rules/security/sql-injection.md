# SQL Injection

- Always use parameterized queries / the ORM query builder. Never string-concatenate SQL.
- Validate + type-coerce all inputs (UUID, int, enum) before they reach the DB layer.
- Least-privilege DB user; no DDL rights from the app runtime.
- For dynamic filters, use an allowlist of sortable/filterable columns.
- Raw SQL requires review + bound parameters only.
