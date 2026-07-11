# Application


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**app_name** | **str** | Application name | 
**organisation** | **str** | Organisation machine name | 
**database** | [**ApplicationDatabase**](ApplicationDatabase.md) |  | [optional] 
**filesystem** | [**ApplicationFilesystem**](ApplicationFilesystem.md) |  | [optional] 
**cache** | [**ApplicationCache**](ApplicationCache.md) |  | [optional] 
**compose_definition** | [**Compose**](Compose.md) |  | [optional] 
**status** | **str** | Application status | [optional] [readonly] 
**deployment_information** | [**List[ApplicationDeploymentInformationInner]**](ApplicationDeploymentInformationInner.md) | Deployment history | [optional] [readonly] 
**image_reference** | [**ApplicationImageReference**](ApplicationImageReference.md) |  | [optional] 
**container_names** | **List[str]** | List of container names | [optional] [readonly] 
**min_capacity** | **int** | Minimum task count for auto-scaling | [optional] 
**max_capacity** | **int** | Maximum task count for auto-scaling | [optional] 
**desired_count** | **int** | Desired task count | [optional] 
**running_count** | **int** | Currently running task count | [optional] 
**environment_names** | **List[str]** | List of environment names (read-only) | [optional] [readonly] 

## Example

```python
from quantcdn.models.application import Application

# TODO update the JSON string below
json = "{}"
# create an instance of Application from a JSON string
application_instance = Application.from_json(json)
# print the JSON string representation of the object
print(Application.to_json())

# convert the object into a dict
application_dict = application_instance.to_dict()
# create an instance of Application from a dict
application_from_dict = Application.from_dict(application_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


