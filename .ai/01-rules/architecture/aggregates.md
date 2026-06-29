# Aggregates

- An aggregate is a consistency boundary with a single root entity.
- All external access goes through the root; internals are not referenced outside.
- Keep aggregates small — favour referencing other aggregates by id.
- Enforce invariants inside the aggregate, not in services.
- One transaction modifies one aggregate (eventual consistency across aggregates).
