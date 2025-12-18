# GetAIUsageStats200ResponseByModelValue


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**requests** | **int** | Number of requests for this model | [optional] 
**tokens** | **int** | Total tokens for this model | [optional] 

## Example

```python
from quantcdn.models.get_ai_usage_stats200_response_by_model_value import GetAIUsageStats200ResponseByModelValue

# TODO update the JSON string below
json = "{}"
# create an instance of GetAIUsageStats200ResponseByModelValue from a JSON string
get_ai_usage_stats200_response_by_model_value_instance = GetAIUsageStats200ResponseByModelValue.from_json(json)
# print the JSON string representation of the object
print(GetAIUsageStats200ResponseByModelValue.to_json())

# convert the object into a dict
get_ai_usage_stats200_response_by_model_value_dict = get_ai_usage_stats200_response_by_model_value_instance.to_dict()
# create an instance of GetAIUsageStats200ResponseByModelValue from a dict
get_ai_usage_stats200_response_by_model_value_from_dict = GetAIUsageStats200ResponseByModelValue.from_dict(get_ai_usage_stats200_response_by_model_value_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


