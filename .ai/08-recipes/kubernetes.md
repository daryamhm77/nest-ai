# Recipe: Kubernetes Deploy
1. Deployment with requests/limits + liveness/readiness probes → `/health/*`.
2. Secrets via external secret operator; config via ConfigMap.
3. HPA on CPU + custom metrics; PDB for availability.
4. Graceful shutdown on SIGTERM; rolling update with surge limits.
Rules: `01-rules/kubernetes/README.md`.
