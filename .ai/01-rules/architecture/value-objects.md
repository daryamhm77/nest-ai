# Value Objects

- Immutable, equality by value, self-validating in the constructor.
- Replace primitive obsession: `Email`, `Money`, `TenantId` instead of `string`/`number`.
- No identity, no lifecycle. Construct invalid → throw.
- Put domain behaviour on them (`money.add(other)` with currency checks).

```ts
export class Money {
  private constructor(readonly amount: number, readonly currency: string) {}
  static of(a: number, c: string): Money { /* validate */ return new Money(a, c); }
  add(o: Money): Money { /* same-currency guard */ }
}
```
