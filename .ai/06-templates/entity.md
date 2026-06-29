# Template: Entity (domain + ORM)
```ts
// domain/example.ts
export class Example {
  private constructor(readonly id: ExampleId, private name: string) {}
  static create(name: string): Example {
    if (!name?.trim()) throw new DomainError('name required');
    return new Example(ExampleId.generate(), name.trim());
  }
  rename(name: string): void { /* guarded transition */ }
}

// infrastructure/persistence/example.orm-entity.ts
@Entity('examples')
export class ExampleOrmEntity {
  @PrimaryColumn('uuid') id!: string;
  @Index() @Column('uuid') tenantId!: string;
  @Column('text') name!: string;
  @CreateDateColumn({ type: 'timestamptz' }) createdAt!: Date;
}
```
