# V2KvLedgerErasureSubjectPreviewRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subject_id** | [**V2KvLedgerSubjectId**](V2KvLedgerSubjectId.md) |  | 
**ref_key_version** | **int** | Optional: the version of the store&#39;s reference key. Sent to the server unchanged. | [optional] 

## Example

```python
from quantcdn.models.v2_kv_ledger_erasure_subject_preview_request import V2KvLedgerErasureSubjectPreviewRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerErasureSubjectPreviewRequest from a JSON string
v2_kv_ledger_erasure_subject_preview_request_instance = V2KvLedgerErasureSubjectPreviewRequest.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerErasureSubjectPreviewRequest.to_json())

# convert the object into a dict
v2_kv_ledger_erasure_subject_preview_request_dict = v2_kv_ledger_erasure_subject_preview_request_instance.to_dict()
# create an instance of V2KvLedgerErasureSubjectPreviewRequest from a dict
v2_kv_ledger_erasure_subject_preview_request_from_dict = V2KvLedgerErasureSubjectPreviewRequest.from_dict(v2_kv_ledger_erasure_subject_preview_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


