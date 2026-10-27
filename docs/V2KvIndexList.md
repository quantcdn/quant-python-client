# V2KvIndexList

Every declared index of the store (at most 20), in declaration order.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**indexes** | [**List[V2KvIndex]**](V2KvIndex.md) |  | 

## Example

```python
from quantcdn.models.v2_kv_index_list import V2KvIndexList

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvIndexList from a JSON string
v2_kv_index_list_instance = V2KvIndexList.from_json(json)
# print the JSON string representation of the object
print(V2KvIndexList.to_json())

# convert the object into a dict
v2_kv_index_list_dict = v2_kv_index_list_instance.to_dict()
# create an instance of V2KvIndexList from a dict
v2_kv_index_list_from_dict = V2KvIndexList.from_dict(v2_kv_index_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


