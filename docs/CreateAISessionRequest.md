# CreateAISessionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user_id** | **str** | User identifier for this session | 
**session_group** | **str** | Optional user-defined grouping identifier (e.g., app name, environment, tenant). Use any format that makes sense for your application. | [optional] 
**metadata** | **Dict[str, object]** | Optional custom metadata for additional context | [optional] 
**expiration_minutes** | **int** | Session expiration in minutes | [optional] [default to 60]
**initial_messages** | [**List[CreateAISessionRequestInitialMessagesInner]**](CreateAISessionRequestInitialMessagesInner.md) | Initial conversation messages (e.g., system prompt) | [optional] 

## Example

```python
from quantcdn.models.create_ai_session_request import CreateAISessionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateAISessionRequest from a JSON string
create_ai_session_request_instance = CreateAISessionRequest.from_json(json)
# print the JSON string representation of the object
print(CreateAISessionRequest.to_json())

# convert the object into a dict
create_ai_session_request_dict = create_ai_session_request_instance.to_dict()
# create an instance of CreateAISessionRequest from a dict
create_ai_session_request_from_dict = CreateAISessionRequest.from_dict(create_ai_session_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


