# CI Rules
- Pipeline: install → typecheck → lint → unit → integration → build → security scan.
- Fail on lint warnings, type errors, coverage below gate, audit criticals.
- Run against real Postgres/Redis (services), not mocks, for integration tests.
- Cache deps; keep pipeline under target minutes. Required checks block merge.
