# SyncToEnvironmentRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**source_environment** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.sync_to_environment_request import SyncToEnvironmentRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SyncToEnvironmentRequest from a JSON string
sync_to_environment_request_instance = SyncToEnvironmentRequest.from_json(json)
# print the JSON string representation of the object
print(SyncToEnvironmentRequest.to_json())

# convert the object into a dict
sync_to_environment_request_dict = sync_to_environment_request_instance.to_dict()
# create an instance of SyncToEnvironmentRequest from a dict
sync_to_environment_request_from_dict = SyncToEnvironmentRequest.from_dict(sync_to_environment_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


