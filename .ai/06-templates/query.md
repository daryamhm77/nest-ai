# Template: Query (CQRS)
```ts
export class GetExampleQuery { constructor(readonly id: string) {} }

@QueryHandler(GetExampleQuery)
export class GetExampleHandler implements IQueryHandler<GetExampleQuery> {
  constructor(private readonly reads: ExampleReadModel) {}
  async execute(q: GetExampleQuery): Promise<ExampleViewDto | null> {
    return this.reads.findById(q.id); // hits optimized read model, bypasses domain
  }
}
```
