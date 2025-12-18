# PatchEnvironmentCompose202Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**architecture** | **str** |  | [optional] 
**task_cpu** | **str** |  | [optional] 
**task_memory** | **str** |  | [optional] 
**min_capacity** | **int** |  | [optional] 
**max_capacity** | **int** |  | [optional] 
**containers** | **List[object]** |  | [optional] 
**spot_configuration** | [**PatchEnvironmentCompose202ResponseSpotConfiguration**](PatchEnvironmentCompose202ResponseSpotConfiguration.md) |  | [optional] 
**enable_cross_env_networking** | **bool** |  | [optional] 
**enable_cross_app_networking** | **bool** |  | [optional] 

## Example

```python
from quantcdn.models.patch_environment_compose202_response import PatchEnvironmentCompose202Response

# TODO update the JSON string below
json = "{}"
# create an instance of PatchEnvironmentCompose202Response from a JSON string
patch_environment_compose202_response_instance = PatchEnvironmentCompose202Response.from_json(json)
# print the JSON string representation of the object
print(PatchEnvironmentCompose202Response.to_json())

# convert the object into a dict
patch_environment_compose202_response_dict = patch_environment_compose202_response_instance.to_dict()
# create an instance of PatchEnvironmentCompose202Response from a dict
patch_environment_compose202_response_from_dict = PatchEnvironmentCompose202Response.from_dict(patch_environment_compose202_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


