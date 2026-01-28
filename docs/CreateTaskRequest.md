# CreateTaskRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **str** | Task title | 
**description** | **str** | Detailed task description | [optional] 
**task_list_id** | **str** | Task list ID for grouping related tasks (implicit - lists are created automatically) | [optional] 
**status** | **str** | Initial task status | [optional] [default to 'pending']
**assigned_agent_id** | **str** | Pre-assign task to specific agent | [optional] 
**created_by_agent_id** | **str** | Agent ID that created this task | [optional] 
**depends_on** | **List[str]** | Task IDs that must complete before this task can start | [optional] 
**metadata** | **object** | Flexible JSON metadata for task-specific data | [optional] 
**max_retries** | **int** | Maximum retry attempts on failure | [optional] [default to 3]
**blocked_reason** | **str** | Reason task is blocked (when status is blocked) | [optional] 
**blocked_by_task_ids** | **List[str]** | Task IDs that are blocking this task | [optional] 

## Example

```python
from quantcdn.models.create_task_request import CreateTaskRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateTaskRequest from a JSON string
create_task_request_instance = CreateTaskRequest.from_json(json)
# print the JSON string representation of the object
print(CreateTaskRequest.to_json())

# convert the object into a dict
create_task_request_dict = create_task_request_instance.to_dict()
# create an instance of CreateTaskRequest from a dict
create_task_request_from_dict = CreateTaskRequest.from_dict(create_task_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


