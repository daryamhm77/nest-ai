# Recipe: Health Checks
1. `/health/live` — process is up (no deps).
2. `/health/ready` — deps reachable (DB, Redis, broker) via `@nestjs/terminus`.
3. Readiness gates traffic in k8s; liveness restarts a hung pod.
4. Keep checks cheap + cached briefly to avoid hammering deps.
