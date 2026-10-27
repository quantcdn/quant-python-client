# V2KvLedgerFailure


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**collection** | **str** |  | 
**shard** | **str** |  | 
**seq** | **int** |  | [optional] 
**reason** | **str** |  | 

## Example

```python
from quantcdn.models.v2_kv_ledger_failure import V2KvLedgerFailure

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerFailure from a JSON string
v2_kv_ledger_failure_instance = V2KvLedgerFailure.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerFailure.to_json())

# convert the object into a dict
v2_kv_ledger_failure_dict = v2_kv_ledger_failure_instance.to_dict()
# create an instance of V2KvLedgerFailure from a dict
v2_kv_ledger_failure_from_dict = V2KvLedgerFailure.from_dict(v2_kv_ledger_failure_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


