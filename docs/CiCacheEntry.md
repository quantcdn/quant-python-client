# CiCacheEntry


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**repo_id** | **int** | GitHub repository id. | 
**repo** | **str** | owner/name recorded for repoId, or null when none is recorded. | 
**ref** | **str** | The git ref that saved the entry. A pull request saves to refs/pull/&lt;number&gt;/merge. | 
**key** | **str** | The actions/cache key. | 
**version** | **str** | The cache version (a hash of the paths and compression the job used). | 
**size_bytes** | **int** |  | 
**created_at** | **datetime** | When the entry was saved. Entries expire 14 days after they are saved. | 

## Example

```python
from quantcdn.models.ci_cache_entry import CiCacheEntry

# TODO update the JSON string below
json = "{}"
# create an instance of CiCacheEntry from a JSON string
ci_cache_entry_instance = CiCacheEntry.from_json(json)
# print the JSON string representation of the object
print(CiCacheEntry.to_json())

# convert the object into a dict
ci_cache_entry_dict = ci_cache_entry_instance.to_dict()
# create an instance of CiCacheEntry from a dict
ci_cache_entry_from_dict = CiCacheEntry.from_dict(ci_cache_entry_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


