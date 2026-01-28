# GetDurableExecutionStatus200ResponseResultUsage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**input_tokens** | **int** |  | [optional] 
**output_tokens** | **int** |  | [optional] 
**total_tokens** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.get_durable_execution_status200_response_result_usage import GetDurableExecutionStatus200ResponseResultUsage

# TODO update the JSON string below
json = "{}"
# create an instance of GetDurableExecutionStatus200ResponseResultUsage from a JSON string
get_durable_execution_status200_response_result_usage_instance = GetDurableExecutionStatus200ResponseResultUsage.from_json(json)
# print the JSON string representation of the object
print(GetDurableExecutionStatus200ResponseResultUsage.to_json())

# convert the object into a dict
get_durable_execution_status200_response_result_usage_dict = get_durable_execution_status200_response_result_usage_instance.to_dict()
# create an instance of GetDurableExecutionStatus200ResponseResultUsage from a dict
get_durable_execution_status200_response_result_usage_from_dict = GetDurableExecutionStatus200ResponseResultUsage.from_dict(get_durable_execution_status200_response_result_usage_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


