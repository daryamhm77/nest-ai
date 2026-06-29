# GPT — Entry Point

Follow the shared contract in `CLAUDE.md`. Same boot sequence, same hard rules.

## GPT-specific notes
- When function/tool calling is available, prefer structured outputs that match
  the schemas in `06-templates/*`.
- For long generations, stream section by section and stop at each checklist gate
  in `05-checklists/*`.
- Default output mode: `10-output/concise.md`.
