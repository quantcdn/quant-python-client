# UpdateFilterPolicyRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**enabled** | **bool** |  | [optional] 
**rules** | [**List[CreateFilterPolicyRequestRulesInner]**](CreateFilterPolicyRequestRulesInner.md) |  | [optional] 

## Example

```python
from quantcdn.models.update_filter_policy_request import UpdateFilterPolicyRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateFilterPolicyRequest from a JSON string
update_filter_policy_request_instance = UpdateFilterPolicyRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateFilterPolicyRequest.to_json())

# convert the object into a dict
update_filter_policy_request_dict = update_filter_policy_request_instance.to_dict()
# create an instance of UpdateFilterPolicyRequest from a dict
update_filter_policy_request_from_dict = UpdateFilterPolicyRequest.from_dict(update_filter_policy_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


