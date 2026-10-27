# V2KvLedgerMeta

Ledger metadata of an entry. Present only on ledger entries.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | The ledger name. | [optional] 
**id** | **str** | A ULID, a hyphen and the two-digit shard. | 
**shard** | **str** |  | 
**seq** | **int** | The sequence number in the shard. | 
**at** | **int** | Server time, epoch milliseconds. | 
**hash** | **str** |  | 
**prev_hash** | **str** | The hash of the previous entry in the same shard. | 
**source** | [**V2KvLedgerProvenance**](V2KvLedgerProvenance.md) |  | [optional] 
**subject** | **str** | Present when the ledger has a subjectField: what the subject field holds. | [optional] 

## Example

```python
from quantcdn.models.v2_kv_ledger_meta import V2KvLedgerMeta

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerMeta from a JSON string
v2_kv_ledger_meta_instance = V2KvLedgerMeta.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerMeta.to_json())

# convert the object into a dict
v2_kv_ledger_meta_dict = v2_kv_ledger_meta_instance.to_dict()
# create an instance of V2KvLedgerMeta from a dict
v2_kv_ledger_meta_from_dict = V2KvLedgerMeta.from_dict(v2_kv_ledger_meta_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


