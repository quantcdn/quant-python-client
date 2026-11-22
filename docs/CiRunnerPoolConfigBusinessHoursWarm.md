# CiRunnerPoolConfigBusinessHoursWarm


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | [optional] [default to False]
**timezone** | **str** |  | [optional] 
**start** | **str** | HH:MM | [optional] 
**end** | **str** | HH:MM | [optional] 

## Example

```python
from quantcdn.models.ci_runner_pool_config_business_hours_warm import CiRunnerPoolConfigBusinessHoursWarm

# TODO update the JSON string below
json = "{}"
# create an instance of CiRunnerPoolConfigBusinessHoursWarm from a JSON string
ci_runner_pool_config_business_hours_warm_instance = CiRunnerPoolConfigBusinessHoursWarm.from_json(json)
# print the JSON string representation of the object
print(CiRunnerPoolConfigBusinessHoursWarm.to_json())

# convert the object into a dict
ci_runner_pool_config_business_hours_warm_dict = ci_runner_pool_config_business_hours_warm_instance.to_dict()
# create an instance of CiRunnerPoolConfigBusinessHoursWarm from a dict
ci_runner_pool_config_business_hours_warm_from_dict = CiRunnerPoolConfigBusinessHoursWarm.from_dict(ci_runner_pool_config_business_hours_warm_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


