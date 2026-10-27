# V2KvLedgerErasureShredPage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**List[V2KvLedgerErasureShredRecord]**](V2KvLedgerErasureShredRecord.md) | Newest first, at most 50. | 
**next_cursor** | **str** | Pass as cursor for the next page. Null on the last page. | 
**has_more** | **bool** |  | 
**page_end** | [**V2KvPageEnd**](V2KvPageEnd.md) |  | 
**ledger** | **str** |  | 

## Example

```python
from quantcdn.models.v2_kv_ledger_erasure_shred_page import V2KvLedgerErasureShredPage

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerErasureShredPage from a JSON string
v2_kv_ledger_erasure_shred_page_instance = V2KvLedgerErasureShredPage.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerErasureShredPage.to_json())

# convert the object into a dict
v2_kv_ledger_erasure_shred_page_dict = v2_kv_ledger_erasure_shred_page_instance.to_dict()
# create an instance of V2KvLedgerErasureShredPage from a dict
v2_kv_ledger_erasure_shred_page_from_dict = V2KvLedgerErasureShredPage.from_dict(v2_kv_ledger_erasure_shred_page_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


