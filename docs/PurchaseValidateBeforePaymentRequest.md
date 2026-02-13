# PurchaseValidateBeforePaymentRequest

Request payload for registering a new purchase transaction. Contains all required information to initiate the purchase of a digital asset.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**asset_id** | **int** | Unique identifier of the digital asset to be purchased | 
**customer_ip** | **str** | Public IP address of the customer for regional restriction validation | 
**quantity** | **int** | The number of asset units to purchase | 

## Example

```python
from hlconnect_client.models.purchase_validate_before_payment_request import PurchaseValidateBeforePaymentRequest

# TODO update the JSON string below
json = "{}"
# create an instance of PurchaseValidateBeforePaymentRequest from a JSON string
purchase_validate_before_payment_request_instance = PurchaseValidateBeforePaymentRequest.from_json(json)
# print the JSON string representation of the object
print(PurchaseValidateBeforePaymentRequest.to_json())

# convert the object into a dict
purchase_validate_before_payment_request_dict = purchase_validate_before_payment_request_instance.to_dict()
# create an instance of PurchaseValidateBeforePaymentRequest from a dict
purchase_validate_before_payment_request_from_dict = PurchaseValidateBeforePaymentRequest.from_dict(purchase_validate_before_payment_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


