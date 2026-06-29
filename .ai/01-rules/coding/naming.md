# Naming

- Files: `kebab-case.ts`. Suffix by role: `*.controller.ts`, `*.service.ts`,
  `*.repository.ts`, `*.dto.ts`, `*.entity.ts`, `*.mapper.ts`, `*.spec.ts`.
- Classes/types: `PascalCase`. Interfaces are NOT prefixed with `I`.
- Variables/functions: `camelCase`. Booleans read as predicates: `isActive`, `hasAccess`.
- Constants/enums values: `UPPER_SNAKE_CASE`.
- DI tokens: `UPPER_SNAKE_CASE` ending in `_PORT`/`_REPOSITORY` for ports.
- Use cases: `verbNoun` (`createOrder`, `getInvoice`). No `manager`/`helper`/`util` god-names.
- Domain terms must match `00-project/glossary.md` exactly.
