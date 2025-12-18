# ChatInferenceRequestResponseFormat

Structured JSON output (Claude 3.5 Sonnet v1/v2, Nova Pro)

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | [optional] 
**json_schema** | **object** | JSON Schema defining expected structure | [optional] 

## Example

```python
from quantcdn.models.chat_inference_request_response_format import ChatInferenceRequestResponseFormat

# TODO update the JSON string below
json = "{}"
# create an instance of ChatInferenceRequestResponseFormat from a JSON string
chat_inference_request_response_format_instance = ChatInferenceRequestResponseFormat.from_json(json)
# print the JSON string representation of the object
print(ChatInferenceRequestResponseFormat.to_json())

# convert the object into a dict
chat_inference_request_response_format_dict = chat_inference_request_response_format_instance.to_dict()
# create an instance of ChatInferenceRequestResponseFormat from a dict
chat_inference_request_response_format_from_dict = ChatInferenceRequestResponseFormat.from_dict(chat_inference_request_response_format_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


