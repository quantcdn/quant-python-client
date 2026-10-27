# V2KvLedgerListItem

A ledger definition with its summary.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**collection** | **str** | A collection, or a pattern where * is one whole segment. | 
**chains** | **int** |  | 
**retention_days** | **int** |  | 
**lock_mode** | **str** |  | 
**personal_fields** | **List[str]** |  | 
**subject_field** | **str** |  | [optional] 
**subject_mode** | **str** | Present when subjectField is set. | [optional] 
**subject_case** | **str** | Present when subjectField is set. | [optional] 
**anchor** | [**V2KvLedgerAnchor**](V2KvLedgerAnchor.md) |  | 
**writer_policy** | [**V2KvLedgerAdminWriterPolicy**](V2KvLedgerAdminWriterPolicy.md) |  | [optional] 
**state** | **str** | PENDING for 75 seconds after a declare, then ACTIVE or FAILED. DROPPED after KV_ledgers_delete. | 
**created_at** | **datetime** |  | 
**active_after** | **datetime** | When a PENDING ledger is checked again and becomes ACTIVE or FAILED. | 
**definition_hash** | **str** | Hex SHA-256 of the canonical (RFC 8785) definition. | 
**updated_at** | **datetime** |  | [optional] 
**error** | **str** | FAILED only: why the ledger failed. | [optional] 
**dropped_at** | **datetime** |  | [optional] 
**summary** | [**V2KvLedgerSummary**](V2KvLedgerSummary.md) |  | 

## Example

```python
from quantcdn.models.v2_kv_ledger_list_item import V2KvLedgerListItem

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerListItem from a JSON string
v2_kv_ledger_list_item_instance = V2KvLedgerListItem.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerListItem.to_json())

# convert the object into a dict
v2_kv_ledger_list_item_dict = v2_kv_ledger_list_item_instance.to_dict()
# create an instance of V2KvLedgerListItem from a dict
v2_kv_ledger_list_item_from_dict = V2KvLedgerListItem.from_dict(v2_kv_ledger_list_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


