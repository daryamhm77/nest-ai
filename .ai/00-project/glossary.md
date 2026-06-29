# Glossary

> Ubiquitous language. Use these exact terms in code, APIs, and docs.
> If a term is missing, add it here before inventing a synonym.

| Term | Definition | Code name |
|------|------------|-----------|
| Tenant | An isolated customer organization | `tenant` |
| Account | A login identity within a tenant | `account` |
| Actor | The authenticated entity performing an action | `actor` |
| Use Case | A single application operation (command or query) | `<verb><noun>` |
| Aggregate | A consistency boundary around entities | `*Aggregate` |
| Port | An interface owned by the application layer | `*Port` / `*Repository` |
| Adapter | An infrastructure implementation of a port | `*Adapter` / `*RepositoryImpl` |

Naming rule: domain terms are singular nouns. Operations are `verbNoun` (e.g. `issueInvoice`).
