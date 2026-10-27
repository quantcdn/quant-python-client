# V2KvLedgerErasureShredResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ledger** | **str** |  | 
**entries** | [**List[V2KvLedgerReceipt]**](V2KvLedgerReceipt.md) | The shred entry of each collection that holds the subject (empty for alreadyShredded, a DROPPED ledger and a forked store). | 
**shredded_at** | **datetime** | When the key was destroyed (the first shred for alreadyShredded). | 
**fully_erased_after** | **datetime** | shreddedAt + 35 days: after this time no backup of the key remains. | 
**already_shredded** | **bool** | Present only when the subject was shredded before this call and this call wrote nothing. | [optional] 
**ledger_forked** | **bool** | Present only when the store is forked: the key is destroyed and no shred entry is recorded. | [optional] 
**shred_id** | **str** | The id of the erasure record (the same on every repeat). | [optional] 
**subject_ref** | **str** | The pseudonym of the subject in the erasure records and receipts. | 
**ref_key_version** | **int** | The version of the reference key that made subjectRef. | 
**receipt** | [**V2KvLedgerErasureSignedShredReceipt**](V2KvLedgerErasureSignedShredReceipt.md) |  | [optional] 

## Example

```python
from quantcdn.models.v2_kv_ledger_erasure_shred_result import V2KvLedgerErasureShredResult

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerErasureShredResult from a JSON string
v2_kv_ledger_erasure_shred_result_instance = V2KvLedgerErasureShredResult.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerErasureShredResult.to_json())

# convert the object into a dict
v2_kv_ledger_erasure_shred_result_dict = v2_kv_ledger_erasure_shred_result_instance.to_dict()
# create an instance of V2KvLedgerErasureShredResult from a dict
v2_kv_ledger_erasure_shred_result_from_dict = V2KvLedgerErasureShredResult.from_dict(v2_kv_ledger_erasure_shred_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


