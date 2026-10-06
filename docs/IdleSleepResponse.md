# IdleSleepResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | 
**idle_minutes** | **int** |  | 
**state** | **str** |  | 
**state_changed_at** | **datetime** |  | 

## Example

```python
from quantcdn.models.idle_sleep_response import IdleSleepResponse

# TODO update the JSON string below
json = "{}"
# create an instance of IdleSleepResponse from a JSON string
idle_sleep_response_instance = IdleSleepResponse.from_json(json)
# print the JSON string representation of the object
print(IdleSleepResponse.to_json())

# convert the object into a dict
idle_sleep_response_dict = idle_sleep_response_instance.to_dict()
# create an instance of IdleSleepResponse from a dict
idle_sleep_response_from_dict = IdleSleepResponse.from_dict(idle_sleep_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


