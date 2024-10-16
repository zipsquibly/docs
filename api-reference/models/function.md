# Function

A tool definition to be used by the OpenAI API.  See: - https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/function-calling


## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `name`                                                   | *str*                                                    | :heavy_check_mark:                                       | The name of the function/tool call.                      |
| `description`                                            | *str*                                                    | :heavy_check_mark:                                       | The description of the tool.                             |
| `parameters`                                             | [models.Parameters](../models/parameters.md)             | :heavy_check_mark:                                       | The JSON Schema of parameters of the function/tool call. |