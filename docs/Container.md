# Container


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Name of the container | 
**image_reference** | [**ContainerImageReference**](ContainerImageReference.md) |  | 
**cpu** | **int** | Container-level CPU units | [optional] 
**memory** | **int** | Container-level memory hard limit (MiB) | [optional] 
**memory_reservation** | **int** | Container-level memory soft limit (MiB) | [optional] 
**exposed_ports** | **List[int]** | List of container ports to expose | [optional] 
**mount_points** | [**List[ContainerMountPointsInner]**](ContainerMountPointsInner.md) |  | [optional] 
**environment** | [**List[ContainerEnvironmentInner]**](ContainerEnvironmentInner.md) | Environment variables specific to this container | [optional] 
**secrets** | [**List[ContainerSecretsInner]**](ContainerSecretsInner.md) | Secrets mapped to environment variables | [optional] 
**health_check** | [**ContainerHealthCheck**](ContainerHealthCheck.md) |  | [optional] 
**depends_on** | [**List[ContainerDependsOnInner]**](ContainerDependsOnInner.md) | Container startup dependencies | [optional] 
**command** | **List[str]** |  | [optional] 
**entry_point** | **List[str]** |  | [optional] 
**working_directory** | **str** |  | [optional] 
**essential** | **bool** |  | [optional] [default to True]
**readonly_root_filesystem** | **bool** |  | [optional] [default to False]
**user** | **str** |  | [optional] 
**origin_protection** | **bool** | Enable origin protection for all exposed ports on this container. Use originProtectionConfig for advanced options like IP allow lists. | [optional] [default to False]
**origin_protection_config** | [**ContainerOriginProtectionConfig**](ContainerOriginProtectionConfig.md) |  | [optional] 

## Example

```python
from quantcdn.models.container import Container

# TODO update the JSON string below
json = "{}"
# create an instance of Container from a JSON string
container_instance = Container.from_json(json)
# print the JSON string representation of the object
print(Container.to_json())

# convert the object into a dict
container_dict = container_instance.to_dict()
# create an instance of Container from a dict
container_from_dict = Container.from_dict(container_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


