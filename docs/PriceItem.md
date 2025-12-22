# PriceItem

Price information for an asset in different currencies or for different customer segments.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type_id** | **int** | Price type ID. | [optional] 
**type_usage** | **str** | Price type usage (e.g., digital, print). | [optional] 
**price** | **float** | Price value. | [optional] 

## Example

```python
from openapi_client.models.price_item import PriceItem

# TODO update the JSON string below
json = "{}"
# create an instance of PriceItem from a JSON string
price_item_instance = PriceItem.from_json(json)
# print the JSON string representation of the object
print(PriceItem.to_json())

# convert the object into a dict
price_item_dict = price_item_instance.to_dict()
# create an instance of PriceItem from a dict
price_item_from_dict = PriceItem.from_dict(price_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


