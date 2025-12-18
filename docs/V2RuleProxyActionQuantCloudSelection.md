# V2RuleProxyActionQuantCloudSelection

Quant Cloud application proxy selection (populated automatically when application_proxy is enabled)

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**app** | **str** | Application name | [optional] 
**env** | **str** | Environment name | [optional] 
**container** | **str** | Container name | [optional] 
**port** | **int** | Container port | [optional] 

## Example

```python
from quantcdn.models.v2_rule_proxy_action_quant_cloud_selection import V2RuleProxyActionQuantCloudSelection

# TODO update the JSON string below
json = "{}"
# create an instance of V2RuleProxyActionQuantCloudSelection from a JSON string
v2_rule_proxy_action_quant_cloud_selection_instance = V2RuleProxyActionQuantCloudSelection.from_json(json)
# print the JSON string representation of the object
print(V2RuleProxyActionQuantCloudSelection.to_json())

# convert the object into a dict
v2_rule_proxy_action_quant_cloud_selection_dict = v2_rule_proxy_action_quant_cloud_selection_instance.to_dict()
# create an instance of V2RuleProxyActionQuantCloudSelection from a dict
v2_rule_proxy_action_quant_cloud_selection_from_dict = V2RuleProxyActionQuantCloudSelection.from_dict(v2_rule_proxy_action_quant_cloud_selection_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


