# ChatWithAIAgentRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** | The user&#39;s message to the agent | 
**session_id** | **str** | Optional session ID to continue a conversation | [optional] 
**user_id** | **str** | Optional user identifier for session isolation | [optional] 
**stream** | **bool** | Whether to stream the response (SSE) | [optional] [default to False]

## Example

```python
from quantcdn.models.chat_with_ai_agent_request import ChatWithAIAgentRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ChatWithAIAgentRequest from a JSON string
chat_with_ai_agent_request_instance = ChatWithAIAgentRequest.from_json(json)
# print the JSON string representation of the object
print(ChatWithAIAgentRequest.to_json())

# convert the object into a dict
chat_with_ai_agent_request_dict = chat_with_ai_agent_request_instance.to_dict()
# create an instance of ChatWithAIAgentRequest from a dict
chat_with_ai_agent_request_from_dict = ChatWithAIAgentRequest.from_dict(chat_with_ai_agent_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


