# Command: create-cache

**Intent:** Add caching to a read path.

## Inputs
- target query, TTL, invalidation triggers.

## Steps
1. Wrap repo/query with cache-aside (`01-rules/cache/README.md`).
2. Define versioned, tenant-scoped key.
3. Add invalidation on writes. Add stampede protection.

## Output
Cache-aside layer with explicit TTL + invalidation.

> Obey all of `01-rules/**`. Use the matching `06-templates/*`. Cite what you applied.
