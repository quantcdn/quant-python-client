# ChatInferenceRequestAutoExecute

Top-level alias for toolConfig.autoExecute. true runs every allowed tool on the AI API; an array names the tools the AI API runs, and the others come back as tool_request.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------

## Example

```python
from quantcdn.models.chat_inference_request_auto_execute import ChatInferenceRequestAutoExecute

# TODO update the JSON string below
json = "{}"
# create an instance of ChatInferenceRequestAutoExecute from a JSON string
chat_inference_request_auto_execute_instance = ChatInferenceRequestAutoExecute.from_json(json)
# print the JSON string representation of the object
print(ChatInferenceRequestAutoExecute.to_json())

# convert the object into a dict
chat_inference_request_auto_execute_dict = chat_inference_request_auto_execute_instance.to_dict()
# create an instance of ChatInferenceRequestAutoExecute from a dict
chat_inference_request_auto_execute_from_dict = ChatInferenceRequestAutoExecute.from_dict(chat_inference_request_auto_execute_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


