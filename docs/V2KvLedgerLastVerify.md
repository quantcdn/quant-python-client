# V2KvLedgerLastVerify

The last verify result of the ledger (the daily scheduled full verify, or the last complete API or dashboard verify). ok is true only when complete is true and no shard failed.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The verification record; KV_ledgers_verifications_report returns it signed. | [optional] 
**at** | **datetime** |  | 
**started_at** | **datetime** |  | 
**duration_ms** | **int** |  | [optional] 
**ok** | **bool** |  | 
**entries** | **int** |  | 
**shards_failed** | **int** |  | 
**complete** | **bool** |  | 
**pages** | **int** |  | [optional] 
**trigger** | **str** |  | 
**scope** | [**V2KvLedgerLastVerifyScope**](V2KvLedgerLastVerifyScope.md) |  | 
**first_failure** | [**V2KvLedgerFailure**](V2KvLedgerFailure.md) |  | [optional] 

## Example

```python
from quantcdn.models.v2_kv_ledger_last_verify import V2KvLedgerLastVerify

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerLastVerify from a JSON string
v2_kv_ledger_last_verify_instance = V2KvLedgerLastVerify.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerLastVerify.to_json())

# convert the object into a dict
v2_kv_ledger_last_verify_dict = v2_kv_ledger_last_verify_instance.to_dict()
# create an instance of V2KvLedgerLastVerify from a dict
v2_kv_ledger_last_verify_from_dict = V2KvLedgerLastVerify.from_dict(v2_kv_ledger_last_verify_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


