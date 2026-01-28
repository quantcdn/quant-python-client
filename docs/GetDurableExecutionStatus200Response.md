# GetDurableExecutionStatus200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**request_id** | **str** |  | [optional] 
**execution_arn** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**aws_status** | **str** | Raw AWS Step Functions status | [optional] 
**callback_id** | **str** | Present when status is waiting_callback - use with /chat/callback | [optional] 
**pending_tools** | [**List[GetDurableExecutionStatus200ResponsePendingToolsInner]**](GetDurableExecutionStatus200ResponsePendingToolsInner.md) | Present when status is waiting_callback - tools waiting for results | [optional] 
**result** | [**GetDurableExecutionStatus200ResponseResult**](GetDurableExecutionStatus200ResponseResult.md) |  | [optional] 
**error** | [**GetDurableExecutionStatus200ResponseError**](GetDurableExecutionStatus200ResponseError.md) |  | [optional] 

## Example

```python
from quantcdn.models.get_durable_execution_status200_response import GetDurableExecutionStatus200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetDurableExecutionStatus200Response from a JSON string
get_durable_execution_status200_response_instance = GetDurableExecutionStatus200Response.from_json(json)
# print the JSON string representation of the object
print(GetDurableExecutionStatus200Response.to_json())

# convert the object into a dict
get_durable_execution_status200_response_dict = get_durable_execution_status200_response_instance.to_dict()
# create an instance of GetDurableExecutionStatus200Response from a dict
get_durable_execution_status200_response_from_dict = GetDurableExecutionStatus200Response.from_dict(get_durable_execution_status200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


