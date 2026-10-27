# V2KvLedgerSubjectEntries

One page of the entries of a data subject. It never holds the subjectId, a subjectRef or a subject token outside the entries.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ledger** | **str** |  | 
**subject_state** | **str** |  | 
**entries** | [**List[V2KvEntry]**](V2KvEntry.md) | Empty when subjectState is shredded. | 
**complete** | **bool** | False when the time budget ended first: send the request again with nextToken. | 
**next_token** | **str** | Present when more entries remain. | [optional] 
**shreds** | **List[str]** | Present when subjectState is shredded: the shred ids (KV_ledgers_shreds_receipt). | [optional] 
**earlier_generations_shredded** | **int** | The number of earlier key generations of this subject that were shredded. | 

## Example

```python
from quantcdn.models.v2_kv_ledger_subject_entries import V2KvLedgerSubjectEntries

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerSubjectEntries from a JSON string
v2_kv_ledger_subject_entries_instance = V2KvLedgerSubjectEntries.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerSubjectEntries.to_json())

# convert the object into a dict
v2_kv_ledger_subject_entries_dict = v2_kv_ledger_subject_entries_instance.to_dict()
# create an instance of V2KvLedgerSubjectEntries from a dict
v2_kv_ledger_subject_entries_from_dict = V2KvLedgerSubjectEntries.from_dict(v2_kv_ledger_subject_entries_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


