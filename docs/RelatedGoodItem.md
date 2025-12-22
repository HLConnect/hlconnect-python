# RelatedGoodItem

Related goods (physical products, digital bundles, etc.) associated with an asset.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**related_product_id** | **int** | Related product ID. | [optional] 
**group_type_id** | **int** | Group type ID. | [optional] 
**good_type** | **str** | Good type (H for hard goods, D for digital, V for virtual). | [optional] 
**sheet** | **bool** | Sheet indicator. | [optional] 
**featured** | **bool** | Featured indicator. | [optional] 
**prime_src** | **bool** | Prime source indicator. | [optional] 

## Example

```python
from openapi_client.models.related_good_item import RelatedGoodItem

# TODO update the JSON string below
json = "{}"
# create an instance of RelatedGoodItem from a JSON string
related_good_item_instance = RelatedGoodItem.from_json(json)
# print the JSON string representation of the object
print(RelatedGoodItem.to_json())

# convert the object into a dict
related_good_item_dict = related_good_item_instance.to_dict()
# create an instance of RelatedGoodItem from a dict
related_good_item_from_dict = RelatedGoodItem.from_dict(related_good_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


