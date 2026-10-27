# V2KvLedgerStatus

The chain instances (50 per page), archive lag, digest, anchor and verify state of a ledger.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ledger** | [**V2KvLedger**](V2KvLedger.md) |  | 
**instances** | [**List[V2KvLedgerInstance]**](V2KvLedgerInstance.md) |  | 
**last_digest_at** | **datetime** |  | [optional] 
**retain_until** | **datetime** |  | [optional] 
**mode_refused** | **int** |  | [optional] 
**digest_mode_refused** | **int** |  | [optional] 
**mode_retry_after** | **datetime** |  | [optional] 
**anchor** | [**V2KvLedgerStatusAnchor**](V2KvLedgerStatusAnchor.md) |  | 
**last_verify** | [**V2KvLedgerLastVerify**](V2KvLedgerLastVerify.md) |  | [optional] 
**verify_progress** | **Dict[str, object]** | Present while a scheduled verify runs or is paused between daily runs. | [optional] 
**forked** | **Dict[str, object]** | Present when the store table no longer matches its archive; appends are refused with LEDGER_FORKED. | [optional] 
**next_cursor** | **str** | Pass as cursor for the next page of instances; null on the last page. | 

## Example

```python
from quantcdn.models.v2_kv_ledger_status import V2KvLedgerStatus

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerStatus from a JSON string
v2_kv_ledger_status_instance = V2KvLedgerStatus.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerStatus.to_json())

# convert the object into a dict
v2_kv_ledger_status_dict = v2_kv_ledger_status_instance.to_dict()
# create an instance of V2KvLedgerStatus from a dict
v2_kv_ledger_status_from_dict = V2KvLedgerStatus.from_dict(v2_kv_ledger_status_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


