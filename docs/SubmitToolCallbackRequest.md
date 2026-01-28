# SubmitToolCallbackRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**callback_id** | **str** | The callbackId from the waiting_callback status response | 
**tool_results** | [**List[SubmitToolCallbackRequestToolResultsInner]**](SubmitToolCallbackRequestToolResultsInner.md) | Results of client-executed tools | 

## Example

```python
from quantcdn.models.submit_tool_callback_request import SubmitToolCallbackRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SubmitToolCallbackRequest from a JSON string
submit_tool_callback_request_instance = SubmitToolCallbackRequest.from_json(json)
# print the JSON string representation of the object
print(SubmitToolCallbackRequest.to_json())

# convert the object into a dict
submit_tool_callback_request_dict = submit_tool_callback_request_instance.to_dict()
# create an instance of SubmitToolCallbackRequest from a dict
submit_tool_callback_request_from_dict = SubmitToolCallbackRequest.from_dict(submit_tool_callback_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


