# UpdateAISessionRequestNewMessagesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**role** | **str** |  | [optional] 
**content** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.update_ai_session_request_new_messages_inner import UpdateAISessionRequestNewMessagesInner

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateAISessionRequestNewMessagesInner from a JSON string
update_ai_session_request_new_messages_inner_instance = UpdateAISessionRequestNewMessagesInner.from_json(json)
# print the JSON string representation of the object
print(UpdateAISessionRequestNewMessagesInner.to_json())

# convert the object into a dict
update_ai_session_request_new_messages_inner_dict = update_ai_session_request_new_messages_inner_instance.to_dict()
# create an instance of UpdateAISessionRequestNewMessagesInner from a dict
update_ai_session_request_new_messages_inner_from_dict = UpdateAISessionRequestNewMessagesInner.from_dict(update_ai_session_request_new_messages_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


