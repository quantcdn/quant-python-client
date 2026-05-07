# AiSearchUpdateSettingsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**public_access** | **object** |  | [optional] 
**rate_limits** | **object** |  | [optional] 

## Example

```python
from quantcdn.models.ai_search_update_settings_request import AiSearchUpdateSettingsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AiSearchUpdateSettingsRequest from a JSON string
ai_search_update_settings_request_instance = AiSearchUpdateSettingsRequest.from_json(json)
# print the JSON string representation of the object
print(AiSearchUpdateSettingsRequest.to_json())

# convert the object into a dict
ai_search_update_settings_request_dict = ai_search_update_settings_request_instance.to_dict()
# create an instance of AiSearchUpdateSettingsRequest from a dict
ai_search_update_settings_request_from_dict = AiSearchUpdateSettingsRequest.from_dict(ai_search_update_settings_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


