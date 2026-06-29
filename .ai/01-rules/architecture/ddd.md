# DDD (light)

Apply tactically where complexity justifies it:
- **Bounded context** = one NestJS module with its own model + language.
- **Ubiquitous language** comes from `00-project/glossary.md`.
- **Aggregates** guard invariants; reference other aggregates by id only.
- **Domain events** record what happened, in past tense.
- **Anti-corruption layer** at integration boundaries (mappers/adapters).

Do NOT over-engineer CRUD contexts — keep them simple.
