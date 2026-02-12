# ChatInferenceStreamRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**messages** | [**List[ChatInferenceStreamRequestMessagesInner]**](ChatInferenceStreamRequestMessagesInner.md) | Array of chat messages. Content can be a simple string or an array of content blocks for multimodal input. | 
**model_id** | **str** | Model ID. Use Nova models for multimodal support. | 
**temperature** | **float** |  | [optional] [default to 0.7]
**max_tokens** | **int** | Max tokens. Claude 4.5 supports up to 64k. | [optional] [default to 4096]
**top_p** | **float** |  | [optional] 
**system_prompt** | **str** | Optional custom system prompt. When tools are enabled, this is prepended with tool usage guidance. | [optional] 
**stop_sequences** | **List[str]** | Custom stop sequences | [optional] 
**response_format** | [**ChatInferenceRequestResponseFormat**](ChatInferenceRequestResponseFormat.md) |  | [optional] 
**tool_config** | [**ChatInferenceRequestToolConfig**](ChatInferenceRequestToolConfig.md) |  | [optional] 
**session_id** | **str** | Optional session ID for conversation continuity. Omit to use stateless mode, include to continue an existing session. | [optional] 
**var_async** | **bool** | Enable async/durable execution mode. When true, returns 202 with pollUrl instead of streaming. Use for long-running inference, client-executed tools, or operations &gt;30 seconds. | [optional] [default to False]
**allowed_tools** | **List[str]** | Top-level convenience alias for toolConfig.allowedTools. Whitelists which tools can be auto-executed. | [optional] 
**guardrails** | [**ChatInferenceRequestGuardrails**](ChatInferenceRequestGuardrails.md) |  | [optional] 

## Example

```python
from quantcdn.models.chat_inference_stream_request import ChatInferenceStreamRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ChatInferenceStreamRequest from a JSON string
chat_inference_stream_request_instance = ChatInferenceStreamRequest.from_json(json)
# print the JSON string representation of the object
print(ChatInferenceStreamRequest.to_json())

# convert the object into a dict
chat_inference_stream_request_dict = chat_inference_stream_request_instance.to_dict()
# create an instance of ChatInferenceStreamRequest from a dict
chat_inference_stream_request_from_dict = ChatInferenceStreamRequest.from_dict(chat_inference_stream_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


