# V2KvKeysPage

One page of keys. A page can hold fewer rows than limit while has_more is true (byte or read budget; see page_end): follow next_cursor while has_more is true.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**List[V2KvEntry]**](V2KvEntry.md) |  | 
**next_cursor** | **str** | Signed; valid 24 hours; bound to the store and the query. Null on the last page. | 
**has_more** | **bool** |  | 
**page_end** | [**V2KvPageEnd**](V2KvPageEnd.md) |  | 
**indexed** | **bool** | Present when collection or index was sent. True for an indexed query on a format 2 store. | [optional] 
**ledger** | **str** | Present on a ledger list (the collection of a ledger): the ledger name. | [optional] 
**hidden_ledger_collections** | **int** | Present when ledger rows were left out because the role does not have ledger_read: the number of ledger collections hidden from this page. | [optional] 
**notice** | **str** | Present with hidden_ledger_collections. | [optional] 

## Example

```python
from quantcdn.models.v2_kv_keys_page import V2KvKeysPage

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvKeysPage from a JSON string
v2_kv_keys_page_instance = V2KvKeysPage.from_json(json)
# print the JSON string representation of the object
print(V2KvKeysPage.to_json())

# convert the object into a dict
v2_kv_keys_page_dict = v2_kv_keys_page_instance.to_dict()
# create an instance of V2KvKeysPage from a dict
v2_kv_keys_page_from_dict = V2KvKeysPage.from_dict(v2_kv_keys_page_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


