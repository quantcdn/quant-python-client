# V2KvLedgerProofEntry

The archived line in stored form; personal fields stay sealed.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** |  | [optional] 
**collection** | **str** |  | [optional] 
**shard** | **str** |  | [optional] 
**id** | **str** |  | [optional] 
**seq** | **int** |  | [optional] 
**at** | **int** |  | [optional] 
**value** | **str** |  | [optional] 
**prev_hash** | **str** |  | [optional] 
**hash** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.v2_kv_ledger_proof_entry import V2KvLedgerProofEntry

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerProofEntry from a JSON string
v2_kv_ledger_proof_entry_instance = V2KvLedgerProofEntry.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerProofEntry.to_json())

# convert the object into a dict
v2_kv_ledger_proof_entry_dict = v2_kv_ledger_proof_entry_instance.to_dict()
# create an instance of V2KvLedgerProofEntry from a dict
v2_kv_ledger_proof_entry_from_dict = V2KvLedgerProofEntry.from_dict(v2_kv_ledger_proof_entry_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


