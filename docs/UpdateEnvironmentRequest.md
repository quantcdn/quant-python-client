# UpdateEnvironmentRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**compose_definition** | [**Compose**](Compose.md) |  | 
**min_capacity** | **int** | Optional. Minimum number of tasks for auto-scaling. If provided at root level, will be merged into composeDefinition. | [optional] 
**max_capacity** | **int** | Optional. Maximum number of tasks for auto-scaling. If provided at root level, will be merged into composeDefinition. | [optional] 

## Example

```python
from quantcdn.models.update_environment_request import UpdateEnvironmentRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateEnvironmentRequest from a JSON string
update_environment_request_instance = UpdateEnvironmentRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateEnvironmentRequest.to_json())

# convert the object into a dict
update_environment_request_dict = update_environment_request_instance.to_dict()
# create an instance of UpdateEnvironmentRequest from a dict
update_environment_request_from_dict = UpdateEnvironmentRequest.from_dict(update_environment_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


