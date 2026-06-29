# .ai — AI Knowledge Base for NestJS Projects

This directory is the single source of truth that AI coding assistants
(Claude, GPT, Gemini, Cursor, Copilot) must read **before** writing or
reviewing any code in this repository.

## How it works
Every assistant entrypoint file in the root (`CLAUDE.md`, `GPT.md`, ...)
points to this same knowledge base. The rules, templates, agents, and
recipes here define **how** code must be written, not just **what**.

## Layout
| Folder | Purpose |
|--------|---------|
| `00-project/` | Vision, architecture, business rules, glossary, roadmap |
| `01-rules/`   | Hard constraints: coding, NestJS, architecture, security, infra |
| `02-prompts/` | Reusable prompt fragments by intent |
| `03-agents/`  | Role personas the assistant can adopt |
| `04-commands/`| Deterministic "do X" command specs |
| `05-checklists/` | Gate checklists for features, PRs, releases |
| `06-templates/`  | Canonical file skeletons |
| `07-examples/`   | Reference implementations |
| `08-recipes/`    | Step-by-step how-tos |
| `09-review/`     | Review rubrics |
| `10-output/`     | Output formatting modes |

## Rules of engagement
1. **Read `00-project/` first.** Never assume the domain.
2. **Obey `01-rules/`.** They are non-negotiable constraints.
3. When generating code, follow the matching `06-templates/` file.
4. When reviewing, use the matching `09-review/` rubric.
5. If a rule conflicts with a request, surface the conflict — do not silently break the rule.

## Stack assumptions
NestJS · TypeScript (strict) · PostgreSQL · Clean Architecture + light DDD ·
CQRS where justified · Jest · Docker · pnpm monorepo (Turborepo).
