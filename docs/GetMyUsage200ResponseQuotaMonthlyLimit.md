# GetMyUsage200ResponseQuotaMonthlyLimit

Per-user monthly spend cap (object form, present when an org-level perUserMonthlyBudget is configured)

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**limit_cents** | **int** | The configured monthly cap in US cents | [optional] 
**used_percent** | **float** | Percentage of the cap consumed this month (0–100+) | [optional] 
**remaining_cents** | **int** | Cents remaining before the cap is hit; can be negative if overspent | [optional] 

## Example

```python
from quantcdn.models.get_my_usage200_response_quota_monthly_limit import GetMyUsage200ResponseQuotaMonthlyLimit

# TODO update the JSON string below
json = "{}"
# create an instance of GetMyUsage200ResponseQuotaMonthlyLimit from a JSON string
get_my_usage200_response_quota_monthly_limit_instance = GetMyUsage200ResponseQuotaMonthlyLimit.from_json(json)
# print the JSON string representation of the object
print(GetMyUsage200ResponseQuotaMonthlyLimit.to_json())

# convert the object into a dict
get_my_usage200_response_quota_monthly_limit_dict = get_my_usage200_response_quota_monthly_limit_instance.to_dict()
# create an instance of GetMyUsage200ResponseQuotaMonthlyLimit from a dict
get_my_usage200_response_quota_monthly_limit_from_dict = GetMyUsage200ResponseQuotaMonthlyLimit.from_dict(get_my_usage200_response_quota_monthly_limit_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


