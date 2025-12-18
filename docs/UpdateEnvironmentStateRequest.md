# UpdateEnvironmentStateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**action** | **str** |  | [optional] 
**image_tag** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.update_environment_state_request import UpdateEnvironmentStateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateEnvironmentStateRequest from a JSON string
update_environment_state_request_instance = UpdateEnvironmentStateRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateEnvironmentStateRequest.to_json())

# convert the object into a dict
update_environment_state_request_dict = update_environment_state_request_instance.to_dict()
# create an instance of UpdateEnvironmentStateRequest from a dict
update_environment_state_request_from_dict = UpdateEnvironmentStateRequest.from_dict(update_environment_state_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


