# SchemasBubblegumV2ToolsTool

SchemasBubblegumV2ToolsTool


## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `name`                                                                 | *str*                                                                  | :heavy_check_mark:                                                     | The name of the tool                                                   |
| `service_id`                                                           | *int*                                                                  | :heavy_check_mark:                                                     | The service this tool belongs to                                       |
| `id`                                                                   | *int*                                                                  | :heavy_check_mark:                                                     | The ID of the tool                                                     |
| `definition`                                                           | [OptionalNullable[models.ToolDefinition]](../models/tooldefinition.md) | :heavy_minus_sign:                                                     | The definition of the tool                                             |
| `service_name`                                                         | *OptionalNullable[str]*                                                | :heavy_minus_sign:                                                     | N/A                                                                    |