# Authentication

- Stateless JWT access tokens (short TTL) + rotating refresh tokens (longer TTL).
- Hash passwords with Argon2id (or bcrypt cost ≥ 12). Never store plaintext.
- Constant-time comparisons for secrets/tokens.
- Lockout / backoff after repeated failures (BR-AUTH-2).
- MFA hooks where the product requires it.
- All auth events go to the audit log.
