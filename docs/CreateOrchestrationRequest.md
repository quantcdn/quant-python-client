# CreateOrchestrationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Orchestration name | 
**description** | **str** | Optional description | [optional] 
**agent_id** | **str** | Agent to process items | [optional] 
**tool_id** | **str** | Tool to execute for items | [optional] 
**workflow_id** | **str** | Workflow to run for items | [optional] 
**input_source** | [**CreateOrchestrationRequestInputSource**](CreateOrchestrationRequestInputSource.md) |  | 
**batch_size** | **int** | Items per batch | [optional] [default to 10]
**concurrency** | **int** | Concurrent items within a batch | [optional] [default to 1]
**stop_condition** | [**CreateOrchestrationRequestStopCondition**](CreateOrchestrationRequestStopCondition.md) |  | [optional] 
**assigned_skills** | **List[str]** | Skill IDs to assign | [optional] 
**auto_start** | **bool** | Whether to start immediately | [optional] [default to True]

## Example

```python
from quantcdn.models.create_orchestration_request import CreateOrchestrationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateOrchestrationRequest from a JSON string
create_orchestration_request_instance = CreateOrchestrationRequest.from_json(json)
# print the JSON string representation of the object
print(CreateOrchestrationRequest.to_json())

# convert the object into a dict
create_orchestration_request_dict = create_orchestration_request_instance.to_dict()
# create an instance of CreateOrchestrationRequest from a dict
create_orchestration_request_from_dict = CreateOrchestrationRequest.from_dict(create_orchestration_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


