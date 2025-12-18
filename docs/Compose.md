# Compose


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**containers** | [**List[Container]**](Container.md) |  | [optional] 
**architecture** | **str** | CPU architecture (X86_64 or ARM64) | [optional] 
**task_cpu** | **int** | Task-level CPU units (e.g., 256, 512, 1024) | [optional] 
**task_memory** | **int** | Task-level memory in MB | [optional] 
**min_capacity** | **int** | Minimum number of instances | [optional] 
**max_capacity** | **int** | Maximum number of instances | [optional] 
**spot_configuration** | [**SpotConfiguration**](SpotConfiguration.md) |  | [optional] 
**enable_cross_env_networking** | **bool** | Optional. Enable cross-environment networking within the same application. When false (default): Uses shared security group for complete isolation (most secure). When true: Uses app-specific security group to enable communication between environments of the same application (e.g., staging can connect to production database). Note: If enableCrossAppNetworking is true, this setting is overridden. | [optional] [default to False]
**enable_cross_app_networking** | **bool** | Optional. Enable cross-application networking within the same organization. When false (default): Uses shared/app-specific security group based on enableCrossEnvNetworking. When true: Uses org-specific security group to enable container-to-container communication with ALL applications in the same organization via service discovery (microservices architecture). This setting takes priority over enableCrossEnvNetworking. | [optional] [default to False]

## Example

```python
from quantcdn.models.compose import Compose

# TODO update the JSON string below
json = "{}"
# create an instance of Compose from a JSON string
compose_instance = Compose.from_json(json)
# print the JSON string representation of the object
print(Compose.to_json())

# convert the object into a dict
compose_dict = compose_instance.to_dict()
# create an instance of Compose from a dict
compose_from_dict = Compose.from_dict(compose_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


