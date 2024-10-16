# Dashboards
(*dashboards*)

## Overview

### Available Operations

* [get_total_call_volume_by_weekday](#get_total_call_volume_by_weekday) - Get Total Call Volume By Weekday
* [get_total_call_volume_by_hour](#get_total_call_volume_by_hour) - Get Total Call Volume By Hour
* [get_weekly_call_volume_by_weekday](#get_weekly_call_volume_by_weekday) - Get Weekly Call Volume By Weekday
* [get_daily_call_volume_by_hour](#get_daily_call_volume_by_hour) - Get Daily Call Volume By Hour
* [get_monthly_call_volume_by_week](#get_monthly_call_volume_by_week) - Get Monthly Call Volume By Week
* [get_monthly_call_volume_by_day](#get_monthly_call_volume_by_day) - Get Monthly Call Volume By Day
* [get_session_summary](#get_session_summary) - Get Session Summary
* [get_session_agents](#get_session_agents) - Get Agents

## get_total_call_volume_by_weekday

Get total call volume by weekday.

### Example Usage

```python
import os
from syllable_sdk import Syllable

s = Syllable(
    api_key_header=os.getenv("SYLLABLE_API_KEY_HEADER", ""),
)

res = s.dashboards.get_total_call_volume_by_weekday()

if res is not None:
    # handle response
    pass

```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |

### Response

**[models.TotalCallVolumeByWeekdayResponseTotalCallVolumeByWeekday](../../models/totalcallvolumebyweekdayresponsetotalcallvolumebyweekday.md)**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| models.SDKError | 4XX, 5XX        | \*/\*           |

## get_total_call_volume_by_hour

Get total call volume by hour.

### Example Usage

```python
import os
from syllable_sdk import Syllable

s = Syllable(
    api_key_header=os.getenv("SYLLABLE_API_KEY_HEADER", ""),
)

res = s.dashboards.get_total_call_volume_by_hour()

if res is not None:
    # handle response
    pass

```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |

### Response

**[models.GetTotalCallVolumeByHourResponseGetTotalCallVolumeByHour](../../models/gettotalcallvolumebyhourresponsegettotalcallvolumebyhour.md)**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| models.SDKError | 4XX, 5XX        | \*/\*           |

## get_weekly_call_volume_by_weekday

Get weekly call volume by weekday.

### Example Usage

```python
import os
from syllable_sdk import Syllable

s = Syllable(
    api_key_header=os.getenv("SYLLABLE_API_KEY_HEADER", ""),
)

res = s.dashboards.get_weekly_call_volume_by_weekday()

if res is not None:
    # handle response
    pass

```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |

### Response

**[models.GetWeeklyCallVolumeByWeekdayResponseGetWeeklyCallVolumeByWeekday](../../models/getweeklycallvolumebyweekdayresponsegetweeklycallvolumebyweekday.md)**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| models.SDKError | 4XX, 5XX        | \*/\*           |

## get_daily_call_volume_by_hour

Get daily call volume by hour.

### Example Usage

```python
import os
from syllable_sdk import Syllable

s = Syllable(
    api_key_header=os.getenv("SYLLABLE_API_KEY_HEADER", ""),
)

res = s.dashboards.get_daily_call_volume_by_hour()

if res is not None:
    # handle response
    pass

```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |

### Response

**[models.GetDailyCallVolumeByHourResponseGetDailyCallVolumeByHour](../../models/getdailycallvolumebyhourresponsegetdailycallvolumebyhour.md)**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| models.SDKError | 4XX, 5XX        | \*/\*           |

## get_monthly_call_volume_by_week

Get monthly cal volume by week.

### Example Usage

```python
import os
from syllable_sdk import Syllable

s = Syllable(
    api_key_header=os.getenv("SYLLABLE_API_KEY_HEADER", ""),
)

res = s.dashboards.get_monthly_call_volume_by_week()

if res is not None:
    # handle response
    pass

```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |

### Response

**[models.GetMonthlyCallVolumeByWeekResponseGetMonthlyCallVolumeByWeek](../../models/getmonthlycallvolumebyweekresponsegetmonthlycallvolumebyweek.md)**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| models.SDKError | 4XX, 5XX        | \*/\*           |

## get_monthly_call_volume_by_day

Get monthly call volume by day.

### Example Usage

```python
import os
from syllable_sdk import Syllable

s = Syllable(
    api_key_header=os.getenv("SYLLABLE_API_KEY_HEADER", ""),
)

res = s.dashboards.get_monthly_call_volume_by_day()

if res is not None:
    # handle response
    pass

```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |

### Response

**[models.GetMonthlyCallVolumeByDayResponseGetMonthlyCallVolumeByDay](../../models/getmonthlycallvolumebydayresponsegetmonthlycallvolumebyday.md)**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| models.SDKError | 4XX, 5XX        | \*/\*           |

## get_session_summary

Get session summary data

### Example Usage

```python
import os
from syllable_sdk import Syllable

s = Syllable(
    api_key_header=os.getenv("SYLLABLE_API_KEY_HEADER", ""),
)

res = s.dashboards.get_session_summary()

if res is not None:
    # handle response
    pass

```

### Parameters

| Parameter                                                                   | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `request`                                                                   | [models.GetSessionSummaryRequest](../../models/getsessionsummaryrequest.md) | :heavy_check_mark:                                                          | The request object to use for the request.                                  |
| `retries`                                                                   | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)            | :heavy_minus_sign:                                                          | Configuration to override the default retry behavior of the client.         |

### Response

**[models.GetSessionSummaryResponseGetSessionSummary](../../models/getsessionsummaryresponsegetsessionsummary.md)**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.HTTPValidationError | 422                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

## get_session_agents

Get list of agents for session summary dropdown

### Example Usage

```python
import os
from syllable_sdk import Syllable

s = Syllable(
    api_key_header=os.getenv("SYLLABLE_API_KEY_HEADER", ""),
)

res = s.dashboards.get_session_agents()

if res is not None:
    # handle response
    pass

```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |

### Response

**[models.GetSessionAgentsResponseGetSessionAgents](../../models/getsessionagentsresponsegetsessionagents.md)**

### Errors

| Error Type      | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| models.SDKError | 4XX, 5XX        | \*/\*           |