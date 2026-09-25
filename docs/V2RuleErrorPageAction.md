# V2RuleErrorPageAction


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error_page_path** | **str** | Published path of the page to serve as the error page | 
**status_codes** | **List[str]** | Status codes this page is served for | 

## Example

```python
from quantcdn.models.v2_rule_error_page_action import V2RuleErrorPageAction

# TODO update the JSON string below
json = "{}"
# create an instance of V2RuleErrorPageAction from a JSON string
v2_rule_error_page_action_instance = V2RuleErrorPageAction.from_json(json)
# print the JSON string representation of the object
print(V2RuleErrorPageAction.to_json())

# convert the object into a dict
v2_rule_error_page_action_dict = v2_rule_error_page_action_instance.to_dict()
# create an instance of V2RuleErrorPageAction from a dict
v2_rule_error_page_action_from_dict = V2RuleErrorPageAction.from_dict(v2_rule_error_page_action_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


