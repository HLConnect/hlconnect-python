# hlconnect_client.HealthApi

All URIs are relative to *https://hlconnect-api.mu.se*

Method | HTTP request | Description
------------- | ------------- | -------------
[**health**](HealthApi.md#health) | **GET** /health | Perform system health check


# **health**
> List[HealthItem] health()

Perform system health check

Checks the status of critical system components such as database connections and external services. Returns an array of health check results indicating whether each component is functioning properly. This endpoint is publicly accessible and can be used for monitoring system uptime.

### Example


```python
import hlconnect_client
from hlconnect_client.models.health_item import HealthItem
from hlconnect_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://hlconnect-api.mu.se
# See configuration.py for a list of all supported configuration parameters.
configuration = hlconnect_client.Configuration(
    host = "https://hlconnect-api.mu.se"
)


# Enter a context with an instance of the API client
with hlconnect_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = hlconnect_client.HealthApi(api_client)

    try:
        # Perform system health check
        api_response = api_instance.health()
        print("The response of HealthApi->health:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling HealthApi->health: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**List[HealthItem]**](HealthItem.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Health check completed successfully. Returns status of system components. |  -  |
**500** | Internal server error - Health check failed due to system issues |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

