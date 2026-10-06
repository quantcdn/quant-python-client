# ScalingPolicyListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**policies** | [**List[GetScalingPolicyResponse]**](GetScalingPolicyResponse.md) |  | [optional] 

## Example

```python
from quantcdn.models.scaling_policy_list_response import ScalingPolicyListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ScalingPolicyListResponse from a JSON string
scaling_policy_list_response_instance = ScalingPolicyListResponse.from_json(json)
# print the JSON string representation of the object
print(ScalingPolicyListResponse.to_json())

# convert the object into a dict
scaling_policy_list_response_dict = scaling_policy_list_response_instance.to_dict()
# create an instance of ScalingPolicyListResponse from a dict
scaling_policy_list_response_from_dict = ScalingPolicyListResponse.from_dict(scaling_policy_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


