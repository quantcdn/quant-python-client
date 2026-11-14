# GetAutoMode200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**auto_mode** | [**AIAutoModeConfig**](AIAutoModeConfig.md) |  | 
**eligible** | [**AIAutoModeEligibility**](AIAutoModeEligibility.md) |  | 

## Example

```python
from quantcdn.models.get_auto_mode200_response import GetAutoMode200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetAutoMode200Response from a JSON string
get_auto_mode200_response_instance = GetAutoMode200Response.from_json(json)
# print the JSON string representation of the object
print(GetAutoMode200Response.to_json())

# convert the object into a dict
get_auto_mode200_response_dict = get_auto_mode200_response_instance.to_dict()
# create an instance of GetAutoMode200Response from a dict
get_auto_mode200_response_from_dict = GetAutoMode200Response.from_dict(get_auto_mode200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


