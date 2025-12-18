# ChatWithAIAgent200ResponseResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** |  | [optional] 
**stop_reason** | **str** |  | [optional] 
**usage** | [**ChatWithAIAgent200ResponseResponseUsage**](ChatWithAIAgent200ResponseResponseUsage.md) |  | [optional] 
**tool_results** | **List[object]** |  | [optional] 

## Example

```python
from quantcdn.models.chat_with_ai_agent200_response_response import ChatWithAIAgent200ResponseResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ChatWithAIAgent200ResponseResponse from a JSON string
chat_with_ai_agent200_response_response_instance = ChatWithAIAgent200ResponseResponse.from_json(json)
# print the JSON string representation of the object
print(ChatWithAIAgent200ResponseResponse.to_json())

# convert the object into a dict
chat_with_ai_agent200_response_response_dict = chat_with_ai_agent200_response_response_instance.to_dict()
# create an instance of ChatWithAIAgent200ResponseResponse from a dict
chat_with_ai_agent200_response_response_from_dict = ChatWithAIAgent200ResponseResponse.from_dict(chat_with_ai_agent200_response_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


