# Template: Command (CQRS)
```ts
export class CreateExampleCommand {
  constructor(readonly name: string, readonly actor: Actor) {}
}

@CommandHandler(CreateExampleCommand)
export class CreateExampleHandler implements ICommandHandler<CreateExampleCommand> {
  constructor(@Inject(EXAMPLE_REPOSITORY) private readonly repo: ExampleRepository) {}
  async execute(cmd: CreateExampleCommand): Promise<{ id: string }> {
    const e = Example.create(cmd.name);
    await this.repo.save(e);
    return { id: e.id.value };
  }
}
```
