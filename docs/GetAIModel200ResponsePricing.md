# GetAIModel200ResponsePricing


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**input_per_m_token** | **float** |  | [optional] 
**output_per_m_token** | **float** |  | [optional] 
**currency** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.get_ai_model200_response_pricing import GetAIModel200ResponsePricing

# TODO update the JSON string below
json = "{}"
# create an instance of GetAIModel200ResponsePricing from a JSON string
get_ai_model200_response_pricing_instance = GetAIModel200ResponsePricing.from_json(json)
# print the JSON string representation of the object
print(GetAIModel200ResponsePricing.to_json())

# convert the object into a dict
get_ai_model200_response_pricing_dict = get_ai_model200_response_pricing_instance.to_dict()
# create an instance of GetAIModel200ResponsePricing from a dict
get_ai_model200_response_pricing_from_dict = GetAIModel200ResponsePricing.from_dict(get_ai_model200_response_pricing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


