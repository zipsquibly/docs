# syllable-sdk

Developer-friendly & type-safe Python SDK specifically catered to leverage *syllable-sdk* API.

<div align="left">
    <a href="https://www.speakeasy.com/?utm_source=syllable-sdk&utm_campaign=python"><img src="https://custom-icon-badges.demolab.com/badge/-Built%20By%20Speakeasy-212015?style=for-the-badge&logoColor=FBE331&logo=speakeasy&labelColor=545454" /></a>
    <a href="https://opensource.org/licenses/MIT">
        <img src="https://img.shields.io/badge/License-MIT-blue.svg" style="width: 100px; height: 28px;" />
    </a>
</div>


<br /><br />
> [!IMPORTANT]
> This SDK is not yet ready for production use. To complete setup please follow the steps outlined in your [workspace](https://app.speakeasy.com/org/syllableai/syllableai). Delete this section before > publishing to a package manager.

<!-- Start Summary [summary] -->
## Summary

SyllableSDK: 
# Syllble Platform SDK

Syllble SDK gives you the power of awesome AI agentry. 🚀

## Overview

The Syllble SDK provides a comprehensive set of tools and APIs to integrate powerful AI capabilities into your applications. Whether you're building chatbots, virtual assistants, or any other AI-driven solutions, Syllble SDK has got you covered.

## Features

- **Natural Language Processing (NLP)**: Understand and generate human language with ease.
- **Machine Learning Models**: Leverage pre-trained models or train your own custom models.
- **Speech Recognition**: Convert speech to text and vice versa.
- **Image Recognition**: Identify objects, faces, and scenes in images.
- **Data Analytics**: Analyze and visualize data to gain insights.
- **Integration**: Seamlessly integrate with other services and platforms.
<!-- End Summary [summary] -->

<!-- Start Table of Contents [toc] -->
## Table of Contents

* [SDK Installation](#sdk-installation)
* [IDE Support](#ide-support)
* [SDK Example Usage](#sdk-example-usage)
* [Available Resources and Operations](#available-resources-and-operations)
* [Retries](#retries)
* [Error Handling](#error-handling)
* [Server Selection](#server-selection)
* [Custom HTTP Client](#custom-http-client)
* [Authentication](#authentication)
* [Debugging](#debugging)
<!-- End Table of Contents [toc] -->

<!-- Start SDK Installation [installation] -->
## SDK Installation

The SDK can be installed with either *pip* or *poetry* package managers.

### PIP

*PIP* is the default package installer for Python, enabling easy installation and management of packages from PyPI via the command line.

```bash
pip install git+<UNSET>.git
```

### Poetry

*Poetry* is a modern tool that simplifies dependency management and package publishing by using a single `pyproject.toml` file to handle project metadata and dependencies.

```bash
poetry add git+<UNSET>.git
```
<!-- End SDK Installation [installation] -->

<!-- Start IDE Support [idesupport] -->
## IDE Support

### PyCharm

Generally, the SDK will work well with most IDEs out of the box. However, when using PyCharm, you can enjoy much better integration with Pydantic by installing an additional plugin.

- [PyCharm Pydantic Plugin](https://docs.pydantic.dev/latest/integrations/pycharm/)
<!-- End IDE Support [idesupport] -->

<!-- Start SDK Example Usage [usage] -->
## SDK Example Usage

### Example

```python
# Synchronous Example
import os
from syllable_sdk import Syllable

s = Syllable(
    api_key_header=os.getenv("SYLLABLE_API_KEY_HEADER", ""),
)

res = s.agents.list()

if res is not None:
    # handle response
    pass
```

</br>

The same SDK client can also be used to make asychronous requests by importing asyncio.
```python
# Asynchronous Example
import asyncio
import os
from syllable_sdk import Syllable

async def main():
    s = Syllable(
        api_key_header=os.getenv("SYLLABLE_API_KEY_HEADER", ""),
    )
    res = await s.agents.list_async()
    if res is not None:
        # handle response
        pass

asyncio.run(main())
```
<!-- End SDK Example Usage [usage] -->

<!-- Start Available Resources and Operations [operations] -->
## Available Resources and Operations

<details open>
<summary>Available methods</summary>

### [agents](docs/sdks/agents/README.md)

* [list](docs/sdks/agents/README.md#list) - Agent List
* [create](docs/sdks/agents/README.md#create) - Create Agent
* [update](docs/sdks/agents/README.md#update) - Update Agent
* [get_by_id](docs/sdks/agents/README.md#get_by_id) - Get Agent By Id
* [delete](docs/sdks/agents/README.md#delete) - Delete Agent

#### [agents.chats](docs/sdks/chats/README.md)

* [send_message](docs/sdks/chats/README.md#send_message) - Send New Message

### [channels](docs/sdks/channels/README.md)

* [list](docs/sdks/channels/README.md#list) - Get Channels
* [delete](docs/sdks/channels/README.md#delete) - Delete Channel

#### [channels.available_targets](docs/sdks/availabletargets/README.md)

* [list](docs/sdks/availabletargets/README.md#list) - Available Targets List

#### [channels.targets](docs/sdks/targets/README.md)

* [list](docs/sdks/targets/README.md#list) - Get Channel Targets
* [create](docs/sdks/targets/README.md#create) - Assign A Channel Target
* [get_by_id](docs/sdks/targets/README.md#get_by_id) - Get A Channel Target
* [update](docs/sdks/targets/README.md#update) - Edit Channel Target

### [conversations](docs/sdks/conversations/README.md)

* [list](docs/sdks/conversations/README.md#list) - Conversations List
* [get](docs/sdks/conversations/README.md#get) - Get Conversation By Id

### [dashboards](docs/sdks/dashboards/README.md)

* [get_total_call_volume_by_weekday](docs/sdks/dashboards/README.md#get_total_call_volume_by_weekday) - Get Total Call Volume By Weekday
* [get_total_call_volume_by_hour](docs/sdks/dashboards/README.md#get_total_call_volume_by_hour) - Get Total Call Volume By Hour
* [get_weekly_call_volume_by_weekday](docs/sdks/dashboards/README.md#get_weekly_call_volume_by_weekday) - Get Weekly Call Volume By Weekday
* [get_daily_call_volume_by_hour](docs/sdks/dashboards/README.md#get_daily_call_volume_by_hour) - Get Daily Call Volume By Hour
* [get_monthly_call_volume_by_week](docs/sdks/dashboards/README.md#get_monthly_call_volume_by_week) - Get Monthly Call Volume By Week
* [get_monthly_call_volume_by_day](docs/sdks/dashboards/README.md#get_monthly_call_volume_by_day) - Get Monthly Call Volume By Day
* [get_session_summary](docs/sdks/dashboards/README.md#get_session_summary) - Get Session Summary
* [get_session_agents](docs/sdks/dashboards/README.md#get_session_agents) - Get Agents

### [events](docs/sdks/events/README.md)

* [list](docs/sdks/events/README.md#list) - Events List

### [greetings](docs/sdks/greetings/README.md)

* [list](docs/sdks/greetings/README.md#list) - Greetings List
* [create](docs/sdks/greetings/README.md#create) - Create Greeting
* [update](docs/sdks/greetings/README.md#update) - Update Greeting
* [get_by_id](docs/sdks/greetings/README.md#get_by_id) - Get Greeting By Id
* [delete](docs/sdks/greetings/README.md#delete) - Delete Greeting

### [organizations](docs/sdks/organizations/README.md)

* [list](docs/sdks/organizations/README.md#list) - Organizations List

### [prompts](docs/sdks/prompts/README.md)

* [list](docs/sdks/prompts/README.md#list) - Prompt List
* [create](docs/sdks/prompts/README.md#create) - Create Prompt
* [update](docs/sdks/prompts/README.md#update) - Update Prompt
* [get_by_id](docs/sdks/prompts/README.md#get_by_id) - Get Prompt By Id
* [delete](docs/sdks/prompts/README.md#delete) - Delete Prompt

### [sessions](docs/sdks/sessions/README.md)

* [list](docs/sdks/sessions/README.md#list) - Sessions List


### [tools](docs/sdks/tools/README.md)

* [list](docs/sdks/tools/README.md#list) - Tool List
* [get_by_name](docs/sdks/tools/README.md#get_by_name) - Tool Info

</details>
<!-- End Available Resources and Operations [operations] -->

<!-- Start Retries [retries] -->
## Retries

Some of the endpoints in this SDK support retries. If you use the SDK without any configuration, it will fall back to the default retry strategy provided by the API. However, the default retry strategy can be overridden on a per-operation basis, or across the entire SDK.

To change the default retry strategy for a single API call, simply provide a `RetryConfig` object to the call:
```python
import os
from syllable.utils import BackoffStrategy, RetryConfig
from syllable_sdk import Syllable

s = Syllable(
    api_key_header=os.getenv("SYLLABLE_API_KEY_HEADER", ""),
)

res = s.agents.list(,
    RetryConfig("backoff", BackoffStrategy(1, 50, 1.1, 100), False))

if res is not None:
    # handle response
    pass

```

If you'd like to override the default retry strategy for all operations that support retries, you can use the `retry_config` optional parameter when initializing the SDK:
```python
import os
from syllable.utils import BackoffStrategy, RetryConfig
from syllable_sdk import Syllable

s = Syllable(
    retry_config=RetryConfig("backoff", BackoffStrategy(1, 50, 1.1, 100), False),
    api_key_header=os.getenv("SYLLABLE_API_KEY_HEADER", ""),
)

res = s.agents.list()

if res is not None:
    # handle response
    pass

```
<!-- End Retries [retries] -->

<!-- Start Error Handling [errors] -->
## Error Handling

Handling errors in this SDK should largely match your expectations. All operations return a response object or raise an exception.

By default, an API error will raise a models.SDKError exception, which has the following properties:

| Property        | Type             | Description           |
|-----------------|------------------|-----------------------|
| `.status_code`  | *int*            | The HTTP status code  |
| `.message`      | *str*            | The error message     |
| `.raw_response` | *httpx.Response* | The raw HTTP response |
| `.body`         | *str*            | The response content  |

When custom error responses are specified for an operation, the SDK may also raise their associated exceptions. You can refer to respective *Errors* tables in SDK docs for more details on possible exception types for each operation. For example, the `list_async` method may raise the following exceptions:

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models.HTTPValidationError | 422                        | application/json           |
| models.SDKError            | 4XX, 5XX                   | \*/\*                      |

### Example

```python
import os
from syllable_sdk import Syllable, models

s = Syllable(
    api_key_header=os.getenv("SYLLABLE_API_KEY_HEADER", ""),
)

res = None
try:
    res = s.agents.list()

    if res is not None:
        # handle response
        pass

except models.HTTPValidationError as e:
    # handle e.data: models.HTTPValidationErrorData
    raise(e)
except models.SDKError as e:
    # handle exception
    raise(e)
```
<!-- End Error Handling [errors] -->

<!-- Start Server Selection [server] -->
## Server Selection

### Select Server by Index

You can override the default server globally by passing a server index to the `server_idx: int` optional parameter when initializing the SDK client instance. The selected server will then be used as the default on the operations that use it. This table lists the indexes associated with the available servers:

| # | Server | Variables |
| - | ------ | --------- |
| 0 | `http://localhost:8001` | None |

#### Example

```python
import os
from syllable_sdk import Syllable

s = Syllable(
    server_idx=0,
    api_key_header=os.getenv("SYLLABLE_API_KEY_HEADER", ""),
)

res = s.agents.list()

if res is not None:
    # handle response
    pass

```


### Override Server URL Per-Client

The default server can also be overridden globally by passing a URL to the `server_url: str` optional parameter when initializing the SDK client instance. For example:
```python
import os
from syllable_sdk import Syllable

s = Syllable(
    server_url="http://localhost:8001",
    api_key_header=os.getenv("SYLLABLE_API_KEY_HEADER", ""),
)

res = s.agents.list()

if res is not None:
    # handle response
    pass

```
<!-- End Server Selection [server] -->

<!-- Start Custom HTTP Client [http-client] -->
## Custom HTTP Client

The Python SDK makes API calls using the [httpx](https://www.python-httpx.org/) HTTP library.  In order to provide a convenient way to configure timeouts, cookies, proxies, custom headers, and other low-level configuration, you can initialize the SDK client with your own HTTP client instance.
Depending on whether you are using the sync or async version of the SDK, you can pass an instance of `HttpClient` or `AsyncHttpClient` respectively, which are Protocol's ensuring that the client has the necessary methods to make API calls.
This allows you to wrap the client with your own custom logic, such as adding custom headers, logging, or error handling, or you can just pass an instance of `httpx.Client` or `httpx.AsyncClient` directly.

For example, you could specify a header for every request that this sdk makes as follows:
```python
from syllable_sdk import Syllable
import httpx

http_client = httpx.Client(headers={"x-custom-header": "someValue"})
s = Syllable(client=http_client)
```

or you could wrap the client with your own custom logic:
```python
from syllable_sdk import Syllable
from syllable_sdk.httpclient import AsyncHttpClient
import httpx

class CustomClient(AsyncHttpClient):
    client: AsyncHttpClient

    def __init__(self, client: AsyncHttpClient):
        self.client = client

    async def send(
        self,
        request: httpx.Request,
        *,
        stream: bool = False,
        auth: Union[
            httpx._types.AuthTypes, httpx._client.UseClientDefault, None
        ] = httpx.USE_CLIENT_DEFAULT,
        follow_redirects: Union[
            bool, httpx._client.UseClientDefault
        ] = httpx.USE_CLIENT_DEFAULT,
    ) -> httpx.Response:
        request.headers["Client-Level-Header"] = "added by client"

        return await self.client.send(
            request, stream=stream, auth=auth, follow_redirects=follow_redirects
        )

    def build_request(
        self,
        method: str,
        url: httpx._types.URLTypes,
        *,
        content: Optional[httpx._types.RequestContent] = None,
        data: Optional[httpx._types.RequestData] = None,
        files: Optional[httpx._types.RequestFiles] = None,
        json: Optional[Any] = None,
        params: Optional[httpx._types.QueryParamTypes] = None,
        headers: Optional[httpx._types.HeaderTypes] = None,
        cookies: Optional[httpx._types.CookieTypes] = None,
        timeout: Union[
            httpx._types.TimeoutTypes, httpx._client.UseClientDefault
        ] = httpx.USE_CLIENT_DEFAULT,
        extensions: Optional[httpx._types.RequestExtensions] = None,
    ) -> httpx.Request:
        return self.client.build_request(
            method,
            url,
            content=content,
            data=data,
            files=files,
            json=json,
            params=params,
            headers=headers,
            cookies=cookies,
            timeout=timeout,
            extensions=extensions,
        )

s = Syllable(async_client=CustomClient(httpx.AsyncClient()))
```
<!-- End Custom HTTP Client [http-client] -->

<!-- Start Authentication [security] -->
## Authentication

### Per-Client Security Schemes

This SDK supports the following security scheme globally:

| Name                      | Type                      | Scheme                    | Environment Variable      |
| ------------------------- | ------------------------- | ------------------------- | ------------------------- |
| `api_key_header`          | apiKey                    | API key                   | `SYLLABLE_API_KEY_HEADER` |

To authenticate with the API the `api_key_header` parameter must be set when initializing the SDK client instance. For example:
```python
import os
from syllable_sdk import Syllable

s = Syllable(
    api_key_header=os.getenv("SYLLABLE_API_KEY_HEADER", ""),
)

res = s.agents.list()

if res is not None:
    # handle response
    pass

```
<!-- End Authentication [security] -->

<!-- Start Debugging [debug] -->
## Debugging

You can setup your SDK to emit debug logs for SDK requests and responses.

You can pass your own logger class directly into your SDK.
```python
from syllable_sdk import Syllable
import logging

logging.basicConfig(level=logging.DEBUG)
s = Syllable(debug_logger=logging.getLogger("syllable_sdk"))
```

You can also enable a default debug logger by setting an environment variable `SYLLABLE_DEBUG` to true.
<!-- End Debugging [debug] -->

<!-- Placeholder for Future Speakeasy SDK Sections -->

# Development

## Maturity

This SDK is in beta, and there may be breaking changes between versions without a major version update. Therefore, we recommend pinning usage
to a specific package version. This way, you can install the same version each time without breaking changes unless you are intentionally
looking for the latest version.

## Contributions

While we value open-source contributions to this SDK, this library is generated programmatically. Any manual changes added to internal files will be overwritten on the next generation. 
We look forward to hearing your feedback. Feel free to open a PR or an issue with a proof of concept and we'll do our best to include it in a future release. 

### SDK Created by [Speakeasy](https://www.speakeasy.com/?utm_source=syllable-sdk&utm_campaign=python)
