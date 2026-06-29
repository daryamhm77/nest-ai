# Template: e2e Test
```ts
describe('POST /v1/examples (e2e)', () => {
  let app: INestApplication;
  beforeAll(async () => { /* full app + test DB */ });
  afterAll(async () => app.close());

  it('creates an example', async () => {
    await request(app.getHttpServer())
      .post('/v1/examples')
      .set('Authorization', `Bearer ${token}`)
      .send({ name: 'Acme' })
      .expect(201)
      .expect(r => expect(r.body.name).toBe('Acme'));
  });

  it('401 without token', async () => {
    await request(app.getHttpServer()).post('/v1/examples').send({ name: 'x' }).expect(401);
  });
});
```
