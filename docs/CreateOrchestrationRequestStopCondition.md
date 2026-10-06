# CreateOrchestrationRequestStopCondition


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | [optional] [default to 'all_complete']
**max_iterations** | **int** | Max iterations (for type&#x3D;max_iterations) | [optional] 
**condition_prompt** | **str** | AI prompt to evaluate stop (for type&#x3D;condition) | [optional] 

## Example

```python
from quantcdn.models.create_orchestration_request_stop_condition import CreateOrchestrationRequestStopCondition

# TODO update the JSON string below
json = "{}"
# create an instance of CreateOrchestrationRequestStopCondition from a JSON string
create_orchestration_request_stop_condition_instance = CreateOrchestrationRequestStopCondition.from_json(json)
# print the JSON string representation of the object
print(CreateOrchestrationRequestStopCondition.to_json())

# convert the object into a dict
create_orchestration_request_stop_condition_dict = create_orchestration_request_stop_condition_instance.to_dict()
# create an instance of CreateOrchestrationRequestStopCondition from a dict
create_orchestration_request_stop_condition_from_dict = CreateOrchestrationRequestStopCondition.from_dict(create_orchestration_request_stop_condition_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


