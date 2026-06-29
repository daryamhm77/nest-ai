# Template: Event
```ts
export class ExampleCreated {
  readonly eventVersion = 1;
  readonly occurredAt = new Date();
  constructor(readonly exampleId: string, readonly tenantId: string) {}
}
```
Past tense, immutable, versioned. Publish via outbox after commit.
