# GetAIUsageStats200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_requests** | **int** | Total number of API requests | [optional] 
**total_tokens** | **int** | Total tokens consumed across all requests | [optional] 
**by_model** | [**Dict[str, GetAIUsageStats200ResponseByModelValue]**](GetAIUsageStats200ResponseByModelValue.md) | Usage breakdown by model ID | [optional] 

## Example

```python
from quantcdn.models.get_ai_usage_stats200_response import GetAIUsageStats200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetAIUsageStats200Response from a JSON string
get_ai_usage_stats200_response_instance = GetAIUsageStats200Response.from_json(json)
# print the JSON string representation of the object
print(GetAIUsageStats200Response.to_json())

# convert the object into a dict
get_ai_usage_stats200_response_dict = get_ai_usage_stats200_response_instance.to_dict()
# create an instance of GetAIUsageStats200Response from a dict
get_ai_usage_stats200_response_from_dict = GetAIUsageStats200Response.from_dict(get_ai_usage_stats200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


