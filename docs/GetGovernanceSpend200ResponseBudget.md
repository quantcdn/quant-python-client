# GetGovernanceSpend200ResponseBudget


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**monthly_budget_cents** | **int** |  | [optional] 
**used_percent** | **float** |  | [optional] 
**remaining_cents** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.get_governance_spend200_response_budget import GetGovernanceSpend200ResponseBudget

# TODO update the JSON string below
json = "{}"
# create an instance of GetGovernanceSpend200ResponseBudget from a JSON string
get_governance_spend200_response_budget_instance = GetGovernanceSpend200ResponseBudget.from_json(json)
# print the JSON string representation of the object
print(GetGovernanceSpend200ResponseBudget.to_json())

# convert the object into a dict
get_governance_spend200_response_budget_dict = get_governance_spend200_response_budget_instance.to_dict()
# create an instance of GetGovernanceSpend200ResponseBudget from a dict
get_governance_spend200_response_budget_from_dict = GetGovernanceSpend200ResponseBudget.from_dict(get_governance_spend200_response_budget_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


