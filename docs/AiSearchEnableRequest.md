# AiSearchEnableRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**base_url** | **str** |  | [optional] 
**crawler_config** | **object** |  | [optional] 

## Example

```python
from quantcdn.models.ai_search_enable_request import AiSearchEnableRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AiSearchEnableRequest from a JSON string
ai_search_enable_request_instance = AiSearchEnableRequest.from_json(json)
# print the JSON string representation of the object
print(AiSearchEnableRequest.to_json())

# convert the object into a dict
ai_search_enable_request_dict = ai_search_enable_request_instance.to_dict()
# create an instance of AiSearchEnableRequest from a dict
ai_search_enable_request_from_dict = AiSearchEnableRequest.from_dict(ai_search_enable_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


