# Controllers

- Thin. Map HTTP ↔ use case. No business logic, no DB calls.
- Validate input with DTOs + `ValidationPipe` (whitelist + forbidNonWhitelisted).
- One controller per resource; RESTful routes; version with `@Controller({ version })`.
- Return DTOs via mappers, never raw entities.
- Set explicit `@HttpCode` and document with Swagger decorators.
- Auth via guards (`@UseGuards`), authorization via `@Roles`/policy decorators.

```ts
@Controller({ path: 'invoices', version: '1' })
export class InvoiceController {
  constructor(private readonly issueInvoice: IssueInvoiceUseCase) {}

  @Post()
  @HttpCode(201)
  async create(@Body() dto: CreateInvoiceDto): Promise<InvoiceResponseDto> {
    const invoice = await this.issueInvoice.execute(dto);
    return InvoiceMapper.toResponse(invoice);
  }
}
```
