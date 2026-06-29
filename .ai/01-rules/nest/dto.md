# DTOs

- Input DTOs use `class-validator` + `class-transformer` decorators.
- Separate Request and Response DTOs. Never expose entities directly.
- `ValidationPipe({ whitelist: true, forbidNonWhitelisted: true, transform: true })` globally.
- No domain logic in DTOs — they are data shapes only.
- Document each field with `@ApiProperty`.

```ts
export class CreateInvoiceDto {
  @ApiProperty() @IsUUID() customerId!: string;
  @ApiProperty({ type: [LineItemDto] }) @ValidateNested({ each: true })
  @Type(() => LineItemDto) items!: LineItemDto[];
}
```
