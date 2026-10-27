# V2KvLedgerSubjectId

The data subject id (the value of the ledger's subjectField): a string of 1 to 1024 bytes or a safe integer. The server canonicalises it (trim, NFC, the ledger's case rule) and refuses an invalid id with VALIDATION. Error messages never contain the id.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------

## Example

```python
from quantcdn.models.v2_kv_ledger_subject_id import V2KvLedgerSubjectId

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerSubjectId from a JSON string
v2_kv_ledger_subject_id_instance = V2KvLedgerSubjectId.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerSubjectId.to_json())

# convert the object into a dict
v2_kv_ledger_subject_id_dict = v2_kv_ledger_subject_id_instance.to_dict()
# create an instance of V2KvLedgerSubjectId from a dict
v2_kv_ledger_subject_id_from_dict = V2KvLedgerSubjectId.from_dict(v2_kv_ledger_subject_id_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


