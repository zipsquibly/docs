# Organizations
(*organizations*)

## Overview

Operations related to organizations

### Available Operations

* [list](#list) - Organizations List

## list

List all organizations

### Example Usage

```python
import os
from syllable_sdk import Syllable

s = Syllable(
    api_key_header=os.getenv("SYLLABLE_API_KEY_HEADER", ""),
)

res = s.organizations.list()

if res is not None:
    # handle response
    pass

```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |

### Response

**[List[models.Organization]](../../models/.md)**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| models.SDKError | 4XX, 5XX        | \*/\*           |