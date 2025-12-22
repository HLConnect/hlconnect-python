# ContributorItem

Contributor information including composers, arrangers, editors, and other personnel associated with an asset.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**is_primary** | **bool** | Indicates if this is the primary contributor for the asset. | [optional] 
**name** | **str** | Name of the contributor. | [optional] 
**mbid** | **str** | MusicBrainz ID for the contributor. | [optional] 
**role** | **str** | Role of the contributor (e.g., Composer, Arranger, Editor). | [optional] 

## Example

```python
from openapi_client.models.contributor_item import ContributorItem

# TODO update the JSON string below
json = "{}"
# create an instance of ContributorItem from a JSON string
contributor_item_instance = ContributorItem.from_json(json)
# print the JSON string representation of the object
print(ContributorItem.to_json())

# convert the object into a dict
contributor_item_dict = contributor_item_instance.to_dict()
# create an instance of ContributorItem from a dict
contributor_item_from_dict = ContributorItem.from_dict(contributor_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


