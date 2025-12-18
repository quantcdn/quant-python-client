# ContainerEnvironmentInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Environment variable name | 
**value** | **str** | Environment variable value | 

## Example

```python
from quantcdn.models.container_environment_inner import ContainerEnvironmentInner

# TODO update the JSON string below
json = "{}"
# create an instance of ContainerEnvironmentInner from a JSON string
container_environment_inner_instance = ContainerEnvironmentInner.from_json(json)
# print the JSON string representation of the object
print(ContainerEnvironmentInner.to_json())

# convert the object into a dict
container_environment_inner_dict = container_environment_inner_instance.to_dict()
# create an instance of ContainerEnvironmentInner from a dict
container_environment_inner_from_dict = ContainerEnvironmentInner.from_dict(container_environment_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


