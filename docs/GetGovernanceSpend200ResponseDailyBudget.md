# GetGovernanceSpend200ResponseDailyBudget


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**daily_budget_cents** | **int** |  | [optional] 
**used_percent** | **float** |  | [optional] 
**remaining_cents** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.get_governance_spend200_response_daily_budget import GetGovernanceSpend200ResponseDailyBudget

# TODO update the JSON string below
json = "{}"
# create an instance of GetGovernanceSpend200ResponseDailyBudget from a JSON string
get_governance_spend200_response_daily_budget_instance = GetGovernanceSpend200ResponseDailyBudget.from_json(json)
# print the JSON string representation of the object
print(GetGovernanceSpend200ResponseDailyBudget.to_json())

# convert the object into a dict
get_governance_spend200_response_daily_budget_dict = get_governance_spend200_response_daily_budget_instance.to_dict()
# create an instance of GetGovernanceSpend200ResponseDailyBudget from a dict
get_governance_spend200_response_daily_budget_from_dict = GetGovernanceSpend200ResponseDailyBudget.from_dict(get_governance_spend200_response_daily_budget_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


