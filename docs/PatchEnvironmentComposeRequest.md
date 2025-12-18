# PatchEnvironmentComposeRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**architecture** | **str** |  | [optional] 
**task_cpu** | **str** |  | [optional] 
**task_memory** | **str** |  | [optional] 
**min_capacity** | **int** |  | [optional] 
**max_capacity** | **int** |  | [optional] 
**containers** | **List[object]** |  | [optional] 
**spot_configuration** | [**PatchEnvironmentComposeRequestSpotConfiguration**](PatchEnvironmentComposeRequestSpotConfiguration.md) |  | [optional] 
**enable_cross_env_networking** | **bool** |  | [optional] 
**enable_cross_app_networking** | **bool** |  | [optional] 

## Example

```python
from quantcdn.models.patch_environment_compose_request import PatchEnvironmentComposeRequest

# TODO update the JSON string below
json = "{}"
# create an instance of PatchEnvironmentComposeRequest from a JSON string
patch_environment_compose_request_instance = PatchEnvironmentComposeRequest.from_json(json)
# print the JSON string representation of the object
print(PatchEnvironmentComposeRequest.to_json())

# convert the object into a dict
patch_environment_compose_request_dict = patch_environment_compose_request_instance.to_dict()
# create an instance of PatchEnvironmentComposeRequest from a dict
patch_environment_compose_request_from_dict = PatchEnvironmentComposeRequest.from_dict(patch_environment_compose_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


