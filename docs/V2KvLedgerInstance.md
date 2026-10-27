# V2KvLedgerInstance

One chain: a collection and shard that holds entries.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**collection** | **str** |  | 
**shard** | **str** |  | 
**head_seq** | **int** | Sequence number of the last entry. | 
**head_at** | **int** | Epoch ms of the last entry. | [optional] 
**archived_seq** | **int** | Last sequence number in the archive. | 
**archive_lag_seconds** | **int** | Age of the oldest unarchived entry; 0 when up to date. | 
**broken** | **Dict[str, object]** | Set when the archive worker found a chain fault (seq, reason, at). | [optional] 

## Example

```python
from quantcdn.models.v2_kv_ledger_instance import V2KvLedgerInstance

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerInstance from a JSON string
v2_kv_ledger_instance_instance = V2KvLedgerInstance.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerInstance.to_json())

# convert the object into a dict
v2_kv_ledger_instance_dict = v2_kv_ledger_instance_instance.to_dict()
# create an instance of V2KvLedgerInstance from a dict
v2_kv_ledger_instance_from_dict = V2KvLedgerInstance.from_dict(v2_kv_ledger_instance_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


