# V2KvLedgerErasureShredEntry


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** | The entry key, &lt;collection&gt;:&lt;id&gt;. | 
**shard** | **str** |  | 
**seq** | **int** |  | 
**hash** | **str** |  | 

## Example

```python
from quantcdn.models.v2_kv_ledger_erasure_shred_entry import V2KvLedgerErasureShredEntry

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerErasureShredEntry from a JSON string
v2_kv_ledger_erasure_shred_entry_instance = V2KvLedgerErasureShredEntry.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerErasureShredEntry.to_json())

# convert the object into a dict
v2_kv_ledger_erasure_shred_entry_dict = v2_kv_ledger_erasure_shred_entry_instance.to_dict()
# create an instance of V2KvLedgerErasureShredEntry from a dict
v2_kv_ledger_erasure_shred_entry_from_dict = V2KvLedgerErasureShredEntry.from_dict(v2_kv_ledger_erasure_shred_entry_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


