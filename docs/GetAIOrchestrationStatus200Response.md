# GetAIOrchestrationStatus200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**orchestration_id** | **str** | Unique orchestration identifier | 
**status** | **str** | Current orchestration status | 
**tool_count** | **int** | Total number of async tools in this orchestration | 
**completed_tools** | **int** | Number of tools that have completed | [optional] 
**synthesized_response** | **str** | AI-synthesized response combining all tool results (only present when status&#x3D;complete) | [optional] 
**tools** | [**List[GetAIOrchestrationStatus200ResponseToolsInner]**](GetAIOrchestrationStatus200ResponseToolsInner.md) | Status of individual tool executions | [optional] 
**error** | **str** | Error message (only present when status&#x3D;failed) | [optional] 
**created_at** | **datetime** | When orchestration was created | 
**completed_at** | **datetime** | When orchestration completed (if status in complete or failed) | [optional] 

## Example

```python
from quantcdn.models.get_ai_orchestration_status200_response import GetAIOrchestrationStatus200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetAIOrchestrationStatus200Response from a JSON string
get_ai_orchestration_status200_response_instance = GetAIOrchestrationStatus200Response.from_json(json)
# print the JSON string representation of the object
print(GetAIOrchestrationStatus200Response.to_json())

# convert the object into a dict
get_ai_orchestration_status200_response_dict = get_ai_orchestration_status200_response_instance.to_dict()
# create an instance of GetAIOrchestrationStatus200Response from a dict
get_ai_orchestration_status200_response_from_dict = GetAIOrchestrationStatus200Response.from_dict(get_ai_orchestration_status200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


