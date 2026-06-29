# Template: DTOs
```ts
export class CreateExampleDto {
  @ApiProperty() @IsString() @IsNotEmpty() @MaxLength(120) name!: string;
}

export class ExampleResponseDto {
  @ApiProperty() id!: string;
  @ApiProperty() name!: string;
  @ApiProperty() createdAt!: string;
}
```
