# V2KvLedgerVerifyShard


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**collection** | **str** |  | 
**shard** | **str** |  | 
**from_seq** | **int** | The first seq checked in this call (0 when no entry was in range). | 
**to_seq** | **int** |  | 
**ok** | **bool** |  | 
**first_broken_seq** | **int** |  | [optional] 
**reason** | **str** |  | [optional] 
**object_from_seq** | **int** |  | [optional] 
**object_to_seq** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.v2_kv_ledger_verify_shard import V2KvLedgerVerifyShard

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerVerifyShard from a JSON string
v2_kv_ledger_verify_shard_instance = V2KvLedgerVerifyShard.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerVerifyShard.to_json())

# convert the object into a dict
v2_kv_ledger_verify_shard_dict = v2_kv_ledger_verify_shard_instance.to_dict()
# create an instance of V2KvLedgerVerifyShard from a dict
v2_kv_ledger_verify_shard_from_dict = V2KvLedgerVerifyShard.from_dict(v2_kv_ledger_verify_shard_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


