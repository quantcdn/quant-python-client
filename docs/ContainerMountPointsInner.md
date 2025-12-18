# ContainerMountPointsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**source_volume** | **str** | The name of the logical volume | 
**container_path** | **str** | The path inside the container where the volume is mounted | 
**read_only** | **bool** |  | [optional] [default to False]

## Example

```python
from quantcdn.models.container_mount_points_inner import ContainerMountPointsInner

# TODO update the JSON string below
json = "{}"
# create an instance of ContainerMountPointsInner from a JSON string
container_mount_points_inner_instance = ContainerMountPointsInner.from_json(json)
# print the JSON string representation of the object
print(ContainerMountPointsInner.to_json())

# convert the object into a dict
container_mount_points_inner_dict = container_mount_points_inner_instance.to_dict()
# create an instance of ContainerMountPointsInner from a dict
container_mount_points_inner_from_dict = ContainerMountPointsInner.from_dict(container_mount_points_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


