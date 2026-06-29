# Command: create-module

**Intent:** Scaffold a new bounded-context module.

## Inputs
- `<context>` name (glossary-aligned).

## Steps
1. Create folder per `01-rules/coding/folder.md`.
2. Generate `<Context>Module` per `06-templates/module.md`.
3. Wire empty domain/application/infrastructure layers.
4. Register in the root app module.

## Output
A compiling module with layer folders and a placeholder test.

> Obey all of `01-rules/**`. Use the matching `06-templates/*`. Cite what you applied.
