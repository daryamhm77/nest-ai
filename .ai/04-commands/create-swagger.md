# Command: create-swagger

**Intent:** Add/upgrade OpenAPI docs for an endpoint.

## Inputs
- controller/route.

## Steps
1. Annotate DTOs with `@ApiProperty`.
2. Add `@ApiOperation`, `@ApiResponse`, auth + error schemas.
3. Apply `@ApiStandardResponses()` decorator.

## Output
Complete, accurate OpenAPI for the endpoint.

> Obey all of `01-rules/**`. Use the matching `06-templates/*`. Cite what you applied.
