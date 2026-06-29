# Anti-Patterns (reject)
- Business logic in controllers, guards, interceptors, or repositories.
- Entities exposed directly over HTTP.
- Cross-module deep imports into `infrastructure/`.
- Service locator / manual `app.get()` in business code.
- Transactions opened in controllers or repositories.
- Publishing integration events before commit (no outbox).
- Trusting client-supplied roles/permissions.
- `any` without justification; swallowing errors silently.
