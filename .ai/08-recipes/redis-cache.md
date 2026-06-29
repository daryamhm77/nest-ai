# Recipe: Redis Cache-Aside
1. On read: check cache → on miss, load from repo, set with TTL.
2. Key: `v1:<tenant>:<entity>:<id>`. On write: invalidate the key(s).
3. Stampede protection: short lock or randomized TTL jitter.
4. System must degrade gracefully if Redis is unavailable.
