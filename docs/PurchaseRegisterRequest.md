# PurchaseRegisterRequest

Request payload for registering a new purchase transaction. Contains all required information to initiate the purchase of a digital asset.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**asset_id** | **int** | Unique identifier for the digital asset to be purchased. This is Hal Leonard&#39;s internal asset ID. | 
**order_number** | **int** | Vendor-generated order number that uniquely identifies this purchase order. | 
**order_line_id** | **int** | Line number within the order that identifies this specific item. Used to distinguish multiple items in the same order. | 
**country_code** | **str** | ISO 3166-1 alpha-2 country code identifying the country of sale for the customer. | 
**line_item_price** | **float** | Price for this specific line item as a real number. Represents the total price for the quantity specified. | 
**unit_price** | **float** | Unit price for a single item as a real number | 
**quantity** | **int** | Quantity of items being purchased in this line item. | 
**customer** | **str** | Customer name for asset personalization. May be printed on the asset if personalization is supported. | 
**parts** | [**List[AssetPartForm]**](AssetPartForm.md) | Optional parts specification for ensemble assets. Allows customers to select specific parts of an ensemble for individual purchase rather than buying the complete set. | [optional] 

## Example

```python
from hlconnect_client.models.purchase_register_request import PurchaseRegisterRequest

# TODO update the JSON string below
json = "{}"
# create an instance of PurchaseRegisterRequest from a JSON string
purchase_register_request_instance = PurchaseRegisterRequest.from_json(json)
# print the JSON string representation of the object
print(PurchaseRegisterRequest.to_json())

# convert the object into a dict
purchase_register_request_dict = purchase_register_request_instance.to_dict()
# create an instance of PurchaseRegisterRequest from a dict
purchase_register_request_from_dict = PurchaseRegisterRequest.from_dict(purchase_register_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


