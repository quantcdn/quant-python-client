# V2RuleProxyActionNotifyConfig

Notification configuration (required when notify is slack)

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**webhook_url** | **str** | Slack webhook URL | [optional] 

## Example

```python
from quantcdn.models.v2_rule_proxy_action_notify_config import V2RuleProxyActionNotifyConfig

# TODO update the JSON string below
json = "{}"
# create an instance of V2RuleProxyActionNotifyConfig from a JSON string
v2_rule_proxy_action_notify_config_instance = V2RuleProxyActionNotifyConfig.from_json(json)
# print the JSON string representation of the object
print(V2RuleProxyActionNotifyConfig.to_json())

# convert the object into a dict
v2_rule_proxy_action_notify_config_dict = v2_rule_proxy_action_notify_config_instance.to_dict()
# create an instance of V2RuleProxyActionNotifyConfig from a dict
v2_rule_proxy_action_notify_config_from_dict = V2RuleProxyActionNotifyConfig.from_dict(v2_rule_proxy_action_notify_config_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


