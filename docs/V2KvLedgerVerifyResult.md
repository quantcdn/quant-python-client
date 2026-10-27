# V2KvLedgerVerifyResult

ok is true when every shard of this call is ok. Continue while next_cursor is not null; every page of one run has the same verificationId.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ok** | **bool** |  | 
**entries** | **int** | Live entries checked in this call. | 
**shards** | [**List[V2KvLedgerVerifyShard]**](V2KvLedgerVerifyShard.md) |  | 
**verification_id** | **str** | The verification record; KV_ledgers_verifications_report returns it signed. | [optional] 
**next_cursor** | **str** |  | 

## Example

```python
from quantcdn.models.v2_kv_ledger_verify_result import V2KvLedgerVerifyResult

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerVerifyResult from a JSON string
v2_kv_ledger_verify_result_instance = V2KvLedgerVerifyResult.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerVerifyResult.to_json())

# convert the object into a dict
v2_kv_ledger_verify_result_dict = v2_kv_ledger_verify_result_instance.to_dict()
# create an instance of V2KvLedgerVerifyResult from a dict
v2_kv_ledger_verify_result_from_dict = V2KvLedgerVerifyResult.from_dict(v2_kv_ledger_verify_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


