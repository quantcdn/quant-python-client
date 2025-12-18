# ChatInferenceRequestToolConfig

Function calling configuration (Claude 3+, Nova Pro)

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tools** | [**List[ChatInferenceRequestToolConfigToolsInner]**](ChatInferenceRequestToolConfigToolsInner.md) |  | [optional] 
**auto_execute** | **bool** | When true, backend automatically executes tools and feeds results back to AI. For async tools (e.g., image generation), returns executionId for polling. Security: Use allowedTools to whitelist which tools can auto-execute. | [optional] [default to False]
**allowed_tools** | **List[str]** | Whitelist of tool names that can be auto-executed. Required when autoExecute is true for security. Example: [&#39;get_weather&#39;, &#39;generate_image&#39;] | [optional] 

## Example

```python
from quantcdn.models.chat_inference_request_tool_config import ChatInferenceRequestToolConfig

# TODO update the JSON string below
json = "{}"
# create an instance of ChatInferenceRequestToolConfig from a JSON string
chat_inference_request_tool_config_instance = ChatInferenceRequestToolConfig.from_json(json)
# print the JSON string representation of the object
print(ChatInferenceRequestToolConfig.to_json())

# convert the object into a dict
chat_inference_request_tool_config_dict = chat_inference_request_tool_config_instance.to_dict()
# create an instance of ChatInferenceRequestToolConfig from a dict
chat_inference_request_tool_config_from_dict = ChatInferenceRequestToolConfig.from_dict(chat_inference_request_tool_config_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


