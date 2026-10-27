# OaiChatCompletions200ResponseChoicesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**index** | **int** |  | [optional] 
**message** | [**OaiChatCompletions200ResponseChoicesInnerMessage**](OaiChatCompletions200ResponseChoicesInnerMessage.md) |  | [optional] 
**finish_reason** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.oai_chat_completions200_response_choices_inner import OaiChatCompletions200ResponseChoicesInner

# TODO update the JSON string below
json = "{}"
# create an instance of OaiChatCompletions200ResponseChoicesInner from a JSON string
oai_chat_completions200_response_choices_inner_instance = OaiChatCompletions200ResponseChoicesInner.from_json(json)
# print the JSON string representation of the object
print(OaiChatCompletions200ResponseChoicesInner.to_json())

# convert the object into a dict
oai_chat_completions200_response_choices_inner_dict = oai_chat_completions200_response_choices_inner_instance.to_dict()
# create an instance of OaiChatCompletions200ResponseChoicesInner from a dict
oai_chat_completions200_response_choices_inner_from_dict = OaiChatCompletions200ResponseChoicesInner.from_dict(oai_chat_completions200_response_choices_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


