# V2KvLedgerList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ledgers** | [**List[V2KvLedgerListItem]**](V2KvLedgerListItem.md) | Every ledger of the store (all states); empty for a format 1 store. A store has at most 20 ledgers. | 

## Example

```python
from quantcdn.models.v2_kv_ledger_list import V2KvLedgerList

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerList from a JSON string
v2_kv_ledger_list_instance = V2KvLedgerList.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerList.to_json())

# convert the object into a dict
v2_kv_ledger_list_dict = v2_kv_ledger_list_instance.to_dict()
# create an instance of V2KvLedgerList from a dict
v2_kv_ledger_list_from_dict = V2KvLedgerList.from_dict(v2_kv_ledger_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


