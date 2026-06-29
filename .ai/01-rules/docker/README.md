# Docker Rules
- Multi-stage builds; final image is slim (distroless/alpine) and non-root.
- Pin base image digests; rebuild for CVEs. No secrets baked into layers.
- One process per container; `HEALTHCHECK` defined.
- `.dockerignore` excludes node_modules, .git, tests.
- Config via env; 12-factor. Tag images with git sha + semver.
