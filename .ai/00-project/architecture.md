# Architecture

## Style
Clean Architecture with a light DDD flavour. Dependencies point inward:
`infrastructure -> application -> domain`. The domain layer has zero framework imports.

## Layers
- **Domain** — entities, value objects, aggregates, domain events, pure rules. No NestJS, no DB.
- **Application** — use cases (commands/queries), ports (interfaces), orchestration. No HTTP, no SQL.
- **Infrastructure** — controllers, repositories, ORM, message brokers, external APIs.

## NestJS mapping
| Concept | NestJS artifact |
|---------|-----------------|
| Use case (write) | Command handler / service method |
| Use case (read)  | Query handler / read service |
| Port             | `interface` + DI token |
| Adapter          | `@Injectable()` provider implementing the port |
| Entry point      | Controller / gateway / message consumer |

## Module boundaries
One NestJS module per bounded context. Modules expose only their public providers.
Cross-module calls go through application services, never repositories.

## Data flow (write)
`Controller -> DTO validation -> Command -> Handler -> Domain -> Repository (port) -> DB`

## Diagrams
Kept in the repo wiki / external tool. This file is the textual source of truth.
