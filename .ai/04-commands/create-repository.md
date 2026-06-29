# Command: create-repository

**Intent:** Scaffold a repository port + adapter.

## Inputs
- aggregate root, persistence tech.

## Steps
1. Define `<Aggregate>Repository` port in `application/`.
2. Implement adapter in `infrastructure/persistence/` per `06-templates/repository.md`.
3. Add a mapper (`06-templates/mapper.md`).
4. Bind via DI token. Add integration test.

## Output
Port + adapter + mapper + DI binding + integration test.

> Obey all of `01-rules/**`. Use the matching `06-templates/*`. Cite what you applied.
