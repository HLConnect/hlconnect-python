# openapi_client.PurchaseViewUrlApi

All URIs are relative to *https://hlconnect-api.mu.se*

Method | HTTP request | Description
------------- | ------------- | -------------
[**connector_purchase_view_url**](PurchaseViewUrlApi.md#connector_purchase_view_url) | **GET** /purchase/view-url | Get asset view URL


# **connector_purchase_view_url**
> ViewUrl connector_purchase_view_url(order_id, order_line_id)

Get asset view URL

Generates and returns a secure, time-limited view URL for a purchased digital asset. The URL can be used to view the asset online (e.g., sheet music viewer).

### Example

* Bearer Authentication (access_token):

```python
import openapi_client
from openapi_client.models.view_url import ViewUrl
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://hlconnect-api.mu.se
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://hlconnect-api.mu.se"
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
    api_instance = openapi_client.PurchaseViewUrlApi(api_client)
    order_id = 12345 # int | Vendor order ID that contains the asset to view
    order_line_id = 1 # int | Specific line item within the order that identifies the asset to view

    try:
        # Get asset view URL
        api_response = api_instance.connector_purchase_view_url(order_id, order_line_id)
        print("The response of PurchaseViewUrlApi->connector_purchase_view_url:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PurchaseViewUrlApi->connector_purchase_view_url: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_id** | **int**| Vendor order ID that contains the asset to view | 
 **order_line_id** | **int**| Specific line item within the order that identifies the asset to view | 

### Return type

[**ViewUrl**](ViewUrl.md)

### Authorization

[access_token](../README.md#access_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | View URL successfully generated and returned |  * X-Environment -  <br>  |
**401** | Unauthorized - Missing or invalid access token |  -  |
**404** | Not Found - No view URL found for the specified order and line item |  -  |
**500** | Internal Server Error - Something went wrong processing the request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

