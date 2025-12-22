# OrderProcessingFailedResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** | Failed order status | [optional] 
**message** | **str** | Detailed error message explaining the failure | [optional] 

## Example

```python
from openapi_client.models.order_processing_failed_response import OrderProcessingFailedResponse

# TODO update the JSON string below
json = "{}"
# create an instance of OrderProcessingFailedResponse from a JSON string
order_processing_failed_response_instance = OrderProcessingFailedResponse.from_json(json)
# print the JSON string representation of the object
print(OrderProcessingFailedResponse.to_json())

# convert the object into a dict
order_processing_failed_response_dict = order_processing_failed_response_instance.to_dict()
# create an instance of OrderProcessingFailedResponse from a dict
order_processing_failed_response_from_dict = OrderProcessingFailedResponse.from_dict(order_processing_failed_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


