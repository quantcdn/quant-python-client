# ChatInferenceRequestMessagesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**role** | **str** |  | 
**content** | [**ChatInferenceRequestMessagesInnerContent**](ChatInferenceRequestMessagesInnerContent.md) |  | 

## Example

```python
from quantcdn.models.chat_inference_request_messages_inner import ChatInferenceRequestMessagesInner

# TODO update the JSON string below
json = "{}"
# create an instance of ChatInferenceRequestMessagesInner from a JSON string
chat_inference_request_messages_inner_instance = ChatInferenceRequestMessagesInner.from_json(json)
# print the JSON string representation of the object
print(ChatInferenceRequestMessagesInner.to_json())

# convert the object into a dict
chat_inference_request_messages_inner_dict = chat_inference_request_messages_inner_instance.to_dict()
# create an instance of ChatInferenceRequestMessagesInner from a dict
chat_inference_request_messages_inner_from_dict = ChatInferenceRequestMessagesInner.from_dict(chat_inference_request_messages_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


