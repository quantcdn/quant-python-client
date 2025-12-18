# CreateAISessionRequestInitialMessagesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**role** | **str** |  | [optional] 
**content** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.create_ai_session_request_initial_messages_inner import CreateAISessionRequestInitialMessagesInner

# TODO update the JSON string below
json = "{}"
# create an instance of CreateAISessionRequestInitialMessagesInner from a JSON string
create_ai_session_request_initial_messages_inner_instance = CreateAISessionRequestInitialMessagesInner.from_json(json)
# print the JSON string representation of the object
print(CreateAISessionRequestInitialMessagesInner.to_json())

# convert the object into a dict
create_ai_session_request_initial_messages_inner_dict = create_ai_session_request_initial_messages_inner_instance.to_dict()
# create an instance of CreateAISessionRequestInitialMessagesInner from a dict
create_ai_session_request_initial_messages_inner_from_dict = CreateAISessionRequestInitialMessagesInner.from_dict(create_ai_session_request_initial_messages_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


