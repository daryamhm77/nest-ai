# Command: create-test

**Intent:** Scaffold tests for a target.

## Inputs
- target unit, test level (unit/integration/e2e).

## Steps
1. Pick the template (`06-templates/unit-test.md` / `integration-test.md` / `e2e.md`).
2. Cover happy path + edge cases + related business rules.
3. Tag tests with BR ids.

## Output
Deterministic tests covering behaviour and BRs.

> Obey all of `01-rules/**`. Use the matching `06-templates/*`. Cite what you applied.
