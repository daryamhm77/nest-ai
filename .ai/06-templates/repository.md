# Template: Repository (port + adapter)
```ts
// application/ports/example.repository.ts
export interface ExampleRepository {
  nextIdentity(): ExampleId;
  findById(id: ExampleId): Promise<Example | null>;
  save(example: Example): Promise<void>;
}
export const EXAMPLE_REPOSITORY = Symbol('EXAMPLE_REPOSITORY');

// infrastructure/persistence/typeorm-example.repository.ts
@Injectable()
export class TypeOrmExampleRepository implements ExampleRepository {
  constructor(@InjectRepository(ExampleOrmEntity) private readonly orm: Repository<ExampleOrmEntity>) {}
  nextIdentity() { return ExampleId.generate(); }
  async findById(id: ExampleId) {
    const row = await this.orm.findOne({ where: { id: id.value } });
    return row ? ExampleMapper.toDomain(row) : null;
  }
  async save(e: Example) { await this.orm.save(ExampleMapper.toOrm(e)); }
}
```
