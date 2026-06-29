# Template: Use Case
```ts
export interface CreateExampleInput { name: string; actor: Actor; }

@Injectable()
export class CreateExampleUseCase {
  constructor(
    @Inject(EXAMPLE_REPOSITORY) private readonly repo: ExampleRepository,
    private readonly uow: UnitOfWork,
  ) {}

  async execute(input: CreateExampleInput): Promise<Example> {
    return this.uow.run(async () => {
      const example = Example.create(input.name); // invariants in domain
      await this.repo.save(example);
      return example;
    });
  }
}
```
