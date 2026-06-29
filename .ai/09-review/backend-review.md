# Backend Review Rubric
Score each; blockers must be fixed before merge.
1. **Correctness** — behaviour + edge cases + error paths.
2. **Architecture** — layer boundaries, ports/adapters, no leakage.
3. **Domain** — invariants in the domain, glossary terms, BRs honoured.
4. **API** — DTO validation, no entity exposure, Swagger accurate.
5. **Data** — transactions correct, queries efficient, migrations safe.
6. **Security** — authn/authz, injection, secrets (`01-rules/security/*`).
7. **Tests** — meaningful, deterministic, coverage gate.
8. **Readability** — naming, structure, comments-the-why.
Output: blocking issues (file:line + rule), then suggestions.
