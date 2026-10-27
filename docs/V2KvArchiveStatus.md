# V2KvArchiveStatus

The archive of one deleted store.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**store** | **str** |  | [optional] 
**status** | **str** | purged: the latest purge is COMPLETE. purging: a purge is not final. blocked: the latest purge is BLOCKED. retained: a lock or the quiet period is in the future. eligible: otherwise. | [optional] 
**deleted_at** | **datetime** |  | [optional] 
**earliest_purge_at** | **datetime** |  | [optional] 
**retained_until** | **datetime** |  | [optional] 
**source** | **str** |  | [optional] 
**project** | **str** |  | [optional] 
**purge** | [**V2KvArchivePurge**](V2KvArchivePurge.md) |  | [optional] 

## Example

```python
from quantcdn.models.v2_kv_archive_status import V2KvArchiveStatus

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvArchiveStatus from a JSON string
v2_kv_archive_status_instance = V2KvArchiveStatus.from_json(json)
# print the JSON string representation of the object
print(V2KvArchiveStatus.to_json())

# convert the object into a dict
v2_kv_archive_status_dict = v2_kv_archive_status_instance.to_dict()
# create an instance of V2KvArchiveStatus from a dict
v2_kv_archive_status_from_dict = V2KvArchiveStatus.from_dict(v2_kv_archive_status_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


