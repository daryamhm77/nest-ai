# Command: security-review

**Intent:** Run a security audit.

## Inputs
- target component / diff.

## Steps
1. Apply `09-review/security-review.md` + `01-rules/security/*`.
2. Categorize by OWASP, assign severity.
3. Give remediation per finding.

## Output
Severity-ranked findings with fixes.

> Obey all of `01-rules/**`. Use the matching `06-templates/*`. Cite what you applied.
