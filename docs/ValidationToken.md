# ValidationToken

Successful validation response containing a temporary token to proceed with the payment.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**token** | **str** | Validation token | 
**exp_date** | **int** | Expiration date in UNIX timestamp format | 

## Example

```python
from hlconnect_client.models.validation_token import ValidationToken

# TODO update the JSON string below
json = "{}"
# create an instance of ValidationToken from a JSON string
validation_token_instance = ValidationToken.from_json(json)
# print the JSON string representation of the object
print(ValidationToken.to_json())

# convert the object into a dict
validation_token_dict = validation_token_instance.to_dict()
# create an instance of ValidationToken from a dict
validation_token_from_dict = ValidationToken.from_dict(validation_token_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


