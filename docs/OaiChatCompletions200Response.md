# OaiChatCompletions200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**object** | **str** |  | [optional] 
**created** | **int** |  | [optional] 
**model** | **str** |  | [optional] 
**choices** | [**List[OaiChatCompletions200ResponseChoicesInner]**](OaiChatCompletions200ResponseChoicesInner.md) |  | [optional] 
**usage** | [**OaiChatCompletions200ResponseUsage**](OaiChatCompletions200ResponseUsage.md) |  | [optional] 

## Example

```python
from quantcdn.models.oai_chat_completions200_response import OaiChatCompletions200Response

# TODO update the JSON string below
json = "{}"
# create an instance of OaiChatCompletions200Response from a JSON string
oai_chat_completions200_response_instance = OaiChatCompletions200Response.from_json(json)
# print the JSON string representation of the object
print(OaiChatCompletions200Response.to_json())

# convert the object into a dict
oai_chat_completions200_response_dict = oai_chat_completions200_response_instance.to_dict()
# create an instance of OaiChatCompletions200Response from a dict
oai_chat_completions200_response_from_dict = OaiChatCompletions200Response.from_dict(oai_chat_completions200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


