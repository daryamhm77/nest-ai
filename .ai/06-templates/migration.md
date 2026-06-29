# Template: Migration (TypeORM)
```ts
export class CreateExamples1700000000000 implements MigrationInterface {
  async up(q: QueryRunner): Promise<void> {
    await q.query(`
      CREATE TABLE examples (
        id uuid PRIMARY KEY,
        tenant_id uuid NOT NULL,
        name text NOT NULL,
        created_at timestamptz NOT NULL DEFAULT now()
      );
      CREATE INDEX idx_examples_tenant ON examples(tenant_id);
    `);
  }
  async down(q: QueryRunner): Promise<void> {
    await q.query(`DROP TABLE examples;`);
  }
}
```
