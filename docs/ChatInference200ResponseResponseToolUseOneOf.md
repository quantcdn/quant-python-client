# ChatInference200ResponseResponseToolUseOneOf

Single tool request

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tool_use_id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**input** | **object** |  | [optional] 
**execution_id** | **str** | Present for async tools with autoExecute | [optional] 
**status** | **str** | Execution status (pending/running/complete/failed) - present for async tools with autoExecute | [optional] 
**result** | [**ChatInference200ResponseResponseToolUseOneOfResult**](ChatInference200ResponseResponseToolUseOneOfResult.md) |  | [optional] 

## Example

```python
from quantcdn.models.chat_inference200_response_response_tool_use_one_of import ChatInference200ResponseResponseToolUseOneOf

# TODO update the JSON string below
json = "{}"
# create an instance of ChatInference200ResponseResponseToolUseOneOf from a JSON string
chat_inference200_response_response_tool_use_one_of_instance = ChatInference200ResponseResponseToolUseOneOf.from_json(json)
# print the JSON string representation of the object
print(ChatInference200ResponseResponseToolUseOneOf.to_json())

# convert the object into a dict
chat_inference200_response_response_tool_use_one_of_dict = chat_inference200_response_response_tool_use_one_of_instance.to_dict()
# create an instance of ChatInference200ResponseResponseToolUseOneOf from a dict
chat_inference200_response_response_tool_use_one_of_from_dict = ChatInference200ResponseResponseToolUseOneOf.from_dict(chat_inference200_response_response_tool_use_one_of_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


