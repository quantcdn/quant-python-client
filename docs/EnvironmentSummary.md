# EnvironmentSummary

Environment summary returned in list responses

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**env_name** | **str** | Environment name | [optional] 
**status** | **str** | Environment status | [optional] 
**deployment_status** | **str** | Current deployment status | [optional] 
**running_count** | **int** | Number of running tasks | [optional] 
**desired_count** | **int** | Desired number of tasks | [optional] 
**min_capacity** | **int** | Minimum capacity for autoscaling | [optional] 
**max_capacity** | **int** | Maximum capacity for autoscaling | [optional] 

## Example

```python
from quantcdn.models.environment_summary import EnvironmentSummary

# TODO update the JSON string below
json = "{}"
# create an instance of EnvironmentSummary from a JSON string
environment_summary_instance = EnvironmentSummary.from_json(json)
# print the JSON string representation of the object
print(EnvironmentSummary.to_json())

# convert the object into a dict
environment_summary_dict = environment_summary_instance.to_dict()
# create an instance of EnvironmentSummary from a dict
environment_summary_from_dict = EnvironmentSummary.from_dict(environment_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


