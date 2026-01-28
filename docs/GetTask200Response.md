# GetTask200Response


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
**created_by_agent_id** | **str** |  | [optional] 
**depends_on** | **List[str]** |  | [optional] 
**metadata** | **object** |  | [optional] 
**progress** | **float** |  | [optional] 
**progress_message** | **str** |  | [optional] 
**result** | **object** | Task result data when completed | [optional] 
**error** | **str** | Error message if status is failed | [optional] 
**retry_count** | **int** |  | [optional] 
**max_retries** | **int** |  | [optional] 
**created_at** | **int** | Unix timestamp in milliseconds | [optional] 
**updated_at** | **int** | Unix timestamp in milliseconds | [optional] 
**started_at** | **int** | When status changed to in_progress | [optional] 
**completed_at** | **int** | When task completed/failed/cancelled | [optional] 
**expires_at** | **int** | TTL timestamp for completed tasks | [optional] 
**blocked_reason** | **str** | Reason task is blocked | [optional] 
**blocked_by_task_ids** | **List[str]** | Task IDs that are blocking this task | [optional] 
**blocked_at** | **int** | When status changed to blocked | [optional] 

## Example

```python
from quantcdn.models.get_task200_response import GetTask200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetTask200Response from a JSON string
get_task200_response_instance = GetTask200Response.from_json(json)
# print the JSON string representation of the object
print(GetTask200Response.to_json())

# convert the object into a dict
get_task200_response_dict = get_task200_response_instance.to_dict()
# create an instance of GetTask200Response from a dict
get_task200_response_from_dict = GetTask200Response.from_dict(get_task200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


