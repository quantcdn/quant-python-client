# ChatInference200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**response** | [**ChatInference200ResponseResponse**](ChatInference200ResponseResponse.md) |  | [optional] 
**model** | **str** | Model used for generation | [optional] 
**request_id** | **str** | Unique request identifier | [optional] 
**finish_reason** | **str** | Why the model stopped generating | [optional] 
**usage** | [**ChatInference200ResponseUsage**](ChatInference200ResponseUsage.md) |  | [optional] 

## Example

```python
from quantcdn.models.chat_inference200_response import ChatInference200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ChatInference200Response from a JSON string
chat_inference200_response_instance = ChatInference200Response.from_json(json)
# print the JSON string representation of the object
print(ChatInference200Response.to_json())

# convert the object into a dict
chat_inference200_response_dict = chat_inference200_response_instance.to_dict()
# create an instance of ChatInference200Response from a dict
chat_inference200_response_from_dict = ChatInference200Response.from_dict(chat_inference200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


