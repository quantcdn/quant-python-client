# V2KvLedgerErasureSubjectPreview


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ledger** | **str** |  | 
**subject_ref** | **str** | The reference that the erasure records and receipts use for this subject. The answer never carries the subject id. | 
**ref_key_version** | **int** | The version of the reference key that made subjectRef. | 
**found** | **bool** |  | 
**key_state** | **str** | live: a shred would destroy the key. shredded: the subject is already shredded. | 
**shredded_at** | **datetime** | Present only when keyState is shredded. | [optional] 
**complete** | **bool** | True when every collection was counted to its end. Even then each count means at least N (eventual reads). | 
**entries** | **int** | The total of the collection counts. Present only when keyState is live. | [optional] 
**collections** | [**List[V2KvLedgerErasureSubjectPreviewCollectionsInner]**](V2KvLedgerErasureSubjectPreviewCollectionsInner.md) | Every collection that holds the subject, in name order. | 

## Example

```python
from quantcdn.models.v2_kv_ledger_erasure_subject_preview import V2KvLedgerErasureSubjectPreview

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerErasureSubjectPreview from a JSON string
v2_kv_ledger_erasure_subject_preview_instance = V2KvLedgerErasureSubjectPreview.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerErasureSubjectPreview.to_json())

# convert the object into a dict
v2_kv_ledger_erasure_subject_preview_dict = v2_kv_ledger_erasure_subject_preview_instance.to_dict()
# create an instance of V2KvLedgerErasureSubjectPreview from a dict
v2_kv_ledger_erasure_subject_preview_from_dict = V2KvLedgerErasureSubjectPreview.from_dict(v2_kv_ledger_erasure_subject_preview_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


