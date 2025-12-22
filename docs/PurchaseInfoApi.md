# openapi_client.PurchaseInfoApi

All URIs are relative to *https://hlconnect-api.mu.se*

Method | HTTP request | Description
------------- | ------------- | -------------
[**connector_purchase_info**](PurchaseInfoApi.md#connector_purchase_info) | **GET** /purchase/info | Retrieve purchase order information


# **connector_purchase_info**
> List[OrderItem] connector_purchase_info(order_id)

Retrieve purchase order information

Returns detailed information about a purchase order including status, asset details, pricing, and fulfillment status. Response varies based on processing status (complete, processing, failed).

### Example

* Bearer Authentication (access_token):

```python
import openapi_client
from openapi_client.models.order_item import OrderItem
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
    api_instance = openapi_client.PurchaseInfoApi(api_client)
    order_id = 12345 # int | Vendor order ID to retrieve purchase details for. This is the unique identifier assigned by the vendor when placing the order.

    try:
        # Retrieve purchase order information
        api_response = api_instance.connector_purchase_info(order_id)
        print("The response of PurchaseInfoApi->connector_purchase_info:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PurchaseInfoApi->connector_purchase_info: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_id** | **int**| Vendor order ID to retrieve purchase details for. This is the unique identifier assigned by the vendor when placing the order. | 

### Return type

[**List[OrderItem]**](OrderItem.md)

### Authorization

[access_token](../README.md#access_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successfully retrieved order information. Returns list of order items with complete details. |  * X-Environment -  <br>  |
**202** | Order is currently processing. Check back later for completion status. |  * X-Environment -  <br>  |
**401** | Unauthorized - Missing or invalid access token |  -  |
**404** | Not Found - No orders found for the specified order ID |  -  |
**500** | Internal Server Error - Something went wrong processing the request |  -  |
**502** | Bad Gateway - Order processing failed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

