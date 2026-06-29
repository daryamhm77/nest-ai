# Folder Structure

Per bounded context (NestJS module):

```
<context>/
  <context>.module.ts
  domain/        entities, value-objects, events, *.aggregate.ts (no framework)
  application/   use-cases, ports (interfaces), dtos
  infrastructure/
    http/        controllers
    persistence/ repositories, orm entities, mappers
    messaging/   consumers, publishers
  __tests__/     or co-located *.spec.ts
```

Rules:
- Domain imports nothing from application/infrastructure.
- Application imports domain + ports only.
- Infrastructure may import everything.
- No barrel `index.ts` re-exports across layer boundaries (keeps deps explicit).
