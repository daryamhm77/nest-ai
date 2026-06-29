# Mappers

- Pure, static, no side effects. Convert: ORM ↔ domain, domain ↔ response DTO.
- One mapper per aggregate. Co-locate with the layer that needs the target type.
- Never put validation in a mapper — that belongs to DTOs/domain.
- Keep them total: every field handled explicitly (no silent drops).

```ts
export const InvoiceMapper = {
  toDomain(row: InvoiceOrmEntity): Invoice { /* ... */ },
  toOrm(inv: Invoice): InvoiceOrmEntity { /* ... */ },
  toResponse(inv: Invoice): InvoiceResponseDto { /* ... */ },
};
```
