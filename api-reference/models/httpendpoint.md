# HTTPEndpoint

The configuration for an HTTP API call.


## Fields

| Field                                             | Type                                              | Required                                          | Description                                       |
| ------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------- |
| `url`                                             | *str*                                             | :heavy_check_mark:                                | The endpoint URL of the external service to call. |
| `method`                                          | *str*                                             | :heavy_check_mark:                                | The HTTP method to use for the service call.      |
| `argument_location`                               | *str*                                             | :heavy_check_mark:                                | How to pass the arguments to the request.         |