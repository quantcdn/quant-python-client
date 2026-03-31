# GetMyUsage200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user_id** | **str** |  | [optional] 
**current_month** | **str** |  | [optional] 
**monthly** | [**GetMyUsage200ResponseMonthly**](GetMyUsage200ResponseMonthly.md) |  | [optional] 
**daily** | [**GetMyUsage200ResponseDaily**](GetMyUsage200ResponseDaily.md) |  | [optional] 
**quota** | **object** |  | [optional] 

## Example

```python
from quantcdn.models.get_my_usage200_response import GetMyUsage200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetMyUsage200Response from a JSON string
get_my_usage200_response_instance = GetMyUsage200Response.from_json(json)
# print the JSON string representation of the object
print(GetMyUsage200Response.to_json())

# convert the object into a dict
get_my_usage200_response_dict = get_my_usage200_response_instance.to_dict()
# create an instance of GetMyUsage200Response from a dict
get_my_usage200_response_from_dict = GetMyUsage200Response.from_dict(get_my_usage200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


