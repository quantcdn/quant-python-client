# V2KvArchivePurgeAnswer

The one answer of KV_archives_purge, for 200 and 202; no property is required. A dry run answers 200 with dryRun true and the counts (nothing is deleted). A start answers 202 with purgeId and state (the purge was accepted, or a repeat with the same Idempotency-Key found the existing one); read it with KV_archives_purge_show. For a dry run, eligible is false when any version is locked, a legal hold is on, a delete marker exists, or the quiet period (24 hours after deletedAt) has not passed. At most 100,000 versions are counted inline (partial true past that).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**purge_id** | **str** | Set on a start (202). | [optional] 
**state** | **str** | Set on a start (202). | [optional] 
**dry_run** | **bool** |  | [optional] 
**store** | **str** |  | [optional] 
**eligible** | **bool** |  | [optional] 
**partial** | **bool** |  | [optional] 
**versions** | **int** |  | [optional] 
**bytes** | **int** |  | [optional] 
**ledger_objects** | **int** |  | [optional] 
**digest_objects** | **int** |  | [optional] 
**anchor_objects** | **int** |  | [optional] 
**delete_markers** | **int** |  | [optional] 
**latest_retain_until** | **datetime** |  | [optional] 
**earliest_purge_at** | **datetime** |  | [optional] 
**quiet_until** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.v2_kv_archive_purge_answer import V2KvArchivePurgeAnswer

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvArchivePurgeAnswer from a JSON string
v2_kv_archive_purge_answer_instance = V2KvArchivePurgeAnswer.from_json(json)
# print the JSON string representation of the object
print(V2KvArchivePurgeAnswer.to_json())

# convert the object into a dict
v2_kv_archive_purge_answer_dict = v2_kv_archive_purge_answer_instance.to_dict()
# create an instance of V2KvArchivePurgeAnswer from a dict
v2_kv_archive_purge_answer_from_dict = V2KvArchivePurgeAnswer.from_dict(v2_kv_archive_purge_answer_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


