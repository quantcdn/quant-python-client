# ScalingPolicy


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metric** | **str** |  | [optional] 
**target_value** | **float** |  | [optional] 
**scale_in_cooldown_seconds** | **int** |  | [optional] 
**scale_out_cooldown_seconds** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.scaling_policy import ScalingPolicy

# TODO update the JSON string below
json = "{}"
# create an instance of ScalingPolicy from a JSON string
scaling_policy_instance = ScalingPolicy.from_json(json)
# print the JSON string representation of the object
print(ScalingPolicy.to_json())

# convert the object into a dict
scaling_policy_dict = scaling_policy_instance.to_dict()
# create an instance of ScalingPolicy from a dict
scaling_policy_from_dict = ScalingPolicy.from_dict(scaling_policy_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


