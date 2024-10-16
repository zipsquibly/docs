# Sessions
(*sessions*)

## Overview

Operations related to agent sessions

### Available Operations

* [list](#list) - Sessions List

## list

Sessions List

### Example Usage

```python
import os
from syllable_sdk import Syllable

s = Syllable(
    api_key_header=os.getenv("SYLLABLE_API_KEY_HEADER", ""),
)

res = s.sessions.list()

if res is not None:
    # handle response
    pass

```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `request`                                                           | [models.SessionsListRequest](../../models/sessionslistrequest.md)   | :heavy_check_mark:                                                  | The request object to use for the request.                          |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |

### Response

**[models.SessionListResponse](../../models/sessionlistresponse.md)**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.HTTPValidationError | 422                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |