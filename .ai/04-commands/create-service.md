# Command: create-service

**Intent:** Scaffold a use-case service.

## Inputs
- `<verbNoun>` use case, target context, dependencies (ports).

## Steps
1. Create `application/use-cases/<verb-noun>.use-case.ts` per `06-templates/service.md`.
2. Inject ports via tokens.
3. Define input/output types.
4. Add a unit test (`06-templates/unit-test.md`).

## Output
`<VerbNoun>UseCase` with `execute()`, ports injected, unit test.

> Obey all of `01-rules/**`. Use the matching `06-templates/*`. Cite what you applied.
