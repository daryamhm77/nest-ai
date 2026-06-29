# Template: Module
```ts
@Module({
  imports: [/* other context modules, infra modules */],
  controllers: [ExampleController],
  providers: [
    CreateExampleUseCase,
    { provide: EXAMPLE_REPOSITORY, useClass: TypeOrmExampleRepository },
  ],
  exports: [CreateExampleUseCase],
})
export class ExampleModule {}
```
