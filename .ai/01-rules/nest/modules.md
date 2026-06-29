# Modules

- One module per bounded context. Name: `<Context>Module`.
- A module declares: controllers, providers, imports, exports — nothing global by default.
- Export only the providers other modules legitimately need (usually application services).
- Use `@Global()` only for true cross-cutting infra (config, logger). Justify in a comment.
- Dynamic modules (`forRoot`/`forRootAsync`) for configurable infra (DB, cache, queue).
- No business logic in the module file.
