# ExtendAISessionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**additional_minutes** | **int** | Minutes to add to expiration time (default 60, max 1440) | [optional] [default to 60]

## Example

```python
from quantcdn.models.extend_ai_session_request import ExtendAISessionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ExtendAISessionRequest from a JSON string
extend_ai_session_request_instance = ExtendAISessionRequest.from_json(json)
# print the JSON string representation of the object
print(ExtendAISessionRequest.to_json())

# convert the object into a dict
extend_ai_session_request_dict = extend_ai_session_request_instance.to_dict()
# create an instance of ExtendAISessionRequest from a dict
extend_ai_session_request_from_dict = ExtendAISessionRequest.from_dict(extend_ai_session_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


