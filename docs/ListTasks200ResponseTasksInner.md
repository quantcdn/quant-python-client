# ListTasks200ResponseTasksInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**task_id** | **str** |  | [optional] 
**org_id** | **str** |  | [optional] 
**task_list_id** | **str** |  | [optional] 
**title** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**assigned_agent_id** | **str** |  | [optional] 
**progress** | **float** |  | [optional] 
**blocked_reason** | **str** |  | [optional] 
**blocked_by_task_ids** | **List[str]** |  | [optional] 
**created_at** | **int** |  | [optional] 
**updated_at** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.list_tasks200_response_tasks_inner import ListTasks200ResponseTasksInner

# TODO update the JSON string below
json = "{}"
# create an instance of ListTasks200ResponseTasksInner from a JSON string
list_tasks200_response_tasks_inner_instance = ListTasks200ResponseTasksInner.from_json(json)
# print the JSON string representation of the object
print(ListTasks200ResponseTasksInner.to_json())

# convert the object into a dict
list_tasks200_response_tasks_inner_dict = list_tasks200_response_tasks_inner_instance.to_dict()
# create an instance of ListTasks200ResponseTasksInner from a dict
list_tasks200_response_tasks_inner_from_dict = ListTasks200ResponseTasksInner.from_dict(list_tasks200_response_tasks_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


