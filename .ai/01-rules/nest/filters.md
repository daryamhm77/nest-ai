# Exception Filters

- A global filter maps domain/application exceptions → HTTP problem responses.
- Use a stable error contract: `{ code, message, traceId, details? }`.
- Never leak stack traces or SQL in production responses.
- Map known exceptions explicitly; unknown → 500 with a logged `traceId`.

```ts
@Catch()
export class AllExceptionsFilter implements ExceptionFilter { /* map + log + respond */ }
```
