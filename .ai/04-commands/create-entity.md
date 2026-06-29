# Command: create-entity

**Intent:** Scaffold domain + ORM entity pair.

## Inputs
- aggregate/entity name, fields, invariants.

## Steps
1. Create domain entity per `06-templates/entity.md` (behaviour + invariants).
2. Create ORM entity in infrastructure.
3. Create mapper between them.
4. Add value objects for primitives where useful.

## Output
Pure domain entity, ORM entity, mapper, value objects.

> Obey all of `01-rules/**`. Use the matching `06-templates/*`. Cite what you applied.
