# Agent


## Fields

| Field                                                        | Type                                                         | Required                                                     | Description                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `name`                                                       | *str*                                                        | :heavy_check_mark:                                           | N/A                                                          |
| `timezone`                                                   | *str*                                                        | :heavy_check_mark:                                           | N/A                                                          |
| `type_extra`                                                 | [models.TypeExtra](../models/typeextra.md)                   | :heavy_check_mark:                                           | N/A                                                          |
| `id`                                                         | *int*                                                        | :heavy_check_mark:                                           | The Agent ID                                                 |
| `variables`                                                  | [OptionalNullable[models.Variables]](../models/variables.md) | :heavy_minus_sign:                                           | N/A                                                          |