# CreateCustomToolRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Unique tool name (alphanumeric and underscores only) | 
**description** | **str** | Human-readable description of what the tool does | 
**edge_function_url** | **str** | HTTPS URL of the edge function | 
**input_schema** | **object** | JSON Schema defining the tool&#39;s input parameters | 
**is_async** | **bool** | Whether this tool runs asynchronously (&gt;5 seconds) | [optional] [default to False]
**timeout_seconds** | **int** | Tool execution timeout | [optional] [default to 30]

## Example

```python
from quantcdn.models.create_custom_tool_request import CreateCustomToolRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateCustomToolRequest from a JSON string
create_custom_tool_request_instance = CreateCustomToolRequest.from_json(json)
# print the JSON string representation of the object
print(CreateCustomToolRequest.to_json())

# convert the object into a dict
create_custom_tool_request_dict = create_custom_tool_request_instance.to_dict()
# create an instance of CreateCustomToolRequest from a dict
create_custom_tool_request_from_dict = CreateCustomToolRequest.from_dict(create_custom_tool_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


