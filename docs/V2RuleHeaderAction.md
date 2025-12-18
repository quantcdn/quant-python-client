# V2RuleHeaderAction


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**headers** | **Dict[str, str]** | Headers to set | 

## Example

```python
from quantcdn.models.v2_rule_header_action import V2RuleHeaderAction

# TODO update the JSON string below
json = "{}"
# create an instance of V2RuleHeaderAction from a JSON string
v2_rule_header_action_instance = V2RuleHeaderAction.from_json(json)
# print the JSON string representation of the object
print(V2RuleHeaderAction.to_json())

# convert the object into a dict
v2_rule_header_action_dict = v2_rule_header_action_instance.to_dict()
# create an instance of V2RuleHeaderAction from a dict
v2_rule_header_action_from_dict = V2RuleHeaderAction.from_dict(v2_rule_header_action_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


