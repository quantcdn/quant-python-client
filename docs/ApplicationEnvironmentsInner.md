# ApplicationEnvironmentsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**env_name** | **str** | Environment name | [optional] 
**status** | **str** | Environment status | [optional] 
**running_count** | **int** | Running task count | [optional] 
**desired_count** | **int** | Desired task count | [optional] 

## Example

```python
from quantcdn.models.application_environments_inner import ApplicationEnvironmentsInner

# TODO update the JSON string below
json = "{}"
# create an instance of ApplicationEnvironmentsInner from a JSON string
application_environments_inner_instance = ApplicationEnvironmentsInner.from_json(json)
# print the JSON string representation of the object
print(ApplicationEnvironmentsInner.to_json())

# convert the object into a dict
application_environments_inner_dict = application_environments_inner_instance.to_dict()
# create an instance of ApplicationEnvironmentsInner from a dict
application_environments_inner_from_dict = ApplicationEnvironmentsInner.from_dict(application_environments_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


