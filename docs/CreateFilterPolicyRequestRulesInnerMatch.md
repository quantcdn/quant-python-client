# CreateFilterPolicyRequestRulesInnerMatch

Match criteria

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | [optional] 
**values** | **List[str]** | Required when type&#x3D;word | [optional] 
**pattern** | **str** | Required when type&#x3D;regex | [optional] 

## Example

```python
from quantcdn.models.create_filter_policy_request_rules_inner_match import CreateFilterPolicyRequestRulesInnerMatch

# TODO update the JSON string below
json = "{}"
# create an instance of CreateFilterPolicyRequestRulesInnerMatch from a JSON string
create_filter_policy_request_rules_inner_match_instance = CreateFilterPolicyRequestRulesInnerMatch.from_json(json)
# print the JSON string representation of the object
print(CreateFilterPolicyRequestRulesInnerMatch.to_json())

# convert the object into a dict
create_filter_policy_request_rules_inner_match_dict = create_filter_policy_request_rules_inner_match_instance.to_dict()
# create an instance of CreateFilterPolicyRequestRulesInnerMatch from a dict
create_filter_policy_request_rules_inner_match_from_dict = CreateFilterPolicyRequestRulesInnerMatch.from_dict(create_filter_policy_request_rules_inner_match_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


