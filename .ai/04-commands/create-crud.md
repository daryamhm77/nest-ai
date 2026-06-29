# Command: create-crud

**Intent:** Scaffold a full CRUD context the clean way.

## Inputs
- entity name, fields, access rules.

## Steps
1. Run create-module, create-entity, create-repository.
2. Generate use cases: create/get/list/update/delete.
3. Generate controller + DTOs + mappers + Swagger.
4. Add tests at each layer.

## Output
End-to-end CRUD context obeying all rules, with tests.

> Obey all of `01-rules/**`. Use the matching `06-templates/*`. Cite what you applied.
