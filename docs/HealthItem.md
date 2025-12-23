# HealthItem

Health check result for a system component. Indicates whether a specific system component is functioning properly.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Name of the system component being checked (e.g., database, cache, external service). | 
**health** | **bool** | Health status of the component. True indicates the component is functioning properly, false indicates a problem. | 

## Example

```python
from hlconnect_client.models.health_item import HealthItem

# TODO update the JSON string below
json = "{}"
# create an instance of HealthItem from a JSON string
health_item_instance = HealthItem.from_json(json)
# print the JSON string representation of the object
print(HealthItem.to_json())

# convert the object into a dict
health_item_dict = health_item_instance.to_dict()
# create an instance of HealthItem from a dict
health_item_from_dict = HealthItem.from_dict(health_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


