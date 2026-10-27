# V2KvLedgerErasureShredInProgress

The time budget of the call ended. Send the same request again until it answers 200; no entry is written twice.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** |  | 
**ledger** | **str** |  | 
**subject_ref** | **str** | The pseudonym of the subject. | 
**entries** | [**List[V2KvLedgerReceipt]**](V2KvLedgerReceipt.md) | The shred entries recorded so far. The final 200 lists them again. | 

## Example

```python
from quantcdn.models.v2_kv_ledger_erasure_shred_in_progress import V2KvLedgerErasureShredInProgress

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerErasureShredInProgress from a JSON string
v2_kv_ledger_erasure_shred_in_progress_instance = V2KvLedgerErasureShredInProgress.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerErasureShredInProgress.to_json())

# convert the object into a dict
v2_kv_ledger_erasure_shred_in_progress_dict = v2_kv_ledger_erasure_shred_in_progress_instance.to_dict()
# create an instance of V2KvLedgerErasureShredInProgress from a dict
v2_kv_ledger_erasure_shred_in_progress_from_dict = V2KvLedgerErasureShredInProgress.from_dict(v2_kv_ledger_erasure_shred_in_progress_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


