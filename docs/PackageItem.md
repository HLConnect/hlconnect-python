# PackageItem

Package deal or bundle that includes an asset.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**asset_id** | **int** | Asset ID included in the package. | [optional] 
**instrumentation_part_code** | **str** | Instrumentation part code. | [optional] 
**instrumentation_part_name** | **str** | Instrumentation part name. | [optional] 
**count** | **int** | Count of items. | [optional] 
**sequence** | **int** | Sequence number. | [optional] 
**score** | **bool** | Score flag indicating if this is a score. | [optional] 

## Example

```python
from openapi_client.models.package_item import PackageItem

# TODO update the JSON string below
json = "{}"
# create an instance of PackageItem from a JSON string
package_item_instance = PackageItem.from_json(json)
# print the JSON string representation of the object
print(PackageItem.to_json())

# convert the object into a dict
package_item_dict = package_item_instance.to_dict()
# create an instance of PackageItem from a dict
package_item_from_dict = PackageItem.from_dict(package_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


