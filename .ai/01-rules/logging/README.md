# Logging Rules
- Structured JSON logs (pino). One logger, injected, no `console.*` in app code.
- Always include `traceId`, `tenantId`, `actorId` where available.
- Levels: error (actionable), warn (degraded), info (lifecycle), debug (dev only).
- Never log secrets, tokens, passwords, full PII. Redact at the logger.
- Correlate logs ↔ traces via the same id.
