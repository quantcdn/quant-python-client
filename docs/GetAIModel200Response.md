# GetAIModel200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**provider** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**context_window** | **int** |  | [optional] 
**max_output_tokens** | **int** |  | [optional] 
**capabilities** | [**GetAIModel200ResponseCapabilities**](GetAIModel200ResponseCapabilities.md) |  | [optional] 
**pricing** | [**GetAIModel200ResponsePricing**](GetAIModel200ResponsePricing.md) |  | [optional] 
**release_date** | **date** |  | [optional] 
**deprecated** | **bool** |  | [optional] 
**available** | **bool** |  | [optional] 

## Example

```python
from quantcdn.models.get_ai_model200_response import GetAIModel200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetAIModel200Response from a JSON string
get_ai_model200_response_instance = GetAIModel200Response.from_json(json)
# print the JSON string representation of the object
print(GetAIModel200Response.to_json())

# convert the object into a dict
get_ai_model200_response_dict = get_ai_model200_response_instance.to_dict()
# create an instance of GetAIModel200Response from a dict
get_ai_model200_response_from_dict = GetAIModel200Response.from_dict(get_ai_model200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


