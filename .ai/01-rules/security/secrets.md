# Secrets

- No secrets in code, env files committed, or logs. `.env` is gitignored.
- Load via a secret manager (Vault / cloud SM / Doppler) at boot.
- Rotate regularly; support zero-downtime rotation (`kid` for keys).
- Scope credentials least-privilege per service.
- CI uses masked secrets; scan the repo for leaked secrets (gitleaks) in CI.
