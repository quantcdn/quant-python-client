# ListAIToolNames200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tools** | **List[str]** | Array of tool names | 
**count** | **int** | Number of tools | 

## Example

```python
from quantcdn.models.list_ai_tool_names200_response import ListAIToolNames200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListAIToolNames200Response from a JSON string
list_ai_tool_names200_response_instance = ListAIToolNames200Response.from_json(json)
# print the JSON string representation of the object
print(ListAIToolNames200Response.to_json())

# convert the object into a dict
list_ai_tool_names200_response_dict = list_ai_tool_names200_response_instance.to_dict()
# create an instance of ListAIToolNames200Response from a dict
list_ai_tool_names200_response_from_dict = ListAIToolNames200Response.from_dict(list_ai_tool_names200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


