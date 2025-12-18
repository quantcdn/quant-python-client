# ListAIModels200ResponseModelsInnerCapabilities

Model capabilities and features

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **bool** | Supports text generation | [optional] 
**multimodal** | **bool** | Supports images/video | [optional] 
**embeddings** | **bool** | Supports embeddings | [optional] 
**streaming** | **bool** | Supports streaming responses | [optional] 
**tool_use** | **bool** | Supports function calling | [optional] 

## Example

```python
from quantcdn.models.list_ai_models200_response_models_inner_capabilities import ListAIModels200ResponseModelsInnerCapabilities

# TODO update the JSON string below
json = "{}"
# create an instance of ListAIModels200ResponseModelsInnerCapabilities from a JSON string
list_ai_models200_response_models_inner_capabilities_instance = ListAIModels200ResponseModelsInnerCapabilities.from_json(json)
# print the JSON string representation of the object
print(ListAIModels200ResponseModelsInnerCapabilities.to_json())

# convert the object into a dict
list_ai_models200_response_models_inner_capabilities_dict = list_ai_models200_response_models_inner_capabilities_instance.to_dict()
# create an instance of ListAIModels200ResponseModelsInnerCapabilities from a dict
list_ai_models200_response_models_inner_capabilities_from_dict = ListAIModels200ResponseModelsInnerCapabilities.from_dict(list_ai_models200_response_models_inner_capabilities_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


