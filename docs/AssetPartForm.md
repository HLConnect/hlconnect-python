# AssetPartForm

Specification for an individual part of an ensemble asset. Used when purchasing specific parts of an ensemble rather than the complete set.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**asset_id** | **int** | Unique identifier for the specific part asset. This is Hal Leonard&#39;s internal asset ID for the individual part. | 
**order_line_id** | **int** | The vendor line number that identifies this specific part within the order. Used to distinguish multiple parts in the same order. | 

## Example

```python
from hlconnect_client.models.asset_part_form import AssetPartForm

# TODO update the JSON string below
json = "{}"
# create an instance of AssetPartForm from a JSON string
asset_part_form_instance = AssetPartForm.from_json(json)
# print the JSON string representation of the object
print(AssetPartForm.to_json())

# convert the object into a dict
asset_part_form_dict = asset_part_form_instance.to_dict()
# create an instance of AssetPartForm from a dict
asset_part_form_from_dict = AssetPartForm.from_dict(asset_part_form_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


