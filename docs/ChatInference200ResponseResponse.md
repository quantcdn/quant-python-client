# ChatInference200ResponseResponse

Assistant's response message. May contain text content and/or tool use requests.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**role** | **str** |  | [optional] 
**content** | **str** | Text response content | [optional] 
**tool_use** | [**ChatInference200ResponseResponseToolUse**](ChatInference200ResponseResponseToolUse.md) |  | [optional] 

## Example

```python
from quantcdn.models.chat_inference200_response_response import ChatInference200ResponseResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ChatInference200ResponseResponse from a JSON string
chat_inference200_response_response_instance = ChatInference200ResponseResponse.from_json(json)
# print the JSON string representation of the object
print(ChatInference200ResponseResponse.to_json())

# convert the object into a dict
chat_inference200_response_response_dict = chat_inference200_response_response_instance.to_dict()
# create an instance of ChatInference200ResponseResponse from a dict
chat_inference200_response_response_from_dict = ChatInference200ResponseResponse.from_dict(chat_inference200_response_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


