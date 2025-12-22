# PurchaseInProcessingResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** | Current processing status of the order | [optional] 

## Example

```python
from openapi_client.models.purchase_in_processing_response import PurchaseInProcessingResponse

# TODO update the JSON string below
json = "{}"
# create an instance of PurchaseInProcessingResponse from a JSON string
purchase_in_processing_response_instance = PurchaseInProcessingResponse.from_json(json)
# print the JSON string representation of the object
print(PurchaseInProcessingResponse.to_json())

# convert the object into a dict
purchase_in_processing_response_dict = purchase_in_processing_response_instance.to_dict()
# create an instance of PurchaseInProcessingResponse from a dict
purchase_in_processing_response_from_dict = PurchaseInProcessingResponse.from_dict(purchase_in_processing_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


