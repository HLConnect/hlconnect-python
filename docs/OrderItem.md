# OrderItem

Represents a purchase order item with complete status and fulfillment information.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**order_id** | **int** | Vendor order ID that uniquely identifies this purchase order. | [optional] 
**order_line_id** | **int** | Line number within the order that identifies this specific item. | [optional] 
**asset_id** | **int** | Unique identifier for the digital asset associated with this order item. | [optional] 
**customer** | **str** | Customer name associated with the order for personalization purposes. | [optional] 
**unit_price** | **float** | Unit price for a single item in the vendor&#39;s currency. | [optional] 
**line_item_price** | **float** | Total price for this line item (unit price × quantity) in the vendor&#39;s currency. | [optional] 
**quantity** | **float** | Quantity of items ordered in this line item. | [optional] 
**country_code** | **str** | ISO 3166-1 alpha-2 country code for the country of sale. | [optional] 
**download_url** | **str** | Secure download URL for the purchased asset. Available when the order is completed. Null if not yet fulfilled or if not applicable. | [optional] 
**view_url** | **str** | Secure view URL for the purchased asset. Available when the order is completed. Null if not yet fulfilled or if not applicable. | [optional] 
**status** | **str** | Current status of the order item (e.g., COMPLETED, PROCESSING, FAILED). | [optional] 

## Example

```python
from openapi_client.models.order_item import OrderItem

# TODO update the JSON string below
json = "{}"
# create an instance of OrderItem from a JSON string
order_item_instance = OrderItem.from_json(json)
# print the JSON string representation of the object
print(OrderItem.to_json())

# convert the object into a dict
order_item_dict = order_item_instance.to_dict()
# create an instance of OrderItem from a dict
order_item_from_dict = OrderItem.from_dict(order_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


