# MedleyAssetItem

Medley asset information included in user-generated content.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Medley asset name. | [optional] 
**song_catalog_id** | **str** | Song catalog ID. | [optional] 
**hl_song_id** | **str** | HL song ID. | [optional] 
**sequence** | **int** | Sequence number. | [optional] 

## Example

```python
from openapi_client.models.medley_asset_item import MedleyAssetItem

# TODO update the JSON string below
json = "{}"
# create an instance of MedleyAssetItem from a JSON string
medley_asset_item_instance = MedleyAssetItem.from_json(json)
# print the JSON string representation of the object
print(MedleyAssetItem.to_json())

# convert the object into a dict
medley_asset_item_dict = medley_asset_item_instance.to_dict()
# create an instance of MedleyAssetItem from a dict
medley_asset_item_from_dict = MedleyAssetItem.from_dict(medley_asset_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


