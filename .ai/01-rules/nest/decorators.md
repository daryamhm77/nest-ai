# Custom Decorators

- `@CurrentUser()` / `@Actor()` to extract the authenticated principal.
- `@Roles(...)`, `@Permissions(...)` to attach authz metadata.
- `@ApiStandardResponses()` to bundle common Swagger responses.
- Keep param decorators pure (read from request, no side effects).
- Compose with `applyDecorators()` to standardize endpoint annotations.
