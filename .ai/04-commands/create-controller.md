# Command: create-controller

**Intent:** Scaffold a thin REST controller.

## Inputs
- resource name, routes, related use cases.

## Steps
1. Generate controller per `06-templates/controller.md`.
2. Add DTOs + validation + Swagger.
3. Apply guards + roles.
4. Map outputs via a mapper. Add an e2e test.

## Output
Versioned controller, DTOs, guards, Swagger, e2e test.

> Obey all of `01-rules/**`. Use the matching `06-templates/*`. Cite what you applied.
