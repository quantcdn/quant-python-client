# ChatInference200ResponseResponseToolUse

Tool use request(s). Can be a single object or array of objects. Only present when AI requests tools.

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
from quantcdn.models.chat_inference200_response_response_tool_use import ChatInference200ResponseResponseToolUse

# TODO update the JSON string below
json = "{}"
# create an instance of ChatInference200ResponseResponseToolUse from a JSON string
chat_inference200_response_response_tool_use_instance = ChatInference200ResponseResponseToolUse.from_json(json)
# print the JSON string representation of the object
print(ChatInference200ResponseResponseToolUse.to_json())

# convert the object into a dict
chat_inference200_response_response_tool_use_dict = chat_inference200_response_response_tool_use_instance.to_dict()
# create an instance of ChatInference200ResponseResponseToolUse from a dict
chat_inference200_response_response_tool_use_from_dict = ChatInference200ResponseResponseToolUse.from_dict(chat_inference200_response_response_tool_use_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


