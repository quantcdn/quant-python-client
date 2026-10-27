# V2KvLedgerErasureShredRecord


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The shredId. | 
**subject_ref** | **str** | The subject reference (never the subject id). | 
**shredded_at** | **datetime** |  | 
**fully_erased_after** | **datetime** |  | 
**entries** | **int** | The number of shred entries recorded. | 
**reason** | **str** |  | 
**authority** | **str** |  | 
**requested_by** | **str** |  | 
**ledger_forked** | **bool** |  | [optional] 
**supersedes** | **str** |  | [optional] 
**ref_key_version** | **int** | The version of the reference key that made subjectRef. | [optional] 

## Example

```python
from quantcdn.models.v2_kv_ledger_erasure_shred_record import V2KvLedgerErasureShredRecord

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerErasureShredRecord from a JSON string
v2_kv_ledger_erasure_shred_record_instance = V2KvLedgerErasureShredRecord.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerErasureShredRecord.to_json())

# convert the object into a dict
v2_kv_ledger_erasure_shred_record_dict = v2_kv_ledger_erasure_shred_record_instance.to_dict()
# create an instance of V2KvLedgerErasureShredRecord from a dict
v2_kv_ledger_erasure_shred_record_from_dict = V2KvLedgerErasureShredRecord.from_dict(v2_kv_ledger_erasure_shred_record_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


