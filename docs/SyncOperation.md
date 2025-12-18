# SyncOperation


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sync_id** | **str** |  | [optional] 
**sync_type** | **str** |  | [optional] 
**source_environment** | **str** |  | [optional] 
**target_environment** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**created_at** | **str** |  | [optional] 
**completed_at** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.sync_operation import SyncOperation

# TODO update the JSON string below
json = "{}"
# create an instance of SyncOperation from a JSON string
sync_operation_instance = SyncOperation.from_json(json)
# print the JSON string representation of the object
print(SyncOperation.to_json())

# convert the object into a dict
sync_operation_dict = sync_operation_instance.to_dict()
# create an instance of SyncOperation from a dict
sync_operation_from_dict = SyncOperation.from_dict(sync_operation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


