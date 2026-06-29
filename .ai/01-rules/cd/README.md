# CD Rules
- Deploy only green, tagged builds. Promote the same artifact across envs.
- Migrations run as a gated step before app rollout (expand/contract).
- Progressive delivery: canary/blue-green with automated rollback on SLO breach.
- Every deploy is traceable to a git sha + changelog (`10-output/changelog.md`).
- Secrets injected at deploy from the secret manager.
