# Command: release

**Intent:** Prepare a release.

## Inputs
- version bump scope.

## Steps
1. Run `05-checklists/release.md` + `production.md`.
2. Generate changelog (`10-output/changelog.md`).
3. Confirm migrations + rollback plan.
4. Tag + deploy via CD.

## Output
Tagged, documented, deployable release.

> Obey all of `01-rules/**`. Use the matching `06-templates/*`. Cite what you applied.
