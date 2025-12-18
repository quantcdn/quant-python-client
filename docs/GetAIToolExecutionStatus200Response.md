# GetAIToolExecutionStatus200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**execution_id** | **str** |  | 
**tool_name** | **str** |  | 
**status** | **str** | Execution status: pending, running, complete, or failed | 
**result** | [**GetAIToolExecutionStatus200ResponseResult**](GetAIToolExecutionStatus200ResponseResult.md) |  | [optional] 
**error** | **str** | Error message (only present when status&#x3D;&#39;failed&#39;) | [optional] 
**created_at** | **int** | Unix timestamp when execution was created | 
**started_at** | **int** | Unix timestamp when execution started (if status &gt;&#x3D; &#39;running&#39;) | [optional] 
**completed_at** | **int** | Unix timestamp when execution completed (if status in [&#39;complete&#39;, &#39;failed&#39;]) | [optional] 
**duration** | **float** | Execution duration in seconds (if completed) | [optional] 

## Example

```python
from quantcdn.models.get_ai_tool_execution_status200_response import GetAIToolExecutionStatus200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetAIToolExecutionStatus200Response from a JSON string
get_ai_tool_execution_status200_response_instance = GetAIToolExecutionStatus200Response.from_json(json)
# print the JSON string representation of the object
print(GetAIToolExecutionStatus200Response.to_json())

# convert the object into a dict
get_ai_tool_execution_status200_response_dict = get_ai_tool_execution_status200_response_instance.to_dict()
# create an instance of GetAIToolExecutionStatus200Response from a dict
get_ai_tool_execution_status200_response_from_dict = GetAIToolExecutionStatus200Response.from_dict(get_ai_tool_execution_status200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


