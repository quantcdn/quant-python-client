# ChatInference200ResponseResponseToolUseOneOf1Inner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tool_use_id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**input** | **object** |  | [optional] 
**execution_id** | **str** | Present for async tools with autoExecute | [optional] 
**status** | **str** | Present for async tools with autoExecute | [optional] 
**result** | **object** | Present when status&#x3D;&#39;complete&#39; for sync tools | [optional] 

## Example

```python
from quantcdn.models.chat_inference200_response_response_tool_use_one_of1_inner import ChatInference200ResponseResponseToolUseOneOf1Inner

# TODO update the JSON string below
json = "{}"
# create an instance of ChatInference200ResponseResponseToolUseOneOf1Inner from a JSON string
chat_inference200_response_response_tool_use_one_of1_inner_instance = ChatInference200ResponseResponseToolUseOneOf1Inner.from_json(json)
# print the JSON string representation of the object
print(ChatInference200ResponseResponseToolUseOneOf1Inner.to_json())

# convert the object into a dict
chat_inference200_response_response_tool_use_one_of1_inner_dict = chat_inference200_response_response_tool_use_one_of1_inner_instance.to_dict()
# create an instance of ChatInference200ResponseResponseToolUseOneOf1Inner from a dict
chat_inference200_response_response_tool_use_one_of1_inner_from_dict = ChatInference200ResponseResponseToolUseOneOf1Inner.from_dict(chat_inference200_response_response_tool_use_one_of1_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


