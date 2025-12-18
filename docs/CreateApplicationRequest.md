# CreateApplicationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**app_name** | **str** | Application name | 
**compose_definition** | [**Compose**](Compose.md) |  | 
**min_capacity** | **int** | Minimum task count for auto-scaling | [optional] [default to 1]
**max_capacity** | **int** | Maximum task count for auto-scaling | [optional] [default to 1]
**database** | [**CreateApplicationRequestDatabase**](CreateApplicationRequestDatabase.md) |  | [optional] 
**filesystem** | [**CreateApplicationRequestFilesystem**](CreateApplicationRequestFilesystem.md) |  | [optional] 
**environment** | [**List[CreateApplicationRequestEnvironmentInner]**](CreateApplicationRequestEnvironmentInner.md) | Optional. Initial environment variables for the production environment. | [optional] 

## Example

```python
from quantcdn.models.create_application_request import CreateApplicationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateApplicationRequest from a JSON string
create_application_request_instance = CreateApplicationRequest.from_json(json)
# print the JSON string representation of the object
print(CreateApplicationRequest.to_json())

# convert the object into a dict
create_application_request_dict = create_application_request_instance.to_dict()
# create an instance of CreateApplicationRequest from a dict
create_application_request_from_dict = CreateApplicationRequest.from_dict(create_application_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


