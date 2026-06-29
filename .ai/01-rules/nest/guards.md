# Guards

- `AuthGuard` (JWT) authenticates; `RolesGuard`/`PolicyGuard` authorizes.
- Guards read metadata set by `@Roles()` / `@Permissions()` decorators.
- Authentication ≠ authorization — keep them in separate guards.
- No DB writes in guards. Read-only checks only; heavy checks belong in the use case.
- Fail closed: missing/invalid context → deny.
