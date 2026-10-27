# V2KvLedgerLastVerifyScope

The request range; empty for a full verify.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**collection** | **str** |  | [optional] 
**since** | **datetime** |  | [optional] 
**until** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.v2_kv_ledger_last_verify_scope import V2KvLedgerLastVerifyScope

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerLastVerifyScope from a JSON string
v2_kv_ledger_last_verify_scope_instance = V2KvLedgerLastVerifyScope.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerLastVerifyScope.to_json())

# convert the object into a dict
v2_kv_ledger_last_verify_scope_dict = v2_kv_ledger_last_verify_scope_instance.to_dict()
# create an instance of V2KvLedgerLastVerifyScope from a dict
v2_kv_ledger_last_verify_scope_from_dict = V2KvLedgerLastVerifyScope.from_dict(v2_kv_ledger_last_verify_scope_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


