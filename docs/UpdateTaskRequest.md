# UpdateTaskRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**task_list_id** | **str** | Move task to different list or remove from list (set null) | [optional] 
**status** | **str** | Task status (triggers automatic timestamp updates) | [optional] 
**assigned_agent_id** | **str** | Reassign task to different agent | [optional] 
**depends_on** | **List[str]** | Update task dependencies | [optional] 
**metadata** | **object** | Update task metadata (replaces entire metadata object) | [optional] 
**progress** | **float** | Progress from 0.0 to 1.0 | [optional] 
**progress_message** | **str** | Human-readable progress message | [optional] 
**result** | **object** | Task result data (set when completing task) | [optional] 
**error** | **str** | Error message (set when task fails) | [optional] 
**retry_count** | **int** | Update retry count | [optional] 
**max_retries** | **int** | Update maximum retry attempts | [optional] 
**blocked_reason** | **str** | Reason task is blocked (set when status is blocked) | [optional] 
**blocked_by_task_ids** | **List[str]** | Task IDs that are blocking this task | [optional] 

## Example

```python
from quantcdn.models.update_task_request import UpdateTaskRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateTaskRequest from a JSON string
update_task_request_instance = UpdateTaskRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateTaskRequest.to_json())

# convert the object into a dict
update_task_request_dict = update_task_request_instance.to_dict()
# create an instance of UpdateTaskRequest from a dict
update_task_request_from_dict = UpdateTaskRequest.from_dict(update_task_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


