# SubmitToolCallback200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**message** | **str** |  | [optional] 
**callback_id** | **str** | Echo of the callbackId for confirmation | [optional] 

## Example

```python
from quantcdn.models.submit_tool_callback200_response import SubmitToolCallback200Response

# TODO update the JSON string below
json = "{}"
# create an instance of SubmitToolCallback200Response from a JSON string
submit_tool_callback200_response_instance = SubmitToolCallback200Response.from_json(json)
# print the JSON string representation of the object
print(SubmitToolCallback200Response.to_json())

# convert the object into a dict
submit_tool_callback200_response_dict = submit_tool_callback200_response_instance.to_dict()
# create an instance of SubmitToolCallback200Response from a dict
submit_tool_callback200_response_from_dict = SubmitToolCallback200Response.from_dict(submit_tool_callback200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


