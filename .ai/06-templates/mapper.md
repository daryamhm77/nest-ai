# Template: Mapper
```ts
export const ExampleMapper = {
  toDomain(row: ExampleOrmEntity): Example { return Example.rehydrate(row); },
  toOrm(e: Example): ExampleOrmEntity {
    const o = new ExampleOrmEntity();
    o.id = e.id.value; o.name = e.nameValue; return o;
  },
  toResponse(e: Example): ExampleResponseDto {
    return { id: e.id.value, name: e.nameValue, createdAt: e.createdAt.toISOString() };
  },
};
```
