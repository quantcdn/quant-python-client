# V2KvErrorLedgersInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | The ledger name. | 
**state** | **str** | The ledger state (PENDING, ACTIVE or DROPPED). | 
**reason** | **str** | not_dropped: drop the ledger first (after its retention ends). not_drained: the ledger is DROPPED but its last entries are not archived yet. | 

## Example

```python
from quantcdn.models.v2_kv_error_ledgers_inner import V2KvErrorLedgersInner

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvErrorLedgersInner from a JSON string
v2_kv_error_ledgers_inner_instance = V2KvErrorLedgersInner.from_json(json)
# print the JSON string representation of the object
print(V2KvErrorLedgersInner.to_json())

# convert the object into a dict
v2_kv_error_ledgers_inner_dict = v2_kv_error_ledgers_inner_instance.to_dict()
# create an instance of V2KvErrorLedgersInner from a dict
v2_kv_error_ledgers_inner_from_dict = V2KvErrorLedgersInner.from_dict(v2_kv_error_ledgers_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


