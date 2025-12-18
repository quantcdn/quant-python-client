# ApplicationDeploymentInformationInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**deployment_id** | **str** | Deployment identifier | [optional] 
**task_definition_arn** | **str** | Task definition ARN used | [optional] 
**created_at** | **datetime** | Deployment creation timestamp | [optional] 
**status** | **str** | Deployment status | [optional] 
**image_tag** | **str** | Image tag deployed | [optional] 

## Example

```python
from quantcdn.models.application_deployment_information_inner import ApplicationDeploymentInformationInner

# TODO update the JSON string below
json = "{}"
# create an instance of ApplicationDeploymentInformationInner from a JSON string
application_deployment_information_inner_instance = ApplicationDeploymentInformationInner.from_json(json)
# print the JSON string representation of the object
print(ApplicationDeploymentInformationInner.to_json())

# convert the object into a dict
application_deployment_information_inner_dict = application_deployment_information_inner_instance.to_dict()
# create an instance of ApplicationDeploymentInformationInner from a dict
application_deployment_information_inner_from_dict = ApplicationDeploymentInformationInner.from_dict(application_deployment_information_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


