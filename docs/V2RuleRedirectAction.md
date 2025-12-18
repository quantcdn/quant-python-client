# V2RuleRedirectAction


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**to** | **str** | Redirect destination URL | 
**status_code** | **str** | HTTP status code for redirect | [optional] [default to '301']

## Example

```python
from quantcdn.models.v2_rule_redirect_action import V2RuleRedirectAction

# TODO update the JSON string below
json = "{}"
# create an instance of V2RuleRedirectAction from a JSON string
v2_rule_redirect_action_instance = V2RuleRedirectAction.from_json(json)
# print the JSON string representation of the object
print(V2RuleRedirectAction.to_json())

# convert the object into a dict
v2_rule_redirect_action_dict = v2_rule_redirect_action_instance.to_dict()
# create an instance of V2RuleRedirectAction from a dict
v2_rule_redirect_action_from_dict = V2RuleRedirectAction.from_dict(v2_rule_redirect_action_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


