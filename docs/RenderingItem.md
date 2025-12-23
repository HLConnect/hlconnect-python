# RenderingItem

Available renderings (formats) for an asset (e.g., PDF, Scorch, MusicXML).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** | Rendering type (pdf, scorch, musicxml, embed, audio, streaming). | [optional] 
**usage** | **str** | Rendering usage (full or preview). | [optional] 

## Example

```python
from hlconnect_client.models.rendering_item import RenderingItem

# TODO update the JSON string below
json = "{}"
# create an instance of RenderingItem from a JSON string
rendering_item_instance = RenderingItem.from_json(json)
# print the JSON string representation of the object
print(RenderingItem.to_json())

# convert the object into a dict
rendering_item_dict = rendering_item_instance.to_dict()
# create an instance of RenderingItem from a dict
rendering_item_from_dict = RenderingItem.from_dict(rendering_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


