# Kubernetes Rules
- Set resource requests/limits; liveness + readiness probes wired to `/health/*`.
- Secrets via k8s Secrets / external secret operator, never in manifests.
- HPA on CPU + custom metrics; PodDisruptionBudgets for availability.
- Rolling updates with surge limits; graceful shutdown (SIGTERM handling).
- Network policies default-deny; least-privilege service accounts.
