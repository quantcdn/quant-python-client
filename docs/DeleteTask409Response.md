# DeleteTask409Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **str** |  | [optional] 
**message** | **str** |  | [optional] 
**dependent_task_ids** | **List[str]** |  | [optional] 

## Example

```python
from quantcdn.models.delete_task409_response import DeleteTask409Response

# TODO update the JSON string below
json = "{}"
# create an instance of DeleteTask409Response from a JSON string
delete_task409_response_instance = DeleteTask409Response.from_json(json)
# print the JSON string representation of the object
print(DeleteTask409Response.to_json())

# convert the object into a dict
delete_task409_response_dict = delete_task409_response_instance.to_dict()
# create an instance of DeleteTask409Response from a dict
delete_task409_response_from_dict = DeleteTask409Response.from_dict(delete_task409_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


