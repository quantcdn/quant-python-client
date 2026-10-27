# V2RuleAuthFunctionAction


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fn_uuid** | **str** | UUID of the auth function (type edge_auth) the rule runs | 

## Example

```python
from quantcdn.models.v2_rule_auth_function_action import V2RuleAuthFunctionAction

# TODO update the JSON string below
json = "{}"
# create an instance of V2RuleAuthFunctionAction from a JSON string
v2_rule_auth_function_action_instance = V2RuleAuthFunctionAction.from_json(json)
# print the JSON string representation of the object
print(V2RuleAuthFunctionAction.to_json())

# convert the object into a dict
v2_rule_auth_function_action_dict = v2_rule_auth_function_action_instance.to_dict()
# create an instance of V2RuleAuthFunctionAction from a dict
v2_rule_auth_function_action_from_dict = V2RuleAuthFunctionAction.from_dict(v2_rule_auth_function_action_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


