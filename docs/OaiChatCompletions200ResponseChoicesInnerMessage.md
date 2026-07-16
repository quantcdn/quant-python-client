# OaiChatCompletions200ResponseChoicesInnerMessage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**role** | **str** |  | [optional] 
**content** | **str** |  | [optional] 
**tool_calls** | **List[object]** |  | [optional] 

## Example

```python
from quantcdn.models.oai_chat_completions200_response_choices_inner_message import OaiChatCompletions200ResponseChoicesInnerMessage

# TODO update the JSON string below
json = "{}"
# create an instance of OaiChatCompletions200ResponseChoicesInnerMessage from a JSON string
oai_chat_completions200_response_choices_inner_message_instance = OaiChatCompletions200ResponseChoicesInnerMessage.from_json(json)
# print the JSON string representation of the object
print(OaiChatCompletions200ResponseChoicesInnerMessage.to_json())

# convert the object into a dict
oai_chat_completions200_response_choices_inner_message_dict = oai_chat_completions200_response_choices_inner_message_instance.to_dict()
# create an instance of OaiChatCompletions200ResponseChoicesInnerMessage from a dict
oai_chat_completions200_response_choices_inner_message_from_dict = OaiChatCompletions200ResponseChoicesInnerMessage.from_dict(oai_chat_completions200_response_choices_inner_message_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


