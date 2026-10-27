# SetIdleSleepRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** | Whether the environment sleeps when idle. | 
**idle_minutes** | **int** | Minutes with no requests before compute sleeps. | [optional] [default to 30]

## Example

```python
from quantcdn.models.set_idle_sleep_request import SetIdleSleepRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SetIdleSleepRequest from a JSON string
set_idle_sleep_request_instance = SetIdleSleepRequest.from_json(json)
# print the JSON string representation of the object
print(SetIdleSleepRequest.to_json())

# convert the object into a dict
set_idle_sleep_request_dict = set_idle_sleep_request_instance.to_dict()
# create an instance of SetIdleSleepRequest from a dict
set_idle_sleep_request_from_dict = SetIdleSleepRequest.from_dict(set_idle_sleep_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


