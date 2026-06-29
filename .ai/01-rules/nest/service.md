# Services / Use Cases

- A use-case service does ONE thing: `execute(input): output`.
- Depends on ports (interfaces), never concrete infrastructure.
- Transaction boundaries live here, not in controllers or repositories.
- No HTTP types, no ORM types leaking in. Inputs/outputs are DTOs or domain objects.
- Throw domain/application exceptions; let filters map them to HTTP.

```ts
@Injectable()
export class IssueInvoiceUseCase {
  constructor(
    @Inject(INVOICE_REPOSITORY) private readonly repo: InvoiceRepository,
    private readonly uow: UnitOfWork,
  ) {}

  async execute(input: CreateInvoiceDto): Promise<Invoice> {
    return this.uow.run(async () => {
      const invoice = Invoice.issue(input); // domain enforces BR-BILL-1
      await this.repo.save(invoice);
      return invoice;
    });
  }
}
```
