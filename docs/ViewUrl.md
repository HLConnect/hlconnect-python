# ViewUrl

Secure view URL for a purchased digital asset. The URL is time-limited and can be used to view the asset online (e.g., sheet music viewer).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** | Secure, time-limited URL that can be used to view the purchased digital asset online. The URL expires after a predetermined period. | [optional] 

## Example

```python
from hlconnect_client.models.view_url import ViewUrl

# TODO update the JSON string below
json = "{}"
# create an instance of ViewUrl from a JSON string
view_url_instance = ViewUrl.from_json(json)
# print the JSON string representation of the object
print(ViewUrl.to_json())

# convert the object into a dict
view_url_dict = view_url_instance.to_dict()
# create an instance of ViewUrl from a dict
view_url_from_dict = ViewUrl.from_dict(view_url_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


