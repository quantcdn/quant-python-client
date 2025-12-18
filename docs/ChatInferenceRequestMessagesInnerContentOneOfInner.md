# ChatInferenceRequestMessagesInnerContentOneOfInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** |  | 
**image** | [**ChatInferenceRequestMessagesInnerContentOneOfInnerOneOf1Image**](ChatInferenceRequestMessagesInnerContentOneOfInnerOneOf1Image.md) |  | 
**video** | [**ChatInferenceRequestMessagesInnerContentOneOfInnerOneOf2Video**](ChatInferenceRequestMessagesInnerContentOneOfInnerOneOf2Video.md) |  | 
**document** | [**ChatInferenceRequestMessagesInnerContentOneOfInnerOneOf3Document**](ChatInferenceRequestMessagesInnerContentOneOfInnerOneOf3Document.md) |  | 

## Example

```python
from quantcdn.models.chat_inference_request_messages_inner_content_one_of_inner import ChatInferenceRequestMessagesInnerContentOneOfInner

# TODO update the JSON string below
json = "{}"
# create an instance of ChatInferenceRequestMessagesInnerContentOneOfInner from a JSON string
chat_inference_request_messages_inner_content_one_of_inner_instance = ChatInferenceRequestMessagesInnerContentOneOfInner.from_json(json)
# print the JSON string representation of the object
print(ChatInferenceRequestMessagesInnerContentOneOfInner.to_json())

# convert the object into a dict
chat_inference_request_messages_inner_content_one_of_inner_dict = chat_inference_request_messages_inner_content_one_of_inner_instance.to_dict()
# create an instance of ChatInferenceRequestMessagesInnerContentOneOfInner from a dict
chat_inference_request_messages_inner_content_one_of_inner_from_dict = ChatInferenceRequestMessagesInnerContentOneOfInner.from_dict(chat_inference_request_messages_inner_content_one_of_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


