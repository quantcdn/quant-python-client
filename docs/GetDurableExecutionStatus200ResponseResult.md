# GetDurableExecutionStatus200ResponseResult

Present when status is complete

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**response** | [**GetDurableExecutionStatus200ResponseResultResponse**](GetDurableExecutionStatus200ResponseResultResponse.md) |  | [optional] 
**usage** | [**GetDurableExecutionStatus200ResponseResultUsage**](GetDurableExecutionStatus200ResponseResultUsage.md) |  | [optional] 
**tool_executions** | **List[object]** |  | [optional] 

## Example

```python
from quantcdn.models.get_durable_execution_status200_response_result import GetDurableExecutionStatus200ResponseResult

# TODO update the JSON string below
json = "{}"
# create an instance of GetDurableExecutionStatus200ResponseResult from a JSON string
get_durable_execution_status200_response_result_instance = GetDurableExecutionStatus200ResponseResult.from_json(json)
# print the JSON string representation of the object
print(GetDurableExecutionStatus200ResponseResult.to_json())

# convert the object into a dict
get_durable_execution_status200_response_result_dict = get_durable_execution_status200_response_result_instance.to_dict()
# create an instance of GetDurableExecutionStatus200ResponseResult from a dict
get_durable_execution_status200_response_result_from_dict = GetDurableExecutionStatus200ResponseResult.from_dict(get_durable_execution_status200_response_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


