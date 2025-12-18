# ChatInferenceRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**messages** | [**List[ChatInferenceRequestMessagesInner]**](ChatInferenceRequestMessagesInner.md) | Array of chat messages. Content can be a simple string or an array of content blocks for multimodal input. | 
**model_id** | **str** | Model ID. Use Nova models for multimodal support. | 
**temperature** | **float** |  | [optional] [default to 0.7]
**max_tokens** | **int** |  | [optional] [default to 1024]
**top_p** | **float** |  | [optional] 
**stream** | **bool** | Ignored in buffered mode, always returns complete response | [optional] 
**system_prompt** | **str** | Optional custom system prompt. When tools are enabled, this is prepended with tool usage guidance. | [optional] 
**stop_sequences** | **List[str]** | Custom stop sequences | [optional] 
**response_format** | [**ChatInferenceRequestResponseFormat**](ChatInferenceRequestResponseFormat.md) |  | [optional] 
**tool_config** | [**ChatInferenceRequestToolConfig**](ChatInferenceRequestToolConfig.md) |  | [optional] 

## Example

```python
from quantcdn.models.chat_inference_request import ChatInferenceRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ChatInferenceRequest from a JSON string
chat_inference_request_instance = ChatInferenceRequest.from_json(json)
# print the JSON string representation of the object
print(ChatInferenceRequest.to_json())

# convert the object into a dict
chat_inference_request_dict = chat_inference_request_instance.to_dict()
# create an instance of ChatInferenceRequest from a dict
chat_inference_request_from_dict = ChatInferenceRequest.from_dict(chat_inference_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


