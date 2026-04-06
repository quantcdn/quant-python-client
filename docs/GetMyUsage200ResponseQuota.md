# GetMyUsage200ResponseQuota


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**monthly_limit** | **int** | Per-user monthly budget in US cents | [optional] 
**daily_limit** | **int** | Per-user daily budget in US cents | [optional] 

## Example

```python
from quantcdn.models.get_my_usage200_response_quota import GetMyUsage200ResponseQuota

# TODO update the JSON string below
json = "{}"
# create an instance of GetMyUsage200ResponseQuota from a JSON string
get_my_usage200_response_quota_instance = GetMyUsage200ResponseQuota.from_json(json)
# print the JSON string representation of the object
print(GetMyUsage200ResponseQuota.to_json())

# convert the object into a dict
get_my_usage200_response_quota_dict = get_my_usage200_response_quota_instance.to_dict()
# create an instance of GetMyUsage200ResponseQuota from a dict
get_my_usage200_response_quota_from_dict = GetMyUsage200ResponseQuota.from_dict(get_my_usage200_response_quota_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


