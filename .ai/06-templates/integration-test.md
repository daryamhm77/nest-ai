# Template: Integration Test
```ts
describe('TypeOrmExampleRepository (integration)', () => {
  let repo: ExampleRepository;
  beforeAll(async () => { /* boot Nest TestingModule with REAL Postgres (testcontainers) */ });
  afterAll(async () => { /* teardown */ });

  it('saves and reloads an example', async () => {
    const e = Example.create('Acme');
    await repo.save(e);
    const loaded = await repo.findById(e.id);
    expect(loaded?.nameValue).toBe('Acme');
  });
});
```
