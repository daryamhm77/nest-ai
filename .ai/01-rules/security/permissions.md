# Permissions / Policies

- Model permissions as `action:resource` (e.g. `invoice:issue`, `tenant:read`).
- For row-level access (multi-tenant), enforce `tenant_id` in queries AND Postgres RLS.
- Policy checks combine: authenticated + role/permission + resource ownership.
- Centralize policy logic; do not scatter `if (user.role === ...)` across controllers.
