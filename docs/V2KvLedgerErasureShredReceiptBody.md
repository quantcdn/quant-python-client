# V2KvLedgerErasureShredReceiptBody

The parsed form of json (a convenience copy; only json is signed).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**v** | **int** |  | 
**type** | **str** |  | 
**id** | **str** | The shredId. | 
**org** | **str** |  | 
**store** | **str** |  | 
**ledger** | **str** |  | 
**subject_ref** | **str** |  | 
**ref_key_version** | **int** | The version of the reference key that made subjectRef. | 
**shredded_at** | **datetime** |  | 
**fully_erased_after** | **datetime** |  | 
**reason** | **str** |  | 
**authority** | **str** |  | 
**requested_by** | **str** |  | 
**entry_count** | **int** | The number of shred entries (0 for a forked store or a DROPPED ledger). | 
**entries_sha256** | **str** | SHA-256 (hex) of the JCS of the shred entries, sorted by key. | 
**entries** | [**List[V2KvLedgerErasureShredEntry]**](V2KvLedgerErasureShredEntry.md) | Left out when the receipt would pass 300 KB: then KV_ledgers_shreds_entries serves them. | [optional] 
**ledger_forked** | **bool** |  | [optional] 
**supersedes** | **str** | The id of the forked record that this re-shred supersedes. | [optional] 

## Example

```python
from quantcdn.models.v2_kv_ledger_erasure_shred_receipt_body import V2KvLedgerErasureShredReceiptBody

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerErasureShredReceiptBody from a JSON string
v2_kv_ledger_erasure_shred_receipt_body_instance = V2KvLedgerErasureShredReceiptBody.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerErasureShredReceiptBody.to_json())

# convert the object into a dict
v2_kv_ledger_erasure_shred_receipt_body_dict = v2_kv_ledger_erasure_shred_receipt_body_instance.to_dict()
# create an instance of V2KvLedgerErasureShredReceiptBody from a dict
v2_kv_ledger_erasure_shred_receipt_body_from_dict = V2KvLedgerErasureShredReceiptBody.from_dict(v2_kv_ledger_erasure_shred_receipt_body_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


