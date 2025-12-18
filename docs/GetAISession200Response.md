# GetAISession200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**title** | **str** |  | [optional] 
**model** | **str** |  | [optional] 
**messages** | **List[object]** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.get_ai_session200_response import GetAISession200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetAISession200Response from a JSON string
get_ai_session200_response_instance = GetAISession200Response.from_json(json)
# print the JSON string representation of the object
print(GetAISession200Response.to_json())

# convert the object into a dict
get_ai_session200_response_dict = get_ai_session200_response_instance.to_dict()
# create an instance of GetAISession200Response from a dict
get_ai_session200_response_from_dict = GetAISession200Response.from_dict(get_ai_session200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


