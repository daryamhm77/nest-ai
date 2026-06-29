# Repositories (architecture view)

- A repository is a collection-like port for an aggregate root, defined in the domain/application.
- It hides persistence entirely; callers never see SQL or ORM types.
- Provide `nextIdentity()` so ids are domain-owned, not DB-owned, where practical.
- Read models for queries are separate from aggregate repositories (see CQRS).
- Transactions are coordinated by the use case via a Unit of Work, not by the repo.
