# CQRS

- Separate write (commands) from read (queries) when read/write models diverge
  or read load demands dedicated projections. Otherwise a single model is fine.
- Commands mutate via aggregates and return ids/void, not full read models.
- Queries bypass the domain and hit optimized read models / SQL views.
- Use Nest `@nestjs/cqrs` only if it adds value; plain use-case services are acceptable.
- Never share DTOs between command and query sides.
