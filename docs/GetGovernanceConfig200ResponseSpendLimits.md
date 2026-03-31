# GetGovernanceConfig200ResponseSpendLimits


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**monthly_budget_cents** | **int** |  | [optional] 
**daily_budget_cents** | **int** |  | [optional] 
**per_user_monthly_budget_cents** | **int** |  | [optional] 
**per_user_daily_budget_cents** | **int** |  | [optional] 
**warning_threshold_percent** | **int** |  | [optional] 

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


