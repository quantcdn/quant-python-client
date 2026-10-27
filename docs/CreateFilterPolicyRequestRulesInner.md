# CreateFilterPolicyRequestRulesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**match** | [**CreateFilterPolicyRequestRulesInnerMatch**](CreateFilterPolicyRequestRulesInnerMatch.md) |  | [optional] 
**action** | **str** |  | [optional] 
**apply_to** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.create_filter_policy_request_rules_inner import CreateFilterPolicyRequestRulesInner

# TODO update the JSON string below
json = "{}"
# create an instance of CreateFilterPolicyRequestRulesInner from a JSON string
create_filter_policy_request_rules_inner_instance = CreateFilterPolicyRequestRulesInner.from_json(json)
# print the JSON string representation of the object
print(CreateFilterPolicyRequestRulesInner.to_json())

# convert the object into a dict
create_filter_policy_request_rules_inner_dict = create_filter_policy_request_rules_inner_instance.to_dict()
# create an instance of CreateFilterPolicyRequestRulesInner from a dict
create_filter_policy_request_rules_inner_from_dict = CreateFilterPolicyRequestRulesInner.from_dict(create_filter_policy_request_rules_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


