# ChatInferenceStreamRequestMessagesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**role** | **str** |  | 
**content** | [**ChatInferenceStreamRequestMessagesInnerContent**](ChatInferenceStreamRequestMessagesInnerContent.md) |  | 

## Example

```python
from quantcdn.models.chat_inference_stream_request_messages_inner import ChatInferenceStreamRequestMessagesInner

# TODO update the JSON string below
json = "{}"
# create an instance of ChatInferenceStreamRequestMessagesInner from a JSON string
chat_inference_stream_request_messages_inner_instance = ChatInferenceStreamRequestMessagesInner.from_json(json)
# print the JSON string representation of the object
print(ChatInferenceStreamRequestMessagesInner.to_json())

# convert the object into a dict
chat_inference_stream_request_messages_inner_dict = chat_inference_stream_request_messages_inner_instance.to_dict()
# create an instance of ChatInferenceStreamRequestMessagesInner from a dict
chat_inference_stream_request_messages_inner_from_dict = ChatInferenceStreamRequestMessagesInner.from_dict(chat_inference_stream_request_messages_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


