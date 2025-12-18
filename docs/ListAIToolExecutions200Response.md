# ListAIToolExecutions200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**executions** | [**List[ListAIToolExecutions200ResponseExecutionsInner]**](ListAIToolExecutions200ResponseExecutionsInner.md) |  | 
**count** | **int** | Number of executions returned | 
**org_id** | **str** | Organization identifier | 
**status** | **str** | Filter applied (or &#39;all&#39;) | [optional] 

## Example

```python
from quantcdn.models.list_ai_tool_executions200_response import ListAIToolExecutions200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListAIToolExecutions200Response from a JSON string
list_ai_tool_executions200_response_instance = ListAIToolExecutions200Response.from_json(json)
# print the JSON string representation of the object
print(ListAIToolExecutions200Response.to_json())

# convert the object into a dict
list_ai_tool_executions200_response_dict = list_ai_tool_executions200_response_instance.to_dict()
# create an instance of ListAIToolExecutions200Response from a dict
list_ai_tool_executions200_response_from_dict = ListAIToolExecutions200Response.from_dict(list_ai_tool_executions200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


