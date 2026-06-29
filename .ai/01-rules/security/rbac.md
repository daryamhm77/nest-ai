# RBAC

- Roles group permissions; permissions gate actions. Check permissions, not roles, in code.
- Roles are per-tenant. The same account may have different roles per tenant.
- Enforce in `RolesGuard`/`PolicyGuard`; never trust client-sent role claims blindly
  (derive from verified token + server-side lookup if sensitive).
- Default deny. New endpoints are inaccessible until a permission is assigned.
- Audit every permission change.
