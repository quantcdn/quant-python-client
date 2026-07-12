# OaiChatCompletionsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**model** | **str** | A model id from GET /oai/v1/models | 
**messages** | [**List[OaiChatCompletionsRequestMessagesInner]**](OaiChatCompletionsRequestMessagesInner.md) |  | 
**stream** | **bool** | Stream the response as SSE chat.completion.chunk events | [optional] [default to False]
**max_tokens** | **int** |  | [optional] 
**temperature** | **float** |  | [optional] 
**top_p** | **float** |  | [optional] 
**tools** | **List[object]** | OpenAI function tool definitions | [optional] 
**tool_choice** | **object** | auto | none | required | {type:function, function:{name}} | [optional] 
**stream_options** | **object** | {include_usage: true} to emit a final usage chunk when streaming | [optional] 

## Example

```python
from quantcdn.models.oai_chat_completions_request import OaiChatCompletionsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of OaiChatCompletionsRequest from a JSON string
oai_chat_completions_request_instance = OaiChatCompletionsRequest.from_json(json)
# print the JSON string representation of the object
print(OaiChatCompletionsRequest.to_json())

# convert the object into a dict
oai_chat_completions_request_dict = oai_chat_completions_request_instance.to_dict()
# create an instance of OaiChatCompletionsRequest from a dict
oai_chat_completions_request_from_dict = OaiChatCompletionsRequest.from_dict(oai_chat_completions_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


