# Clean Architecture

- Dependency rule: source code dependencies point only inward.
  `infrastructure → application → domain`.
- Inner layers define interfaces (ports); outer layers implement them (adapters).
- Frameworks (NestJS, ORM, brokers) are details, isolated in infrastructure.
- The domain is testable with zero mocks of frameworks.
- A use case is the unit of application behaviour; one class, one `execute`.
