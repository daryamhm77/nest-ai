# Pipes

- Global `ValidationPipe` for all DTOs (whitelist, transform).
- `ParseUUIDPipe`, `ParseIntPipe` for path/query params — never trust strings.
- Custom pipes only for cross-cutting transforms (e.g. trimming, normalization).
- Pipes do not perform DB lookups or business checks — that is the use case's job.
