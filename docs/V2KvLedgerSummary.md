# V2KvLedgerSummary

A short state of the ledger, from the archive worker's last run (at).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**archive_lag_seconds** | **int** |  | 
**broken** | **bool** |  | 
**retain_until** | **datetime** |  | [optional] 
**anchor_failing_since** | **datetime** |  | [optional] 
**last_verify** | [**V2KvLedgerLastVerify**](V2KvLedgerLastVerify.md) |  | [optional] 
**at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.v2_kv_ledger_summary import V2KvLedgerSummary

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerSummary from a JSON string
v2_kv_ledger_summary_instance = V2KvLedgerSummary.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerSummary.to_json())

# convert the object into a dict
v2_kv_ledger_summary_dict = v2_kv_ledger_summary_instance.to_dict()
# create an instance of V2KvLedgerSummary from a dict
v2_kv_ledger_summary_from_dict = V2KvLedgerSummary.from_dict(v2_kv_ledger_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


