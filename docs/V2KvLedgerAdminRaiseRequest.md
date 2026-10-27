# V2KvLedgerAdminRaiseRequest

Raise only. Send at least one field. A value lower than the current value is 400 LEDGER_DIRECTION. Any other field is 400 VALIDATION.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**chains** | **int** | Not lower than the current value. | [optional] 
**retention_days** | **int** | Not lower than the current value. The archive worker extends the retention of the existing archive objects. | [optional] 
**lock_mode** | **str** | governance can become compliance, never back. | [optional] 

## Example

```python
from quantcdn.models.v2_kv_ledger_admin_raise_request import V2KvLedgerAdminRaiseRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerAdminRaiseRequest from a JSON string
v2_kv_ledger_admin_raise_request_instance = V2KvLedgerAdminRaiseRequest.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerAdminRaiseRequest.to_json())

# convert the object into a dict
v2_kv_ledger_admin_raise_request_dict = v2_kv_ledger_admin_raise_request_instance.to_dict()
# create an instance of V2KvLedgerAdminRaiseRequest from a dict
v2_kv_ledger_admin_raise_request_from_dict = V2KvLedgerAdminRaiseRequest.from_dict(v2_kv_ledger_admin_raise_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


