# V2KvLedgerErasureShredEntriesPage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**List[V2KvLedgerErasureShredEntry]**](V2KvLedgerErasureShredEntry.md) | Sorted by key. | 
**next_cursor** | **str** | Pass as cursor for the next page. Null on the last page. | 
**has_more** | **bool** |  | 
**page_end** | [**V2KvPageEnd**](V2KvPageEnd.md) |  | 
**shred_id** | **str** |  | 
**entry_count** | **int** |  | 

## Example

```python
from quantcdn.models.v2_kv_ledger_erasure_shred_entries_page import V2KvLedgerErasureShredEntriesPage

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerErasureShredEntriesPage from a JSON string
v2_kv_ledger_erasure_shred_entries_page_instance = V2KvLedgerErasureShredEntriesPage.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerErasureShredEntriesPage.to_json())

# convert the object into a dict
v2_kv_ledger_erasure_shred_entries_page_dict = v2_kv_ledger_erasure_shred_entries_page_instance.to_dict()
# create an instance of V2KvLedgerErasureShredEntriesPage from a dict
v2_kv_ledger_erasure_shred_entries_page_from_dict = V2KvLedgerErasureShredEntriesPage.from_dict(v2_kv_ledger_erasure_shred_entries_page_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


