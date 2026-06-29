# Imports

- Order: node builtins → external packages → `@app/*` aliases → relative.
- Use path aliases (`tsconfig` `paths`) for cross-package imports; relative only within a folder.
- No deep imports into another module's `infrastructure/`. Go through its public providers.
- No circular imports. If detected, extract a shared port or value object.
- `import type { ... }` for type-only imports (faster builds, no runtime edge).
