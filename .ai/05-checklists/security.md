# Security Checklist
- [ ] AuthN robust (hashing, lockout, token rotation).
- [ ] AuthZ default-deny; permissions + RLS for multi-tenant.
- [ ] All inputs validated; parameterized queries only.
- [ ] Secrets in a manager; none in code/logs.
- [ ] Security headers (Helmet) + TLS enforced.
- [ ] Dependencies scanned; no critical CVEs.
- [ ] OWASP Top 10 reviewed (`01-rules/security/owasp.md`).
