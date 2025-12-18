# V2RuleCustomResponseAction


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**custom_response_body** | **str** | Custom response body content | 
**custom_response_status_code** | **int** | HTTP status code for custom response | [optional] [default to 200]

## Example

```python
from quantcdn.models.v2_rule_custom_response_action import V2RuleCustomResponseAction

# TODO update the JSON string below
json = "{}"
# create an instance of V2RuleCustomResponseAction from a JSON string
v2_rule_custom_response_action_instance = V2RuleCustomResponseAction.from_json(json)
# print the JSON string representation of the object
print(V2RuleCustomResponseAction.to_json())

# convert the object into a dict
v2_rule_custom_response_action_dict = v2_rule_custom_response_action_instance.to_dict()
# create an instance of V2RuleCustomResponseAction from a dict
v2_rule_custom_response_action_from_dict = V2RuleCustomResponseAction.from_dict(v2_rule_custom_response_action_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


