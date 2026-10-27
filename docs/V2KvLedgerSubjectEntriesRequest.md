# V2KvLedgerSubjectEntriesRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subject_id** | [**V2KvLedgerSubjectId**](V2KvLedgerSubjectId.md) |  | 
**collection** | **str** | Read only this collection of the ledger. | [optional] 
**since** | **datetime** | Only entries at or after this time. | [optional] 
**until** | **datetime** | Only entries before this time. | [optional] 
**limit** | **int** | Entries per page, 1 to 1000. The default is 100. | [optional] 
**next_token** | **str** | The nextToken of the previous page. | [optional] 
**personal** | **str** | sealed (the default): personal fields read \&quot;[PERSONAL]\&quot; and the subject field shows the subject token. decrypted: personal fields in clear; needs the ledger_reveal permission and is logged as kv.ledger.reveal. | [optional] 

## Example

```python
from quantcdn.models.v2_kv_ledger_subject_entries_request import V2KvLedgerSubjectEntriesRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerSubjectEntriesRequest from a JSON string
v2_kv_ledger_subject_entries_request_instance = V2KvLedgerSubjectEntriesRequest.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerSubjectEntriesRequest.to_json())

# convert the object into a dict
v2_kv_ledger_subject_entries_request_dict = v2_kv_ledger_subject_entries_request_instance.to_dict()
# create an instance of V2KvLedgerSubjectEntriesRequest from a dict
v2_kv_ledger_subject_entries_request_from_dict = V2KvLedgerSubjectEntriesRequest.from_dict(v2_kv_ledger_subject_entries_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


