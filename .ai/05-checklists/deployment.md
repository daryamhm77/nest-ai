# Deployment Checklist
- [ ] Same artifact promoted from a green build.
- [ ] Migrations applied (expand/contract) before app rollout.
- [ ] Config + secrets present for target env.
- [ ] Health probes pass; readiness gates traffic.
- [ ] Rollback plan defined and tested.
- [ ] Dashboards + alerts active for the new version.
