# GetAIToolExecutionStatus200ResponseResult

Tool execution result (only present when status='complete'). Structure varies by tool type.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**images** | **List[str]** | For image generation: Array of base64-encoded data URIs for inline display/preview | [optional] 
**s3_urls** | **List[str]** | For image generation: Array of signed S3 URLs for high-quality downloads (expire after 1 hour) | [optional] 

## Example

```python
from quantcdn.models.get_ai_tool_execution_status200_response_result import GetAIToolExecutionStatus200ResponseResult

# TODO update the JSON string below
json = "{}"
# create an instance of GetAIToolExecutionStatus200ResponseResult from a JSON string
get_ai_tool_execution_status200_response_result_instance = GetAIToolExecutionStatus200ResponseResult.from_json(json)
# print the JSON string representation of the object
print(GetAIToolExecutionStatus200ResponseResult.to_json())

# convert the object into a dict
get_ai_tool_execution_status200_response_result_dict = get_ai_tool_execution_status200_response_result_instance.to_dict()
# create an instance of GetAIToolExecutionStatus200ResponseResult from a dict
get_ai_tool_execution_status200_response_result_from_dict = GetAIToolExecutionStatus200ResponseResult.from_dict(get_ai_tool_execution_status200_response_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


