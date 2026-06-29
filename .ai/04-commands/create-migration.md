# Command: create-migration

**Intent:** Author a schema migration.

## Inputs
- schema change description.

## Steps
1. Generate a timestamped migration per `06-templates/migration.md`.
2. Use expand/contract for zero downtime.
3. Add constraints + indexes.
4. Verify in CI against Postgres.

## Output
Forward-only, reversible-in-dev migration; tested.

> Obey all of `01-rules/**`. Use the matching `06-templates/*`. Cite what you applied.
