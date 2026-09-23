# OaiChatCompletions200ResponseUsage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**prompt_tokens** | **int** |  | [optional] 
**completion_tokens** | **int** |  | [optional] 
**total_tokens** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.oai_chat_completions200_response_usage import OaiChatCompletions200ResponseUsage

# TODO update the JSON string below
json = "{}"
# create an instance of OaiChatCompletions200ResponseUsage from a JSON string
oai_chat_completions200_response_usage_instance = OaiChatCompletions200ResponseUsage.from_json(json)
# print the JSON string representation of the object
print(OaiChatCompletions200ResponseUsage.to_json())

# convert the object into a dict
oai_chat_completions200_response_usage_dict = oai_chat_completions200_response_usage_instance.to_dict()
# create an instance of OaiChatCompletions200ResponseUsage from a dict
oai_chat_completions200_response_usage_from_dict = OaiChatCompletions200ResponseUsage.from_dict(oai_chat_completions200_response_usage_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


