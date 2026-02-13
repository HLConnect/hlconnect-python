# hlconnect_client.PurchaseValidationApi

All URIs are relative to *https://hlconnect-api.mu.se*

Method | HTTP request | Description
------------- | ------------- | -------------
[**connector_purchase_validate_purchase_before_payment**](PurchaseValidationApi.md#connector_purchase_validate_purchase_before_payment) | **POST** /purchase/validate-purchase-before-payment | Validate purchase before payment


# **connector_purchase_validate_purchase_before_payment**
> ValidationToken connector_purchase_validate_purchase_before_payment(purchase_validate_before_payment_request)

Validate purchase before payment

Validates purchase parameters before payment is initiated. Checks asset availability, regional restrictions (based on buyer IP), and minimum quantity requirements. 

### Example

* Bearer Authentication (access_token):

```python
import hlconnect_client
from hlconnect_client.models.purchase_validate_before_payment_request import PurchaseValidateBeforePaymentRequest
from hlconnect_client.models.validation_token import ValidationToken
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
    api_instance = hlconnect_client.PurchaseValidationApi(api_client)
    purchase_validate_before_payment_request = hlconnect_client.PurchaseValidateBeforePaymentRequest() # PurchaseValidateBeforePaymentRequest | Purchase validation request with asset, buyer IP and quantity

    try:
        # Validate purchase before payment
        api_response = api_instance.connector_purchase_validate_purchase_before_payment(purchase_validate_before_payment_request)
        print("The response of PurchaseValidationApi->connector_purchase_validate_purchase_before_payment:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PurchaseValidationApi->connector_purchase_validate_purchase_before_payment: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **purchase_validate_before_payment_request** | [**PurchaseValidateBeforePaymentRequest**](PurchaseValidateBeforePaymentRequest.md)| Purchase validation request with asset, buyer IP and quantity | 

### Return type

[**ValidationToken**](ValidationToken.md)

### Authorization

[access_token](../README.md#access_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Validation successful. Verification token generated |  * X-Environment -  <br>  |
**400** | Bad Request |  -  |
**401** | Unauthorized - Missing or invalid access token |  -  |
**404** | Not Found - Specified asset ID does not exist |  -  |
**422** | Unprocessable Entity - Request validation failed |  -  |
**500** | Internal Server Error - Something went wrong processing the request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

