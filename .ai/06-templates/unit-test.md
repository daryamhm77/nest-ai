# Template: Unit Test
```ts
describe('CreateExampleUseCase', () => {
  it('creates an example (BR-EX-1)', async () => {
    const repo = { save: jest.fn(), findById: jest.fn(), nextIdentity: jest.fn() };
    const uow = { run: (fn: any) => fn() };
    const useCase = new CreateExampleUseCase(repo as any, uow as any);

    const result = await useCase.execute({ name: 'Acme', actor: testActor });

    expect(result.nameValue).toBe('Acme');
    expect(repo.save).toHaveBeenCalledTimes(1);
  });

  it('rejects empty name', async () => {
    /* expect DomainError */
  });
});
```
