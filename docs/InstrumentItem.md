# InstrumentItem

Instrument information associated with an asset.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** | Instrument type code. | [optional] 
**name** | **str** | Instrument name. | [optional] 

## Example

```python
from openapi_client.models.instrument_item import InstrumentItem

# TODO update the JSON string below
json = "{}"
# create an instance of InstrumentItem from a JSON string
instrument_item_instance = InstrumentItem.from_json(json)
# print the JSON string representation of the object
print(InstrumentItem.to_json())

# convert the object into a dict
instrument_item_dict = instrument_item_instance.to_dict()
# create an instance of InstrumentItem from a dict
instrument_item_from_dict = InstrumentItem.from_dict(instrument_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


