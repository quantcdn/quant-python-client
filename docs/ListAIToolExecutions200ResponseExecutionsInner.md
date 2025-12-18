# ListAIToolExecutions200ResponseExecutionsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**execution_id** | **str** |  | [optional] 
**tool_name** | **str** |  | [optional] 
**status** | **str** | Execution status: pending, running, complete, or failed | [optional] 
**created_at** | **datetime** |  | [optional] 
**completed_at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.list_ai_tool_executions200_response_executions_inner import ListAIToolExecutions200ResponseExecutionsInner

# TODO update the JSON string below
json = "{}"
# create an instance of ListAIToolExecutions200ResponseExecutionsInner from a JSON string
list_ai_tool_executions200_response_executions_inner_instance = ListAIToolExecutions200ResponseExecutionsInner.from_json(json)
# print the JSON string representation of the object
print(ListAIToolExecutions200ResponseExecutionsInner.to_json())

# convert the object into a dict
list_ai_tool_executions200_response_executions_inner_dict = list_ai_tool_executions200_response_executions_inner_instance.to_dict()
# create an instance of ListAIToolExecutions200ResponseExecutionsInner from a dict
list_ai_tool_executions200_response_executions_inner_from_dict = ListAIToolExecutions200ResponseExecutionsInner.from_dict(list_ai_tool_executions200_response_executions_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


