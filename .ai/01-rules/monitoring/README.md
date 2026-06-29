# Monitoring Rules
- Expose Prometheus metrics: RED (rate, errors, duration) per endpoint + queue depth.
- Distributed tracing (OpenTelemetry) across HTTP, DB, broker boundaries.
- Health endpoints: `/health/live`, `/health/ready` (see `08-recipes/health-check.md`).
- Alert on SLO burn, error spikes, queue backlog, cron failures.
- Dashboards per service; runbooks linked from alerts.
