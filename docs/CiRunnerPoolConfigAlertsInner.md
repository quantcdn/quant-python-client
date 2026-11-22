# CiRunnerPoolConfigAlertsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** | pool_error: runner VMs failed to start, VMs reported themselves unhealthy, or a job never reached this pool&#39;s runners (detail says which). labels_unfit: a job asked for labels or an architecture this pool&#39;s runners do not have, so the pool did not take it. | [optional] 
**since** | **str** |  | [optional] 
**detail** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.ci_runner_pool_config_alerts_inner import CiRunnerPoolConfigAlertsInner

# TODO update the JSON string below
json = "{}"
# create an instance of CiRunnerPoolConfigAlertsInner from a JSON string
ci_runner_pool_config_alerts_inner_instance = CiRunnerPoolConfigAlertsInner.from_json(json)
# print the JSON string representation of the object
print(CiRunnerPoolConfigAlertsInner.to_json())

# convert the object into a dict
ci_runner_pool_config_alerts_inner_dict = ci_runner_pool_config_alerts_inner_instance.to_dict()
# create an instance of CiRunnerPoolConfigAlertsInner from a dict
ci_runner_pool_config_alerts_inner_from_dict = CiRunnerPoolConfigAlertsInner.from_dict(ci_runner_pool_config_alerts_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


