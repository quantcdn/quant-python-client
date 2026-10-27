# V2KvLedgerErasureSubjectPreviewCollectionsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**collection** | **str** |  | 
**entries** | **int** | At least this many entries of the subject (shred entries not counted). | 
**complete** | **bool** | false: the time budget ended before this collection was counted to its end. | 
**first_at** | **datetime** |  | [optional] 
**last_at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.v2_kv_ledger_erasure_subject_preview_collections_inner import V2KvLedgerErasureSubjectPreviewCollectionsInner

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerErasureSubjectPreviewCollectionsInner from a JSON string
v2_kv_ledger_erasure_subject_preview_collections_inner_instance = V2KvLedgerErasureSubjectPreviewCollectionsInner.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerErasureSubjectPreviewCollectionsInner.to_json())

# convert the object into a dict
v2_kv_ledger_erasure_subject_preview_collections_inner_dict = v2_kv_ledger_erasure_subject_preview_collections_inner_instance.to_dict()
# create an instance of V2KvLedgerErasureSubjectPreviewCollectionsInner from a dict
v2_kv_ledger_erasure_subject_preview_collections_inner_from_dict = V2KvLedgerErasureSubjectPreviewCollectionsInner.from_dict(v2_kv_ledger_erasure_subject_preview_collections_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


