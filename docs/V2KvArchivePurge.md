# V2KvArchivePurge

One purge of a retained archive. The reason text is the one the caller sent; requestedBy is set by Quant (user:<id> or token:<id>).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**purge_id** | **str** | OpenAPI schemas and path parameters for the retained ledger archive routes of deleted stores (A5). Shapes follow the backend contract C-1 (ArchiveStatus, DryRun, Purge, PurgeReceipt, manifest). The list uses the KV page envelope (data, next_cursor, has_more, page_end). | [optional] 
**store** | **str** |  | [optional] 
**state** | **str** | COMPLETE, RETAINED, BLOCKED and CANCELLED are final. RETAINED: a lock or the quiet period was found at the gate, nothing was deleted. BLOCKED: needs an operator. | [optional] 
**requested_by** | **str** |  | [optional] 
**requested_at** | **datetime** |  | [optional] 
**reason** | **str** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 
**completed_at** | **datetime** |  | [optional] 
**retained_until** | **datetime** | On a RETAINED purge, the latest lock found. | [optional] 
**counts** | [**V2KvArchivePurgeCounts**](V2KvArchivePurgeCounts.md) |  | [optional] 
**last_error** | [**V2KvArchivePurgeLastError**](V2KvArchivePurgeLastError.md) |  | [optional] 

## Example

```python
from quantcdn.models.v2_kv_archive_purge import V2KvArchivePurge

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvArchivePurge from a JSON string
v2_kv_archive_purge_instance = V2KvArchivePurge.from_json(json)
# print the JSON string representation of the object
print(V2KvArchivePurge.to_json())

# convert the object into a dict
v2_kv_archive_purge_dict = v2_kv_archive_purge_instance.to_dict()
# create an instance of V2KvArchivePurge from a dict
v2_kv_archive_purge_from_dict = V2KvArchivePurge.from_dict(v2_kv_archive_purge_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


