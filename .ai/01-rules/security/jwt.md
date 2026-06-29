# JWT

- Algorithm: RS256/ES256 (asymmetric) in production; never `none`.
- Claims: `sub`, `tenant`, `roles`, `iat`, `exp`, `jti`. Keep payload minimal.
- Access TTL ~15m; refresh TTL days, single-use + rotated (BR-AUTH-1).
- Validate `iss`, `aud`, `exp`, signature on every request.
- Store signing keys in a secret manager; support key rotation via `kid`.
- Never put PII or secrets in the token.
