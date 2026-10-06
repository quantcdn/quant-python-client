# GetMyUsage200ResponseQuotaDailyLimit

Per-user daily spend cap (object form, present when an org-level perUserDailyBudget is configured)

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**limit_cents** | **int** | The configured daily cap in US cents | [optional] 
**used_percent** | **float** | Percentage of the cap consumed today (0–100+) | [optional] 
**remaining_cents** | **int** | Cents remaining before the cap is hit; can be negative if overspent | [optional] 
**resets_at** | **datetime** | UTC timestamp when the daily counter resets (always next UTC midnight) | [optional] 

## Example

```python
from quantcdn.models.get_my_usage200_response_quota_daily_limit import GetMyUsage200ResponseQuotaDailyLimit

# TODO update the JSON string below
json = "{}"
# create an instance of GetMyUsage200ResponseQuotaDailyLimit from a JSON string
get_my_usage200_response_quota_daily_limit_instance = GetMyUsage200ResponseQuotaDailyLimit.from_json(json)
# print the JSON string representation of the object
print(GetMyUsage200ResponseQuotaDailyLimit.to_json())

# convert the object into a dict
get_my_usage200_response_quota_daily_limit_dict = get_my_usage200_response_quota_daily_limit_instance.to_dict()
# create an instance of GetMyUsage200ResponseQuotaDailyLimit from a dict
get_my_usage200_response_quota_daily_limit_from_dict = GetMyUsage200ResponseQuotaDailyLimit.from_dict(get_my_usage200_response_quota_daily_limit_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


