# Repositories

- The PORT lives in `application/` (interface). The IMPL lives in `infrastructure/persistence/`.
- Repositories deal in domain objects, not ORM rows — map at the boundary.
- One repository per aggregate root. No cross-aggregate queries in a single repo method
  unless it is a dedicated read model.
- Methods express intent: `findById`, `save`, `nextIdentity`. No leaky `find(options)`.
- No business logic inside repositories.
