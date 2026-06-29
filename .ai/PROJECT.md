# Project Profile

> Fill this in per repository. The assistant reads this to ground every answer.

## Identity
- **Name:** <project-name>
- **Owner / Team:** <team>
- **Repository:** <git-url>
- **Runtime:** Node.js LTS, TypeScript strict mode
- **Package manager:** pnpm (workspaces)

## Type
- [ ] Single service
- [ ] Monorepo (apps/* + packages/*)
- [ ] Modular monolith
- [ ] Microservices

## Primary stack
- Framework: NestJS
- DB: PostgreSQL (+ Row-Level Security if multi-tenant)
- ORM/Query: <Prisma | TypeORM | Drizzle | Kysely>
- Cache/Queue: Redis + BullMQ
- Transport: REST + <gRPC | WebSocket | RabbitMQ | Kafka>
- Auth: JWT access + refresh, RBAC

## Non-functional targets
- p95 latency: <ms>
- Availability: <SLA>
- Test coverage gate: <%>

## Constraints
- Compliance: <GDPR / Art.9 health data / PCI / none>
- Data residency: <region>
- Hard deadlines: <dates>

## Glossary pointer
Domain terms live in `00-project/glossary.md`. Use those exact words.
