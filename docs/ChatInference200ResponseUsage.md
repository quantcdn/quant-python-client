# ChatInference200ResponseUsage

Token usage information

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**input_tokens** | **int** | Number of input tokens | [optional] 
**output_tokens** | **int** | Number of output tokens | [optional] 
**total_tokens** | **int** | Total tokens consumed | [optional] 

## Example

```python
from quantcdn.models.chat_inference200_response_usage import ChatInference200ResponseUsage

# TODO update the JSON string below
json = "{}"
# create an instance of ChatInference200ResponseUsage from a JSON string
chat_inference200_response_usage_instance = ChatInference200ResponseUsage.from_json(json)
# print the JSON string representation of the object
print(ChatInference200ResponseUsage.to_json())

# convert the object into a dict
chat_inference200_response_usage_dict = chat_inference200_response_usage_instance.to_dict()
# create an instance of ChatInference200ResponseUsage from a dict
chat_inference200_response_usage_from_dict = ChatInference200ResponseUsage.from_dict(chat_inference200_response_usage_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


