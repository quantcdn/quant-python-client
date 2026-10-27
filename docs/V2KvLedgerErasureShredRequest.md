# V2KvLedgerErasureShredRequest

An unknown field is 400 VALIDATION. reason, authority and requestedBy must not be only spaces; they are stored in the shred entries and the signed receipt.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subject_id** | [**V2KvLedgerSubjectId**](V2KvLedgerSubjectId.md) |  | 
**reason** | **str** | Why the subject is shredded. | 
**authority** | **str** | The legal authority, for example Records authority 2023/00456 class 12. | 
**requested_by** | **str** | Who asked for the shred. | 

## Example

```python
from quantcdn.models.v2_kv_ledger_erasure_shred_request import V2KvLedgerErasureShredRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerErasureShredRequest from a JSON string
v2_kv_ledger_erasure_shred_request_instance = V2KvLedgerErasureShredRequest.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerErasureShredRequest.to_json())

# convert the object into a dict
v2_kv_ledger_erasure_shred_request_dict = v2_kv_ledger_erasure_shred_request_instance.to_dict()
# create an instance of V2KvLedgerErasureShredRequest from a dict
v2_kv_ledger_erasure_shred_request_from_dict = V2KvLedgerErasureShredRequest.from_dict(v2_kv_ledger_erasure_shred_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


