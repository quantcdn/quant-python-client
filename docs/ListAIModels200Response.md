# ListAIModels200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**count** | **int** |  | [optional] 
**models** | [**List[ListAIModels200ResponseModelsInner]**](ListAIModels200ResponseModelsInner.md) |  | [optional] 

## Example

```python
from quantcdn.models.list_ai_models200_response import ListAIModels200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListAIModels200Response from a JSON string
list_ai_models200_response_instance = ListAIModels200Response.from_json(json)
# print the JSON string representation of the object
print(ListAIModels200Response.to_json())

# convert the object into a dict
list_ai_models200_response_dict = list_ai_models200_response_instance.to_dict()
# create an instance of ListAIModels200Response from a dict
list_ai_models200_response_from_dict = ListAIModels200Response.from_dict(list_ai_models200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


