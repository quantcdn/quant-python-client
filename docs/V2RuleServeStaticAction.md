# V2RuleServeStaticAction


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**static_file_path** | **str** | Path to the static file to serve | 

## Example

```python
from quantcdn.models.v2_rule_serve_static_action import V2RuleServeStaticAction

# TODO update the JSON string below
json = "{}"
# create an instance of V2RuleServeStaticAction from a JSON string
v2_rule_serve_static_action_instance = V2RuleServeStaticAction.from_json(json)
# print the JSON string representation of the object
print(V2RuleServeStaticAction.to_json())

# convert the object into a dict
v2_rule_serve_static_action_dict = v2_rule_serve_static_action_instance.to_dict()
# create an instance of V2RuleServeStaticAction from a dict
v2_rule_serve_static_action_from_dict = V2RuleServeStaticAction.from_dict(v2_rule_serve_static_action_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


