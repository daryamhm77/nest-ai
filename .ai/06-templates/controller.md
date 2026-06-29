# Template: Controller
```ts
@ApiTags('examples')
@Controller({ path: 'examples', version: '1' })
@UseGuards(JwtAuthGuard, RolesGuard)
export class ExampleController {
  constructor(private readonly createExample: CreateExampleUseCase) {}

  @Post()
  @Roles('example:create')
  @HttpCode(201)
  @ApiOperation({ summary: 'Create an example' })
  async create(@Body() dto: CreateExampleDto, @Actor() actor: Actor): Promise<ExampleResponseDto> {
    const example = await this.createExample.execute({ ...dto, actor });
    return ExampleMapper.toResponse(example);
  }
}
```
