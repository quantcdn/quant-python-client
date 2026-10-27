# V2KvArchivePurgeCounts


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**versions** | **int** |  | [optional] 
**bytes** | **int** |  | [optional] 
**deleted** | **int** |  | [optional] 
**manifest_pages** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.v2_kv_archive_purge_counts import V2KvArchivePurgeCounts

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvArchivePurgeCounts from a JSON string
v2_kv_archive_purge_counts_instance = V2KvArchivePurgeCounts.from_json(json)
# print the JSON string representation of the object
print(V2KvArchivePurgeCounts.to_json())

# convert the object into a dict
v2_kv_archive_purge_counts_dict = v2_kv_archive_purge_counts_instance.to_dict()
# create an instance of V2KvArchivePurgeCounts from a dict
v2_kv_archive_purge_counts_from_dict = V2KvArchivePurgeCounts.from_dict(v2_kv_archive_purge_counts_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


