# CreateEnvironmentRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**env_name** | **str** | Environment name (e.g., &#39;staging&#39;, &#39;development&#39;) | 
**min_capacity** | **int** | Minimum number of instances | [optional] 
**max_capacity** | **int** | Maximum number of instances | [optional] 
**clone_configuration_from** | **str** | Clone configuration from an existing environment | [optional] 
**compose_definition** | [**Compose**](Compose.md) |  | [optional] 
**image_suffix** | **str** | Optional image tag suffix for cloning | [optional] 
**spot_configuration** | [**SpotConfiguration**](SpotConfiguration.md) |  | [optional] 
**environment** | [**List[CreateEnvironmentRequestEnvironmentInner]**](CreateEnvironmentRequestEnvironmentInner.md) | Environment variables to inject | [optional] 
**merge_environment** | **bool** | Whether to merge environment variables with cloned ones (true) or replace them (false). Default: false | [optional] 

## Example

```python
from quantcdn.models.create_environment_request import CreateEnvironmentRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateEnvironmentRequest from a JSON string
create_environment_request_instance = CreateEnvironmentRequest.from_json(json)
# print the JSON string representation of the object
print(CreateEnvironmentRequest.to_json())

# convert the object into a dict
create_environment_request_dict = create_environment_request_instance.to_dict()
# create an instance of CreateEnvironmentRequest from a dict
create_environment_request_from_dict = CreateEnvironmentRequest.from_dict(create_environment_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


