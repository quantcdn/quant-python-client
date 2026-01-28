# GetAIOrchestrationStatus200ResponseToolsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**execution_id** | **str** |  | [optional] 
**tool_name** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**result** | **object** | Tool result (if complete) | [optional] 
**error** | **str** | Error message (if failed) | [optional] 

## Example

```python
from quantcdn.models.get_ai_orchestration_status200_response_tools_inner import GetAIOrchestrationStatus200ResponseToolsInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetAIOrchestrationStatus200ResponseToolsInner from a JSON string
get_ai_orchestration_status200_response_tools_inner_instance = GetAIOrchestrationStatus200ResponseToolsInner.from_json(json)
# print the JSON string representation of the object
print(GetAIOrchestrationStatus200ResponseToolsInner.to_json())

# convert the object into a dict
get_ai_orchestration_status200_response_tools_inner_dict = get_ai_orchestration_status200_response_tools_inner_instance.to_dict()
# create an instance of GetAIOrchestrationStatus200ResponseToolsInner from a dict
get_ai_orchestration_status200_response_tools_inner_from_dict = GetAIOrchestrationStatus200ResponseToolsInner.from_dict(get_ai_orchestration_status200_response_tools_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


