# SubmitToolCallbackRequestToolResultsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tool_use_id** | **str** | The toolUseId from pendingTools | 
**result** | **object** | The result of executing the tool | 

## Example

```python
from quantcdn.models.submit_tool_callback_request_tool_results_inner import SubmitToolCallbackRequestToolResultsInner

# TODO update the JSON string below
json = "{}"
# create an instance of SubmitToolCallbackRequestToolResultsInner from a JSON string
submit_tool_callback_request_tool_results_inner_instance = SubmitToolCallbackRequestToolResultsInner.from_json(json)
# print the JSON string representation of the object
print(SubmitToolCallbackRequestToolResultsInner.to_json())

# convert the object into a dict
submit_tool_callback_request_tool_results_inner_dict = submit_tool_callback_request_tool_results_inner_instance.to_dict()
# create an instance of SubmitToolCallbackRequestToolResultsInner from a dict
submit_tool_callback_request_tool_results_inner_from_dict = SubmitToolCallbackRequestToolResultsInner.from_dict(submit_tool_callback_request_tool_results_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


