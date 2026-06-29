# Comments

- Code should be self-explanatory; comment the *why*, not the *what*.
- Reference business rules: `// enforces BR-BILL-1`.
- Every `any`, every `@ts-expect-error`, and every disabled lint rule needs a one-line reason.
- Public application services and ports get a short JSDoc summarizing intent + invariants.
- TODOs are tracked: `// TODO(<owner>, <ticket>): ...`. No anonymous TODOs.
