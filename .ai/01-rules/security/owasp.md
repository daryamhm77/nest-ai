# OWASP Baseline

Map every release against the OWASP Top 10:
1. Broken access control → RBAC + RLS + default deny.
2. Cryptographic failures → TLS everywhere, Argon2id, no homemade crypto.
3. Injection → parameterized queries, validation.
4. Insecure design → threat model new features.
5. Misconfiguration → Helmet, least privilege, no debug in prod.
6. Vulnerable components → `pnpm audit` / Dependabot in CI.
7. Auth failures → lockout, MFA, secure session handling.
8. Integrity failures → signed artifacts, verified dependencies.
9. Logging/monitoring gaps → audit log + alerts (see `01-rules/monitoring`).
10. SSRF → allowlist outbound URLs, no fetching user-supplied internal hosts.
