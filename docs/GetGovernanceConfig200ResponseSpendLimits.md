# GetGovernanceConfig200ResponseSpendLimits


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**monthly_budget_cents** | **int** |  | [optional] 
**daily_budget_cents** | **int** |  | [optional] 
**per_user_monthly_budget_cents** | **int** |  | [optional] 
**per_user_daily_budget_cents** | **int** |  | [optional] 
**warning_threshold_percent** | **int** |  | [optional] 
**interface_limits** | [**Dict[str, GetGovernanceConfig200ResponseSpendLimitsInterfaceLimitsValue]**](GetGovernanceConfig200ResponseSpendLimitsInterfaceLimitsValue.md) | Aggregate spend caps per interface label (slack, autonomous, api-gateway, streaming, websocket). Keys are interface labels. | [optional] 
**user_overrides** | [**Dict[str, GetGovernanceConfig200ResponseSpendLimitsUserOverridesValue]**](GetGovernanceConfig200ResponseSpendLimitsUserOverridesValue.md) | Per-user budget overrides keyed by userId (numeric portal id, slack-&lt;id&gt;, or system:code-agent). Replaces the flat per-user budget for that user; unlimited&#x3D;true exempts them. | [optional] 
**per_token_monthly_budget_cents** | **int** | Flat monthly cap in cents applied to every API token without a named override | [optional] 
**per_token_daily_budget_cents** | **int** | Flat daily cap in cents applied to every API token without a named override | [optional] 
**token_overrides** | [**Dict[str, GetGovernanceConfig200ResponseSpendLimitsUserOverridesValue]**](GetGovernanceConfig200ResponseSpendLimitsUserOverridesValue.md) | Per-token budget overrides keyed by API token id. Replaces the flat per-token budget for that token; unlimited&#x3D;true exempts it. | [optional] 

## Example

```python
from quantcdn.models.get_governance_config200_response_spend_limits import GetGovernanceConfig200ResponseSpendLimits

# TODO update the JSON string below
json = "{}"
# create an instance of GetGovernanceConfig200ResponseSpendLimits from a JSON string
get_governance_config200_response_spend_limits_instance = GetGovernanceConfig200ResponseSpendLimits.from_json(json)
# print the JSON string representation of the object
print(GetGovernanceConfig200ResponseSpendLimits.to_json())

# convert the object into a dict
get_governance_config200_response_spend_limits_dict = get_governance_config200_response_spend_limits_instance.to_dict()
# create an instance of GetGovernanceConfig200ResponseSpendLimits from a dict
get_governance_config200_response_spend_limits_from_dict = GetGovernanceConfig200ResponseSpendLimits.from_dict(get_governance_config200_response_spend_limits_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


