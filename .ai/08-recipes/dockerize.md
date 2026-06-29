# Recipe: Dockerize
1. Multi-stage: builder (install + build) → runtime (prod deps only).
2. Non-root user, distroless/alpine base, pinned digest.
3. `HEALTHCHECK` hitting `/health/ready`. Config via env.
4. `.dockerignore` excludes node_modules/.git/tests. Tag with git sha + semver.
Rules: `01-rules/docker/README.md`.
