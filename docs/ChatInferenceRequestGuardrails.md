# ChatInferenceRequestGuardrails

AWS Bedrock guardrails configuration for content filtering and safety.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**guardrail_identifier** | **str** | Guardrail identifier from AWS Bedrock | [optional] 
**guardrail_version** | **str** | Guardrail version | [optional] 
**trace** | **str** | Enable guardrail trace output | [optional] 

## Example

```python
from quantcdn.models.chat_inference_request_guardrails import ChatInferenceRequestGuardrails

# TODO update the JSON string below
json = "{}"
# create an instance of ChatInferenceRequestGuardrails from a JSON string
chat_inference_request_guardrails_instance = ChatInferenceRequestGuardrails.from_json(json)
# print the JSON string representation of the object
print(ChatInferenceRequestGuardrails.to_json())

# convert the object into a dict
chat_inference_request_guardrails_dict = chat_inference_request_guardrails_instance.to_dict()
# create an instance of ChatInferenceRequestGuardrails from a dict
chat_inference_request_guardrails_from_dict = ChatInferenceRequestGuardrails.from_dict(chat_inference_request_guardrails_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


