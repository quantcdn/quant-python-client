# SetScalingPolicyRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metric** | **str** | Metric to track for scaling. | 
**target_value** | **float** | Target value. Percentage for CPU/Memory; req/sec per task for RPS. | 
**scale_in_cooldown_seconds** | **int** | Cooldown (seconds) before another scale-in can start. | [optional] [default to 300]
**scale_out_cooldown_seconds** | **int** | Cooldown (seconds) before another scale-out can start. | [optional] [default to 60]

## Example

```python
from quantcdn.models.set_scaling_policy_request import SetScalingPolicyRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SetScalingPolicyRequest from a JSON string
set_scaling_policy_request_instance = SetScalingPolicyRequest.from_json(json)
# print the JSON string representation of the object
print(SetScalingPolicyRequest.to_json())

# convert the object into a dict
set_scaling_policy_request_dict = set_scaling_policy_request_instance.to_dict()
# create an instance of SetScalingPolicyRequest from a dict
set_scaling_policy_request_from_dict = SetScalingPolicyRequest.from_dict(set_scaling_policy_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


