# GetEnvironmentLogs200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**log_events** | [**List[GetEnvironmentLogs200ResponseLogEventsInner]**](GetEnvironmentLogs200ResponseLogEventsInner.md) | Array of log events | [optional] 
**next_token** | **str** | Token for fetching next page of results (null if no more pages) | [optional] 

## Example

```python
from quantcdn.models.get_environment_logs200_response import GetEnvironmentLogs200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetEnvironmentLogs200Response from a JSON string
get_environment_logs200_response_instance = GetEnvironmentLogs200Response.from_json(json)
# print the JSON string representation of the object
print(GetEnvironmentLogs200Response.to_json())

# convert the object into a dict
get_environment_logs200_response_dict = get_environment_logs200_response_instance.to_dict()
# create an instance of GetEnvironmentLogs200Response from a dict
get_environment_logs200_response_from_dict = GetEnvironmentLogs200Response.from_dict(get_environment_logs200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


