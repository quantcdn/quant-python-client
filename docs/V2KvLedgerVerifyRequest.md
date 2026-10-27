# V2KvLedgerVerifyRequest

All fields are optional; an empty body verifies the whole ledger. Send the same collection, since and until with cursor to continue.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**collection** | **str** | One concrete collection of the ledger (no *). Absent: every collection. | [optional] 
**since** | [**V2KvLedgerVerifyRequestSince**](V2KvLedgerVerifyRequestSince.md) |  | [optional] 
**until** | [**V2KvLedgerVerifyRequestUntil**](V2KvLedgerVerifyRequestUntil.md) |  | [optional] 
**cursor** | **str** | The next_cursor of the previous call (signed, bound to the range, lasts 24 hours). | [optional] 
**max_entries** | **int** |  | [optional] [default to 10000]

## Example

```python
from quantcdn.models.v2_kv_ledger_verify_request import V2KvLedgerVerifyRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerVerifyRequest from a JSON string
v2_kv_ledger_verify_request_instance = V2KvLedgerVerifyRequest.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerVerifyRequest.to_json())

# convert the object into a dict
v2_kv_ledger_verify_request_dict = v2_kv_ledger_verify_request_instance.to_dict()
# create an instance of V2KvLedgerVerifyRequest from a dict
v2_kv_ledger_verify_request_from_dict = V2KvLedgerVerifyRequest.from_dict(v2_kv_ledger_verify_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


