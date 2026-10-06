# CreateOrchestrationRequestInputSource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** | Input source type (api type not yet supported) | 
**items** | **List[object]** | Static items (for type&#x3D;static) | [optional] 
**task_query** | **object** | Task query filters (for type&#x3D;task_query) | [optional] 
**generator_prompt** | **str** | AI prompt (for type&#x3D;generator) | [optional] 

## Example

```python
from quantcdn.models.create_orchestration_request_input_source import CreateOrchestrationRequestInputSource

# TODO update the JSON string below
json = "{}"
# create an instance of CreateOrchestrationRequestInputSource from a JSON string
create_orchestration_request_input_source_instance = CreateOrchestrationRequestInputSource.from_json(json)
# print the JSON string representation of the object
print(CreateOrchestrationRequestInputSource.to_json())

# convert the object into a dict
create_orchestration_request_input_source_dict = create_orchestration_request_input_source_instance.to_dict()
# create an instance of CreateOrchestrationRequestInputSource from a dict
create_orchestration_request_input_source_from_dict = CreateOrchestrationRequestInputSource.from_dict(create_orchestration_request_input_source_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


