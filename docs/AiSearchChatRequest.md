# AiSearchChatRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | 
**session_id** | **str** |  | [optional] 
**context_url** | **str** |  | [optional] 
**max_context_chunks** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.ai_search_chat_request import AiSearchChatRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AiSearchChatRequest from a JSON string
ai_search_chat_request_instance = AiSearchChatRequest.from_json(json)
# print the JSON string representation of the object
print(AiSearchChatRequest.to_json())

# convert the object into a dict
ai_search_chat_request_dict = ai_search_chat_request_instance.to_dict()
# create an instance of AiSearchChatRequest from a dict
ai_search_chat_request_from_dict = AiSearchChatRequest.from_dict(ai_search_chat_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


