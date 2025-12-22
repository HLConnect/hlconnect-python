# openapi_client.AssetsApi

All URIs are relative to *https://hlconnect-api-sandbox.mu.se*

Method | HTTP request | Description
------------- | ------------- | -------------
[**assets_list**](AssetsApi.md#assets_list) | **GET** /assets/list | Retrieve a paginated list of digital assets


# **assets_list**
> AssetsListResponse assets_list(page_size=page_size, last_id=last_id)

Retrieve a paginated list of digital assets

Returns a list of digital assets with their complete metadata. Assets include information about formats, pricing, contributors, categories, instruments, and related media.

### Example

* Bearer Authentication (access_token):

```python
import openapi_client
from openapi_client.models.assets_list_response import AssetsListResponse
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://hlconnect-api-sandbox.mu.se
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://hlconnect-api-sandbox.mu.se"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: access_token
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.AssetsApi(api_client)
    page_size = 20 # int | Number of assets to return per page (optional) (default to 20)
    last_id = 56 # int | The ID of the last asset from the previous page. Used for pagination to retrieve the next page of results. (optional)

    try:
        # Retrieve a paginated list of digital assets
        api_response = api_instance.assets_list(page_size=page_size, last_id=last_id)
        print("The response of AssetsApi->assets_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AssetsApi->assets_list: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page_size** | **int**| Number of assets to return per page | [optional] [default to 20]
 **last_id** | **int**| The ID of the last asset from the previous page. Used for pagination to retrieve the next page of results. | [optional] 

### Return type

[**AssetsListResponse**](AssetsListResponse.md)

### Authorization

[access_token](../README.md#access_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successfully retrieved list of assets with pagination information |  * X-Environment -  <br>  |
**401** | Unauthorized - Missing or invalid access token |  -  |
**500** | Internal server error - Something went wrong processing the request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

