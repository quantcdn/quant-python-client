# GetDurableExecutionStatus200ResponseError

Present when status is failed

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error_message** | **str** |  | [optional] 
**error_type** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.get_durable_execution_status200_response_error import GetDurableExecutionStatus200ResponseError

# TODO update the JSON string below
json = "{}"
# create an instance of GetDurableExecutionStatus200ResponseError from a JSON string
get_durable_execution_status200_response_error_instance = GetDurableExecutionStatus200ResponseError.from_json(json)
# print the JSON string representation of the object
print(GetDurableExecutionStatus200ResponseError.to_json())

# convert the object into a dict
get_durable_execution_status200_response_error_dict = get_durable_execution_status200_response_error_instance.to_dict()
# create an instance of GetDurableExecutionStatus200ResponseError from a dict
get_durable_execution_status200_response_error_from_dict = GetDurableExecutionStatus200ResponseError.from_dict(get_durable_execution_status200_response_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


