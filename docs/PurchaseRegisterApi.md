# hlconnect_client.PurchaseRegisterApi

All URIs are relative to *https://hlconnect-api.mu.se*

Method | HTTP request | Description
------------- | ------------- | -------------
[**connector_purchase_register**](PurchaseRegisterApi.md#connector_purchase_register) | **POST** /purchase/register | Register a new purchase transaction


# **connector_purchase_register**
> connector_purchase_register(purchase_register_request)

Register a new purchase transaction

Initiates the purchase process for a digital asset. Validates request parameters, creates a new order, and begins fulfillment. This is an asynchronous operation - use /purchase/info to check order status.

### Example

* Bearer Authentication (access_token):

```python
import hlconnect_client
from hlconnect_client.models.purchase_register_request import PurchaseRegisterRequest
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
    api_instance = hlconnect_client.PurchaseRegisterApi(api_client)
    purchase_register_request = hlconnect_client.PurchaseRegisterRequest() # PurchaseRegisterRequest | Purchase registration request with asset and order details

    try:
        # Register a new purchase transaction
        api_instance.connector_purchase_register(purchase_register_request)
    except Exception as e:
        print("Exception when calling PurchaseRegisterApi->connector_purchase_register: %s\n" % e)
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

