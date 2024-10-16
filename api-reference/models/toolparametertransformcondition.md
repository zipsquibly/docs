# ToolParameterTransformCondition

A condition to be met for a transform to be applied to the value of a parameter.


## Fields

| Field                                     | Type                                      | Required                                  | Description                               |
| ----------------------------------------- | ----------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| `key`                                     | *str*                                     | :heavy_check_mark:                        | The name of the parameter to check.       |
| `value`                                   | *str*                                     | :heavy_check_mark:                        | The value to check against the parameter. |
| `operator`                                | *OptionalNullable[str]*                   | :heavy_minus_sign:                        | N/A                                       |