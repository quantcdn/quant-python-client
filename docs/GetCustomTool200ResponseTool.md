# GetCustomTool200ResponseTool


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**edge_function_url** | **str** |  | [optional] 
**is_async** | **bool** |  | [optional] 
**input_schema** | **object** |  | [optional] 
**output_schema** | **object** |  | [optional] 
**output_schema_description** | **str** |  | [optional] 
**category** | **str** |  | [optional] 
**response_mode** | **str** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.get_custom_tool200_response_tool import GetCustomTool200ResponseTool

# TODO update the JSON string below
json = "{}"
# create an instance of GetCustomTool200ResponseTool from a JSON string
get_custom_tool200_response_tool_instance = GetCustomTool200ResponseTool.from_json(json)
# print the JSON string representation of the object
print(GetCustomTool200ResponseTool.to_json())

# convert the object into a dict
get_custom_tool200_response_tool_dict = get_custom_tool200_response_tool_instance.to_dict()
# create an instance of GetCustomTool200ResponseTool from a dict
get_custom_tool200_response_tool_from_dict = GetCustomTool200ResponseTool.from_dict(get_custom_tool200_response_tool_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


