# UsergenItem

User-generated content or customization options associated with an asset.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**black_box** | **bool** | Black box flag indicating if the asset is a black box item. | [optional] 
**arrangeable** | **bool** | Arrangeable flag indicating if the asset can be arranged. | [optional] 
**vendor_product_type** | **str** | Vendor product type identifier. | [optional] 
**seller_id** | **int** | Seller ID for the user-generated content. | [optional] 
**authorized_performers** | **int** | Number of authorized performers for the content. | [optional] 
**content_provider** | **str** | Content provider name. | [optional] 
**adaptation_product_id** | **int** | Adaptation product ID. | [optional] 
**adaptation_vendor** | **str** | Adaptation vendor name. | [optional] 
**vendor_song_id** | **str** | Vendor song ID. | [optional] 
**commission_override_rate** | **float** | Commission override rate as a decimal. | [optional] 
**publisher_name** | **str** | Publisher name. | [optional] 
**medley_assets** | [**List[MedleyAssetItem]**](MedleyAssetItem.md) | List of medley assets included in this user-generated content. | [optional] 

## Example

```python
from hlconnect_client.models.usergen_item import UsergenItem

# TODO update the JSON string below
json = "{}"
# create an instance of UsergenItem from a JSON string
usergen_item_instance = UsergenItem.from_json(json)
# print the JSON string representation of the object
print(UsergenItem.to_json())

# convert the object into a dict
usergen_item_dict = usergen_item_instance.to_dict()
# create an instance of UsergenItem from a dict
usergen_item_from_dict = UsergenItem.from_dict(usergen_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


