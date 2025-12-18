# GetEnvironmentLogs200ResponseLogEventsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timestamp** | **int** | Unix timestamp in milliseconds | [optional] 
**message** | **str** | Log message content | [optional] 

## Example

```python
from quantcdn.models.get_environment_logs200_response_log_events_inner import GetEnvironmentLogs200ResponseLogEventsInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetEnvironmentLogs200ResponseLogEventsInner from a JSON string
get_environment_logs200_response_log_events_inner_instance = GetEnvironmentLogs200ResponseLogEventsInner.from_json(json)
# print the JSON string representation of the object
print(GetEnvironmentLogs200ResponseLogEventsInner.to_json())

# convert the object into a dict
get_environment_logs200_response_log_events_inner_dict = get_environment_logs200_response_log_events_inner_instance.to_dict()
# create an instance of GetEnvironmentLogs200ResponseLogEventsInner from a dict
get_environment_logs200_response_log_events_inner_from_dict = GetEnvironmentLogs200ResponseLogEventsInner.from_dict(get_environment_logs200_response_log_events_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


