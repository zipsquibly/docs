# SchemasCortexV1ToolsTool

A tool definition to be used by the OpenAI API.


## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `function`                                                       | [models.Function](../models/function.md)                         | :heavy_check_mark:                                               | The tool definition including the JSON Schema of its parameters. |
| `type`                                                           | *OptionalNullable[str]*                                          | :heavy_minus_sign:                                               | Always `function`.                                               |