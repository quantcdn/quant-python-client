# GetMyUsage200ResponseMonthly


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**spend_cents** | **int** |  | [optional] 
**request_count** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.get_my_usage200_response_monthly import GetMyUsage200ResponseMonthly

# TODO update the JSON string below
json = "{}"
# create an instance of GetMyUsage200ResponseMonthly from a JSON string
get_my_usage200_response_monthly_instance = GetMyUsage200ResponseMonthly.from_json(json)
# print the JSON string representation of the object
print(GetMyUsage200ResponseMonthly.to_json())

# convert the object into a dict
get_my_usage200_response_monthly_dict = get_my_usage200_response_monthly_instance.to_dict()
# create an instance of GetMyUsage200ResponseMonthly from a dict
get_my_usage200_response_monthly_from_dict = GetMyUsage200ResponseMonthly.from_dict(get_my_usage200_response_monthly_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


