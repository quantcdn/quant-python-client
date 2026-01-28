# ChatWithAIAgent202Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**request_id** | **str** | Unique request identifier for polling | 
**agent_id** | **str** | The agent processing the request | 
**agent_name** | **str** | Human-readable agent name | [optional] 
**session_id** | **str** | Session ID (if provided) | [optional] 
**status** | **str** | Initial status | 
**message** | **str** |  | [optional] 
**poll_url** | **str** | URL to poll for execution status | 

## Example

```python
from quantcdn.models.chat_with_ai_agent202_response import ChatWithAIAgent202Response

# TODO update the JSON string below
json = "{}"
# create an instance of ChatWithAIAgent202Response from a JSON string
chat_with_ai_agent202_response_instance = ChatWithAIAgent202Response.from_json(json)
# print the JSON string representation of the object
print(ChatWithAIAgent202Response.to_json())

# convert the object into a dict
chat_with_ai_agent202_response_dict = chat_with_ai_agent202_response_instance.to_dict()
# create an instance of ChatWithAIAgent202Response from a dict
chat_with_ai_agent202_response_from_dict = ChatWithAIAgent202Response.from_dict(chat_with_ai_agent202_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


