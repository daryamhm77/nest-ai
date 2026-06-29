# Providers & DI

- Bind ports to adapters with explicit tokens, not class references across layers.
- Prefer `useClass`/`useFactory` with tokens for swappability + testability.
- No service locator / no manual `app.get()` in business code.
- Provider scope is default (singleton). Use `REQUEST` scope only when truly needed
  (it has performance cost) and document why.

```ts
{ provide: INVOICE_REPOSITORY, useClass: TypeOrmInvoiceRepository }
```
