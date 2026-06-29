# Lint & Format

- ESLint (typescript-eslint, strict) + Prettier. CI fails on warnings.
- `noImplicitAny`, `strictNullChecks`, `noUncheckedIndexedAccess` on.
- Enforced rules: no floating promises, no unused vars, consistent-type-imports,
  no console in app code (use the logger), explicit function return types on exports.
- Format on commit (lint-staged + husky or repo equivalent).
- One rule set at repo root; packages extend, never redefine from scratch.
