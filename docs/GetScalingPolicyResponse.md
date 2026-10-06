# GetScalingPolicyResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metric** | **str** |  | [optional] 
**target_value** | **float** |  | [optional] 
**scale_in_cooldown_seconds** | **int** |  | [optional] 
**scale_out_cooldown_seconds** | **int** |  | [optional] 
**policy_name** | **str** | Name of the underlying Application Auto Scaling policy. | [optional] 
**resource_label** | **str** | ALB ResourceLabel for RPS policies (target group identifier). | [optional] 

## Example

```python
from quantcdn.models.get_scaling_policy_response import GetScalingPolicyResponse

# TODO update the JSON string below
json = "{}"
# create an instance of GetScalingPolicyResponse from a JSON string
get_scaling_policy_response_instance = GetScalingPolicyResponse.from_json(json)
# print the JSON string representation of the object
print(GetScalingPolicyResponse.to_json())

# convert the object into a dict
get_scaling_policy_response_dict = get_scaling_policy_response_instance.to_dict()
# create an instance of GetScalingPolicyResponse from a dict
get_scaling_policy_response_from_dict = GetScalingPolicyResponse.from_dict(get_scaling_policy_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


