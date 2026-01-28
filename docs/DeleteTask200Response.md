# DeleteTask200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**deleted** | **bool** |  | [optional] 
**deleted_count** | **int** | Number of tasks deleted (more than 1 for cascade) | [optional] 
**deleted_task_ids** | **List[str]** |  | [optional] 

## Example

```python
from quantcdn.models.delete_task200_response import DeleteTask200Response

# TODO update the JSON string below
json = "{}"
# create an instance of DeleteTask200Response from a JSON string
delete_task200_response_instance = DeleteTask200Response.from_json(json)
# print the JSON string representation of the object
print(DeleteTask200Response.to_json())

# convert the object into a dict
delete_task200_response_dict = delete_task200_response_instance.to_dict()
# create an instance of DeleteTask200Response from a dict
delete_task200_response_from_dict = DeleteTask200Response.from_dict(delete_task200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


