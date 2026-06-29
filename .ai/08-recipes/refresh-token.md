# Recipe: Refresh Token Rotation
1. Store refresh tokens hashed with `jti`, `familyId`, `expiresAt`.
2. On refresh: validate, then rotate — issue new pair, mark old `jti` used (BR-AUTH-1).
3. Reuse of a used token → revoke the whole family (theft detection).
4. Logout revokes the family. Keep TTLs short; cleanup expired rows via cron.
