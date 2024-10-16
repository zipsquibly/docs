# Targets
(*channels.targets*)

## Overview

Operations related to channel targets

### Available Operations

* [list](#list) - Get Channel Targets
* [create](#create) - Assign A Channel Target
* [get_by_id](#get_by_id) - Get A Channel Target
* [update](#update) - Edit Channel Target

## list

Get Channel Targets

### Example Usage

```python
import os
from syllable_sdk import Syllable

s = Syllable(
    api_key_header=os.getenv("SYLLABLE_API_KEY_HEADER", ""),
)

res = s.channels.targets.list()

if res is not None:
    # handle response
    pass

```

### Parameters

| Parameter                                                                     | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `request`                                                                     | [models.ChannelTargetsListRequest](../../models/channeltargetslistrequest.md) | :heavy_check_mark:                                                            | The request object to use for the request.                                    |
| `retries`                                                                     | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)              | :heavy_minus_sign:                                                            | Configuration to override the default retry behavior of the client.           |

### Response

**[models.ChannelTargetListResponse](../../models/channeltargetlistresponse.md)**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.HTTPValidationError | 422                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

## create

Assign A Channel Target

### Example Usage

```python
import os
from syllable_sdk import Syllable

s = Syllable(
    api_key_header=os.getenv("SYLLABLE_API_KEY_HEADER", ""),
)

res = s.channels.targets.create(channel_id=134365, channel_target_create_request={
    "channel_id": 486589,
    "channel_name": "<value>",
    "agent_id": 638424,
    "target": "<value>",
    "target_mode": "<value>",
    "fallback_target": "<value>",
    "is_test": True,
})

if res is not None:
    # handle response
    pass

```

### Parameters

| Parameter                                                                       | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `channel_id`                                                                    | *int*                                                                           | :heavy_check_mark:                                                              | N/A                                                                             |
| `channel_target_create_request`                                                 | [models.ChannelTargetCreateRequest](../../models/channeltargetcreaterequest.md) | :heavy_check_mark:                                                              | N/A                                                                             |
| `retries`                                                                       | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)                | :heavy_minus_sign:                                                              | Configuration to override the default retry behavior of the client.             |

### Response

**[models.ChannelTarget](../../models/channeltarget.md)**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.HTTPValidationError | 422                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

## get_by_id

Get A Channel Target

### Example Usage

```python
import os
from syllable_sdk import Syllable

s = Syllable(
    api_key_header=os.getenv("SYLLABLE_API_KEY_HEADER", ""),
)

res = s.channels.targets.get_by_id(channel_id=931598, target_id=505057)

if res is not None:
    # handle response
    pass

```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `channel_id`                                                        | *int*                                                               | :heavy_check_mark:                                                  | N/A                                                                 |
| `target_id`                                                         | *int*                                                               | :heavy_check_mark:                                                  | N/A                                                                 |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |

### Response

**[models.ChannelTarget](../../models/channeltarget.md)**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.HTTPValidationError | 422                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

## update

Update channel target by ID

### Example Usage

```python
import os
from syllable_sdk import Syllable

s = Syllable(
    api_key_header=os.getenv("SYLLABLE_API_KEY_HEADER", ""),
)

res = s.channels.targets.update(channel_id=627690, target_id=488852, channel_target={
    "id": 857478,
    "channel_id": 597129,
    "channel_name": "<value>",
    "agent_id": 344620,
    "target": "<value>",
    "target_mode": "<value>",
    "fallback_target": "<value>",
    "is_test": False,
})

if res is not None:
    # handle response
    pass

```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `channel_id`                                                        | *int*                                                               | :heavy_check_mark:                                                  | N/A                                                                 |
| `target_id`                                                         | *int*                                                               | :heavy_check_mark:                                                  | N/A                                                                 |
| `channel_target`                                                    | [models.ChannelTarget](../../models/channeltarget.md)               | :heavy_check_mark:                                                  | N/A                                                                 |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |

### Response

**[models.ChannelTarget](../../models/channeltarget.md)**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.HTTPValidationError | 422                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |