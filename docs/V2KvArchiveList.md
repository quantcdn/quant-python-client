# V2KvArchiveList

A page of deleted stores that still hold archive objects (the KV page envelope).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**List[V2KvArchiveStatus]**](V2KvArchiveStatus.md) |  | 
**next_cursor** | **str** | Pass as cursor for the next page; null on the last page. | 
**has_more** | **bool** |  | 
**page_end** | [**V2KvPageEnd**](V2KvPageEnd.md) |  | 

## Example

```python
from quantcdn.models.v2_kv_archive_list import V2KvArchiveList

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvArchiveList from a JSON string
v2_kv_archive_list_instance = V2KvArchiveList.from_json(json)
# print the JSON string representation of the object
print(V2KvArchiveList.to_json())

# convert the object into a dict
v2_kv_archive_list_dict = v2_kv_archive_list_instance.to_dict()
# create an instance of V2KvArchiveList from a dict
v2_kv_archive_list_from_dict = V2KvArchiveList.from_dict(v2_kv_archive_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


