# V2KvLedgerAppendRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**collection** | **str** | A concrete collection (no *) that a declared ledger covers. At most 512 UTF-8 bytes. | 
**value** | **Dict[str, object]** | The entry, a JSON object (not a list). At most 350,000 bytes as JSON. Top-level at is reserved (the KV service sets it) and $event is reserved for shred entries; a top-level field whose value is an object with a $enc or $shredded key fails VALIDATION. When the ledger has personal fields, value must hold the subject field (else LEDGER_SUBJECT_REQUIRED). | 
**idempotency_key** | **str** | Optional. A retry with the same key and the same collection and value within 24 hours returns the first receipt with replayed true and appends nothing. The same key with another collection or value fails VALIDATION. A key is unique within the store; derive one key per append. Send it to make a lost-connection 503 retryable. | [optional] 

## Example

```python
from quantcdn.models.v2_kv_ledger_append_request import V2KvLedgerAppendRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerAppendRequest from a JSON string
v2_kv_ledger_append_request_instance = V2KvLedgerAppendRequest.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerAppendRequest.to_json())

# convert the object into a dict
v2_kv_ledger_append_request_dict = v2_kv_ledger_append_request_instance.to_dict()
# create an instance of V2KvLedgerAppendRequest from a dict
v2_kv_ledger_append_request_from_dict = V2KvLedgerAppendRequest.from_dict(v2_kv_ledger_append_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


