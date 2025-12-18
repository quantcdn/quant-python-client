# ListAIModels200ResponseModelsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**provider** | **str** |  | [optional] 
**capabilities** | [**ListAIModels200ResponseModelsInnerCapabilities**](ListAIModels200ResponseModelsInnerCapabilities.md) |  | [optional] 

## Example

```python
from quantcdn.models.list_ai_models200_response_models_inner import ListAIModels200ResponseModelsInner

# TODO update the JSON string below
json = "{}"
# create an instance of ListAIModels200ResponseModelsInner from a JSON string
list_ai_models200_response_models_inner_instance = ListAIModels200ResponseModelsInner.from_json(json)
# print the JSON string representation of the object
print(ListAIModels200ResponseModelsInner.to_json())

# convert the object into a dict
list_ai_models200_response_models_inner_dict = list_ai_models200_response_models_inner_instance.to_dict()
# create an instance of ListAIModels200ResponseModelsInner from a dict
list_ai_models200_response_models_inner_from_dict = ListAIModels200ResponseModelsInner.from_dict(list_ai_models200_response_models_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


