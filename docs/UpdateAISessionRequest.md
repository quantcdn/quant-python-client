# UpdateAISessionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**new_messages** | [**List[UpdateAISessionRequestNewMessagesInner]**](UpdateAISessionRequestNewMessagesInner.md) | New messages to append to conversation | [optional] 
**tokens_used** | **int** | Tokens consumed in this turn | [optional] 
**status** | **str** | Update session status | [optional] 
**metadata** | **object** | Update custom metadata | [optional] 

## Example

```python
from quantcdn.models.update_ai_session_request import UpdateAISessionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateAISessionRequest from a JSON string
update_ai_session_request_instance = UpdateAISessionRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateAISessionRequest.to_json())

# convert the object into a dict
update_ai_session_request_dict = update_ai_session_request_instance.to_dict()
# create an instance of UpdateAISessionRequest from a dict
update_ai_session_request_from_dict = UpdateAISessionRequest.from_dict(update_ai_session_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


