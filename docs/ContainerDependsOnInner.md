# ContainerDependsOnInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**container_name** | **str** | The name of the container this container depends on | 
**condition** | **str** | The condition to wait for on the dependency | [optional] 

## Example

```python
from quantcdn.models.container_depends_on_inner import ContainerDependsOnInner

# TODO update the JSON string below
json = "{}"
# create an instance of ContainerDependsOnInner from a JSON string
container_depends_on_inner_instance = ContainerDependsOnInner.from_json(json)
# print the JSON string representation of the object
print(ContainerDependsOnInner.to_json())

# convert the object into a dict
container_depends_on_inner_dict = container_depends_on_inner_instance.to_dict()
# create an instance of ContainerDependsOnInner from a dict
container_depends_on_inner_from_dict = ContainerDependsOnInner.from_dict(container_depends_on_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


