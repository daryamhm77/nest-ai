# Recipe: Multi-Device Sessions
1. Track sessions per device: `deviceId`, `userAgent`, `lastSeen`, refresh `familyId`.
2. Expose "active sessions" list + per-session revoke.
3. "Logout everywhere" revokes all families for the account.
4. On password change, revoke all sessions.
