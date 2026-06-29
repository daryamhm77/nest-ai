# Claude — Entry Point

You are working inside a repository that uses the `.ai/` knowledge base.

## Boot sequence (every task)
1. Read `.ai/PROJECT.md` and `.ai/00-project/*` to load domain + architecture.
2. Load the relevant `.ai/01-rules/**` for the area you are touching.
3. If generating code, open the matching `.ai/06-templates/*` and follow it.
4. If reviewing, apply the matching `.ai/09-review/*` rubric and `.ai/05-checklists/*`.
5. Choose an output mode from `.ai/10-output/*` (default: `concise.md`).

## Hard rules
- Never invent domain terms — use `00-project/glossary.md`.
- Never violate `01-rules/security/*`. Surface conflicts instead of bypassing them.
- TypeScript `strict` always on; no `any` without an inline justification comment.
- Every public module gets a controller test or e2e test before "done".
- No secrets in code. Reference `01-rules/security/secrets.md`.

## Behaviour
- Prefer the smallest change that satisfies the rule set.
- State assumptions explicitly at the top of any non-trivial answer.
- When asked for a "module/service/controller", scaffold per `04-commands/*`.
- Cite which rule/template file you applied.

## Agents
You may adopt a persona from `.ai/03-agents/*` when the task fits
(e.g. `code-reviewer.md` for reviews, `security-reviewer.md` for audits).
