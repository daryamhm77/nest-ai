# Security Review Rubric
Walk the OWASP Top 10 (`01-rules/security/owasp.md`):
- Access control: default deny, RBAC, RLS, ownership checks.
- Crypto: TLS, Argon2id, no homemade crypto, key management.
- Injection: parameterized queries, validated inputs.
- Secrets: managed, never logged.
- AuthN: lockout, token rotation, session safety.
- Dependencies: no critical CVEs.
- Logging/monitoring: audit trail for sensitive actions.
Each finding: severity, exploit sketch, remediation.
