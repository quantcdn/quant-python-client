# V2KvLedgerAdminDeclareRequest

A ledger definition. The collection must be empty (no keys, no ledger entries). name, collection, personalFields, subjectField, subjectMode, subjectCase, anchor and writerPolicy can never change. chains, retentionDays and lockMode can only go up (KV_ledgers_update). An unknown field is 400 VALIDATION.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Unique in the store. | 
**collection** | **str** | A collection name, or a pattern where * as a whole segment matches exactly one segment. Must not overlap another ledger. At most 512 UTF-8 bytes; every concrete collection appended to the ledger is at most 512 bytes too. | 
**chains** | **int** | Parallel hash chains (shards) per collection. | 
**retention_days** | **int** | S3 Object Lock retention of the archive, in days. The ledger cannot be dropped before it ends. | 
**lock_mode** | **str** | S3 Object Lock mode of the archive. governance can become compliance later, never back. | 
**personal_fields** | **List[str]** | Top-level value fields that are encrypted per data subject, so a shred (KV_ledgers_shred) can erase them. Needs subjectField (else 400 LEDGER_SUBJECT_REQUIRED). Any field name except at. An index cannot use a personal field (400 INDEX_FIELD_ENCRYPTED). | [optional] 
**subject_field** | **str** | The top-level value field that names the data subject. It is not a personal field. May be set without personal fields; such a ledger is pseudonymised and can be shredded. $subject and $subjectTag are reserved value field names. | [optional] 
**subject_mode** | **str** | How the subject field is stored. pseudonym (the default): a random token, and after a shred nobody can link the remaining entries to the person. clear: the value as written; after a shred the id and the activity stay. Needs subjectField. Cannot change. | [optional] 
**subject_case** | **str** | exact (the default): ids that differ in case are different subjects. fold: case is ignored; use it for email addresses and usernames. Needs subjectField. Cannot change. | [optional] 
**anchor** | [**V2KvLedgerAnchor**](V2KvLedgerAnchor.md) |  | [optional] 
**writer_policy** | [**V2KvLedgerAdminWriterPolicy**](V2KvLedgerAdminWriterPolicy.md) |  | [optional] 

## Example

```python
from quantcdn.models.v2_kv_ledger_admin_declare_request import V2KvLedgerAdminDeclareRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerAdminDeclareRequest from a JSON string
v2_kv_ledger_admin_declare_request_instance = V2KvLedgerAdminDeclareRequest.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerAdminDeclareRequest.to_json())

# convert the object into a dict
v2_kv_ledger_admin_declare_request_dict = v2_kv_ledger_admin_declare_request_instance.to_dict()
# create an instance of V2KvLedgerAdminDeclareRequest from a dict
v2_kv_ledger_admin_declare_request_from_dict = V2KvLedgerAdminDeclareRequest.from_dict(v2_kv_ledger_admin_declare_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


