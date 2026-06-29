# Entities

Two distinct meanings — keep them separate:

- **Domain entity** (`domain/`): pure class with identity + behaviour, enforces invariants.
  No decorators, no framework, no getters/setters bag of data.
- **ORM entity** (`infrastructure/persistence/`): persistence model with ORM decorators.

A mapper converts between them. Domain entities never carry `@Column`.

```ts
// domain
export class Invoice {
  private constructor(readonly id: InvoiceId, private status: InvoiceStatus) {}
  static issue(input: IssueInput): Invoice { /* invariants here */ }
  markPaid(): void { /* state transition with guards */ }
}
```
