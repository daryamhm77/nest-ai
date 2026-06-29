# Sessions

- Prefer stateless JWT; if server sessions are needed, store in Redis with TTL.
- Cookies: `HttpOnly`, `Secure`, `SameSite=Lax/Strict`, scoped path.
- Rotate session id on privilege change / login.
- Invalidate all sessions on password change or suspected compromise.
- Track device/session list for multi-device logout (see `08-recipes/multi-device.md`).
