# ChatInference202Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**request_id** | **str** | Unique request identifier for polling | 
**session_id** | **str** | Session ID for conversation continuity | [optional] 
**status** | **str** | Initial execution status | 
**message** | **str** | Human-readable status message | [optional] 
**poll_url** | **str** | URL to poll for execution status | 

## Example

```python
from quantcdn.models.chat_inference202_response import ChatInference202Response

# TODO update the JSON string below
json = "{}"
# create an instance of ChatInference202Response from a JSON string
chat_inference202_response_instance = ChatInference202Response.from_json(json)
# print the JSON string representation of the object
print(ChatInference202Response.to_json())

# convert the object into a dict
chat_inference202_response_dict = chat_inference202_response_instance.to_dict()
# create an instance of ChatInference202Response from a dict
chat_inference202_response_from_dict = ChatInference202Response.from_dict(chat_inference202_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


