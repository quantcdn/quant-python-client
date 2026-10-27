# V2KvIndexLookup

The key that holds the value, with the same body as a key read. A ledger entry adds ledger; its personal fields are [PERSONAL] (listed in personal) unless the caller has ledger_reveal and sends reveal=true.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** |  | 
**value** | **object** | The stored JSON value (any JSON type). | [optional] 
**status** | **str** |  | 
**message** | **str** |  | 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 
**expires_at** | **int** | Epoch seconds. Absent when the key does not expire. | [optional] 
**encrypted** | **bool** |  | [optional] 
**version** | **str** | ULID, new on every write. Absent on ledger entries. | [optional] 
**ledger** | [**V2KvLedgerMeta**](V2KvLedgerMeta.md) |  | [optional] 
**personal** | **List[str]** | Ledger entries only: the personal fields the portal replaced with [PERSONAL] (* &#x3D; the whole value). | [optional] 

## Example

```python
from quantcdn.models.v2_kv_index_lookup import V2KvIndexLookup

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvIndexLookup from a JSON string
v2_kv_index_lookup_instance = V2KvIndexLookup.from_json(json)
# print the JSON string representation of the object
print(V2KvIndexLookup.to_json())

# convert the object into a dict
v2_kv_index_lookup_dict = v2_kv_index_lookup_instance.to_dict()
# create an instance of V2KvIndexLookup from a dict
v2_kv_index_lookup_from_dict = V2KvIndexLookup.from_dict(v2_kv_index_lookup_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


