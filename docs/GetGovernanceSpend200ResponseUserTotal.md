# GetGovernanceSpend200ResponseUserTotal


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**monthly_spend_cents** | **int** |  | [optional] 
**daily_spend_cents** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.get_governance_spend200_response_user_total import GetGovernanceSpend200ResponseUserTotal

# TODO update the JSON string below
json = "{}"
# create an instance of GetGovernanceSpend200ResponseUserTotal from a JSON string
get_governance_spend200_response_user_total_instance = GetGovernanceSpend200ResponseUserTotal.from_json(json)
# print the JSON string representation of the object
print(GetGovernanceSpend200ResponseUserTotal.to_json())

# convert the object into a dict
get_governance_spend200_response_user_total_dict = get_governance_spend200_response_user_total_instance.to_dict()
# create an instance of GetGovernanceSpend200ResponseUserTotal from a dict
get_governance_spend200_response_user_total_from_dict = GetGovernanceSpend200ResponseUserTotal.from_dict(get_governance_spend200_response_user_total_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


