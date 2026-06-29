# Code Review Checklist
- [ ] Correctness: does it do what it claims, including edge cases?
- [ ] Rules: complies with `01-rules/**`; conflicts surfaced not hidden.
- [ ] Boundaries: no layer leakage, no cross-module deep imports.
- [ ] Naming + readability per `01-rules/coding/*`.
- [ ] Tests present, meaningful, green.
- [ ] Security + performance considered.
- [ ] No dead code, no TODOs without owner/ticket.
