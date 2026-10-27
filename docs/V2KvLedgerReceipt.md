# V2KvLedgerReceipt

The receipt of an appended entry. Keep receipts: the offline verifier checks them against the archive.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** | collection:id | 
**id** | **str** | ULID, a hyphen and the two-digit shard. Increases within a shard. | 
**shard** | **str** |  | 
**seq** | **int** | Sequence number of the entry on its shard. | 
**at** | **int** | Epoch milliseconds (the ULID time of id). | 
**hash** | **str** | SHA-256 hex of this entry. | 
**prev_hash** | **str** | SHA-256 hex of the previous entry on the shard (the genesis hash for seq 1). | 
**ledger** | **str** | The ledger name. | 
**source** | [**V2KvLedgerProvenance**](V2KvLedgerProvenance.md) |  | [optional] 
**replayed** | **bool** | Present only on a retry with the same idempotencyKey: this is the first receipt. | [optional] 

## Example

```python
from quantcdn.models.v2_kv_ledger_receipt import V2KvLedgerReceipt

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerReceipt from a JSON string
v2_kv_ledger_receipt_instance = V2KvLedgerReceipt.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerReceipt.to_json())

# convert the object into a dict
v2_kv_ledger_receipt_dict = v2_kv_ledger_receipt_instance.to_dict()
# create an instance of V2KvLedgerReceipt from a dict
v2_kv_ledger_receipt_from_dict = V2KvLedgerReceipt.from_dict(v2_kv_ledger_receipt_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


