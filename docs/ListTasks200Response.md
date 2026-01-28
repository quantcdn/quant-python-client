# ListTasks200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tasks** | [**List[ListTasks200ResponseTasksInner]**](ListTasks200ResponseTasksInner.md) |  | [optional] 
**task_ids** | **List[str]** | Task IDs (only with dependsOn filter) | [optional] 
**count** | **int** |  | [optional] 
**depends_on** | **str** | The queried task ID (only with dependsOn filter) | [optional] 

## Example

```python
from quantcdn.models.list_tasks200_response import ListTasks200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListTasks200Response from a JSON string
list_tasks200_response_instance = ListTasks200Response.from_json(json)
# print the JSON string representation of the object
print(ListTasks200Response.to_json())

# convert the object into a dict
list_tasks200_response_dict = list_tasks200_response_instance.to_dict()
# create an instance of ListTasks200Response from a dict
list_tasks200_response_from_dict = ListTasks200Response.from_dict(list_tasks200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


