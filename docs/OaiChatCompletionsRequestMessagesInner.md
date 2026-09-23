# OaiChatCompletionsRequestMessagesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**role** | **str** |  | [optional] 
**content** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.oai_chat_completions_request_messages_inner import OaiChatCompletionsRequestMessagesInner

# TODO update the JSON string below
json = "{}"
# create an instance of OaiChatCompletionsRequestMessagesInner from a JSON string
oai_chat_completions_request_messages_inner_instance = OaiChatCompletionsRequestMessagesInner.from_json(json)
# print the JSON string representation of the object
print(OaiChatCompletionsRequestMessagesInner.to_json())

# convert the object into a dict
oai_chat_completions_request_messages_inner_dict = oai_chat_completions_request_messages_inner_instance.to_dict()
# create an instance of OaiChatCompletionsRequestMessagesInner from a dict
oai_chat_completions_request_messages_inner_from_dict = OaiChatCompletionsRequestMessagesInner.from_dict(oai_chat_completions_request_messages_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


