# Recipe: JWT Auth
1. `AuthModule` with `JwtModule` (RS256, keys from secret manager).
2. `login` use case: verify credentials (Argon2id), issue access (15m) + refresh (rotating).
3. `JwtAuthGuard` validates signature, `iss/aud/exp`; attaches `Actor`.
4. `RolesGuard` reads `@Roles()` metadata and checks permissions server-side.
5. Audit-log every login/refresh/logout.
Rules: `01-rules/security/{auth,jwt,rbac}.md`.
