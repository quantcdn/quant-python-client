# V2KvLedgerDetail

KV_ledgers_show: the definition with the retention end, the last digest time and the last verify result.

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
**retain_until** | **datetime** | The archive retention end; an ACTIVE ledger can be dropped after it. | [optional] 
**last_digest_at** | **datetime** |  | [optional] 
**last_verify** | [**V2KvLedgerLastVerify**](V2KvLedgerLastVerify.md) |  | [optional] 

## Example

```python
from quantcdn.models.v2_kv_ledger_detail import V2KvLedgerDetail

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerDetail from a JSON string
v2_kv_ledger_detail_instance = V2KvLedgerDetail.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerDetail.to_json())

# convert the object into a dict
v2_kv_ledger_detail_dict = v2_kv_ledger_detail_instance.to_dict()
# create an instance of V2KvLedgerDetail from a dict
v2_kv_ledger_detail_from_dict = V2KvLedgerDetail.from_dict(v2_kv_ledger_detail_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


