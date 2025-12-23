# hlconnect_client.PurchaseCancelApi

All URIs are relative to *https://hlconnect-api.mu.se*

Method | HTTP request | Description
------------- | ------------- | -------------
[**connector_purchase_cancel**](PurchaseCancelApi.md#connector_purchase_cancel) | **DELETE** /purchase/cancel | Cancel purchase order line item


# **connector_purchase_cancel**
> connector_purchase_cancel(order_id, order_line_id)

Cancel purchase order line item

Cancels a specific line item within a purchase order. The order must be in a cancellable status. Both order ID and order line ID must be specified.

### Example

* Bearer Authentication (access_token):

```python
import hlconnect_client
from hlconnect_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://hlconnect-api.mu.se
# See configuration.py for a list of all supported configuration parameters.
configuration = hlconnect_client.Configuration(
    host = "https://hlconnect-api.mu.se"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: access_token
configuration = hlconnect_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with hlconnect_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = hlconnect_client.PurchaseCancelApi(api_client)
    order_id = 12345 # int | Vendor order ID containing the line item to cancel
    order_line_id = 1 # int | Specific line item within the order to cancel

    try:
        # Cancel purchase order line item
        api_instance.connector_purchase_cancel(order_id, order_line_id)
    except Exception as e:
        print("Exception when calling PurchaseCancelApi->connector_purchase_cancel: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_id** | **int**| Vendor order ID containing the line item to cancel | 
 **order_line_id** | **int**| Specific line item within the order to cancel | 

### Return type

void (empty response body)

### Authorization

[access_token](../README.md#access_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Order line item successfully cancelled |  * X-Environment -  <br>  |
**400** | Bad Request - Invalid order status for cancellation |  -  |
**401** | Unauthorized - Missing or invalid access token |  -  |
**404** | Not Found - No order found for the specified order and line item |  -  |
**500** | Internal Server Error - Something went wrong processing the request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

