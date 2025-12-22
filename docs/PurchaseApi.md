# openapi_client.PurchaseApi

All URIs are relative to *https://hlconnect-api-sandbox.mu.se*

Method | HTTP request | Description
------------- | ------------- | -------------
[**connector_purchase_cancel**](PurchaseApi.md#connector_purchase_cancel) | **DELETE** /purchase/cancel | Cancel purchase order line item
[**connector_purchase_download_url**](PurchaseApi.md#connector_purchase_download_url) | **GET** /purchase/download-url | Get asset download URL
[**connector_purchase_info**](PurchaseApi.md#connector_purchase_info) | **GET** /purchase/info | Retrieve purchase order information
[**connector_purchase_register**](PurchaseApi.md#connector_purchase_register) | **POST** /purchase/register | Register a new purchase transaction
[**connector_purchase_view_url**](PurchaseApi.md#connector_purchase_view_url) | **GET** /purchase/view-url | Get asset view URL


# **connector_purchase_cancel**
> connector_purchase_cancel(order_id, order_line_id)

Cancel purchase order line item

Cancels a specific line item within a purchase order. The order must be in a cancellable status. Both order ID and order line ID must be specified.

### Example

* Bearer Authentication (access_token):

```python
import openapi_client
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
    api_instance = openapi_client.PurchaseApi(api_client)
    order_id = 12345 # int | Vendor order ID containing the line item to cancel
    order_line_id = 1 # int | Specific line item within the order to cancel

    try:
        # Cancel purchase order line item
        api_instance.connector_purchase_cancel(order_id, order_line_id)
    except Exception as e:
        print("Exception when calling PurchaseApi->connector_purchase_cancel: %s\n" % e)
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

# **connector_purchase_download_url**
> DownloadUrl connector_purchase_download_url(order_id, order_line_id)

Get asset download URL

Generates and returns a secure download URL for a purchased digital asset. The URL can be used to download the asset file.

### Example

* Bearer Authentication (access_token):

```python
import openapi_client
from openapi_client.models.download_url import DownloadUrl
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
    api_instance = openapi_client.PurchaseApi(api_client)
    order_id = 12345 # int | Vendor order ID that contains the asset to download
    order_line_id = 1 # int | Specific line item within the order that identifies the asset to download

    try:
        # Get asset download URL
        api_response = api_instance.connector_purchase_download_url(order_id, order_line_id)
        print("The response of PurchaseApi->connector_purchase_download_url:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PurchaseApi->connector_purchase_download_url: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_id** | **int**| Vendor order ID that contains the asset to download | 
 **order_line_id** | **int**| Specific line item within the order that identifies the asset to download | 

### Return type

[**DownloadUrl**](DownloadUrl.md)

### Authorization

[access_token](../README.md#access_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Download URL successfully generated and returned |  * X-Environment -  <br>  |
**401** | Unauthorized - Missing or invalid access token |  -  |
**404** | Not Found - No download URL found for the specified order and line item |  -  |
**500** | Internal Server Error - Something went wrong processing the request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

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
    api_instance = openapi_client.PurchaseApi(api_client)
    order_id = 12345 # int | Vendor order ID to retrieve purchase details for. This is the unique identifier assigned by the vendor when placing the order.

    try:
        # Retrieve purchase order information
        api_response = api_instance.connector_purchase_info(order_id)
        print("The response of PurchaseApi->connector_purchase_info:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PurchaseApi->connector_purchase_info: %s\n" % e)
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

# **connector_purchase_register**
> connector_purchase_register(purchase_register_request)

Register a new purchase transaction

Initiates the purchase process for a digital asset. Validates request parameters, creates a new order, and begins fulfillment. This is an asynchronous operation - use /purchase/info to check order status.

### Example

* Bearer Authentication (access_token):

```python
import openapi_client
from openapi_client.models.purchase_register_request import PurchaseRegisterRequest
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
    api_instance = openapi_client.PurchaseApi(api_client)
    purchase_register_request = openapi_client.PurchaseRegisterRequest() # PurchaseRegisterRequest | Purchase registration request with asset and order details

    try:
        # Register a new purchase transaction
        api_instance.connector_purchase_register(purchase_register_request)
    except Exception as e:
        print("Exception when calling PurchaseApi->connector_purchase_register: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **purchase_register_request** | [**PurchaseRegisterRequest**](PurchaseRegisterRequest.md)| Purchase registration request with asset and order details | 

### Return type

void (empty response body)

### Authorization

[access_token](../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Purchase registration process successfully initiated |  * X-Environment -  <br>  |
**401** | Unauthorized - Missing or invalid access token |  -  |
**404** | Not Found - Specified asset ID does not exist |  -  |
**409** | Conflict - Order already exists for the specified parameters |  -  |
**422** | Unprocessable Entity - Request validation failed |  -  |
**500** | Internal Server Error - Something went wrong processing the request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

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
    api_instance = openapi_client.PurchaseApi(api_client)
    order_id = 12345 # int | Vendor order ID that contains the asset to view
    order_line_id = 1 # int | Specific line item within the order that identifies the asset to view

    try:
        # Get asset view URL
        api_response = api_instance.connector_purchase_view_url(order_id, order_line_id)
        print("The response of PurchaseApi->connector_purchase_view_url:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PurchaseApi->connector_purchase_view_url: %s\n" % e)
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

