# ChatInference200ResponseResponseToolUseOneOfResult

Tool execution result (only present when status='complete' for sync auto-executed tools). For async tools, poll /tools/executions/{executionId}

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**images** | **List[str]** | Base64 data URIs for images | [optional] 
**s3_urls** | **List[str]** | Signed S3 URLs for downloads | [optional] 

## Example

```python
from quantcdn.models.chat_inference200_response_response_tool_use_one_of_result import ChatInference200ResponseResponseToolUseOneOfResult

# TODO update the JSON string below
json = "{}"
# create an instance of ChatInference200ResponseResponseToolUseOneOfResult from a JSON string
chat_inference200_response_response_tool_use_one_of_result_instance = ChatInference200ResponseResponseToolUseOneOfResult.from_json(json)
# print the JSON string representation of the object
print(ChatInference200ResponseResponseToolUseOneOfResult.to_json())

# convert the object into a dict
chat_inference200_response_response_tool_use_one_of_result_dict = chat_inference200_response_response_tool_use_one_of_result_instance.to_dict()
# create an instance of ChatInference200ResponseResponseToolUseOneOfResult from a dict
chat_inference200_response_response_tool_use_one_of_result_from_dict = ChatInference200ResponseResponseToolUseOneOfResult.from_dict(chat_inference200_response_response_tool_use_one_of_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


