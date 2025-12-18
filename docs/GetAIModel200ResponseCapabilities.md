# GetAIModel200ResponseCapabilities


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**supports_tools** | **bool** |  | [optional] 
**supports_structured_output** | **bool** |  | [optional] 
**supports_multimodal** | **bool** |  | [optional] 
**supports_vision** | **bool** |  | [optional] 
**supports_streaming** | **bool** |  | [optional] 

## Example

```python
from quantcdn.models.get_ai_model200_response_capabilities import GetAIModel200ResponseCapabilities

# TODO update the JSON string below
json = "{}"
# create an instance of GetAIModel200ResponseCapabilities from a JSON string
get_ai_model200_response_capabilities_instance = GetAIModel200ResponseCapabilities.from_json(json)
# print the JSON string representation of the object
print(GetAIModel200ResponseCapabilities.to_json())

# convert the object into a dict
get_ai_model200_response_capabilities_dict = get_ai_model200_response_capabilities_instance.to_dict()
# create an instance of GetAIModel200ResponseCapabilities from a dict
get_ai_model200_response_capabilities_from_dict = GetAIModel200ResponseCapabilities.from_dict(get_ai_model200_response_capabilities_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


