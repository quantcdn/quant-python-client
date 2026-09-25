# GetGovernanceSpend200ResponseTodayTotal


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**spend_cents** | **int** | Org spend today in US cents | [optional] 
**request_count** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.get_governance_spend200_response_today_total import GetGovernanceSpend200ResponseTodayTotal

# TODO update the JSON string below
json = "{}"
# create an instance of GetGovernanceSpend200ResponseTodayTotal from a JSON string
get_governance_spend200_response_today_total_instance = GetGovernanceSpend200ResponseTodayTotal.from_json(json)
# print the JSON string representation of the object
print(GetGovernanceSpend200ResponseTodayTotal.to_json())

# convert the object into a dict
get_governance_spend200_response_today_total_dict = get_governance_spend200_response_today_total_instance.to_dict()
# create an instance of GetGovernanceSpend200ResponseTodayTotal from a dict
get_governance_spend200_response_today_total_from_dict = GetGovernanceSpend200ResponseTodayTotal.from_dict(get_governance_spend200_response_today_total_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


