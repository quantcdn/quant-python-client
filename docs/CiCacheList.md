# CiCacheList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_bytes** | **int** | Size of every entry that matches the filter (partial when totalsComplete is false). | 
**entry_count** | **int** | Number of entries that match the filter (partial when totalsComplete is false). | 
**totals_complete** | **bool** | false when the count stopped at its time limit (about 10 seconds) on a very large cache; totalBytes and entryCount then cover only the part counted. | 
**entries** | [**List[CiCacheEntry]**](CiCacheEntry.md) |  | 
**next_cursor** | **str** | Opaque. Pass as cursor, with the same filter, for the next page; null on the last page. | 

## Example

```python
from quantcdn.models.ci_cache_list import CiCacheList

# TODO update the JSON string below
json = "{}"
# create an instance of CiCacheList from a JSON string
ci_cache_list_instance = CiCacheList.from_json(json)
# print the JSON string representation of the object
print(CiCacheList.to_json())

# convert the object into a dict
ci_cache_list_dict = ci_cache_list_instance.to_dict()
# create an instance of CiCacheList from a dict
ci_cache_list_from_dict = CiCacheList.from_dict(ci_cache_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


