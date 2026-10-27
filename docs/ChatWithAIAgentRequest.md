# ChatWithAIAgentRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** | The user&#39;s message to the agent | 
**session_id** | **str** | Optional session ID to continue a conversation | [optional] 
**user_id** | **str** | Ignored by the API since 4.28.0; the portal sets the requester. | [optional] 
**allowed_collections** | **List[str]** | Ignored by the API since 4.28.0; the portal sets the requester. | [optional] 
**stream** | **bool** | Whether to stream the response (SSE) | [optional] [default to False]
**var_async** | **bool** | Enable async/durable execution mode. When true, returns 202 with pollUrl. Use for long-running agent tasks. | [optional] [default to False]
**system** | **str** | Optional additional system prompt (appended to agent&#39;s configured prompt) | [optional] 
**long_context** | **bool** | Per-request override to force 1M context window routing | [optional] [default to False]
**proposal_ids** | **List[str]** | Tool approval proposal ids this turn relates to. Forwarded unchanged. | [optional] 
**client_session_id** | **str** | Client session id used to scope tool approval grants. Forwarded unchanged. | [optional] 
**max_tool_iterations** | **int** | Maximum tool auto-execution iterations for this request | [optional] 

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


