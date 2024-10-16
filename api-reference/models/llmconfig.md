# LlmConfig

LlmConfig


## Fields

| Field                                                                 | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `provider`                                                            | [OptionalNullable[models.Provider]](../models/provider.md)            | :heavy_minus_sign:                                                    | Provider of the LLM model.                                            |
| `model`                                                               | *OptionalNullable[str]*                                               | :heavy_minus_sign:                                                    | Name of the model. Must match the deployment name in Azure AI Studio. |
| `version`                                                             | *OptionalNullable[str]*                                               | :heavy_minus_sign:                                                    | N/A                                                                   |
| `api_version`                                                         | *OptionalNullable[str]*                                               | :heavy_minus_sign:                                                    | N/A                                                                   |