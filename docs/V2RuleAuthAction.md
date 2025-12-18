# V2RuleAuthAction


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**auth_user** | **str** | Authentication username | 
**auth_pass** | **str** | Authentication password | 

## Example

```python
from quantcdn.models.v2_rule_auth_action import V2RuleAuthAction

# TODO update the JSON string below
json = "{}"
# create an instance of V2RuleAuthAction from a JSON string
v2_rule_auth_action_instance = V2RuleAuthAction.from_json(json)
# print the JSON string representation of the object
print(V2RuleAuthAction.to_json())

# convert the object into a dict
v2_rule_auth_action_dict = v2_rule_auth_action_instance.to_dict()
# create an instance of V2RuleAuthAction from a dict
v2_rule_auth_action_from_dict = V2RuleAuthAction.from_dict(v2_rule_auth_action_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


